---
title: Vispārējās plānošanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar vispārējo plānošanu.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1492854b7d2da480942800e378be9d2bb60bb1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645069"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="15ffd-103">Vispārējās plānošanas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="15ffd-103">Troubleshoot master planning</span></span>

<span data-ttu-id="15ffd-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar vispārējo plānošanu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="15ffd-105">Materiālu komplekta izvēršana darbojas atšķirīgi apstiprinātajiem ražošanas pasūtījumiem un prognozētajiem ražošanas pasūtījumiem manuāli izveidotajam darbam.</span><span class="sxs-lookup"><span data-stu-id="15ffd-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="15ffd-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="15ffd-106">Issue description</span></span>

<span data-ttu-id="15ffd-107">Kad ražošanas pasūtījums ir apstiprināts, krājumi netiek izvērsti, kad tiek izvērsti materiālu komplekti (MK).</span><span class="sxs-lookup"><span data-stu-id="15ffd-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="15ffd-108">Tomēr, kad manuāli veidojat darba pasūtījumu un pēc tam novērtējat ražošanas pasūtījumu, krājumi tiek izvērsti.</span><span class="sxs-lookup"><span data-stu-id="15ffd-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="15ffd-109">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="15ffd-109">Issue resolution</span></span>

<span data-ttu-id="15ffd-110">Sistēma darbojas, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="15ffd-110">The system is working as expected.</span></span> <span data-ttu-id="15ffd-111">Izvērsums, kas rodas, kad ražošanas pasūtījums ir apstiprināts, norādīs uz plānoto pasūtījumu, bet neparādās, ka šajā gadījumā plānotais pasūtījums pašlaik ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="15ffd-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="15ffd-112">Tomēr, ja ražošanas pasūtījums ir novērtēts, izvērsums tiek izraisīts no nodotā ražošanas pasūtījuma, kur nepastāv plānotais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="15ffd-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="15ffd-113">Kavējuma vērtība netiek atjaunināta, pārplānojot plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="15ffd-114">Lai atjauninātu plānoto pasūtījumu kavēšanos, atveriet plānotā pasūtījuma dialoglodziņu **Pārplānošana**.</span><span class="sxs-lookup"><span data-stu-id="15ffd-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="15ffd-115">Kopsavilkuma cilnē **Izvēršana** pārliecinieties, ka opcija **Veikt izvēršanu pēc pārplānošanas** ir iestatīts uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="15ffd-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="15ffd-116">Ražošanas plānošanā netiek ņemtas vērā drošības rezerves, kas iestatītas krājuma segumam piesaistītajai piegādei.</span><span class="sxs-lookup"><span data-stu-id="15ffd-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="15ffd-117">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="15ffd-117">Issue description</span></span>

<span data-ttu-id="15ffd-118">Vispārējā plānošanā tiek aplūkotas drošības rezerves.</span><span class="sxs-lookup"><span data-stu-id="15ffd-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="15ffd-119">Tomēr drošības rezerves tiek ignorētas, kad ir paredzēti plānoti ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="15ffd-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="15ffd-120">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="15ffd-120">Issue resolution</span></span>

<span data-ttu-id="15ffd-121">Rezerves tiek apsvērtas tikai vispārējās plānošanas laikā, nevis manuālajā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="15ffd-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="15ffd-122">Rezerves ir paredzētas, lai tā darbotos kā buferis plānošanas fāzes laikā, lai piešķirtu kādam "rezervi" faktiskajam procesam.</span><span class="sxs-lookup"><span data-stu-id="15ffd-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="15ffd-123">Lai iegūtu vēlamo rezultātu, varat noņemt rezervi.</span><span class="sxs-lookup"><span data-stu-id="15ffd-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="15ffd-124">Pēc tam maršruts ir jāatjaunina, lai tas ietvertu vēlamo laiku (piemēram, kā gaidīšanas laiku).</span><span class="sxs-lookup"><span data-stu-id="15ffd-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="15ffd-125">Tad gan vispārējā plānošana, gan manuālā plānošana uzrāda tādu pašu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="15ffd-126">Plānotie pasūtījumi tiek ģenerēti, pat ja tiem ir preces krājumos un ražošanas pasūtījumi jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="15ffd-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="15ffd-127">Šo problēmu var novērst, palielinot **Pozitīvo dienu** vērtību attiecīgajām grupām lapā **Pārklājumu grupa**.</span><span class="sxs-lookup"><span data-stu-id="15ffd-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="15ffd-128">Šī izmaiņa liks sistēmai noteikt, vai rīcībā esošie krājumi var tikt izmantoti pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="15ffd-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="15ffd-129">Pēc tam krājumos esošām precēm netiks ģenerēts jauns plānotais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="15ffd-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="15ffd-130">Vispārējai plānošanai nav jāievēro noslodzes ierobežojumi, un tā plānošana ir lielāka par pieejamo noslodzi.</span><span class="sxs-lookup"><span data-stu-id="15ffd-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="15ffd-131">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="15ffd-131">Issue description</span></span>

<span data-ttu-id="15ffd-132">Kad izmantojat operāciju plānošanu, kur ir ierobežota noslodze un kur maršruts norāda vajadzību kopumu gan resursu grupai, gan atsevišķiem resursiem, ir neliela iespēja rezervēt vairāk, jo algoritms apstiprina noslodzes konfliktus.</span><span class="sxs-lookup"><span data-stu-id="15ffd-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="15ffd-133">Šī rezervēšana var notikt, kad izmantojat palīgus, lai veiktu vispārējo plānošanu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="15ffd-134">Tas visdrīzāk var notikt, ja ir daudz darbu ar relatīvi īsu izpildlaiku.</span><span class="sxs-lookup"><span data-stu-id="15ffd-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="15ffd-135">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="15ffd-135">Issue resolution</span></span>

<span data-ttu-id="15ffd-136">Ja ir svarīgi, lai operāciju plānošana netiktu pārgrāmatota, ieslēdzot opciju **Precīza ierobežota noslodzes operāciju plānošanai** opciju lapā **Vispārējās plānošanas plānošana**.</span><span class="sxs-lookup"><span data-stu-id="15ffd-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="15ffd-137">Šī opcija nav pieejama pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="15ffd-137">This option isn't available by default.</span></span> <span data-ttu-id="15ffd-138">Tas ir manuāli jāpievieno lapai, izmantojot personalizēšanas līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="15ffd-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="15ffd-139">Kad izmantojat šo opciju, plānošana darbosies lēnāk, jo nav paralēlās apstrādes.</span><span class="sxs-lookup"><span data-stu-id="15ffd-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="15ffd-140">Plānotajiem pasūtījumiem nepieciešams ilgs laiks, lai atjauninātu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="15ffd-141">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="15ffd-141">Issue description</span></span>

<span data-ttu-id="15ffd-142">Atjauninot vajadzības daudzumu un/vai piedāvājuma datumu plānotajā pasūtījumā, parasti katrā pasūtījumā ir nepieciešamas vismaz 30 sekundes, lai saglabātu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="15ffd-143">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="15ffd-143">Issue resolution</span></span>

<span data-ttu-id="15ffd-144">Šī ir zināma problēma iebūvētajā vispārējās plānošanas programmā.</span><span class="sxs-lookup"><span data-stu-id="15ffd-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="15ffd-145">Tas ir saistīts ar pamata automātisko izvēršanu rediģēšanas laikā, izmantojot MK struktūru.</span><span class="sxs-lookup"><span data-stu-id="15ffd-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="15ffd-146">Šī problēma ir adresēta Plānošanas optimizācijā, kur plānotājs var atjaunināt un apstiprināt atbilstošos pasūtījumus un, ja nepieciešams, aktivizēt plānošanas izpildi, lai atjauninātu plānotos pasūtījumus pamata MK struktūrai.</span><span class="sxs-lookup"><span data-stu-id="15ffd-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="15ffd-147">Viens no veidiem, kā uzlabot veiktspēju ar iebūvēto vispārējās plānošanas programmu, ir veikt šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="15ffd-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="15ffd-148">Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.</span><span class="sxs-lookup"><span data-stu-id="15ffd-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="15ffd-149">Atlasiet plānu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-149">Select a plan.</span></span>
1. <span data-ttu-id="15ffd-150">Izvērsiet kopsavilkuma cilni **Laika robeža dienās**.</span><span class="sxs-lookup"><span data-stu-id="15ffd-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="15ffd-151">Iestatiet **Izvēršana** uz *Jā* un iestatiet lauku zem šī iestatījuma uz 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="15ffd-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="15ffd-152">Tas ierobežos šim vispārējam plānam veikto sprādzienu periodu uz vienu dienu.</span><span class="sxs-lookup"><span data-stu-id="15ffd-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>
