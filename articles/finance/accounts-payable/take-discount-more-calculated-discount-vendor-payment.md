---
title: Vairāk par kreditora maksājumam aprēķinātās atlaides iekasēšana
description: Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi. Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810250"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="d9be9-104">Vairāk par kreditora maksājumam aprēķinātās atlaides iekasēšana</span><span class="sxs-lookup"><span data-stu-id="d9be9-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9be9-105">Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi.</span><span class="sxs-lookup"><span data-stu-id="d9be9-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="d9be9-106">Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu.</span><span class="sxs-lookup"><span data-stu-id="d9be9-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="d9be9-107">Kreditors 3051 piešķir uzņēmumam Fabrikam termiņatlaidi 4 procentu apmēra, ja rēķins tiek apmaksāts septiņu dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="d9be9-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="d9be9-108">Eiprila 29. jūnijā ievada rēķinu par summu 1000,00.</span><span class="sxs-lookup"><span data-stu-id="d9be9-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="d9be9-109">Kreditors dod Eiprilai atļauju piemērot atlaidi par summu 60,00 rēķinam aprēķinātās noklusējuma summas 40,00 vietā.</span><span class="sxs-lookup"><span data-stu-id="d9be9-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="d9be9-110">Eiprila reģistrē vienreizēju maksājumu, izmantojot kreditoru maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="d9be9-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="d9be9-111">Viņa ievada maksājuma kreditoru un pēc tam atver lapu **Transakciju nosegšana**.</span><span class="sxs-lookup"><span data-stu-id="d9be9-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="d9be9-112">Viņa atzīmē rēķinu un maina lauka **Termiņatlaides summa** vērtību uz **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="d9be9-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="d9be9-113">Atzīmēt</span><span class="sxs-lookup"><span data-stu-id="d9be9-113">Mark</span></span>     | <span data-ttu-id="d9be9-114">Izmantot termiņatlaidi</span><span class="sxs-lookup"><span data-stu-id="d9be9-114">Use cash discount</span></span> | <span data-ttu-id="d9be9-115">Dokuments</span><span class="sxs-lookup"><span data-stu-id="d9be9-115">Voucher</span></span>   | <span data-ttu-id="d9be9-116">Konts</span><span class="sxs-lookup"><span data-stu-id="d9be9-116">Account</span></span> | <span data-ttu-id="d9be9-117">Datums</span><span class="sxs-lookup"><span data-stu-id="d9be9-117">Date</span></span>      | <span data-ttu-id="d9be9-118">Izpildes datums</span><span class="sxs-lookup"><span data-stu-id="d9be9-118">Due date</span></span>  | <span data-ttu-id="d9be9-119">Rēķins</span><span class="sxs-lookup"><span data-stu-id="d9be9-119">Invoice</span></span> | <span data-ttu-id="d9be9-120">Summa darījuma valūtā</span><span class="sxs-lookup"><span data-stu-id="d9be9-120">Amount in transaction currency</span></span> | <span data-ttu-id="d9be9-121">Valūta</span><span class="sxs-lookup"><span data-stu-id="d9be9-121">Currency</span></span> | <span data-ttu-id="d9be9-122">Nosedzamā summa</span><span class="sxs-lookup"><span data-stu-id="d9be9-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="d9be9-123">Atlasīts</span><span class="sxs-lookup"><span data-stu-id="d9be9-123">Selected</span></span> | <span data-ttu-id="d9be9-124">Parastais</span><span class="sxs-lookup"><span data-stu-id="d9be9-124">Normal</span></span>            | <span data-ttu-id="d9be9-125">Rēķ.-10040</span><span class="sxs-lookup"><span data-stu-id="d9be9-125">Inv-10040</span></span> | <span data-ttu-id="d9be9-126">3051</span><span class="sxs-lookup"><span data-stu-id="d9be9-126">3051</span></span>    | <span data-ttu-id="d9be9-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="d9be9-127">6/29/2015</span></span> | <span data-ttu-id="d9be9-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="d9be9-128">7/29/2015</span></span> | <span data-ttu-id="d9be9-129">10040</span><span class="sxs-lookup"><span data-stu-id="d9be9-129">10040</span></span>   | <span data-ttu-id="d9be9-130">1000,00</span><span class="sxs-lookup"><span data-stu-id="d9be9-130">1,000.00</span></span>                       | <span data-ttu-id="d9be9-131">USD</span><span class="sxs-lookup"><span data-stu-id="d9be9-131">USD</span></span>      | <span data-ttu-id="d9be9-132">940,00</span><span class="sxs-lookup"><span data-stu-id="d9be9-132">940.00</span></span>           |

<span data-ttu-id="d9be9-133">Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.</span><span class="sxs-lookup"><span data-stu-id="d9be9-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

| <span data-ttu-id="d9be9-134">Lauks</span><span class="sxs-lookup"><span data-stu-id="d9be9-134">Field</span></span>                        | <span data-ttu-id="d9be9-135">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d9be9-135">Value</span></span>     |
|------------------------------|-----------|
| <span data-ttu-id="d9be9-136">Termiņatlaides datums</span><span class="sxs-lookup"><span data-stu-id="d9be9-136">Cash discount date</span></span>           | <span data-ttu-id="d9be9-137">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="d9be9-137">7/12/2015</span></span> |
| <span data-ttu-id="d9be9-138">Termiņatlaides summa</span><span class="sxs-lookup"><span data-stu-id="d9be9-138">Cash discount amount</span></span>         | <span data-ttu-id="d9be9-139">60.00</span><span class="sxs-lookup"><span data-stu-id="d9be9-139">60.00</span></span>     |
| <span data-ttu-id="d9be9-140">Izmantot termiņatlaidi</span><span class="sxs-lookup"><span data-stu-id="d9be9-140">Use cash discount</span></span>            | <span data-ttu-id="d9be9-141">Parastais</span><span class="sxs-lookup"><span data-stu-id="d9be9-141">Normal</span></span>    |
| <span data-ttu-id="d9be9-142">Paņemta termiņatlaides summa</span><span class="sxs-lookup"><span data-stu-id="d9be9-142">Cash discount taken</span></span>          | <span data-ttu-id="d9be9-143">0,00</span><span class="sxs-lookup"><span data-stu-id="d9be9-143">0.00</span></span>      |
| <span data-ttu-id="d9be9-144">Ņemamā termiņatlaides summa</span><span class="sxs-lookup"><span data-stu-id="d9be9-144">Cash discount amount to take</span></span> | <span data-ttu-id="d9be9-145">60,00</span><span class="sxs-lookup"><span data-stu-id="d9be9-145">60.00</span></span>     |

<span data-ttu-id="d9be9-146">Eiprila iegrāmato maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="d9be9-146">April posts the payment journal.</span></span> <span data-ttu-id="d9be9-147">Rēķins tiek pilnībā nosegts, veicot maksājumu par summu 940,00 un piemērojot atlaidi 60,00.</span><span class="sxs-lookup"><span data-stu-id="d9be9-147">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]