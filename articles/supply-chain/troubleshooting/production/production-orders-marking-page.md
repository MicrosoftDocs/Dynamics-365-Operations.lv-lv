---
title: Ražošanas pasūtījumi netiek rādīti Marķējuma lapā
description: Daži ražošanas pasūtījumi netiek parādīti Marķējuma lapā. Šajā tēmā izskaidrotas trīs preču konfigurācijas, kurām nav pieejama marķēšana.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476930"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Ražošanas pasūtījumi netiek rādīti Marķējuma lapā

## <a name="symptoms"></a>Simptomi

Strādājot ar diskrēto ražošanu, daži ražošanas pasūtījumi netiek rādīti **Marķējuma** lapā.

## <a name="resolution"></a>Novēršana

Marķēšanai nav pieejamas preces ar šādu konfigurāciju. Tāpēc tie netiks parādīti **Marķējuma** lapā:

- Preces tiek definētas kā *pieļaujamā svara* veida preces.
- Tās ir iespējotas papildu noliktavas procesiem.
- Tās ir konfigurētas tā, lai tās varētu kontrolēt ar *Standarta izmaksu* principu.
