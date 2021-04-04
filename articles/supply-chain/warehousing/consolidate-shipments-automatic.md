---
title: Konsolidēt sūtījumus, kad tie tiek izlaisti noliktavā, izmantojot automātisko pārdošanas pasūtījumu izlaišanu
description: Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā automatizētajā, periodiskajā izdošanas-nodošanas procedūrā.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 7102eade4a26f4b4dc08adb395aa7b50a630b9d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243947"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="53374-103">Konsolidēt sūtījumus, kad tie tiek izlaisti noliktavā, izmantojot automātisko pārdošanas pasūtījumu izlaišanu</span><span class="sxs-lookup"><span data-stu-id="53374-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53374-104">Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā automatizētajā, periodiskajā izdošanas-nodošanas procedūrā.</span><span class="sxs-lookup"><span data-stu-id="53374-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="53374-105">Pasūtījumi automātiski tiks konsolidēti sūtījumos, pamatojoties uz noteikumiem, kas definēti kā piegādes konsolidācijas politikas.</span><span class="sxs-lookup"><span data-stu-id="53374-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="53374-106">Scenārija laikā jūs izveidosiet pārdošanas pasūtījumu kopas un izlaidīsiet katru kopu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="53374-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="53374-107">Pēc tam jūs pārskatīsiet sūtījumus, kas izveidoti vai atjaunināti sūtījuma konsolidācijas laikā, pamatojoties uz konfigurētajām politikām.</span><span class="sxs-lookup"><span data-stu-id="53374-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="53374-108">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="53374-108">Make demo data available</span></span>

<span data-ttu-id="53374-109">Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="53374-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="53374-110">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="53374-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="53374-111">Iestatīt sūtījumu konsolidācijas politikas un preču filtrus</span><span class="sxs-lookup"><span data-stu-id="53374-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="53374-112">Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="53374-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="53374-113">Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.</span><span class="sxs-lookup"><span data-stu-id="53374-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="53374-114">Izveidot pārdošanas pasūtījumus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="53374-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="53374-115">Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt.</span><span class="sxs-lookup"><span data-stu-id="53374-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="53374-116">Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem.</span><span class="sxs-lookup"><span data-stu-id="53374-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="53374-117">Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="53374-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="53374-118">Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="53374-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="53374-119">Izveidot 1. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="53374-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="53374-120">Pārdošanas pasūtījums 1-1</span><span class="sxs-lookup"><span data-stu-id="53374-120">Sales order 1-1</span></span>

1. <span data-ttu-id="53374-121">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="53374-122">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="53374-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="53374-123">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="53374-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="53374-124">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-125">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-126">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="53374-127">Pārdošanas pasūtījums 1-2</span><span class="sxs-lookup"><span data-stu-id="53374-127">Sales order 1-2</span></span>

1. <span data-ttu-id="53374-128">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="53374-129">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="53374-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="53374-130">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="53374-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="53374-131">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-132">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-133">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="53374-134">Pārdošanas pasūtījums 1-3</span><span class="sxs-lookup"><span data-stu-id="53374-134">Sales order 1-3</span></span>

1. <span data-ttu-id="53374-135">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="53374-136">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="53374-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="53374-137">**Piegādes veids:** *10*</span><span class="sxs-lookup"><span data-stu-id="53374-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="53374-138">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-139">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-140">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="53374-141">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-142">**Krājuma kods:** *A0002* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-143">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="53374-144">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="53374-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="53374-145">Izveidot 2. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="53374-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="53374-146">Pārdošanas pasūtījumi 2-1 un 2-2</span><span class="sxs-lookup"><span data-stu-id="53374-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="53374-147">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="53374-148">**Debitora konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="53374-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="53374-149">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-150">**Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)</span><span class="sxs-lookup"><span data-stu-id="53374-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="53374-151">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="53374-152">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-153">**Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)</span><span class="sxs-lookup"><span data-stu-id="53374-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="53374-154">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="53374-155">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="53374-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="53374-156">Izveidot 3. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="53374-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="53374-157">Pārdošanas pasūtījums 3-1</span><span class="sxs-lookup"><span data-stu-id="53374-157">Sales order 3-1</span></span>

1. <span data-ttu-id="53374-158">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="53374-159">**Debitora konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="53374-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="53374-160">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-161">**Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)</span><span class="sxs-lookup"><span data-stu-id="53374-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="53374-162">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="53374-163">Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-164">**Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)</span><span class="sxs-lookup"><span data-stu-id="53374-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="53374-165">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="53374-166">**Piegādes veids:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="53374-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="53374-167">Šis pasūtījums ir identisks diviem pasūtījumiem, kurus izveidojāt 2. pasūtījuma kopai.</span><span class="sxs-lookup"><span data-stu-id="53374-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="53374-168">Tomēr tas ir norādīts kā atsevišķa pasūtījumu kopa, jo vēlāk šajā scenārijā jūs to atbrīvosit atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="53374-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="53374-169">Izveidot 4. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="53374-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="53374-170">Pārdošanas pasūtījums 4-1</span><span class="sxs-lookup"><span data-stu-id="53374-170">Sales order 4-1</span></span>

1. <span data-ttu-id="53374-171">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="53374-172">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="53374-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="53374-173">**Debitora pieprasījums:** *1*</span><span class="sxs-lookup"><span data-stu-id="53374-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="53374-174">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-175">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-176">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="53374-177">Izveidot 5. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="53374-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="53374-178">Pārdošanas pasūtījumi 5-1 un 5-2</span><span class="sxs-lookup"><span data-stu-id="53374-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="53374-179">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="53374-180">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="53374-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="53374-181">**Debitora pieprasījums:** *2*</span><span class="sxs-lookup"><span data-stu-id="53374-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="53374-182">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-183">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-184">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="53374-185">Pārdošanas pasūtījums 5-3</span><span class="sxs-lookup"><span data-stu-id="53374-185">Sales order 5-3</span></span>

1. <span data-ttu-id="53374-186">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="53374-187">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="53374-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="53374-188">**Debitora pieprasījums:** *1*</span><span class="sxs-lookup"><span data-stu-id="53374-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="53374-189">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-190">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-191">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="53374-192">Izveidot 6. pasūtījuma kopu</span><span class="sxs-lookup"><span data-stu-id="53374-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="53374-193">Pārdošanas pasūtījumi 6-1 un 6-2</span><span class="sxs-lookup"><span data-stu-id="53374-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="53374-194">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="53374-195">**Debitora konts:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="53374-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="53374-196">**Debitora pieprasījums:** *2*</span><span class="sxs-lookup"><span data-stu-id="53374-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="53374-197">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-198">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-199">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="53374-200">Pārdošanas pasūtījumi 6-3 un 6-4</span><span class="sxs-lookup"><span data-stu-id="53374-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="53374-201">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="53374-202">**Debitora konts:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="53374-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="53374-203">**Debitora pieprasījums:** *1*</span><span class="sxs-lookup"><span data-stu-id="53374-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="53374-204">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-205">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-206">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="53374-207">Pārdošanas pasūtījumi 6-5 un 6-6</span><span class="sxs-lookup"><span data-stu-id="53374-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="53374-208">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="53374-209">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="53374-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="53374-210">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="53374-210">**Site:** *6*</span></span>
    - <span data-ttu-id="53374-211">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="53374-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="53374-212">**Kopa:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="53374-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="53374-213">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-214">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-215">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="53374-216">Pārdošanas pasūtījumi 6-7 un 6-8</span><span class="sxs-lookup"><span data-stu-id="53374-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="53374-217">Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="53374-218">**Debitora konts:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="53374-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="53374-219">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="53374-219">**Site:** *6*</span></span>
    - <span data-ttu-id="53374-220">**Noliktava:** *61*</span><span class="sxs-lookup"><span data-stu-id="53374-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="53374-221">**Kopa:** atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="53374-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="53374-222">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="53374-223">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="53374-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="53374-224">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="53374-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="53374-225">Automātiska pārdošanas pasūtījumu pārvietošana uz noliktavu</span><span class="sxs-lookup"><span data-stu-id="53374-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="53374-226">Katrai iepriekš izveidoto pārdošanas pasūtījumu kopai jūs veiksit automātiskas izlaišanas procedūru noliktavā.</span><span class="sxs-lookup"><span data-stu-id="53374-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="53374-227">Katrā gadījumā jums būs jāstrādā, izmantojot [pamata nodošana uz noliktavu procedūru](#release-procedure), kas tiek sniegta šeit.</span><span class="sxs-lookup"><span data-stu-id="53374-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="53374-228">Pamata nodošana uz noliktavu procedūra</span><span class="sxs-lookup"><span data-stu-id="53374-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="53374-229">Katrai iepriekš izveidotajai pārdošanas pasūtījumu kopai tiks izpildītas trīs procedūras, kas norādītas šādās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="53374-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="53374-230">Atjaunināt kopuma veidni, kas tiks izmantota izlaišanas laikā</span><span class="sxs-lookup"><span data-stu-id="53374-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="53374-231">Dodieties uz **Noliktavas vadība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="53374-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="53374-232">Iestatiet lauku **Kopuma veidnes veids** uz *Sūtīšana*.</span><span class="sxs-lookup"><span data-stu-id="53374-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="53374-233">Meklējiet un atlasiet kopuma veidni, kas ir saistīta ar noliktavu, ko izmantojāt pasūtījuma kopās, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="53374-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="53374-234">Piemēram, ja izmantojāt noliktavu *24*, atlasiet **24 nosūtīšanas noklusējuma** kopuma veidni.</span><span class="sxs-lookup"><span data-stu-id="53374-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="53374-235">Ja izmantojāt noliktavu *61*, atlasiet **61 nosūtīšanas noklusējuma** kopuma veidni.</span><span class="sxs-lookup"><span data-stu-id="53374-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="53374-236">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="53374-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="53374-237">Iestatiet opciju **Apstrādāt kopumu, to pārvietojot uz noliktavu** uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="53374-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="53374-238">Nodot izpildei noliktavā</span><span class="sxs-lookup"><span data-stu-id="53374-238">Release to the warehouse</span></span>

1. <span data-ttu-id="53374-239">Doties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Automātiska pārdošanas pasūtījumu nodošana**.</span><span class="sxs-lookup"><span data-stu-id="53374-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="53374-240">Iestatiet lauku **Nododamais daudzums** uz *Visi*.</span><span class="sxs-lookup"><span data-stu-id="53374-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="53374-241">Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu vaicājuma dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="53374-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="53374-242">Cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="53374-243">**Tabula:** *Pārdošanas pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="53374-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="53374-244">**Atveidotā tabula:** *Pārdošanas pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="53374-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="53374-245">**Lauks:** *Pārdošanas pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="53374-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="53374-246">**Kritēriji:** Ievadiet ar komatu atdalītu pārdošanas pasūtījumu numuru sarakstu no vēlamā pasūtījuma komplekta.</span><span class="sxs-lookup"><span data-stu-id="53374-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="53374-247">Atlasiet **Labi**, lai saglabātu vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="53374-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="53374-248">Atlasiet **Labi**, lai sāktu procedūru *Automātiski pārvietot uz noliktavu*.</span><span class="sxs-lookup"><span data-stu-id="53374-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="53374-249">Pārskatiet izveidoto vai atjaunināto sūtījumu</span><span class="sxs-lookup"><span data-stu-id="53374-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="53374-250">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="53374-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="53374-251">Atrast un atlasīt nepieciešamo sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="53374-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="53374-252">Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.</span><span class="sxs-lookup"><span data-stu-id="53374-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="53374-253">Izlaist pārdošanas pasūtījumus no 1. pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="53374-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="53374-254">Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 1. pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="53374-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="53374-255">Kad esat pabeidzis, jums būtu jāredz, ka ir izveidoti divi sūtījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="53374-256">Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="53374-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="53374-257">Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="53374-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="53374-258">Izlaist pārdošanas pasūtījumus no 2. pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="53374-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="53374-259">Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 2. pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="53374-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="53374-260">Kad esat pabeidzis, jums būtu jāredz, ka ir izveidoti trīs sūtījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="53374-261">Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.</span><span class="sxs-lookup"><span data-stu-id="53374-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="53374-262">Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.</span><span class="sxs-lookup"><span data-stu-id="53374-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="53374-263">Izlaist pārdošanas pasūtījumus no 3. pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="53374-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="53374-264">Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 3. pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="53374-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="53374-265">Kad esat pabeidzis, jums vajadzētu redzēt, ka ir notikušas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="53374-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="53374-266">Tika atjaunināts viens esošais sūtījums (sūtījums, kas tika izveidots, kad tika nodota 2. pasūtījuma kopa).</span><span class="sxs-lookup"><span data-stu-id="53374-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="53374-267">Tika pievienota rinda ar viegli *Uzliesmojošu* krājumu.</span><span class="sxs-lookup"><span data-stu-id="53374-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="53374-268">Tika izveidots viens jauns sūtījums, kas satur *sprādzienbīstamu* krājumu.</span><span class="sxs-lookup"><span data-stu-id="53374-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="53374-269">Izlaist pārdošanas pasūtījumus no 4. pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="53374-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="53374-270">Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 4. pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="53374-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="53374-271">Kad esat pabeidzis, jums būtu jāredz, ka ir atjaunināts viens esošais sūtījums (kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*).</span><span class="sxs-lookup"><span data-stu-id="53374-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="53374-272">Tai tika pievienota viena jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="53374-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="53374-273">Izlaist pārdošanas pasūtījumus no 5. pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="53374-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="53374-274">Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 5. pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="53374-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="53374-275">Kad esat pabeidzis, jums vajadzētu redzēt, ka ir notikušas šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="53374-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="53374-276">Tika atjaunināts viens esošais sūtījums (kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*).</span><span class="sxs-lookup"><span data-stu-id="53374-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="53374-277">Tai tika pievienota rinda no pārdošanas pasūtījuma 5-3 (kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*).</span><span class="sxs-lookup"><span data-stu-id="53374-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="53374-278">Tika izveidots viens jauns sūtījums, kur pārdošanas pasūtījumu 5-1 un 5-2 rindas tiek grupētas vienā sūtījumā.</span><span class="sxs-lookup"><span data-stu-id="53374-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="53374-279">Izlaist pārdošanas pasūtījumus no 6. pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="53374-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="53374-280">Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 6. pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="53374-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="53374-281">Kad esat pabeidzis, jums būtu jāredz, ka ir izveidoti četri sūtījumi:</span><span class="sxs-lookup"><span data-stu-id="53374-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="53374-282">Rindas no diviem pasūtījumiem debitoram *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="53374-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="53374-283">Rindas no diviem pasūtījumiem debitoram *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="53374-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="53374-284">Rindas no pārdošanas pasūtījumiem 6-5 un 6-6 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="53374-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="53374-285">Rindas no pārdošanas pasūtījumiem 6-7 un 6-8 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="53374-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53374-286">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="53374-286">Additional resources</span></span>

- [<span data-ttu-id="53374-287">Sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="53374-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="53374-288">Sūtījumu konsolidācijas politiku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="53374-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]