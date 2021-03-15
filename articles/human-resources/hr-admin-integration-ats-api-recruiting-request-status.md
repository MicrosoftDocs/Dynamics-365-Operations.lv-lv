---
title: Personāla atlases pieprasījuma statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125958"
---
# <a name="recruiting-request-status"></a>Personāla atlases pieprasījuma statuss

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