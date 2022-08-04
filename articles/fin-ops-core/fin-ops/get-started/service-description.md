---
title: Pakalpojuma apraksts finanšu un operāciju programmām
description: Šajā rakstā ir sniegts pakalpojuma apraksts finanšu un operāciju programmām.
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 9e5160cc3961703475ffb8dc4a4daf2ae872aaba
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124932"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Pakalpojuma apraksts finanšu un operāciju programmām

[!include[banner](../includes/banner.md)]

Finanšu un operāciju programmas ir uzņēmuma resursu plānošanas (Enterprise Resource Planning — ERP) programmatūra, kas ir pakalpojuma (SAAS) piedāvājumi, kas ir veidoti [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). Finanšu un operāciju pakalpojums nodrošina organizācijas ar ERP funkcionalitāti, kas atbalsta to unikālās prasības un palīdz tām mainīt biznesa vides, nepieprasot pārvaldīt infrastruktūru. Finanšu un operāciju programmas var ietvert vienu vai vairākus no šiem risinājumu apgabaliem:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Kopā ar [biznesa inteliģences](/power-bi/fundamentals/power-bi-service-overview), [infrastruktūras](https://azure.microsoft.com/global-infrastructure/), [skaitļošanas](/azure/service-fabric/service-fabric-overview) un [datu bāzes pakalpojumiem](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) šīs lietojumprogrammas ļauj organizācijām darbināt nozarei specifiskus un darbības biznesa procesus. Debitori, kurus atbalsta ieviešanas partneris, nosaka tās biznesa lietojumprogrammas loģikas konfigurāciju, kas vislabāk atbilst viņu unikālajiem biznesa procesiem. Funkcionalitāti un biznesa procesus var paplašināt vai paplašināt, izmantojot vienu no šiem risinājumiem vai to kombināciju:

- Iebūvēta [personalizēšanas pieredze](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md) rīki
- [Visual Studio](https://visualstudio.microsoft.com)– finanšu un [operāciju programmatūras izstrādes komplekts (SDK) un automatizācijas](../../dev-itpro/dev-tools/developer-home-page.md)[Azure DevOps būvējumam](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Neatkarīga programmatūras izstrādātāja (ISV) risinājumi no [AppSource](https://appsource.microsoft.com/partners)

Pamatojoties uz prasībām, debitori izvēlas savu risinājumu pieeju. Viņi sadarbojas ar ieviešanas partneri, lai definētu, izstrādātu un pārbaudītu to risinājumu, izmantojot rīkus un paraugpraksi, kas sniegti pakalpojumos [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). Ir četri parastie scenāriji:

- Standarta finanšu un operāciju programmas "ārpus kastes" konfigurācija (nav paplašinājumu)
- Finanšu un operāciju programmu konfigurācija, kas ietver vienu vai vairākus ISV risinājumus
- Finanšu un operāciju programmu konfigurācija, kas ietver vienu vai vairākus klientam raksturīgus paplašinājumus
- Finanšu un operāciju programmu konfigurācija, kas ietver debitoram specifisku paplašinājumu un viena vai vairāku ISV risinājumu kombināciju

Organizācijas var pieskaņot viņu biznesa izaugsmi, vienkārši pievienojot lietotājus un biznesa procesus caur vienkāršu, pārskatāmu abonementa modeli. Plašāku informāciju skatiet [Dynamics 365 licencēšanas rokasgrāmatā](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Darbības modelis

Finanšu un operāciju programmu darbības modelis nosaka specifiskas lomas un atbildību debitoram, ieviešanas partnerim un korporācijai Microsoft visā pakalpojuma dzīves ciklā. Papildinformāciju skatiet [Mākoņa operācijas un apkalpošana](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Debitoru darbības

Klienti strādā ar savu partneri [un Microsoft FastTrack](/dynamics365/fasttrack/)[pēc Dynamics 365](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide) ieviešanas rokasgrāmatas, struktūras un rīkiem un labākās prakses veidnēm, [Success by Design](/dynamics365/fasttrack/success-by-design-overview)[kas sniegtas Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md), lai ieviestu savu risinājumu. Parastās aktivitātes ietver:

- Lietotāju identitātes un drošības pārvaldība
- Biznesa procesu definēšana, izstrādāšana un pārvaldība
- Definēt, izstrādāt, pārbaudīt un pārvaldīt paplašinājumus
- Pārraudzīt un pārvaldīt ar ražošanu nesaistītās izvietošanas
- Pārvaldīt programmu atjauninājumus un pārbaudīt paplašinājumus
- Pārvaldīt ISV risinājumus un 3. pušu integrācijas

### <a name="microsoft-responsibilities"></a>Microsoft atbildība

Microsoft pārvalda finanšu un operāciju pakalpojumu, izvietojot, aktīvi pārraugot un apkalpošanas debitoru kastē un ražošanas vides Microsoft SaaS abonementā. Šī pārvaldība ietver nepieciešamo sistēmas infrastruktūru izveidi, lai palaistu pakalpojumu un proaktīvi sazinātos ar klientiem par pakalpojuma darbspēju. Pienākumi ietver:

**Infrastruktūras pārvaldība**
- Drošība un izolēšana
- Operētājsistēmas un virtualizācija
- Serveri, uzglabāšana un noliktava
- Datu centra jauda, tīklošana, dzesēšana

**Programmas platformas pārvaldība**
- 24/7 pieteikuma pārraudzība un paziņojumi
- Diagnostika, platformu atjauninājumi, ielāpi, pakalpojumu atjauninājumi
- Lietojumprogrammas maršrutēšana, noslodzes līdzsvarošana, vietas replicēšana
- Vides nodrošināšana un pārvaldība
- Datu bāzes pārvaldība, augsta pieejamība (high availability - HA)/ārkārtas atgūšana (disaster recovery - DR), mērogs, operācijas
- Skaitļot izvietošanu, mērogošanai un mērogošanai

## <a name="system-configuration"></a>Sistēmas konfigurācija

Finanšu un operāciju programmu mērogs atbilstoši darījuma apjomam un lietotāja noslodzei. Katra debitora ieviešana rada unikālu risinājumu, kas sastāv no šādiem elementiem:

- **Datu sastāvs** – unikāla parametru kopa, kas kontrolē uzvedību, organizācijas izkārtojumu, pamatdatu struktūru (piemēram, finanšu un krājumu dimensijas) un darbību izsekošanas granularitāti.
- **Paplašinājums un konfigurācija** – paplašinājuma mehānismi, kas izmanto kodu paplašinājumus, ISV risinājumus un unikālas konfigurācijas, kas ietver darbplūsmas, integrācijas un pārskatu konfigurācijas.
- **Lietojuma modeļi** – unikāla tiešsaistes un pakešveida lietošanas kombinācija kopā ar spēju integrēties ar augšupstraumes un lejupstraumes sistēmām vienotai datu plūsmai un spēju diferencēt, balstoties uz informācijas skatījumiem, ko klienti izmanto saviem biznesa procesiem.

Sistēma Microsoft konfigurē debitora ražošanas vides, kas ir lieluma, lai apstrādātu darbību apjomus un lietotāja vienlaicīgumam. Microsoft ir atbildīgs par šādiem uzdevumiem:

- Pareizi sadaliniet ražošanas vides resursus, balstoties uz debitora profilēšanas informāciju [LCS abonementa novērtēšanā](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Nepārtraukti uzraudzīt un diagnostiku ražošanas vides pakalpojumu pieejamībai
- Sistēmas veiktspējas problēmu analizēšana un traucējummeklēšana ar finanšu un operāciju programmām

Lai nodrošinātu, ka ieviešana ir konfigurēta augstas veiktspējas vajadzībām, debitoriem ir jāveic šie uzdevumi:

- Nodrošiniet precīzu informāciju par finanšu un operāciju ieviešanu [LCS abonementa novērtējumā](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Izveidojiet un pārbaudiet paplašinājumus veiktspējai un apjomam.
- Atbilstoši pārbaudiet datu konfigurācijas veiktspējai.
- Pārliecinieties, vai ir mērogojams, veicot [veiktspējas pārbaudi](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) pirms uzturēšanās.

## <a name="onboarding-and-implementation"></a>Pievienošana un ieviešana

Tabulā redzami tipiskas uzņēmuma darbības un ieviešanas notikumi.

| Pieprasīt | Paredzētā Microsoft darbība | Sagaidāmā debitora/ieviešanas partnera darbība |
|---|---|---|
| Sākotnējais piedāvājuma pirkums | LCS projekts tiek izveidots pēc piedāvājuma pirkšanas, pamatojoties uz notikumu, ko izraisījis debitors. | Dodieties caur uzņēmuma līguma (Enterprise Agreement - EA) vai mākoņa risinājumu nodrošinātāja (Cloud Solution Provider - CSP) [tirdzniecības procesu](before-you-buy.md). Partneris debitoram izveido nomnieku, ja piemērojams. |
| Pievienojumprogramma pirkšanai | Piešķirt debitoram piekļuvi pievienojumprogrammai, kas atlasīta ieviešanas laikā. | Nav attiecināms |
| Ieviešanas plānošana un analīze | Nodrošiniet atbilstošus rīkus LCS, piemēram, [Biznesa procesu modelētājs (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) un [atbilstība ar Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Veiciet projekta plānošanu, iestatiet Azure DevOps, pabeidziet sistēmu darbu izpildē un iestatiet administratora kontus. |

Papildinformāciju skatiet sadaļā [Īstenošanas projekta iesniegšana](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globalizācija

Finanšu un operāciju programmas ir apkalpotas no vairākiem Azure reģioniem visā pasaulē. Finanšu un operāciju programmas nodrošina funkcionalitāti, lai atbalstītu dažādas valstis/reģionus un dzimtās valodas. Papildinformāciju skatiet [lokalizācijas un regulēšanas līdzekļi](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Valstij/reģionam specifiski apsvērumi

- Klientiem saistīto nozari vai komerciālās organizācijās, kas veic darījumus ar entītijām Francijā, kam nepieciešami lokālie dati, jāpārskata [Finanses un operācijas Francijā](../../dev-itpro/deployment/france-local-deployment.md).
- Debitoriem, kuriem ir operācijas Ķīnā, ir jāpārskata [Azure Ķīnā lietotā tiešsaistes](/azure/china/)[grāmata, finanses un operācijas, ko nodrošina 21Vianet Ķīnā lietotā versija](../../dev-itpro/deployment/china-local-deployment.md).
- Debitoriem, kuriem ir operācijas Krievijā, jāpārskata [Krievijas personas datu lokalizācijas likums](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Vispārīgā datu aizsardzības regula (VDAR)

Finanšu un operāciju programmām Microsoft darbojas kā procesors. Finanses un operācijas kā datu procesors nodrošina procesus un līdzekļus, kas palīdz klientiem izpildīt GDPR saistības kā datu kontrolleri. Plašāku informāciju skatiet [VDAR pārskats](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Vide un datu pārvaldība

Šajā sadaļā aprakstīti daži tipiski vides un datu pārvaldības notikumi, kas rodas pakalpojumā.

### <a name="environment-and-data-management-events-for-production-instances"></a>Vides un datu pārvaldības notikumi ražošanas instancēm

LCS nodrošina [pašapkalpošanās rīkus](../../dev-itpro/deployment/infrastructure-stack.md) un [datu bāzes kustības darbības](../../dev-itpro/database/dbmovement-operations.md), kas tiek izmantotas vides un datu pārvaldības uzdevumu veikšanai. Daži piemēri:

**Notikums:** [Ražošanas instances pieprasījums](../imp-lifecycle/go-live-faq.md#when-can-i-configure-and-request-my-production-environment)

- Izpildiet [Go-Live gatavības](../imp-lifecycle/prepare-go-live.md) pārskatu un iesniedziet to [Microsoft FastTrack](/dynamics365/fasttrack/) komandai.
- Pirms pieprasāt ražošanas instanci, pabeidziet [LCS](../../dev-itpro/lifecycle-services/subscription-estimator.md) abonementa novērtējumu.
- Veiciet visus ieviešanas uzdevumus, kas norādīti [LCS metodoloģijā](../../dev-itpro/lifecycle-services/create-methodology.md).

**Notikums:** [Smilškastes datu bāzes kopēšana ražošanas instancē](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Tiek izpildīts kā nepatiesa tiešsaites vai faktiskā tiešsaites pārslēgšana.

**Notikums:** [Uzturēšanas režīms](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Ieslēdziet uzturēšanas režīmu LCS.
2. Pabeidziet nepieciešamo uzturēšanu.
3. Izslēdziet uzturēšanas režīmu LCS.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Vides un datu pārvaldības notikumi neražošanas instancēm

LCS nodrošina [pašapkalpošanās nodrošināšana](../../dev-itpro/deployment/infrastructure-stack.md) un [datu bāzes kustības darbības](../../dev-itpro/database/dbmovement-operations.md), kas tiek izmantotas vides un datu pārvaldības uzdevumu veikšanai. Daži piemēri:

**Notikums:** [Jaunas smilškastes instances izvietošana](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Pārliecinieties, ka visas nepieciešamās instances ir [ieplānotas](../imp-lifecycle/environment-planning.md) un ka ir iegādāti piemērojamie pievienojumprogrammu piedāvājumi.
- Palaist izvietošanas procesu LCS.
- Pabeidziet visus uzdevumus, kas norādīti LCS kontrolsarakstos.
    
>[!NOTE]
>Izstrādes smilškastes vide ir virtuālā mašīna (VM), kas ir [izvietota debitora Azure abonementā](../../dev-itpro/dev-tools/access-instances.md) un ko pārvalda debitors.

**Notikums:** [Zelta konfigurācijas datu bāzes kopēšana no smilškastes uz ražošanu](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Tiek izpildīts kā nepatiesa tiešsaites vai faktiskā tiešsaites pārslēgšana.

**Notikums:** [Ražošanas punkta laika dublējuma atjaunošana instancei, kas nav ražošanas instance](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Palaidiet [Datu bāzes atsvaidzināšanas](../../dev-itpro/database/database-refresh.md) opciju LCS.
- Pēckopija: dzēsiet vai aptumšojiet jutīgos datus, izmantojot skriptus, pielāgojiet vides raksturīgās programmas konfigurācijas (piemēram, integrācijas galapunktus) un iespējojiet vai pievienojiet lietotājus. Ievērojiet, ka šīs izmaiņas tiek veiktas, lietojot [datu pakotni](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Notikums:** [Datu bāzes, kas nav ražošanas instance, atjaunošana laikā](../../dev-itpro/database/database-point-in-time-restore.md)

- Apstipriniet, ka procesu nevar atsaukt.
- Palaidiet laika brīdi atjaunoto operāciju LCS.

**Notikums:** 2. pakāpes vadīklu datu bāzes kopēšana izstrādes smilškastē problēmu novēršanai un [atkļūdošanai](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Palaidiet datu bāzes eksporta operāciju LCS 2. pakāpes smilškastes vidē.
- Importējiet un atjauniniet datu bāzi izstrādes vidē.

## <a name="data-backup-and-retention"></a>Datu dublēšana un saglabāšana

Datu bāzes finanšu un operāciju vidēm SAA abonementā ir aizsargātas ar automātisku dublējumu. Ražošanas vidēs automātiskās dublējumkopijas tiek saglabātas 28 dienas, ja vien Microsoft neveic atriti. Smilškastes (pakāpe 2+) vidēs tās tiek saglabātas septiņu dienu laikā. Ražošanas vides atrite var tikt veikta, ja jebkura plānotās apkopes atjaunināšanas laikā rodas kļūme.

Papildinformāciju par automātisko dublējumu skatiet sadaļā [Automatizētās dublējumkopijas — Azure SQL datu bāze & SQL pārvaldīta instance](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Pakalpojuma darbības pienākumi

Tabulā ir aprakstīti daži tipiski pakalpojuma scenāriji un darbības. Tas arī norāda, vai korporācija Microsoft, debitors vai gan korporācija Microsoft, gan debitors atbild par aktivitātēm.

| Aktivitāte | Microsoft atbildība | Klienta atbildība |
|---|---|---|
| **Nodrošinājuma sākotnējie nomnieki** | | |
| Izmēriet prognozēto noslodzi LCS, izmantojot abonementa novērtējuma rīku, un pieprasiet nodrošināt noteiktas vides. | | X |
| Nodrošināt visas ražošanas instances un gadījumus, kas nav ražošanas gadījumi. | X | |
| Validēt izvietotās ražošanas instances un gadījumus, kas nav ražošanas gadījumi. | | X |
| **Pakalpojuma atjauninājumi** | |
| Piemērojiet pakalpojumu atjauninājumus norādītajām ar ražošanu saistītām un nesaistītām instancēm. | X | |
| Manuāli piemērojiet pakalpojumu atjauninājumus no LCS smilškastes instancēm. Definējiet, izstrādājiet, pārbaudiet atjauninājumu un nodrošiniet koda atjaunināšanas pakotni atpakaļ uz LCS. | | X |
| Pieprasiet un ieplānojiet, lai ražošanas instancei tiktu lietoti paplašinājuma atjauninājumi. | | X |
| Izveidojiet kodu un datu dublējumu ražošanas instancei pirms jebkādu atjauninājumu lietošanas. | X | |
| Jebkuras kļūmes gadījumā atritiniet ražošanas instanci uz kodu un datu dublējumu. | X | |
| **Datu pārvaldība (dublēšana, atjaunošana un atjaunināšana)** | | |
| Datu bāzes dublējumkopija. | X | |
| Nosakiet augstu pieejamību un ārkārtas atgūšanas plānu. | X | |
| Pārraudzīt ražošanas instances datu bāzes veiktspēju. | X | |
| Lai nodrošinātu veiktspēju, noregulējiet ražošanas instanču datu bāzi. | X | |
| Veiciet ražošanas instances datu bāzes laicīgu atsvaidzināšanu instancei, kas nav ražošanas instance. | | X |
| **Infrastruktūras atjaunināšana** | | |
| Plānot regulārus infrastruktūras atjauninājumus. | X | |
| **Mērogošana uz augšu un uz leju (lietotāji, noliktava un instances)** | | |
| Papildus lietotāju un ar ražošanu nesaistījušo pievienojumprogrammu iegāde. | | X |
| Atjauniniet lietošanas izmaiņas LCS abonementa novērtējuma rīkā. | | X |
| Ziņojiet par jebkādām nozīmīgu veiktspējas problēmām, kas ietekmē pakalpojuma izmantošanu. | | X |
| Proaktīvi pārvaldiet resursus, kas ir nepieciešami piemērojamam pakalpojumam. | X | |
| Izpētīt un novērst incidentus; | X | |
| **Drošība (lietotāja piekļuve)** | | |
| Nodrošiniet lietotāja piekļuvi pakalpojumam. | | X |
| Nodrošiniet LCS projekta piekļuvi to instanču pārvaldībai un darbībai, kas izvietotas, izmantojot LCS. | | X |
| **Ražošanas instanču pārraudzība** | | |
| Ražošanas instanču pārraudzība 24/7. | X | |
| Proaktīvi paziņojiet debitoram par incidentiem, kuros ir iesaistīts ražošanas gadījums. | X | |
| **Ar ražošanu nesaistījuču instanču pārvaldība un pārraudzība** | | |
| Pārvaldīt instances, kas nav ražošanas instances, izmantojot LCS. | | X |
| Pārraudzīt ar ražošanu nesaistītus instances. | | X |

## <a name="service-update-strategy"></a>Pakalpojuma atjauninājuma sretēģija

Saskaņā ar programmatūras [dzīves cikla](../../dev-itpro/migration-upgrade/versions-update-policy.md) politiku finanšu un operāciju programmas seko Microsoft [Modern Lifecycle Policy](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), kas attiecas uz precēm, kas ir pastāvīgi apkalpotas un atbalstītas. 

Microsoft katru gadu atbrīvo astoņas finanšu un operāciju programmas pakalpojuma atjauninājumus šādos mēnešos:

- Janvāris
- Februāris
- Aprīlis
- Maijā
- Jūlijā
- Augustā
- Oktobrī
- Novembrī

>[!NOTE]
>Aprīlis un oktobris ir galvenie līdzekļu laidieni. Klienti var apturēt atsevišķu pakalpojuma atjauninājumu līdz trim secīgiem atjaunināšanas cikliem.

Papildinformāciju skatiet tālāk norādītajās tēmās:

- [One Version pakalpojuma atjauninājumu pārskats](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Pakalpojumu atjauninājumu konfigurēšana, izmantojot LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Pakalpojumu atjauninājumu apturēšana, izmantojot LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Paziņojumu saņemšana par pakalpojumu atjauninājumiem, izmantojot LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regresiju testēšanas rīki pakalpojuma atjauninājumu pārbaudei](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 kopumi un laidieni](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Drošība un administratīvā piekļuve

Administratīvā piekļuve finanšu un operāciju ražošanas videi ir stingri kontrolēta un reģistrēta. Klienta dati tiek apstrādāti saskaņā ar [Microsoft tiešsaistes pakalpojumu noteikumiem](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Debitora administratīvās piekļuves tiesības

Debitora nomnieka administrators var piekļūt ražošanas instancēm vai instancēm, kas nav ražošanas instances, kā aprakstīts šajā tabulā:

| Vides veids | Nolūks | Debitora piekļuves līmenis |
|---|---|---|
| **Ar ražošanu nesaistīts**<br>1. pakāpes smilškaste | Vide, kas nav ražošanas vide, ko klienti izvieto izstrādes, demonstrācijas vai apmācības nolūkos. | 1. pakāpes smilškaste (tiek saukta arī par mākonī viesotu vidi) ir debitora pārvaldīta VM, kas ir izvietots debitora Azure abonementā no LCS. Tā kā debitora Azure abonements ir VM, debitoram ir pilna administratīvā piekļuve videi, izmantojot attālo darbvirsmu. |
| **Ar ražošanu nesaistīts**<br>2. pakāpes (vai augstāka) smilškaste | Vide, kas nav ražošanas vide, ko debitori izmanto lietotāju pieņemšanas pārbaudei, integrācijas testēšanai, apmācībai, sagatavošanai vai jebkuram citam pirms produkcijas scenārijam. | 2. pakāpe un citas rūtiņas tiek izvietotas finanšu un operāciju SaaS abonementā. Piekļuve Azure SQL datu bāzēm, kas ir saistītas ar ne produkcijas vidi, tiek piešķirtas, izmantojot [piekļuvu laikā](../../dev-itpro/database/database-just-in-time-jit-access.md). Attālās darbvirsmas piekļuve nav pieejama. |
| **Ražošana** | Ražošanas vide tiek izvietota, kad projekts ir [gatavs sākotnējai izvietošanai](../imp-lifecycle/environment-planning.md#production-system-readiness). | Ražošanas vides tiek izvietotas SaaS abonementā. Visa piekļuve ir caur pārlūku, pakalpojuma galapunktiem vai LCS. |

### <a name="microsoft-administrative-access"></a>Microsoft administratīvās piekļuves tiesības

Tabulā ir parādīti dažādie piekļuves līmeņi dažādiem Microsoft administratoriem:

| Administrators | Debitora dati |
|---|---|
| Operāciju atbilžu grupa<br>(Ierobežots tikai atslēgas personālam) | Piekļuve tiek piešķirta ar atbalsta biļeti. Piekļuve ir auditēta un ierobežota līdz atbalsta aktivitātes ilgumam. |
| Microsoft klientu atbalsta pakalpojumi (CSS) | Nav tiešās piekļuves. Debitors var izmantot ekrāna koplietošanu, lai strādātu ar atbalsta personālu, lai atkļūdotu problēmas. |
| Tehnika | Nav tiešās piekļuves. Darbību atbilžu grupa var izmantot ekrāna koplietošanu, lai strādātu ar tehnoloģiju un atkļūdotu problēmas. |
| Citi programmā Microsoft | Nav piekļuves. |

## <a name="monitoring"></a>Pārraudzīšana

Korporācija Microsoft ir daudzpusēja rīku kopā, lai pārraudzītu un veltītu debitoru ražošanas instances. Microsoft uzrauga klientu ražošanas vides 24 stundas dienā, 7 dienas nedēļā. Papildinformāciju skatiet sadaļā [Ražošanas atbalsts un pārraudzība](../imp-lifecycle/production-support-monitoring.md).

| Microsoft atbildība | Debitora atbildība |
|---|---|
| <ul><li>Pārraudzīt pakalpojuma pieejamību.</li><li>Pastāvīgi uzraugiet un brīdināt, izmantojot darbspējas rādītājus un datu apstrādes kritiskos komponentus, piemēram, Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce un Management Reporter.</li><li>Uzraugiet veiktspēju, ko izraisa infrastruktūras pakalpojumi (piemēram, Azure Active Directory \[Azure AD\] un Azure SQL).</li><li>Ja Korporācija Microsoft nosaka, ka atsevišķs process vai pakešuzdevums izraisa sabrīdzēšanu, šis process vai darbs tiks pārtraukts pēc saziņas ar klientu.</li></ul> | <ul><li>Pārraudzīt izmaiņas programmas konfigurācijās un paplašinājumos, kas var izraisīt funkcionalitātes un veiktspējas problēmas.</li><li>Lietošanas kļūdas ir jādiagnosticē, izmantojot monitoringa rīkus. Izmantojiet šos rīkus, lai lietotāja ziņotās veiktspējas izmaiņas izmantotu.</li><li>Informējiet Microsoft, ja sistēmā ir paredzama noslodze, kas ir ārpus prognozētās noslodzes.</li><li>Ja attiecīgajā ražošanas instancē pakalpojums nav pieejams, debitors var izmantot LCS, lai ziņotu par [ražošanas zaudējumu](../../dev-itpro/lifecycle-services/report-production-outage.md).</li></ul> |

Iesniedzot atbalsta pieprasījumus tiešsaistē, izmantojot LCS, debitori ļauj korporācijai Microsoft ātri un padziļināti sniegt tehnisko zināšanas vislietīgāk un efektīvāk. Kaut arī tālruņa opcija ir pieejama, tā jāizmanto tikai tad, ja tiešsaistes opcija nav pieejama. Papildinformāciju skatiet tēmā [Tālruņa atbalsta opcijas](/power-platform/admin/support-overview?toc=%2Fdynamics365%2Ffin-ops-core%2Fdev-itpro%2Ftoc.json&bc=%2Fdynamics365%2Fbreadcrumb%2Ftoc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Incidentu pārvaldība

Microsoft atbild uz un labo incidentus, ņemot vērā nozīmīguma līmeņus. Sākotnējās incidenta novērtēšanas laikā Microsoft incidenta smaguma līmeņus var mainīt, un, tā kā kļūst pieejama plašāka informācija par ietekmi un tvērumu. Ja incidents tiek samazināts, incidenta stingrība netiek mainīta.

Papildinformāciju par nozīmīguma līmeņiem skatiet [šajā nozīmīguma tabulā](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Biznesa nepārtrauktība, izmantojot augstu pieejamību un ārkārtas atgūšanu 

Korporācija Microsoft nodrošina biznesa nepārtrauktību un ārkārtas atgūšanu finanšu un operāciju programmu ražošanas gadījumiem Azure reģiona plašu zaudējumu gadījumā. Papildinformāciju, iekļaujot pakalpojuma atgūšanas laika mērķi (RTO) un atgūšanas punkta uzdevumu (RPO), skatiet biznesa [nepārtrauktību un ārkārtas atgūšanu](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Augsta pieejamība** - HA funkcionalitāte nodrošina veidus, kā novērst dīkstāves laiku, ko izraisa viena zara kļūme Azure datu centrā. Katra pakalpojuma mākoņa arhitektūrā tiek izmantotas Azure pieejamības kopas skaitļošanas pakāpei, lai novērstu viena punkta kļūmes notikumus. HA datu bāzēm ir nodrošināts, izmantojot [Azure SQL HA līdzekļus](/azure/azure-sql/database/high-availability-sla).
- **Parādu atgūšana** – [Azure katastrofas seku likvidēšanas līdzekļi](/azure/best-practices-availability-paired-regions) aizsargā katru pakalpojumu pret pārtraukumiem, kas plaši ietekmē visu Azure datu centru. Tālāk ir norādītas dažas no šiem līdzekļiem:

    - Azure SQL aktīvās ģeogrāfiskā replicēšanas funkcija primārajai datu bāzei (biznesa datu bāze).
    - Azure BLOB krātuves ģeogrāfiskā liekā kopija (kurā ir dokumentu pielikumi) citos Azure reģionos.
    - Azure SQL un Azure Blob Storage replicēšanas sekundārais reģions.

Ja ārkārtas atgūšana tiek izmantota, lai atkoptu debitora ražošanas instanci, Microsoft un debitors izpildīt savus [incidenta pārvaldības](service-description.md#incident-management) pienākumus.

Microsoft parādu atgūšanas plāni un procedūras tiek regulāri pārbaudīti, izmantojot sistēmas un organizācijas kontroles (SOC) auditus. Šie atbilstības auditi apstiprina Microsoft DR tehnisko un procedurālo procesu, tostarp Dynamics 365 finanšu un operāciju programmas. [SOC atbilstība](/compliance/regulatory/offering-soc-2) audita pārskati un visi citi saskaņotības pārskati ir pieejami [Microsoft drošības centra saskaņotības piedāvājumos](/compliance/regulatory/offering-home).

## <a name="finance-and-operations-support-offerings"></a>Finanšu un operāciju atbalsta piedāvājumi

Tehniskais atbalsts ir pieejams tirgū, kur tiek piedāvāti finanšu un operāciju pakalpojumi. [Atbalsta pieredze ir](../../dev-itpro/lifecycle-services/lcs-support.md) sniegta LCS vai finanšu un operāciju programmās. Daži piemēri:

- [Problēmu meklētājs](../../dev-itpro/lifecycle-services/issue-search-lcs.md) LCS
- [Integrētais tehniskais atbalsts](../../dev-itpro/lifecycle-services/support-experience.md) finanšu un operāciju programmās
- [Mākonī nodrošināts atbalsts](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) LCS

Microsoft piedāvā finanšu un operāciju debitoriem trīs atbalsta plānus: Toms, Profesionāl Direct un atbalsts, kas iekļauts abonementā. Atbalsta līmenis katrā plānā atšķiras. Šajā tabulā parādīts trīs plānu salīdzinājums.

| Atbalsta līdzeklis | Premier | Profesionālais tiešais atbalsts | Abonements |
|---|---|---|---|
| Neierobežots pārtraukuma/labojuma incidenta iesniegšana | Jā | Jā | Jā |
| 24/7 piekļuve, izmantojot LCS | Jā | Jā | Jā |
| Incidenta atbildes laiks | Mazāk nekā viena stunda | Mazāk nekā viena stunda | Nākamā darba diena |
| Konsultāciju stundas | Kopas tiek iegādātas saskaņā ar līgumu. | Nē | Nē |
| Atvēlētais atbalsta konta pārvaldnieks | Jā | Nē | Nē |
| Atvēlētais atbalsta inženieris | Uz kā attiecas atsevišķs līgums | Nē | Nē |

Papildinformāciju skatiet tēmā [Pārskats par atbalstu](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Apstrādāt, lai iesaistītu atbalstu

Ja incidentu gadījumā ir iesaistītas finanšu un operāciju programmas, debitori iesniedz atbalsta biļeti korporācijai Microsoft, izmantojot LCS. CSS apstrādā incidentus, balstoties uz debitora atbalsta plānu un incidenta nozīmīgumu, kā norādīts CSS.

### <a name="service-level-agreement"></a>Pakalpojuma līmeņa līgums

Korporācija Microsoft ir apņēmusies izmantot pakalpojuma pieejamības koeficientu 99,9 procenti mēnesī. Ja korporācija Microsoft nesniedz un uztur pakalpojumu līmeni piemērojamam pakalpojumam, kā tas ir aprakstīts pakalpojumu līmeņa līgumā (SLA), iespējams, ka klients ir tiesīgs saņemt kredītu uz daļu no šī pakalpojuma ikmēneša pakalpojumu papildmaksām. Informāciju par to, kā iniciēt pakalpojuma kredītu, skatiet [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services) sadaļā "Prasības".

## <a name="important-resources"></a>Svarīgi resursi

- **[Drošības centrs](https://www.microsoft.com/trust-center)** – iegūstiet informāciju par to, kur tiek uzglabāti jūsu finanšu un operāciju dati, kā arī papildu informāciju par konfidencialitāti, atbilstību un drošības procedūrām.
- **[Licencēšanas noteikumi un dokumentācija](https://www.microsoftvolumelicensing.com/)** – ātri piekļūstiet licencēšanas noteikumiem, nosacījumiem un papildu informācijai, kas ir būtiska to preču un pakalpojumu izmantošanai, kas ir licencēti ar Microsoft apjoma licencēšanas programmu palīdzību.
- **[Licencēšanas nosacījumi](https://www.microsoft.com/licensing/product-licensing/)** – šīs lapas resursi nosaka noteikumus un nosacījumus programmatūrai un tiešsaistes pakalpojumu produktiem, ko iegādājaties ar Microsoft komerciālās licencēšanas programmu palīdzību.
- **[Microsoft Lifecycle Policy](/lifecycle/)** — šī lapa nodrošina konsekventas un paredzamas vadlīnijas atbalsta pieejamībai visā produkta dzīves laikā.
- **[Licencēšanas rokasgrāmata](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – izmantojiet šo rokasgrāmatu, lai uzzinātu vairāk par to, kā licencēt sistēmu Dynamics 365.
- **[Klientu atbalsts](https://dynamics.microsoft.com/support/)** – iegūstiet nozares galveno atbalstu jūsu Dynamics 365 programmām.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** — pārvaldiet programmas dzīves ciklu un pārvietojieties uz paredzamu, atkārtojamu, augstas kvalitātes ieviešanai.
- **[Dynamics 365 ieviešanas](https://aka.ms/D365ImplementationGuideFlip)** rokasgrāmata — Dynamics 365 Success by Design ieviešanas rokasgrāmatas dokumentu laika pārbaudes principi un sniedz iepriekšējus norādījumus arhitektam, veidot, pārbaudīt un izvietot Dynamics 365 risinājumus.

## <a name="definitions"></a>Definīcijas

### <a name="azure-region"></a>[Azure reģions](/azure/availability-zones/az-overview#regions)

Ģeogrāfisks reģions, kurā pastāv viens vai vairāki Azure datu resursi. Piemēri iekļauj ASV un Eiropā.

### <a name="business-process-modeler-bpm"></a>[Biznesa procesu modelētājs (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

Rīks LCS, kas palīdz veikt atšķirību analīzi dotajā implementācijā, izmantojot biznesa procesa definīcijas no Amerikas produktivitātes > Kvalitātes centra (APQC), kas tiek atbalstītas finanšu un operāciju programmās.

### <a name="cloud-solution-provider"></a>Mākoņa risinājumu sniedzējs

Partneris, kas ir daļa no Microsoft Cloud Solution Provider (CSP) programmas un kas nodrošina klientus ar pievienotās vērtības mākoņa pakalpojumiem, atbalstu, vienu rēķinu un debitoru pārvaldību mēroga.

### <a name="customer"></a>Debitors

Uzņēmuma entītija, kas patērē finanšu un operāciju programmas un kurā atrodas nomnieks Office 365.

### <a name="development-environment"></a>Izstrādes vide

Ar ražošanu nesaistījus slodziņu vide, kas tiek izmantota paplašinājumu izstrādāšana. Debitori izvieto šo vidi savā Azure abonementā no LCS. Šo vidi var izmantot arī demonstrācijai, apmācībai vai citiem testēšanas uzdevumiem. To sauc arī par [1. pakāpes smilškasti](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Darbības pārtraukums

Jebkurā periodā, kad lietotāji nevar pieteikties vai piekļūt viņu aktīvajam nomniekam, jo nebeigušās platformas vai pakalpojumu infrastruktūras dēļ, jo Microsoft nosaka no automatizētas veselības uzraudzības un sistēmas žurnāliem. Dīkstāves laikā nav ietvertas ieplānotās dīkstāves laika, pakalpojumu pievienojumprogrammu līdzekļu nepieejamība, iespēja piekļūt pakalpojumam jūsu pakalpojuma modifikāciju dēļ vai periodi, kuros ir pārsniegta mēroga vienības noslodze.

### <a name="implementation-partner"></a>Ieviešanas partneris

Partneris, ko debitors izvēlas, lai pielāgotu, konfigurētu, ieviestu un pārvaldītu tā finanšu un operāciju risinājumus.

### <a name="incident"></a>Incidents

Problēma, ar kuru klienti saskaras laikā, kad tie izmanto finanšu un operāciju pakalpojumus, un ka viņi iesniedz biļeti, izmantojot LCS.

### <a name="microsoft-customer-support-services-css"></a>Microsoft klientu atbalsta pakalpojumi (CSS)

Microsoft globālā atbalsta komanda, kas ir paredzēta kvalitātes pakalpojuma sniegšanu finanšu un operāciju programmām.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Administratīvais portāls finanšu un operāciju programmu dzīves cikla pārvaldībai no izmēģinājuma līdz ieviešanai, pēc ražošanas vadības un atbalsta. Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Ar ražošanu nesaistīta instance

Jebkura no šīm debitora lietoto pakalpojumu instancēm, lai validētu paplašinājumus un veiktu citus izstrādes uzdevumus:

- **1. pakāpes smilškaste** - izstrādātāja instance (debitora viesota)
- **2. pakāpes smilškaste** - standarta pieņemšanas testēšanas instance
- **3.–5. pakapes smilškaste** - pievienojumprogrammas smilškastes

Papildinformāciju par 2. līdz 5. pakāpei skatiet [Pareizas 2. pakapes vai jaunākas vides atlasīšana](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Ražošanas instance

Finanšu un operāciju vide, ko debitors izmanto, lai pārvaldītu tā "uz vietas" ikdienas darbības un biznesa procesus.

### <a name="sandbox-environment"></a>Smilškastes vide

Ārpus produkcijas vide, ko klients izmanto demonstrācijai, apmācībai, lietotāju pieņemšanas pārbaudei, paplašinājumu pārbaudei un citiem testēšanas uzdevumiem.

### <a name="service"></a>Pakalpojums

Jebkurš no pamata pakalpojumiem, kas ir iekļauts finanšu un operāciju programmās.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Pakalpojuma līmeņa līgums (SLA) Microsoft tiešsaistes pakalpojumiem

SLA attiecas uz Microsoft tiešsaistes pakalpojumiem. Plašāku informāciju skatiet tēmā [Pakalpojumu līmeņa līgumi](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Pakalpojuma atjauninājums

Microsoft pakalpojumu finanšu un operāciju vides, balstoties uz konsekventu pakalpojumu atjauninājumu palīdzību. Debitori iestata savu pakalpojuma atjaunināšanas kalendāru, ņemot vērā viņu biznesa vajadzības. Papildinformāciju skatiet sadaļā [Vienas versijas pakalpojuma atjauninājumi](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Struktūra, kas sistemātiski vada ieviešanu caur novērtēšanas sērijām kritiskos posmos, lai nodrošinātu optimālu arhitektūru, drošību, veiktspēju un lietotāja pieredzi Dynamics 365 risinājumam.

### <a name="user"></a>Lietotājs

Viena persona, kas izmanto finanšu un operāciju vides un ir saistīta ar debitora nomnieku.

