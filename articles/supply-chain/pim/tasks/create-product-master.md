---
title: Preces šablona izveide
description: Izveidojiet preces šablonu iepriekš definētiem variantiem.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdb30b46a0e5a6d4fac997588dd47148f2664c03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432776"
---
# <a name="create-a-product-master"></a><span data-ttu-id="c0973-103">Preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="c0973-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0973-104">Izveidojiet preces šablonu iepriekš definētiem variantiem.</span><span class="sxs-lookup"><span data-stu-id="c0973-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="c0973-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="c0973-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c0973-106">Šī procedūra ir paredzēta preču noformētājam.</span><span class="sxs-lookup"><span data-stu-id="c0973-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="c0973-107">Izveidot jaunu preces šablonu</span><span class="sxs-lookup"><span data-stu-id="c0973-107">Create a new product master</span></span>
1. <span data-ttu-id="c0973-108">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Preces šabloni**.</span><span class="sxs-lookup"><span data-stu-id="c0973-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="c0973-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c0973-109">Click **New**.</span></span>
3. <span data-ttu-id="c0973-110">Laukā **Preces numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c0973-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="c0973-111">Numuram jābūt unikālam.</span><span class="sxs-lookup"><span data-stu-id="c0973-111">The number must be unique.</span></span> <span data-ttu-id="c0973-112">Laukam **Preces numurs** var iestatīt numuru secību.</span><span class="sxs-lookup"><span data-stu-id="c0973-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="c0973-113">Šajā gadījumā lietotājam nav jāievada vērtība.</span><span class="sxs-lookup"><span data-stu-id="c0973-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="c0973-114">Laukā **Preces nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c0973-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="c0973-115">Ievadiet aprakstošo preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c0973-115">Enter a descriptive product name.</span></span> <span data-ttu-id="c0973-116">Pēc noklusējuma vērtība ir meklēšanas nosaukums, bet lietotājs var to mainīt.</span><span class="sxs-lookup"><span data-stu-id="c0973-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="c0973-117">Laukā **Preces dimensijas grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c0973-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="c0973-118">Preces dimensiju grupa nosaka, kuru no 4 preču dimensijām var izmantot, lai izveidotu preces variantus.</span><span class="sxs-lookup"><span data-stu-id="c0973-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="c0973-119">Šajā piemērā tiek izmantota grupa ar krāsu un izmēru.</span><span class="sxs-lookup"><span data-stu-id="c0973-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="c0973-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c0973-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c0973-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c0973-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="c0973-122">Noklusējuma **Konfigurēšanas tehnoloģija** ir 'Iepriekš definēts variants'.</span><span class="sxs-lookup"><span data-stu-id="c0973-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="c0973-123">Tas tiks izmantots šajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="c0973-123">This will be used for this example.</span></span>
8. <span data-ttu-id="c0973-124">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c0973-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="c0973-125">Preču dimensiju grupu atlasīšana</span><span class="sxs-lookup"><span data-stu-id="c0973-125">Select product dimension groups</span></span>
1. <span data-ttu-id="c0973-126">Laukā **Krāsu grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c0973-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c0973-127">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c0973-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c0973-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c0973-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c0973-129">Laukā **Izmēru grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c0973-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c0973-130">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c0973-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c0973-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c0973-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="c0973-132">Pievienot dimensiju grupas</span><span class="sxs-lookup"><span data-stu-id="c0973-132">Add dimension groups</span></span>
1. <span data-ttu-id="c0973-133">**Darbību rūtī** noklikšķiniet uz **Prece**.</span><span class="sxs-lookup"><span data-stu-id="c0973-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="c0973-134">Noklikšķiniet uz **Dimensiju grupas**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c0973-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="c0973-135">Laukā **Noliktavas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c0973-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="c0973-136">Noliktavas dimensijas palīdz kontrolēt krājumu uzglabāšanu un izņemšanu no krājumiem.</span><span class="sxs-lookup"><span data-stu-id="c0973-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="c0973-137">Piemēram, noliktavas dimensija var iekļaut vietu un noliktavu.</span><span class="sxs-lookup"><span data-stu-id="c0973-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="c0973-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c0973-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c0973-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c0973-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c0973-140">Laukā **Izsekošanas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c0973-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="c0973-141">Izsekošanas dimensiju grupa nosaka izsekošanas dimensijas, kuras var pievienot precei.</span><span class="sxs-lookup"><span data-stu-id="c0973-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="c0973-142">Piemēram, partijas numuru un sērijas numuru izmanto krājuma vienību izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="c0973-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="c0973-143">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c0973-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c0973-144">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c0973-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c0973-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c0973-145">Click **OK**.</span></span>
10. <span data-ttu-id="c0973-146">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c0973-146">Click **Save**.</span></span>
11. <span data-ttu-id="c0973-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c0973-147">Close the page.</span></span>

