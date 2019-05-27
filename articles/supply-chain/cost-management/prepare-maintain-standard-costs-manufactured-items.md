---
title: Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas
description: Šajā tēmā aprakstītas darbības, kas jāveic, lai sagatavotos ražoto krājumu izmaksu uzturēšanai.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbd7344f3d542cbd46e3568d8a7911ab4ab53b17
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545952"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="14ee3-103">Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas</span><span class="sxs-lookup"><span data-stu-id="14ee3-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14ee3-104">Šajā tēmā aprakstītas darbības, kas jāveic, lai sagatavotos ražoto krājumu izmaksu uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="14ee3-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="14ee3-105">Ražotajiem krājumiem veicamās darbības nedaudz atšķiras no iegādātajiem krājumiem izmantotajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="14ee3-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="14ee3-106">Ražotajiem krājumiem piešķirtās politikas var ietekmēt ražoto vecākkrājumu izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="14ee3-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="14ee3-107">Lai sagatavotos ražoto krājumu izmaksu uzturēšanai, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="14ee3-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="14ee3-108">Piešķiriet ražotajam krājumam modeļa grupu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="14ee3-109">Krājumu modeļa grupa identificē standarta izmaksu lietojumu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="14ee3-110">Piešķiriet grupu ražotajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="14ee3-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="14ee3-111">Krājuma grupa satur virsgrāmatas kontus, kas attiecas uz ražoto krājumu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="14ee3-112">Ražotā krājuma ar standarta izmaksu krājumu modeli virsgrāmatas konti ietver vairākas ražošanas novirzes, izmaksu maiņas novirzi un krājumu izmaksu pārvērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="14ee3-113">Piešķiriet šim krājumam mērvienību.</span><span class="sxs-lookup"><span data-stu-id="14ee3-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="14ee3-114">Krājumu izmaksas vienmēr tiek attēlotas krājumu mērvienībās.</span><span class="sxs-lookup"><span data-stu-id="14ee3-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="14ee3-115">Nepiešķiriet ražotajam krājumam izmaksu grupu, ja vien tas netiks uzskatīts par iegādātu krājumu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="14ee3-116">Piešķiriet ražotajam krājumam materiālu komplekta (MK) aprēķinu grupu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="14ee3-117">Krājuma MK aprēķinu grupa definē lietojamus brīdinājuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="14ee3-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="14ee3-118">Šādi, kad ir pabeigts MK aprēķins, var ģenerēt brīdinājuma ziņojumus par iespējamiem aprēķinu kļūdu avotiem.</span><span class="sxs-lookup"><span data-stu-id="14ee3-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="14ee3-119">Piemēram, brīdinājuma ziņojums var identificēt gadījumu, kad nepastāv aktīvs MK vai maršruts.</span><span class="sxs-lookup"><span data-stu-id="14ee3-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="14ee3-120">MK aprēķinu grupa ietver izvēršanas apturēšanas politiku, kas norāda, kad ražots krājums jāuzskata par iegādātu krājumu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="14ee3-121">Ja ražotajam krājumam ir konstantas izmaksas, piešķiriet tam standarta pasūtījuma daudzumu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="14ee3-122">Standarta pasūtījuma daudzums ir uzskaites laidiena apjoms konstantu izmaksu amortizēšanai.</span><span class="sxs-lookup"><span data-stu-id="14ee3-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="14ee3-123">Konstantu izmaksu piemēri ietver maršrutēšanas operāciju iestatīšanas laiku un konstantu komponentu daudzumu materiālu komplektā.</span><span class="sxs-lookup"><span data-stu-id="14ee3-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="14ee3-124">Definējiet MK ražotajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="14ee3-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="14ee3-125">Ražotajam krājumam var tikt definēta viena vai vairākas MK versijas.</span><span class="sxs-lookup"><span data-stu-id="14ee3-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="14ee3-126">Apstipriniet, ka jums vajadzīgās versijas ir atzīmētas kā apstiprinātas un aktīvas un tām ir jums vajadzīgie spēkā stāšanās datumi.</span><span class="sxs-lookup"><span data-stu-id="14ee3-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="14ee3-127">MK versija var būt uzņēmuma mēroga vai vietas mēroga.</span><span class="sxs-lookup"><span data-stu-id="14ee3-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="14ee3-128">Definējiet ražotā krājuma maršrutēšanu.</span><span class="sxs-lookup"><span data-stu-id="14ee3-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="14ee3-129">Ražotajam krājumam var tikt definēta viena vai vairākas maršruta versijas.</span><span class="sxs-lookup"><span data-stu-id="14ee3-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="14ee3-130">Apstipriniet, ka jums vajadzīgās versijas ir atzīmētas kā apstiprinātas un aktīvas un tām ir jums vajadzīgie spēkā stāšanās datumi.</span><span class="sxs-lookup"><span data-stu-id="14ee3-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="14ee3-131">Maršruta versijai jābūt vietas mēroga.</span><span class="sxs-lookup"><span data-stu-id="14ee3-131">The route version must be site-specific.</span></span>

<span data-ttu-id="14ee3-132">Ja maršrutēšanas informāciju vēlaties izmantot izmaksu aprēķināšanai, ir javeic papildu sagatavošanās soļi.</span><span class="sxs-lookup"><span data-stu-id="14ee3-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="14ee3-133">Piemēram, maršrutēšanas operācijām piešķirtajām izmaksu kategorijām ir jābūt pareizām un pabeigtām.</span><span class="sxs-lookup"><span data-stu-id="14ee3-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="14ee3-134">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="14ee3-134">Related topics</span></span>
--------

[<span data-ttu-id="14ee3-135">Ražotā krājuma konstanto izmaksu amortizācija</span><span class="sxs-lookup"><span data-stu-id="14ee3-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="14ee3-136">Saražojamo vai sagādājamo preču iestatīšana</span><span class="sxs-lookup"><span data-stu-id="14ee3-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

