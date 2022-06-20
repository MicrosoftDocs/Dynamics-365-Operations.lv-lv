---
title: Darbā pieņemšanas pieprasījuma amats
description: Šajā rakstā ir aprakstīta personāla atlases pieprasījuma pozīcijas elements Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0996532edf09ea5159e143d92fb2a93c4d6f826d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904251"
---
# <a name="recruiting-request-position"></a>Darbā pieņemšanas pieprasījuma amats


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīta personāla atlases pieprasījuma pozīcijas elements Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>Apraksts

Apraksta amatu vai amatus, kas jāaizpilda personāla atlases pieprasījumam. Amata pievienošana personāla atlases pieprasījumam nav obligāta. Amata rekvizīti ir tikai lasāmi, jo amata rekvizītiem personāla atlases pieprasījumā nav jāatšķiras no tā, kādi tie ir amata šablona ierakstā. Ja rekvizīti jāmaina, tas jādara amata šablona ierakstā pirms amata pievienošanas personāla atlases pieprasījumam.

### <a name="json-representation"></a>JSON pārstāvība
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personāla atlases pieprasījuma amata elementa ID**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Tikai lasāms<br>Obligāts |    Sistēmas ģenerēts personāla atlases pieprasījuma amata identifikators. |
| **Pieņemšanas darbā pieprasījuma ID**<br>mshr_recruitingrequestid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Lietotājam lasāms personāla atlases pieprasījuma unikālais identifikators. |
| **Pieņemšanas darbā pieprasījuma ID vērtība**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmrecruitingrequestentity elementa mshr_hcmrecruitingrequestentityid | Sistēmas ģenerēts personāla atlases pieprasījuma, kuram amats ir piešķirts, identifikators. |
| **Amata ID**<br>mshr_positionid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Lietotājam lasāms amata unikālais identifikators. |
| **Amata ID vērtība**<br>_mshr_fk_position_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmpositionv2entity elementa mshr_hcmpositionv2entityid | Sistēmas ģenerēts amata identifikators. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Tikai lasāms<br>Obligāts | Amata apraksts. |
| **Amata veida ID**<br>mshr_positiontypeid<br>*Virkne* | Tikai lasāms<br>Neobligāti | Lietotājam lasāms amata veida unikālais identifikators šim amatam. |
| **Amata veida ID vērtība**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmpositiontypeentity elementa mshr_hcmpositiontypeentityid | Sistēmas ģenerēts amata veida unikālais identifikators šim amatam. |
| **Statuss**<br>mshr_status<br>*RecruitingRequestPositionStatus* opciju kopa | Lasīt/rakstīt<br>Obligāts | Darbā pieņemšanas pieprasījuma amata statuss. |
| **Nodaļas numurs**<br>mshr_departmentnumber<br>*Virkne* | Tikai lasāms<br>Neobligāti<br> | Amata nodaļas numurs. |
| **Nodaļas ID vērtība**<br>_mshr_fk_department_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_omdepartmententity elementa mshr_omdepartmententityid | Sistēmas ģenerēts amata nodaļas unikālais identifikators. |
| **Tiešā vadītāja amata ID**<br>mshr_reportstopositionid<br>*Virkne* | Tikai lasāms<br>Obligāts | Lietotājam lasāms amata ID, kam darbā pieņemtais amats ir tiešais vadītājs organizācijas hierarhijā. |
| **Tiešā vadītāja amata ID vērtība**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmpositionv2entity elementa mshr_hcmpositionv2entityid | Sistēmas ģenerēts tā amata ID, kuram darbā pieņemtais amats ir tiešais vadītājs. |
| **Tiešā vadītājs personāla numurs**<br>mshr_reportstopersonnelnumber<br>*Virkne* | Tikai lasāms<br>Obligāts | Tā darbinieka ID, kuram nolīgtais kandidāts būs tiešais pakļautais. |
| **Tiešā vadītāja pakļautā ID vērtība**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmworkerbaseentity elementa mshr_hcmworkerbaseentityid | Sistēmas ģenerēts ID, kuram nolīgtais kandidāts būs tiešais pakļautais. |
| **Finanšu dimensija**<br>mshr_financialdimension<br>*Virkne* | Tikai lasāms<br>Neobligāti | Amatam piešķirtā finanšu dimensija (piemēram, izmaksu centrs). Finanšu dimensija katram amatam tiek piešķirta juridiskajai personai. Izmaksu centri, kas ir definēti dimensijās, ir pieejami, izmantojot elementu mshr_dimattributeomcostcenterentity. |
| **Datu apgabala ID**<br>mshr_dataareaid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Norāda juridisko personu (uzņēmumu) personāla atlases pieprasījuma amatam. |
| **Datu apgabala ID vērtība**<br>_mshr_dataareaid_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: cdm_companyid cdm_company elements | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu) personāla atlases pieprasījuma amatam. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Tikai lasāms<br>Obligāts | Personāla atlases pieprasījuma vērtības un amata ID konkatenācija kā cita metode ieraksta unikālai identifikācijai. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
