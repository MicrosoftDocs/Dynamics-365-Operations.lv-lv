---
title: Kravu un sūtījumu plānošana, izmantojot kravu plānošanas rīku
description: Šajā tēmā ir parādīts, kā lietot noslodzes plānošanas rīku, lai izveidotu kravu pārdošanas pasūtījumam.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4fdff8bdc383a85d604fa6e545c625d5782241f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976817"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="fa672-103">Kravu un sūtījumu plānošana, izmantojot kravu plānošanas rīku</span><span class="sxs-lookup"><span data-stu-id="fa672-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa672-104">Šajā tēmā ir parādīts, kā lietot noslodzes plānošanas rīku, lai izveidotu kravu pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="fa672-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="fa672-105">Kā priekšnosacījumu mēs vispirms izveidosim pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="fa672-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="fa672-106">Šī procedūra ir daļa no transportēšanas koordinatora ikdienas darba.</span><span class="sxs-lookup"><span data-stu-id="fa672-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="fa672-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="fa672-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="fa672-108">Izveidot pārdošanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="fa672-108">Create a sales order</span></span>
1. <span data-ttu-id="fa672-109">Dodieties uz **Navigācijas rūts > Moduļi > Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="fa672-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="fa672-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fa672-110">Select **New**.</span></span>
3. <span data-ttu-id="fa672-111">Laukā **Debitora konts** atlasiet nolaižamā saraksta pogu, lai atvērtu pārlūku.</span><span class="sxs-lookup"><span data-stu-id="fa672-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fa672-112">Atlasiet kontu **US-004**.</span><span class="sxs-lookup"><span data-stu-id="fa672-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="fa672-113">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fa672-113">Select **OK**.</span></span>
6. <span data-ttu-id="fa672-114">Laukā **Krājuma kods** atlasiet nolaižamā saraksta pogu, lai atvērtu pārlūku.</span><span class="sxs-lookup"><span data-stu-id="fa672-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fa672-115">Atlasiet preci **A0001**.</span><span class="sxs-lookup"><span data-stu-id="fa672-115">Select item **A0001**.</span></span> <span data-ttu-id="fa672-116">**A0001** ir iespējots transportēšanas pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="fa672-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="fa672-117">Laukā **Vieta** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu, pēc tam atlasiet preci.</span><span class="sxs-lookup"><span data-stu-id="fa672-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="fa672-118">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="fa672-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="fa672-119">Laukā **Noliktava** šim piemēram ierakstiet vērtību '24'.</span><span class="sxs-lookup"><span data-stu-id="fa672-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="fa672-120">Šī noliktava ir iespējota transportēšanas pārvaldībai un papildu noliktavas vadībai.</span><span class="sxs-lookup"><span data-stu-id="fa672-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="fa672-121">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fa672-121">Select **Save**.</span></span>
12. <span data-ttu-id="fa672-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fa672-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="fa672-123">Jaunas noslodzes izveide</span><span class="sxs-lookup"><span data-stu-id="fa672-123">Create a new load</span></span>
1. <span data-ttu-id="fa672-124">Dodieties uz **Navigācijas rūts > Moduļi > Transportēšanas pārvaldība > Plānošana > Noslodzes plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="fa672-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="fa672-125">Atlasiet cilni **Pārdošanas rindas**. Tagad varat izveidot kravu tikko izveidotajam pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="fa672-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="fa672-126">Kravas var veidot, balstoties uz piedāvājumu un pieprasījumu no pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="fa672-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="fa672-127">Darbību rūtī atlasiet **Piedāvājums un pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="fa672-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="fa672-128">Atlasiet **Uz jaunu noslodzi**.</span><span class="sxs-lookup"><span data-stu-id="fa672-128">Select **To new load**.</span></span>
5. <span data-ttu-id="fa672-129">Laukā **Kravas veidnes ID** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="fa672-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="fa672-130">Kravas veidne nosaka maksimālos mērījumus visas kravas svaram un tilpumam.</span><span class="sxs-lookup"><span data-stu-id="fa672-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="fa672-131">Piemēram, kravas veidne var atspoguļot konteinera vai kravas automašīnas lielumu.</span><span class="sxs-lookup"><span data-stu-id="fa672-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="fa672-132">Atlasiet krājumu.</span><span class="sxs-lookup"><span data-stu-id="fa672-132">Select an item.</span></span>
6. <span data-ttu-id="fa672-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fa672-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="fa672-134">Noslodzes novērtēšana un maršrutēšana</span><span class="sxs-lookup"><span data-stu-id="fa672-134">Rate and route the load</span></span>
1. <span data-ttu-id="fa672-135">Atlasiet **Novērtēšana un maršrutēšana**.</span><span class="sxs-lookup"><span data-stu-id="fa672-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="fa672-136">Atlasiet **Likmju un maršrutu rīks**.</span><span class="sxs-lookup"><span data-stu-id="fa672-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="fa672-137">Atlasiet **Likmes veikals**.</span><span class="sxs-lookup"><span data-stu-id="fa672-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="fa672-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="fa672-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fa672-139">Atlasiet **Piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="fa672-139">Select **Assign**.</span></span>
6. <span data-ttu-id="fa672-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fa672-140">Close the page.</span></span>

