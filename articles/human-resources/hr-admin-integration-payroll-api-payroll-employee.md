---
title: Algots darbinieks
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu algas darbinieka elementam programmā Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3977b758f65875a36749a49459c2a81459a7b69
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882034"
---
# <a name="payroll-employee"></a>Algots darbinieks

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šī tēma sniedz detalizētu informāciju un parauga vaicājumu algas darbinieka elementam programmā Dynamics 365 Human Resources.

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieku skaits**<br>mshr_personnelnumber<br>*Virkne* | Tikai lasāms<br>Obligāts | Darbinieka unikālais personāla numurs. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Obligāts<br>Sistēmas ģenerēts |  |
| **Uzvārds**<br>mshr_lastname<br>*Virkne* | Tikai lasāms<br>Obligāts | Darbinieka uzvārds. |
| **Juridiskas personas ID**<br>mshr_legalentityID<br>*Virkne* | Tikai lasāms<br>Obligāts | Norāda juridisko personu (uzņēmumu). |
| **Derīgs no**<br>mshr_namevalidfrom<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, no kura ir derīga informācija par darbinieku.  |
| **Dzimums**<br>mshr_gender<br>*Int32* | Tikai lasāms<br>Obligāts | Darbinieka dzimums. |
| **Payroll darbinieka elementa ID**<br>mshr_payrollemployeeentityid<br>*GUID* | Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu darbinieku. |
| **Darba attiecību uzsākšanas datums**<br>mshr_employmentstartdate<br>*Datuma laika nobīde* | Tikai lasāms<br>Obligāts | Darbinieka nodarbinātības sākuma datums. |
| **Identifikācijas veida ID**<br>mshr_identificationtypeid<br>*Virkne* |Tikai lasāms<br>Obligāts | Darbiniekam definētais identifikācijas veids. |
| **Nodarbinātības beigu datums**<br>mshr_employmentenddate<br>*Datuma laika nobīde* | Tikai lasāms<br>Obligāts |Darbinieka nodarbinātības beigas.  |
| **Datu apgabala ID**<br>mshr_dataareaid_id<br>*GUID* | Obligāts <br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu). |
| **Derīgs līdz**<br>mshr_namevalidto<br>*Datuma Laika Nobīde* |  Tikai lasāms<br>Obligāts | Datums, līdz kuram ir derīga informācija par darbinieku. |
| **Dzimšanas datums**<br>mshr_birthdate<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Darbinieka dzimšanas datums |
| **Identifikācijas numurs uz**<br>mshr_identificationnumber<br>*Virkne* | Tikai lasāms <br>Obligāts |Darbiniekam definētais identifikācijas numurs.  |
| **Vārds**<br>mshr_firstname<br>*Virkne* | Tikai lasāms<br>Obligāts | Darbinieka vārds. |
| **Otrais vārds**<br>mshr_middlename<br>*Virkne* | Tikai lasāms<br>Obligāts |Darbinieka otrais vārds.  |

## <a name="example-query-for-payroll-employee"></a>Payroll darbinieka vaicājuma piemērs

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Atbilde**

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
