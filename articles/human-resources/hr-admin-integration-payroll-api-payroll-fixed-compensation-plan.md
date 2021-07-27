---
title: Algu aprēķina fiksētās atlīdzības plāns
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Payroll fiksētā atlīdzības plāna elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 24f8af4d691c3085c36018c574fa3b917a3d6953
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314217"
---
# <a name="payroll-fixed-compensation-plan"></a>Algu aprēķina fiksētās atlīdzības plāns

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Algas fiksētas atlīdzības plāna elements Dynamics 365 Human Resources .

### <a name="description"></a>Apraksts

Šis elements nodrošina fiksētās atlīdzības plānu, kas piešķirts noteiktam darbinieka amatam.

Fiziskais nosaukums: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieka ID**<br>mshr_fk_employee_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga:mshr_Employee_id no mshr_payrollemployeeentity elementa  | Darbinieka ID |
| **Maksājuma kurss**<br>mshr_payrate<br>*Decimāldaļskaitlis* | Tikai lasāms<br>Obligāts | Fiksētās atlīdzības plānā definētais algas kurss. |
| **Plāna ID**<br>mshr_planid<br>*Virkne* | Tikai lasāms<br>Obligāts |Norāda atlīdzības plānu.  |
| **Derīgs no**<br>mshr_validfrom<br>*Datuma Laika Nobīde* |  Tikai lasāms<br>Obligāts |Datums, no kura ir fiksētā atlīdzība par darbinieku.  |
| **Elements Algu aprēķina fiksētās atlīdzības plāns**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu atlīdzības plānu. |
| **Algas izmaksas biežums**<br>mshr_payfrequency<br>*Virkne* | Tikai lasāms<br>Obligāts |Darbinieka apmaksas biežums.  |
| **Derīgs līdz**<br>mshr_validto<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, līdz kuram ir fiksētā atlīdzība par darbinieku. |
| **Amata ID**<br>mshr_positionid<br>*Virkne* | Tikai lasāms <br>Obligāts | Amata ID, kas saistīts ar darbinieka un fiksētās atlīdzības plāna reģistrāciju. |
| **Valūta**<br>mshr_currency<br>*Virkne* | Tikai lasāms <br>Obligāts |Fiksētās atlīdzības plānam definētā valūta   |
| **Darbinieku skaits**<br>mshr_personnelnumber<br>*Virkne* | Tikai lasāms<br>Obligāts |Darbinieka unikālais personāla numurs.  |

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
