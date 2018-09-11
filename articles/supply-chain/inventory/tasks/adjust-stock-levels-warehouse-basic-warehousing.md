--- 
title: "Krājumu līmeņu korekcija noliktavā (pamata noliktava)"
description: "Šajā procedūrā parādīts krājumu korekcijas žurnāla izveides un grāmatošanas process, lai koriģētu noteiktu preču krājumu līmeņus noliktavā."
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 75ff53872fd81d5b25964c1ba65127f9feaf2b45
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="0df61-103">Krājumu līmeņu korekcija noliktavā (pamata noliktava)</span><span class="sxs-lookup"><span data-stu-id="0df61-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0df61-104">Šajā procedūrā parādīts krājumu korekcijas žurnāla izveides un grāmatošanas process, lai koriģētu noteiktu preču krājumu līmeņus noliktavā.</span><span class="sxs-lookup"><span data-stu-id="0df61-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="0df61-105">Pirms procesa sākšanas ir jābūt izveidotam krājumu žurnāla nosaukumam krājumu korekcijām.</span><span class="sxs-lookup"><span data-stu-id="0df61-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="0df61-106">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="0df61-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="0df61-107">Šos uzdevumus parasti veic noliktavas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="0df61-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="0df61-108">Krājumu korekcijas žurnāla izveide</span><span class="sxs-lookup"><span data-stu-id="0df61-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="0df61-109">Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumi > Krājumu korekcija.</span><span class="sxs-lookup"><span data-stu-id="0df61-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="0df61-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0df61-110">Click New.</span></span>
3. <span data-ttu-id="0df61-111">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0df61-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0df61-112">Sarakstā noklikšķiniet uz krājumu korekcijas žurnāla nosaukuma, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="0df61-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="0df61-113">Daži citi lauki tiks aizpildīti, pamatojoties uz atlasītajiem krājumu korekcijas žurnāla nosaukuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="0df61-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="0df61-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0df61-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="0df61-115">Žurnāla rindu izveide</span><span class="sxs-lookup"><span data-stu-id="0df61-115">Create journal lines</span></span>
1. <span data-ttu-id="0df61-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0df61-116">Click New.</span></span>
2. <span data-ttu-id="0df61-117">Sarakstā atzīmējiet krājuma koda lauku.</span><span class="sxs-lookup"><span data-stu-id="0df61-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="0df61-118">Laukā Krājuma kods atlasiet krājumu.</span><span class="sxs-lookup"><span data-stu-id="0df61-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="0df61-119">Ja izmantojat demonstrācijas datu uzņēmumu USMF atlasiet "D0001".</span><span class="sxs-lookup"><span data-stu-id="0df61-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="0df61-120">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0df61-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0df61-121">Sarakstā atlasiet vietu.</span><span class="sxs-lookup"><span data-stu-id="0df61-121">In the list, select a site.</span></span>
6. <span data-ttu-id="0df61-122">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0df61-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0df61-123">Sarakstā atlasiet noliktavu.</span><span class="sxs-lookup"><span data-stu-id="0df61-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="0df61-124">Ja esat atlasījis krājumu ar Novietojumu kā obligāto dimensiju, jums būs jānorāda novietojums šeit.</span><span class="sxs-lookup"><span data-stu-id="0df61-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="0df61-125">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="0df61-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0df61-126">Izmaksu cenas laukā norādītas krājumu saņemšanas izmaksas uz vienību.</span><span class="sxs-lookup"><span data-stu-id="0df61-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="0df61-127">Ja krājuma kodam izmaksa nav norādīta vai vēlaties to mainīt manuāli, tad tas ir jādara šeit.</span><span class="sxs-lookup"><span data-stu-id="0df61-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="0df61-128">Krājumu korekcijas žurnāla apstiprināšana un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="0df61-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="0df61-129">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="0df61-129">Click Validate.</span></span>
2. <span data-ttu-id="0df61-130">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0df61-130">Click OK.</span></span>
3. <span data-ttu-id="0df61-131">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="0df61-131">Click Post.</span></span>
    * <span data-ttu-id="0df61-132">Grāmatojot šāda veida žurnālus, krājumu ieejas plūsma vai izejas plūsma tiek iegrāmatota, krājuma līmenis un vērtība tiek mainīta un Virsgrāmatas darbības tiek ģenerētas.</span><span class="sxs-lookup"><span data-stu-id="0df61-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="0df61-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0df61-133">Click OK.</span></span>
5. <span data-ttu-id="0df61-134">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="0df61-134">Close the form.</span></span>
6. <span data-ttu-id="0df61-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0df61-135">Close the page.</span></span>


