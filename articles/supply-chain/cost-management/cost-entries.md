---
title: Izmaksu ieraksti
description: Šajā rakstā ir sniegta informācija par izmaksu ierakstiem un to, kad tie tiek izveidoti. Izmaksu ieraksts ir ieraksts, kas reģistrē noteikta notikuma daudzumu un izmaksas.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ddd263852fc328756a6dc06bc3f02c661cbd40f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228639"
---
# <a name="cost-entries"></a><span data-ttu-id="48dd4-104">Izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="48dd4-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48dd4-105">Šajā rakstā ir sniegta informācija par izmaksu ierakstiem un to, kad tie tiek izveidoti.</span><span class="sxs-lookup"><span data-stu-id="48dd4-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="48dd4-106">Izmaksu ieraksts ir ieraksts, kas reģistrē noteikta notikuma daudzumu un izmaksas.</span><span class="sxs-lookup"><span data-stu-id="48dd4-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="48dd4-107">Izmaksu ieraksti ir tādu krājumu transakciju apkopojumi, kas ir reģistrētas aktīvajās finanšu krājumu dimensijās.</span><span class="sxs-lookup"><span data-stu-id="48dd4-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="48dd4-108">Piemēri</span><span class="sxs-lookup"><span data-stu-id="48dd4-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="48dd4-109">1. piemērs: netiek izveidoti izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="48dd4-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="48dd4-110">Tiek reģistrēts pārsūtīšanas žurnāla notikums.</span><span class="sxs-lookup"><span data-stu-id="48dd4-110">A transfer journal event is registered.</span></span> <span data-ttu-id="48dd4-111">Notikuma ietvaros viens krājuma A gabals tiek pārsūtīts no novietojuma A uz novietojumu B. Krājumu dimensija Novietojums nav uzskatāma par daļu no izmaksu objekta.</span><span class="sxs-lookup"><span data-stu-id="48dd4-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="48dd4-112">Tādējādi notikuma ietvaros tiek izveidotas divas krājumu transakcijas un netiek izveidoti izmaksu ieraksti.</span><span class="sxs-lookup"><span data-stu-id="48dd4-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="48dd4-113">2. piemērs: tiek izveidoti izmaksu ieraksti</span><span class="sxs-lookup"><span data-stu-id="48dd4-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="48dd4-114">Tiek reģistrēts pārsūtīšanas žurnāla notikums.</span><span class="sxs-lookup"><span data-stu-id="48dd4-114">A transfer journal event is registered.</span></span> <span data-ttu-id="48dd4-115">Notikuma ietvaros viens krājuma A gabals tiek pārsūtīts no 1. vietas uz 2. vietu.</span><span class="sxs-lookup"><span data-stu-id="48dd4-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="48dd4-116">Krājumu dimensija Vieta tiek uzskatīta par daļu no izmaksu objekta.</span><span class="sxs-lookup"><span data-stu-id="48dd4-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="48dd4-117">Tādējādi notikuma ietvaros tiek izveidotas divas krājumu transakcijas un divi izmaksu ieraksti.</span><span class="sxs-lookup"><span data-stu-id="48dd4-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="48dd4-118">3. piemērs: tiek izveidots viens izmaksu ieraksts</span><span class="sxs-lookup"><span data-stu-id="48dd4-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="48dd4-119">Pirkšanas pasūtījumam tiek reģistrēts produktu ieejas plūsmas notikums.</span><span class="sxs-lookup"><span data-stu-id="48dd4-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="48dd4-120">Notikuma ietvaros tiek reģistrēti 100 krājuma A gabali, kuru vienības izmaksas ir 10,00 ASV dolāri (USD).</span><span class="sxs-lookup"><span data-stu-id="48dd4-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="48dd4-121">Tā kā krājumam A tiek izmantots sērijas numuru, lai izsekotu krājumu vadības mērķi, katram saņemtajam krājumam tiek izveidots unikāls sērijas numurs.</span><span class="sxs-lookup"><span data-stu-id="48dd4-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="48dd4-122">Tādējādi notikuma ietvaros tiek izveidotas 100 krājumu transakcijas un viens izmaksu ieraksts.</span><span class="sxs-lookup"><span data-stu-id="48dd4-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="48dd4-123">Izmaksu ierakstu lapa</span><span class="sxs-lookup"><span data-stu-id="48dd4-123">Cost entries page</span></span>
<span data-ttu-id="48dd4-124">Jaunā lapa **Izmaksu ieraksti** ļauj skatīt un kontrolēt daudzuma un izmaksu reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="48dd4-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="48dd4-125">Šī lapa papildina lapas **Krājumu darbība** un **Krājumu nosegšana**.</span><span class="sxs-lookup"><span data-stu-id="48dd4-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="48dd4-126">Notikuma ieraksti tiek reģistrēti hronoloģiskā secībā.</span><span class="sxs-lookup"><span data-stu-id="48dd4-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="48dd4-127">Tādējādi var ātri atrast un kontrolēt uzkrātās izmaksas noteiktam notikumam vai visiem notikumiem, kas ir saistīti ar dokumentu.</span><span class="sxs-lookup"><span data-stu-id="48dd4-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="48dd4-128">Tālāk minēts piemērs:</span><span class="sxs-lookup"><span data-stu-id="48dd4-128">Here is an example:</span></span>

-   <span data-ttu-id="48dd4-129">Krājumam A tiek reģistrēts produktu ieejas plūsmas notikums. Ir saņemti 100 gabali, kuru vienības izmaksas ir 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="48dd4-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="48dd4-130">Dažas dienas pēc rēķina notikuma reģistrēšanas, izmaksas palielinās līdz 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="48dd4-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="48dd4-131">Tādējādi kopsumma ir 1100 USD.</span><span class="sxs-lookup"><span data-stu-id="48dd4-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="48dd4-132">Tiek izveidots otrais dokuments, lai uzskaitītu 100 USD starpību.</span><span class="sxs-lookup"><span data-stu-id="48dd4-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="48dd4-133">Dažas dienas vēlāk pirkšanas pasūtījumā tiek reģistrēta papildmaksa 15,00 USD transportēšanas izmaksu segšanai.</span><span class="sxs-lookup"><span data-stu-id="48dd4-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="48dd4-134">Dokuments</span><span class="sxs-lookup"><span data-stu-id="48dd4-134">Voucher</span></span> | <span data-ttu-id="48dd4-135">Datums</span><span class="sxs-lookup"><span data-stu-id="48dd4-135">Date</span></span>       | <span data-ttu-id="48dd4-136">Atsauce</span><span class="sxs-lookup"><span data-stu-id="48dd4-136">Reference</span></span>      | <span data-ttu-id="48dd4-137">Skaits</span><span class="sxs-lookup"><span data-stu-id="48dd4-137">Number</span></span> | <span data-ttu-id="48dd4-138">Laidiena ID</span><span class="sxs-lookup"><span data-stu-id="48dd4-138">Lot ID</span></span>  | <span data-ttu-id="48dd4-139">Daudzums</span><span class="sxs-lookup"><span data-stu-id="48dd4-139">Quantity</span></span> | <span data-ttu-id="48dd4-140">Summa</span><span class="sxs-lookup"><span data-stu-id="48dd4-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="48dd4-141">00001</span><span class="sxs-lookup"><span data-stu-id="48dd4-141">00001</span></span>   | <span data-ttu-id="48dd4-142">01.01.2015</span><span class="sxs-lookup"><span data-stu-id="48dd4-142">01-01-2015</span></span> | <span data-ttu-id="48dd4-143">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="48dd4-143">Purchase order</span></span> | <span data-ttu-id="48dd4-144">100001</span><span class="sxs-lookup"><span data-stu-id="48dd4-144">100001</span></span> | <span data-ttu-id="48dd4-145">0000101</span><span class="sxs-lookup"><span data-stu-id="48dd4-145">0000101</span></span> | <span data-ttu-id="48dd4-146">100,00</span><span class="sxs-lookup"><span data-stu-id="48dd4-146">100.00</span></span>   | <span data-ttu-id="48dd4-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="48dd4-147">1000.00</span></span> |
| <span data-ttu-id="48dd4-148">00002</span><span class="sxs-lookup"><span data-stu-id="48dd4-148">00002</span></span>   | <span data-ttu-id="48dd4-149">20.01.2015</span><span class="sxs-lookup"><span data-stu-id="48dd4-149">20-01-2015</span></span> | <span data-ttu-id="48dd4-150">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="48dd4-150">Purchase order</span></span> | <span data-ttu-id="48dd4-151">100001</span><span class="sxs-lookup"><span data-stu-id="48dd4-151">100001</span></span> | <span data-ttu-id="48dd4-152">0000101</span><span class="sxs-lookup"><span data-stu-id="48dd4-152">0000101</span></span> |          | <span data-ttu-id="48dd4-153">100,00</span><span class="sxs-lookup"><span data-stu-id="48dd4-153">100.00</span></span>  |
| <span data-ttu-id="48dd4-154">00003</span><span class="sxs-lookup"><span data-stu-id="48dd4-154">00003</span></span>   | <span data-ttu-id="48dd4-155">31.01.2015</span><span class="sxs-lookup"><span data-stu-id="48dd4-155">31-01-2015</span></span> | <span data-ttu-id="48dd4-156">Korekcija</span><span class="sxs-lookup"><span data-stu-id="48dd4-156">Adjustment</span></span>     | <span data-ttu-id="48dd4-157">100001</span><span class="sxs-lookup"><span data-stu-id="48dd4-157">100001</span></span> | <span data-ttu-id="48dd4-158">0000101</span><span class="sxs-lookup"><span data-stu-id="48dd4-158">0000101</span></span> |          | <span data-ttu-id="48dd4-159">15,00</span><span class="sxs-lookup"><span data-stu-id="48dd4-159">15.00</span></span>   |

<span data-ttu-id="48dd4-160">Lapa **Izmaksu ieraksti** ļauj veikt filtrēšanu pēc dokumenta ID un dokumenta datuma.</span><span class="sxs-lookup"><span data-stu-id="48dd4-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="48dd4-161">Izmaksu ieraksti ir pieejami tikai [izmaksu objektiem](cost-object.md) vai izlaistajām precēm.</span><span class="sxs-lookup"><span data-stu-id="48dd4-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="48dd4-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="48dd4-162">Additional resources</span></span>
--------

[<span data-ttu-id="48dd4-163">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="48dd4-163">Cost objects</span></span>](cost-object.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]