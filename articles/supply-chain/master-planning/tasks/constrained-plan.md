---
title: Ierobežotā plāna ģenerēšana
description: Šajā tēmā paskaidrots, kā izveidot plānu, kurā ņemti vērā gan materiāla, gan noslodzes ierobežojumi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b5d37de41fe68845cec3f2285aed2484ac117aa
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867177"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="1c03a-103">Ierobežotā plāna ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="1c03a-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c03a-104">Šajā tēmā paskaidrots, kā izveidot plānu, kurā ņemti vērā gan materiāla, gan noslodzes ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="1c03a-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="1c03a-105">Šis plāns nodrošina, ka ražošana nesākas, pirms materiāli kļūst pieejami, un resursiem netiek pārsniegta rezervācija.</span><span class="sxs-lookup"><span data-stu-id="1c03a-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="1c03a-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="1c03a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1c03a-107">Šī procedūra ir paredzēta ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="1c03a-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="1c03a-108">Iestatīt ierobežotu plānu</span><span class="sxs-lookup"><span data-stu-id="1c03a-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="1c03a-109">Sākumlapā izvēlieties **Vispārējās plānošanas** darbvietu.</span><span class="sxs-lookup"><span data-stu-id="1c03a-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="1c03a-110">Izvēlieties **Galvenie plāni** saišu sarakstā darbvietas tālajā labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="1c03a-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="1c03a-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1c03a-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="1c03a-112">Piemērs: **StatisksPlāns**</span><span class="sxs-lookup"><span data-stu-id="1c03a-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="1c03a-113">Atlasiet **Jā** laukā **Galīgā noslodze**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="1c03a-114">Laukā **Galīgās noslodzes robežas** ievadiet `30`.</span><span class="sxs-lookup"><span data-stu-id="1c03a-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="1c03a-115">Izvērsiet sadaļu **Laika robežas dienās**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="1c03a-116">Atlasiet **Jā** laukā **Noslodze**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="1c03a-117">Laukā **Noslodzes plānošanas laika robežas (dienas)** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="1c03a-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="1c03a-118">Piemērs: `60`</span><span class="sxs-lookup"><span data-stu-id="1c03a-118">Example: `60`</span></span>  
9. <span data-ttu-id="1c03a-119">Atlasiet **Jā** laukā **Aprēķinātie kavējumi**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="1c03a-120">Laukā **Aprēķināt kavējumu laiku robežas (dienas)** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="1c03a-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="1c03a-121">Piemērs: `60`</span><span class="sxs-lookup"><span data-stu-id="1c03a-121">Example: `60`</span></span> 
11. <span data-ttu-id="1c03a-122">Izvērsiet sadaļu **Aprēķinātie kavējumi**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="1c03a-123">Atlasiet **Jā** visos laukos **Pievienot aprēķināto kavējumu prasības datumam**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="1c03a-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1c03a-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="1c03a-125">Ierobežota plāna izveide</span><span class="sxs-lookup"><span data-stu-id="1c03a-125">Create a constrained plan</span></span>
1. <span data-ttu-id="1c03a-126">Atlasiet **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-126">Select **Run**.</span></span>
2. <span data-ttu-id="1c03a-127">Laukā **Vispārējais plāns** ievadiet vai atlasiet plānu, kam esat iestatījis ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="1c03a-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="1c03a-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-128">Select **OK**.</span></span>
4. <span data-ttu-id="1c03a-129">Atlasiet **Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="1c03a-129">Select **Planned orders**.</span></span>

