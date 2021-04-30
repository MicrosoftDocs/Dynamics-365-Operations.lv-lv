---
title: Sagādes un avotu darbplūsmas
description: Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu. Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 126e9969f312ff7f6a6c64b733708754e7659214
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909235"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="26cbc-104">Sagādes un avotu darbplūsmas</span><span class="sxs-lookup"><span data-stu-id="26cbc-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26cbc-105">Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu.</span><span class="sxs-lookup"><span data-stu-id="26cbc-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="26cbc-106">Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="26cbc-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="26cbc-107">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="26cbc-107">A workflow represents a business process.</span></span> <span data-ttu-id="26cbc-108">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kuram ir jāpabeidz uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="26cbc-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="26cbc-109">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="26cbc-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="26cbc-110">**Saskaņoti procesi** — varat definēt noteiktu dokumentiem, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="26cbc-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="26cbc-111">Izmantojot darbplūsmas sistēmu, varat nodrošināt saskaņotu un efektīvu dokumentu apstrādes un apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="26cbc-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="26cbc-112">**Procesa pārskatāmība** — varat sekot līdzi noteiktas darbplūsmas instances statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="26cbc-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="26cbc-113">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="26cbc-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="26cbc-114">**Centralizēts darbu saraksts** — lietotāji var skatīt centralizētu darbu sarakstu, lai skatītu darbplūsmas uzdevumus un apstiprinājumus, kas viņiem ir piešķirti visās darbplūsmās, kurās viņi piedalās.</span><span class="sxs-lookup"><span data-stu-id="26cbc-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="26cbc-115">Šī funkcija ir pieejama lapā Darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="26cbc-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="26cbc-116">Izveidojamo darbplūsmu veidi</span><span class="sxs-lookup"><span data-stu-id="26cbc-116">The types of workflows that you can create</span></span>

<span data-ttu-id="26cbc-117">Sagādei un avotiem ir pieejami šādi darbplūsmu veidi.</span><span class="sxs-lookup"><span data-stu-id="26cbc-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="26cbc-118">tips</span><span class="sxs-lookup"><span data-stu-id="26cbc-118">Type</span></span> | <span data-ttu-id="26cbc-119">Šī tipa lietošanas nolūks</span><span class="sxs-lookup"><span data-stu-id="26cbc-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="26cbc-120">Pirkšanas pieprasījuma pārskats</span><span class="sxs-lookup"><span data-stu-id="26cbc-120">Purchase requisition review</span></span> | <span data-ttu-id="26cbc-121">Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="26cbc-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="26cbc-122">Pirkšanas pieprasījuma rindas pārskats</span><span class="sxs-lookup"><span data-stu-id="26cbc-122">Purchase requisition line review</span></span> | <span data-ttu-id="26cbc-123">Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumu rindām.</span><span class="sxs-lookup"><span data-stu-id="26cbc-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="26cbc-124">Pirkšanas pasūtījuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="26cbc-124">Purchase order workflow</span></span> | <span data-ttu-id="26cbc-125">Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="26cbc-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="26cbc-126">Pirkšanas pasūtījuma rindas darbplūsma</span><span class="sxs-lookup"><span data-stu-id="26cbc-126">Purchase order line workflow</span></span> | <span data-ttu-id="26cbc-127">Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas rindas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="26cbc-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="26cbc-128">Kreditoru pievienošanas pieteikumu darbplūsma</span><span class="sxs-lookup"><span data-stu-id="26cbc-128">Vendor add application workflow</span></span> | <span data-ttu-id="26cbc-129">Izveidot pārskatīšanas un apstiprināšanas darbplūsmas jaunu piegādātāju pievienošanai, izmantojot piegādātāju pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="26cbc-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="26cbc-130">Kad jūs pievienojat jaunu darbplūsmu, jūs varētu redzēt arī šādas novecojušas darbplūsmas, kas uzskaitītas dialoglodziņā **Izveidot darbplūsmu**.</span><span class="sxs-lookup"><span data-stu-id="26cbc-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="26cbc-131">Tie ir saistīti ar *kvīts apstiprinājuma* funkcionalitāti, kas bija pieejams [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), bet tagad ir novecojis.</span><span class="sxs-lookup"><span data-stu-id="26cbc-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="26cbc-132">Šīs darbplūsmas pašlaik netiek atbalstītas.</span><span class="sxs-lookup"><span data-stu-id="26cbc-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="26cbc-133">Piegādes izpildes datuma paziņojuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="26cbc-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="26cbc-134">Rēķina saņemšanas paziņojuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="26cbc-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="26cbc-135">Produktu ieejas plūsma neizdevās paziņojumu darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="26cbc-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="26cbc-136">Neapstiprinātu produktu ieejas plūsmas noraidīšanas paziņojuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="26cbc-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="26cbc-137">Darbplūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="26cbc-137">Creating a workflow</span></span>

<span data-ttu-id="26cbc-138">Lai izveidotu darbplūsmu, pārejiet uz sadaļu Sagāde un avoti &gt; Iestatījumi &gt; Sagādes un avotu darbplūsmas un izveidojiet jaunu darbplūsmu, atlasot izveidojamās darbplūsmas veidu.</span><span class="sxs-lookup"><span data-stu-id="26cbc-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="26cbc-139">Darbplūsmas audeklā varat vilkt darbplūsmas elementus uz veidotāju un saistīt elementus plūsmā.</span><span class="sxs-lookup"><span data-stu-id="26cbc-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="26cbc-140">Darbplūsmas elementi ir jākonfigurē.</span><span class="sxs-lookup"><span data-stu-id="26cbc-140">The workflow elements should be configured.</span></span> <span data-ttu-id="26cbc-141">Apstiprinājumam un uzdevuma darbplūsmas elementiem var konfigurēt to, kuram dalībniekam jāveic darbība.</span><span class="sxs-lookup"><span data-stu-id="26cbc-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="26cbc-142">Dalībnieku tipi</span><span class="sxs-lookup"><span data-stu-id="26cbc-142">Types of participants</span></span>

<span data-ttu-id="26cbc-143">Apstiprināšanas darbību varat piešķirt šādām dalībnieku grupām.</span><span class="sxs-lookup"><span data-stu-id="26cbc-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="26cbc-144">Lietotāju grupa</span><span class="sxs-lookup"><span data-stu-id="26cbc-144">User group</span></span> | <span data-ttu-id="26cbc-145">Apraksts</span><span class="sxs-lookup"><span data-stu-id="26cbc-145">Description</span></span> |
|---|---|
| <span data-ttu-id="26cbc-146">Dalībnieks</span><span class="sxs-lookup"><span data-stu-id="26cbc-146">Participant</span></span> | <span data-ttu-id="26cbc-147">Piešķiriet apstiprināšanas darbību kādas grupas vai lomas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="26cbc-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="26cbc-148">Hierarhija</span><span class="sxs-lookup"><span data-stu-id="26cbc-148">Hierarchy</span></span> | <span data-ttu-id="26cbc-149">Piešķiriet apstiprināšanas darbību lietotājiem noteiktā organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="26cbc-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="26cbc-150">Darbplūsmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="26cbc-150">Workflow user</span></span> | <span data-ttu-id="26cbc-151">Piešķiriet apstiprināšanas darbību šīs darbplūsmas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="26cbc-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="26cbc-152">Rinda</span><span class="sxs-lookup"><span data-stu-id="26cbc-152">Queue</span></span> | <span data-ttu-id="26cbc-153">Piešķiriet apstiprinājuma darbību darba vienumu rindai.</span><span class="sxs-lookup"><span data-stu-id="26cbc-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="26cbc-154">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="26cbc-154">User</span></span> | <span data-ttu-id="26cbc-155">Piešķiriet apstiprināšanas darbību konkrētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="26cbc-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="26cbc-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="26cbc-156">Additional resources</span></span>

- [<span data-ttu-id="26cbc-157">Biznesa procesu darbplūsmu definēšana pirkšanas pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="26cbc-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="26cbc-158">Pirkšanas pieprasījuma darbplūsma</span><span class="sxs-lookup"><span data-stu-id="26cbc-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="26cbc-159">Kreditoru pievienošana</span><span class="sxs-lookup"><span data-stu-id="26cbc-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]