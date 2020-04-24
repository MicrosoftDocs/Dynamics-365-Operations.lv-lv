---
title: Tāda pieprasījuma izveide, kas lieto PP
description: Šajā tēmā paskaidrots, kā pievienot cenas un piegādātāja informāciju pirkšanas pieprasījumam no piedāvājuma pieprasījuma procesa.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 205cba2325e76dae9572301e44e0e89cbcfd106e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204704"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="8fc94-103">Tāda pieprasījuma izveide, kas lieto PP</span><span class="sxs-lookup"><span data-stu-id="8fc94-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fc94-104">Šajā tēmā paskaidrots, kā pievienot cenas un piegādātāja informāciju pirkšanas pieprasījumam no piedāvājuma pieprasījuma procesa.</span><span class="sxs-lookup"><span data-stu-id="8fc94-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="8fc94-105">Šajā ceļvedī parādīto piemēru var izmantot ar uzņēmuma USMF demonstrācijas datiem, un jums ir jāpiesakās kā administratoram, lai izpildītu visas darbības.</span><span class="sxs-lookup"><span data-stu-id="8fc94-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="8fc94-106">Šajā ceļvedī aprakstītos uzdevumus parasti veiktu sagādes speciālisti.</span><span class="sxs-lookup"><span data-stu-id="8fc94-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="8fc94-107">Izveidot pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="8fc94-107">Create a requisition</span></span>
1. <span data-ttu-id="8fc94-108">Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Pirkšanas pieprasījumi > Manis sagatavotie pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="8fc94-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-109">Select **New**.</span></span>
3. <span data-ttu-id="8fc94-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8fc94-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="8fc94-111">Laukā **Pieprasītais datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="8fc94-112">Laukā **Uzskaites datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="8fc94-113">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-113">Select **OK**.</span></span>
7. <span data-ttu-id="8fc94-114">Laukā **Iemesls** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8fc94-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="8fc94-115">Atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-115">Select **Add line**.</span></span>
9. <span data-ttu-id="8fc94-116">Laukā **Iepirkuma kategorija**, atlasiet kategoriju kokā, tad atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="8fc94-117">Laukā **Preces nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8fc94-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="8fc94-118">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8fc94-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="8fc94-119">Laukā **Vienība** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8fc94-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="8fc94-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-120">Select **Save**.</span></span>
14. <span data-ttu-id="8fc94-121">Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="8fc94-122">Atlasiet **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-122">Select **Submit**.</span></span>
16. <span data-ttu-id="8fc94-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-123">Close the page.</span></span>
17. <span data-ttu-id="8fc94-124">Atlasiet **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="8fc94-125">Darbplūsmas uzdevuma piešķires maiņa</span><span class="sxs-lookup"><span data-stu-id="8fc94-125">Reassign a workflow task</span></span>
<span data-ttu-id="8fc94-126">Nākamais uzdevums ir izveidot IP, lai no kreditoriem saņemtu piedāvājumus par preci.</span><span class="sxs-lookup"><span data-stu-id="8fc94-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="8fc94-127">USMF demonstrācijas datos pieprasījuma darbplūsma ir iestatīta ar kārtulu, tāpēc, ja nav atlasīts kreditors vai ja vienības cena kādai rindai ir 0, konkrētam nodarbinātajam tiek piešķirts uzdevums izveidot IP.</span><span class="sxs-lookup"><span data-stu-id="8fc94-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="8fc94-128">Lai turpinātu ar šo ceļvedi, šis uzdevums ir jāpiešķir citam lietotājam (sev).</span><span class="sxs-lookup"><span data-stu-id="8fc94-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="8fc94-129">To varat izdarīt tikai tad, ja esat pieteicies kā Administrators.</span><span class="sxs-lookup"><span data-stu-id="8fc94-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="8fc94-130">Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="8fc94-131">Atlasiet **Skatīt vēsturi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-131">Select **View history**.</span></span>
3. <span data-ttu-id="8fc94-132">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-132">Refresh the page.</span></span>
4. <span data-ttu-id="8fc94-133">Izvērsiet **Izsekošanas detaļas** sadaļu</span><span class="sxs-lookup"><span data-stu-id="8fc94-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="8fc94-134">Kokā atlasiet rindu, kas sākas ar "Rindas darbplūsma aktivizēta".</span><span class="sxs-lookup"><span data-stu-id="8fc94-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="8fc94-135">Atlasiet **Skatīt darbplūsmas detaļas**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="8fc94-136">Izvērsiet sadaļu **Darba vienumi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="8fc94-137">Atlasiet **Atkārtoti piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="8fc94-138">Laukā **Lietotājs** atlasiet **Administrators**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="8fc94-139">Atlasiet **Atkārtoti piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="8fc94-140">Aizveriet abas lapas.</span><span class="sxs-lookup"><span data-stu-id="8fc94-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="8fc94-141">Izveidot PP</span><span class="sxs-lookup"><span data-stu-id="8fc94-141">Create an RFQ</span></span>

1. <span data-ttu-id="8fc94-142">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-142">Refresh the page.</span></span>
2. <span data-ttu-id="8fc94-143">Atlasiet **Piedāvājuma pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="8fc94-144">Lauka **Pērkošā juridiskā persona** atlasiet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="8fc94-145">Jums ir jāatlasa tā pati juridiskā persona, kas ir norādīta pieprasījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="8fc94-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="8fc94-146">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-146">In the list, mark the selected row.</span></span> <span data-ttu-id="8fc94-147">Ja jūsu pirkšanas pieprasījumā bija vairākas rindas, atlasiet visas tās rindas, kuras vēlaties pievienot šim IP.</span><span class="sxs-lookup"><span data-stu-id="8fc94-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="8fc94-148">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-148">Select **OK**.</span></span>
6. <span data-ttu-id="8fc94-149">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-149">Refresh the page.</span></span>
7. <span data-ttu-id="8fc94-150">Pārliecinieties, ka ir atvērti Notikumi, tad izvērsiet sadaļu **Saistīti dokumenti**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="8fc94-151">Atlasiet saiti laukā **Piedāvājuma pieprasījums**, lai atvērtu tikko izveidoto piedāvājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="8fc94-152">Atlasiet **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-152">Select **Header**.</span></span>
10. <span data-ttu-id="8fc94-153">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-153">Select **Add**.</span></span>
11. <span data-ttu-id="8fc94-154">Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8fc94-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="8fc94-155">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-155">Select **Add**.</span></span>
13. <span data-ttu-id="8fc94-156">Laukā **Kreditora konts** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8fc94-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="8fc94-157">Atlasiet **Nosūtīt**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-157">Select **Send**.</span></span>
15. <span data-ttu-id="8fc94-158">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-158">Select **OK**.</span></span>
16. <span data-ttu-id="8fc94-159">Atlasiet **Ievadīt atbildi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="8fc94-160">Darbību rūtī atlasiet **Atbilde**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="8fc94-161">Atlasiet **Kopēt datus uz atbildi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="8fc94-162">Šādi no IP uz atbildi tiek kopēti dati, piemēram, daudzums un datumi.</span><span class="sxs-lookup"><span data-stu-id="8fc94-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="8fc94-163">Laukā **Vienības cena** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8fc94-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="8fc94-164">Šī ir cena, ko saņēmāt no kreditora.</span><span class="sxs-lookup"><span data-stu-id="8fc94-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="8fc94-165">Iespējams, vēlaties arī ievadīt papildinformāciju no kreditora.</span><span class="sxs-lookup"><span data-stu-id="8fc94-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="8fc94-166">Atlasiet **Pieņemt**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-166">Select **Accept**.</span></span>
21. <span data-ttu-id="8fc94-167">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="8fc94-168">Pārliecinieties, ka uz pieprasījumu ir pārsūtīts kreditors un cena</span><span class="sxs-lookup"><span data-stu-id="8fc94-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="8fc94-169">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-169">Close the page.</span></span>
2. <span data-ttu-id="8fc94-170">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-170">Select **Lines**.</span></span>
3. <span data-ttu-id="8fc94-171">Atlasiet **Saistītā informācija**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-171">Select **Related information**.</span></span>
4. <span data-ttu-id="8fc94-172">Atlasiet **Pirkšanas pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="8fc94-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="8fc94-173">Atlasiet rindu, kura tika pārsūtīta uz IP.</span><span class="sxs-lookup"><span data-stu-id="8fc94-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="8fc94-174">Pārliecinieties, ka uz pieprasījumu ir pārkopēta cena un kreditors.</span><span class="sxs-lookup"><span data-stu-id="8fc94-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="8fc94-175">Atlasiet **Darbplūsma**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="8fc94-176">Atlasiet Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="8fc94-176">Select Complete.</span></span>
8. <span data-ttu-id="8fc94-177">Atlasiet lapu.</span><span class="sxs-lookup"><span data-stu-id="8fc94-177">Select the page.</span></span>
9. <span data-ttu-id="8fc94-178">Atlasiet Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="8fc94-178">Select Complete.</span></span>

