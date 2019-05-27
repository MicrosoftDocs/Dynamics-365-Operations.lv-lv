---
title: Piemērs dienu skaita samazināšanai
description: Piemērs dienu skaita samazināšanai.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564512"
---
# <a name="reduction-days-example"></a><span data-ttu-id="703c2-103">Piemērs dienu skaita samazināšanai</span><span class="sxs-lookup"><span data-stu-id="703c2-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="703c2-104">Jūs esat izveidojis abonementa darījumu klienta uzturēšanas abonementam, kā aprakstīts šajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="703c2-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="703c2-105">No datuma</span><span class="sxs-lookup"><span data-stu-id="703c2-105">From date</span></span></p></th>
<th><p><span data-ttu-id="703c2-106">Līdz datumam</span><span class="sxs-lookup"><span data-stu-id="703c2-106">To date</span></span></p></th>
<th><p><span data-ttu-id="703c2-107">Abonements</span><span class="sxs-lookup"><span data-stu-id="703c2-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="703c2-108">Abonementa tips</span><span class="sxs-lookup"><span data-stu-id="703c2-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="703c2-109">Project</span><span class="sxs-lookup"><span data-stu-id="703c2-109">Project</span></span></p></th>
<th><p><span data-ttu-id="703c2-110">Kategorija</span><span class="sxs-lookup"><span data-stu-id="703c2-110">Category</span></span></p></th>
<th><p><span data-ttu-id="703c2-111">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="703c2-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="703c2-112">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="703c2-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="703c2-113">2011. gada 01. marts</span><span class="sxs-lookup"><span data-stu-id="703c2-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="703c2-114">2011. gada 31. marts</span><span class="sxs-lookup"><span data-stu-id="703c2-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="703c2-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="703c2-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="703c2-116"><strong>Regulārs</strong></span><span class="sxs-lookup"><span data-stu-id="703c2-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="703c2-117">9013</span><span class="sxs-lookup"><span data-stu-id="703c2-117">9013</span></span></p></td>
<td><p><span data-ttu-id="703c2-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="703c2-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="703c2-119">EUR</span><span class="sxs-lookup"><span data-stu-id="703c2-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="703c2-120">200,00</span><span class="sxs-lookup"><span data-stu-id="703c2-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="703c2-121">Klients ziņo, ka tam nav nepieciešams pakalpojumu nodrošinājums uz divām dienām (10. marts un 11. marts).</span><span class="sxs-lookup"><span data-stu-id="703c2-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="703c2-122">Jūs piekrītat samazināt abonementu par šīm divām dienām.</span><span class="sxs-lookup"><span data-stu-id="703c2-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="703c2-123">Jūs izveidojat jaunu darbību, kuras tips ir **Dienu skaita samazināšana**, kā aprakstīts šajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="703c2-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="703c2-124">No datuma</span><span class="sxs-lookup"><span data-stu-id="703c2-124">From date</span></span></p></th>
<th><p><span data-ttu-id="703c2-125">Līdz datumam</span><span class="sxs-lookup"><span data-stu-id="703c2-125">To date</span></span></p></th>
<th><p><span data-ttu-id="703c2-126">Abonements</span><span class="sxs-lookup"><span data-stu-id="703c2-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="703c2-127">Abonementa tips</span><span class="sxs-lookup"><span data-stu-id="703c2-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="703c2-128">Project</span><span class="sxs-lookup"><span data-stu-id="703c2-128">Project</span></span></p></th>
<th><p><span data-ttu-id="703c2-129">Kategorija</span><span class="sxs-lookup"><span data-stu-id="703c2-129">Category</span></span></p></th>
<th><p><span data-ttu-id="703c2-130">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="703c2-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="703c2-131">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="703c2-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="703c2-132">2011. gada 10. marts</span><span class="sxs-lookup"><span data-stu-id="703c2-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="703c2-133">2011. gada 11. marts</span><span class="sxs-lookup"><span data-stu-id="703c2-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="703c2-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="703c2-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="703c2-135"><strong>Dienu skaita samazināšana</strong></span><span class="sxs-lookup"><span data-stu-id="703c2-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="703c2-136">9013</span><span class="sxs-lookup"><span data-stu-id="703c2-136">9013</span></span></p></td>
<td><p><span data-ttu-id="703c2-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="703c2-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="703c2-138">EUR</span><span class="sxs-lookup"><span data-stu-id="703c2-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="703c2-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="703c2-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="703c2-140">Kad par 2011. gada darbībām tiek sagatavots rēķins, pārdošanas cena EUR 200 tiek samazināta par EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="703c2-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="703c2-141">Tādējādi atskaitāmā summa par abonementa darbību ir EUR 187,10, un tiks izsūtīti rēķini par divām darbībām ar kopējo summu EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="703c2-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="703c2-142">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="703c2-142">See also</span></span>

[<span data-ttu-id="703c2-143">Abonementa apmaksas dienu samazināšana</span><span class="sxs-lookup"><span data-stu-id="703c2-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


