---
title: Līdzekļa MK
description: Šajā tēmā ir aprakstīti līdzekļu materiālu komplekti (MK) Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f42646ae865cd530203c997fd10c8ccd59e7fa2b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890061"
---
# <a name="asset-boms"></a><span data-ttu-id="4678d-103">Līdzekļa MK</span><span class="sxs-lookup"><span data-stu-id="4678d-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4678d-104">Šajā tēmā ir aprakstīti līdzekļu materiālu komplekti (MK) Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="4678d-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="4678d-105">Lapā **Līdzekļa MK** tiek parādīts visu to preču (rezerves daļu un citu vienību) saraksts, kuras tiek izmantotas līdzeklism visā tā dzīves cikla laikā.</span><span class="sxs-lookup"><span data-stu-id="4678d-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="4678d-106">Kad veidojat jaunu līdzekli, apsveriet iespēju iestatīt līdzekļa MK kā iestatīšanas procedūras daļu.</span><span class="sxs-lookup"><span data-stu-id="4678d-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="4678d-107">Šādi var izsekot līdzekļa vienību vēsturi no izveides datuma.</span><span class="sxs-lookup"><span data-stu-id="4678d-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="4678d-108">Kad esat pabeidzis uzturēšanas darbu un krājuma patēriņš ir reģistrēts darba pasūtījumā, varat izsekot to rezerves daļu un citu vienību patēriņu, kas ir izmantotas līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="4678d-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="4678d-109">Šī funkcionalitāte ļauj saglabāt pilnīgu vienību patēriņa ierakstu par visiem jūsu līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="4678d-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="4678d-110">Piemēram, var izmantot ierakstu, lai pārraudzītu, vai konkrēta rezerves daļa bieži tiek aizstāta, vai lai reģistrētu rezerves daļas vai citas vienības, kas pašlaik tiek izmantotas līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="4678d-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="4678d-111">Darba pasūtījumā krājuma patēriņš var ietvert gan rezerves daļas, gan citas papildu vienības, piemēram, smērvielas, bultskrūves un starplikas.</span><span class="sxs-lookup"><span data-stu-id="4678d-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="4678d-112">Līdzekļa MK var automātiski atjaunināt, pamatojoties uz iestatījumu Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="4678d-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="4678d-113">Ja darba pasūtījuma dzīves cikla stāvoklis ir izveidots, lai apstrādātu pabeigtos vai izpildītos darba pasūtījumus, un ja opcija **Atjaunināt līdzekļa MK** šim darba pasūtījuma dzīves cikla stāvoklim ir iestatīta uz **Jā** lapā **Darba pasūtījuma dzīves cikla stāvokļi**, visas vienības, kas izmantotas darba pasūtījumam, tiek automātiski atjauninātas lapā **Līdzekļa MK**, kad darba pasūtījums tiek atjaunināts uz šo dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="4678d-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="4678d-114">Varat arī manuāli atjaunināt līdzekļa MK, izveidojot jaunas vienību rindas lapā **Līdzekļa MK**.</span><span class="sxs-lookup"><span data-stu-id="4678d-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="4678d-115">Lapā **Līdzekļa MK** varat izsekot rezerves daļu vēsturi līdzekļiem pēc tam, kad vienību patēriņš ir reģistrēts darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="4678d-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="4678d-116">Lai izmantotu šo funkcionalitāti, ir jāatlasa vienību grupas, kas jāizmanto rezerves daļu reģistrēšanai lapā **Rezerves daļu vienību grupas**.</span><span class="sxs-lookup"><span data-stu-id="4678d-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="4678d-117">Lai izmantotu līdzekļa MK funkcionalitāti, vispirms ir jāiestata nepieciešamās rezerves daļu vienību grupas.</span><span class="sxs-lookup"><span data-stu-id="4678d-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="4678d-118">Pēc tam, ja vēlaties, lai līdzekļa MK tiktu automātiski atjaunināts, kad darba pasūtījums ir pabeigts, varat iestatīt darba pasūtījuma dzīves cikla stāvokli, lai apstrādātu šo atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="4678d-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="4678d-119">Rezerves daļu vienību grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4678d-119">Set up spare parts item groups</span></span>

<span data-ttu-id="4678d-120">Rezerves daļu vēstures iestatīšana ir balstīta uz vienību grupām, kas izveidotas modulī **Krājumu un noliktavas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="4678d-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="4678d-121">Līdzekļu pārvaldībā iestatiet vienību grupas, lai varētu izsekot rezerves daļu vēsturi vienībām atlasītajās krājumu grupās.</span><span class="sxs-lookup"><span data-stu-id="4678d-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="4678d-122">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzeklis** \> **Rezerves daļu vienību grupas**.</span><span class="sxs-lookup"><span data-stu-id="4678d-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="4678d-123">Atlasiet **Jauns**, lai iestatītu vienību grupu.</span><span class="sxs-lookup"><span data-stu-id="4678d-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="4678d-124">Atlasiet grupu laukā **Vienības grupa**.</span><span class="sxs-lookup"><span data-stu-id="4678d-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="4678d-125">Grupas nosaukums tiek automātiski ierakstīts laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="4678d-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="4678d-126">Llīdzekļa MK skatīšana un atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="4678d-126">View and update asset BOMs</span></span>

<span data-ttu-id="4678d-127">Pēc vienību patēriņa iegrāmatošanas darba pasūtījumā varat skatīt reģistrēto vienību patēriņu lapā **Līdzekļa MK**.</span><span class="sxs-lookup"><span data-stu-id="4678d-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="4678d-128">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Aktīvie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="4678d-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="4678d-129">Atlasiet sarakstā līdzekli un pēc tam atlasiet **Llīdzekļa MK**.</span><span class="sxs-lookup"><span data-stu-id="4678d-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4678d-130">Lai skatītu visu vienību patēriņa reģistrācijas par visiem līdzekļiem, atlasiet **Līdzekļu pārvaldība** \> **Uzziņas** \> **Līdzekļi** \> **Līdzekļa MK**.</span><span class="sxs-lookup"><span data-stu-id="4678d-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="4678d-131">Atlasiet **Atjaunināt līdzekļa MK**.</span><span class="sxs-lookup"><span data-stu-id="4678d-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="4678d-132">Varat pēc vajadzības pievienot līdzekļus, līdzekļu veidus un resursus ajauninājumam, atlasot **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="4678d-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="4678d-133">Atlasiet **Labi**, lai sāktu atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="4678d-133">Select **OK** to start the update.</span></span> <span data-ttu-id="4678d-134">Varat arī iestatīt atjaunināšanas funkciju kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="4678d-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="4678d-135">Ja vēlaties redzēt papildu informāciju, kas saistīta ar vienībām, varat pievienot krājumu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4678d-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="4678d-136">Atlasiet **Krājumi** \> **Dimensiju parādīšana** un pēc tam atlasiet izvēles rūtiņas dimensijām, kuras vēlaties skatīt.</span><span class="sxs-lookup"><span data-stu-id="4678d-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="4678d-137">Lai paturētu šo iestatījumu visiem līdzekļiem lapā **Līdzekļa MK**, iestatiet opciju **Saglabāt iestatījumu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4678d-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="4678d-138">Lai iegūtu pārskatu par to, kur Līdzekļu pārvaldībā tiek izmantots atlasītās rindas vienība saistībā ar līdzekļiem, darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem, atlasiet **Vienība tika izmantota**.</span><span class="sxs-lookup"><span data-stu-id="4678d-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="4678d-139">Ja vēlaties redzēt tikai aktīvo vienību rindas, atlasiet **Skatīt** \> **Pašreizējais**.</span><span class="sxs-lookup"><span data-stu-id="4678d-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="4678d-140">Lai skatītu visas vienību rindas, ieskaitot rindas, kurās beigu datums ir agrāks par pašreizējo datumu, atlasiet **Skatīt** \> **Viss**.</span><span class="sxs-lookup"><span data-stu-id="4678d-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="4678d-141">Kad esat pabeidzis darba pasūtījumu, ja dažām vienībām vai rezerves daļām, kas saistītas ar saistīto līdzekli, ir beidzies derīguma termiņš vai arī tās ir aizstātas ar citām vienībām vai rezerves daļām, ieteicams attiecīgi atjaunināt līdzekļa MK.</span><span class="sxs-lookup"><span data-stu-id="4678d-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="4678d-142">Jaunas vienības rindas izveide līdzekļa MK</span><span class="sxs-lookup"><span data-stu-id="4678d-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="4678d-143">Varat manuāli izveidot vienību rindas līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="4678d-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="4678d-144">Lapā **Līdzekļa MK** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4678d-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="4678d-145">Laukā **Līdzeklis** atlasiet līdzekli, kuram pievienot vienības rindu.</span><span class="sxs-lookup"><span data-stu-id="4678d-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="4678d-146">Laukā **Rindas numurs** ievadiet secīgu rindas numuru.</span><span class="sxs-lookup"><span data-stu-id="4678d-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="4678d-147">Laukā **Ir spēkā** ievadiet sākuma datumu attiecīgajai vienībai.</span><span class="sxs-lookup"><span data-stu-id="4678d-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="4678d-148">Ja vienībai beigsies derīguma termiņš, laukā **Beigu datums** ievadiet beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="4678d-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="4678d-149">Laukā **Vienības numurs** atlasiet vienību.</span><span class="sxs-lookup"><span data-stu-id="4678d-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="4678d-150">Nosaukums tiek automātiski ievadīts laukā **Preces nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="4678d-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="4678d-151">Laukā **Daudzums** ievadiet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="4678d-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="4678d-152">Lauks **Mērvienība** tiek automātiski atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="4678d-152">The **Unit** field is automatically updated.</span></span>
