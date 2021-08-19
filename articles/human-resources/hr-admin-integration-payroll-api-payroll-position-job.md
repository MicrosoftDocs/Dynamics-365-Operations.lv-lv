---
title: Algas pozīcijas darbs
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu algas pozīcijas darba elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: d5f84a1a6ff794cdc8b4b81e8518983789a0b33f1708719906f6ad094d9c4285
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722635"
---
# <a name="payroll-position-job"></a>Algas pozīcijas darbs

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Algas pozīcijas darba elements Dynamics 365 Human Resources .

### <a name="description"></a>Apraksts

Šis elements nodrošina saistību starp amatu un darbu noteiktam fiksētas atlīdzības plānam.

Fiziskais nosaukums: mshr_payrollpositionjobentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darba ID**<br>mshr_jobid<br>*Virkne* | Tikai lasāms<br>Obligāts |Darba ID. |
| **Derīgs no**<br>mshr_validto<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, no kurā ir spēkā posīcijas un darba attiecības. |
| **Derīgs līdz**<br>mshr_validto<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, līdz kuram ir spēkā posīcijas un darba attiecības.  |
| **Amata ID**<br>mshr_positionid<br>*Virkne* | Tikai lasāms<br>Obligāts | Pozīcijas ID. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Obligāts<br>Sistēmas ģenerēts |  |
| **Pozīcijas darba ID vērtība**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga:mshr_PayrollPositionJobEntity no mshr_payrollpositionjobentity |Darba ID, kas saistīts ar amatu.|
| **Fiksētās atlīdzības plāna ID vērtība**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_FixedCompPlan_id no mshr_payrollfixedcompensationplanentity  | Fiksētās atlīdzības plāna ID, kas saistīts ar amatu. |
| **Algas pozīcijas darba elementa ID**<br>mshr_payrollpositionjobentityid<br>*Guid* | Obligāts<br>Sistēmas ģenerēts. | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu darbu.  |

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
