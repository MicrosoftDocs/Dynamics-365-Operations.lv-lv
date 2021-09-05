---
title: plānošanas programmas veiktspējas uzlabošana
description: Šajā tēmā ir sniegta informācija par plānošanas programmu un to, kā uzlabot veiktspēju.
author: ChristianRytt
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0a37e3463273d1ffd35b267b36dfbd6fd92bb255
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343481"
---
# <a name="improve-scheduling-engine-performance"></a>plānošanas programmas veiktspējas uzlabošana

[!include [banner](../includes/banner.md)]

Resursu plānošanas programmu izmanto, plānojot maršrutus plānotajiem un nodotajiem ražošanas pasūtījumiem. Programma sākotnēji tika izlaista kā daļa no Dynamics AX 2012, un kopš tās izlaišanas programmai bijušo vairāki uzlabojumi.

[Darbu veikalu plānošanas problēma](https://en.wikipedia.org/wiki/Job_shop_scheduling) ir ārkārtīgi sarežģīta, kombinēta problēma, kur risināšanas laiks eksponenciāli palielinās līdz ar lēmumu variantu skaitu. Nereti klienti iestata ražošanas maršrutus un saistītos datus veidā, kas izraisa plānošanas problēmu, ko nevar atrisināt saprātīgā laikā, pat lietojot vismodernāko aparatūru. Šī tēma palīdzēs jums izprast plānošanas programmu un to, kā noteiktiem iestatījumiem var būt ietekme uz veiktspēju.

Lai uzlabotu plānošanas veiktspēju, vispārējās vadlīnijas iesaka samazināt problēmas sarežģītību, kas programmai ir jārisina. Daži no galvenajiem faktoriem, kas var ietekmēt veiktspēju, ir šādi:

- Maršruti ar daudzām operācijām
- Maršruti ar vienlaicīgām operācijām
- Darbības ar resursu daudzumu, kas lielāks par vienu
- Operācijas ar daudziem piemērojamiem resursiem
- Fiksēto saišu izmantošana
- Ierobežotas noslodzes izmantošana
- Dažādu izmantoto kalendāru skaits
- Darba laika slotu skaits kalendārās dienas ietvaros
- Maršruta kopējais ilgums
- Vairāku plānošanas dzinēju vienlaicīga palaišana

## <a name="overview-of-basic-scheduling-flow"></a>Pamata plānošanas plūsmas pārskats

Lai saprastu, kā attiecīgie iestatījumi var ietekmēt veiktspēju, ir svarīgi zināmā mērā saprast, kā process plūst gan programmā, gan X++ kodā, kas to ietver.

Pasūtījuma plānošanas pamata process sastāv no trim galvenajām darbībām:

- **Datu ielāde** — Šeit X++ datu modeļi tiek pārveidoti par programmas iekšējo datu modeli darbu un ierobežojumu formā.
- **Plānošana** — šis ir galvenais avots plānošanai, kas apstrādā doto modeli un ierobežojumus un ģenerē rezultātu. Šī procesa laikā programma pēc nepieciešamības pieprasīs darba laika informāciju un esošās noslodzes rezervācijas no X++.
- **Saglabāt datus** — programmas rezultāts darba noslodzes rezervācijas slotu formā tiek apstrādāts, izmantojot X++ kodu, lai saglabātu noslodzes rezervācijas un atjauninātu darbu/operāciju/pasūtījumu sākuma un beigu laikus.

## <a name="load-data-into-the-engine"></a>Datu ielāde programmā

Plānošanas programmai ir abstraktāks datu modelis nekā Supply Chain Management datu bāzei, jo tā ir izveidota kā vispārīgā programma, kas var apstrādāt dažādus datu avotus. Maršruta, sekundāro operāciju un izpildes laika jēdzieni ir „jātulko” vispārīgajā darba un ierobežojumu modelī, ko parāda programma. Modeļa izveides loģikā ir ievērojama daļā biznesa loģikas, un tā atšķiras atkarībā no avota datiem. Atbildīgā X++ klase ir `WrkCtrScheduler`, un tai ir atvasinātās klases plānotajiem ražošanas pasūtījumiem, nodotajiem ražošanas pasūtījumiem un projekta prognozēm.

Piemēram, apsveriet maršrutu, kas parādīts tālāk redzamajā tabulā un attēlā, kas izskatās samērā vienkāršs.

| Oper. Nr.p.k. | Prioritāte | Uzstādīšanas laiks | Izpildes laiks | Gaidīšanas laiks pēc | Resursu daudzums | Nākamā |
| --- | --- | --- | --- | --- | --- | --- |
| 10. | Primārais | 1.00 | 2.00 | | 1 | 20 |
| 10. | Sekundārs&nbsp;1 | | | | 1 | 20 |
| 20 | Primārais | | 3.00 | 1.00 | 3 | 0 |

![Maršruta parauga diagramma.](media/scheduling-engine-route.png "Maršruta parauga diagramma")

Sūtot to uz programmu, tā tiek sadalīta astoņos darbos, kā parādīts tālāk redzamajā ilustrācijā (atlasiet attēlu, lai to palielinātu).

[![Plānošanas programmas darbi](media/scheduling-engine-jobs.png "Plānošanas programmas darbi.")](media/scheduling-engine-jobs-large.png)

Standarta saite starp diviem darbiem ir `FinishStart`, kas nozīmē, ka viena darba beigu laikam jābūt pirms cita darba sākuma laika. Tā kā iestatījumus ir jāpilda tam pašam resursam, kas vēlāk veiks procesu, starp tiem pastāv `OnSameResource` ierobežojumi. Starp darbiem primārajai un sekundārajai operācijai 10 pastāv `StartStart` un `FinishFinish` saites, kas nozīmē, ka abiem darbiem ir jāsākas un jābeidzas vienlaicīgi, un pastāv `NotOnSameResource` ierobežojumi, kas nepieļaus vienu resursu primārajam un sekundārajam darbam.

Operācijai 20, kur resursu daudzums ir iestatīts kā 3, procesa darbs ir sadalīts trīs atšķirīgos darbos, kur visiem darbiem ir jātiek izpildītiem vienā un tajā pašā laikā.
Šajā gadījumā maršruta grupa ir iestatīta tā, lai nerezervētu gaidīšanas laiku pēc, tāpēc rindai pēc tam ir tikai viens darbs.

Plānošanas programma izprot tikai darbu jēdzienus un tai nav informācijas par operācijām. Tas nozīmē, ka, veicot operāciju plānošanu, arī operācijas tiek sadalītas darbos, kaut gan tie netiks saglabātas datu bāzē.

Katram darbam mēs noteiksim arī, kādas ir darba noslodzes prasības (nepieciešamo sekunžu skaits). Atkarībā no tā, kā definētas resursu prasības, mēs varam arī katram darbam nosūtīt sarakstu ar visiem potenciālajiem izmantojamajiem resursiem, kas būtu nepieciešami darba palaišanai, un to, kādas noslodzes prasības ir konkrētajam resursam. Kaut gan izmantojamo resursu saraksts tiek nosūtīts, veidojot modeli, programmai tik un tā ir jānodrošina, ka resursu piešķire ir faktiski atbilstoša visam darba ilgumam.

## <a name="scheduling-engine-internals"></a>Plānošanas programmas iekšējie parametri

### <a name="scheduling-engine-interface"></a>Plānošanas programmas interfeiss

Lai gūtu priekšstatu par to, kā programma darbojas iekšēji, vislabāk ir apskatīt funkcionalitāti, ko tā parāda ārēji. X++ galvenais interfeiss ir `WrkCtrSchedulerEngineInterface`. Tam ir metodes, kas aprakstītas tālākajās apakšsadaļās.

#### <a name="general-engine"></a>Vispārēja programma

| **Metode** | **Nolūks** |
| --- | --- |
| `run` | Ieplāno visus ielādētos darbus un atgriež kļūdas kodu. |
| `getJobSchedulingSequenceResult` | Iegūst plānošanas rezultātu un pirmo kļūdas darbu secībai, ko identificējis noteikts darbs. |
| `validateJobCapacityReservations` | Pārbauda noslodzes rezervācijas visiem darbiem, ko programma saglabājusi. |
| `setReservationsTimeStamp` | Nosūta laikspiedolu programmai, kuras kešatmiņā iestatītas visas jaunās noslodzes rezervācijas ieplānotajiem darbiem. |
| `addPropertyToGroupAggregation` | Pievieno rekvizītu prefiksu rekvizītu kopai, kas tiek izmantota, kad noslodze tiek apkopota. |
| `addResource` | Pievieno resursu plānošanas programmas resursu kopai. |
| `addResourceGroup` | Pievieno resursu grupu plānošanas programmas resursu grupas kopai. |
| `addResourceGroupMembership` | Pievieno resursu kā resursu grupas elementu. |
| `addOptimizationGoal` | Pievieno plānošanas optimizācijas mērķi (ilgumu vai prioritāti). |

#### <a name="individual-jobs"></a>Atsevišķi darbi

| **Metode** | **Nolūks** |
| --- | --- |
| `addJobInfo` | Pievieno darba informācijas ierakstu, kas informē programmu par darbu, kas jāieplāno. |
| `addConstraintJobEndsAt` | Pievieno ierobežojumu, ka darbs būtu jāpabeidz norādītajā datumā un laikā. |
| `addConstraintJobStartsAt` | Pievieno ierobežojumu, ka darbs būtu jāsāk norādītajā datumā un laikā. |
| `addConstraintMaxJobDays` | Definē ierobežojumu, ka darba process var tikt izdalīts norādīta maksimālā dienu skaita ietvaros. |
| `addConstraintResourceRequirement` | Pievieno ierobežojumu, ka darba izpildē ir jāieplāno noteikta resursa izmantošana. |
| `addJobBindPriority` | Pievieno ar darbu saistītu prioritāti (darba, ierobežojuma līmeņa) pārim. Augstākas prioritātes vērtība nozīmē, ka darba mainīgie tiks saistīti agrāk. Darbs tiks apstrādāts pirms darbiem ar zemāku prioritātes vērtību tajā pašā secībā. |
| `addJobCapacity` | Pievieno darba noslodzes informāciju (piemēram, darbam nepieciešamo izpildlaiku) neatkarīgi no tā, kāds resurss tiek izmantos darba izpildē. |
| `addJobResourceCapacity` | Pievieno resursu resursu kopai, ko var izmantot, lai veiktu darbu, un nosaka noslodzi, kas nepieciešama, lai veiktu darbu, izmantojot šo resursu. |
| `addJobGoal` | Pievieno darba mērķa informāciju noteiktam ierobežojuma līmenim (agrākais beigu laiks vai vēlākais sākuma laiks). |
| `addJobResourcePriority` | Pievieno prioritāti, ko izmantot, kad ieplānota darba veikšana, izmantojot konkrētu resursu. |
| `addJobResourceRuntime` | Norāda darba laiku, kas ir atkarīgs no resursa, uz kuru pamatojoties tiks ieplānots darbs. |
| `addJobRuntime` | Norāda darba laiku, kas nav atkarīgs no resursa, uz kura pamata tiks ieplānots darbs. |
| `scheduleJobOnResourceGroup` | Atzīmē darbu plānošanai resursu grupas līmenī. |
| `setJobResourcePreemptionAllowed` | Iestata, vai darbam uz resursa pamata ir atļautas pirmtiesības (ja programmai ir atļauts ieplānot darbu attālos noslodzes slotos). |
| `setRequiredNumberOfResources` | Iestata resursu skaitu, kas nepieciešami, lai ieplānotu darbu (tikai operāciju plānošanai). |

#### <a name="constraints-between-jobs"></a>Ierobežojumi starp darbiem

| **Metode** | **Nolūks** |
| --- | --- |
| `addJobLink` | Pievieno saiti (piemēram, beigas\>sākums) starp diviem darbiem. |
| `addConstraintEndsDelayed` | Definē ierobežojumu, ka darbu nevar beigt pirms citu darbu beigšanas, ieskaitot zināmu aizkavēšanās laiku. |
| `addConstraintJobListWorkingTimeIntersect` | Pievieno ierobežojumu, ka darbiem paredzētajiem noslodzes slotiem jābūt pārklātos darba laikos tiem diviem resursiem, kas izmantoti šajos darbos. |
| `addConstraintJobOverlap` | Pievieno ierobežojumu, kas nosaka, kā darbi tiek kārtoti, kad norādīts krājuma daudzums var tikt pārvietots starp diviem resursiem, kamēr pirmā resursa apstrāde vēl nav beigusies, lai varētu sākt otrā resursa apstrādi. |
| `addConstraintNotOnSameResource` | Pievieno ierobežojumu, ka divus darbus nedrīkst ieplānot uz viena un tā paša resursa pamata. |
| `addConstraintOnSameResource` | Pievieno ierobežojumu, ka diviem darbiem jāizmanto viens un tas pats resurss. |
| `addJobSameReservations` | Pievieno ierobežojumu, ka darbam rezultātā jābūt ar noslodzes rezervācijām tajos pašos laika slotos kā primārajam darbam. |
| `setPrimaryParallelJob` | Pievieno informāciju par to, kurš darbs ir primārais darbs paralēlu darbu kopā. |

### <a name="solver"></a>Risinātājs

Pati programma būtībā ir specializēts ierobežojumu risinātājs ar pievienotu pielāgotu heiristiku. Risinātāja pamatā ir divi galvenie elementi: mainīgie un ierobežojumi.

#### <a name="variable"></a>Mainīgā

Mainīgais attēlo iespējamo vērtību domēnu. Plānošanas programmai ir divi mainīgo tipi:

- **DateTime mainīgais** — tam ir domēns visiem datumiem un laikiem, un domēnu var ierobežot, pārvietojot apakšējo un augšējo mainīgā laika robežu tuvāk vienu otrai.
- **Resursu mainīgais** — tam ir piemērojamo resursu domēns, un domēnu var ierobežot, izslēdzot resursus no saraksta.

#### <a name="constraint"></a>Ierobežojums

Ierobežojums attiecas uz mainīgajiem, ierobežojot to domēnus, bet tas ir atkarīgs arī no mainīgajiem, tāpēc tas tiek aktivizēts, kad mainās mainīgie. „Ierobežojuma izplatīšanas” process ir, kad ierobežojums veic savu galveno funkciju un sniedz atskaites galvenajai loģikai, ja tas ir veiksmīgs.

Mainīgais ir uzskatāms par saistītu, kad to nevar vairāk ierobežot, kas DateTime mainīgajam nozīmē, ka augšējā un apakšējā robeža ir vienāda un resursa mainīgajam, ka tam ir tikai viens piemērojams resurss. Kad visi mainīgie ir saistīti, tiek atrasts risinājums.

### <a name="constraint-levels"></a>Ierobežojumu līmeņi

Kad plānošana tiek izpildīta kā daļa no materiālu vajadzību plānošanas (MRP) segšanas posma, pasūtījumi tiks plānoti atpakaļejošā secībā no pieprasījuma datuma. Tomēr, ja nav iespējams atrast grafiku, kas sākas šodien vai vēlāk, un beidzas pirms pieprasījuma datuma, tad plānošanas virziens mainīsies uz priekšu no šodienas.

Šī galvenā biznesa kārtula tiek apstrādāta, grupējot ierobežojumus līmeņos. Ja, izmantojot augstākā līmeņa ierobežojumus, netiek atrasts risinājums, tad visi šī līmeņa ierobežojumi tiek atmesti, un tiek izmēģināts zemāks līmenis. Praksē tas nozīmē, ka atpakaļejošas plānošanas gadījumā modelī būs 1. līmenis ar darba mērķiem, ar vēlāko sākuma laiku, kam piešķirts maksimālais beigu laika ierobežojums (pieprasījuma datums), un 0. līmenis ar darba mērķiem ar agrāko, kam piešķirts minimālais sākuma laika ierobežojums no šodienas.

### <a name="algorithm"></a>Algoritms

Galvenie programmas algoritma soļi ir šādi:

1. Atrast sērijas (darbu ķēdes), ko var atrisināt atsevišķi.
1. Mēģināt atrast sākotnējo sērijas risinājumu augstākajam ierobežojuma līmenim.
    1. Kārtot darbus secībā, pamatojoties uz darba mērķi un prioritātēm, lai varētu atrast sākšanas darbu.
    1. Atkārtot darbus šādā secībā:
        1. Atrast visus ierobežojumus, kas ir jāizplata un jāpalaiž izplatīšana.
        1. Ja ir saistīti visi darba mainīgie, tad šim darbam ir atrasts risinājums.
        1. Ja kādu no mainīgajiem nevar saistīt, nepārkāpjot ierobežojumus, atritiniet mainīgo saistījumu, izmēģiniet citu vērtību domēnā (resursa mainīgajam) un atkārtoti palaidiet ierobežojumu izplatīšanu.
1. Ja risinājums netika atrasts, tiks noņemti visi pašreizējā ierobežojuma līmeņa ierobežojumi, pazemināts ierobežojuma līmenis (ja ir pieejami zemāki līmeņi) un risinājuma meklēšana tiks veikta atkārtoti ar jauno ierobežojuma kopu.
1. Ja ir atrasts izpildāms risinājums, tiek sākta optimizācijas fāze, kas mēģinās atrast labāku risinājumu, līdz tiks sasniegts optimizācijas taimauts vai visas resursu kombinācijas būs izsmeltas.

Ierobežojumu risinātājs neapzinās plānošanas algoritma specifiku. „Maģija” norisinās dažādo ierobežojumu definīcijās un kombinācijās.

### <a name="determining-working-times"></a>Darba laiku noteikšana

Liela daļa no (iekšējiem) ierobežojumiem programmā kontrolē resursa darba laiku un noslodzi. Būtībā uzdevums ir šķērsot resursa darba laika slotus no noteikta punkta noteiktā virzienā, un atrast pietiekami ilgu intervālu, kurā var ietilpt darbam nepieciešamā noslodze (laiks).

Lai to paveiktu, programmai ir jāzina resursa darba laiki. Pretēji galvenā modeļa datiem, darba laiki tiek *atlikti ielādēti*, kas nozīmē, ka tie tiek ielādēti programmā pēc nepieciešamības. Pamatojums šai pieejai ir tāds, ka bieži vien Supply Chain Management kalendārā darba laiki atrodas ļoti ilga laika perioda ietvaros, un parasti pastāv daudz kalendāru, tāpēc datu apjoms būtu samērā liels iepriekšējas ielādes veikšanai.

Programma pieprasa kalendāra informāciju pa daļām, izsaucot X++ klases metodi `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Pieprasījums ir paredzēts noteiktam kalendāra ID noteiktā laika intervālā. Atkarībā no servera kešatmiņas stāvokļa Supply Chain Management, katrs no šiem pieprasījumiem varētu rezultēties ar vairākiem datu bāzes izsaukumiem, kas aizņem ilgu laiku (salīdzinot ar tīro skaitļošanas laiku). Turklāt, ja kalendārā ir iekļautas ļoti detalizētas darba laika definīcijas ar vairākiem darba laika intervāliem dienā, tas palielina ielādes laiku.

Kad darba laika dati ir ielādēti plānošanas programmā, tas tiek saglabāts tās iekšējā kešatmiņā noteiktajam kalendāram, kas nozīmē, ka, ja kādi citi darbi vai resursi izmanto to pašu kalendāru, tad nākamās uzmeklēšanas no atmiņas varēs veikt ātri. Viens kopīgs sliktas veiktspējas cēlonis ir, ja katram resursam tiek izmantots atsevišķs kalendāra ID, jo pēc tam dati ir jāpieprasa katram kalendāram, kaut gan kalendāru saturs var būt vienāds.

### <a name="finite-capacity"></a>Ierobežota noslodze

Izmantojot ierobežoto noslodzi, darba laika sloti kalendārā tiek sadalīti un samazināti, pamatojoties uz esošajām noslodzes rezervācijām. Šīs rezervācijas tiek paņemtas arī, izmantojot to pašu `WrkCtrSchedulingInteropDataProvider` klasi, ko izmanto kalendāri, bet izmantojiet metodi `getCapacityReservations`. Plānojot vispārējās plānošanas laikā, rezervācijas noteiktam vispārējam plānam tiek ņemtas vērā un, ja tās ir iespējotas lapā **Vispārējās plānošanas parametri**, tiek iekļautas arī rezervācijas no apstiprinātajiem ražošanas pasūtījumiem. Līdzīgi, plānojot ražošanas pasūtījumu, pastāv arī opcija iekļaut rezervācijas no esošajiem plānotajiem pasūtījumiem, lai gan šī pieeja nav tik izplatīta kā rīkošanās otrādi.

Ierobežotas noslodzes izmantošana izraisīs plānošanas paildzināšanos vairāku iemeslu dēļ:

- Noslodzes informācijas paņemšana no datu bāzes ir lēna operācija, un noslodzes informācijas servera puses kešdarbe parasti nav tik laba kā darba laikos, jo tie netiek koplietoti starp resursiem kā, piemēram, parasti tiek koplietoti kalendāri.
- Darba laika slotu skaits, kas jāšķērso, palielinās sadalījumu dēļ, un parasti slotiem jātiek pārbaudītiem ilgāku laika posmu, līdz tiek atrasts risinājums.
- Pēc tam, kad plānošana ir pabeigta, ir jāveic konfliktējošo rezervāciju pārbaude (detalizētu informāciju skatiet sadaļā „Plānošanas programmu vienlaicīga palaišana”).

### <a name="examining-the-resource-combinations"></a>Resursu kombināciju izpēte

Ja darba secība ietver tikai standarta `FinishStart` saites, tas ir, tā veido vienkāršu ķēdi bez zariem, optimālais rezultāts (redzams no viena pasūtījuma, nevis viscaur pasūtījumiem) var tikt sasniegts, atrodot labāko risinājumu pirmajam darbam un pēc tam meklējot labāko risinājumu nākamajam darbam. Labākais risinājums darbam nozīmē, ka tiek atrasts resurss, kas var iegūt darba mērķim tuvākā darba sākuma un beigu datumu (turpmākajā plānošanā tas nozīmē iegūt darba beigu datumu pēc iespējas ātrāk), joprojām ievērojot ierobežojumus.

Ja pastāv paralēli darbi, risinājuma atrašana var ietvert dažādu resursu kombināciju izpēti. Iespējamo resursu kombināciju skaits ir piemērojamu resursu skaita reizinājums, ko iespējams izmantot saistītajiem paralēlajiem darbiem. Jo īpaši, plānojot pasūtījumu atpakaļejošā veidā no pieprasījuma datuma, tas var aizņemt diezgan ilgu laiku, lai loģika saprastu, ka nepastāv problēmas risinājums, kas ietilpinās paralēlus darbus pirms šodienas datuma, tā kā tai būs jāpārbauda visas kombinācijas, jo varētu būt daži resursi, kam ir augstāka efektivitāte vai cits kalendārs, kas varētu dot rezultātu. Tas nozīmē, ka, ja nav iestatīts taimauta ierobežojums, tā darbosies ilgu laiku pirms virziena maiņas uz priekšu.

Šī kombinētā loģika nozīmē arī to, ka, papildu piemērotu resursu pievienošana var izraisīt programmas palēnināšanos. Ja veiktspējas problēmas rodas, veicot paralēlas operācijas un plānojot ar neierobežotu noslodzi, to daļēji var labot, liekot maršruta projektētāju pieņemt lēmumu par to, kurš resurss jāizmanto, un pēc tam tieši piešķirt resursu operācijai (jo vairumā gadījumu programma vienmēr norādīs vienu un to pašu resursu, tāpēc gala rezultāts būs tāds pats).

### <a name="hard-links"></a>Fiksētās saites

Fiksēta saites veida iestatīšana starp diviem darbiem nodrošina, ka nav laika intervālu starp viena darba beigām un nākamā darba sākumu. Tas var būt ļoti noderīgi situācijās, kā, piemēram, kad metāls tiek karsēts viena darba ietvaros un pēc tam apstrādāts nākamajā darbā, kad nav vēlama metāla atdzišana starpposmā.

Ar standarta nefiksētajām saitēm un plānošanu uz priekšu, ja maršruts veido vienkāršu ķēdi bez zariem, rezultātu var sasniegt, atrodot risinājumu pirmajam darbam, kas ievēro tā ierobežojumus, un tad virzīties cauri ķēdei, izplatot beigu laiku no iepriekšējā darba uz nākamo darbu. Ja pašreizējais darbs nevar atrast nevienu noslodzi, tā sākuma laiks tiks pārvietots tālāk, neietekmējot iepriekšējos darbus, kas potenciāli radītu atstarpes starp darbiem. Tomēr ar fiksētajām saitēm (jo īpaši saistībā ar ierobežoto noslodzi) tādā pašā situācijā fakts, ka viens darbs tālāk ķēdē nevar atrast noslodzi, nozīmēs, ka visi iepriekšējie ieplānotie darbi būs „jāvelk” pa vienam, un tādējādi jāpārplāno vairākas reizes. Jo īpaši tādās situācijās, kurās ir liela vairāku resursu noslodze, fiksētās saites var izraisīt ķēdes reakciju, kur darbi ietekmēs cits citu un tie būs jāatkārto vairākas reizes, pirms rezultāts tiks stabilizēts iespējama grafika formā.

## <a name="running-scheduling-engines-in-parallel"></a>Plānošanas programmu vienlaicīga palaišana

Veicot plānošanu kā daļu no vispārējās plānošanas izpildes, kur tiek izmantoti palīgi, katrs no vispārējā plānošanas palīga pavedieniem var saņemt arī ražošanas pasūtījuma plānošanas uzdevumus. Tas nozīmē, ka vienlaicīgi var darboties vairākas plānošanas programmas. Kaut gan vairākpavedienu struktūra kopumā ir ļoti nozīmīga veiktspējas priekšrocība, attiecībā uz plānošanu pastāv arī daži funkcionālie trūkumi.

MRP visi norādītā materiālu komplekta (MK) līmeņa ražošanas pasūtījumi tiek plānoti pieprasījuma datumu secībā, tas nozīmē, ka pasūtījumi ar agrāko pieprasījuma datumu ir jāieplāno vispirms un tādējādi tiem ir vislielākā iespēja saņemt pieejamo resursu noslodzi. Tomēr, vairākām programmām veicot izvēli no neieplānoto pasūtījumu saraksta, secība vairs netiek nodrošināta, jo viens var tikt paveikts ātrāk nekā cits.

Turklāt, plānojot ierobežotas noslodzes lietošanu, kad vairākas programmas instances mēģina ieplānot pasūtījumus, kas potenciāli izmanto vienus un tos pašus resursus tajā pašā laika intervālā, var rasties sacensības nosacījums. Šādu sacensības nosacījumu skaits tiek saglabāts laukā **Plānošanas konflikti** vispārējā plānu vēstures lapā. Konfliktu risināšanas loģika ir šāda:

- Ieplānojiet pasūtījumu (bez bloķēšanas) un iegūstiet noslodzes rezervācijas.
- Paņemiet slēdzeni.
- Pārbaudiet, vai ieplānotajiem resursiem laika intervālā pastāv jaunākas noslodzes rezervācijas.
  - Ja nē, ierakstiet noslodzi un noņemiet bloķēšanu.
  - Ja atbilde ir Jā, noņemiet bloķēšanu un pārplānojiet pasūtījumu no sākuma.

Tātad, plānojot ar vairākiem programmas instancēm, rezultāts nav pilnībā noteikts, jo tas būs atkarīgs no katra pavediena precīzā laika.

## <a name="operation-scheduling-performance"></a>Operāciju plānošanas veiktspēja

Lai gan operāciju plānošana ir zināma arī kā rupja griezuma noslodzes plānošana, kas redzams no programmas skatpunkta, tā var būt grūtāk risināma problēma, ja tiek izmantota ierobežota noslodze, jo ir nepieciešams vairāk datu, lai noteiktu iespējamību.

Resursu grupas noslodze ir atkarīga no tā, kuri un cik daudzi resursi ir resursu grupas dalībnieki. Resursu grupai pašai par sevi nav noslodzes&mdash;, tikai, ja resursi ir grupas dalībnieki, tai būs noslodze. Tā kā dalība resursu grupā var laika gaitā mainīties, noslodze ir jānovērtē ik dienu.

Operāciju plānošanā resursu grupas kalendārs tiek izmantots, lai noteiktu katras operācijas sākuma un beigu laikus. Tas nozīmē, ka resursu grupas kalendārs nosaka limitu, cik laika var ieplānot vienai operācijai vienā dienā vienā resursu grupā. Pretēji noteikta resursa kalendāram, resursu grupas efektivitātes dati kalendārā tiek ignorēti, jo tie vienkārši apzīmē darba laiku un nevis faktisko noslodzi.

Piemēram, ja darba laiks resursu grupai kādā noteiktā datumā ir no 8:00 līdz 16:00, viena operācija nevar likt lielāku slodzi uz resursu grupu, kā to, ko var ietilpināt 8 stundu intervālā, neatkarīgi no tā, cik liela noslodze resursu grupai kopā ir pieejama šajā dienā. Tomēr pieejamā noslodze var vairāk ierobežot noslodzi.

Noslodze no darba plānošanas uz visiem resursiem, kas iekļauti resursu grupā attiecīgajā dienā, tiek ņemta vērā, kad tiek aprēķināta pieejamā resursu grupas noslodze tajā pašā dienā. Katram datumam aprēķins ir šāds:

*Pieejamo resursu grupas noslodze = resursu noslodze grupā, pamatojoties uz to kalendāru &ndash; Darba ieplānoto noslodzi resursiem grupā &ndash; Operāciju ieplānoto noslodzi resursiem grupā &ndash; Operāciju ieplānoto noslodzi resursiem grupā*

Cilnē **Resursu vajadzības**, kas atrodas maršruta operācijā, resursu vajadzības var norādīt, izmantojot noteiktu resursu (tādā gadījumā operācija tiks ieplānota, izmantojot šo resursu), resursu grupai, resursu veidam vai vienai vai vairākām iespējām, prasmei, kursam vai sertifikātam. Lai gan visu šo opciju izmantošana sniedz lielu elastību maršruta dizainā, tas arī sarežģī programmas plānošanu, jo noslodze jāuzskaita katram „Rekvizītam” (abstrakts nosaukums, kas tiek izmantots programmā, lai aprakstītu iespējas, prasmes utt.).

Resursu grupas noslodze iespējai ir noslodzes summa visiem resursu grupas resursiem, kam ir attiecīgā noslodze. Ja resursam grupā ir iespēja, tad tā tiks ņemta vērā neatkarīgi no tā, kāds ir nepieciešamās noslodzes līmenis.

Operāciju plānošanā pieejamā noslodze noteiktai resursu grupas iespējai tiks samazināta, kad tā tiks ielādēta ar operāciju, kas pieprasa attiecīgo iespēju. Ja operācijai ir nepieciešama vairāk nekā viena iespēja, noslodze tiks samazināta visām nepieciešamajām iespējām.

Katram datumam nepieciešamais aprēķins ir šāds:

*Pieejamā iespējas noslodze = iespējas noslodze &ndash; Darba ieplānotā noslodze resursiem ar specifiskām iespējām, kas iekļautas resursu grupā &ndash; Operāciju ieplānotā noslodze resursiem ar specifiskām iespējām, kas iekļautas resursu grupā &ndash; Operāciju ieplānotā noslodze pašā resursu grupā, kurai nepieciešama konkrētā iespēja*

Tas nozīmē, ka, ja ir noslodze uz noteiktu resursu, noslodze tiek ņemta vērā, aprēķinot resursu grupai pieejamo noslodzi vienai iespējai, jo noslodze uz noteiktu resursu samazina tā ieguldījumu resursu grupas noslodzē, lai varētu izmantot iespēju, neatkarīgi no tā, vai noslodze uz konkrēto resursu paredzēta konkrētajai iespējai. Ja ir noslodze resursu grupas līmenī, tas tiek ņemts vērā, aprēķinot resursu grupas pieejamo noslodzi vienai iespējai tikai tad, ja noslodze ir no operācijas, kurai nepieciešama noteiktā iespēja.

Iepriekšminētā loģika ir komplicēta, jo tā ir vienāda katram „rekvizīta” veidam, tāpēc, lai izmantotu operāciju plānošanu ar ierobežotu noslodzi, nepieciešams ielādēt ievērojamu datu apjomu.

## <a name="viewing-scheduling-engine-input-and-output"></a>Plānošanas programmas ievades un izvades skatīšana

Lai iegūtu noteiktu, detalizētu informāciju par plānošanas procesa ievadi un izvadi, iespējojiet reģistrēšanu, dodoties uz **Organizācijas administrēšana \> Iestatījumi \> Plānošana \> Plānošanas izsekošanas kontrolpults**.

Šajā lapā vispirms atlasiet **Iespējot reģistrēšanu** darbību rūtī. Tad palaidiet ražošanas pasūtījuma plānošanu. Kad tā pabeigta, atgriezieties lapā **Plānošanas izsekošanas kontrolpults** un darbības rūtī atlasiet **Atspējot reģistrēšanu**. Atsvaidziniet lapu, un režģī tiks parādīta jauna rinda. Atlasiet jauno rindu un darbības rūtī atlasiet **Lejupielādēt**. Šī darbība sniegs jums. zip formātā saspiestu mapi, kurā ietverti šādi faili:

- **Log.txt** — šis ir žurnāla fails, kas apraksta darbības, kuras secīgi veic programma. Tas ir ļoti komplicēts, un var būt mazliet apgrūtinošs, bet, ja tas tiek izmantots kā daļa no eksperimentēšanas ar maršruta iestatīšanu, lai atrisinātu veiktspējas problēmas, pirmā lieta, ko meklēt, ir laika atšķirība starp pirmo un pēdējo rindu, jo tas dos jums precīzu laiku, kuru patērējis plānotājs.
- **XmlModel.xml** — tas satur modeli, kas ir būvēts X++ un uz kura pamata darbojas programma. Failā izmantotais `JobId` korelē ar `RecId` no avota tabulas, kas satur darbus (`ReqRouteJob` vai `ProdRouteJob`). Tipiskā lieta, ko meklēt šajā failā, ir tas, ka datumi, kas doti `ConstraintJobStartsAt` un `ConstraintJobEndsAt` atbilst paredzētajam, ka `JobGoal` rekvizīts ir iestatīts pareizi un ka darbi ir saistīti viens ar otru, izmantojot `JobLink` ierobežojumus.
- **XmlSlots.xml** — tas ietver visus darba laikus un noslodzes rezervācijas, ko programma ir pieprasījusi. Kalendāra darba laiki un rezervācijas programma pieprasīs tikai tiem laika posmiem, kuros tā mēģina izvietot darbus (un papildu buferi), tāpēc, ja fails ietver laikus ļoti tālu nākotnē, tas var norādīt uz problēmu ar iestatījumiem. `ResourceProperty` mezgli katram resursam parādīs, ar kuru resursu grupu un iespējām tas ir saistīts un kuros periodos.
- **Result.xml** — tas ietver plānošanas izpildes rezultātus.

Ņemiet vērā, ka izsekošanas funkcionalitāte var pievienot būtisku veiktspējas pārtēriņu, tāpēc izmantojiet to tikai, lai izpētītu noteiktu pasūtījumu plānošanu kontrolētā veidā. Ja vispārējās plānošanas izpildes laikā tas ir ieslēgts, tas ātri sasniegs savu lieluma ierobežojumu un apstāsies.

## <a name="troubleshooting-performance"></a>Problēmu novēršanas veiktspēja

Kā tas ir saprotams no visām iepriekšējām sadaļām, plānošanas programmas iestatīšanai un izmantošanai piemīt dažas nepilnības, kas var izraisīt veiktspējas problēmas. Problēmu novēršanai varat izmantot šādu kontrolsarakstu. Ir svarīgi apskatīt visus punktus, jo problēmas visbiežāk iztaisa vairāku faktoru kombinācija.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Tiek veikta plānošana kā daļa no MRP, ja tā nav nepieciešams

Kaut arī maršruti tiek izmantoti ražošanas kontroles nolūkiem, piemēram, izmaksu aprēķināšanai un pārskatiem, iespējams, MRP laikā nav nepieciešams tos ņemt vērā. Dažos gadījumos, standarta ražošanas izpildes laika norādīšana krājumam būs pietiekama plānošanai. Lai izslēgtu maršruta plānošanu, iestatiet noslodzes periodu uz nulli. Ja plānošana ir jāveic, noslodzes laika periods ir rūpīgi jāiestata, jo, iespējams, nav nepieciešams ņemt vērā maršrutus pilna MRP vajadzības perioda robežās.

Ņemiet vērā, ka, ja pasūtījums nav ieplānots MRP laikā, tā vietā tas ir jāplāno, kad plānotais pasūtījums ir apstiprināts. Tas nozīmē, ka apstiprināšanas process būs ilgāks, tāpēc atkarībā no tā, cik no ieteiktajiem plānotajiem pasūtījumiem tiek apstiprināti, veiktspējas pieaugums MRP laikā var tikt zaudēts pie apstiprināšanas.

### <a name="route-with-unnecessary-operations"></a>Maršruts ar nevajadzīgām operācijām

Veidojot maršrutu, ir vilinoši mēģināt modelēt reālo pasauli tieši — ar visām ražošanas darbībām. Lai gan dažos gadījumos tas var būt noderīgi, tas nav labi veiktspējai, jo modelis, uz kura pamata programmai ir jāstrādā, palielinās (attiecībā gan uz darbu, gan ierobežojumiem), un vairāk SQL priekšrakstu tiks izpildīti, lai ievietotu un atjauninātu darbus un noslodzes rezervācijas. Ir arī pakārtotās sekas — laika gaitā par darbu norisi ir jāziņo, ko var atvieglot ar automātiskiem grāmatojumiem. Ja dati nekam netiek lietoti, tas veido nevajadzīgu noslodzi.

Ieteicams izveidot tikai tās operācijas, kas ir absolūti nepieciešamas plānošanai (kas parasti ir deficīta resursi) un/vai izmaksu aprēķināšanas nolūkam. Vai arī jums jāgrupē daudzas mazākas, atšķirīgas operācijas vienā lielākā operācijā, kas pārstāv lielāko procesa daļu.

### <a name="many-applicable-resources-for-an-operation"></a>Daudzi operācijām piemērojami resursi

Piemērojamo resursu skaitu operācijai nosaka resursu prasības, kas iestatītas operāciju relācijā. Vajadzība var būt pēc specifiska (atsevišķa) resursa, vai arī tā var pamatoties uz resursa piederību resursu grupai vai iespēju.

Ja plānošana nav veikta, izmantojot ierobežoto noslodzi un visiem piemērojamajiem resursiem ir viens un tas pats kalendārs un efektivitāte, tad plānošanas programma operācijai vienmēr rezultātā izvēlēsies vienu un to pašu resursu, bet tikai pēc visu atbilstošo resursu izmēģināšanas, lai pārbaudītu, vai ir viens, kas ir „labāks” par citiem. Šādā gadījumā plānošanas noslodzi var ievērojami samazināt vienkārši, vienmēr piešķirot operācijai noteiktu resursu maršruta izveides laikā.

### <a name="route-with-parallel-operations"></a>Maršruts ar vienlaicīgām operācijām

Lai gan paralēlas operācijas (primāras/sekundāras) ir spēcīgs rīks scenāriju modelēšanai, piemēram, kad iekārta un operators abi ir nepieciešami noteikta uzdevuma izpildei, tas ir arī daudzu veiktspējas problēmu avots. Ja noteikta, atsevišķa resursa prasība ir piešķirta gan primārajai, gan sekundārajai operācijai, parasti tā nav problēma. Bet, ja katrai operācijai ir daudz iespējamo resursu, tad plānošanai tiek ievērojami palielināta skaitļošanas sarežģītība.

Paralēlu operāciju izmantošanas alternatīva ir vai nu modelēt pārus kā „virtuālos” resursus (kas pēc tam pārstāvēs grupu, kas vienmēr operācijai tiks piešķirta kopā), vai vienkārši nemodelēt kādu no operācijām, ja tā nepārstāv kādu deficīta resursu.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Operācijas ar resursu daudzumu, kas lielāks par 1

Ja iestatāt operācijai nepieciešamo resursu daudzumu, kas ir lielāks par vienu, tad tas efektīvi darbojas tāpat, kā lietojot primārās/sekundārās operācijas, jo programmai tiek nosūtīti vairāki paralēli darbi. Tomēr šim gadījumam nav iespējams izmantot noteiktas resursu piešķires, jo daudzumam, kas ir lielāks par vienu, nepieciešams, ka operācijai būtu piemērojami vairāki resursi.

### <a name="excessive-use-of-finite-capacity"></a>Pārmērīga ierobežotas noslodzes izmantošana

Ierobežotas noslodzes izmantošana paredz, ka programma noslodzes informāciju ielādētu no datu bāzes, un iespējama skaitļošanas pieskaitīšana, jo būs grūtāk atrast risinājumu, it īpaši vidēs, kur resursi ir rezervēti tuvu to maksimālajai noslodzei. Tā rezultātā ir svarīgi rūpīgi izvērtēt, vai resursam patiešām ir jāizmanto ierobežota noslodze, vai arī tos var pārrezervēt. Tā kā, iespējams, pastāv atšķirība starp ierobežotas noslodzes resursiem mērā, cik svarīgi ir tos nepārrezervēt, mēs rekomendējam resursam izmantot deficīta opciju kombinācijā ar atsevišķu vērtību plānā „Perioda noslodze deficīta resursiem”. Izmantojot deficīta konceptu, var nodrošināt, ka vispārējo ierobežoto noslodzes periodu iespējams samazināt.

### <a name="setting-hard-links"></a>Fiksēto saišu iestatīšana

Maršruta standarta saites tips ir *nefiksēts*, kas nozīmē, ka ir atļauts laika intervāls starp vienas operācijas pabeigšanas laiku un nākamās sākumu. Šī pieļaušana var izraisīt nevēlamas sekas, ka materiāli vai noslodze nav pieejama vienai no operācijām ļoti ilgu laiku, ražošana varētu būt dīkstāvē diezgan ilgu laiku, kas nozīmē iespējamu nepabeigtu darbu pieaugumu. Šis nenotiks ar fiksētām saitēm, jo beigām un sākumam ir precīzi jāsakrīt. Taču fiksētu saišu iestatīšana padara plānošanas problēmu sarežģītāku, jo darba laiks un noslodzes krustpunkti ir jāaprēķina diviem operāciju resursiem. Ja ir iesaistītas arī paralēlas operācijas, tas ievērojami palielina skaitļošanas laiku. Ja abu operāciju resursiem ir atšķirīgi kalendāri, kas vispār nepārklājas, problēma ir neatrisināma.

Ieteicams izmantot fiksētās saites tikai tad, kad tas ir konkrēti nepieciešams, un rūpīgi apsvērt, vai tas ir nepieciešams katrai maršruta operācijai.

Lai samazinātu nepabeigto darbu, nelietojot fiksētās saites, risinājuma metode ir ieplānot pasūtījumu divreiz, mainot otrā soļa virzienu uz pretējo. Ja pirmais grafiks tika veikts atpakaļejošā virzienā no saņemšanas datuma, tad otrais ir jāveic no plānotā sākuma datuma uz priekšu. Tā rezultātā darbi tiks saspiesti pēc iespējas vairāk, lai nepabeigtais darbs tiktu minimizēts.

### <a name="separate-calendar-for-each-resource"></a>Atsevišķs kalendārs katram resursam

Viens no galvenajiem plānošanas programmas datu avotiem ir kalendāra informācija, ko var būt dārgi ielādēt no datu bāzes. Tā kā kalendāri tiek ģenerēti, pamatojoties uz veidnēm, būtu vilinoši ģenerēt kalendāru katram resursam un pēc tam pielāgot informāciju šajā kalendārā, kad resurss atrodas dīkstāve vai ar to saistītas citas problēmas. Tomēr, veicot šo darbību, tiks ievērojami ierobežota programmas spēja ierakstīt kešatmiņā kalendāra datus, jo tai būtu jāpieprasa jauni dati katram resursam, un tas var būt liels veiktspējas problēmu avots. Tā vietā ieteicams starp resursiem atkārtoti izmantot kalendārus un pēc tam kontrolēt dīkstāves izmaiņas, katram periodam piešķirot citu kalendāra ID.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Liels darba laika slotu skaits kalendārās dienas ietvaros

Tā kā programma darbojas, pa vienam izpētot laika slotus un to noslodzi, ir lietderīgi minimizēt laika slotu skaitu uz vienu kalendāro dienu. To var darīt, piemēram, apsverot, vai ir svarīgi iegūtajā grafikā, lai atspoguļot to, ka darbiniekiem ik stundu ir 5 minūšu pārtraukums.

### <a name="large-or-none-scheduling-timeouts"></a>Liels (vai neviens) plānošanas taimauts

Plānošanas programmas veiktspēju var optimizēt, izmantojot parametrus, kas atrodami lapā **Plānošanas parametri**. Iestatījumiem **Iespējots plānošanas taimauts** un **Iespējots plānošanas optimizācijas taimauts** vienmēr jābūt iestatītiem uz **Jā**. Ja iestatīti uz **Nē**, plānošana potenciāli var darboties neierobežoti, ja ir izveidots neizpildāms maršruts ar daudzām opcijām.

**Maksimālais plānošanas laiks vienai secībai** vērtība kontrolē, kāds ir maksimālais sekunžu skaits, ko drīkst iztērēt, mēģinot atrast risinājumu vienai secībai (vairumā gadījumu secība atbilst vienam pasūtījumam). Šeit izmantojamā vērtība lielā mērā ir atkarīga no tā, cik sarežģīts ir maršruts un iestatījumi, piemēram, ierobežota noslodze ar maksimumu, kas nepārsniedz 30 sekundes, ir labs sākuma punkts.

**Optimizācijas mēģinājumu taimauts** kontrolē, kāds ir maksimālais sekunžu skaits, ko drīkst iztērēt, lai atrastu piemērotāku risinājumu, nekā sākotnēji atrasts. Tas ietekmēs tikai tos maršrutus, kuri lieto paralēlās operācijas, jo tie liek pārbaudīt dažādas kombinācijas.

> [!NOTE]
> Taimautiem iestatītās vērtības tiks piemērotas gan izpildei nodoto ražošanas pasūtījumu, gan plānoto pasūtījumu plānošanai, kā daļai no MRP. Tā rezultātā, iestatot ļoti lielas vērtības, var būtiski palielināt MRP izpildes laiku, kad tiek palaists plāns ar daudziem plānotiem ražošanas pasūtījumiem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]