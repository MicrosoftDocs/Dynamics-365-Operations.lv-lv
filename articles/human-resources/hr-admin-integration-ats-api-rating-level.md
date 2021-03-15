---
title: Novērtējuma līmenis
description: Šajā tēmā aprakstīta Novērtējuma līmenis entītija programmai Dynamics 365 Human Resources .
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125261"
---
# <a name="rating-level"></a>Novērtējuma līmenis

Šajā tēmā aprakstīta Novērtējuma līmenis entītija programmai Dynamics 365 Human Resources .

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