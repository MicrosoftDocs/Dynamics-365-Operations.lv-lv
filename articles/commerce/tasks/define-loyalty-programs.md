---
title: " Lojalitātes programmu definēšana"
description: Šajā procedūrā parādīts, kā lojalitātes programmai iestatīt divus lojalitātes programmas līmeņus.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b178f1c6a71b34b70db4dbcd1765117215a4d2a1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023278"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="9f539-103"> Lojalitātes programmu definēšana</span><span class="sxs-lookup"><span data-stu-id="9f539-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9f539-104">Šajā procedūrā parādīts, kā lojalitātes programmai iestatīt divus lojalitātes programmas līmeņus.</span><span class="sxs-lookup"><span data-stu-id="9f539-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="9f539-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="9f539-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="9f539-106">Dodieties uz Mazumtirdzniecība un komercija > ..</span><span class="sxs-lookup"><span data-stu-id="9f539-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="9f539-107">> Lojalitātes programmas.</span><span class="sxs-lookup"><span data-stu-id="9f539-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="9f539-108">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f539-108">Click New.</span></span>
3. <span data-ttu-id="9f539-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f539-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9f539-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f539-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9f539-111">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="9f539-111">Click Add line.</span></span>
6. <span data-ttu-id="9f539-112">Laukā Līmenis ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f539-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="9f539-113">Laukā Līmenis ievadiet lojalitātes programmas līmeņa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9f539-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="9f539-114">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f539-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="9f539-115">Laukā Datumu intervāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9f539-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9f539-116">Šo datumu intervālu ir jāpagarina tā, lai tas beigtos nākotnē.</span><span class="sxs-lookup"><span data-stu-id="9f539-116">This date interval should extend into the future.</span></span> <span data-ttu-id="9f539-117">Piemēram, ja datumu intervāls, kas ir atlasīts zelta līmenim, ir viena gada periods, klients, kurš kvalificējas zelta līmenim, var saņemt zelta līmenim piešķirto atlīdzību uz vienu gadu.</span><span class="sxs-lookup"><span data-stu-id="9f539-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="9f539-118">Ja klients atkārtoti kvalificējas zelta līmenim, kamēr viņam jau ir šis līmenis, līmeņa derīguma datums tiek pagarināts par vēl vienu gadu, sākot no dienas, kad klients atkārtoti iegūst zelta līmeņa statusu.</span><span class="sxs-lookup"><span data-stu-id="9f539-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="9f539-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9f539-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9f539-120">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="9f539-120">Click Add line.</span></span>
12. <span data-ttu-id="9f539-121">Laukā Līmenis ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f539-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="9f539-122">Laukā Līmenis ievadiet lojalitātes programmas līmeņa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9f539-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="9f539-123">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f539-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="9f539-124">Laukā Datumu intervāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9f539-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="9f539-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9f539-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9f539-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f539-126">Click Save.</span></span>
18. <span data-ttu-id="9f539-127">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9f539-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9f539-128">Līmeņu kārtulās tiek definēts minimālais atlīdzības punktu skaits, kas laika gaitā jāsakrāj, lai kvalificētos līmenim.</span><span class="sxs-lookup"><span data-stu-id="9f539-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="9f539-129">Pārslēdziet sadaļas Līmeņu kārtulas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="9f539-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="9f539-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f539-130">Click New.</span></span>
    * <span data-ttu-id="9f539-131">Vienam līmenim var būt vairākas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="9f539-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="9f539-132">Piemēram, lai kvalificētos līmenim, var būt iestatīti trīs atšķirīgi kritēriji; iztērēt 500 ASV dolārus viena mēneša laikā, iztērēt 1000 ASV dolārus viena gada laikā un veikt 20 transakcijas viena gada laikā.</span><span class="sxs-lookup"><span data-stu-id="9f539-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="9f539-133">Lai to paveiktu, ir jāizveido trīs limeņa kārtulas.</span><span class="sxs-lookup"><span data-stu-id="9f539-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="9f539-134">Laukā Atlīdzības punkts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="9f539-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9f539-135">Tiem ir jābūt neizpērkamiem lojalitātes programmas atlīdzības punktiem.</span><span class="sxs-lookup"><span data-stu-id="9f539-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="9f539-136">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9f539-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="9f539-137">Laukā Minimālais izsniegto punktu skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f539-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="9f539-138">Attiecībā uz viszemāko līmeni: ja visi debitori kvalificējas, tikai piedaloties programmā, ievadiet vērtību 0.</span><span class="sxs-lookup"><span data-stu-id="9f539-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="9f539-139">Laukā Novērtēšanas datums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="9f539-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9f539-140">Šo datumu intervālu ir jāpagarina tā, lai tas beigtos pagātnē.</span><span class="sxs-lookup"><span data-stu-id="9f539-140">This date interval should extend into the past.</span></span> <span data-ttu-id="9f539-141">Lai iegūtu minimālo izsniegto punktu vērtību, skaitīti tiks tikai šajā datumu intervālā iegūtie punkti.</span><span class="sxs-lookup"><span data-stu-id="9f539-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="9f539-142">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9f539-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="9f539-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f539-143">Click Save.</span></span>
27. <span data-ttu-id="9f539-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9f539-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="9f539-145">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f539-145">Click New.</span></span>
29. <span data-ttu-id="9f539-146">Laukā Atlīdzības punkts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="9f539-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="9f539-147">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9f539-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="9f539-148">Laukā Minimālais izsniegto punktu skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f539-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="9f539-149">Laukā Novērtēšanas datums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="9f539-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9f539-150">Šo datumu intervālu ir jāpagarina tā, lai tas beigtos pagātnē.</span><span class="sxs-lookup"><span data-stu-id="9f539-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="9f539-151">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9f539-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="9f539-152">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f539-152">Click Save.</span></span>
35. <span data-ttu-id="9f539-153">Noklikšķiniet uz Cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="9f539-153">Click Price groups.</span></span>
    * <span data-ttu-id="9f539-154">Ja saviem lojalitātes programmas debitoriem vēlaties piešķirt atlaides.</span><span class="sxs-lookup"><span data-stu-id="9f539-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="9f539-155">Piešķiriet lojalitātes programmai un atlaidēm vienu vai vairākas cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="9f539-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="9f539-156">Tas ir vislabākais veids, kā nesajaukt cenu grupas dažāda veida atlaižu elementiem.</span><span class="sxs-lookup"><span data-stu-id="9f539-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="9f539-157">Piemēram, nelietojiet vienu cenu grupu lojalitātes programmas atlaidēm un kanāla atlaidēm.</span><span class="sxs-lookup"><span data-stu-id="9f539-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="9f539-158">Laukā Cenu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="9f539-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9f539-159">Lapas augšdaļā esošā cenu grupas saite ir paredzēta lojalitātes programmai.</span><span class="sxs-lookup"><span data-stu-id="9f539-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="9f539-160">Programmas līmeņu kopsavilkuma cilnēs esošās cenu grupas saites ir paredzētas tikai noteiktam lojalitātes programmas līmenim.</span><span class="sxs-lookup"><span data-stu-id="9f539-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="9f539-161">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9f539-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="9f539-162">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f539-162">Click Save.</span></span>
39. <span data-ttu-id="9f539-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9f539-163">Close the page.</span></span>
40. <span data-ttu-id="9f539-164">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f539-164">Click Save.</span></span>

