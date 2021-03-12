---
title: Darbplūsmu pārskata izveide
description: Šajā tēmā ir paskaidrots, kā izveidot darbplūsmu.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: d1402019dbaaa60827499fcb6b93ee31440cfc3d
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797656"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="04309-103">Darbplūsmu pārskata izveide</span><span class="sxs-lookup"><span data-stu-id="04309-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04309-104">Šajā tēmā ir paskaidrots, kā izveidot darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="04309-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="04309-105">Atveriet darbplūsmas redaktoru</span><span class="sxs-lookup"><span data-stu-id="04309-105">Open the workflow editor</span></span>

<span data-ttu-id="04309-106">Tas, kāda veida darbplūsmas varat izveidot, ir atkarīgs no moduļa, kurā strādājat.</span><span class="sxs-lookup"><span data-stu-id="04309-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="04309-107">Izpildiet šeit aprakstītās darbības, lai atlasītu izveidojamo darbplūsmas tipu un atvērtu darbplūsmas redaktoru.</span><span class="sxs-lookup"><span data-stu-id="04309-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="04309-108">Atveriet moduli, kuram vēlaties izveidot jaunu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="04309-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="04309-109">Piemēram, lai izveidotu darbplūsmu pirkšanas pieprasījumiem, noklikšķiniet uz **Sagāde un avoti**.</span><span class="sxs-lookup"><span data-stu-id="04309-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="04309-110">Noklikšķiniet uz **Iestatīšana** &gt; **\[Moduļa nosaukums\] darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="04309-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="04309-111">Parādītās lapas darbību rūtī noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="04309-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="04309-112">Lapā **Izveidot darbplūsmu** atlasiet izveidojamās darbplūsmas tipu un pēc tam noklikšķiniet uz **Izveidot darbplūsmu**.</span><span class="sxs-lookup"><span data-stu-id="04309-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="04309-113">Tiek parādīts darbplūsmas redaktors.</span><span class="sxs-lookup"><span data-stu-id="04309-113">The workflow editor appears.</span></span> <span data-ttu-id="04309-114">Tagad varat izmantot tālāk aprakstītās procedūras, lai veidotu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="04309-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="04309-115">Velciet darbplūsmas elementus uz audekla</span><span class="sxs-lookup"><span data-stu-id="04309-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="04309-116">Darbplūsmas redaktora apgabals **Darbplūsmas elementi** satur elementus, ko varat pievienot savai darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="04309-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="04309-117">Lai elementus pievienotu darbplūsmai, ievelciet tos audeklā.</span><span class="sxs-lookup"><span data-stu-id="04309-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="04309-118">Savienojiet elementus</span><span class="sxs-lookup"><span data-stu-id="04309-118">Connect the elements</span></span>

<span data-ttu-id="04309-119">Lai savienotu vienu darbplūsmas elementu ar citu, turiet rādītāju virs elementa, līdz savienojuma punkti tiek parādīti.</span><span class="sxs-lookup"><span data-stu-id="04309-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="04309-120">Noklikšķiniet uz savienojuma punkta un velciet to uz citu elementu.</span><span class="sxs-lookup"><span data-stu-id="04309-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="04309-121">Pārliecinieties, ka tiek savienoti visi elementi.</span><span class="sxs-lookup"><span data-stu-id="04309-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="04309-122">Konfigurējiet darbplūsmas rekvizītus</span><span class="sxs-lookup"><span data-stu-id="04309-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="04309-123">Izpildiet šīs darbības, lai konfigurētu darbplūsmas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="04309-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="04309-124">Noklikšķiniet uz audekla, lai pārliecinātos, vai ir atlasīts darbplūsmas elements.</span><span class="sxs-lookup"><span data-stu-id="04309-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="04309-125">Noklikšķiniet uz **Rekvizīti**, lai darbplūsmai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="04309-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="04309-126">Izpildiet tēmā [Konfigurēt darbplūsmas rekvizītus](configure-workflow-properties.md) aprakstītās procedūras.</span><span class="sxs-lookup"><span data-stu-id="04309-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="04309-127">Konfigurējiet darbplūsmas elementus</span><span class="sxs-lookup"><span data-stu-id="04309-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="04309-128">Konfigurējiet katru uz audekla uzvilkto elementu.</span><span class="sxs-lookup"><span data-stu-id="04309-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="04309-129">Informāciju par to, kā konfigurēt katru darbplūsmas elementu, skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="04309-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="04309-130">Manuālu uzdevumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="04309-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="04309-131">Automatizētu uzdevumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="04309-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="04309-132">Apstiprināšanas procesu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="04309-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="04309-133">Apstiprināšanas darbību konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="04309-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="04309-134">Manuālu lēmumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="04309-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="04309-135">Nosacījuma lēmumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="04309-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="04309-136">Paralēlu zaru konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="04309-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="04309-137">Konfigurēt paralēlu zaru</span><span class="sxs-lookup"><span data-stu-id="04309-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="04309-138">Konfigurēt dokumenta rindas darbplūsmas</span><span class="sxs-lookup"><span data-stu-id="04309-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="04309-139">Atrisināt jebkuras kļūdas vai brīdinājumus</span><span class="sxs-lookup"><span data-stu-id="04309-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="04309-140">Darbplūsmas redaktora apakšā esošajā rūtī **Kļūdas un brīdinājumi** tiek rādīti darbplūsmai ģenerētie ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="04309-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="04309-141">Lai atrastu elementu, kurā radās kļūda vai brīdinājums, veiciet dubultklikšķi uz kļūdas vai brīdinājuma ziņojuma.</span><span class="sxs-lookup"><span data-stu-id="04309-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="04309-142">Lai darbplūsmu varētu padarīt par aktīvu, jums ir jāatrisina visas kļūdas un brīdinājumi.</span><span class="sxs-lookup"><span data-stu-id="04309-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="04309-143">Saglabājiet un aktivizējiet darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="04309-143">Save and activate the workflow</span></span>

<span data-ttu-id="04309-144">Kad esat gatavs saglabāt un aktivizēt darbplūsmu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="04309-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="04309-145">Noklikšķiniet uz **Saglabāt un aizvērt**, lai aizvērtu darbplūsmas redaktoru un atvērtu lapu **Saglabāt darbplūsmu**.</span><span class="sxs-lookup"><span data-stu-id="04309-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="04309-146">Ievadiet komentārus par darbplūsmā veiktajām izmaiņām un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="04309-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="04309-147">Ja visas kļūdas un brīdinājumi ir novērsti, tiek parādīta lapa **Aktivizēt darbplūsmu**.</span><span class="sxs-lookup"><span data-stu-id="04309-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="04309-148">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="04309-148">Select one of the following options:</span></span>

    - <span data-ttu-id="04309-149">Lai aktivizētu šo darbplūsmas versiju, noklikšķiniet uz **Aktivizēt jauno versiju**.</span><span class="sxs-lookup"><span data-stu-id="04309-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="04309-150">Kad darbplūsma ir aktīva, lietotāji var tajā iesniegt dokumentus apstrādei.</span><span class="sxs-lookup"><span data-stu-id="04309-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="04309-151">Ja nevēlaties aktivizēt šo versiju, noklikšķiniet uz **Neaktivizēt jauno versiju**.</span><span class="sxs-lookup"><span data-stu-id="04309-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="04309-152">Varat aktivizēt darbplūsmu vēlāk.</span><span class="sxs-lookup"><span data-stu-id="04309-152">You can activate the workflow later.</span></span>
