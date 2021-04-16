---
title: Ražošanas pasūtījuma plānošana
description: Šajā procedūrā parādīts kā plānot ražošanas pasūtījumu.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a52e2ee3bf0c5dadeda375882d16de60b31d658
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831894"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="e675e-103">Ražošanas pasūtījuma plānošana</span><span class="sxs-lookup"><span data-stu-id="e675e-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e675e-104">Šajā procedūrā parādīts kā plānot ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e675e-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="e675e-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e675e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e675e-106">Šī ir trešā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="e675e-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="e675e-107">Ražošanas pasūtījuma plānošana</span><span class="sxs-lookup"><span data-stu-id="e675e-107">Schedule a production order</span></span>
1. <span data-ttu-id="e675e-108">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e675e-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="e675e-109">Atlasiet ražošanas pasūtījumu, kura statuss ir Plānots.</span><span class="sxs-lookup"><span data-stu-id="e675e-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="e675e-110">Darbību rūtī noklikšķiniet uz Grafiks.</span><span class="sxs-lookup"><span data-stu-id="e675e-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="e675e-111">Noklikšķiniet uz Plānot darbus.</span><span class="sxs-lookup"><span data-stu-id="e675e-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="e675e-112">Šajā lapā var iestatīt plānošanas parametrus.</span><span class="sxs-lookup"><span data-stu-id="e675e-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="e675e-113">Parametrus var iestatīt tikai noteiktiem vai visiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="e675e-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="e675e-114">Laukā Plānošanas virziens atlasiet No šodienas uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="e675e-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="e675e-115">Laukā Plānošanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="e675e-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="e675e-116">Atzīmējiet izvēles rūtiņu Ierobežota noslodze vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="e675e-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="e675e-117">Atzīmējiet izvēles rūtiņu Ierobežots materiāls vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="e675e-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="e675e-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e675e-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="e675e-119">Plānošanas rezultātu skatīšana</span><span class="sxs-lookup"><span data-stu-id="e675e-119">View the scheduling results</span></span>
1. <span data-ttu-id="e675e-120">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e675e-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e675e-121">Noklikšķiniet uz Visi darbi.</span><span class="sxs-lookup"><span data-stu-id="e675e-121">Click All jobs.</span></span>
    * <span data-ttu-id="e675e-122">Šajā lapā ir parādīti plānotie darbi, ko tikko ģenerējāt.</span><span class="sxs-lookup"><span data-stu-id="e675e-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="e675e-123">Izvērsiet vai sakļaujiet sadaļu Plānošana.</span><span class="sxs-lookup"><span data-stu-id="e675e-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="e675e-124">Plānošanas kopsavilkuma cilnē varat skatīt plānotos datumus un laikus.</span><span class="sxs-lookup"><span data-stu-id="e675e-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="e675e-125">Noklikšķiniet uz Uzziņas.</span><span class="sxs-lookup"><span data-stu-id="e675e-125">Click Inquiries.</span></span>
5. <span data-ttu-id="e675e-126">Noklikšķiniet uz Noslodzes grafiks.</span><span class="sxs-lookup"><span data-stu-id="e675e-126">Click Capacity load.</span></span>
    * <span data-ttu-id="e675e-127">Noslodzes grafika lapā tiek rādīta noslodze, kas tika rezervēta, izmantojot darbu plānu, kopējais stundu skaits, kas pašlaik ir rezervēts resursam, un stundu skaits, kas paliek pieejams darbu plānošanai resursam.</span><span class="sxs-lookup"><span data-stu-id="e675e-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="e675e-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e675e-128">Close the page.</span></span>
7. <span data-ttu-id="e675e-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e675e-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]