---
title: Izpildes statuss
description: Šajā tēmā aprakstīta opcija Izpildes statuss, kas iestatīta programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468207"
---
# <a name="completion-status"></a>Izpildes statuss 

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