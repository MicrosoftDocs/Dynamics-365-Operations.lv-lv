---
title: Ienākošo dokumentu parsēšana Excel formātā
description: Šajā tēmā ir sniegta informācija par elektronisko pārskatu izveides (Electronic Reporting — ER) formātu izstrādi ienākošo Microsoft Excel failu satura parsēšanai.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3f83271327df186d407516ff1a197800ffc8c78c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249360"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Ienākošo dokumentu parsēšana Excel formātā

[!include[banner](../includes/banner.md)]

Varat izstrādāt tādus elektronisko pārskatu izveides (ER) formātus ienākošo Microsoft Excel failus parsēšanai, kas atveido Microsoft Excel darbgrāmatās (XLSX formāta failos) ietvertos datus. Pēc tam saturu no šiem failiem varat izmantot, lai atjauninātu programmas datus. Tas ir noderīgi tālāk norādītajos gadījumos.

- Esat noformējis jaunu modeli un formātu un vēlaties tos pārbaudīt izpildlaikā. Tādā gadījumā programma Excel simulē faktiskos programmas datus.
- Pārvaldāt datus ārpus jūsu programmas programmā Excel un vēlaties šos datus importēt, lai iesniegtu noteiktu pārskatu.

Lai uzzinātu vairāk par šo līdzekli, noskatieties uzdevumu ceļvežus **ER: datu importēšana no Microsoft Excel faila (1. daļa. Formāta izstrāde)** un **ER: datu importēšana no Microsoft Excel faila (2. daļa. Datu importēšana)** (tie ir ietverti biznesa procesā 7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)). Šajos uzdevumu ceļvežos ir izklāstīts, kā ienākošo Excel failu var parsēt, izmantojot ER formātu, lai importētu informāciju no ienākošiem dokumentiem un atjauninātu programmas datus. Šo uzdevumu ceļvežu failus varat lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).

Lai izpildītu iepriekš minētos uzdevumu ceļvežus, lejupielādējiet tālāk norādītos failus.

| Satura apraksts                         | Fails                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Ienākošais fails .XLSX formātā — veidne    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Ienākošais fails .XLSX formātā — datu paraugs | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Ja vēl neesat atskaņojis tālāk norādīto uzdevuma ceļvedi, [ER Nepieciešamo konfigurāciju izveide datu importēšanai no ārēja faila](./tasks/er-required-configurations-import-data.md) pašreizējā Finance and Operations programmā, lejupielādējiet tālāk norādīto failu.

| Satura apraksts    | Fails                                                            |
|------------------------|-----------------------------------------------------------------|
| ER modeļa konfigurācija | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |