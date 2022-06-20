---
title: Personāla atlases pieprasījuma statuss
description: Šajā rakstā ir aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859609"
---
# <a name="recruiting-request-status"></a>Personāla atlases pieprasījuma statuss


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta Dynamics 365 Human Resources.

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
