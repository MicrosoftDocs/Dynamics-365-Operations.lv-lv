---
title: Tāda pieprasījuma izveide, kas lieto PP
description: Šajā tēmā paskaidrots, kā pievienot cenas un piegādātāja informāciju pirkšanas pieprasījumam no piedāvājuma pieprasījuma procesa.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e67dafd02a3b2a38832d8a4f0e9809adffcbb80
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211842"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="c7f6a-103">Tāda pieprasījuma izveide, kas lieto PP</span><span class="sxs-lookup"><span data-stu-id="c7f6a-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7f6a-104">Šajā tēmā paskaidrots, kā pievienot cenas un piegādātāja informāciju pirkšanas pieprasījumam no piedāvājuma pieprasījuma procesa.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="c7f6a-105">Šajā ceļvedī parādīto piemēru var izmantot paraugdatu uzņēmumā USMF, un jums ir jāpiesakās kā administratoram, lai izpildītu visas darbības.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="c7f6a-106">Šajā ceļvedī aprakstītos uzdevumus parasti veiktu sagādes speciālisti.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="c7f6a-107">Izveidot pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="c7f6a-107">Create a requisition</span></span>
1. <span data-ttu-id="c7f6a-108">Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Pirkšanas pieprasījumi > Manis sagatavotie pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="c7f6a-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-109">Select **New**.</span></span>
3. <span data-ttu-id="c7f6a-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c7f6a-111">Laukā **Pieprasītais datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="c7f6a-112">Laukā **Uzskaites datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="c7f6a-113">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-113">Select **OK**.</span></span>
7. <span data-ttu-id="c7f6a-114">Laukā **Iemesls** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="c7f6a-115">Atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-115">Select **Add line**.</span></span>
9. <span data-ttu-id="c7f6a-116">Laukā **Iepirkuma kategorija**, atlasiet kategoriju kokā, tad atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="c7f6a-117">Laukā **Preces nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="c7f6a-118">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="c7f6a-119">Laukā **Vienība** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="c7f6a-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-120">Select **Save**.</span></span>
14. <span data-ttu-id="c7f6a-121">Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="c7f6a-122">Atlasiet **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-122">Select **Submit**.</span></span>
16. <span data-ttu-id="c7f6a-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-123">Close the page.</span></span>
17. <span data-ttu-id="c7f6a-124">Atlasiet **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="c7f6a-125">Darbplūsmas uzdevuma piešķires maiņa</span><span class="sxs-lookup"><span data-stu-id="c7f6a-125">Reassign a workflow task</span></span>
<span data-ttu-id="c7f6a-126">Nākamais uzdevums ir izveidot IP, lai no kreditoriem saņemtu piedāvājumus par preci.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="c7f6a-127">USMF paraugdatos pieprasījuma darbplūsma ir iestatīta ar kārtulu, tāpēc, ja nav atlasīts kreditors vai ja vienības cena kādai rindai ir 0, konkrētam nodarbinātajam tiek piešķirts uzdevums izveidot IP.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="c7f6a-128">Lai turpinātu ar šo ceļvedi, šis uzdevums ir jāpiešķir citam lietotājam (sev).</span><span class="sxs-lookup"><span data-stu-id="c7f6a-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="c7f6a-129">To varat izdarīt tikai tad, ja esat pieteicies kā Administrators.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="c7f6a-130">Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="c7f6a-131">Atlasiet **Skatīt vēsturi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-131">Select **View history**.</span></span>
3. <span data-ttu-id="c7f6a-132">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-132">Refresh the page.</span></span>
4. <span data-ttu-id="c7f6a-133">Izvērsiet **Izsekošanas detaļas** sadaļu</span><span class="sxs-lookup"><span data-stu-id="c7f6a-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="c7f6a-134">Kokā atlasiet rindu, kas sākas ar "Rindas darbplūsma aktivizēta".</span><span class="sxs-lookup"><span data-stu-id="c7f6a-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="c7f6a-135">Atlasiet **Skatīt darbplūsmas detaļas**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="c7f6a-136">Izvērsiet sadaļu **Darba vienumi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="c7f6a-137">Atlasiet **Atkārtoti piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="c7f6a-138">Laukā **Lietotājs** atlasiet **Administrators**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="c7f6a-139">Atlasiet **Atkārtoti piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="c7f6a-140">Aizveriet abas lapas.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="c7f6a-141">Izveidot PP</span><span class="sxs-lookup"><span data-stu-id="c7f6a-141">Create an RFQ</span></span>

1. <span data-ttu-id="c7f6a-142">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-142">Refresh the page.</span></span>
2. <span data-ttu-id="c7f6a-143">Atlasiet **Piedāvājuma pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="c7f6a-144">Lauka **Pērkošā juridiskā persona** atlasiet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="c7f6a-145">Jums ir jāatlasa tā pati juridiskā persona, kas ir norādīta pieprasījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="c7f6a-146">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-146">In the list, mark the selected row.</span></span> <span data-ttu-id="c7f6a-147">Ja jūsu pirkšanas pieprasījumā bija vairākas rindas, atlasiet visas tās rindas, kuras vēlaties pievienot šim IP.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="c7f6a-148">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-148">Select **OK**.</span></span>
6. <span data-ttu-id="c7f6a-149">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-149">Refresh the page.</span></span>
7. <span data-ttu-id="c7f6a-150">Pārliecinieties, ka ir atvērti Notikumi, tad izvērsiet sadaļu **Saistīti dokumenti**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="c7f6a-151">Atlasiet saiti laukā **Piedāvājuma pieprasījums**, lai atvērtu tikko izveidoto piedāvājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="c7f6a-152">Atlasiet **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-152">Select **Header**.</span></span>
10. <span data-ttu-id="c7f6a-153">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-153">Select **Add**.</span></span>
11. <span data-ttu-id="c7f6a-154">Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="c7f6a-155">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-155">Select **Add**.</span></span>
13. <span data-ttu-id="c7f6a-156">Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="c7f6a-157">Atlasiet **Nosūtīt**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-157">Select **Send**.</span></span>
15. <span data-ttu-id="c7f6a-158">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-158">Select **OK**.</span></span>
16. <span data-ttu-id="c7f6a-159">Atlasiet **Ievadīt atbildi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="c7f6a-160">Darbību rūtī atlasiet **Atbilde**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="c7f6a-161">Atlasiet **Kopēt datus uz atbildi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="c7f6a-162">Šādi no IP uz atbildi tiek kopēti dati, piemēram, daudzums un datumi.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="c7f6a-163">Laukā **Vienības cena** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="c7f6a-164">Šī ir cena, ko saņēmāt no kreditora.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="c7f6a-165">Iespējams, vēlaties arī ievadīt papildinformāciju no kreditora.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="c7f6a-166">Atlasiet **Pieņemt**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-166">Select **Accept**.</span></span>
21. <span data-ttu-id="c7f6a-167">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="c7f6a-168">Pārliecinieties, ka uz pieprasījumu ir pārsūtīts kreditors un cena</span><span class="sxs-lookup"><span data-stu-id="c7f6a-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="c7f6a-169">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-169">Close the page.</span></span>
2. <span data-ttu-id="c7f6a-170">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-170">Select **Lines**.</span></span>
3. <span data-ttu-id="c7f6a-171">Atlasiet **Saistītā informācija**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-171">Select **Related information**.</span></span>
4. <span data-ttu-id="c7f6a-172">Atlasiet **Pirkšanas pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="c7f6a-173">Atlasiet rindu, kura tika pārsūtīta uz IP.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="c7f6a-174">Pārliecinieties, ka uz pieprasījumu ir pārkopēta cena un kreditors.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="c7f6a-175">Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="c7f6a-176">Atlasiet Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-176">Select Complete.</span></span>
8. <span data-ttu-id="c7f6a-177">Atlasiet lapu.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-177">Select the page.</span></span>
9. <span data-ttu-id="c7f6a-178">Atlasiet Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="c7f6a-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]