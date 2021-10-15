---
title: MK versijas noteikšana
description: Ja krājuma noklusējuma pasūtījuma veids ir Ražošana, tad pieprasījuma izvēršanas laikā plānošanas programmā tiek atrasta derīga MK versija, pamatojoties uz atrašanās vietu.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370091eed4ee050031d5d135aa7b1d8d0fe82491
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570973"
---
# <a name="determine-the-bom-version"></a>MK versijas noteikšana

[!include [banner](../includes/banner.md)]

Ja krājuma noklusējuma pasūtījuma veids ir Ražošana, tad pieprasījuma izvēršanas laikā plānošanas programmā tiek atrasta derīga MK versija, pamatojoties uz atrašanās vietu. 

Vietas dimensija vienmēr ir zināma, un tā ir norādīta pieprasījuma transakcijā. Tālāk aprakstītais process tiek lietots, lai noteiktu, kuru MK versiju izmantot:

-   Ja pieprasījuma vietā krājumam ir definēta MK versija, tiek lietots vietai specifiskais MK.
-   Ja pieprasījuma vietā krājumam nav definēta no vietas atkarīga MK versija, tiek lietots vispārīgs MK. Vispārīgais MK nenosaka vietu, tas ir derīga vairākām vietām. Ja pastāv vispārīgs MK, tiek izmantots tas.
-   Ja nav izmantojamas vispārīgas MK versijas, pieprasījuma izvēršana šajā vietā apstājas.

Derīgai MK versijai, vietai specifiskai vai vispārīgai, jāatbilst vajadzīgajiem datuma un daudzuma kritērijiem.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]