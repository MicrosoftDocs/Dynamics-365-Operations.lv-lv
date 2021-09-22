---
title: Algu aprēķina fiksētās atlīdzības plāns
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll fiksētā atlīdzības plāna elementam programmā Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dcb253fabbb183003048119c7a627bf0ab960050
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429237"
---
# <a name="payroll-fixed-compensation-plan"></a>Algu aprēķina fiksētās atlīdzības plāns

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Algas fiksētas atlīdzības plāna elements Dynamics 365 Human Resources .

### <a name="description"></a>Apraksts

Šis elements nodrošina fiksētās atlīdzības plānu, kas piešķirts noteiktam darbinieka amatam.

Fiziskais nosaukums: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Plāna ID**</br>mshr_planid</br>*Virkne* | Tikai lasāms | Norāda atlīdzības plānu.  |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms | Darbinieka unikālais personāla numurs. |
| **Maksājuma kurss**</br>mshr_payrate</br>*Decimāldaļskaitlis* | Tikai lasāms | Fiksētās atlīdzības plānā definētais algas kurss. |
| **Amata ID**</br>mshr_positionid</br>*Virkne* | Tikai lasāms | Amata ID, kas saistīts ar darbinieka un fiksētās atlīdzības plāna reģistrāciju. |
| **Derīgs no**</br>mshr_validfrom</br>*Datuma Laika Nobīde* |  Tikai lasāms | Datums, no kura ir fiksētā atlīdzība par darbinieku.  |
| **Derīgs līdz**</br>mshr_validto</br>*Datuma Laika Nobīde* | Tikai lasāms | Datums, līdz kuram ir fiksētā atlīdzība par darbinieku. |
| **Algas izmaksas biežums**</br>mshr_payfrequency</br>*Virkne* | Tikai lasāms | Darbinieka apmaksas biežums.  |
| **Valūta**</br>mshr_currency</br>*Virkne* | Tikai lasāms | Valūta definēta fiksētās atlīdzības plānam. |
| **Elements Algu aprēķina fiksētās atlīdzības plāns**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu atlīdzības plānu. |

## <a name="relations"></a>Saites

|Rekvizīta vērtība | Saistītā entītija | Navigācijas rekvizīts | Kolekcijas veids |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Atbilde**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
