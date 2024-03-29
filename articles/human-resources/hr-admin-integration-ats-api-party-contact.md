---
title: Puses kontaktpersona
description: Šajā rakstā ir aprakstītas puses kontaktpersonas entītija Dynamics 365 Human Resources.
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
ms.openlocfilehash: f10bb89757419bcb29bfa5a4f44d30a38f41dfb0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909880"
---
# <a name="party-contact"></a>Puses kontaktpersona


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstītas puses kontaktpersonas entītija Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_dirpartycontactentities

## <a name="description"></a>Apraksts

Šis elements apraksta kandidāta kontaktinformāciju, tostarp tālruni, e-pastu un sociālās multivides kontus.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Puses kontaktpersonas elementa ID**<br>mshr_dirpartycontactentityid<br>*Virkne* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators elementa ierakstam. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Saistītās puses (personas) ieraksta ID. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts puses (personas) elementa ieraksta identifikators. |
| **Atrašanās vietas ID**<br>mshr_locationid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Adreses ieraksta atrašanās vietas ID. Iestatīt mshr_logisticspostaladdresslocationcdsentity elementā. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Detalizēts kontaktinformācijas apraksts. |
| **tips**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype opciju kopa* | Lasīt/rakstīt<br>Obligāts | Kontaktpersonas informācijas veids. |
| **Valsts reģiona kods**<br>mshr_countryregioncode<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Adreses valsts vai reģions. |
| **Vietrādis**<br>mshr_locator<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Detalizēta informācija par kontaktpersonu. Piemēram, ja veids ir **E-pasta adrese**, tad šajā laukā ir kandidāta e-pasta adrese. |
| **Vietrāža paplašinājums**<br>mshr_locatorextension<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Vietrāža paplašinājums. Piemēram, ja veids ir **Tālrunis**, tad šajā rekvizītā būtu jāietver tālruņa numura paplašinājums. |
| **Vai ir mobilais tālrunis**<br>mshr_ismobile<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Obligāts | Norāda, vai tas ir mobilā tālruņa numurs. |
| **Ir tūlītējais ziņojums**<br>mshr_isinstantmessage<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Obligāts | Norāda, vai tālrunis ir iespējots tūlītējai ziņojumapmaiņai. |
| **Ir primārais**<br>mshr_isprimary<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Obligāts | Nosaka kontaktinformācijas veida primāro kontaktpersonu. Katram kontaktinformācijas veidam drīkst būt tikai viens primārais ieraksts. |
| **Privātie iestatījumi**<br>mshr_isprivate<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Obligāts | Norāda, vai šī adrese ir fiziskas personas adrese. |
| **Nolūks**<br>mshr_purpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Detalizēts kontaktinformācijas mērķa/lomas apraksts. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauks, kas tiek izmantots kā elementa ieraksta primārais identifikators. Puses numura, veida, apraksta un vietrāža kombinācija. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
