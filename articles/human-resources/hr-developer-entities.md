---
title: Common Data Service elementi
description: Microsoft Dynamics 365 Human Resources izmanto Common Data Service, lai iespējotu paplašināšanas un integrācijas scenārijus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530010"
---
# <a name="common-data-service-entities"></a>Common Data Service elementi

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources izmanto Common Data Service, lai iespējotu paplašināšanas un integrācijas scenārijus.

Plašāku informāciju par Common Data Service skatiet [Kas ir Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Common Data Service ir pieejami šādas cilvēkresursu entitījas.

## <a name="benefit-entities"></a>Atvieglojumu elementi

| Vārds/nosaukums | Elements |
| --- | --- |
| Atvieglojumu aprēķina biežums | cdm_benefitcalculationfrequency |
| Atvieglojumu aprēķina biežuma izmaksas periods | cdm_benefitcalculationfrequencypayperiod |
| Atvieglojumu aprēķina likme | cdm_benefitcalculationrate |
| Atvieglojumu aprēķina likmes detalizēta informācija | cdm_benefitcalculationratedetail |
| Atvieglojumu opcija | cdm_benefitoption |
| Atvieglojumu plāns | cdm_benefitplan (nav iespējots pielāgoto lauku atbalsts) |
| Atvieglojumu veids | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Biznesa procesa uzdevumu entītijas

| Vārds/nosaukums | Elements |
| --- | --- |
| Biznesa procesu kalendārs | cdm_businessprocesscalendar |
| Biznesa procesu grupu piešķire | cdm_businessprocessgroupassignment |
| Biznesa procesu bibliotēkas uzdevumu grupa | cdm_businessprocesslibrarytaskgroup |
| Biznesa procesu stadija | cdm_businessprocessstage |
| Kontrolsaraksta veidnes galvene | cdm_businessprocesstemplateheader |
| Kontrolsaraksta veidnes uzdevums | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Atlīdzības entitījas

| Vārds/nosaukums | Elements |
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

## <a name="organization-entities"></a>Organizācijas entītijas

| Vārds/nosaukums | Elements |
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
> Finanšu dimensijas **Amata veidam**, **Amata darbinieka piešķirei** un **Nodarbinātībai** pakalpojumam Common Data Service nodrošina vienvirziena integrāciju. Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Common Data Service uz personāla vadības resursiem. 

## <a name="leave-and-absence-entities"></a>Atvaļinājumu un kavējumu elementi

| Vārds/nosaukums | Elements |
| --- | --- |
| Atvaļinājuma bankas transakcija | cdm_leavebanktransaction |
| Atvaļinājuma reģistrācija | cdm_leaveenrollment |
| Atvaļinājumu plāns | cdm_leaveplan |
| Atvaļinājuma pieprasījums | cdm_leaverequest |
| Atvaļinājuma pieprasījuma informācija | cdm_leaverequestdetail |
| Atvaļinājuma tips | cdm_leavetype |
| Atvaļinājuma veida iemesla kods | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Algas elementi

| Vārds/nosaukums | Elements |
| --- | --- |
| Apmaksas cikls | cdm_paycycle |
| Apmaksas periods | cdm_payperiod |
| Algas nopelnīšanas kods | cdm_payrollearningcode |
| Bankas konta izdevumi | cdm_bankaccountdisbursement |
| Nodokļu reģions | cdm_taxregion |

## <a name="worker-entities"></a>Nodarbinātā elementi

| Vārds/nosaukums | Elements |
| --- | --- |
| Nodarbinātais | cdm_worker |
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

## <a name="worker-setup-entities"></a>Nodarbinātā iestatījumu entitījas

| Vārds/nosaukums | Elements |
| --- | --- |
| Veterāna statuss | cdm_veteranstatus |
| Etniskā izcelsme | cdm_ethnicorigin |
| Iemesla kods | cdm_reasoncode |
| Personas identifikācijas dokumenta izdevējiestāde | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Kompetences entitījas

| Vārds/nosaukums | Elements |
| --- | --- |
| Prasmju veids | cdm_skilltype |

## <a name="entity-relationship-models"></a>Entitījas attiecību modeļi

### <a name="worker"></a>Nodarbinātais

![Nodarbinātais](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Darbs un amats

![Darbs un amats](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Priekšrocības

![Priekšrocības](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensācija

![Kompensācija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Pamest

![Pamest](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Darba kalendārs

![Darba kalendārs](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Skatiet arī

[Izvēlēties datu integrācijas tehnoloģiju](hr-admin-integration-choose-technology.md)</br>
[Common Data Service integrācijas konfigurēšana](hr-admin-integration-common-data-service.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]