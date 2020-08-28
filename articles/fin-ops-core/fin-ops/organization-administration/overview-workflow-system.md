---
title: Darbplūsmu sistēmas apskats
description: Šajā tēmā ir aprakstīta darbplūsmu sistēma.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068f464fe5385486827b2f904114eb663e08b2e8
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697973"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="d1c2c-103">Darbplūsmu sistēmas apskats</span><span class="sxs-lookup"><span data-stu-id="d1c2c-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1c2c-104">Šajā tēmā ir aprakstīta darbplūsmu sistēma.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="d1c2c-105">Kas ir darbplūsma?</span><span class="sxs-lookup"><span data-stu-id="d1c2c-105">What is workflow?</span></span>

<span data-ttu-id="d1c2c-106">Terminu *darbplūsma* var definēt divos veidos — gan kā sistēmu, gan kā biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="d1c2c-107">Darbplūsma ir sistēma</span><span class="sxs-lookup"><span data-stu-id="d1c2c-107">Workflow is a system</span></span>

<span data-ttu-id="d1c2c-108">Darbplūsma ir sistēma, kas darbojas serverī Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="d1c2c-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="d1c2c-109">Darbplūsmas sistēma nodrošina funkcionalitāti, kuru jūs varat izmantot, lai izveidotu individuālas darbplūsmas vai biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="d1c2c-110">Darbplūsma ir biznesa process</span><span class="sxs-lookup"><span data-stu-id="d1c2c-110">Workflow is a business process</span></span>

<span data-ttu-id="d1c2c-111">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-111">A workflow represents a business process.</span></span> <span data-ttu-id="d1c2c-112">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kam ir jāpabeidz uzdevums, jāpieņem lēmums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="d1c2c-113">Piemēram, nākamajā attēlā ir redzama darbplūsma izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Darbplūsma ar lietotājiem piešķirtajiem elementiem](./media/workflow_user.gif)

<span data-ttu-id="d1c2c-115">Lai varētu labāk izprast šo darbplūsmu, pieņemsim, ka Sems iesniedz izdevumu pārskatu par summu USD 7000.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="d1c2c-116">Šajā gadījumā Jānim ir jāpārskata kvītis, kuras viņam ir maršrutējis Sems.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="d1c2c-117">Pēc tam Kārlim un Santai ir jāapstiprina izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="d1c2c-118">Tagad pieņemsim, ka Sems iesniedz izdevumu pārskatu par 11 000 USD.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="d1c2c-119">Šajā scenārijā Jānim ir jāpārskata kvītis un Kārlim, Sanitai un Annai ir jāapstiprina izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="d1c2c-120">Darbplūsmas sistēmas izmantošanas priekšrocības</span><span class="sxs-lookup"><span data-stu-id="d1c2c-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="d1c2c-121">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="d1c2c-122">**Saskaņoti procesi** — varat definēt noteiktu dokumentu, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="d1c2c-123">Izmantojot darbplūsmas sistēmu, jūs nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti saskaņotā un efektīvā veidā.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="d1c2c-124">**Procesa pārskatāmība** — varat izsekot noteiktu darbplūsmas instanču statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="d1c2c-125">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="d1c2c-126">**Centralizēts darbu saraksts** — lietotāji var apskatīt centralizētu darbu sarakstu, kurā ir iekļauti tiem piešķirtie darbplūsmas uzdevumi un apstiprinājumi.</span><span class="sxs-lookup"><span data-stu-id="d1c2c-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="d1c2c-127">Darbplūsmas saturs</span><span class="sxs-lookup"><span data-stu-id="d1c2c-127">Workflow content</span></span>

+ [<span data-ttu-id="d1c2c-128">Darbplūsmas sistēmas arhitektūra</span><span class="sxs-lookup"><span data-stu-id="d1c2c-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="d1c2c-129">Darbplūsmas elementi</span><span class="sxs-lookup"><span data-stu-id="d1c2c-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="d1c2c-130">Darbības darbplūsmas apstiprināšanas procesos</span><span class="sxs-lookup"><span data-stu-id="d1c2c-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="d1c2c-131">Izveidot darbplūsmu pārskatu</span><span class="sxs-lookup"><span data-stu-id="d1c2c-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="d1c2c-132">Konfigurēt darbplūsmas rekvizītus</span><span class="sxs-lookup"><span data-stu-id="d1c2c-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="d1c2c-133">Manuālu uzdevumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="d1c2c-134">Automatizētu uzdevumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="d1c2c-135">Apstiprināšanas procesu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="d1c2c-136">Apstiprināšanas darbību konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="d1c2c-137">Manuālu lēmumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="d1c2c-138">Nosacījuma lēmumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="d1c2c-139">Paralēlu aktivitāšu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="d1c2c-140">Paralēlu zaru konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="d1c2c-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="d1c2c-141">Konfigurēt dokumenta rindas darbplūsmas</span><span class="sxs-lookup"><span data-stu-id="d1c2c-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="d1c2c-142">Bieži uzdotie jautājumi par darbplūsmām</span><span class="sxs-lookup"><span data-stu-id="d1c2c-142">Workflow FAQ</span></span>](workflow-FAQ.md)
