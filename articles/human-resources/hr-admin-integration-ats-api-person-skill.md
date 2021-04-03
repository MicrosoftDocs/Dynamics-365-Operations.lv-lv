---
title: Personas prasme
description: Šajā tēmā aprakstīts Personas prasmes elements programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 65d5492ed988c51efe9e1629fa13225f1b4a3c15
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464206"
---
# <a name="person-skill"></a>Personas prasme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Personas prasmes elements programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmpersonskillentity

## <a name="description"></a>Apraksts

Šis elements apraksta kandidāta prasmes.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas prasmes elementa ID**<br>mshr_hcmpersonskillentityid<br>*GUID* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators elementa ierakstam. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt/rakstīt<br>Obligāts |   Saistītās puses (personas) ieraksta ID. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts puses (personas) elementa ieraksta identifikators. |
| **Sertificētājs**<br>mshr_certifier<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Tā darbinieka numurs, kurš sertificējis šo prasmi. |
| **Certificētāja ID vērtība**<br>_mshr_fk_certifier_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmworkerentity mshr_hcmworkerentityid | Sistēmas ģenerēts darbinieka ieraksta unikālais identifikators darbiniekam, kurš sertificēja prasmi. |
| **Prasmes ID**<br>mshr_skillid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Personāla pārvaldībā definētais prasmes identifikators. |
| **Prasmes ID vērtība**<br>_mshr_fk_skill_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmskillentityid of mshr_hcmskillentity | Sistēmas ģenerēts atlasītās prasmes identifikators. |
| **Pieredzes gadu skaits**<br>mshr_yearsofexperience<br>*Decimāldaļskaitlis* | Lasīt/rakstīt<br>Neobligāti | Pieredzes gadu skaits, kopš kandidātam ir šī prasme. |
| **Novērtēšanas ID**<br>mshr_ratingid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Vērtēšanas skalas veids. Šī elementa vērtība ir **Prasmes**. |
| **Līmeņa veids**<br>mshr_leveltype<br>*mshr_hrmskillleveltype opciju kopa* | Lasīt/rakstīt<br>Obligāts | Veidam iedalīta kategorija līmenim, kas piešķirts prasmei. |
| **Līmeņa ID**<br>mshr_levelid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Vērtējuma līmeņa ID, kas kandidātam ir šai prasmei. |
| **Novērtējuma līmeņa ID vērtība**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmratinglevelentity mshr_hcmratinglevelentityid | Sistēmas ģenerēts novērtējuma līmeņa identifikators. |
| **Līmeņa datums**<br>mshr_leveldate<br>*Datetime* | Lasīt/rakstīt<br>Obligāts | Datums, kurā kandidāta prasme tika novērtēta. |
| **Novērtējuma līmeņa pārbaudītājs**<br>mshr_ratinglevelexaminer<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Tā darbinieka numurs, kurš novērtēja kandidātu. |
| **Novērtējuma līmeņa pārbaudītāja ID vērtība**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmworkerentity mshr_hcmworkerentityid | Sistēmas ģenerēts tā darbinieka identifikators, kurš pārbaudīja kandidāta prasmes līmeni. |
| **Pārbaudīts**<br>mshr_verified<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Obligāts | Norāda, vai novērtētais prasmes līmenis ir pārbaudīts. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauks, kas jāizmanto kā elementa ieraksta identifikators. Puses numura, līmeņa veida, prasmes ID un līmeņa datuma kombinācija. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]