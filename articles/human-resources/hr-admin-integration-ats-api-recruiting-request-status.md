---
title: Personāla atlases pieprasījuma statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: d845179077fc2e04dfb3bd05eaa70b0a2a016121
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067105"
---
# <a name="recruiting-request-status"></a>Personāla atlases pieprasījuma statuss


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmrecruitingrequeststatus

Šis uzskaitījums sniedz vienuma RecruitingRequest statusa vērtību opciju kopu.

| Vērtība | Iezīme | Apraksts |
| --- | --- | --- |
| 200000000 | Melnraksts | Pieprasījums ir melnrakstā un nav gatavs aktīvai personāla atlasei. |
| 200000001 | Pārskatīšanā | Pieprasījums ir iesniegts un tiek maršrutēts apstiprināšanai ar darbplūsmu. Pieejams tikai tad, ja darbplūsma ir iespējota. |
| 200000002 | Gaida | Pieprasījums gaida darbplūsmas darbību. Pieejams tikai tad, ja darbplūsma ir iespējota. |
| 200000003 | Atcelts | Pieprasījums ir atcelts. Pieejams tikai tad, ja darbplūsma ir iespējota. |
| 200000004 | Liegts | Pieprasījums ir noraidīts. Pieejams tikai tad, ja darbplūsma ir iespējota. |
| 200000005 | Aktīvie | Darbplūsma tiek pabeigta un apstiprināta, un pieprasījums ir gatavs aktīvai personāla atlasei. |
| 200000006 | Slēgtas | Personāla atlases pieprasījums ir slēgts. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
