---
title: Proaktīvi kvalitātes atjauninājumi
description: Šajā rakstā ir sniegta informācija par proaktīvu kvalitātes atjauninājumu piegādi.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d417b16706ac4389e40e25ffbbddde5ebac92db3
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775514"
---
# <a name="proactive-quality-updates"></a>Proaktīvi kvalitātes atjauninājumi

[!include[banner](../includes/banner.md)]

Pēdējo gadu laikā Microsoft ir nepārtraukti progresējis attiecībā uz to, ko mēs saucam par [vienu versiju](../../dev-itpro/lifecycle-services/oneversion-overview.md). One Version priekšnoteikums ir vienkāršs: jo tuvāk mēs varam nokļūt pie tā, ka visi klienti izmanto vienu un to pašu programmatūras versiju, jo augstāku kvalitāti mēs varam nodrošināt. Mēs atrodam un novēršam problēmas vienu reizi, un mēs ātrāk saņemam šos risinājumus vairāk klientu rokās.

Šo priekšnoteikumu apstiprina rezultāti: mazāks incidentu skaits mūsu produktos. Ja klienti neizmanto vienu un to pašu versiju, mēs pastāvīgi redzam, ka viņus ietekmē problēmas, kuru risinājums jau ir pieejams. Mēs jau esam panākuši lielu progresu ar Dynamics 365 Finance, Dynamics 365 Supply Chain Dynamics 365 Project Operations un, un Dynamics 365 Commerce, pateicoties jaunākajiem tehniskajiem sasniegumiem, tagad ir iespējams veikt nākamo darbību. Tālāk sniegtajā informācijā ir izklāstīts, ko mēs darīsim, ko mēs jau esam izdarījuši, lai iestatītu skatuvi, un kā un kad mēs bez traucējumiem ieviesīsim jaunās iespējas.

## <a name="what-you-need-to-know"></a>Kas jums jāzina

- Proaktīvi kvalitātes atjauninājumi tiek piemēroti katru mēnesi.
- Microsoft piemēros proaktīvus kvalitātes atjauninājumus visām smilškastes vidēm, kurās darbojas pakalpojuma atjauninājums, kas tika izmantots [, kad tika](./public-preview-releases.md#targeted-release-schedule-dates-subject-to-change) izveidoti proaktīvie kvalitātes atjauninājumi.
- Izņēmumi attiecībā uz proaktīviem kvalitātes atjauninājumiem būs atļauti klientiem, kurus regulē ASV Pārtikas un zāļu pārvalde (FDA).
- Microsoft nosaka, kā proaktīvi kvalitātes atjauninājumi tiks pārvaldīti regulētām vidēm, kā arī valsts un valdības mākoņa klientiem.
- Paziņojumi, kas ir saistīti ar proaktīviem kvalitātes atjauninājumiem, [Microsoft 365 tiek publicēti ziņojumu centrā](https://admin.microsoft.com/AdminPortal/) un reklāmkarogā klienta Microsoft Dynamics dzīves cikla pakalpojumu projektā.
- Piecas dienas pirms proaktīva kvalitātes atjauninājuma lietošanas videi klientiem tiek paziņots, ka atjauninājums notiks.
- Klienti nevar atcelt vai atlikt proaktīvus kvalitātes atjauninājumus.
- Proaktīvi kvalitātes atjauninājumi tiek instalēti reģionam raksturīgā [plānotā uzturēšanas perioda](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) laikā.
- Kvalitātes atjauninājumi ir izstrādāti tā, lai tiem būtu zems problēmu vai regresiju risks, un to atbalsta Microsoft dati.
- Microsoft iesaka mērķtiecīgu testēšanu attiecībā uz noteiktām problēmām vai konkrētiem labojumfailiem, kas ir saistīti ar proaktīvu kvalitātes atjauninājumu.

## <a name="focus-on-quality-updates"></a>Koncentrējieties uz kvalitātes atjauninājumiem

Pašlaik mēs nodrošinām septiņus [pakalpojumu atjauninājumus](public-preview-releases.md) gadā. Piemēram, versija 10.0.29 ir pakalpojuma atjauninājums. Vēl nesen bija astoņi atjauninājumi gadā. Tomēr, reaģējot uz klientu atsauksmēm, mēs atteicāmies no viena atjauninājuma, kas atklāja vēlmi izvairīties no izmaiņām kalendārā gada beigās.

Mēs nemainīsim pakalpojumu atjauninājumu ritmu. Tā vietā mūsu nākamais solis uz priekšu One Version ceļojumā ir vērsts uz *kvalitatīviem atjauninājumiem*. Kvalitātes atjauninājumi ir kumulatīvs labojumfailu būvējums. Tajos nav iekļautas jaunas funkcijas. Jebkurā brīdī visa mūsu klientu kopiena ir sadalīta starp trim vai četriem jaunākajiem pakalpojumu atjauninājumiem. Tomēr jebkuram konkrētam pakalpojuma atjauninājumam grupā var izmantot desmitiem dažādu kvalitātes atjauninājumu versiju atkarībā no datumiem, kad lietotāji tos izvietoja. Nākamajā solī mēs proaktīvi pārraidīsim kvalitātes atjauninājumus. Mēs jau izmantojam šo modeli savām Dataverse lietojumprogrammām un esam redzējuši gaidītos rezultātus, uzlabojot kvalitāti un samazinot atbalsta incidentu skaitu.

Protams, defektu samazināšana varētu samazināt vai pilnībā novērst nepieciešamību pēc kvalitātes atjauninājumiem. Mums ir vairākas iniciatīvas lidojuma laikā, lai samazinātu defektus, kuriem nepieciešami kvalitātes atjauninājumi. Pat tad, ja kvalitātes atjauninājumā tiek samazinātas lietderīgās slodzes, konsekvence visā klientu bāzē uzlabos atbalsta iespējas, ātrāk iegūs uzlabojumus klientiem un samazinās to klientu biežumu, kuri saskaras ar problēmām, kurām jau pastāv risinājumi.

## <a name="making-proactive-distribution-possible"></a>Iespējama proaktīva izplatīšana

Jau ir ieviesti vairāki uzlabojumi, kas ļauj proaktīvi piegādāt kvalitātes atjauninājumus:

- **Gandrīz nulles dīkstāves atjaunināšana** — lai nodrošinātu biežākas vides, ir svarīgi samazināt ietekmi uz vides pieejamību, lai saglabātu Dynamics 365 servisa līmeņa līgumus (SLA). Gandrīz nulles dīkstāves atjaunināšana sākotnēji tika ieviesta, lai palīdzētu uzlabot ikmēneša operētājsistēmas ielāpu, izmantojot klastera kļūmjpārlēci, lai aktivizētu atjaunināto attēlu ar minimāliem traucējumiem. Atjauninājumu piemērošanas mehānisms tiek uzlabots, lai tas būtu vēl mazāk traucējošs, un tas aptvers gan operētājsistēmas ielāpu, gan kvalitatīvu atjauninājumu izvietošanu.

    Interaktīviem lietotājiem aktīvā sesija var tikt pārtraukta, un mēģinājums no jauna tiks veikts tagad atjauninātajā vidē. Ieviešot [uz prioritāti balstītu pakešu plānošanu, pakešu](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) plānošana un apstrāde tiek atjaunota un atsākta tūlīt pēc atjaunināšanas. Uz prioritātēm balstīta pakešu plānošana būs pieejama klientiem, pirms viņi sāks piedalīties proaktīvā kvalitātes atjauninājumu izplatīšanā savai ražošanas videi.

- **Tumšās stundas — tumšās stundas tiek definētas katram Azure reģionam, un gandrīz nulles dīkstāves atjauninājumi tiks veikti tumšās stundas** periodā.

## <a name="the-proactive-update-process"></a>Proaktīvais atjaunināšanas process

Proaktīvu kvalitātes atjauninājumu ieviešana notiks pēc droša izvietošanas procesa (SDP). SDP specifika attīstīsies, bet kvalitātes atjauninājumi sākotnēji tiks izvietoti smilškastes vidē. Palielinoties veiksmīgi izvietoto smilškastu procentuālajam daudzumam, sāksies izvietošana ražošanas vidēs. Klausīšanās sistēmas uzraudzīs sistēmas telemetriju un Livesite incidentus un pārtrauks konkrētas versijas izlaišanu, ja tiks konstatēta regresija. Klienti joprojām varēs izvilkt kvalitātes atjauninājumus pirms proaktīvas izvietošanas, ja viņi to vēlēsies.

Pašreizējie laidienu pārvaldības dati liecina, ka kvalitātes atjauninājumos tiek ieviesti mazāk nekā 3 procenti regresiju. Pastiprināti koncentrējoties uz regresijas novēršanu un uzlabotu SDP, regresiju potenciālā ietekme būs ievērojami zemāka nekā kvalitātes ieguvumi, kas tiek panākti, ātrāk ieviešot labojumus klientiem kopumā.

## <a name="process-changes"></a>Apstrādāt izmaiņas

Pirms proaktīvas kvalitātes atjauninājumu izvietošanas aktivizēšanas tiek ieviesta procesa izmaiņu kopa:

- **Shēma** - Rīki nodrošinās, ka kvalitātes atjauninājumu būvējumi ietver tikai shēmas izmaiņas, kuras var lietot, kamēr pakalpojums ir tiešsaistē. Šī pieeja palīdzēs saglabāt iespēju piemērot atjauninājumu ar gandrīz nulles dīkstāvi.
- **Pastiprināta izmaiņu pārbaude** - Pašlaik jau ir papildu procesa solis, lai apstiprinātu izmaiņas iekļaušanai kvalitātes atjauninājumā. Papildu soļa pārbaude tiks palielināta, lai palīdzētu samazināt regresijas iespējamību. Izmaiņu pārtraukšana nav atļauta kvalitātes atjauninājumos, un pastiprināta izmaiņu pārbaude palīdzēs nodrošināt, ka mēs sasniedzam šo mērķi.
- **Redzamība** — paziņojumi tiek nosūtīti, izmantojot administrēšanas centru, dzīves cikla pakalpojumus un citus pieejamos kanālus, lai saņemtu gaidāmos proaktīvos kvalitātes atjauninājumus. Turklāt atbalsta komandām un incidentu interesentiem būs redzamība, kur kvalitātes atjauninājumi ir proaktīvi izvietoti.

    > [!NOTE]
    > Microsoft saziņas komanda izmeklē pastāvīgu e-pasta rīku degradāciju, kas neļauj piegādāt e-pasta paziņojumus. Lūdzu, turpiniet uzraudzīt ziņojumu centru, Microsoft 365 lai atrastu ar pievienošanu un paziņojumiem saistītus ziņojumus.

- **Fail Safe, izmantojot lidojumu - Flighting tiks izmantots, lai aizsargātu koda izmaiņas, kur vien tas ir piemērojams, kvalitātes atjauninājuma kļūdu labojumā vai izmantojot esošo funkciju,** kas attiecas uz labojumu. Ja pēc proaktīvas izvietošanas ir nepieciešama atkāpšanās vai izmaiņu izslēgšana, to var izdarīt, izmantojot lidojuma sistēmu, lai izvairītos no turpmākām kļūmēm.
- **Smilškastes sinhronizācijas apzīmējums** — mūsdienās mazāk nekā 20 procentiem klientu ir vairākas smilškastes un tiek izvietota viena smilškaste, kur versija atbilst ražošanai, lai palīdzētu novērst problēmas. Ja klients izmanto smilškasti, lai testētu jaunāku versiju nekā viņa produkcija, šī smilškaste saņems jaunākās versijas kvalitātes atjauninājumus.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Kāds ir kvalitātes atjauninājumu ieviešanas ceļvedis?

Paredzams, ka proaktīvu kvalitātes atjauninājumu izplatīšana smilškastes vidēm sāksies 2022. gada septembra beigās vai oktobrī Azure publiskajiem mākoņa klientiem. Izmēģinājuma vides tajā laikā sāks saņemt arī proaktīvu atjauninājumu izvietošanu. Septembrī katram klientam tiks nosūtīts paziņojums, lai informētu viņu par paredzamo grafiku viņu videi. Izņēmumi no proaktīvā atjauninātā izplatīšanas procesa būs atļauti tikai FDA regulētiem klientiem. Mēs joprojām strādājam pie tā, kā tiks pārvaldīta regulēta vide un suverēnie un valdības mākoņa klienti.

Nākamo sešu mēnešu laikā mēs pakāpeniski palielināsim to smilškastes vides procentuālo daļu, kas saņem proaktīvus atjauninājumus, līdz tiks iekļautas visas norādītās vides un tiks veikta ražošanas vides atjaunināšana. Visa perioda laikā mēs veiksim uzraudzību, lai nodrošinātu, ka izvietošanas process ir nevainojams un ka mēs sasniedzam savu mērķi, kas rada netraucētas derīgās kravas.

Tā kā klienti regulāri saņems mazākas derīgās kravas, mēs sagaidām, ka strāvas uzturēšanas process kļūs vienkāršāks. Mēs pielāgosim atjauninājumu izvietošanas biežumu, parādot spēju palaist procesu bez traucējumiem. Šis process jau efektīvi darbojas mūsu Dataverse platformā un lietojumprogrammās un nodrošina gaidītos pakalpojumu kvalitātes uzlabojumus. Mēs ļoti vēlamies spert tādu pašu soli uz priekšu attiecībā uz Finance and Operations lietojumprogrammām.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Kad sāksies kvalitātes atjauninājumi ražošanas vidēm?
Šobrīd kvalitātes atjauninājumi ir vērsti tikai uz smilšu kastēm. Mēs atjaunināsim šo telpu ar ražošanas vides sākuma datumu, kad mums būs konkrētāki dati un metrika, sākot no proaktīviem atjauninājumiem smilškastēm, lai novērtētu gatavību prod.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Kāds ir smilškastes proaktīvo kvalitātes atjauninājumu grafiks?
Informāciju par katra reģiona tumšajām stundām skatiet sadaļā [Kādi ir plānotie uzturēšanas logi pēc reģiona](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)?.

### <a name="proactive-quality-update-release-10028"></a>Proaktīvs kvalitātes atjauninājuma laidiens: 10.0.28
**Lietotnes versija: 10.0.1265.89**  
**Atbilstošais jaunākais KB raksts: 745340**

| Stacija | Reģioni | Pabeigts grafiks| Gaidāmais smilškastes grafiks
|---|---|---|---|
| 1. stacija | Kanāda Centrālā, Kanāda Austrumi, Francija Centrālā, Indija Centrālā, Norvēģija Austrumi, Šveice Rietumi | No 2022. gada 15. septembra līdz 18. septembrim, no 2022. gada 19. septembra līdz 22. septembrim un no 2022. gada 7. oktobra līdz 10. oktobrim | 2022. gada 25. oktobris – 28. oktobris |
| 2. stacija | Francija Dienvidi, Indija Dienvidi, Norvēģija Rietumi, Šveice Ziemeļi, Dienvidāfrika Ziemeļi, Austrālija Austrumi, Apvienotā Karaliste Dienvidi, AAE Ziemeļi, Japāna Austrumi, Austrālija Dienvidaustrumi, Dienvidaustrumāzija | No 2022. gada 25. septembra līdz 28. septembrim un no 2022. gada 7. oktobra līdz 10. oktobrim | 2022. gada 25. oktobris – 28. oktobris |
| 3. stacija | Austrumāzija, Apvienotā Karaliste Rietumi, Japāna Rietumi, Brazīlija Dienvidi, Rietumeiropa, Austrumasv, AAE Centrālā | No 2022. gada 26. septembra līdz 29. septembrim un no 2022. gada 7. oktobra līdz 10. oktobrim | 2022. gada 25. oktobris – 28. oktobris |
| 4. stacija | Ziemeļeiropa, ASV centrālā daļa, ASV rietumi | No 2022. gada 28. septembra līdz 1. oktobrim un no 2022. gada 7. oktobra līdz 10. oktobrim | 2022. gada 25. oktobris – 28. oktobris |
| 5. stacija | DoD, Government Community Cloud, Ķīna | Nav ieplānots | Nav ieplānots |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Proaktīvs kvalitātes atjauninājuma laidiens: 10.0.29
**Lietotnes versija: 10.0.1326.70**  
**Atbilstošais jaunākais KB raksts: 748926**

| Stacija | Reģioni | Pabeigts grafiks | Gaidāmais smilškastes grafiks|
|---|---|---|---|
| 1. stacija | Kanāda Centrālā, Kanāda Austrumi, Francija Centrālā, Indija Centrālā, Norvēģija Austrumi, Šveice Rietumi | 2022. gada 14. oktobris – 17. oktobris, 2022. gada 2. novembris – 5. novembris | 2022. gada 13. novembris – 16. novembris |
| 2. stacija | Francija Dienvidi, Indija Dienvidi, Norvēģija Rietumi, Šveice Ziemeļi, Dienvidāfrika Ziemeļi, Austrālija Austrumi, Apvienotā Karaliste Dienvidi, AAE Ziemeļi, Japāna Austrumi, Austrālija Dienvidaustrumi, Dienvidaustrumāzija | 2022. gada 15. oktobris – 18. oktobris, 2022. gada 2. novembris – 5. novembris | 2022. gada 13. novembris – 16. novembris |
| 3. stacija | Austrumāzija, Apvienotā Karaliste Rietumi, Japāna Rietumi, Brazīlija Dienvidi, Rietumeiropa, Austrumasv, AAE Centrālā | 2022. gada 16. oktobris – 19. oktobris, 2022. gada 2. novembris – 5. novembris | 2022. gada 13. novembris – 16. novembris |
| 4. stacija | Ziemeļeiropa, ASV centrālā daļa, ASV rietumi | 2022. gada 17. oktobris – 20. oktobris, 2022. gada 2. novembris – 5. novembris | 2022. gada 15. novembris – 18. novembris |
| 5. stacija | DoD, Government Community Cloud, Ķīna | Nav ieplānots | Nav ieplānots |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> Proaktīvs kvalitātes atjauninājuma laidiens: 10.0.30
**Lietotnes versija: TBD Atbilstošais jaunākais KB raksts: TBD**
 **·**

| Stacija | Reģioni | Gaidāmais smilškastes grafiks |
|---|---|---|
| 1. stacija | Kanāda Centrālā, Kanāda Austrumi, Francija Centrālā, Indija Centrālā, Norvēģija Austrumi, Šveice Rietumi | 2022. gada 1. decembris – 4. decembris |
| 2. stacija | Francija Dienvidi, Indija Dienvidi, Norvēģija Rietumi, Šveice Ziemeļi, Dienvidāfrika Ziemeļi, Austrālija Austrumi, Apvienotā Karaliste Dienvidi, AAE Ziemeļi, Japāna Austrumi, Austrālija Dienvidaustrumi, Dienvidaustrumāzija | 2022. gada 2. decembris – 5. decembris |
| 3. stacija | Austrumāzija, Apvienotās Karalistes rietumi, Japāna Rietumi, Brazīlija Dienvidi, Ziemeļeiropa, ASV austrumi, AAE Centrālā | 2022. gada 3. decembris – 6. decembris |
| 4. stacija | Rietumeiropa, ASV centrālā daļa, ASV rietumi | 2022. gada 4. decembris – 7. decembris |
| 5. stacija | DoD, Government Community Cloud, Ķīna | Nav ieplānots |

> [!IMPORTANT] 
> Piecas dienas iepriekš Microsoft atjauninās iepriekšējo grafiku un nosūtīs paziņojumu par to vidi kopu, kurām ir plānots saņemt šos kvalitātes atjauninājumus. Iepriekšējais grafiks ir piemērojams tikai tām vidēm, par kurām ir paziņots par gaidāmo atjauninājumu. Informāciju par katra reģiona tumšajām stundām skatiet sadaļā [Kādi ir plānotie uzturēšanas logi pēc reģiona](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)?.
>
> Katrai reģionu grupai vai *stacijai*, kurā pašlaik ir plānots ieviest kvalitātes atjauninājumu, grafiks parāda četru dienu diapazonu. Kvalitātes atjauninājumi sāksies tikai ar smilškastes vidēm. Pēc tam, palielinoties veiksmīgi izvietoto smilškastu procentuālajam daudzumam, izvietošana ražošanas vidēs sāksies ar iepriekšējiem paziņojumiem klientiem.
> 
> Kvalitātes atjauninājumi vienmēr notiks slīdošā veidā, kas ļauj mums mērķēt uz vides kopu pēc grafika un pabeigt visus komplektus līdz stacijas ceturtās dienas beigām. Tomēr tas nenozīmē, ka vides atjauninājums ilgs četras dienas. Tas tikai nozīmē, ka mēs nevaram iepriekš noteikt, kura vides kopa tiks atjaunināta noteiktā dienā četru dienu diapazonā. Visi atjauninājumi tiks veikti tumšajā laikā ar gandrīz nulles dīkstāvi. Atjauninājumi noteikti beigsies konkrētā reģiona tumšās stundas logā.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Kā tiek apstrādāts tumšais darba laiks klientiem, kuriem ir viena Finance and Operations programmu instance, bet kuri ir aktīvi vairākās laika joslās? 
Nav īpašu grafiku ārpus tumšajām stundām, kurās pastāv Finance and Operations programmu instance, jo mēs plānojam ieviest kvalitātes atjauninājumus minimāli traucējošā veidā, izmantojot [nZDT.](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean)

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Kāds ir pašreizējais proaktīvu kvalitātes atjauninājumu ieviešanas ritms?
Proaktīvi kvalitātes atjauninājumi (PQU) pašlaik tiek piegādāti reizi mēnesī katrai atbalstītajai pakalpojuma atjauninājuma versijai. Tikai viens atjauninājums mēnesī tiek virzīts noteiktām smilškastes vidēm, ja vien klienti nepārceļas uz jaunu pakalpojuma atjauninājuma versiju. Tādā gadījumā viņi var saņemt iepriekš ieplānotu PQU kā daļu no esošā vilciena, kas paredzēts jaunajam pakalpojuma atjauninājumam. Pēc tam, kad 2023. gadā tiks pabeigta ieviešana visā pasaulē, šo atjauninājumu biežums palielināsies. Jūs vienmēr saņemsiet vismaz vienu mēnesi ilgu paziņojumu ikreiz, kad tiks mainīts nosūtīšanas kadence.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Kā Microsoft nodrošinās šo atjauninājumu kvalitāti?
Microsoft cenšas nodrošināt laidiena konveijera pietiekamu efektivitāti, lai piegādātu nelielas derīgās kravas un saglabātu zemas validācijas izmaksas. Katrs kvalitātes atjauninājuma labojums iziet stingru un drošu izvietošanas procesu, kas palīdz uzlabot kvalitāti un uzticamību, tādējādi samazinot klientu ietekmi. Izvietošana vispirms notiks pa posmiem smilškastes vidē, kam sekos ražošana. Pakāpeniska izvietošana ļauj veikt pienācīgu uzraudzību, lai noteiktu, vai turpmāka izvietošana ir droša. Mēs pārtrauksim izlaišanu, ja tiks konstatētas problēmas ar katru izvietoto klientu grupu, un nodrošināsim, ka katram izlaišanas solim ir pietiekami daudz laika, lai problēmas varētu parādīties. Katram gaidāmajam kvalitātes atjauninājumam mēs nodrošināsim grafika redzamību, izmantojot publiskās dokumentācijas atjauninājumus un e-pastus, lai klienti varētu plānot uz priekšu.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Vai klienti var aizkavēt, pārplānot vai apturēt kvalitātes atjauninājumu?
Nē. Kvalitātes atjauninājumu galvenais mērķis ir nodrošināt, ka mūsu klientiem nepārtraukti uzlabojas tādi pamati kā drošība, konfidencialitāte, uzticamība, pieejamība un veiktspēja. Atliekot vai pauzējot atjauninājumu, tiks apdraudēta drošība, pieejamība un uzticamība.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Kā es varu zināt, kāda izmaiņu kopa tika iekļauta kvalitātes atjauninājuma lietderīgajā slodzē?
Tālāk norādītās darbības ir pagaidu risinājums, jo mēs turpinām strādāt pie labāka risinājuma nodrošināšanas, lai identificētu to izmaiņu sarakstu, kas nonāk kvalitātes atjauninājuma lietderīgajā slodzē. 

Izmantojiet KB# 745340 10.0.28 kvalitātes atjaunināšanas vilcienam un saistītajai lietotnes versijai 10.0.1265.89.

1. Sadaļā Lifecycle Services atveriet savas smilškastes lapu Detalizēta informācija **par** vidi. 
2. Sadaļā Pieejamie **atjauninājumi** atlasiet **Skatīt atjauninājumu** jaunākajam kvalitātes atjauninājuma būvējumam. 
3. Eksportējiet iebūvēto CSV vai Microsoft Excel failā.
4. Eksportētajā failā kārtojiet informāciju pēc laika (vispirms vecākais) un pēc tam kolonnā Update ID **meklējiet** KB numuru 745340. Tagad jums vajadzētu būt iespējai redzēt KB delta sarakstu.
 
> [!NOTE]
> Eksportēšanai uz CSV vai Excel failu ir jānotiek pirms vides atjaunināšanas. Pretējā gadījumā varat izmantot vidi ar līdzīgu konfigurāciju, kurā nav instalēts atjauninājums, un veikt iepriekš norādītās darbības.

[![Vides piemērs ar kvalitātes atjaunināšanu.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Kāds ir process, ja pēc kvalitātes atjaunināšanas tiek konstatēta kritiska problēma?
Kritiska problēma vai regress ir viens vai vairāki notikumi, kas parasti izraisa vairāku klientu pasliktinātu pieredzi ar vienu vai vairākiem mūsu pakalpojumiem. Šīs problēmas var izraisīt neplānotu dīkstāvi, tostarp nepieejamību, veiktspējas pasliktināšanos un traucējumus pakalpojumu pārvaldībā. Ja šādu regresiju dēļ ir plaša ietekme uz klientiem, mēs pārtrauksim kvalitātes atjauninājuma ieviešanu, līdz varēsim sazināties un novērst problēmu. Parasti nākamajam kvalitātes atjauninājumam būs nepieciešamais labojums, lai atsāktu izlaišanu.

Ja tiek ietekmēta viena klienta vide, sazinieties ar Microsoft atbalsta dienestu, lai atvērtu biļeti. Pamatojoties uz pamatojumu, mēs pārtrauksim kvalitātes atjauninājuma ieviešanu visās citās šī projekta vidēs, līdz problēma tiks mazināta.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Vai klienti joprojām var manuāli lietot labojumfailu atjauninājumus no Lifecycle Services?
Jā. Lai nodrošinātu pastāvīgu paritāti ar to, kā labojumfaili darbojas, labojumfailu atjauninājumus joprojām var lietot klientu vidēs Lifecycle Services. Tomēr ir svarīgi atzīmēt, ka labojumfaili, kas tiek izvietoti kā daļa no kvalitātes atjauninājuma, pirms atjauninājuma izvietošanas iziet cauri standarta SDP. Tas samazina regresijas risku augstākas kvalitātes dēļ. Lai palielinātu uzticamību, ieteicams izvēlēties kvalitātes atjauninājumu, nevis manuāli lietot labojumfailus.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Vai klienti var proaktīvi instalēt kvalitātes atjauninājumu veidošanu pirms grafika?
Jā. Jūs varat proaktīvi instalēt kvalitātes atjauninājumu. Microsoft izlaidīs atjauninājumu, ja vides pašreizējā būvējuma versija ir vienāda vai augstāka par attiecīgo kvalitātes atjauninājumu.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Ja videi nedēļas laikā ir gaidāms plānots ikmēneša pakalpojuma atjauninājums, vai tā joprojām saņems kvalitatīvus atjauninājumus?
- Kvalitātes atjauninājumi netiek lietoti ražošanas vidēm, ja ir ieplānots gaidāms pakalpojuma atjauninājums nedēļas laikā no dienas, kad ir ieplānots kvalitātes atjauninājums.
- Ja smilškastes videi ir tāda pati vai augstāka būvējuma versija nekā gaidāmajam kvalitātes atjauninājumam, tā tiks izlaista.
- Ja ražošanas videi ir tāda pati vai jaunāka būvējuma versija nekā gaidāmajam kvalitātes atjauninājumam, tā tiks izlaista.
- Ja smilškastei ir tāda pati vai jaunāka būvējuma versija kvalitātes atjauninājuma vai manuāla ražošanas atjauninājuma dēļ, ražošana joprojām saņems ikmēneša pakalpojuma atjauninājuma plānoto versiju. Ja nevēlaties, lai ieplānotā ražošanas vide tiktu atjaunināta uz pakalpojuma atjaunināšanas versiju, varat pauzēt pakalpojuma atjauninājumu no Lifecycle Services. 
- Mēs iesakām izmantot jaunāko kvalitātes atjauninājuma būvējumu, lai pārbaudītu izmaiņas gaidāmajam pakalpojuma atjauninājumam, lai nodrošinātu labāku stabilitāti un rezultātus.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Ja videi ir gaidāma ieplānota darbība un plānots kvalitātes atjauninājums tajā pašā uzturēšanas periodā, vai tā joprojām saņems kvalitātes atjauninājumu?
Ja rodas strīdi par iepriekš ieplānotu darbību, piemēram, punkta laika atjaunošanu (PITR), kvalitātes atjauninājums tiks pārplānots uz nākamo pieejamo uzturēšanas periodu četru dienu logā. Papildinformāciju par grafiku skatiet sadaļā [Kāds ir proaktīvu kvalitātes atjauninājumu grafiks?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Vai vidi var atgriezt iepriekšējā stāvoklī, ja rodas problēmas pēc kvalitātes atjauninājuma lietošanas?
Pēc kvalitātes atjauninājuma piemērošanas nekādā gadījumā netiek atcelts. Problēmu mazināšanai ir pieejamas tikai ielāpa pārsūtīšanas iespējas.

## <a name="what-about-fda-regulation-and-gpx"></a>Kā ar FDA regulējumu un GPX?
Plāns klientiem, uz kuriem attiecas FDA validācija un regulējums, joprojām attīstās. Drīzumā sagaidiet vairāk atjauninājumu šajā telpā. Pagaidām visi šādi klienti ir atbrīvoti no kvalitātes atjauninājumiem. Lai pārliecinātos, ka klients atbilst FDA noteikumiem, lūdzu, apmeklējiet GPX [Microsoft Azure piedāvājumu](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Kādas pakalpojumu atjauninājumu versijas tiek atbalstītas šiem kvalitātes atjauninājumiem?
Klienti visās atbalstītajās pakalpojumu atjauninājumu versijās ir tiesīgi saņemt kvalitatīvus atjauninājumus. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Finance and operations programmu izvietošanai ar mazumtirdzniecības komponentiem parasti ir nepieciešams papildu darbs papildus MPOS atkārtotai izvietošanai. Kā šie kvalitātes atjauninājumi ietekmēs mazumtirdzniecības SDK? 
Tā kā paša labojumfaila raksturs nemainās kvalitātes atjauninājumu lietderīgajā slodzē, mēs pašlaik neparedzam nekādu papildu ietekmi, kas īpaši saistīta ar mazumtirdzniecības komponentiem.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Vai ir kāda ietekme uz mākoņa viesoto vidi (CHE)? 
Augstākās izglītības nodaļas vides ir ārpus kvalitātes atjauninājumu tvēruma, jo tās ir ārpus korporācijas Microsoft darbības jomas.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Vai ir kādas integrācijas problēmas ar Microsoft Dataverse? 
Nav zināmu integrācijas problēmu kvalitātes atjauninājumiem ar Dataverse.

