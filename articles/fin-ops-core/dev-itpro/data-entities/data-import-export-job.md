---
title: Datu importēšanas un darbu eksportēšanas pārskats
description: Lai izveidotu un pārvaldītu datu importēšanas un eksportēšanas darbus, izmantojiet darbvietu Datu pārvaldība.
author: Sunil-Garg
manager: AnnBe
ms.date: 09/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b852a73268251241cd66a07d7e4f4720706c0d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184558"
---
# <a name="data-import-and-export-jobs-overview"></a>Datu importēšanas un eksportēšanas darbu pārskats

[!include [banner](../includes/banner.md)]

Datu importēšanas un eksportēšanas darbu izveidei un pārvaldībai tiek izmantota darbvieta **Datu pārvaldība**. Pēc noklusējuma datu importēšanas un eksportēšanas process izveido sagatavošanas tabulu katram elementam mērķa datu bāzē. Sagatavošanas tabulas pirms jums ļauj datus pārbaudīt, iztīrīt vai konvertēt, pirms tos pārvietojat.

> [!NOTE]
> Šajā tēmā tiek pieņemts, ka pārzināt [datu elementus](data-entities.md).

## <a name="data-importexport-process"></a>Datu importēšanas/eksportēšanas process
Tālāk ir aprakstītas darbības datu importēšanai vai eksportēšanai.

1. Izveidojiet importēšanas vai eksportēšanas darbu, kur jūs izpildāt tālāk uzskaitītos uzdevumus.

    - Definējiet projekta kategoriju.
    - Norādiet importējamos vai eksportējamos elementus.
    - Iestatiet darba datu formātu.
    - Norādiet elementu secību, lai tie tiktu apstrādāti loģiskās grupās un saprotamā secībā.
    - Nosakiet, vai izmantot sagatavošanas tabulas.

2. Pārliecinieties, vai avota dati un mērķa dati ir kartēti pareizi.
3. Pārbaudiet sava importēšanas vai eksportēšanas darba drošību.
4. Palaidiet importēšanas vai eksportēšanas darbu.
5. Pārbaudiet, vai darba norise notiek, kā paredzēts, pārskatot darba vēsturi.
6. Iztīriet sagatavošanas tabulas.

Atlikušajās šīs tēmas sadaļās ir sniegta plašāka informāciju par katru šī procesa posmu.

> [!NOTE]
> Lai atsvaidzinātu datu importēšanas/eksportēšanas veidlapu un tajā tiktu rādīta jaunākā informācija par norisi, izmantojiet veidlapas atsvaidzināšanas ikonu. Pārlūka līmeņa atsvaidzināšana nav ieteicama, jo tā pārtrauks visus importēšanas/eksportēšanas darbus, kas nedarbojas paketē.

## <a name="create-an-import-or-export-job"></a>Importēšanas vai eksportēšanas darba izveidošana
Datu importēšanas vai eksportēšanas darbu var palaist vienu reizi vai vairākas reizes.

### <a name="define-the-project-category"></a>Projekta kategorijas definēšana
Iesakām jums veltīt laiku tam, lai savam importēšanas vai eksportēšanas darbam atlasītu atbilstošu projektu kategoriju. Projektu kategorijas var jums palīdzēt saistīto darbu pārvaldīšanā.

### <a name="identify-the-entities-to-import-or-export"></a>Importējamo vai eksportējamo elementu norādīšana
Importēšanas vai eksportēšanas darbiem varat pievienot konkrētus elementus vai atlasīt izmantojamo veidni. Veidnes darbu aizpilda ar elementu sarakstu. Opcija **Lietot veidni** ir pieejama pēc tam, kad darbam piešķirat nosaukumu un šo darbu saglabājat.

### <a name="set-the-data-format-for-the-job"></a>Darba datu formāta iestatīšana
Kad atlasāt kādu elementu, ir jāatlasa formāts tiem datiem, kas tiks eksportēti vai importēti. Formātus jūs definējat, izmantojot elementu **Datu avotu iestatīšana**. Avota datu formāts sastāv no atribūtiem **Tips**, **Faila formāts**, **Rindas norobežotājs** un **Kolonnas norobežotājs**. Pastāv arī citi atribūti, bet minētie ir vissvarīgākie. Sekojošajā tabulā ir minētas derīgās kombinācijas.

| Faila formāts            | Rindas/kolonnas norobežotājs                       | XML stils                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-NA-                     |
| XML                    | \-NA-                                      | XML-elements XML-atribūts |
| Norobežots, fiksēts platums | Komats, semikols, tabulēšanas rakstzīme, vertikālā josla, kols | \-NA-                     |

### <a name="sequence-the-entities"></a>Elementu secības norādīšana
Datu veidnē vai importēšanas un eksportēšanas darbos elementus var izkārtot noteiktā secībā. Kad palaižat darbu, kurā ir vairāki datu elementi, jums ir pārliecinās, vai šie datu elementi ir sakārtoti pareizā secībā. Elementu secību jūs galvenokārt norādāt tā, lai varētu ievērot visas funkcionālās atkarības starp elementiem. Ja elementiem nav funkcionālo atkarību, tad tos var ieplānot paralēlai importēšanai vai eksportēšanai.

#### <a name="execution-units-levels-and-sequences"></a>Izpildes vienības, līmeņi un secības
Izpildes vienība, līmenis izpildes vienībā un elementu secība palīdzēt kontrolēt kārtību, kādā dati tiek eksportēti vai importēti.

- Elementi citās izpildes vienībās tiek apstrādāti paralēli.
- Katrā izpildes vienībā elementi tiek apstrādāti paralēli, ja tiem ir viens līmenis.
- Katrā līmenī elementi tiek apstrādāti atbilstoši to kārtas numuram attiecīgajā līmenī.
- Kad viens līmenis ir apstrādāts, tiek apstrādāts nākamais līmenis.

#### <a name="resequencing"></a>Atkārtota secības norādīšana
Elementu secību varat vēlēties norādīt no jauna tālāk uzskaitītajos gadījumos.

- Ja visām jūsu izmaiņām tiek lietots tikai viens datu darbs, tad atkārtotas secības norādīšanas opcijas varat izmantot, lai optimizētu pilnā darba izpildes laiku. Šajos gadījumos varat izmantot izpildes vienību, lai pārstāvētu moduli, varat izmantot līmeni, lai pārstāvētu moduļa līdzekļa apgabalu, un izmantot secību, lai pārstāvētu elementu. Izmantojot šo metodi, varat strādāt dažādos moduļos paralēli, bet katrā modulī joprojām varat strādāt secībā. Lai palīdzētu nodrošināt, ka paralēlās operācijas norit sekmīgi, ir jāņem vērā visas atkarības.
- Ja tiek lietoti vairāki datu darbi (piemēram, viens darbs katram modulim), tad secības noteikšanu varat izmantot, lai ietekmētu elementu līmeni un secību optimālai izpildīšanai.
- Ja atkarību nav vispār, tad maksimālas optimizēšanas nolūkos elementus varat sakārtot dažādās izpildes vienībās.

Izvēlne **Atkārtota secības norādīšana** ir pieejama, ja ir atlasīti vairāki elementi. Secību varat atkārtoti norādīt, pamatojoties uz izpildes vienības, līmeņa vai secības opcijām. Lai atkārtoti norādītu secību atlasītiem elementiem, varat izmantot kādu soli. Katram elementam atlasītā vienība, līmenis un/vai kārtas numurs tiek atjaunināts ar norādīto soli.

#### <a name="sorting"></a>Kārtošana
Lai elementu sarakstu skatītu secības kārtībā, varat izmantot opciju **Kārtot pēc**.

### <a name="truncating"></a>Apciršana
Importa projektiem varat izlemt, ka ieraksti entītijās pirms importēšanas ir jāapcērt. Tas ir noderīgi, ja jūsu ieraksti ir jāimportē tīrā tabulu kopā. Pēc noklusējuma šis iestatījums ir izslēgts.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Pārliecināšanās, vai avota dati un mērķa dati ir kartēti pareizi
Kartēšana ir funkcija, kas attiecas gan uz importēšanas, gan uz eksportēšanas darbiem.

- Saistībā ar importēšanas darbu kartēšanas apraksta, kuras kolonnas avota failā kļūst par kolonnām sagatavošanas tabulā. Tādēļ sistēma var noteikt, kuras avota faila kolonnas dati ir jākopē kurā sagatavošanas tabulas kolonnā.
- Saistībā ar eksportēšanas darbu kartēšanas apraksta, kuras sagatavošanas tabulas (t.i., avota) kolonnas kļūst par kolonnām mērķa failā.

Ja kolonnu nosaukumi sagatavošanas tabulā atbilst nosaukumiem failā, tad sistēma kartējumu izveido automātiski, pamatojoties uz nosaukumiem. Taču, ja nosaukumi atšķiras, kolonnas netiek kartētas automātiski. Šādos gadījumos jums ir jāizpilda kartēšana, datu darbā atlasot elementa opciju **Skatīt karti**.

Pastāv divi kartēšanas skati: **Kartēšanas vizualizēšana**, kurš ir noklusējuma skats, un **Detalizēta informācija par kartēšanu**. Sarkana zvaigznīte (\*) norāda visus elementa obligātos laukus. Lai varētu strādāt ar elementu, ir jānorāda šo lauku kartējums. Kad strādājat ar elementu, ja nepieciešams, varat atcelt kartējumu citiem laukiem. Lai atceltu kartējumu kādam laukam, atzīmējiet šo lauku kolonnā **Elements** vai kolonnā **Avots** un pēc tam atlasiet **Dzēst atlasi**. Atlasiet **Saglabāt**, lai saglabātu veiktās izmaiņas, un pēc tam aizveriet lapu, lai atgrieztos pie projekta. Šo pašu procesu varat izmantot, lai pēc importēšanas rediģētu lauku kartējumu no avota uz sagatavošanu.

Kartējumu lapā varat ģenerēt, atlasot **Ģenerēt avota kartējumu**. Ģenerēts kartējums darbojas tāpat kā automātisks kartējums. Tādēļ visi nekartētie lauki jums ir jākartē manuāli.

![Datu kartēšana](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Sava importēšanas vai eksportēšanas darba drošības pārbaudīšana
Piekļuve darbvietai **Datu pārvaldība** var būt ierobežota, lai lietotāji bez administratora tiesībām varētu piekļūt tikai noteiktiem datu darbiem. Piekļuve datu darbam tostarp nozīmē pilnu piekļuvi šī darba izpildes vēsturei un piekļuvi sagatavošanas tabulām. Tādēļ, kad veidojat datu darbu, jums ir jāpārliecinās, vai tiek izmantotas atbilstošas piekļuves kontroles.

### <a name="secure-a-job-by-roles-and-users"></a>Darba nodrošināšana pēc lomām un lietotājiem
Lai piekļuvi darbam atļautu tikai vienai vai vairākām drošības lomām, izmantojiet izvēlni **Piemērojamās lomas**. Šim darbam varēs piekļūt tikai lietotāji ar šīm lomām.

Piekļuvi darbam varat arī sniegt tikai konkrētiem lietotājiem. Kad darbu nodrošināt pēc lietotājiem, nevis pēc lomām, tad notiek lielāka kontrole, ja vienai lomai ir piešķirti vairāki lietotāji.

### <a name="secure-a-job-by-legal-entity"></a>Darba nodrošināšana pēc juridiskajās personas
Datu darbi ir globāla rakstura. Tādēļ, ja datu darbs tika izveidots un izmantots kādā juridiskajā personā, tad šis darbs būs redzams citās sistēmas juridiskajās personās. Šai noklusējuma uzvedībai var tikt dota priekšroka noteiktos lietojuma scenārijos. Piemēram, organizācija, kas importē rēķinus, izmantojot datu elementus, var nodrošināt centralizēta rēķinu apstrādes darba grupu, kas ir atbildīga par rēķinu kļūdu pārvaldīšanu visās organizācijas nodaļās. Šādā scenārijā centralizētajai rēķinu apstrādes darba grupai var noderēt piekļuve rēķinu importēšanas darbiem no visām juridiskajām personām. Tādēļ noklusējuma uzvedība atbilst prasībām no juridiskās personas perspektīvas.

Taču organizācija var vēlēties, lai rēķinu apstrādes darba grupas darbotos katrā juridiskajā personā. Šajā gadījumā darba grupai kādā juridiskajā personā ir nepieciešama piekļuve tikai rēķinu importēšanas darbam savā juridiskajā personā. Lai izpildītu šo prasību, datu darbiem varat konfigurēt no juridiskās personas atkarīgu piekļuves kontroli, datu darbā izmantojot izvēlni **Piemērojamās juridiskās personas**. Kad konfigurēšana ir pabeigta, lietotāji var redzēt tikai darbus, kas ir pieejami tajā juridiskajā personā, kurā šie lietotāji pašlaik ir pierakstījušies. Lai redzētu darbus no citas juridiskās personas, lietotājiem ir jāpārslēdzas uz attiecīgo juridisko personu.

Darbu var vienlaikus nodrošināt pēc lomām, lietotājiem un juridiskajām personām.

## <a name="run-the-import-or-export-job"></a>Importēšanas vai eksportēšanas darba palaišana
Darbu varat palaist vienu reizi, pēc darba definēšanas atlasot pogu **Importēt** vai **Eksportēt**. Lai iestatītu periodisko darbu, atlasiet **Izveidot periodisku datu darbu**.

> [!NOTE]
> Importēšanas vai eksportēšanas darbu var izpildīt asinhroni, atlasot pogu **Importēt** vai **Eksportēt**. Asinhronai izpildei tiek izmantota asinhronā struktūra, kas atšķiras no pakešuzdevumu struktūras. Tomēr tāpat kā pakešuzdevumu struktūrai arī asinhronajai struktūrai var tikt veikta ierobežošana un tā rezultātā darba izpilde var nenotikt nekavējoties. Darbus arī var izpildīt sinhroni, atlasot **Importēt tūlīt** vai **Eksportēt tūlīt**. Tas sāk darbu nekavējoties un ir noderīgi, ja asinhrona vai pakešuzdevumu izpilde netiek uzsākta ierobežošanas dēļ. Darbus var izpildīt arī kā pakešuzdevumu, izvēloties opciju **Izpilde partijā**. Uz partijas resursiem attiecas ierobežošana, tādēļ pakešuzdevuma izpilde var nenotikt nekavējoties. Asinhronā opcija ir noderīga, kad lietotāji mijiedarbojas tieši ar lietotāja interfeisu un nav tik pieredzējuši, lai saprastu pakešuzdevumu plānošanu. Partijas izmantošana ir alternatīvs risinājums, ja ir nepieciešams importēt vai eksportēt lielu apjomu. Pakešuzdevumus var plānot izpildei noteiktā pakešuzdevumu grupā — tas sniedz lielāku kontroli slodzes līdzsvarošanas ziņā. Ja asinhronai un pakešuzdevumu izpildei tiek veikta ierobežošana liela sistēmas resursu izmantojuma dēļ, tad kā tūlītēju risinājumu var izmantot sinhronu importēšanas/eksportēšanas versiju. Sinhronā opcija sāksies nekavējoties un bloķēs lietotāja interfeisu, jo notiek sinhrona izpilde. Pārlūkprogrammas logam jāpaliek atvērtam, kad notiek sinhrona darbība.

## <a name="validate-that-the-job-ran-as-expected"></a>Pārbaudīšana, vai darba norise notiek paredzētajā veidā
Gan eksportēšanas, gan importēšanas darbiem problēmu novēršanai un izmeklēšanai ir pieejama darbu vēsture. Vēsturiskās darbu izpildes ir sakārtotas pēc laika diapazoniem.

![Darbu vēsture diapazoni](./media/dixf-job-history.md.png)

Par katru darba palaišanu ir tālāk aprakstītā detalizētā informācija.

- Detalizēta informācija par izpildi
- Izpildes žurnāls

Detalizēta informācija par izpildi rāda stāvokli katram datu elementam, kuru šis darbs apstrādāja. Tādēļ jūs varat ātri atrast tālāk uzskaitīto informāciju.

- Kuri elementi tika apstrādāti.
- Attiecībā uz elementu — cik ierakstu tika sekmīgi apstrādāti un cik daudzi bija nesekmīgi.
- Sagatavošanas posmu ieraksti katram elementam.

Sagatavošanas posmu datus eksportēšanas darbiem varat lejupielādēt failā, vai importēšanas un eksportēšanas darbiem tos varat lejupielādēt kā paketi.

No detalizētas informācijas par izpildi varat arī atvērt izpildes žurnālu.

## <a name="clean-up-the-staging-tables"></a>Sagatavošanas tabulu iztīrīšana
Sākot ar platformas atjauninājumu 29, šī funkcionalitāte ir novecojusi. Tā ir aizstāta ar jaunu darbu vēstures tīrīšanas funkcionalitātes versiju, kas izskaidrota tālāk.

Sagatavošanas tabulas varat iztīrīt, izmantojot līdzekli **Sagatavošanas iztīrīšana** darbvietā **Datu pārvaldība**. Lai atlasītu, kuri ieraksti ir jāizdzēš un no kuras sagatavošanas tabulas, varat izmantot tālāk aprakstītās opcijas.

- **Elements** — ja ir nodrošināts tikai elements, no šī elementa sagatavošanas tabulas tiek dzēsti visi ieraksti. Atlasiet šo opciju, lai šim elementam iztīrītu visus datus visos datu projektos un visos darbos.
- **Darba ID** — ja ir nodrošināts tikai darba ID, no atbilstošajām sagatavošanas tabulām tiek dzēsti visi ieraksti visiem elementiem atlasītajā darbā.
- **Datu projekti** — ja ir atlasīts tikai datu projekts, atlasītajam datu projektam tiek dzēsti visi ieraksti visiem elementiem un visos darbos.

Šīs opcijas varat arī kombinēt, lai dzēšamo ierakstu kopu ierobežotu vēl vairāk.

## <a name="job-history-clean-up-available-in-platform-update-29-and-later"></a>Darbu vēstures tīrīšana (pieejama platformas atjauninājumā 29 un jaunākās versijās)

Darba vēstures tīrīšanas funkcionalitāte datu pārvaldībā jāizmanto, lai ieplānotu periodisku izpildes vēstures tīrīšanu. Šī funkcionalitāte aizstāj iepriekšējo sagatavošanas posmu tabulas tīrīšanas funkcionalitāti, kas tagad ir novecojusi. Tālāk minētās tabulas tiks tīrītas, izmantojot tīrīšanas procesu.

-   Visas inscinējuma tabulas

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Funkcionalitātei jābūt iespējotai līdzekļu pārvaldībā, pēc tam tai var piekļūt no **Datu pārvaldība \> Darbu vēstures tīrīšana**.

### <a name="scheduling-parameters"></a>Parametru plānošana

Plānojot tīrīšanas procesu, ir jānorāda tālāk norādītie parametri, lai definētu tīrīšanas kritērijus.

-   **Vēstures saglabāšanas dienu skaits**  — šis iestatījums tiek izmantots, lai kontrolētu izpildes vēstures apjomu, kas jāsaglabā. Tas tiek norādīts kā dienu skaits. Kad tīrīšanas darbs ir ieplānots kā periodisks pakešuzdevums, šis iestatījums darbosies kā pastāvīgi kustīgs logs, tādējādi vienmēr atstājot norādītā dienu skaita vēsturi neskartu un dzēšot pārējo. Noklusējums ir 7 dienas.

-   **Darba izpildes stundu skaits** — atkarībā no notīrāmā vēstures apjoma kopējais tīrīšanas darba izpildes laiks var būt robežās no dažām minūtēm līdz dažām stundām. Tā kā minēto tabulu tīrīšana ir jāveic, kad sistēmā nav citu datu pārvaldības aktivitāšu, ir svarīgi pārliecināties, ka tīrīšanas darbs tiek izpildīts un pabeigts pirms biznesa aktivitātes sākuma.

    Maksimālo izpildes laiku var norādīt, iestatot maksimālo ierobežojumu stundu skaitam, kad darbs ir jāpalaiž, izmantojot šo iestatījumu. Tīrīšanas loģika izpaužas kā viena darba izpildes ID vienā laikā hronoloģiski sakārtotā secībā, saistītās izpildes vēstures tīrīšanā pirmo notīrot vecāko. Tas pārtrauks jauna izpildes ID pieņemšanu, ja atlikušais izpildes ilgums ir pēdējo 10 % robežās no norādītā ilguma. Dažos gadījumos tiks prognozēts, ka tīrīšanas darbs turpināsies pēc norādītā maksimālā laika. Tas lielā mērā būs atkarīgs no to ierakstu skaita, kuri tiks dzēsti pašreizējam izpildes ID, kas tika sākts pirms 10 % sliekšņa sasniegšanas. Sāktā tīrīšana ir jāpabeidz, lai nodrošinātu datu integritāti, kas nozīmē, ka tīrīšana turpināsies, neraugoties uz noteiktā ierobežojuma pārsniegšanu. Kad tas ir pabeigts, jauni izpildes ID netiek pieņemti, un tīrīšanas darbs tiek pabeigts. Atlikusī izpildes vēsture, kas netika iztīrīta pietiekama izpildes laika trūkuma dēļ, tiks izvēlēta nākamajā reizē, kad ieplānots tīrīšanas darbs. Noklusējuma un minimālā vērtība šim iestatījumam ir iestatīta uz 2 stundām.

-   **Periodiska partija** — tīrīšanas darbu var palaist kā vienreizēju, manuālu izpildi vai arī to var plānot periodiskai izpildei partijā. Partiju var ieplānot, izmantojot iestatījumus **Palaist fonā**, kas ir partijas standarta iestatījums.