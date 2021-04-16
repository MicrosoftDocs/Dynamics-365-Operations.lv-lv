---
title: Preces šablona izveide
description: Izveidojiet preces šablonu iepriekš definētiem variantiem.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70008e903763fff35c6cff12c42396fe5fcabbee
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832086"
---
# <a name="create-a-product-master"></a><span data-ttu-id="f5951-103">Preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="f5951-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5951-104">Izveidojiet preces šablonu iepriekš definētiem variantiem.</span><span class="sxs-lookup"><span data-stu-id="f5951-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="f5951-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="f5951-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f5951-106">Šī procedūra ir paredzēta preču noformētājam.</span><span class="sxs-lookup"><span data-stu-id="f5951-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="f5951-107">Izveidot jaunu preces šablonu</span><span class="sxs-lookup"><span data-stu-id="f5951-107">Create a new product master</span></span>
1. <span data-ttu-id="f5951-108">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Preces šabloni**.</span><span class="sxs-lookup"><span data-stu-id="f5951-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="f5951-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f5951-109">Click **New**.</span></span>
3. <span data-ttu-id="f5951-110">Laukā **Preces numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f5951-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="f5951-111">Numuram jābūt unikālam.</span><span class="sxs-lookup"><span data-stu-id="f5951-111">The number must be unique.</span></span> <span data-ttu-id="f5951-112">Laukam **Preces numurs** var iestatīt numuru secību.</span><span class="sxs-lookup"><span data-stu-id="f5951-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="f5951-113">Šajā gadījumā lietotājam nav jāievada vērtība.</span><span class="sxs-lookup"><span data-stu-id="f5951-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="f5951-114">Laukā **Preces nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f5951-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="f5951-115">Ievadiet aprakstošo preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f5951-115">Enter a descriptive product name.</span></span> <span data-ttu-id="f5951-116">Pēc noklusējuma vērtība ir meklēšanas nosaukums, bet lietotājs var to mainīt.</span><span class="sxs-lookup"><span data-stu-id="f5951-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="f5951-117">Laukā **Preces dimensijas grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f5951-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f5951-118">Preces dimensiju grupa nosaka, kuru no 4 preču dimensijām var izmantot, lai izveidotu preces variantus.</span><span class="sxs-lookup"><span data-stu-id="f5951-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="f5951-119">Šajā piemērā tiek izmantota grupa ar krāsu un izmēru.</span><span class="sxs-lookup"><span data-stu-id="f5951-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="f5951-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f5951-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f5951-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f5951-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="f5951-122">Noklusējuma **Konfigurēšanas tehnoloģija** ir 'Iepriekš definēts variants'.</span><span class="sxs-lookup"><span data-stu-id="f5951-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="f5951-123">Tas tiks izmantots šajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="f5951-123">This will be used for this example.</span></span>
8. <span data-ttu-id="f5951-124">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f5951-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="f5951-125">Preču dimensiju grupu atlasīšana</span><span class="sxs-lookup"><span data-stu-id="f5951-125">Select product dimension groups</span></span>
1. <span data-ttu-id="f5951-126">Laukā **Krāsu grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f5951-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f5951-127">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f5951-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f5951-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f5951-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f5951-129">Laukā **Izmēru grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f5951-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f5951-130">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f5951-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f5951-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f5951-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="f5951-132">Pievienot dimensiju grupas</span><span class="sxs-lookup"><span data-stu-id="f5951-132">Add dimension groups</span></span>
1. <span data-ttu-id="f5951-133">**Darbību rūtī** noklikšķiniet uz **Prece**.</span><span class="sxs-lookup"><span data-stu-id="f5951-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="f5951-134">Noklikšķiniet uz **Dimensiju grupas**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="f5951-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="f5951-135">Laukā **Noliktavas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f5951-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f5951-136">Noliktavas dimensijas palīdz kontrolēt krājumu uzglabāšanu un izņemšanu no krājumiem.</span><span class="sxs-lookup"><span data-stu-id="f5951-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="f5951-137">Piemēram, noliktavas dimensija var iekļaut vietu un noliktavu.</span><span class="sxs-lookup"><span data-stu-id="f5951-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="f5951-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f5951-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f5951-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f5951-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f5951-140">Laukā **Izsekošanas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f5951-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f5951-141">Izsekošanas dimensiju grupa nosaka izsekošanas dimensijas, kuras var pievienot precei.</span><span class="sxs-lookup"><span data-stu-id="f5951-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="f5951-142">Piemēram, partijas numuru un sērijas numuru izmanto krājuma vienību izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="f5951-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="f5951-143">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f5951-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f5951-144">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f5951-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f5951-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f5951-145">Click **OK**.</span></span>
10. <span data-ttu-id="f5951-146">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f5951-146">Click **Save**.</span></span>
11. <span data-ttu-id="f5951-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f5951-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]