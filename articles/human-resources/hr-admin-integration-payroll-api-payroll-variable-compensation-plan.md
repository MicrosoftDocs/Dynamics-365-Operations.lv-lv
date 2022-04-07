---
title: Algu aprēķina mainīgās atlīdzības plāns
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll mainīgās atlīdzības plāna elementam programmā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5cc9e02ff2dd49e2eb0c8131fcff2eca4b9c3b1
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533652"
---
# <a name="payroll-variable-compensation-plan"></a>Algu aprēķina mainīgās atlīdzības plāns


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Algas mainīgās atlīdzības plāna elements Dynamics 365 Human Resources .

### <a name="description"></a>Apraksts

Šis elements nodrošina mainīgās atlīdzības plānu, kas piešķirts noteiktam darbinieka amatam.

Fiziskais nosaukums: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms | Darbinieka unikālais personāla numurs.  |
| **Piemaksas datums**</br>mshr_awarddate</br>*Datuma Laika Nobīde* | Tikai lasāms | Piemaksas datums. |
| **Piemaksas tips**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType opciju kopa](hr-admin-integration-payroll-api-award-type.md)* | Tikai lasāms | Piemaksu tips, kas tiek definēts atlīdzības mainīgās daļas plānam. |
| **Valūta**</br>mshr_unitcurrencycode</br>*Virkne* | Tikai lasāms |Mainīgās atlīdzības plānam definētā valūta.   |
| **Fiksētas atlīdzības plāna ID**</br>mshr_fixedplanid</br>*Virkne* | Tikai lasāms | Fiksētās atlīdzības plāns, kas tiek izmantots, kā pamats piemaksas aprēķinam. |
| **Vienības vērtība**</br>mshr_awardamount</br>*Decimāldaļskaitlis* | Tikai lasāms | Vienības vērtība |
| **Procesa tips**</br>mshr_processtype</br>*[mshr_hrmCompProcessType opciju kopa](hr-admin-integration-payroll-api-process-type.md)* | Tikai lasāms | Procesa tips. |
| **Mainīgās atlīdzības plāna tips**</br>Virkne</br>*mshr_typeid* | Tikai lasāms | Mainīgās atlīdzības plāna tips. |
| **Mainīgās atlīdzības plāna ID**</br>Virkne</br>*mshr_planid* | Tikai lasāms | Mainīgās atlīdzības plāna ID. |
| **Vienību skaits**</br>Decimāldaļskaitlis</br>*mshr_numberofunits* | Tikai lasāms | Piešķīruma vienību skaits. |
| **Primārais lauks**</br>mshr_primaryfield</br>*GUID* | Tikai lasāms</br>Sistēmas ģenerēts. | |
| **Algu aprēķina mainīgās atlīdzības plāna elements**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu atlīdzības plānu. |

## <a name="relations"></a>Saites 

|Rekvizīta vērtība | Saistītais elements | Navigācijas rekvizīts | Kolekcijas veids |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Atbilde**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
