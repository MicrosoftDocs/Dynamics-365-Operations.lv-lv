---
title: Personas profesionālā pieredze
description: Šajā tēmā aprakstīts Personas profesionālās pieredzes elements programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 7cb728a29ccf6c23a227e63edd6bb5226d2ffdd0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053711"
---
# <a name="person-professional-experience"></a>Personas profesionālā pieredze

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts Personas profesionālās pieredzes elements programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>Apraksts

Šis elements apraksta kandidāta profesionālo pieredzi vai darba vēsturi.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas profesionālās pieredzes elementa ID**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators elementa ierakstam. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Unikāls kandidāta personas ieraksta identifikators. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_dirpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts unikāls personas elementa ieraksta identifikators. |
| **Darba devēja amats**<br>mshr_employerposition<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Amata nosaukums, ko kandidāts ieņēma nodarbinātības laikā. |
| **Darbinieka vārds**<br>mshr_employername<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Darba devēja vārds. |
| **Darba devēja atrašanās vieta**<br>mshr_employerlocation<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Darba devēja atrašanās vieta. Maks. garums: 60. Nav noteikts vai nepieciešams noteikts formāts. |
| **Tālruņa numurs**<br>mshr_phone<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Darba devēja tālruņa numurs. |
| **Vietrādis URL**<br>mshr_url<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Darba devēja tīmekļa vietnes vietrādis URL. |
| **Sākuma datums**<br>mshr_startdate<br>*Datetime* | Lasīt/rakstīt<br>Obligāts | Kandidāta nodarbinātības sākuma datums. |
| **Beigu datums**<br>mshr_enddate<br>*Datetime* | Lasīt/rakstīt<br>Neobligāti | Kandidāta nodarbinātības beigu datums vai null, ja kandidāts joprojām šeit strādā. |
| **Atļaut sazināties ar darba devēju**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Norāda, vai kandidāts atļauj sazināties ar iepriekšējo darba devēju. |
| **Piezīmes**<br>mshr_note<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Piezīmes, ko izmantot darbā pieņēmējam vai personāla atlases darbiniekam. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauks, kas tiek izmantots kā elementa ieraksta primārais identifikators. Puses numura, sākuma datuma, darba devēja amata un darba devēja vārda kombinācija. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]