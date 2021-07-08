---
title: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
description: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301309"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="b81bf-103">Nevar apstiprināt sūtījumu, jo nav izdoti krājumi</span><span class="sxs-lookup"><span data-stu-id="b81bf-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="b81bf-104">Kļūdas kods: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="b81bf-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="b81bf-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="b81bf-105">Symptoms</span></span>

<span data-ttu-id="b81bf-106">Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="b81bf-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="b81bf-107">Daļa noslodzei %1 nepieciešamo krājumu vēl nav izdoti un pārvietoti uz galīgo nosūtīšanas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="b81bf-108">Tādēļ kravas nosūtīšanu nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="b81bf-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="b81bf-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="b81bf-109">Cause</span></span>

<span data-ttu-id="b81bf-110">Kravu vai sūtījumu nevar apstiprināt tās pašreizējā stāvoklī, jo var pastāvēt viens no tālāk norādītajiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="b81bf-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="b81bf-111">Saistītais darbs vēl nav izdots un pārvietots uz beigu nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="b81bf-112">Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="b81bf-113">Izmantojot kopuma veidnes konteinerizāciju, novietojuma direktīva tika konfigurēta ar iepakošanas vietu kā galīgo nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="b81bf-114">Novēršana</span><span class="sxs-lookup"><span data-stu-id="b81bf-114">Resolution</span></span>

<span data-ttu-id="b81bf-115">Krava vai sūtījums pašlaik ir stāvoklī, kad sūtījuma apstiprināšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="b81bf-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="b81bf-116">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="b81bf-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="b81bf-117">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="b81bf-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="b81bf-118">Atceliet darba ID, kas izveidoti ar iepakošanas novietojumu kā galīgās nosūtīšanas vietu, pārkonfigurējiet novietojuma direktīvu un atkārtoti ielādējiet kravu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="b81bf-119">Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt</span><span class="sxs-lookup"><span data-stu-id="b81bf-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="b81bf-120">Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.</span><span class="sxs-lookup"><span data-stu-id="b81bf-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="b81bf-121">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b81bf-122">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="b81bf-123">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.</span><span class="sxs-lookup"><span data-stu-id="b81bf-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="b81bf-124">Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="b81bf-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="b81bf-125">Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="b81bf-126">Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.</span><span class="sxs-lookup"><span data-stu-id="b81bf-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="b81bf-127">Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.</span><span class="sxs-lookup"><span data-stu-id="b81bf-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="b81bf-128">Atceliet darba ID, kas izveidoti ar iepakošanas novietojumu kā galīgās nosūtīšanas vietu, pārkonfigurējiet novietojuma direktīvu un atkārtoti ielādējiet kravu</span><span class="sxs-lookup"><span data-stu-id="b81bf-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="b81bf-129">Izmantojiet šo procedūru, lai atceltu darba ID, kuru iepakošanas vieta ir galīgā izvietošanas vieta ar automatizētu konteinerizēšanu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="b81bf-130">Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="b81bf-131">Tiek atvērts dialogs **Atcelt darbu**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="b81bf-132">Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt.</span><span class="sxs-lookup"><span data-stu-id="b81bf-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="b81bf-133">Atlasītā darba ID vērtībai **Darba statuss** jābūt *Atvērts*, *Procesā*, *Atcelts*, *Apvienots* vai *Slēgts*.</span><span class="sxs-lookup"><span data-stu-id="b81bf-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="b81bf-134">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-134">Select **OK**.</span></span>
1. <span data-ttu-id="b81bf-135">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="b81bf-136">Pēc nepieciešamības, atkārtojiet šo procedūru pārējiem darba ID.</span><span class="sxs-lookup"><span data-stu-id="b81bf-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="b81bf-137">Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="b81bf-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="b81bf-138">Izmantojiet šo procedūru, lai pārkonfigurētu novietojuma direktīvu, jo, iestatot kopuma veidni, iepakošanas vieta netiks izmantota kā galīgā nosūtīšanas vieta.</span><span class="sxs-lookup"><span data-stu-id="b81bf-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="b81bf-139">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b81bf-140">Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="b81bf-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="b81bf-141">Atlasiet novietojuma direktīvu, ko izmantojat automatizētai konteinerizēšanai.</span><span class="sxs-lookup"><span data-stu-id="b81bf-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="b81bf-142">Kopsavilkuma cilnes rīkjoslā **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="b81bf-143">Vaicājumu redaktora dialogā cilnē **Diapazons** atrodiet rindu, kur **Lauks** ir iestatīts uz *Novietojuma profils*, un pārbaudiet, vai laukā **Kritēriji** rindai nav iestatīts novietojuma profils ar **Novietojuma veidu** *Iepakojums*.</span><span class="sxs-lookup"><span data-stu-id="b81bf-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="b81bf-144">Koriģēt lauku **Kritēriji**, lai labotu pēdējo izvietošanas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="b81bf-145">Izmantojiet šo procedūru, lai atkārtoti ielādētu kravu un izveidotu darba ID ar pareizo galīgo nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="b81bf-146">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="b81bf-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="b81bf-147">Sadaļā **Kravas** atrodiet kravu, kas ir jāizlaiž.</span><span class="sxs-lookup"><span data-stu-id="b81bf-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="b81bf-148">Sadaļas **Kravas** rīkjoslā atlasiet opciju **Pārvietot \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto kravu uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="b81bf-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="b81bf-149">Pēc nepieciešamības, atkārtojiet šo procedūru pārējam kravām.</span><span class="sxs-lookup"><span data-stu-id="b81bf-149">Repeat this procedure for the other loads as needed.</span></span>
