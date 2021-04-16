---
title: Konsolidēt sūtījumus, ja sūtījuma konsolidācijas politika tiek ignorēta lapā “Pārvietot uz noliktavu”
description: Šī tēma piedāvā scenāriju, kur viena vai vairākas pārdošanas rindas ir manuāli jāpārvieto uz noliktavu no lapas Pārvietot uz noliktavu, un sistēmas definētā sūtījumu konsolidācijas politika ir jāignorē pirms pārvietošanas.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dcd619ad2906d4224966e2696712ed0e71886eb2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837493"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="a277a-103">Konsolidēt sūtījumus, ja sūtījuma konsolidācijas politika tiek ignorēta lapā “Pārvietot uz noliktavu”</span><span class="sxs-lookup"><span data-stu-id="a277a-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a277a-104">Šī tēma piedāvā scenāriju, kur viena vai vairākas pārdošanas rindas ir manuāli jāpārvieto uz noliktavu no lapas **Pārvietot uz noliktavu**, un sistēmas definētā sūtījumu konsolidācijas politika ir jāignorē pirms pārvietošanas.</span><span class="sxs-lookup"><span data-stu-id="a277a-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="a277a-105">Sūtījuma konsolidācijas politikas ignorēšana var būt nepieciešama, ja, piemēram, pasūtījums, kas parasti netiek konsolidēts ar atvērtiem sūtījumiem, ir jākonsolidē ar atvērtiem sūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="a277a-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="a277a-106">Scenārija laikā jūs izveidosiet pārdošanas pasūtījumu kopu un pēc tam ignorēsiet noklusējuma sūtījumu konsolidācijas politiku pirms pasūtījumu nodošanas noliktavā.</span><span class="sxs-lookup"><span data-stu-id="a277a-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="a277a-107">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="a277a-107">Make demo data available</span></span>

<span data-ttu-id="a277a-108">Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a277a-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a277a-109">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="a277a-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="a277a-110">Iestatīt sūtījumu konsolidācijas politikas un preču filtrus</span><span class="sxs-lookup"><span data-stu-id="a277a-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="a277a-111">Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a277a-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="a277a-112">Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.</span><span class="sxs-lookup"><span data-stu-id="a277a-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="a277a-113">Izveidot pārdošanas pasūtījumus šim scenārijam</span><span class="sxs-lookup"><span data-stu-id="a277a-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="a277a-114">Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet trīs identiskus pārdošanas pasūtījumus, kuriem ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="a277a-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a277a-115">**Debitora konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a277a-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="a277a-116">Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="a277a-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a277a-117">**Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)</span><span class="sxs-lookup"><span data-stu-id="a277a-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a277a-118">**Daudzums:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a277a-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a277a-119">Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="a277a-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="a277a-120">Pārvietot pārdošanas pasūtījumus no lapas Pārvietot uz noliktavu</span><span class="sxs-lookup"><span data-stu-id="a277a-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="a277a-121">Sekojiet šiem soļiem, lai ignorētu sūtījuma konsolidācijas politiku izlaišanas noliktavā laikā.</span><span class="sxs-lookup"><span data-stu-id="a277a-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="a277a-122">Dodieties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Pārvietot uz noliktavu**.</span><span class="sxs-lookup"><span data-stu-id="a277a-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="a277a-123">Augšējā rūtī atlasiet pirmo pārdošanas pasūtījumu, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="a277a-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="a277a-124">Atlasiet **Pievienot**, lai pievienotu rindu izlaišanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="a277a-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="a277a-125">Ievērojiet, ka apakšējā rūtī tiek lietota *Noklusējuma* sūtījumu konsolidācijas politika.</span><span class="sxs-lookup"><span data-stu-id="a277a-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="a277a-126">Apakšējā rūtī atlasiet **Atlasīt jaunu sūtījumu konsolidācijas politiku**.</span><span class="sxs-lookup"><span data-stu-id="a277a-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="a277a-127">Atlasiet politiku, kas ļauj veikt konsolidāciju ar citiem tās pašas politikas atvērtajiem sūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="a277a-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="a277a-128">Piemēram, atlasiet *CustomerOrderNo* politiku.</span><span class="sxs-lookup"><span data-stu-id="a277a-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="a277a-129">Atlasiet **Pārvietot uz noliktavu**.</span><span class="sxs-lookup"><span data-stu-id="a277a-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a277a-130">Atlasiet otro un trešo pārdošanas pasūtījumu, ko izveidojāt šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="a277a-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="a277a-131">Atlasiet **Pievienot**, lai pievienotu rindas izlaišanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="a277a-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="a277a-132">Ievērojiet, ka apakšējā rūtī tiek lietota *Noklusējuma* politika.</span><span class="sxs-lookup"><span data-stu-id="a277a-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="a277a-133">Atlasiet otro rindu un pēc tam laukā **Atlasīt jaunu sūtījumu konsolidācijas politiku** atlasiet *CustomerOrderNo* politiku.</span><span class="sxs-lookup"><span data-stu-id="a277a-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="a277a-134">Atlasiet **Pārvietot uz noliktavu** abām rindām.</span><span class="sxs-lookup"><span data-stu-id="a277a-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="a277a-135">Pārbaudīt sūtījumus</span><span class="sxs-lookup"><span data-stu-id="a277a-135">Verify the shipments</span></span>

<span data-ttu-id="a277a-136">Ir jābūt izveidotiem diviem sūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="a277a-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="a277a-137">Pirmajā sūtījumā ir divas rindas, un tās tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="a277a-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="a277a-138">Otrajā sūtījumā ir viena rinda, un tā tika izveidota, izmantojot *Noklusējuma* sūtījumu konsolidācijas politiku.</span><span class="sxs-lookup"><span data-stu-id="a277a-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="a277a-139">Sekojiet šiem soļiem, lai pārskatītu izveidotos sūtījumus.</span><span class="sxs-lookup"><span data-stu-id="a277a-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="a277a-140">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a277a-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="a277a-141">Atrast un atlasīt nepieciešamo sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a277a-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="a277a-142">Laukā **Sūtījuma konsolidācijas politika** pārskatiet izveidoto konsolidācijas politiku, izveidojot sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a277a-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a277a-143">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a277a-143">Additional resources</span></span>

- [<span data-ttu-id="a277a-144">Sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="a277a-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="a277a-145">Sūtījumu konsolidācijas politiku konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a277a-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]