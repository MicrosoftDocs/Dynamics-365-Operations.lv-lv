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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059188"
---
# <a name="recruiting-request-status"></a>Personāla atlases pieprasījuma statuss

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