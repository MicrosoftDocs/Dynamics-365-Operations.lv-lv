--- 
title: "Ierobežotā plāna ģenerēšana"
description: "Šajā procedūrā ir parādīts, kā izveidot plānu, kurš ņem vērā gan materiālu, gan noslodzes ierobežojumus."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="488e9-103">Ierobežotā plāna ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="488e9-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="488e9-104">Šajā procedūrā ir parādīts, kā izveidot plānu, kurš ņem vērā gan materiālu, gan noslodzes ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="488e9-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="488e9-105">Šis plāns nodrošina, ka ražošana nesākas, pirms materiāli kļūst pieejami, un resursiem netiek pārsniegta rezervācija.</span><span class="sxs-lookup"><span data-stu-id="488e9-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="488e9-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="488e9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="488e9-107">Šī procedūra ir paredzēta ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="488e9-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="488e9-108">Iestatīt ierobežotu plānu</span><span class="sxs-lookup"><span data-stu-id="488e9-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="488e9-109">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="488e9-109">Click Master planning.</span></span>
2. <span data-ttu-id="488e9-110">Noklikšķiniet uz Vispārējie plāni.</span><span class="sxs-lookup"><span data-stu-id="488e9-110">Click Master plans.</span></span>
3. <span data-ttu-id="488e9-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="488e9-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="488e9-112">Piemērs: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="488e9-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="488e9-113">Laukā Ierobežota noslodze atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="488e9-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="488e9-114">Laukā Ierobežotās noslodzes periods ievadiet “30”.</span><span class="sxs-lookup"><span data-stu-id="488e9-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="488e9-115">Izvērsiet sadaļu Periodi dienās.</span><span class="sxs-lookup"><span data-stu-id="488e9-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="488e9-116">Laukā Noslodze atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="488e9-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="488e9-117">Laukā Noslodzes plānošanas periods (dienās) ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="488e9-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="488e9-118">Piemērs: 60</span><span class="sxs-lookup"><span data-stu-id="488e9-118">Example: 60</span></span>  
9. <span data-ttu-id="488e9-119">Laukā Aprēķinātās aizkaves atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="488e9-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="488e9-120">Laukā Aprēķināt aizkaves periodu (dienās) ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="488e9-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="488e9-121">Piemērs: 60</span><span class="sxs-lookup"><span data-stu-id="488e9-121">Example: 60</span></span>  
11. <span data-ttu-id="488e9-122">Izvērsiet sadaļu Aprēķinātās aizkaves.</span><span class="sxs-lookup"><span data-stu-id="488e9-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="488e9-123">Laukā Pieprasījuma datumam pieskaitīt aprēķināto aizkavi atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="488e9-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="488e9-124">Laukā Pieprasījuma datumam pieskaitīt aprēķināto aizkavi atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="488e9-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="488e9-125">Laukā Pieprasījuma datumam pieskaitīt aprēķināto aizkavi atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="488e9-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="488e9-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="488e9-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="488e9-127">Ierobežota plāna izveide</span><span class="sxs-lookup"><span data-stu-id="488e9-127">Create a constrained plan</span></span>
1. <span data-ttu-id="488e9-128">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="488e9-128">Click Run.</span></span>
2. <span data-ttu-id="488e9-129">Laukā Vispārējais plāns ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="488e9-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="488e9-130">Atlasiet plānu, kuram esat iestatījis ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="488e9-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="488e9-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="488e9-131">Click OK.</span></span>
    * <span data-ttu-id="488e9-132">Tas var aizņemt kādu laiku.</span><span class="sxs-lookup"><span data-stu-id="488e9-132">This may take a while.</span></span>  
4. <span data-ttu-id="488e9-133">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="488e9-133">Click Planned orders.</span></span>


