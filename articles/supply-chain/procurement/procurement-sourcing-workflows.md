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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3bf244786e308ebcaee27a16fae378f41086f963
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="85307-104">Sagādes un avotu darbplūsmas</span><span class="sxs-lookup"><span data-stu-id="85307-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="85307-105">Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu.</span><span class="sxs-lookup"><span data-stu-id="85307-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="85307-106">Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="85307-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="85307-107">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="85307-107">A workflow represents a business process.</span></span> <span data-ttu-id="85307-108">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kuram ir jāpabeidz uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="85307-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="85307-109">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="85307-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="85307-110">**Saskaņoti procesi** — varat definēt noteiktu dokumentiem, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="85307-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="85307-111">Izmantojot darbplūsmas sistēmu, varat nodrošināt saskaņotu un efektīvu dokumentu apstrādes un apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="85307-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="85307-112">**Procesa pārskatāmība** — varat sekot līdzi noteiktas darbplūsmas instances statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="85307-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="85307-113">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="85307-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="85307-114">**Centralizēts darbu saraksts** — lietotāji var skatīt centralizētu darbu sarakstu, lai skatītu darbplūsmas uzdevumus un apstiprinājumus, kas viņiem ir piešķirti visās darbplūsmās, kurās viņi piedalās.</span><span class="sxs-lookup"><span data-stu-id="85307-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="85307-115">Šī funkcija ir pieejama lapā Darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="85307-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="85307-116"> Izveidojamo darbplūsmu veidi</span><span class="sxs-lookup"><span data-stu-id="85307-116">The types of workflows that you can create</span></span>
<span data-ttu-id="85307-117">Sagādei un avotiem ir pieejami šādi darbplūsmu veidi.</span><span class="sxs-lookup"><span data-stu-id="85307-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="85307-118">**Tips**</span><span class="sxs-lookup"><span data-stu-id="85307-118">**Type**</span></span>                         | <span data-ttu-id="85307-119">**Šī tipa lietošanas nolūks**</span><span class="sxs-lookup"><span data-stu-id="85307-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="85307-120">Pirkšanas pieprasījuma pārskats</span><span class="sxs-lookup"><span data-stu-id="85307-120">Purchase requisition review</span></span>      | <span data-ttu-id="85307-121">Izveidojiet pārskatīšanas darbplūsmas pirkšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="85307-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="85307-122">Pirkšanas pieprasījuma rindas pārskats</span><span class="sxs-lookup"><span data-stu-id="85307-122">Purchase requisition line review</span></span> | <span data-ttu-id="85307-123">Izveidojiet pārskatīšanas darbplūsmas pirkšanas rindas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="85307-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="85307-124">Pirkšanas pasūtījuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="85307-124">Purchase order workflow</span></span>          | <span data-ttu-id="85307-125">Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="85307-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="85307-126">Pirkšanas pasūtījuma rindas darbplūsma</span><span class="sxs-lookup"><span data-stu-id="85307-126">Purchase order line workflow</span></span>     | <span data-ttu-id="85307-127">Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas rindas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="85307-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="85307-128">Darbplūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="85307-128">Creating a workflow</span></span>
<span data-ttu-id="85307-129">Lai izveidotu darbplūsmu, pārejiet uz sadaļu Sagāde un avoti &gt; Iestatījumi &gt; Sagādes un avotu darbplūsmas un izveidojiet jaunu darbplūsmu, atlasot izveidojamās darbplūsmas veidu.</span><span class="sxs-lookup"><span data-stu-id="85307-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="85307-130">Darbplūsmas audeklā varat vilkt darbplūsmas elementus uz veidotāju un saistīt elementus plūsmā.</span><span class="sxs-lookup"><span data-stu-id="85307-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="85307-131">Darbplūsmas elementi ir jākonfigurē.</span><span class="sxs-lookup"><span data-stu-id="85307-131">The workflow elements should be configured.</span></span> <span data-ttu-id="85307-132">Apstiprinājumam un uzdevuma darbplūsmas elementiem var konfigurēt to, kuram dalībniekam jāveic darbība.</span><span class="sxs-lookup"><span data-stu-id="85307-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="85307-133">Dalībnieku tipi</span><span class="sxs-lookup"><span data-stu-id="85307-133">Types of participants</span></span>
----------------------

<span data-ttu-id="85307-134">Apstiprināšanas darbību varat piešķirt šādām dalībnieku grupām.</span><span class="sxs-lookup"><span data-stu-id="85307-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="85307-135">Lietotāju grupa</span><span class="sxs-lookup"><span data-stu-id="85307-135">User group</span></span>    | <span data-ttu-id="85307-136">Apraksts</span><span class="sxs-lookup"><span data-stu-id="85307-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="85307-137">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="85307-137">Participant</span></span>   | <span data-ttu-id="85307-138">Piešķiriet apstiprināšanas darbību kādas grupas vai lomas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="85307-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="85307-139">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="85307-139">Hierarchy</span></span>     | <span data-ttu-id="85307-140">Piešķiriet apstiprināšanas darbību lietotājiem noteiktā organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="85307-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="85307-141">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="85307-141">Workflow user</span></span> | <span data-ttu-id="85307-142">Piešķiriet apstiprināšanas darbību šīs darbplūsmas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="85307-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="85307-143">Rinda</span><span class="sxs-lookup"><span data-stu-id="85307-143">Queue</span></span>         | <span data-ttu-id="85307-144">Piešķiriet apstiprinājuma darbību darba vienumu rindai.</span><span class="sxs-lookup"><span data-stu-id="85307-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="85307-145">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="85307-145">User</span></span>          | <span data-ttu-id="85307-146">Piešķiriet apstiprināšanas darbību konkrētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="85307-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="85307-147">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="85307-147">See also</span></span>
--------

[<span data-ttu-id="85307-148">Biznesa procesu darbplūsmu definēšana pirkšanas pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="85307-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="85307-149">Pirkšanas pieprasījuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="85307-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




