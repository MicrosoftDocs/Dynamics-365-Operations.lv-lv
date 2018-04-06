--- 
title: "Paplašināt datu modeli dokumentu pārvaldības failu lietošanai formāta izvades datos elektronisko pārskatu veidošanai (ER)"
description: "Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektroniskā pārskata izstrādātājs, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="72c60-103">Paplašināt datu modeli dokumentu pārvaldības failu lietošanai formāta izvades datos elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="72c60-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72c60-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektroniskā pārskata izstrādātājs, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="72c60-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="72c60-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="72c60-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="72c60-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti uzdevuma ceļvedī “ER Izmantot dokumentu pārvaldības failus formāta izvadē (1. daļa: Sagatavot datu modeli)”.</span><span class="sxs-lookup"><span data-stu-id="72c60-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="72c60-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="72c60-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="72c60-108">Paplašināt datu modeli, lai parādītu tajā dokumentu pārvaldības failus</span><span class="sxs-lookup"><span data-stu-id="72c60-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="72c60-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="72c60-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="72c60-110">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="72c60-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="72c60-111">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="72c60-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="72c60-112">Koka struktūrā atlasiet 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="72c60-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="72c60-113">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="72c60-113">Click Designer.</span></span>
6. <span data-ttu-id="72c60-114">Koka struktūrā atlasiet 'Customer invoice(InvoiceCustomer)'.</span><span class="sxs-lookup"><span data-stu-id="72c60-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="72c60-115">Mēs paplašināsim šo datu modeli, lai būtu pieejami visi tam pārdošanas pasūtījumam pievienotie faili, kas ir saistīts ar elektroniski apstrādātu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="72c60-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="72c60-116">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72c60-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="72c60-117">Laukā Nosaukums ierakstiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="72c60-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="72c60-118">Rēķinu pielikumi</span><span class="sxs-lookup"><span data-stu-id="72c60-118">Invoice attachments</span></span>  
9. <span data-ttu-id="72c60-119">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="72c60-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="72c60-120">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72c60-120">Click Add.</span></span>
11. <span data-ttu-id="72c60-121">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72c60-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="72c60-122">Laukā Nosaukums ierakstiet 'File content'.</span><span class="sxs-lookup"><span data-stu-id="72c60-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="72c60-123">Faila saturs</span><span class="sxs-lookup"><span data-stu-id="72c60-123">File content</span></span>  
13. <span data-ttu-id="72c60-124">Laukā Vienuma tips atlasiet 'Container'.</span><span class="sxs-lookup"><span data-stu-id="72c60-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="72c60-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72c60-125">Click Add.</span></span>
15. <span data-ttu-id="72c60-126">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72c60-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="72c60-127">Laukā Nosaukums ierakstiet 'File name'.</span><span class="sxs-lookup"><span data-stu-id="72c60-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="72c60-128">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="72c60-128">File name</span></span>  
17. <span data-ttu-id="72c60-129">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="72c60-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="72c60-130">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72c60-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="72c60-131">Jaunu datu modeļa elementu kartēšana uz Dynamics 365 for Finance and Operations datu avotiem</span><span class="sxs-lookup"><span data-stu-id="72c60-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="72c60-132">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="72c60-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="72c60-133">Izmantojiet ātrā filtra funkciju, lai filtrētu lauku Definīcija ar vērtību 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="72c60-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="72c60-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="72c60-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="72c60-135">Mēs saistīsim jaunā modeļa elementus ar piemērotiem datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="72c60-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="72c60-136">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="72c60-136">Click Designer.</span></span>
4. <span data-ttu-id="72c60-137">Koka struktūrā atlasiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="72c60-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="72c60-138">Koka struktūrā izvērsiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="72c60-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="72c60-139">Koka struktūrā atlasiet 'Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="72c60-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="72c60-140">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="72c60-140">Click Edit.</span></span>
8. <span data-ttu-id="72c60-141">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="72c60-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="72c60-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="72c60-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="72c60-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="72c60-143">Click Save.</span></span>
10. <span data-ttu-id="72c60-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72c60-144">Close the page.</span></span>
11. <span data-ttu-id="72c60-145">Koka struktūrā atlasiet 'Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="72c60-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="72c60-146">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="72c60-146">Click Edit.</span></span>
13. <span data-ttu-id="72c60-147">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="72c60-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="72c60-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="72c60-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="72c60-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="72c60-149">Click Save.</span></span>
15. <span data-ttu-id="72c60-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72c60-150">Close the page.</span></span>
16. <span data-ttu-id="72c60-151">Koka struktūrā atlasiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="72c60-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="72c60-152">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="72c60-152">Click Edit.</span></span>
18. <span data-ttu-id="72c60-153">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="72c60-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="72c60-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="72c60-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="72c60-155">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="72c60-155">Click Save.</span></span>
20. <span data-ttu-id="72c60-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72c60-156">Close the page.</span></span>
21. <span data-ttu-id="72c60-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="72c60-157">Click Save.</span></span>
22. <span data-ttu-id="72c60-158">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72c60-158">Close the page.</span></span>
23. <span data-ttu-id="72c60-159">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72c60-159">Close the page.</span></span>
24. <span data-ttu-id="72c60-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72c60-160">Close the page.</span></span>
25. <span data-ttu-id="72c60-161">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="72c60-161">Click Change status.</span></span>
26. <span data-ttu-id="72c60-162">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="72c60-162">Click Complete.</span></span>
27. <span data-ttu-id="72c60-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="72c60-163">Click OK.</span></span>


