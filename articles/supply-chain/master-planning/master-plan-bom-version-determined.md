---
title: "MK versijas noteikšana"
description: "Ja krājuma noklusējuma pasūtījuma veids ir Ražošana, tad pieprasījuma izvēršanas laikā plānošanas programmā tiek atrasta derīga MK versija, pamatojoties uz atrašanās vietu."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ceeb82130a3ab214ef3e9eda09294c9bcc0c7cc0
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="determine-the-bom-version"></a>MK versijas noteikšana

[!include[banner](../includes/banner.md)]


Ja krājuma noklusējuma pasūtījuma veids ir Ražošana, tad pieprasījuma izvēršanas laikā plānošanas programmā tiek atrasta derīga MK versija, pamatojoties uz atrašanās vietu. 

Vietas dimensija vienmēr ir zināma, un tā ir norādīta pieprasījuma transakcijā. Tālāk aprakstītais process tiek lietots, lai noteiktu, kuru MK versiju izmantot.

-   Ja pieprasījuma vietā krājumam ir definēta MK versija, tiek lietots vietai specifiskais MK.
-   Ja pieprasījuma vietā krājumam nav definēta no vietas atkarīga MK versija, tiek lietots vispārīgs MK. Vispārīgais MK nenosaka vietu, tas ir derīga vairākām vietām. Ja pastāv vispārīgs MK, tiek izmantots tas.
-   Ja nav izmantojamas vispārīgas MK versijas, pieprasījuma izvēršana šajā vietā apstājas.

Derīgai MK versijai, vietai specifiskai vai vispārīgai, jāatbilst vajadzīgajiem datuma un daudzuma kritērijiem.






