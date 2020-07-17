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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4dd188cbd17cfed372283ecb3389633b0c0021eb
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530470"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="a9bf6-104">Kopuma veidņu grupēšana</span><span class="sxs-lookup"><span data-stu-id="a9bf6-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9bf6-105">Kopuma veidņu grupēšana ļauj sistēmai izmantot [kopuma veidnes](tasks/configure-wave-processing.md) iestatījumus, lai, pamatojoties uz jūsu noteiktajiem kritērijiem, definētu, kā ir jāsadala izlaistās rindas un tās jāpiešķir jauniem vai esošiem kopumiem.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="a9bf6-106">Šis līdzeklis var noderēt noliktavās, kur kopumi tiek izveidoti, pamatojoties uz konkrētiem kritērijiem, bet vadītāji dod priekšroku kopumu automātiskai izveidei (nevis manuālai).</span><span class="sxs-lookup"><span data-stu-id="a9bf6-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="a9bf6-107">Tā ļauj sistēmai piešķirt katru no jauna izlaistu sūtījumu pirmajam kopumam, ko sistēma atrod ar atbilstošām grupēšanas lauka vērtībām.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="a9bf6-108">Ja neviena atbilstība netiek atrasta, sistēma jaunajam sūtījumam izveido jaunu kopumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9bf6-109">Kopuma veidņu grupēšana netiek atbalstīta darba veidiem *ražošanas izejmateriāla izdošana* vai *Kanban izdošana*.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="a9bf6-110">Iemesls — kopuma grupēšanas pamatā ir sūtījumi, bet šie darba veidi neizmanto sūtījumus.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="a9bf6-111">Līdzekļa Kopuma veidņu grupēšana ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="a9bf6-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="a9bf6-112">Lai varētu izmantot līdzekli *Kopuma veidņu grupēšana*, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a9bf6-113">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a9bf6-114">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a9bf6-115">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a9bf6-116">**Līdzekļa nosaukums:** *Kopuma veidņu grupēšana*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="a9bf6-117">Iestatiet kopuma veidni, lai izmantotu kopuma veidņu grupēšanu</span><span class="sxs-lookup"><span data-stu-id="a9bf6-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="a9bf6-118">Lai padarītu pieejamu kopuma veidņu grupēšanu, veiciet tālāk norādītās darbības [kopuma veidnes](tasks/configure-wave-processing.md) iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="a9bf6-119">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="a9bf6-120">Kreisajā rūtī atlasiet kopuma veidni, kas jāiestata.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="a9bf6-121">Ja vēlaties ar šajā tēmā minēto scenāriju strādāt vēlāk, izmantojot demonstrācijas datus, atlasiet veidni **62 sūtījuma noklusējums**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="a9bf6-122">Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="a9bf6-123">Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-124">**Automatizēt kopuma izveidi:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="a9bf6-125">**Piešķirt atvērtajiem kopumiem:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="a9bf6-126">**Apstrādāt kopumu, to pārvietojot uz noliktavu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="a9bf6-127">Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="a9bf6-128">Vaicājuma dialoglodziņā cilnē **Kārtošana** pārskatiet kārtošanas kritērijus un pārliecinieties, vai ir iekļauta kārtula, kas ietver lauku, ko vēlaties izmatot jūsu kopumu grupēšanai.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="a9bf6-129">Ja gatavojaties strādāt ar scenāriju, izmantojot demonstrācijas datus, pievienojiet rindu, kurai ir tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="a9bf6-130">**Tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="a9bf6-131">**Atvasinātā tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="a9bf6-132">**Lauks:** *Pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="a9bf6-133">Pēc šīs vērtības atlasīšanas, iespējams, tiks rādīts šāds ziņojums: “Lauks Pārvadātāja pakalpojums nav indeksa lauks.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="a9bf6-134">Vai šim vēlaties pievienot kārtošanu?”</span><span class="sxs-lookup"><span data-stu-id="a9bf6-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="a9bf6-135">Lai pievienotu kārtošanu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="a9bf6-136">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a9bf6-137">Atlasiet **Labi**, lai saglabātu izmaiņas un aizvērtu vaicājuma dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="a9bf6-138">Darbību rūtī atlasiet **Kopuma veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="a9bf6-139">Lapā **Kopuma veidņu grupēšana** atzīmējiet izvēles rūtiņu **Grupēt pēc** katrai rindai, kuru vēlaties izmantot, lai pasūtījuma rindas pēc nepieciešamības grupētu kopumos.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="a9bf6-140">Ja gatavojaties strādāt ar šo scenāriju, izmantojot demonstrācijas datus, rindai *Pārvadātāja pakalpojums* atzīmējiet izvēles rūtiņu **Grupēt pēc**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="a9bf6-141">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-141">Select **Save**.</span></span>
1. <span data-ttu-id="a9bf6-142">Aizveriet lapu **Kopuma veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="a9bf6-143">Atlasiet **Saglabāt**, lai saglabātu veidni.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="a9bf6-144">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="a9bf6-144">Scenario</span></span>

<span data-ttu-id="a9bf6-145">Šajā sadaļā ir nodrošināts skripts, kuru varat izmantot, lai uzzinātu, ko šis līdzeklis nodrošina un kā ar to darboties.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a9bf6-146">Padarīt pieejamus datu paraugus</span><span class="sxs-lookup"><span data-stu-id="a9bf6-146">Make sample data available</span></span>

<span data-ttu-id="a9bf6-147">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a9bf6-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a9bf6-148">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="a9bf6-149">Varat arī izmantot šo scenāriju kā norādījumus, lai līdzekli lietotu darbā ar ražošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="a9bf6-150">Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="a9bf6-151">Scenārijs: Kopuma veidņu grupēšana</span><span class="sxs-lookup"><span data-stu-id="a9bf6-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="a9bf6-152">Šajā scenārijā ir izskaidrots, kā izmantot kopuma veidņu grupēšanu, lai automātiski izveidotu vairākus kopumus, pamatojoties uz kopuma veidnē definētajiem grupēšanas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="a9bf6-153">Šajā scenārijā kopuma veidne ir iestatīta sistēmā, lai katram pārvadātāja pakalpojumam izveidotu vienu kopumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="a9bf6-154">Pirms darba sākšanas sagatavojiet kopuma veidni, kā tas ir iepriekš izklāstīts šīs tēmas sadaļā [Kopuma veidnes iestatīšana, lai izmantotu kopuma veidņu grupēšanu](#set-up-template).</span><span class="sxs-lookup"><span data-stu-id="a9bf6-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="a9bf6-155">Ja strādāsit ar šim scenārijam paredzētajiem demonstrācijas datiem, noteikti izmantojiet šajā procedūrā ieteiktās demonstrācijas datu vērtības.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="a9bf6-156">Šajā iestatījumā kopumi tiks grupēti atbilstoši pārvadātāja pakalpojumam, kas ir iestatīts katram pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="a9bf6-157">1. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="a9bf6-157">Create sales order 1</span></span>

1. <span data-ttu-id="a9bf6-158">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a9bf6-159">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a9bf6-160">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-161">Kopsavilkuma cilnē **Klients** iestatiet laukam **Klienta konts** vērtību *US-004*.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="a9bf6-162">Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="a9bf6-163">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="a9bf6-164">Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="a9bf6-165">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a9bf6-166">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="a9bf6-167">Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-168">**Sūtījuma pārvadātājs:** *Kravas lidmašīnas*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="a9bf6-169">**Pārvadātāja pakalpojums:** *Gaisa*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="a9bf6-170">Pārejiet atpakaļ uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="a9bf6-171">Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="a9bf6-172">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-173">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="a9bf6-174">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="a9bf6-175">Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a9bf6-176">Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="a9bf6-177">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="a9bf6-178">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a9bf6-179">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="a9bf6-180">Pierakstiet kopuma ID numuru un sūtījuma ID numurus.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="a9bf6-181">No 1. pārdošanas pasūtījuma izveidotā kopuma skatīšana</span><span class="sxs-lookup"><span data-stu-id="a9bf6-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="a9bf6-182">Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a9bf6-183">Atlasiet kopuma ID, kas tika izveidots no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="a9bf6-184">Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="a9bf6-185">Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="a9bf6-186">2. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="a9bf6-186">Create sales order 2</span></span>

1. <span data-ttu-id="a9bf6-187">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a9bf6-188">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a9bf6-189">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-190">Kopsavilkuma cilnē **Klients** iestatiet lauka **Klienta konts** vērtību uz *US-005*.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="a9bf6-191">Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="a9bf6-192">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="a9bf6-193">Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="a9bf6-194">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a9bf6-195">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="a9bf6-196">Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-197">**Sūtījuma pārvadātājs:** *Ziedu pārvietošana*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="a9bf6-198">**Pārvadātāja pakalpojums:** *Stand.*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="a9bf6-199">Pārejiet atpakaļ uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="a9bf6-200">Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="a9bf6-201">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-202">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a9bf6-203">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="a9bf6-204">Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a9bf6-205">Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="a9bf6-206">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="a9bf6-207">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a9bf6-208">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="a9bf6-209">Pierakstiet kopuma ID numuru un sūtījuma ID numurus.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="a9bf6-210">Ņemiet vērā, ka kopuma ID atšķiras no pirmā pārdošanas pasūtījuma kopuma ID.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="a9bf6-211">No 2. pārdošanas pasūtījuma izveidotā kopuma skatīšana</span><span class="sxs-lookup"><span data-stu-id="a9bf6-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="a9bf6-212">Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a9bf6-213">Atlasiet kopuma ID, kas tika izveidots no otrā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="a9bf6-214">Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="a9bf6-215">Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="a9bf6-216">Šim sūtījumam tika izveidots jauns kopums, jo tas izmanto no pirmā pārdošanas pasūtījuma atšķirīgu pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="a9bf6-217">3. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="a9bf6-217">Create sales order 3</span></span>

1. <span data-ttu-id="a9bf6-218">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a9bf6-219">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a9bf6-220">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-221">Kopsavilkuma cilnē **Klients** iestatiet lauka **Klienta konts** vērtību uz *US-006*.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="a9bf6-222">Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="a9bf6-223">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="a9bf6-224">Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="a9bf6-225">Pierakstiet pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a9bf6-226">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="a9bf6-227">Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-228">**Sūtījuma pārvadātājs:** *Kravas lidmašīnas*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="a9bf6-229">**Pārvadātāja pakalpojums:** *Gaisa*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="a9bf6-230">Pārejiet atpakaļ uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="a9bf6-231">Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="a9bf6-232">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9bf6-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a9bf6-233">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a9bf6-234">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="a9bf6-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="a9bf6-235">Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a9bf6-236">Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="a9bf6-237">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="a9bf6-238">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a9bf6-239">Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="a9bf6-240">Pierakstiet kopuma ID numuru un sūtījuma ID numurus.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="a9bf6-241">Sūtījums ir piešķirts esošajam kopumam no pirmā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="a9bf6-242">1. un 3. pārdošanas pasūtījuma kopumu skatīšana</span><span class="sxs-lookup"><span data-stu-id="a9bf6-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="a9bf6-243">Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="a9bf6-244">Atlasiet kopuma ID, kas tika izveidots no trešā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="a9bf6-245">Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="a9bf6-246">Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas** kopā ar pirmajam pārdošanas pasūtījumam paredzēto sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
