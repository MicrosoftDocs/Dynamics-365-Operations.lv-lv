---
title: Darbā pieņemšanas prasmes
description: Šajā rakstā ir aprakstīts personāla atlases pieprasījuma prasmju elements Dynamics 365 Human Resources.
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
ms.openlocfilehash: b17bbdfbc977112344302deada085681ceca9bb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856401"
---
# <a name="recruiting-request-skill"></a>Darbā pieņemšanas prasmes


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts personāla atlases pieprasījuma prasmju elements Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>Apraksts

Apraksta RecruitingRequest prasmju prasības.

### <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personāla atlases pieprasījuma prasmju elementa ID**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators **Personāla atlases pieprasījuma prasmju** ierakstam. |
| **Pieņemšanas darbā pieprasījuma ID**<br>mshr_recruitingrequestid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Lietotājam lasāms saistītā personāla atlases pieprasījuma unikālais identifikators. |
| **Pieņemšanas darbā pieprasījuma ID vērtība**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br> Ārējā atslēga: mshr_hcmrecruitingrequestentity elementa mshr_hcmrecruitingrequestentityid | Sistēmas ģenerēts saistītā personāla atlases pieprasījuma unikālais identifikators. |
| **Prasmes ID**<br>mshr_skillid<br>*Virkne*<br> | Rakstīt vienu reizi<br>Obligāts | Lietotājam lasāms nepieciešamās prasmes unikālais identifikators. |
| **Prasmes ID vērtība**<br>_mshr_fk_skill_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmskillentity elementa mshr_hcmskillentityid | Sistēmas ģenerēts nepieciešamās prasmes unikālais identifikators. |
| **Novērtējuma līmeņa ID**<br>mshr_ratinglevelid<br>*Virkne* | Rakstīt vienu reizi<br>Neobligāti | Nepieciešamā prasmju līmeņa vērtība, kas atlasīta darbam, pamatojoties uz prasmēm piešķirto novērtējuma modeli. |
| **Novērtējuma līmeņa ID vērtība**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmratinglevelentity elementa mshr_hcmratinglevelentityid | Sistēmas ģenerēts līmeņa unikālais identifikators. |
| **Prasmes apraksts**<br>mshr_skilldescription<br>*Virkne* | Tikai lasāms<br>Obligāts | Prasmes apraksts. |
| **Vērtējuma līmeņa apraksts**<br>mshr_ratingleveldescription<br>*Virkne* | Tikai lasāms<br>Neobligāti | Atlasītā prasmes līmeņa apraksts. |
| **Datu apgabala ID**<br>mshr_dataareaid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Norāda juridisko personu (uzņēmumu). |
| **Datu apgabala ID vērtība**<br>_mshr_dataareaid_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: cdm_companyid cdm_company elements | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu). |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Personāla atlases pieprasījuma vērtības un prasmes ID konkatenācija kā cita metode ieraksta unikālai identifikācijai. |
| **Novērtēšanas modeļa ID**<br>mshr_ratingmodelid<br>*Virkne* | Lasīt-rakstīt<br>Obligāts | Prasmju vērtēšanā izmantotais vērtēšanas modelis. |
| **Novērtējuma modeļa ID vērtība**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmratingmodelentity elementa mshr_hcmratingmodelentityid | Sistēmas ģenerēts unikāls novērtējuma modeļa identifikators, kas tiek izmantots prasmes vērtēšanā. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
