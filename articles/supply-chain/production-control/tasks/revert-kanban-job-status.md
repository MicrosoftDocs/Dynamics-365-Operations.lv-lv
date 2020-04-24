---
title: Atjaunot Kanban darba statusu
description: Šajā procedūrā aprakstīts nepareiza Kanban darba statusa atgriešanas process.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adf65175669d4cd5ec4cb431a7e1436ea3da83ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210513"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="d707a-103">Atjaunot Kanban darba statusu</span><span class="sxs-lookup"><span data-stu-id="d707a-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d707a-104">Šajā procedūrā aprakstīts nepareiza Kanban darba statusa atgriešanas process.</span><span class="sxs-lookup"><span data-stu-id="d707a-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="d707a-105">Tas ir noderīgi, ja datoru ievades operators kļūdas dēļ atjaunina nepareizu darbu vai iestata nepareizu statusu.</span><span class="sxs-lookup"><span data-stu-id="d707a-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="d707a-106">Šajā procedūrā Kanban darbs kļūdas pēc tika reģistrēts kā sagatavots, un tā statuss tiek atgriezts.</span><span class="sxs-lookup"><span data-stu-id="d707a-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="d707a-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="d707a-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d707a-108">Šī procedūra ir paredzēta veikala vadītājam vai datu ievades operatoram, kurš strādā Lean manufacturing uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="d707a-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="d707a-109">Apstrādes ziņojumu dēļa atvēršana darba šūnai</span><span class="sxs-lookup"><span data-stu-id="d707a-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="d707a-110">Dodieties uz procesa darbu Kanban paneli.</span><span class="sxs-lookup"><span data-stu-id="d707a-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="d707a-111">Laukā Darba šūna ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d707a-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="d707a-112">Atlasiet darba šūnu 1260.</span><span class="sxs-lookup"><span data-stu-id="d707a-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="d707a-113">Kanban darba sagatavošana</span><span class="sxs-lookup"><span data-stu-id="d707a-113">Prepare kanban job</span></span>
1. <span data-ttu-id="d707a-114">Noklikšķiniet uz Sagatavot.</span><span class="sxs-lookup"><span data-stu-id="d707a-114">Click Prepare.</span></span>
    * <span data-ttu-id="d707a-115">Ja vienums Sagatavot ir pelēkots un tādēļ nav aktīvs, pārliecinieties, vai atlasītā Kanban darba statuss ir Plānots, par ko norāda tukša Kanban ikona.</span><span class="sxs-lookup"><span data-stu-id="d707a-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="d707a-116">Ja sagatavošana neizdevās, pārliecinieties, vai ir pieejami visi izdošanas saraksta materiāli.</span><span class="sxs-lookup"><span data-stu-id="d707a-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="d707a-117">Sarakstā atlasiet sagatavoto darbu.</span><span class="sxs-lookup"><span data-stu-id="d707a-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="d707a-118">Atlasiet pirmo darbu, ko tikko sagatavojāt.</span><span class="sxs-lookup"><span data-stu-id="d707a-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="d707a-119">Ņemiet vērā! Darba statuss ir Sagatavots, par ko norāda trīsstūris Kanban ikonas iekšpusē.</span><span class="sxs-lookup"><span data-stu-id="d707a-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="d707a-120">Sagatavota Kanban darba statusa atgriešana</span><span class="sxs-lookup"><span data-stu-id="d707a-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="d707a-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d707a-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d707a-122">Atlasiet pirmo darbu, kas tika sagatavots.</span><span class="sxs-lookup"><span data-stu-id="d707a-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="d707a-123">Darbību rūtī noklikšķiniet uz Ražošana.</span><span class="sxs-lookup"><span data-stu-id="d707a-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="d707a-124">Noklikšķiniet uz Atgriezt statusu.</span><span class="sxs-lookup"><span data-stu-id="d707a-124">Click Revert status.</span></span>
    * <span data-ttu-id="d707a-125">Var izmantot alternatīvu Kanban nosacījumu, ja ir spēkā tālāk minētie nosacījumi. - Abiem nosacījumiem ir vienāda papildināšanas stratēģija.</span><span class="sxs-lookup"><span data-stu-id="d707a-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="d707a-126">- Abiem nosacījumiem ir vienāda ražošanas plūsmas versija.</span><span class="sxs-lookup"><span data-stu-id="d707a-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="d707a-127">- Abiem nosacījumiem tiek piegādāta vienāda preces.</span><span class="sxs-lookup"><span data-stu-id="d707a-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="d707a-128">- Abiem nosacījumiem jābūt vienādām visām pakārtotajām darbībām, kas ir konfigurētas Kanban nosacījumu pēdējai aktivitātei.</span><span class="sxs-lookup"><span data-stu-id="d707a-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="d707a-129">- Abiem nosacījumiem jābūt konfigurētām vienādām piegādātā krājuma dimensijām.</span><span class="sxs-lookup"><span data-stu-id="d707a-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="d707a-130">- Materiālu apstrādes vienības statusam jābūt Nav piešķirts.</span><span class="sxs-lookup"><span data-stu-id="d707a-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="d707a-131">- Notikuma Kanban darbu konfigurācijai jābūt vienādai.</span><span class="sxs-lookup"><span data-stu-id="d707a-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="d707a-132">Nodrošiniet, ka jaunais statuss ir Plānots.</span><span class="sxs-lookup"><span data-stu-id="d707a-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="d707a-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d707a-133">Click OK.</span></span>
5. <span data-ttu-id="d707a-134">Sarakstā noņemiet atzīmi no atlasītās rindas.</span><span class="sxs-lookup"><span data-stu-id="d707a-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="d707a-135">Atlasiet vienu darbu.</span><span class="sxs-lookup"><span data-stu-id="d707a-135">Select the same job.</span></span>  
    * <span data-ttu-id="d707a-136">Ņemiet vērā! Kanban darba statuss tiek atgriezts uz Plānots, par ko norāda tukša Kanban ikona.</span><span class="sxs-lookup"><span data-stu-id="d707a-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

