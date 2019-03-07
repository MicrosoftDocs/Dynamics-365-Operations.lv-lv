---
title: Vispārējās plānošanas izpildes pārraudzība
description: Ražošanas plānotājs vēlas redzēt, vai tiek īstenota vispārējās plānošanas izpilde.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "367505"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="7bf22-103">Vispārējās plānošanas izpildes pārraudzība</span><span class="sxs-lookup"><span data-stu-id="7bf22-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7bf22-104">Ražošanas plānotājs vēlas redzēt, vai tiek īstenota vispārējās plānošanas izpilde.</span><span class="sxs-lookup"><span data-stu-id="7bf22-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="7bf22-105">Lai izpildītu šo procedūru, izmantojiet demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="7bf22-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="7bf22-106">Vispārējās plānošanas izpildīšana</span><span class="sxs-lookup"><span data-stu-id="7bf22-106">Run master planning</span></span>
1. <span data-ttu-id="7bf22-107">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="7bf22-107">Click Master planning.</span></span>
    * <span data-ttu-id="7bf22-108">Tas ir atrodams noklusējuma informācijas panelī.</span><span class="sxs-lookup"><span data-stu-id="7bf22-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="7bf22-109">Laukā Plāns ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7bf22-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="7bf22-110">Piemērs: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="7bf22-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="7bf22-111">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="7bf22-111">Click Run.</span></span>
4. <span data-ttu-id="7bf22-112">Laukā Izsekot apstrādes laiku atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="7bf22-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="7bf22-113">Ja lauks jau ir atlasīts, izlaidiet šo soli.</span><span class="sxs-lookup"><span data-stu-id="7bf22-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="7bf22-114">Laukā Pavedienu skaits ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="7bf22-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="7bf22-115">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="7bf22-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="7bf22-116">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="7bf22-116">Click Filter.</span></span>
8. <span data-ttu-id="7bf22-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="7bf22-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7bf22-118">Atzīmējiet rindu, kurā Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="7bf22-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="7bf22-119">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7bf22-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="7bf22-120">Piemērs: T0001</span><span class="sxs-lookup"><span data-stu-id="7bf22-120">Example: T0001</span></span>  
10. <span data-ttu-id="7bf22-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7bf22-121">Click OK.</span></span>
11. <span data-ttu-id="7bf22-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7bf22-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="7bf22-123">Pārraudzīt vispārējās plānošanas izpildi</span><span class="sxs-lookup"><span data-stu-id="7bf22-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="7bf22-124">Noklikšķiniet uz Vēsture.</span><span class="sxs-lookup"><span data-stu-id="7bf22-124">Click History.</span></span>
2. <span data-ttu-id="7bf22-125">Noklikšķiniet uz Uzziņas.</span><span class="sxs-lookup"><span data-stu-id="7bf22-125">Click Inquiries.</span></span>
3. <span data-ttu-id="7bf22-126">Noklikšķiniet uz Apstrādes uzdevuma ilgums.</span><span class="sxs-lookup"><span data-stu-id="7bf22-126">Click Process task duration.</span></span>
4. <span data-ttu-id="7bf22-127">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7bf22-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7bf22-128">Katram krājumam var iegūt pārskatu par to, cik ilgs laiks bija nepieciešams, lai veiktu katru plānošanas soli.</span><span class="sxs-lookup"><span data-stu-id="7bf22-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

