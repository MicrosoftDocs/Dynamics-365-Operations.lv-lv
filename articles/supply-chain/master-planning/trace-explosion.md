---
title: "Izsekošanas izmantošana izvēršanai"
description: "Šajā rakstā ir paskaidrots, kā varat izmantot izsekošanu, lai izpētītu pasūtījuma izvērsuma iznākuma cēloņus."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f3891688542ac6d4f9afce026808c65992a592d4
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="use-tracing-for-explosion"></a><span data-ttu-id="7c1de-103">Izsekošanas izmantošana izvēršanai</span><span class="sxs-lookup"><span data-stu-id="7c1de-103">Use tracing for explosion</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7c1de-104">Šajā rakstā ir paskaidrots, kā varat izmantot izsekošanu, lai izpētītu pasūtījuma izvērsuma iznākuma cēloņus.</span><span class="sxs-lookup"><span data-stu-id="7c1de-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="7c1de-105">Iespējojot izsekošanu, varat skatīt informāciju par faktoriem, kas ietekmē konkrēta pasūtījuma izvēršanas rezultātu.</span><span class="sxs-lookup"><span data-stu-id="7c1de-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="7c1de-106">Nākamajos piemēros ir parādīts, kā varat izmantot izsekošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="7c1de-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="7c1de-107">Skatiet attiecības starp darbībām plānotajos pasūtījumos, lai optimizētu piegādes ķēdi un krājumu rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="7c1de-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="7c1de-108">Skatiet attiecības ar pasūtījumiem, kas jau ir apstiprināti.</span><span class="sxs-lookup"><span data-stu-id="7c1de-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="7c1de-109">Varat koncentrēties uz atvasināto pieprasījumu automātisku apstiprināšanu un pēc tam precīzāk norādīt pasūtījumu prioritāti.</span><span class="sxs-lookup"><span data-stu-id="7c1de-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="7c1de-110">Simulējiet plānošanas rezultātus, lai noteiktu, vai plānošanas parametri ir optimāli.</span><span class="sxs-lookup"><span data-stu-id="7c1de-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="7c1de-111">Identificējiet, kā tika noteikta tāda informācija kā ražošanas datumi, daudzumi un pasūtījumu prioritātes.</span><span class="sxs-lookup"><span data-stu-id="7c1de-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="7c1de-112">Varat skatīt detalizētu informāciju par aizkavējumiem un darbībām atlasītajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="7c1de-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="7c1de-113">Lapā **Izvēršana** izsekošanas informācija ir pieejama cilnē **Skaidrojums**, kas atrodas augšēja rūtī.</span><span class="sxs-lookup"><span data-stu-id="7c1de-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="7c1de-114">Izsekošana notiek, kad izvēršat pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="7c1de-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="7c1de-115">Lai sāktu pasūtījuma izsekošanu, noklikšķiniet uz **Atjaunināt** un pēc tam atzīmējiet izvēles rūtiņu **Iespējot izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7c1de-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="7c1de-116">Varat izmantot lauku **Atrast tekstu**, lai žurnālā meklētu noteiktu informāciju.</span><span class="sxs-lookup"><span data-stu-id="7c1de-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="7c1de-117">Meklēšanas rezultāti tiek iezīmēti koka struktūrā.</span><span class="sxs-lookup"><span data-stu-id="7c1de-117">Search results are highlighted in the tree.</span></span>

<a name="see-also"></a><span data-ttu-id="7c1de-118">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="7c1de-118">See also</span></span>
--------

[<span data-ttu-id="7c1de-119">Vispārējie plāni</span><span class="sxs-lookup"><span data-stu-id="7c1de-119">Master plans</span></span>](master-plans.md)




