---
title: Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana
description: Šajā tēmā aprakstīts, kā jaunināt vienotu dokumentu žurnālu un valūtas pārvērtēšanu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559525"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana

[!include [banner](../includes/banner.md)]

Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem. Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.

Veiciet šīs darbības, jauninot uz Microsoft Dynamics 365 for Operations versiju 1611.

1.  Pirms veicat jaunināšanu uz programmu Finance and Operations, izpildiet ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem. Laukā **Metode** iestatiet vienumu **Rēķina datums**. Tiek izveidota pārvērtēšanas darbība, kas atceļ pēdējo ārvalstu valūtas pārvērtēšanu. Tādējādi atvērtās darbības tiek vērtētas pēc to sākotnējās uzskaites valūtas.
2.  Jauniniet uz versiju 1611.
3.  Vēlreiz izpildiet ārvalstu valūtas pārvērtēšanu debitoru un kreditoru parādiem. Šoreiz laukā **Metode** iestatiet vienumu **Standarta**. Tiek izveidota jauna pārvērtēšanas darbība, kas ir balstīta uz pašreizējiem maiņas kursiem. Ar šo darbību tiek ierakstīta nerealizētā peļņa/zaudējumi un pareizais Virsgrāmatas kopsavilkuma konts.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]