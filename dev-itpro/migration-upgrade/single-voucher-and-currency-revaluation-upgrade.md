---
title: "Viena dokumenta un valūtas pārvērtēšanas jauninājums"
description: "Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem. Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3c6d817424be79b09ccdd89deb7f31599fe9bf5
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Viena dokumenta un valūtas pārvērtēšanas jauninājums

[!include[banner](../includes/banner.md)]


Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem. Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.

Veiciet šīs darbības, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.

1.  Pirms veicat jaunināšanu uz programmu Dynamics 365 for Operations, izpildiet ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem. Laukā **Metode** iestatiet vienumu **Rēķina datums**. Tiek izveidota pārvērtēšanas darbība, kas atceļ pēdējo ārvalstu valūtas pārvērtēšanu. Tādējādi atvērtās darbības tiek vērtētas pēc to sākotnējās uzskaites valūtas.
2.  Jauniniet uz Dynamics 365 for Operations versiju 1611.
3.  Vēlreiz izpildiet ārvalstu valūtas pārvērtēšanu debitoru un kreditoru parādiem. Šoreiz laukā **Metode** iestatiet vienumu **Standarta**. Tiek izveidota jauna pārvērtēšanas darbība, kas ir balstīta uz pašreizējiem maiņas kursiem. Ar šo darbību tiek ierakstīta nerealizētā peļņa/zaudējumi un pareizais Virsgrāmatas kopsavilkuma konts.




