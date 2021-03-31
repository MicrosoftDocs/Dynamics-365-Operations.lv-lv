---
title: Izmaksu kontroles darbvietas parametru konfigurēšana
description: Izmantojiet šo procedūru, lai konfigurētu izmaksu kontroles darbvietu, lai dažādu līmeņu vadītāji organizācijā var gūt ieskatu par to izmaksu objektiem, piemēram, izmaksu centriem un preču grupām.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61f25b93440495b2d1b70227ecda011c43c2e564
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208779"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="cf40f-103">Izmaksu kontroles darbvietas parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cf40f-103">Configure cost control workspace parameters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf40f-104">Izmantojiet šo procedūru, lai konfigurētu izmaksu kontroles darbvietu, lai dažādu līmeņu vadītāji organizācijā var gūt ieskatu par to izmaksu objektiem, piemēram, izmaksu centriem un preču grupām.</span><span class="sxs-lookup"><span data-stu-id="cf40f-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="cf40f-105">USP2 demonstrācijas uzņēmums tika izmantots, lai izveidotu šo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cf40f-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="cf40f-106">Dodieties uz Izmaksu uzskaite > Iestatījumi > Izmaksu kontroles darbvietas konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="cf40f-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="cf40f-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf40f-107">Click New.</span></span>
3. <span data-ttu-id="cf40f-108">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cf40f-109">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cf40f-110">Laukā Publicēts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cf40f-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="cf40f-111">Iestatot šo opciju uz Jā, lietotāji, kuriem ir piešķirta viena no tālāk minētajām lomām, var redzēt pārskatu izmaksu kontroles darbvietā: izmaksu uzskaites vadītājs, izmaksu grāmatvedis, izmaksu grāmatvedības darbinieks vai izmaksu objekta kontrolieris.</span><span class="sxs-lookup"><span data-stu-id="cf40f-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="cf40f-112">Iestatot šo opciju uz Nē, tikai lietotāji, kuriem ir piešķirta viena no tālāk minētajām lomām, var redzēt pārskatu izmaksu kontroles darbvietā: izmaksu uzskaites vadītājs, izmaksu grāmatvedis vai izmaksu grāmatvedības darbinieks.</span><span class="sxs-lookup"><span data-stu-id="cf40f-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="cf40f-113">Izvērsiet sadaļu Datu filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="cf40f-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="cf40f-114">Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="cf40f-115">Laukā Budžeta sākotnējā versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="cf40f-116">Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="cf40f-117">Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="cf40f-118">Izvērsiet sadaļu Piešķirt aprēķina ierakstus.</span><span class="sxs-lookup"><span data-stu-id="cf40f-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="cf40f-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf40f-119">Click New.</span></span>
13. <span data-ttu-id="cf40f-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="cf40f-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="cf40f-121">Laukā Finanšu kalendāra periods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="cf40f-122">Laukā Faktiskā versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="cf40f-123">Izvērsiet sadaļu Finanšu periodi pēc kolonnas.</span><span class="sxs-lookup"><span data-stu-id="cf40f-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="cf40f-124">Laukā Pašreizējais periods atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cf40f-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="cf40f-125">Izvērsiet sadaļu Kolonnas, ko rādīt izmaksām.</span><span class="sxs-lookup"><span data-stu-id="cf40f-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="cf40f-126">Laukā Fiksētās izmaksas atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cf40f-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="cf40f-127">Laukā Mainīgās izmaksas atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cf40f-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="cf40f-128">Laukā Kopējās izmaksas atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="cf40f-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="cf40f-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cf40f-129">Click Save.</span></span>
23. <span data-ttu-id="cf40f-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cf40f-130">Close the page.</span></span>
24. <span data-ttu-id="cf40f-131">Dodieties uz Izmaksu uzskaite > Darbvietas > Izmaksu kontrole.</span><span class="sxs-lookup"><span data-stu-id="cf40f-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="cf40f-132">Atlasiet pārskatu, lai skatītu fiksētās, mainīgās, kopējās un neklasificētās izmaksas atlasītajiem finanšu periodiem.</span><span class="sxs-lookup"><span data-stu-id="cf40f-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="cf40f-133">Laukā Finanšu kalendāra periods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="cf40f-134">Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cf40f-135">Pēc tam, kad esat atlasījis izmaksu objekta dimensiju hierarhiju, izvērsiet izmaksu elementa dimensiju hierarhiju, lai skatītu vēlamās izmaksu vērtības.</span><span class="sxs-lookup"><span data-stu-id="cf40f-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="cf40f-136">Piemēram, varat izvērst hierarhiju līdz ražošanai pieskaitāmajām izmaksām, lai redzētu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf40f-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]