---
title: Ierobežotā plāna ģenerēšana
description: Šajā tēmā paskaidrots, kā izveidot plānu, kurā ņemti vērā gan materiāla, gan noslodzes ierobežojumi.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808020"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="0070c-103">Ierobežotā plāna ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="0070c-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0070c-104">Šajā tēmā paskaidrots, kā izveidot plānu, kurā ņemti vērā gan materiāla, gan noslodzes ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="0070c-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="0070c-105">Šis plāns nodrošina, ka ražošana nesākas, pirms materiāli kļūst pieejami, un resursiem netiek pārsniegta rezervācija.</span><span class="sxs-lookup"><span data-stu-id="0070c-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="0070c-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="0070c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0070c-107">Šī procedūra ir paredzēta ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="0070c-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="0070c-108">Iestatīt ierobežotu plānu</span><span class="sxs-lookup"><span data-stu-id="0070c-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="0070c-109">Sākumlapā izvēlieties **Vispārējās plānošanas** darbvietu.</span><span class="sxs-lookup"><span data-stu-id="0070c-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="0070c-110">Izvēlieties **Galvenie plāni** saišu sarakstā darbvietas tālajā labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="0070c-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="0070c-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0070c-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="0070c-112">Piemērs: **StatisksPlāns**</span><span class="sxs-lookup"><span data-stu-id="0070c-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="0070c-113">Atlasiet **Jā** laukā **Galīgā noslodze**.</span><span class="sxs-lookup"><span data-stu-id="0070c-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="0070c-114">Laukā **Galīgās noslodzes robežas** ievadiet `30`.</span><span class="sxs-lookup"><span data-stu-id="0070c-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="0070c-115">Izvērsiet sadaļu **Laika robežas dienās**.</span><span class="sxs-lookup"><span data-stu-id="0070c-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="0070c-116">Atlasiet **Jā** laukā **Noslodze**.</span><span class="sxs-lookup"><span data-stu-id="0070c-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="0070c-117">Laukā **Noslodzes plānošanas laika robežas (dienas)** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="0070c-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="0070c-118">Piemērs: `60`</span><span class="sxs-lookup"><span data-stu-id="0070c-118">Example: `60`</span></span>  
9. <span data-ttu-id="0070c-119">Atlasiet **Jā** laukā **Aprēķinātie kavējumi**.</span><span class="sxs-lookup"><span data-stu-id="0070c-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="0070c-120">Laukā **Aprēķināt kavējumu laiku robežas (dienas)** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="0070c-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="0070c-121">Piemērs: `60`</span><span class="sxs-lookup"><span data-stu-id="0070c-121">Example: `60`</span></span> 
11. <span data-ttu-id="0070c-122">Izvērsiet sadaļu **Aprēķinātie kavējumi**.</span><span class="sxs-lookup"><span data-stu-id="0070c-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="0070c-123">Atlasiet **Jā** visos laukos **Pievienot aprēķināto kavējumu prasības datumam**.</span><span class="sxs-lookup"><span data-stu-id="0070c-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="0070c-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0070c-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="0070c-125">Ierobežota plāna izveide</span><span class="sxs-lookup"><span data-stu-id="0070c-125">Create a constrained plan</span></span>
1. <span data-ttu-id="0070c-126">Atlasiet **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="0070c-126">Select **Run**.</span></span>
2. <span data-ttu-id="0070c-127">Laukā **Vispārējais plāns** ievadiet vai atlasiet plānu, kam esat iestatījis ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="0070c-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="0070c-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0070c-128">Select **OK**.</span></span>
4. <span data-ttu-id="0070c-129">Atlasiet **Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="0070c-129">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]