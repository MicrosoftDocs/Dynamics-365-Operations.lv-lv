---
title: "Krājumu skaitīšana noliktavā"
description: "Šajā procedūrā parādīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5099e82aa3f0408cbfbf816a69c38c5d48989dd2
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="43d20-103">Krājumu skaitīšana noliktavā</span><span class="sxs-lookup"><span data-stu-id="43d20-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43d20-104">Šajā procedūrā parādīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="43d20-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="43d20-105">Procedūra attiecas uz "pamata noliktavas" funkcionalitāti, kas pieejama krājumu vadības modulī, nevis uz noliktavas funkcionalitāti, kas ir pieejama noliktavas vadības modulī.</span><span class="sxs-lookup"><span data-stu-id="43d20-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="43d20-106">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="43d20-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="43d20-107">Ja izmantojat savus datus, pārliecinieties, ka ir izveidoti produkti un novietojumi un ka esat izveidojis krājumu žurnāla nosaukumu inventarizācijas žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="43d20-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="43d20-108">Krājumu inventarizāciju parasti veic noliktavas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="43d20-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="43d20-109">Izveidojiet krājumu inventarizācijas žurnālu</span><span class="sxs-lookup"><span data-stu-id="43d20-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="43d20-110">Pārejiet uz sadaļu Krājumu pārvaldība > Žurnāla ieraksti > Krājumu inventarizācija > Inventarizācija.</span><span class="sxs-lookup"><span data-stu-id="43d20-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="43d20-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="43d20-111">Click New.</span></span>
3. <span data-ttu-id="43d20-112">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43d20-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="43d20-113">Sarakstā noklikšķiniet uz krājumu inventarizācijas žurnāla nosaukuma, kuru vēlaties izmantot</span><span class="sxs-lookup"><span data-stu-id="43d20-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="43d20-114">Daži citi lauki tiks aizpildīti, pamatojoties uz atlasītajiem krājumu inventarizācijas žurnāla nosaukuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="43d20-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="43d20-115">Laukā Darbinieks noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43d20-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="43d20-116">Sarakstā atlasiet darbinieku, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="43d20-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="43d20-117">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="43d20-117">Click Select.</span></span>
8. <span data-ttu-id="43d20-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="43d20-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="43d20-119">Žurnāla rindu izveide</span><span class="sxs-lookup"><span data-stu-id="43d20-119">Create journal lines</span></span>
1. <span data-ttu-id="43d20-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="43d20-120">Click New.</span></span>
2. <span data-ttu-id="43d20-121">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43d20-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="43d20-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="43d20-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43d20-123">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet "A0001".</span><span class="sxs-lookup"><span data-stu-id="43d20-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="43d20-124">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43d20-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="43d20-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="43d20-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43d20-126">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet atrašanās vietu "2".</span><span class="sxs-lookup"><span data-stu-id="43d20-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="43d20-127">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43d20-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="43d20-128">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="43d20-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43d20-129">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet noliktavu "24".</span><span class="sxs-lookup"><span data-stu-id="43d20-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="43d20-130">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43d20-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="43d20-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="43d20-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43d20-132">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet novietojumu "Lielapjoma-001".</span><span class="sxs-lookup"><span data-stu-id="43d20-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="43d20-133">Laukā Saskaitīts ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="43d20-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="43d20-134">Ja ievadāt saskaitīto skaitu, kas atšķiras no laukā Rīcībā esošs parādītā skaita, lauks Daudzums tiek atjaunināts, lai parādītu neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="43d20-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="43d20-135">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="43d20-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="43d20-136">Krājumu inventarizācijas žurnāla grāmatošana</span><span class="sxs-lookup"><span data-stu-id="43d20-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="43d20-137">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="43d20-137">Click Post.</span></span>
    * <span data-ttu-id="43d20-138">Grāmatojot krājumu inventarizācijas žurnālu, ja saskaitītais skaits atšķiras no skaita, kas norādīts laukā Rīcībā esošs, tiek grāmatota krājumu ieejas plūsma vai izejas plūsma, tiek mainīts krājumu līmenis un vērtība un tiek ģenerētas virsgrāmatas darbības.</span><span class="sxs-lookup"><span data-stu-id="43d20-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="43d20-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="43d20-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="43d20-140">Skatiet krājumu darbības</span><span class="sxs-lookup"><span data-stu-id="43d20-140">View inventory transactions</span></span>
1. <span data-ttu-id="43d20-141">Noklikšķiniet uz Krājumi.</span><span class="sxs-lookup"><span data-stu-id="43d20-141">Click Inventory.</span></span>
2. <span data-ttu-id="43d20-142">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="43d20-142">Click Transactions.</span></span>
    * <span data-ttu-id="43d20-143">Šeit varat redzēt saistītās darbības, kas tiks izveidotas, grāmatojot krājumu inventarizācijas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="43d20-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

