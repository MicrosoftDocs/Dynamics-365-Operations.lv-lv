---
title: Vispārējās plānošanas izpildes pārraudzība
description: Šajā tēmā izskaidrots, kā ražošanas plānotājs var redzēt, vai notiek vispārējās plānošanas izpilde.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 159043f37b067df26fdd1de5610eafd663bf6a57
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209563"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="0a569-103">Vispārējās plānošanas izpildes pārraudzība</span><span class="sxs-lookup"><span data-stu-id="0a569-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="0a569-104">Ganta diagrammas izmantošana, lai vizualizētu vispārējās plānošanas norisi</span><span class="sxs-lookup"><span data-stu-id="0a569-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="0a569-105">Lapā **Skatīt vispārējās plānošanas norisi** varat skatīt detalizētu informāciju par vēsturisko vispārējo plānošanu, kas tiek veikta kā Ganta diagramma.</span><span class="sxs-lookup"><span data-stu-id="0a569-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="0a569-106">Šī funkcionalitāte var palīdzēt jums aprēķināt laiku, kas tiek pavadīts dažādos vispārējās plānošanas posmos.</span><span class="sxs-lookup"><span data-stu-id="0a569-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="0a569-107">Pašreizējam aktīvajam plānošanas darbam lapu **Skatīt vispārējās plānošanas norisi** var izmantot, lai izsekotu norisei un skatītu prognozēto atlikušo laiku.</span><span class="sxs-lookup"><span data-stu-id="0a569-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="0a569-108">Vispārējā plāna progresa vizualizācijas līdzekļa ieslēgšana un izmantošana</span><span class="sxs-lookup"><span data-stu-id="0a569-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="0a569-109">Lai izmantotu šo funkcionalitāti, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0a569-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="0a569-110">Darbvietā **Līdzekļu pārvaldība** cilnē **Jauns** atlasiet sarakstā **Vispārējās plānošanas norises vizualizācija**.</span><span class="sxs-lookup"><span data-stu-id="0a569-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="0a569-111">Ja šī funkcija netiek parādīta cilnē **Jauns**, skatiet cilnēs **Neiespējotās** un **Visas**.</span><span class="sxs-lookup"><span data-stu-id="0a569-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="0a569-112">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="0a569-112">Select **Enable now**.</span></span> <span data-ttu-id="0a569-113">Pēc izvēles atlasiet **Grafiks** un pēc tam atlasiet laiku, kad vēlaties ieslēgt līdzekli.</span><span class="sxs-lookup"><span data-stu-id="0a569-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="0a569-114">Lapā **Skatīt vispārējās plānošanas norisi** var apskatīt gan vēsturiskos, gan aktīvos plānošanas darbus.</span><span class="sxs-lookup"><span data-stu-id="0a569-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="0a569-115">Lai skatītu vēsturiskos plānošanas darbus, ir divas opcijas.</span><span class="sxs-lookup"><span data-stu-id="0a569-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="0a569-116">Dodieties uz **Vispārējā plānošana \>Iestatīšana \>Plāni \>Vispārējie plāni** un pēc tam darbību rūtī atlasiet **Vēsture**.</span><span class="sxs-lookup"><span data-stu-id="0a569-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="0a569-117">Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.</span><span class="sxs-lookup"><span data-stu-id="0a569-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="0a569-118">Dodieties uz **Vispārējā plānošana \>Darbvietas \>Vispārējā plānošana**, vispārējā plānošanā noklikšķiniet uz **Vēsture**.</span><span class="sxs-lookup"><span data-stu-id="0a569-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="0a569-119">Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.</span><span class="sxs-lookup"><span data-stu-id="0a569-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="0a569-120">Lai skatītu aktīvos plānošanas darbus, ir divas opcijas.</span><span class="sxs-lookup"><span data-stu-id="0a569-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="0a569-121">Dodieties uz **Vispārējā plānošana \>Darbvietas \>Vispārējā plānošana**, darbību rūtī atlasiet **Nepabeigtais plānošanas process**.</span><span class="sxs-lookup"><span data-stu-id="0a569-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="0a569-122">Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.</span><span class="sxs-lookup"><span data-stu-id="0a569-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="0a569-123">Dodieties uz **Vispārējā plānošana \>Darbvietas \>Vispārējā plānošana**, vispārējā plānošanā noklikšķiniet uz **Skatīt norisi**.</span><span class="sxs-lookup"><span data-stu-id="0a569-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="0a569-124">Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.</span><span class="sxs-lookup"><span data-stu-id="0a569-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="0a569-125">Piezīme: aktīvos darbus var skatīt tikai tad, kad plānošanas darbs tiek apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="0a569-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="0a569-126">Vispārējās plānošanas darbu analizēšana</span><span class="sxs-lookup"><span data-stu-id="0a569-126">Analyze a master planning job</span></span>

<span data-ttu-id="0a569-127">Ganta diagrammā varat izvērst katru no sekojošajiem plānošanas procesiem, lai apskatītu papildu detaļas par patērēto laiku:</span><span class="sxs-lookup"><span data-stu-id="0a569-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="0a569-128">Notiek inicializēšana</span><span class="sxs-lookup"><span data-stu-id="0a569-128">Initializing</span></span>
- <span data-ttu-id="0a569-129">Datu dzēšana un ievietošana</span><span class="sxs-lookup"><span data-stu-id="0a569-129">Deleting and inserting data</span></span>
- <span data-ttu-id="0a569-130">Vajadzību plānošana</span><span class="sxs-lookup"><span data-stu-id="0a569-130">Coverage planning</span></span>
- <span data-ttu-id="0a569-131">Aizkaves</span><span class="sxs-lookup"><span data-stu-id="0a569-131">Delays</span></span>
- <span data-ttu-id="0a569-132">Optimizācijas priekšlikumi</span><span class="sxs-lookup"><span data-stu-id="0a569-132">Action messages</span></span>
- <span data-ttu-id="0a569-133">Pabeigšana</span><span class="sxs-lookup"><span data-stu-id="0a569-133">Finalization</span></span>
- <span data-ttu-id="0a569-134">Automātiskā apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="0a569-134">Auto-firming</span></span>

<span data-ttu-id="0a569-135">Ganta diagramma ir noderīgs rīks, ja vēlaties skatīt darbības ziņojumu izmantošanas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="0a569-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="0a569-136">Navigācija Ganta diagrammā</span><span class="sxs-lookup"><span data-stu-id="0a569-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="0a569-137">Lai izvērstu atlasīto grupu un parādītu detaļas, koka skatā atlasiet pluszīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="0a569-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="0a569-138">Lai sakļautu atlasīto grupu, koka skatā atlasiet mīnusa zīmi (**–**).</span><span class="sxs-lookup"><span data-stu-id="0a569-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="0a569-139">Navigācijai varat izmantot tastatūru.</span><span class="sxs-lookup"><span data-stu-id="0a569-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="0a569-140">Izmantojiet **Augšupvērsto bultiņu** un **Lejupvērsto bultiņu**, lai pārvietotos starp rindām.</span><span class="sxs-lookup"><span data-stu-id="0a569-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="0a569-141">Izmantojiet **Labo bultiņu** un **Kreiso bultiņu**, lai izvērstu un sakļautu grupas.</span><span class="sxs-lookup"><span data-stu-id="0a569-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="0a569-142">Lai atvērtu vai aizvērtu visus Ganta diagrammas līmeņus, atlasiet **Izvērst visu** vai **Sakļaut visu**.</span><span class="sxs-lookup"><span data-stu-id="0a569-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="0a569-143">Lai skatītu saistīto apstrādes laiku, novietojiet kursoru virs uzdevuma.</span><span class="sxs-lookup"><span data-stu-id="0a569-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="0a569-144">(Uzdevumi ir viszemākais līmenis Ganta diagrammā.)</span><span class="sxs-lookup"><span data-stu-id="0a569-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="0a569-145">Skatīt papildu vispārējās plānošanas izpildi, lai salīdzinātu darbus</span><span class="sxs-lookup"><span data-stu-id="0a569-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="0a569-146">Atlasot vispārējās plānošanas darbu laukā **Rādīt papildu vispārējās plānošanas izpildi**, Ganta diagrammā var apskatīt papildu vispārējo plānošanu un salīdzināt abus darbus.</span><span class="sxs-lookup"><span data-stu-id="0a569-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="0a569-147">MK līmeņa displejs</span><span class="sxs-lookup"><span data-stu-id="0a569-147">BOM-level display</span></span>

<span data-ttu-id="0a569-148">Materiālu komplekta (MK) līmeņi tiek parādīti dažādi segumi plānošanai, kavējumiem, darbībām un apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="0a569-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="0a569-149">**Vajadzību plānošana** – MK līmeņi tiek parādīti, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="0a569-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="0a569-150">Tie tiek aprēķināti no augšmalas.</span><span class="sxs-lookup"><span data-stu-id="0a569-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="0a569-151">**Piemērs:** MK līmenis 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="0a569-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="0a569-152">**Kavēšanās** – MK līmeņi tiek parādīti kā seguma plānošanas MK līmeņi, kas reizināti ar –1.</span><span class="sxs-lookup"><span data-stu-id="0a569-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="0a569-153">(Citiem vārdiem, tiem ir negatīva zīme.)</span><span class="sxs-lookup"><span data-stu-id="0a569-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="0a569-154">**Piemērs:** MK līmenis –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="0a569-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="0a569-155">**Darbības ziņojums** – MK līmeņi tiek parādīti, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="0a569-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="0a569-156">Tie tiek aprēķināti no augšmalas.</span><span class="sxs-lookup"><span data-stu-id="0a569-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="0a569-157">**Piemērs:** MK līmenis 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="0a569-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="0a569-158">**Automātiskā apstiprināšana** — MK līmeņi tiek parādīti kā 999 mīnus seguma plānošanas MK līmenis.</span><span class="sxs-lookup"><span data-stu-id="0a569-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="0a569-159">**Piemērs:** MK līmenis 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="0a569-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="0a569-160">Sekojošajā tabulā ir apkopotas darbības.</span><span class="sxs-lookup"><span data-stu-id="0a569-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="0a569-161">Parādītais MK līmenis</span><span class="sxs-lookup"><span data-stu-id="0a569-161">BOM level that is shown</span></span> | <span data-ttu-id="0a569-162">Galaprodukts</span><span class="sxs-lookup"><span data-stu-id="0a569-162">End item</span></span> | <span data-ttu-id="0a569-163">Apakškomponents</span><span class="sxs-lookup"><span data-stu-id="0a569-163">Subcomponent</span></span> | <span data-ttu-id="0a569-164">Izejmateriāls</span><span class="sxs-lookup"><span data-stu-id="0a569-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="0a569-165">Vajadzību plānošana</span><span class="sxs-lookup"><span data-stu-id="0a569-165">Coverage planning</span></span> | <span data-ttu-id="0a569-166">0</span><span class="sxs-lookup"><span data-stu-id="0a569-166">0</span></span> | <span data-ttu-id="0a569-167">1.</span><span class="sxs-lookup"><span data-stu-id="0a569-167">1</span></span> | <span data-ttu-id="0a569-168">2.</span><span class="sxs-lookup"><span data-stu-id="0a569-168">2</span></span> |
| <span data-ttu-id="0a569-169">Aizkaves</span><span class="sxs-lookup"><span data-stu-id="0a569-169">Delays</span></span> | <span data-ttu-id="0a569-170">0</span><span class="sxs-lookup"><span data-stu-id="0a569-170">0</span></span> | <span data-ttu-id="0a569-171">–1</span><span class="sxs-lookup"><span data-stu-id="0a569-171">–1</span></span> | <span data-ttu-id="0a569-172">–2</span><span class="sxs-lookup"><span data-stu-id="0a569-172">–2</span></span> |
| <span data-ttu-id="0a569-173">Optimizācijas priekšlikums</span><span class="sxs-lookup"><span data-stu-id="0a569-173">Action message</span></span> | <span data-ttu-id="0a569-174">0</span><span class="sxs-lookup"><span data-stu-id="0a569-174">0</span></span> | <span data-ttu-id="0a569-175">1.</span><span class="sxs-lookup"><span data-stu-id="0a569-175">1</span></span> | <span data-ttu-id="0a569-176">2.</span><span class="sxs-lookup"><span data-stu-id="0a569-176">2</span></span> |
| <span data-ttu-id="0a569-177">Automātiskā apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="0a569-177">Auto-firming</span></span> | <span data-ttu-id="0a569-178">999</span><span class="sxs-lookup"><span data-stu-id="0a569-178">999</span></span> | <span data-ttu-id="0a569-179">998</span><span class="sxs-lookup"><span data-stu-id="0a569-179">998</span></span> | <span data-ttu-id="0a569-180">997</span><span class="sxs-lookup"><span data-stu-id="0a569-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="0a569-181">Norises vizualizēšana</span><span class="sxs-lookup"><span data-stu-id="0a569-181">Visualize progress</span></span>

<span data-ttu-id="0a569-182">Ja skatāt vispārējās plānošanas darbu, kas pašlaik tiek palaists, Ganta diagrammā tiek rādīta norise ar krāsām.</span><span class="sxs-lookup"><span data-stu-id="0a569-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="0a569-183">Sekojošās krāsas attiecas uz zilo krāsu dizainu.</span><span class="sxs-lookup"><span data-stu-id="0a569-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="0a569-184">Citiem krāsu dizainiem krāsas atšķirsies.</span><span class="sxs-lookup"><span data-stu-id="0a569-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="0a569-185">**Tumši zils** – pabeigti plānošanas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="0a569-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="0a569-186">**Oranžs** — uzdevums pašlaik darbībā.</span><span class="sxs-lookup"><span data-stu-id="0a569-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="0a569-187">**Gaiši zils** — atlikušo uzdevumu novērtējums.</span><span class="sxs-lookup"><span data-stu-id="0a569-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="0a569-188">Krāsa tiek rādīta tikai zemākajā Ganta diagrammas līmenī.</span><span class="sxs-lookup"><span data-stu-id="0a569-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="0a569-189">Atlasiet **Izvērst visu**, lai skatītu visus uzdevumus vispārējā plānošanas darbā.</span><span class="sxs-lookup"><span data-stu-id="0a569-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="0a569-190">Atlikušo uzdevumu novērtējums ir balstīts uz vēsturiskiem vispārējiem plānošanas darbiem.</span><span class="sxs-lookup"><span data-stu-id="0a569-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="0a569-191">Veikt vispārējo plānošanu un izsekot apstrādes laiku</span><span class="sxs-lookup"><span data-stu-id="0a569-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="0a569-192">Noklusējuma informācijas panelī atlasiet **Vispārējā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="0a569-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="0a569-193">Laukā **Plāns** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a569-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="0a569-194">Atlasiet **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="0a569-194">Select **Run**.</span></span>
1. <span data-ttu-id="0a569-195">Iestatiet **Izsekot apstrādes laiku** opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0a569-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="0a569-196">Laukā **Pavedienu skaits** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="0a569-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="0a569-197">Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.</span><span class="sxs-lookup"><span data-stu-id="0a569-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="0a569-198">Režģī atlasiet rindu, kur **Lauks** ir iestatīts uz **Krājuma kods**.</span><span class="sxs-lookup"><span data-stu-id="0a569-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="0a569-199">Laukā **Kritērijs** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0a569-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="0a569-200">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0a569-200">Select **OK**.</span></span>
