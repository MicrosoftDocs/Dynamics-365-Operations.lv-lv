---
title: ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (2. daļa. Datu modeļa paplašināšana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu dokumentu pārvaldības failu (pielikumu) izmantošanai ER izvadē. (2. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092595"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="7a03d-104">ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (2. daļa. Datu modeļa paplašināšana)</span><span class="sxs-lookup"><span data-stu-id="7a03d-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a03d-105">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektroniskā pārskata izstrādātājs, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="7a03d-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="7a03d-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="7a03d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="7a03d-107">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti uzdevuma ceļvedī "ER Izmantot dokumentu pārvaldības failus formāta izvadē (1. daļa: Sagatavot datu modeli)".</span><span class="sxs-lookup"><span data-stu-id="7a03d-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="7a03d-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="7a03d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="7a03d-109">Paplašināt datu modeli, lai parādītu tajā dokumentu pārvaldības failus</span><span class="sxs-lookup"><span data-stu-id="7a03d-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="7a03d-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="7a03d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7a03d-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="7a03d-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7a03d-112">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="7a03d-113">Koka struktūrā atlasiet 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="7a03d-114">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="7a03d-114">Click Designer.</span></span>
6. <span data-ttu-id="7a03d-115">Koka struktūrā atlasiet 'Customer invoice(InvoiceCustomer)'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="7a03d-116">Mēs paplašināsim šo datu modeli, lai būtu pieejami visi tam pārdošanas pasūtījumam pievienotie faili, kas ir saistīts ar elektroniski apstrādātu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="7a03d-117">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="7a03d-118">Laukā Nosaukums ierakstiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="7a03d-119">Rēķinu pielikumi</span><span class="sxs-lookup"><span data-stu-id="7a03d-119">Invoice attachments</span></span>  
9. <span data-ttu-id="7a03d-120">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="7a03d-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="7a03d-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="7a03d-121">Click Add.</span></span>
11. <span data-ttu-id="7a03d-122">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7a03d-123">Laukā Nosaukums ierakstiet 'File content'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="7a03d-124">Faila saturs</span><span class="sxs-lookup"><span data-stu-id="7a03d-124">File content</span></span>  
13. <span data-ttu-id="7a03d-125">Laukā Vienuma tips atlasiet 'Container'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="7a03d-126">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="7a03d-126">Click Add.</span></span>
15. <span data-ttu-id="7a03d-127">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="7a03d-128">Laukā Nosaukums ierakstiet 'File name'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="7a03d-129">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="7a03d-129">File name</span></span>  
17. <span data-ttu-id="7a03d-130">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="7a03d-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="7a03d-131">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="7a03d-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="7a03d-132">Saistīt jauna datu modeļa elementus ar datu avotiem</span><span class="sxs-lookup"><span data-stu-id="7a03d-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="7a03d-133">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="7a03d-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="7a03d-134">Izmantojiet ātrā filtra funkciju, lai filtrētu lauku Definīcija ar vērtību 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="7a03d-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="7a03d-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="7a03d-136">Mēs saistīsim jaunā modeļa elementus ar piemērotiem datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="7a03d-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="7a03d-137">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="7a03d-137">Click Designer.</span></span>
4. <span data-ttu-id="7a03d-138">Koka struktūrā atlasiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="7a03d-139">Koka struktūrā izvērsiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="7a03d-140">Koka struktūrā atlasiet 'Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="7a03d-141">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-141">Click Edit.</span></span>
8. <span data-ttu-id="7a03d-142">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="7a03d-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="7a03d-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="7a03d-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="7a03d-144">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-144">Click Save.</span></span>
10. <span data-ttu-id="7a03d-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-145">Close the page.</span></span>
11. <span data-ttu-id="7a03d-146">Koka struktūrā atlasiet 'Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="7a03d-147">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-147">Click Edit.</span></span>
13. <span data-ttu-id="7a03d-148">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="7a03d-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="7a03d-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="7a03d-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="7a03d-150">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-150">Click Save.</span></span>
15. <span data-ttu-id="7a03d-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-151">Close the page.</span></span>
16. <span data-ttu-id="7a03d-152">Koka struktūrā atlasiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="7a03d-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="7a03d-153">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-153">Click Edit.</span></span>
18. <span data-ttu-id="7a03d-154">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="7a03d-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="7a03d-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="7a03d-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="7a03d-156">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-156">Click Save.</span></span>
20. <span data-ttu-id="7a03d-157">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-157">Close the page.</span></span>
21. <span data-ttu-id="7a03d-158">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-158">Click Save.</span></span>
22. <span data-ttu-id="7a03d-159">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-159">Close the page.</span></span>
23. <span data-ttu-id="7a03d-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-160">Close the page.</span></span>
24. <span data-ttu-id="7a03d-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-161">Close the page.</span></span>
25. <span data-ttu-id="7a03d-162">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="7a03d-162">Click Change status.</span></span>
26. <span data-ttu-id="7a03d-163">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="7a03d-163">Click Complete.</span></span>
27. <span data-ttu-id="7a03d-164">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7a03d-164">Click OK.</span></span>

