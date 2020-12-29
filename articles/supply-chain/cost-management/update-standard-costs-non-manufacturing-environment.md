---
title: Standarta izmaksu atjaunināšana vidē, kas nav saistīta ar ražošanu
description: Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas vidē, kas nav saistīta ar ražošanu.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dca3012952b739a75a6930908752fba73a4550
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432726"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="6a8f3-103">Standarta izmaksu atjaunināšana vidē, kas nav saistīta ar ražošanu</span><span class="sxs-lookup"><span data-stu-id="6a8f3-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a8f3-104">Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas vidē, kas nav saistīta ar ražošanu.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="6a8f3-105">Norādījumi tālāk tiek sniegti, pieņemot, ka standarta izmaksu atjaunināšanai tiek izmantota divu versiju pieeja.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="6a8f3-106">Izmantojot šo pieeju, viena izmaksu aprēķināšanas versija ietver standarta izmaksas, kas sākotnēji ir noteiktas uz fiksētu periodu, un otra izmaksu aprēķināšanas versija ietver inkrementālos atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="6a8f3-107">Visi atjauninājumi tiek ievadīti kā izmaksu ieraksti, kas ir ietverti otrā izmaksu aprēķināšanas versijā, un galu galā tiek iespējoti.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="6a8f3-108">Papildu vienas versijas pieeja izmanto sākotnēji definētu standarta izmaksu kopu.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="6a8f3-109">Lai varētu izmantot divu versiju pieeju, jādefinē otra izmaksu aprēķināšanas versija.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="6a8f3-110">Tālāk ir sniegtas norādes, ka definēt šo izmaksu aprēķināšanas versiju.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="6a8f3-111">Piešķiriet izmaksu aprēķināšanas veidu **Standartizmaksas**.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="6a8f3-112">Piešķiriet jēgpilnu identifikatoru, kas norāda izmaksu aprēķināšanas versijas komponentus, piemēram, **2016-ATJAUNINĀJUMI**.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="6a8f3-113">Pārliecināties, ka saturā ir ietverti izmaksu ieraksti.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="6a8f3-114">Atļaujiet visām vietām ievadīt izmaksu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="6a8f3-115">Ja tiek norādīta vietu, izmaksu ierakstus var ievadīt tikai šai vietai.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="6a8f3-116">Norādiet regresa principu **Nav**.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="6a8f3-117">Regresa princips attiecas tikai uz ražoto krājumu izmaksu aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="6a8f3-118">Lai labotu, pielāgotu vai atjauninātu jauno krājumu standarta izmaksas, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="6a8f3-119">Izmantojiet lapu **Izmaksu aprēķināšanas versijas** **iestatījumi**, lai iespējotu otrajā izmaksu aprēķināšanas versijā ievadāmos izmaksu datus.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="6a8f3-120">Papildus var nepieļaut neapstiprinātu izmaksu aktivizāciju, lai aktivizācija tādējādi ir atļauta tikai tad, kad neapstiprinātās izmaksas ir pilnībā un precīzi definētas.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="6a8f3-121">Var arī papildus ievadīt datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="6a8f3-122">Kā vispārīgu norādi izmantojiet datumu, kad tiek plānots iespējot inkrementālos atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="6a8f3-123">Ar izmaksu aprēķināšanu saistīto lauku **No datuma** var atstāt arī tukšu, bet pēc tam katram izmaksu ierakstam ievadiet datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="6a8f3-124">Izmantojiet lapu **Krājuma cena**, lai ievadītu atjauninājumus kā krājumu izmaksu ierakstus, kas ir ietverti otrajā izmaksu aprēķināšanas versijā.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="6a8f3-125">Izmantojiet pārskatu **Krājuma cenas**, lai pārbaudītu otrajā izmaksu aprēķināšanas versijā iekļauto krājuma izmaksu ierakstu aizpildīšanu un precizitāti.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="6a8f3-126">Izmantojiet lapu **Izmaksu aprēķināšanas versijas uzturēšana**, lai mainītu bloķējošo karodziņu un tādējādi atļautu otrajā izmaksu aprēķināšanas versijā iekļauto neapstiprināto izmaksu ierakstu aktivizēšanu.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="6a8f3-127">Izmantojiet lapu **Aktivizēt cenas** (ko var atvērt, izmantojot lapu **Izmaksu aprēķināšanas versijas uzturēšana**), lai atļautu visu otrajā izmaksu aprēķināšanas versijā iekļauto neapstiprināto krājumu izmaksu ierakstu aktivizēšanu.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="6a8f3-128">Var aktivizēt arī atsevišķu krājumu neapstiprināto izmaksu ierakstus, lapā **Krājuma cena** noklikšķinot uz pogas **Aktivizēt neapstiprinātās cenas**.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="6a8f3-129">Lai nepieļautu papildu datu uzturēšanu, izmantojiet lapu **Izmaksu aprēķināšanas versijas iestatīšana**, lai mainītu bloķējošos karodziņus, kas ir iekļauti otrajā izmaksu aprēķināšanas versijā.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="6a8f3-130">Bloķēšana novērsīs jaunu nenokārtotu izmaksu ievadi un nenokārtoto izmaksu aktivizāciju.</span><span class="sxs-lookup"><span data-stu-id="6a8f3-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>




