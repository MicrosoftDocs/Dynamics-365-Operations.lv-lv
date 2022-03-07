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
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052293"
---
# <a name="payroll-worker-address"></a>Algas nodarbinātā adrese

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šī tēma sniedz detalizētu informāciju un parauga vaicājumu Algas nodarbinātā adreses elementam programmā Dynamics 365 Human Resources.

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Pilsēta**<br>mshr_city<br>*Virkne* | Tikai lasāms<br>Obligāts | Adresei definētā pilsēta.   |
| **Darbinieku skaits**<br>mshr_personnelnumber<br>*Virkne* | Tikai lasāms<br>Obligāts | Darbinieka unikālais personāla numurs.  |
| **Valsts reģions**<br>mshr_countryregionid<br>*Virkne* | Tikai lasāms<br>Obligāts | Adresei definētais valsts reģions  |
| **Derīgs no**<br>mshr_postaladdressvalidfrom<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, no kura adrese ir spēkā. |
| **Darba adrese**<br>mshr_isworkedinaddressbr>*Int32* | Tikai lasāms<br>Obligāts | Norāda, vai šī adrese ir darbinieka darba adrese. |
| **Pagasts**<br>mshr_county<br>*Virkne* | Tikai lasāms<br>Obligāts | Adresei definētā valsts.  |
| **Algas nodarbinātā adreses ID**<br>mshr_payrollworkeraddressentityid<br>*GUID* | Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu adresi.  |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts |  |
| **Iela**<br>mshr_street<br>*Virkne* | Tikai lasāms<br>Obligāts | Adresei definētā iela. |
| **Derīgs līdz**<br>mshr_postaladdressvalidto<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, līdz kuram adrese ir spēkā.  |
| **Atrašanās vietas ID**<br>mshr_locationidbr>*Virkne* | Tikai lasāms <br>Obligāts | Adreses ID.  |
| **Pasta indekss**<br>mshr_zipcode<br>*Virkne* | Tikai lasāms <br>Obligāts |Darbiniekam definētais identifikācijas numurs.  |
| **Dzīves vieta**<br>mshr_islivedinaddressbr>*Virkne* | Tikai lasāms<br>Obligāts | Norāda, vai šī adrese ir darbinieka dzīves vieta. |
| **Novads**<br>mshr_state<br>*Virkne* | Tikai lasāms<br>Obligāts | Adresei definēts štats.  |

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
