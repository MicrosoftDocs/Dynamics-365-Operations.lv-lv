---
title: Plānot darba izveidi kopuma laikā
description: Šajā tēmā ir aprakstīts, kā iestatīt un izmantot grafika darba izveides kopuma apstrādes metodi.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078284"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="c9e92-103">Plānot darba izveidi kopuma laikā</span><span class="sxs-lookup"><span data-stu-id="c9e92-103">Schedule work creation during wave</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9e92-104">Izmantojiet *Darba plānošanas darba izveides* līdzekli kā daļu no jūsu izveidošanas procesa, lai palīdzētu palielināt kopuma apstrādes caurlaidi, liekot sistēmai izveidot darbu, izmantojot paralēlu apstrādi.</span><span class="sxs-lookup"><span data-stu-id="c9e92-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="c9e92-105">Kad funkcionalitāte ir aktivizēta, plānotais darbs tiks izveidots automātiski, un sistēma tiks visbeidzot apstrādājusi faktisko darbu.</span><span class="sxs-lookup"><span data-stu-id="c9e92-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="c9e92-106">Ja kopuma noslodzes rindu skaits sasniedz iepriekš noteiktu slieksni, sistēma izveidos faktisko darbu ātrāk, lietojot paralēlo, asinhrono apstrādi.</span><span class="sxs-lookup"><span data-stu-id="c9e92-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="c9e92-107">Iespējot darba plānošanas darba izveides līdzekli</span><span class="sxs-lookup"><span data-stu-id="c9e92-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="c9e92-108">Jaunu līdzekļu iespējošana līdzekļu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="c9e92-108">Enable the feature in feature management</span></span>

<span data-ttu-id="c9e92-109">Lai varētu izmantot līdzekli *Darba izveides grafiks*, tas vispirms ir jāieslēdz jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="c9e92-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="c9e92-110">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="c9e92-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c9e92-111">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="c9e92-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c9e92-112">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="c9e92-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c9e92-113">**Līdzekļa nosaukums:** *Darba izveides grafiks*</span><span class="sxs-lookup"><span data-stu-id="c9e92-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="c9e92-114">Pirms *Darba plānošanas izveides* jāiespējo *Organizācijas līmeņa darba bloķēšanas* funkcija.</span><span class="sxs-lookup"><span data-stu-id="c9e92-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="c9e92-115">Manuāli iespējot kopumu pakešveida apstrādi</span><span class="sxs-lookup"><span data-stu-id="c9e92-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="c9e92-116">Lai izmantotu paralēlās asinhronās metodes priekšrocības noliktavas darba izveidošanai, kopuma procesam ir jādarbojas paketē.</span><span class="sxs-lookup"><span data-stu-id="c9e92-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="c9e92-117">Lai to iestatītu:</span><span class="sxs-lookup"><span data-stu-id="c9e92-117">To set this up:</span></span>

1. <span data-ttu-id="c9e92-118">Dodieties uz  **Noliktavas vadība \> Iestatīšana \> Noliktavas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="c9e92-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="c9e92-119">Cilnē **Vispārīgi** iestatiet opciju **Veikt kopumiem pakešveida apstrādi** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="c9e92-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="c9e92-120">Varat arī atlasīt atvēlēto **Kopuma apstrādes pakešuzdevumu grupu**, lai novērstu pakešuzdevumu rindas apstrādes darbību vienlaicīgi ar citiem procesiem.</span><span class="sxs-lookup"><span data-stu-id="c9e92-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="c9e92-121">Iestatiet **Gaidīt bloķēšanas (ms) laiku**, kas tiek lietots, ja sistēma apstrādā vairākus kopumus vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="c9e92-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="c9e92-122">Lielākajai daļai ražošanas procesu ieteicams izmantot vērtību *60000*.</span><span class="sxs-lookup"><span data-stu-id="c9e92-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="c9e92-123">Manuāli iespējot jauno kopuma darbības metodi esošajām kopuma veidnēm</span><span class="sxs-lookup"><span data-stu-id="c9e92-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="c9e92-124">Sākt, izveidojot jaunu kopuma darbības metodi un iespējojot to paralēlā asinhronā uzdevuma apstrādē.</span><span class="sxs-lookup"><span data-stu-id="c9e92-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="c9e92-125">Dodieties uz  **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.</span><span class="sxs-lookup"><span data-stu-id="c9e92-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="c9e92-126">Atlasiet  **Reģenerēšanas metodi** un ievērojiet, ka *WHSScheduleWorkCreationWaveStepMethod* ir pievienots kopuma apstrādes metožu sarakstam, ko varat izmantot nosūtīšanas kopuma veidnēs.</span><span class="sxs-lookup"><span data-stu-id="c9e92-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="c9e92-127">Atlasiet ierakstu ar **Metodes nosaukumu** *WHSScheduleWorkCreationWaveStepMethod* un atlasiet **Uzdevuma konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="c9e92-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="c9e92-128">Darbību rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un pēc tam atlasiet šos iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="c9e92-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="c9e92-129">**Noliktava** - izvēlieties noliktavu, ko izmantosiet darba izveides apstrādes plānošanai.</span><span class="sxs-lookup"><span data-stu-id="c9e92-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="c9e92-130">**Maksimālais pakešuzdevumu skaits** - norādiet maksimālo pakešuzdevumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="c9e92-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="c9e92-131">Vairākumā gadījumu šai vērtībai jābūt diapazonā no 8 līdz 16, tomēr mēs iesakām veikt optimālu iestatījumu, kas veidots, pamatojoties uz jūsu scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="c9e92-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="c9e92-132">**Kopuma apstrādes partijas** grupa — atlasiet atvēlēto kopuma apstrādes partijas grupu, lai optimizētu jūsu partijas rindas apstrādi.</span><span class="sxs-lookup"><span data-stu-id="c9e92-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="c9e92-133">Tagad varat atjaunināt esošu kopuma veidni (vai izveidot jaunu), lai izmantotu *Darba izveides grafika* kopuma apstrādes metodi.</span><span class="sxs-lookup"><span data-stu-id="c9e92-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="c9e92-134">Dodieties uz  **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="c9e92-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="c9e92-135">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c9e92-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="c9e92-136">Saraksta rūtī atlasiet kopuma veidni, kuru vēlaties atjaunināt (ja pārbaudes izmantojat demonstrācijas datus, tad varat izmantot *24 nosūtīšanas noklusējumu*).</span><span class="sxs-lookup"><span data-stu-id="c9e92-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="c9e92-137">Izvērsiet kopsavilkuma cilni **Metodes** un atlasiet rindu ar **Nosaukumu** *Darba izveides grafiku* režģī **Atlikušās metodes**.</span><span class="sxs-lookup"><span data-stu-id="c9e92-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="c9e92-138">Atlasiet bultiņu, kas norāda uz kolonnu **Atlasītās metodes**, lai pārvietotu atlasīto rindu uz šo kolonnu.</span><span class="sxs-lookup"><span data-stu-id="c9e92-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="c9e92-139">(Vienlaicīgi var būt tikai viena atlasītā metode, kas izmanto vai nu *WHSScheduleWorkCreationWaveStepMethod*, vai *createWork*, tāpēc esošā rinda ar **Metodes nosaukumu** *createWork*  tiek automātiski pārvietota uz režģi **Atlikušās metodes**.)</span><span class="sxs-lookup"><span data-stu-id="c9e92-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="c9e92-140">Iestatīt kopuma uzdevuma apstrādes sliekšņa datus</span><span class="sxs-lookup"><span data-stu-id="c9e92-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="c9e92-141">Sistēma izveidos noklusējuma kopuma uzdevuma apstrādes sliekšņa datus, pirmo reizi palaižot kopuma procesu, izmantojot jebkuru uz uzdevumu balstītu apstrādi.</span><span class="sxs-lookup"><span data-stu-id="c9e92-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="c9e92-142">Dati tiek izmantoti, lai kontrolētu, kad kopuma apstrāde darbosies asinhroni un būs uz uzdevumiem balstīta, kas ļauj to apstrādāt un izveidot darbu paralēli.</span><span class="sxs-lookup"><span data-stu-id="c9e92-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="c9e92-143">Noklusējuma dati sākotnēji izmantos 15 sliekšņa vērtību minimālajam kravas rindu skaitam (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="c9e92-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="c9e92-144">Tas nozīmē, ka, kad sistēma apstrādā laidienu ar vairāk nekā 15 noslodzes rindām, tas izmantos asinhronu uzdevumu apstrādi.</span><span class="sxs-lookup"><span data-stu-id="c9e92-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="c9e92-145">Varat manuāli ievietot/atjaunināt šos datus tabulā **WHSWaveTaskProcessingThresholdParameters** savās pārbaudes vidēs, bet, ja jums ir jāmaina šis iestatījums ražošanas vidē, ir jāsazinās ar Microsoft atbalsta dienestu, lai pieprasītu atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="c9e92-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="c9e92-146">Darbs ar šo līdzekli</span><span class="sxs-lookup"><span data-stu-id="c9e92-146">Work with the feature</span></span>

<span data-ttu-id="c9e92-147">Kad *Grafika darba izveides* funkcionalitāte ir aktivizēta, kopuma apstrāde izveidos plānoto darbu, ko visbeidzot izmantos jaunais darba izveides process.</span><span class="sxs-lookup"><span data-stu-id="c9e92-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="c9e92-148">Darba izveides laikā darbs tiks bloķēts, izmantojot *Organizācijas līmeņa darba bloķēšanas* iespēju.</span><span class="sxs-lookup"><span data-stu-id="c9e92-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="c9e92-149">Šajā plūsmkartē ir parādīts, kā kopuma apstrādes laikā tiek veidots plānotais darbs.</span><span class="sxs-lookup"><span data-stu-id="c9e92-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Ieplānot darba izveidi](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="c9e92-151">Plānots darbs</span><span class="sxs-lookup"><span data-stu-id="c9e92-151">Planned work</span></span>

<span data-ttu-id="c9e92-152">**Plānotā darba detalizētas informācijas** lapa (**Noliktavas pārvaldība \> Darbs \> Plānotā darba informācija**) rāda informāciju par plānoto darbu, kas sākotnēji tika izveidots kopuma apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="c9e92-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="c9e92-153">Ir pieejami sekojošas **Procesa statusa** vērtības:</span><span class="sxs-lookup"><span data-stu-id="c9e92-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="c9e92-154">**Ievietots rindā** - plānotais darbs gaida darbu izveides procesu.</span><span class="sxs-lookup"><span data-stu-id="c9e92-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="c9e92-155">**Pabeigts** – plānotais darbs ir izmantots darba izveidei.</span><span class="sxs-lookup"><span data-stu-id="c9e92-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="c9e92-156">**Neizdevās** — kopuma apstrāde neizdevās.</span><span class="sxs-lookup"><span data-stu-id="c9e92-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="c9e92-157">Ievērojiet, ka plānotais darbs var būt stāvoklī **Neizdevās** ar vai bez saistītā faktiskā darba.</span><span class="sxs-lookup"><span data-stu-id="c9e92-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="c9e92-158">Ja faktiskais darba izveides process neizdodas, faktiskais darbs paliek statusā *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="c9e92-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="c9e92-159">Pakešuzdevums darba izveides procesam</span><span class="sxs-lookup"><span data-stu-id="c9e92-159">Batch job for the work creation process</span></span>

<span data-ttu-id="c9e92-160">Lai skatītu kopumu apstrādes pakešuzdevumus, atlasiet darbību rūtī **Pakešuzdevumi** lapā **Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="c9e92-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="c9e92-161">No šejienes jūs varat skatīt visu pakešuzdevumu detaļas katram pakešuzdevumu laukā.</span><span class="sxs-lookup"><span data-stu-id="c9e92-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>
