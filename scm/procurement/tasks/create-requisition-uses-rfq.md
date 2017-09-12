--- 
title: "Pieprasījuma izveide, kas lieto PP"
description: "Šajā ceļvedī ir parādīts, kā pirkšanas pieprasījumam pievienot cenas un kreditora informāciju no IP procesa."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="808e2-103">Pieprasījuma izveide, kas lieto PP</span><span class="sxs-lookup"><span data-stu-id="808e2-103">Create a requisition that uses an RFQ</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="808e2-104">Šajā ceļvedī ir parādīts, kā pirkšanas pieprasījumam pievienot cenas un kreditora informāciju no IP procesa.</span><span class="sxs-lookup"><span data-stu-id="808e2-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="808e2-105">Šajā ceļvedī parādīto piemēru var izmantot ar uzņēmuma USMF demonstrācijas datiem, un jums ir jāpiesakās kā administratoram, lai izpildītu visas darbības.</span><span class="sxs-lookup"><span data-stu-id="808e2-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="808e2-106">Šajā ceļvedī aprakstītos uzdevumus parasti veiktu sagādes speciālisti.</span><span class="sxs-lookup"><span data-stu-id="808e2-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="808e2-107">Izveidot pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="808e2-107">Create a requisition</span></span>
1. <span data-ttu-id="808e2-108">Pārejiet uz sadaļu Sagāde un avoti > Pirkuma pieprasījumi > Mani sagatavotie pirkšanas pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="808e2-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="808e2-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="808e2-109">Click New.</span></span>
3. <span data-ttu-id="808e2-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="808e2-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="808e2-111">Laukā Pieprasītais datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="808e2-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="808e2-112">Laukā Uzskaites datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="808e2-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="808e2-113">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="808e2-113">Click OK.</span></span>
7. <span data-ttu-id="808e2-114">Laukā Pamatojums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="808e2-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="808e2-115">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="808e2-115">Click Add line.</span></span>
9. <span data-ttu-id="808e2-116">Lauka Sagādes kategorija koka struktūrā atlasiet kādu kategoriju un noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="808e2-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="808e2-117">Laukā Preces nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="808e2-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="808e2-118">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="808e2-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="808e2-119">Laukā Vienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="808e2-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="808e2-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="808e2-120">Click Save.</span></span>
14. <span data-ttu-id="808e2-121">Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="808e2-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="808e2-122">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="808e2-122">Click Submit.</span></span>
16. <span data-ttu-id="808e2-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-123">Close the page.</span></span>
17. <span data-ttu-id="808e2-124">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="808e2-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="808e2-125">Darbplūsmas uzdevuma piešķires maiņa</span><span class="sxs-lookup"><span data-stu-id="808e2-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="808e2-126">Nākamais uzdevums ir izveidot IP, lai no kreditoriem saņemtu piedāvājumus par preci.</span><span class="sxs-lookup"><span data-stu-id="808e2-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="808e2-127">USMF demonstrācijas datos pieprasījuma darbplūsma ir iestatīta ar kārtulu, tāpēc, ja nav atlasīts kreditors vai ja vienības cena kādai rindai ir 0, konkrētam nodarbinātajam tiek piešķirts uzdevums izveidot IP.</span><span class="sxs-lookup"><span data-stu-id="808e2-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="808e2-128">Lai turpinātu ar šo ceļvedi, šis uzdevums ir jāpiešķir citam lietotājam (sev).</span><span class="sxs-lookup"><span data-stu-id="808e2-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="808e2-129">To varat izdarīt tikai tad, ja esat pieteicies kā Administrators.</span><span class="sxs-lookup"><span data-stu-id="808e2-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="808e2-130">Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="808e2-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="808e2-131">Noklikšķiniet uz Skatīt vēsturi.</span><span class="sxs-lookup"><span data-stu-id="808e2-131">Click View history.</span></span>
3. <span data-ttu-id="808e2-132">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-132">Refresh the page.</span></span>
4. <span data-ttu-id="808e2-133">Izvērsiet sadaļu Izsekošanas detaļas.</span><span class="sxs-lookup"><span data-stu-id="808e2-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="808e2-134">Koka struktūrā atlasiet vienumu “rinda, kas sākas ar “Rindas darbplūsma aktivizēta””.</span><span class="sxs-lookup"><span data-stu-id="808e2-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="808e2-135">Noklikšķiniet uz Skatīt darbplūsmas detaļas.</span><span class="sxs-lookup"><span data-stu-id="808e2-135">Click View workflow details.</span></span>
7. <span data-ttu-id="808e2-136">Izvērsiet sadaļu Darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="808e2-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="808e2-137">Noklikšķiniet uz Mainīt piešķiri.</span><span class="sxs-lookup"><span data-stu-id="808e2-137">Click Reassign.</span></span>
9. <span data-ttu-id="808e2-138">Laukā Lietotājs atlasiet vienumu Administrators.</span><span class="sxs-lookup"><span data-stu-id="808e2-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="808e2-139">Noklikšķiniet uz Mainīt piešķiri.</span><span class="sxs-lookup"><span data-stu-id="808e2-139">Click Reassign.</span></span>
11. <span data-ttu-id="808e2-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-140">Close the page.</span></span>
12. <span data-ttu-id="808e2-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="808e2-142">Izveidot PP</span><span class="sxs-lookup"><span data-stu-id="808e2-142">Create an RFQ</span></span>
1. <span data-ttu-id="808e2-143">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-143">Refresh the page.</span></span>
2. <span data-ttu-id="808e2-144">Noklikšķiniet uz Piedāvājuma pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="808e2-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="808e2-145">Laukā Pērkošā juridiskā persona atlasiet USMF.</span><span class="sxs-lookup"><span data-stu-id="808e2-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="808e2-146">Jums ir jāatlasa tā pati juridiskā persona, kas ir norādīta pieprasījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="808e2-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="808e2-147">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="808e2-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="808e2-148">Ja jūsu pirkšanas pieprasījumā bija vairākas rindas, atlasiet visas tās rindas, kuras vēlaties pievienot šim IP.</span><span class="sxs-lookup"><span data-stu-id="808e2-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="808e2-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="808e2-149">Click OK.</span></span>
6. <span data-ttu-id="808e2-150">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-150">Refresh the page.</span></span>
7. <span data-ttu-id="808e2-151">Atveriet papildinformāciju un pēc tam izvērsiet sadaļu Saistītie dokumenti.</span><span class="sxs-lookup"><span data-stu-id="808e2-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="808e2-152">Iespējams, jums jau ir atvērta papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="808e2-152">You may already have the FactBox open.</span></span> <span data-ttu-id="808e2-153">Meklējiet ikonu, uz kuras ir bultiņa, pa labi no rindu/virsrakstu pārslēgšanas pogām.</span><span class="sxs-lookup"><span data-stu-id="808e2-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="808e2-154">Ja bultiņa norāda pa labi, tad papildinformācija jau ir atvērta.</span><span class="sxs-lookup"><span data-stu-id="808e2-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="808e2-155">Ja bultiņa norāda pa kreisi, noklikšķiniet uz tās, lai atvērtu papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="808e2-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="808e2-156">Noklikšķiniet uz saites laukā Piedāvājuma pieprasījums, lai atvērtu tikko izveidoto IP.</span><span class="sxs-lookup"><span data-stu-id="808e2-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="808e2-157">Noklikšķiniet uz Virsraksts.</span><span class="sxs-lookup"><span data-stu-id="808e2-157">Click Header.</span></span>
10. <span data-ttu-id="808e2-158">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="808e2-158">Click Add.</span></span>
11. <span data-ttu-id="808e2-159">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="808e2-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="808e2-160">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="808e2-160">Click Add.</span></span>
13. <span data-ttu-id="808e2-161">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="808e2-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="808e2-162">Noklikšķiniet uz Sūtīt.</span><span class="sxs-lookup"><span data-stu-id="808e2-162">Click Send.</span></span>
15. <span data-ttu-id="808e2-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="808e2-163">Click OK.</span></span>
16. <span data-ttu-id="808e2-164">Noklikšķiniet uz Ievadīt atbildi.</span><span class="sxs-lookup"><span data-stu-id="808e2-164">Click Enter reply.</span></span>
17. <span data-ttu-id="808e2-165">Darbību rūtī noklikšķiniet uz Atbilde.</span><span class="sxs-lookup"><span data-stu-id="808e2-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="808e2-166">Noklikšķiniet uz Kopēt datus uz atbildēm.</span><span class="sxs-lookup"><span data-stu-id="808e2-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="808e2-167">Šādi no IP uz atbildi tiek kopēti dati, piemēram, daudzums un datumi.</span><span class="sxs-lookup"><span data-stu-id="808e2-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="808e2-168">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="808e2-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="808e2-169">Šī ir cena, ko saņēmāt no kreditora.</span><span class="sxs-lookup"><span data-stu-id="808e2-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="808e2-170">Iespējams, vēlaties arī ievadīt papildinformāciju no kreditora.</span><span class="sxs-lookup"><span data-stu-id="808e2-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="808e2-171">Noklikšķiniet uz Akceptēt.</span><span class="sxs-lookup"><span data-stu-id="808e2-171">Click Accept.</span></span>
21. <span data-ttu-id="808e2-172">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="808e2-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="808e2-173">Pārliecinieties, ka uz pieprasījumu ir pārsūtīts kreditors un cena</span><span class="sxs-lookup"><span data-stu-id="808e2-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="808e2-174">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-174">Close the page.</span></span>
2. <span data-ttu-id="808e2-175">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="808e2-175">Click Lines.</span></span>
3. <span data-ttu-id="808e2-176">Noklikšķiniet uz Saistītā informācija.</span><span class="sxs-lookup"><span data-stu-id="808e2-176">Click Related information.</span></span>
4. <span data-ttu-id="808e2-177">Noklikšķiniet uz Pirkšanas pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="808e2-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="808e2-178">Atlasiet rindu, kura tika pārsūtīta uz IP.</span><span class="sxs-lookup"><span data-stu-id="808e2-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="808e2-179">Pārliecinieties, ka uz pieprasījumu ir pārkopēta cena un kreditors.</span><span class="sxs-lookup"><span data-stu-id="808e2-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="808e2-180">Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="808e2-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="808e2-181">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="808e2-181">Click Complete.</span></span>
8. <span data-ttu-id="808e2-182">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="808e2-182">Close the page.</span></span>
9. <span data-ttu-id="808e2-183">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="808e2-183">Click Complete.</span></span>


