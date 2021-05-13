---
title: Kanālu navigācijas hierarhijas izveide
description: Šajā tēmā aprakstīts, kā izveidot kanālu navigācijas hierarhiju risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951912"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="62251-103">Izveidot kanāla navigācijas hierarhiju</span><span class="sxs-lookup"><span data-stu-id="62251-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="62251-104">Šajā tēmā aprakstīts, kā izveidot kanālu navigācijas hierarhiju risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="62251-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="62251-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="62251-105">Overview</span></span>

<span data-ttu-id="62251-106">Kanālu navigācijas hierarhiju lieto preču grupēšanai un kārtošanai kategorijās tā, lai preces var pārlūkot tiešsaistē vai pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="62251-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="62251-107">Kanālu navigācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="62251-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="62251-108">Lai izveidotu kanālu navigācijas hierarhiju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="62251-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="62251-109">Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Produkti un kategorijas \> Kanālu navigācijas kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="62251-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="62251-110">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="62251-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="62251-111">Lodziņā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="62251-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="62251-112">Lodziņā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="62251-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="62251-113">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="62251-113">Select **Create**.</span></span>
1. <span data-ttu-id="62251-114">Darbību rūtī atlasiet **Jauns kategoriju mezgls**, lai izveidotu saknes mezglu.</span><span class="sxs-lookup"><span data-stu-id="62251-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="62251-115">Lodziņā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="62251-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="62251-116">Lodziņā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="62251-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="62251-117">Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="62251-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="62251-118">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="62251-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="62251-119">Tālāk redzamajā attēlā ir parādīts saknes mezgla piemērs.</span><span class="sxs-lookup"><span data-stu-id="62251-119">The following image shows a example root node.</span></span>

![Saknes mezgla paraugs](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="62251-121">Navigācijas kategoriju mezglu izveide</span><span class="sxs-lookup"><span data-stu-id="62251-121">Create navigation category nodes</span></span>

<span data-ttu-id="62251-122">Lai izveidotu papildu navigācijas kategoriju mezglus, kas kanālā pārstāvēs preču kategorijas, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="62251-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="62251-123">Navigācijas rūtī atlasiet virsmezglu, lai tam pievienotu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="62251-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="62251-124">Darbību rūtī atlasiet **Jauns kategorijas zars**.</span><span class="sxs-lookup"><span data-stu-id="62251-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="62251-125">Lodziņā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="62251-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="62251-126">Lodziņā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="62251-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="62251-127">Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="62251-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="62251-128">Lodziņā **Rādīšanas secība** ievadiet rādīšanas secību (nav obligāti).</span><span class="sxs-lookup"><span data-stu-id="62251-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="62251-129">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="62251-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="62251-130">Tālāk redzamajā attēlā parādīts pabeigtas kanālu navigācijas hierarhijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="62251-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Kanālu hierarhijas paraugs](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="62251-132">Preču pievienošana kategoriju mezgliem</span><span class="sxs-lookup"><span data-stu-id="62251-132">Add products to category nodes</span></span>

<span data-ttu-id="62251-133">Lai pievienotu preces kategoriju mezgliem, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="62251-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="62251-134">Atlasiet kategoriju mezglu.</span><span class="sxs-lookup"><span data-stu-id="62251-134">Select a category node.</span></span>
1. <span data-ttu-id="62251-135">Sadaļā **Preces** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="62251-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="62251-136">Atrodiet jaunās preces, kuras vēlaties pievienot, izmantojot preces numuru vai preces nosaukumu, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="62251-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="62251-137">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="62251-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="62251-138">Preču pievienošana mezglam, kas atrodas kanālu navigācijas hierarhijā, nav pietiekama, lai preces tiktu rādītas atlasītajā kanālā, turklāt produktiem jābūt arī dažādiem kanāliem.</span><span class="sxs-lookup"><span data-stu-id="62251-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="62251-139">Papildinformāciju par preču klāstiem skatiet sadaļā [Preču klāsta pārvaldība](assortments.md).</span><span class="sxs-lookup"><span data-stu-id="62251-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="62251-140">Tālāk redzamajā attēlā parādīts mezgla piemērs ar pievienotām precēm.</span><span class="sxs-lookup"><span data-stu-id="62251-140">The following image shows an example node with products added.</span></span>

![Kategoriju mezglam pievienotās preces](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="62251-142">Preču īpašību grupu pievienošana kategoriju mezgliem</span><span class="sxs-lookup"><span data-stu-id="62251-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="62251-143">Īpašību grupas jāizveido pirms to pievienošanas mezglam kanālu navigācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="62251-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="62251-144">Lai preču īpašību grupu pievienotu kategoriju mezglam, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="62251-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="62251-145">Atlasiet kategoriju mezglu.</span><span class="sxs-lookup"><span data-stu-id="62251-145">Select a category node.</span></span>
1. <span data-ttu-id="62251-146">Sadaļā **Preču īpašību grupa** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="62251-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="62251-147">Atrodiet īpašību grupu(-as), kuru(-as) vēlaties pievienot, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="62251-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="62251-148">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="62251-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="62251-149">Tālāk redzamajā attēlā parādīts mezgla paraugs ar pievienotām preču īpašību grupām.</span><span class="sxs-lookup"><span data-stu-id="62251-149">The following image shows a sample node with product attribute groups added.</span></span>

![Preču īpašību grupas mezglā](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="62251-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="62251-151">Additional resources</span></span>

[<span data-ttu-id="62251-152">Preču klāstu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="62251-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="62251-153">Atribūtu un atribūtu grupu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="62251-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
