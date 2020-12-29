---
title: Kanban kārtulas izveide vairākām aktivitātēm
description: Šajā procedūrā ir parādīts, kā izveidot Kanban nosacījumu, kas ietver vairākas aktivitātes no ražošanas plūsmas.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68cac0f581e786cdb3801e03fb60db7bc05ffb2f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432497"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="88b45-103">Kanban kārtulas izveide vairākām aktivitātēm</span><span class="sxs-lookup"><span data-stu-id="88b45-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88b45-104">Šajā procedūrā ir parādīts, kā izveidot Kanban nosacījumu, kas ietver vairākas aktivitātes no ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="88b45-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="88b45-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="88b45-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="88b45-106">Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad viņi sagatavo jaunas vai modificētas preces ražošanu racionālā vidē.</span><span class="sxs-lookup"><span data-stu-id="88b45-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="88b45-107">Izveidot jaunu Kanban nosacījumu</span><span class="sxs-lookup"><span data-stu-id="88b45-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="88b45-108">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="88b45-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="88b45-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="88b45-109">Click New.</span></span>
3. <span data-ttu-id="88b45-110">Laukā Papildināšanas stratēģija atlasiet “Plānots”.</span><span class="sxs-lookup"><span data-stu-id="88b45-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="88b45-111">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="88b45-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="88b45-112">Atlasiet vērtību SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="88b45-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="88b45-113">Atzīmējiet izvēles rūtiņu Vairākas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="88b45-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="88b45-114">Mērķis ir Kanban nosacījumā iekļaut vairākas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="88b45-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="88b45-115">Ceļu ražošanas plūsmā jūs izvēlaties, kad atlasāt pēdējo plāna aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="88b45-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="88b45-116">Laukā Pēdējā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="88b45-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="88b45-117">Atlasiet vērtību SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="88b45-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="88b45-118">Pēc vērtības atlasīšanas automātiski tiek atvērta lapa.</span><span class="sxs-lookup"><span data-stu-id="88b45-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="88b45-119">Atlasiet Kanban plūsmu SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="88b45-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="88b45-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="88b45-120">Click OK.</span></span>  
7. <span data-ttu-id="88b45-121">Izvērsiet sadaļu Detalizēti.</span><span class="sxs-lookup"><span data-stu-id="88b45-121">Expand the Details section.</span></span>
8. <span data-ttu-id="88b45-122">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="88b45-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="88b45-123">Atlasiet krājumu L0006.</span><span class="sxs-lookup"><span data-stu-id="88b45-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="88b45-124">Izveidot Kanban un skatīt darbus</span><span class="sxs-lookup"><span data-stu-id="88b45-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="88b45-125">Izvērsiet sadaļu Vairāki Kanban.</span><span class="sxs-lookup"><span data-stu-id="88b45-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="88b45-126">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="88b45-126">Click Add.</span></span>
3. <span data-ttu-id="88b45-127">Laukā Jaunu Kanban skaits ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="88b45-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="88b45-128">Šādi tiks izveidots viens Kanban.</span><span class="sxs-lookup"><span data-stu-id="88b45-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="88b45-129">Iestatiet vērtību 3 laikā Preču daudzums.</span><span class="sxs-lookup"><span data-stu-id="88b45-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="88b45-130">Kanban apstrādās 3 preces.</span><span class="sxs-lookup"><span data-stu-id="88b45-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="88b45-131">Laukā Izpildes datums/laiks ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="88b45-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="88b45-132">Varat ievadīt Šodien.</span><span class="sxs-lookup"><span data-stu-id="88b45-132">You can enter Today.</span></span>  
6. <span data-ttu-id="88b45-133">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="88b45-133">Click Create.</span></span>
7. <span data-ttu-id="88b45-134">Noklikšķiniet uz Detaļas.</span><span class="sxs-lookup"><span data-stu-id="88b45-134">Click Details.</span></span>
    * <span data-ttu-id="88b45-135">Ievērojiet, ka šim Kanban ir divi procesa darbi no ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="88b45-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="88b45-136">Pirmais ir SpeakerAssemblyAndPolish, un otrais ir SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="88b45-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="88b45-137">Šis ir pēdējais solis!</span><span class="sxs-lookup"><span data-stu-id="88b45-137">This is the last step!</span></span>  

