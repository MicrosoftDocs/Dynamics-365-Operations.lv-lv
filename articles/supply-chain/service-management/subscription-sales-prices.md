---
title: Abonementu pārdošanas cenas
description: Kad veidojot abonementu, pārdošanas cena tiek atvasināta no pārdošanas cenas iestatījuma, kas bija izveidots formā Pārdošanas cena (abonements).
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560693"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="0b103-103">Abonementu pārdošanas cenas</span><span class="sxs-lookup"><span data-stu-id="0b103-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0b103-104">Kad veidojot abonementu, pārdošanas cena tiek atvasināta no pārdošanas cenas iestatījuma, kas bija izveidots formā **Pārdošanas cena (abonements)**.</span><span class="sxs-lookup"><span data-stu-id="0b103-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="0b103-105">Formā **Pārdošanas cena (abonements)** varat izveidot pārdošanas cenas konkrētam abonementam vai plašāk izmantojamas pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="0b103-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="0b103-106">Lai pārdošanas cenu lietotu kādam abonementam, šī abonementa perioda kodam un valūtai ir jābūt identiskiem ar attiecīgās pārdošanas cenas perioda kodu un valūtu.</span><span class="sxs-lookup"><span data-stu-id="0b103-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="0b103-107">Ja perioda kods un valūta gan abonementam, gan pārdošanas cenai ir identiski, abonementa pārdošanas cenas tiek atlasītas atkarībā no nākamajā tabulā norādītajām prioritātēm.</span><span class="sxs-lookup"><span data-stu-id="0b103-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="0b103-108">Tukša šūna tabulā nozīmē tukšu lauku, un atzīme X nozīmē, ka vērtība ir vienāda ar vērtību abonementā, no kura transakcija tiek ģenerēta.</span><span class="sxs-lookup"><span data-stu-id="0b103-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b103-109">Prioritāte</span><span class="sxs-lookup"><span data-stu-id="0b103-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="0b103-110"><strong>Kategorija</strong></span><span class="sxs-lookup"><span data-stu-id="0b103-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="0b103-111"><strong>Projekta ID</strong></span><span class="sxs-lookup"><span data-stu-id="0b103-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="0b103-112"><strong>Abonements</strong></span><span class="sxs-lookup"><span data-stu-id="0b103-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="0b103-113"><strong>Pārdošanas valūta</strong></span><span class="sxs-lookup"><span data-stu-id="0b103-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="0b103-114"><strong>Perioda kods</strong></span><span class="sxs-lookup"><span data-stu-id="0b103-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b103-115">1</span><span class="sxs-lookup"><span data-stu-id="0b103-115">1</span></span></p></td>
<td><p><span data-ttu-id="0b103-116">X</span><span class="sxs-lookup"><span data-stu-id="0b103-116">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-117">X</span><span class="sxs-lookup"><span data-stu-id="0b103-117">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-118">X</span><span class="sxs-lookup"><span data-stu-id="0b103-118">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-119">X</span><span class="sxs-lookup"><span data-stu-id="0b103-119">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-120">X</span><span class="sxs-lookup"><span data-stu-id="0b103-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-121">2</span><span class="sxs-lookup"><span data-stu-id="0b103-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-122">X</span><span class="sxs-lookup"><span data-stu-id="0b103-122">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-123">X</span><span class="sxs-lookup"><span data-stu-id="0b103-123">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-124">X</span><span class="sxs-lookup"><span data-stu-id="0b103-124">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-125">X</span><span class="sxs-lookup"><span data-stu-id="0b103-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b103-126">3</span><span class="sxs-lookup"><span data-stu-id="0b103-126">3</span></span></p></td>
<td><p><span data-ttu-id="0b103-127">X</span><span class="sxs-lookup"><span data-stu-id="0b103-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-128">X</span><span class="sxs-lookup"><span data-stu-id="0b103-128">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-129">X</span><span class="sxs-lookup"><span data-stu-id="0b103-129">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-130">X</span><span class="sxs-lookup"><span data-stu-id="0b103-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-131">4</span><span class="sxs-lookup"><span data-stu-id="0b103-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-132">X</span><span class="sxs-lookup"><span data-stu-id="0b103-132">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-133">X</span><span class="sxs-lookup"><span data-stu-id="0b103-133">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-134">X</span><span class="sxs-lookup"><span data-stu-id="0b103-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b103-135">5</span><span class="sxs-lookup"><span data-stu-id="0b103-135">5</span></span></p></td>
<td><p><span data-ttu-id="0b103-136">X</span><span class="sxs-lookup"><span data-stu-id="0b103-136">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-137">X</span><span class="sxs-lookup"><span data-stu-id="0b103-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-138">X</span><span class="sxs-lookup"><span data-stu-id="0b103-138">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-139">X</span><span class="sxs-lookup"><span data-stu-id="0b103-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-140">6</span><span class="sxs-lookup"><span data-stu-id="0b103-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-141">X</span><span class="sxs-lookup"><span data-stu-id="0b103-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-142">X</span><span class="sxs-lookup"><span data-stu-id="0b103-142">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-143">X</span><span class="sxs-lookup"><span data-stu-id="0b103-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b103-144">7</span><span class="sxs-lookup"><span data-stu-id="0b103-144">7</span></span></p></td>
<td><p><span data-ttu-id="0b103-145">X</span><span class="sxs-lookup"><span data-stu-id="0b103-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-146">X</span><span class="sxs-lookup"><span data-stu-id="0b103-146">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-147">X</span><span class="sxs-lookup"><span data-stu-id="0b103-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-148">8</span><span class="sxs-lookup"><span data-stu-id="0b103-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0b103-149">X</span><span class="sxs-lookup"><span data-stu-id="0b103-149">X</span></span></p></td>
<td><p><span data-ttu-id="0b103-150">X</span><span class="sxs-lookup"><span data-stu-id="0b103-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b103-151">Kad tiek izveidota abonēšanas maksa, par abonementa pārdošanas cenu tiek atlasīta pārdošanas cena ar augstāko detalizācijas līmeni (kā norādīts iepriekš redzamajā tabulā).</span><span class="sxs-lookup"><span data-stu-id="0b103-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="0b103-152">Abonementu pārdošanas cenu atjaunināšana un indeksēšana</span><span class="sxs-lookup"><span data-stu-id="0b103-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="0b103-153">Abonementa pārdošanas cenu var atjaunināt, atjauninot pamatcenu vai indeksu.</span><span class="sxs-lookup"><span data-stu-id="0b103-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="0b103-154">Atjaunināt var par procentuālu daudzumu vai uz jaunu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b103-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="0b103-155">Abonēšanas maksas pārdošanas cenas</span><span class="sxs-lookup"><span data-stu-id="0b103-155">Subscription fee sales prices</span></span>

<span data-ttu-id="0b103-156">Veidojot abonēšanas maksu, pārdošanas cena ir atkarīga no abonementam iestatītās pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="0b103-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="0b103-157">Varat izmantot pamatcenu no abonementa cenas iestatījuma vai izveidot indeksētas pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="0b103-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="0b103-158">Piemērs</span><span class="sxs-lookup"><span data-stu-id="0b103-158">Example</span></span>

<span data-ttu-id="0b103-159">Jūs jaunam projektam 9030 vēlaties iestatīt abonementa pārdošanas cenas EUR 500 vērtībā.</span><span class="sxs-lookup"><span data-stu-id="0b103-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="0b103-160">Formā **Pārdošanas cena (abonements)** jūs izveidojat abonementa pārdošanas cenas rindu, kā noradīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0b103-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b103-161">Derīgs no</span><span class="sxs-lookup"><span data-stu-id="0b103-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0b103-162">Kategorija</span><span class="sxs-lookup"><span data-stu-id="0b103-162">Category</span></span></p></th>
<th><p><span data-ttu-id="0b103-163">Projekts</span><span class="sxs-lookup"><span data-stu-id="0b103-163">Project</span></span></p></th>
<th><p><span data-ttu-id="0b103-164">Abonements</span><span class="sxs-lookup"><span data-stu-id="0b103-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0b103-165">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="0b103-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="0b103-166">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="0b103-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0b103-167">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="0b103-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b103-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0b103-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0b103-169">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0b103-170">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="0b103-170">Month</span></span></p></td>
<td><p><span data-ttu-id="0b103-171">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-172">500</span><span class="sxs-lookup"><span data-stu-id="0b103-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b103-173">Pievērsiet uzmanību, ka lauki **Kategorija** un **Abonements** ir tukši.</span><span class="sxs-lookup"><span data-stu-id="0b103-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="0b103-174">Pēc tam jūs izveidojat tālāk norādītos abonementus.</span><span class="sxs-lookup"><span data-stu-id="0b103-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b103-175">Pakalpojuma abonements</span><span class="sxs-lookup"><span data-stu-id="0b103-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0b103-176">Projekts</span><span class="sxs-lookup"><span data-stu-id="0b103-176">Project</span></span></p></th>
<th><p><span data-ttu-id="0b103-177">Abonementu grupa</span><span class="sxs-lookup"><span data-stu-id="0b103-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="0b103-178">Kategorija</span><span class="sxs-lookup"><span data-stu-id="0b103-178">Category</span></span></p></th>
<th><p><span data-ttu-id="0b103-179">Valūta</span><span class="sxs-lookup"><span data-stu-id="0b103-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="0b103-180">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="0b103-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b103-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="0b103-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0b103-182">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-182">9030</span></span></p></td>
<td><p><span data-ttu-id="0b103-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="0b103-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0b103-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0b103-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0b103-185">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-186">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="0b103-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="0b103-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0b103-188">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-188">9030</span></span></p></td>
<td><p><span data-ttu-id="0b103-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="0b103-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0b103-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="0b103-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0b103-191">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-192">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="0b103-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b103-193">Tagad jūs izveidojat abonēšanas maksas abiem abonementiem abonementu grupā Sub1:</span><span class="sxs-lookup"><span data-stu-id="0b103-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="0b103-194">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.</span><span class="sxs-lookup"><span data-stu-id="0b103-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="0b103-195">Formā **Abonementu grupas** noklikšķiniet uz **Funkcija** \> **Izveidot abonēšanas maksu**.</span><span class="sxs-lookup"><span data-stu-id="0b103-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="0b103-196">Formā **Izveidot abonēšanas maksu** ievadiet atbilstošo informāciju.</span><span class="sxs-lookup"><span data-stu-id="0b103-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="0b103-197">Plašāku informāciju skatiet tēmā [Abonēšanas maksu transakciju izveidošana](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="0b103-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="0b103-198">Abiem abonementiem tiek izveidotas abonēšanas maksas, kam ir pārdošanas cena 500 EUR, kā parādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0b103-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="0b103-199">Projekta datums</span><span class="sxs-lookup"><span data-stu-id="0b103-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="0b103-200">Pakalpojuma abonements</span><span class="sxs-lookup"><span data-stu-id="0b103-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0b103-201">Projekts</span><span class="sxs-lookup"><span data-stu-id="0b103-201">Project</span></span></p></th>
<th><p><span data-ttu-id="0b103-202">Kategorija</span><span class="sxs-lookup"><span data-stu-id="0b103-202">Category</span></span></p></th>
<th><p><span data-ttu-id="0b103-203">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="0b103-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="0b103-204">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="0b103-204">End date</span></span></p></th>
<th><p><span data-ttu-id="0b103-205">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="0b103-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0b103-206">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="0b103-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b103-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0b103-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0b103-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="0b103-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0b103-209">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-209">9030</span></span></p></td>
<td><p><span data-ttu-id="0b103-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0b103-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0b103-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="0b103-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0b103-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="0b103-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0b103-213">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-214">500</span><span class="sxs-lookup"><span data-stu-id="0b103-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0b103-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0b103-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="0b103-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0b103-217">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-217">9030</span></span></p></td>
<td><p><span data-ttu-id="0b103-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="0b103-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0b103-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="0b103-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0b103-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="0b103-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0b103-221">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-222">500</span><span class="sxs-lookup"><span data-stu-id="0b103-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b103-223">Vēlāk jūs izlemjat, ka vēlaties norādīt pārdošanas cenas projekta 9030 kategorijai SubCat1.</span><span class="sxs-lookup"><span data-stu-id="0b103-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="0b103-224">Tāpēc jūs izveidojat jaunu pārdošanas cenu rindu, kuras pārdošanas cena ir 550 EUR projekta 9030 un maksu kategorijas SubCat1 kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="0b103-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="0b103-225">Tagad projektam 9030 ir divas abonementa pārdošanas cenu rindas, kā parādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0b103-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b103-226">Derīgs no</span><span class="sxs-lookup"><span data-stu-id="0b103-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0b103-227">Kategorija</span><span class="sxs-lookup"><span data-stu-id="0b103-227">Category</span></span></p></th>
<th><p><span data-ttu-id="0b103-228">Projekts</span><span class="sxs-lookup"><span data-stu-id="0b103-228">Project</span></span></p></th>
<th><p><span data-ttu-id="0b103-229">Abonements</span><span class="sxs-lookup"><span data-stu-id="0b103-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0b103-230">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="0b103-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="0b103-231">Valūta</span><span class="sxs-lookup"><span data-stu-id="0b103-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="0b103-232">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="0b103-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b103-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="0b103-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0b103-234">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0b103-235">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="0b103-235">Month</span></span></p></td>
<td><p><span data-ttu-id="0b103-236">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-237">500</span><span class="sxs-lookup"><span data-stu-id="0b103-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="0b103-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="0b103-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0b103-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0b103-240">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0b103-241">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="0b103-241">Month</span></span></p></td>
<td><p><span data-ttu-id="0b103-242">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-243">550</span><span class="sxs-lookup"><span data-stu-id="0b103-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b103-244">Jūs atkārtojat iepriekš aprakstīto procedūru, lai izveidotu abonēšanas maksas abiem abonementiem abonementu grupā Sub1.</span><span class="sxs-lookup"><span data-stu-id="0b103-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="0b103-245">Nākamajā tabulā ir parādītas transakcijas, kas tiek izveidotas katram abonementam, kurš ir pievienots abonementu grupai.</span><span class="sxs-lookup"><span data-stu-id="0b103-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="0b103-246">Projekta datums</span><span class="sxs-lookup"><span data-stu-id="0b103-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="0b103-247">Abonements</span><span class="sxs-lookup"><span data-stu-id="0b103-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0b103-248">Projekts</span><span class="sxs-lookup"><span data-stu-id="0b103-248">Project</span></span></p></th>
<th><p><span data-ttu-id="0b103-249">Kategorija</span><span class="sxs-lookup"><span data-stu-id="0b103-249">Category</span></span></p></th>
<th><p><span data-ttu-id="0b103-250">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="0b103-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="0b103-251">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="0b103-251">End date</span></span></p></th>
<th><p><span data-ttu-id="0b103-252">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="0b103-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0b103-253">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="0b103-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b103-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="0b103-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="0b103-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="0b103-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0b103-256">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-256">9030</span></span></p></td>
<td><p><span data-ttu-id="0b103-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0b103-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0b103-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="0b103-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0b103-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="0b103-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0b103-260">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-261">550</span><span class="sxs-lookup"><span data-stu-id="0b103-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b103-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="0b103-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="0b103-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="0b103-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0b103-264">9030</span><span class="sxs-lookup"><span data-stu-id="0b103-264">9030</span></span></p></td>
<td><p><span data-ttu-id="0b103-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="0b103-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0b103-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="0b103-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0b103-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="0b103-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0b103-268">EUR</span><span class="sxs-lookup"><span data-stu-id="0b103-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="0b103-269">500</span><span class="sxs-lookup"><span data-stu-id="0b103-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b103-270">Pirmajā transakcijā abonementam 00020\_135 pārdošanas cena 550 EUR tiek atvasināta no abonementa pārdošanas cenas, kas ir iestatīta konkrētā projekta un kategorijas kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="0b103-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="0b103-271">Otrajā transakcijā abonementam 00021\_135 pārdošanas cena 500 EUR tiek izmantota kā projekta abonementa pārdošanas cena, jo projekta 9030 un kategorijas SubCat2 kombinācijai pārdošanas cena nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="0b103-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b103-272">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="0b103-272">See also</span></span>

[<span data-ttu-id="0b103-273">Abonementu pārdošanas cenu atjaunināšana un indeksēšana</span><span class="sxs-lookup"><span data-stu-id="0b103-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


