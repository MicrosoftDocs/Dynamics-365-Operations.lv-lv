---
title: Iestatīt dažādas iepakošanas un glabāšanas dimensijas
description: Šajā tēmā ir parādīts, kā norādīt, kurai procesam (iepakošanai, uzglabāšanai vai ligzdotam iepakojumam) tiek izmantota katra noteiktā dimensija.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078286"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="96d75-103">Iestatīt dažādas iepakošanas un glabāšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="96d75-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96d75-104">Daži krājumi tiek iepakoti vai uzglabāti tā, ka katram no vairākiem dažādiem procesiem fiziskās dimensijas var būt atšķirīgas.</span><span class="sxs-lookup"><span data-stu-id="96d75-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="96d75-105">Funkcija *Iepakojuma preces dimensijas* ļauj iestatīt katram produktam vienu vai vairākus dimensiju tipus.</span><span class="sxs-lookup"><span data-stu-id="96d75-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="96d75-106">Katrs dimensiju tips sniedz fizisko mērījumu kopu (svars, platums, dziļums un augstums) un nosaka procesu, kur tiek pielietotas šīs fiziskās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="96d75-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="96d75-107">Kad šī funkcija ir aktivizēta, sistēma atbalsta šādus dimensiju tipus:</span><span class="sxs-lookup"><span data-stu-id="96d75-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="96d75-108">*Noliktava* - noliktavas dimensijas tiek izmantotas kopā ar atrašanās vietas tilpums, lai noteiktu, cik no katra krājuma var uzglabāt dažādās noliktavas vietās.</span><span class="sxs-lookup"><span data-stu-id="96d75-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="96d75-109">*Iepakošana* - iepakošanas dimensijas tiek izmantotas konteinerinēšanas un manuālās iepakošanas procesa laikā, lai noteiktu, cik daudz katra krājuma iederēsies dažādos konteinera tipos.</span><span class="sxs-lookup"><span data-stu-id="96d75-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="96d75-110">*Ligzdots iepakojums* - ligzdotas iepakojuma dimensijas tiek izmantotas, kad iepakošanas procesā ir vairāki līmeņi.</span><span class="sxs-lookup"><span data-stu-id="96d75-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="96d75-111">*Noliktavas dimensijas* tiek atbalstītas pat tad, ja nav iespējota funkcija *Iepakojuma preces dimensijas*.</span><span class="sxs-lookup"><span data-stu-id="96d75-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="96d75-112">Jūs tos iestatāt, izmantojot **Fizisko dimensiju** lapu programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="96d75-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="96d75-113">Šīs dimensijas tiek izmantotas visos procesos, kuros nav norādītas iepakošanas un ligzdotās iepakojuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="96d75-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="96d75-114">*Iepakošanas* un *ligzdotā iepakojuma* dimensijas tiek iestatītas, izmantojot lapu **Fizisko preču dimensijas**, kas tiek pievienotas, iespējojot iespēju *Iepakojuma preces dimensijas*.</span><span class="sxs-lookup"><span data-stu-id="96d75-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="96d75-115">Šajā tēmā sniegts scenārijs, kas parāda, kā izmantot šo funkciju.</span><span class="sxs-lookup"><span data-stu-id="96d75-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="96d75-116">Ieslēgt iepakojuma preču dimensiju līdzekli</span><span class="sxs-lookup"><span data-stu-id="96d75-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="96d75-117">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="96d75-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="96d75-118">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="96d75-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="96d75-119">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="96d75-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="96d75-120">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="96d75-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="96d75-121">**Līdzekļa nosaukums:** *Produkta iepakojuma dimensijas*</span><span class="sxs-lookup"><span data-stu-id="96d75-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="96d75-122">Piemērs</span><span class="sxs-lookup"><span data-stu-id="96d75-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="96d75-123">Scenārija iestatīšana</span><span class="sxs-lookup"><span data-stu-id="96d75-123">Set up the scenario</span></span>

<span data-ttu-id="96d75-124">Pirms jūs varat palaist piemēra scenāriju, jums ir jāsagatavo sistēma, kā aprakstīts šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="96d75-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="96d75-125">Iespējot paraugdatus</span><span class="sxs-lookup"><span data-stu-id="96d75-125">Enable demo data</span></span>

<span data-ttu-id="96d75-126">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [paraugdati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="96d75-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="96d75-127">Turklāt pirms sākšanas ir jāatlasa *USMF* juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="96d75-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="96d75-128">Pievienot precei jaunu fizisko dimensiju</span><span class="sxs-lookup"><span data-stu-id="96d75-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="96d75-129">Pievienojiet precei jaunu fizisko dimensiju, rīkojoties šādi:</span><span class="sxs-lookup"><span data-stu-id="96d75-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="96d75-130">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="96d75-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="96d75-131">Atlasiet preci ar **Krājuma numuru** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="96d75-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="96d75-132">Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Preces fiziskās dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="96d75-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="96d75-133">Atveras lapa **Preces fiziskās dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="96d75-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="96d75-134">Darbību rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un pēc tam atlasiet šos iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="96d75-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="96d75-135">**Fiziskās dimensijas tips** - *Iepakojums*</span><span class="sxs-lookup"><span data-stu-id="96d75-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="96d75-136">**Fiziska vienība** - *gab*</span><span class="sxs-lookup"><span data-stu-id="96d75-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="96d75-137">**Svars** - *4*</span><span class="sxs-lookup"><span data-stu-id="96d75-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="96d75-138">**Svara mērvienība** - *kg*</span><span class="sxs-lookup"><span data-stu-id="96d75-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="96d75-139">**Dziļums** - *3*</span><span class="sxs-lookup"><span data-stu-id="96d75-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="96d75-140">**Augstums** - *4*</span><span class="sxs-lookup"><span data-stu-id="96d75-140">**Height** - *4*</span></span>
    - <span data-ttu-id="96d75-141">**Platums** - *3*</span><span class="sxs-lookup"><span data-stu-id="96d75-141">**Width** - *3*</span></span>
    - <span data-ttu-id="96d75-142">**Garums** - *cm*</span><span class="sxs-lookup"><span data-stu-id="96d75-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="96d75-143">**Tilpuma mērvienība** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="96d75-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="96d75-144">Lauks **Tilpums** tiek aprēķināts automātiski, pamatojoties uz **Dziļuma**, **Augstuma** un **Platuma** iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="96d75-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="96d75-145">Izveidot jaunu konteinera tipu</span><span class="sxs-lookup"><span data-stu-id="96d75-145">Create a new container type</span></span>

<span data-ttu-id="96d75-146">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Konteineri \> Konteinera tipi** un izveidojiet jaunu ierakstu ar šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="96d75-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="96d75-147">**Konteinera tipa kods** - *maza kaste*</span><span class="sxs-lookup"><span data-stu-id="96d75-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="96d75-148">**Apraksts** - *maza kaste*</span><span class="sxs-lookup"><span data-stu-id="96d75-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="96d75-149">**Maksimālais neto svars** - *50*</span><span class="sxs-lookup"><span data-stu-id="96d75-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="96d75-150">**Tilpums** - *144*</span><span class="sxs-lookup"><span data-stu-id="96d75-150">**Volume** - *144*</span></span>
- <span data-ttu-id="96d75-151">**Garums** - *6*</span><span class="sxs-lookup"><span data-stu-id="96d75-151">**Length** - *6*</span></span>
- <span data-ttu-id="96d75-152">**Platums** - *6*</span><span class="sxs-lookup"><span data-stu-id="96d75-152">**Width** - *6*</span></span>
- <span data-ttu-id="96d75-153">**Augstums** - *4*</span><span class="sxs-lookup"><span data-stu-id="96d75-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="96d75-154">Konteineru grupas izveide</span><span class="sxs-lookup"><span data-stu-id="96d75-154">Create a container group</span></span>

<span data-ttu-id="96d75-155">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Konteineri \> Konteinera tipi** un izveidojiet jaunu ierakstu ar šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="96d75-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="96d75-156">**Konteineru grupas ID** - *maza kaste*</span><span class="sxs-lookup"><span data-stu-id="96d75-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="96d75-157">**Apraksts** - *maza kaste*</span><span class="sxs-lookup"><span data-stu-id="96d75-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="96d75-158">Pievienojiet jauu rindu sadaļā **Detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="96d75-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="96d75-159">Iestatiet **Konteinera veidu** uz *maza kaste*.</span><span class="sxs-lookup"><span data-stu-id="96d75-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="96d75-160">Konteinera būvējuma veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="96d75-160">Set up a container build template</span></span>

<span data-ttu-id="96d75-161">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Konteineris \> Konteinera būvējuma veidnes** un atlasiet **Kastes**.</span><span class="sxs-lookup"><span data-stu-id="96d75-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="96d75-162">Mainīt **Konteineru grupas ID** uz *maza kaste*.</span><span class="sxs-lookup"><span data-stu-id="96d75-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="96d75-163">Palaist scenāriju</span><span class="sxs-lookup"><span data-stu-id="96d75-163">Run the scenario</span></span>

<span data-ttu-id="96d75-164">Kad esat sagatavojis sistēmu tā, kā aprakstīts iepriekšējā sadaļā, esat gatavs palaist scenāriju tā, kā aprakstīts nākamajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="96d75-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="96d75-165">Izveidot pārdošanas pasūtījumu un izveidot kravu</span><span class="sxs-lookup"><span data-stu-id="96d75-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="96d75-166">Šajā procesā tiks izveidots sūtījums, balstoties uz krājuma *iepakojuma* dimensijām, kurām augstums ir mazāks par 3.</span><span class="sxs-lookup"><span data-stu-id="96d75-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="96d75-167">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="96d75-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="96d75-168">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="96d75-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="96d75-169">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="96d75-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="96d75-170">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="96d75-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="96d75-171">**Noliktava:** *63*</span><span class="sxs-lookup"><span data-stu-id="96d75-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="96d75-172">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="96d75-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="96d75-173">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="96d75-173">The new sales order is opened.</span></span> <span data-ttu-id="96d75-174">Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="96d75-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="96d75-175">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="96d75-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="96d75-176">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="96d75-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="96d75-177">**Daudzums:** *5*</span><span class="sxs-lookup"><span data-stu-id="96d75-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="96d75-178">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="96d75-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="96d75-179">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="96d75-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="96d75-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="96d75-180">Close the page.</span></span>
1. <span data-ttu-id="96d75-181">Darbību rūts cilnē **Noliktava** atlasiet **Pārvietot uz noliktavu**, lai noliktavai izveidotu darbu.</span><span class="sxs-lookup"><span data-stu-id="96d75-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="96d75-182">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava \> Detalizēta informācija par sūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="96d75-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="96d75-183">Darbības rūtī atveriet cilni **Transports** un atlasiet **Skatīt konteinerus**.</span><span class="sxs-lookup"><span data-stu-id="96d75-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="96d75-184">Apstipriniet, ka krājums ir salikts divos *mazo kastu* konteineros.</span><span class="sxs-lookup"><span data-stu-id="96d75-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="96d75-185">Preces novietošana noliktavā</span><span class="sxs-lookup"><span data-stu-id="96d75-185">Place an item into storage</span></span>

1. <span data-ttu-id="96d75-186">Atveriet mobilo ierīci, piesakieties noliktavā 63 un dodieties uz sadaļu **Krājums \> Pielāgošana**.</span><span class="sxs-lookup"><span data-stu-id="96d75-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="96d75-187">Ievadiet **Loc** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="96d75-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="96d75-188">Izveidojiet jaunu numura zīmi ar **Krājumu** = *A0001* un **Daudzumu** = *1 gab.*.</span><span class="sxs-lookup"><span data-stu-id="96d75-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="96d75-189">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96d75-189">Select **OK**.</span></span> <span data-ttu-id="96d75-190">Tiks saņemts kļūdas ziņojums "Atrašanās vieta SHORT-01 neizdevās, jo krājums A0001 neatbilst novietojumā norādītajām dimensijām."</span><span class="sxs-lookup"><span data-stu-id="96d75-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="96d75-191">Tas tādēļ, ka preces *Noliktavas* tipa dimensijas ir lielākas par noliktavas profilā norādītajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="96d75-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>
