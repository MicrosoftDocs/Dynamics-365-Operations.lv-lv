---
title: Kravu un sūtījumu plānošana, izmantojot noslodzes plānošanas rīku
description: Šajā procedūrā tiek parādīts, kā lietot noslodzes plānošanas rīku, lai izveidotu kravu pārdošanas pasūtījumam.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564804"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="6f4fd-103">Kravu un sūtījumu plānošana, izmantojot noslodzes plānošanas rīku</span><span class="sxs-lookup"><span data-stu-id="6f4fd-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f4fd-104">Šajā procedūrā tiek parādīts, kā lietot noslodzes plānošanas rīku, lai izveidotu kravu pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="6f4fd-105">Kā priekšnosacījumu mēs vispirms izveidosim pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="6f4fd-106">Šī procedūra ir daļa no transportēšanas koordinatora ikdienas darba.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="6f4fd-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="6f4fd-108">Pārdošanas pasūtījuma izveidošana</span><span class="sxs-lookup"><span data-stu-id="6f4fd-108">Create a sales order</span></span>
1. <span data-ttu-id="6f4fd-109">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="6f4fd-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-110">Click New.</span></span>
3. <span data-ttu-id="6f4fd-111">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6f4fd-112">Konta US-004 atlase</span><span class="sxs-lookup"><span data-stu-id="6f4fd-112">Select account US-004.</span></span>
5. <span data-ttu-id="6f4fd-113">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-113">Click OK.</span></span>
6. <span data-ttu-id="6f4fd-114">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6f4fd-115">Atlasiet krājumu A0001.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-115">Select item A0001.</span></span>
    * <span data-ttu-id="6f4fd-116">A0001 ir iespējots transportēšanas pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="6f4fd-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6f4fd-118">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="6f4fd-119">Laukā Noliktava ierakstiet "24".</span><span class="sxs-lookup"><span data-stu-id="6f4fd-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="6f4fd-120">Šajā piemērā atlasiet noliktavu 24.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-120">In this example select warehouse 24.</span></span> <span data-ttu-id="6f4fd-121">Šī noliktava ir iespējota transportēšanas pārvaldībai un papildu noliktavas vadībai.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="6f4fd-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-122">Click Save.</span></span>
12. <span data-ttu-id="6f4fd-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="6f4fd-124">Jaunas noslodzes izveide</span><span class="sxs-lookup"><span data-stu-id="6f4fd-124">Create a new load</span></span>
1. <span data-ttu-id="6f4fd-125">Dodieties uz Transportēšanas pārvaldība > Plānošana > Kravu plānošanas rīks.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="6f4fd-126">Noklikšķiniet uz cilnes Pārdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="6f4fd-127">Tagad varat izveidot kravu tikko izveidotajam pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="6f4fd-128">Kravas var veidot, balstoties uz piedāvājumu un pieprasījumu no pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="6f4fd-129">Darbību rūtī noklikšķiniet uz Piedāvājums un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="6f4fd-130">Noklikšķiniet uz Jaunai noslodzei.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-130">Click To new load.</span></span>
5. <span data-ttu-id="6f4fd-131">Laukā Kravas veidnes ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6f4fd-132">Kravas veidne nosaka maksimālos mērījumus visas kravas svaram un tilpumam.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="6f4fd-133">Piemēram, kravas veidne var atspoguļot konteinera vai kravas automašīnas lielumu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="6f4fd-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6f4fd-135">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="6f4fd-136">Noslodzes novērtēšana un maršrutēšana</span><span class="sxs-lookup"><span data-stu-id="6f4fd-136">Rate and route the load</span></span>
1. <span data-ttu-id="6f4fd-137">Noklikšķiniet uz Novērtēšana un maršrutēšana.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="6f4fd-138">Noklikšķiniet uz Likmju un maršrutu rīks.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="6f4fd-139">Noklikšķiniet uz Likmes izvēle.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-139">Click Rate shop.</span></span>
4. <span data-ttu-id="6f4fd-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6f4fd-141">Noklikšķiniet uz Piešķirt.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-141">Click Assign.</span></span>
6. <span data-ttu-id="6f4fd-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-142">Close the page.</span></span>
7. <span data-ttu-id="6f4fd-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6f4fd-143">Close the page.</span></span>

