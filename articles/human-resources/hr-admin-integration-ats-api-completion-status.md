---
title: Izpildes statuss
description: Šajā tēmā aprakstīta opcija Izpildes statuss, kas iestatīta programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: da91084d30873b79033d789beab829da9fbdb010
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065550"
---
# <a name="completion-status"></a>Izpildes statuss


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīta opcija Izpildes statuss, kas iestatīta programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmcompletionstatus

Šis uzskaitījums sniedz statusa vērtību opciju kopu kandidātu ieteikšanai. 

| Vērtība | Iezīme | Apraksts |
| --- | --- | --- |
| 200000000 | Nepabeigta | Kandidātam vēl nav pabeigta izvērtēšana. |
| 200000001 | Pāreja | Kandidātam ir veikta izvērtēšana. |
| 200000002 | Neizdevās | Kandidātas neatbilst izvērtēšanas prasībām. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
