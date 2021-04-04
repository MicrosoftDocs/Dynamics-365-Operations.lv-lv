---
title: Deleģēt darba vienumus darbplūsmā
description: Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 054e183374d2b24f38b0f90ff90acfeeca013861
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560559"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="7e1e6-103">Darba vienumu deleģēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="7e1e6-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="7e1e6-104">Manuāla darba vienības deleģēšana</span><span class="sxs-lookup"><span data-stu-id="7e1e6-104">Manually delegate a work item</span></span>

<span data-ttu-id="7e1e6-105">Lai deleģētu atsevišķu darba vienību, atlasiet opciju **Deleģēt** izvēlnē **Darbplūsma** un pēc tam ievadiet deleģējamo lietotāju kopā ar komentāru.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="7e1e6-106">Tādējādi darba vienība tiek atkārtoti piešķirta konkrētajam lietotājam, lai šis lietotājs varētu to pabeigt.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="7e1e6-107">Manuāli deleģēt vairākus darba vienumus</span><span class="sxs-lookup"><span data-stu-id="7e1e6-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="7e1e6-108">Vairākus darba vienumus var deleģēt kopā no lapas **Man piešķirtie darba vienumi**.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="7e1e6-109">Masveida deleģēšanai ir piemēroti šādi darbplūsmas tipi: Pirkšanas līguma apstiprināšanas darbplūsma, Pirkšanas pasūtījumu darbplūsma, Pirkšanas pieprasījuma pārskats un Kreditora rēķina darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="7e1e6-110">Līdzeklis **Deleģēt vairākus darba vienumus** ir atspējots pēc noklusējuma, un to var iespējot sadaļā **Darbvietas > Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="7e1e6-111">Sazinieties ar sistēmas administratoru, lai saņemtu palīdzību šī līdzekļa iespējošanā.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="7e1e6-112">Dodieties uz **Vispārīgi > Vispārīgi > Darba vienumi > Man piešķirtie darba vienumi**.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="7e1e6-113">Atlasiet darba vienumus, kas tiks deleģēti.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="7e1e6-114">Noklikšķiniet uz izvēlnes **Darba vienumu deleģēšana**.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="7e1e6-115">Laukā **Lietotājs** atlasiet lietotāju, kuram deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="7e1e6-116">Laukā **Komentārs** ievadiet paskaidrojošu komentāru, kāpēc deleģējat šos darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="7e1e6-117">Noklikšķiniet uz pogas **Deleģēt darba vienumus**, lai pabeigtu darba vienuma deleģēšanu.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="7e1e6-118">Automātiska darba vienību deleģēšana</span><span class="sxs-lookup"><span data-stu-id="7e1e6-118">Automatically delegate work items</span></span>

<span data-ttu-id="7e1e6-119">Ja plānojat atrasties ārpus biroja vai noteiktu laika periodu nevarēsiet rīkoties ar darba vienībām citu iemeslu dēļ, varat automātiski deleģēt jaunas darba vienības citiem lietotājiem, izmantojot lapu **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="7e1e6-120">Iestatīt automātisku deleģēšanu</span><span class="sxs-lookup"><span data-stu-id="7e1e6-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="7e1e6-121">Pārejiet uz sadaļu **Kopējs > Iestatīšana > Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="7e1e6-122">Noklikšķiniet uz cilnes **Darbplūsma**. Pārliecinieties, vai sadaļa Deleģēšana ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="7e1e6-123">Lai sistēmu konfigurētu automātiskai jūsu darba vienumu deleģēšanai citiem lietotājiem, ir jāizveido deleģēšanas kārtulas, kuras norāda, kad tiek deleģēti noteikta tipa darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="7e1e6-124">Lai izveidotu deleģēšanas kārtulu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="7e1e6-125">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-125">Click **Add**.</span></span>
4. <span data-ttu-id="7e1e6-126">Laukā **Tvērums** atlasiet opciju:</span><span class="sxs-lookup"><span data-stu-id="7e1e6-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="7e1e6-127">Viss — deleģēt visus jums piešķirtos uzdevumus vai darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="7e1e6-128">Modulis — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmas tipu.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="7e1e6-129">Ja atlasāt šo opciju, tad laukā **Nosaukums** ir jāatlasa darbplūsmas veids.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="7e1e6-130">Darbplūsma — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="7e1e6-131">Ja atlasāt šo opciju, tad laukā **Nosaukums** ir jāatlasa darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="7e1e6-132">Laukā **Nosaukums**:</span><span class="sxs-lookup"><span data-stu-id="7e1e6-132">In the **Name** field:</span></span>
    - <span data-ttu-id="7e1e6-133">Tvērumam **Modulis** atlasiet mērķa moduli.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="7e1e6-134">Tvērumam **Darbplūsma** atlasiet mērķa darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="7e1e6-135">Laukā **Pārstāvis** atlasiet lietotāju, kuram deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="7e1e6-136">Izmantojiet laukus **Sākuma datums/laiks** un **Beigu datums/laiks**, lai norādītu, kad vēlaties automātiski deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="7e1e6-137">Laukā **Sākuma datums/laiks** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="7e1e6-138">Laukā **Beigu datums/laiks** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="7e1e6-139">Atlasiet izvēles rūtiņu **Iespējots** deleģēšanas noteikumu aktivizēšanai.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="7e1e6-140">Laukā **Komentārs** ievadiet paskaidrojošu komentāru, kāpēc deleģējat šos darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="7e1e6-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]