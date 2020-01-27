---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 14. decembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad677d1c36ac5159111afdcb5c31aed215d7b0a1
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897745"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 14. decembris)

**8.1.2085 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.

## <a name="changes"></a>Izmaiņas

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>ASV — ACA (Pieejamās aprūpes akts) atbalsts 2018. taksācijas gada formām 1095-B un 1095-C

Katru gadu attiecīgajiem lielajiem darba devējiem (ALE) jāsniedz katram pilnas slodzes darbiniekam forma 1095-C. Turklāt, ja darba devējs nodrošina paša apdrošinātu segumu, tam ir jāsniedz forma 1095-C (ja tas ir ALE) un 1095-B (ja tas ir mazais darba devējs) visiem pilna laika vai nepilna laika darbiniekiem, uz kuriem attiecas kāds no tā piedāvātajiem veselības aizsardzības plāniem. Šis līdzeklis nodrošina drukājamas formas 1095-C un 1095-B.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Importēšanas laikā tiek ignorēts lauks SubmittedByPersonId sadaļā HcmPerfJournalEntity

Importējot/eksportējot veiktspējas žurnāla ierakstus, lauks **Iesniedza** tiek ignorēts. Ar šīm izmaiņām vērtība **importēts/eksportēts** atspoguļos tabulas vērtību eksportēšanas laikā; importējot sistēma tiks atjaunināta ar vērtību, kas norādīta importa failā.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Darbvietas "Atvaļinājumi un kavējumi" cilnē Analīze tiek parādīta kļūda "OpenConnectionError" ar sistēmu nesaistītām administratora lomām

Ar šo atjauninājumu netiks rādītas kļūdas, atverot cilni **Analīze** darbvietā **Atvaļinājumi un kavējumi**.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Darbinieku pašapkalpošanās, amatu hierarhijas detalizētas rādīšanas rezultātā no elementa neizdodas iegūt pamatzaru

Ir veiktas izmaiņas, lai labotu kļūdu "Pamatzara iegūšana neizdevās", kad amatu hierarhija ir personalizēta, lai parādītos esošā darbvietā, un hierarhijā tiek atlasīts amats.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Lai skatītu cilni Alga lapā Amats, ir jābūt sistēmas administratoram.

Ir veiktas izmaiņas, lai ietvertu pareizos drošības elementus esošajā privilēģijā: "Uzturēt algas nodarbinātā un amata informāciju". Ar šīm izmaiņām pēc noklusējuma algu administratoram būs piekļuve lapas Amats laukiem Alga.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Kļūda, iesniedzot veiktspējas pārskatu vadītājam un ja sadaļā Iesniegšanas instrukcijas ir izmantots vietturis %Reviews.PerfPeriod%

Ir veiktas izmaiņas, kas izlabo kļūdu "Nulles atsauces" kļūdu, izmantojot vietturi %Reviews.PerfPeriod% sadaļā Iesniegšanas instrukcijas.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Darbaspēka Power BI pārskats rāda kļūdu, ja nodarbinātā darba stāža datums ir liekā diena garajā gadā

Ar šīm izmaiņām pakalpojumā Power BI tagad tiek atbalstītas liekās dienas.

### <a name="integration-between-core-hr-and-attract"></a>Integrācija starp Core HR un Attract

Ir veiktas izmaiņas, lai atjauninātu integrāciju starp Core HR un Attract saistībā darbā pieņemamajiem kandidātiem. Lai darbā pieņemamie kandidāti būtu redzami darbvietā **Personāla vadība**, tiek izmantotas tālāk aprakstītās Common Data Service entītijas.

Darba pieteikums
- Statusa iemeslam jābūt iestatītam kā Piedāvājums pieņemts
-   Nodrošina vienumus Kandidāts un Darba piedāvājums

Kandidāts
-   Nodrošina vienumu Informācija par kandidātu

Darba piedāvājums
-   Nodrošina vienumus Darba piedāvājuma ID un Darba piedāvājuma dalībnieki

Darba piedāvājuma dalībnieki
-   Nodrošina vienumu Par pieņemšanu darbā atbildīgais vadītājs

Kad kandidāts ir pievienots personāla vadībai, to tagad var arī noraidīt, izmantojot jaunu opciju, kas pieejama kandidāta kartītē.

## <a name="coming-soon"></a>Drīzumā

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Atvaļinājumi un kavējumi: turpmāko atvaļinājumu un prognozēto atvaļinājumu atlikumi

Līdz ar izmaiņām, kas veiktas, lai ļautu darbiniekiem prognozēt prombūtni un iesniegt turpmākās prombūtnes pieprasījumus, neietekmējot pašreizējos prombūtnes atlikumus, ir mainīts arī prombūtnes atlikumu attēlošanas veids. 

Pašlaik parādītais pieejamais atlikums ir pieprasījumiem pieejamais atvaļinājuma laika daudzums, ieskaitot uzkrāto atvaļinājumu līdz attiecīgajai dienai un visus apstiprinātos atvaļinājuma pieprasījumus līdz laika beigām. 

Izlaižot prognozēšanas iespēju, parādītais atlikums mainās uz pašreizējo prombūtnes laika atlikumu, ieskaitot uzkrāto atvaļinājumu līdz attiecīgajai dienai un pieprasījumiem līdz attiecīgajai dienai. Darbinieki un vadītāji redzēs šos atjauninātos atlikumus darbinieku un vadītāju pašapkalpošanās sadaļā kartītē **Prombūtne** un logā **Prombūtnes atlikumi**. Personāldaļas vadītāji redzēs šos atjauninātos atlikumus darbvietā **Cilvēki** un logā **Piešķirtie atvaļinājumu plāni**, kas attiecas uz darbinieku.

## <a name="known-issue"></a>Zināma problēma

### <a name="mapping-errors-in-the-integration-with-finance"></a>Kartēšanas kļūdas integrēšanā ar programmu Finance

Pašreizējā veidnē Talent integrēšanai ar Dynamics 365 Finance ir identificētas šādas problēmas. Drīzumā tiks publicēta jauna veidne, un tā tiks lietota visiem jaunajiem izveidotajiem integrācijas projektiem. Esošajiem integrācijas projektiem var atjaunināt uzdevuma kartējumus. Informāciju par atjauninātajiem kartējumiem skatiet tālāk esošajā tabulā. 

>[!NOTE]
> Uzdevums No sadaļas Amati uz sadaļu Amatu pamatdarba piešķire neintegrē datus. Šī problēma pašreiz tiek pētīta. Pašreizējā kartējumā nav kļūdas apiešanas risinājuma. 

Uzdevumam No sadaļas Nodaļas uz sadaļu Pārvaldības struktūrvienības ir jāatjaunina šādi kartējumi.

| Esošais avota lauks          | Jaunais avota lauks |
| -------------------------------|------------------|
| cdm_description (Apraksts)  | cdm_name (Nosaukums)  |

Ir jāpievieno arī papildu kartējums. Atlasiet pēdējo lauku **Nav**, lai pievienotu šādu kartējumu.

| Avota lauks                   | Mērķa lauks    |
| -------------------------------|----------------------|
| cdm_description (Apraksts)  | NAMEALIAS (NAMEALIAS)|

Atjauninātajiem kartējumiem jāizskatās, kā norādīts tālāk redzamajā attēlā.

![Uzdevums No sadaļas Nodaļas uz sadaļu Pārvaldības struktūrvienības](./media/DepartmentMapping.png)


Uzdevumam No sadaļas Darbi uz sadaļu Darba papildinformācija ir jāatjaunina šādi kartējumi.

| Esošais avota lauks          | Jaunais avota lauks                   |
| -------------------------------|------------------------------------|
| cdm_name (Nosaukums)                | cdm_description (Apraksts)      |
| cdm_name (Apraksts)         | cdm_jobdescription (Pienākumu apraksts)|


Atjauninātajiem kartējumiem jāizskatās, kā norādīts tālāk redzamajā attēlā.

![Uzdevums No sadaļas Darbi uz sadaļu Darba papildinformācija](./media/JobMapping.png)

Uzdevumam No sadaļas Nodarbinātie uz sadaļu Darbs ir jāatjaunina šādi kartējumi.

| Esošais avota lauks                 | Jaunais avota lauks                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (1. e-pasta adrese)   | cdm_primaryemailaddress (Primārā e-pasta adrese |
| cdm_telephone1 (1. tālrunis)          | cdm_primarytelephone (Primārais tālrunis)       |

Ir jāatjaunina arī lauka Dzimums pārveidošana. Atlasiet **fn** (funkcijas) kartes veidu vienumam Dzimums un atjauniniet šādus vērtību kartējumus.

| Common Data Service vērtība                   | Finance and Operations vērtība                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Vīrietis                                             |
| 75440001                    | Sieviete                                           |
| 75440002                    | Nav                                             | 
| 75440003                    | Nenoteikts                                      |

Atjauninātajiem kartējumiem jāizskatās, kā norādīts tālāk redzamajos attēlos.

![Uzdevums No sadaļas Nodarbinātie uz sadaļu Darbs](./media/WorkerMapping.png)

![Lauka Dzimums pārveidošana](./media/WorkerTransform.png)
