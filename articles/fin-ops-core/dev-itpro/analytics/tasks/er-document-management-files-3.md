---
title: ER izmantot dokumentu pārvaldības failus formātu izvades datos (3. daļa - Izveidot formātu)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu dokumentu pārvaldības failu (pielikumu) izmantošanai ER izvadē. (3. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092620"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="2248c-104">ER izmantot dokumentu pārvaldības failus formātu izvades datos (3. daļa - Izveidot formātu)</span><span class="sxs-lookup"><span data-stu-id="2248c-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2248c-105">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="2248c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="2248c-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="2248c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="2248c-107">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Izmantot dokumentu pārvaldības failus formāta izvadē (2. daļa: Paplašināt datu modeli)".</span><span class="sxs-lookup"><span data-stu-id="2248c-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="2248c-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="2248c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="2248c-109">Izveidot rēķinu apstrādes formātu</span><span class="sxs-lookup"><span data-stu-id="2248c-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="2248c-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="2248c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2248c-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="2248c-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2248c-112">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="2248c-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="2248c-113">Koka struktūrā atlasiet 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="2248c-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="2248c-114">Tiks izveidots formāts, lai ģenerētu elektroniskos ziņojumus ar informāciju par visiem failiem, kas ir pievienoti ar elektroniski apstrādāto rēķinu saistītajam pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="2248c-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="2248c-115">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2248c-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="2248c-116">Laukā Jauns ievadiet 'Format based on data model Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="2248c-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="2248c-117">Laukā Nosaukums ierakstiet 'Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="2248c-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="2248c-118">Elektronisks rēķina parauga ziņojums</span><span class="sxs-lookup"><span data-stu-id="2248c-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="2248c-119">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="2248c-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2248c-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="2248c-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="2248c-121">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="2248c-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="2248c-122">Izstrādāt pielikumu aizpildīšanas formātu, ģenerējot ziņojums MIME formātā</span><span class="sxs-lookup"><span data-stu-id="2248c-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="2248c-123">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="2248c-123">Click Designer.</span></span>
2. <span data-ttu-id="2248c-124">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="2248c-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="2248c-125">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="2248c-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="2248c-126">Laukā Nosaukums ierakstiet 'Invoice'.</span><span class="sxs-lookup"><span data-stu-id="2248c-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="2248c-127">Rēķins</span><span class="sxs-lookup"><span data-stu-id="2248c-127">Invoice</span></span>  
5. <span data-ttu-id="2248c-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-128">Click OK.</span></span>
6. <span data-ttu-id="2248c-129">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2248c-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="2248c-130">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="2248c-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="2248c-131">Laukā Nosaukums ierakstiet 'SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="2248c-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="2248c-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="2248c-132">SalesOrder</span></span>  
9. <span data-ttu-id="2248c-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-133">Click OK.</span></span>
10. <span data-ttu-id="2248c-134">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="2248c-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="2248c-135">Laukā Nosaukums ierakstiet 'InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="2248c-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="2248c-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="2248c-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="2248c-137">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-137">Click OK.</span></span>
13. <span data-ttu-id="2248c-138">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="2248c-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="2248c-139">Laukā Nosaukums ierakstiet 'InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="2248c-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="2248c-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="2248c-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="2248c-141">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-141">Click OK.</span></span>
16. <span data-ttu-id="2248c-142">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2248c-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="2248c-143">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="2248c-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="2248c-144">Laukā Nosaukums ierakstiet 'EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="2248c-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="2248c-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="2248c-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="2248c-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-146">Click OK.</span></span>
20. <span data-ttu-id="2248c-147">Koka struktūrā atlasiet 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="2248c-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="2248c-148">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="2248c-148">Click Add Element.</span></span>
22. <span data-ttu-id="2248c-149">Laukā Nosaukums ierakstiet 'Document'.</span><span class="sxs-lookup"><span data-stu-id="2248c-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="2248c-150">Attaisnojuma dokuments</span><span class="sxs-lookup"><span data-stu-id="2248c-150">Document</span></span>  
23. <span data-ttu-id="2248c-151">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-151">Click OK.</span></span>
24. <span data-ttu-id="2248c-152">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="2248c-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="2248c-153">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2248c-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="2248c-154">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="2248c-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="2248c-155">Laukā Nosaukums ierakstiet 'FileName'.</span><span class="sxs-lookup"><span data-stu-id="2248c-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="2248c-156">FileName</span><span class="sxs-lookup"><span data-stu-id="2248c-156">FileName</span></span>  
28. <span data-ttu-id="2248c-157">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-157">Click OK.</span></span>
29. <span data-ttu-id="2248c-158">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2248c-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="2248c-159">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="2248c-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="2248c-160">Laukā Nosaukums ierakstiet 'FileContent'.</span><span class="sxs-lookup"><span data-stu-id="2248c-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="2248c-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="2248c-161">FileContent</span></span>  
32. <span data-ttu-id="2248c-162">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-162">Click OK.</span></span>
33. <span data-ttu-id="2248c-163">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileContent'.</span><span class="sxs-lookup"><span data-stu-id="2248c-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="2248c-164">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2248c-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="2248c-165">Koka struktūrā atlasiet 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="2248c-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="2248c-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2248c-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="2248c-167">Saistīt formāta elementus ar datu modeli kā datu avotu</span><span class="sxs-lookup"><span data-stu-id="2248c-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="2248c-168">Koka struktūrā atlasiet 'Invoice\SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="2248c-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="2248c-169">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="2248c-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="2248c-170">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="2248c-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="2248c-171">Koka struktūrā atlasiet 'model\Sales order number(SalesId)'.</span><span class="sxs-lookup"><span data-stu-id="2248c-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="2248c-172">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2248c-172">Click Bind.</span></span>
6. <span data-ttu-id="2248c-173">Koka struktūrā atlasiet 'Invoice\InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="2248c-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="2248c-174">Koka struktūrā izvērsiet 'model\Base invoice(InvoiceBase)'.</span><span class="sxs-lookup"><span data-stu-id="2248c-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="2248c-175">Koka struktūrā izvērsiet 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span><span class="sxs-lookup"><span data-stu-id="2248c-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="2248c-176">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2248c-176">Click Bind.</span></span>
10. <span data-ttu-id="2248c-177">Koka struktūrā atlasiet 'Invoice\InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="2248c-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="2248c-178">Koka struktūrā atlasiet 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span><span class="sxs-lookup"><span data-stu-id="2248c-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="2248c-179">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2248c-179">Click Bind.</span></span>
13. <span data-ttu-id="2248c-180">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="2248c-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="2248c-181">Koka struktūrā atlasiet 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="2248c-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="2248c-182">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span><span class="sxs-lookup"><span data-stu-id="2248c-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="2248c-183">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2248c-183">Click Bind.</span></span>
17. <span data-ttu-id="2248c-184">Koka struktūrā atlasiet 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="2248c-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="2248c-185">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileName'.</span><span class="sxs-lookup"><span data-stu-id="2248c-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="2248c-186">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2248c-186">Click Bind.</span></span>
20. <span data-ttu-id="2248c-187">Koka struktūrā atlasiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="2248c-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="2248c-188">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="2248c-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="2248c-189">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="2248c-189">Click Bind.</span></span>
23. <span data-ttu-id="2248c-190">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2248c-190">Click Save.</span></span>
24. <span data-ttu-id="2248c-191">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2248c-191">Close the page.</span></span>

