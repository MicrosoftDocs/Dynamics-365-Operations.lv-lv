---
title: Projekta pārdošanas pasūtījumi laika un materiāla projektiem
description: Šajā tēmā ir sniegta informācija par to, kā izveidot no projekta atkarīgus pārdošanas pasūtījumus laika un materiāla projektiem.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 2f27e3e0a2d6aadc4c5224b55f8a416cbe4e83aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551206"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projekta pārdošanas pasūtījumi laika un materiāla projektiem

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegta informācija par to, kā izveidot projekta pārdošanas pasūtījumu. Pārdošanas pasūtījumus var izmantot tikai tipa **Laiks un materiāls** projektiem.

Ja laika un materiāla projektam projekta līgumā ir vairāki finansējuma avoti, parametru lapā **Projektu pārvaldības un uzskaites parametri** ir jāiespējo parametrs **Atļaut pārdošanas pasūtījumus projektiem ar vairākiem finansējuma avotiem**. 

> [!NOTE]
> - Projekta pārdošanas pasūtījumu ar vairākiem finansējuma avotiem atbalsts ir pieejams, sākot ar programmas laidiena 10.0.2 un jaunāku versiju.
> - Parametrs projekta pārdošanas pasūtījumu ar vairākiem finansējuma avotiem atbalsta iespējošanai tiks noņemts 2020. gada aprīļa laidiena kopumā, pēc kura funkcionalitāte vienmēr būs iespējota.

No projekta atkarīgus pārdošanas pasūtījumus var izveidot divējādi.

- Atveriet konkrēto projektu. Darbību rūtī atlasiet **Pārvaldīt > Krājumu uzdevumi > Pārdošanas pasūtījums**. Informācijā par projektu pēc noklusējuma tiek iekļauts projekta pārdošanas pasūtījums. Ja projekta līgumā ir iekļauts vairāk nekā viens finansējuma avots, vispirms ir jāatlasa finansējuma avots, lai varētu iestatīt pārdošanas pasūtījuma debitoru. Ja ir iekļauts tikai viens projekta finansējuma avots, debitors tiek iestatīts automātiski.
- Atveriet saraksta lapu **Visi pārdošanas pasūtījumi** un izveidojiet jaunu pārdošanas pasūtījumu. Ir jāatlasa projekta pārdošanas pasūtījums. Kad projekts ir atlasīts, debitors tiek iestatīts pēc finansējuma avota vai arī ir jāatlasa finansējuma avots, ja projekta līgumā ir ietverti vairāki finansējuma avoti.

