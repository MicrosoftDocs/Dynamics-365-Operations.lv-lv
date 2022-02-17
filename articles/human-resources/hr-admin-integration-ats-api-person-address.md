---
title: Personas adrese
description: Šajā tēmā aprakstīts Personas adreses elements programmai Dynamics 365 Human Resources .
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d428c2b1ce69c55fda2e574715021d4763544a6b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065481"
---
# <a name="person-address"></a>Personas adrese


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Personas adreses elements programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmpersonaddressentities

## <a name="description"></a>Apraksts

Šis elements ietver kandidāta ierakstu pasta adrešu sarakstu.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas adreses elementa ID**<br>mshr_hcmpersonaddressentityid<br>*Virkne* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators elementa ierakstam. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Saistītās puses (personas) ieraksta ID. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts puses (personas) elementa ieraksta identifikators. |
| **Atrašanās vietas ID**<br>mshr_locationid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Adreses ieraksta atrašanās vietas ID. Iestatīt mshr_logisticspostaladdresslocationcdsentity elementā. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Kandidāta adreses apraksts. |
| **Lomas**<br>mshr_roles<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Šai adresei piešķirtās lomas. Var piešķirt vairāk nekā vienu lomu. Katra loma ir jāatdala ar semikolu. Derīgas vērtības, kas mshr_logisticslocationroleentity elementā. |
| **Iela**<br>mshr_street<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Ielas numurs. |
| **Pilsēta**<br>mshr_city<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Adreses pilsēta. Iestatīt mshr_logisticsaddresscityentity elementā. |
| **Novads**<br>mshr_state<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Administratīvais apgabals adresē. Iestatīt mshr_logisticsaddressstateentity elementā. |
| **Pagasts**<br>mshr_county<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Adreses apgabals. Iestatīt mshr_logisticsaddresscountyentity elementā. |
| **Pasta indekss**<br>mshr_zipcode<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Adreses ZIP/ pasta indekss. Iestatīt mshr_logisticsaddresspostalcodeentity elementā. |
| **Valsts reģiona ID**<br>mshr_countryregionid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Adreses valsts vai reģions. |
| **Valsts/reģiona ID vērtība**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_logisticsaddresscountryregionentity mshr_logisticaddresscountryregionentityid | Sistēmas ģenerēts unikālais adreses valsts/reģiona identifikators. |
| **Ir primārais**<br>mshr_isprimary<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Obligāts | Nosaka, vai šī adrese ir definētās lomas personas primārā adrese. |
| **Ir privāta**<br>mshr_isprivate<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Obligāts | Norāda, vai šī adrese ir fiziskas personas adrese. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauks, kas tiek izmantots kā elementa ieraksta primārais identifikators. Puses numura un atrašanās vietas ID kombinācija. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
