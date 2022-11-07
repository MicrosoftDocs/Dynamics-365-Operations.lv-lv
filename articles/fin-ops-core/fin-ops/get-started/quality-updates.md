---
title: Proaktīvi kvalitātes atjauninājumi
description: Šajā rakstā ir sniegta informācija par apsteidz aktīvo kvalitātes atjauninājumu piegādi.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: da5881a901d3ba4d01e6d4510a53ca079efd7e75
ms.sourcegitcommit: c8b97eea28f07b6b179825f3b134c8c8704ff8fc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2022
ms.locfileid: "9731615"
---
# <a name="proactive-quality-updates"></a>Proaktīvi kvalitātes atjauninājumi

[!include[banner](../includes/banner.md)]

Pēdējos gados Microsoft ir progresējusi attiecībā uz to, ko mēs nosaucām par [vienu versiju](../../dev-itpro/lifecycle-services/oneversion-overview.md). Vienas versijas priekšnoteikums ir vienkāršs: jo tuvāk var būt visiem klientiem tajā pašā programmatūras versijā, jo augstāka kvalitātes, ko mēs varam piegādāt. Kļūdas tiek meklētas un izlabotas vienu reizi, un šie risinājumi tiek ievadīti ātrāk un ātrāk.

Šo telpu apstiprina rezultāti: zemāka incidentu skaits starp mūsu produktiem. Ja debitori nav ar vienu versiju, pastāvīgi redzams, ka tos ietekmē problēmas, kurām risinājums jau ir pieejams. Dynamics 365 Finanses, Dynamics 365 Piegādes Dynamics 365 Project Operations Dynamics 365 Commerce ķēde jau ir progresējusi un paldies nesenajiem tehniskajiem avansiem, tagad ir iespējams veikt nākamo soli. Tālāk ir aprakstīts, ko mēs gatavojam darīt, ko mēs jau esam veikuši, lai iestatītu pakāpi un to, kā un kad mēs ieviesām jaunās iespējas bez pārrāvuma.

## <a name="focus-on-quality-updates"></a>Fokuss uz kvalitātes atjauninājumiem

Šobrīd gadā tiek nodrošināti [septiņi](public-preview-releases.md) pakalpojumu atjauninājumi. Piemēram, versija 10.0.29 ir pakalpojuma atjauninājums. Līdz nesen ir astoņi atjauninājumi gadā. Tomēr viens atjauninājums tika nomests, atbildot uz debitora datiem, kas norāda uz vēlmi izvairīties no izmaiņām kalendārā gada beigās.

Mēs mainīsim pakalpojumu atjauninājumu laiku. Tā vietā nākamais solis vienas versijas ceļojuma laikā ir fokusēts uz kvalitātes *atjauninājumiem*. Kvalitātes atjauninājumi ir labojumfailu kumulatīvie būvumi. Tajos nav iekļautas jaunas funkcijas. Jebkurā laikā mūsu visa debitoru kopiena tiek izplatīta starp trim vai četriem jaunākajiem pakalpojuma atjauninājumiem. Tomēr jebkurā konkrētā pakalpojuma atjauninājumā grupā var izmantot ducis dažādu kvalitātes atjauninājumu versiju, atkarībā no lietotāju izvietošanas datumiem. Nākamajā solī mēs apsteidzam kvalitātes atjauninājumus. Mēs jau izmantojam šo modeli mūsu programmām Dataverse un esiet redzams uzlabotās kvalitātes rezultātu paredzamais rezultāts un jāsamazina atbalsta incidenti.

Protams, defektu samazināšana var samazināt vai pilnībā izslēgt nepieciešamību pēc kvalitātes atjauninājumiem. Lidojumam ir vairākas iniciatīvas, lai samazinātu defektus, kuriem nepieciešami kvalitātes atjauninājumi. Pat ja kvalitātes atjauninājumā tiek samazinātas lietderīgās noslodzes, saskaņotība starp debitora bāzi uzlabos izmantojamību, ātrāku uzlabojumus debitoriem un samazina debitoru frekvenci, kas saskaras ar problēmām, kam jau pastāv risinājumi.

## <a name="making-proactive-distribution-possible"></a>Padarīt proaktīvo sadali par iespējamo

Vairāki avansi jau ir izvietoti, kas iespējo kvalitātes atjauninājumu proaktīvo piegādi:

- **Nulles dīkstāves** atjaunināšana – Lai virzītu biežākas vides, ir svarīgi samazināt ietekmi uz vides pieejamību, lai saglabātu Dynamics 365 pakalpojumu līmeņa līgumus (SLA). Sākotnēji tika ieviesta nulles dīkstāves atjaunināšana, lai palīdzētu uzlabot mēneša operētājsistēmas ielāpošanu, izmantojot klastera atteici, lai aktivizētu atjaunināto attēlu ar minimālu pārrāvumu. Atjaunināšanas lietošanas mehānisms tiek uzlabots, lai tas būtu vēl mazāk traucējošs, un tas segs gan operētājsistēmas ielāpošanu, gan kvalitātes atjauninājumu izvietošanu.

Interaktīviem lietotājiem aktīva sesija var tikt pārtraukta, un mēģinājums tiks atkārtoti iet uz pašreiz atjaunināto vidi. Ieviešot uz prioritāti balstītu [pakešuzdevumu plānošanu, pakešuzdevumu plānošana](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) un apstrāde atkop un atsākas tūlīt pēc atjaunināšanas. Uz prioritāti balstīta pakešuzdevumu plānošana tiks vieta debitoriem, pirms tie sāks piedalīties savā ražošanas vidē proaktīvā kvalitātes atjauninājumu sadalē.

- **Tumšas** stundas — tumšās stundas ir definētas katram Azure reģionam, un tumšajā stundu periodā tiek lietoti nulles dīkstāves atjauninājumi.

## <a name="the-proactive-update-process"></a>Proaktīvās atjaunināšanas process

Proaktīvo kvalitātes atjauninājumu izvietošana sekos drošas izvietošanas procesam (SDP). SDP specifika attīstīsies, bet kvalitātes atjauninājumi sākotnēji tiks izvietoti kastu vidēs. Kad palielinās veiksmīgi izvietoto kastu procentuālā vērtība, sāks izvietot ražošanas vidēs. Klausības sistēmas uzraudzīs sistēmas telemārketinga un dzīves vietas incidentus un apturēs noteiktas versijas izriti, ja tiks atklāta jebkāda regresija. Ja debitori vēlas, joprojām būs iespēja izvilkt kvalitātes atjauninājumus pirms proaktīvās izvietošanas.

Pašreizējie laidiena pārvaldības dati parāda, ka kvalitātes atjauninājumos ir ieviestas mazāk nekā 3 procenti no regresijām. Kad ir palielināta fokuss uz regresijas un uzlabotās SDP likvidēšanas iespēju, regresiju potenciālā ietekme būs īpaši zemāka nekā kvalitātes ieguvumi, kas tiek sasniegti, ātrāk iegūstot klientiem plaši izvietotus labojumus.

## <a name="process-changes"></a>Apstrādāt izmaiņas

Notiek procesa izmaiņu kopa, kas apsteidz proaktīvās kvalitātes atjauninājuma izvietošanas aktivizāciju:

- **Shēma** – rīku rīks nodrošina, ka kvalitātes atjauninājumu būvējuma laikā tiek iekļautas tikai shēmu izmaiņas, kuras var tikt lietotas pakalpojuma tiešsaistes režīmā. Šī pieeja palīdzēs saglabāt iespēju pielietot atjauninājumu ar nulles dīkstāves laiku.
- **Palielināto izmaiņu** veikšana — pašlaik ir jau papildu procesa solis, lai apstiprinātu izmaiņas iekļaušanai kvalitātes atjauninājumā. Papildu darbība tiks palielināta, lai palīdzētu samazināt regresiju potenciālu. Kvalitātes atjauninājumos nav atļautas sadalīšanas izmaiņas, un palielinātais izmaiņu apraksts palīdzēs nodrošināt, ka mēs nodrošināt atbilstību šim mērķim.
- **Redzamība** – mēs nosūtīsim paziņojumus caur administratoru centru, dzīves cikla pakalpojumiem (LCS) un citiem pieejamajiem kanāliem gaidāmajiem apsteidzošo kvalitātes atjauninājumiem. Turklāt atbalsta darba grupas un incidentu potenciālie klienti būs redzamība tur, kur kvalitātes atjauninājumi ir proaktīvi izvietoti.
 > [!NOTE]
 > Microsoft Sakaru komanda pēta notiekošu e-pasta rīku izveidi, kas novērš e-pasta paziņojumu piegādi. Lūdzu, turpiniet pārraudzīt ziņojumu Microsoft 365 centru, kurā vēlaties skatīt ar darbu saistītos ziņojumus un paziņojumus.
- **Kļūme lidojuma laikā** — lidojuma laikā tiks izmantota lidojuma informācija, kas tiek izmantota, lai veiktu koda izmaiņas, kad tas ir piemērojams kvalitātes atjauninājuma kļūdas labojumā vai izmantot esošās līdzekļa lidojuma izmaiņas, kas attiecas uz labojumu. Ja atkāpšanās vai izmaiņu izslēgšana ir nepieciešama pēc proaktīvās izvietošanas, to var veikt, izmantojot lidojuma sistēmu, lai izvairītos no turpmākām kļūmēm.
- **Slīpstlodziņa** sinhronizācijas apzīmējums — šodien mazāk nekā 20 procenti debitoru ir vairākas kastēs un viena glabāta vieta, kur versija sakrīt ar ražošanu, lai saņemtu palīdzību par problēmu novēršanas. Ja debitors izmanto kasti, lai pārbaudītu jaunāku versiju nekā tā ražošana, šī slīpmaksa saņems jaunākās versijas kvalitātes atjauninājumus.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Kāds ir kvalitātes atjauninājumu atrites mērķis?

Ir paredzēts, ka proaktīvās kvalitātes atjauninājumu sadale kastu vidēm sākas vēlā septembrī vai 2022. gadā Azure publiskajiem mākoņa debitoriem. Pārbaudes vides šajā laikā arī sāks saņemt proaktīvās atjaunināšanas izvietošanu. Septembrī katram debitoram tiks nosūtīts paziņojums, lai informētu tos par paredzēto vides plānu. Proaktīvā atjauninātā sadales procesa izņēmumi būs atļauti tikai ar FDA saistīto debitoru gadījumos. Joprojām strādājam, kā tiks pārvaldītas regulējamās vides un valdības mākonī klienti.

Nākamajā sešu mēnešu periodā mēs pakāpeniski palielināsim kešlodziņa vides daļu procentos, kas saņem proaktīvos atjauninājumus, līdz visas norādītās vides ir iekļautas un turpinās atjaunināt ražošanas vides. Visa perioda laikā mēs pārraudzīsim, lai nodrošinātu, ka izvietošanas process ir efektīvi un ka mēs ieturējam mūsu mērķi - neizjaukjošas lietderīgās noslodzes.

Ņemot vērā, ka debitori regulāri saņems mazāku lietderīgo slodzi, paredzams, ka norēķinu process kļūs vienkāršāks. Tiks pielāgots atjaunināšanas biežums, kad mēs rādīsim spēju palaist procesu bez pārrāvuma. Šis process jau strādā efektīvi mūsu platformā un Dataverse lietojumprogrammās un nodrošina gaidītos pakalpojumu kvalitātes uzlabojumus. Mēs iesakām to pašu soli uz priekšu lietojumprogrammām, kas saistītas ar finansēm un operācijām.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Kad kvalitātes atjauninājumi tiks sākti ražošanas vidēs?
Pašlaik kvalitātes atjauninājumi ir tikai mērķa kastēs. Mēs atjauninām šo vietu ar ražošanas vides sākuma datumu, kad būsim precīzāki dati un rādītāji no proaktīvās lauku atjauninājumiem līdz ražošanas gatavībai.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Kāds ir kešlodziņa apsteidzēšanas kvalitātes atjauninājumu grafiks?
Informāciju par tumšajām stundām katram reģionam skatiet sadaļā ["Kas ir plānotās apkopes logi pēc reģiona?"](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)

### <a name="proactive-quality-update-release-10028"></a>Apsteidzošās kvalitātes atjaunināšanas izlaide: 10.0.28
**Programmas versija: 10.0.1265.89**
**atbilstošs jaunākais zināšanu bāzes rakstā: 745340**

| Stacijas | Reģioni | Pabeigts grafiks| Gaidāmās rūtiņas grafiks
|---|---|---|---|
| 1. stacija | Kanādas Centrālā, Kanādas Austrumi, Francija Centrālā, Indijas Centrālā, Norvēģijas Austrumi, Šveices Rietumi | 2022. gada 15. septembris – 2022. gada 19. septembris – 2022. gada 22. septembris, un 7. oktobris – 2022. gada 10. oktobris | 2022. gada 25. oktobris uz 2022. gada 28. oktobris |
| 2. stacija | Francija Dienvidsudāna, Indija Dienvidsudāna, Norvēģija, Šveice Ziemeļamerikas, Dienvidāfrikas Austrumi, Austrālijas Austrumi, Lielbritānijas Dienvidsudānas, Japānas Austrumi, Austrālijas Dienvidāzijā. | 2022. gada 25. septembris un 7. oktobris – 2022. gada 10. oktobris | 2022. gada 25. oktobris uz 2022. gada 28. oktobris |
| 3. stacija | Austrumāzijas, Lielbritānijas Rietumi, Japānas Rietumi, Brazīlijas Dienvidsudāna, Austrumeiropa, Austrumi ASV, APVIENOTO Arābu Emirātu Centrālā | 2022. gada 26. septembris un 7. oktobris – 2022. gada 10. oktobris | 2022. gada 25. oktobris uz 2022. gada 28. oktobris |
| 4. stacija | Ziemeļ eiropa, Centrālā ASV, Rietumi ASV | 2022. gada 1. oktobris un 7. oktobris – uz 2022. gada 10. oktobris | 2022. gada 25. oktobris uz 2022. gada 28. oktobris |
| 5. stacija | Dod, Government Community Cloud, Ķīna | Nav ieplānots | Nav ieplānots |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Apsteidzošās kvalitātes atjaunināšanas izlaide: 10.0.29
**Programmas versija: 10.0.1326.70**
**atbilstošs jaunākais zināšanu bāzes rakstā: 748926**

| Stacijas | Reģioni | Pabeigts grafiks | Gaidāmās rūtiņas grafiks|
|---|---|---|---|
| 1. stacija | Kanādas Centrālā, Kanādas Austrumi, Francija Centrālā, Indijas Centrālā, Norvēģijas Austrumi, Šveices Rietumi | 2022. gada 14. oktobris uz 17. oktobris | 2022. gada 2. novembris līdz 5. novembris |
| 2. stacija | Francija Dienvidsudāna, Indija Dienvidsudāna, Norvēģija, Šveice Ziemeļamerikas, Dienvidāfrikas Austrumi, Austrālijas Austrumi, Lielbritānijas Dienvidsudānas, Japānas Austrumi, Austrālijas Dienvidāzijā. | 2022. gada 15. oktobris uz 18. oktobris | 2022. gada 2. novembris līdz 5. novembris |
| 3. stacija | Austrumāzijas, Lielbritānijas Rietumi, Japānas Rietumi, Brazīlijas Dienvidsudāna, Austrumeiropa, Austrumi ASV, APVIENOTO Arābu Emirātu Centrālā | 2022. gada 16. oktobris uz 19. oktobris | 2022. gada 2. novembris līdz 5. novembris |
| 4. stacija | Ziemeļ eiropa, Centrālā ASV, Rietumi ASV | 2022. gada 17. oktobris uz 2022. gada 20. oktobris | 2022. gada 2. novembris līdz 5. novembris |
| 5. stacija | Dod, Government Community Cloud, Ķīna | Nav ieplānots | Nav ieplānots |

> [!IMPORTANT] 
> Piecas dienas iepriekš, korporācija Microsoft atjauninās iepriekšējo grafiku un nosūtīs e-pasta paziņojumus uz vidi kopu, kuras ir plānots saņemt šos kvalitātes atjauninājumus. Iepriekšējais grafiks attiecas tikai uz vidēm, kas ir paziņotas par gaidāmo atjaunināšanu. Informāciju par tumšajām stundām katram reģionam skatiet sadaļā ["Kas ir plānotās apkopes logi pēc reģiona?"](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)
>
> Katrai reģionu grupai vai *stacijai*, kurā pašlaik ir ieplānots veikt kvalitātes atjauninājumu atriti, grafiks rāda četru dienu diapazonu. Kvalitātes atjauninājumi sāksies tikai ar kases vides. Tad, pieaugot veiksmīgi izvietoto kastu procentuālajai vērtībai, izvietošana ražošanas vidēs sāksies ar avansa paziņojumiem debitoriem.
> 
> Kvalitātes atjauninājumi vienmēr notiksritīgā veidā, kas iespējo mums plānot vides kopu pēc grafika un pabeigt visas kopas līdz ceturtās stacijas dienas beigām. Tomēr tas nenozīmē, ka vides atjauninājums ietvers četras dienas. Tas nozīmē, ka mēs nevaram iepriekš noteikt, kura vides kopa tiks atjaunināta noteiktā dienā četru dienu diapazonā. Visi atjauninājumi tiks veikti tumšo stundu laikā ar nulles dīkstāvi. Atjauninājumi noteikti tiks pabeigti dotā reģiona tumšo stundu logā.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Kā tumšās stundas tiek apstrādātas debitoriem, kuriem ir viena finanšu un operāciju programmu instance, bet kas ir aktīvas vairākās laika joslās? 
Nav īpašu grafiku ārpus tumšajām stundām, kur eksistē finanšu un operāciju lietojumprogrammu instance, jo mēs plānojam izritināt kvalitātes atjauninājumus minimāli izjaukjošā [veidā ar nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Kāda ir pašreizējā apsteidzēto kvalitātes atjauninājumu atrites kadence?
Apsteidztīvās kvalitātes atjauninājumi (PQUs) pašlaik tiek nosūtīti vienreiz mēnesī katrai atbalstītajām pakalpojuma atjauninājuma versijām. Tikai viens atjauninājums mēnesī tiek pārvietots uz atlasīto kastu vidi, ja debitori nenovieto uz jaunu pakalpojuma atjaunināšanas versiju. Šādā gadījumā tās var iegūt iepriekš plānotu PQU kā daļu no esošas vilcienu jaunajam pakalpojuma atjauninājumam. Pēc globālās atrites pabeigšanas 2023. gadā šo atjauninājumu biežums pieaugs. Jūs vienmēr saņemsiet vismaz viena mēneša paziņojumu, kad tiek mainīta nosūtīšanas kadsija.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Kā Microsoft nodrošina šo atjauninājumu kvalitāti?
Microsoft aprēķini, lai uzturētu izdošanas konveijeru pietiekoši efektīvu, lai piegādātu mazu lietderīgo slodzi, lai uzturētu zemu validācijas izmaksu. Katrs labojums kvalitātes atjauninājumā ir klienta un drošas izvietošanas procesa gaitā, kas palīdz uzlabot kvalitāti un uzticamību, tādējādi samazinot debitora ietekmi. Izvietojums tiks veikts kastu vides stadijās, vispirms sekos ražošana. Stadijas izvietošana ļauj pareizi uzraudzīt, lai noteiktu, vai turpmākā izvietošana ir droša. Ja problēmas tiek konstatētas katrā izvietoto debitoru grupā, mēs aptursim izriti un pārliecinieties, ka katram izrites solim ir pietiekami daudz laika, lai izejas plūsmas izvietotu uz virsmas. Veicot katru gaidāmo kvalitātes atjauninājumu, mēs veiksim grafika redzamību, izmantojot publiskās dokumentācijas un e-pasta atjauninājumu atjauninājumus, lai debitori varētu plānot uz priekšu.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Vai debitori var aizkavēt, pārplānot vai apturēt kvalitātes atjauninājumu?
Nē. Kvalitātes atjauninājumu galvenais mērķis ir nodrošināt, lai mūsu debitoriem pastāvīgi uzlabotu drošību, konfidencialitāti, uzticamību, pieejamību un veiktspēju. Ar atjaunināšanas, drošības, pieejamības un uzticamības aizkavēšanos vai pauzēšanu pastāvēs risks.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Kā es jāzina, kādas izmaiņas tika veiktas kvalitātes atjauninājumu lietderīgajā slodzei?
Turpmākie soļi ir pagaidu risinājums, jo mēs turpinām strādāt pie labāka risinājuma, lai identificētu kvalitātes atjauninājuma lietderīgās slodzes izmaiņu sarakstu. 

Izmantojiet KB# 745340 10.0.28 kvalitātes atjauninājuma vilcienu un saistīto programmas versiju 10.0.1265.89.

1. Sadaļā LCS atveriet lapu Detalizēta informācija par **vidi** savā kastē. 
2. Sadaļā Pieejamie **atjauninājumi** atlasiet Skatīt atjauninājumu **jaunākajam** Kvalitātes atjauninājuma būvējumam. 
3. Eksportējiet būvējumu CSV vai Microsoft Excel failā.
4. Eksportētajā failā kārtojiet informāciju, pamatojoties uz laiku (pirmais vecākais) un pēc tam meklējiet KB 745340 **kolonnā Atjaunināt** ID. Tagad vajadzētu būt redzamiem KBs delta sarakstam.
 
 > [!NOTE]
 > Eksportam uz CSV vai Excel failu ir jāveic pirms vides atjaunināšanas. Pretējā gadījumā varat izmantot vidi ar līdzīgu konfigurāciju, kurā nav instalēts atjauninājums, un izpildiet iepriekš norādītās darbības.

[![Piemērs par vidi ar kvalitātes atjaunināšanu.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Kas ir process, ja pēc kvalitātes atjauninājuma tiek atrasta kritiska problēma?
Kritiska problēma vai regresija ir viens vai vairāki notikumi, kas parasti izraisa vairāku klientu iespējas samazināt pieredzi ar vienu vai vairākiem mūsu pakalpojumiem. Šie jautājumi var izraisīt neplānotas dīkstāves laika, ieskaitot nepieejamību, veiktspējas apkalpošanu un iejaukšanos pakalpojumu pārvaldībā. Ja šādu regresiju dēļ ir plaša debitora ietekme, kvalitātes atjauninājumu atrite tiks apturēta līdz brīdim, kad mēs varam komunicēt un labot problēmu. Parasti nākamajam kvalitātes atjauninājumam būs nepieciešama izlabošana, lai atsāktu atriti.

Ja tiek ietekmēta viena debitora vide, sazinieties ar Microsoft atbalsta dienestu, lai atvērtu biļeti. Pamatojoties uz pamatojumu, mēs apturam kvalitātes atjauninājumu izriti visām pārējām šī projekta vidēm, līdz problēma ir saasinājama.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Vai debitori joprojām var manuāli lietot labojumfailu atjauninājumus no LCS?
Jā. Lai nodrošinātu notiekošu pārību, kā darbojas labojumfaili, joprojām var pielietot debitora vidēm LCS. Tomēr ir svarīgi atzīmēt, ka labojumfaili, kas ir izvietoti kā daļa no kvalitātes atjauninājuma, atrodas standarta SDP pirms atjaunināšanas izvietošanas. Tas samazina regresiju risku augstākas kvalitātes dēļ. Ieteicams izvēlēties kvalitātes atjauninājumu manuāli pielietojot labojumfailus palielinātai uzticamībai.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Vai debitori proaktīvi var instalēt kvalitātes atjauninājumu būvējumu pirms grafika?
Jā. Jūs varat instalēt kvalitātes atjauninājumu proaktīvi. Microsoft izlaidīs atjauninājumu, ja vides pašreizējā būvējuma versija ir vienāda vai augstāka par attiecīgo kvalitātes atjauninājumu.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Ja videi ir gaidāma plānotā mēneša pakalpojuma atjaunināšana nedēļas laikā, vai tā joprojām saņems kvalitātes atjauninājumus?
- Kvalitātes atjauninājumi nav pielietoti ražošanas vidēs, ja ir gaidāms pakalpojuma atjauninājums, kas ieplānots nedēļas laikā no laika, kad ir plānots veikt kvalitātes atjauninājumu.
- Ja kastītes videi ir tāda pati vai augstāka būvējuma versija nekā gaidāmais kvalitātes atjauninājums, tā tiks izlaista.
- Ja ražošanas videi ir tāda pati vai augstāka būvējuma versija nekā gaidāmais kvalitātes atjauninājums, tas tiks izlaists.
- Ja kastītei ir tāda pati vai augstāka būvējuma versija, jo ražošanai ir kvalitātes atjauninājums vai manuāls atjauninājums, ražošana vēl aizvien saņems mēneša pakalpojuma atjauninājuma ieplānoto versiju. Ja nevēlaties, lai plānotā ražošanas vide tiktu atjaunināta uz pakalpojuma atjaunināšanas versiju, varat pauzēt pakalpojuma atjauninājumu no LCS. 
- Ieteicams izmantot jaunāko kvalitātes atjauninājumu būvējumu, lai pārbaudītu gaidāmā pakalpojuma atjauninājuma izmaiņas, lai uzlabotu stabilitātes un rezultātus.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Ja videi ir gaidāma plānota darbība un ieplānota kvalitātes atjaunināšana vienā un tajā pašā uzturēšanas logā, vai joprojām tiks saņemts kvalitātes atjauninājums?
Ja pastāv jebkādas iepriekš plānotas darbības saturēšanas darbības, piemēram, punktu atjaunošana laikā (PITR), kvalitātes atjaunināšana tiks pārplānota uz nākamo pieejamo uzturēšanas logu četru dienu logā. Plašāku informāciju par grafiku skatiet šeit: Kas [ir proaktīvās kvalitātes atjauninājumu grafiks](#schedule)?. 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Vai vidi var atgriezties iepriekšējā stāvoklī, ja pēc kvalitātes atjaunināšanas ir izejas plūsmas?
Pēc kvalitātes atjaunināšanas atrite netiek atrite jebkuros apstākļos. Ir pieejamas tikai ielāpa uz priekšu vērstas opcijas, lai mazinātu problēmas.

## <a name="what-about-fda-regulation-and-gpx"></a>Kas par FDA noteikumiem un UTX?
Debitoru plāns, uz ko attiecas FDA pārbaude un noteikumi joprojām nav apmierināti. Drīz gaidīt vairāk atjauninājumu šajā vietā. Tagad visi šādi debitori ir atbrīvoti no kvalitātes atjauninājumiem. Lai nodrošinātu, ka debitors atbilst FDA noteikumiem, lūdzu, apmeklējiet [Microsoft Azure UTX piedāvājumu](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Kādas pakalpojuma atjauninājumu versijas šiem kvalitātes atjauninājumiem tiek atbalstītas?
Klienti visās atbalstītās pakalpojuma atjauninājumu versijās apstiprina kvalitātes atjauninājumus. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Finanšu un operāciju programmu izvietošanai ar Retail komponentiem parasti nepieciešams papildu darbs papildus MPOS atkārtotai izvietošanai. Kā šie kvalitātes atjauninājumi ietekmēs RetailSDK? 
Tā kā labojumfaila raksturs nemainās kvalitātes atjauninājumu lietderīgo slodzi, mēs pašlaik ne paredzam nekādu papildu ietekmi, kas pašlaik tiek saistīta ar Retail komponentiem.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Vai mākonī viesotās vides (CHE)? 
Čeku vides ir ārpus sfēras kvalitātes atjauninājumiem, jo tās ir ārpus Microsoft purview

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Ar ko ir saistītas integrācijas problēmas Microsoft Dataverse? 
Nav zināms, ar kvalitāti atjauninājumiem saistītas integrācijas problēmas Dataverse.

