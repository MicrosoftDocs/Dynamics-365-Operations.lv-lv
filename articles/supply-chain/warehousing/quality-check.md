---
title: Kvalitātes pārbaude
description: Šajā tēmā ir sniegta informācija par Kvalitātes pārbaudes līdzekli. Šis līdzeklis ļauj noliktavas darbiniekiem ātri veikt pārbaudes uz vietas, kamēr tie saņem krājumus saņemšanas doka zonā.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 31afcfcb9d8dbb91f4ea4e3e7a7282c2a87328d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228469"
---
# <a name="quality-check"></a><span data-ttu-id="ef0f2-104">Kvalitātes pārbaude</span><span class="sxs-lookup"><span data-stu-id="ef0f2-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef0f2-105">*Kvalitātes pārbaudes* līdzeklis ļauj noliktavas darbiniekiem ātri veikt pārbaudes uz vietas, kamēr tie saņem krājumus saņemšanas doka zonā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="ef0f2-106">Šīs vietas pārbaudes ir noderīgas, kad darbinieki pārbauda iepakojumu vai citas viegli atpazīstamas krājuma daļas.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="ef0f2-107">Šī funkcija palīdz darbiniekiem ātri apskatīt, vai kaut kas nav acīmredzami kļūdains vai sabojāts, pirms viņi krājumu novieto tā paredzētajā vietā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="ef0f2-108">Šis līdzeklis ir alternatīva standarta kvalitātes pārbaudes procesam.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="ef0f2-109">Tas piedāvā lielāku elastību un ātrāku apstrādi.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="ef0f2-110">Izmantojot šo funkciju, saņemšanas un kvalitātes pārbaude notiek šādi:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="ef0f2-111">Kad sūtījums pienāk, noliktavas darbinieks reģistrē saņemšanu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="ef0f2-112">Darbinieks arī noskenē numura zīmi, lai reģistrētu atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="ef0f2-113">Darbinieks veic ātro kvalitātes pārbaudi un ieraksta rezultātu (izdošana vai kļūme) šai numura zīmei.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="ef0f2-114">Notiek viena no sekojošajām darbībām:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="ef0f2-115">Ja kvalitātes pārbaude ir nokārtota, numura zīme tiek pieņemta un aizvadīta uz saņemšanas vietu kā parasti.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="ef0f2-116">Ja kvalitātes pārbaude neizdodas, numura zīme tiek noraidīta, un esošais izvietošanas darbs tiek novirzīts uz alternatīvo atrašanās vietu turpmākai pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="ef0f2-117">Tiek izveidots jauns kvalitātes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-117">A new quality order is created.</span></span> <span data-ttu-id="ef0f2-118">Lai skatītu kvalitātes pasūtījumu, kas izveidots no neizdevušās kvalitātes pārbaudes, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="ef0f2-119">Šo procesu var arī iestatīt tā, lai visas skenētās numura zīmes tiktu nekavējoties novirzītas uz kvalitātes pārbaudes atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="ef0f2-120">Ieslēgt kvalitātes pārbaudes līdzekli</span><span class="sxs-lookup"><span data-stu-id="ef0f2-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="ef0f2-121">Lai varētu izmantot *Kvalitātes pārbaudes* līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="ef0f2-122">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ef0f2-123">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ef0f2-124">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ef0f2-125">**Līdzekļa nosaukums:** *Kvalitātes pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="ef0f2-126">Iestatīt līdzekli piemēra scenārijam</span><span class="sxs-lookup"><span data-stu-id="ef0f2-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="ef0f2-127">Šajā sadaļā ir sniegti norādījumi un piemērs, kas parāda, kā iestatīt *Kvalitātes pārbaudes* funkciju un sagatavot parauga datus piemēru scenārijam, kas sniegts tālāk šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="ef0f2-128">Padarīt pieejamus datu paraugus</span><span class="sxs-lookup"><span data-stu-id="ef0f2-128">Make sample data available</span></span>

<span data-ttu-id="ef0f2-129">Lai, izmantojot šo [scenārija piemēru](#example-scenario), strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ef0f2-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ef0f2-130">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="ef0f2-131">Kvalitātes pārbaudes veidne</span><span class="sxs-lookup"><span data-stu-id="ef0f2-131">Quality check template</span></span>

<span data-ttu-id="ef0f2-132">Kvalitātes pārbaudes veidne definē noteikumus, lai veiktu ātro pārbaudi uz vietas kvalitātes saņemšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="ef0f2-133">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Kvalitātes pārbaudes veidne**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="ef0f2-134">Atlasiet **Jauns**, lai režģim pievienotu veidni.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="ef0f2-135">Definējot jauno veidni, iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="ef0f2-136">**Kvalitātes pārbaudes veidnes nosaukums:** *Doka pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="ef0f2-137">Ievadiet nosaukumu, kas identificē šai veidnei piemērotās politikas.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="ef0f2-138">**Pieņemšanas politika:** *Uzvedne lietotājam*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="ef0f2-139">Norādiet, vai lietotājiem ir jāsaņem uzvedne, lai pieņemtu vai noraidītu krājumu kvalitāti, kamēr tie apstrādā darbu, vai arī kvalitāte automātiski tiks noraidīta.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="ef0f2-140">Pieejamās opcijas ir *Automātiska noraidīšana* un *Uzvedne lietotājam*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="ef0f2-141">**Kvalitātes apstrādes politika:** *Izveidot kvalitātes pasūtījumu*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="ef0f2-142">Atlasiet politiku, kas jāizmanto, kad krājumu kvalitāte tiek noraidīta.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="ef0f2-143">Pieejamas šādas opcijas</span><span class="sxs-lookup"><span data-stu-id="ef0f2-143">The following options are available:</span></span>

        - <span data-ttu-id="ef0f2-144">*Izveidot tikai darbu* - vienkārši izveidojiet darbu, lai atvieglotu krājumu kustību.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="ef0f2-145">*Izveidot kvalitātes pasūtījumu* - izveidojiet kvalitātes pasūtījumu, lai atvieglotu kvalitātes testus.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="ef0f2-146">**Testa grupa:** *Norobežojums*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="ef0f2-147">Norādiet testu grupu, kas jāizmanto izveidotajā kvalitātes pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="ef0f2-148">Testu grupas ir iestatītas **Krājumu pārvaldības** modulī.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="ef0f2-149">Atstājiet opciju **Destruktīvais teksts** testa grupai izslēgtu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="ef0f2-150">Šī opcija definē, vai paraugs tiks iznīcināts kā daļa no testiem testu grupas ietvaros.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="ef0f2-151">Ja tiek izmantots desktruktīvais tests, sistēma veido krājumu darbību, kad krājumam tiek izveidots kvalitātes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="ef0f2-152">Jaunā krājumu darbība prognozē testa daudzuma krājumu samazināšanos.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="ef0f2-153">Krājumu samazināšana notiek, kad kvalitātes pasūtījums tiek pabeigts, izmantojot validācijas soli.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="ef0f2-154">Krājumu darbība tiek identificēta kā kvalitātes pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="ef0f2-155">Darba klase - Kvalitātes pārbaude</span><span class="sxs-lookup"><span data-stu-id="ef0f2-155">Work class – Quality check</span></span>

<span data-ttu-id="ef0f2-156">Darba klases tiek izmantotas, lai virzītu un/vai ierobežotu darba pasūtījuma rindu tipu, ko noliktavas darbinieki var apstrādāt mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="ef0f2-157">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="ef0f2-158">Atlasiet **Jauns**, lai izveidotu darba klasi.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="ef0f2-159">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-160">**Darba klases ID:** *QC pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="ef0f2-161">Ievadiet nosaukumu, kas identificē darba klasi.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="ef0f2-162">**Apraksts:** *QC pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="ef0f2-163">Ievadiet īsu aprakstu, kas norāda, kam tiek lietota darba klase.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="ef0f2-164">**Darba pasūtījuma tips:** *Kvalitātes pārbaudes kvalitāte*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="ef0f2-165">Atlasiet darba klases izveidoto darba pasūtījumu tipu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="ef0f2-166">Iestatot kvalitātes kontroles darbu, vienmēr atlasiet *Kvalitātes pārbaudes kvalitāti*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="ef0f2-167">Kopsavilkuma cilnē **Derīgs novietojuma tips** atstājiet **Atrašanās vietas veida** lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="ef0f2-168">Ja atlasāt atrašanās vietas tipu, tiek ierobežotas vietas, kur krājumus var ievietot pēc to izdošanas.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="ef0f2-169">Šis lauks tiek izmantots, kad novietojuma direktīva mēģina atrisināt novietojumu vai kad noliktavas darbinieks manuāli precizē mobilās ierīces izvēlnes elementa novietojumu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="ef0f2-170">Lai iegūtu vairāk informācijas par darba klasēm un to izveidi, skatiet sadaļu [Izveidot darba klasi](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="ef0f2-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="ef0f2-171">Darba veidne</span><span class="sxs-lookup"><span data-stu-id="ef0f2-171">Work template</span></span>

<span data-ttu-id="ef0f2-172">Darbu veidnes ļauj jums definēt darba operācijas, kas jāveic noliktavā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="ef0f2-173">Parasti, noliktavas darba operācijas sastāv no darbību pāra: noliktavas darbinieks paņem rīcībā esošos krājumus vienā novietojumā un pēc tam liek paņemtos krājumus citā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="ef0f2-174">Kvalitātes kontroles darba veidne nosaka darba operācijas kvalitātes pārbaužu veikšanai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="ef0f2-175">Pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="ef0f2-175">Purchase orders</span></span>

1. <span data-ttu-id="ef0f2-176">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ef0f2-177">Galvenē iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="ef0f2-178">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef0f2-179">Atlasiet darba veidni, kurai jāietver kvalitātes pārbaudes darbība.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="ef0f2-180">Sadaļā **Pārskats**, kas atrodas laukā **Darba veidnes**, atlasiet *51 PO kvīti*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="ef0f2-181">Sadaļā **Darba veidnes detaļas** ievērojiet, ka režģim ir divas esošas rindas: viena *Saņemšanai* un viena *Izvietošanai*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="ef0f2-182">Sadaļā **Darba veidnes detaļas** atlasiet **Jauns**, lai režģim pievienotu kvalitātes kontroles rindu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="ef0f2-183">Ievērojiet, ka **Rindas numura** lauks jaunajai rindai ir iestatīts uz *3*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="ef0f2-184">Jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-184">On the new line, set the following values.</span></span> <span data-ttu-id="ef0f2-185">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="ef0f2-186">**Darba tips:** *Kvalitātes pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="ef0f2-187">**Darba klases ID:** *Pirkums*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="ef0f2-188">**Kvalitātes pārbaudes veidnes nosaukums:** *Doka pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="ef0f2-189">Atlasiet darba klases unikālo ID.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="ef0f2-190">Šo vērtību izmantojat, lai konfigurētu izvēlnes elementus mobilajā ierīcē un darba veidus, kuru var apstrādāt šīs izvēlnes elementi.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="ef0f2-191">Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jūsu darbu līdz šim.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="ef0f2-192">Jūs saņemat informatīvu ziņojumu, kurā teikts: "Nederīgs - Kvalitātes pārbaudei ir jābūt tieši pēc saņemšanas."</span><span class="sxs-lookup"><span data-stu-id="ef0f2-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="ef0f2-193">Tāpēc **Rindas numura** vērtība ir jāmaina tikko pievienotajai rindai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="ef0f2-194">Lai mainītu **Rindas numura** vērtību jaunajai rindai, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="ef0f2-195">Sadaļā **Darba veidnes detaļas** atlasiet rindu, kur **Darba tipa** lauks ir iestatīts uz *Kvalitātes pārbaude*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="ef0f2-196">Atlasiet pogu **Pārvietot uz augšu** vai uz **Pārvietot uz leju**, lai pārvietotu *Kvalitātes pārbaudes* rindu tā, lai tā būtu pēc *Saņemšanas* rindas.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="ef0f2-197">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="ef0f2-198">Kvalitāte kvalitātes pārbaudē</span><span class="sxs-lookup"><span data-stu-id="ef0f2-198">Quality in quality check</span></span>

<span data-ttu-id="ef0f2-199">Pēc tam izveidojiet darba veidni kvalitātes pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="ef0f2-200">Lapas **Darba veidnes** virsrakstā mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kvalitāte kvalitātes pārbaudē*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="ef0f2-201">Lai režģim sadaļā **Pārskats** pievienotu rindu, darbības rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="ef0f2-202">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-203">**Darba veidne:** *51 kvalitātes pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="ef0f2-204">Ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="ef0f2-205">**Darba veidnes apraksts:** *51 kvalitātes pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="ef0f2-206">Darbības rūtī atlasiet **Saglabāt**, lai padarītu pieejamu sadaļu **Darba veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="ef0f2-207">Kamēr jaunā veidne joprojām ir atlasīta sadaļā **Pārskats**, atlasiet **Jauns** sadaļā **Darba veidnes informācija**, lai režģī pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="ef0f2-208">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-209">**Darba veids:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="ef0f2-210">**Darba klases ID:** *QC pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="ef0f2-211">Atlasiet [Darba klases](#work-class) nosaukumu, ko izveidojāt iepriekš kvalitātes kontroles darbam.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="ef0f2-212">Sadaļā **Darba veidnes informācija** atlasiet **Jauns**, lai pievienotu citu rindu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="ef0f2-213">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-214">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="ef0f2-215">**Darba klases ID:** *QC pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="ef0f2-216">Atlasiet [Darba klases](#work-class) nosaukumu, ko izveidojāt iepriekš kvalitātes kontroles darbam.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="ef0f2-217">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="ef0f2-218">Plašāku informāciju par darbu veidnēm skatiet sadaļā [Noliktavas darbu kontrolēšana, izmantojot darba veidnes un novietojuma direktīvas](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="ef0f2-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="ef0f2-219">Novietojuma direktīva — kvalitātes kļūmes</span><span class="sxs-lookup"><span data-stu-id="ef0f2-219">Location directive – Quality failures</span></span>

<span data-ttu-id="ef0f2-220">Novietojuma direktīvas ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="ef0f2-221">Piemēram, pārdošanas pasūtījuma transakcijā novietojuma direktīva nosaka, kur krājumi tiks izdoti un kur izdotie krājumi tiks izvietoti.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="ef0f2-222">Jums ir jākonfigurē novietojuma direktīvas kārtula, lai noteiktu, kā tiek apstrādātas neveiksmīgas kvalitātes pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="ef0f2-223">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ef0f2-224">Kreisās puses rūtī iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumiem*, lai strādātu ar šāda veida atrašanās vietas direktīvām.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="ef0f2-225">Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma direktīvu kvalitātes pārbaudēm.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="ef0f2-226">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-227">**Kārtas numurs:** akceptējiet noklusējuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="ef0f2-228">**Nosaukums:** *51 uz kvalitāti*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="ef0f2-229">Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="ef0f2-230">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="ef0f2-231">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="ef0f2-232">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-232">**Site:** *5*</span></span>
    - <span data-ttu-id="ef0f2-233">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ef0f2-234">Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jūsu direktīvu un padarītu kopsavilkuma cilni **Rindas** pieejamu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="ef0f2-235">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ef0f2-236">Jaunajā rindā iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-236">On the new line, set the following values.</span></span> <span data-ttu-id="ef0f2-237">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="ef0f2-238">**No daudzuma:** *1*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="ef0f2-239">**Līdz daudzumam:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="ef0f2-240">Darbības rūtī atlasiet **Saglabāt**, lai saglabātu jauno rindu un padarītu kopsavilkuma cilni **Novietojuma direktīvas darbības** pieejamu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="ef0f2-241">Kamēr jaunā rinda joprojām ir atlasīta kopsavilkuma cilnē **Rindas** atlasiet **Jauns** kopsavilkuma cilnē **Novietojuma direktīvas darbības**, lai režģī pievienotu rindu, tādējādi rindai var iestatīt darbību.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="ef0f2-242">Jaunā rindā iestatiet **Nosaukums** lauku uz *Kvalitāte*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="ef0f2-243">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="ef0f2-244">Darbības rūtī atlasiet **Saglabāt**, lai padarītu pogu **Rediģēt vaicājumu** pieejamu **Novietojuma direktīvu darbības** kopsavilkuma cilnē.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="ef0f2-245">Kamēr tikko pievienotā rinda joprojām ir atlasīta kopsavilkuma cilnē **Novietojuma direktīvas darbības**, atlasiet **Rediģēt vaicājumu**, lai atvērtu dialoglodziņu, kur varat rediģēt vaicājumu darbībai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="ef0f2-246">Cilnē **Diapazons** atlasiet **Pievienot**, lai vaicājumam pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="ef0f2-247">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-248">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ef0f2-249">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="ef0f2-250">**Lauks:** *Novietojums*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="ef0f2-251">**Kritēriji:** *KPS*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="ef0f2-252">*QMS* atrašanās vieta ir noliktavas atrašanās vieta kvalitātei.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="ef0f2-253">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ef0f2-254">Jums tūlīt ir jānomaina pirkšanas pasūtījuma novietojuma direktīvu secība noliktavai *51*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="ef0f2-255">Saglabājiet jauno *51 uz kvalitāti* novietojuma direktīvu, atsvaidziniet lapu un sarakstā atlasiet atrašanās vietas direktīvu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="ef0f2-256">Pēc tam darbības rūtī izmantojiet pogas **Pārvietot uz augšu** un uz **Pārvietot uz leju**, lai novietojuma direktīvu ievietotu noliktavai *51* šādā secībā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="ef0f2-257">(Pirms atlasāt **Pārvietot uz augšu** vai uz **Pārvietot uz leju**, sarakstā atlasiet atrašanās vietas direktīvu.)</span><span class="sxs-lookup"><span data-stu-id="ef0f2-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="ef0f2-258">51 uz kvalitāti</span><span class="sxs-lookup"><span data-stu-id="ef0f2-258">51 To Quality</span></span>
    2. <span data-ttu-id="ef0f2-259">51 PO tiešais</span><span class="sxs-lookup"><span data-stu-id="ef0f2-259">51 PO Direct</span></span>
    3. <span data-ttu-id="ef0f2-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="ef0f2-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="ef0f2-261">Mobilās ierīces izvēlnes vienumi</span><span class="sxs-lookup"><span data-stu-id="ef0f2-261">Mobile device menu items</span></span>

<span data-ttu-id="ef0f2-262">Konfigurējiet izvēlnes elementu, lai mobilās ierīces varētu veikt **Kvalitātes pārbaudes** funkciju.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="ef0f2-263">Pirkuma izvietošana</span><span class="sxs-lookup"><span data-stu-id="ef0f2-263">Purchase putaway</span></span>

1. <span data-ttu-id="ef0f2-264">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ef0f2-265">Sarakstā atlasiet **Pirkšanas izvietošana** izvēlnes krājumu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="ef0f2-266">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef0f2-267">Sadaļā **Darba klases** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="ef0f2-268">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-269">**Darba klases ID:** *QC pārbaude*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="ef0f2-270">Ievadiet [Darba klases](#work-class) nosaukumu, ko izveidojāt iepriekš kvalitātes kontroles darbam.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="ef0f2-271">**Darba pasūtījuma tips:** *Kvalitātes pārbaudes kvalitāte*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="ef0f2-272">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="ef0f2-273">Pirkšanas pasūtījuma rindas saņemšana</span><span class="sxs-lookup"><span data-stu-id="ef0f2-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="ef0f2-274">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ef0f2-275">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ef0f2-276">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-277">**Izvēlnes elementa nosaukums:** *PO rindas saņemšana*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="ef0f2-278">**Nosaukums:** *PO rindas saņemšana*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="ef0f2-279">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ef0f2-280">**Izmantot esošo darbu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="ef0f2-281">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="ef0f2-282">Pieņemiet noklusējuma vērtības atlikušajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="ef0f2-283">**Darba izveides process:** *Pirkšanas pasūtījuma rindas saņemšana un nosūtīšana*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="ef0f2-284">**Ģenerēt numura zīmi:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="ef0f2-285">**Darba veidne:** *51 PP kvīts*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="ef0f2-286">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="ef0f2-287">Izvēlnes elementa pievienošana mobilās ierīces izvēlnei</span><span class="sxs-lookup"><span data-stu-id="ef0f2-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="ef0f2-288">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="ef0f2-289">Kreisajā rūtī atlasiet izvēlni **Ienākošie**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="ef0f2-290">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ef0f2-291">Kolonnā **Pieejamās izvēlnes un izvēlņu elementi** atrodiet jaunu **PP rindas saņemšanas** izvēlnes elementu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="ef0f2-292">Atlasiet bultiņas pa labi pogu, lai pārvietotu **PP rindas saņemšana** uz kolonnu **Izvēlnes struktūra**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="ef0f2-293">Kolonnā **Izvēlnes struktūra** atlasiet **PP rindas saņemšanu** un atlasiet augšupvērsto un lejupvērsto bultiņu, lai pārvietot izvēlnes elementu uz vēlamo pozīciju mobilās lietotnes izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="ef0f2-294">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="ef0f2-295">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="ef0f2-295">Example scenario</span></span>

<span data-ttu-id="ef0f2-296">Pēc tam, kad esat veicis visus iepriekš aprakstītos, pieejamos parauga datus un to iestatījis, varat strādāt ar šo scenāriju, lai izmēģinātu *Kvalitātes pārbaudes* funkciju.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="ef0f2-297">Šajā scenārijā parādītās vērtības pieņem, ka strādājat ar standarta demonstrācijas datiem, ar kuriem atlasījāt **USMF** juridisko personu un ka sagatavojāt parauga ierakstus, kas ir aprakstīti iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="ef0f2-298">Šis scenārijs kalpo arī kā piemērs, kas parāda, kā līdzekli var izmantot ražošanas iestatījumā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="ef0f2-299">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="ef0f2-299">Create a purchase order</span></span>

1. <span data-ttu-id="ef0f2-300">Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="ef0f2-301">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ef0f2-302">Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-303">**Tirgotāja konts:** *104*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="ef0f2-304">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ef0f2-305">Atlasiet **Labi**, lai aizvērtu dialoglodziņu un atvērtu jaunu pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="ef0f2-306">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** režģim tiek pievienota jauna, tukša rinda.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="ef0f2-307">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="ef0f2-308">**Krājuma numurs:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="ef0f2-309">**Daudzums:** *3*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="ef0f2-310">**Vienība:** *PL*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="ef0f2-311">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="ef0f2-312">Apstrādāt kvalitātes pārbaudes saņemšanu</span><span class="sxs-lookup"><span data-stu-id="ef0f2-312">Process quality check receiving</span></span>

<span data-ttu-id="ef0f2-313">Pēc tam, kad pirkšanas pasūtījums ir izveidots, to var saņemt, izmantojot **PP rindas saņemšanas** izvēlnes elementu un *Kvalitātes pārbaudes* funkciju.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="ef0f2-314">Saņemt paletes 1</span><span class="sxs-lookup"><span data-stu-id="ef0f2-314">Receive pallet 1</span></span>

1. <span data-ttu-id="ef0f2-315">Pierakstieties noliktavas programmā kā lietotājs noliktavai *51*.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="ef0f2-316">(Ievadiet *51* kā lietotāja ID un *1* kā paroli.)</span><span class="sxs-lookup"><span data-stu-id="ef0f2-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ef0f2-317">Dodieties uz **Ienākošie \> PP rindas saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="ef0f2-318">Laukā **PONUM** ievadiet savu pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="ef0f2-319">Apstipriniet pirkšanas pasūtījumu numuru.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="ef0f2-320">Laukā **LINENUM** ievadiet pirkšanas pasūtījuma rindas numuru, kas tiek saņemts.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="ef0f2-321">Tā kā pasūtījumam šajā scenārijā ir tikai viena rinda, jums jāievada *1* laukā **LINENUM** katram saņemšanas solim.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="ef0f2-322">Apstipriniet rindas numuru.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-322">Confirm the line number.</span></span>
1. <span data-ttu-id="ef0f2-323">Ievadiet saņemto daudzumu laukā **DAUDZ.**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="ef0f2-324">Tā kā pirkšanas pasūtījums ir paredzēts trīs paletēm (*PL*) šajā scenārijā, un ir trīs saņemšanas soļi, jūs ievadīsiet *1* laukā **DAUDZ.** katrai saņemšanas darbībai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="ef0f2-325">Apstipriniet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-325">Confirm the quantity.</span></span>

    <span data-ttu-id="ef0f2-326">Lapā **Kvalitātes pārbaude**, kas parādās, nav ierakstu lauku.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="ef0f2-327">Tam ir tikai apstiprinājuma (atzīme) poga apakšā un izvēlnes poga (**≡**) augšā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="ef0f2-328">(Izvēlnes poga dažreiz tiek saukta par hamburgeru vai hamburgeru pogu.) Lai paātrinātu kvalitātes pārbaudes procesu, kad palete iztur kvalitātes pārbaudi, lietotājs vienkārši apstiprina **Kvalitātes pārbaudes** lapu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="ef0f2-329">![Kvalitātes pārbaudes lapa](media/quality-check.png "Kvalitātes pārbaudes lapa")</span><span class="sxs-lookup"><span data-stu-id="ef0f2-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="ef0f2-330">Izvēlieties apstiprināšanas pogu, lai nokārtotu kvalitātes pārbaudi paletei 1 no 1. rindas.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="ef0f2-331">**Pirkšanas pasūtījumi: Izvietot** lapa parāda detalizētu informāciju par izvietošanas darbu:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="ef0f2-332">**LOC:** sistēmas noteiktā atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="ef0f2-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="ef0f2-333">Šī atrašanās vieta ir norādītā izvietošanas vieta pirkšanas pasūtījuma saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="ef0f2-334">**LP:** sistēmas ģenerētais numura zīmes ID</span><span class="sxs-lookup"><span data-stu-id="ef0f2-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="ef0f2-335">**Krājums:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="ef0f2-336">**Daudzums:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="ef0f2-337">Tiek norādīts arī krājuma apraksts.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-337">The item description is also shown.</span></span>

1. <span data-ttu-id="ef0f2-338">Apstipriniet izvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="ef0f2-339">Lapā **Uzdevums** pirkšanas pasūtījuma rindas saņemšanai jūs saņemsiet ziņojumu "Darbs pabeigts".</span><span class="sxs-lookup"><span data-stu-id="ef0f2-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="ef0f2-340">Lauks **LINENUM** ir pieejams, lai varētu sākt saņemt nākamo paleti.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="ef0f2-341">Saņemt paletes 2</span><span class="sxs-lookup"><span data-stu-id="ef0f2-341">Receive pallet 2</span></span>

<span data-ttu-id="ef0f2-342">Šim scenārijam palete 2 tiks noraidīta.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="ef0f2-343">Laukā **LINENUM** ievadiet *1* un apstipriniet rindas numuru.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="ef0f2-344">Lauks **DAUDZ.** tagad ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-344">The **QTY** field is now available.</span></span> <span data-ttu-id="ef0f2-345">Ievadiet *1* un apstipriniet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="ef0f2-346">Tiek parādīta lapa **Kvalitātes pārbaude**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-346">The **Quality check** page appears.</span></span> <span data-ttu-id="ef0f2-347">Šai kvīts paletei kvalitāte tiks noraidīta, un tā tiks ievietota *QMS* kvalitātes novietojumā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="ef0f2-348">Lapas augšā atlasiet izvēlnes pogu (**≡**), un pēc tam izvēlnē atlasiet **Noraidīt**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="ef0f2-349">Parādītajā lapā **Uzdevums** ievadiet **QMS** kā *Izvietot* novietojumu, lai nosūtītu paletes tālākai pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="ef0f2-350">**Kvalitāte kvalitātes pārbaudē: Izvietot** lapa parāda detalizētu informāciju par izvietošanas darbu:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="ef0f2-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="ef0f2-352">Šī atrašanās vieta ir norādītā izvietošanas vieta noraidītai kvalitātes saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="ef0f2-353">**LP:** sistēmas ģenerētais numura zīmes ID</span><span class="sxs-lookup"><span data-stu-id="ef0f2-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="ef0f2-354">**Krājums:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="ef0f2-355">**Daudzums:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="ef0f2-356">Tiek norādīts arī krājuma apraksts.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-356">The item description is also shown.</span></span>

1. <span data-ttu-id="ef0f2-357">Apstipriniet izvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="ef0f2-358">Lapā **Uzdevums** pirkšanas pasūtījuma rindas saņemšanai jūs saņemsiet ziņojumu "Darbs pabeigts".</span><span class="sxs-lookup"><span data-stu-id="ef0f2-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="ef0f2-359">Lauks **LINENUM** ir pieejams, lai varētu sākt saņemt nākamo paleti.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="ef0f2-360">Tagad jūs esat pabeiguši kvalitātes pārbaudi un izveidojis kvalitātes pasūtījumu noraidītajai paletei.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="ef0f2-361">Lai skatītu izveidoto kvalitātes pasūtījumu, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="ef0f2-362">Kvalitātes pasūtījumu pārbaudes tagad var apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="ef0f2-363">Šajā tēmā nav iekļauta kvalitātes testēšana.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="ef0f2-364">Papildinformāciju par kvalitātes pārvaldību skatiet [Pārskats par kvalitātes pārvaldību](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="ef0f2-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="ef0f2-365">Saņemt paletes 3</span><span class="sxs-lookup"><span data-stu-id="ef0f2-365">Receive pallet 3</span></span>

<span data-ttu-id="ef0f2-366">Šim scenārijam palete 3 tiks pieņemta.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="ef0f2-367">Laukā **LINENUM** ievadiet *1* un apstipriniet rindas numuru.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="ef0f2-368">Lauks **DAUDZ.** tagad ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-368">The **QTY** field is now available.</span></span> <span data-ttu-id="ef0f2-369">Ievadiet *1* un apstipriniet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="ef0f2-370">Tiek parādīta lapa **Kvalitātes pārbaude**.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-370">The **Quality check** page appears.</span></span> <span data-ttu-id="ef0f2-371">Šai kvīts paletei kvalitāte tiks pieņemta, un tā tiks ievietota vairuma izvietošanas novietojumā.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="ef0f2-372">Izvēlieties apstiprināšanas pogu, lai nokārtotu kvalitātes pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="ef0f2-373">**Pirkšanas pasūtījumi: Izvietot** lapa parāda detalizētu informāciju par izvietošanas darbu:</span><span class="sxs-lookup"><span data-stu-id="ef0f2-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="ef0f2-374">**LOC:** sistēmas noteiktā atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="ef0f2-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="ef0f2-375">Šī atrašanās vieta ir norādītā izvietošanas vieta pirkšanas pasūtījuma saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="ef0f2-376">**LP:** sistēmas ģenerētais numura zīmes ID</span><span class="sxs-lookup"><span data-stu-id="ef0f2-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="ef0f2-377">**Krājums:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="ef0f2-378">**Daudzums:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="ef0f2-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="ef0f2-379">Tiek norādīts arī krājuma apraksts.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-379">The item description is also shown.</span></span>

1. <span data-ttu-id="ef0f2-380">Apstipriniet izvietošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="ef0f2-381">Lapā **Uzdevums** pirkšanas pasūtījuma rindas saņemšanai jūs saņemsiet ziņojumu "Darbs pabeigts".</span><span class="sxs-lookup"><span data-stu-id="ef0f2-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="ef0f2-382">Lauks **LINENUM** ir pieejams, lai varētu sākt saņemt nākamo paleti.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="ef0f2-383">Lapas augšā atlasiet izvēlnes pogu (**≡**), un pēc tam izvēlnē atlasiet **Atcelt**, lai atgrieztos izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="ef0f2-384">Tagad varat aizvērt mobilo programmu.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-384">You can now close the mobile app.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]