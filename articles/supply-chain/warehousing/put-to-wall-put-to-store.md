---
title: Novietot pie sienas – Novietot veikalā
description: Šajā tēmā ir sniegta informācija par funkcionalitāti Novietot pie sienas – novietot veikalā. Šī funkcionalitāte ļauj apstrādāt scenārijus, kuros ir jākonsolidē prece fasēšanas sagatavošanas zonā, pamatojoties uz konfigurējamajiem kritērijiem. Tas palīdz samazināt izdošanas laiku, jo ļauj veikt izdošanu vienai mērķa noliktavas vienībai, un var izmantot vairāk izvietošanas vietu nekā klastera izdošana.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cf34a61d0b3f784b5a424473588d05bf8703635c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823291"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="363ca-105">Novietot pie sienas – Novietot veikalā</span><span class="sxs-lookup"><span data-stu-id="363ca-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="363ca-106">Funkcionalitāte *Novietot pie sienas – novietot veikalā* ļauj apstrādāt scenārijus, kuros ir jākonsolidē prece fasēšanas sagatavošanas zonā, pamatojoties uz konfigurējamajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="363ca-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="363ca-107">Tā kā šī funkcionalitāte ļauj veikt izdošanu vienai mērķa noliktavas vienībai, un var izmantot vairāk izvietošanas vietu nekā klastera izdošana, uzņēmumi, kas nosūta uz veikaliem vai apstrādā mazus krājumus, gūs labumu no samazināta izdošanas laika.</span><span class="sxs-lookup"><span data-stu-id="363ca-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="363ca-108">Šīs funkcionalitātes darbplūsma novirza izvēlēto preci uz kārtošanas vietu sadalei dažādu veidu konteineros.</span><span class="sxs-lookup"><span data-stu-id="363ca-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="363ca-109">Parasti katra kārtošanas vieta ietver vairākas kārtošanas pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="363ca-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="363ca-110">Katra kārtošanas pozīcija tiek piešķirta atbilstoši kritērijiem, ko iestata biznesa process.</span><span class="sxs-lookup"><span data-stu-id="363ca-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="363ca-111">Raksturīgākie kritēriji ir galamērķis, sūtījums vai krava.</span><span class="sxs-lookup"><span data-stu-id="363ca-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="363ca-112">Pēc preces saņemšanas, tā tiek sadalīta katrai kārtošanas pozīcijai, pamatojoties uz daudzumu, kas ir saistīts ar pasūtījumu, galamērķi, sūtījumu vai kravu.</span><span class="sxs-lookup"><span data-stu-id="363ca-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="363ca-113">Kad konteiners ir pilns vai pabeigts, tas tiek pārvietots uz sagatavošanas novietojumu vai nosūtīšanas novietojumu turpmākai apstrādei, atkarībā no biznesa procesa.</span><span class="sxs-lookup"><span data-stu-id="363ca-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="363ca-114">Šī noliktavas funkcionalitāte ir attiecināta arī uz citiem nosaukumiem, piemēram, novietot pie gaismas un pārtraukumos.</span><span class="sxs-lookup"><span data-stu-id="363ca-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="363ca-115">Ieslēgt līdzekli Izejošā kārtošana</span><span class="sxs-lookup"><span data-stu-id="363ca-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="363ca-116">Pirms varat izmantot funkcionalitāti *Novietot pie sienas – novietot veikalā*, jūsu sistēmā ir jābūt ieslēgtam līdzeklim *Izejošā kārtošana*.</span><span class="sxs-lookup"><span data-stu-id="363ca-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="363ca-117">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="363ca-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="363ca-118">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="363ca-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="363ca-119">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="363ca-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="363ca-120">**Līdzekļa nosaukums:** *Izejošā kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="363ca-121">Līdzekli *Izejošā kārtošana* var izmantot savienojumā ar *Organizācijas līmeņa kopuma darbības kods* līdzekli, ja tas ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="363ca-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="363ca-122">Šis līdzeklis ir jāieslēdz arī tad, ja izmantosit iepriekš definētus kodus, kas iestatīti kopuma darbību kodos.</span><span class="sxs-lookup"><span data-stu-id="363ca-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="363ca-123">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="363ca-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="363ca-124">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="363ca-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="363ca-125">**Līdzekļa nosaukums:** *Organizācijas līmeņa kopuma darbības kods*</span><span class="sxs-lookup"><span data-stu-id="363ca-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="363ca-126">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="363ca-126">Setup</span></span>

<span data-ttu-id="363ca-127">Šai demonstrācijai tiek izmantoti standarta Contoso dati un noliktava *62*.</span><span class="sxs-lookup"><span data-stu-id="363ca-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="363ca-128">Tiek izmantoti arī daži papildinājumi, kas tiks minēti vēlāk.</span><span class="sxs-lookup"><span data-stu-id="363ca-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="363ca-129">Vietas veids</span><span class="sxs-lookup"><span data-stu-id="363ca-129">Location type</span></span>

1. <span data-ttu-id="363ca-130">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma veidi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="363ca-131">Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma veidu kārtošanai.</span><span class="sxs-lookup"><span data-stu-id="363ca-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="363ca-132">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-132">Set the following values:</span></span>

    - <span data-ttu-id="363ca-133">**Novietojuma veids:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="363ca-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="363ca-134">**Apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="363ca-135">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="363ca-136">Noliktavas vadības parametri</span><span class="sxs-lookup"><span data-stu-id="363ca-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="363ca-137">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="363ca-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="363ca-138">Cilnē **Vispārīgi**, kopsavilkuma cilnes **Novietojuma veidi** laukā **Kārtošanas novietojuma veids** ievadiet *SORT*.</span><span class="sxs-lookup"><span data-stu-id="363ca-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="363ca-139">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="363ca-140">Novietojuma profils</span><span class="sxs-lookup"><span data-stu-id="363ca-140">Location profile</span></span>

1. <span data-ttu-id="363ca-141">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.</span><span class="sxs-lookup"><span data-stu-id="363ca-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="363ca-142">Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma profilu kārtošanas novietojumam.</span><span class="sxs-lookup"><span data-stu-id="363ca-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="363ca-143">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="363ca-144">**Novietojuma profila ID:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="363ca-145">**Nosaukums:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="363ca-146">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="363ca-147">**Novietojuma formāts:** *PACK*</span><span class="sxs-lookup"><span data-stu-id="363ca-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="363ca-148">**Novietojuma veids:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="363ca-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="363ca-149">**Izmantot noliktavas vienības izsekošanu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="363ca-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="363ca-150">**Atļaut jauktus krājumus:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="363ca-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="363ca-151">**Atļaut jauktus krājumu statusus:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="363ca-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="363ca-152">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="363ca-153">Novietojumi</span><span class="sxs-lookup"><span data-stu-id="363ca-153">Locations</span></span>

1. <span data-ttu-id="363ca-154">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojums**.</span><span class="sxs-lookup"><span data-stu-id="363ca-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="363ca-155">Noņemiet atzīmi izvēles rūtiņai **Ģenerēt novietojuma kontrolciparus**.</span><span class="sxs-lookup"><span data-stu-id="363ca-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="363ca-156">Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="363ca-157">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="363ca-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="363ca-158">**Novietojums:** *Kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="363ca-159">**Novietojuma profila ID:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="363ca-160">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="363ca-161">Iepakošanas profili</span><span class="sxs-lookup"><span data-stu-id="363ca-161">Packing profiles</span></span>

1. <span data-ttu-id="363ca-162">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Iepakošanas profili**.</span><span class="sxs-lookup"><span data-stu-id="363ca-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="363ca-163">Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="363ca-164">**Iepakošanas profila ID:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="363ca-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="363ca-165">**Apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="363ca-166">**Konteineru iepakošanas politika:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="363ca-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="363ca-167">**Konteinera ID režīms:** *Automātiski*</span><span class="sxs-lookup"><span data-stu-id="363ca-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="363ca-168">**Konteinera veids:** *PALLET 48X48*</span><span class="sxs-lookup"><span data-stu-id="363ca-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="363ca-169">**Konteinera slēgšanas laikā automātiski izveidot konteineru:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="363ca-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="363ca-170">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="363ca-171">Kopuma darbību kodi</span><span class="sxs-lookup"><span data-stu-id="363ca-171">Wave step codes</span></span>

<span data-ttu-id="363ca-172">Ja līdzeklis *Organizācijas līmeņa kopuma darbības kods* ir ieslēgts, iestatiet tālāk norādīto kodu.</span><span class="sxs-lookup"><span data-stu-id="363ca-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="363ca-173">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma darbību kodi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="363ca-174">Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="363ca-175">**Kopuma darbības kods:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="363ca-176">**Kopuma darbības apraksts:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="363ca-177">**Kopuma darbības veids:** *Kārtošanas veidne*</span><span class="sxs-lookup"><span data-stu-id="363ca-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="363ca-178">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="363ca-179">Izejošās kārtošanas veidne</span><span class="sxs-lookup"><span data-stu-id="363ca-179">Outbound sorting template</span></span>

<span data-ttu-id="363ca-180">Kārtošanas veidne kontrolē, vai tiek veidotas kārtošanas pozīcijas, kādi kritēriji tiek izmantoti un citus kārtošanas procesa atribūtus.</span><span class="sxs-lookup"><span data-stu-id="363ca-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="363ca-181">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Izejošās kārtošanas veidne**.</span><span class="sxs-lookup"><span data-stu-id="363ca-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="363ca-182">Lai izveidotu kārtošanas veidni, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="363ca-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="363ca-183">Jaunās veidnes galvenē iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="363ca-184">**Izejošās kārtošanas veidnes ID:** *Wave Sort*</span><span class="sxs-lookup"><span data-stu-id="363ca-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="363ca-185">**Apraksts:** *Kopuma kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="363ca-186">**Kārtošanas veidnes veids:** *Kopuma pieprasījums*</span><span class="sxs-lookup"><span data-stu-id="363ca-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="363ca-187">Šis lauks definē procesu, kam tiek izmantota kārtošanas veidne.</span><span class="sxs-lookup"><span data-stu-id="363ca-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="363ca-188">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-188">The following values are available:</span></span>

        - <span data-ttu-id="363ca-189">**Kopuma pieprasījums** – kārtošanas veidne tiek izmantota procesam *Novietot pie sienas*.</span><span class="sxs-lookup"><span data-stu-id="363ca-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="363ca-190">Šis veidnes veids tiek izmantots, lai apietu iepakošanas staciju un apstrādātu krājumus tieši no kopuma.</span><span class="sxs-lookup"><span data-stu-id="363ca-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="363ca-191">Šo veidu varat izmantot, ja **kārtošanas** kopuma procesa metode ir iekļauta kopuma veidnē.</span><span class="sxs-lookup"><span data-stu-id="363ca-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="363ca-192">**Konteiners** – kārtošanas veidne tiek izmantota procesam *Paletes izveide pēc iepakošanas*.</span><span class="sxs-lookup"><span data-stu-id="363ca-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="363ca-193">Šis veidnes veids tiek izmantots, lai apstrādātu konteinerus, kas tika slēgti iepakošanas stacijā un ir jākārto paletēs.</span><span class="sxs-lookup"><span data-stu-id="363ca-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="363ca-194">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="363ca-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="363ca-195">**Novietojums:** *Kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="363ca-196">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="363ca-197">**Kārtošanas pārbaude:** *Pozīcijas skenēšana*.</span><span class="sxs-lookup"><span data-stu-id="363ca-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="363ca-198">Šis lauks definē pārbaudi, kas ir nepieciešama kārtošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="363ca-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="363ca-199">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-199">The following values are available:</span></span>

        - <span data-ttu-id="363ca-200">None</span><span class="sxs-lookup"><span data-stu-id="363ca-200">None</span></span>
        - <span data-ttu-id="363ca-201">Numura zīmes skenēšana</span><span class="sxs-lookup"><span data-stu-id="363ca-201">License plate scan</span></span>
        - <span data-ttu-id="363ca-202">Pozīcijas skenēšana</span><span class="sxs-lookup"><span data-stu-id="363ca-202">Position scan</span></span>

    - <span data-ttu-id="363ca-203">**Izveidot darbu slēgtai pozīcijai:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="363ca-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="363ca-204">Ja šī opcija ir iestatīta uz *Jā*, kad pozīcija tiek slēgta, tiks izveidots darbs, lai pārvietotu krājumus uz galējo nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="363ca-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="363ca-205">Ja tā ir iestatīta uz *Nē*, krājumi tiks nekavējoties izdoti pasūtījumam, kad pozīcija tiks slēgta.</span><span class="sxs-lookup"><span data-stu-id="363ca-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="363ca-206">**Pozīcijas piešķiršana:** *Manuāli*</span><span class="sxs-lookup"><span data-stu-id="363ca-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="363ca-207">Šis lauks definē pozīcijas piešķires veidu.</span><span class="sxs-lookup"><span data-stu-id="363ca-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="363ca-208">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-208">The following values are available:</span></span>

        - <span data-ttu-id="363ca-209">**Manuāli** – lietotājam vienmēr jānorāda, kurā pozīcijā krājums ir jākārto.</span><span class="sxs-lookup"><span data-stu-id="363ca-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="363ca-210">**Automātiski** – sistēma automātiski novirzīs krājumus uz pozīciju, kad vien iespējams, pamatojoties uz kārtošanas veidnes pārtraukumiem.</span><span class="sxs-lookup"><span data-stu-id="363ca-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="363ca-211">**Piešķirt kārtošanas pozīcijas kritērijus:** *Izmantot tikai tukšu pozīciju*</span><span class="sxs-lookup"><span data-stu-id="363ca-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="363ca-212">Šis lauks kontrolē, vai krājumi, kuri jau atrodas kārtošanas pozīcijās, ir ņemti vērā, piešķirot pozīciju pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="363ca-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="363ca-213">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-213">The following values are available:</span></span>

        - <span data-ttu-id="363ca-214">**Izmantot tikai tukšu pozīciju** – pozīcijas, kurām jau ir ar tām saistīti krājumi, tiks ņemtas vērā.</span><span class="sxs-lookup"><span data-stu-id="363ca-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="363ca-215">**Pieņemsim, ka pozīcija ir tukša** – visi krājumi, kas jau ir pozīcijā, piešķiršanas laikā netiks ņemti vērā.</span><span class="sxs-lookup"><span data-stu-id="363ca-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="363ca-216">Tiks izmantotas visas pieejamās pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="363ca-216">All available positions will be used.</span></span>

    - <span data-ttu-id="363ca-217">**Kopuma darbības kods:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="363ca-218">Ja ir ieslēgts līdzeklis *Organizācijas līmeņa kopuma darbības kods*, tad kopuma darbību kodos ir jābūt iestatītam arī kopuma darbības kodam *Kārtot*.</span><span class="sxs-lookup"><span data-stu-id="363ca-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="363ca-219">**Automātiski slēgt kārtošanas pozīciju:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="363ca-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="363ca-220">Ja šī opcija ir iestatīta uz *Jā*, kārtošanas pozīcija automātiski tiks slēgta, kad visi darbi, kas tuvojas pozīcijai, būs pabeigti.</span><span class="sxs-lookup"><span data-stu-id="363ca-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="363ca-221">**Kārtošanas pozīciju skaits:** *3*</span><span class="sxs-lookup"><span data-stu-id="363ca-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="363ca-222">Šis lauks definē maksimālo kārtošanas pozīciju skaitu, ko sistēma izveidos.</span><span class="sxs-lookup"><span data-stu-id="363ca-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="363ca-223">**Kārtošanas pozīcijas prefikss:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="363ca-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="363ca-224">Šis lauks definē prefiksu, ko sistēma piešķir pirms pozīcijas numura.</span><span class="sxs-lookup"><span data-stu-id="363ca-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="363ca-225">**Automātiski iepakot kārtošanas pozīciju:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="363ca-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="363ca-226">Ja šī opcija ir iestatīta uz *Jā*, krājumi kārtošanas pozīcijā tiks iepakoti konteinerā, kad pozīcija tiks slēgta.</span><span class="sxs-lookup"><span data-stu-id="363ca-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="363ca-227">**Iepakošanas profila ID:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="363ca-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="363ca-228">Šis lauks definē iepakošanas profilu, kas tiks izmantots, kad kārtošanas pozīcija tiks iepakota konteinerā.</span><span class="sxs-lookup"><span data-stu-id="363ca-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="363ca-229">Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai norādītu kritērijus, kas tiek izmantoti šai kārtošanas veidnei.</span><span class="sxs-lookup"><span data-stu-id="363ca-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="363ca-230">Vaicājuma dialoglodziņa cilnē **Kārtošana** atlasiet **Jauns**, lai pievienotu rindu, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="363ca-231">**Tabula:** *Kravas informācija*</span><span class="sxs-lookup"><span data-stu-id="363ca-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="363ca-232">**Atveidotā tabula:** *Kravas informācija*</span><span class="sxs-lookup"><span data-stu-id="363ca-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="363ca-233">**Lauks:** *Sūtījuma ID*</span><span class="sxs-lookup"><span data-stu-id="363ca-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="363ca-234">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="363ca-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="363ca-235">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-235">Select **OK**.</span></span>
1. <span data-ttu-id="363ca-236">Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?”</span><span class="sxs-lookup"><span data-stu-id="363ca-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="363ca-237">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="363ca-237">Select **Yes**.</span></span>

    <span data-ttu-id="363ca-238">Tagad darbību rūtī ir pieejama poga **Izejošās kārtošanas veidnes pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="363ca-239">Darbību rūtī atlasiet **Izejošās kārtošanas veidnes pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="363ca-240">Atzīmējiet izvēles rūtiņu **Grupēt pēc lauka**, lai grupētu pēc sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="363ca-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="363ca-241">Šis iestatījums izveidos vienu kārtošanas pozīciju katram sūtījumam, kas ir kopuma konteiners.</span><span class="sxs-lookup"><span data-stu-id="363ca-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="363ca-242">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="363ca-243">Kopuma apstrādes metodes</span><span class="sxs-lookup"><span data-stu-id="363ca-243">Wave process methods</span></span>

1. <span data-ttu-id="363ca-244">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.</span><span class="sxs-lookup"><span data-stu-id="363ca-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="363ca-245">Darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**.</span><span class="sxs-lookup"><span data-stu-id="363ca-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="363ca-246">Pieejamo metožu sarakstam tiek pievienota **kārtošanas** metode, un tai tiek atlasīts kopuma veidnes veids *Nosūtīšana*.</span><span class="sxs-lookup"><span data-stu-id="363ca-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="363ca-247">Laidiena veidnes</span><span class="sxs-lookup"><span data-stu-id="363ca-247">Wave templates</span></span>

<span data-ttu-id="363ca-248">Rediģējiet kopuma veidni, kas tiek izmantota kopuma pieprasījuma kārtošanai.</span><span class="sxs-lookup"><span data-stu-id="363ca-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="363ca-249">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="363ca-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="363ca-250">Laukā **Kopuma veidnes veids** atlasiet *Nosūtīšana*.</span><span class="sxs-lookup"><span data-stu-id="363ca-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="363ca-251">Atlasiet esošo veidni **62 Sūtījums pēc noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="363ca-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="363ca-252">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="363ca-253">Kopsavilkuma cilnē **Vispārīgi** veiciet šādas izmaiņas:</span><span class="sxs-lookup"><span data-stu-id="363ca-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="363ca-254">Iestatiet opciju **Apstrādāt kopumu, to pārvietojot uz noliktavu** uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="363ca-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="363ca-255">Iestatiet opciju **Piešķirt atvērtajiem kopumiem** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="363ca-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="363ca-256">Kopsavilkuma cilnē **Metodes** iestatiet **kārtošanas** metodi:</span><span class="sxs-lookup"><span data-stu-id="363ca-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="363ca-257">Režģī **Atlikušās metodes** atlasiet **Kārtošana**.</span><span class="sxs-lookup"><span data-stu-id="363ca-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="363ca-258">Atlasiet bultiņas pa labi pogu, lai pārvietotu **Kārtošana** uz režģi **Atlasītās metodes**.</span><span class="sxs-lookup"><span data-stu-id="363ca-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="363ca-259">Režģī **Atlasītās metodes** atlasiet **Kārtošana**.</span><span class="sxs-lookup"><span data-stu-id="363ca-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="363ca-260">Iestatiet lauku **Kopuma darbības kods** uz *Kārtot*.</span><span class="sxs-lookup"><span data-stu-id="363ca-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="363ca-261">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="363ca-262">Mobilās ierīces izvēlnes vienumi</span><span class="sxs-lookup"><span data-stu-id="363ca-262">Mobile device menu items</span></span>

1. <span data-ttu-id="363ca-263">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="363ca-264">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="363ca-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="363ca-265">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="363ca-266">**Izvēlnes vienuma nosaukums:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="363ca-267">**Nosaukums:** *Kārtot*</span><span class="sxs-lookup"><span data-stu-id="363ca-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="363ca-268">**Režīms:** *Netiešs*</span><span class="sxs-lookup"><span data-stu-id="363ca-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="363ca-269">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="363ca-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="363ca-270">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="363ca-271">**Aktivitātes kods:** *Izejošā kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="363ca-272">**Izmantot procesa ceļvedi:** *Jā* (noklusējuma vērtība)</span><span class="sxs-lookup"><span data-stu-id="363ca-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="363ca-273">**Izejošās kārtošanas veidnes ID:** *Wave Sort*</span><span class="sxs-lookup"><span data-stu-id="363ca-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="363ca-274">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="363ca-275">Mobilās ierīces izvēlne</span><span class="sxs-lookup"><span data-stu-id="363ca-275">Mobile device menu</span></span>

1. <span data-ttu-id="363ca-276">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="363ca-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="363ca-277">Izvēlņu sarakstā atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="363ca-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="363ca-278">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="363ca-279">Režģī **Pieejamās izvēlnes un izvēļņu elementi** meklējiet un atlasiet tikko izveidoto izvēlnes elementu **Kārtot**.</span><span class="sxs-lookup"><span data-stu-id="363ca-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="363ca-280">Atlasiet bultiņas pa labi pogu, lai pārvietotu **Kārtot** uz režģi **Izvēlnes struktūra**.</span><span class="sxs-lookup"><span data-stu-id="363ca-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="363ca-281">Šādā veidā jūs pievienojat izvēlnes elementu izvēlnei **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="363ca-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="363ca-282">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="363ca-283">Vietas direktīvas</span><span class="sxs-lookup"><span data-stu-id="363ca-283">Location directives</span></span>

<span data-ttu-id="363ca-284">Ir jāizveido novietojuma direktīvas, lai vadītu darbu, kas tiek izveidots pēc kārtošanas pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="363ca-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="363ca-285">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="363ca-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="363ca-286">Laukā **Darba pasūtījuma veids** atlasiet *Kārtotu krājumu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="363ca-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="363ca-287">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="363ca-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="363ca-288">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="363ca-289">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="363ca-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="363ca-290">**Nosaukums:** *Novietot pie angāra durvīm*</span><span class="sxs-lookup"><span data-stu-id="363ca-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="363ca-291">Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="363ca-292">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="363ca-293">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="363ca-293">**Site:** *6*</span></span>
    - <span data-ttu-id="363ca-294">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="363ca-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="363ca-295">**Direktīvas kods:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="363ca-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="363ca-296">**Vairākas SKU:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="363ca-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="363ca-297">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="363ca-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="363ca-298">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="363ca-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="363ca-299">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="363ca-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="363ca-300">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="363ca-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="363ca-301">**No daudzuma:** *0*</span><span class="sxs-lookup"><span data-stu-id="363ca-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="363ca-302">**Līdz daudzumam:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="363ca-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="363ca-303">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="363ca-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="363ca-304">Kopsavilkuma cilnē **Novietojuma direktīvu darbības** atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="363ca-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="363ca-305">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="363ca-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="363ca-306">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="363ca-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="363ca-307">**Nosaukums:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="363ca-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="363ca-308">Atlasiet **Saglabāt**, lai padarītu pogu **Rediģēt vaicājumu** pieejamu **Novietojuma direktīvu darbības** kopsavilkuma cilnē.</span><span class="sxs-lookup"><span data-stu-id="363ca-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="363ca-309">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="363ca-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="363ca-310">Vaicājuma dialoglodziņā cilnē **Diapazons** sameklējiet rindu, kurā lauks **Lauks** ir iestatīts uz *Novietojums*.</span><span class="sxs-lookup"><span data-stu-id="363ca-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="363ca-311">Iestatiet lauku **Kritēriji** šai rindai uz *Angāra durvis*.</span><span class="sxs-lookup"><span data-stu-id="363ca-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="363ca-312">Lai apstiprinātu rediģēšanu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="363ca-313">Darba klases</span><span class="sxs-lookup"><span data-stu-id="363ca-313">Work classes</span></span>

1. <span data-ttu-id="363ca-314">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="363ca-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="363ca-315">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="363ca-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="363ca-316">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="363ca-317">**Darba klases ID:** *Kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="363ca-318">**Apraksts:** *Kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="363ca-319">**Darba pasūtījuma veids:** *Kārtotu krājumu izdošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="363ca-320">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="363ca-321">Darbu veidnes</span><span class="sxs-lookup"><span data-stu-id="363ca-321">Work templates</span></span>

1. <span data-ttu-id="363ca-322">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darbu veidnes**.</span><span class="sxs-lookup"><span data-stu-id="363ca-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="363ca-323">Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="363ca-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="363ca-324">Režģī atlasiet darba veidni **62 izdot iepakošanai**.</span><span class="sxs-lookup"><span data-stu-id="363ca-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="363ca-325">Darbību rūtī atlasiet **Darba galvenes pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="363ca-326">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="363ca-327">Rindā, kur lauks **Lauka nosaukums** ir iestatīts uz *Sūtījuma ID*, noņemiet atzīmi izvēles rūtiņā **Grupēt pēc šī lauka**.</span><span class="sxs-lookup"><span data-stu-id="363ca-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="363ca-328">Atlasiet **Saglabāt** un pēc tam aizveriet dialoglodziņu **Darba galvenes pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="363ca-329">Laukā **Darba pasūtījuma veids** atlasiet *Kārtotu krājumu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="363ca-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="363ca-330">Atlasiet **Jauns**, lai izveidotu darba veidni.</span><span class="sxs-lookup"><span data-stu-id="363ca-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="363ca-331">Sadaļā **Pārskats** iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="363ca-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="363ca-332">Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="363ca-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="363ca-333">**Darba veidne:** *Kārtota izdošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="363ca-334">**Darba veidnes apraksts:** *Kārtota izdošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="363ca-335">Atlasiet **Saglabāt**, lai padarītu pieejamu sadaļu **Darba veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="363ca-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="363ca-336">Sadaļā **Darba veidnes informācija** tiks izveidotas divas rindas.</span><span class="sxs-lookup"><span data-stu-id="363ca-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="363ca-337">Atlasiet **Jauns** un pēc tam 1. rindai iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="363ca-338">**Darba veids:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="363ca-339">**Obligāts:** atlasīts (= *Jā*)</span><span class="sxs-lookup"><span data-stu-id="363ca-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="363ca-340">**Darba klases ID:** *Kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="363ca-341">Vēlreiz atlasiet **Jauns** un pēc tam 2. rindai iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="363ca-342">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="363ca-343">**Obligāts:** atlasīts (= *Jā*)</span><span class="sxs-lookup"><span data-stu-id="363ca-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="363ca-344">**Darba klases ID:** *Kārtošana*</span><span class="sxs-lookup"><span data-stu-id="363ca-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="363ca-345">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="363ca-346">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="363ca-346">Example scenario</span></span>

<span data-ttu-id="363ca-347">Šis scenārijs simulē situāciju, kad noliktavas novietojumos tiek uzglabāti mazi krājumi un tie pirms nosūtīšanas ir jāiepako kastēs, bet iepakošanas stacijas funkcionalitāte nav īsti piemērota.</span><span class="sxs-lookup"><span data-stu-id="363ca-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="363ca-348">Darbinieki vienlaicīgi izdot pasūtījumus vairākiem klientiem un atšķirīgās adresēs, lai palielinātu izdošanas ātrumu.</span><span class="sxs-lookup"><span data-stu-id="363ca-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="363ca-349">Kad izdošana ir pabeigta, darbinieki ierodas kārtošanas vietā, kur izdotos krājumus var kārtot pareizajā kastē, pamatojoties uz nepieciešamajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="363ca-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="363ca-350">Šajā piemērā sūtījuma ID tiks izmantots, lai noteiktu pareizo kasti, jo katram sūtījumam ir cita adrese.</span><span class="sxs-lookup"><span data-stu-id="363ca-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="363ca-351">Kad visi noslodzes krājumi ir iepakoti un sakārtoti pēc sūtījuma, kastes tiks pārvietotas uz sagatavošanas zonu, un visbeidzot ielādētas kravas automašīnā.</span><span class="sxs-lookup"><span data-stu-id="363ca-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="363ca-352">Pirms sākat scenāriju, pārliecinieties, vai noliktavai ir pareizi iestatīta visa standarta noliktavas funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="363ca-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="363ca-353">Šim nolūkam tiek izmantota standarta Contoso noliktava *62*.</span><span class="sxs-lookup"><span data-stu-id="363ca-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="363ca-354">Standarta konfigurācijas nav mainītas papildus tam, kas aprakstīts iestatījumā.</span><span class="sxs-lookup"><span data-stu-id="363ca-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="363ca-355">Pieprasījuma izveide</span><span class="sxs-lookup"><span data-stu-id="363ca-355">Create demand</span></span>

<span data-ttu-id="363ca-356">Lai funkcionalitāti varētu demonstrēt, ir jāizveido daži pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="363ca-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="363ca-357">Šim scenārijam tiks izveidoti trīs pārdošanas pasūtījumi trīs dažādiem klientiem, lai simulētu dažādas piegādes adreses.</span><span class="sxs-lookup"><span data-stu-id="363ca-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="363ca-358">Šādā veidā tiks izveidoti trīs atsevišķi sūtījumi.</span><span class="sxs-lookup"><span data-stu-id="363ca-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="363ca-359">Pirms pārdošanas pasūtījumu un sūtījumu izveides, ir jāpārliecinās, vai izdošanas vietās ir pietiekami daudz krājumu visiem krājumiem pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="363ca-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="363ca-360">Pārskatiet novietojuma direktīvas iestatījumus, lai apstiprinātu izdošanas vietas, kas tiek izmantotas pārdošanas pasūtījuma izdošanai.</span><span class="sxs-lookup"><span data-stu-id="363ca-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="363ca-361">Pielāgojot krājumus, varat izveidot manuālo kustību, izmantot papildināšanu vai jebkuru citu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="363ca-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="363ca-362">Pēc tam rezervējiet krājumus.</span><span class="sxs-lookup"><span data-stu-id="363ca-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="363ca-363">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="363ca-364">Atlasiet **Jauns**, lai 1. pasūtījumam izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="363ca-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="363ca-365">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="363ca-366">**Klients:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="363ca-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="363ca-367">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="363ca-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="363ca-368">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-368">Select **OK**.</span></span>
1. <span data-ttu-id="363ca-369">Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="363ca-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="363ca-370">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-370">Set the following values:</span></span>

    - <span data-ttu-id="363ca-371">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="363ca-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="363ca-372">**Daudzums:** *5*</span><span class="sxs-lookup"><span data-stu-id="363ca-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="363ca-373">Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="363ca-374">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="363ca-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="363ca-375">**Daudzums:** *10*</span><span class="sxs-lookup"><span data-stu-id="363ca-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="363ca-376">Atkārtojiet šīs darbības katrai pasūtījuma pārdošanas rindai, lai rezervētu tai krājumus:</span><span class="sxs-lookup"><span data-stu-id="363ca-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="363ca-377">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Krājumi** atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="363ca-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="363ca-378">Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="363ca-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="363ca-379">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-379">Select **Save**.</span></span>

1. <span data-ttu-id="363ca-380">Atlasiet **Jauns**, lai 2. pasūtījumam izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="363ca-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="363ca-381">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="363ca-382">**Klients:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="363ca-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="363ca-383">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="363ca-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="363ca-384">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-384">Select **OK**.</span></span>
1. <span data-ttu-id="363ca-385">Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="363ca-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="363ca-386">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-386">Set the following values:</span></span>

    - <span data-ttu-id="363ca-387">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="363ca-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="363ca-388">**Daudzums:** *7*</span><span class="sxs-lookup"><span data-stu-id="363ca-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="363ca-389">Atlasiet **Pievienot rindu**, lai pievienotu otro rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="363ca-390">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="363ca-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="363ca-391">**Daudzums:** *3*</span><span class="sxs-lookup"><span data-stu-id="363ca-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="363ca-392">Atkārtojiet šīs darbības katrai pasūtījuma pārdošanas rindai, lai rezervētu tai krājumus:</span><span class="sxs-lookup"><span data-stu-id="363ca-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="363ca-393">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Krājumi** atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="363ca-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="363ca-394">Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="363ca-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="363ca-395">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-395">Select **Save**.</span></span>

1. <span data-ttu-id="363ca-396">Atlasiet **Jauns**, lai 3. pasūtījumam izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="363ca-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="363ca-397">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="363ca-398">**Klients:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="363ca-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="363ca-399">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="363ca-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="363ca-400">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-400">Select **OK**.</span></span>
1. <span data-ttu-id="363ca-401">Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="363ca-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="363ca-402">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="363ca-402">Set the following values:</span></span>

    - <span data-ttu-id="363ca-403">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="363ca-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="363ca-404">**Daudzums:** *8*</span><span class="sxs-lookup"><span data-stu-id="363ca-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="363ca-405">Veiciet tālāk norādītās darbības, lai rezervētu krājumus pārdošanas rindām:</span><span class="sxs-lookup"><span data-stu-id="363ca-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="363ca-406">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Krājumi** atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="363ca-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="363ca-407">Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="363ca-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="363ca-408">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-408">Select **Save**.</span></span>

<span data-ttu-id="363ca-409">Izpildiet šo procedūru, lai katru pārdošanas pasūtījumu izlaistu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="363ca-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="363ca-410">Tiks izveidoti trīs dažādi sūtījumi.</span><span class="sxs-lookup"><span data-stu-id="363ca-410">Three different shipments will be created.</span></span> <span data-ttu-id="363ca-411">Pēc tam visi trīs sūtījumi ir jāpievieno vienam jaunam kopumam.</span><span class="sxs-lookup"><span data-stu-id="363ca-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="363ca-412">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="363ca-413">Režģī atlasiet pirmo izveidoto pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="363ca-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="363ca-414">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="363ca-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="363ca-415">Tiks saņemts informatīvs ziņojums, kurā norādīts izveidotais kopuma ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="363ca-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="363ca-416">Atkārtojiet iepriekšējās darbības, lai izlaistu noliktavā 2. un 3. pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="363ca-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="363ca-417">Ievērojiet, ka saņemtais informatīvais ziņojums norāda, ka sūtījums ir pievienots kopumam, kas tika izveidots, izlaižot 1. pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="363ca-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="363ca-418">Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="363ca-419">Atlasiet kopuma ID, kas tika izveidots no pārdošanas pasūtījuma izlaides, lai atvērtu lapu **Kopumi**.</span><span class="sxs-lookup"><span data-stu-id="363ca-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="363ca-420">Šajā lapā tiek rādīta kopuma informācija.</span><span class="sxs-lookup"><span data-stu-id="363ca-420">This page shows the wave details.</span></span> <span data-ttu-id="363ca-421">Kopsavilkuma cilne **Kopuma rindas** rāda izveidotos sūtījumus.</span><span class="sxs-lookup"><span data-stu-id="363ca-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="363ca-422">Tagad ir jāizveido darbs, lai krājumus no izdošanas vietām pārnestu uz kārtošanas vietām.</span><span class="sxs-lookup"><span data-stu-id="363ca-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="363ca-423">Darbību rūtī atlasiet **Apstrādāt**.</span><span class="sxs-lookup"><span data-stu-id="363ca-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="363ca-424">Kopuma apstrādes laikā kārtošanas metode izmanto kārtošanas veidni, lai piešķirtu krājumus kārtošanas pozīcijām.</span><span class="sxs-lookup"><span data-stu-id="363ca-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="363ca-425">Kad kopuma apstrāde ir pabeigta, tiks saņemts informatīvs ziņojums, ka kopums ir iegrāmatots un darbs ir izveidots.</span><span class="sxs-lookup"><span data-stu-id="363ca-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="363ca-426">Darbību rūtī cilnes **Kopums** grupā **Saistītā informācija**, atlasiet **Darbs**, lai skatītu izveidoto darbu.</span><span class="sxs-lookup"><span data-stu-id="363ca-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="363ca-427">Pierakstiet darba ID.</span><span class="sxs-lookup"><span data-stu-id="363ca-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="363ca-428">Dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Izejošās kārtošanas pozīciju piešķires**.</span><span class="sxs-lookup"><span data-stu-id="363ca-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="363ca-429">Kreisajā kolonnā varat skatīt izejošo kārtošanas pozīciju, kas tika izveidota katram sūtījumam.</span><span class="sxs-lookup"><span data-stu-id="363ca-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="363ca-430">Kopsavilkuma cilnē **Kārtošanas pozīcijas kritēriji** varat skatīt šīs pozīcijas sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="363ca-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="363ca-431">Viens darba ID ir izveidots, lai krājumus no izdošanas vietām pārnestu uz kārtošanas vietām.</span><span class="sxs-lookup"><span data-stu-id="363ca-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="363ca-432">Lai pabeigtu darbu, ir nepieciešams darba ID, kas tika izveidots kopuma apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="363ca-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="363ca-433">Pārdošanas pasūtījuma izdošana kārtošanas vietai</span><span class="sxs-lookup"><span data-stu-id="363ca-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="363ca-434">Piesakieties mobilajā programmā kā darbinieks noliktavā *62*.</span><span class="sxs-lookup"><span data-stu-id="363ca-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="363ca-435">Galvenajā izvēlnē atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="363ca-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="363ca-436">Izvēlnē **Izejošs** atlasiet **Pārdošanas izdošana**.</span><span class="sxs-lookup"><span data-stu-id="363ca-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="363ca-437">Atlasiet lauku **ID** un pēc tam ievadiet darba ID no kopuma apstrādes.</span><span class="sxs-lookup"><span data-stu-id="363ca-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="363ca-438">Apstipriniet ievadīto.</span><span class="sxs-lookup"><span data-stu-id="363ca-438">Confirm your entry.</span></span>

    <span data-ttu-id="363ca-439">Pēc tam tiek parādīta uzvedne ievadīt mērķa noliktavas vienību (LP).</span><span class="sxs-lookup"><span data-stu-id="363ca-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="363ca-440">Ievērojiet, ka 1. pārdošanas pasūtījuma 1. rinda ir jāizdod un jāpievieno mērķa noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="363ca-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="363ca-441">Tiek parādīts krājuma kods, daudzums, krājuma apraksts un izdošanas vieta.</span><span class="sxs-lookup"><span data-stu-id="363ca-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="363ca-442">Laukā **Mērķa LP** ievadiet unikālu noliktavas vienības identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="363ca-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="363ca-443">Visas izveidotās rindas no apstrādātā kopuma tiks izdotas tai pašai mērķa noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="363ca-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="363ca-444">Apstipriniet ievadīto.</span><span class="sxs-lookup"><span data-stu-id="363ca-444">Confirm your entry.</span></span>

    <span data-ttu-id="363ca-445">Mobilā programma tagad piedāvā lapu sēriju **Izdošana**, kas norāda uz izdošanas vietu, krājumu un daudzumu, kas ir jāizdod.</span><span class="sxs-lookup"><span data-stu-id="363ca-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="363ca-446">Pēc tam, kad izdotais krājums ir pievienots noliktavas vienībai, tiks apstiprināts izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="363ca-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="363ca-447">Pēdējā lapa būs darbs, lai izdotos krājumus izvietotu kārtošanas vietā.</span><span class="sxs-lookup"><span data-stu-id="363ca-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="363ca-448">Apstipriniet pirmo izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="363ca-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="363ca-449">Tiek parādīts nākamais izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="363ca-449">The next pick work is shown.</span></span> <span data-ttu-id="363ca-450">Apstipriniet izdošanu.</span><span class="sxs-lookup"><span data-stu-id="363ca-450">Confirm the pick.</span></span>
1. <span data-ttu-id="363ca-451">Turpiniet apstiprināt atlikušo izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="363ca-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="363ca-452">Pēdējā darbība ir pabeigt izvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="363ca-452">The last step is to complete the put work.</span></span> <span data-ttu-id="363ca-453">Apstipriniet izvietošanu kārtošanas vietā.</span><span class="sxs-lookup"><span data-stu-id="363ca-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="363ca-454">Tiek saņemts ziņojums “Darbs pabeigts”.</span><span class="sxs-lookup"><span data-stu-id="363ca-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="363ca-455">Izejiet no mobilās programmas **Pārdošanas izdošana**.</span><span class="sxs-lookup"><span data-stu-id="363ca-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="363ca-456">Kārtošana/novietot pie sienas</span><span class="sxs-lookup"><span data-stu-id="363ca-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="363ca-457">Tagad, kad visi krājumi ir novietoti kārtošanas vietā, tie ir jākārto pareizajā kārtošanas pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="363ca-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="363ca-458">Piesakieties mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="363ca-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="363ca-459">Galvenajā izvēlnē atlasiet **Izejošs**.</span><span class="sxs-lookup"><span data-stu-id="363ca-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="363ca-460">Izvēlnē **Izejošs** atlasiet **Kārtot**, lai sāktu kārtot krājumus.</span><span class="sxs-lookup"><span data-stu-id="363ca-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="363ca-461">Laukā **LP/CON** ievadiet mērķa noliktavas vienību izdotajam pārdošanas pasūtījuma darbam.</span><span class="sxs-lookup"><span data-stu-id="363ca-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="363ca-462">Apstipriniet ievadīto.</span><span class="sxs-lookup"><span data-stu-id="363ca-462">Confirm your entry.</span></span>
1. <span data-ttu-id="363ca-463">Ievadiet krājuma kodu, kas jākārto kā pirmais.</span><span class="sxs-lookup"><span data-stu-id="363ca-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="363ca-464">Sistēma nosaka pirmo kārtošanas pozīciju, kas ir jāparāda.</span><span class="sxs-lookup"><span data-stu-id="363ca-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="363ca-465">Apstipriniet kārtošanas pozīciju.</span><span class="sxs-lookup"><span data-stu-id="363ca-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="363ca-466">Tiek pieprasīts piešķirt noliktavas vienību kārtošanas pozīcijai.</span><span class="sxs-lookup"><span data-stu-id="363ca-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="363ca-467">Atlasiet lauku **LP**, ievadiet unikālo noliktavas vienības identifikatoru un pēc tam apstipriniet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="363ca-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="363ca-468">Tā kā kārtošanas pozīcija ir saistīta ar sūtījuma ID, izdotie krājumi tiks kārtoti noliktavas vienībā, kas ir raksturīga izejošajam sūtījumam un pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="363ca-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="363ca-469">Nākamā lapa parāda krājuma ID, daudzumu, kārtošanas pozīcijas ID un “no” (izdošana) un “uz” (kārtošana) noliktavas vienības ID.</span><span class="sxs-lookup"><span data-stu-id="363ca-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="363ca-470">Šajā lapā sniegtā informācija sniedz norādījumus, kārtot norādīto krājumu un daudzumus no izdošanas noliktavas vienības uz kārtošanas noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="363ca-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="363ca-471">Apstipriniet kārtošanas pozīciju.</span><span class="sxs-lookup"><span data-stu-id="363ca-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="363ca-472">Kārtojiet krājumus pirmajā kārtošanas pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="363ca-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="363ca-473">Kad esat beidzis, sistēma novirza jūs uz nākamo kārtošanas pozīciju.</span><span class="sxs-lookup"><span data-stu-id="363ca-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="363ca-474">Atkārtojiet šo procesu visām izdošanas rindām darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="363ca-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="363ca-475">Šo procesu ir jāizmanto arī tad, ja ir vairākas izdošanas rindas ar vienādu krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="363ca-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="363ca-476">Atkārtojot šo procesu visiem krājumiem, sistēma novērtē nākamā skenētā krājuma (darba rinda) kritērijus un nosaka, kurā kārtošanas pozīcijā tie ir jānovieto.</span><span class="sxs-lookup"><span data-stu-id="363ca-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="363ca-477">Jūs automātiski tiekat novirzīts novietot krājumu pareizā kārtošanas pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="363ca-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="363ca-478">Atkarībā no apstiprinājuma iestatījumiem, jūs tiekat novirzīts apstiprināt šo darbību, ievadot pozīcijas numuru vai noliktavas vienības ID.</span><span class="sxs-lookup"><span data-stu-id="363ca-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="363ca-479">Ja automātiskā kārtošana ir ieslēgta, manuālā ignorēšana nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="363ca-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="363ca-480">Kad esat pabeidzis, programmā Microsoft Dynamics 365 Supply Chain Management atveriet lapu **Izejošās kārtošanas pozīciju piešķires**, lai pārskatītu pozīciju statusu.</span><span class="sxs-lookup"><span data-stu-id="363ca-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="363ca-481">Ja pozīcijas tiek slēgtas automātiski, atlasiet **Rādīt slēgto**, lai parādītu slēgtās pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="363ca-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="363ca-482">Ievērojiet, ka tiek parādītas kārtošanas pozīcijas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="363ca-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="363ca-483">Tiek parādīts krājums un daudzums, kas tika apstrādāts, izmantojot pozīciju.</span><span class="sxs-lookup"><span data-stu-id="363ca-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="363ca-484">Iestatot izejošās kārtošanas veidni, opcija **Automātiski slēgt kārtošanas pozīciju** ir jāiestata uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="363ca-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="363ca-485">Tādēļ pozīcija tiek automātiski slēgta pēc tam, kad tajā tiek novietots pēdējais paredzētais krājums.</span><span class="sxs-lookup"><span data-stu-id="363ca-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="363ca-486">Kārtošanas pozīcijas statuss ir **Slēgts** un ir izveidots darbs, lai pārvietotu kārtotos krājumus uz novietojumu *Angāra durvis*.</span><span class="sxs-lookup"><span data-stu-id="363ca-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="363ca-487">Pabeidziet kārtoto krājumu izdošanas darbu, lai pārvietotu krājumus uz nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="363ca-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="363ca-488">Kad krājumi ir gatavi, apstipriniet tos nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="363ca-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="363ca-489">Lai kārtoto krājumu izdošanas darbs tiktu apstrādāts pareizi, pārvietošanas un iekraušanas procesam ir jāizmanto mobilās ierīces izvēlnes elements, kam ir darba klases ID, kur lauks **Darba pasūtījuma veids** ir iestatīts uz *Kārtotu krājumu izdošana*.</span><span class="sxs-lookup"><span data-stu-id="363ca-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="363ca-490">Pozīcijas manuāla slēgšana (neobligāts)</span><span class="sxs-lookup"><span data-stu-id="363ca-490">Manually close a position (optional)</span></span>

<span data-ttu-id="363ca-491">Ja kārtošanas pozīcijas jāslēdz manuāli, izejošās kārtošanas veidnes opcijai **Automātiski slēgt kārtošanas pozīciju** jābūt iestatītai uz *Nē*, un slēgšana jāveic pirms krājumus var pārvietot uz angāra durvis zonu.</span><span class="sxs-lookup"><span data-stu-id="363ca-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="363ca-492">Pozīcijas var slēgt dažādos veidos:</span><span class="sxs-lookup"><span data-stu-id="363ca-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="363ca-493">Ar lietotni Warehouse Management mobile:</span><span class="sxs-lookup"><span data-stu-id="363ca-493">Via the Warehouse Management mobile app:</span></span>

    - <span data-ttu-id="363ca-494">Lietotājs var skenēt vienu no krājumiem, kas jau ir pozīcijā, un pēc tam atlasīt **Slēgt**, lai slēgtu pozīciju.</span><span class="sxs-lookup"><span data-stu-id="363ca-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="363ca-495">Ja lietotājs skenē konteineru, kas jau ir sakārtots, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="363ca-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="363ca-496">Tomēr lietotājs joprojām var turpināt pozīcijas slēgšanu.</span><span class="sxs-lookup"><span data-stu-id="363ca-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="363ca-497">Izmantojot lapu Microsoft Dynamics 365 Supply Chain Management **Izejošās kārtošanas pozīcijas piešķires**:</span><span class="sxs-lookup"><span data-stu-id="363ca-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="363ca-498">Lietotājs var atlasīt izejošās kārtošanas pozīcijas ierakstu un pēc tam darbību rūtī atlasīt **Slēgt pozīciju**.</span><span class="sxs-lookup"><span data-stu-id="363ca-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="363ca-499">Padomi</span><span class="sxs-lookup"><span data-stu-id="363ca-499">Tips</span></span>

- <span data-ttu-id="363ca-500">Krājumus nevar pārvietot starp pozīcijām pēc to piešķiršanas.</span><span class="sxs-lookup"><span data-stu-id="363ca-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="363ca-501">Sistēma novērtē, cik daudz no katra krājuma ir jāpārvieto uz noteiktu pozīciju.</span><span class="sxs-lookup"><span data-stu-id="363ca-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="363ca-502">Kārtošanas veidni var konfigurēt, lai automātiski izveidotu konteinerus, kad pozīcijas ir slēgtas.</span><span class="sxs-lookup"><span data-stu-id="363ca-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="363ca-503">Šī pieeja veidos standarta konteinera ID struktūru, kas balstīta uz norādīto iepakošanas profilu.</span><span class="sxs-lookup"><span data-stu-id="363ca-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="363ca-504">Pēc tam, kad no kārtošanas vietas ir izveidots pārvietošanas darbs, darbu nedrīkst atcelt.</span><span class="sxs-lookup"><span data-stu-id="363ca-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="363ca-505">Pretējā gadījumā pozīcija un tajā esošie konteineri tiks dzēsti no sistēmas un nebūs pieejami turpmākai apstrādei.</span><span class="sxs-lookup"><span data-stu-id="363ca-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="363ca-506">Tiks noņemti arī krājumi.</span><span class="sxs-lookup"><span data-stu-id="363ca-506">The inventory will also be removed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]