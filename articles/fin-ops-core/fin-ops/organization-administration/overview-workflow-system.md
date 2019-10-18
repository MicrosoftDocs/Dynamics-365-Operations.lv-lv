---
title: Darbplūsmu sistēmas apskats
description: Šajā tēmā ir aprakstīta darbplūsmu sistēma.
author: sericks007
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
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190009"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="eef6a-103">Darbplūsmu sistēmas apskats</span><span class="sxs-lookup"><span data-stu-id="eef6a-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eef6a-104">Šajā tēmā ir aprakstīta darbplūsmu sistēma.</span><span class="sxs-lookup"><span data-stu-id="eef6a-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="eef6a-105">Kas ir darbplūsma?</span><span class="sxs-lookup"><span data-stu-id="eef6a-105">What is workflow?</span></span>

<span data-ttu-id="eef6a-106">Terminu *darbplūsma* var definēt divos veidos — gan kā sistēmu, gan kā biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="eef6a-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="eef6a-107">Darbplūsma ir sistēma</span><span class="sxs-lookup"><span data-stu-id="eef6a-107">Workflow is a system</span></span>

<span data-ttu-id="eef6a-108">Darbplūsma ir sistēma, kas darbojas serverī Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="eef6a-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="eef6a-109">Darbplūsmas sistēma nodrošina funkcionalitāti, kuru jūs varat izmantot, lai izveidotu individuālas darbplūsmas vai biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="eef6a-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="eef6a-110">Darbplūsma ir biznesa process</span><span class="sxs-lookup"><span data-stu-id="eef6a-110">Workflow is a business process</span></span>

<span data-ttu-id="eef6a-111">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="eef6a-111">A workflow represents a business process.</span></span> <span data-ttu-id="eef6a-112">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kam ir jāpabeidz uzdevums, jāpieņem lēmums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="eef6a-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="eef6a-113">Piemēram, nākamajā attēlā ir redzama darbplūsma izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="eef6a-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Darbplūsma ar lietotājiem piešķirtajiem elementiem](./media/workflow_user.gif)

<span data-ttu-id="eef6a-115">Lai varētu labāk izprast šo darbplūsmu, pieņemsim, ka Sems iesniedz izdevumu pārskatu par summu USD 7000.</span><span class="sxs-lookup"><span data-stu-id="eef6a-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="eef6a-116">Šajā gadījumā Jānim ir jāpārskata kvītis, kuras viņam ir maršrutējis Sems.</span><span class="sxs-lookup"><span data-stu-id="eef6a-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="eef6a-117">Pēc tam Kārlim un Santai ir jāapstiprina izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="eef6a-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="eef6a-118">Tagad pieņemsim, ka Sems iesniedz izdevumu pārskatu par 11 000 USD.</span><span class="sxs-lookup"><span data-stu-id="eef6a-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="eef6a-119">Šajā scenārijā Jānim ir jāpārskata kvītis un Kārlim, Sanitai un Annai ir jāapstiprina izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="eef6a-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="eef6a-120">Darbplūsmas sistēmas izmantošanas priekšrocības</span><span class="sxs-lookup"><span data-stu-id="eef6a-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="eef6a-121">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="eef6a-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="eef6a-122">**Saskaņoti procesi** — varat definēt noteiktu dokumentu, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="eef6a-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="eef6a-123">Izmantojot darbplūsmas sistēmu, jūs nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti saskaņotā un efektīvā veidā.</span><span class="sxs-lookup"><span data-stu-id="eef6a-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="eef6a-124">**Procesa pārskatāmība** — varat izsekot noteiktu darbplūsmas instanču statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="eef6a-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="eef6a-125">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="eef6a-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="eef6a-126">**Centralizēts darbu saraksts** — lietotāji var apskatīt centralizētu darbu sarakstu, kurā ir iekļauti tiem piešķirtie darbplūsmas uzdevumi un apstiprinājumi.</span><span class="sxs-lookup"><span data-stu-id="eef6a-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="eef6a-127">Darbplūsmas saturs</span><span class="sxs-lookup"><span data-stu-id="eef6a-127">Workflow content</span></span>

+ [<span data-ttu-id="eef6a-128">Darbplūsmas arhitektūra</span><span class="sxs-lookup"><span data-stu-id="eef6a-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="eef6a-129">Darbplūsmas elementi</span><span class="sxs-lookup"><span data-stu-id="eef6a-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="eef6a-130">Darbplūsmas darbības</span><span class="sxs-lookup"><span data-stu-id="eef6a-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="eef6a-131">Izveidot darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="eef6a-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="eef6a-132">Konfigurēt darbplūsmas rekvizītus</span><span class="sxs-lookup"><span data-stu-id="eef6a-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="eef6a-133">Konfigurēt manuālu uzdevumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="eef6a-134">Konfigurēt automatizētu uzdevumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="eef6a-135">Konfigurēt apstiprināšanas procesu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="eef6a-136">Konfigurēt apstiprināšanas darbību darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="eef6a-137">Konfigurēt manuālu lēmumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="eef6a-138">Konfigurēt nosacījuma lēmumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="eef6a-139">Konfigurēt paralēlu aktivitāti darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="eef6a-140">Konfigurēt paralēlu zaru darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="eef6a-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="eef6a-141">Konfigurēt dokumenta rindas darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="eef6a-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="eef6a-142">Bieži uzdotie jautājumi par darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="eef6a-142">Workflow FAQ</span></span>](workflow-FAQ.md)
