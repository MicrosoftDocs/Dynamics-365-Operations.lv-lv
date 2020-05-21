---
title: Plānošanas optimizācijas pārskats
description: Šajā tēmā ir sniegts pārskats par Plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 110045d4c7e4f32c29b73096dd4df3a09b5434ac
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323397"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="1c45e-103">Plānošanas optimizācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="1c45e-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c45e-104">Plānošanas optimizācijas pievienojumprogramma, kas paredzēta Microsoft Dynamics 365 Supply Chain Management, ļauj veikt vispārējās plānošanas aprēķinus Dynamics 365 Supply Chain Management, kas tiek notiek ārpusē, un saistīto SQL datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="1c45e-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="1c45e-105">Priekšrocības, kas saistītas ar plānošanas optimizācijas funkcionalitāti, vispārējās plānošanas izpildes laikā ietver uzlabotu veiktspēju un minimālu ietekmi uz SQL datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="1c45e-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="1c45e-106">Ātro plānošanu var veikt arī darba stundu laikā, lai plānotāji varētu nekavējoties reaģēt uz pieprasījumu vai parametru izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="1c45e-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="1c45e-107">Lai izmantotu plānošanas optimizāciju, jums ir jāinstalē Plānošanas optimizācijas pievienojumprogramma no jūsu projekta Microsoft Dynamics Lifecycle Services (LCS) un jāieslēdz Plānošanas optimizācijas funkcionalitāte Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c45e-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="1c45e-108">Papildinformāciju skatiet [Sākt darbu ar Plānošanas optimizāciju ](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="1c45e-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="1c45e-109">Sekojošajā attēlā redzama Plānošanas optimizācijas priekšrocība darba stundu laikā.</span><span class="sxs-lookup"><span data-stu-id="1c45e-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Plānošanas optimizācijas priekšrocība darba stundu laikā](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="1c45e-111">Uzlabota veiktspēja</span><span class="sxs-lookup"><span data-stu-id="1c45e-111">Improved performance</span></span>

<span data-ttu-id="1c45e-112">Plānošanas optimizāciju var izmantot scenārijos, kas ietver ilgstošus galvenos plānus.</span><span class="sxs-lookup"><span data-stu-id="1c45e-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="1c45e-113">Tas ir īpaši izstrādāts ļoti ātriem aprēķiniem, kas ietver ļoti lielus datu apjomus.</span><span class="sxs-lookup"><span data-stu-id="1c45e-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="1c45e-114">Tā kā tas ir izveidots kā hiperpielāgojams daudznomnieka pakalpojums, vairākas instances vienlaicīgi var strādāt kopā, lai aprēķinātu plānu.</span><span class="sxs-lookup"><span data-stu-id="1c45e-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="1c45e-115">Turklāt plānošanas pakalpojums noņem vispārējās plānošanas noslodzi no sistēmas un strādā ar datu plūsmu, kas samazina servera noslodzi.</span><span class="sxs-lookup"><span data-stu-id="1c45e-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="1c45e-116">Plānošanas optimizācija var palīdzēt sasniegt šādus mērķus:</span><span class="sxs-lookup"><span data-stu-id="1c45e-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="1c45e-117">Uzlabot plānošanas veiktspēju, izmantojot īsāku izpildlaiku.</span><span class="sxs-lookup"><span data-stu-id="1c45e-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="1c45e-118">Samazināt ietekmi uz citiem procesiem vispārējās plānošanas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="1c45e-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="1c45e-119">Veikt biežāku plānošanu.</span><span class="sxs-lookup"><span data-stu-id="1c45e-119">Do more frequent planning runs.</span></span> <span data-ttu-id="1c45e-120">(Jūs neesat ierobežots ar ikdienas plānošanu.)</span><span class="sxs-lookup"><span data-stu-id="1c45e-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="1c45e-121">Esiet pārliecināts, ka turpmākā biznesa izaugsme nepārslogos plānošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="1c45e-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="1c45e-122">Arhitektūra un datu plūsma</span><span class="sxs-lookup"><span data-stu-id="1c45e-122">Architecture and data flow</span></span>

<span data-ttu-id="1c45e-123">Kad Plānošanas optimizācijas pievienojumprogramma ir instalēta no LCS, tiek izveidots drošs savienojums ar Plānošanas optimizācijas pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="1c45e-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="1c45e-124">Pakalpojums atrodas tajā pašā datu centra valstī vai reģionā, kā saistītā Supply Chain Management instance.</span><span class="sxs-lookup"><span data-stu-id="1c45e-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="1c45e-125">Pēc Plānošanas optimizācijas iestatīšanas, kad tiek palaista vispārējā plānošana, galvenie dati un transakciju dati tiek sūtīti no Supply Chain Management uz Plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="1c45e-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="1c45e-126">Ja Plānošanas optimizācijas pievienojumprogramma ir atinstalēta, visi saistītie dati Plānošanas optimizācijas pakalpojumā tiek noņemti.</span><span class="sxs-lookup"><span data-stu-id="1c45e-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="1c45e-127">Augsta līmeņa datu plūsma atjaunošanai tiek veikta</span><span class="sxs-lookup"><span data-stu-id="1c45e-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="1c45e-128">Supply Chain Management klients nosūta signālu, lai pieprasītu plānošanas palaišanu no plānošanas optimizācijas.</span><span class="sxs-lookup"><span data-stu-id="1c45e-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="1c45e-129">Plānošanas optimizācija pieprasa vajadzīgos datus, izmantojot iebūvēto savienotāju.</span><span class="sxs-lookup"><span data-stu-id="1c45e-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="1c45e-130">SQL datu bāze sūta pieprasīto informāciju par iestatīšanas, šablona un darbības datiem plānošanas optimizēšanai, izmantojot savienotāju.</span><span class="sxs-lookup"><span data-stu-id="1c45e-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="1c45e-131">Savienotājs tulko informāciju starp Supply Chain Management un plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="1c45e-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="1c45e-132">Plānošanas optimizācijas pakalpojuma rīcībā ir ar plānošanu saistīti dati atmiņā un tiek veikti vajadzīgie aprēķini.</span><span class="sxs-lookup"><span data-stu-id="1c45e-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="1c45e-133">Plānošanas rezultāts tiek nosūtīts uz Supply Chain Management  datu bāzi, izmantojot savienotāju.</span><span class="sxs-lookup"><span data-stu-id="1c45e-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="1c45e-134">Rezultātos ietilpst informācija, piemēram, plānotie pasūtījumi un piesaistes informācija.</span><span class="sxs-lookup"><span data-stu-id="1c45e-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="1c45e-135">Plānošanas optimizācija nosūta signālu uz Supply Chain Management, lai norādītu, ka plānošanas izpilde ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="1c45e-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="1c45e-136">Tas arī nosūta jebkādus svarīgus ziņojumus un brīdinājumus.</span><span class="sxs-lookup"><span data-stu-id="1c45e-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="1c45e-137">Nākamajā attēlā ir redzamas datu plūsmas.</span><span class="sxs-lookup"><span data-stu-id="1c45e-137">The following illustration shows the data flow.</span></span>

![Datu plūsma atjaunošanai tiek veikta](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="1c45e-139">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="1c45e-139">Related resources</span></span>

[<span data-ttu-id="1c45e-140">Darba sākšana ar Plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="1c45e-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1c45e-141">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="1c45e-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1c45e-142">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="1c45e-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1c45e-143">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="1c45e-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1c45e-144">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="1c45e-144">Cancel a planning job</span></span>](cancel-planning-job.md)
