---
title: MyLeaveRequests pārskats
description: MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 724c4c91e38bb8ac9fe1fd0794dc5a79b2435472
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339743"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests pārskats

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.

## <a name="key"></a>Taustiņš

  | Rekvizīta nosaukums | Datu veids |
  |---------------|-----------|
  | dataAreaId    | Virkne    |
  | RequestId     | Virkne    |
  | LeaveType     | Virkne    |
  | LeaveDate     | Datums      |
  
## <a name="properties"></a>Rekvizīti

  | Rekvizīta nosaukums     | Datu veids | Pieprasīts |
  |-------------------|-----------|----------|
  | dataAreaId        | Virkne    | X        |
  | RequestId         | Virkne    | X        |
  | LeaveType         | Virkne    | X        |
  | LeaveDate         | Datums      | X        |
  | ReasonCodeId      | Virkne    |          |
  | PersonnelNumber   | Virkne    | X        |
  | RequestDate       | Datums      | X        |
  | Komentārs           | Virkne    |          |
  | Statuss            | Uzskaitījums      | X        |
  | Apjoms            | Reāls      |          |
  | HalfDayDefinition | Uzskaitījums      |          |

## <a name="actions"></a>Darbības

 | Darbības nosaukums                               | Apraksts                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [iesniegt](hr-developer-api-myleaverequests-submit.md)   | Iesniedziet darbplūsmā apstrādājamo pieprasījumu. |

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājuma pieprasījuma iesniegšana darbplūsmai](hr-developer-api-myleaverequests-submit.md)
- [Autentifikācija](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]