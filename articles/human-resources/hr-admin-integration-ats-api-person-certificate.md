---
title: Personas sertifikāts
description: Šajā tēmā aprakstīts Personas sertifikāta elements programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 300bf294bb4b2fadd4c5d3e68e74674a69dd48f2
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067833"
---
# <a name="person-certificate"></a>Personas sertifikāts


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Personas sertifikāta elements programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmpersoncertificateentity

## <a name="description"></a>Apraksts

Šis elements apraksta kandidāta profesionālos sertifikātus.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas sertifikāta elementa ID**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators personas sertifikāta elementa ierakstam. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Kandidāta puses (personas) ID. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts puses (personas) elementa ieraksta identifikators. |
| **Sertifikāta veida ID**<br>mshr_certificatetypeid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts |  Personāla vadībā definētā sertifikāta veida identifikators. |
| **Sertifikāta veida ID vērtība**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmcertificatetypeentity mshr_hcmcertificatetypeentityid | Sistēmas ģenerēts saistītā elementa sertifikāta veida unikālais identifikators. |
| **Sākuma datums**<br>mshr_startdate<br>*Datetime* | Lasīt/rakstīt<br>Obligāts | Datums, kurā sertifikāts tika izsniegts. |
| **Beigu datums**<br>mshr_enddate<br>*Datetime* | Lasīt/rakstīt<br>Neobligāti | Datums, kurā sertifikāta derīgums beigsies. |
| **Piezīmes**<br>mshr_notes<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Piezīmes, ko izmantot personāla atlases darbiniekiem un darbā pieņēmējiem. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts |  Lauks, kas jāizmanto kā elementa ieraksta identifikators. Puses numura, sertifikāta veida ID un sākuma datuma kombinācija. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
