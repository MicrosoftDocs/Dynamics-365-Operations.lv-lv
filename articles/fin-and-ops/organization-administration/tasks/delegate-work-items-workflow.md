---
title: Deleģēt darba vienumus darbplūsmā
description: Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916419"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="526e6-103">Darba vienumu deleģēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="526e6-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="526e6-104">Manuāla darba vienības deleģēšana</span><span class="sxs-lookup"><span data-stu-id="526e6-104">Manually delegate a work item</span></span>

<span data-ttu-id="526e6-105">Lai deleģētu atsevišķu darba vienību, atlasiet opciju **Deleģēt** izvēlnē **Darbplūsma** un pēc tam ievadiet deleģējamo lietotāju kopā ar komentāru.</span><span class="sxs-lookup"><span data-stu-id="526e6-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="526e6-106">Tādējādi darba vienība tiek atkārtoti piešķirta konkrētajam lietotājam, lai šis lietotājs varētu to pabeigt.</span><span class="sxs-lookup"><span data-stu-id="526e6-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="526e6-107">Automātiska darba vienību deleģēšana</span><span class="sxs-lookup"><span data-stu-id="526e6-107">Automatically delegate work items</span></span>

<span data-ttu-id="526e6-108">Ja plānojat atrasties ārpus biroja vai noteiktu laika periodu nevarēsiet rīkoties ar darba vienībām citu iemeslu dēļ, varat automātiski deleģēt jaunas darba vienības citiem lietotājiem, izmantojot lapu **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="526e6-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="526e6-109">Iestatīt automātisku deleģēšanu</span><span class="sxs-lookup"><span data-stu-id="526e6-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="526e6-110">Pārejiet uz sadaļu **Kopējs > Iestatīšana > Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="526e6-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="526e6-111">Noklikšķiniet uz cilnes **Darbplūsma**. Pārliecinieties, vai sadaļa Deleģēšana ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="526e6-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="526e6-112">Lai sistēmu konfigurētu automātiskai jūsu darba vienumu deleģēšanai citiem lietotājiem, ir jāizveido deleģēšanas kārtulas, kuras norāda, kad tiek deleģēti noteikta tipa darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="526e6-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="526e6-113">Lai izveidotu deleģēšanas kārtulu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="526e6-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="526e6-114">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="526e6-114">Click **Add**.</span></span>
4. <span data-ttu-id="526e6-115">Atlasiet opciju laukā **Detalizācijas līmenis**.</span><span class="sxs-lookup"><span data-stu-id="526e6-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="526e6-116">Viss — deleģēt visus jums piešķirtos uzdevumus vai darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="526e6-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="526e6-117">Modulis — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmas tipu.</span><span class="sxs-lookup"><span data-stu-id="526e6-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="526e6-118">Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsmas tips.</span><span class="sxs-lookup"><span data-stu-id="526e6-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="526e6-119">Darbplūsma — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="526e6-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="526e6-120">Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="526e6-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="526e6-121">Laukā **Pārstāvis** atlasiet lietotāju, kuram deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="526e6-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="526e6-122">Izmantojiet laukus Sākuma datums/laiks un Beigu datums/laiks, lai norādītu, kad vēlaties automātiski deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="526e6-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="526e6-123">Laukā **Sākuma datums/laiks** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="526e6-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="526e6-124">Laukā **Beigu datums/laiks** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="526e6-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="526e6-125">Atlasiet izvēles rūtiņu **Iespējots** deleģēšanas noteikumu aktivizēšanai.</span><span class="sxs-lookup"><span data-stu-id="526e6-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="526e6-126">Atlasot **Moduli** kā Tvērumu, tālāk jums ir jāatlasa modulis laukā Nosaukums.</span><span class="sxs-lookup"><span data-stu-id="526e6-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="526e6-127">Atlasot **Darbplūsmu** kā Tvērumu, tālāk jums ir jāatlasa noteikta darbplūsma deleģēšanai laukā Nosaukums.</span><span class="sxs-lookup"><span data-stu-id="526e6-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="526e6-128">Laukā **Komentārs** ievadiet paskaidrojošu komentāru, kāpēc deleģējat šos darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="526e6-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

