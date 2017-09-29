--- 
title: "Veidot pārdošanas piedāvājumus masveidā"
description: "Šajā procedūrā ir parādīts, kā efektīvi izveidot tādus piedāvājumus, piedāvājot vairākas preces un pakalpojumus, kurus paredzēts sūtīt vairākiem debitoriem."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1fcb2c4d47f0c8e701be025e0554ed476693d732
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="2930f-103">Veidot pārdošanas piedāvājumus masveidā</span><span class="sxs-lookup"><span data-stu-id="2930f-103">Mass create sales quotations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2930f-104">Šajā procedūrā ir parādīts, kā efektīvi izveidot tādus piedāvājumus, piedāvājot vairākas preces un pakalpojumus, kurus paredzēts sūtīt vairākiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="2930f-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="2930f-105">Šo masveida piedāvājumu izveide ir balstīta uz piedāvājumu veidnēm.</span><span class="sxs-lookup"><span data-stu-id="2930f-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="2930f-106">Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="2930f-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="2930f-107">Piedāvājuma veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="2930f-107">Create a quotation template</span></span>
1. <span data-ttu-id="2930f-108">Dodieties uz sadaļu Pārdošana un mārketings > Iestatījumi > Piedāvājumi > Veidņu grupas.</span><span class="sxs-lookup"><span data-stu-id="2930f-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="2930f-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2930f-109">Click New.</span></span>
3. <span data-ttu-id="2930f-110">Laukā Grupas ID ierakstiet ID pēc savas izvēles.</span><span class="sxs-lookup"><span data-stu-id="2930f-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="2930f-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2930f-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2930f-112">Click Save.</span></span>
6. <span data-ttu-id="2930f-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2930f-113">Close the page.</span></span>
7. <span data-ttu-id="2930f-114">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="2930f-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="2930f-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2930f-115">Click New.</span></span>
9. <span data-ttu-id="2930f-116">Laukā Konta veids atlasiet Debitors.</span><span class="sxs-lookup"><span data-stu-id="2930f-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="2930f-117">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="2930f-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2930f-118">Click OK.</span></span>
    * <span data-ttu-id="2930f-119">Lai piedāvājumu pārveidotu par veidni, ir jāveic iestatīšanas darbības piedāvājuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="2930f-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="2930f-120">Tas jādara pirms rindu pievienošanas piedāvājumā.</span><span class="sxs-lookup"><span data-stu-id="2930f-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="2930f-121">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="2930f-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="2930f-122">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="2930f-122">Click Change view.</span></span>
14. <span data-ttu-id="2930f-123">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="2930f-123">Click Header view.</span></span>
15. <span data-ttu-id="2930f-124">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="2930f-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="2930f-125">Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="2930f-126">Ierakstiet vērtību laukā Veidnes nosaukums.</span><span class="sxs-lookup"><span data-stu-id="2930f-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="2930f-127">Laukā Aktīvs atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="2930f-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="2930f-128">Lietojot veidni jaunam pārdošanas piedāvājumam, var izmantot tikai aktīvās veidnes.</span><span class="sxs-lookup"><span data-stu-id="2930f-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="2930f-129">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="2930f-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="2930f-130">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="2930f-130">Click Change view.</span></span>
21. <span data-ttu-id="2930f-131">Noklikšķiniet uz Rindas skats.</span><span class="sxs-lookup"><span data-stu-id="2930f-131">Click Line view.</span></span>
22. <span data-ttu-id="2930f-132">Laukā Krājums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="2930f-133">Laukā Krājums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="2930f-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2930f-134">Close the page.</span></span>
25. <span data-ttu-id="2930f-135">Laukā Atlaides procents ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2930f-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="2930f-136">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="2930f-136">Click Add line.</span></span>
27. <span data-ttu-id="2930f-137">Laukā Krājums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="2930f-138">Laukā Krājums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="2930f-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2930f-139">Close the page.</span></span>
30. <span data-ttu-id="2930f-140">Laukā Vienības cena ievadiet jaunu cenu vai mainiet pašreizējo vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="2930f-141">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="2930f-141">Click Add line.</span></span>
32. <span data-ttu-id="2930f-142">Laukā Krājums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="2930f-143">Laukā Krājums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="2930f-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2930f-144">Close the page.</span></span>
35. <span data-ttu-id="2930f-145">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2930f-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="2930f-146">Laukā Atlaide ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2930f-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="2930f-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2930f-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="2930f-148">Veidnes izmantošana viena piedāvājuma izveidei</span><span class="sxs-lookup"><span data-stu-id="2930f-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="2930f-149">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="2930f-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="2930f-150">Ievērojiet, ka jūsu tikko izveidotais piedāvājums ir atzīmēts kā veidne.</span><span class="sxs-lookup"><span data-stu-id="2930f-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="2930f-151">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2930f-151">Click New.</span></span>
3. <span data-ttu-id="2930f-152">Laukā Konta veids atlasiet Debitors.</span><span class="sxs-lookup"><span data-stu-id="2930f-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="2930f-153">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="2930f-154">Izvērsiet sadaļu Veidne.</span><span class="sxs-lookup"><span data-stu-id="2930f-154">Expand the Template section.</span></span>
6. <span data-ttu-id="2930f-155">Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="2930f-156">Laukā Veidnes nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="2930f-157">Laukā Aprēķina metode atlasiet vienumu Pamatots uz veidnes vērtībām.</span><span class="sxs-lookup"><span data-stu-id="2930f-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="2930f-158">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2930f-158">Click OK.</span></span>
    * <span data-ttu-id="2930f-159">Ir izveidots jaunais piedāvājums, pamatojoties uz veidnes datiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="2930f-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="2930f-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2930f-160">Close the page.</span></span>
11. <span data-ttu-id="2930f-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2930f-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="2930f-162">Veidnes izmantošana piedāvājumu veidošanai masveidā</span><span class="sxs-lookup"><span data-stu-id="2930f-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="2930f-163">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Piedāvājuma atjaunināšana > Masveida piedāvājumu izveide.</span><span class="sxs-lookup"><span data-stu-id="2930f-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="2930f-164">Laukā Konta veids atlasiet Debitors.</span><span class="sxs-lookup"><span data-stu-id="2930f-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="2930f-165">Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="2930f-166">Laukā Veidnes nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2930f-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="2930f-167">Laukā Aprēķina metode atlasiet vienumu Pamatots uz veidnes vērtībām.</span><span class="sxs-lookup"><span data-stu-id="2930f-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="2930f-168">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="2930f-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="2930f-169">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="2930f-169">Click Filter.</span></span>
8. <span data-ttu-id="2930f-170">Laukā Kritērijs iestatiet filtru, lai aptvertu tādu debitoru diapazonu, kurus vēlaties iekļaut šajā masveida piedāvājumu izveidē.</span><span class="sxs-lookup"><span data-stu-id="2930f-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="2930f-171">Izmantojiet šādu formātu: "Customer1..CustomerN".</span><span class="sxs-lookup"><span data-stu-id="2930f-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="2930f-172">Piemēram, varat iestatīt filtru šādi: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="2930f-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="2930f-173">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2930f-173">Click OK.</span></span>
10. <span data-ttu-id="2930f-174">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2930f-174">Click OK.</span></span>
11. <span data-ttu-id="2930f-175">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="2930f-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="2930f-176">Pārbaudiet, vai piedāvājumi ir izveidoti visiem debitoriem, kas norādīti masveida atjaunināšanas kārtībā, pamatojoties uz atlasīto veidni.</span><span class="sxs-lookup"><span data-stu-id="2930f-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


