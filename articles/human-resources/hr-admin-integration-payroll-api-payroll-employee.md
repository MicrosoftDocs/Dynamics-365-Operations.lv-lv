---
title: Algots darbinieks
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu algas darbinieka elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 672db002ddf8d12aaab5b97241390c036ad7ab5c
ms.sourcegitcommit: 8fb79920bea14746a71551a4456236a6386bfcea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2021
ms.locfileid: "6538858"
---
# <a name="payroll-employee"></a>Algots darbinieks

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Algas darbinieka elements Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_payrollemployeeentity.

### <a name="description"></a>Apraksts

Šis elements sniedz informāciju par darbinieku. Pirms šī elementa lietošanas jāiestata [algas integrācijas parametri](hr-admin-integration-payroll-api-parameters.md).

>[!IMPORTANT] 
>**FirstName**, **MiddleName**, **LastName**, **NameValidFrom** un **NameValidTo** lauki vairs nebūs pieejami šim elementam. Tas ir tādēļ, lai nodrošinātu, ka ir tikai viens efektīvo datu avots, kas atbalsta šo elementu, kas ir **HcmEmployment** ar laukiem **EmploymentStartDate** un **EmploymentEndDate**.

>Šie lauki būs pieejami **DirPersonNameHistoricalEntity**, kas tika izlaists Platformas atjauninājumā 43. Laukā **Persona** pastāv OData relācija no **PayrollEmployeeEntity** uz **DirPersonNameHistoricalEntity**. Vai arī entītija **DirPersonNameHistoricalEntity** var tikt tieši vaicāta ar OData, izmantojot publisko nosaukumu **PersonHistoricalNames**.


## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieku skaits**<br>mshr_personnelnumber<br>*Virkne* | Tikai lasāms<br>Obligāts | Darbinieka unikālais personāla numurs. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Obligāts<br>Sistēmas ģenerēts |  |
| **Juridiskas personas ID**<br>mshr_legalentityID<br>*Virkne* | Tikai lasāms<br>Obligāts | Norāda juridisko personu (uzņēmumu). |
| **Dzimums**<br>mshr_gender<br>[mshr_hcmpersongender opciju kopa](hr-admin-integration-payroll-api-gender.md) | Tikai lasāms<br>Obligāts | Darbinieka dzimums. |
| **Payroll darbinieka elementa ID**<br>mshr_payrollemployeeentityid<br>*GUID* | Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu darbinieku. |
| **Darba attiecību uzsākšanas datums**<br>mshr_employmentstartdate<br>*Datuma laika nobīde* | Tikai lasāms<br>Obligāts | Darbinieka nodarbinātības sākuma datums. |
| **Identifikācijas veida ID**<br>mshr_identificationtypeid<br>*Virkne* |Tikai lasāms<br>Obligāts | Darbiniekam definētais identifikācijas veids. |
| **Nodarbinātības beigu datums**<br>mshr_employmentenddate<br>*Datuma laika nobīde* | Tikai lasāms<br>Obligāts |Darbinieka nodarbinātības beigas.  |
| **Datu apgabala ID**<br>mshr_dataareaid_id<br>*GUID* | Obligāts <br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu). |
| **Derīgs līdz**<br>mshr_namevalidto<br>*Datuma Laika Nobīde* |  Tikai lasāms<br>Obligāts | Datums, līdz kuram ir derīga informācija par darbinieku. |
| **Dzimšanas datums**<br>mshr_birthdate<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Darbinieka dzimšanas datums |
| **Identifikācijas numurs uz**<br>mshr_identificationnumber<br>*Virkne* | Tikai lasāms <br>Obligāts |Darbiniekam definētais identifikācijas numurs.  |

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
## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
