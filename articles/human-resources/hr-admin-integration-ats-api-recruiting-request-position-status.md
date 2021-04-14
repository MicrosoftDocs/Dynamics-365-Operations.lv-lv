---
title: Personāla atlases pieprasījuma pozīcijas statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma pozīcijas statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789736"
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