---
title: Plānošanas optimizācijas saderības analīze
description: Šajā tēmā skaidrots, kā verificēt jūsu pašreizējos iestatījumus un datus, salīdzinot ar Plānošanas optimizācijas funkcionalitātes iespējām.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a61529da63bc20fdd591afc94db960b05c284bb9
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935879"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="67659-103">Plānošanas optimizācijas saderības analīze</span><span class="sxs-lookup"><span data-stu-id="67659-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="67659-104">Lai apskatītu, cik saderīgi ir jūsu pašreizējie iestatījumi un dati ar Plānošanas optimizācijas funkcionalitāti, dodieties uz **Vispārējā plānošana**\>**Iestatīšana**\>**Plānošanas optimizācijas saderības analīze**, un pēc tam atlasiet **Palaist analīzi**.</span><span class="sxs-lookup"><span data-stu-id="67659-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="67659-105">Ja analīze atklāj neatbilstības, tās ir uzskaitītas tajā pašā lapā.</span><span class="sxs-lookup"><span data-stu-id="67659-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="67659-106">(Analīze var ilgt dažas minūtes.)</span><span class="sxs-lookup"><span data-stu-id="67659-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="67659-107">Ja atrastas neatbilstības, joprojām varat izmantot Plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="67659-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="67659-108">Saderības analīzes rezultāti tikai rāda vietas, kur plānošanas pakalpojums neievēros jūsu pašreizējos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="67659-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="67659-109">Citiem vārdiem, tas rāda vietas, kur daži procesi var tikt ignorēti vai, iespējams, netiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="67659-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="67659-110">Analīzes rezultāti: 1. piemērs</span><span class="sxs-lookup"><span data-stu-id="67659-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="67659-111">**Līdzeklis:** ražošana</span><span class="sxs-lookup"><span data-stu-id="67659-111">**Feature:** Production</span></span>
- <span data-ttu-id="67659-112">**Problēma:** krājumi ar MK līmeni lielāki par nulli: 56</span><span class="sxs-lookup"><span data-stu-id="67659-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="67659-113">**Paskaidrojums:** saderības analīze atrada 56 krājumus, kuriem ir materiālu komplekta (MK) iestatījums ražošanai.</span><span class="sxs-lookup"><span data-stu-id="67659-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="67659-114">Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta ražošanu, tā izveidos plānotos pirkšanas pasūtījumus, nevis plānotos ražošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="67659-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="67659-115">Tiks parādīts arī brīdinājums, kas uzskaita ietekmētos krājumus.</span><span class="sxs-lookup"><span data-stu-id="67659-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="67659-116">Analīzes rezultāti: 2. piemērs</span><span class="sxs-lookup"><span data-stu-id="67659-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="67659-117">**Līdzeklis:** darbības</span><span class="sxs-lookup"><span data-stu-id="67659-117">**Feature:** Actions</span></span>
- <span data-ttu-id="67659-118">**Problēma:** nodrošinājuma grupas ar iespējotu darbību aprēķinu: 6</span><span class="sxs-lookup"><span data-stu-id="67659-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="67659-119">**Paskaidrojums:** saderības analīze atrada sešas nodrošinājuma grupas, kurās ir ieslēgts darbības aprēķins.</span><span class="sxs-lookup"><span data-stu-id="67659-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="67659-120">Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta darbības, vispārējās plānošanas laikā netiks ģenerētas darbības.</span><span class="sxs-lookup"><span data-stu-id="67659-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="67659-121">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="67659-121">Related resources</span></span>

[<span data-ttu-id="67659-122">Plānošanas optimizācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="67659-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="67659-123">Darba sākšana ar Plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="67659-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="67659-124">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="67659-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="67659-125">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="67659-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="67659-126">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="67659-126">Cancel a planning job</span></span>](cancel-planning-job.md)
