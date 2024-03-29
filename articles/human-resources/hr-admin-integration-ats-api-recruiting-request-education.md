---
title: Personāla atlases pieprasījuma izglītība
description: Šajā rakstā ir aprakstīta personāla atlases pieprasījuma izglītības entītija Dynamics 365 Human Resources.
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
ms.openlocfilehash: bcdb5e2cc61ce551af21401ea34d8e85bc21fc6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893850"
---
# <a name="recruiting-request-education"></a>Personāla atlases pieprasījuma izglītība


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīta personāla atlases pieprasījuma izglītības entītija Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>Apraksts

Apraksta RecruitingRequest izglītības prasības.

### <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personāla atlases pieprasījuma izglītības elementa ID**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators Personāla atlases pieprasījuma izglītības ierakstam. |
| **Pieņemšanas darbā pieprasījuma ID**<br>mshr_recruitingrequestid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Lietotājam lasāms saistītā personāla atlases pieprasījuma unikālais identifikators. |
| **Pieņemšanas darbā pieprasījuma ID vērtība**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmrecruitingrequestentity mshr_hcmrecruitingrequestentityid | Sistēmas ģenerēts saistītā personāla atlases pieprasījuma unikālais identifikators. |
| **Izglītības līmeņa ID**<br>mshr_educationlevelid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Nepieciešamās izglītības līmenis. |
| **Izglītības līmeņa ID vērtība**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmeducationlevelentity mshr_hcmeducationlevelentityid | Sistēmas ģenerēts pieprasītās izglītības līmeņa unikālais identifikators. |
| **Izglītības līmeņa apraksts**<br>mshr_educationleveldescription<br>*Virkne* | Tikai lasāms<br>Obligāts | Prasmei nepieciešamā līmeņa apraksts. |
| **Izglītības nozares ID**<br>mshr_educationdisciplinedescription<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Izglītības nozares joma. |
| **Izglītības nozares ID vērtība**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmeducationdisciplineentity mshr_hcmeducationdisciplineentityid | Sistēmas ģenerēts izglītības nozares jomas unikālais identifikators. |
| **Izglītības nozares apraksts**<br>mshr_educationdisciplinedescription<br>Virkne | Tikai lasāms<br>Obligāts | Izglītības nozares jomas apraksts. |
| **Datu apgabala ID**<br>mshr_dataareaid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Norāda juridisko personu (uzņēmumu).|
| **Datu apgabala ID vērtība**<br>_mshr_dataareaid_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: cdm_companyid cdm_company elements | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu). |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Personāla atlases pieprasījuma vērtības, izglītības līmeņa ID un izglītības nozares ID konkatenācija kā cita metode ieraksta unikāli identifikācijai. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
