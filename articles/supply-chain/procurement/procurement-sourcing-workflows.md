---
title: "Sagādes un avotu darbplūsmas"
description: "Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu. Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cc995b474e86272b49629f97e1b4d4b4fb597b9d
ms.openlocfilehash: d25ca64fb6a3fa7d7898ec68568703f3de7b1595
ms.contentlocale: lv-lv
ms.lasthandoff: 11/13/2018

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="309ea-104">Sagādes un avotu darbplūsmas</span><span class="sxs-lookup"><span data-stu-id="309ea-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="309ea-105">Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu.</span><span class="sxs-lookup"><span data-stu-id="309ea-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="309ea-106">Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="309ea-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="309ea-107">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="309ea-107">A workflow represents a business process.</span></span> <span data-ttu-id="309ea-108">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kuram ir jāpabeidz uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="309ea-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="309ea-109">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="309ea-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="309ea-110">**Saskaņoti procesi** — varat definēt noteiktu dokumentiem, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="309ea-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="309ea-111">Izmantojot darbplūsmas sistēmu, varat nodrošināt saskaņotu un efektīvu dokumentu apstrādes un apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="309ea-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="309ea-112">**Procesa pārskatāmība** — varat sekot līdzi noteiktas darbplūsmas instances statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="309ea-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="309ea-113">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="309ea-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="309ea-114">**Centralizēts darbu saraksts** — lietotāji var skatīt centralizētu darbu sarakstu, lai skatītu darbplūsmas uzdevumus un apstiprinājumus, kas viņiem ir piešķirti visās darbplūsmās, kurās viņi piedalās.</span><span class="sxs-lookup"><span data-stu-id="309ea-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="309ea-115">Šī funkcija ir pieejama lapā Darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="309ea-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="309ea-116">Izveidojamo darbplūsmu veidi</span><span class="sxs-lookup"><span data-stu-id="309ea-116">The types of workflows that you can create</span></span>
<span data-ttu-id="309ea-117">Sagādei un avotiem ir pieejami šādi darbplūsmu veidi.</span><span class="sxs-lookup"><span data-stu-id="309ea-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="309ea-118">**Tips**</span><span class="sxs-lookup"><span data-stu-id="309ea-118">**Type**</span></span>                         | <span data-ttu-id="309ea-119">**Šī tipa lietošanas nolūks**</span><span class="sxs-lookup"><span data-stu-id="309ea-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="309ea-120">Pirkšanas pieprasījuma pārskats</span><span class="sxs-lookup"><span data-stu-id="309ea-120">Purchase requisition review</span></span>      | <span data-ttu-id="309ea-121">Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="309ea-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="309ea-122">Pirkšanas pieprasījuma rindas pārskats</span><span class="sxs-lookup"><span data-stu-id="309ea-122">Purchase requisition line review</span></span> | <span data-ttu-id="309ea-123">Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumu rindām.</span><span class="sxs-lookup"><span data-stu-id="309ea-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="309ea-124">Pirkšanas pasūtījuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="309ea-124">Purchase order workflow</span></span>          | <span data-ttu-id="309ea-125">Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="309ea-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="309ea-126">Pirkšanas pasūtījuma rindas darbplūsma</span><span class="sxs-lookup"><span data-stu-id="309ea-126">Purchase order line workflow</span></span>     | <span data-ttu-id="309ea-127">Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas rindas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="309ea-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="309ea-128">Kreditoru pievienošanas pieteikumu darbplūsma</span><span class="sxs-lookup"><span data-stu-id="309ea-128">Vendor add application workflow</span></span>  | <span data-ttu-id="309ea-129">Izveidot pārskatīšanas un apstiprināšanas darbplūsmas jaunu piegādātāju pievienošanai, izmantojot piegādātāju pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="309ea-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="309ea-130">Darbplūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="309ea-130">Creating a workflow</span></span>

<span data-ttu-id="309ea-131">Lai izveidotu darbplūsmu, pārejiet uz sadaļu Sagāde un avoti &gt; Iestatījumi &gt; Sagādes un avotu darbplūsmas un izveidojiet jaunu darbplūsmu, atlasot izveidojamās darbplūsmas veidu.</span><span class="sxs-lookup"><span data-stu-id="309ea-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="309ea-132">Darbplūsmas audeklā varat vilkt darbplūsmas elementus uz veidotāju un saistīt elementus plūsmā.</span><span class="sxs-lookup"><span data-stu-id="309ea-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="309ea-133">Darbplūsmas elementi ir jākonfigurē.</span><span class="sxs-lookup"><span data-stu-id="309ea-133">The workflow elements should be configured.</span></span> <span data-ttu-id="309ea-134">Apstiprinājumam un uzdevuma darbplūsmas elementiem var konfigurēt to, kuram dalībniekam jāveic darbība.</span><span class="sxs-lookup"><span data-stu-id="309ea-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="309ea-135">Dalībnieku tipi</span><span class="sxs-lookup"><span data-stu-id="309ea-135">Types of participants</span></span>

<span data-ttu-id="309ea-136">Apstiprināšanas darbību varat piešķirt šādām dalībnieku grupām.</span><span class="sxs-lookup"><span data-stu-id="309ea-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="309ea-137">Lietotāju grupa</span><span class="sxs-lookup"><span data-stu-id="309ea-137">User group</span></span>    | <span data-ttu-id="309ea-138">Apraksts</span><span class="sxs-lookup"><span data-stu-id="309ea-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="309ea-139">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="309ea-139">Participant</span></span>   | <span data-ttu-id="309ea-140">Piešķiriet apstiprināšanas darbību kādas grupas vai lomas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="309ea-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="309ea-141">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="309ea-141">Hierarchy</span></span>     | <span data-ttu-id="309ea-142">Piešķiriet apstiprināšanas darbību lietotājiem noteiktā organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="309ea-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="309ea-143">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="309ea-143">Workflow user</span></span> | <span data-ttu-id="309ea-144">Piešķiriet apstiprināšanas darbību šīs darbplūsmas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="309ea-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="309ea-145">Rinda</span><span class="sxs-lookup"><span data-stu-id="309ea-145">Queue</span></span>         | <span data-ttu-id="309ea-146">Piešķiriet apstiprinājuma darbību darba vienumu rindai.</span><span class="sxs-lookup"><span data-stu-id="309ea-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="309ea-147">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="309ea-147">User</span></span>          | <span data-ttu-id="309ea-148">Piešķiriet apstiprināšanas darbību konkrētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="309ea-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="309ea-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="309ea-149">Additional resources</span></span>

- [<span data-ttu-id="309ea-150">Biznesa procesu darbplūsmu definēšana pirkšanas pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="309ea-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="309ea-151">Pirkšanas pieprasījuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="309ea-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="309ea-152">Kreditoru pievienošana</span><span class="sxs-lookup"><span data-stu-id="309ea-152">Onboarding vendors</span></span>](vendor-onboarding.md)


