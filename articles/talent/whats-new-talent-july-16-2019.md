---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 16. jūlijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ac0990a72224395cf109c7eb42cbb48ece2a0b4f
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795200"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-16-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 16. jūlijs)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract
Šajā laidienā ir ietverti nelieli programmas Dynamics 365 Talent: Attract kļūdu labojumi.

### <a name="coming-soon-in-attract"></a>Drīzumā risinājumā Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Darbu apstiprinājumu rādīšana sākumlapā

Apstiprinājumi tiek rādīti informācijas paneļa sadaļā **Apstiprinājumi**. Apstiprinātāji var pārskatīt savus apstiprinājumus sadaļā **Piešķirts jums**, kur ir norādīts darba ID, amata nosaukums, citi apstiprinātāji un datums, kad šis darbs tika piešķirts. Lietotāji, kuri iesniedz darbu apstiprināšanai, var pārskatīt savus darbus sadaļā **Jūsu pieprasījumi**, kur ir norādīti apstiprinātāji, kam šis iesniegtais darbs joprojām ir jāapstiprina.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard
Šajā laidienā ir ietverti nelieli programmas Dynamics 365 Talent: Onboard kļūdu labojumi.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR
Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service elementi, kas atbalsta pielāgotos laukus

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OmDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Nevar redzēt mērķus un pārskatus vadītāju pašapkalpošanās modulī

Šīs nedēļas izmaiņas tagad ļauj parādīt un rediģēt mērķus un pārskatus izlaišanas līmeņa vadītājiem vadītāja pašapkalpošanās modulī.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Mērķa veidlapu nevar aizvērt, ja lietotājs rediģē kādu mērķa lauku

Šis laidiens izlabo problēmu, kad mērķa veidlapa netiek aizvērta, atlasot **Aizvērt**.

### <a name="creating-new-goals-and-saving-displays-error"></a>Jaunu mērķu izveide un displeju kļūdas saglabāšana

Šis laidiens novērš problēmu, saglabājot mērķus darbinieku un vadītāju pašapkalpošanās modulī.

### <a name="unable-to-add-a-field-to-position-details"></a>Nevar pievienot lauku amata detalizētai informācijai 

Ar šo laidienu pielāgotie lauki tagad ir atbalstīti amata detalizētajā informācijā.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Nevar iestatīt beigu datumu ienākumu veida kodam, izmantojot datu pārvaldību

Tagad izmaiņas ļauj iestatīt beigu datumus ienākumu veida kodiem datu pārvaldībā.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Jauni pielāgotie lauki netiek sinhronizēti pietiekami ātri

Pielāgotas lauku sinhronizācijas ar Common Data Service veiktspēja ir uzlabota ar šīs nedēļas laidienu.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Elementa eksports uz datu bāzes darbiem neizdodas ar kļūdas ziņojumu: "Inicializācijas virknes formāts neatbilst specifikācijai, kas sākas ar indeksu 0".

Šis laidiens labo problēmu, kad nedarbojas datu bāzes pakešuzdevumi. Lai atjauninātu manuāli, veiciet tālāk norādītās darbības.

1. Dodieties uz **Datu pārvaldība**.
2. Atlasiet **Konfigurēt elementu eksportēšanu uz datu bāzi**.
3. Atkārtoti ievadiet savienojuma virkni ar mērķa datu bāzi un atlasiet **Saglabāt**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP e-pasta konfigurācija pēkšņi neizdodas ar kļūdas ziņojumu: "SMTP serveris pieprasa drošu savienojumu vai arī klients nav autentificēts."

Šis laidiens labo SMTP e-pasta konfigurāciju, kas pēkšņi neizdodas. Lai atjauninātu manuāli, veiciet tālāk norādītās darbības.

1. Dodieties uz **Sistēmas administrēšana**.
2. Atlasiet **E-pasta parametri**.
3. Atlasiet **SMTP iestatījumi**. 
4. Atkārtoti ievadiet SMTP serverim izmantoto lietotājvārdu un paroli un atlasiet **Saglabāt**.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Priekšskatījuma līdzekļi ir iespējoti tikai smilškastes instancēs

Kad nodrošināt jaunu Talent instanci, varat norādīt, vai šīs instances tips ir **Ražošana** vai **Smilškaste**. Instances, kuru tips ir **Smilškaste**, ļauj agri testēt jaunos līdzekļus. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu **Ražošana**. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu **Smilškaste**, sazinieties ar [atbalsta dienestu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), lai sāktu izmaiņu pieprasījumu.

Papildinformāciju par to, kā tiek publicētas izmaiņas, skatiet tēmā [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Atvaļinājumu tipu ierobežošana brīvā laika pieprasījumos

Organizācijas var piedāvāt darbiniekiem daudz dažādus atvaļinājumu tipus. Taču daži brīvā laika pieprasījumu atvaļinājumu tipi var nebūt piemēroti tam, lai tos iesniegtu darbinieki. Tā vietā šos atvaļinājumu tipus var pārvaldīt personāla vadība (HR). Šajā laidienā jūs varat konfigurēt, kuriem atvaļinājumu tipiem darbinieki var iesniegt brīvā laika pieprasījumus. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Veiktspējas informācijas skatīšana tiešajām un izvērstajām atskaitēm vadītāja patstāvīgi lietojamajā pakalpojumā

Jauna opcija ļaus vadītājiem apskatīt gan savas tiešās veiktspējas atskaites, gan izvērstās atskaites. Pašlaik rindu pārvaldnieki var piešķirt un atjaunināt veiktspējas mērķus un izdot jaunas atsauksmes. Turklāt tiešie vadītāji un viņu darbinieki var uzturēt un atjaunināt veiktspējas žurnālus, lai palīdzētu nodrošināt, ka veiktspējas pārskatīšanas process norit raiti. Kad šīs izmaiņas būs ieviestas, papildus savām tiešajām atskaitēm pārvaldnieki varēs skatīt un uzturēt ar veiktspēju saistītu informāciju par savām izvērstajām atskaitēm.
