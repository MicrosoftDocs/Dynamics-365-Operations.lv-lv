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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803637"
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