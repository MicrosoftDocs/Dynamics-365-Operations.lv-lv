---
title: Krājumu vajadzības kārtulu definēšana
description: Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ecd56c84b232fd7855bf2fb01eaebe3f3bd4440
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150290"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="31587-103">Krājumu vajadzības kārtulu definēšana</span><span class="sxs-lookup"><span data-stu-id="31587-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31587-104">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="31587-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="31587-105">Šajā procedūrā ir parādīts, kā izveidot vajadzību noteikumus un ignorēt vajadzības iestatījumus noteiktajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="31587-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="31587-106">Tajā ir arī parādīts, kā norādīt krājumu noklusējuma iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="31587-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="31587-107">Vajadzības grupas izveide</span><span class="sxs-lookup"><span data-stu-id="31587-107">Create a coverage group</span></span>
1. <span data-ttu-id="31587-108">Dodieties uz **Navigācijas rūts > Moduļi > Vispārējā plānošana > Iestatīšana > Vajadzības grupas**.</span><span class="sxs-lookup"><span data-stu-id="31587-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="31587-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="31587-109">Click **New**.</span></span>
3. <span data-ttu-id="31587-110">Laukā **Vajadzības grupa** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="31587-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="31587-111">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="31587-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="31587-112">Laukā **Kalendārs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="31587-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="31587-113">Izvēlieties kalendāru, ko vispārējā plānošana izmanto, lai izveidotu papildināšanas ieteikumus šajā grupā iekļautajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="31587-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="31587-114">Laukā **Vajadz. aprēķ. metode** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="31587-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="31587-115">Šai procedūrai atlasiet 'Vajadzība'.</span><span class="sxs-lookup"><span data-stu-id="31587-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="31587-116">Laukā **Vajadzības periods (dienās)** ievadiet '90'.</span><span class="sxs-lookup"><span data-stu-id="31587-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="31587-117">Šīs grupas krājumiem vispārējā plānošana izveidos papildināšanas ieteikumus līdz 90 dienām nākotnē.</span><span class="sxs-lookup"><span data-stu-id="31587-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="31587-118">Laukā **Dienas(-)** ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="31587-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="31587-119">Laukā **Dienas(+)** ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="31587-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="31587-120">Izvērsiet vai sakļaujiet sadaļu **Cits**.</span><span class="sxs-lookup"><span data-stu-id="31587-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="31587-121">Sadaļā **Drošības rezerves dienās** laukā **Pieprasījuma datumam pieskaitītā saņemšanas rezerve** ievadiet '1'.</span><span class="sxs-lookup"><span data-stu-id="31587-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="31587-122">Piemēram, ja drošības rezerve ir iestatīta uz 1 dienu un pirkšanas pasūtījuma rinda ir ieplānota saņemšanai 15. maijā, tad vispārējā plānošana pielāgoto saņemšanas datumu aprēķina kā 16. maiju.</span><span class="sxs-lookup"><span data-stu-id="31587-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="31587-123">Laukā **No pieprasījuma datuma atņemtā izsniegšanas rezerve** ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="31587-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="31587-124">Piemēram, ja saņemšanas rezerve ir iestatīta uz 1 dienu un pārdošanas pasūtījuma rinda ir ieplānota piegādei 15. maijā, tad vispārējā plānošana pielāgoto piegādes datumu aprēķina kā 14. maiju.</span><span class="sxs-lookup"><span data-stu-id="31587-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="31587-125">Laukā **Krājuma izpildlaikam pieskaitītā atkārtotas pasūtīšanas rezerve** ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="31587-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="31587-126">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="31587-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="31587-127">Jaunas preces izveide</span><span class="sxs-lookup"><span data-stu-id="31587-127">Create a new product</span></span>
1. <span data-ttu-id="31587-128">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="31587-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="31587-129">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="31587-129">Click **New**.</span></span>
3. <span data-ttu-id="31587-130">Laukā **Preces numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="31587-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="31587-131">Laukā **Preces nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="31587-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="31587-132">In the **Krājumu modeļu grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="31587-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="31587-133">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="31587-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="31587-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="31587-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="31587-135">Laukā **Krājumu grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="31587-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="31587-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="31587-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="31587-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="31587-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="31587-138">Laukā **Noliktavas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="31587-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="31587-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="31587-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="31587-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="31587-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="31587-141">Laukā **Izsekošanas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="31587-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="31587-142">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="31587-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="31587-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="31587-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="31587-144">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="31587-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="31587-145">Iestatīt noklusējuma pasūtījuma iestatījumus</span><span class="sxs-lookup"><span data-stu-id="31587-145">Setup default order settings</span></span>
1. <span data-ttu-id="31587-146">**Darbību rūtī** noklikšķiniet uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="31587-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="31587-147">Sadaļā **Pasūtījuma iestatījumi** noklikšķiniet uz lauka **Noklusējuma pasūtījuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="31587-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="31587-148">Sadaļā **Pirkšanas pasūtījums** laukā **Noklusējuma vieta** ierakstiet vietu, ko izmantojat kā noklusējumu, kad tiek izveidoti pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="31587-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="31587-149">Laukā **Noklusējuma noliktava** ierakstiet vietu, kur šis krājums tiek glabāts.</span><span class="sxs-lookup"><span data-stu-id="31587-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="31587-150">Izvērsiet vai sakļaujiet sadaļu **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="31587-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="31587-151">Laukā **Dalītājs** ierakstiet '10'.</span><span class="sxs-lookup"><span data-stu-id="31587-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="31587-152">Laukā **Minimālais pasūtījuma daudzums** ierakstiet '10'.</span><span class="sxs-lookup"><span data-stu-id="31587-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="31587-153">Laukā **Maksimālais pasūtījuma daudzums** ierakstiet '100'.</span><span class="sxs-lookup"><span data-stu-id="31587-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="31587-154">Laukā **Standarta pasūtījuma daudzums** ierakstiet '10'.</span><span class="sxs-lookup"><span data-stu-id="31587-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="31587-155">Laukā **Pirkšanas izpildes laiks** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="31587-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="31587-156">Atzīmējiet izvēles rūtiņu **Darba dienas** vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="31587-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="31587-157">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="31587-157">Click **Save**.</span></span>
13. <span data-ttu-id="31587-158">Laukā **Noklusējuma pasūtījuma veids** atlasiet “Pirkšanas pasūtījums”.</span><span class="sxs-lookup"><span data-stu-id="31587-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="31587-159">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="31587-159">Click **Save**.</span></span>
15. <span data-ttu-id="31587-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="31587-160">Close the page.</span></span> <span data-ttu-id="31587-161">Aizveriet lapu Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="31587-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="31587-162">Pievienot krājumu kādai vajadzības grupai</span><span class="sxs-lookup"><span data-stu-id="31587-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="31587-163">Izvērsiet vai sakļaujiet sadaļu **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="31587-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="31587-164">Laukā **Vajadzības grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="31587-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="31587-165">Šajā sarakstā atrodiet izveidoto **Vajadzības grupu**.</span><span class="sxs-lookup"><span data-stu-id="31587-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="31587-166">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="31587-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="31587-167">Izveidot krājumu vajadzības kārtulas</span><span class="sxs-lookup"><span data-stu-id="31587-167">Create item coverage rules</span></span>
1. <span data-ttu-id="31587-168">**Darbību rūtī** noklikšķiniet uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="31587-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="31587-169">Sadaļā **Vajadzība** noklikšķiniet uz **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="31587-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="31587-170">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="31587-170">Click **New**.</span></span>
4. <span data-ttu-id="31587-171">Noklikšķiniet uz cilnes **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="31587-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="31587-172">Atzīmējiet izvēles rūtiņu iestatījumu **Ignorēt vajadzības grupu** virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="31587-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="31587-173">Laukā **Vajadzības periods (dienās)** ievadiet '60'.</span><span class="sxs-lookup"><span data-stu-id="31587-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="31587-174">Lai gan krājumi vajadzības grupā Pieprasījums tiek plānoti 90 dienas uz priekšu, šis krājums tiks plānots 60 dienas uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="31587-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="31587-175">Laukā **Dienas(-)** ievadiet “2”.</span><span class="sxs-lookup"><span data-stu-id="31587-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="31587-176">Laukā **Dienas(+)** ievadiet “2”.</span><span class="sxs-lookup"><span data-stu-id="31587-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="31587-177">Noklikšķiniet uz cilnes **Izpildes laiks**.</span><span class="sxs-lookup"><span data-stu-id="31587-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="31587-178">Atzīmējiet izvēles rūtiņu **Pirkšana** virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="31587-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="31587-179">Laukā **Pirkšanas laiks** ievadiet “5”.</span><span class="sxs-lookup"><span data-stu-id="31587-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="31587-180">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="31587-180">Click **Save**.</span></span>

