---
title: Mainīt darba pūlu darbam
description: Šajā tēmā ir paskaidrots, kā darba vienumiem var izmantot pogu Mainīt darba pūlu, lai mainītu esošā darba pūlu.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cdd0a1b6d022c958e00a1ba8fa87a8715ff88ce5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808898"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="8cf6e-103">Mainīt darba pūlu darbam</span><span class="sxs-lookup"><span data-stu-id="8cf6e-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cf6e-104">Darba pūlus var izmantot, lai organizētu darbu grupās.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="8cf6e-105">Piemēram, varat izveidot darba pūlu, lai klasificētu noteiktas noliktavas atrašanās vietā notiekošos darbus.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="8cf6e-106">Līdzeklis *Mainīt darba pūlu darbam* pievieno pogu **Mainīt darba pūlu**, kas atrodas darba vienumu darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="8cf6e-107">Tāpēc noliktavu pārvaldnieki var viegli mainīt esošā darba pūlu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="8cf6e-108">Šis līdzeklis ļauj pārvaldniekiem ātri reaģēt uz izmaiņām noliktavas ražotnē, palīdzot uzlabot spēju pielāgoties mainīgajām situācijām un nepieciešamībai pārsūtīt darbu uz citu darba pūlu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="8cf6e-109">Ieslēgt līdzekli Mainīt darba pūlu darbam</span><span class="sxs-lookup"><span data-stu-id="8cf6e-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="8cf6e-110">Pirms sākat iestatīt vai izmantot šo līdzekli, ir jāpārliecinās, vai tas ir pieejams jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="8cf6e-111">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8cf6e-112">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8cf6e-113">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="8cf6e-114">**Līdzekļa nosaukums:** *Mainīt darba pūlu darbam*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="8cf6e-115">Iestatīt līdzekli Mainīt darba pūlu darbam</span><span class="sxs-lookup"><span data-stu-id="8cf6e-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="8cf6e-116">Lai izmantotu šo līdzekli, ir jābūt iestatītiem darba pūliem.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="8cf6e-117">Varat arī iestatīt darba veidnes, lai tās automātiski piešķirtu pūlu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="8cf6e-118">Ja vēlaties strādāt ar piemēra scenāriju, kas ir sniegts tālāk šajā tēmā, iestatiet sistēmu, kā aprakstīts šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="8cf6e-119">Darba pūlu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8cf6e-119">Set up work pools</span></span>

<span data-ttu-id="8cf6e-120">Darba pūli ļauj kārtot darba vienumus pēc veida.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="8cf6e-121">Lai strādātu ar līdzekli *Mainīt darba pūlu darbam*, ir jābūt pieejamiem vismaz diviem darba pūliem.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="8cf6e-122">Veiciet tālāk norādītās darbības, lai skatītu un pievienotu darba pūlus.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="8cf6e-123">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba pūli**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="8cf6e-124">Ja strādājat ar uzņēmuma **USMF** demonstrācijas datiem un šajā tēmā strādāsiet ar piemēra scenāriju, pievienojiet divus darba pūlus, ar šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="8cf6e-125">1. darba pūls:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-125">Work pool 1:</span></span>

        - <span data-ttu-id="8cf6e-126">**Darba pūla ID:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="8cf6e-127">**Apraksts:** *Tīmekļa veikals*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="8cf6e-128">2. darba pūls:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-128">Work pool 2:</span></span>

        - <span data-ttu-id="8cf6e-129">**Darba pūla ID:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="8cf6e-130">**Apraksts:** *Zvanu centrs*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="8cf6e-131">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="8cf6e-132">Iestatīt darba veidnes</span><span class="sxs-lookup"><span data-stu-id="8cf6e-132">Set up work templates</span></span>

<span data-ttu-id="8cf6e-133">Katrai darba veidnei varat iestatīt noklusējuma darba pūlu, pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="8cf6e-134">Katrai atbilstošajai veidnei ir jāpiešķir darba pūls kolonnā **Darba pūla ID**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="8cf6e-135">Šādā gadījumā visi darba vienumi, kas tiek ģenerēti, izmantojot doto veidni, automātiski pārmanto piešķirto darba pūlu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="8cf6e-136">Ja strādājat ar uzņēmuma **USMF** demonstrācijas datiem un šajā tēmā strādāsiet ar piemēra scenāriju,veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="8cf6e-137">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="8cf6e-138">Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="8cf6e-139">Rediģējiet veidni, iestatot šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="8cf6e-140">**Darba veidne:** *62 izdot iepakošanai*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="8cf6e-141">**Darba pūla ID:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="8cf6e-142">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="8cf6e-143">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="8cf6e-143">Example scenario</span></span>

<span data-ttu-id="8cf6e-144">Šajā scenārijā ir parādīts, kā mainīt pašreizējo darba vienumu apstrādes straumi, mainot to darba pūlu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="8cf6e-145">Tas izmanto uzņēmuma **USMF** demonstrācijas datus un iestatījumus, kas tika ieteikti iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="8cf6e-146">Izveidot pārdošanas pasūtījumu un nodot to noliktavai</span><span class="sxs-lookup"><span data-stu-id="8cf6e-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="8cf6e-147">Apstipriniet, ka rīcībā esošajos krājumos ir pietiekami daudz *A0001* un *A0002* krājumu, noliktavā *62*.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="8cf6e-148">Dodieties uz **Krājumu vadība \> Pieprasījumi un pārskati \> Rīcībā esošs** un rediģējiet filtrus, kā norādīts šeit:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="8cf6e-149">Vērtība **Noliktava** sākas ar *62*.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="8cf6e-150">Vērtība **Krājuma kods** ir vai nu *A001* vai *A002*.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="8cf6e-151">Katram demonstrācijas datu daudzumam jābūt 10.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="8cf6e-152">Pēc tam jāizveido pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="8cf6e-153">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8cf6e-154">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8cf6e-155">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="8cf6e-156">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="8cf6e-157">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="8cf6e-158">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="8cf6e-159">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-159">The new sales order is opened.</span></span> <span data-ttu-id="8cf6e-160">Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="8cf6e-161">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="8cf6e-162">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="8cf6e-163">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="8cf6e-164">Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="8cf6e-165">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="8cf6e-166">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-166">Close the page.</span></span>
1. <span data-ttu-id="8cf6e-167">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai pievienotu vēl vienu pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="8cf6e-168">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="8cf6e-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="8cf6e-169">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="8cf6e-170">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="8cf6e-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="8cf6e-171">Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="8cf6e-172">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="8cf6e-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-173">Close the page.</span></span>
1. <span data-ttu-id="8cf6e-174">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="8cf6e-175">Tiks saņemti informatīvi ziņojumi, kuros būs norādīts no izlaides izveidotais kopuma ID un sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="8cf6e-176">Pierakstiet kopuma ID.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="8cf6e-177">Pārskatiet izejošo kopumu</span><span class="sxs-lookup"><span data-stu-id="8cf6e-177">Review the outbound wave</span></span>

1. <span data-ttu-id="8cf6e-178">Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="8cf6e-179">Režģī meklējiet kopuma ID, kas tika izveidots no pārdošanas pasūtījuma izlaides.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="8cf6e-180">Atlasiet kopuma ID, lai skatītu detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="8cf6e-181">Kopsavilkuma cilnē **Kopuma rindas** pārliecinieties, ka pārdošanas pasūtījumam ir norādīts sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="8cf6e-182">Ja sūtījuma kopuma veidnes iestatījumos opcija **Apstrādāt kopumu, to pārvietojot uz noliktavu** ir iestatīta uz *Nē*, kopums ir jāapstrādā manuāli, darbību rūtī atlasot **Apstrādāt** no cilnes **Kopums**, lai izveidotu darbu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="8cf6e-183">Pārliecinieties, vai kopums ir apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="8cf6e-184">Šī apstrāde izveido nepieciešamo darbu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="8cf6e-185">Skatīt detalizētu informāciju par darbu un mainīt darba pūlu</span><span class="sxs-lookup"><span data-stu-id="8cf6e-185">View work details and change the work pool</span></span>

<span data-ttu-id="8cf6e-186">Varat izmantot lapu **Detalizēta informācija par darbu**, lai skatītu izveidoto darbu un pārvaldītu darba pūlu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="8cf6e-187">Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="8cf6e-188">Atlasiet tikko izveidotā darba rindu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="8cf6e-189">Kolonnā **Pasūtījuma numurs** tiks parādīts pārdošanas pasūtījuma numurs.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="8cf6e-190">Lauks **Darba pūla ID** tiks iestatīts uz darba veidnē iestatīto darba pūla ID.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="8cf6e-191">Ja nav redzams lauks **Darba pūla ID**, pievienojiet kolonnu režģim un pēc tam atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="8cf6e-192">Lai mainītu darba pūlu, kas ir saistīta ar darba ID, darbību rūts cilnē **Darbs** atlasiet **Mainīt darba pūla ID**.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="8cf6e-193">Dialoglodziņā **Mainīt darba pūlu**, kopsavilkuma cilnes **Parametri** laukā **Darba pūla ID** atlasiet *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="8cf6e-194">Atlasiet **Labi**, lai piemērotu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="8cf6e-195">Ievērojiet, ka lauka **Darba pūla ID** vērtība tagad ir nomainīta uz *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cf6e-196">Kad tiek parādīts dialoglodziņš **Mainīt darba pūlu**, lauks **Darba pūla ID** var būt tukšs pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="8cf6e-197">Ja lauks ir tukšs, kad atlasāt **Labi**, lai piemērotu izmaiņas, darba pūls tiks pilnībā noņemts no darba.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="8cf6e-198">Papildus darba pūlu pārslēgšanai šo procedūru var izmantot, lai pievienotu darba pūlu jebkuram darba vienumam, kuram nav darba pūla, vai noņemtu darba pūlu no jebkura darba vienuma, kuram tāds ir.</span><span class="sxs-lookup"><span data-stu-id="8cf6e-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]