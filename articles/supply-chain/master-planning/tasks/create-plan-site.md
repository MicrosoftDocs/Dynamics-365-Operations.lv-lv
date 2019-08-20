---
title: Plāna izveide vietai
description: Ražošanas plānotājs aprēķina materiālu un noslodzes prasības noteikta krājuma ražošanai.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: daa185864052849b2c78d975a7eb02e9697cb618
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845178"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="60361-103">Plāna izveide vietai</span><span class="sxs-lookup"><span data-stu-id="60361-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60361-104">Ražošanas plānotājs aprēķina materiālu un noslodzes prasības noteikta krājuma ražošanai.</span><span class="sxs-lookup"><span data-stu-id="60361-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="60361-105">Kad ir izveidoti avotu ieteikumi, viņš atrod pasūtījumus tajā vietā, kurai viņš plānošanas un apstiprina pasūtījumus, sākot no steidzamajiem.</span><span class="sxs-lookup"><span data-stu-id="60361-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="60361-106">Vissteidzamākie pasūtījumi ir tie, kurus nepieciešams apstiprināt pašreizējā datumā.</span><span class="sxs-lookup"><span data-stu-id="60361-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="60361-107">Lai veiktu šos uzdevumus, izmantojiet demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="60361-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="60361-108">Izveidot materiālu un noslodzes plānu krājumam</span><span class="sxs-lookup"><span data-stu-id="60361-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="60361-109">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="60361-109">Click Master planning.</span></span>
    * <span data-ttu-id="60361-110">Jums ir jāpāriet uz noklusējuma informācijas paneli.</span><span class="sxs-lookup"><span data-stu-id="60361-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="60361-111">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="60361-111">Click Run.</span></span>
3. <span data-ttu-id="60361-112">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="60361-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="60361-113">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="60361-113">Click Filter.</span></span>
5. <span data-ttu-id="60361-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="60361-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="60361-115">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="60361-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="60361-116">Piemērs: D0001</span><span class="sxs-lookup"><span data-stu-id="60361-116">Example: D0001</span></span>  
7. <span data-ttu-id="60361-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60361-117">Click OK.</span></span>
8. <span data-ttu-id="60361-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60361-118">Click OK.</span></span>
    * <span data-ttu-id="60361-119">Tas var aizņemt dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="60361-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="60361-120">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="60361-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="60361-121">Norādīt steidzami plānotos pasūtījumus krājumam</span><span class="sxs-lookup"><span data-stu-id="60361-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="60361-122">Atveriet kolonnas filtru Krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="60361-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="60361-123">Lietojiet filtru laukam “Krājuma kods” ar vērtību “D0001”, izmantojot filtra operatoru “sākas ar”.</span><span class="sxs-lookup"><span data-stu-id="60361-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="60361-124">Atveriet kolonnas filtru Pasūtījuma datums.</span><span class="sxs-lookup"><span data-stu-id="60361-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="60361-125">Lietojiet filtru laukā “Pasūtījuma datums” ar pašreizējā datuma vērtību, izmantojot filtra operatoru “ir precīzi”.</span><span class="sxs-lookup"><span data-stu-id="60361-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="60361-126">Apstiprināt visus steidzamos pasūtījumus krājumam</span><span class="sxs-lookup"><span data-stu-id="60361-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="60361-127">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="60361-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="60361-128">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="60361-128">Click Firm.</span></span>
3. <span data-ttu-id="60361-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60361-129">Click OK.</span></span>

