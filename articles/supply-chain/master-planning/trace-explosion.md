---
title: Izsekošanas izmantošana izvēršanai
description: Šajā rakstā ir paskaidrots, kā varat izmantot izsekošanu, lai izpētītu pasūtījuma izvērsuma iznākuma cēloņus.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e777d69c9da8a19c186bca3ca591e59af232f0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978084"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="104e2-103">Izsekošanas izmantošana izvēršanai</span><span class="sxs-lookup"><span data-stu-id="104e2-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="104e2-104">Šajā rakstā ir paskaidrots, kā varat izmantot izsekošanu, lai izpētītu pasūtījuma izvērsuma iznākuma cēloņus.</span><span class="sxs-lookup"><span data-stu-id="104e2-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="104e2-105">Iespējojot izsekošanu, varat skatīt informāciju par faktoriem, kas ietekmē konkrēta pasūtījuma izvēršanas rezultātu.</span><span class="sxs-lookup"><span data-stu-id="104e2-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="104e2-106">Nākamajos piemēros ir parādīts, kā varat izmantot izsekošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="104e2-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="104e2-107">Skatiet attiecības starp darbībām plānotajos pasūtījumos, lai optimizētu piegādes ķēdi un krājumu rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="104e2-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="104e2-108">Skatiet attiecības ar pasūtījumiem, kas jau ir apstiprināti.</span><span class="sxs-lookup"><span data-stu-id="104e2-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="104e2-109">Varat koncentrēties uz atvasināto pieprasījumu automātisku apstiprināšanu un pēc tam precīzāk norādīt pasūtījumu prioritāti.</span><span class="sxs-lookup"><span data-stu-id="104e2-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="104e2-110">Simulējiet plānošanas rezultātus, lai noteiktu, vai plānošanas parametri ir optimāli.</span><span class="sxs-lookup"><span data-stu-id="104e2-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="104e2-111">Identificējiet, kā tika noteikta tāda informācija kā ražošanas datumi, daudzumi un pasūtījumu prioritātes.</span><span class="sxs-lookup"><span data-stu-id="104e2-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="104e2-112">Varat skatīt detalizētu informāciju par aizkavējumiem un darbībām atlasītajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="104e2-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="104e2-113">Lapā **Izvēršana** izsekošanas informācija ir pieejama cilnē **Skaidrojums**, kas atrodas augšēja rūtī.</span><span class="sxs-lookup"><span data-stu-id="104e2-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="104e2-114">Izsekošana notiek, kad izvēršat pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="104e2-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="104e2-115">Lai sāktu pasūtījuma izsekošanu, noklikšķiniet uz **Atjaunināt** un pēc tam atzīmējiet izvēles rūtiņu **Iespējot izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="104e2-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="104e2-116">Varat izmantot lauku **Atrast tekstu**, lai žurnālā meklētu noteiktu informāciju.</span><span class="sxs-lookup"><span data-stu-id="104e2-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="104e2-117">Meklēšanas rezultāti tiek iezīmēti koka struktūrā.</span><span class="sxs-lookup"><span data-stu-id="104e2-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="104e2-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="104e2-118">Additional resources</span></span>
--------

[<span data-ttu-id="104e2-119">Vispārējo plānu pārskats</span><span class="sxs-lookup"><span data-stu-id="104e2-119">Master plans overview</span></span>](master-plans.md)



