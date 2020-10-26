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
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 8320c8aab82a39a8a5565e6b3e805e1065c67453
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986820"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="d4a51-103">Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku</span><span class="sxs-lookup"><span data-stu-id="d4a51-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4a51-104">Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā un pēc tam vēlāk tiek konsolidēti sūtījumos, izmantojot sūtījumu konsolidācijas darbgaldu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="d4a51-105">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="d4a51-105">Make demo data available</span></span>

<span data-ttu-id="d4a51-106">Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d4a51-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d4a51-107">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="d4a51-108">Iestatīt sūtījumu konsolidācijas politikas un preču filtrus</span><span class="sxs-lookup"><span data-stu-id="d4a51-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="d4a51-109">Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d4a51-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="d4a51-110">Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.</span><span class="sxs-lookup"><span data-stu-id="d4a51-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="d4a51-111">Ieslēgt manuālo sūtījumu konsolidācijas līdzekli</span><span class="sxs-lookup"><span data-stu-id="d4a51-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="d4a51-112">Lai varētu izmantot *Manuālo sūtījumu konsolidācijas līdzekli*, tas ir jāieslēdz sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d4a51-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="d4a51-113">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d4a51-114">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d4a51-115">**Modulis:** *Noliktavas vadība*</span><span class="sxs-lookup"><span data-stu-id="d4a51-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d4a51-116">**Līdzekļa nosaukums:** *Manuālā sūtījumu konsolidācija*</span><span class="sxs-lookup"><span data-stu-id="d4a51-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="d4a51-117">Kā tika minēts sadaļā [Konfigurēt sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md), pirms varat izveidot politikas, ir jāieslēdz arī *Konsolidācijas nosūtījuma* līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="d4a51-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="d4a51-118">Tomēr jums jau ir jābūt pabeigtam šim solim.</span><span class="sxs-lookup"><span data-stu-id="d4a51-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="d4a51-119">Izveidot pārdošanas pasūtījumus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="d4a51-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="d4a51-120">Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt.</span><span class="sxs-lookup"><span data-stu-id="d4a51-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="d4a51-121">Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem.</span><span class="sxs-lookup"><span data-stu-id="d4a51-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="d4a51-122">Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="d4a51-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="d4a51-123">Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="d4a51-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="d4a51-124">Izveidot 1. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="d4a51-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="d4a51-125">Pārdošanas pasūtījumi 1-1 un 1-2</span><span class="sxs-lookup"><span data-stu-id="d4a51-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="d4a51-126">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-127">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d4a51-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d4a51-128">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d4a51-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="d4a51-129">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-130">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-131">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-132">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="d4a51-133">Pārdošanas pasūtījums 1-3</span><span class="sxs-lookup"><span data-stu-id="d4a51-133">Sales order 1-3</span></span>

1. <span data-ttu-id="d4a51-134">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-135">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d4a51-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d4a51-136">**Piegādes veids:** *10*</span><span class="sxs-lookup"><span data-stu-id="d4a51-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="d4a51-137">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-138">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-139">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-140">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="d4a51-141">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-142">**Krājuma kods:** *A0002* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-143">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="d4a51-144">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d4a51-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="d4a51-145">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="d4a51-146">Izveidot 2. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="d4a51-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="d4a51-147">Pārdošanas pasūtījumi 2-1 un 2-2</span><span class="sxs-lookup"><span data-stu-id="d4a51-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="d4a51-148">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-149">**Debitora konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d4a51-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="d4a51-150">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d4a51-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="d4a51-151">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-152">**Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)</span><span class="sxs-lookup"><span data-stu-id="d4a51-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="d4a51-153">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-154">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="d4a51-155">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-156">**Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)</span><span class="sxs-lookup"><span data-stu-id="d4a51-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="d4a51-157">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="d4a51-158">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="d4a51-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="d4a51-159">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="d4a51-160">Izveidot 3. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="d4a51-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="d4a51-161">Pārdošanas pasūtījumi 3-1 un 3-2</span><span class="sxs-lookup"><span data-stu-id="d4a51-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="d4a51-162">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-163">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d4a51-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d4a51-164">**Debitora pieprasījums:** *1*</span><span class="sxs-lookup"><span data-stu-id="d4a51-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="d4a51-165">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-166">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-167">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-168">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="d4a51-169">Pārdošanas pasūtījumi 3-3 un 3-4</span><span class="sxs-lookup"><span data-stu-id="d4a51-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="d4a51-170">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-171">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d4a51-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d4a51-172">**Debitora pieprasījums:** *2*</span><span class="sxs-lookup"><span data-stu-id="d4a51-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="d4a51-173">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-174">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-175">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-176">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="d4a51-177">Izveidot 4. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="d4a51-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="d4a51-178">Pārdošanas pasūtījumi 4-1 un 4-2</span><span class="sxs-lookup"><span data-stu-id="d4a51-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="d4a51-179">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-180">**Debitora konts:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="d4a51-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="d4a51-181">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-182">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-183">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-184">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="d4a51-185">Pārdošanas pasūtījumi 4-3 un 4-4</span><span class="sxs-lookup"><span data-stu-id="d4a51-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="d4a51-186">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-187">**Debitora konts:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="d4a51-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="d4a51-188">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-189">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-190">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-191">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="d4a51-192">Pārdošanas pasūtījumi 4-5 un 4-6</span><span class="sxs-lookup"><span data-stu-id="d4a51-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="d4a51-193">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-194">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="d4a51-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="d4a51-195">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="d4a51-195">**Site:** *6*</span></span>
    - <span data-ttu-id="d4a51-196">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="d4a51-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="d4a51-197">**Kopa:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="d4a51-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="d4a51-198">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-199">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-200">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-201">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="d4a51-202">Pārdošanas pasūtījumi 4-7 un 4-8</span><span class="sxs-lookup"><span data-stu-id="d4a51-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="d4a51-203">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4a51-204">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="d4a51-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="d4a51-205">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="d4a51-205">**Site:** *6*</span></span>
    - <span data-ttu-id="d4a51-206">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="d4a51-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="d4a51-207">**Kopa:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="d4a51-208">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4a51-209">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="d4a51-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4a51-210">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4a51-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4a51-211">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="d4a51-212">Pasūtījumu izlaišana noliktavā</span><span class="sxs-lookup"><span data-stu-id="d4a51-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="d4a51-213">Sekojiet šiem soļiem, lai izlaistu pārdošanas pasūtījumu, ko izveidojāt šim scenārijam noliktavā.</span><span class="sxs-lookup"><span data-stu-id="d4a51-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="d4a51-214">Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="d4a51-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d4a51-215">Atrodiet un atlasiet izlaižamo pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="d4a51-216">Darbību rūtī cilnē **Noliktava**, atlasiet **Darbības \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="d4a51-217">Atkārtojiet šo procedūru katram otrajam pārdošanas pasūtījumam, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="d4a51-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="d4a51-218">Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku</span><span class="sxs-lookup"><span data-stu-id="d4a51-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="d4a51-219">Dodieties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Sūtījumu konsolidācijas rīks**.</span><span class="sxs-lookup"><span data-stu-id="d4a51-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="d4a51-220">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="d4a51-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="d4a51-221">Vaicājuma redaktora dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d4a51-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="d4a51-222">**Tabula:** *Pārdošanas pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="d4a51-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="d4a51-223">**Lauks:** *Pārdošanas pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="d4a51-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="d4a51-224">**Kritēriji:** ievadiet ar komatu atdalītu pārdošanas pasūtījumu numuru sarakstu katrai pasūtījumu kopai, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="d4a51-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="d4a51-225">Atlasiet **Labi**, lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="d4a51-226">Darbību rūtī atlasiet **Konsolidēt sūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="d4a51-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="d4a51-227">Atlasiet visus sūtījumus un pēc tam Darbību rūtī atlasiet **Konsolidēt**.</span><span class="sxs-lookup"><span data-stu-id="d4a51-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="d4a51-228">Pārbaudīt sūtījumus</span><span class="sxs-lookup"><span data-stu-id="d4a51-228">Verify the shipments</span></span>

<span data-ttu-id="d4a51-229">Šī procedūra ļauj pārbaudīt sūtījumus, kas ir izveidoti vai atjaunināti, veicot sūtījuma konsolidāciju.</span><span class="sxs-lookup"><span data-stu-id="d4a51-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="d4a51-230">Izmantojiet to, lai pārskatītu katru pasūtījuma kopu, ko izveidojāt šim scenārijam, un tad pārskatītu sekojošās apakšsadaļas, lai pārliecinātos, ka esat ieguvis plānotos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="d4a51-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="d4a51-231">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="d4a51-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="d4a51-232">Atrast un atlasīt nepieciešamo sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d4a51-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="d4a51-233">Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.</span><span class="sxs-lookup"><span data-stu-id="d4a51-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="d4a51-234">1. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="d4a51-234">Related shipments for order set 1</span></span>

<span data-ttu-id="d4a51-235">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="d4a51-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="d4a51-236">Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="d4a51-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="d4a51-237">Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="d4a51-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="d4a51-238">2. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="d4a51-238">Related shipments for order set 2</span></span>

<span data-ttu-id="d4a51-239">Ir jābūt izveidotiem trīs sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="d4a51-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="d4a51-240">Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.</span><span class="sxs-lookup"><span data-stu-id="d4a51-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="d4a51-241">Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.</span><span class="sxs-lookup"><span data-stu-id="d4a51-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="d4a51-242">3. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="d4a51-242">Related shipments for order set 3</span></span>

<span data-ttu-id="d4a51-243">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="d4a51-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="d4a51-244">Pirmajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*.</span><span class="sxs-lookup"><span data-stu-id="d4a51-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="d4a51-245">Otrajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *2*.</span><span class="sxs-lookup"><span data-stu-id="d4a51-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="d4a51-246">4. pasūtījumu kopas saistītie sūtījumi</span><span class="sxs-lookup"><span data-stu-id="d4a51-246">Related shipments for order set 4</span></span>

<span data-ttu-id="d4a51-247">Ir jābūt izveidotiem četriem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="d4a51-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="d4a51-248">Rindas no diviem pasūtījumiem debitoram *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="d4a51-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="d4a51-249">Rindas no diviem pasūtījumiem debitoram *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="d4a51-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="d4a51-250">Rindas no pārdošanas pasūtījumiem 4-5 un 4-6 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="d4a51-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="d4a51-251">Rindas no pārdošanas pasūtījumiem 4-7 un 4-8 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="d4a51-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4a51-252">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d4a51-252">Additional resources</span></span>

- [<span data-ttu-id="d4a51-253">Sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="d4a51-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="d4a51-254">Sūtījumu konsolidācijas politiku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d4a51-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
