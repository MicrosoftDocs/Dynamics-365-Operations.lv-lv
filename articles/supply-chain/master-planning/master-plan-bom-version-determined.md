---
title: MK versijas noteikšana
description: Ja krājuma noklusējuma pasūtījuma veids ir Ražošana, tad pieprasījuma izvēršanas laikā plānošanas programmā tiek atrasta derīga MK versija, pamatojoties uz atrašanās vietu.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6f1f1656f0ef04799b1ce6b397dac0f829e41c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251941"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="bb4b3-103">MK versijas noteikšana</span><span class="sxs-lookup"><span data-stu-id="bb4b3-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb4b3-104">Ja krājuma noklusējuma pasūtījuma veids ir Ražošana, tad pieprasījuma izvēršanas laikā plānošanas programmā tiek atrasta derīga MK versija, pamatojoties uz atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="bb4b3-105">Vietas dimensija vienmēr ir zināma, un tā ir norādīta pieprasījuma transakcijā.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="bb4b3-106">Tālāk aprakstītais process tiek lietots, lai noteiktu, kuru MK versiju izmantot.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="bb4b3-107">Ja pieprasījuma vietā krājumam ir definēta MK versija, tiek lietots vietai specifiskais MK.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="bb4b3-108">Ja pieprasījuma vietā krājumam nav definēta no vietas atkarīga MK versija, tiek lietots vispārīgs MK.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="bb4b3-109">Vispārīgais MK nenosaka vietu, tas ir derīga vairākām vietām.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="bb4b3-110">Ja pastāv vispārīgs MK, tiek izmantots tas.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="bb4b3-111">Ja nav izmantojamas vispārīgas MK versijas, pieprasījuma izvēršana šajā vietā apstājas.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="bb4b3-112">Derīgai MK versijai, vietai specifiskai vai vispārīgai, jāatbilst vajadzīgajiem datuma un daudzuma kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]