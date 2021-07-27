---
title: Algu aprēķina mainīgās atlīdzības plāns
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll mainīgās atlīdzības plāna elementam programmā Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5dc096c08ed808f577c8cdc96ca84000a0b80679
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314437"
---
# <a name="payroll-variable-compensation-plan"></a>Algu aprēķina mainīgās atlīdzības plāns

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Algas mainīgās atlīdzības plāna elements Dynamics 365 Human Resources .

### <a name="description"></a>Apraksts

Šis elements nodrošina mainīgās atlīdzības plānu, kas piešķirts noteiktam darbinieka amatam.

Fiziskais nosaukums: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms</br>Obligāts |Darbinieka unikālais personāla numurs.  |
| **Piemaksas datums**</br>mshr_awarddate</br>*Datuma Laika Nobīde* | Tikai lasāms</br>Obligāts | Piemaksas datums. |
| **Piemaksas tips**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType opciju kopa](hr-admin-integration-payroll-api-award-type.md)* | Tikai lasāms</br>Obligāts | Piemaksu tips, kas tiek definēts atlīdzības mainīgās daļas plānam. |
| **Valūta**</br>mshr_unitcurrencycode</br>*Virkne* | Tikai lasāms </br>Obligāts |Mainīgās atlīdzības plānam definētā valūta.   |
| **Fiksētas atlīdzības plāna ID**</br>mshr_fixedplanid</br>*Virkne* | Tikai lasāms | Fiksētās atlīdzības plāns, kas tiek izmantots, kā pamats piemaksas aprēķinam. |
| **Vienības vērtība**</br>mshr_awardamount</br>*Decimāldaļskaitlis* | Tikai lasāms | Vienības vērtība |
| **Procesa tips**</br>mshr_processtype</br>*[mshr_hrmCompProcessType opciju kopa](hr-admin-integration-payroll-api-process-type.md)* | Tikai lasāms | Procesa tips. |
| **Mainīgās atlīdzības plāna tips**</br>Virkne</br>*mshr_typeid* | Tikai lasāms | Mainīgās atlīdzības plāna tips. |
| **Mainīgās atlīdzības plāna ID**</br>Virkne</br>*mshr_planid* | Tikai lasāms | Mainīgās atlīdzības plāna ID. |
| **Primārais lauks**</br>mshr_primaryfield</br>*GUID* | Tikai lasāms</br>Sistēmas ģenerēts. | |
| **Darbinieka ID**</br>mshr_fk_employee_id_value</br>*GUID* | Tikai lasāms</br>Obligāts</br>Ārējā atslēga:mshr_Employee_id no mshr_payrollemployeeentity elementa  | Darbinieka ID. |
| **Algu aprēķina mainīgās atlīdzības plāna elements**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Obligāts</br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu atlīdzības plānu. |


## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Atbilde**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
