---
title: Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku
description: Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā un pēc tam vēlāk tiek konsolidēti sūtījumos, izmantojot sūtījumu konsolidācijas darbgaldu.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9d0a2671e18603f701d343a4150128a04c626952
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963389"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="c53a5-103">Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku</span><span class="sxs-lookup"><span data-stu-id="c53a5-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c53a5-104">Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā un pēc tam vēlāk tiek konsolidēti sūtījumos, izmantojot sūtījumu konsolidācijas darbgaldu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="c53a5-105">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="c53a5-105">Make demo data available</span></span>

<span data-ttu-id="c53a5-106">Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c53a5-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c53a5-107">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="c53a5-108">Iestatīt sūtījumu konsolidācijas politikas un preču filtrus</span><span class="sxs-lookup"><span data-stu-id="c53a5-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="c53a5-109">Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="c53a5-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="c53a5-110">Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.</span><span class="sxs-lookup"><span data-stu-id="c53a5-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="c53a5-111">Ieslēgt manuālo sūtījumu konsolidācijas līdzekli</span><span class="sxs-lookup"><span data-stu-id="c53a5-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="c53a5-112">Lai varētu izmantot *Manuālo sūtījumu konsolidācijas līdzekli*, tas ir jāieslēdz sistēmā.</span><span class="sxs-lookup"><span data-stu-id="c53a5-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="c53a5-113">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c53a5-114">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c53a5-115">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="c53a5-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c53a5-116">**Līdzekļa nosaukums:** *Manuālā sūtījumu konsolidācija*</span><span class="sxs-lookup"><span data-stu-id="c53a5-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="c53a5-117">Kā tika minēts sadaļā [Konfigurēt sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md), pirms varat izveidot politikas, ir jāieslēdz arī *Konsolidācijas nosūtījuma* līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="c53a5-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="c53a5-118">Tomēr jums jau ir jābūt pabeigtam šim solim.</span><span class="sxs-lookup"><span data-stu-id="c53a5-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="c53a5-119">Izveidot pārdošanas pasūtījumus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="c53a5-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="c53a5-120">Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt.</span><span class="sxs-lookup"><span data-stu-id="c53a5-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="c53a5-121">Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem.</span><span class="sxs-lookup"><span data-stu-id="c53a5-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="c53a5-122">Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="c53a5-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="c53a5-123">Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="c53a5-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="c53a5-124">Izveidot 1. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c53a5-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="c53a5-125">Pārdošanas pasūtījumi 1-1 un 1-2</span><span class="sxs-lookup"><span data-stu-id="c53a5-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="c53a5-126">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-127">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c53a5-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c53a5-128">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c53a5-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c53a5-129">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-130">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-131">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-132">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="c53a5-133">Pārdošanas pasūtījums 1-3</span><span class="sxs-lookup"><span data-stu-id="c53a5-133">Sales order 1-3</span></span>

1. <span data-ttu-id="c53a5-134">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-135">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c53a5-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c53a5-136">**Piegādes veids:** *10*</span><span class="sxs-lookup"><span data-stu-id="c53a5-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="c53a5-137">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-138">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-139">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-140">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="c53a5-141">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-142">**Krājuma kods:** *A0002* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-143">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c53a5-144">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c53a5-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c53a5-145">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="c53a5-146">Izveidot 2. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c53a5-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="c53a5-147">Pārdošanas pasūtījumi 2-1 un 2-2</span><span class="sxs-lookup"><span data-stu-id="c53a5-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="c53a5-148">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-149">**Debitora konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="c53a5-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="c53a5-150">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c53a5-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c53a5-151">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-152">**Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)</span><span class="sxs-lookup"><span data-stu-id="c53a5-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="c53a5-153">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-154">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="c53a5-155">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-156">**Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)</span><span class="sxs-lookup"><span data-stu-id="c53a5-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="c53a5-157">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c53a5-158">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c53a5-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c53a5-159">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="c53a5-160">Izveidot 3. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c53a5-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="c53a5-161">Pārdošanas pasūtījumi 3-1 un 3-2</span><span class="sxs-lookup"><span data-stu-id="c53a5-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="c53a5-162">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-163">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c53a5-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c53a5-164">**Debitora pieprasījums:** *1*</span><span class="sxs-lookup"><span data-stu-id="c53a5-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="c53a5-165">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-166">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-167">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-168">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="c53a5-169">Pārdošanas pasūtījumi 3-3 un 3-4</span><span class="sxs-lookup"><span data-stu-id="c53a5-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="c53a5-170">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-171">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c53a5-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c53a5-172">**Debitora pieprasījums:** *2*</span><span class="sxs-lookup"><span data-stu-id="c53a5-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="c53a5-173">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-174">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-175">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-176">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="c53a5-177">Izveidot 4. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c53a5-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="c53a5-178">Pārdošanas pasūtījumi 4-1 un 4-2</span><span class="sxs-lookup"><span data-stu-id="c53a5-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="c53a5-179">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-180">**Debitora konts:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="c53a5-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="c53a5-181">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-182">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-183">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-184">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="c53a5-185">Pārdošanas pasūtījumi 4-3 un 4-4</span><span class="sxs-lookup"><span data-stu-id="c53a5-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="c53a5-186">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-187">**Debitora konts:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="c53a5-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="c53a5-188">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-189">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-190">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-191">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="c53a5-192">Pārdošanas pasūtījumi 4-5 un 4-6</span><span class="sxs-lookup"><span data-stu-id="c53a5-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="c53a5-193">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-194">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c53a5-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c53a5-195">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="c53a5-195">**Site:** *6*</span></span>
    - <span data-ttu-id="c53a5-196">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="c53a5-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c53a5-197">**Kopa:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="c53a5-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="c53a5-198">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-199">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-200">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-201">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="c53a5-202">Pārdošanas pasūtījumi 4-7 un 4-8</span><span class="sxs-lookup"><span data-stu-id="c53a5-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="c53a5-203">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c53a5-204">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c53a5-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c53a5-205">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="c53a5-205">**Site:** *6*</span></span>
    - <span data-ttu-id="c53a5-206">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="c53a5-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c53a5-207">**Kopa:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="c53a5-208">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c53a5-209">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c53a5-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c53a5-210">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c53a5-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c53a5-211">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="c53a5-212">Pasūtījumu izlaišana noliktavā</span><span class="sxs-lookup"><span data-stu-id="c53a5-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="c53a5-213">Sekojiet šiem soļiem, lai izlaistu pārdošanas pasūtījumu, ko izveidojāt šim scenārijam noliktavā.</span><span class="sxs-lookup"><span data-stu-id="c53a5-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="c53a5-214">Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c53a5-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c53a5-215">Atrodiet un atlasiet izlaižamo pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="c53a5-216">Darbību rūtī cilnē **Noliktava**, atlasiet **Darbības \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="c53a5-217">Atkārtojiet šo procedūru katram otrajam pārdošanas pasūtījumam, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="c53a5-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="c53a5-218">Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku</span><span class="sxs-lookup"><span data-stu-id="c53a5-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="c53a5-219">Dodieties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Sūtījumu konsolidācijas rīks**.</span><span class="sxs-lookup"><span data-stu-id="c53a5-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="c53a5-220">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="c53a5-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c53a5-221">Vaicājuma redaktora dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c53a5-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="c53a5-222">**Tabula:** *Pārdošanas pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="c53a5-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="c53a5-223">**Lauks:** *Pārdošanas pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="c53a5-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="c53a5-224">**Kritēriji:** ievadiet ar komatu atdalītu pārdošanas pasūtījumu numuru sarakstu katrai pasūtījumu kopai, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="c53a5-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="c53a5-225">Atlasiet **Labi**, lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="c53a5-226">Darbību rūtī atlasiet **Konsolidēt sūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="c53a5-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="c53a5-227">Atlasiet visus sūtījumus un pēc tam Darbību rūtī atlasiet **Konsolidēt**.</span><span class="sxs-lookup"><span data-stu-id="c53a5-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="c53a5-228">Pārbaudīt sūtījumus</span><span class="sxs-lookup"><span data-stu-id="c53a5-228">Verify the shipments</span></span>

<span data-ttu-id="c53a5-229">Šī procedūra ļauj pārbaudīt sūtījumus, kas ir izveidoti vai atjaunināti, veicot sūtījuma konsolidāciju.</span><span class="sxs-lookup"><span data-stu-id="c53a5-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="c53a5-230">Izmantojiet to, lai pārskatītu katru pasūtījuma kopu, ko izveidojāt šim scenārijam, un tad pārskatītu sekojošās apakšsadaļas, lai pārliecinātos, ka esat ieguvis plānotos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="c53a5-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="c53a5-231">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c53a5-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="c53a5-232">Atrast un atlasīt nepieciešamo sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c53a5-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="c53a5-233">Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.</span><span class="sxs-lookup"><span data-stu-id="c53a5-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="c53a5-234">1. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="c53a5-234">Related shipments for order set 1</span></span>

<span data-ttu-id="c53a5-235">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c53a5-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="c53a5-236">Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c53a5-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="c53a5-237">Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c53a5-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="c53a5-238">2. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="c53a5-238">Related shipments for order set 2</span></span>

<span data-ttu-id="c53a5-239">Ir jābūt izveidotiem trīs sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c53a5-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="c53a5-240">Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.</span><span class="sxs-lookup"><span data-stu-id="c53a5-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="c53a5-241">Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.</span><span class="sxs-lookup"><span data-stu-id="c53a5-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="c53a5-242">3. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="c53a5-242">Related shipments for order set 3</span></span>

<span data-ttu-id="c53a5-243">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c53a5-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="c53a5-244">Pirmajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*.</span><span class="sxs-lookup"><span data-stu-id="c53a5-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="c53a5-245">Otrajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *2*.</span><span class="sxs-lookup"><span data-stu-id="c53a5-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="c53a5-246">4. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="c53a5-246">Related shipments for order set 4</span></span>

<span data-ttu-id="c53a5-247">Ir jābūt izveidotiem četriem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c53a5-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="c53a5-248">Rindas no diviem pasūtījumiem debitoram *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c53a5-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c53a5-249">Rindas no diviem pasūtījumiem debitoram *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c53a5-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c53a5-250">Rindas no pārdošanas pasūtījumiem 4-5 un 4-6 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c53a5-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c53a5-251">Rindas no pārdošanas pasūtījumiem 4-7 un 4-8 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c53a5-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c53a5-252">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c53a5-252">Additional resources</span></span>

- [<span data-ttu-id="c53a5-253">Sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="c53a5-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="c53a5-254">Sūtījumu konsolidācijas politiku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c53a5-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
