---
title: Fizisko krājumu pārsūtīšana noliktavā
description: Šajā procedūrā parādīts krājumu pārsūtīšanas žurnāla izveides un grāmatošanas process, lai reģistrētu krājuma kustību no viena novietojuma noliktavā uz citu novietojumu.
author: MarkusFogelberg
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a298f05185f3c81f2fde995e4d731b95a5f8d870
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832110"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="5fab1-103">Fizisko krājumu pārsūtīšana noliktavā</span><span class="sxs-lookup"><span data-stu-id="5fab1-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5fab1-104">Šajā procedūrā parādīts krājumu pārsūtīšanas žurnāla izveides un grāmatošanas process, lai reģistrētu krājuma kustību no viena novietojuma noliktavā uz citu novietojumu.</span><span class="sxs-lookup"><span data-stu-id="5fab1-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="5fab1-105">Pirms procesa sākšanas ir jābūt izveidotam krājumu žurnāla nosaukumam krājumu pārsūtīšanām.</span><span class="sxs-lookup"><span data-stu-id="5fab1-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="5fab1-106">Šo procedūru var izmēģināt demonstrācijas datu uzņēmumā USMF, izmantojot parādītās piemēra vērtības vai izmantojot savus datus, ja jums ir izveidoti produkti un novietojumi.</span><span class="sxs-lookup"><span data-stu-id="5fab1-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="5fab1-107">Šos uzdevumus parasti veic noliktavas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="5fab1-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="5fab1-108">Krājumu pārsūtīšanas žurnāla izveide</span><span class="sxs-lookup"><span data-stu-id="5fab1-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="5fab1-109">**Navigācijas rūtī** pārejiet uz **Krājuma pārvaldība > Žurnāla ieraksti > Krājumi > Pārsūtīšana**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="5fab1-110">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-110">Click **New**.</span></span>
3. <span data-ttu-id="5fab1-111">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="5fab1-112">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-112">Click **OK**.</span></span> <span data-ttu-id="5fab1-113">Pastāv opcija norādīt dimensijas No un Uz katrai žurnāla rindai.</span><span class="sxs-lookup"><span data-stu-id="5fab1-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="5fab1-114">Tās ir būtiskas šim žurnāla tipam.</span><span class="sxs-lookup"><span data-stu-id="5fab1-114">These are essential for this journal type.</span></span> <span data-ttu-id="5fab1-115">Krājumus var pārsūtīt uz novietojumiem, izmantojot dažādas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="5fab1-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="5fab1-116">Šajā piemērā krājums tiks pārsūtīts tajā pašā noliktavā no novietojuma, kas ir atkarīgs no numura zīmes, uz novietojumu, kas nav atkarīgs no numura zīmes.</span><span class="sxs-lookup"><span data-stu-id="5fab1-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="5fab1-117">Izveidot žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="5fab1-117">Create journal lines</span></span>
1. <span data-ttu-id="5fab1-118">Kopsavilkuma rūtī **Žurnāla rindas** noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="5fab1-119">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-120">Ja izmantojat USMF, varat izvēlēties "A0001".</span><span class="sxs-lookup"><span data-stu-id="5fab1-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="5fab1-121">Laukā **No atrašanās vietas** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-122">Ja izmantojat USMF, varat izvēlēties "2".</span><span class="sxs-lookup"><span data-stu-id="5fab1-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="5fab1-123">Laukā **Uz atrašanās vietu** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-124">Ja izmantojat USMF, varat izvēlēties "2".</span><span class="sxs-lookup"><span data-stu-id="5fab1-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="5fab1-125">Laukā **No noliktavas** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-126">Ja izmantojat USMF, varat izvēlēties "24".</span><span class="sxs-lookup"><span data-stu-id="5fab1-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="5fab1-127">Laukā **Uz noliktavu** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-128">Ja izmantojat USMF, varat izvēlēties "24".</span><span class="sxs-lookup"><span data-stu-id="5fab1-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="5fab1-129">Laukā **No novietojuma** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-130">Ja izmantojat USMF, varat izvēlēties "FL-001".</span><span class="sxs-lookup"><span data-stu-id="5fab1-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="5fab1-131">Laukā **Uz novietojumu** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-132">Ja izmantojat USMF, varat izvēlēties "Lielapjoma-001".</span><span class="sxs-lookup"><span data-stu-id="5fab1-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="5fab1-133">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="5fab1-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="5fab1-134">Kopsavilkuma cilnē **Rindas informācija** noklikšķiniet uz cilnes **Krājumu dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="5fab1-135">Laukos **No krājumu dimensijām** un **Numura zīme** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fab1-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="5fab1-136">Ja izmantojat USMF, varat izvēlēties "24".</span><span class="sxs-lookup"><span data-stu-id="5fab1-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="5fab1-137">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="5fab1-138">Krājumu pārsūtīšanas žurnāla grāmatošana</span><span class="sxs-lookup"><span data-stu-id="5fab1-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="5fab1-139">**Darbību rūtī** noklikšķiniet uz **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="5fab1-140">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="5fab1-141">Skatiet krājumu darbības</span><span class="sxs-lookup"><span data-stu-id="5fab1-141">View inventory transactions</span></span>
1. <span data-ttu-id="5fab1-142">Noklikšķiniet uz **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="5fab1-143">Noklikšķiniet uz **Transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="5fab1-143">Click **Transactions**.</span></span> <span data-ttu-id="5fab1-144">Šeit varat redzēt darbības, kas tika izveidotas, grāmatojot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="5fab1-144">Here you can see the transactions that were created when you posted your journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]