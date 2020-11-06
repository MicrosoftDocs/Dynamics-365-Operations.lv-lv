---
title: Zonas sliekšņa papildināšana
description: Uz zonu pamatota papildināšana izmanto minimālo/maksimālo (min./maks.) papildināšanas stratēģiju, bet novērtē visas noliktavas zonas, nevis tikai atsevišķus novietojumus. Tāpēc noliktavas vadītājs var ātrāk uzzināt par gadījumiem, kad izdošanas zonā ir nepieciešami papildu krājumi.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e13b5fd895fca7f8fe77809348d63ed8867dea9e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017326"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="1367f-104">Zonas sliekšņa papildināšana</span><span class="sxs-lookup"><span data-stu-id="1367f-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1367f-105">Uz zonu pamatota papildināšana izmanto minimālo/maksimālo (min./maks.) [papildināšanas](replenishment.md) stratēģiju, bet novērtē visas noliktavas zonas, nevis tikai atsevišķus novietojumus.</span><span class="sxs-lookup"><span data-stu-id="1367f-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="1367f-106">Tāpēc noliktavas vadītājs var ātrāk uzzināt par gadījumiem, kad izdošanas zonā ir nepieciešami papildu krājumi.</span><span class="sxs-lookup"><span data-stu-id="1367f-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="1367f-107">Šī līdzekļa iestatīšana līdzinās uz novietojumu pamatotas papildināšanas iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="1367f-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="1367f-108">Iestatot min./maks. papildināšanas veidni, varat arī norādīt, vai slieksnis ir jānovērtē katram novietojumam vai katrai zonai.</span><span class="sxs-lookup"><span data-stu-id="1367f-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="1367f-109">Ja iestatāt uz zonām pamatotu novērtējumu, zonas atlases vaicājumam ir jāpievieno konkrētas zonas.</span><span class="sxs-lookup"><span data-stu-id="1367f-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="1367f-110">Tāpat kā uz novietojumu pamatota min./maks. papildināšana, uz zonu pamatota min./maks. papildināšana ir pamatota uz minimālo krājumu iestatīšanu, kas aktivizē papildināšanas darba izveidi atlasītiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="1367f-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="1367f-111">Šis papildināšanas darbs palielinās krājumu līdz norādītajam maksimālajam zonas slieksnim.</span><span class="sxs-lookup"><span data-stu-id="1367f-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="1367f-112">Zonas papildināšanas procesi produkta variantiem netiek atbalstīti pašreizējā laidienā.</span><span class="sxs-lookup"><span data-stu-id="1367f-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="1367f-113">Atšķirībā no uz novietojumu pamatotas min./maks. papildināšanas, uz zonu pamatotai min./maks. papildināšanai nav nepieciešami izvietojumi, no novērtētu, vai novietojumos ir jāglabā kāds konkrēts krājums.</span><span class="sxs-lookup"><span data-stu-id="1367f-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="1367f-114">Tāpēc uz zonu pamatotā papildināšana ļauj izmantot min./maks. papildināšanu pat tad, ja jums noliktavā nav fiksēta novietojuma katram krājumam vai krājuma variantam.</span><span class="sxs-lookup"><span data-stu-id="1367f-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="1367f-115">Ja zonā esošais daudzums nokrītas zem norādītā minimālā sliekšņa, tiek izveidots papildināšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="1367f-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="1367f-116">Novietojuma direktīvas noteiks, kurā konkrētajā novietojumā ir jāievieto krājumi.</span><span class="sxs-lookup"><span data-stu-id="1367f-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="1367f-117">Līdzekļa Zonas sliekšņa papildināšana ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="1367f-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="1367f-118">Lai varētu izmantot līdzekli *Zonas sliekšņa papildināšana* , tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1367f-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="1367f-119">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="1367f-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1367f-120">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="1367f-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1367f-121">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="1367f-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1367f-122">**Līdzekļa nosaukums:** *Zonas sliekšņa papildināšana*</span><span class="sxs-lookup"><span data-stu-id="1367f-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="1367f-123">Uz zonu pamatotas papildināšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1367f-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="1367f-124">Lai iestatītu uz zonu pamatotu papildināšanu, ir jākonfigurē vairākas sistēmas daļas.</span><span class="sxs-lookup"><span data-stu-id="1367f-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="1367f-125">Šajā sadaļā ir izklāstīti vairāki iestatījumi un nodrošināti demonstrācijas dati, ko varat ievadīt, ja šīs tēmas beigās vēlaties strādāt ar scenāriju.</span><span class="sxs-lookup"><span data-stu-id="1367f-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="1367f-126">Direktīvas kodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1367f-126">Set up directive codes</span></span>

<span data-ttu-id="1367f-127">[Direktīvas kodi](control-warehouse-location-directives.md) sniedz iespēju konkrētāk definēt novietojuma veidni, kas tiek izmantota darba veidnē.</span><span class="sxs-lookup"><span data-stu-id="1367f-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="1367f-128">Katrs kods izveido kopīgu vērtību, uz ko varat atsaukties, konfigurējot katras veidnes veidu.</span><span class="sxs-lookup"><span data-stu-id="1367f-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="1367f-129">Direktīvas kodu skatīšana un rediģēšana</span><span class="sxs-lookup"><span data-stu-id="1367f-129">View and edit directive codes</span></span>

<span data-ttu-id="1367f-130">Lai skatītu vai rediģētu direktīvas kodus, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Direktīvas kodi**.</span><span class="sxs-lookup"><span data-stu-id="1367f-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="1367f-131">Demonstrācijas datu direktīvas kodu sagatavošana</span><span class="sxs-lookup"><span data-stu-id="1367f-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="1367f-132">Šajā piemērā ir parādīts, kā sagatavot direktīvas kodu.</span><span class="sxs-lookup"><span data-stu-id="1367f-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="1367f-133">Ja plānojat strādāt ar scenāriju šīs tēmas beigās, izmantojiet šeit sniegtās demonstrācijas datu vērtības.</span><span class="sxs-lookup"><span data-stu-id="1367f-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="1367f-134">Pretējā gadījumā izmantojiet savas vērtības.</span><span class="sxs-lookup"><span data-stu-id="1367f-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="1367f-135">Atlasiet **USMF** juridisko personu, lai strādātu ar demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="1367f-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="1367f-136">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Direktīvas kodi**.</span><span class="sxs-lookup"><span data-stu-id="1367f-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="1367f-137">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1367f-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="1367f-138">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-139">**Direktīvas kods:** _Zonas papild._</span><span class="sxs-lookup"><span data-stu-id="1367f-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="1367f-140">**Direktīvas apraksts:** _Zonas papildināšana_</span><span class="sxs-lookup"><span data-stu-id="1367f-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="1367f-141">Atlasiet **Saglabāt** , lai saglabātu jauno kodu.</span><span class="sxs-lookup"><span data-stu-id="1367f-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="1367f-142">Iestatīt papildināšanas veidnes</span><span class="sxs-lookup"><span data-stu-id="1367f-142">Set up replenishment templates</span></span>

<span data-ttu-id="1367f-143">[Min./maks. papildināšanas veidnes](tasks/set-up-min-max-replenishment-process.md) ir galvenais mehānisms optimālu līmeņu uzturēšanai izdošanas novietojumos.</span><span class="sxs-lookup"><span data-stu-id="1367f-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="1367f-144">Šajās veidnēs ir jāiestata kārtulas, kas tiks izmantotas krājumu papildināšanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="1367f-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="1367f-145">Papildināšana, ko veidnes var izmantot uz iekļaušanas zonu pamatotai papildināšanai.</span><span class="sxs-lookup"><span data-stu-id="1367f-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="1367f-146">Papildināšanas veidņu skatīšana un labošana</span><span class="sxs-lookup"><span data-stu-id="1367f-146">View and edit replenishment templates</span></span>

<span data-ttu-id="1367f-147">Papildināšanas veidne ir kārtulu kopa, kas kontrolē novietojuma papildināšanas laiku un veidu.</span><span class="sxs-lookup"><span data-stu-id="1367f-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="1367f-148">Atlasiet veidni, lai kontrolētu, kad un kā tiek veikta papildināšana.</span><span class="sxs-lookup"><span data-stu-id="1367f-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="1367f-149">Lai skatītu vai rediģētu papildināšanas veidnes, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes**.</span><span class="sxs-lookup"><span data-stu-id="1367f-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="1367f-150">Demonstrācijas datu papildināšanas veidnes sagatavošana</span><span class="sxs-lookup"><span data-stu-id="1367f-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="1367f-151">Šajā piemērā ir parādīts, kā sagatavot papildināšanas veidni.</span><span class="sxs-lookup"><span data-stu-id="1367f-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="1367f-152">Ja plānojat strādāt ar scenāriju šīs tēmas beigās, izmantojiet šeit sniegtās demonstrācijas datu vērtības.</span><span class="sxs-lookup"><span data-stu-id="1367f-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="1367f-153">Pretējā gadījumā izmantojiet savas vērtības.</span><span class="sxs-lookup"><span data-stu-id="1367f-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="1367f-154">Atlasiet **USMF** juridisko personu, lai strādātu ar demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="1367f-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="1367f-155">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes**.</span><span class="sxs-lookup"><span data-stu-id="1367f-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="1367f-156">Darbību rūtī atlasiet **Rediģēt** , lai lapu padarītu rediģējamu.</span><span class="sxs-lookup"><span data-stu-id="1367f-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="1367f-157">Lai režģim **Pārskats** pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1367f-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="1367f-158">Jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="1367f-158">In the new row, set the following values.</span></span> <span data-ttu-id="1367f-159">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="1367f-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1367f-160">**Papildināšanas veidne:** _Zonas min/maks. papild._</span><span class="sxs-lookup"><span data-stu-id="1367f-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="1367f-161">**Apraksts:** _Zonas min./maks. papildināšana_</span><span class="sxs-lookup"><span data-stu-id="1367f-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="1367f-162">**Papildināšanas veids:** _Minimums vai maksimums_</span><span class="sxs-lookup"><span data-stu-id="1367f-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="1367f-163">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1367f-163">Select **Save**.</span></span>
1. <span data-ttu-id="1367f-164">Kamēr jaunā rinda vēl ir atlasīta režģī **Pārskats** , atlasiet vērtību **Jauns** virs režģa **Detalizēta informācija par papildināšanas veidni** , lai pievienotu rindu, kas ir saistīta ar tikko izveidoto papildināšanas veidni *Zonas min./maks. papild.*</span><span class="sxs-lookup"><span data-stu-id="1367f-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="1367f-165">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-166">**Kārtas numurs:** ievadiet _1_.</span><span class="sxs-lookup"><span data-stu-id="1367f-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1367f-167">**Apraksts:** ievadiet _Izdošanas zonas papildināšana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="1367f-168">**Papildināšanas vienība:** atlasiet _ea_.</span><span class="sxs-lookup"><span data-stu-id="1367f-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="1367f-169">**Pieprasījuma veids:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="1367f-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="1367f-170">**Direktīvas kods:** šis lauks saista papildināšanas veidni ar novietojuma direktīvu.</span><span class="sxs-lookup"><span data-stu-id="1367f-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="1367f-171">Atlasiet iepriekš izveidoto demonstrācijas datu direktīvas kodu ( _Zonas papild._ )</span><span class="sxs-lookup"><span data-stu-id="1367f-171">Select the demo data directive code that you created earlier ( _Zone replen_ ).</span></span>
    - <span data-ttu-id="1367f-172">**Darba veidne:** Atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="1367f-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="1367f-173">**Minimālais daudzums:** šajā laukā tiek iestatīts daudzums, saistībā ar kuru tiek aktivizēta papildināšana.</span><span class="sxs-lookup"><span data-stu-id="1367f-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="1367f-174">Ievadiet _50_.</span><span class="sxs-lookup"><span data-stu-id="1367f-174">Enter _50_.</span></span>
    - <span data-ttu-id="1367f-175">**Maksimālais daudzums:** šajā laukā tiek iestatīts maksimālais krājuma daudzums, kāds var būt zonā.</span><span class="sxs-lookup"><span data-stu-id="1367f-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="1367f-176">Ģenerētais papildināšanas darbs palielinās krājumus līdz šim daudzumam.</span><span class="sxs-lookup"><span data-stu-id="1367f-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="1367f-177">Ievadiet _150_.</span><span class="sxs-lookup"><span data-stu-id="1367f-177">Enter _150_.</span></span>
    - <span data-ttu-id="1367f-178">**Vienība:** šajā laukā tiek iestatīta minimālo un maksimālo vērtību vienība.</span><span class="sxs-lookup"><span data-stu-id="1367f-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="1367f-179">Atlasiet _ea_.</span><span class="sxs-lookup"><span data-stu-id="1367f-179">Select _ea_.</span></span>
    - <span data-ttu-id="1367f-180">**Pieprasījuma pieaugums:** atlasiet _Noapaļot uz augšu_.</span><span class="sxs-lookup"><span data-stu-id="1367f-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="1367f-181">**Papildināt tukšus fiksētos novietojumus:** atlasiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="1367f-182">**Papildināt tikai fiksētos novietojumus:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-183">**Produkta vaicājuma režīms:** atlasiet _Produkta vaicājums_.</span><span class="sxs-lookup"><span data-stu-id="1367f-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="1367f-184">**Papildināšanas sliekšņa diapazons:** šajā laukā tiek definēts, vai veidnei ir jānovērtē pēc zonas vai pēc konkrēta novietojuma.</span><span class="sxs-lookup"><span data-stu-id="1367f-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="1367f-185">Atlasiet _Zona_.</span><span class="sxs-lookup"><span data-stu-id="1367f-185">Select _Zone_.</span></span>
    - <span data-ttu-id="1367f-186">**Noliktava:** atlasiet _61_.</span><span class="sxs-lookup"><span data-stu-id="1367f-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="1367f-187">Atlasiet opciju **Atlasīt produktus** virs režģa **Detalizēta informācija par papildināšanas veidni**.</span><span class="sxs-lookup"><span data-stu-id="1367f-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="1367f-188">Dialoglodziņā **Produkta vaicājums** cilnē **Diapazon** atlasiet **Pievienot** , lai pievienotu rindu režģim.</span><span class="sxs-lookup"><span data-stu-id="1367f-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="1367f-189">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-190">**Tabula:** _Krājums_</span><span class="sxs-lookup"><span data-stu-id="1367f-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="1367f-191">**Atveidotā tabula:** _Krājums_</span><span class="sxs-lookup"><span data-stu-id="1367f-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="1367f-192">**Lauks:** _Krājuma numurs_</span><span class="sxs-lookup"><span data-stu-id="1367f-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="1367f-193">**Kritēriji:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="1367f-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="1367f-194">Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="1367f-195">Atlasiet opciju **Atlasīt papildināmās zonas** virs režģa **Detalizēta informācija par papildināšanas veidni**.</span><span class="sxs-lookup"><span data-stu-id="1367f-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="1367f-196">Dialoglodziņā **Zonas vaicājums** cilnē **Diapazons** pievienojiet rindu režģim.</span><span class="sxs-lookup"><span data-stu-id="1367f-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="1367f-197">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-198">**Tabula:** _Noliktavas zona_</span><span class="sxs-lookup"><span data-stu-id="1367f-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="1367f-199">**Atveidotā tabula:** _Noliktavas zona_</span><span class="sxs-lookup"><span data-stu-id="1367f-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="1367f-200">**Lauks:** _Zonas ID_</span><span class="sxs-lookup"><span data-stu-id="1367f-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="1367f-201">**Kritēriji:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="1367f-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="1367f-202">Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="1367f-203">Iestatīt novietojuma direktīvas</span><span class="sxs-lookup"><span data-stu-id="1367f-203">Set up location directives</span></span>

<span data-ttu-id="1367f-204">Atšķirībā no min./maks. papildināšanas, kas pamatota uz novietojumu, uz zonu pamatotajai min./maks papildināšanai ir jāiestata gan izdošanas novietojuma direktīvas, gan izvietošanas novietojuma direktīvas, jo sistēma novērtē visu zonu, nevis tikai izejošā darba izdošanas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="1367f-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="1367f-205">Novietojuma direktīvu skatīšana un rediģēšana</span><span class="sxs-lookup"><span data-stu-id="1367f-205">View and edit location directives</span></span>

<span data-ttu-id="1367f-206">Lai skatītu vai rediģētu novietojuma direktīvas, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="1367f-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="1367f-207">Piemērus par to, kā izmantot iestatījumus, lai izveidotu nepieciešamās izdošanas novietojuma direktīvas un izvietošanas novietojuma direktīvas, skatiet nākamajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="1367f-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="1367f-208">Demonstrācijas datu novietojuma direktīvas sagatavošana</span><span class="sxs-lookup"><span data-stu-id="1367f-208">Prepare demo data location directives</span></span>

<span data-ttu-id="1367f-209">Lai sagatavotu demonstrācijas datus tā, ka tos var izmantot scenārijā šīs tēmas beigās, ir jāizveido divas novietojuma direktīvas — viena izdošanai un viena izvietošanai.</span><span class="sxs-lookup"><span data-stu-id="1367f-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="1367f-210">Papildināšanas izdošanas direktīvas izveide</span><span class="sxs-lookup"><span data-stu-id="1367f-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="1367f-211">Atlasiet **USMF** juridisko personu, lai strādātu ar demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="1367f-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="1367f-212">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="1367f-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1367f-213">Kreisajā rūtī laukam **Darba pasūtījuma veids** iestatiet vērtību _Papildināšana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="1367f-214">Lai izveidotu jaunu direktīvu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1367f-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="1367f-215">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-215">Set the following values:</span></span>

    - <span data-ttu-id="1367f-216">**Kārtas numurs:** akceptējiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="1367f-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="1367f-217">**Nosaukums:** ievadiet _Zonas izdošana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="1367f-218">**Darba veids:** atlasiet _Izdošana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="1367f-219">**Vieta:** atlasiet _6_.</span><span class="sxs-lookup"><span data-stu-id="1367f-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="1367f-220">**Noliktava:** atlasiet _61_.</span><span class="sxs-lookup"><span data-stu-id="1367f-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="1367f-221">**Direktīvas kods:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="1367f-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="1367f-222">**Vairāki SKU:** opcijai iestatiet vērtību _Nē_.</span><span class="sxs-lookup"><span data-stu-id="1367f-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="1367f-223">Atlasiet **Saglabāt** , lai izveidotu direktīvu, kurai ir jūsu līdz šim brīdim izveidotie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="1367f-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="1367f-224">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns** , lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1367f-225">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1367f-226">**Kārtas numurs:** ievadiet _1_.</span><span class="sxs-lookup"><span data-stu-id="1367f-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1367f-227">**No daudzuma:** ievadiet _0_.</span><span class="sxs-lookup"><span data-stu-id="1367f-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="1367f-228">**Līdz daudzumam:** ievadiet _10000000_.</span><span class="sxs-lookup"><span data-stu-id="1367f-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="1367f-229">**Vienība:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="1367f-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="1367f-230">**Meklēt daudzumu:** atlasiet _Nav_.</span><span class="sxs-lookup"><span data-stu-id="1367f-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="1367f-231">**Ierobežot pēc vienības:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-232">**Noapaļot līdz vienībai:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-233">**Meklēt iepakojuma daudzumu:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-234">**Atļaut sadali:** atlasiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="1367f-235">Atlasiet **Saglabāt** , lai saglabātu jauno rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="1367f-236">Kamēr jūsu jaunā rinda vēl ir atlasīta režģī **Rindas** , kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns** , lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="1367f-237">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-238">**Kārtas numurs:** ievadiet _1_.</span><span class="sxs-lookup"><span data-stu-id="1367f-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1367f-239">**Nosaukums:** ievadiet _Izdot no lielapjoma_.</span><span class="sxs-lookup"><span data-stu-id="1367f-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="1367f-240">**Fiksēta novietojuma lietojums:** atlasiet _Fiksēti un nefiksēti novietojumi_.</span><span class="sxs-lookup"><span data-stu-id="1367f-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="1367f-241">**Atļaut negatīvus krājumus:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-242">**Partija iespējota:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-243">**Stratēģija:** atlasiet _Nav_.</span><span class="sxs-lookup"><span data-stu-id="1367f-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="1367f-244">Atlasiet **Saglabāt** , lai saglabātu jauno darbību.</span><span class="sxs-lookup"><span data-stu-id="1367f-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="1367f-245">Kamēr jaunā darbība vēl ir atlasīta, atlasiet **Rediģēt vaicājumu** virs režģa **Novietojuma direktīvas darbības**.</span><span class="sxs-lookup"><span data-stu-id="1367f-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="1367f-246">Tiks parādīts dialoglodziņš, kurā varat atlasīt novietojumus, no kuriem papildināt.</span><span class="sxs-lookup"><span data-stu-id="1367f-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="1367f-247">Cilnē **Diapazons** atlasiet **Pievienot** , lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="1367f-248">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-249">**Tabula:** _Novietojumi_</span><span class="sxs-lookup"><span data-stu-id="1367f-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="1367f-250">**Atvasinātā tabula:** _Vietas_</span><span class="sxs-lookup"><span data-stu-id="1367f-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="1367f-251">**Lauks:** _Zonas ID_</span><span class="sxs-lookup"><span data-stu-id="1367f-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="1367f-252">**Kritēriji:** _LIELAPJOMA_</span><span class="sxs-lookup"><span data-stu-id="1367f-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="1367f-253">Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="1367f-254">Atlasiet **Saglabāt** , lai saglabātu novietojuma direktīvu.</span><span class="sxs-lookup"><span data-stu-id="1367f-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="1367f-255">Papildināšanas izvietošanas direktīvas izveide</span><span class="sxs-lookup"><span data-stu-id="1367f-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="1367f-256">Lapā **Novietojuma direktīvas** kreisajā rūtī pārbaudiet, vai laukam **Darba pasūtījuma veids** joprojām ir iestatīta vērtība _Papildināšana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="1367f-257">Lai izveidotu vēl vienu jaunu direktīvu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1367f-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="1367f-258">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-258">Set the following values:</span></span>

    - <span data-ttu-id="1367f-259">**Kārtas numurs:** akceptējiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="1367f-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="1367f-260">**Nosaukums:** ievadiet _Zonas izvietošana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="1367f-261">**Darba pasūtījuma veids:** atlasiet _Izvietošana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="1367f-262">**Vieta:** atlasiet _6_.</span><span class="sxs-lookup"><span data-stu-id="1367f-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="1367f-263">**Noliktava:** atlasiet _61_.</span><span class="sxs-lookup"><span data-stu-id="1367f-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="1367f-264">**Direktīvas kods**  — atlasiet _Zonas papild._ , lai saistītu novietojuma direktīvu ar papildināšanas veidni, ko izveidojāt iepriekš, izmantojot iepriekš izveidoto kodu.</span><span class="sxs-lookup"><span data-stu-id="1367f-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="1367f-265">**Vairāki SKU:** opcijai iestatiet vērtību _Nē_.</span><span class="sxs-lookup"><span data-stu-id="1367f-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="1367f-266">Atlasiet **Saglabāt** , lai izveidotu direktīvu, kurai ir jūsu līdz šim brīdim izveidotie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="1367f-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="1367f-267">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns** , lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1367f-268">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1367f-269">**Kārtas numurs:** ievadiet _1_.</span><span class="sxs-lookup"><span data-stu-id="1367f-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1367f-270">**No daudzuma:** ievadiet _0_.</span><span class="sxs-lookup"><span data-stu-id="1367f-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="1367f-271">**Līdz daudzumam:** ievadiet _10000000_.</span><span class="sxs-lookup"><span data-stu-id="1367f-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="1367f-272">**Vienība:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="1367f-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="1367f-273">**Meklēt daudzumu:** atlasiet _Nav_.</span><span class="sxs-lookup"><span data-stu-id="1367f-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="1367f-274">**Ierobežot pēc vienības:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-275">**Noapaļot līdz vienībai:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-276">**Meklēt iepakojuma daudzumu:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-277">**Atļaut sadali:** atlasiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="1367f-278">Atlasiet **Saglabāt** , lai saglabātu jauno rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="1367f-279">Kamēr jūsu jaunā rinda vēl ir atlasīta režģī **Rindas** , kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns** , lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="1367f-280">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-281">**Kārtas numurs:** ievadiet _1_.</span><span class="sxs-lookup"><span data-stu-id="1367f-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1367f-282">**Nosaukums:** ievadiet _Zonas izvietošana_.</span><span class="sxs-lookup"><span data-stu-id="1367f-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="1367f-283">**Fiksēta novietojuma lietojums:** atlasiet _Fiksēti un nefiksēti novietojumi_.</span><span class="sxs-lookup"><span data-stu-id="1367f-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="1367f-284">**Atļaut negatīvus krājumus:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-285">**Partija iespējota:** notīriet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="1367f-286">**Stratēģija:** atlasiet _Konsolidēt_.</span><span class="sxs-lookup"><span data-stu-id="1367f-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="1367f-287">Atlasiet **Saglabāt** , lai saglabātu jauno darbību.</span><span class="sxs-lookup"><span data-stu-id="1367f-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="1367f-288">Kamēr jaunā darbība vēl ir atlasīta, atlasiet **Rediģēt vaicājumu** virs režģa **Novietojuma direktīvas darbības**.</span><span class="sxs-lookup"><span data-stu-id="1367f-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="1367f-289">Tiks parādīts dialoglodziņš, kurā varat atlasīt papildināmo zonu.</span><span class="sxs-lookup"><span data-stu-id="1367f-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="1367f-290">Šai zonai ir jābūt tai pašai zonai, kas norādīta papildināšanas veidnē.</span><span class="sxs-lookup"><span data-stu-id="1367f-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="1367f-291">Cilnē **Diapazons** atlasiet **Pievienot** , lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="1367f-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="1367f-292">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1367f-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1367f-293">**Tabula:** _Novietojumi_</span><span class="sxs-lookup"><span data-stu-id="1367f-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="1367f-294">**Atvasinātā tabula:** _Vietas_</span><span class="sxs-lookup"><span data-stu-id="1367f-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="1367f-295">**Lauks:** _Zonas ID_</span><span class="sxs-lookup"><span data-stu-id="1367f-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="1367f-296">**Kritēriji:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="1367f-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="1367f-297">Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="1367f-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="1367f-298">Atlasiet **Saglabāt** , lai saglabātu novietojuma direktīvu.</span><span class="sxs-lookup"><span data-stu-id="1367f-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="1367f-299">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="1367f-299">Scenario</span></span>

<span data-ttu-id="1367f-300">Šajā sadaļā ir pieejams parauga scenārijs, kur parādīts, kā strādāt ar līdzekli.</span><span class="sxs-lookup"><span data-stu-id="1367f-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="1367f-301">Parauga scenārijam nepieciešamo parauga datu sagatavošana</span><span class="sxs-lookup"><span data-stu-id="1367f-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="1367f-302">Pirms sākt darbu ar scenāriju, aktivizējiet parauga datus un iestatiet līdzekli, kā tas ir izklāstīts šajā sadaļā un iepriekšējās šīs tēmas sadaļās.</span><span class="sxs-lookup"><span data-stu-id="1367f-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="1367f-303">USMF juridiskas personas izmantošana</span><span class="sxs-lookup"><span data-stu-id="1367f-303">Use the USMF legal entity</span></span>

<span data-ttu-id="1367f-304">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1367f-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="1367f-305">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="1367f-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="1367f-306">Papildu parauga datu sagatavošana</span><span class="sxs-lookup"><span data-stu-id="1367f-306">Prepare additional sample data</span></span>

<span data-ttu-id="1367f-307">Kad atlasīsit **USMF** juridisko vienību, pievienojiet nepieciešamos papildu parauga datus, kas norādīti sadaļā [Uz zonu pamatotas papildināšanas iestatīšana](#setup) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="1367f-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="1367f-308">Rīcībā esošo krājumu pārbaude</span><span class="sxs-lookup"><span data-stu-id="1367f-308">Check your on-hand inventory</span></span>

<span data-ttu-id="1367f-309">Izpildiet šīs darbības, lai pārliecinātos, vai jūsu sistēmā ir iekļauti pietiekami daudz krājumu, kas nepieciešami parauga scenārija atbalstīšanai.</span><span class="sxs-lookup"><span data-stu-id="1367f-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="1367f-310">Pārbaudiet, vai rīcībā ir krājumi krājumam *A0001* divos dažādos novietojumos izdošanas zonā ( *FLOOR* ), kas ir norādīta papildināšanas veidnē.</span><span class="sxs-lookup"><span data-stu-id="1367f-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone ( *FLOOR* ) that is specified in the replenishment template.</span></span> <span data-ttu-id="1367f-311">Tomēr kopējiem krājumiem ir jābūt mazākiem par nepieciešamo minimālo daudzumu ( *50* ), kas norādīts papildināšanas veidnē.</span><span class="sxs-lookup"><span data-stu-id="1367f-311">However, the total inventory should be less than the required minimum quantity ( *50* ) that is specified on the replenishment template.</span></span> <span data-ttu-id="1367f-312">Šādi varat simulēt, kā notiek aprēķini visai zonai, nevis tikai vienam atsevišķam novietojumam.</span><span class="sxs-lookup"><span data-stu-id="1367f-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="1367f-313">**Izmantojiet jebkuru no noliktavas procesiem, lai pēc nepieciešamības koriģētu krājumus.**</span><span class="sxs-lookup"><span data-stu-id="1367f-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="1367f-314">Pārliecinieties, vai krājumam *A0001* ir pietiekami daudz krājumu lielapjoma novietojumā, kas norādīts zonas izdošanas novietojuma direktīvā, kur papildināšanas darbam ir jāpaņem krājumi no zonas ID *BULK*.</span><span class="sxs-lookup"><span data-stu-id="1367f-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="1367f-315">Kopējiem krājumiem ir jābūt lielākiem par nepieciešamo maksimālo daudzumu ( *150* ), kas norādīts papildināšanas veidnē.</span><span class="sxs-lookup"><span data-stu-id="1367f-315">The total inventory must be more than the required maximum quantity ( *150* ) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="1367f-316">Ieteicama izvēles iespēja: izpildiet šīs darbības, lai izveidotu krājumu korekcijas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="1367f-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="1367f-317">Dodieties uz **Krājumu pārvaldība \> Žurnāla ieraksti \> Krājumi \> Krājumu korekcija**.</span><span class="sxs-lookup"><span data-stu-id="1367f-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="1367f-318">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1367f-318">Select **New**.</span></span>
    1. <span data-ttu-id="1367f-319">Dialoglodziņā **Krājumu žurnāla izveide** laukā **Noliktava** atlasiet *61*.</span><span class="sxs-lookup"><span data-stu-id="1367f-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="1367f-320">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1367f-320">Select **OK**.</span></span>
    1. <span data-ttu-id="1367f-321">Kopsavilkuma cilnē **Žurnāla rindas** izmantojiet pogu **Jauns** , lai režģim pievienotu trīs rindas un iestatītu tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1367f-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="1367f-322">Pēc katras rindas iestatīšanas beigām atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1367f-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="1367f-323">**1. rinda**</span><span class="sxs-lookup"><span data-stu-id="1367f-323">**Line 1:**</span></span>

            - <span data-ttu-id="1367f-324">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1367f-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="1367f-325">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="1367f-325">**Site:** *6*</span></span>
            - <span data-ttu-id="1367f-326">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="1367f-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="1367f-327">**Novietojums:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="1367f-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="1367f-328">**Unikāla noliktavas vienība**  — sarakstā atlasiet esošu unikālu noliktavas vienību sarakstā vai izveidojiet jaunu unikālu noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="1367f-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="1367f-329">**Daudzums:** *1000*</span><span class="sxs-lookup"><span data-stu-id="1367f-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="1367f-330">**2. rinda**</span><span class="sxs-lookup"><span data-stu-id="1367f-330">**Line 2:**</span></span>

            - <span data-ttu-id="1367f-331">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1367f-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="1367f-332">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="1367f-332">**Site:** *6*</span></span>
            - <span data-ttu-id="1367f-333">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="1367f-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="1367f-334">**Novietojums:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="1367f-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="1367f-335">**Unikāla noliktavas vienība**  — sarakstā atlasiet esošu unikālu noliktavas vienību sarakstā vai izveidojiet jaunu unikālu noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="1367f-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="1367f-336">**Daudzums:** *15*</span><span class="sxs-lookup"><span data-stu-id="1367f-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="1367f-337">**3. rinda**</span><span class="sxs-lookup"><span data-stu-id="1367f-337">**Line 3:**</span></span>

            - <span data-ttu-id="1367f-338">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1367f-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="1367f-339">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="1367f-339">**Site:** *6*</span></span>
            - <span data-ttu-id="1367f-340">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="1367f-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="1367f-341">**Novietojums:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="1367f-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="1367f-342">**Unikāla noliktavas vienība**  — sarakstā atlasiet esošu unikālu noliktavas vienību sarakstā vai izveidojiet jaunu unikālu noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="1367f-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="1367f-343">**Daudzums:** *10*</span><span class="sxs-lookup"><span data-stu-id="1367f-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="1367f-344">Darbību rūtī atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="1367f-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="1367f-345">Pirms pāriešanas uz nākamo soli novērsiet visas atrastās kļūdas.</span><span class="sxs-lookup"><span data-stu-id="1367f-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="1367f-346">Darbību rūtī atlasiet **Grāmatot** , lai noliktavā grāmatotu krājumus.</span><span class="sxs-lookup"><span data-stu-id="1367f-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="1367f-347">Parauga scenārijs: uz zonas pamatotas min./maks. papildināšanas izpilde</span><span class="sxs-lookup"><span data-stu-id="1367f-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="1367f-348">Kad ir ievietoti visi priekšnosacījuma parauga dati, varat aktivizēt papildināšanu, izpildot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1367f-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="1367f-349">Dodieties uz **Noliktavas pārvaldība \> Papildināšana \> Papildināšanas**.</span><span class="sxs-lookup"><span data-stu-id="1367f-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="1367f-350">Dialoglodziņā **Papildināšana** kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**.</span><span class="sxs-lookup"><span data-stu-id="1367f-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="1367f-351">Dialoglodziņā **Vaicājums** cilnē **Diapazons** rediģējiet noklusējuma tabulas rindu, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="1367f-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="1367f-352">**Tabula:** atlasiet _Papildināšanas veidnes_.</span><span class="sxs-lookup"><span data-stu-id="1367f-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="1367f-353">**Atveidotā tabula:** atlasiet _Papildināšanas veidnes_.</span><span class="sxs-lookup"><span data-stu-id="1367f-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="1367f-354">**Lauks:** atlasiet _Papildināšanas veidne_.</span><span class="sxs-lookup"><span data-stu-id="1367f-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="1367f-355">**Kritēriji:** atlasiet _Zonas min./maks. papild._</span><span class="sxs-lookup"><span data-stu-id="1367f-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="1367f-356">Šī papildināšanas veidne ir tā papildināšanas veidne, kuru izveidojāt, kad šim scenārijam sagatavojāt demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="1367f-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="1367f-357">Atlasiet **Labi** , lai saglabātu vaicājumu, un dodieties atpakaļ uz dialoglodziņu **Papildināšana**.</span><span class="sxs-lookup"><span data-stu-id="1367f-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="1367f-358">Atlasiet **Labi** , lai palaistu papildināšanas veidni.</span><span class="sxs-lookup"><span data-stu-id="1367f-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="1367f-359">Papildināšanas darbs tagad ir izveidots, lai izdotu krājumus no zonas *BULK* un papildinātu zonu *FLOOR*.</span><span class="sxs-lookup"><span data-stu-id="1367f-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="1367f-360">Piezīmes un padomi</span><span class="sxs-lookup"><span data-stu-id="1367f-360">Notes and tips</span></span>

<span data-ttu-id="1367f-361">Tālāk ir sniegtas dažas piezīmes un padomi darbam ar līdzekli.</span><span class="sxs-lookup"><span data-stu-id="1367f-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="1367f-362">Lai iestatītu papildināšanas darbu, kas tiks novirzīts uz vēlamo zonu, papildināšanas veidnes rindas un novietojuma direktīvas varat saistīt, izmantojot kādu no tālāk norādītajiem veidiem.</span><span class="sxs-lookup"><span data-stu-id="1367f-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="1367f-363">Rediģējiet novietojuma direktīvas galvenes vaicājumu un filtrējiet atlasītās papildināšanas veidnes rindas.</span><span class="sxs-lookup"><span data-stu-id="1367f-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="1367f-364">Izmantojiet direktīvas kodu papildināšanas veidnes rindā un saskaņojiet to ar izvietošanas novietojuma direktīvu.</span><span class="sxs-lookup"><span data-stu-id="1367f-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="1367f-365">Ja izmantojat dinamiskos novietojumus, papildināšanas darbs tiks izveidots vai nu pirmajam pieejamajam novietojumam, vai novietojumam, kurā jau ir krājumi, ja novietojuma direktīvas darbība ir iestatīta izmantot stratēģiju **Konsolidēt**.</span><span class="sxs-lookup"><span data-stu-id="1367f-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="1367f-366">Ja zonu vietā izmantojat fiksētus novietojumus, izmantojiet [standarta min./maks. papildināšanu](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="1367f-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
