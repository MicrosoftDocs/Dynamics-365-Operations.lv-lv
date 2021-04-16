---
title: Abonementu pārdošanas cenas
description: Kad veidojot abonementu, pārdošanas cena tiek atvasināta no pārdošanas cenas iestatījuma, kas bija izveidots formā Pārdošanas cena (abonements).
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b4b02af0a535e67818751c437482c3663524474
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817417"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="d04a7-103">Abonementu pārdošanas cenas</span><span class="sxs-lookup"><span data-stu-id="d04a7-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d04a7-104">Kad veidojot abonementu, pārdošanas cena tiek atvasināta no pārdošanas cenas iestatījuma, kas bija izveidots formā **Pārdošanas cena (abonements)**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="d04a7-105">Formā **Pārdošanas cena (abonements)** varat izveidot pārdošanas cenas konkrētam abonementam vai plašāk izmantojamas pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="d04a7-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="d04a7-106">Lai pārdošanas cenu lietotu kādam abonementam, šī abonementa perioda kodam un valūtai ir jābūt identiskiem ar attiecīgās pārdošanas cenas perioda kodu un valūtu.</span><span class="sxs-lookup"><span data-stu-id="d04a7-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="d04a7-107">Ja perioda kods un valūta gan abonementam, gan pārdošanas cenai ir identiski, abonementa pārdošanas cenas tiek atlasītas atkarībā no nākamajā tabulā norādītajām prioritātēm.</span><span class="sxs-lookup"><span data-stu-id="d04a7-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="d04a7-108">Tukša šūna tabulā nozīmē tukšu lauku, un atzīme X nozīmē, ka vērtība ir vienāda ar vērtību abonementā, no kura transakcija tiek ģenerēta.</span><span class="sxs-lookup"><span data-stu-id="d04a7-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="d04a7-109">Prioritāte</span><span class="sxs-lookup"><span data-stu-id="d04a7-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="d04a7-110"><strong>Kategorija</strong></span><span class="sxs-lookup"><span data-stu-id="d04a7-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="d04a7-111"><strong>Projekta ID</strong></span><span class="sxs-lookup"><span data-stu-id="d04a7-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="d04a7-112"><strong>Abonements</strong></span><span class="sxs-lookup"><span data-stu-id="d04a7-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="d04a7-113"><strong>Pārdošanas valūta</strong></span><span class="sxs-lookup"><span data-stu-id="d04a7-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="d04a7-114"><strong>Perioda kods</strong></span><span class="sxs-lookup"><span data-stu-id="d04a7-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-115">1</span><span class="sxs-lookup"><span data-stu-id="d04a7-115">1</span></span></p></td>
<td><p><span data-ttu-id="d04a7-116">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-116">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-117">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-117">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-118">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-118">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-119">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-119">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-120">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-121">2</span><span class="sxs-lookup"><span data-stu-id="d04a7-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-122">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-122">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-123">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-123">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-124">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-124">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-125">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-126">3</span><span class="sxs-lookup"><span data-stu-id="d04a7-126">3</span></span></p></td>
<td><p><span data-ttu-id="d04a7-127">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-128">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-128">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-129">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-129">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-130">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-131">4</span><span class="sxs-lookup"><span data-stu-id="d04a7-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-132">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-132">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-133">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-133">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-134">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-135">5</span><span class="sxs-lookup"><span data-stu-id="d04a7-135">5</span></span></p></td>
<td><p><span data-ttu-id="d04a7-136">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-136">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-137">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-138">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-138">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-139">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-140">6</span><span class="sxs-lookup"><span data-stu-id="d04a7-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-141">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-142">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-142">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-143">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-144">7</span><span class="sxs-lookup"><span data-stu-id="d04a7-144">7</span></span></p></td>
<td><p><span data-ttu-id="d04a7-145">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-146">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-146">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-147">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-148">8</span><span class="sxs-lookup"><span data-stu-id="d04a7-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d04a7-149">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-149">X</span></span></p></td>
<td><p><span data-ttu-id="d04a7-150">X</span><span class="sxs-lookup"><span data-stu-id="d04a7-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d04a7-151">Kad tiek izveidota abonēšanas maksa, par abonementa pārdošanas cenu tiek atlasīta pārdošanas cena ar augstāko detalizācijas līmeni (kā norādīts iepriekš redzamajā tabulā).</span><span class="sxs-lookup"><span data-stu-id="d04a7-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="d04a7-152">Abonementu pārdošanas cenu atjaunināšana un indeksēšana</span><span class="sxs-lookup"><span data-stu-id="d04a7-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="d04a7-153">Abonementa pārdošanas cenu var atjaunināt, atjauninot pamatcenu vai indeksu.</span><span class="sxs-lookup"><span data-stu-id="d04a7-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="d04a7-154">Atjaunināt var par procentuālu daudzumu vai uz jaunu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d04a7-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="d04a7-155">Abonēšanas maksas pārdošanas cenas</span><span class="sxs-lookup"><span data-stu-id="d04a7-155">Subscription fee sales prices</span></span>

<span data-ttu-id="d04a7-156">Veidojot abonēšanas maksu, pārdošanas cena ir atkarīga no abonementam iestatītās pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="d04a7-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="d04a7-157">Varat izmantot pamatcenu no abonementa cenas iestatījuma vai izveidot indeksētas pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="d04a7-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="d04a7-158">Piemērs</span><span class="sxs-lookup"><span data-stu-id="d04a7-158">Example</span></span>

<span data-ttu-id="d04a7-159">Jūs jaunam projektam 9030 vēlaties iestatīt abonementa pārdošanas cenas EUR 500 vērtībā.</span><span class="sxs-lookup"><span data-stu-id="d04a7-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="d04a7-160">Formā **Pārdošanas cena (abonements)** jūs izveidojat abonementa pārdošanas cenas rindu, kā noradīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="d04a7-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="d04a7-161">Derīgs no</span><span class="sxs-lookup"><span data-stu-id="d04a7-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="d04a7-162">Kategorija</span><span class="sxs-lookup"><span data-stu-id="d04a7-162">Category</span></span></p></th>
<th><p><span data-ttu-id="d04a7-163">Projekts</span><span class="sxs-lookup"><span data-stu-id="d04a7-163">Project</span></span></p></th>
<th><p><span data-ttu-id="d04a7-164">Abonements</span><span class="sxs-lookup"><span data-stu-id="d04a7-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d04a7-165">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="d04a7-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="d04a7-166">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="d04a7-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d04a7-167">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="d04a7-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="d04a7-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d04a7-169">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d04a7-170">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="d04a7-170">Month</span></span></p></td>
<td><p><span data-ttu-id="d04a7-171">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-172">500</span><span class="sxs-lookup"><span data-stu-id="d04a7-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d04a7-173">Pievērsiet uzmanību, ka lauki **Kategorija** un **Abonements** ir tukši.</span><span class="sxs-lookup"><span data-stu-id="d04a7-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="d04a7-174">Pēc tam jūs izveidojat tālāk norādītos abonementus.</span><span class="sxs-lookup"><span data-stu-id="d04a7-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="d04a7-175">Pakalpojuma abonements</span><span class="sxs-lookup"><span data-stu-id="d04a7-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="d04a7-176">Projekts</span><span class="sxs-lookup"><span data-stu-id="d04a7-176">Project</span></span></p></th>
<th><p><span data-ttu-id="d04a7-177">Abonementu grupa</span><span class="sxs-lookup"><span data-stu-id="d04a7-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="d04a7-178">Kategorija</span><span class="sxs-lookup"><span data-stu-id="d04a7-178">Category</span></span></p></th>
<th><p><span data-ttu-id="d04a7-179">Valūta</span><span class="sxs-lookup"><span data-stu-id="d04a7-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="d04a7-180">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="d04a7-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="d04a7-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d04a7-182">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-182">9030</span></span></p></td>
<td><p><span data-ttu-id="d04a7-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="d04a7-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="d04a7-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d04a7-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d04a7-185">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-186">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="d04a7-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="d04a7-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d04a7-188">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-188">9030</span></span></p></td>
<td><p><span data-ttu-id="d04a7-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="d04a7-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="d04a7-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d04a7-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d04a7-191">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-192">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="d04a7-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d04a7-193">Tagad jūs izveidojat abonēšanas maksas abiem abonementiem abonementu grupā Sub1:</span><span class="sxs-lookup"><span data-stu-id="d04a7-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="d04a7-194">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="d04a7-195">Formā **Abonementu grupas** noklikšķiniet uz **Funkcija** \> **Izveidot abonēšanas maksu**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="d04a7-196">Formā **Izveidot abonēšanas maksu** ievadiet atbilstošo informāciju.</span><span class="sxs-lookup"><span data-stu-id="d04a7-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="d04a7-197">Plašāku informāciju skatiet tēmā [Abonēšanas maksu transakciju izveidošana](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="d04a7-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="d04a7-198">Abiem abonementiem tiek izveidotas abonēšanas maksas, kam ir pārdošanas cena 500 EUR, kā parādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="d04a7-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="d04a7-199">Projekta datums</span><span class="sxs-lookup"><span data-stu-id="d04a7-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="d04a7-200">Pakalpojuma abonements</span><span class="sxs-lookup"><span data-stu-id="d04a7-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="d04a7-201">Projekts</span><span class="sxs-lookup"><span data-stu-id="d04a7-201">Project</span></span></p></th>
<th><p><span data-ttu-id="d04a7-202">Kategorija</span><span class="sxs-lookup"><span data-stu-id="d04a7-202">Category</span></span></p></th>
<th><p><span data-ttu-id="d04a7-203">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="d04a7-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="d04a7-204">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="d04a7-204">End date</span></span></p></th>
<th><p><span data-ttu-id="d04a7-205">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="d04a7-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d04a7-206">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="d04a7-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="d04a7-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="d04a7-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="d04a7-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d04a7-209">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-209">9030</span></span></p></td>
<td><p><span data-ttu-id="d04a7-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d04a7-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d04a7-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="d04a7-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="d04a7-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="d04a7-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="d04a7-213">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-214">500</span><span class="sxs-lookup"><span data-stu-id="d04a7-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="d04a7-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="d04a7-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="d04a7-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d04a7-217">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-217">9030</span></span></p></td>
<td><p><span data-ttu-id="d04a7-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d04a7-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d04a7-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="d04a7-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="d04a7-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="d04a7-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="d04a7-221">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-222">500</span><span class="sxs-lookup"><span data-stu-id="d04a7-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d04a7-223">Vēlāk jūs izlemjat, ka vēlaties norādīt pārdošanas cenas projekta 9030 kategorijai SubCat1.</span><span class="sxs-lookup"><span data-stu-id="d04a7-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="d04a7-224">Tāpēc jūs izveidojat jaunu pārdošanas cenu rindu, kuras pārdošanas cena ir 550 EUR projekta 9030 un maksu kategorijas SubCat1 kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="d04a7-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="d04a7-225">Tagad projektam 9030 ir divas abonementa pārdošanas cenu rindas, kā parādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="d04a7-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="d04a7-226">Derīgs no</span><span class="sxs-lookup"><span data-stu-id="d04a7-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="d04a7-227">Kategorija</span><span class="sxs-lookup"><span data-stu-id="d04a7-227">Category</span></span></p></th>
<th><p><span data-ttu-id="d04a7-228">Projekts</span><span class="sxs-lookup"><span data-stu-id="d04a7-228">Project</span></span></p></th>
<th><p><span data-ttu-id="d04a7-229">Abonements</span><span class="sxs-lookup"><span data-stu-id="d04a7-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d04a7-230">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="d04a7-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="d04a7-231">Valūta</span><span class="sxs-lookup"><span data-stu-id="d04a7-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="d04a7-232">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="d04a7-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="d04a7-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d04a7-234">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d04a7-235">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="d04a7-235">Month</span></span></p></td>
<td><p><span data-ttu-id="d04a7-236">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-237">500</span><span class="sxs-lookup"><span data-stu-id="d04a7-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="d04a7-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="d04a7-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d04a7-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d04a7-240">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d04a7-241">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="d04a7-241">Month</span></span></p></td>
<td><p><span data-ttu-id="d04a7-242">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-243">550</span><span class="sxs-lookup"><span data-stu-id="d04a7-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d04a7-244">Jūs atkārtojat iepriekš aprakstīto procedūru, lai izveidotu abonēšanas maksas abiem abonementiem abonementu grupā Sub1.</span><span class="sxs-lookup"><span data-stu-id="d04a7-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="d04a7-245">Nākamajā tabulā ir parādītas transakcijas, kas tiek izveidotas katram abonementam, kurš ir pievienots abonementu grupai.</span><span class="sxs-lookup"><span data-stu-id="d04a7-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="d04a7-246">Projekta datums</span><span class="sxs-lookup"><span data-stu-id="d04a7-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="d04a7-247">Abonements</span><span class="sxs-lookup"><span data-stu-id="d04a7-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d04a7-248">Projekts</span><span class="sxs-lookup"><span data-stu-id="d04a7-248">Project</span></span></p></th>
<th><p><span data-ttu-id="d04a7-249">Kategorija</span><span class="sxs-lookup"><span data-stu-id="d04a7-249">Category</span></span></p></th>
<th><p><span data-ttu-id="d04a7-250">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="d04a7-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="d04a7-251">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="d04a7-251">End date</span></span></p></th>
<th><p><span data-ttu-id="d04a7-252">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="d04a7-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d04a7-253">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="d04a7-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d04a7-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="d04a7-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="d04a7-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="d04a7-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d04a7-256">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-256">9030</span></span></p></td>
<td><p><span data-ttu-id="d04a7-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d04a7-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d04a7-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="d04a7-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="d04a7-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="d04a7-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="d04a7-260">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-261">550</span><span class="sxs-lookup"><span data-stu-id="d04a7-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d04a7-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="d04a7-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="d04a7-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="d04a7-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d04a7-264">9030</span><span class="sxs-lookup"><span data-stu-id="d04a7-264">9030</span></span></p></td>
<td><p><span data-ttu-id="d04a7-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d04a7-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d04a7-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="d04a7-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="d04a7-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="d04a7-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="d04a7-268">EUR</span><span class="sxs-lookup"><span data-stu-id="d04a7-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="d04a7-269">500</span><span class="sxs-lookup"><span data-stu-id="d04a7-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d04a7-270">Pirmajā transakcijā abonementam 00020\_135 pārdošanas cena 550 EUR tiek atvasināta no abonementa pārdošanas cenas, kas ir iestatīta konkrētā projekta un kategorijas kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="d04a7-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="d04a7-271">Otrajā transakcijā abonementam 00021\_135 pārdošanas cena 500 EUR tiek izmantota kā projekta abonementa pārdošanas cena, jo projekta 9030 un kategorijas SubCat2 kombinācijai pārdošanas cena nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="d04a7-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="d04a7-272">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d04a7-272">See also</span></span>

[<span data-ttu-id="d04a7-273">Abonementu pārdošanas cenu atjaunināšana un indeksēšana</span><span class="sxs-lookup"><span data-stu-id="d04a7-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]