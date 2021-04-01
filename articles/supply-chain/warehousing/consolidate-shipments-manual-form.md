---
title: Manuāli konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas lapu
description: Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā un pēc tam vēlāk tiek konsolidēti, izmantojot lapu Konsolidēt sūtījumus.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 6d9186fe242fa56b6a360d6a4e4284c0c3eac141
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242209"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="3281b-103">Manuāli konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas lapu</span><span class="sxs-lookup"><span data-stu-id="3281b-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3281b-104">Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā un pēc tam vēlāk tiek konsolidēti, izmantojot lapu **Konsolidēt sūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="3281b-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="3281b-105">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="3281b-105">Make demo data available</span></span>

<span data-ttu-id="3281b-106">Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3281b-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3281b-107">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="3281b-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="3281b-108">Iestatīt sūtījumu konsolidācijas politikas un preču filtrus</span><span class="sxs-lookup"><span data-stu-id="3281b-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="3281b-109">Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="3281b-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="3281b-110">Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.</span><span class="sxs-lookup"><span data-stu-id="3281b-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="3281b-111">Izveidot pārdošanas pasūtījumus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="3281b-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="3281b-112">Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt.</span><span class="sxs-lookup"><span data-stu-id="3281b-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="3281b-113">Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem.</span><span class="sxs-lookup"><span data-stu-id="3281b-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="3281b-114">Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="3281b-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="3281b-115">Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="3281b-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="3281b-116">Pārdošanas pasūtījumu 1 un 2 izveide</span><span class="sxs-lookup"><span data-stu-id="3281b-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="3281b-117">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="3281b-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3281b-118">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="3281b-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="3281b-119">**Kopa:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="3281b-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="3281b-120">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="3281b-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3281b-121">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="3281b-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3281b-122">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3281b-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3281b-123">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="3281b-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="3281b-124">Pārdošanas pasūtījumu 3 un 4 izveide</span><span class="sxs-lookup"><span data-stu-id="3281b-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="3281b-125">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="3281b-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="3281b-126">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="3281b-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="3281b-127">**Kopa:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="3281b-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="3281b-128">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="3281b-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="3281b-129">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="3281b-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="3281b-130">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="3281b-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="3281b-131">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="3281b-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="3281b-132">Pasūtījumu izlaišana noliktavā</span><span class="sxs-lookup"><span data-stu-id="3281b-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="3281b-133">Sekojiet šiem soļiem, lai izlaistu pārdošanas pasūtījumu, ko izveidojāt šim scenārijam noliktavā.</span><span class="sxs-lookup"><span data-stu-id="3281b-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="3281b-134">Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3281b-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3281b-135">Atrodiet un atlasiet izlaižamo pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3281b-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="3281b-136">Darbību rūtī cilnē **Noliktava**, atlasiet **Darbības \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3281b-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="3281b-137">Atkārtojiet šo procedūru katram otrajam pārdošanas pasūtījumam, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="3281b-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="3281b-138">Konsolidēt sūtījumus</span><span class="sxs-lookup"><span data-stu-id="3281b-138">Consolidate shipments</span></span>

1. <span data-ttu-id="3281b-139">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3281b-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="3281b-140">Meklējiet un atlasiet sūtījumu, kas tika izveidots, kad pārdošanas pasūtījums 1 tika nodots noliktavā.</span><span class="sxs-lookup"><span data-stu-id="3281b-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="3281b-141">(Tā **Sūtījuma konsolidācijas politikas** laukam jābūt iestatītam uz *Pasūtījuma kopa* .)</span><span class="sxs-lookup"><span data-stu-id="3281b-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="3281b-142">Darbību rūts cilnē **Sūtījumi** atlasiet **Sūtījumi \> Konsolidēt sūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="3281b-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="3281b-143">Pārbaudiet konsolidācijai ieteiktos sūtījumus.</span><span class="sxs-lookup"><span data-stu-id="3281b-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="3281b-144">Konsolidācijai jāierosina tikai viens sūtījums, kam ir tāda pati politika.</span><span class="sxs-lookup"><span data-stu-id="3281b-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="3281b-145">Aizveriet lapu **Sūtījuma konsolidācija**.</span><span class="sxs-lookup"><span data-stu-id="3281b-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="3281b-146">Meklējiet un atlasiet sūtījumu, kas tika izveidots, kad pārdošanas pasūtījums 3 tika nodots noliktavā.</span><span class="sxs-lookup"><span data-stu-id="3281b-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="3281b-147">(Tā **Sūtījuma konsolidācijas politikas** laukam jābūt iestatītam uz *Noklusējums* .)</span><span class="sxs-lookup"><span data-stu-id="3281b-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="3281b-148">Darbību rūts cilnē **Sūtījumi** atlasiet **Sūtījumi \> Konsolidēt sūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="3281b-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="3281b-149">Pārbaudiet, lai neviens sūtījums netiek ieteikts konsolidācijai.</span><span class="sxs-lookup"><span data-stu-id="3281b-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="3281b-150">Atlasiet **Rādīt filtrus**.</span><span class="sxs-lookup"><span data-stu-id="3281b-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="3281b-151">Rūtī **Filtri** noņemiet **Pasūtījuma numura** filtru un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="3281b-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="3281b-152">Pārbaudiet konsolidācijai ieteiktos sūtījumus.</span><span class="sxs-lookup"><span data-stu-id="3281b-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="3281b-153">Konsolidācijai jāierosina tikai viens sūtījums, kam ir tāda pati politika.</span><span class="sxs-lookup"><span data-stu-id="3281b-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3281b-154">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3281b-154">Additional resources</span></span>

- [<span data-ttu-id="3281b-155">Sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="3281b-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="3281b-156">Sūtījumu konsolidācijas politiku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3281b-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]