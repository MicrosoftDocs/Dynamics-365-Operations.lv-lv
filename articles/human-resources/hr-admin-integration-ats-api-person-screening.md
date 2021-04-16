---
title: Personas izvērtēšana
description: Šajā tēmā aprakstīts Personas izvērtēšanas elements Dynamics 365 Human Resources .
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798037"
---
# <a name="person-screening"></a>Personas izvērtēšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Personas izvērtēšanas elements Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmpersonscreeningentity

## <a name="description"></a>Apraksts

Šis elements apraksta kandidāta izvērtēšanu, kas kandidātam ir veikta vai jāveic, lai tiktu pieņemts darbā.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas izvērtēšanas elementa ID**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Unikāls personas izvērtēšanas ieraksta primārais identifikators. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Ar kandidātu saistītais puses (personas) numurs. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts puses (personas) elementa ieraksta identifikators. |
| **Izvērtēšanas veida ID**<br>mshr_screeningtypeid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts<br>Ārējā atslēga: ScreeningType | Personāla vadībā definētā izvērtēšanas veida identifikators. |
| **Izvērtēšanas veida ID vērtība**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmscreeningtypeentity mshr_hcmscreeningtypeentityid | Sistēmas ģenerēts izvērtēšanas veida ieraksta identifikators saistītajā elementā. |
| **Nepieciešams līdz šādam datumam:**<br>mshr_requiredby<br>*Datetime* | Lasīt/rakstīt<br>Neobligāti | Datums, līdz kuram nepieciešams veikt izvērtēšanu. |
| **Statuss**<br>mshr_status<br>*mshr_hcmcompletionstatus opciju kopa*<br>Lasīt/rakstīt<br>Obligāts | Sniedz kandidāta statusu izvērtēšanai. |
| **Pabeigšanas datums**<br>mshr_completeddate<br>*Datetime* | Lasīt/rakstīt<br>Neobligāti | Datums, kad izvērtēšana tika pabeigta. |
| **Piezīmes**<br>mshr_note<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Piezīmes, ko izmantot personāla atlases darbiniekiem un darbā pieņēmējiem. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]