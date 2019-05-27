---
title: Krājumu vajadzības kārtulu definēšana
description: Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565662"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="393f4-103">Krājumu vajadzības kārtulu definēšana</span><span class="sxs-lookup"><span data-stu-id="393f4-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="393f4-104">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="393f4-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="393f4-105">Šajā procedūrā ir parādīts, kā izveidot vajadzību noteikumus un ignorēt vajadzības iestatījumus noteiktajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="393f4-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="393f4-106">Tajā ir arī parādīts, kā norādīt krājumu noklusējuma iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="393f4-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="393f4-107">Vajadzības grupas izveide</span><span class="sxs-lookup"><span data-stu-id="393f4-107">Create a coverage group</span></span>
1. <span data-ttu-id="393f4-108">Dodieties uz Vajadzības grupas.</span><span class="sxs-lookup"><span data-stu-id="393f4-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="393f4-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="393f4-109">Click New.</span></span>
3. <span data-ttu-id="393f4-110">Laukā Vajadzības grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="393f4-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="393f4-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="393f4-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="393f4-112">Laukā Kalendārs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="393f4-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="393f4-113">Izvēlieties kalendāru, ko vispārējā plānošana izmanto, lai izveidotu papildināšanas ieteikumus šajā grupā iekļautajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="393f4-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="393f4-114">Laukā Vajadz. aprēķ. metode atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="393f4-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="393f4-115">Šai procedūrai atlasiet Vajadzība.</span><span class="sxs-lookup"><span data-stu-id="393f4-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="393f4-116">Laukā Vajadzības periods (dienās) ievadiet “90”.</span><span class="sxs-lookup"><span data-stu-id="393f4-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="393f4-117">Šīs grupas krājumiem vispārējā plānošana izveidos papildināšanas ieteikumus līdz 90 dienām nākotnē.</span><span class="sxs-lookup"><span data-stu-id="393f4-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="393f4-118">Laukā Dienas(-) ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="393f4-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="393f4-119">Laukā Dienas(+) ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="393f4-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="393f4-120">Izvērsiet vai sakļaujiet sadaļu Cits.</span><span class="sxs-lookup"><span data-stu-id="393f4-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="393f4-121">Laukā Pieprasījuma datumam pieskaitītā saņemšanas rezerve ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="393f4-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="393f4-122">Piemēram, ja drošības rezerve ir iestatīta uz 1 dienu un pirkšanas pasūtījuma rinda ir ieplānota saņemšanai 15. maijā, tad vispārējā plānošana pielāgoto saņemšanas datumu aprēķina kā 16. maiju.</span><span class="sxs-lookup"><span data-stu-id="393f4-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="393f4-123">Laukā No pieprasījuma datuma atņemtā izsniegšanas rezerve ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="393f4-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="393f4-124">Piemēram, ja saņemšanas rezerve ir iestatīta uz 1 dienu un pārdošanas pasūtījuma rinda ir ieplānota piegādei 15. maijā, tad vispārējā plānošana pielāgoto piegādes datumu aprēķina kā 14. maiju.</span><span class="sxs-lookup"><span data-stu-id="393f4-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="393f4-125">Laukā Krājuma izpildlaikam pieskaitītā atkārtotas pasūtīšanas rezerve ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="393f4-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="393f4-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="393f4-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="393f4-127">Izveidot jaunu preci</span><span class="sxs-lookup"><span data-stu-id="393f4-127">Create a new product</span></span>
1. <span data-ttu-id="393f4-128">Dodieties uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="393f4-128">Go to Released products.</span></span>
2. <span data-ttu-id="393f4-129">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="393f4-129">Click New.</span></span>
3. <span data-ttu-id="393f4-130">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="393f4-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="393f4-131">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="393f4-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="393f4-132">Laukā Krājumu modeļu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="393f4-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="393f4-133">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="393f4-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="393f4-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="393f4-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="393f4-135">Laukā Krājumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="393f4-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="393f4-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="393f4-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="393f4-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="393f4-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="393f4-138">Laukā Noliktavas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="393f4-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="393f4-139">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="393f4-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="393f4-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="393f4-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="393f4-141">Laukā Izsekošanas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="393f4-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="393f4-142">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="393f4-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="393f4-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="393f4-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="393f4-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="393f4-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="393f4-145">Iestatīt noklusējuma pasūtījuma iestatījumus</span><span class="sxs-lookup"><span data-stu-id="393f4-145">Setup default order settings</span></span>
1. <span data-ttu-id="393f4-146">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="393f4-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="393f4-147">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="393f4-147">Click Default order settings.</span></span>
3. <span data-ttu-id="393f4-148">Laukā Pirkšanas vieta ierakstiet vietu, ko izmantojat kā noklusējumu, kad tiek izveidoti pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="393f4-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="393f4-149">Laukā Krājumu atrašanās vieta ierakstiet vietu, kur šis krājums tiek glabāts.</span><span class="sxs-lookup"><span data-stu-id="393f4-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="393f4-150">Izvērsiet vai sakļaujiet sadaļu Krājumi.</span><span class="sxs-lookup"><span data-stu-id="393f4-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="393f4-151">Vienumam Vairāki iestatiet vērtību “10”.</span><span class="sxs-lookup"><span data-stu-id="393f4-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="393f4-152">Vienumam Min.</span><span class="sxs-lookup"><span data-stu-id="393f4-152">Set Min.</span></span> <span data-ttu-id="393f4-153">pasūtījuma daudzums iestatiet vērtību “10”.</span><span class="sxs-lookup"><span data-stu-id="393f4-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="393f4-154">Vienumam Maks.</span><span class="sxs-lookup"><span data-stu-id="393f4-154">Set Max.</span></span> <span data-ttu-id="393f4-155">pasūtījuma daudzums iestatiet vērtību “100”.</span><span class="sxs-lookup"><span data-stu-id="393f4-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="393f4-156">Vienumam Standarta pasūtījuma daudzums iestatiet vērtību “10”.</span><span class="sxs-lookup"><span data-stu-id="393f4-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="393f4-157">Laukā Pirkšanas izpildes laiks ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="393f4-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="393f4-158">Atzīmējiet izvēles rūtiņu Darba dienas vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="393f4-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="393f4-159">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="393f4-159">Click Save.</span></span>
13. <span data-ttu-id="393f4-160">Laukā Noklusējuma pasūtījuma tips atlasiet “Pirkšanas pasūtījums”.</span><span class="sxs-lookup"><span data-stu-id="393f4-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="393f4-161">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="393f4-161">Click Save.</span></span>
15. <span data-ttu-id="393f4-162">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="393f4-162">Close the page.</span></span>
    * <span data-ttu-id="393f4-163">Aizveriet lapu Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="393f4-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="393f4-164">Pievienot krājumu kādai vajadzības grupai</span><span class="sxs-lookup"><span data-stu-id="393f4-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="393f4-165">Izvērsiet vai sakļaujiet sadaļu Plāns.</span><span class="sxs-lookup"><span data-stu-id="393f4-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="393f4-166">Laukā Vajadzības grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="393f4-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="393f4-167">Šajā sarakstā atrodiet izveidoto vajadzības grupu.</span><span class="sxs-lookup"><span data-stu-id="393f4-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="393f4-168">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="393f4-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="393f4-169">Izveidot krājumu vajadzības kārtulas</span><span class="sxs-lookup"><span data-stu-id="393f4-169">Create item coverage rules</span></span>
1. <span data-ttu-id="393f4-170">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="393f4-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="393f4-171">Noklikšķiniet uz Krājumu vajadzība.</span><span class="sxs-lookup"><span data-stu-id="393f4-171">Click Item coverage.</span></span>
3. <span data-ttu-id="393f4-172">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="393f4-172">Click New.</span></span>
4. <span data-ttu-id="393f4-173">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="393f4-173">Click the General tab.</span></span>
5. <span data-ttu-id="393f4-174">Atzīmējiet izvēles rūtiņu lauka Ignorēt seguma grupas iestatījumus virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="393f4-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="393f4-175">Laukā Vajadzības periods (dienās) ievadiet “60”.</span><span class="sxs-lookup"><span data-stu-id="393f4-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="393f4-176">Lai gan krājumi vajadzības grupā Pieprasījums tiek plānoti 90 dienas uz priekšu, šis krājums tiks plānots 60 dienas uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="393f4-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="393f4-177">Laukā Dienas(-) ievadiet “2”.</span><span class="sxs-lookup"><span data-stu-id="393f4-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="393f4-178">Laukā Dienas(+) ievadiet “2”.</span><span class="sxs-lookup"><span data-stu-id="393f4-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="393f4-179">Noklikšķiniet uz cilnes Izpildes laiks.</span><span class="sxs-lookup"><span data-stu-id="393f4-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="393f4-180">Atzīmējiet izvēles rūtiņu lauka Pirkšana virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="393f4-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="393f4-181">Laukā Pirkšanas laiks ievadiet “5”.</span><span class="sxs-lookup"><span data-stu-id="393f4-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="393f4-182">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="393f4-182">Click Save.</span></span>

