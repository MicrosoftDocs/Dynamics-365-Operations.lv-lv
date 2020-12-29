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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2f1dd5c743664e638c043b600ae7b0f6bce5ddcd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432542"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="9044f-103">Konsolidēt sūtījumus, kravu plānošanas rīkā izmantojot pārvietošanu uz noliktavu</span><span class="sxs-lookup"><span data-stu-id="9044f-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9044f-104">Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā noslodzē un pēc tam tiek automātiski apvienoti sūtījumos.</span><span class="sxs-lookup"><span data-stu-id="9044f-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="9044f-105">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="9044f-105">Make demo data available</span></span>

<span data-ttu-id="9044f-106">Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9044f-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9044f-107">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="9044f-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="9044f-108">Iestatīt sūtījumu konsolidācijas politikas un preču filtrus</span><span class="sxs-lookup"><span data-stu-id="9044f-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="9044f-109">Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="9044f-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="9044f-110">Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.</span><span class="sxs-lookup"><span data-stu-id="9044f-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="9044f-111">Izveidot pārdošanas pasūtījumus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="9044f-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="9044f-112">Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt.</span><span class="sxs-lookup"><span data-stu-id="9044f-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="9044f-113">Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem.</span><span class="sxs-lookup"><span data-stu-id="9044f-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="9044f-114">Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="9044f-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="9044f-115">Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="9044f-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="9044f-116">Izveidot 1. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="9044f-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="9044f-117">Pārdošanas pasūtījums 1-1</span><span class="sxs-lookup"><span data-stu-id="9044f-117">Sales order 1-1</span></span>

1. <span data-ttu-id="9044f-118">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9044f-119">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9044f-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9044f-120">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9044f-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9044f-121">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-122">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-123">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-124">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="9044f-125">Pārdošanas pasūtījums 1-2</span><span class="sxs-lookup"><span data-stu-id="9044f-125">Sales order 1-2</span></span>

1. <span data-ttu-id="9044f-126">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9044f-127">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9044f-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9044f-128">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9044f-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9044f-129">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-130">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-131">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-132">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="9044f-133">Pārdošanas pasūtījums 1-3</span><span class="sxs-lookup"><span data-stu-id="9044f-133">Sales order 1-3</span></span>

1. <span data-ttu-id="9044f-134">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9044f-135">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9044f-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9044f-136">**Piegādes veids:** *10*</span><span class="sxs-lookup"><span data-stu-id="9044f-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="9044f-137">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-138">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-139">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-140">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9044f-141">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-142">**Krājuma kods:** *A0002* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-143">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9044f-144">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9044f-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9044f-145">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="9044f-146">Izveidot 2. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="9044f-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="9044f-147">Pārdošanas pasūtījumi 2-1 un 2-2</span><span class="sxs-lookup"><span data-stu-id="9044f-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="9044f-148">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9044f-149">**Debitora konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="9044f-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="9044f-150">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-151">**Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)</span><span class="sxs-lookup"><span data-stu-id="9044f-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="9044f-152">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-153">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9044f-154">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-155">**Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)</span><span class="sxs-lookup"><span data-stu-id="9044f-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="9044f-156">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9044f-157">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9044f-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9044f-158">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="9044f-159">Izveidot 3. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="9044f-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="9044f-160">Pārdošanas pasūtījumi 3-1 un 3-2</span><span class="sxs-lookup"><span data-stu-id="9044f-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="9044f-161">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9044f-162">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9044f-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9044f-163">**Debitora pieprasījums:** *1*</span><span class="sxs-lookup"><span data-stu-id="9044f-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="9044f-164">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-165">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-166">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-167">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="9044f-168">Pārdošanas pasūtījumi 3-3 un 3-4</span><span class="sxs-lookup"><span data-stu-id="9044f-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="9044f-169">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9044f-170">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9044f-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9044f-171">**Debitora pieprasījums:** *2*</span><span class="sxs-lookup"><span data-stu-id="9044f-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="9044f-172">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-173">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-174">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-175">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="9044f-176">Izveidot 4. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="9044f-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="9044f-177">Pārdošanas pasūtījumi 4-1 un 4-2</span><span class="sxs-lookup"><span data-stu-id="9044f-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="9044f-178">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9044f-179">**Debitora konts:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="9044f-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="9044f-180">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-181">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-182">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-183">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="9044f-184">Pārdošanas pasūtījumi 4-3 un 4-4</span><span class="sxs-lookup"><span data-stu-id="9044f-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="9044f-185">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9044f-186">**Debitora konts:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="9044f-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="9044f-187">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-188">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-189">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-190">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="9044f-191">Pārdošanas pasūtījumi 4-5 un 4-6</span><span class="sxs-lookup"><span data-stu-id="9044f-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="9044f-192">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9044f-193">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9044f-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9044f-194">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="9044f-194">**Site:** *6*</span></span>
    - <span data-ttu-id="9044f-195">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="9044f-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9044f-196">**Kopa:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="9044f-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="9044f-197">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-198">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-199">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-200">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="9044f-201">Pārdošanas pasūtījumi 4-7 un 4-8</span><span class="sxs-lookup"><span data-stu-id="9044f-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="9044f-202">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9044f-203">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9044f-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9044f-204">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="9044f-204">**Site:** *6*</span></span>
    - <span data-ttu-id="9044f-205">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="9044f-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9044f-206">**Kopa:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="9044f-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="9044f-207">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="9044f-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9044f-208">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="9044f-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9044f-209">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9044f-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9044f-210">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9044f-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="9044f-211">Izmantojiet noslodzes plānošanas darbvietu, lai izveidotu noslodzes un nodotu tās noliktavā</span><span class="sxs-lookup"><span data-stu-id="9044f-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="9044f-212">Sekojiet šiem soļiem, lai izveidotu noslodzi katrai pasūtījuma kopai, ko izveidojāt šim scenārijam, un tad to nodotu noliktavai.</span><span class="sxs-lookup"><span data-stu-id="9044f-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="9044f-213">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="9044f-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="9044f-214">Cilnē **Pārdošanas rindas** meklējiet un atlasiet visas pārdošanas pasūtījuma rindas vienā no šim scenārijam izveidotajām pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="9044f-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="9044f-215">Darbības rūtī cilnē **Piedāvājums un pieprasījums** atlasiet **Pievienot \> Jaunajai noslodzei**, lai pievienotu atlasītās pasūtījuma rindas jaunai noslodzei.</span><span class="sxs-lookup"><span data-stu-id="9044f-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="9044f-216">Dialoglodziņā **Noslodzes veidnes piešķire** laukā **Noslodzes veidnes ID** atlasiet noslodzes veidni, piemēram, *Stnd noslodzes veidne*.</span><span class="sxs-lookup"><span data-stu-id="9044f-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="9044f-217">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9044f-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="9044f-218">Sadaļā **Noslodzes** meklējiet un atlasiet tikko izveidoto noslodzi.</span><span class="sxs-lookup"><span data-stu-id="9044f-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="9044f-219">Atlasiet opciju **Pārvietot \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto noslodzi uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="9044f-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="9044f-220">Atkārtojiet šo procedūru pārējām trim pasūtījumu kopām, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="9044f-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="9044f-221">Pārbaudīt sūtījumus</span><span class="sxs-lookup"><span data-stu-id="9044f-221">Verify the shipments</span></span>

<span data-ttu-id="9044f-222">Šī procedūra ļauj pārbaudīt sūtījumus, kas ir izveidoti vai atjaunināti, veicot sūtījuma konsolidāciju.</span><span class="sxs-lookup"><span data-stu-id="9044f-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="9044f-223">Izmantojiet to, lai pārskatītu katru pasūtījuma kopu, ko izveidojāt šim scenārijam, un tad pārskatītu sekojošās apakšsadaļas, lai pārliecinātos, ka esat ieguvis plānotos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="9044f-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="9044f-224">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="9044f-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="9044f-225">Atrast un atlasīt nepieciešamo sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="9044f-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="9044f-226">Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.</span><span class="sxs-lookup"><span data-stu-id="9044f-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="9044f-227">Nodot 1. pasūtījuma kopu vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="9044f-227">Release order set 1 in one load</span></span>

<span data-ttu-id="9044f-228">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="9044f-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="9044f-229">Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="9044f-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="9044f-230">Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="9044f-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="9044f-231">Nodot 2. pasūtījuma kopu vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="9044f-231">Release order set 2 in one load</span></span>

<span data-ttu-id="9044f-232">Ir jābūt izveidotiem trīs sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="9044f-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="9044f-233">Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.</span><span class="sxs-lookup"><span data-stu-id="9044f-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="9044f-234">Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.</span><span class="sxs-lookup"><span data-stu-id="9044f-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="9044f-235">Nodot pasūtījuma kopu 3 vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="9044f-235">Release order set 3 in one load</span></span>

<span data-ttu-id="9044f-236">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="9044f-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="9044f-237">Pirmajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*.</span><span class="sxs-lookup"><span data-stu-id="9044f-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="9044f-238">Otrajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *2*.</span><span class="sxs-lookup"><span data-stu-id="9044f-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="9044f-239">Nodot 4. pasūtījuma kopu vienā noslodzē</span><span class="sxs-lookup"><span data-stu-id="9044f-239">Release order set 4 in one load</span></span>

<span data-ttu-id="9044f-240">Ir jābūt izveidotiem četriem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="9044f-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="9044f-241">Rindas no diviem pasūtījumiem debitoru kontam *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="9044f-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9044f-242">Rindas no diviem pasūtījumiem debitoru kontam *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="9044f-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9044f-243">Rindas no pārdošanas pasūtījumiem 4-5 un 4-6 debitoru kontam *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="9044f-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9044f-244">Rindas no pārdošanas pasūtījumiem 4-7 un 4-8 debitoru kontam *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="9044f-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9044f-245">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9044f-245">Additional resources</span></span>

- [<span data-ttu-id="9044f-246">Sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="9044f-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="9044f-247">Sūtījumu konsolidācijas politiku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9044f-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
