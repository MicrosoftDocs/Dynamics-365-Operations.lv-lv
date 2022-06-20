---
title: Algas detalizēta informācija Pozīcijām
description: Šajā rakstā ir sniegta detalizēta informācija un piemēram vaicājums algas detalizētai informācijai par pozīciju elementu sadaļā Dynamics 365 Human Resources.
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
ms.openlocfilehash: ac36b0386312e1631528b8ab5976db2cb3924caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904135"
---
# <a name="payroll-position"></a>Algas pozīcija


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts algu saraksta pozīciju elements sadaļā Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_payrollpositionentity.

### <a name="description"></a>Apraksts

Šī entītija sniedz ar pozīciju saistīto informāciju par šo darbinieku.

Fiziskais nosaukums: mshr_payrollpositionentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_Veids_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Amata ID**</br>mshr_positionid</br>*Virkne* | Tikai lasāms | Pozīcijas ID. |
| **Apmaksas cikla ID**</br>mshr_paycycleid</br>*Virkne* | Tikai lasāms | Pozīcijai definētais algas cikls. |
| **Ikgadējas regulāras stundas**</br>Ikgadējās regulārās stundas</br>*Decimāls* | Tikai lasāms | Ikgadējās regulārās stundas, kas definētas šajā pozīcijā. |
| **Apmaksātāja juridiskā persona**</br>paidbylegalentity</br>*Virkne* | Tikai lasāms | Par maksājuma izsniegšanu atbildīgā pozīcijā definētā juridiskā persona. |
| **Derīgs līdz**</br>derīgs līdz</br>*Datuma Laika Nobīde* | Tikai lasāms | Datums, līdz kuram ir derīga pozīcijas informācija. |
| **Derīgs no**</br>derīgs no</br>*Datuma Laika Nobīde* | Tikai lasāms | Datums, no kura ir derīga pozīcijas informācija. |
| **Primārais lauks**</br>mshr_primaryfield</br>*Virkne* | Sistēmas ģenerēts | Primārais lauks. |
| **Algas pozīcijas detalizētas informācijas elementa ID**</br>payrollpositiondetailsentityid</br>*Guid* | Obligāts</br>Sistēmas ģenerēts. | Sistēmas ģenerēta globālā unikālā identifikatora (GUID) vērtība, lai unikāli identificētu pozīciju. |

## <a name="relations"></a>Saites

| Rekvizīta vērtība | Saistītais elements | Navigācijas rekvizīts | Kolekcijas veids |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Nav attiecināms |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Nav attiecināms |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Atbilde**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
