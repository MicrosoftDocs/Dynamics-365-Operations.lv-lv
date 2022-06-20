---
title: Personas identifikācijas numurs.
description: Šajā rakstā ir aprakstīta personas identifikācijas numura elements Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2d3641ffede29b7fda904ffb6cd70cb33d7800d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858277"
---
# <a name="person-identification-number"></a>Personas identifikācijas numurs.


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīta personas identifikācijas numura elements Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>Apraksts

Šis elements apraksta kandidāta identifikācijas numurus. Tas ļauj API patērētājam ierakstīt kandidāta ierakstā identifikācijas numurus, piemēram, sociālās apdrošināšanas numurus vai pases numurus. Identifikācijas numuriem var piekļūt darbinieka ierakstā, bet ne kandidāta ierakstā. Integrācijas programma var rakstīt vērtības Personāla pārvaldības datu bāzē, bet Personāla pārvaldībā numuri nebūs redzami, kamēr nav izveidots kandidāta darbinieka ieraksts.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas identifikācijas numura elementa ID**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Unikāls personas identifikācijas numura ieraksta primārais identifikators. |
| **Ieraksta veids**<br>mshr_entrytype<br>*Virkne* | Lasīt-rakstīt<br>Neobligāti | Brīvā vērtība atsaucei uz identifikācijas numura ieraksta veidu. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt-rakstīt<br>Neobligāti | Identifikācijas numura apraksts |
| **Beigu datums**<br>mshr_expirationdate<br>*Datetime* | Lasīt-rakstīt<br>Neobligāti | Datums, kad beidzas identifikācijas numura vai saistītā dokumenta derīgums. |
| **Ir primārais**<br>mshr_isprimary<br>*mshr_noyes opciju kopa* | Lasīt-rakstīt<br>Neobligāti | Nosaka, vai identifikācijas numurs ir galvenais personas ieraksts šim identifikācijas veidam. |
| **Identifikācijas numurs**<br>mshr_identificationnumber<br>*Virkne* | Lasīt-rakstīt<br>Obligāts | Identifikācijas numurs |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt-rakstīt<br>Obligāts | Tās puses (personas) identifikators, kurai pieder identifikācijas numurs. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity elementa mshr_dirpersonentityid | Puses (personas) unikālais identifikators. |
| **Identifikācijas veida ID**<br>mshr_identificationtypeid<br>*Virkne* | Lasīt-rakstīt<br>Obligāts | Identifikācijas numura veids. |
| **Identifikācijas veida ID vērtība**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmidentificationtypeentity elementa mshr_hcmidentificationtypeentityid | Sistēmas ģenerēts identifikācijas veida unikālais identifikators. |
| **Izdevējiestādes ID**<br>mshr_issuingagencyid<br>*Virkne* | Lasīt-rakstīt<br>Neobligāti | Iestāde vai organizācija, kas izsniedz identifikācijas numuru. |
| **Izdevējiestādes ID vērtība**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmissuingagencyentity elementa mshr_hcmissuingagencyentityid | Sistēmas ģenerēts identifikācijas numura izdevējiestādes unikālais identifikators. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauks, kas jāizmanto kā elementa ieraksta identifikators. Puses numura, identifikācijas veida ID un identifikācijas numura kombinācija. |
| **Izsniegšanas datums**<br>mshr_issuedate<br>*Datums* | Lasīt-rakstīt<br>Neobligāti | Datums, kurā identifikācijas numurs tika izsniegts. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
