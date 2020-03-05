---
title: Variantu grupas izveide
description: Šajā tēmā aprakstīts, kā izveidot preces izmēru, stilu vai krāsu variantu grupu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001879"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="57b21-103">Variantu grupas izveide</span><span class="sxs-lookup"><span data-stu-id="57b21-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="57b21-104">Šajā tēmā aprakstīts, kā izveidot preces izmēru, stilu vai krāsu variantu grupu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="57b21-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="57b21-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="57b21-105">Overview</span></span>

<span data-ttu-id="57b21-106">Dynamics 365 Commerce atbalsta vairākus preču variantus.</span><span class="sxs-lookup"><span data-stu-id="57b21-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="57b21-107">Vislabāk iestatīt variantu grupas dažādām preču kategorijām.</span><span class="sxs-lookup"><span data-stu-id="57b21-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="57b21-108">Piemēram, izmēru grupu var izveidot t-krekliem, kuru izmēri ir īpaši mazi, mazi, vidēji, lieli un īpaši lieli, vai krāsu grupu var izveidot, lai iekļautu visas pieejamās preces krāsas.</span><span class="sxs-lookup"><span data-stu-id="57b21-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="57b21-109">Pirms preču pievienošanas ir jāpievieno variantu grupas.</span><span class="sxs-lookup"><span data-stu-id="57b21-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="57b21-110">Šajā tēmā tiks izveidota un konfigurēta izmēra grupa.</span><span class="sxs-lookup"><span data-stu-id="57b21-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="57b21-111">Līdzīgas procedūras var izmantot stilu grupu un krāsu grupu pievienošanai un konfigurēšanai.</span><span class="sxs-lookup"><span data-stu-id="57b21-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="57b21-112">Izmēra grupas izveide</span><span class="sxs-lookup"><span data-stu-id="57b21-112">Create a size group</span></span>

<span data-ttu-id="57b21-113">Lai izveidotu izmēra grupu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="57b21-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="57b21-114">Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Variantu grupas \> Izmēru grupas**.</span><span class="sxs-lookup"><span data-stu-id="57b21-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="57b21-115">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="57b21-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="57b21-116">Laukā **Izmēra grupa** ievadiet izmēra grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="57b21-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="57b21-117">Lodziņā **Apraksts** ievadiet atbilstošu aprakstu.</span><span class="sxs-lookup"><span data-stu-id="57b21-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="57b21-118">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="57b21-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="57b21-119">Atribūtu pievienošana izmēra grupai</span><span class="sxs-lookup"><span data-stu-id="57b21-119">Add attributes to the size group</span></span>

<span data-ttu-id="57b21-120">Lai pievienotu atribūtus izmēra grupai, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="57b21-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="57b21-121">Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Variantu grupas \> Izmēru grupas**</span><span class="sxs-lookup"><span data-stu-id="57b21-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="57b21-122">Navigācijas rūtī atlasiet izmēra grupu.</span><span class="sxs-lookup"><span data-stu-id="57b21-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="57b21-123">Sadaļā **Izmēru grupas rindas** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="57b21-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="57b21-124">Lodziņā **Izmērs** ievadiet virkni, kurā norādīts izmērs (piemēram, "XL").</span><span class="sxs-lookup"><span data-stu-id="57b21-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="57b21-125">Lodziņā **Izmēra nosaukums** ievadiet izmēra nosaukumu (piemēram, "Īpaši liels").</span><span class="sxs-lookup"><span data-stu-id="57b21-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="57b21-126">Lodziņā **Papildināšanas svars** ievadiet skaitli, kas norāda papildināšanas svaru.</span><span class="sxs-lookup"><span data-stu-id="57b21-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="57b21-127">Lodziņā **Numurs svītrkodā** ievadiet skaitli, kas norāda svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="57b21-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="57b21-128">Lodziņā **Rādīšanas secība** ievadiet skaitli, kas norāda rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="57b21-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="57b21-129">Kad izmēri pievienoti, darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="57b21-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="57b21-130">Tālāk redzamajā attēlā parādīts "brīvā stila krekla izmēru" izmēru grupas piemērs.</span><span class="sxs-lookup"><span data-stu-id="57b21-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Izmēra grupas izveide](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="57b21-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="57b21-132">Additional resources</span></span>

[<span data-ttu-id="57b21-133">Preču informācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="57b21-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="57b21-134">Mazumtirdzniecības preču iestatīšana</span><span class="sxs-lookup"><span data-stu-id="57b21-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="57b21-135">Preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="57b21-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)