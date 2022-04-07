---
title: Dataverse tabulas
description: Microsoft Dynamics 365 Human Resources izmanto Dataverse, lai iespējotu paplašināšanas un integrācijas scenārijus.
author: twheeloc
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8378418bdd0f4cb3f22b38a44e35179aad3ca33
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534238"
---
# <a name="dataverse-tables"></a>Dataverse tabulas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources izmanto Dataverse, lai iespējotu paplašināšanas un integrācijas scenārijus.

> [!NOTE]
> Human Resources elementi atbilst Dataverse tabulām. Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Šādas Dataverse tabulas ir pieejamas, pamatojoties uz Human Resources elementiem.

## <a name="benefit-tables"></a>Atvieglojumu tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Atvieglojumu aprēķina biežums | cdm_benefitcalculationfrequency |
| Atvieglojumu aprēķina biežuma izmaksas periods | cdm_benefitcalculationfrequencypayperiod |
| Atvieglojumu aprēķina likme | cdm_benefitcalculationrate |
| Atvieglojumu aprēķina likmes detalizēta informācija | cdm_benefitcalculationratedetail |
| Atvieglojumu opcija | cdm_benefitoption |
| Atvieglojumu plāns | cdm_benefitplan (nav iespējots pielāgoto lauku atbalsts) |
| Atvieglojumu veids | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Biznesa procesa uzdevumu tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Biznesa procesu kalendārs | cdm_businessprocesscalendar |
| Biznesa procesu grupu piešķire | cdm_businessprocessgroupassignment |
| Biznesa procesu bibliotēkas uzdevumu grupa | cdm_businessprocesslibrarytaskgroup |
| Biznesa procesu stadija | cdm_businessprocessstage |
| Kontrolsaraksta veidnes galvene | cdm_businessprocesstemplateheader |
| Kontrolsaraksta veidnes uzdevums | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Kompensāciju tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Atlīdzības fiksētais plāns | cdm_compensationfixedplan |
| Atlīdzības režģis | cdm_compensationgrid |
| Atlīdzības līmenis | cdm_compensationlevel |
| Atlīdzības izmaksas biežums | cdm_compensationpayfrequency |
| Atlīdzības raksturojuma punktu iestatīšana | cdm_compensationreferencepointsetup |
| Atlīdzības raksturojuma punktu iestatīšanas līnija | cdm_compensationreferencepointsetupline |
| Atlīdzības reģions | cdm_compensationregion |
| Atlīdzības struktūra | cdm_compensationstructure |
| Atlīdzības mainīgais plāns | cdm_compensationvariableplan |
| Atlīdzības mainīgā plāna līmenis | cdm_compensationvariableplantype |
| Atlīdzības mainīgā plāna tips | cdm_compensationvariableplantype |
| Fiksētas atlīdzības notikums | cdm_fixedcompensationevent |
| Izmaksu noteikums | cdm_vestingrule |
| Nodarbinātā fiksētā atlīdzība | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Organizācijas tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Nodaļa | cdm_department |
| Nodarbinātība | cdm_employment |
| Uzņēmums | cdm_company |
| Darbs | cdm_job |
| Darba funkcija | cdm_jobfunction |
| Amats | cdm_jobposition |
| Amata veids | cdm_positiontype |
| Amatā nodarbinātā piešķire | cdm_positionworkerassignmentmap |
| Amata dimensija | cdm_jobpositiondimension|
| Darba tips | cdm_jobtype |
| Valoda | cdm_language |
| Nosaukums | cdm_title |

> [!NOTE]
> Finanšu dimensijas **Amata veidam**, **Amata darbinieka piešķirei** un **Nodarbinātībai** pakalpojumam Dataverse nodrošina vienvirziena integrāciju. Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Dataverse uz personāla vadības resursiem. 

## <a name="leave-and-absence-tables"></a>Atvaļinājumu un prombūtnes tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Atvaļinājuma bankas transakcija | cdm_leavebanktransaction |
| Atvaļinājuma reģistrācija | cdm_leaveenrollment |
| Atvaļinājumu plāns | cdm_leaveplan |
| Atvaļinājuma pieprasījums | cdm_leaverequest |
| Atvaļinājuma pieprasījuma informācija | cdm_leaverequestdetail |
| Atvaļinājuma tips | cdm_leavetype |
| Atvaļinājuma veida iemesla kods | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Algu tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Apmaksas cikls | cdm_paycycle |
| Apmaksas periods | cdm_payperiod |
| Algas ienākumu veida kods | cdm_payrollearningcode |
| Bankas konta izdevumi | cdm_bankaccountdisbursement |
| Nodokļu reģions | cdm_taxregion |

## <a name="worker-tables"></a>Darbinieku tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Darbinieks | cdm_worker |
| Nodarbinātā adrese | cdm_workeraddress |
| Nodarbinātā personas dati | cdm_workerpersonaldetail |
| Nodarbinātās personas identifikācijas numurs | cdm_workerpersonidentificationnumber |
| Nodarbinātās personas identifikācijas veids | cdm_workerpersonidentificationtype |
| Darba kalendārs | cdm_workcalendar |
| Darba kalendāra diena | cdm_workcalendarday |
| Brīvdienas darba kalendārā |cdm_workcalendarholiday |
| Brīvdienu rinda darba kalendārā | cdm_workcalendarholidayline |
| Darba kalendāra laika intervāls | cdm_workcalendartimeinterval (nav iespējots pielāgoto lauku atbalsts) |
| Nodarbinātā bankas konts | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Darbinieka iestatījumu tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Veterāna statuss | cdm_veteranstatus |
| Etniskā izcelsme | cdm_ethnicorigin |
| Iemesla kods | cdm_reasoncode |
| Personas identifikācijas izsniedzēja iestāde | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Kompetenču tabulas

| Vārds, uzvārds | Tabula |
| --- | --- |
| Prasmju tips | cdm_skilltype |

## <a name="table-relationship-models"></a>Tabulas attiecību modeļi

### <a name="worker"></a>Darbinieks

![Nodarbinātais](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Darbs un amats

![Darbs un amats.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Atvieglojumi

![Atvieglojumi.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensācija

![Kompensācija.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Atvaļinājums

![Atvaļinājums.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Darba kalendārs

![Darba kalendārs.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Skatiet arī

[Datu integrācijas tehnoloģiju izvēle](hr-admin-integration-choose-technology.md)<br>
[Pakalpojuma Dataverse integrācijas konfigurēšana](hr-admin-integration-common-data-service.md)<br>
[Pakalpojuma Dataverse virtuālo tabulu konfigurēšana](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources virtuālās tabulas: Bieži uzdotie jautājumi](hr-admin-virtual-entity-faq.md)<br>
[Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminoloģijas atjauninājumi](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
