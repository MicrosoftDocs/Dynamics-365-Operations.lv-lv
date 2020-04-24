---
title: Vairāklīmeņu līdzekļi
description: Šajā tēmā ir paskaidrots, kā izveidot un dzēst vairāklīmeņu līdzekļus.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214893"
---
# <a name="multi-level-assets"></a><span data-ttu-id="ecfaa-103">Vairāklīmeņu līdzekļi</span><span class="sxs-lookup"><span data-stu-id="ecfaa-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ecfaa-104">Šajā tēmā ir paskaidrots, kā izveidot un dzēst vairāklīmeņu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="ecfaa-105">Varat izveidot līdzekļus un saistītos pakārtotos līdzekļus hierarhiskā koka struktūrā.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="ecfaa-106">Šādā veidā var parādīt relācijas un atkarības starp līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="ecfaa-107">Uzturēšanas darbi var būt saistīti ar visiem koka struktūras līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="ecfaa-108">Statistiku var izveidot arī individuālam līmenim vai kā visu pakārtoto līdzekļu līmeņu summu.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="ecfaa-109">Saraksta lapā **Visi līdzekļi** (**Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**) kolonnā **Līdzeklis** līdzekļi ir uzskaitīti hierarhiskā kārtībā.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="ecfaa-110">Kolonnā **Vecākelements** tiek rādīts saistītais vecākelements.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="ecfaa-111">Turklāt, ja līdzekļi un pakārtotie līdzekļi jau ir izveidoti, sadaļā **Līdzekļu koks** rūtī **Saistītā informācija** tiek parādīti līdzekļi koka struktūrā.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="ecfaa-112">Papildinformāciju par līdzekļa izveidi skatiet nodaļā [Līdzekļa izveide](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="ecfaa-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="ecfaa-113">Lai izveidotu pakārtotu līdzekli, kopsavilkuma cilnē **Vispārīgi** atlasiet primāro līdzekli laukā **Vecākelements**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="ecfaa-114">Līdzekļa vai līdzekļu struktūras kopēšana</span><span class="sxs-lookup"><span data-stu-id="ecfaa-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="ecfaa-115">Ja jūsu uzņēmumam ir vairākas līdzīgas līdzekļu struktūras, varat izmantot funkciju Kopēt Līdzekļu pārvaldībā, lai tos ātri izveidotu.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="ecfaa-116">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="ecfaa-117">Saraksta lapā **Visi līdzekļi** atlasiet līdzekli, kuru kopēt.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="ecfaa-118">Piemēram, ja vēlaties kopēt visu līdzekļu struktūru, tostarp pakārtotos līdzekļus, atlasiet primāro līdzekli.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="ecfaa-119">Atlasiet **Kopēt līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-119">Select **Copy asset**.</span></span> <span data-ttu-id="ecfaa-120">Sadaļā **Kopēt no** lauks **Līdzeklis** ir iestatīts uz saraksta lapā atlasīto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="ecfaa-121">Sadaļā **Kopēt uz** laukā **Līdzeklis** ievadiet jaunā līdzekļa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="ecfaa-122">Ja līdzeklim, kas tiek veidots, ir jābūt daļai no esošas līdzekļu struktūras, sadaļas **Primārais līdzeklis** laukā **Līdzeklis** atlasiet vecākelementa ID.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="ecfaa-123">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-123">Select **OK**.</span></span> <span data-ttu-id="ecfaa-124">Jaunā līdzekļu struktūra tiek rādīta saraksta lapā **Visi līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="ecfaa-125">Visi līdzekļu atribūti, uzturēšanas plāni un uzturēšanas cikli, kas saistīti ar nokopēto līdzekli, tiek pārsūtīti uz jauno līdzekli vai līdzekļu struktūru.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="ecfaa-126">Kopējot līdzekļu struktūru, jaunās struktūras pakārtotajiem līdzekļiem ir tāds pats nosaukums kā apakšlīdzekļiem, kurus nokopējāt.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="ecfaa-127">Pēc kopēšanas procedūras pabeigšanas varat viegli mainīt līdzekļa nosaukumu un citus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="ecfaa-128">Atlasiet līdzekli saraksta lapā **Visi līdzekļi** un pēc tam atlasiet pogu **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="ecfaa-129">Kopējot līdzekli vai līdzekļu struktūru, jauno līdzekļu dzīves cikla stāvoklis tiek atiestatīts uz stāvokli, ko jūs definējat kā līdzekļu sākotnējo dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="ecfaa-130">Funkcionālais novietojums tiek atiestatīts uz noklusējuma funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="ecfaa-131">Līdzekļa vai līdzekļu struktūras dzēšana</span><span class="sxs-lookup"><span data-stu-id="ecfaa-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="ecfaa-132">Ja līdzeklim ir saistītie pakārtotie līdzekļi, to var dzēst tikai tad, ja nav uzturēšanas pieprasījumu, darba pasūtījuma darbu, defektu reģistrāciju vai nosacījumu novērtējumu, kas reģistrēti kādam no līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="ecfaa-133">Saraksta lapā **Visi līdzekļi** atlasiet līdzekli, kuru dzēst.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="ecfaa-134">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="ecfaa-135">Ja nevarat dzēst līdzekli, izmantojot šo procedūru, vēl viens veids, kā rīkoties ar dzēšanu, ir iestatīt līdzekļa dzīves cikla stāvokli šim nolūkam.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="ecfaa-136">Piemēram, lapā **Līdzekļa dzīves cikla stāvokļi** varat iestatīt **Brāķis** vai **Dzēsts**.</span><span class="sxs-lookup"><span data-stu-id="ecfaa-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
