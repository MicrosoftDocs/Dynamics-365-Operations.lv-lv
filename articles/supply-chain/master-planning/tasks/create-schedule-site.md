---
title: Grafika izveide vietai
description: Šajā procedūrā ir parādīts, kā plānot ražošanas pasūtījumus, kas vēl nav sākti kādai vietai.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54bb2532534d5567239dad4fab7fd74fa50d2826
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "330061"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="ba630-103">Grafika izveide vietai</span><span class="sxs-lookup"><span data-stu-id="ba630-103">Create a schedule for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba630-104">Šajā procedūrā ir parādīts, kā plānot ražošanas pasūtījumus, kas vēl nav sākti kādai vietai.</span><span class="sxs-lookup"><span data-stu-id="ba630-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="ba630-105">Lai izpildītu šo procedūru, tiek izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="ba630-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="ba630-106">Identificēt ražošanas pasūtījumus, kas vēl nav sākti</span><span class="sxs-lookup"><span data-stu-id="ba630-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="ba630-107">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ba630-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="ba630-108">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="ba630-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ba630-109">Piemēram, filtrējiet pēc lauka Vieta, izmantojot vērtību “1”.</span><span class="sxs-lookup"><span data-stu-id="ba630-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="ba630-110">1 apzīmē vietu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="ba630-110">1 represents a site in USMF.</span></span> <span data-ttu-id="ba630-111">Ja neizmantojat uzņēmumu USMF, atlasiet vietu no sava uzņēmuma.</span><span class="sxs-lookup"><span data-stu-id="ba630-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="ba630-112">Atveriet statusa kolonnas filtru.</span><span class="sxs-lookup"><span data-stu-id="ba630-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="ba630-113">Lietojiet filtru laukam “Statuss” ar vērtību “Ieplānots”, izmantojot filtra operatoru “ir precīzi”.</span><span class="sxs-lookup"><span data-stu-id="ba630-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="ba630-114">Izveidot grafiku</span><span class="sxs-lookup"><span data-stu-id="ba630-114">Create a schedule</span></span>
1. <span data-ttu-id="ba630-115">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="ba630-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="ba630-116">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="ba630-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="ba630-117">Noklikšķiniet uz Plānot darbus.</span><span class="sxs-lookup"><span data-stu-id="ba630-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="ba630-118">Laukā Plānošanas virziens atlasiet “Atpakaļ no piegādes datuma”.</span><span class="sxs-lookup"><span data-stu-id="ba630-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="ba630-119">Laukā Ierobežota noslodze atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="ba630-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="ba630-120">Laukā Ierobežots materiāls atlasiet Nē.</span><span class="sxs-lookup"><span data-stu-id="ba630-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="ba630-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ba630-121">Click OK.</span></span>
    * <span data-ttu-id="ba630-122">Tas var aizņemt kādu laiku.</span><span class="sxs-lookup"><span data-stu-id="ba630-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="ba630-123">Skatīt plānoto ražošanas pasūtījumu rezultātu</span><span class="sxs-lookup"><span data-stu-id="ba630-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="ba630-124">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba630-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ba630-125">Varat atzīmēt jebkuru rindu.</span><span class="sxs-lookup"><span data-stu-id="ba630-125">You can mark any row.</span></span>  
2. <span data-ttu-id="ba630-126">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="ba630-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="ba630-127">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="ba630-127">Click All jobs.</span></span>
    * <span data-ttu-id="ba630-128">Šajā lapā varat redzēt darbu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="ba630-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="ba630-129">Cilnē Plānošana varat redzēt darba vērtības Sākuma datums un Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="ba630-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="ba630-130">Noklikšķiniet uz Materiāli.</span><span class="sxs-lookup"><span data-stu-id="ba630-130">Click Materials.</span></span>
    * <span data-ttu-id="ba630-131">Šajā lapā varat redzēt prognozēto materiālu patēriņu ražošanas pasūtījumā iekļautajām operācijām un pašreiz pieejamos krājumus.</span><span class="sxs-lookup"><span data-stu-id="ba630-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

