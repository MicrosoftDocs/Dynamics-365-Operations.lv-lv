---
title: Pirkšanas pieprasījumi
description: Šajā tēmā ir aprakstīts, kā plānošanas optimizācijā tiek atbalstīti pirkšanas pieprasījumi.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501082"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="d7669-103">Pirkšanas pieprasījumi</span><span class="sxs-lookup"><span data-stu-id="d7669-103">Purchase requisitions</span></span>

<span data-ttu-id="d7669-104">Vispārējā plānošana var papildināt apstiprinātos pirkšanas pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="d7669-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="d7669-105">Tādēļ, lai segtu pirkšanas pieprasījumus, lietotājiem nav jāizmanto darbplūsma pirkšanas pasūtījumu izveidei.</span><span class="sxs-lookup"><span data-stu-id="d7669-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="d7669-106">Tā vietā pirkšanas pieprasījumus var segt vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="d7669-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="d7669-107">Šīs funkcionalitātes dēļ pirkšanas pieprasījums var izveidot pirkšanas pasūtījumu, pārsūtīšanas pasūtījumu vai ražošanas pasūtījumu atkarībā no **Plānotā pasūtījuma tipa** vērtības, kas iestatīta saistītajam produktam.</span><span class="sxs-lookup"><span data-stu-id="d7669-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="d7669-108">Iestatīt vispārējos plānus, lai iekļautu pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="d7669-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="d7669-109">Lai vispārējā plāna seguma aprēķina laikā iekļautu pieprasījumus, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="d7669-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="d7669-110">Dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plāni** \> **Vispārējie plāni**.</span><span class="sxs-lookup"><span data-stu-id="d7669-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="d7669-111">Izveidojiet vai atlasiet vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="d7669-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="d7669-112">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Izmantot noklusējuma datus** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="d7669-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="d7669-113">Atkārtojiet 2. un 3. soli katram papildu vispārējam plānam, kurā vēlaties iekļaut pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="d7669-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="d7669-114">Apstiprināto pieprasījumu periods</span><span class="sxs-lookup"><span data-stu-id="d7669-114">Approved requisitions time fence</span></span>

<span data-ttu-id="d7669-115">*Apstiprināto pieprasījumu laika periods* izveido, cik tālu (dienās) vispārējais plāns ietvers pieprasījumu no apstiprinātiem papildināšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="d7669-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="d7669-116">Varat iestatīt apstiprināto pieprasījumu laika periodu gan vajadzību grupas līmenī, gan vispārējā plāna līmenī.</span><span class="sxs-lookup"><span data-stu-id="d7669-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="d7669-117">Vajadzības perioda iestatīšana vajadzību grupai</span><span class="sxs-lookup"><span data-stu-id="d7669-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="d7669-118">Dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Vajadzība** \> **Vajadzību grupas**.</span><span class="sxs-lookup"><span data-stu-id="d7669-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="d7669-119">Izveidojiet vai atlasiet vajadzību grupu.</span><span class="sxs-lookup"><span data-stu-id="d7669-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="d7669-120">Kopsavilkuma cilnē **Citi** iestatiet lauku **Apstiprināts pieprasījumu periods (dienas)** uz dienu skaitu, ko iekļaut laika periodā.</span><span class="sxs-lookup"><span data-stu-id="d7669-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="d7669-121">Atkārtojiet 2. un 3. soli katrai papildu vajadzību grupai, kur vēlaties iestatīt apstiprināto pieprasījumu periodu.</span><span class="sxs-lookup"><span data-stu-id="d7669-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="d7669-122">Apstiprināto pieprasījumu laika perioda iestatīšana atsevišķiem vispārējiem plāniem</span><span class="sxs-lookup"><span data-stu-id="d7669-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="d7669-123">Kad iestatāt apstiprinātu pieprasījumu periodu atsevišķam vispārējai plānam, iestatījums ignorē laika perioda iestatījumu jebkurai piemērojamai vajadzību grupai.</span><span class="sxs-lookup"><span data-stu-id="d7669-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="d7669-124">Dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plāni** \> **Vispārējie plāni**.</span><span class="sxs-lookup"><span data-stu-id="d7669-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="d7669-125">Izveidojiet vai atlasiet vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="d7669-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="d7669-126">Kopsavilkuma cilnē **Citi** iestatiet lauku **Apstiprināto pieprasījumu periods (dienas)** uz dienu skaitu, ko iekļaut laika periodā.</span><span class="sxs-lookup"><span data-stu-id="d7669-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="d7669-127">Atkārtojiet 2. un 3. soli katrai papildu vajadzību grupai, kur vēlaties iestatīt apstiprināto pieprasījumu periodu.</span><span class="sxs-lookup"><span data-stu-id="d7669-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7669-128">**Drīzumā:** Apstiprinātie pieprasījumu laika periodi vēl nav atbalstīti plānošanas optimizēšanai.</span><span class="sxs-lookup"><span data-stu-id="d7669-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="d7669-129">Kamēr tās netiek atbalstītas, visas laukā **Apstiprināto pieprasījumu periods (dienas)** ievadītās vērtības tiks ignorētas.</span><span class="sxs-lookup"><span data-stu-id="d7669-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="d7669-130">Neatkarīga piegāde, neņemot vērā vajadzības kodu</span><span class="sxs-lookup"><span data-stu-id="d7669-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="d7669-131">Pirkšanas pieprasījumus vienmēr sedz neatkarīgi plānotie pasūtījumi, neatkarīgi no vajadzību koda.</span><span class="sxs-lookup"><span data-stu-id="d7669-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="d7669-132">Šī darbība nodrošina skaidru izsekošanu un darbplūsmas starp pirkšanas pieprasījumiem un papildināšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d7669-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="d7669-133">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="d7669-133">Example 1</span></span>

<span data-ttu-id="d7669-134">Prece ir iestatīta tā, lai tai būtu **Vajadzību koda** vērtība *Min./maks.* Tai ir šādi krājumu un pieprasījumu statusi:</span><span class="sxs-lookup"><span data-stu-id="d7669-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="d7669-135">Rīcībā esošo krājumu saraksts = 10.</span><span class="sxs-lookup"><span data-stu-id="d7669-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="d7669-136">Minimālais krājumu daudzums = 15.</span><span class="sxs-lookup"><span data-stu-id="d7669-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="d7669-137">Maksimālais krājumu daudzums = 20.</span><span class="sxs-lookup"><span data-stu-id="d7669-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="d7669-138">Eksistē pirkšanas pieprasījums vienam gabalam.</span><span class="sxs-lookup"><span data-stu-id="d7669-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="d7669-139">Tā pieprasītais datums ir šodien.</span><span class="sxs-lookup"><span data-stu-id="d7669-139">It has a requested date of today.</span></span>

<span data-ttu-id="d7669-140">Kad tiek palaista vispārējā plānošana, tiek izveidoti divi plānotie pasūtījumi: viens 10 gabaliem, lai papildinātu krājumus līdz maksimālajam daudzumam, un viens vienam gabalam, lai papildinātu pirkšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="d7669-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="d7669-141">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="d7669-141">Example 2</span></span>

<span data-ttu-id="d7669-142">Prece ir iestatīta tā, lai tai būtu **Vajadzību koda** vērtība *Min./maks.* Tai ir šādi krājumu un pieprasījumu statusi:</span><span class="sxs-lookup"><span data-stu-id="d7669-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="d7669-143">Rīcībā esošo krājumu saraksts = 17.</span><span class="sxs-lookup"><span data-stu-id="d7669-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="d7669-144">Minimālais krājumu daudzums = 15.</span><span class="sxs-lookup"><span data-stu-id="d7669-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="d7669-145">Maksimālais krājumu daudzums = 20.</span><span class="sxs-lookup"><span data-stu-id="d7669-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="d7669-146">Eksistē pirkšanas pieprasījums vienam gabalam.</span><span class="sxs-lookup"><span data-stu-id="d7669-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="d7669-147">Tā pieprasītais datums ir šodien.</span><span class="sxs-lookup"><span data-stu-id="d7669-147">It has a requested date of today.</span></span>

<span data-ttu-id="d7669-148">Kad tiek palaista vispārējā plānošana, pirkšanas pieprasījuma papildināšanai tiek izveidots viens plānotais pasūtījums vienam gabalam.</span><span class="sxs-lookup"><span data-stu-id="d7669-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="d7669-149">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="d7669-149">Example 3</span></span>

<span data-ttu-id="d7669-150">Prece ir iestatīta tā, lai tās *Periods* ir **Vajadzību koda** vērtība un septiņu dienu perioda ilgums.</span><span class="sxs-lookup"><span data-stu-id="d7669-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="d7669-151">Tai ir šādi krājumi, pārdošanas pasūtījumi un pieprasījumu statusi:</span><span class="sxs-lookup"><span data-stu-id="d7669-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="d7669-152">Rīcībā esošo krājumu saraksts = 0.</span><span class="sxs-lookup"><span data-stu-id="d7669-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="d7669-153">Pastāv pārdošanas pasūtījums pieciem gabaliem.</span><span class="sxs-lookup"><span data-stu-id="d7669-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="d7669-154">Tam paredzamais nosūtīšanas datums ir šodiena, plus viena diena.</span><span class="sxs-lookup"><span data-stu-id="d7669-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="d7669-155">Eksistē pirkšanas pieprasījums trim gabaliem.</span><span class="sxs-lookup"><span data-stu-id="d7669-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="d7669-156">Tā pieprasītais datums ir šodiena un vēl trīs dienas.</span><span class="sxs-lookup"><span data-stu-id="d7669-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="d7669-157">Kad tiek palaista vispārējā plānošana, tiek izveidoti divi plānotie pasūtījumi: viens trim gabaliem, lai papildinātu krājumus līdz maksimālajam daudzumam, un viens pieciem gabalam, lai papildinātu pirkšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="d7669-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="d7669-158">Kad plānotais pasūtījums, kas ir piesaistīts pirkšanas pieprasījumam, ir apstiprināts, plānošanas programma uztur piesaisti pirkšanas pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="d7669-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="d7669-159">Ja pēc tam apstiprinātajam pasūtījumam trūkst daudzuma, kas ir nepieciešams pirkšanas pieprasījuma izpildei, sistēma izveidos jaunu plānoto pasūtījumu starpībai.</span><span class="sxs-lookup"><span data-stu-id="d7669-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="d7669-160">Vispārīgāku informāciju par pirkšanas pasūtījumiem skatiet rakstā [Pirkšanas pasūtījuma pārskats](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d7669-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]