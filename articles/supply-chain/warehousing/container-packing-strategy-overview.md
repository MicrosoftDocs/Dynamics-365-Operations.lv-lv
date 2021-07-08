---
title: Konteinera iepakošanas stratēģijas
description: Šajā tēmā aprakstītas atšķirības starp konteinera iepakošanas stratēģiju un sniegti piemēri.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292765"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="800bd-103">Konteinera iepakošanas stratēģijas</span><span class="sxs-lookup"><span data-stu-id="800bd-103">Container packing strategies</span></span>

<span data-ttu-id="800bd-104">Šī *konteinera iepakošanas stratēģija* ir stratēģija, ko varat izmantot, lai definētu krājumu sadalījumus konteineros.</span><span class="sxs-lookup"><span data-stu-id="800bd-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="800bd-105">Šajā tēmā skaidrotas atšķirības starp stratēģijām *Iepakot visos atvērtajos konteineros* un *Iepakot tikai pašreizējā konteinerā*.</span><span class="sxs-lookup"><span data-stu-id="800bd-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="800bd-106">**Iepakot visos atvērtajos konteineros** — sistēmai ir jāpārbauda visi atvērtie konteineri, kas jau ir izveidoti konteinerizācijas cikla laikā, lai pārliecinātos, vai krājums ietilps vienā no tiem.</span><span class="sxs-lookup"><span data-stu-id="800bd-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="800bd-107">Iepakošanas laikā sistēma pārbauda katru krājumu, lai noteiktu, vai tas iederas jebkurā no iepriekš izveidotajiem konteineriem.</span><span class="sxs-lookup"><span data-stu-id="800bd-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="800bd-108">Ja krājums neietilpst esošajā konteinerā, sistēma izveido jaunu konteineru un turpina, līdz pabeigta visa pasūtījuma iepakošana.</span><span class="sxs-lookup"><span data-stu-id="800bd-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="800bd-109">Piemēram, *n* pasūtītiem krājumiem nepieciešama konteinerizācija.</span><span class="sxs-lookup"><span data-stu-id="800bd-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="800bd-110">Tādā gadījumā, katru reizi, kad sistēma apstrādā krājumu, kas neietilpst neviena esošā konteinerā, tiks veiktas visas (\[(*n* – 1) × (*n* + 1)\] ÷ 2) pārbaudes, lai novērtētu, vai krājums iederas esošos konteineros.</span><span class="sxs-lookup"><span data-stu-id="800bd-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="800bd-111">**Iepakot tikai esošajā konteinerā** — Sistēmai jāpārbauda tikai nesen izveidotais konteiners, lai pārliecinātos, vai vienums tajā iederēsies.</span><span class="sxs-lookup"><span data-stu-id="800bd-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="800bd-112">Iepakošanas laikā sistēma pārbauda katru krājumu, lai noteiktu, vai tas iederēsies nesen izveidotajā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="800bd-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="800bd-113">Ja krājums neietilpst šajā konteinerā, sistēma izveido jaunu konteineru un turpina, līdz pabeigta visa pasūtījuma iepakošana.</span><span class="sxs-lookup"><span data-stu-id="800bd-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="800bd-114">Piemēram, *n* pasūtītiem krājumiem nepieciešama konteinerizācija.</span><span class="sxs-lookup"><span data-stu-id="800bd-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="800bd-115">Sliktākajā gadījumā sistēma veiks visas (*n* – 1) pārbaudes, lai novērtētu, vai krājums iederas konteineros.</span><span class="sxs-lookup"><span data-stu-id="800bd-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="800bd-116">Konteinera iepakošanas stratēģiju plūsmas piemērs</span><span class="sxs-lookup"><span data-stu-id="800bd-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="800bd-117">Konteinerizācijai tiek iestatīti šādi vienumi.</span><span class="sxs-lookup"><span data-stu-id="800bd-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="800bd-118">Objekts</span><span class="sxs-lookup"><span data-stu-id="800bd-118">Item</span></span> | <span data-ttu-id="800bd-119">Fiziskās dimensijas (platums × dziļums × augstums)</span><span class="sxs-lookup"><span data-stu-id="800bd-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="800bd-120">Lielums</span><span class="sxs-lookup"><span data-stu-id="800bd-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="800bd-121">HDMI kabelis 6´</span><span class="sxs-lookup"><span data-stu-id="800bd-121">HDMI Cable 6'</span></span> | <span data-ttu-id="800bd-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="800bd-122">1 × 1 × 1</span></span> | <span data-ttu-id="800bd-123">1</span><span class="sxs-lookup"><span data-stu-id="800bd-123">1</span></span> |
| <span data-ttu-id="800bd-124">HDMI kabelis 12´</span><span class="sxs-lookup"><span data-stu-id="800bd-124">HDMI Cable 12'</span></span> | <span data-ttu-id="800bd-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="800bd-125">2 × 1 × 1</span></span> | <span data-ttu-id="800bd-126">1</span><span class="sxs-lookup"><span data-stu-id="800bd-126">1</span></span> |
| <span data-ttu-id="800bd-127">HDMI kabelis 18´</span><span class="sxs-lookup"><span data-stu-id="800bd-127">HDMI Cable 18'</span></span> | <span data-ttu-id="800bd-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="800bd-128">3 × 1 × 1</span></span> | <span data-ttu-id="800bd-129">2</span><span class="sxs-lookup"><span data-stu-id="800bd-129">2</span></span> |

<span data-ttu-id="800bd-130">Iepakošanai tiks izmantota tālāk norādītās rūtiņas iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="800bd-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="800bd-131">Konteiners</span><span class="sxs-lookup"><span data-stu-id="800bd-131">Container</span></span> | <span data-ttu-id="800bd-132">Fiziskās dimensijas (garums × platums × augstums)</span><span class="sxs-lookup"><span data-stu-id="800bd-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="800bd-133">Lielums</span><span class="sxs-lookup"><span data-stu-id="800bd-133">Weight</span></span> | <span data-ttu-id="800bd-134">Tilpums</span><span class="sxs-lookup"><span data-stu-id="800bd-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="800bd-135">Vidēja kaste</span><span class="sxs-lookup"><span data-stu-id="800bd-135">Medium Box</span></span> | <span data-ttu-id="800bd-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="800bd-136">6 × 3 × 2</span></span> | <span data-ttu-id="800bd-137">10.</span><span class="sxs-lookup"><span data-stu-id="800bd-137">10</span></span> | <span data-ttu-id="800bd-138">100</span><span class="sxs-lookup"><span data-stu-id="800bd-138">100</span></span> |

<span data-ttu-id="800bd-139">Visbeidzot jūs iestatāt pasūtījumu, kam ir šādas preces un daudzumi.</span><span class="sxs-lookup"><span data-stu-id="800bd-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="800bd-140">Pārdošanas pasūtījumu rinda</span><span class="sxs-lookup"><span data-stu-id="800bd-140">Sales order line</span></span> | <span data-ttu-id="800bd-141">Daudzums</span><span class="sxs-lookup"><span data-stu-id="800bd-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="800bd-142">HDMI kabelis 12´</span><span class="sxs-lookup"><span data-stu-id="800bd-142">HDMI Cable 12'</span></span> | <span data-ttu-id="800bd-143">9</span><span class="sxs-lookup"><span data-stu-id="800bd-143">9</span></span> |
| <span data-ttu-id="800bd-144">HDMI kabelis 18´</span><span class="sxs-lookup"><span data-stu-id="800bd-144">HDMI Cable 18'</span></span> | <span data-ttu-id="800bd-145">8</span><span class="sxs-lookup"><span data-stu-id="800bd-145">8</span></span> |
| <span data-ttu-id="800bd-146">HDMI kabelis 6´</span><span class="sxs-lookup"><span data-stu-id="800bd-146">HDMI Cable 6'</span></span> | <span data-ttu-id="800bd-147">13</span><span class="sxs-lookup"><span data-stu-id="800bd-147">13</span></span> |

<span data-ttu-id="800bd-148">Šajā tabulā ir apkopots, kā konteinerizācija darbojas, kad izmantojat stratēģiju *Iepakot visos atvērtajos konteineros* un, ja izmantojat stratēģiju *Iepakot tikai esošajā konteinerā*.</span><span class="sxs-lookup"><span data-stu-id="800bd-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="800bd-149">Iepakot visos atvērtajos konteineros</span><span class="sxs-lookup"><span data-stu-id="800bd-149">Pack into all open containers</span></span> | <span data-ttu-id="800bd-150">Iepakot pašreizējā konteinerā</span><span class="sxs-lookup"><span data-stu-id="800bd-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="800bd-151">HDMI kabelis 12´:</span><span class="sxs-lookup"><span data-stu-id="800bd-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="800bd-152">Izveidot jaunu konteineru, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="800bd-153">Ievietojiet 9 ea konteinerā CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="800bd-154">HDMI kabelis 12´:</span><span class="sxs-lookup"><span data-stu-id="800bd-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="800bd-155">Izveidot jaunu konteineru, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="800bd-156">Ievietojiet 9 ea konteinerā CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="800bd-157">HDMI kabelis 18´:</span><span class="sxs-lookup"><span data-stu-id="800bd-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="800bd-158">Pārbaudiet, vai krājums var ietilpt konteinerā CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="800bd-159">Izveidot jaunu konteineru, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="800bd-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="800bd-160">Ievietojiet 5 ea konteinerā CONT0002.</span><span class="sxs-lookup"><span data-stu-id="800bd-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="800bd-161">Izveidot jaunu konteineru, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="800bd-162">Ievietojiet 3 ea konteinerā CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="800bd-163">HDMI kabelis 18´:</span><span class="sxs-lookup"><span data-stu-id="800bd-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="800bd-164">Pārbaudiet, vai krājums var ietilpt konteinerā CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="800bd-165">Izveidot jaunu konteineru, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="800bd-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="800bd-166">Ievietojiet 5 ea konteinerā CONT0002.</span><span class="sxs-lookup"><span data-stu-id="800bd-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="800bd-167">Izveidot jaunu konteineru, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="800bd-168">Ievietojiet 3 ea konteinerā CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="800bd-169">HDMI kabelis 6´:</span><span class="sxs-lookup"><span data-stu-id="800bd-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="800bd-170">Pārbaudiet, vai krājums var ietilpt konteinerā CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="800bd-171">Ievietojiet 1 ea konteinerā CONT0001.</span><span class="sxs-lookup"><span data-stu-id="800bd-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="800bd-172">Pārbaudiet, vai krājums var ietilpt konteinerā CONT0002.</span><span class="sxs-lookup"><span data-stu-id="800bd-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="800bd-173">Pārbaudiet, vai krājums var ietilpt konteinerā CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="800bd-174">Ievietojiet 4 ea konteinerā CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="800bd-175">Izveidot jaunu konteineru, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="800bd-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="800bd-176">Ievietojiet 8 ea konteinerā CONT0004.</span><span class="sxs-lookup"><span data-stu-id="800bd-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="800bd-177">HDMI kabelis 6´:</span><span class="sxs-lookup"><span data-stu-id="800bd-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="800bd-178">Pārbaudiet, vai krājums var ietilpt konteinerā CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="800bd-179">Ievietojiet 4 ea konteinerā CONT0003.</span><span class="sxs-lookup"><span data-stu-id="800bd-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="800bd-180">Izveidot jaunu konteineru, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="800bd-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="800bd-181">Ievietojiet 9 ea konteinerā CONT0004.</span><span class="sxs-lookup"><span data-stu-id="800bd-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="800bd-182">Scenārija piemērs: iepakojiet vienu pasūtījumu katrā konteinerā</span><span class="sxs-lookup"><span data-stu-id="800bd-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="800bd-183">Šajā sadaļā ir scenārijs, kurā sistēma ir iestatīta vairāku pasūtījumu konsolidēšanai vienā sūtījumā.</span><span class="sxs-lookup"><span data-stu-id="800bd-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="800bd-184">Tāpēc konteinerizācija tiks veikta no pārdošanas pasūtījuma, lai nodrošinātu, ka katrs pasūtījums, kurā ir vairākas preces, tiek iepakots savā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="800bd-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="800bd-185">Šī funkcionalitāte ļauj rīkoties ar scenārijiem, kuros katrā konteinerā ir jāiepako tikai viens pārdošanas pasūtījums, tādējādi sadales centrs var veikt pilnu konteineru pārkraušanu sadales centrā starp mazumtirdzniecības veikaliem.</span><span class="sxs-lookup"><span data-stu-id="800bd-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="800bd-186">Papildus mazumtirdzniecības scenārijiem (pasūtījums katram mazumtirdzniecības veikalam un nosūtīšana uz sadales centru pārkraušanai sadales centrā) šī tehnika parasti tiek izmantota arī racionālās piegādes ķēdēs (pārdošanas pasūtījums tikai laika ražošanas rindā).</span><span class="sxs-lookup"><span data-stu-id="800bd-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="800bd-187">Šajā scenārijā ir parādīts, kā var samazināt to konteineru skaitu, kas tiek novērtēti iepakošanas laikā, izmantojot konteinerizācijas stratēģiju *Iepakot tikai esošajā konteinerā*.</span><span class="sxs-lookup"><span data-stu-id="800bd-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="800bd-188">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="800bd-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="800bd-189">Ieslēgt iespēju Konsolidēt sūtījumus jūsu sistēmā</span><span class="sxs-lookup"><span data-stu-id="800bd-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="800bd-190">Šajā scenārijā tiek izmantots līdzeklis *Konsolidēt sūtījumus*.</span><span class="sxs-lookup"><span data-stu-id="800bd-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="800bd-191">Ja šis līdzeklis sistēmā vēl nav pieejams, as ir jāslēdz, izmantojot [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="800bd-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="800bd-192">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="800bd-192">Make demo data available</span></span>

<span data-ttu-id="800bd-193">Šis scenārijs ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="800bd-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="800bd-194">Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.</span><span class="sxs-lookup"><span data-stu-id="800bd-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="800bd-195">Pārbaudīt vai izveidot konteineru tipus</span><span class="sxs-lookup"><span data-stu-id="800bd-195">Inspect or create container types</span></span>

<span data-ttu-id="800bd-196">Lai pārbaudītu konteinera tipus vai izveidotu jaunus konteineru tipus, ja tie ir nepieciešami, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="800bd-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="800bd-197">Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Konteineri** \> **Konteineru tipi**.</span><span class="sxs-lookup"><span data-stu-id="800bd-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="800bd-198">Pārliecinieties, vai demonstrācijas datos ir pieejams katrs no šiem konteineru tipiem.</span><span class="sxs-lookup"><span data-stu-id="800bd-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="800bd-199">Pēc vajadzības rediģējiet vai izveidojiet konteineru tipus.</span><span class="sxs-lookup"><span data-stu-id="800bd-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="800bd-200">Konteinera tips 1:</span><span class="sxs-lookup"><span data-stu-id="800bd-200">Container type 1:</span></span>

        - <span data-ttu-id="800bd-201">**Konteinera tipa kods:** *Kaste - liela*</span><span class="sxs-lookup"><span data-stu-id="800bd-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="800bd-202">**Apraksts:** *Liela kaste*</span><span class="sxs-lookup"><span data-stu-id="800bd-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="800bd-203">**Maksimālais neto svars:** *100*</span><span class="sxs-lookup"><span data-stu-id="800bd-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="800bd-204">**Tilpums:** *400*</span><span class="sxs-lookup"><span data-stu-id="800bd-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="800bd-205">**Garums:** *4*</span><span class="sxs-lookup"><span data-stu-id="800bd-205">**Length:** *4*</span></span>
        - <span data-ttu-id="800bd-206">**Platums:** *10*</span><span class="sxs-lookup"><span data-stu-id="800bd-206">**Width:** *10*</span></span>
        - <span data-ttu-id="800bd-207">**Augstums:** *10*</span><span class="sxs-lookup"><span data-stu-id="800bd-207">**Height:** *10*</span></span>

    - <span data-ttu-id="800bd-208">Konteinera tips 2:</span><span class="sxs-lookup"><span data-stu-id="800bd-208">Container type 2:</span></span>

        - <span data-ttu-id="800bd-209">**Konteinera tipa kods:** *Kaste - vidēja*</span><span class="sxs-lookup"><span data-stu-id="800bd-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="800bd-210">**Apraksts:** *Vidēja kaste*</span><span class="sxs-lookup"><span data-stu-id="800bd-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="800bd-211">**Maksimālais neto svars:** *50*</span><span class="sxs-lookup"><span data-stu-id="800bd-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="800bd-212">**Tilpums:** *200*</span><span class="sxs-lookup"><span data-stu-id="800bd-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="800bd-213">**Garums:** *2*</span><span class="sxs-lookup"><span data-stu-id="800bd-213">**Length:** *2*</span></span>
        - <span data-ttu-id="800bd-214">**Platums:** *10*</span><span class="sxs-lookup"><span data-stu-id="800bd-214">**Width:** *10*</span></span>
        - <span data-ttu-id="800bd-215">**Augstums:** *10*</span><span class="sxs-lookup"><span data-stu-id="800bd-215">**Height:** *10*</span></span>

    - <span data-ttu-id="800bd-216">Konteinera tips 3:</span><span class="sxs-lookup"><span data-stu-id="800bd-216">Container type 3:</span></span>

        - <span data-ttu-id="800bd-217">**Konteinera tipa kods:** *Kaste - maza*</span><span class="sxs-lookup"><span data-stu-id="800bd-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="800bd-218">**Apraksts:** *Maza kaste*</span><span class="sxs-lookup"><span data-stu-id="800bd-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="800bd-219">**Maksimālais neto svars:** *20*</span><span class="sxs-lookup"><span data-stu-id="800bd-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="800bd-220">**Tilpums:** *100*</span><span class="sxs-lookup"><span data-stu-id="800bd-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="800bd-221">**Garums:** *1*</span><span class="sxs-lookup"><span data-stu-id="800bd-221">**Length:** *1*</span></span>
        - <span data-ttu-id="800bd-222">**Platums:** *10*</span><span class="sxs-lookup"><span data-stu-id="800bd-222">**Width:** *10*</span></span>
        - <span data-ttu-id="800bd-223">**Augstums:** *10*</span><span class="sxs-lookup"><span data-stu-id="800bd-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="800bd-224">Pārbaudīt vai izveidot konteineru grupas</span><span class="sxs-lookup"><span data-stu-id="800bd-224">Inspect or create container groups</span></span>

<span data-ttu-id="800bd-225">Lai pārbaudītu konteinera grupas vai izveidotu jaunus konteineru grupas, ja tie ir nepieciešami, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="800bd-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="800bd-226">Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru grupas**.</span><span class="sxs-lookup"><span data-stu-id="800bd-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="800bd-227">Pārliecinieties, vai demonstrācijas datos ir pieejamas šīs konteineru grupas.</span><span class="sxs-lookup"><span data-stu-id="800bd-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="800bd-228">Ja tās nav pieejamas, atlasiet **Jauns**, lai tās izveidotu.</span><span class="sxs-lookup"><span data-stu-id="800bd-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="800bd-229">**Konteineru grupas ID:** *Kastes*</span><span class="sxs-lookup"><span data-stu-id="800bd-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="800bd-230">**Apraksts:** *Kastes izmēri*</span><span class="sxs-lookup"><span data-stu-id="800bd-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="800bd-231">Kopsavilkuma cilnē **Detalizēta informācija** pārliecinieties, vai pastāv tālāk norādītās rindas konteineru grupai *Kastes*.</span><span class="sxs-lookup"><span data-stu-id="800bd-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="800bd-232">Ja tās nav, atlasiet **Jauns**, lai tās pievienotu.</span><span class="sxs-lookup"><span data-stu-id="800bd-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="800bd-233">1. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-233">Line 1:</span></span>

        - <span data-ttu-id="800bd-234">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="800bd-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="800bd-235">**Konteinera veids:** *Kaste - liela*</span><span class="sxs-lookup"><span data-stu-id="800bd-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="800bd-236">**Konteinera izmantošanas procentuālā vērtība:** *100*</span><span class="sxs-lookup"><span data-stu-id="800bd-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="800bd-237">2. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-237">Line 2:</span></span>

        - <span data-ttu-id="800bd-238">**Secības numurs:** *2*</span><span class="sxs-lookup"><span data-stu-id="800bd-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="800bd-239">**Konteinera tips:** *Kaste - vidēja*</span><span class="sxs-lookup"><span data-stu-id="800bd-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="800bd-240">**Konteinera izmantošanas procentuālā vērtība:** *100*</span><span class="sxs-lookup"><span data-stu-id="800bd-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="800bd-241">3. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-241">Line 3:</span></span>

        - <span data-ttu-id="800bd-242">**Secības numurs:** *3*</span><span class="sxs-lookup"><span data-stu-id="800bd-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="800bd-243">**Konteinera veids:** *Kaste-maza*</span><span class="sxs-lookup"><span data-stu-id="800bd-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="800bd-244">**Konteinera izmantošanas procentuālā vērtība:** *100*</span><span class="sxs-lookup"><span data-stu-id="800bd-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="800bd-245">Izveidojiet jaunu konteinera būvējuma veidni</span><span class="sxs-lookup"><span data-stu-id="800bd-245">Create a new container build template</span></span>

<span data-ttu-id="800bd-246">Lai izveidotu jaunu konteinera būvējuma veidni, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="800bd-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="800bd-247">Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Konteineri** \> **Konteinera būvējuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="800bd-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="800bd-248">Atlasiet **Jauns**, lai izveidotu konteinera būvējuma veidni, kurā ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="800bd-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="800bd-249">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="800bd-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="800bd-250">**Konteinera veidnes ID:** *Kaste*</span><span class="sxs-lookup"><span data-stu-id="800bd-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="800bd-251">**Konteineru grupas ID:** *Kastes*</span><span class="sxs-lookup"><span data-stu-id="800bd-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="800bd-252">**Bāzes vaicājumu veidi:** *Pārdošanas sadalījuma rinda*</span><span class="sxs-lookup"><span data-stu-id="800bd-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="800bd-253">**Kopuma darbības kods:** *234*</span><span class="sxs-lookup"><span data-stu-id="800bd-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="800bd-254">**Atļaut izdošanas sadali:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="800bd-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="800bd-255">**Konteinera iepakošanas stratēģija:** *Iepakot tikai pašreizējā konteinerā*</span><span class="sxs-lookup"><span data-stu-id="800bd-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="800bd-256">**Iepakot pēc direktīvas vienības:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="800bd-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="800bd-257">Kamēr rinda jaunai veidnei joprojām ir atlasīta, darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="800bd-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="800bd-258">Parādās standarta vaicājumu redaktora dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="800bd-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="800bd-259">Cilnē **Kārtošana** atlasiet **Pievienot**, lai pievienotu rindu, kurai ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="800bd-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="800bd-260">**Tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="800bd-261">**Atveidotā tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="800bd-262">**Lauks:** *Pasūtījuma numurs*</span><span class="sxs-lookup"><span data-stu-id="800bd-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="800bd-263">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="800bd-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="800bd-264">Lai izvairītos no meklēšanas visos citos atvērtajos konteineros un paātrinātu procesu, vienlaikus pārbaudot vienu konteineru, izmantojiet stratēģiju *Iepakot tikai pašreizējā konteinerā* papildus šķirošanai pēc pasūtījuma numura.</span><span class="sxs-lookup"><span data-stu-id="800bd-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="800bd-265">Šī kombinācija darbosies kā darba veidnes darba pārtraukums.</span><span class="sxs-lookup"><span data-stu-id="800bd-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="800bd-266">Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="800bd-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="800bd-267">Kamēr rinda jaunai veidnei joprojām ir atlasīta, darbību rūtī atlasiet **Konteineru sajaukšanas ierobežojumi**.</span><span class="sxs-lookup"><span data-stu-id="800bd-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="800bd-268">Tagad jūs pievienosiet ierobežojumu, kas ievieto krājumus no viena pasūtījuma vienā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="800bd-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="800bd-269">Krājumi no jebkura cita pasūtījuma tiks ievietoti atsevišķā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="800bd-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="800bd-270">Atlasiet **Jauns**, lai izveidotu sajaukšanas ierobežojumu kurā ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="800bd-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="800bd-271">**Tabula:** *Pārdošanas pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="800bd-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="800bd-272">**Lauka atlase:** *SalesId* (Lauks režģī parādīsies kā *Pārdošanas pasūtījums*.)</span><span class="sxs-lookup"><span data-stu-id="800bd-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="800bd-273">Atlasiet **Labi**, lai pievienotu ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="800bd-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="800bd-274">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="800bd-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="800bd-275">Kopuma veidnes iestatīšana konteinerizācijai</span><span class="sxs-lookup"><span data-stu-id="800bd-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="800bd-276">Lai iestatītu kopuma veidni, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="800bd-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="800bd-277">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="800bd-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="800bd-278">Saraksta rūtī lauku **Kopuma veidnes tips** iestatiet vērtību *Sūtīšana*.</span><span class="sxs-lookup"><span data-stu-id="800bd-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="800bd-279">Sarakstā atlasiet veidni **63 konteinerizācija**.</span><span class="sxs-lookup"><span data-stu-id="800bd-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="800bd-280">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="800bd-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="800bd-281">Kopsavilkuma cilnē **Metodes** kolonnā **Atlasītās metodes** atrodama šāda rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="800bd-282">**Metodes nosaukums:** *konteinerizācija*</span><span class="sxs-lookup"><span data-stu-id="800bd-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="800bd-283">**Nosaukums:** *Konteinerizēšana*</span><span class="sxs-lookup"><span data-stu-id="800bd-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="800bd-284">Iestatiet lauku **Kopuma soļa kods** rindai uz *234*.</span><span class="sxs-lookup"><span data-stu-id="800bd-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="800bd-285">Darba veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="800bd-285">Set up a work template</span></span>

<span data-ttu-id="800bd-286">Lai iestatītu darba veidni, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="800bd-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="800bd-287">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="800bd-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="800bd-288">Iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="800bd-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="800bd-289">Režģī **Pārskats** atrodiet un atlasiet darba veidni, kas jāizmanto atsevišķu pasūtījumu iepakošanai vienā konteinerā.</span><span class="sxs-lookup"><span data-stu-id="800bd-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="800bd-290">Šim scenārijam atlasiet **63 izdot konteineram** veidni.</span><span class="sxs-lookup"><span data-stu-id="800bd-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="800bd-291">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="800bd-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="800bd-292">Parādās standarta vaicājumu redaktora dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="800bd-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="800bd-293">Cilnē **Kārtošana** pievienojiet tālāk minētās rindas.</span><span class="sxs-lookup"><span data-stu-id="800bd-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="800bd-294">1. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-294">Line 1:</span></span>

        - <span data-ttu-id="800bd-295">**Tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="800bd-296">**Atveidotā tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="800bd-297">**Lauks:** *Sūtījuma ID*</span><span class="sxs-lookup"><span data-stu-id="800bd-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="800bd-298">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="800bd-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="800bd-299">2. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-299">Line 2:</span></span>

        - <span data-ttu-id="800bd-300">**Tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="800bd-301">**Atveidotā tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="800bd-302">**Lauks:** *Pasūtījuma numurs*</span><span class="sxs-lookup"><span data-stu-id="800bd-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="800bd-303">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="800bd-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="800bd-304">3. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-304">Line 3:</span></span>

        - <span data-ttu-id="800bd-305">**Tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="800bd-306">**Atveidotā tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="800bd-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="800bd-307">**Lauks:** *Konteinera ID*</span><span class="sxs-lookup"><span data-stu-id="800bd-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="800bd-308">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="800bd-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="800bd-309">Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="800bd-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="800bd-310">Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?”</span><span class="sxs-lookup"><span data-stu-id="800bd-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="800bd-311">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="800bd-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="800bd-312">Lai gan joprojām ir atlasīta veidne **63 Izdot konteineram**, darbību rūtī atlasiet **Darba virsraksta pārtraukumi**.</span><span class="sxs-lookup"><span data-stu-id="800bd-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="800bd-313">Tagad tiks lietoti iestatījumi darba pārtraukumam, lai katrs pasūtījumā atvērts konteiners būtu saistīts ar vienu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="800bd-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="800bd-314">Atzīmējiet izvēles rūtiņu **Grupēt pēc šī lauka** katrai rindai lapā **Darba virsraksta pārtraukumi** (**Sūtījuma ID**, **Pasūtījuma numurs** un **Konteinera ID**).</span><span class="sxs-lookup"><span data-stu-id="800bd-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="800bd-315">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="800bd-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="800bd-316">Iestatiet sūtījumu konsolidācijas politikas</span><span class="sxs-lookup"><span data-stu-id="800bd-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="800bd-317">Lai iestatītu sūtījumu konsolidācijas politiku, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="800bd-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="800bd-318">Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.</span><span class="sxs-lookup"><span data-stu-id="800bd-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="800bd-319">Saraksta rūtī iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="800bd-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="800bd-320">Izvēlieties sarakstā politiku **Noklusējums**.</span><span class="sxs-lookup"><span data-stu-id="800bd-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="800bd-321">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="800bd-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="800bd-322">Kopsavilkuma cilnē **Konsolidācijas lauki** sarakstā **Atlasītie lauki**, atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Pasūtījuma numurs*.</span><span class="sxs-lookup"><span data-stu-id="800bd-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="800bd-323">Atlasiet pogu **Noņemt** ![Kreisā bultiņa](media/backward-button.png), lai pārvietotu lauku uz sarakstu **Atlikušie lauki**.</span><span class="sxs-lookup"><span data-stu-id="800bd-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="800bd-324">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="800bd-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="800bd-325">Iestatiet preces fiziskās dimensijas</span><span class="sxs-lookup"><span data-stu-id="800bd-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="800bd-326">Lai iestatītu fiziskas dimensijas precēm, kas tiks izmantotas šajā scenārijā, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="800bd-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="800bd-327">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="800bd-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="800bd-328">Atlasiet preci, kuras lauks **Krājuma numura** ir iestatīts uz *A0001*.</span><span class="sxs-lookup"><span data-stu-id="800bd-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="800bd-329">Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Fiziskās dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="800bd-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="800bd-330">Lapā **Fiziskās dimensijas** jums vajadzētu redzēt šādu līniju režģī:</span><span class="sxs-lookup"><span data-stu-id="800bd-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="800bd-331">**Vienība:** *gab*</span><span class="sxs-lookup"><span data-stu-id="800bd-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="800bd-332">**Bruto svars:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="800bd-333">**Platums:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="800bd-334">**Dziļums:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="800bd-335">**Augstums:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="800bd-336">**Tilpums:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="800bd-337">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="800bd-337">Close the page.</span></span>
1. <span data-ttu-id="800bd-338">Atlasiet preci, kuras lauks **Krājuma numura** ir iestatīts uz *A0002*.</span><span class="sxs-lookup"><span data-stu-id="800bd-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="800bd-339">Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Fiziskās dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="800bd-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="800bd-340">Lapā **Fiziskās dimensijas** jums vajadzētu redzēt šādu līniju režģī:</span><span class="sxs-lookup"><span data-stu-id="800bd-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="800bd-341">**Vienība:** *gab*</span><span class="sxs-lookup"><span data-stu-id="800bd-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="800bd-342">**Bruto svars:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="800bd-343">**Platums:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="800bd-344">**Dziļums:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="800bd-345">**Augstums:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="800bd-346">**Tilpums:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="800bd-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="800bd-347">1. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="800bd-347">Create sales order 1</span></span>

<span data-ttu-id="800bd-348">Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="800bd-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="800bd-349">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="800bd-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="800bd-350">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="800bd-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="800bd-351">Parādās dialoglodziņš jauna pārdošanas pasūtījuma izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="800bd-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="800bd-352">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="800bd-352">Set the following values:</span></span>

    - <span data-ttu-id="800bd-353">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="800bd-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="800bd-354">**Noliktava:** *63*</span><span class="sxs-lookup"><span data-stu-id="800bd-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="800bd-355">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="800bd-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="800bd-356">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="800bd-356">The new sales order is opened.</span></span> <span data-ttu-id="800bd-357">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet šādas pārdošanas rindas:</span><span class="sxs-lookup"><span data-stu-id="800bd-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="800bd-358">1. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-358">Line 1:</span></span>

        - <span data-ttu-id="800bd-359">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="800bd-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="800bd-360">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="800bd-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="800bd-361">2. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-361">Line 2:</span></span>

        - <span data-ttu-id="800bd-362">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="800bd-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="800bd-363">**Daudzums:** *2*</span><span class="sxs-lookup"><span data-stu-id="800bd-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="800bd-364">Atlasiet pirmo rindu un pēc tam atlasiet **Krājumi \> Rezervēšana**.</span><span class="sxs-lookup"><span data-stu-id="800bd-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="800bd-365">Lapā **Rezervācija** atlasiet **Rezervēt vietu**.</span><span class="sxs-lookup"><span data-stu-id="800bd-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="800bd-366">Tad aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="800bd-366">Then close the page.</span></span>
1. <span data-ttu-id="800bd-367">Atkārtojiet iepriekšējās divas darbības otrajai rindai.</span><span class="sxs-lookup"><span data-stu-id="800bd-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="800bd-368">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="800bd-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="800bd-369">2. pārdošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="800bd-369">Create sales order 2</span></span>

<span data-ttu-id="800bd-370">Lai izveidotu otru pārdošanas pasūtījumu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="800bd-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="800bd-371">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="800bd-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="800bd-372">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="800bd-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="800bd-373">Parādās dialoglodziņš jauna pārdošanas pasūtījuma izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="800bd-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="800bd-374">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="800bd-374">Set the following values:</span></span>

    - <span data-ttu-id="800bd-375">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="800bd-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="800bd-376">**Noliktava:** *63*</span><span class="sxs-lookup"><span data-stu-id="800bd-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="800bd-377">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="800bd-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="800bd-378">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="800bd-378">The new sales order is opened.</span></span> <span data-ttu-id="800bd-379">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet šādas pārdošanas rindas:</span><span class="sxs-lookup"><span data-stu-id="800bd-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="800bd-380">1. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-380">Line 1:</span></span>

        - <span data-ttu-id="800bd-381">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="800bd-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="800bd-382">**Daudzums:** *4*</span><span class="sxs-lookup"><span data-stu-id="800bd-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="800bd-383">2. rinda:</span><span class="sxs-lookup"><span data-stu-id="800bd-383">Line 2:</span></span>

        - <span data-ttu-id="800bd-384">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="800bd-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="800bd-385">**Daudzums:** *4*</span><span class="sxs-lookup"><span data-stu-id="800bd-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="800bd-386">Atlasiet pirmo rindu un pēc tam atlasiet **Krājumi \> Rezervēšana**.</span><span class="sxs-lookup"><span data-stu-id="800bd-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="800bd-387">Lapā **Rezervācija** atlasiet **Rezervēt vietu**.</span><span class="sxs-lookup"><span data-stu-id="800bd-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="800bd-388">Tad aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="800bd-388">Then close the page.</span></span>
1. <span data-ttu-id="800bd-389">Atkārtojiet iepriekšējās divas darbības otrajai rindai.</span><span class="sxs-lookup"><span data-stu-id="800bd-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="800bd-390">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="800bd-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="800bd-391">Kravas izveide</span><span class="sxs-lookup"><span data-stu-id="800bd-391">Create the load</span></span>

<span data-ttu-id="800bd-392">Lai izveidotu kravu katram pasūtījumam, kuru izveidojāt šim scenārijam, un pēc tam izlaistu to noliktavā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="800bd-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="800bd-393">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="800bd-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="800bd-394">Cilnē **Pārdošanas rindas** meklējiet un atlasiet visas pārdošanas pasūtījuma rindas šim scenārijam izveidotajiem pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="800bd-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="800bd-395">Darbību rūtī cilnē **Piedāvājums un pieprasījums** grupā **Pievienot**, atlasiet **Jaunai kravai**.</span><span class="sxs-lookup"><span data-stu-id="800bd-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="800bd-396">Atlasītās pasūtījuma rindas tiek pievienotas jaunai kravai.</span><span class="sxs-lookup"><span data-stu-id="800bd-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="800bd-397">Dialoglodziņā **Noslodzes veidnes piešķire** laukā **Noslodzes veidnes ID** atlasiet noslodzes veidni, piemēram, *40' konteiners*.</span><span class="sxs-lookup"><span data-stu-id="800bd-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="800bd-398">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="800bd-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="800bd-399">Sadaļā **Noslodzes** meklējiet un atlasiet tikko izveidoto noslodzi.</span><span class="sxs-lookup"><span data-stu-id="800bd-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="800bd-400">Atlasiet **Izlaist \> Pārvietot uz noliktavu**.</span><span class="sxs-lookup"><span data-stu-id="800bd-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="800bd-401">Dialoglodziņā **Pārvietot uz noliktavu** atlasiet **Labi**, lai pārvietotu atlasīto noslodzi uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="800bd-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="800bd-402">Pārbaudīt sūtījumus un konteinerus</span><span class="sxs-lookup"><span data-stu-id="800bd-402">Verify the shipments and containers</span></span>

<span data-ttu-id="800bd-403">Šī procedūra ļauj pārbaudīt izveidotās kravas.</span><span class="sxs-lookup"><span data-stu-id="800bd-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="800bd-404">Izmantojiet to, lai pārskatītu pasūtījumu, ko izveidojāt šim scenārijam, lai pārliecinātos, ka esat ieguvis sagaidāmos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="800bd-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="800bd-405">Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="800bd-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="800bd-406">Atrodiet un atlasiet sūtījumu, kas tika izveidots tikko izlaistai kravai.</span><span class="sxs-lookup"><span data-stu-id="800bd-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="800bd-407">Darbības rūtī, cilnē **Transports** atlasiet **Skatīt konteinerus**.</span><span class="sxs-lookup"><span data-stu-id="800bd-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="800bd-408">Apstipriniet, ka krājumi no pārdošanas pasūtījumiem ir konteineros divos dažādos konteineros.</span><span class="sxs-lookup"><span data-stu-id="800bd-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="800bd-409">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="800bd-409">Additional resources</span></span>

- [<span data-ttu-id="800bd-410">Konteinerizēšana</span><span class="sxs-lookup"><span data-stu-id="800bd-410">Containerization</span></span>](wave-containerization.md)
