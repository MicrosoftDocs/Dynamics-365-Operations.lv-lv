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
ms.openlocfilehash: 13238818de10596de34eaf9d8cd7d55562a307eb
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150313"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="f3e79-103">Plāna izveide vietai</span><span class="sxs-lookup"><span data-stu-id="f3e79-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3e79-104">Ražošanas plānotājs aprēķina materiālu un noslodzes prasības noteikta krājuma ražošanai.</span><span class="sxs-lookup"><span data-stu-id="f3e79-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="f3e79-105">Kad ir izveidoti avotu ieteikumi, viņš atrod pasūtījumus tajā vietā, kurai viņš plānošanas un apstiprina pasūtījumus, sākot no steidzamajiem.</span><span class="sxs-lookup"><span data-stu-id="f3e79-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="f3e79-106">Vissteidzamākie pasūtījumi ir tie, kurus nepieciešams apstiprināt pašreizējā datumā.</span><span class="sxs-lookup"><span data-stu-id="f3e79-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="f3e79-107">Lai veiktu šos uzdevumus, izmantojiet demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="f3e79-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="f3e79-108">Izveidot materiālu un noslodzes plānu krājumam</span><span class="sxs-lookup"><span data-stu-id="f3e79-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="f3e79-109">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="f3e79-109">Click Master planning.</span></span>
    * <span data-ttu-id="f3e79-110">Jums ir jāpāriet uz noklusējuma informācijas paneli.</span><span class="sxs-lookup"><span data-stu-id="f3e79-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="f3e79-111">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="f3e79-111">Click Run.</span></span>
3. <span data-ttu-id="f3e79-112">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="f3e79-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="f3e79-113">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="f3e79-113">Click Filter.</span></span>
5. <span data-ttu-id="f3e79-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f3e79-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f3e79-115">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f3e79-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f3e79-116">Piemērs: D0001</span><span class="sxs-lookup"><span data-stu-id="f3e79-116">Example: D0001</span></span>  
7. <span data-ttu-id="f3e79-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3e79-117">Click OK.</span></span>
8. <span data-ttu-id="f3e79-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3e79-118">Click OK.</span></span>
    * <span data-ttu-id="f3e79-119">Tas var aizņemt dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="f3e79-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="f3e79-120">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="f3e79-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="f3e79-121">Norādīt steidzami plānotos pasūtījumus krājumam</span><span class="sxs-lookup"><span data-stu-id="f3e79-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="f3e79-122">Atveriet kolonnas filtru Krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="f3e79-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="f3e79-123">Lietojiet filtru laukam “Krājuma kods” ar vērtību “D0001”, izmantojot filtra operatoru “sākas ar”.</span><span class="sxs-lookup"><span data-stu-id="f3e79-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="f3e79-124">Atveriet kolonnas filtru Pasūtījuma datums.</span><span class="sxs-lookup"><span data-stu-id="f3e79-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="f3e79-125">Lietojiet filtru laukā “Pasūtījuma datums” ar pašreizējā datuma vērtību, izmantojot filtra operatoru “ir precīzi”.</span><span class="sxs-lookup"><span data-stu-id="f3e79-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="f3e79-126">Apstiprināt visus steidzamos pasūtījumus krājumam</span><span class="sxs-lookup"><span data-stu-id="f3e79-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="f3e79-127">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="f3e79-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="f3e79-128">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="f3e79-128">Click Firm.</span></span>
3. <span data-ttu-id="f3e79-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3e79-129">Click OK.</span></span>

