---
title: Ražošanas izpildes darba slodzes mākoņa un malas mēroga vienībām
description: Šajā tēmā aprakstīts, kā ražošanas izpildes darba slodzes darbojas ar mākoņa un malas mēroga vienībām.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b1e2006c0d9b9effe331a644aaaa9fa33ff2fb7c
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270539"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="9c02b-103">Ražošanas izpildes darba slodzes mākoņa un malas mēroga vienībām</span><span class="sxs-lookup"><span data-stu-id="9c02b-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]

> [!WARNING]
> <span data-ttu-id="9c02b-104">Ražošanas izpildes darba slodze ir pieejama priekšskatījumā šajā brīdī.</span><span class="sxs-lookup"><span data-stu-id="9c02b-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="9c02b-105">Dažas biznesa funkcionalitātes netiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes mēroga vienības tiek izmantotas.</span><span class="sxs-lookup"><span data-stu-id="9c02b-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="9c02b-106">Ražošanas izpildē mēroga vienības nodrošina šādas iespējas:</span><span class="sxs-lookup"><span data-stu-id="9c02b-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="9c02b-107">Iekārtu operatori un ražotnes uzraudzības iestādes var piekļūt operāciju ražošanas plānam.</span><span class="sxs-lookup"><span data-stu-id="9c02b-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="9c02b-108">Iekārtu operatori var uzturēt plāna atjaunināšanu, izpildot diskrētus un procesa ražošanas darbus.</span><span class="sxs-lookup"><span data-stu-id="9c02b-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="9c02b-109">Ražotnes vadītājs var koriģēt darbības plānu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="9c02b-110">Darbinieki var piekļūt ierašanās un aiziešanas reģistrācijas laikam un apmeklējumam, lai nodrošinātu pareizu darbinieka algas aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="9c02b-111">Šajā tēmā aprakstīts, kā ražošanas izpildes darba slodzes darbojas ar mākoņa un malas mēroga vienībām.</span><span class="sxs-lookup"><span data-stu-id="9c02b-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="9c02b-112">Ražošanas cikls</span><span class="sxs-lookup"><span data-stu-id="9c02b-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="9c02b-113">Kā parādīts sekojošajā attēlā, ražošanas cikls ir sadalīts trīs fāzēs: *Plānošana*, *Izpilde* un *Pabeigšana*.</span><span class="sxs-lookup"><span data-stu-id="9c02b-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="9c02b-114">[![Ražošanas izpildes fāzes, kad tiek izmantota viena vide](media/mes-phases.png "Ražošanas izpildes fāzes, kad tiek izmantotas viena vide")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="9c02b-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="9c02b-115">Fāzē _Plānošana_ ietver produkta definīciju, plānošanu, pasūtījuma izveidi un plānošanu un izlaišanu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="9c02b-116">Izlaišanas darbība norāda pāreju no fāzes _Plānošana_ uz fāzi _Izpilde_.</span><span class="sxs-lookup"><span data-stu-id="9c02b-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="9c02b-117">Kad ražošanas pasūtījums tiek izlaists, ražošanas pasūtījuma darbi būs redzami ražotnē un gatavi izpildei.</span><span class="sxs-lookup"><span data-stu-id="9c02b-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="9c02b-118">Kad ražošanas darbs ir atzīmēts kā pabeigts, tas tiek pārvietots no fāzes _Izpilde_ uz fāzi _Pabeigšana_.</span><span class="sxs-lookup"><span data-stu-id="9c02b-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="9c02b-119">Fāzē _Pabeigšana_ reģistrācijas no fāzes *Izpilde* tiek veiktas, izmantojot apstiprinājuma darbplūsmu, kur tās tiek aprēķinātas, apstiprinātas un pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="9c02b-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="9c02b-120">Šajā brīdī ražošanas pasūtījums ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="9c02b-120">At that point, the production order is completed.</span></span> <span data-ttu-id="9c02b-121">Tāpēc tiek ģenerēts darbinieku apmaksas pamats.</span><span class="sxs-lookup"><span data-stu-id="9c02b-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="9c02b-122">Izpildes fāzes sadalīšana atsevišķā darba slodzē</span><span class="sxs-lookup"><span data-stu-id="9c02b-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="9c02b-123">Kā redzams ilustrācijā, kad tiek izmantotas mēroga vienības, fāze _Izpilde_ tiek sadalīta kā atsevišķa darba slodze.</span><span class="sxs-lookup"><span data-stu-id="9c02b-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="9c02b-124">[![Ražošanas izpildes fāzes, kad tiek izmantotas mēroga vienības](media/mes-phases-workloads.png "Ražošanas izpildes fāzes, kad tiek izmantotas mēroga vienības")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="9c02b-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="9c02b-125">Tagad modelis pāriet no viena gadījuma instalācijas modeļa uz modeli, kura pamatā ir centrmezgls un mēroga vienības.</span><span class="sxs-lookup"><span data-stu-id="9c02b-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="9c02b-126">Fāzes _Plānošana_ un _Pabeigšana_ tiek izpildītas kā biroja operācijas, un ražošanas izpildes darba slodze darbojas uz mēroga vienībām.</span><span class="sxs-lookup"><span data-stu-id="9c02b-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="9c02b-127">Dati tiek pārsūtīti asinhroni starp centrmezglu un mēroga vienībām.</span><span class="sxs-lookup"><span data-stu-id="9c02b-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="9c02b-128">Kad ražošanas pasūtījums tiek izlaists centrmezglā, visi dati, kas nepieciešami ražošanas darbu apstrādei, tiek pārsūtīti uz mēroga vienību.</span><span class="sxs-lookup"><span data-stu-id="9c02b-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="9c02b-129">Šie dati ietver ražošanas pasūtījumus, ražošanas maršrutus, materiālu komplektus un produktus.</span><span class="sxs-lookup"><span data-stu-id="9c02b-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="9c02b-130">Dati, kas nav saistīti ar ražošanas pasūtījumu (piemēram, netiešās aktivitātes, kavējumu kodi un ražošanas parametri), arī tiek pārsūtīti no centrmezgla uz mēroga vienību.</span><span class="sxs-lookup"><span data-stu-id="9c02b-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="9c02b-131">Parasti dati, kas rodas no centrmezgla un kas tiek pārsūtīti uz mēroga vienību, var tikt izveidoti vai atjaunināti tikai centrmezglā.</span><span class="sxs-lookup"><span data-stu-id="9c02b-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="9c02b-132">Piemēram, jaunu kavējuma kodu vai netiešo aktivitāti nevar izveidot mēroga vienībās,&mdash;tos var izmantot tikai reģistrācijai.</span><span class="sxs-lookup"><span data-stu-id="9c02b-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="9c02b-133">Reģistrācijas, kas veiktas mēroga vienībās izpildes laikā, pēc tam tiek pārsūtītas uz centrmezglu, kur tiek apstrādāti laika un klātbūtnes apstiprinājums, krājumi un finanšu atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="9c02b-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="9c02b-134">Ražošanas izpildes uzdevumi, kurus var izpildīt darba slodzēm</span><span class="sxs-lookup"><span data-stu-id="9c02b-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="9c02b-135">Tālāk norādītos ražošanas izpildes uzdevumus pašlaik var palaist darba noslodzēm, kad tiek izmantotas mēroga vienības:</span><span class="sxs-lookup"><span data-stu-id="9c02b-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="9c02b-136">Ierašanās, pieteikšanās, aiziešana un kavējums</span><span class="sxs-lookup"><span data-stu-id="9c02b-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="9c02b-137">Sākt darbu</span><span class="sxs-lookup"><span data-stu-id="9c02b-137">Start job</span></span>
- <span data-ttu-id="9c02b-138">Komplekta darbi</span><span class="sxs-lookup"><span data-stu-id="9c02b-138">Bundle jobs</span></span>
- <span data-ttu-id="9c02b-139">Pārskata norise</span><span class="sxs-lookup"><span data-stu-id="9c02b-139">Report progress</span></span>
- <span data-ttu-id="9c02b-140">Ziņot par lūžņiem</span><span class="sxs-lookup"><span data-stu-id="9c02b-140">Report scrap</span></span>
- <span data-ttu-id="9c02b-141">Netiešā aktivitāte</span><span class="sxs-lookup"><span data-stu-id="9c02b-141">Indirect activity</span></span>
- <span data-ttu-id="9c02b-142">Pārtraukums</span><span class="sxs-lookup"><span data-stu-id="9c02b-142">Break</span></span>
- <span data-ttu-id="9c02b-143">Reģistrēt pabeigšanu un izvietot (nepieciešams, lai tiktu palaista arī noliktavas izpildes darba slodze jūsu mēroga vienībai, skatiet arī [Reģistrēt pabeigšanu un izvietot mēroga vienībā](#RAF))</span><span class="sxs-lookup"><span data-stu-id="9c02b-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="9c02b-144">Darbs ar ražošanas izpildes darba slodzēm centrmezglā</span><span class="sxs-lookup"><span data-stu-id="9c02b-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="9c02b-145">Parasti procesi, kas ir nepieciešami ražošanas izpildes darba slodzēm, tiek palaisti automātiski, lai pēc nepieciešamības uzturētu centrmezglu un visas mēroga vienības sinhronizācijā.</span><span class="sxs-lookup"><span data-stu-id="9c02b-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="9c02b-146">Tomēr, ja rodas problēmas, varat manuāli aktivizēt neapstrādāto reģistrāciju apstrādi, kas tiek saņemta no darba slodzēm un/vai pārbaudīt reģistrācijas apstrādes žurnālu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="9c02b-147">Apstrādāt neapstrādātās reģistrācijas manuāli</span><span class="sxs-lookup"><span data-stu-id="9c02b-147">Manually process raw registrations</span></span>

<span data-ttu-id="9c02b-148">Pakalpojumā Supply Chain Management pakešuzdevums tiek palaists automātiski, lai apstrādātu visas reģistrācijas, kas saņemtas no darba slodzēm.</span><span class="sxs-lookup"><span data-stu-id="9c02b-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="9c02b-149">Šis darbs izveido vajadzīgos ražošanas žurnālus un reģistrācijas žurnāla ierakstus, kad reģistrācija tiek apstrādāta pabeigtam darbam uz darba slodzes.</span><span class="sxs-lookup"><span data-stu-id="9c02b-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="9c02b-150">Lai gan darbs parasti tiek palaists automātiski, to var palaist manuāli jebkurā laikā, piesakoties centrmezglā un dodoties uz **Ražošanas kontrole \> Periodiskie uzdevumie \> Biroja darba slodzes pārvaldība \> Apstrādāt neapstrādātās reģistrācijas**.</span><span class="sxs-lookup"><span data-stu-id="9c02b-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="9c02b-151">Pārbaudīt neapstrādāto reģistrāciju apstrādes žurnālu</span><span class="sxs-lookup"><span data-stu-id="9c02b-151">Check the raw registration processing log</span></span>

<span data-ttu-id="9c02b-152">Lai pārskatītu reģistrācijas apstrādes žurnālu, piesakieties centrmezglam un dodieties uz **Ražošanas kontrole \> Periodiskie uzdevumi \> Biroja darba slodzes pārvaldība \> Neapstrādāto reģistrāciju apstrādes žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="9c02b-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="9c02b-153">Lapa **Neapstrādāto reģistrāciju apstrādes žurnāls** rāda apstrādāto neapstrādāto reģistrāciju sarakstu un katras reģistrācijas statusu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="9c02b-154">![Neapstrādāto reģistrāciju apstrādes žurnāla lapa](media/mes-processing-log.png "Neapstrādāto reģistrāciju apstrādes žurnāla lapa")</span><span class="sxs-lookup"><span data-stu-id="9c02b-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="9c02b-155">Jūs varat strādāt ar jebkuru reģistrāciju sarakstā, atlasot to un pēc tam atlasot vienu no šīm pogām darbības rūtī:</span><span class="sxs-lookup"><span data-stu-id="9c02b-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="9c02b-156">**Apstrādāt** – manuāli apstrādāt atlasīto reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="9c02b-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="9c02b-157">Šī darbība var būt noderīga, ja darbs _Apstrādāt neapstrādātu reģistrāciju_ nav palaists vai arī tas neizdevās.</span><span class="sxs-lookup"><span data-stu-id="9c02b-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="9c02b-158">**Atcelt** – atcelt atlasīto reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="9c02b-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="9c02b-159">Darbs ar ražošanas izpildes darba slodzēm mēroga vienībā</span><span class="sxs-lookup"><span data-stu-id="9c02b-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="9c02b-160">Parasti procesi, kas ir nepieciešami ražošanas izpildes darba slodzēm, tiek palaisti automātiski, lai pēc nepieciešamības uzturētu centrmezglu un visas mēroga vienības sinhronizācijā.</span><span class="sxs-lookup"><span data-stu-id="9c02b-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="9c02b-161">Tomēr, ja rodas problēmas, varat pārbaudīt to pasūtījumu vēsturi, kas ir apstrādāti apjoma vienībās, vai manuāli palaist darbu _Ražošanas centrmezgls mēroga vienību ziņojuma procesoram_.</span><span class="sxs-lookup"><span data-stu-id="9c02b-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="9c02b-162">Skatīt to ražošanas darbu vēsturi, kas ir apstrādāti mēroga vienībās</span><span class="sxs-lookup"><span data-stu-id="9c02b-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="9c02b-163">Lai pārskatītu to ražošanas darbu vēsturi, kas ir apstrādāti mēroga vienībās, piesakieties apjoma mērvienību iekārtā un dodieties uz **Ražošanas kontrole \> Periodiskie uzdevumi \> Biroja darba slodzes pērvaldība \> Ražošanas darbu apstrādes vēsture**.</span><span class="sxs-lookup"><span data-stu-id="9c02b-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="9c02b-164">Lapā **Ražošanas darbu apstrādes vēsture** tiek parādīta ražošanas pasūtījumu apstrādes vēsture mēroga vienībā.</span><span class="sxs-lookup"><span data-stu-id="9c02b-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="9c02b-165">Jūs varat strādāt ar jebkuru ražošanas pasūtījumu sarakstā, atlasot to un pēc tam atlasot vienu no šīm pogām darbības rūtī:</span><span class="sxs-lookup"><span data-stu-id="9c02b-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="9c02b-166">**Apstrādāt** – manuāli apstrādāt atlasīto ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="9c02b-167">**Atcelt** – atcelt atlasīto ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="9c02b-168">Ražošanas centrmezgls mēroga vienības ziņojuma procesora darbām</span><span class="sxs-lookup"><span data-stu-id="9c02b-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="9c02b-169">Darbs _Ražošanas centrmezgls mēroga vienības ziņojuma procesoram_ apstrādā datus no centrmezgla uz mēroga vienību.</span><span class="sxs-lookup"><span data-stu-id="9c02b-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="9c02b-170">Šis darbs tiek automātiski sākts, kad tiek izvietota ražošanas izpildes darba slodze.</span><span class="sxs-lookup"><span data-stu-id="9c02b-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="9c02b-171">Tomēr to var palaist manuāli jebkurā laikā, pārejot uz **Ražošanas kontrole \> Periodiskie uzdevumi \> Biroja darba slodzes pārvadība \> Ražošanas centrmezgls mēroga vienības ziņojuma procesoram**.</span><span class="sxs-lookup"><span data-stu-id="9c02b-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="9c02b-172">Reģistrēt pabeigšanu un izvietot mēroga vienībā</span><span class="sxs-lookup"><span data-stu-id="9c02b-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="9c02b-173">Pašreizējā laidienā, reģistrējot pabeigšanu un izvietošanas operācijas, (pabeigtajām precēm, līdzproduktiem un blakusproduktiem) tiek atbalstītas [noliktavas izpildes darba slodzes](cloud-edge-workload-warehousing.md) (nevis ražošanas izpildes darba slodzes).</span><span class="sxs-lookup"><span data-stu-id="9c02b-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="9c02b-174">Tāpēc, lai izmantotu šo funkcionalitāti, ja ir izveidots savienojums ar mēroga vienību, ir jāveic šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="9c02b-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="9c02b-175">Instalējiet gan noliktavas izpildes darba noslodzi, gan ražošanas izpildes darba slodzi mēroga vienībai.</span><span class="sxs-lookup"><span data-stu-id="9c02b-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="9c02b-176">Izmantojiet mobilo programmu Warehouse Management, lai reģistrētu kā pabeigtu un apstrādātu izvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="9c02b-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="9c02b-177">Ražošanas izpildes interfeiss pašlaik neatbalsta šos procesus.</span><span class="sxs-lookup"><span data-stu-id="9c02b-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
