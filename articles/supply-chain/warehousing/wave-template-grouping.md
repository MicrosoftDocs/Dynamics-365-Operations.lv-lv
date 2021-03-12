---
title: Kopuma veidņu grupēšana
description: Kopuma veidņu grupēšana ļauj sistēmai izmantot kopuma veidnes iestatījumus, lai, pamatojoties uz jūsu noteiktajiem kritērijiem, definētu, kā ir jāsadala izlaistās rindas un tās jāpiešķir jauniem vai esošiem kopumiem. Šis līdzeklis var noderēt noliktavās, kur kopumi tiek izveidoti, pamatojoties uz konkrētiem kritērijiem, bet vadītāji dod priekšroku kopumu automātiskai izveidei (nevis manuālai).
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b422eb432e579d4ae914fbc0efa79aaa15f1de27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998382"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="e6cd4-104">Kopuma veidņu grupēšana</span><span class="sxs-lookup"><span data-stu-id="e6cd4-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6cd4-105">Kopuma veidņu grupēšana ļauj sistēmai izmantot [kopuma veidnes](tasks/configure-wave-processing.md) iestatījumus, lai, pamatojoties uz jūsu noteiktajiem kritērijiem, definētu, kā ir jāsadala izlaistās rindas un tās jāpiešķir jauniem vai esošiem kopumiem.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="e6cd4-106">Šis līdzeklis var noderēt noliktavās, kur kopumi tiek izveidoti, pamatojoties uz konkrētiem kritērijiem, bet vadītāji dod priekšroku kopumu automātiskai izveidei (nevis manuālai).</span><span class="sxs-lookup"><span data-stu-id="e6cd4-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="e6cd4-107">Tā ļauj sistēmai piešķirt katru no jauna izlaistu sūtījumu pirmajam kopumam, ko sistēma atrod ar atbilstošām grupēšanas lauka vērtībām.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="e6cd4-108">Ja neviena atbilstība netiek atrasta, sistēma jaunajam sūtījumam izveido jaunu kopumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e6cd4-109">Kopuma veidņu grupēšana netiek atbalstīta darba veidiem *ražošanas izejmateriāla izdošana* vai *Kanban izdošana*.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="e6cd4-110">Iemesls — kopuma grupēšanas pamatā ir sūtījumi, bet šie darba veidi neizmanto sūtījumus.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="e6cd4-111">Līdzekļa Kopuma veidņu grupēšana ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="e6cd4-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="e6cd4-112">Lai varētu izmantot līdzekli *Kopuma veidņu grupēšana*, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="e6cd4-113">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e6cd4-114">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e6cd4-115">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e6cd4-116">**Līdzekļa nosaukums:** *Kopuma veidņu grupēšana*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="e6cd4-117">Iestatiet kopuma veidni, lai izmantotu kopuma veidņu grupēšanu</span><span class="sxs-lookup"><span data-stu-id="e6cd4-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="e6cd4-118">Lai padarītu pieejamu kopuma veidņu grupēšanu, veiciet tālāk norādītās darbības [kopuma veidnes](tasks/configure-wave-processing.md) iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="e6cd4-119">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="e6cd4-120">Kreisajā rūtī atlasiet kopuma veidni, kas jāiestata.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="e6cd4-121">Ja vēlaties ar šajā tēmā minēto scenāriju strādāt vēlāk, izmantojot demonstrācijas datus, atlasiet veidni **62 sūtījuma noklusējums**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="e6cd4-122">Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="e6cd4-123">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-124">**Automatizēt kopuma izveidi:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="e6cd4-125">**Piešķirt atvērtajiem kopumiem:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="e6cd4-126">**Apstrādāt kopumu, to pārvietojot uz noliktavu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="e6cd4-127">Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="e6cd4-128">Vaicājuma dialoglodziņā cilnē **Kārtošana** pārskatiet kārtošanas kritērijus un pārliecinieties, vai ir iekļauta kārtula, kas ietver lauku, ko vēlaties izmatot jūsu kopumu grupēšanai.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="e6cd4-129">Ja gatavojaties strādāt ar scenāriju, izmantojot demonstrācijas datus, pievienojiet rindu, kurai ir tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="e6cd4-130">**Tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e6cd4-131">**Atvasinātā tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e6cd4-132">**Lauks:** *Pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="e6cd4-133">Pēc šīs vērtības atlasīšanas, iespējams, tiks rādīts šāds ziņojums: “Lauks Pārvadātāja pakalpojums nav indeksa lauks.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="e6cd4-134">Vai šim vēlaties pievienot kārtošanu?”</span><span class="sxs-lookup"><span data-stu-id="e6cd4-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="e6cd4-135">Lai pievienotu kārtošanu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="e6cd4-136">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e6cd4-137">Atlasiet **Labi**, lai saglabātu izmaiņas un aizvērtu vaicājuma dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="e6cd4-138">Darbību rūtī atlasiet **Kopuma veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="e6cd4-139">Lapā **Kopuma veidņu grupēšana** atzīmējiet izvēles rūtiņu **Grupēt pēc** katrai rindai, kuru vēlaties izmantot, lai pasūtījuma rindas pēc nepieciešamības grupētu kopumos.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="e6cd4-140">Ja gatavojaties strādāt ar šo scenāriju, izmantojot demonstrācijas datus, rindai *Pārvadātāja pakalpojums* atzīmējiet izvēles rūtiņu **Grupēt pēc**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="e6cd4-141">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-141">Select **Save**.</span></span>
1. <span data-ttu-id="e6cd4-142">Aizveriet lapu **Kopuma veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="e6cd4-143">Atlasiet **Saglabāt**, lai saglabātu veidni.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="e6cd4-144">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="e6cd4-144">Scenario</span></span>

<span data-ttu-id="e6cd4-145">Šajā sadaļā ir nodrošināts skripts, kuru varat izmantot, lai uzzinātu, ko šis līdzeklis nodrošina un kā ar to darboties.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="e6cd4-146">Padarīt pieejamus datu paraugus</span><span class="sxs-lookup"><span data-stu-id="e6cd4-146">Make sample data available</span></span>

<span data-ttu-id="e6cd4-147">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e6cd4-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="e6cd4-148">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="e6cd4-149">Varat arī izmantot šo scenāriju kā norādījumus, lai līdzekli lietotu darbā ar ražošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="e6cd4-150">Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="e6cd4-151">Scenārijs: Kopuma veidņu grupēšana</span><span class="sxs-lookup"><span data-stu-id="e6cd4-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="e6cd4-152">Šajā scenārijā ir izskaidrots, kā izmantot kopuma veidņu grupēšanu, lai automātiski izveidotu vairākus kopumus, pamatojoties uz kopuma veidnē definētajiem grupēšanas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="e6cd4-153">Šajā scenārijā kopuma veidne ir iestatīta sistēmā, lai katram pārvadātāja pakalpojumam izveidotu vienu kopumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="e6cd4-154">Pirms darba sākšanas sagatavojiet kopuma veidni, kā tas ir iepriekš izklāstīts šīs tēmas sadaļā [Kopuma veidnes iestatīšana, lai izmantotu kopuma veidņu grupēšanu](#set-up-template).</span><span class="sxs-lookup"><span data-stu-id="e6cd4-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="e6cd4-155">Ja strādāsit ar šim scenārijam paredzētajiem demonstrācijas datiem, noteikti izmantojiet šajā procedūrā ieteiktās demonstrācijas datu vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="e6cd4-156">Šajā iestatījumā kopumi tiks grupēti atbilstoši pārvadātāja pakalpojumam, kas ir iestatīts katram pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="e6cd4-157">1. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="e6cd4-157">Create sales order 1</span></span>

1. <span data-ttu-id="e6cd4-158">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e6cd4-159">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="e6cd4-160">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-161">Kopsavilkuma cilnē **Klients** iestatiet laukam **Klienta konts** vērtību *US-004*.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="e6cd4-162">Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="e6cd4-163">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="e6cd4-164">Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="e6cd4-165">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="e6cd4-166">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="e6cd4-167">Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-168">**Sūtījuma pārvadātājs:** *Kravas lidmašīnas*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="e6cd4-169">**Pārvadātāja pakalpojums:** *Gaisa*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="e6cd4-170">Pārejiet atpakaļ uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="e6cd4-171">Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="e6cd4-172">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-173">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="e6cd4-174">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="e6cd4-175">Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e6cd4-176">Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="e6cd4-177">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e6cd4-178">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="e6cd4-179">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="e6cd4-180">Pierakstiet kopuma ID numuru un sūtījuma ID numurus.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="e6cd4-181">No 1. pārdošanas pasūtījuma izveidotā kopuma skatīšana</span><span class="sxs-lookup"><span data-stu-id="e6cd4-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="e6cd4-182">Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="e6cd4-183">Atlasiet kopuma ID, kas tika izveidots no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="e6cd4-184">Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="e6cd4-185">Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="e6cd4-186">2. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="e6cd4-186">Create sales order 2</span></span>

1. <span data-ttu-id="e6cd4-187">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e6cd4-188">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="e6cd4-189">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-190">Kopsavilkuma cilnē **Klients** iestatiet lauka **Klienta konts** vērtību uz *US-005*.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="e6cd4-191">Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="e6cd4-192">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="e6cd4-193">Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="e6cd4-194">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="e6cd4-195">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="e6cd4-196">Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-197">**Sūtījuma pārvadātājs:** *Ziedu pārvietošana*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="e6cd4-198">**Pārvadātāja pakalpojums:** *Stand.*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="e6cd4-199">Pārejiet atpakaļ uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="e6cd4-200">Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="e6cd4-201">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-202">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="e6cd4-203">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="e6cd4-204">Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e6cd4-205">Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="e6cd4-206">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e6cd4-207">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="e6cd4-208">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="e6cd4-209">Pierakstiet kopuma ID numuru un sūtījuma ID numurus.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="e6cd4-210">Ņemiet vērā, ka kopuma ID atšķiras no pirmā pārdošanas pasūtījuma kopuma ID.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="e6cd4-211">No 2. pārdošanas pasūtījuma izveidotā kopuma skatīšana</span><span class="sxs-lookup"><span data-stu-id="e6cd4-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="e6cd4-212">Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="e6cd4-213">Atlasiet kopuma ID, kas tika izveidots no otrā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="e6cd4-214">Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="e6cd4-215">Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="e6cd4-216">Šim sūtījumam tika izveidots jauns kopums, jo tas izmanto no pirmā pārdošanas pasūtījuma atšķirīgu pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="e6cd4-217">3. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="e6cd4-217">Create sales order 3</span></span>

1. <span data-ttu-id="e6cd4-218">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e6cd4-219">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="e6cd4-220">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-221">Kopsavilkuma cilnē **Klients** iestatiet lauka **Klienta konts** vērtību uz *US-006*.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="e6cd4-222">Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="e6cd4-223">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="e6cd4-224">Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="e6cd4-225">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="e6cd4-226">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="e6cd4-227">Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-228">**Sūtījuma pārvadātājs:** *Kravas lidmašīnas*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="e6cd4-229">**Pārvadātāja pakalpojums:** *Gaisa*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="e6cd4-230">Pārejiet atpakaļ uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="e6cd4-231">Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="e6cd4-232">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e6cd4-233">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="e6cd4-234">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="e6cd4-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="e6cd4-235">Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e6cd4-236">Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="e6cd4-237">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e6cd4-238">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="e6cd4-239">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="e6cd4-240">Pierakstiet kopuma ID numuru un sūtījuma ID numurus.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="e6cd4-241">Sūtījums ir piešķirts esošajam kopumam no pirmā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="e6cd4-242">1. un 3. pārdošanas pasūtījuma kopumu skatīšana</span><span class="sxs-lookup"><span data-stu-id="e6cd4-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="e6cd4-243">Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="e6cd4-244">Atlasiet kopuma ID, kas tika izveidots no trešā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="e6cd4-245">Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="e6cd4-246">Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas** kopā ar pirmajam pārdošanas pasūtījumam paredzēto sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
