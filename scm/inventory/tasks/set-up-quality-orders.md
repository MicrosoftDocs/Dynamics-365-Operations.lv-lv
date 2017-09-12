---
title: "Kvalitātes pasūtījumu iestatīšana"
description: "Šajā procedūrā parādīts, kā iespējot kvalitātes pārvaldības procesu, kurā ienākošie krājumi ir jāpārbauda uzreiz pēc saņemšanas reģistrācijas."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: lv-lv
ms.lasthandoff: 09/12/2017

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="b2be6-103">Kvalitātes pasūtījumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b2be6-103">Set up quality orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2be6-104">Šajā procedūrā parādīts, kā iespējot kvalitātes pārvaldības procesu, kurā ienākošie krājumi ir jāpārbauda uzreiz pēc saņemšanas reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="b2be6-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="b2be6-105">Procedūru parasti veic kvalitātes pārvaldītājs.</span><span class="sxs-lookup"><span data-stu-id="b2be6-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="b2be6-106">Process ietver kvalitātes grupas izveidi, lai definētu krājumus, kuriem būs jāveic paraugu ņemšana, un testa grupas izveidi, lai grupētu testus, kas jāveic kvalitātes grupas krājumiem.</span><span class="sxs-lookup"><span data-stu-id="b2be6-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="b2be6-107">Šo ceļvedi varat palaist demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="b2be6-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="b2be6-108">Iespējot kvalitātes pārvaldību</span><span class="sxs-lookup"><span data-stu-id="b2be6-108">Enable quality management</span></span>
1. <span data-ttu-id="b2be6-109">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Krājumu un noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="b2be6-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="b2be6-110">Noklikšķiniet uz cilnes Kvalitātes pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="b2be6-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="b2be6-111">Opcijai Izmantot kvalitātes pārvaldību iestatiet Jā.</span><span class="sxs-lookup"><span data-stu-id="b2be6-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="b2be6-112">Noklikšķiniet uz Pārskatu iestatījums.</span><span class="sxs-lookup"><span data-stu-id="b2be6-112">Click Report setup.</span></span>
    * <span data-ttu-id="b2be6-113">Uzņēmumā USMF kvalitātes pārvaldības pārskata iestatījumi jau ir definēti.</span><span class="sxs-lookup"><span data-stu-id="b2be6-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="b2be6-114">Ja tas nebija izdarīts, varat šeit pievienot jaunas rindas dažādiem pārskatu tipiem, un atlasīt dokumentu tipu, kuru vēlaties lietot katram pārskatam.</span><span class="sxs-lookup"><span data-stu-id="b2be6-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="b2be6-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-115">Close the page.</span></span>
6. <span data-ttu-id="b2be6-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="b2be6-117">Testa izveide</span><span class="sxs-lookup"><span data-stu-id="b2be6-117">Create a test</span></span>
1. <span data-ttu-id="b2be6-118">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Testi.</span><span class="sxs-lookup"><span data-stu-id="b2be6-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="b2be6-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-119">Click New.</span></span>
3. <span data-ttu-id="b2be6-120">Ierakstiet vērtību laukā Tests.</span><span class="sxs-lookup"><span data-stu-id="b2be6-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="b2be6-121">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2be6-122">Laukā Tips atlasiet Opcija.</span><span class="sxs-lookup"><span data-stu-id="b2be6-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="b2be6-123">Šajā piemērā atlasīsim „Opcija”, kas ļaus piešķirt testa rezultātus, ņemot vērā iepriekš definētās vērtības.</span><span class="sxs-lookup"><span data-stu-id="b2be6-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="b2be6-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-124">Click Save.</span></span>
7. <span data-ttu-id="b2be6-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="b2be6-126">Testa mainīgo lielumu izveide, lai noteiktu to, kā tiek ierakstīti testa rezultāti</span><span class="sxs-lookup"><span data-stu-id="b2be6-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="b2be6-127">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Testa mainīgie lielumi.</span><span class="sxs-lookup"><span data-stu-id="b2be6-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="b2be6-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-128">Click New.</span></span>
3. <span data-ttu-id="b2be6-129">Ierakstiet vērtību laukā Mainīgais.</span><span class="sxs-lookup"><span data-stu-id="b2be6-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="b2be6-130">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2be6-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-131">Click Save.</span></span>
6. <span data-ttu-id="b2be6-132">Noklikšķiniet uz Rezultāti.</span><span class="sxs-lookup"><span data-stu-id="b2be6-132">Click Outcomes.</span></span>
7. <span data-ttu-id="b2be6-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-133">Click New.</span></span>
8. <span data-ttu-id="b2be6-134">Ierakstiet vērtību laukā Rezultāts.</span><span class="sxs-lookup"><span data-stu-id="b2be6-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="b2be6-135">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="b2be6-136">Laukā Rezultāta statuss atlasiet Veiksmīgs.</span><span class="sxs-lookup"><span data-stu-id="b2be6-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="b2be6-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-137">Click Save.</span></span>
12. <span data-ttu-id="b2be6-138">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-138">Click New.</span></span>
13. <span data-ttu-id="b2be6-139">Ierakstiet vērtību laukā Rezultāts.</span><span class="sxs-lookup"><span data-stu-id="b2be6-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="b2be6-140">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="b2be6-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-141">Click Save.</span></span>
16. <span data-ttu-id="b2be6-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-142">Close the page.</span></span>
17. <span data-ttu-id="b2be6-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="b2be6-144">Krājuma paraugu izveides iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b2be6-144">Set up item sampling</span></span>
1. <span data-ttu-id="b2be6-145">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Krājumu paraugu ņemšana.</span><span class="sxs-lookup"><span data-stu-id="b2be6-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="b2be6-146">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-146">Click New.</span></span>
3. <span data-ttu-id="b2be6-147">Ierakstiet vērtību laukā Krājumu paraugu ņemšana.</span><span class="sxs-lookup"><span data-stu-id="b2be6-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="b2be6-148">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2be6-149">Ievadiet skaitli laukā Vērtība.</span><span class="sxs-lookup"><span data-stu-id="b2be6-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="b2be6-150">Šī vērtība attiecas uz daudzuma specifikāciju, kas atlasīta blakus esošajā laukā.</span><span class="sxs-lookup"><span data-stu-id="b2be6-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="b2be6-151">Izvērsiet vai sakļaujiet sadaļu Process.</span><span class="sxs-lookup"><span data-stu-id="b2be6-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="b2be6-152">Atzīmējiet izvēles rūtiņu Pilna bloķēšana vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="b2be6-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="b2be6-153">Ja atlasāt šo opciju, neveiksmīga testa gadījumā tiek bloķēta visa partija vai pasūtījuma rindas daudzums.</span><span class="sxs-lookup"><span data-stu-id="b2be6-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="b2be6-154">Ja tā netiek atlasīta, tiek bloķēti tikai krājumi kvalitātes pārbaudes pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="b2be6-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="b2be6-155">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-155">Click Save.</span></span>
9. <span data-ttu-id="b2be6-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="b2be6-157">Kvalitātes grupas izveide</span><span class="sxs-lookup"><span data-stu-id="b2be6-157">Create a quality group</span></span>
1. <span data-ttu-id="b2be6-158">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Kvalitātes grupas.</span><span class="sxs-lookup"><span data-stu-id="b2be6-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="b2be6-159">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-159">Click New.</span></span>
3. <span data-ttu-id="b2be6-160">Ierakstiet vērtību laukā Kvalitātes grupa.</span><span class="sxs-lookup"><span data-stu-id="b2be6-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="b2be6-161">Ierakstiet aprakstošu nosaukumu, kas palīdzētu noteikt, kāda veida krājumus grupa ietvers (paraugu atlases kritēriji).</span><span class="sxs-lookup"><span data-stu-id="b2be6-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="b2be6-162">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2be6-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-163">Click Save.</span></span>
6. <span data-ttu-id="b2be6-164">noklikšķiniet uz Pievienot preces.</span><span class="sxs-lookup"><span data-stu-id="b2be6-164">Click Add items.</span></span>
7. <span data-ttu-id="b2be6-165">Izvēlieties krājuma koda rindu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-165">Select the Item number row</span></span>
    * <span data-ttu-id="b2be6-166">Šajā piemērā filtrēšana tiks veikta pēc krājuma koda.</span><span class="sxs-lookup"><span data-stu-id="b2be6-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="b2be6-167">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b2be6-168">Piemēram, ierakstiet T*, lai atfiltrētu krājumu numurus, kas sākas ar burtu T.</span><span class="sxs-lookup"><span data-stu-id="b2be6-168">For example, type T* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="b2be6-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b2be6-169">Click OK.</span></span>
10. <span data-ttu-id="b2be6-170">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b2be6-170">Click OK.</span></span>
11. <span data-ttu-id="b2be6-171">Noklikšķiniet uz Krājumu kvalitātes grupas.</span><span class="sxs-lookup"><span data-stu-id="b2be6-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="b2be6-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-172">Close the page.</span></span>
13. <span data-ttu-id="b2be6-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="b2be6-174">Testa grupas izveide</span><span class="sxs-lookup"><span data-stu-id="b2be6-174">Create a test group</span></span>
1. <span data-ttu-id="b2be6-175">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Testa grupas.</span><span class="sxs-lookup"><span data-stu-id="b2be6-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="b2be6-176">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-176">Click New.</span></span>
3. <span data-ttu-id="b2be6-177">Ierakstiet vērtību laukā Testa grupa.</span><span class="sxs-lookup"><span data-stu-id="b2be6-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="b2be6-178">Piešķiriet testa grupai nosaukumu, kas palīdzēs atcerēties, kāda veida testi tiek izmantoti un ar kuru kvalitātes grupu tai jābūt saistītai.</span><span class="sxs-lookup"><span data-stu-id="b2be6-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="b2be6-179">Piemēram, ja tā ir jāizmanto ar kvalitātes grupu, kas atlasa krājumus, kuru identifikatori sākas ar "T", tās nosaukums varētu būt "T krājumu testi".</span><span class="sxs-lookup"><span data-stu-id="b2be6-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="b2be6-180">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2be6-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2be6-181">Laukā Krājumu paraugu ņemšana atlasiet krājumu paraugu ņemšanas rindu, kuru izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="b2be6-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="b2be6-182">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b2be6-183">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b2be6-183">Click Add.</span></span>
8. <span data-ttu-id="b2be6-184">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="b2be6-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="b2be6-185">Laukā Tests atlasiet iepriekš izveidoto testu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="b2be6-186">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="b2be6-187">Noklikšķiniet uz cilnes Tests.</span><span class="sxs-lookup"><span data-stu-id="b2be6-187">Click the Test tab.</span></span>
12. <span data-ttu-id="b2be6-188">Laukā Mainīgais atlasiet iepriekš izveidoto mainīgo.</span><span class="sxs-lookup"><span data-stu-id="b2be6-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="b2be6-189">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b2be6-190">Laukā Rezultāts pēc noklusējuma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b2be6-191">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b2be6-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b2be6-192">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-192">Click Save.</span></span>
17. <span data-ttu-id="b2be6-193">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="b2be6-194">Kvalitātes pārbaudes pasūtījumu izveides definēšana</span><span class="sxs-lookup"><span data-stu-id="b2be6-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="b2be6-195">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes kontrole > Kvalitātes piesaistes.</span><span class="sxs-lookup"><span data-stu-id="b2be6-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="b2be6-196">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2be6-196">Click New.</span></span>
3. <span data-ttu-id="b2be6-197">Atlasiet opciju laukā Atsauces tips.</span><span class="sxs-lookup"><span data-stu-id="b2be6-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="b2be6-198">Laukā Krājuma kods atlasiet Grupa.</span><span class="sxs-lookup"><span data-stu-id="b2be6-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="b2be6-199">Šajā piemērā tiks atlasīta "Grupa" un izmantota iepriekš izveidotā kvalitātes grupa.</span><span class="sxs-lookup"><span data-stu-id="b2be6-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="b2be6-200">Var arī iestatīt "Tabula", lai norādītu krājumus manuāli, vai izvēlieties "Visi", lai kvalitātes pārbaudes pasūtījumam pievienotu visus krājumus.</span><span class="sxs-lookup"><span data-stu-id="b2be6-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="b2be6-201">Laukā Krājums izvēlieties iepriekš izveidoto kvalitātes grupu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="b2be6-202">Laukā Krājums pieejamās opcijas ir atkarīgas no tā, ko iestatāt laukā Krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="b2be6-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="b2be6-203">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b2be6-204">Izvērsiet vai sakļaujiet sadaļu Process.</span><span class="sxs-lookup"><span data-stu-id="b2be6-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="b2be6-205">Atlasiet opciju laukā Notikuma tips.</span><span class="sxs-lookup"><span data-stu-id="b2be6-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="b2be6-206">Tas ir notikums, kas aktivizē testu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-206">This is the event that triggers the test.</span></span> <span data-ttu-id="b2be6-207">Šeit pieejamās opcijas ir atkarīgas no tā, kuri procesi atlasīti laukā Atsauces tips.</span><span class="sxs-lookup"><span data-stu-id="b2be6-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="b2be6-208">Atlasiet opciju laukā Izpilde.</span><span class="sxs-lookup"><span data-stu-id="b2be6-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="b2be6-209">Izvērsiet vai sakļaujiet sadaļu Kvalitātes pārbaudes pasūtījuma process.</span><span class="sxs-lookup"><span data-stu-id="b2be6-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="b2be6-210">Laukā Notikumu aizturēšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b2be6-211">Šajā laukā parādīts procesu saraksts, kurus ir iespējams bloķēt, ja kvalitātes pasūtījums ir joprojām atvērts.</span><span class="sxs-lookup"><span data-stu-id="b2be6-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="b2be6-212">Opcijas ir atkarīgas no tā, ko atlasījāt laukā Notikuma tips.</span><span class="sxs-lookup"><span data-stu-id="b2be6-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="b2be6-213">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b2be6-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2be6-214">Tas būs atkarīgs no iepriekš atlasītajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="b2be6-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="b2be6-215">Atlasiet, ja šie procesi ir jābloķē laikā, kad pastāv atvērti kvalitātes pārbaudes pasūtījumi, kas saistīti ar pamatdokumenta rindu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="b2be6-216">Izvērsiet vai sakļaujiet sadaļu Specifikācijas.</span><span class="sxs-lookup"><span data-stu-id="b2be6-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="b2be6-217">Laukā Testa grupa atlasiet iepriekš izveidoto grupu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="b2be6-218">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="b2be6-219">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b2be6-219">Click Save.</span></span>
17. <span data-ttu-id="b2be6-220">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2be6-220">Close the page.</span></span>

