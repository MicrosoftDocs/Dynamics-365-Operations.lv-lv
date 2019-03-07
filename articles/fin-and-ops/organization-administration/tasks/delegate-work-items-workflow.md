---
title: Deleģēt darba vienumus darbplūsmā
description: Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "346253"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="2ad58-103">Deleģēt darba vienumus darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="2ad58-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ad58-104">Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="2ad58-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="2ad58-105">Šī procedūra jums palīdz konfigurēt sistēmu, lai savus darba vienumus automātiski deleģētu citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="2ad58-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="2ad58-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="2ad58-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="2ad58-107">Iestatīt automātisku deleģēšanu</span><span class="sxs-lookup"><span data-stu-id="2ad58-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="2ad58-108">Dodieties uz Vispārīgi > Iestatīšana > Lietotāja opcijas.</span><span class="sxs-lookup"><span data-stu-id="2ad58-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="2ad58-109">Noklikšķiniet uz cilnes Darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="2ad58-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="2ad58-110">Pārliecinieties, ka sadaļa Deleģēšana ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="2ad58-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="2ad58-111">Lai sistēmu konfigurētu automātiskai jūsu darba vienumu deleģēšanai citiem lietotājiem, ir jāizveido deleģēšanas kārtulas, kuras norāda, kad tiek deleģēti noteikta tipa darba vienumi.</span><span class="sxs-lookup"><span data-stu-id="2ad58-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="2ad58-112">Lai izveidotu deleģēšanas kārtulu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="2ad58-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="2ad58-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2ad58-113">Click Add.</span></span>
4. <span data-ttu-id="2ad58-114">Laukā Tvērums atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="2ad58-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="2ad58-115">Viss — deleģēt visus jums piešķirtos uzdevumus vai darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2ad58-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="2ad58-116">Modulis — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmas tipu.</span><span class="sxs-lookup"><span data-stu-id="2ad58-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="2ad58-117">Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsmas tips.</span><span class="sxs-lookup"><span data-stu-id="2ad58-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="2ad58-118">Darbplūsma — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="2ad58-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="2ad58-119">Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="2ad58-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="2ad58-120">Laukā Deleģēt atlasiet lietotāju, kam deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2ad58-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="2ad58-121">Izmantojiet laukus Sākuma datums/laiks un Beigu datums/laiks, lai norādītu, kad vēlaties automātiski deleģēt darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2ad58-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="2ad58-122">Laukā Sākuma datums/laiks ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="2ad58-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="2ad58-123">Laukā Beigu datums/laiks ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="2ad58-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="2ad58-124">Atzīmējiet izvēles rūtiņu Iespējots, lai aktivizētu deleģēšanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="2ad58-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="2ad58-125">Ja vienumam Tvērums atlasāt vērtību Modulis, tad laukā Nosaukums ir jāatlasa šis modulis.</span><span class="sxs-lookup"><span data-stu-id="2ad58-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="2ad58-126">Ja vienumam Tvērums atlasāt vērtību Darbplūsma, tad laukā Nosaukums ir jāatlasa konkrētā deleģējamā darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="2ad58-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="2ad58-127">Laukā Komentārs ievadiet komentāru, kurā ir paskaidrots, kāpēc deleģējat šos darba vienumus.</span><span class="sxs-lookup"><span data-stu-id="2ad58-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

