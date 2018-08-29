--- 
title: "Datu modeļu paplašināšana, lai dokumentu pārvaldības failus lietotu ER izvadē"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8363dd2af728577175a620d7b645d90cea84803a
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="extend-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="0d335-103">Datu modeļu paplašināšana, lai dokumentu pārvaldības failus lietotu ER izvadē</span><span class="sxs-lookup"><span data-stu-id="0d335-103">Extend data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d335-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektroniskā pārskata izstrādātājs, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="0d335-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0d335-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="0d335-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0d335-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti uzdevuma ceļvedī “ER Izmantot dokumentu pārvaldības failus formāta izvadē (1. daļa: Sagatavot datu modeli)”.</span><span class="sxs-lookup"><span data-stu-id="0d335-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="0d335-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="0d335-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="0d335-108">Paplašināt datu modeli, lai parādītu tajā dokumentu pārvaldības failus</span><span class="sxs-lookup"><span data-stu-id="0d335-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="0d335-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="0d335-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0d335-110">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="0d335-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0d335-111">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="0d335-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="0d335-112">Koka struktūrā atlasiet 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="0d335-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="0d335-113">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="0d335-113">Click Designer.</span></span>
6. <span data-ttu-id="0d335-114">Koka struktūrā atlasiet 'Customer invoice(InvoiceCustomer)'.</span><span class="sxs-lookup"><span data-stu-id="0d335-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="0d335-115">Mēs paplašināsim šo datu modeli, lai būtu pieejami visi tam pārdošanas pasūtījumam pievienotie faili, kas ir saistīts ar elektroniski apstrādātu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="0d335-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="0d335-116">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0d335-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="0d335-117">Laukā Nosaukums ierakstiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="0d335-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="0d335-118">Rēķinu pielikumi</span><span class="sxs-lookup"><span data-stu-id="0d335-118">Invoice attachments</span></span>  
9. <span data-ttu-id="0d335-119">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="0d335-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="0d335-120">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0d335-120">Click Add.</span></span>
11. <span data-ttu-id="0d335-121">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0d335-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0d335-122">Laukā Nosaukums ierakstiet 'File content'.</span><span class="sxs-lookup"><span data-stu-id="0d335-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="0d335-123">Faila saturs</span><span class="sxs-lookup"><span data-stu-id="0d335-123">File content</span></span>  
13. <span data-ttu-id="0d335-124">Laukā Vienuma tips atlasiet 'Container'.</span><span class="sxs-lookup"><span data-stu-id="0d335-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="0d335-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0d335-125">Click Add.</span></span>
15. <span data-ttu-id="0d335-126">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0d335-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="0d335-127">Laukā Nosaukums ierakstiet 'File name'.</span><span class="sxs-lookup"><span data-stu-id="0d335-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="0d335-128">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="0d335-128">File name</span></span>  
17. <span data-ttu-id="0d335-129">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="0d335-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="0d335-130">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0d335-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="0d335-131">Jaunu datu modeļa elementu kartēšana uz Dynamics 365 for Finance and Operations datu avotiem</span><span class="sxs-lookup"><span data-stu-id="0d335-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="0d335-132">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="0d335-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="0d335-133">Izmantojiet ātrā filtra funkciju, lai filtrētu lauku Definīcija ar vērtību 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="0d335-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="0d335-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="0d335-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="0d335-135">Mēs saistīsim jaunā modeļa elementus ar piemērotiem datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="0d335-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="0d335-136">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="0d335-136">Click Designer.</span></span>
4. <span data-ttu-id="0d335-137">Koka struktūrā atlasiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="0d335-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="0d335-138">Koka struktūrā izvērsiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="0d335-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="0d335-139">Koka struktūrā atlasiet 'Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="0d335-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="0d335-140">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0d335-140">Click Edit.</span></span>
8. <span data-ttu-id="0d335-141">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="0d335-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="0d335-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="0d335-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="0d335-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0d335-143">Click Save.</span></span>
10. <span data-ttu-id="0d335-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0d335-144">Close the page.</span></span>
11. <span data-ttu-id="0d335-145">Koka struktūrā atlasiet 'Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="0d335-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="0d335-146">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0d335-146">Click Edit.</span></span>
13. <span data-ttu-id="0d335-147">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="0d335-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="0d335-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="0d335-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="0d335-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0d335-149">Click Save.</span></span>
15. <span data-ttu-id="0d335-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0d335-150">Close the page.</span></span>
16. <span data-ttu-id="0d335-151">Koka struktūrā atlasiet 'Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="0d335-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="0d335-152">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0d335-152">Click Edit.</span></span>
18. <span data-ttu-id="0d335-153">Laukā Formula ievadiet 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="0d335-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="0d335-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="0d335-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="0d335-155">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0d335-155">Click Save.</span></span>
20. <span data-ttu-id="0d335-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0d335-156">Close the page.</span></span>
21. <span data-ttu-id="0d335-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0d335-157">Click Save.</span></span>
22. <span data-ttu-id="0d335-158">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0d335-158">Close the page.</span></span>
23. <span data-ttu-id="0d335-159">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0d335-159">Close the page.</span></span>
24. <span data-ttu-id="0d335-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0d335-160">Close the page.</span></span>
25. <span data-ttu-id="0d335-161">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="0d335-161">Click Change status.</span></span>
26. <span data-ttu-id="0d335-162">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="0d335-162">Click Complete.</span></span>
27. <span data-ttu-id="0d335-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0d335-163">Click OK.</span></span>


