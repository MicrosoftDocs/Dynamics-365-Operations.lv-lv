---
title: Darbplūsmas sistēma
description: Šajā tēmā ir aprakstīta darbplūsmu sistēma programmā Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
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
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/01/2019
ms.locfileid: "773092"
---
# <a name="workflow-system"></a><span data-ttu-id="6fb99-103">Darbplūsmas sistēma</span><span class="sxs-lookup"><span data-stu-id="6fb99-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fb99-104">Šajā tēmā ir aprakstīta darbplūsmu sistēma programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6fb99-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="6fb99-105">Kas ir darbplūsma?</span><span class="sxs-lookup"><span data-stu-id="6fb99-105">What is workflow?</span></span>

<span data-ttu-id="6fb99-106">Terminu *darbplūsma* var definēt divos veidos — gan kā sistēmu, gan kā biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="6fb99-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="6fb99-107">Darbplūsma ir sistēma</span><span class="sxs-lookup"><span data-stu-id="6fb99-107">Workflow is a system</span></span>

<span data-ttu-id="6fb99-108">Darbplūsma ir sistēma, kas tiek instalēta kopā ar programmatūru Finance and Operations un darbojas serverī Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="6fb99-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="6fb99-109">Darbplūsmas sistēma nodrošina funkcionalitāti, kuru jūs varat izmantot, lai izveidotu individuālas darbplūsmas vai biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="6fb99-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="6fb99-110">Darbplūsma ir biznesa process</span><span class="sxs-lookup"><span data-stu-id="6fb99-110">Workflow is a business process</span></span>

<span data-ttu-id="6fb99-111">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="6fb99-111">A workflow represents a business process.</span></span> <span data-ttu-id="6fb99-112">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kam ir jāpabeidz uzdevums, jāpieņem lēmums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="6fb99-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="6fb99-113">Piemēram, nākamajā attēlā ir redzama darbplūsma izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="6fb99-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Darbplūsma ar lietotājiem piešķirtajiem elementiem](./media/workflow_user.gif)

<span data-ttu-id="6fb99-115">Lai varētu labāk izprast šo darbplūsmu, pieņemsim, ka Sems iesniedz izdevumu pārskatu par summu USD 7000.</span><span class="sxs-lookup"><span data-stu-id="6fb99-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="6fb99-116">Šajā gadījumā Jānim ir jāpārskata kvītis, kuras viņam ir maršrutējis Sems.</span><span class="sxs-lookup"><span data-stu-id="6fb99-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="6fb99-117">Pēc tam Kārlim un Santai ir jāapstiprina izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="6fb99-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="6fb99-118">Tagad pieņemsim, ka Sems iesniedz izdevumu pārskatu par 11 000 USD.</span><span class="sxs-lookup"><span data-stu-id="6fb99-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="6fb99-119">Šajā scenārijā Jānim ir jāpārskata kvītis un Kārlim, Sanitai un Annai ir jāapstiprina izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="6fb99-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="6fb99-120">Darbplūsmas sistēmas izmantošanas priekšrocības</span><span class="sxs-lookup"><span data-stu-id="6fb99-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="6fb99-121">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="6fb99-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="6fb99-122">**Saskaņoti procesi** — varat definēt noteiktu dokumentu, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="6fb99-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="6fb99-123">Izmantojot darbplūsmas sistēmu, jūs nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti saskaņotā un efektīvā veidā.</span><span class="sxs-lookup"><span data-stu-id="6fb99-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="6fb99-124">**Procesa pārskatāmība** — varat izsekot noteiktu darbplūsmas instanču statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="6fb99-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="6fb99-125">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="6fb99-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="6fb99-126">**Centralizēts darbu saraksts** — lietotāji var apskatīt centralizētu darbu sarakstu, kurā ir iekļauti tiem piešķirtie darbplūsmas uzdevumi un apstiprinājumi.</span><span class="sxs-lookup"><span data-stu-id="6fb99-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="6fb99-127">Darbplūsmas saturs</span><span class="sxs-lookup"><span data-stu-id="6fb99-127">Workflow content</span></span>

+ [<span data-ttu-id="6fb99-128">Darbplūsmas arhitektūra</span><span class="sxs-lookup"><span data-stu-id="6fb99-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="6fb99-129">Darbplūsmas elementi</span><span class="sxs-lookup"><span data-stu-id="6fb99-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="6fb99-130">Darbplūsmas darbības</span><span class="sxs-lookup"><span data-stu-id="6fb99-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="6fb99-131">Izveidot darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="6fb99-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="6fb99-132">Konfigurēt darbplūsmas rekvizītus</span><span class="sxs-lookup"><span data-stu-id="6fb99-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="6fb99-133">Konfigurēt manuālu uzdevumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="6fb99-134">Konfigurēt automatizētu uzdevumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="6fb99-135">Konfigurēt apstiprināšanas procesu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="6fb99-136">Konfigurēt apstiprināšanas darbību darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="6fb99-137">Konfigurēt manuālu lēmumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="6fb99-138">Konfigurēt nosacījuma lēmumu darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="6fb99-139">Konfigurēt paralēlu aktivitāti darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="6fb99-140">Konfigurēt paralēlu zaru darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="6fb99-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="6fb99-141">Konfigurēt dokumenta rindas darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="6fb99-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="6fb99-142">Bieži uzdotie jautājumi par darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="6fb99-142">Workflow FAQ</span></span>](workflow-FAQ.md)
