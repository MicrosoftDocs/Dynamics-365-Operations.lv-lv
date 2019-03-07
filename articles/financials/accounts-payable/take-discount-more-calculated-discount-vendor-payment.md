---
title: Atlaides, kas ir lielāka par kreditora maksājumam aprēķināto atlaidi, piemērošana
description: Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi. Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66296bc22cb3b940ed914b77b8c3a7c054d4aa71
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "326841"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="72e38-104">Atlaides, kas ir lielāka par kreditora maksājumam aprēķināto atlaidi, piemērošana</span><span class="sxs-lookup"><span data-stu-id="72e38-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72e38-105">Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi.</span><span class="sxs-lookup"><span data-stu-id="72e38-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="72e38-106">Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu.</span><span class="sxs-lookup"><span data-stu-id="72e38-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="72e38-107">Kreditors 3051 piešķir uzņēmumam Fabrikam termiņatlaidi 4 procentu apmēra, ja rēķins tiek apmaksāts septiņu dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="72e38-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="72e38-108">Eiprila 29. jūnijā ievada rēķinu par summu 1000,00.</span><span class="sxs-lookup"><span data-stu-id="72e38-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="72e38-109">Kreditors dod Eiprilai atļauju piemērot atlaidi par summu 60,00 rēķinam aprēķinātās noklusējuma summas 40,00 vietā.</span><span class="sxs-lookup"><span data-stu-id="72e38-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="72e38-110">Eiprila reģistrē vienreizēju maksājumu, izmantojot kreditoru maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="72e38-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="72e38-111">Viņa ievada maksājuma kreditoru un pēc tam atver lapu **Transakciju nosegšana**.</span><span class="sxs-lookup"><span data-stu-id="72e38-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="72e38-112">Viņa atzīmē rēķinu un maina lauka **Termiņatlaides summa** vērtību uz **-60,00**.</span><span class="sxs-lookup"><span data-stu-id="72e38-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="72e38-113">Atzīmēt</span><span class="sxs-lookup"><span data-stu-id="72e38-113">Mark</span></span>     | <span data-ttu-id="72e38-114">Izmantot termiņatlaidi</span><span class="sxs-lookup"><span data-stu-id="72e38-114">Use cash discount</span></span> | <span data-ttu-id="72e38-115">Dokuments</span><span class="sxs-lookup"><span data-stu-id="72e38-115">Voucher</span></span>   | <span data-ttu-id="72e38-116">Konts</span><span class="sxs-lookup"><span data-stu-id="72e38-116">Account</span></span> | <span data-ttu-id="72e38-117">Datums</span><span class="sxs-lookup"><span data-stu-id="72e38-117">Date</span></span>      | <span data-ttu-id="72e38-118">Izpildes datums</span><span class="sxs-lookup"><span data-stu-id="72e38-118">Due date</span></span>  | <span data-ttu-id="72e38-119">Rēķins</span><span class="sxs-lookup"><span data-stu-id="72e38-119">Invoice</span></span> | <span data-ttu-id="72e38-120">Summa darījuma valūtā</span><span class="sxs-lookup"><span data-stu-id="72e38-120">Amount in transaction currency</span></span> | <span data-ttu-id="72e38-121">Valūta</span><span class="sxs-lookup"><span data-stu-id="72e38-121">Currency</span></span> | <span data-ttu-id="72e38-122">Nosedzamā summa</span><span class="sxs-lookup"><span data-stu-id="72e38-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="72e38-123">Atlasīts</span><span class="sxs-lookup"><span data-stu-id="72e38-123">Selected</span></span> | <span data-ttu-id="72e38-124">Parastais</span><span class="sxs-lookup"><span data-stu-id="72e38-124">Normal</span></span>            | <span data-ttu-id="72e38-125">Rēķ.-10040</span><span class="sxs-lookup"><span data-stu-id="72e38-125">Inv-10040</span></span> | <span data-ttu-id="72e38-126">3051</span><span class="sxs-lookup"><span data-stu-id="72e38-126">3051</span></span>    | <span data-ttu-id="72e38-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="72e38-127">6/29/2015</span></span> | <span data-ttu-id="72e38-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="72e38-128">7/29/2015</span></span> | <span data-ttu-id="72e38-129">10040</span><span class="sxs-lookup"><span data-stu-id="72e38-129">10040</span></span>   | <span data-ttu-id="72e38-130">1000,00</span><span class="sxs-lookup"><span data-stu-id="72e38-130">1,000.00</span></span>                       | <span data-ttu-id="72e38-131">USD</span><span class="sxs-lookup"><span data-stu-id="72e38-131">USD</span></span>      | <span data-ttu-id="72e38-132">940,00</span><span class="sxs-lookup"><span data-stu-id="72e38-132">940.00</span></span>           |

<span data-ttu-id="72e38-133">Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.</span><span class="sxs-lookup"><span data-stu-id="72e38-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="72e38-134">Termiņatlaides datums</span><span class="sxs-lookup"><span data-stu-id="72e38-134">Cash discount date</span></span>           | <span data-ttu-id="72e38-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="72e38-135">7/12/2015</span></span> |
| <span data-ttu-id="72e38-136">Termiņatlaides summa</span><span class="sxs-lookup"><span data-stu-id="72e38-136">Cash discount amount</span></span>         | <span data-ttu-id="72e38-137">60,00</span><span class="sxs-lookup"><span data-stu-id="72e38-137">60.00</span></span>     |
| <span data-ttu-id="72e38-138">Izmantot termiņatlaidi</span><span class="sxs-lookup"><span data-stu-id="72e38-138">Use cash discount</span></span>            | <span data-ttu-id="72e38-139">Parastais</span><span class="sxs-lookup"><span data-stu-id="72e38-139">Normal</span></span>    |
| <span data-ttu-id="72e38-140">Paņemta termiņatlaides summa</span><span class="sxs-lookup"><span data-stu-id="72e38-140">Cash discount taken</span></span>          | <span data-ttu-id="72e38-141">0,00</span><span class="sxs-lookup"><span data-stu-id="72e38-141">0.00</span></span>      |
| <span data-ttu-id="72e38-142">Ņemamā termiņatlaides summa</span><span class="sxs-lookup"><span data-stu-id="72e38-142">Cash discount amount to take</span></span> | <span data-ttu-id="72e38-143">60,00</span><span class="sxs-lookup"><span data-stu-id="72e38-143">60.00</span></span>     |

<span data-ttu-id="72e38-144">Eiprila iegrāmato maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="72e38-144">April posts the payment journal.</span></span> <span data-ttu-id="72e38-145">Rēķins tiek pilnībā nosegts, veicot maksājumu par summu 940,00 un piemērojot atlaidi 60,00.</span><span class="sxs-lookup"><span data-stu-id="72e38-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



