---
title: Kanban procesa darbu izpilde
description: Šī procedūra fokusējas uz kanban procesa darbu izpildi.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9da49ae17d6c25166f6b0e05e3c45fc991c9a54d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994158"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="8c41d-103">Kanban procesa darbu izpilde</span><span class="sxs-lookup"><span data-stu-id="8c41d-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c41d-104">Šī procedūra fokusējas uz kanban procesa darbu izpildi.</span><span class="sxs-lookup"><span data-stu-id="8c41d-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="8c41d-105">Pirmais darbs tiek pabeigts ar paredzamo daudzumu un bez kļūdām.</span><span class="sxs-lookup"><span data-stu-id="8c41d-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="8c41d-106">Otrs darbs tiek pabeigts ar kļūdām.</span><span class="sxs-lookup"><span data-stu-id="8c41d-106">The second job is completed with errors.</span></span> <span data-ttu-id="8c41d-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="8c41d-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8c41d-108">Šī procedūra ir paredzēta mašīnas operatoram.</span><span class="sxs-lookup"><span data-stu-id="8c41d-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="8c41d-109">Atlasiet kanban darbu.</span><span class="sxs-lookup"><span data-stu-id="8c41d-109">Select a kanban job</span></span>
1. <span data-ttu-id="8c41d-110">Pārejiet uz sadaļu Ražošanas kontrole > Kanban > Kanban panelis procesa darbiem.</span><span class="sxs-lookup"><span data-stu-id="8c41d-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="8c41d-111">Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8c41d-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8c41d-112">Noklikšķiniet uz rindas ar resursu grupu 1250.</span><span class="sxs-lookup"><span data-stu-id="8c41d-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="8c41d-113">Šādi atfiltrēsiet darbu sarakstu, lai parādītu tikai darbus šūnai 1250.</span><span class="sxs-lookup"><span data-stu-id="8c41d-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="8c41d-114">Iezīmējiet rindu, kurā ir plānotā darba statuss.</span><span class="sxs-lookup"><span data-stu-id="8c41d-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="8c41d-115">Pabeidziet darbu ar paredzēto daudzumu</span><span class="sxs-lookup"><span data-stu-id="8c41d-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="8c41d-116">Izvērsiet vai sakļaujiet sadaļu Detalizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="8c41d-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="8c41d-117">Šajā sadaļā tiek parādīta svarīga informācija par kartes numuru, preces numuru, pasūtīto daudzumu un aktivitātes nosaukums.</span><span class="sxs-lookup"><span data-stu-id="8c41d-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="8c41d-118">Izvērsiet vai sakļaujiet sadaļu Ražošanas instrukcija.</span><span class="sxs-lookup"><span data-stu-id="8c41d-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="8c41d-119">Šajā sadaļā tiek parādītas ražošanas instrukcijas aktivitātei.</span><span class="sxs-lookup"><span data-stu-id="8c41d-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="8c41d-120">Instrukcijas var būt teksts, attēli, zīmējumi un citi dokumenti.</span><span class="sxs-lookup"><span data-stu-id="8c41d-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="8c41d-121">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="8c41d-121">Click Start.</span></span>
    * <span data-ttu-id="8c41d-122">Atlasiet darbu, kas nav pabeigts.</span><span class="sxs-lookup"><span data-stu-id="8c41d-122">Select a job that is not completed.</span></span> <span data-ttu-id="8c41d-123">Izmantojiet darba statusa lauka statusa ikonas, lai skatītu darba statusu.</span><span class="sxs-lookup"><span data-stu-id="8c41d-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="8c41d-124">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="8c41d-124">Click Complete.</span></span>
    * <span data-ttu-id="8c41d-125">Darbs ir pabeigts ar paredzamo kvalitāti.</span><span class="sxs-lookup"><span data-stu-id="8c41d-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="8c41d-126">Pabeidziet darbu ar kļūdām</span><span class="sxs-lookup"><span data-stu-id="8c41d-126">Complete a job with errors</span></span>
1. <span data-ttu-id="8c41d-127">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="8c41d-127">Click Start.</span></span>
    * <span data-ttu-id="8c41d-128">Kad darbs ir pabeigts, nākamais darbs sarakstā tiek atlasīts automātiski.</span><span class="sxs-lookup"><span data-stu-id="8c41d-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="8c41d-129">Šī iemesla dēļ nav nepieciešams atlasīt darbu, pirms noklikšķināt uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="8c41d-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="8c41d-130">Darbību rūtī noklikšķiniet uz Ražošana.</span><span class="sxs-lookup"><span data-stu-id="8c41d-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="8c41d-131">Noklikšķiniet uz Pabeigt (informācija).</span><span class="sxs-lookup"><span data-stu-id="8c41d-131">Click Complete (details).</span></span>
4. <span data-ttu-id="8c41d-132">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="8c41d-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8c41d-133">Ierakstiet skaitli laukā Kļūdu daudzums.</span><span class="sxs-lookup"><span data-stu-id="8c41d-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="8c41d-134">Laukā Derīgais daudzums ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8c41d-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="8c41d-135">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="8c41d-135">Click OK.</span></span>

