---
title: Darba nodokļu atvieglojumu statuss
description: Šajā tēmā aprakstīta opciju kopa Darba nodokļu atvieglojumu statuss, kas iestatīta programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464456"
---
# <a name="job-exempt-status"></a>Darba nodokļu atvieglojumu statuss

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīta opciju kopa Darba nodokļu atvieglojumu statuss, kas iestatīta programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: cdm_jobexemptstatus

Šis uzskaitījums precizē opciju kopu FLSA Darba nodokļu atvieglojumu statusa vērtībām. Tas ir nodrošināts esošajā cdm_jobexemptstatus opciju kopā.

| Vērtība | Iezīme | Apraksts |
| --- | --- | --- |
| 200000000 | Neapliekams | Darbam ir neapliekams statuss, kas pamatots uz FLSA vadlīnijām. |
| 200000001 | NonExempt | Darbam nav neapliekams statuss, kas pamatots uz FLSA vadlīnijām. |
| 200000002 | Nav piemērojams | FLSA statusa vadlīnijas neattiecas uz darbu. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]