---
title: Algas detalizēta informācija Pozīcijām
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas informācijai elementam Pozīcijas programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056784"
---
# <a name="payroll-position"></a>Algas pozīcija

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas informācijai elementam Pozīcijas programmā Dynamics 365 Human Resources.

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Ikgadējas regulāras stundas**<br>Ikgadējās regulārās stundas<br>*Decimāldaļskaitlis* | Tikai lasāms<br>Obligāts | Ikgadējās regulārās stundas, kas definētas šajā pozīcijā.  |
| **Algas pozīcijas detalizētas informācijas elementa ID**<br>payrollpositiondetailsentityid<br>*Guid* | Obligāts<br>Sistēmas ģenerēts. | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu pozīciju.  |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Obligāts<br>Sistēmas ģenerēts |  |
| **Pozīcijas darba ID vērtība**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga:mshr_PayrollPositionJobEntity no mshr_payrollpositionjobentity |Darba ID, kas saistīts ar amatu.|
| **Fiksētās atlīdzības plāna ID vērtība**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_FixedCompPlan_id no mshr_payrollfixedcompensationplanentity  | Fiksētās atlīdzības plāna ID, kas saistīts ar amatu. |
| **Apmaksas cikla ID**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Pozīcijai definētais algas cikls. |
| **Apmaksātāja juridiskā persona**<br>paidbylegalentity<br>*Virkne* | Tikai lasāms<br>Obligāts | Par maksājuma izsniegšanu atbildīgā pozīcijā definētā juridiskā persona. |
| **Amata ID**<br>mshr_positionid<br>*Virkne* | Tikai lasāms<br>Obligāts | Pozīcijas ID. |
| **Derīgs līdz**<br>derīgs līdz<br>*Datuma Laika Nobīde* | Tikai lasāms<br>Obligāts |Datums, no kura ir derīga pozīcijas informācija.  |
| **Derīgs no**<br>derīgs no<br>*Datuma Laika Nobīde* | Tikai lasāms<br>Obligāts |Datums, līdz kuram ir derīga pozīcijas informācija.  |

**Vaicājums**

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
