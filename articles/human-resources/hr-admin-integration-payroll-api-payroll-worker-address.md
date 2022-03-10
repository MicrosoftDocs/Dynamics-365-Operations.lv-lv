---
title: Algas nodarbinātā adrese
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas nodarbinātā adreses elementam programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 70e42cbf657a28327699d927731edd36de7c4a64
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069761"
---
# <a name="payroll-worker-address"></a>Algas nodarbinātā adrese


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Algas nodarbinātā adreses elements Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_payrollworkeraddressentity.

### <a name="description"></a>Apraksts

Šis elements nodrošina algas atrašanās vietu un algas darba atrašanās vietu dotam darbiniekam.

## <a name="properties"></a>Rekvizīti

| Rekvizīts</br>**Fiziskais nosaukums**</br>**_Veids_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darbinieku skaits**</br>mshr_personnelnumber</br>*Virkne* | Tikai lasāms | Darbinieka unikālais personāla numurs. |
| **Atrašanās vietas ID**</br>mshr_locationidbr>*Virkne* | Tikai lasāms | Adreses ID. |
| **Dzīves vieta**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes opciju kopa](hr-admin-integration-payroll-api-no-yes.md)* | Tikai lasāms | Vērtība, kas norāda, vai adrese ir darbinieka dzīves vieta. |
| **Darba adrese** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes opciju kopa](hr-admin-integration-payroll-api-no-yes.md)* | Tikai lasāms | Vērtība, kas norāda, vai adrese ir darbinieka darba vieta. |
| **Valsts reģions**</br>mshr_countryregionid</br>*Virkne* | Tikai lasāms</br>Obligāts | Adresei definētais valsts vai reģions. |
| **Pasta indekss**</br>mshr_zipcode<br>*Virkne* | Tikai lasāms | Darbiniekam definētais identifikācijas numurs. |
| **Iela**</br>mshr_street</br>*Virkne* | Tikai lasāms | Adresei definētā iela. |
| **Pilsēta**</br>mshr_city</br>*Virkne* | Tikai lasāms | Adresei definētā pilsēta. |
| **Novads**</br>mshr_state</br>*Virkne* | Tikai lasāms | Adresei definētais reģions vai province. |
| **Pagasts**</br>mshr_county</br>*Virkne* | Tikai lasāms | Adresei definētais rajons. |
| **Derīgs no**</br>mshr_postaladdressvalidfrom</br>*Datuma Laika Nobīde* | Tikai lasāms | Datums, no kura adrese ir spēkā. |
| **Derīgs līdz**</br>mshr_postaladdressvalidto</br>*Datuma Laika Nobīde* | Tikai lasāms | Datums, l​īdz kura adrese ir spēkā. |
| **Primārais lauks**</br>mshr_primaryfield</br>*Virkne* | Tikai lasāms | Primārais lauks. |
| **Algas nodarbinātā adreses ID**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Sistēmas ģenerēts | Sistēmas ģenerēta globālā unikālā identifikatora (GUID) vērtība, lai unikāli identificētu adresi. |

## <a name="relations"></a>Saites

| Rekvizīta vērtība | Saistītais elements | Navigācijas rekvizīts | Kolekcijas veids |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Piemēra vaicājums

**Pieprasīt**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Atbilde**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
