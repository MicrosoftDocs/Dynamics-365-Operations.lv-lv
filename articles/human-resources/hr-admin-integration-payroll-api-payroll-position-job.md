---
title: Algas pozīcijas darbs
description: Šajā rakstā ir sniegta detalizēta informācija un piemēra vaicājums algas pozīcijas darba elementam sadaļā Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
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
ms.openlocfilehash: fa347f4b99adc7c29d69daf62ad2bbfc14726a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864088"
---
# <a name="payroll-position-job"></a>Algas pozīcijas darbs


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts algas pozīcijas darba elements Dynamics 365 Human Resources.

### <a name="description"></a>Apraksts

Šis elements nodrošina saistību starp amatu un darbu noteiktam fiksētas atlīdzības plānam.

Fiziskais nosaukums: mshr_payrollpositionjobentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_Veids_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Amata ID**</br>mshr_positionid</br>*Virkne* | Tikai lasāms | Pozīcijas ID. |
| **Derīgs no**</br>mshr_validto</br>*Datuma Laika Nobīde* | Tikai lasāms | Datums, no kurā ir spēkā pozīcija un darba attiecības. |
| **Derīgs līdz**</br>mshr_validto</br>*Datuma Laika Nobīde* | Tikai lasāms | Datums, līdz kuram ir spēkā pozīcija un darba attiecības. |
| **Darba ID**</br>mshr_jobid</br>*Virkne* | Tikai lasāms | Darba ID. |
| **Primārais lauks**</br>mshr_primaryfield</br>*Virkne* | Sistēmas ģenerēts | Primārais lauks. |
| **Algas pozīcijas darba elementa ID**</br>mshr_payrollpositionjobentityid</br>*Guid* | Sistēmas ģenerēts. | Sistēmas ģenerēta globālā unikālā identifikatora (GUID) vērtība, lai unikāli identificētu darbu. |

## <a name="relations"></a>Saites

| Rekvizīta vērtība | Saistītais elements | Navigācijas rekvizīts | Kolekcijas veids |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Nav attiecināms |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Atbilde**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
