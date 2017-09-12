---
title: "Materiālu patēriņa reģistrēšana, izmantojot mobilo ierīci"
description: "Šajā tēmā ir aprakstītas darbplūsmas, kas ļauj reģistrēt izejmateriālu patēriņu ražošanas procesā, izmantojot rokas ierīci."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: lv-lv
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="d761b-103">Materiālu patēriņa reģistrēšana, izmantojot mobilo ierīci</span><span class="sxs-lookup"><span data-stu-id="d761b-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="d761b-104">Šajā tēmā ir aprakstītas darbplūsmas, kas ļauj reģistrēt izejmateriālu patēriņu ražošanas procesā, izmantojot rokas ierīci.</span><span class="sxs-lookup"><span data-stu-id="d761b-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="d761b-105">Ievads</span><span class="sxs-lookup"><span data-stu-id="d761b-105">Introduction</span></span>
------------

<span data-ttu-id="d761b-106">Šī darbplūsma ir nepieciešama, ja ir stingra prasība pēc materiālu izsekojamības.</span><span class="sxs-lookup"><span data-stu-id="d761b-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="d761b-107">Šādos gadījumos, lai uzturētu materiālu izsekojamību, jāziņo par precīzu patēriņam paredzēto laiku un daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d761b-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="d761b-108">Šo procesu var redzēt pretēji sākotnējām vai atgriezeniskajām norakstīšanas operācijām, ja pastāv nobīde starp reģistrācijas laiku un laiku, kad notiek faktiskais patēriņš.</span><span class="sxs-lookup"><span data-stu-id="d761b-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="d761b-109">Tas izskaidro, kāpēc automātiskā patēriņa stratēģiju nevar izmantot dažiem materiāliem ar izsekojamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="d761b-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="d761b-110">Aplūkosim vienkāršu scenāriju, kas skaidro, kā iestatīt darbplūsmu, lai aktivizētu izejmateriālu patēriņa reģistrāciju ražošanas vajadzībām, izmantojot rokas ierīci.</span><span class="sxs-lookup"><span data-stu-id="d761b-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="d761b-111">Detalizēta informācija par scenāriju</span><span class="sxs-lookup"><span data-stu-id="d761b-111">Scenario details</span></span>

<span data-ttu-id="d761b-112">Nepārtrauktā ražošanas procesā (5) tiek patērēts no partijas atkarīgs izejmateriāls RM-100.</span><span class="sxs-lookup"><span data-stu-id="d761b-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="d761b-113">Materiāls ir rīcībā esošos atrašanās vietā Bulk-001 (1) ar noliktavas vienību PL-1 un divām partijām B1 un B2, abās ar daudzumu 100 mārciņas.</span><span class="sxs-lookup"><span data-stu-id="d761b-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="d761b-114">RM 100 noliktavas darbs (2) tiek izlaists un apstrādāts, un materiāli tiek izdoti no Bulk-001 ražošanas ievades atrašanās vietā PIL-01 (3), kas tiek definēta kā no noliktavas vienības neatkarīga.</span><span class="sxs-lookup"><span data-stu-id="d761b-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="d761b-115">Mašīnu operators nosver materiālus no ražošanas ievades atrašanās vieta (3) un reģistrē svaru un partijas numuru kā patērētu (4).</span><span class="sxs-lookup"><span data-stu-id="d761b-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="d761b-116">No ražošanas ievades vietas daļu materiālu manuāli pievieno ražošanas procesam noteiktajos laika intervālos.</span><span class="sxs-lookup"><span data-stu-id="d761b-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="d761b-117">Kad mašīnas operators pievieno materiālu, tas tiek novērtēts uz svariem, un tiek reģistrēts partijas numurs.</span><span class="sxs-lookup"><span data-stu-id="d761b-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="d761b-118">Darbplūsmas iestatīšana, lai reģistrētu patēriņu, izmantojot rokas ierīci</span><span class="sxs-lookup"><span data-stu-id="d761b-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="d761b-119">Izveidojiet pabeigtu derīgu preci, FG 100, ar materiālu krājumu, kuram ir no partijas atkarīgs izejmateriāls RM-100.</span><span class="sxs-lookup"><span data-stu-id="d761b-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="d761b-120">Pievienojiet divas partijas, B1 un B2, no RM-100 ar daudzumu 100 atrašanās vietai: Bulk-001 noliktavas vienībai: PL-1.</span><span class="sxs-lookup"><span data-stu-id="d761b-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="d761b-121">Materiālu komplekta rindā esošais tīrīšanas princips attiecībā uz RM-100 tiek iestatīts uz **Manuāls**.</span><span class="sxs-lookup"><span data-stu-id="d761b-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="d761b-122">Iestatiet ražošanas ievades vietu PIL-01.</span><span class="sxs-lookup"><span data-stu-id="d761b-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="d761b-123">To var izdarīt, atlasot šo atrašanās vietu kā noklusējuma ražošanas ievades vietu noliktavā 51.</span><span class="sxs-lookup"><span data-stu-id="d761b-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="d761b-124">Jaunas mobilās ierīces izvēlnes elementa izveide:</span><span class="sxs-lookup"><span data-stu-id="d761b-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="d761b-125">**Izvēlnes vienuma nosaukums** — reģistrē materiālu patēriņu.</span><span class="sxs-lookup"><span data-stu-id="d761b-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="d761b-126">**Virsraksts** — reģistrē materiālu patēriņu.</span><span class="sxs-lookup"><span data-stu-id="d761b-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="d761b-127">**Režīms** — netiešs.</span><span class="sxs-lookup"><span data-stu-id="d761b-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="d761b-128">**Aktivitātes kods** — reģistrē materiālu patēriņu.</span><span class="sxs-lookup"><span data-stu-id="d761b-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="d761b-129">Pievienojiet ierīces izvēlnei elementu **Mobilā ražošana**.</span><span class="sxs-lookup"><span data-stu-id="d761b-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="d761b-130">Izveidojiet ražošanas pasūtījumu galaproduktam:</span><span class="sxs-lookup"><span data-stu-id="d761b-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="d761b-131">**Krājuma numurs** — FG-100</span><span class="sxs-lookup"><span data-stu-id="d761b-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="d761b-132">**Vieta** — 5</span><span class="sxs-lookup"><span data-stu-id="d761b-132">**Site** - 5</span></span> 
-    <span data-ttu-id="d761b-133">**Noliktava** — 51</span><span class="sxs-lookup"><span data-stu-id="d761b-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="d761b-134">**Daudzums** — 150</span><span class="sxs-lookup"><span data-stu-id="d761b-134">**Quantity** - 150</span></span>

<span data-ttu-id="d761b-135">Ražošanas pasūtījums ir **Novērtēts** un **Izlaists** un noliktavas darbs tiek izveidots.</span><span class="sxs-lookup"><span data-stu-id="d761b-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="d761b-136">Pabeidziet darbu, izmantojot izejmateriālu izdošanas rokas ierīcei darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="d761b-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="d761b-137">Tas izdos materiālu no lielapjoma atrašanās vietas uz ražošanas ievades vietu PIL-01.</span><span class="sxs-lookup"><span data-stu-id="d761b-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="d761b-138">Kad darbs pabeigts, materiālu statuss ir **Izdots ražošanas ievades vietā**.</span><span class="sxs-lookup"><span data-stu-id="d761b-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="d761b-139">Statuss pēc darba apstrādes var būt vai nu **Izdots** vai **Rezervēts fiziski**.</span><span class="sxs-lookup"><span data-stu-id="d761b-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="d761b-140">Tas ir konfigurēta ar parametru **Izejas plūsmas statuss pēc izvietošanas noliktavas veidlapas**.</span><span class="sxs-lookup"><span data-stu-id="d761b-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="d761b-141">Sāciet ražošanas pasūtījumu no klienta vai no rokas ierīces, izmantojot izvēlnes elementu **Ražošanas sākums**.</span><span class="sxs-lookup"><span data-stu-id="d761b-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="d761b-142">Pēc tam, kad ražošanas pasūtījums ir sākts, materiālu patēriņu var reģistrēt ar rokas ierīces darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="d761b-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="d761b-143">Sāciet ar 25 mārciņu partijas B1 patēriņa reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="d761b-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="d761b-144">Atlasiet rokas ierīces izvēlnes elementu **Reģistrēt materiālu** **patēriņu** un ievadiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="d761b-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="d761b-145">Ražošanas pasūtījuma numurs.</span><span class="sxs-lookup"><span data-stu-id="d761b-145">The production order number.</span></span> 
-    <span data-ttu-id="d761b-146">Atrašanās vieta, kurā materiāls tiks patērēts; šajā gadījumā PIL-01.</span><span class="sxs-lookup"><span data-stu-id="d761b-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="d761b-147">Krājuma numurs: RM-100.</span><span class="sxs-lookup"><span data-stu-id="d761b-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="d761b-148">Partijas numurs: B1.</span><span class="sxs-lookup"><span data-stu-id="d761b-148">Batch number B1.</span></span> 
-    <span data-ttu-id="d761b-149">Daudzums: 25.</span><span class="sxs-lookup"><span data-stu-id="d761b-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="d761b-150">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d761b-150">Select **OK**.</span></span>

<span data-ttu-id="d761b-151">Ņemiet vērā! Displejā tiks parādīts ziņojums “Žurnāla rinda ir izveidota”.</span><span class="sxs-lookup"><span data-stu-id="d761b-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="d761b-152">Ražošanas pasūtījumā ir atvērts žurnāls ar veidu **Ražošanas izdošanas saraksts** krājumam ar numuru RM-100 un partijas numuru B1.</span><span class="sxs-lookup"><span data-stu-id="d761b-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="d761b-153">Tagad varat izvēlēties turpināt savu reģistrāciju, piemēram, partijas numura B2, un ikreiz, kad atlasāt **Labi**, atvērtajam žurnālam tiek pievienota jauna žurnāla rinda.</span><span class="sxs-lookup"><span data-stu-id="d761b-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="d761b-154">Kad esat pabeidzis savu reģistrāciju, atlasiet **Gatavs**, lai grāmatotu žurnālu un beigu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="d761b-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="d761b-155">Papildu piebilde</span><span class="sxs-lookup"><span data-stu-id="d761b-155">Additional comments</span></span> 

-   <span data-ttu-id="d761b-156">Ja lietotājs atceļ darbplūsmu pēc žurnāla rindas izveides, žurnālam ir statuss Negrāmatots, bet, ja lietotājs vēlāk izmanto darbplūsmu tam pašam ražošanas pasūtījumam, tad rindas tiek pievienotas atvērtajam žurnālam, nevis jaunajam žurnālam.</span><span class="sxs-lookup"><span data-stu-id="d761b-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="d761b-157">Jauna darbplūsma atbalsta arī sērijas numuru reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="d761b-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="d761b-158">Var reģistrēt tikai to krājuma numuru, kas ir definēta materiālu komplektā vai atlasītā ražošanas pasūtījuma vai partijas pasūtījuma formulā.</span><span class="sxs-lookup"><span data-stu-id="d761b-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="d761b-159">Materiālu var pārmērīgi patērēt.</span><span class="sxs-lookup"><span data-stu-id="d761b-159">Material can be overconsumed.</span></span> <span data-ttu-id="d761b-160">Piemēram, ja tika novērtēts materiāla patēriņš 100 mārciņas, tad tas var tikt pārmērīgi patērēts ar daudzumu, piemēram, 105 mārciņas.</span><span class="sxs-lookup"><span data-stu-id="d761b-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



