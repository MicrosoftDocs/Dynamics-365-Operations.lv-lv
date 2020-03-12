---
title: Izveidot jaunu preču hierarhiju
description: Šajā tēmā aprakstīts, kā izveidot jaunu preču hierarhiju programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070425"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="f3a1d-103">Izveidot jaunu preču hierarhiju</span><span class="sxs-lookup"><span data-stu-id="f3a1d-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f3a1d-104">Šajā tēmā aprakstīts, kā izveidot jaunu preču hierarhiju programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f3a1d-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="f3a1d-105">Overview</span></span>

<span data-ttu-id="f3a1d-106">Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="f3a1d-107">Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali).</span><span class="sxs-lookup"><span data-stu-id="f3a1d-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="f3a1d-108">Katram mazumtirdzniecības veikala kanālam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="f3a1d-109">Pirms varat izveidot mazumtirdzniecības veikala kanālu, jums tam ir jāiestata visi šie elementi.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="f3a1d-110">Tirdzniecības preču hierarhiju izmanto, lai definētu vispārējo savas organizācijas preču hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="f3a1d-111">Varat izmantot šo tirdzniecības preču hierarhiju preču virzīšanai tirgū, cenu noteikšanai un reklamēšanas pasākumiem, kā arī ziņojumu izveides un preču klāsta plānošanai.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="f3a1d-112">Katrai organizācijai var piešķirt tikai vienu tirdzniecības preču hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="f3a1d-113">Preču hierarhijas izveide un konfigurācija</span><span class="sxs-lookup"><span data-stu-id="f3a1d-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="f3a1d-114">Lai izveidotu un konfigurētu tidzniecības preču hierarhiju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f3a1d-115">Navgācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Tirdzniecības preču kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="f3a1d-116">Ja vēl nav izveidota neviena hierarhija, **Darbību rūtī** atlasiet **Jauna**, lai izveidotu hierarhijas sakni.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="f3a1d-117">Zem cilnes **Vispārīgi**:</span><span class="sxs-lookup"><span data-stu-id="f3a1d-117">Under **General**:</span></span>
    1. <span data-ttu-id="f3a1d-118">Lodziņā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="f3a1d-119">Lodziņā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="f3a1d-120">Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="f3a1d-121">Iestatiet **Aktīvs** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="f3a1d-122">Hierarhijas mezglu pievienošana</span><span class="sxs-lookup"><span data-stu-id="f3a1d-122">Add hierarchy nodes</span></span>

<span data-ttu-id="f3a1d-123">Lai pievienotu hierarhijas mezglus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="f3a1d-124">Darbību rūtī atlasiet **Rediģēt kategoriju hierarhiju**.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="f3a1d-125">Atlasiet pamatmezglu, kuram vēlaties pievienot jaunu mezglu, un pēc tam atlasiet **Jauns kategorijas mezgls**.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="f3a1d-126">Sadaļā **Vispārīgi** norādiet **Nosaukums**, **Apraksts**, **Draudzīgais nosaukums** un **Atslēgvārdi**.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="f3a1d-127">Zem cilnes **Vispārīgi**:</span><span class="sxs-lookup"><span data-stu-id="f3a1d-127">Under **General**:</span></span>
    1. <span data-ttu-id="f3a1d-128">Lodziņā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="f3a1d-129">Lodziņā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="f3a1d-130">Lodziņā **Draudzīgais nosaukums** ievadiet draudzīgo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="f3a1d-131">Lodziņā **Atslēgvārdi** ievadiet atbilstošos atslēgvārdus.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="f3a1d-132">Lodziņā **Rādīšanas secība** ievadiet rādīšanas secības skaitli (nav obligāti).</span><span class="sxs-lookup"><span data-stu-id="f3a1d-132">In the **Display order**box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="f3a1d-133">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="f3a1d-134">Atkārtojiet iepriekš minētās darbības, lai pievienotu papildu mezglus.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="f3a1d-135">Tālāk redzamajā attēlā parādīta jauna preču hierarhijas mezgla izveide.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Preču hierarhijas izveide](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="f3a1d-137">Citi iestatījumi</span><span class="sxs-lookup"><span data-stu-id="f3a1d-137">Other settings</span></span>

<span data-ttu-id="f3a1d-138">Kategoriju atribūtu grupas var piešķirt arī katrai grupai pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="f3a1d-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="f3a1d-139">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f3a1d-139">Additional resources</span></span>

[<span data-ttu-id="f3a1d-140">komercijas hierarhijas</span><span class="sxs-lookup"><span data-stu-id="f3a1d-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="f3a1d-141">Preču kategoriju un preču pārvaldība</span><span class="sxs-lookup"><span data-stu-id="f3a1d-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="f3a1d-142">Kārtošanas secības mainīšana virzīšanas tirgū elementiem</span><span class="sxs-lookup"><span data-stu-id="f3a1d-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
