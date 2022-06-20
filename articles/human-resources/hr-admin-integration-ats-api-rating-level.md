---
title: Novērtējuma līmenis
description: Šajā rakstā ir aprakstīts elementa Vērtējums līmenī Dynamics 365 Human Resources.
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
ms.openlocfilehash: dcd366632456c186eca9682d79a0c8690772e8bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893879"
---
# <a name="rating-level"></a>Novērtējuma līmenis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts elementa Vērtējums līmenī Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmratinglevelentity

## <a name="description"></a>Apraksts

Šis elements nodrošina pieejamos prasmju novērtējuma līmeņus. Novērtējuma līmeņi attiecas uz visām juridiskajām personām.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Novērtējuma līmeņa elementa ID**<br>mshr_hcmratinglevelentityid<br>*GUID* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēts līmeņa unikālais identifikators. |
| **Novērtējuma līmeņa ID**<br>mshr_ratinglevelid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Unikāls lietotājam lasāms līmeņa identifikators. |
| **Novērtēšanas modeļa ID**<br>mshr_ratingmodelid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Novērtēšanas modelis, kuram pieder novērtēšanas līmenis. |
| **Novērtējuma modeļa elementa ID**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmratingmodelentity mshr_hcmratingmodelentityid | Sistēmas ģenerēts identifikators novērtēšanas modelim, kuram pieder novērtēšanas līmenis. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Novērtējuma līmeņa apraksts. |
| **Koeficients**<br>mshr_factor<br>*Vesels skaitlis* | Lasīt/rakstīt<br>Obligāts | Novērtējuma līmeņa koeficients. Salīdzinot krājumus ar dažādu novērtējuma līmeņu skaitu, koeficients tiek izmantots rādītāju normalizēšanai. Vērtībai jābūt veselam skaitlim no 0 līdz 9. |
| **Piezīme.**<br>mshr_note<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Jebkādas ar novērtējuma līmeni saistītas piezīmes. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauks, kas jāizmanto kā elementa ieraksta identifikators. Novērtēšanas līmeņa ID un novērtēšanas modeļa ID kombinācija. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
