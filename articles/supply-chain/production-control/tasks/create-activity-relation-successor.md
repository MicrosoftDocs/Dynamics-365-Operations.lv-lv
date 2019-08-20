---
title: 'Izveidot aktivitāšu relāciju: Pēctecīga aktivitāte'
description: Racionālās ražošanas plūsmas aktivitāšu plūsma tiek dokumentēta, izmantojot aktivitāšu relācijas.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58e003c6521c4ef007b8e0e1e17d51715435e875
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838731"
---
# <a name="create-activity-relation-successor"></a><span data-ttu-id="d7638-103">Aktivitāšu relācija izveide: pēctecīga aktivitāte</span><span class="sxs-lookup"><span data-stu-id="d7638-103">Create activity relation: Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7638-104">Racionālās ražošanas plūsmas aktivitāšu plūsma tiek dokumentēta, izmantojot aktivitāšu relācijas.</span><span class="sxs-lookup"><span data-stu-id="d7638-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="d7638-105">Šajā ierakstā ir parādīts, kā izveidot aktivitāšu relācijas.</span><span class="sxs-lookup"><span data-stu-id="d7638-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="d7638-106">Priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="d7638-106">Prerequisites:</span></span>

- <span data-ttu-id="d7638-107">Ražošanas plūsma un versija melnraksta režīmā.</span><span class="sxs-lookup"><span data-stu-id="d7638-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="d7638-108">Divas aktivitātes, kuras seko viena otrai ražošanas plūsmā, ir izveidotas, bet nav saistītas.</span><span class="sxs-lookup"><span data-stu-id="d7638-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="d7638-109">Ražošanas plūsmas versijas atrašana</span><span class="sxs-lookup"><span data-stu-id="d7638-109">Find the production flow version</span></span> 
1. <span data-ttu-id="d7638-110">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="d7638-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d7638-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d7638-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d7638-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d7638-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d7638-113">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d7638-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d7638-114">Sarakstā atlasiet melnraksta versiju.</span><span class="sxs-lookup"><span data-stu-id="d7638-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="d7638-115">Aktivitātes relācijas var pievienot gan melnraksta, gan aktīvām ražošanas plūsmas versijām.</span><span class="sxs-lookup"><span data-stu-id="d7638-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="d7638-116">Aktivitāšu pārskata atvēršana</span><span class="sxs-lookup"><span data-stu-id="d7638-116">Open the activity overview</span></span>
1. <span data-ttu-id="d7638-117">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="d7638-117">Click Activities.</span></span>
    * <span data-ttu-id="d7638-118">Ievērojiet, ka formās tiek parādītas visas ražošanas plūsmas aktivitātes, kas piešķirtas Ražošanas plūsmu versijai, ar kuru strādājat.</span><span class="sxs-lookup"><span data-stu-id="d7638-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="d7638-119">Pēctecīgas aktivitātes pievienošana</span><span class="sxs-lookup"><span data-stu-id="d7638-119">Add a Successor</span></span>
1. <span data-ttu-id="d7638-120">Noklikšķiniet uz Pievienojiet pēctecīgu aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="d7638-120">Click Add successor.</span></span>
2. <span data-ttu-id="d7638-121">Laukā Aktivitāte noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d7638-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d7638-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d7638-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d7638-123">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d7638-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d7638-124">Atzīmējiet izvēles rūtiņu Ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="d7638-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="d7638-125">Laukā Ierobežojuma vērtība ievadiet vai atlasiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="d7638-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="d7638-126">Ierobežojuma laiks ir laiks, kas jāieplāno starp plānotām pirmstecīgas aktivitātes beigām (izpildes datumu un laiku) un plānoto pēctecīgas aktivitātes sākumu.</span><span class="sxs-lookup"><span data-stu-id="d7638-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="d7638-127">Laukā Vienības ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d7638-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="d7638-128">Laukā Cikla laika koeficients ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="d7638-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="d7638-129">Ja abas aktivitātes tiek veiktas vienā un tajā pašā izgatavošanas laikā, cikla laika koeficientam ir jābūt 1.</span><span class="sxs-lookup"><span data-stu-id="d7638-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="d7638-130">Ja pirmstecīgu aktivitāti veic ar dubultotu pēctecīgas aktivitātes ātrumu, koeficientam ir jābūt 2.</span><span class="sxs-lookup"><span data-stu-id="d7638-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="d7638-131">Cikla laiks koeficientus izmanto, lai aprēķinātu ražošanas plūsmas aktivitāšu atsevišķos cikla laikus.</span><span class="sxs-lookup"><span data-stu-id="d7638-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="d7638-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d7638-132">Click OK.</span></span>
10. <span data-ttu-id="d7638-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d7638-133">Close the page.</span></span>
11. <span data-ttu-id="d7638-134">Noklikšķiniet uz cilnes GridPanel.</span><span class="sxs-lookup"><span data-stu-id="d7638-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="d7638-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d7638-135">Close the page.</span></span>
13. <span data-ttu-id="d7638-136">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="d7638-136">Refresh the page.</span></span>

