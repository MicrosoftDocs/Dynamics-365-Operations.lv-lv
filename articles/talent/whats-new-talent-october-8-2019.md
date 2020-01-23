---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 8. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 06758ff5eb1c00ae299b1b8849fcabb0cd9593e8
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896639"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 8. oktobris)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2542. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Noņemot atvieglojumus, atvērt reģistrāciju no publiska priekšskatījuma

Saistībā ar mūsu sludinājumu [Stratēģiskās investīcijas Core HR Drive Operational Excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) blogā, korporācija Microsoft noņem atvieglojumus, kas atvērti reģistrācijai no publiskās priekšskatīšanas 2019. gada 18. oktobrī. Tā vietā nākotnē tiks izlaista jauna funkcionalitāte. Atbalsta atvērtās reģistrācijas funkcija, kas pašlaik atrodas publiskajā priekšskatījumā, netiks atbalstīta. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service integrācija tagad pēc noklusējuma ir izslēgta pēc jaunajiem noteikumiem (343675)
 
Kad jaunas vides tiek nodrošinātas, Common Data Service integrēšana ir izslēgta. Papildinformāciju skatiet sadaļu [Konfigurēt Common Data Service integrāciju](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Racionalizēta darbinieku ievade un navigācija

Tagad darbinieku ieceļošanas un navigācijas funkcionalitāte ir pieejama visās vidēs. Lai ieslēgtu šo līdzekli, dodieties uz **Sistēmas administrēšana\>Saites\>Iestatīšana\>Sistēmas parametri\>Priekšskatījuma funkcijas** un atlasiet **Uzlabota darbinieka forma un navigācija**. Šis līdzeklis tiek ieslēgts visiem lietotājiem. Šo opciju varat izslēgt jebkurā laikā.

Lai iegūtu papildu informāciju, skatiet [Racionalizēta darbinieku datu ievadīšana](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract and Onboard izveido neaktīvus darbiniekus Core HR (380517).

Šīs nedēļas laidiens labo problēmu, kad Attract and Onboard izveido neaktīvus darbiniekus Core HR.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Darbplūsma cieš neveiksmi, kad vadītājs ir pieteicies citā uzņēmumā, pārtraucot darbinieku (346852)

Pamatojoties uz juridisku personu, ar kuru vadītājs ir pieteicies, darbplūsma atsāk darbību.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Trūkst informācijas par HcmOnboardingWorkerChecklistTaskEntity (349591)

Šis laidiens ietver papildu informāciju par **HcmOnboardingWorkerChecklistTaskEntity**. Daži piemēri:

- **Grupas nosaukums**, ja piešķirtais tips ir **Grupa**
- **Grupas nosaukums**, ja piešķirtais tips ir **Darbinieks**
- **Vadītāja nosaukums**, ja piešķirtais tips ir **Vadītājs**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Entītijas nav norādītas alfabētiskā secībā Common Data Service administrācijā (377414)

Entītijas šobrīd ir norādītas alfabētiskā secībā **CDS administrācijas** lapā.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Nodarbinātības tipa maiņa ar nākotnes datumu neatļauj amata piešķiri (339958)

Šīs izmaiņas ļauj veikt pozīcijas piešķiri, ja darbinieku tipi tiek mainīti (piemēram, no darbinieka uz darbuzņēmēju).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Atjauninot Common Data Service atvaļinājuma bankas darījumu elements izveido jaunu ierakstu Talent (352938)

Atvaļinājuma darījums tagad tiek atjaunināts, kad tiek veikts atjauninājums Common Data Service atvaļinājumu bankas darījumiem.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Atsauksmes elementu nosaukums parāda atsauksmes aprakstu (343765)

Atsauksmes apraksts vairs netiek parādīts pielikuma nosaukumā.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Atlīdzības darbplūsmas komentāru lauks rāda nepareizu saturu (339297)

Šīs izmaiņas parāda saturu **%HcmActionState.HcmWorkerActionComment.Comments%** laukā.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity un WorkCalendarDayEntity netiek atklātas, izmantojot OData (376329)

Šajā laidienā **WorkCalendarEntity** un **WorkCalendarDayEntity** tagad ir pieejami, izmantojot Atvērto datu protokolu (OData).

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity ir lēns laikā, kad OData tiek lietots (375221)

Izmaiņas uzlabo **HCMWorkerEntity** veiktspēju, ja tiek izmantots Microsoft Excel darbgrāmatas veidotājs.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Pārvaldnieka veiktspējas žurnāla ievade rāda kļūdu pēc veiktspējas žurnāla dzēšanas un jauna žurnāla izveides (336061).

Šis laidiens izlabo problēmu, kas rodas pēc vienas veiktspējas žurnāla dzēšanas un pēc tam nekavējoties izveido jaunu. Šis labojums maina vadītāja pašapkalpošanās darbības uzvedību.

## <a name="coming-soon"></a>Drīzumā

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.
