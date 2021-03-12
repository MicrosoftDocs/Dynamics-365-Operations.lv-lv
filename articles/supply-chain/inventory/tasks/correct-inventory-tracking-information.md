---
title: Krājumu izsekošanas informācijas labošana
description: Šajā procedūrā parādīts, kā izveidot un grāmatot krājumu pārsūtīšanas žurnālu, lai labotu krājumu izsekošanas informāciju.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c70dba7d21eab372cec235efa5a4be19587a409
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000138"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="197b7-103">Krājumu izsekošanas informācijas labošana</span><span class="sxs-lookup"><span data-stu-id="197b7-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="197b7-104">Šajā procedūrā parādīts, kā izveidot un grāmatot krājumu pārsūtīšanas žurnālu, lai labotu krājumu izsekošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="197b7-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="197b7-105">Šajā piemērā tiks atjaunināta informācija par krājumu, kas ir atkarīgs no partijas, mainot nepareizi reģistrēto partiju uz citu partiju.</span><span class="sxs-lookup"><span data-stu-id="197b7-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="197b7-106">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USPI vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="197b7-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="197b7-107">Ja izmantojat savus datus, jums ir jābūt krājumam, kuram ir iespējota partija, un tas nedrīkst būt atkarīgs no novietojuma.</span><span class="sxs-lookup"><span data-stu-id="197b7-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="197b7-108">Ir jābūt izveidotam arī krājumu žurnāla nosaukumam krājumu pārsūtīšanām.</span><span class="sxs-lookup"><span data-stu-id="197b7-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="197b7-109">Šos uzdevumus parasti veic noliktavas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="197b7-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="197b7-110">Krājumu pārsūtīšanas žurnāla izveide</span><span class="sxs-lookup"><span data-stu-id="197b7-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="197b7-111">Dodieties uz sadaļu Pārsūtīšana.</span><span class="sxs-lookup"><span data-stu-id="197b7-111">Go to Transfer.</span></span>
2. <span data-ttu-id="197b7-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="197b7-112">Click New.</span></span>
3. <span data-ttu-id="197b7-113">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="197b7-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="197b7-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="197b7-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="197b7-115">Žurnāla rindu izveide</span><span class="sxs-lookup"><span data-stu-id="197b7-115">Create journal lines</span></span>
1. <span data-ttu-id="197b7-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="197b7-116">Click New.</span></span>
2. <span data-ttu-id="197b7-117">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="197b7-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="197b7-118">Ja izmantojat USPI, atlasiet krājumu "M5003".</span><span class="sxs-lookup"><span data-stu-id="197b7-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="197b7-119">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="197b7-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="197b7-120">Noklikšķiniet uz cilnes Krājumu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="197b7-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="197b7-121">Laukā Partijas numurs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="197b7-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="197b7-122">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="197b7-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="197b7-123">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="197b7-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="197b7-124">Laukā Partijas numurs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="197b7-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="197b7-125">Grāmatot žurnālu</span><span class="sxs-lookup"><span data-stu-id="197b7-125">Post the journal</span></span>
1. <span data-ttu-id="197b7-126">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="197b7-126">Click Post.</span></span>
2. <span data-ttu-id="197b7-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="197b7-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="197b7-128">Izsekošanas informācijas pārbaude</span><span class="sxs-lookup"><span data-stu-id="197b7-128">Check tracing information</span></span>
1. <span data-ttu-id="197b7-129">Noklikšķiniet uz Krājumi.</span><span class="sxs-lookup"><span data-stu-id="197b7-129">Click Inventory.</span></span>
2. <span data-ttu-id="197b7-130">Noklikšķiniet uz Izsekot.</span><span class="sxs-lookup"><span data-stu-id="197b7-130">Click Trace.</span></span>
3. <span data-ttu-id="197b7-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="197b7-131">Click OK.</span></span>
    * <span data-ttu-id="197b7-132">Izmantojot šo izsekošanas informāciju var izsekot, no kuras partijas tika veikts krājuma labojums.</span><span class="sxs-lookup"><span data-stu-id="197b7-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="197b7-133">Lai skatītu šo informāciju, var izmantot arī lapu Krājumu izsekošana.</span><span class="sxs-lookup"><span data-stu-id="197b7-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="197b7-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="197b7-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="197b7-135">Krājumu darbību pārbaude</span><span class="sxs-lookup"><span data-stu-id="197b7-135">Check inventory transactions</span></span>
1. <span data-ttu-id="197b7-136">Noklikšķiniet uz Krājumi.</span><span class="sxs-lookup"><span data-stu-id="197b7-136">Click Inventory.</span></span>
2. <span data-ttu-id="197b7-137">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="197b7-137">Click Transactions.</span></span>
    * <span data-ttu-id="197b7-138">Šeit varat redzēt darbības, kas tika izveidotas, grāmatojot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="197b7-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

