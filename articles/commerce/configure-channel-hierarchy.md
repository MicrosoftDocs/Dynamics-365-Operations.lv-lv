---
title: Konfigurējiet kanālu, lai izmantotu kanāla navigācijas hierarhiju
description: Šajā tēmā aprakstīts, kā konfigurēt kanālu, lai lietotu kanālu navigācijas hierarhiju risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: 94d38c5c3a091263b310f346f839e1a67d6c0609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796128"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="7e22b-103">Konfigurējiet kanālu, lai izmantotu kanāla navigācijas hierarhiju</span><span class="sxs-lookup"><span data-stu-id="7e22b-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7e22b-104">Šajā tēmā aprakstīts, kā konfigurēt kanālu, lai lietotu kanālu navigācijas hierarhiju risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7e22b-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7e22b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="7e22b-105">Overview</span></span>

<span data-ttu-id="7e22b-106">Kanālu navigācijas hierarhijas organizē preces kategorijās tā, lai preces var pārlūkot e-Commerce vietnē vai pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="7e22b-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="7e22b-107">Mazumtirdzniecības un tiešsaistes kanāli ir jākonfigurē ar kanāla navigācijas hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="7e22b-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="7e22b-108">Kanāla konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="7e22b-108">Configure the channel</span></span>

<span data-ttu-id="7e22b-109">Lai kanālu konfigurētu kanālu navigācijas hierarhijas izmantošanai, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7e22b-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7e22b-110">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preces īpašības**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="7e22b-111">Atlasiet konfigurējamo kanālu.</span><span class="sxs-lookup"><span data-stu-id="7e22b-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="7e22b-112">Darbību rūtī atlasiet **Atribūtu metadatu iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="7e22b-113">Nolaižamajā sarakstā **Kategoriju hierarhija** atlasiet atbilstošo kanāla navigācijas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="7e22b-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="7e22b-114">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="7e22b-115">Sadaļā **Atribūtu grupa** pievienojiet visas atribūtu grupas, kas būs globālie atribūti visiem mezgliem.</span><span class="sxs-lookup"><span data-stu-id="7e22b-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="7e22b-116">Tālāk esošais attēls parāda, kā konfigurēt kanālu, lai izmantotu kanāla navigācijas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="7e22b-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Kanāla konfigurācijas piemērs](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="7e22b-118">Atribūtu metadatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7e22b-118">Set attribute metadata</span></span>

<span data-ttu-id="7e22b-119">Atribūtu metadatu iestatīšana atļaus katra mezgla atribūtu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="7e22b-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="7e22b-120">Lai iestatītu atribūtu metadatus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7e22b-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="7e22b-121">Darbību rūtī atlasiet **Atribūtu metadatu iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="7e22b-122">Katram mezglam atlasiet vērtību **Kanāla preču atribūts**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="7e22b-123">Iestatiet **Rādīt kanāla atribūtu** un **Jā**, un **Var precizēt** uz **Jā**, lai iespējotu rafinētājus šajā kanālā.</span><span class="sxs-lookup"><span data-stu-id="7e22b-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="7e22b-124">Pēc katra mezgla konfigurēšanas pēc vēlēšanās **Darbības rūtī** atlasiet pogu **Saglabāt**, lai saglabātu.</span><span class="sxs-lookup"><span data-stu-id="7e22b-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="7e22b-125">Augšējā labajā stūrī atlasiet **X**, lai izietu no šī ekrāna uz lapu **Kanāla kategorijas un preču atribūti**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="7e22b-126">Tālāk esošajā attēlā redzams kanāla preču atribūtu kopums, kas konfigurēts kanāla kategorijas mezglā.</span><span class="sxs-lookup"><span data-stu-id="7e22b-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanāla atribūti kanāla kategorijas mezglā](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="7e22b-128">Izmaiņu publicēšana</span><span class="sxs-lookup"><span data-stu-id="7e22b-128">Publish changes</span></span>

<span data-ttu-id="7e22b-129">Lai izmaiņas stātos spēkā, jums tās ir jāpublicē.</span><span class="sxs-lookup"><span data-stu-id="7e22b-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="7e22b-130">Lai publicētu izmaiņas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7e22b-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="7e22b-131">Darbības rūtī atlasiet **Publicēt kanāla atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="7e22b-132">Rūtī **Publicēt kanāla atjauninājumus** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7e22b-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="7e22b-133">Tālāk esošajā attēlā ir parādīts, kā publicēt kanālu atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="7e22b-133">The following image shows how to publish channel updates.</span></span>

![Publicēt kanāla atjauninājumus](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="7e22b-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7e22b-135">Additional resources</span></span>

[<span data-ttu-id="7e22b-136">Kanālu navigācijas hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="7e22b-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]