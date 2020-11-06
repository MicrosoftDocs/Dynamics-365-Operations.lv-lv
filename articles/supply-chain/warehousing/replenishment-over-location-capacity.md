---
title: Papildināšana, pārsniedzot vietas ietilpību
description: Šajā tēmā ir sniegta informācija par funkciju Papildināšana, pārsniedzot vietas ietilpību. Šī funkcija ļauj veikt visus papildināšanas darbus, kas būs nepieciešami šīs dienas izveidošanai, un pārvalda šī papildināšanas darba pieejamību, lai nodrošinātu, ka saņemšanas vieta neizbeidzas krājumi un tā nepārsniedz noslodzi.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8e9ae16fea892d1d6b6a6b5d06137576623e7f5b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016612"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="54215-104">Papildināšana, pārsniedzot vietas ietilpību</span><span class="sxs-lookup"><span data-stu-id="54215-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54215-105">Dažām lielizmēra noliktavām vai noliktavām ar ierobežotu telpu ir jānosūta vairāk krājuma daudzumu dienā, nekā tas ietilptu izdošanas vietā.</span><span class="sxs-lookup"><span data-stu-id="54215-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="54215-106">*Papildināšana, pārsniedzot vietas ietilpību* funkcija ļauj veikt visus papildināšanas darbus, kas būs nepieciešami šīs dienas izveidošanai, un pārvalda šī papildināšanas darba pieejamību, lai nodrošinātu, ka saņemšanas vieta neizbeidzas krājumi un tā nepārsniedz noslodzi.</span><span class="sxs-lookup"><span data-stu-id="54215-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="54215-107">Funkcija ļauj izveidot papildu papildināšanas darbu, nekā tas ietilptu atrašanās vietā, un tas bloķē papildināšanas darbus no pabeigšanas, ja vieta ir pilna.</span><span class="sxs-lookup"><span data-stu-id="54215-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="54215-108">Tā kā krājumu līmenis izdošanas vietā nokrītas zem konfigurējama sliekšņa, tiek darīts lielāks papildināšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="54215-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="54215-109">Ieslēgt Papildināšana, pārsniedzot vietas ietilpību funkciju</span><span class="sxs-lookup"><span data-stu-id="54215-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="54215-110">Lai padarītu šo līdzekli pieejamu, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):</span><span class="sxs-lookup"><span data-stu-id="54215-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="54215-111">Organizācijas mēroga darba aizturēšana</span><span class="sxs-lookup"><span data-stu-id="54215-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="54215-112">Papildināšana, pārsniedzot vietas ietilpību</span><span class="sxs-lookup"><span data-stu-id="54215-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="54215-113">Iestatīt līdzekli piemēra scenārijam</span><span class="sxs-lookup"><span data-stu-id="54215-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="54215-114">Šajā sadaļā ir sniegti norādījumi un piemērs, kas parāda, kā iestatīt šo funkciju un sagatavot parauga datus piemēru scenārijam, kas sniegts tālāk šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="54215-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="54215-115">Iespējot datu paraugu</span><span class="sxs-lookup"><span data-stu-id="54215-115">Enable sample data</span></span>

<span data-ttu-id="54215-116">Lai, izmantojot šo [scenārija piemēru](#example-scenario), strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="54215-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="54215-117">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="54215-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="54215-118">Novietojuma profils</span><span class="sxs-lookup"><span data-stu-id="54215-118">Location profile</span></span>

<span data-ttu-id="54215-119">Iespējot papildināt, pārsniedzot vietas ietilpību, funkcionalitāti novietojumu profilā.</span><span class="sxs-lookup"><span data-stu-id="54215-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="54215-120">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojumu profili**.</span><span class="sxs-lookup"><span data-stu-id="54215-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="54215-121">Kreisajā rūtī atlasiet **PICK-06**.</span><span class="sxs-lookup"><span data-stu-id="54215-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="54215-122">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="54215-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="54215-123">Kopsavilkuma cilnē **Papildināšana** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="54215-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="54215-124">**Pārsniegt novietojuma noslodzi:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="54215-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="54215-125">Iespējojot, tiks atļauts pārsniegt vietas maksimālo noslodzi, izmantojot papildināšana darbu.</span><span class="sxs-lookup"><span data-stu-id="54215-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="54215-126">Tas arī iespējo citus laukus kopsavilkuma cilnē **Papildināšana**.</span><span class="sxs-lookup"><span data-stu-id="54215-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="54215-127">**Darba pieejamības sliekšņa tips:** *Daudzums*</span><span class="sxs-lookup"><span data-stu-id="54215-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="54215-128">Šis lauks definē metodi, kas tiek izmantota, lai noteiktu, kad ir jānodod vairāk darba.</span><span class="sxs-lookup"><span data-stu-id="54215-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="54215-129">Varat atbrīvot vai nu pēc daudzuma, vai procentiem:</span><span class="sxs-lookup"><span data-stu-id="54215-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="54215-130">*Procenti* – Atlasiet šo opciju, lai izmantotu procentuālo noslodzi, kas ir balstīta uz krājumu ierobežojumiem vai tilpumiem.</span><span class="sxs-lookup"><span data-stu-id="54215-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="54215-131">Atlasot šo opciju, tiek aktivizēts **Pārpildes procentu** lauks un tiek atspējoti divi ar daudzumu saistīti lauki **Pārpildes daudzums** un **Pārpildes vienība**.</span><span class="sxs-lookup"><span data-stu-id="54215-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="54215-132">Šo opciju var izmantot, ja izdošanas vietas izmanto tilpumus.</span><span class="sxs-lookup"><span data-stu-id="54215-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="54215-133">Ja šī opcija ir atlasīta, iestatiet **Pārpildes procentu** lauku uz procentuālo daļu, pie kuras papildu papildināšanas darbs būs pieejams.</span><span class="sxs-lookup"><span data-stu-id="54215-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="54215-134">*Daudzums* - Atlasiet šo opciju, lai izmantotu specifisku daudzuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="54215-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="54215-135">Atlasot šo opciju, tiek deaktivizēts **Pārpildes procentu** lauks un tiek iespējoti lauki **Pārpildes daudzums** un **Pārpildes vienība**.</span><span class="sxs-lookup"><span data-stu-id="54215-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="54215-136">Izmantojiet šo opciju, ja nelietojat apjoma datus par novietojumiem, kuri tiek papildināti, vai ja jums ir nemainīgi daudzumi, par kuriem vēlaties, lai uz vietas tiktu nogādāti vairāk krājumu.</span><span class="sxs-lookup"><span data-stu-id="54215-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="54215-137">Ja šī opcija ir atlasīta, iestatiet **Pārpildes daudzumu** un **Pārpildes vienības** laukus uz daudzumu un mērvienību, kādā būs pieejams papildu papildināšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="54215-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="54215-138">**Pārpildes daudzums:** *0.65*</span><span class="sxs-lookup"><span data-stu-id="54215-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="54215-139">Šis lauks nosaka daudzumu, pie kura notiek novietojuma pārplūšana.</span><span class="sxs-lookup"><span data-stu-id="54215-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="54215-140">Darbs būs pieejams ikreiz, kad rīcībā esošo daudzumu summa novietojumā un darba daudzums būs zemāks par šo vērtību.</span><span class="sxs-lookup"><span data-stu-id="54215-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="54215-141">Jebkurš papildināšanas darbs virs šīs vērtības tiks bloķēts, un tas būs jāatbloķē manuāli.</span><span class="sxs-lookup"><span data-stu-id="54215-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="54215-142">Novietojuma krājumu limiti tiek ņemti vērā, aprēķinot darba daudzumu.</span><span class="sxs-lookup"><span data-stu-id="54215-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="54215-143">**Pārpildes vienība:** *PL*</span><span class="sxs-lookup"><span data-stu-id="54215-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="54215-144">Šis lauks nosaka vienību, kas ir saistīta ar pārpildes daudzumu.</span><span class="sxs-lookup"><span data-stu-id="54215-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="54215-145">Šādā gadījumā papildu papildināšanas darbs būs pieejams, kad novietojumā līmenis samazinās uz 0,65 paletēm (PL).</span><span class="sxs-lookup"><span data-stu-id="54215-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="54215-146">**Pārpildes procentuālā vērtība**</span><span class="sxs-lookup"><span data-stu-id="54215-146">**Overflow percentage**</span></span>

        <span data-ttu-id="54215-147">Šis lauks nosaka procentuālo daudzumu, pie kura notiek novietojuma pārplūšana.</span><span class="sxs-lookup"><span data-stu-id="54215-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="54215-148">Darbs būs pieejams ikreiz, kad rīcībā esošo daudzumu summa novietojumā un darba daudzums būs zemāks par šo procentuālo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="54215-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="54215-149">Jebkura papildināšanas darba daudzuma procentuālā vērtība virs šīs vērtības tiks bloķēta, un tā būs jāatbloķē manuāli.</span><span class="sxs-lookup"><span data-stu-id="54215-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="54215-150">Novietojuma krājumu limiti tiek ņemti vērā, aprēķinot darba procentuālo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="54215-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="54215-151">Ja nav definēts neviens rīcībā esošo krājumu ierobežojums, darba daudzuma procentuālā vērtība tiks aprēķināta pēc tilpuma, ja novietojuma profilā ir definēti tilpuma ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="54215-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54215-152">Ja jūs izmantojat demonstrācijas datus **USMF** juridiskajai personai un iepriekš ieslēdzāt *Novietojuma numura zīmes pozicionēšanas* līdzekli, jums ir jāizslēdz opcija **Iespējot numura zīmes pozicionēšanas** iestatījumu **BULK-06** novietojuma profilā, lai pabeigtu mobilās darbības piemēru scenārijā.</span><span class="sxs-lookup"><span data-stu-id="54215-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="54215-153">Kopuma darbības kods</span><span class="sxs-lookup"><span data-stu-id="54215-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="54215-154">Lai iestatītu kopuma soļa kodu atbilstoši šeit aprakstītajam, varat vispirms izmantot [funkciju pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu līdzekli vārdā *Organizācijas plašu kopuma soļa kods*.</span><span class="sxs-lookup"><span data-stu-id="54215-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="54215-155">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma darbību kodi**.</span><span class="sxs-lookup"><span data-stu-id="54215-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="54215-156">Atlasiet **Jauns** , un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="54215-156">Select **New** , and set the following values:</span></span>

    - <span data-ttu-id="54215-157">**Kopuma darbības kods:** *Replen*</span><span class="sxs-lookup"><span data-stu-id="54215-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="54215-158">**Kopuma darbības apraksts:** *Papildināšana*</span><span class="sxs-lookup"><span data-stu-id="54215-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="54215-159">**Kopuma darbības veids:** *Papildināšana*</span><span class="sxs-lookup"><span data-stu-id="54215-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="54215-160">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54215-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="54215-161">Papildināšanas veidne</span><span class="sxs-lookup"><span data-stu-id="54215-161">Replenishment template</span></span>

<span data-ttu-id="54215-162">Papildināšanas veidnes ir kārtulu kopa, kas kontrolē novietojuma papildināšanas laiku un veidu.</span><span class="sxs-lookup"><span data-stu-id="54215-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="54215-163">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes**.</span><span class="sxs-lookup"><span data-stu-id="54215-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="54215-164">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="54215-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="54215-165">Sadaļā **Pārskats** atlasiet rindu, kur lauks **Papildināt veidni** ir iestatīts uz *Pieprasīt papildināšanu*.</span><span class="sxs-lookup"><span data-stu-id="54215-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="54215-166">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="54215-166">Set the following values:</span></span>

    - <span data-ttu-id="54215-167">**Kopuma darbības kods:** *Replen*</span><span class="sxs-lookup"><span data-stu-id="54215-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="54215-168">**Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus**  — *Jā*</span><span class="sxs-lookup"><span data-stu-id="54215-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="54215-169">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54215-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="54215-170">Kopuma veidne</span><span class="sxs-lookup"><span data-stu-id="54215-170">Wave template</span></span>

1. <span data-ttu-id="54215-171">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="54215-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="54215-172">Kreisajā rūtī lauku **Kopuma veidnes tips** iestatiet vērtību *Sūtīšana*.</span><span class="sxs-lookup"><span data-stu-id="54215-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="54215-173">Atlasiet sarakstā veidni **61 Sūtīšana**</span><span class="sxs-lookup"><span data-stu-id="54215-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="54215-174">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="54215-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="54215-175">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Automātiskās papildināšanas darba laidiens** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="54215-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="54215-176">Iestatiet šo opciju uz *Jā* , lai izveidotu uz pieprasījuma balstītu papildināšanas darbu un automātiski to izlaistu.</span><span class="sxs-lookup"><span data-stu-id="54215-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="54215-177">Jums ir jāpievieno papildināšanas kopuma metode kopuma veidnei un jāizveido papildināšanas veidne **Kopuma pieprasījuma** tipam.</span><span class="sxs-lookup"><span data-stu-id="54215-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="54215-178">Iestatiet papildināšanas veidni lapā **Papildināšanas veidnes**.</span><span class="sxs-lookup"><span data-stu-id="54215-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="54215-179">Lai iestatītu papildināšanas veidni, ir jāpievieno papildināšanas metode laidiena veidnei.</span><span class="sxs-lookup"><span data-stu-id="54215-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="54215-180">Kopsavilkuma cilnē **Metodes** kolonnā **Atlasītās metodes** atrodama šāda rinda:</span><span class="sxs-lookup"><span data-stu-id="54215-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="54215-181">**Metodes nosaukums:** *papildināt*</span><span class="sxs-lookup"><span data-stu-id="54215-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="54215-182">**Nosaukums:** *Papildināšana*</span><span class="sxs-lookup"><span data-stu-id="54215-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="54215-183">Iestatiet lauku **Kopuma soļa kods** šai rindai uz *Replen*.</span><span class="sxs-lookup"><span data-stu-id="54215-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="54215-184">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54215-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="54215-185">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="54215-185">Example scenario</span></span>

<span data-ttu-id="54215-186">Pēc tam, kad esat veicis visus iepriekš aprakstītos, pieejamos parauga datus un to iestatījis, varat strādāt ar šo scenāriju, lai izmēģinātu *Papildināšana, pārsniedzot vietas ietilpību* funkciju.</span><span class="sxs-lookup"><span data-stu-id="54215-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="54215-187">Šajā scenārijā parādītās vērtības pieņem, ka strādājat ar standarta demonstrācijas datiem, ar kuriem atlasījāt **USMF** juridisko personu un ka sagatavojāt parauga ierakstus, kas ir aprakstīti iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="54215-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="54215-188">Šis scenārijs kalpo arī kā piemērs, kas parāda, kā līdzekli var izmantot ražošanas iestatījumā.</span><span class="sxs-lookup"><span data-stu-id="54215-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="54215-189">Izveidot papildināšanas darbu</span><span class="sxs-lookup"><span data-stu-id="54215-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="54215-190">1. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="54215-190">Create sales order 1</span></span>

1. <span data-ttu-id="54215-191">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="54215-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="54215-192">Darbību rūtī atlasiet **Jauns** , lai atvērtu dialoglodziņu jauna pārdošanas pasūtījuma izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="54215-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="54215-193">Dialoglodziņā iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="54215-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="54215-194">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="54215-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="54215-195">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="54215-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="54215-196">Atlasiet **Labi** , lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="54215-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="54215-197">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="54215-197">The new sales order is opened.</span></span> <span data-ttu-id="54215-198">Tajā ir ietverta jauna, tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="54215-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="54215-199">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="54215-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="54215-200">**Krājuma numurs:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="54215-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="54215-201">**Daudzums:** *40*</span><span class="sxs-lookup"><span data-stu-id="54215-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="54215-202">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="54215-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="54215-203">Lapā **Rezervācija** atlasiet **Rezervēt vietu**.</span><span class="sxs-lookup"><span data-stu-id="54215-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="54215-204">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54215-204">Close the page.</span></span>
1. <span data-ttu-id="54215-205">Cilnē **Noliktava** , kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="54215-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="54215-206">Tiks saņemts informatīvi ziņojumi, kurā norādīts izveidotais kopuma ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="54215-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="54215-207">Tiek izveidots arī papildināšanas kopums.</span><span class="sxs-lookup"><span data-stu-id="54215-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="54215-208">Jūs saņemat arī brīdinājuma ziņojumu, kurā teikts: "Darba ID XXXX nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."</span><span class="sxs-lookup"><span data-stu-id="54215-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="54215-209">2. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="54215-209">Create sales order 2</span></span>

1. <span data-ttu-id="54215-210">Lapā **Visi pārdošanas pasūtījumi** atlasiet **Jauns** , lai atvērtu dialoglodziņu jauna pārdošanas pasūtījuma izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="54215-210">On the **All sales orders** , page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="54215-211">Dialoglodziņā iestatiet tālāk norādīto vērtību:</span><span class="sxs-lookup"><span data-stu-id="54215-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="54215-212">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="54215-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="54215-213">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="54215-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="54215-214">Atlasiet **Labi** , lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="54215-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="54215-215">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="54215-215">The new sales order is opened.</span></span> <span data-ttu-id="54215-216">Tajā ir ietverta jauna, tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="54215-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="54215-217">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="54215-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="54215-218">**Krājuma numurs:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="54215-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="54215-219">**Daudzums:** *60*</span><span class="sxs-lookup"><span data-stu-id="54215-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="54215-220">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="54215-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="54215-221">Lapā **Rezervācija** atlasiet **Rezervēt vietu**.</span><span class="sxs-lookup"><span data-stu-id="54215-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="54215-222">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54215-222">Close the page.</span></span>
1. <span data-ttu-id="54215-223">Cilnē **Noliktava** , kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="54215-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="54215-224">Tiks saņemts informatīvi ziņojumi, kurā norādīts izveidotais kopuma ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="54215-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="54215-225">Tiek izveidots arī papildināšanas kopums.</span><span class="sxs-lookup"><span data-stu-id="54215-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="54215-226">Jūs saņemat arī brīdinājuma ziņojumu, kurā teikts: "Darba ID XXXX nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."</span><span class="sxs-lookup"><span data-stu-id="54215-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="54215-227">3. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="54215-227">Create sales order 3</span></span>

1. <span data-ttu-id="54215-228">Lapā **Visi pārdošanas pasūtījumi** atlasiet **Jauns** , lai atvērtu dialoglodziņu jauna pārdošanas pasūtījuma izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="54215-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="54215-229">Dialoglodziņā iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="54215-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="54215-230">**Debitora konts:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="54215-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="54215-231">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="54215-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="54215-232">Atlasiet **Labi** , lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="54215-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="54215-233">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="54215-233">The new sales order is opened.</span></span> <span data-ttu-id="54215-234">Tajā ir ietverta jauna, tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="54215-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="54215-235">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="54215-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="54215-236">**Krājuma numurs:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="54215-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="54215-237">**Daudzums:** *30*</span><span class="sxs-lookup"><span data-stu-id="54215-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="54215-238">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="54215-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="54215-239">Lapā **Rezervācija** atlasiet **Rezervēt vietu**.</span><span class="sxs-lookup"><span data-stu-id="54215-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="54215-240">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54215-240">Close the page.</span></span>
1. <span data-ttu-id="54215-241">Cilnē **Noliktava** , kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="54215-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="54215-242">Tiks saņemts informatīvi ziņojumi, kurā norādīts izveidotais kopuma ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="54215-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="54215-243">Tiek izveidots arī papildināšanas kopums.</span><span class="sxs-lookup"><span data-stu-id="54215-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="54215-244">Jūs saņemat arī brīdinājuma ziņojumu, kurā teikts: "Darba ID XXXX nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."</span><span class="sxs-lookup"><span data-stu-id="54215-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="54215-245">Skatīt detalizētu informāciju par darbu</span><span class="sxs-lookup"><span data-stu-id="54215-245">View work details</span></span>

1. <span data-ttu-id="54215-246">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="54215-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="54215-247">Sadaļā **Pārskats** filtrējiet **Noliktavas** kolonnu noliktavai *61*.</span><span class="sxs-lookup"><span data-stu-id="54215-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="54215-248">Ir jāredz, ka trīs pieprasījumu pārdošanas pasūtījumiem tika izveidoti septiņi darba ID.</span><span class="sxs-lookup"><span data-stu-id="54215-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="54215-249">Trijiem no septiņiem darba ID ir **Darba pasūtījuma tipa** vērtība no *Papildināšanas* , un četriem ir **Darba pasūtījuma tipa** vērtība no *Pārdošanas pasūtījumiem*.</span><span class="sxs-lookup"><span data-stu-id="54215-249">Three of the seven work IDs have a **Work order type** value of *Replenishment* , and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="54215-250">Visiem trim darbu ID, kuru **Darba pasūtījuma tipa** vērtība no *Papildināšanas* ir vienāda ar *Saņemšanu* un *Izvietošanu* sadaļā **Rindas** :</span><span class="sxs-lookup"><span data-stu-id="54215-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="54215-251">**Saņemt:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="54215-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="54215-252">**Izvietot:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="54215-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="54215-253">Pārdošanas pasūtījumam 1 tika izveidoti divi darba ID.</span><span class="sxs-lookup"><span data-stu-id="54215-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="54215-254">Pierakstiet darba ID katram pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="54215-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="54215-255">Atkarībā no rīcībā esošajiem daudzumiem izveidotie darba daudzumi var nedaudz atšķirties.</span><span class="sxs-lookup"><span data-stu-id="54215-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="54215-256">Tomēr kopumā izveidotajiem darba virsrakstiem ir jāatbilst šim scenārija paraugam.</span><span class="sxs-lookup"><span data-stu-id="54215-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="54215-257">Rīcībā esošo krājumu numura zīmes ID</span><span class="sxs-lookup"><span data-stu-id="54215-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="54215-258">Vēlāk šajā scenārijā jūs izmantosiet noliktavas programmu (vai emulatoru), kur ir jāidentificē numura zīme, lai pabeigtu izdošanas un papildināšanas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="54215-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="54215-259">Lai atrastu numura zīmes ID, kas būs nepieciešams vēlāk, veiciet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="54215-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="54215-260">Dodieties uz **Krājumu vadība \> Uzziņas un atskaites \> Rīcībā esošie krājumu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="54215-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="54215-261">Atlasiet pogu **Rādīt filtrus** , lai atvērtu filtra rūti.</span><span class="sxs-lookup"><span data-stu-id="54215-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="54215-262">Lai iegūtu scenārijam numura zīmes, ievadiet tālāk norādītos filtrēšanas kritērijus.</span><span class="sxs-lookup"><span data-stu-id="54215-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="54215-263">Izmantojiet filtru *sākt ar*.</span><span class="sxs-lookup"><span data-stu-id="54215-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="54215-264">**Krājuma numurs:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="54215-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="54215-265">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="54215-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="54215-266">Atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="54215-266">Select **Apply**.</span></span>
1. <span data-ttu-id="54215-267">Darbību rūtī atlasiet **Dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="54215-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="54215-268">Dialoglodziņā **Dimensiju rādīšana** sadaļā **Noliktavas dimensijas** atlasiet visas vērtības.</span><span class="sxs-lookup"><span data-stu-id="54215-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="54215-269">Sadaļā **Darbības** atlasiet **Krājuma kods** un **Daudzums \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="54215-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="54215-270">Kad esat pabeidzis, atlasiet **Labi** , lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="54215-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="54215-271">**Rīcībā esošais** režģis rāda unikāls noliktavas vienības identifikatorus krājumam *T0100* katrā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="54215-272">Pierakstiet numura zīmi, kas atrodas katrā novietojumā, jo šī informācija būs nepieciešama vēlāk.</span><span class="sxs-lookup"><span data-stu-id="54215-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="54215-273">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54215-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="54215-274">Procesa darbības</span><span class="sxs-lookup"><span data-stu-id="54215-274">Process steps</span></span>

<span data-ttu-id="54215-275">Pirmajos divos darba ID tiks veikta noliktavas novietojuma papildināšana.</span><span class="sxs-lookup"><span data-stu-id="54215-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="54215-276">Darbs pie trešā papildināšanas darba tiks bloķēts, līdz krājumu līmenis izdošanas vietā nokrītas zem sliekšņa.</span><span class="sxs-lookup"><span data-stu-id="54215-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="54215-277">Papildināšana</span><span class="sxs-lookup"><span data-stu-id="54215-277">Replenishment</span></span>

1. <span data-ttu-id="54215-278">Pierakstieties noliktavas programmā kā lietotājs noliktavā *61*.</span><span class="sxs-lookup"><span data-stu-id="54215-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="54215-279">(Ievadiet *61* kā lietotāja ID un *1* kā paroli.)</span><span class="sxs-lookup"><span data-stu-id="54215-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="54215-280">Doties uz **Krājumi \> Papildināšana**.</span><span class="sxs-lookup"><span data-stu-id="54215-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="54215-281">Jūs tiekat aicināts pabeigt pirmo papildināšanas darbu.</span><span class="sxs-lookup"><span data-stu-id="54215-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="54215-282">Tiek parādīts krājuma kods, daudzums, novietojumu, no kura izdot.</span><span class="sxs-lookup"><span data-stu-id="54215-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="54215-283">Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="54215-284">Atlasiet pogu **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="54215-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="54215-285">Sistēma ģenerē mērķa unikālo noliktavas vienības identifikatoru jaunajai numura zīmei izdotajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="54215-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="54215-286">Lai apstiprinātu vērtību, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="54215-287">Izvietošanas darbs, kas uzdod lietotājam izvietot mērķa numura zīmi papildināšanas novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="54215-288">*Izvietošanas* novietojumam jābūt **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="54215-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="54215-289">Apstipriniet detalizētu informāciju par izvietošanu un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="54215-290">Tiek parādīts ziņojums "Darbs pabeigts" un nākamās papildināšanas izdošanas uzdevuma detaļas: krājuma numurs, daudzums un novietojums, no kura izvieto.</span><span class="sxs-lookup"><span data-stu-id="54215-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="54215-291">Izvietošanas novietojums būs vienāds ar pirmo papildināšanas novietojumu.</span><span class="sxs-lookup"><span data-stu-id="54215-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="54215-292">Tāpēc numura zīmei būs tas pats numura zīmes ID, kas tika izmantots pirmajam papildināšanas darba uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="54215-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="54215-293">Atkārtojiet iepriekšējās darbības, lai pabeigtu otrā darba uzdevuma papildināšanas darbu.</span><span class="sxs-lookup"><span data-stu-id="54215-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="54215-294">Daudzums un mērķa numura zīme atšķirsies no daudzuma un mērķa numura zīmes pirmajam darba uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="54215-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="54215-295">Kad otrais papildināšanas darbs ir pabeigts, jūs saņemat ziņojumu "Darbs pabeigts".</span><span class="sxs-lookup"><span data-stu-id="54215-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="54215-296">Mobilā ierīce arī informē, ka nav pieejams darbs, kaut arī saglabājas daži papildināšanas darbi.</span><span class="sxs-lookup"><span data-stu-id="54215-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="54215-297">Šī problēma rodas tādēļ, ka papildināšanas darbam ir *Aizturēts* pieejamības statuss, tāpēc tas ir atzīmēts kā **Bloķēts**.</span><span class="sxs-lookup"><span data-stu-id="54215-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="54215-298">*Aizturētais* statuss tika izraisīts, jo novietojuma profils saņemšanas novietojumam, kuram darbs tiek piešķirts, ir **Pārpildes daudzuma** vērtība *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="54215-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="54215-299">Divi iepriekšējie papildināšanas darba uzdevumi pildīja atrašanās vietu gandrīz līdz tā pārpildes ierobežojumam krājumam *T0100*.</span><span class="sxs-lookup"><span data-stu-id="54215-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="54215-300">(Vienības pārveidošana krājumam ir *1 PL = 100 ea*.) Tāpēc atlikušā papildināšanas darba rezultātā novietojums pārsniegtu pārpildes robežu.</span><span class="sxs-lookup"><span data-stu-id="54215-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="54215-301">Kamēr no novietojuma netiks izdots pietiekami daudz krājumu, lai mobilās ierīces izvēlnes vienumā tas nepārsniegtu darba atbrīvošanas slieksni, šis papildināšanas darbs paliks bloķēts.</span><span class="sxs-lookup"><span data-stu-id="54215-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="54215-302">Pārdošanas pasūtījums saņemšana</span><span class="sxs-lookup"><span data-stu-id="54215-302">Sales order pick</span></span>

<span data-ttu-id="54215-303">Pirms atlikušo papildināšanas darba uzdevumu var pabeigt, izdošanas novietojums ir jāsamazina līdz līmenim, kurā atlikušo papildināšanas darbu var atbloķēt.</span><span class="sxs-lookup"><span data-stu-id="54215-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="54215-304">Citiem vārdiem sakot, rīcībā esošo krājumu daudzuma summa novietojumā un papildināšanas daudzums nedrīkst pārsniegt **Pārpildes daudzuma** vērtību.</span><span class="sxs-lookup"><span data-stu-id="54215-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="54215-305">Ja šī summa ir mazāka nekā pārpildes daudzums, atlikušais papildināšanas darbs tiks atbloķēts.</span><span class="sxs-lookup"><span data-stu-id="54215-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="54215-306">Pierakstieties noliktavas programmā kā lietotājs noliktavā *61*.</span><span class="sxs-lookup"><span data-stu-id="54215-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="54215-307">(Ievadiet *61* kā lietotāja ID un *1* kā paroli.)</span><span class="sxs-lookup"><span data-stu-id="54215-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="54215-308">Doties uz **Izejošs \> Pārdošanas saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="54215-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="54215-309">Ievadiet pirmo darba ID pārdošanas pasūtījumam 1.</span><span class="sxs-lookup"><span data-stu-id="54215-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="54215-310">Skatiet to pārdošanas pasūtījumu darba ID, kurus esat veicis iepriekš **Darba informācijas** lapā.</span><span class="sxs-lookup"><span data-stu-id="54215-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="54215-311">Šeit ievadītais darba ID ģenerēs izdošanas darbu daudzumam 10 EA no diviem atsevišķiem novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="54215-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="54215-312">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-312">Select **OK**.</span></span>

    <span data-ttu-id="54215-313">Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums, no kura izvēlēties pirmo atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="54215-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="54215-314">Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="54215-315">Atlasiet pogu **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="54215-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="54215-316">Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums, no kura izvēlēties nākamo atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="54215-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="54215-317">Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="54215-318">Atlasiet pogu **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="54215-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="54215-319">**Pārdošanas pasūtījumi: izdošana** lapa, kas dod jums iespēju izdot abus pabeigtos saņemšanas darbus uz izejošo sagatavošanas posmu norises vietu.</span><span class="sxs-lookup"><span data-stu-id="54215-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="54215-320">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-320">Select **OK**.</span></span>

    <span data-ttu-id="54215-321">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="54215-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="54215-322">Ievadiet otro darba ID pārdošanas pasūtījumam 1.</span><span class="sxs-lookup"><span data-stu-id="54215-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="54215-323">Šim darba ID ir tikai viens saņemšanas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="54215-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="54215-324">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-324">Select **OK**.</span></span>

    <span data-ttu-id="54215-325">Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums.</span><span class="sxs-lookup"><span data-stu-id="54215-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="54215-326">Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="54215-327">Norādītā numura zīme būs viena no sistēmas ģenerētajām numura zīmēm no papildināšanas darba uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="54215-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="54215-328">Lai pārliecinātos, ka uztverat pareizo numura zīmes ID, pārbaudiet krājumus **Rīcībā esošā saraksta** lapā krājumam, novietojumam un daudzumam.</span><span class="sxs-lookup"><span data-stu-id="54215-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="54215-329">Atlasiet pogu **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="54215-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="54215-330">Apstipriniet norādījumus par izdošanas uzdevumu uz izejošo sagatavošanas posmu novietojumu.</span><span class="sxs-lookup"><span data-stu-id="54215-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="54215-331">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-331">Select **OK**.</span></span>

    <span data-ttu-id="54215-332">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="54215-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="54215-333">Pārdošanas pasūtījums 2 ir bloķēts no saņemšanas, jo papildināšanas uzdevums, ar kuru tas ir saistīts, nav pabeigts.</span><span class="sxs-lookup"><span data-stu-id="54215-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="54215-334">Pašlaik izdošanas vietā joprojām ir 30 ea daudzums, un pārdošanas pasūtījumam 2 papildināšanas daudzums ir 60 EA.</span><span class="sxs-lookup"><span data-stu-id="54215-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="54215-335">Rīcībā esošo krājumu un papildināšanas krājumu summa (90 ea) pārsniedz pārpildes daudzumu 0,65 PL (vai 65 ea).</span><span class="sxs-lookup"><span data-stu-id="54215-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="54215-336">Pirms papildināšanas darbu var pabeigt, ir jāsaņem pārdošanas pasūtījums 3.</span><span class="sxs-lookup"><span data-stu-id="54215-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="54215-337">Ievadiet darba ID pārdošanas pasūtījumam 3.</span><span class="sxs-lookup"><span data-stu-id="54215-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="54215-338">Šim darba ID ir tikai viens saņemšanas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="54215-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="54215-339">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-339">Select **OK**.</span></span>

    <span data-ttu-id="54215-340">Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums.</span><span class="sxs-lookup"><span data-stu-id="54215-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="54215-341">Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="54215-342">Norādītā numura zīme būs viena no sistēmas ģenerētajām numura zīmēm no papildināšanas darba uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="54215-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="54215-343">Lai pārliecinātos, ka uztverat pareizo numura zīmes ID, pārbaudiet krājumus **Rīcībā esošā saraksta** lapā krājumam, novietojumam un daudzumam.</span><span class="sxs-lookup"><span data-stu-id="54215-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="54215-344">Atlasiet pogu **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="54215-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="54215-345">Apstipriniet norādījumus par izdošanas uzdevumu uz izejošo sagatavošanas posmu novietojumu.</span><span class="sxs-lookup"><span data-stu-id="54215-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="54215-346">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-346">Select **OK**.</span></span>

    <span data-ttu-id="54215-347">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="54215-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="54215-348">Tiklīdz rīcībā esošo krājumu summa saņemšanas vietā un papildināšanas daudzums ir zem robežas, būs iespējams apstrādāt atlikušo papildināšanas darbu.</span><span class="sxs-lookup"><span data-stu-id="54215-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="54215-349">Atgriezieties **Darba informācijas** lapā un ievērojiet, ka papildināšanas darba pieejamība pēdējai papildināšanas vienībai (pārdošanas pasūtījumam 2) ir *Atvērta* , jo atrašanās vietā tagad ir pietiekami daudz vietas, lai akceptētu papildināšanu.</span><span class="sxs-lookup"><span data-stu-id="54215-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open* , because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="54215-350">Tagad varat apstrādāt šo papildināšanas darbu ar mobilās ierīces starpniecību.</span><span class="sxs-lookup"><span data-stu-id="54215-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="54215-351">Doties uz **Krājumi \> Papildināšana**.</span><span class="sxs-lookup"><span data-stu-id="54215-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="54215-352">Jūs tiekat aicināts pabeigt atlikušo papildināšanas darbu.</span><span class="sxs-lookup"><span data-stu-id="54215-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="54215-353">Tiek parādīts krājuma kods, daudzums, novietojumu, no kura izdot.</span><span class="sxs-lookup"><span data-stu-id="54215-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="54215-354">Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="54215-355">Atlasiet pogu **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="54215-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="54215-356">Sistēma ģenerē mērķa unikālo noliktavas vienības identifikatoru jaunajai numura zīmei izdotajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="54215-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="54215-357">Lai apstiprinātu vērtību, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="54215-358">Izvietošanas darbs, kas uzdod lietotājam izvietot mērķa numura zīmi papildināšanas novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="54215-359">*Izvietošanas* novietojumam jābūt **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="54215-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="54215-360">Apstipriniet detalizētu informāciju par izvietošanu un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="54215-361">Tiek saņemti ziņojumi "Darbs pabeigts" un "Nav pieejams darbs".</span><span class="sxs-lookup"><span data-stu-id="54215-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="54215-362">Tagad varat saņemt 2. pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="54215-362">You can now pick sales order 2.</span></span> <span data-ttu-id="54215-363">Tas kļuva atbloķēts, kad tika pabeigts papildināšanas darbs, kas ir saistīts ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="54215-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="54215-364">Ievadiet darba ID 2. pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="54215-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="54215-365">Šim darba ID ir tikai viens saņemšanas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="54215-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="54215-366">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-366">Select **OK**.</span></span>

    <span data-ttu-id="54215-367">Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums.</span><span class="sxs-lookup"><span data-stu-id="54215-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="54215-368">Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="54215-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="54215-369">Norādītā numura zīme būs sistēmas ģenerētā numura zīme no papildināšanas darba uzdevuma.</span><span class="sxs-lookup"><span data-stu-id="54215-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="54215-370">Lai pārliecinātos, ka uztverat pareizo numura zīmes ID, pārbaudiet krājumus **Rīcībā esošā saraksta** lapā krājumam, novietojumam un daudzumam.</span><span class="sxs-lookup"><span data-stu-id="54215-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="54215-371">Atlasiet pogu **Labi** (atzīmes simbols).</span><span class="sxs-lookup"><span data-stu-id="54215-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="54215-372">Apstipriniet norādījumus par izdošanas uzdevumu uz izejošo sagatavošanas posmu novietojumu.</span><span class="sxs-lookup"><span data-stu-id="54215-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="54215-373">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54215-373">Select **OK**.</span></span>

    <span data-ttu-id="54215-374">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="54215-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="54215-375">Piezīmes un padomi</span><span class="sxs-lookup"><span data-stu-id="54215-375">Notes and tips</span></span>

- <span data-ttu-id="54215-376">Šī funkcionalitāte darbojas ar visiem papildināšanas tipiem: kopuma pieprasījums, min/max, noslodzes pieprasījums un slotēšana.</span><span class="sxs-lookup"><span data-stu-id="54215-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="54215-377">Ja vēlaties, varat manuāli ignorēt papildināšanas darba pieejamību katram darba virsrakstam no **Darba informācijas** lapas.</span><span class="sxs-lookup"><span data-stu-id="54215-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="54215-378">Kad sistēma iestata papildināšanas darba pieejamību, tā ņem vērā visus krājumus, kas jau ir novietojumā, pirms darbs ir pabeigts</span><span class="sxs-lookup"><span data-stu-id="54215-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="54215-379">Katra pārdošanas pasūtījuma darba daļa ir saistīta ar specifisku papildināšanas darbu.</span><span class="sxs-lookup"><span data-stu-id="54215-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="54215-380">Nav atbilstošas pārdošanas darba pieejamības funkcionalitātes.</span><span class="sxs-lookup"><span data-stu-id="54215-380">There is no corresponding sales work availability functionality.</span></span>
