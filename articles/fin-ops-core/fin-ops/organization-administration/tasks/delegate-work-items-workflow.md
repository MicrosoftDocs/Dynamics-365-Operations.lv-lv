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
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140586"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="2c9ba-103">Darba vienumu deleģēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="2c9ba-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="2c9ba-104">Manuāla darba vienības deleģēšana</span><span class="sxs-lookup"><span data-stu-id="2c9ba-104">Manually delegate a work item</span></span>

<span data-ttu-id="2c9ba-105">Lai deleģētu atsevišķu darba vienību, atlasiet opciju **Deleģēt** izvēlnē **Darbplūsma** un pēc tam ievadiet deleģējamo lietotāju kopā ar komentāru.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="2c9ba-106">Tādējādi darba vienība tiek atkārtoti piešķirta konkrētajam lietotājam, lai šis lietotājs varētu to pabeigt.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="2c9ba-107">Automātiska darba vienību deleģēšana</span><span class="sxs-lookup"><span data-stu-id="2c9ba-107">Automatically delegate work items</span></span>

<span data-ttu-id="2c9ba-108">Ja plānojat atrasties ārpus biroja vai noteiktu laika periodu nevarēsiet rīkoties ar darba vienībām citu iemeslu dēļ, varat automātiski deleģēt jaunas darba vienības citiem lietotājiem, izmantojot lapu **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="2c9ba-109">Iestatīt automātisku deleģēšanu</span><span class="sxs-lookup"><span data-stu-id="2c9ba-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="2c9ba-110">Pārejiet uz sadaļu **Kopējs > Iestatīšana > Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="2c9ba-111">Noklikšķiniet uz cilnes **Darbplūsma**. Pārliecinieties, vai sadaļa Deleģēšana ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="2c9ba-112">Lai sistēmu konfigurētu automātiskai jūsu darba vienumu deleģēšanai citiem lietotājiem, ir jāizveido deleģēšanas kārtulas, kuras norāda, kad tiek deleģēti noteikta tipa darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="2c9ba-113">Lai izveidotu deleģēšanas kārtulu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="2c9ba-114">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-114">Click **Add**.</span></span>
4. <span data-ttu-id="2c9ba-115">Atlasiet opciju laukā **Detalizācijas līmenis**.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="2c9ba-116">Viss — deleģēt visus jums piešķirtos uzdevumus vai darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="2c9ba-117">Modulis — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmas tipu.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="2c9ba-118">Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsmas tips.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="2c9ba-119">Darbplūsma — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="2c9ba-120">Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="2c9ba-121">Laukā **Pārstāvis** atlasiet lietotāju, kuram deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="2c9ba-122">Izmantojiet laukus Sākuma datums/laiks un Beigu datums/laiks, lai norādītu, kad vēlaties automātiski deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="2c9ba-123">Laukā **Sākuma datums/laiks** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="2c9ba-124">Laukā **Beigu datums/laiks** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="2c9ba-125">Atlasiet izvēles rūtiņu **Iespējots** deleģēšanas noteikumu aktivizēšanai.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="2c9ba-126">Atlasot **Moduli** kā Tvērumu, tālāk jums ir jāatlasa modulis laukā Nosaukums.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="2c9ba-127">Atlasot **Darbplūsmu** kā Tvērumu, tālāk jums ir jāatlasa noteikta darbplūsma deleģēšanai laukā Nosaukums.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="2c9ba-128">Laukā **Komentārs** ievadiet paskaidrojošu komentāru, kāpēc deleģējat šos darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2c9ba-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

