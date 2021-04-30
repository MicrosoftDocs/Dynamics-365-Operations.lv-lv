---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 03. septembris)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 3. septembri.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891773"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 3. septembris)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3504. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

Lai iegūtu papildinformāciju par gaidāmajiem līdzekļiem programmā Human Resources, skatiet [Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. laidiens](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Papildinformāciju par Human Resources atjaunināšanas procesu skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>Šajā laidienā

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Jauns noklusējuma finanšu dimensiju režģis un dialoga modelis visā programmā Human Resources (469495)

Jaunais finanšu dimensiju modelis tagad ir pieejams šādās jomās:

- Pozīcijas darbības (veidlapa: **HcmPositionActionDetail**)
- Algu ieņēmumu kodi (veidlapa: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Ieraksti nav redzami uzņēmuma atvaļinājumu kalendārā, ja nav iespējoti atvaļinājumu un kavējumu kalendāra uzlabojumi (484406)

Šajā laidienā tiek risināta problēma, kad uzņēmuma atvaļinājumu kalendārs netiek rādīts. Šī problēma rodas tikai tad, kad funkciju pārvaldības opcija **Atvaļinājumu un kavējumu kalendāra uzlabojumi** nav iespējota.

### <a name="benefitplanemployeeentity-issue-467597"></a>Problēma BenefitPlanEmployeeEntity (467597)

Šis laidiens izlabo problēmu ar **BenefitsPlanEmployee** elementu. Importējot darbinieku reģistrācijas, opcijas **Pārklājuma kods** un **Plāna tipa kods** tagad ir iestatīti pareizi. Šī problēma izraisīja darbinieku atvieglojumu plānu nekorektu attēlošanu veidlapās **Darbinieku atvieglojumu plāna** un **Atvērt reģistrāciju** darbinieku pašapkalpošanās.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>XML (435190) elektroniskā faila 1094-C izvadē trūkst rakstzīmes

Šīs izmaiņas izlabo problēmu, kas saistīta ar to , ka 1094-C izvades failā trūkst rakstzīmes, kas nepieciešama, iesniedzot IRS.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Darbinieka mainīgās atlīdzības tabula, kas kartēta fiksētās atlīdzības veidlapā (476117)

Šīs izmaiņas saskaņo fiksētās atlīdzības laukus ar fiksētās atlīdzības veidlapu. Mainīgās atlīdzības lauki tagad ir pieejami tikai ar mainīgās atlīdzības veidlapu.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Atstājiet pieprasījumus, kas atļauti pirms reģistrācijas, ja šim atvaļinājuma veidam ir negatīva minimālā bilance (469917)

Šīs izmaiņas aizliedz ievadīt atvaļinājumu pieprasījumus, pirms tie tiek reģistrēti plānā, pat ja reģistrācijai ir negatīva minimālā bilance. Jūs varat ievadīt vai iesniegt pieprasījumus, tikai tad, ja plāns ir aktīvs.

### <a name="document-templates-dont-download-457279"></a>Dokumentu veidnes netiek lejupielādētas (457279)

Ar šīm izmaiņām tagad var lejupielādēt visas dokumentu veidnes. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Dati tiek rādīti kā kolonnu galvenes, nevis kā rindas, kas paredzētas apmaksas likmes laukā atlīdzības plāna pārskatā (476077)

Analīzes pārskats tagad rāda pareizu **apmaksas likmes** informāciju.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Plašāku informāciju skatiet:

- [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 1. laidiena plānā
- [Programma Human Resources risinājumā Teams](./hr-admin-teams-leave-app.md) Human Resources dokumentācijā

### <a name="human-resources-app-in-teams-preview-features"></a>Programma Human Resources programmas Teams priekšskatījuma līdzekļos
 
-  **Paziņojumi**: iesniedzēji un pārtraukuma pieprasījumu apstiprinātāji tiek informēti par Personāla vadības lietotni programmā Teams. Apstiprinātāji varēs apstiprināt vai noraidīt brīvā laika pieprasījumus. Iesniedzēji tiks informēti, ja pieprasījums tika apstiprināts vai noraidīts. Plašāku informāciju skatiet:
   - [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 2. laidiena plānā
   - [Iespējot paziņojumus programmai Human Resources risinājumā Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) Human Resources dokumentācijā
   - [Ieslēgt vai izslēgt Teams paziņojumus atsevišķiem lietotājiem](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) Human Resources dokumentācijā
   - [Teams paziņojumi](./hr-teams-leave-app.md#respond-to-teams-notifications) Human Resources dokumentācijā
   - [Skatīt jūsu grupas atvaļinājumu kalendāru](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources dokumentācijā
 
- **Pārvaldnieka pārtraukuma kalendārs** : vadītājiem būs iespēja redzēt apstiprināto un gaidāmo laiku to tiešajiem pārskatiem kalendāra skatā. Šis skats nodrošina vieglu izpratni par to, kad viņu grupas dalībnieki ir prom no darba. Plašāku informāciju skatiet:
   - [Darbinieka atvaļinājuma un kavējumu pieredze Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. gada izlaiduma 2. laidiena plānā
   - [Skatīt jūsu grupas atvaļinājumu kalendāru](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources dokumentācijā

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi (477004)

Tagad ir pieejama jauna opcija, lai pozicionētu sarakstu **Man piešķirtie darbplūsmas elementi** informācijas paneļa labajā kolonnā. Ar šīm izmaiņām visi darba elementi un uzdevumu saraksti tiek rādīti tajā pašā apgabalā. Iespējojiet šo funkcionalitāti, ieslēdzot **Priekšskatījums - darbplūsmas ērtību uzlabojumi** līdzekļu pārvaldībā. Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu ieslēgšanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

Šis līdzeklis arī veicina darbplūsmas opcijas, kas parādās personāla darbību veidlapās. Darbplūsmas opcijas parādās arī virs darbību kopsavilkuma cilnes, lai tām varētu ātri piekļūt. Plašāku informāciju skatiet: 

- [Organizācijas un personāla vadības darbplūsmas ērtības uzlabojumi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) risinājuma Dynamics 365 2020. gada laidiena 2. kopuma plānā

![Darba vienumi, kas saistīti ar mani](./media/hr-workflow-work-items-assigned-to-me.png)

![Ātrā piekļuve arbplūsmas elementiem](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Drīzumā

### <a name="checklist-entities-included-in-dataverse"></a>Kontrolsaraksta entītijas iekļautas Dataverse

Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Dataverse.

### <a name="benefits-management-reason-codes"></a>Priekšrocību pārvaldības pamatojuma kodi

Priekšrocību pārvaldības pamatojuma kodi drīz tiks apvienoti ar esošajiem pamatojuma kodiem programmā Human Resources. Ja izveidojāt pamatojuma kodus Priekšrocību pārvaldībā, kas ir garāki par 15 rakstzīmēm, ir jāmaina pamatojuma koda nosaukums Priekšrocību pārvaldībā veidlapā **Pamatojuma kodi** uz tādu, kas ir 15 rakstzīmes vai mazāk. Pēc nosaukuma atjaunināšanas pamatojuma kods būs redzams Personāla vadības sadaļā esošajā pamatojuma koda veidlapā. Šīs izmaiņas būs pieejamas nākotnē, un funkcionāli tās neietekmēs jau esošos.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
