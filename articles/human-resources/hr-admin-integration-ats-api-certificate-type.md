---
title: Sertifikāta veids
description: Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: cc8f49be9af3f95ba182e1e0f1b288334a959ec40315b319a73feff3dbb3fdc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771567"
---
# <a name="certificate-type"></a>Sertifikāta veids

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīta Sertifikāta veida entītija programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmcertificatetypeentity

## <a name="description"></a>Apraksts

Šī entītija definē profesionālo sertifikātu veidu sarakstu, kas iestatīti programmai Human Resources. Šī entītija nav specifiska juridiskajai personai (uzņēmumam).

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Sertifikāta veida elementa ID**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Tikai lasāms<br>Obligāts 
Sistēmas ģenerēts | Unikāls sertifikāta veida primārais identifikators. |
| **Sertifikāta veids**<br>mshr_certificatetype<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Unikāls sertifikāta veida lietotājam lasāms identifikators. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Sertifikāta veida apraksts. |
| **Nepieciešama atjaunošana**<br>mshr_requirerenewal<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Norāda, vai sertifikātam ir nepieciešama atjaunošana. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]