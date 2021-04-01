---
title: Konsolidēt sūtījumus, kravu plānošanas rīkā izmantojot pārvietošanu uz noliktavu
description: Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā noslodzē un pēc tam tiek automātiski apvienoti sūtījumos.
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
ms.openlocfilehash: 2fd13c2ceb8843b79b9dbc87acf77f219f0244f5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242257"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="c719b-103">Konsolidēt sūtījumus, kravu plānošanas rīkā izmantojot pārvietošanu uz noliktavu</span><span class="sxs-lookup"><span data-stu-id="c719b-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c719b-104">Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā noslodzē un pēc tam tiek automātiski apvienoti sūtījumos.</span><span class="sxs-lookup"><span data-stu-id="c719b-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="c719b-105">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="c719b-105">Make demo data available</span></span>

<span data-ttu-id="c719b-106">Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c719b-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c719b-107">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="c719b-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="c719b-108">Iestatīt sūtījumu konsolidācijas politikas un preču filtrus</span><span class="sxs-lookup"><span data-stu-id="c719b-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="c719b-109">Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="c719b-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="c719b-110">Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.</span><span class="sxs-lookup"><span data-stu-id="c719b-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="c719b-111">Izveidot pārdošanas pasūtījumus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="c719b-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="c719b-112">Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt.</span><span class="sxs-lookup"><span data-stu-id="c719b-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="c719b-113">Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem.</span><span class="sxs-lookup"><span data-stu-id="c719b-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="c719b-114">Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="c719b-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="c719b-115">Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="c719b-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="c719b-116">Izveidot 1. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c719b-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="c719b-117">Pārdošanas pasūtījums 1-1</span><span class="sxs-lookup"><span data-stu-id="c719b-117">Sales order 1-1</span></span>

1. <span data-ttu-id="c719b-118">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c719b-119">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c719b-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c719b-120">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c719b-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c719b-121">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-122">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-123">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-124">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="c719b-125">Pārdošanas pasūtījums 1-2</span><span class="sxs-lookup"><span data-stu-id="c719b-125">Sales order 1-2</span></span>

1. <span data-ttu-id="c719b-126">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c719b-127">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c719b-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c719b-128">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c719b-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c719b-129">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-130">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-131">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-132">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="c719b-133">Pārdošanas pasūtījums 1-3</span><span class="sxs-lookup"><span data-stu-id="c719b-133">Sales order 1-3</span></span>

1. <span data-ttu-id="c719b-134">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c719b-135">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c719b-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c719b-136">**Piegādes veids:** *10*</span><span class="sxs-lookup"><span data-stu-id="c719b-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="c719b-137">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-138">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-139">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-140">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="c719b-141">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-142">**Krājuma kods:** *A0002* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-143">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c719b-144">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c719b-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c719b-145">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="c719b-146">Izveidot 2. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c719b-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="c719b-147">Pārdošanas pasūtījumi 2-1 un 2-2</span><span class="sxs-lookup"><span data-stu-id="c719b-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="c719b-148">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c719b-149">**Debitora konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="c719b-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="c719b-150">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-151">**Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)</span><span class="sxs-lookup"><span data-stu-id="c719b-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="c719b-152">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-153">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="c719b-154">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-155">**Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)</span><span class="sxs-lookup"><span data-stu-id="c719b-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="c719b-156">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c719b-157">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c719b-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c719b-158">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="c719b-159">Izveidot 3. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c719b-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="c719b-160">Pārdošanas pasūtījumi 3-1 un 3-2</span><span class="sxs-lookup"><span data-stu-id="c719b-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="c719b-161">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c719b-162">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c719b-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c719b-163">**Debitora pieprasījums:** *1*</span><span class="sxs-lookup"><span data-stu-id="c719b-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="c719b-164">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-165">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-166">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-167">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="c719b-168">Pārdošanas pasūtījumi 3-3 un 3-4</span><span class="sxs-lookup"><span data-stu-id="c719b-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="c719b-169">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c719b-170">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c719b-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c719b-171">**Debitora pieprasījums:** *2*</span><span class="sxs-lookup"><span data-stu-id="c719b-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="c719b-172">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-173">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-174">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-175">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="c719b-176">Izveidot 4. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="c719b-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="c719b-177">Pārdošanas pasūtījumi 4-1 un 4-2</span><span class="sxs-lookup"><span data-stu-id="c719b-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="c719b-178">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c719b-179">**Debitora konts:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="c719b-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="c719b-180">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-181">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-182">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-183">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="c719b-184">Pārdošanas pasūtījumi 4-3 un 4-4</span><span class="sxs-lookup"><span data-stu-id="c719b-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="c719b-185">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c719b-186">**Debitora konts:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="c719b-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="c719b-187">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-188">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-189">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-190">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="c719b-191">Pārdošanas pasūtījumi 4-5 un 4-6</span><span class="sxs-lookup"><span data-stu-id="c719b-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="c719b-192">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c719b-193">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c719b-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c719b-194">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="c719b-194">**Site:** *6*</span></span>
    - <span data-ttu-id="c719b-195">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="c719b-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c719b-196">**Kopa:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="c719b-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="c719b-197">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-198">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-199">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-200">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="c719b-201">Pārdošanas pasūtījumi 4-7 un 4-8</span><span class="sxs-lookup"><span data-stu-id="c719b-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="c719b-202">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c719b-203">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c719b-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c719b-204">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="c719b-204">**Site:** *6*</span></span>
    - <span data-ttu-id="c719b-205">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="c719b-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c719b-206">**Kopa:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="c719b-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="c719b-207">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="c719b-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c719b-208">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="c719b-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c719b-209">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c719b-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c719b-210">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="c719b-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="c719b-211">Izmantojiet noslodzes plānošanas darbvietu, lai izveidotu noslodzes un nodotu tās noliktavā</span><span class="sxs-lookup"><span data-stu-id="c719b-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="c719b-212">Sekojiet šiem soļiem, lai izveidotu noslodzi katrai pasūtījuma kopai, ko izveidojāt šim scenārijam, un tad to nodotu noliktavai.</span><span class="sxs-lookup"><span data-stu-id="c719b-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="c719b-213">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="c719b-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="c719b-214">Cilnē **Pārdošanas rindas** meklējiet un atlasiet visas pārdošanas pasūtījuma rindas vienā no šim scenārijam izveidotajām pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="c719b-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="c719b-215">Darbības rūtī cilnē **Piedāvājums un pieprasījums** atlasiet **Pievienot \> Jaunajai noslodzei**, lai pievienotu atlasītās pasūtījuma rindas jaunai noslodzei.</span><span class="sxs-lookup"><span data-stu-id="c719b-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="c719b-216">Dialoglodziņā **Noslodzes veidnes piešķire** laukā **Noslodzes veidnes ID** atlasiet noslodzes veidni, piemēram, *Stnd noslodzes veidne*.</span><span class="sxs-lookup"><span data-stu-id="c719b-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="c719b-217">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c719b-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="c719b-218">Sadaļā **Noslodzes** meklējiet un atlasiet tikko izveidoto noslodzi.</span><span class="sxs-lookup"><span data-stu-id="c719b-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="c719b-219">Atlasiet opciju **Pārvietot \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto noslodzi uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="c719b-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="c719b-220">Atkārtojiet šo procedūru pārējām trim pasūtījumu kopām, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="c719b-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="c719b-221">Pārbaudīt sūtījumus</span><span class="sxs-lookup"><span data-stu-id="c719b-221">Verify the shipments</span></span>

<span data-ttu-id="c719b-222">Šī procedūra ļauj pārbaudīt sūtījumus, kas ir izveidoti vai atjaunināti, veicot sūtījuma konsolidāciju.</span><span class="sxs-lookup"><span data-stu-id="c719b-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="c719b-223">Izmantojiet to, lai pārskatītu katru pasūtījuma kopu, ko izveidojāt šim scenārijam, un tad pārskatītu sekojošās apakšsadaļas, lai pārliecinātos, ka esat ieguvis plānotos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="c719b-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="c719b-224">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c719b-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="c719b-225">Atrast un atlasīt nepieciešamo sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c719b-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="c719b-226">Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.</span><span class="sxs-lookup"><span data-stu-id="c719b-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="c719b-227">Nodot 1. pasūtījuma kopu vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="c719b-227">Release order set 1 in one load</span></span>

<span data-ttu-id="c719b-228">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c719b-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="c719b-229">Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c719b-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="c719b-230">Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c719b-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="c719b-231">Nodot 2. pasūtījuma kopu vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="c719b-231">Release order set 2 in one load</span></span>

<span data-ttu-id="c719b-232">Ir jābūt izveidotiem trīs sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c719b-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="c719b-233">Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.</span><span class="sxs-lookup"><span data-stu-id="c719b-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="c719b-234">Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.</span><span class="sxs-lookup"><span data-stu-id="c719b-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="c719b-235">Nodot pasūtījuma kopu 3 vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="c719b-235">Release order set 3 in one load</span></span>

<span data-ttu-id="c719b-236">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c719b-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="c719b-237">Pirmajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*.</span><span class="sxs-lookup"><span data-stu-id="c719b-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="c719b-238">Otrajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *2*.</span><span class="sxs-lookup"><span data-stu-id="c719b-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="c719b-239">Nodot 4. pasūtījuma kopu vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="c719b-239">Release order set 4 in one load</span></span>

<span data-ttu-id="c719b-240">Ir jābūt izveidotiem četriem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="c719b-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="c719b-241">Rindas no diviem pasūtījumiem debitoru kontam *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c719b-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c719b-242">Rindas no diviem pasūtījumiem debitoru kontam *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c719b-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c719b-243">Rindas no pārdošanas pasūtījumiem 4-5 un 4-6 debitoru kontam *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c719b-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c719b-244">Rindas no pārdošanas pasūtījumiem 4-7 un 4-8 debitoru kontam *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="c719b-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c719b-245">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c719b-245">Additional resources</span></span>

- [<span data-ttu-id="c719b-246">Sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="c719b-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="c719b-247">Sūtījumu konsolidācijas politiku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c719b-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]