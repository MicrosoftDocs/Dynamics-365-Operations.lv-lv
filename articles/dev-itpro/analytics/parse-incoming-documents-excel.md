---
title: "Ienākošo dokumentu parsēšana Excel formātā"
description: "Šajā tēmā ir sniegta informācija par elektronisko pārskatu (Electronic Reporting — ER) formātu noformēšanu, lai parsētu ienākošajos Microsoft Excel failos esošo saturu."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 32fd82f0e46068c7ed7bfcfddc4ff84603bd20b4
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="parse-incoming-documents-in-excel-format"></a>Ienākošo dokumentu parsēšana Excel formātā

[!include[banner](../includes/banner.md)]

Varat noformēt elektronisko pārskatu (Electronic Reporting — ER) formātus tā, lai parsētu ienākošos Microsoft Excel failus, kas ataino datus Microsoft Excel darbgrāmatās (XLSX formāta failus). Pēc tam saturu no šiem failiem varat izmantot, lai atjauninātu programmas datus. Tas ir noderīgi tālāk norādītajos gadījumos.

- Esat noformējis jaunu modeli un formātu un vēlaties tos pārbaudīt izpildlaikā. Tādā gadījumā programma Excel simulē faktiskos programmas datus.
- Pārvaldāt datus ārpus jūsu programmas programmā Excel un vēlaties šos datus importēt, lai iesniegtu noteiktu pārskatu.

Lai par šo līdzekli uzzinātu vairāk, noskatieties uzdevumu ceļvežus **ER Datu importēšana no Microsoft Excel faila (1. daļa. Formāta noformēšana)** un **ER Datu importēšana no Microsoft Excel faila (2. daļa. Datu importēšana)** (tie veido daļu no 7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)). Šajos uzdevumu ceļvežos ir izklāstīts, kā ienākošo Excel failu var parsēt, izmantojot ER formātu, lai importētu informāciju no ienākošiem dokumentiem un atjauninātu programmas datus. Šo uzdevumu ceļvežu failus varat lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).

Lai izpildītu iepriekš minētos uzdevumu ceļvežus, lejupielādējiet tālāk norādītos failus.

| Satura apraksts                         | Fails                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Ienākošais fails .XLSX formātā — veidne    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Ienākošais fails .XLSX formātā — datu paraugs | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Ja vēl neesat atskaņojis tālāk norādīto uzdevuma ceļvedi, [ER Nepieciešamo konfigurāciju izveide datu importēšanai no ārēja faila](./tasks/er-required-configurations-import-data.md) pašreizējā Dynamics 365 for Finance and Operation programmā, lejupielādējiet tālāk norādīto failu.

| Satura apraksts    | Fails                                                            |
|------------------------|-----------------------------------------------------------------|
| ER modeļa konfigurācija | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |

