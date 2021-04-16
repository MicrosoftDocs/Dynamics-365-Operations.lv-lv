---
title: Veidot pārdošanas piedāvājumus masveidā
description: Šajā procedūrā ir parādīts, kā efektīvi izveidot tādus piedāvājumus, piedāvājot vairākas preces un pakalpojumus, kurus paredzēts sūtīt vairākiem debitoriem.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0422817576d9d93d0ec6bbfb5f3777013ee09ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817705"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="d37fc-103">Veidot pārdošanas piedāvājumus masveidā</span><span class="sxs-lookup"><span data-stu-id="d37fc-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d37fc-104">Šajā procedūrā ir parādīts, kā efektīvi izveidot tādus piedāvājumus, piedāvājot vairākas preces un pakalpojumus, kurus paredzēts sūtīt vairākiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="d37fc-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="d37fc-105">Šo masveida piedāvājumu izveide ir balstīta uz piedāvājumu veidnēm.</span><span class="sxs-lookup"><span data-stu-id="d37fc-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="d37fc-106">Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="d37fc-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="d37fc-107">Piedāvājuma veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="d37fc-107">Create a quotation template</span></span>
1. <span data-ttu-id="d37fc-108">Dodieties uz sadaļu Pārdošana un mārketings > Iestatījumi > Piedāvājumi > Veidņu grupas.</span><span class="sxs-lookup"><span data-stu-id="d37fc-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="d37fc-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d37fc-109">Click New.</span></span>
3. <span data-ttu-id="d37fc-110">Laukā Grupas ID ierakstiet ID pēc savas izvēles.</span><span class="sxs-lookup"><span data-stu-id="d37fc-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="d37fc-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d37fc-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d37fc-112">Click Save.</span></span>
6. <span data-ttu-id="d37fc-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-113">Close the page.</span></span>
7. <span data-ttu-id="d37fc-114">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="d37fc-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="d37fc-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d37fc-115">Click New.</span></span>
9. <span data-ttu-id="d37fc-116">Laukā Konta veids atlasiet Debitors.</span><span class="sxs-lookup"><span data-stu-id="d37fc-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="d37fc-117">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="d37fc-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d37fc-118">Click OK.</span></span>
    * <span data-ttu-id="d37fc-119">Lai piedāvājumu pārveidotu par veidni, ir jāveic iestatīšanas darbības piedāvājuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="d37fc-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="d37fc-120">Tas jādara pirms rindu pievienošanas piedāvājumā.</span><span class="sxs-lookup"><span data-stu-id="d37fc-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="d37fc-121">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="d37fc-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="d37fc-122">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-122">Click Change view.</span></span>
14. <span data-ttu-id="d37fc-123">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="d37fc-123">Click Header view.</span></span>
15. <span data-ttu-id="d37fc-124">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="d37fc-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="d37fc-125">Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="d37fc-126">Ierakstiet vērtību laukā Veidnes nosaukums.</span><span class="sxs-lookup"><span data-stu-id="d37fc-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="d37fc-127">Laukā Aktīvs atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="d37fc-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="d37fc-128">Lietojot veidni jaunam pārdošanas piedāvājumam, var izmantot tikai aktīvās veidnes.</span><span class="sxs-lookup"><span data-stu-id="d37fc-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="d37fc-129">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="d37fc-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="d37fc-130">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-130">Click Change view.</span></span>
21. <span data-ttu-id="d37fc-131">Noklikšķiniet uz Rindas skats.</span><span class="sxs-lookup"><span data-stu-id="d37fc-131">Click Line view.</span></span>
22. <span data-ttu-id="d37fc-132">Laukā Krājums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="d37fc-133">Laukā Krājums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="d37fc-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-134">Close the page.</span></span>
25. <span data-ttu-id="d37fc-135">Laukā Atlaides procents ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d37fc-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="d37fc-136">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-136">Click Add line.</span></span>
27. <span data-ttu-id="d37fc-137">Laukā Krājums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="d37fc-138">Laukā Krājums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="d37fc-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-139">Close the page.</span></span>
30. <span data-ttu-id="d37fc-140">Laukā Vienības cena ievadiet jaunu cenu vai mainiet pašreizējo vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="d37fc-141">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-141">Click Add line.</span></span>
32. <span data-ttu-id="d37fc-142">Laukā Krājums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="d37fc-143">Laukā Krājums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="d37fc-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-144">Close the page.</span></span>
35. <span data-ttu-id="d37fc-145">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d37fc-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="d37fc-146">Laukā Atlaide ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d37fc-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="d37fc-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d37fc-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="d37fc-148">Veidnes izmantošana viena piedāvājuma izveidei</span><span class="sxs-lookup"><span data-stu-id="d37fc-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="d37fc-149">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="d37fc-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="d37fc-150">Ievērojiet, ka jūsu tikko izveidotais piedāvājums ir atzīmēts kā veidne.</span><span class="sxs-lookup"><span data-stu-id="d37fc-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="d37fc-151">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d37fc-151">Click New.</span></span>
3. <span data-ttu-id="d37fc-152">Laukā Konta veids atlasiet Debitors.</span><span class="sxs-lookup"><span data-stu-id="d37fc-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="d37fc-153">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="d37fc-154">Izvērsiet sadaļu Veidne.</span><span class="sxs-lookup"><span data-stu-id="d37fc-154">Expand the Template section.</span></span>
6. <span data-ttu-id="d37fc-155">Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="d37fc-156">Laukā Veidnes nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="d37fc-157">Laukā Aprēķina metode atlasiet vienumu Pamatots uz veidnes vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d37fc-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="d37fc-158">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d37fc-158">Click OK.</span></span>
    * <span data-ttu-id="d37fc-159">Ir izveidots jaunais piedāvājums, pamatojoties uz veidnes datiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="d37fc-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="d37fc-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-160">Close the page.</span></span>
11. <span data-ttu-id="d37fc-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d37fc-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="d37fc-162">Veidnes izmantošana piedāvājumu veidošanai masveidā</span><span class="sxs-lookup"><span data-stu-id="d37fc-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="d37fc-163">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Piedāvājuma atjaunināšana > Masveida piedāvājumu izveide.</span><span class="sxs-lookup"><span data-stu-id="d37fc-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="d37fc-164">Laukā Konta veids atlasiet Debitors.</span><span class="sxs-lookup"><span data-stu-id="d37fc-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="d37fc-165">Laukā Grupas ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="d37fc-166">Laukā Veidnes nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d37fc-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="d37fc-167">Laukā Aprēķina metode atlasiet vienumu Pamatots uz veidnes vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d37fc-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="d37fc-168">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="d37fc-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="d37fc-169">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="d37fc-169">Click Filter.</span></span>
8. <span data-ttu-id="d37fc-170">Laukā Kritērijs iestatiet filtru, lai aptvertu tādu debitoru diapazonu, kurus vēlaties iekļaut šajā masveida piedāvājumu izveidē.</span><span class="sxs-lookup"><span data-stu-id="d37fc-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="d37fc-171">Izmantojiet šādu formātu: "Customer1..CustomerN".</span><span class="sxs-lookup"><span data-stu-id="d37fc-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="d37fc-172">Piemēram, varat iestatīt filtru šādi: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="d37fc-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="d37fc-173">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d37fc-173">Click OK.</span></span>
10. <span data-ttu-id="d37fc-174">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d37fc-174">Click OK.</span></span>
11. <span data-ttu-id="d37fc-175">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas piedāvājumi > Visi piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="d37fc-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="d37fc-176">Pārbaudiet, vai piedāvājumi ir izveidoti visiem debitoriem, kas norādīti masveida atjaunināšanas kārtībā, pamatojoties uz atlasīto veidni.</span><span class="sxs-lookup"><span data-stu-id="d37fc-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]