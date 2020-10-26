---
title: 'Izveidot aktivitāšu relāciju: Pēctecīga aktivitāte'
description: Racionālās ražošanas plūsmas aktivitāšu plūsma tiek dokumentēta, izmantojot aktivitāšu relācijas.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91e1535ab6b53ad60394967d0377606a0cd27d01
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983450"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="a81cb-103">Izveidot aktivitāšu relāciju: Pēctecīga aktivitāte</span><span class="sxs-lookup"><span data-stu-id="a81cb-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a81cb-104">Racionālās ražošanas plūsmas aktivitāšu plūsma tiek dokumentēta, izmantojot aktivitāšu relācijas.</span><span class="sxs-lookup"><span data-stu-id="a81cb-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="a81cb-105">Šajā ierakstā ir parādīts, kā izveidot aktivitāšu relācijas.</span><span class="sxs-lookup"><span data-stu-id="a81cb-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="a81cb-106">Priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="a81cb-106">Prerequisites:</span></span>

- <span data-ttu-id="a81cb-107">Ražošanas plūsma un versija melnraksta režīmā.</span><span class="sxs-lookup"><span data-stu-id="a81cb-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="a81cb-108">Divas aktivitātes, kuras seko viena otrai ražošanas plūsmā, ir izveidotas, bet nav saistītas.</span><span class="sxs-lookup"><span data-stu-id="a81cb-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="a81cb-109">Ražošanas plūsmas versijas atrašana</span><span class="sxs-lookup"><span data-stu-id="a81cb-109">Find the production flow version</span></span> 
1. <span data-ttu-id="a81cb-110">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="a81cb-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="a81cb-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a81cb-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a81cb-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a81cb-113">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a81cb-114">Sarakstā atlasiet melnraksta versiju.</span><span class="sxs-lookup"><span data-stu-id="a81cb-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="a81cb-115">Aktivitātes relācijas var pievienot gan melnraksta, gan aktīvām ražošanas plūsmas versijām.</span><span class="sxs-lookup"><span data-stu-id="a81cb-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="a81cb-116">Aktivitāšu pārskata atvēršana</span><span class="sxs-lookup"><span data-stu-id="a81cb-116">Open the activity overview</span></span>
1. <span data-ttu-id="a81cb-117">Noklikšķiniet uz Aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="a81cb-117">Click Activities.</span></span>
    * <span data-ttu-id="a81cb-118">Ievērojiet, ka formās tiek parādītas visas ražošanas plūsmas aktivitātes, kas piešķirtas Ražošanas plūsmu versijai, ar kuru strādājat.</span><span class="sxs-lookup"><span data-stu-id="a81cb-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="a81cb-119">Pēctecīgas aktivitātes pievienošana</span><span class="sxs-lookup"><span data-stu-id="a81cb-119">Add a Successor</span></span>
1. <span data-ttu-id="a81cb-120">Noklikšķiniet uz Pievienojiet pēctecīgu aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="a81cb-120">Click Add successor.</span></span>
2. <span data-ttu-id="a81cb-121">Laukā Aktivitāte noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a81cb-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a81cb-123">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a81cb-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a81cb-124">Atzīmējiet izvēles rūtiņu Ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="a81cb-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="a81cb-125">Laukā Ierobežojuma vērtība ievadiet vai atlasiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="a81cb-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="a81cb-126">Ierobežojuma laiks ir laiks, kas jāieplāno starp plānotām pirmstecīgas aktivitātes beigām (izpildes datumu un laiku) un plānoto pēctecīgas aktivitātes sākumu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="a81cb-127">Laukā Vienības ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a81cb-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="a81cb-128">Laukā Cikla laika koeficients ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a81cb-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="a81cb-129">Ja abas aktivitātes tiek veiktas vienā un tajā pašā izgatavošanas laikā, cikla laika koeficientam ir jābūt 1.</span><span class="sxs-lookup"><span data-stu-id="a81cb-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="a81cb-130">Ja pirmstecīgu aktivitāti veic ar dubultotu pēctecīgas aktivitātes ātrumu, koeficientam ir jābūt 2.</span><span class="sxs-lookup"><span data-stu-id="a81cb-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="a81cb-131">Cikla laiks koeficientus izmanto, lai aprēķinātu ražošanas plūsmas aktivitāšu atsevišķos cikla laikus.</span><span class="sxs-lookup"><span data-stu-id="a81cb-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="a81cb-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a81cb-132">Click OK.</span></span>
10. <span data-ttu-id="a81cb-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-133">Close the page.</span></span>
11. <span data-ttu-id="a81cb-134">Noklikšķiniet uz cilnes GridPanel.</span><span class="sxs-lookup"><span data-stu-id="a81cb-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="a81cb-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-135">Close the page.</span></span>
13. <span data-ttu-id="a81cb-136">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="a81cb-136">Refresh the page.</span></span>

