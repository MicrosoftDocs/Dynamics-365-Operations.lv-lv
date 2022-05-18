---
title: MyLeaveRequests pārskats
description: Elements MyLeaveRequests programmā Microsoft Dynamics 365 Human Resources nodrošina atvaļinājumu pieprasījumu sarakstu.
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717060"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests pārskats


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
