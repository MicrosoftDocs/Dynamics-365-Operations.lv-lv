---
title: Detalizēta darba rindas informācija
description: Šajā tēmā ir sniegta informācija par lapu Detalizēta informācija par darba rindām, kurā ir attēlots visaptverošs, kārtojams un filtrējams saraksts ar atsevišķām darba rindām jūsu sistēmā.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0cb182242a42443d5894b864523fc5f5fea9c5b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245110"
---
# <a name="work-line-details"></a><span data-ttu-id="94dde-103">Detalizēta darba rindas informācija</span><span class="sxs-lookup"><span data-stu-id="94dde-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94dde-104">Lapā **Detalizēta informācija par darba rindām** ir attēlots visaptverošs, kārtojams un filtrējams saraksts ar atsevišķām darba rindām jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="94dde-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="94dde-105">Tas sniedz pilnīgu pārskatu par noliktavā plānoto un izpildīto darbu.</span><span class="sxs-lookup"><span data-stu-id="94dde-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="94dde-106">Varat viegli pārslēgties starp visu darba rindu skatīšanu un tikai atvērto darba rindu skatīšanu.</span><span class="sxs-lookup"><span data-stu-id="94dde-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="94dde-107">Detalizētajā informācijā, kas tiek sniegta katrai rindai, ir ietverts darba statuss, krājuma kods, novietojums, darba daudzums, kravas ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="94dde-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="94dde-108">Līdzekļa Detalizēta informācija par darba rindu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="94dde-108">Turn on the work line details feature</span></span>

<span data-ttu-id="94dde-109">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="94dde-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="94dde-110">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="94dde-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="94dde-111">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="94dde-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="94dde-112">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="94dde-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="94dde-113">**Līdzekļa nosaukums:** *Detalizēta informācija par darba rindu*</span><span class="sxs-lookup"><span data-stu-id="94dde-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="94dde-114">Lapas Detalizēta informācija par darba rindu atvēršana un lietošana</span><span class="sxs-lookup"><span data-stu-id="94dde-114">Open and use the Work line details page</span></span>

<span data-ttu-id="94dde-115">Lai skatītu detalizētu informāciju par darba rindu sarakstu, atveriet **Noliktavas pārvaldība \> Darbs \> Detalizēta informācija par darba rindu**.</span><span class="sxs-lookup"><span data-stu-id="94dde-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="94dde-116">Šeit varat veikt tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="94dde-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="94dde-117">Lietojiet lauku **Filtrs**, lai meklētu rindas ar konkrētu vērtību jebkuram pieejamajam parametram.</span><span class="sxs-lookup"><span data-stu-id="94dde-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="94dde-118">(Pieejamajos parametros ietilpst daudzi parametri, kas režģī netiek rādīti kā kolonnas.)</span><span class="sxs-lookup"><span data-stu-id="94dde-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="94dde-119">Izmantojiet izvēles rūtiņu **Rādīt slēgto**, lai rādītu vai paslēptu slēgtās rindas.</span><span class="sxs-lookup"><span data-stu-id="94dde-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="94dde-120">Atlasiet **Rādīt dimensijas**, lai atvērtu dialoglodziņu **Dimensiju attēlojums**, kur varat izvēlēties režģī rādīt vai paslēpt dažādas dimensiju kolonnas.</span><span class="sxs-lookup"><span data-stu-id="94dde-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="94dde-121">Atlasiet jebkuras kolonnas virsrakstu, lai atvērtu izvēlni, kurā varat izvēlēties šajā kolonnā kārtot vai filtrēt sarakstu pēc vērtībām.</span><span class="sxs-lookup"><span data-stu-id="94dde-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="94dde-122">Atlasiet darba rindu un pēc tam atlasiet **Mainīt novietojumu**, lai atvērtu dialoglodziņu, kurā varēsit mainīt šīs darba rindas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="94dde-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="94dde-123">Jūsu norādītais novietojums pārlabos novietojuma direktīvas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="94dde-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="94dde-124">Atlasiet darba rindu un pēc tam atlasiet **Atcelt darba rindu**, lai atvērtu dialoglodziņu, kur varat daļēji vai pilnībā samazināt šīs darba rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="94dde-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="94dde-125">Koriģējiet daudzumus.</span><span class="sxs-lookup"><span data-stu-id="94dde-125">Adjust quantities.</span></span>
- <span data-ttu-id="94dde-126">Skatiet jebkurā darba rindā ietvertās darbības.</span><span class="sxs-lookup"><span data-stu-id="94dde-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="94dde-127">Līdzekļa izmēģināšana</span><span class="sxs-lookup"><span data-stu-id="94dde-127">Try out the feature</span></span>

<span data-ttu-id="94dde-128">Šajā sadaļā tiek piedāvāta demonstrācija no trīs daļām, kurā ir parādīts, kā strādāt ar detalizētu informāciju par darba rindu.</span><span class="sxs-lookup"><span data-stu-id="94dde-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="94dde-129">Padarīt pieejamus datu paraugus</span><span class="sxs-lookup"><span data-stu-id="94dde-129">Make sample data available</span></span>

<span data-ttu-id="94dde-130">Lai, izmantojot šo demonstrāciju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="94dde-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="94dde-131">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="94dde-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="94dde-132">Varat izmantot šo demonstrāciju arī kā vadlīnijas, strādājot ar ražošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="94dde-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="94dde-133">Tomēr jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.</span><span class="sxs-lookup"><span data-stu-id="94dde-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="94dde-134">Pārbaude, vai scenārija iestatījumos ir ietverts pietiekami daudz pieejamo krājumu</span><span class="sxs-lookup"><span data-stu-id="94dde-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="94dde-135">Ja strādājat ar **USMF** demonstrācijas datiem, vispirms pārliecinieties, vai sistēma ir iestatīta tā, lai katrā atbilstošajā vietā būtu pieejami pietiekami daudz krājumu.</span><span class="sxs-lookup"><span data-stu-id="94dde-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="94dde-136">Šajā demonstrācijā ir paredzēts, ka jums ir pieejami šādi krājumi:</span><span class="sxs-lookup"><span data-stu-id="94dde-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="94dde-137">**Krājums M9200:** 45 ea.</span><span class="sxs-lookup"><span data-stu-id="94dde-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="94dde-138">(vai vairāk)</span><span class="sxs-lookup"><span data-stu-id="94dde-138">(or more)</span></span>
- <span data-ttu-id="94dde-139">**Krājums M9202:** 10 ea.</span><span class="sxs-lookup"><span data-stu-id="94dde-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="94dde-140">(vai vairāk)</span><span class="sxs-lookup"><span data-stu-id="94dde-140">(or more)</span></span>

<span data-ttu-id="94dde-141">Veiciet šīs darbības, lai pārbaudītu, vai ir pieejams pietiekami daudz krājumu, un lai veiktu visas nepieciešamās korekcijas.</span><span class="sxs-lookup"><span data-stu-id="94dde-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="94dde-142">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Novietojuma direktīvas** un nosakiet, kuri izdošanas novietojumi ir izmantoti pārdošanas pasūtījuma izdošanai 51. noliktavā.</span><span class="sxs-lookup"><span data-stu-id="94dde-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="94dde-143">(Papildinformāciju skatiet šeit: [Noliktavas darba kontrolēšana, izmantojot darbu veidnes un novietojuma direktīvas](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="94dde-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="94dde-144">Pārbaudiet krājumu līmeņus atbilstošajos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="94dde-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="94dde-145">Pielāgojiet krājumus pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="94dde-145">Adjust inventory as required.</span></span> <span data-ttu-id="94dde-146">Varat izveidot manuālo kustību, izmantot papildināšanu vai lietot jebkuru citu plūsmu, lai koriģētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="94dde-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="94dde-147">1. daļa: izdošanas darba izveide</span><span class="sxs-lookup"><span data-stu-id="94dde-147">Part 1: Create picking work</span></span>

<span data-ttu-id="94dde-148">Pirms sākt darba izveidi, pārliecinieties, vai noliktava ir iestatīta, lai paredzētajā veidā atbilstu darba prasībām.</span><span class="sxs-lookup"><span data-stu-id="94dde-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="94dde-149">Lai izveidotu izdošanas darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="94dde-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="94dde-150">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="94dde-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="94dde-151">Atlasiet **Jauns**, lai atvērtu dialoglodziņu **Pārdošanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="94dde-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="94dde-152">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="94dde-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="94dde-153">Kopsavilkuma cilnē **Klients** iestatiet lauku **Klienta konts** uz _US-001_.</span><span class="sxs-lookup"><span data-stu-id="94dde-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="94dde-154">Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noliktava** uz _51_.</span><span class="sxs-lookup"><span data-stu-id="94dde-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="94dde-155">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="94dde-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="94dde-156">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="94dde-156">Your new sales order is opened.</span></span> <span data-ttu-id="94dde-157">Tajā ir ietverta jauna tukša rinda režģī **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="94dde-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="94dde-158">Šajā pasūtījuma rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="94dde-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="94dde-159">**Krājuma numurs:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="94dde-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="94dde-160">**Daudzums:** _20_</span><span class="sxs-lookup"><span data-stu-id="94dde-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="94dde-161">**Vienība:** _ea_</span><span class="sxs-lookup"><span data-stu-id="94dde-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="94dde-162">Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** atlasiet **Rezervācija**, lai atvēru lapu **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="94dde-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="94dde-163">Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="94dde-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="94dde-164">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="94dde-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="94dde-165">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="94dde-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="94dde-166">Sistēma izveido sūtījumu, pievieno to jaunajai kravai un izveido nepieciešamo darbu.</span><span class="sxs-lookup"><span data-stu-id="94dde-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="94dde-167">Tam pašam klienta kontam un noliktavai, ko izmantojāt pirmajā pasūtījumā, izveidojiet otru pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="94dde-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="94dde-168">Pievienojiet šim pasūtījumam šādas divas pasūtījuma rindas:</span><span class="sxs-lookup"><span data-stu-id="94dde-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="94dde-169">**1. rinda:** iestatiet lauku **Kravas numurs** uz _M9200_, lauku **Daudzums** uz _25_ un lauku **Vienība** uz _Katrs_.</span><span class="sxs-lookup"><span data-stu-id="94dde-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="94dde-170">**2. rinda:** iestatiet lauku **Kravas numurs** uz _M9202_, lauku **Daudzums** uz _10_ un lauku **Vienība** uz _Katrs_.</span><span class="sxs-lookup"><span data-stu-id="94dde-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="94dde-171">Atkārtojiet 6.–8. darbību, lai rezervētu krājumus katrai pasūtījuma rindai (pa vienai), un pēc tam atkārtojiet 9. darbību, lai izdotu pasūtījumu noliktavai.</span><span class="sxs-lookup"><span data-stu-id="94dde-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="94dde-172">2. daļa: darba rindai paredzētā novietojuma maiņa</span><span class="sxs-lookup"><span data-stu-id="94dde-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="94dde-173">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Detalizēta informācija par darba rindu**.</span><span class="sxs-lookup"><span data-stu-id="94dde-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="94dde-174">Atrodiet darba rindas, kuras izveidojāt šai demonstrācijai, un atlasiet vienu no tām.</span><span class="sxs-lookup"><span data-stu-id="94dde-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="94dde-175">Atlasiet **Mainīt novietojumu**, lai atvērtu dialoglodziņu **Jauna novietojuma atlase**.</span><span class="sxs-lookup"><span data-stu-id="94dde-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="94dde-176">Dialoglodziņā **Jauna novietojuma atlase** laukā **Novietojums** darba rindai atlasiet jaunu novietojumu.</span><span class="sxs-lookup"><span data-stu-id="94dde-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="94dde-177">Atlasiet **Labi**, lai izmaiņas piemērotu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="94dde-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94dde-178">Novietojuma izmaiņas varat iesniegt tikai tad, ja jaunajā novietojumā ir pieejami pietiekami daudz krājumu (izdošanai) vai tas atbilst novietojuma tipa pārbaudei (izvietošanai).</span><span class="sxs-lookup"><span data-stu-id="94dde-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="94dde-179">3. daļa: darba rindas daudzuma mainīšana vai darba rindas atcelšana</span><span class="sxs-lookup"><span data-stu-id="94dde-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="94dde-180">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Detalizēta informācija par darba rindu**.</span><span class="sxs-lookup"><span data-stu-id="94dde-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="94dde-181">Atrodiet darba rindas, kuras izveidojāt šai demonstrācijai, un atlasiet vienu no tām.</span><span class="sxs-lookup"><span data-stu-id="94dde-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="94dde-182">Ņemiet vērā, ka daudzumus varat atcelt vai mainīt tikai tām darba rindām, kur darba veids ir _izdošana_.</span><span class="sxs-lookup"><span data-stu-id="94dde-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="94dde-183">Atlasiet **Atcelt darba rindu**, lai atvērtu dialoglodziņu **Atceļamais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="94dde-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="94dde-184">Dialoglodziņā **Atceļamais daudzums** mainiet vērtību laukā **Daudzums**, lai norādītu daudzumu, kas *jāatņem no* rindai pašlaik norādītā daudzuma.</span><span class="sxs-lookup"><span data-stu-id="94dde-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="94dde-185">Pēc noklusējuma laukā **Daudzums** tiek rādīts viss daudzums.</span><span class="sxs-lookup"><span data-stu-id="94dde-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="94dde-186">Ja atcelsit visu daudzumu, vērtība **Darba statuss** tiks mainīta uz _Atcelts_, bet laukā **Darba daudzums** tiks rādīta sākotnējā vērtība.</span><span class="sxs-lookup"><span data-stu-id="94dde-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="94dde-187">Ja atcelsit tikai daļu daudzuma, lauks **Darba daudzums** tiks atjaunināts, lai rādītu jauno vērtību, bet vērtība **Darba statuss** netiks mainīta.</span><span class="sxs-lookup"><span data-stu-id="94dde-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="94dde-188">Atlasiet **Labi**, lai izmaiņas piemērotu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="94dde-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94dde-189">Ja darba rindai atcelsit tikai daļu daudzuma, no kravas rindas ir jānoņem arī novecojušais daudzums.</span><span class="sxs-lookup"><span data-stu-id="94dde-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="94dde-190">Pretējā gadījumā, ja netiek iestatīta pareiza nepietiekamas piegādes vērtība, kravas rindai nevar apstiprināt sūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="94dde-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]