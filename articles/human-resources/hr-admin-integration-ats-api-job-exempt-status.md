---
title: Darba nodokļu atvieglojumu statuss
description: Šajā tēmā aprakstīta opciju kopa Darba nodokļu atvieglojumu statuss, kas iestatīta programmai Dynamics 365 Human Resources .
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798301"
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