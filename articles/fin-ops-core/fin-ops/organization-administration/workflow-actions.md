---
title: Darbības darbplūsmas apstiprināšanas procesos
description: Šajā rakstā ir paskaidrotas darbības, kuras darbplūsmas apstiprināšanas procesā var veikt katrs dalībnieks.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e6331746d2634a3686b0a7368d060d94567c4ff
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567960"
---
# <a name="actions-in-workflow-approval-processes"></a><span data-ttu-id="50dd5-103">Darbības darbplūsmas apstiprināšanas procesos</span><span class="sxs-lookup"><span data-stu-id="50dd5-103">Actions in workflow approval processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50dd5-104">Šajā rakstā ir paskaidrotas darbības, kuras darbplūsmas apstiprināšanas procesā var veikt katrs dalībnieks.</span><span class="sxs-lookup"><span data-stu-id="50dd5-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="50dd5-105">Darbplūsma var ietvert vairākas cilvēku grupas: iniciatoru, uzdevuma veicējus, lēmumu pieņēmējus un apstiprinātājus.</span><span class="sxs-lookup"><span data-stu-id="50dd5-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="50dd5-106">Piemēram, nākamajā izdevumu atskaites darbplūsmā Sems ir iniciators, rindas dalībnieki ir uzdevumu veicēji, Džons ir lēmumu pieņēmējs, bet Frenks, Sjū un Anna ir apstiprinātāji.</span><span class="sxs-lookup"><span data-stu-id="50dd5-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>

<span data-ttu-id="50dd5-107">[![Darbplūsma\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="50dd5-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span>

<span data-ttu-id="50dd5-108">Nākamajās sadaļās ir skaidrotas darbplūsmas darbības, ko var veikt katra no šīm grupām.</span><span class="sxs-lookup"><span data-stu-id="50dd5-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="50dd5-109">Darbības, ko var izpildīt iniciators</span><span class="sxs-lookup"><span data-stu-id="50dd5-109">Actions that an originator can perform</span></span>

<span data-ttu-id="50dd5-110">Iniciators uzsāk darbplūsmas instanci, iesniedzot dokumentu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="50dd5-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="50dd5-111">Piemēram, lai iesniegtu savu izdevumu atskaiti, Semam lapā **Izdevumu atskaite** ir jānoklikšķina uz pogas **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="50dd5-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="50dd5-112">Darbības, ko var izpildīt uzdevuma veicējs</span><span class="sxs-lookup"><span data-stu-id="50dd5-112">Actions that a task assignee can perform</span></span>

<span data-ttu-id="50dd5-113">Uzdevumu var piešķirt vairākām personām vai darba vienumu rindai, ko uzrauga vairākas personas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="50dd5-114">Taču uzdevumu izpildīt var tikai viena persona.</span><span class="sxs-lookup"><span data-stu-id="50dd5-114">However, only one person can complete a task.</span></span> <span data-ttu-id="50dd5-115">Piemēram, Sems ir iesniedzis izdevumu atskaiti un savas ienākošās plūsmas ir novirzījis pārskatīšanai uz savas organizācijas nodaļu Izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="50dd5-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span>

<span data-ttu-id="50dd5-116">Uzņēmuma Adventure Works nodaļas Izdevumu atskaites darbinieki pārrauga šo rindu.</span><span class="sxs-lookup"><span data-stu-id="50dd5-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="50dd5-117">Šīs nodaļas dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="50dd5-118">Tagad viņa var veikt kādu no šādām darbībām: pabeigt, noraidīt, deleģēt, pieprasīt izmaiņas, mainīt piešķiri vai izlaist.</span><span class="sxs-lookup"><span data-stu-id="50dd5-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span>

> [!NOTE]
> <span data-ttu-id="50dd5-119">Pieejamās darbības atšķiras atkarībā no tā, kā programmatūras izstrādātājs šo uzdevumu projektēja.</span><span class="sxs-lookup"><span data-stu-id="50dd5-119">The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="50dd5-120">Izpildīt</span><span class="sxs-lookup"><span data-stu-id="50dd5-120">Complete</span></span>

<span data-ttu-id="50dd5-121">Ja lietotājs pabeidz uzdevumu, apstrādei iesniegtais dokuments tiek piešķirts nākamajam lietotājam šajā darbplūsmā, ja nākamais lietotājs pastāv.</span><span class="sxs-lookup"><span data-stu-id="50dd5-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="50dd5-122">Ja papildu apstrāde nav nepieciešama, darbplūsmas process beidzas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-122">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="50dd5-123">Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="50dd5-124">Kad Jūlija pabeidz savu pārskatīšanu, dokuments tiek piešķirts Džonam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="50dd5-125">Noraidīt</span><span class="sxs-lookup"><span data-stu-id="50dd5-125">Reject</span></span>

<span data-ttu-id="50dd5-126">Kad lietotājs noraida dokumentu, darbplūsmas process beidzas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-126">When a user rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="50dd5-127">Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="50dd5-128">Ja Jūlija noraida izdevumu atskaiti, darbplūsmas process beidzas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-128">If Julie rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="50dd5-129">Pēc tam Sems šo izdevumu atskaiti var iesniegt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="50dd5-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="50dd5-130">Viņš pirms tam var veikt izmaiņas vai atkārtoti iesniegt sākotnējo versiju.</span><span class="sxs-lookup"><span data-stu-id="50dd5-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="50dd5-131">Ja Sems izdevumu atskaiti iesniedz atkārtoti, darbplūsmas process sākas ar manuālās pārskatīšanas uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="50dd5-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="50dd5-132">Deleģēt</span><span class="sxs-lookup"><span data-stu-id="50dd5-132">Delegate</span></span>

<span data-ttu-id="50dd5-133">Kad lietotājs deleģē uzdevumu, šis uzdevums tiek piešķirts citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-133">When a user delegates a task, the task is assigned to another user.</span></span>

<span data-ttu-id="50dd5-134">Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="50dd5-135">Jūlija šo uzdevumu deleģē savam asistentam Timam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-135">Julie delegates this task to Tim, who is her assistant.</span></span>

<span data-ttu-id="50dd5-136">Pēc tam Tims darbojas Jūlijas vārdā.</span><span class="sxs-lookup"><span data-stu-id="50dd5-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="50dd5-137">Tāpēc, kad Tims pabeidz savu pārskatīšanu, izdevumu atskaite tiek piešķirta Džonam, it kā šo uzdevumu būtu pildījusi Jūlija.</span><span class="sxs-lookup"><span data-stu-id="50dd5-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="50dd5-138">Pieprasīt izmaiņas</span><span class="sxs-lookup"><span data-stu-id="50dd5-138">Request change</span></span>

<span data-ttu-id="50dd5-139">Kad lietotājs pieprasa iesniegtā dokumenta izmaiņas, dokuments tiek nosūtīts atpakaļ iniciatoram.</span><span class="sxs-lookup"><span data-stu-id="50dd5-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span>

<span data-ttu-id="50dd5-140">Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="50dd5-141">Jūlija izdevumu atskaitē pamana dažas kļūdas un pieprasa izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="50dd5-142">Izdevumu atskaite tiek nosūtīta atpakaļ Semam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-142">The expense report is sent back to Sam.</span></span>

<span data-ttu-id="50dd5-143">Sems šo izdevumu atskaiti var iesniegt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="50dd5-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="50dd5-144">Viņš pirms tam var veikt pieprasītās izmaiņas vai atkārtoti iesniegt sākotnējo versiju.</span><span class="sxs-lookup"><span data-stu-id="50dd5-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="50dd5-145">Ja Sems šo izdevumu atskaiti iesniedz atkārtoti, kādam darba vienumu rindas dalībniekam šī izdevumu atskaite un ieejas plūsmas ir jāpārskata vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="50dd5-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="50dd5-146">Mainīt piešķiri</span><span class="sxs-lookup"><span data-stu-id="50dd5-146">Reassign</span></span>

<span data-ttu-id="50dd5-147">Darba vienumu rindas dalībnieki šajā rindā esošajiem dokumentiem var mainīt piešķiri uz citu rindu.</span><span class="sxs-lookup"><span data-stu-id="50dd5-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span>

<span data-ttu-id="50dd5-148">Piemēram, uzņēmuma Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija uzrauga šo rindu.</span><span class="sxs-lookup"><span data-stu-id="50dd5-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="50dd5-149">Lai palīdzētu sabalansēt darba slodzi, izdevumu atskaites un tajā iekļauto ieejas plūsmu piešķiri viņa var mainīt uz citu rindu.</span><span class="sxs-lookup"><span data-stu-id="50dd5-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="50dd5-150">Izlaist</span><span class="sxs-lookup"><span data-stu-id="50dd5-150">Release</span></span>

<span data-ttu-id="50dd5-151">Laiku pa laikam kāds darba vienumu rindas dalībnieks var pieņemt uzdevumu, bet pēc tam izlemt, ka viņš vai viņa šo uzdevumu nevar izpildīt līdz galam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="50dd5-152">Tādā gadījumā persona, kas pieņēma uzdevumu, šo dokumentu var izlaist atpakaļ uz darba vienumu rindu.</span><span class="sxs-lookup"><span data-stu-id="50dd5-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span>

<span data-ttu-id="50dd5-153">Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="50dd5-154">Ja Jūlija izlemj, ka viņa uzdevumu nevar pabeigt, viņa šo dokumentu var izlaist.</span><span class="sxs-lookup"><span data-stu-id="50dd5-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="50dd5-155">Izdevumu atskaite tiek atgriezta rindā, lai citi Adventure Works nodaļas Izdevumu atskaites dalībnieki šo uzdevumu varētu pabeigt.</span><span class="sxs-lookup"><span data-stu-id="50dd5-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="50dd5-156">Darbības, ko var izpildīt lēmumu pieņēmējs</span><span class="sxs-lookup"><span data-stu-id="50dd5-156">Actions that a decision maker can perform</span></span>

<span data-ttu-id="50dd5-157">Parasti dokuments tiek piešķirts lēmumu pieņēmējam, jo pastāv kāds jautājums, uz kuru lēmumu pieņēmējam ir jāatbild.</span><span class="sxs-lookup"><span data-stu-id="50dd5-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="50dd5-158">Atbilde uz šo jautājumu ir parasti ir **Jā** vai **Nē**, vai **Patiess** vai **Aplams**.</span><span class="sxs-lookup"><span data-stu-id="50dd5-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="50dd5-159">Ja lēmumu pieņēmējs neatlasa vienu no šiem izvēles variantiem, viņš vai viņa šo lēmumu var deleģēt.</span><span class="sxs-lookup"><span data-stu-id="50dd5-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="50dd5-160">\[1. izvēles variants\] vai \[2. izvēles variants\]</span><span class="sxs-lookup"><span data-stu-id="50dd5-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="50dd5-161">Lēmumu pieņēmējam ir jāatbild uz jautājumu, kas ir saistīts ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="50dd5-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="50dd5-162">Atbilde uz šo jautājumu ir parasti ir **Jā** vai **Nē**, vai **Patiess** vai **Aplams**.</span><span class="sxs-lookup"><span data-stu-id="50dd5-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="50dd5-163">Lēmumu pieņēmēja izvēlētā atbilde nosaka darbplūsmas zaru, kas tiek izmantots šī dokumenta apstrādāšanai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span>

<span data-ttu-id="50dd5-164">Piemēram, Sema izdevumu atskaite tiek piešķirta Džonam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="50dd5-165">Džonam ir jāizlemj, vai saistībā ar dokumentā ietverto informāciju ir nepieciešams zvanīt Sema vadītājam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="50dd5-166">Ja Džons izlemj, ka šāds zvans ir nepieciešams, izdevumu atskaite tiek piešķirta Ārijai, kurai pēc tam ir jāzvana Sema vadītājam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="50dd5-167">Ja Džons izlemj, ka zvans nav nepieciešams, izdevumu atskaite tiek piešķirta Frenkam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="50dd5-168">Deleģēt</span><span class="sxs-lookup"><span data-stu-id="50dd5-168">Delegate</span></span>

<span data-ttu-id="50dd5-169">Kad lēmumu pieņēmējs deleģē kādu lēmumu, dokuments tiek piešķirts citam lietotājam, kuram ir jāpieņem lēmums.</span><span class="sxs-lookup"><span data-stu-id="50dd5-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span>

<span data-ttu-id="50dd5-170">Piemēram, Sema izdevumu atskaite tiek piešķirta Džonam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="50dd5-171">Džons šo lēmumu deleģē savai asistentei Marijai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-171">John delegates the decision to Maria, who is his assistant.</span></span>

<span data-ttu-id="50dd5-172">Pēc tam Marija darbojas Džona vārdā.</span><span class="sxs-lookup"><span data-stu-id="50dd5-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="50dd5-173">Ja Marija izlemj, ka ir nepieciešams zvanīt Sema vadītājam, izdevumu atskaite tiek piešķirta Ārijai, kurai pēc tam ir jāzvana Sema vadītājam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="50dd5-174">Ja Marija izlemj, ka zvans nav nepieciešams, izdevumu atskaite tiek piešķirta Frenkam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="50dd5-175">Darbības, ko var izpildīt apstiprinātājs</span><span class="sxs-lookup"><span data-stu-id="50dd5-175">Actions that an approver can perform</span></span>

<span data-ttu-id="50dd5-176">Kad dokuments tiek piešķirts apstiprinātājam, apstiprinātājs var izpildīt vienu no šādām darbībām: apstiprināt, noraidīt, deleģēt vai pieprasīt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="50dd5-177">Apstiprināt</span><span class="sxs-lookup"><span data-stu-id="50dd5-177">Approve</span></span>

<span data-ttu-id="50dd5-178">Kad apstiprinātājs dokumentu apstiprina, šis dokuments tiek piešķirts nākamajam lietotājam darbplūsmā, ja pastāv nākamais lietotājs.</span><span class="sxs-lookup"><span data-stu-id="50dd5-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="50dd5-179">Ja papildu apstrāde nav nepieciešama, darbplūsmas process beidzas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-179">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="50dd5-180">Piemēram, Sems ir iesniedzis izdevumu atskaiti par 6000 USD, un šis dokuments tiek piešķirts Frenkam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="50dd5-181">Kad Frenks dokumentu apstiprina, tas tiek piešķirts Sjū apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="50dd5-182">Kad Sjū apstiprina šo izdevumu atskaiti, darbplūsmas process beidzas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="50dd5-183">Noraidīt</span><span class="sxs-lookup"><span data-stu-id="50dd5-183">Reject</span></span>

<span data-ttu-id="50dd5-184">Kad apstiprinātājs noraida dokumentu, darbplūsmas process beidzas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-184">When an approver rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="50dd5-185">Piemēram, Sems ir iesniedzis izdevumu atskaiti par 12 000 USD, un šis dokuments tiek piešķirts Sjū.</span><span class="sxs-lookup"><span data-stu-id="50dd5-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="50dd5-186">Ja Sjū noraida šo izdevumu atskaiti, darbplūsmas process beidzas.</span><span class="sxs-lookup"><span data-stu-id="50dd5-186">If Sue rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="50dd5-187">Sems šo izdevumu atskaiti var iesniegt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="50dd5-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="50dd5-188">Viņš pirms tam var veikt izmaiņas vai atkārtoti iesniegt izdevumu atskaites sākotnējo versiju.</span><span class="sxs-lookup"><span data-stu-id="50dd5-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="50dd5-189">Ja Sems atkārtoti iesniedz šo izdevumu atskaiti, tad darbplūsmas process sākas no apstiprināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="50dd5-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="50dd5-190">Deleģēt</span><span class="sxs-lookup"><span data-stu-id="50dd5-190">Delegate</span></span>

<span data-ttu-id="50dd5-191">Kad apstiprinātājs deleģē dokumentu, dokuments tiek piešķirts citam lietotājam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span>

<span data-ttu-id="50dd5-192">Piemēram, Sems ir iesniedzis izdevumu atskaiti par 12 000 USD, un šis dokuments tiek piešķirts Frenkam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="50dd5-193">Frenks deleģē izdevumu pārskatu Annai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-193">Frank delegates the expense report to Ann.</span></span>

<span data-ttu-id="50dd5-194">Pēc tam Anna darbojas Frenka vārdā.</span><span class="sxs-lookup"><span data-stu-id="50dd5-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="50dd5-195">Līdz ar to, kad Anna apstiprina šo dokumentu, tas tiek piešķirts Sjū apstiprināšanai, it kā to būtu apstiprinājis Frenks.</span><span class="sxs-lookup"><span data-stu-id="50dd5-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="50dd5-196">Kad Sjū apstiprina šo dokumentu, tas tiek nosūtīts Annai apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="50dd5-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="50dd5-197">Pieprasīt izmaiņas</span><span class="sxs-lookup"><span data-stu-id="50dd5-197">Request change</span></span>

<span data-ttu-id="50dd5-198">Kad apstiprinātājs pieprasa dokumenta izmaiņas, dokuments tiek nosūtīts atpakaļ iniciatoram.</span><span class="sxs-lookup"><span data-stu-id="50dd5-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span>

<span data-ttu-id="50dd5-199">Piemēram, Sems ir iesniedzis izdevumu atskaiti par 12 000 USD, un šis dokuments tiek piešķirts Sjū.</span><span class="sxs-lookup"><span data-stu-id="50dd5-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="50dd5-200">Ja Sjū pieprasa veikt izmaiņas, izdevumu atskaite tiek sūtīta atpakaļ Semam.</span><span class="sxs-lookup"><span data-stu-id="50dd5-200">If Sue requests a change, the expense report is sent back to Sam.</span></span>

<span data-ttu-id="50dd5-201">Sems šo izdevumu atskaiti var iesniegt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="50dd5-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="50dd5-202">Viņš pirms tam var veikt pieprasītās izmaiņas vai atkārtoti iesniegt izdevumu atskaites sākotnējo versiju.</span><span class="sxs-lookup"><span data-stu-id="50dd5-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="50dd5-203">Ja Sems izdevumu atskaiti iesniedz atkārtoti, tas tiek nosūtīts Frenkam apstiprināšanai, jo Frenks ir pirmais apstiprinātājs šajā apstiprināšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="50dd5-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]