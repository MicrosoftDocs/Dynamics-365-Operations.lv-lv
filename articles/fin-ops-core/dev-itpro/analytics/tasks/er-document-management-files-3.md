---
title: ER izmantot dokumentu pārvaldības failus formātu izvades datos (3. daļa - Izveidot formātu)
description: Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus ER izvadē.
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
ms.openlocfilehash: bfcc03fa7470d4f2fa45ef012e30acef0712bf99
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681857"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="9ab9c-103">ER izmantot dokumentu pārvaldības failus formātu izvades datos (3. daļa - Izveidot formātu)</span><span class="sxs-lookup"><span data-stu-id="9ab9c-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ab9c-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9ab9c-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9ab9c-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Izmantot dokumentu pārvaldības failus formāta izvadē (2. daļa: Paplašināt datu modeli)".</span><span class="sxs-lookup"><span data-stu-id="9ab9c-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="9ab9c-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="9ab9c-108">Izveidot rēķinu apstrādes formātu</span><span class="sxs-lookup"><span data-stu-id="9ab9c-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="9ab9c-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9ab9c-110">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9ab9c-111">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="9ab9c-112">Koka struktūrā atlasiet 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="9ab9c-113">Tiks izveidots formāts, lai ģenerētu elektroniskos ziņojumus ar informāciju par visiem failiem, kas ir pievienoti ar elektroniski apstrādāto rēķinu saistītajam pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="9ab9c-114">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="9ab9c-115">Laukā Jauns ievadiet 'Format based on data model Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="9ab9c-116">Laukā Nosaukums ierakstiet 'Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="9ab9c-117">Elektronisks rēķina parauga ziņojums</span><span class="sxs-lookup"><span data-stu-id="9ab9c-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="9ab9c-118">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="9ab9c-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="9ab9c-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="9ab9c-120">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="9ab9c-121">Izstrādāt pielikumu aizpildīšanas formātu, ģenerējot ziņojums MIME formātā</span><span class="sxs-lookup"><span data-stu-id="9ab9c-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="9ab9c-122">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-122">Click Designer.</span></span>
2. <span data-ttu-id="9ab9c-123">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="9ab9c-124">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="9ab9c-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="9ab9c-125">Laukā Nosaukums ierakstiet 'Invoice'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="9ab9c-126">Rēķins</span><span class="sxs-lookup"><span data-stu-id="9ab9c-126">Invoice</span></span>  
5. <span data-ttu-id="9ab9c-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-127">Click OK.</span></span>
6. <span data-ttu-id="9ab9c-128">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="9ab9c-129">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="9ab9c-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="9ab9c-130">Laukā Nosaukums ierakstiet 'SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="9ab9c-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="9ab9c-131">SalesOrder</span></span>  
9. <span data-ttu-id="9ab9c-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-132">Click OK.</span></span>
10. <span data-ttu-id="9ab9c-133">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="9ab9c-134">Laukā Nosaukums ierakstiet 'InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="9ab9c-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="9ab9c-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="9ab9c-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-136">Click OK.</span></span>
13. <span data-ttu-id="9ab9c-137">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="9ab9c-138">Laukā Nosaukums ierakstiet 'InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="9ab9c-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="9ab9c-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="9ab9c-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-140">Click OK.</span></span>
16. <span data-ttu-id="9ab9c-141">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="9ab9c-142">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="9ab9c-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="9ab9c-143">Laukā Nosaukums ierakstiet 'EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="9ab9c-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="9ab9c-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="9ab9c-145">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-145">Click OK.</span></span>
20. <span data-ttu-id="9ab9c-146">Koka struktūrā atlasiet 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="9ab9c-147">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-147">Click Add Element.</span></span>
22. <span data-ttu-id="9ab9c-148">Laukā Nosaukums ierakstiet 'Document'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="9ab9c-149">Attaisnojuma dokuments</span><span class="sxs-lookup"><span data-stu-id="9ab9c-149">Document</span></span>  
23. <span data-ttu-id="9ab9c-150">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-150">Click OK.</span></span>
24. <span data-ttu-id="9ab9c-151">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="9ab9c-152">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="9ab9c-153">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="9ab9c-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="9ab9c-154">Laukā Nosaukums ierakstiet 'FileName'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="9ab9c-155">FileName</span><span class="sxs-lookup"><span data-stu-id="9ab9c-155">FileName</span></span>  
28. <span data-ttu-id="9ab9c-156">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-156">Click OK.</span></span>
29. <span data-ttu-id="9ab9c-157">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="9ab9c-158">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="9ab9c-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="9ab9c-159">Laukā Nosaukums ierakstiet 'FileContent'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="9ab9c-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="9ab9c-160">FileContent</span></span>  
32. <span data-ttu-id="9ab9c-161">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-161">Click OK.</span></span>
33. <span data-ttu-id="9ab9c-162">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileContent'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="9ab9c-163">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="9ab9c-164">Koka struktūrā atlasiet 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="9ab9c-165">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="9ab9c-166">Saistīt formāta elementus ar datu modeli kā datu avotu</span><span class="sxs-lookup"><span data-stu-id="9ab9c-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="9ab9c-167">Koka struktūrā atlasiet 'Invoice\SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="9ab9c-168">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="9ab9c-169">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="9ab9c-170">Koka struktūrā atlasiet 'model\Sales order number(SalesId)'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="9ab9c-171">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-171">Click Bind.</span></span>
6. <span data-ttu-id="9ab9c-172">Koka struktūrā atlasiet 'Invoice\InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="9ab9c-173">Koka struktūrā izvērsiet 'model\Base invoice(InvoiceBase)'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="9ab9c-174">Koka struktūrā izvērsiet 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="9ab9c-175">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-175">Click Bind.</span></span>
10. <span data-ttu-id="9ab9c-176">Koka struktūrā atlasiet 'Invoice\InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="9ab9c-177">Koka struktūrā atlasiet 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="9ab9c-178">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-178">Click Bind.</span></span>
13. <span data-ttu-id="9ab9c-179">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="9ab9c-180">Koka struktūrā atlasiet 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="9ab9c-181">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="9ab9c-182">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-182">Click Bind.</span></span>
17. <span data-ttu-id="9ab9c-183">Koka struktūrā atlasiet 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="9ab9c-184">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document\FileName'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="9ab9c-185">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-185">Click Bind.</span></span>
20. <span data-ttu-id="9ab9c-186">Koka struktūrā atlasiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="9ab9c-187">Koka struktūrā atlasiet 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="9ab9c-188">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-188">Click Bind.</span></span>
23. <span data-ttu-id="9ab9c-189">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-189">Click Save.</span></span>
24. <span data-ttu-id="9ab9c-190">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ab9c-190">Close the page.</span></span>

