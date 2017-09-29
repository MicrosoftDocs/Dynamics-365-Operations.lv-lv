--- 
title: "Preces šablona izveide"
description: "Izveidojiet preces šablonu iepriekš definētiem variantiem."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4e8d438da1524850c115f5c38865fac2f19f3ff5
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-master"></a><span data-ttu-id="c844a-103">Preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="c844a-103">Create a product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c844a-104">Izveidojiet preces šablonu iepriekš definētiem variantiem.</span><span class="sxs-lookup"><span data-stu-id="c844a-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="c844a-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="c844a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c844a-106">Šī procedūra ir paredzēta preču noformētājam.</span><span class="sxs-lookup"><span data-stu-id="c844a-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="c844a-107">Izveidot jaunu preces šablonu</span><span class="sxs-lookup"><span data-stu-id="c844a-107">Create a new product master</span></span>
1. <span data-ttu-id="c844a-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Preces šabloni.</span><span class="sxs-lookup"><span data-stu-id="c844a-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="c844a-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c844a-109">Click New.</span></span>
3. <span data-ttu-id="c844a-110">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c844a-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c844a-111">Numuram jābūt unikālam.</span><span class="sxs-lookup"><span data-stu-id="c844a-111">The number must be unique.</span></span> <span data-ttu-id="c844a-112">Laukam Preces numurs var iestatīt numuru secību.</span><span class="sxs-lookup"><span data-stu-id="c844a-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="c844a-113">Šajā gadījumā lietotājam nav jāievada vērtība.</span><span class="sxs-lookup"><span data-stu-id="c844a-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="c844a-114">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c844a-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="c844a-115">Ievadiet aprakstošo preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c844a-115">Enter a descriptive product name.</span></span> <span data-ttu-id="c844a-116">Pēc noklusējuma vērtība ir meklēšanas nosaukums, bet lietotājs var to mainīt.</span><span class="sxs-lookup"><span data-stu-id="c844a-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="c844a-117">Laukā Preces dimensijas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c844a-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c844a-118">Preces dimensiju grupa nosaka, kuru no 4 preču dimensijām var izmantot, lai izveidotu preces variantus.</span><span class="sxs-lookup"><span data-stu-id="c844a-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="c844a-119">Šajā piemērā tiek izmantota grupa ar krāsu un izmēru.</span><span class="sxs-lookup"><span data-stu-id="c844a-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="c844a-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c844a-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c844a-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c844a-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c844a-122">Noklusējuma konfigurēšanas tehnoloģija ir Iepriekš definēts variants.</span><span class="sxs-lookup"><span data-stu-id="c844a-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="c844a-123">Tas tiks izmantots šajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="c844a-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="c844a-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c844a-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="c844a-125">Preču dimensiju grupu atlasīšana</span><span class="sxs-lookup"><span data-stu-id="c844a-125">Select product dimension groups</span></span>
1. <span data-ttu-id="c844a-126">Laukā Krāsu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c844a-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c844a-127">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c844a-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c844a-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c844a-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c844a-129">Laukā Izmēru grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c844a-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c844a-130">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c844a-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c844a-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c844a-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="c844a-132">Pievienot dimensiju grupas</span><span class="sxs-lookup"><span data-stu-id="c844a-132">Add dimension groups</span></span>
1. <span data-ttu-id="c844a-133">Darbību rūtī noklikšķiniet uz Prece.</span><span class="sxs-lookup"><span data-stu-id="c844a-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="c844a-134">Noklikšķiniet uz Dimensiju grupas, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c844a-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="c844a-135">Laukā Noliktavas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c844a-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c844a-136">Noliktavas dimensijas palīdz kontrolēt krājumu uzglabāšanu un izņemšanu no krājumiem.</span><span class="sxs-lookup"><span data-stu-id="c844a-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="c844a-137">Piemēram, noliktavas dimensija var iekļaut vietu un noliktavu.</span><span class="sxs-lookup"><span data-stu-id="c844a-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="c844a-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c844a-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c844a-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c844a-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c844a-140">Laukā Izsekošanas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c844a-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c844a-141">Izsekošanas dimensiju grupa nosaka izsekošanas dimensijas, kuras var pievienot precei.</span><span class="sxs-lookup"><span data-stu-id="c844a-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="c844a-142">Piemēram, partijas numuru un sērijas numuru izmanto krājuma vienību izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="c844a-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="c844a-143">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c844a-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c844a-144">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c844a-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c844a-145">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="c844a-145">Click OK.</span></span>
10. <span data-ttu-id="c844a-146">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c844a-146">Click Save.</span></span>
11. <span data-ttu-id="c844a-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c844a-147">Close the page.</span></span>


