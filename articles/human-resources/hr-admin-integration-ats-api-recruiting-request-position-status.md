---
title: Personāla atlases pieprasījuma pozīcijas statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma pozīcijas statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: dee34366289f2e7ade1a1ae24bea15c0d19683d79720a44a6327879e8060a810
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725894"
---
# <a name="recruiting-request-position-status"></a>Personāla atlases pieprasījuma pozīcijas statuss

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīta personāla atlases pieprasījuma pozīcijas statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmrecruitingrequestpositionstatus

Šis uzskaitījums nodrošina opciju, kas iestatīta katras personāla atlases pozīcijas pieprasījuma statusa vērtībām entītijā RecruitingRequestPosition.

| Vērtība | Iezīme | Apraksts |
| --- | --- | --- |
| 200000000 | Atvērtās | Pozīcija personāla atlases pieprasījumā ir atvērta personāla atlasei. Tas nenorāda, ka šim amatam pašlaik nav aktīva amata piešķires. Personāla atlases laikā amatā var būt darbinieks. Tas norāda tikai to, ka amats ir pieejams personāla atlasei personāla atlases pieprasījuma kontekstā. |
| 200000001 | Aizpildīts | Darbinieks ir atlasīts amata piešķirei. |
| 200000002 | Atcelts | Pieprasījums pieņemt darbā šo amatu ir atcelts. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]