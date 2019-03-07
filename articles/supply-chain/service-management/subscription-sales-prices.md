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
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2019
ms.locfileid: "352164"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="5fba0-103">Abonementu pārdošanas cenas</span><span class="sxs-lookup"><span data-stu-id="5fba0-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5fba0-104">Kad veidojot abonementu, pārdošanas cena tiek atvasināta no pārdošanas cenas iestatījuma, kas bija izveidots formā **Pārdošanas cena (abonements)**.</span><span class="sxs-lookup"><span data-stu-id="5fba0-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="5fba0-105">Formā **Pārdošanas cena (abonements)** varat izveidot pārdošanas cenas konkrētam abonementam vai plašāk izmantojamas pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="5fba0-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="5fba0-106">Lai pārdošanas cenu lietotu kādam abonementam, šī abonementa perioda kodam un valūtai ir jābūt identiskiem ar attiecīgās pārdošanas cenas perioda kodu un valūtu.</span><span class="sxs-lookup"><span data-stu-id="5fba0-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="5fba0-107">Ja perioda kods un valūta gan abonementam, gan pārdošanas cenai ir identiski, abonementa pārdošanas cenas tiek atlasītas atkarībā no nākamajā tabulā norādītajām prioritātēm.</span><span class="sxs-lookup"><span data-stu-id="5fba0-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="5fba0-108">Tukša šūna tabulā nozīmē tukšu lauku, un atzīme X nozīmē, ka vērtība ir vienāda ar vērtību abonementā, no kura transakcija tiek ģenerēta.</span><span class="sxs-lookup"><span data-stu-id="5fba0-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="5fba0-109">Prioritāte</span><span class="sxs-lookup"><span data-stu-id="5fba0-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="5fba0-110"><strong>Kategorija</strong></span><span class="sxs-lookup"><span data-stu-id="5fba0-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="5fba0-111"><strong>Projekta ID</strong></span><span class="sxs-lookup"><span data-stu-id="5fba0-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="5fba0-112"><strong>Abonements</strong></span><span class="sxs-lookup"><span data-stu-id="5fba0-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="5fba0-113"><strong>Pārdošanas valūta</strong></span><span class="sxs-lookup"><span data-stu-id="5fba0-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="5fba0-114"><strong>Perioda kods</strong></span><span class="sxs-lookup"><span data-stu-id="5fba0-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-115">1</span><span class="sxs-lookup"><span data-stu-id="5fba0-115">1</span></span></p></td>
<td><p><span data-ttu-id="5fba0-116">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-116">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-117">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-117">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-118">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-118">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-119">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-119">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-120">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-121">2</span><span class="sxs-lookup"><span data-stu-id="5fba0-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-122">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-122">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-123">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-123">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-124">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-124">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-125">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-126">3</span><span class="sxs-lookup"><span data-stu-id="5fba0-126">3</span></span></p></td>
<td><p><span data-ttu-id="5fba0-127">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-128">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-128">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-129">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-129">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-130">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-131">4</span><span class="sxs-lookup"><span data-stu-id="5fba0-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-132">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-132">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-133">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-133">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-134">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-135">5</span><span class="sxs-lookup"><span data-stu-id="5fba0-135">5</span></span></p></td>
<td><p><span data-ttu-id="5fba0-136">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-136">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-137">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-138">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-138">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-139">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-140">6</span><span class="sxs-lookup"><span data-stu-id="5fba0-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-141">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-142">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-142">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-143">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-144">7</span><span class="sxs-lookup"><span data-stu-id="5fba0-144">7</span></span></p></td>
<td><p><span data-ttu-id="5fba0-145">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-146">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-146">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-147">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-148">8</span><span class="sxs-lookup"><span data-stu-id="5fba0-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5fba0-149">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-149">X</span></span></p></td>
<td><p><span data-ttu-id="5fba0-150">X</span><span class="sxs-lookup"><span data-stu-id="5fba0-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5fba0-151">Kad tiek izveidota abonēšanas maksa, par abonementa pārdošanas cenu tiek atlasīta pārdošanas cena ar augstāko detalizācijas līmeni (kā norādīts iepriekš redzamajā tabulā).</span><span class="sxs-lookup"><span data-stu-id="5fba0-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="5fba0-152">Abonementu pārdošanas cenu atjaunināšana un indeksēšana</span><span class="sxs-lookup"><span data-stu-id="5fba0-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="5fba0-153">Abonementa pārdošanas cenu var atjaunināt, atjauninot pamatcenu vai indeksu.</span><span class="sxs-lookup"><span data-stu-id="5fba0-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="5fba0-154">Atjaunināt var par procentuālu daudzumu vai uz jaunu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5fba0-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="5fba0-155">Abonēšanas maksas pārdošanas cenas</span><span class="sxs-lookup"><span data-stu-id="5fba0-155">Subscription fee sales prices</span></span>

<span data-ttu-id="5fba0-156">Veidojot abonēšanas maksu, pārdošanas cena ir atkarīga no abonementam iestatītās pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="5fba0-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="5fba0-157">Varat izmantot pamatcenu no abonementa cenas iestatījuma vai izveidot indeksētas pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="5fba0-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="5fba0-158">Piemērs</span><span class="sxs-lookup"><span data-stu-id="5fba0-158">Example</span></span>

<span data-ttu-id="5fba0-159">Jūs jaunam projektam 9030 vēlaties iestatīt abonementa pārdošanas cenas EUR 500 vērtībā.</span><span class="sxs-lookup"><span data-stu-id="5fba0-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="5fba0-160">Formā **Pārdošanas cena (abonements)** jūs izveidojat abonementa pārdošanas cenas rindu, kā noradīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="5fba0-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="5fba0-161">Derīgs no</span><span class="sxs-lookup"><span data-stu-id="5fba0-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="5fba0-162">Kategorija</span><span class="sxs-lookup"><span data-stu-id="5fba0-162">Category</span></span></p></th>
<th><p><span data-ttu-id="5fba0-163">Projekts</span><span class="sxs-lookup"><span data-stu-id="5fba0-163">Project</span></span></p></th>
<th><p><span data-ttu-id="5fba0-164">Abonements</span><span class="sxs-lookup"><span data-stu-id="5fba0-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="5fba0-165">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="5fba0-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="5fba0-166">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="5fba0-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="5fba0-167">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="5fba0-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="5fba0-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5fba0-169">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5fba0-170">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="5fba0-170">Month</span></span></p></td>
<td><p><span data-ttu-id="5fba0-171">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-172">500</span><span class="sxs-lookup"><span data-stu-id="5fba0-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5fba0-173">Pievērsiet uzmanību, ka lauki **Kategorija** un **Abonements** ir tukši.</span><span class="sxs-lookup"><span data-stu-id="5fba0-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="5fba0-174">Pēc tam jūs izveidojat tālāk norādītos abonementus.</span><span class="sxs-lookup"><span data-stu-id="5fba0-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="5fba0-175">Pakalpojuma abonements</span><span class="sxs-lookup"><span data-stu-id="5fba0-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="5fba0-176">Projekts</span><span class="sxs-lookup"><span data-stu-id="5fba0-176">Project</span></span></p></th>
<th><p><span data-ttu-id="5fba0-177">Abonementu grupa</span><span class="sxs-lookup"><span data-stu-id="5fba0-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="5fba0-178">Kategorija</span><span class="sxs-lookup"><span data-stu-id="5fba0-178">Category</span></span></p></th>
<th><p><span data-ttu-id="5fba0-179">Valūta</span><span class="sxs-lookup"><span data-stu-id="5fba0-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="5fba0-180">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="5fba0-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="5fba0-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="5fba0-182">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-182">9030</span></span></p></td>
<td><p><span data-ttu-id="5fba0-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="5fba0-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="5fba0-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="5fba0-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="5fba0-185">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-186">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="5fba0-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="5fba0-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="5fba0-188">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-188">9030</span></span></p></td>
<td><p><span data-ttu-id="5fba0-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="5fba0-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="5fba0-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="5fba0-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="5fba0-191">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-192">Reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="5fba0-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5fba0-193">Tagad jūs izveidojat abonēšanas maksas abiem abonementiem abonementu grupā Sub1:</span><span class="sxs-lookup"><span data-stu-id="5fba0-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="5fba0-194">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.</span><span class="sxs-lookup"><span data-stu-id="5fba0-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="5fba0-195">Formā **Abonementu grupas** noklikšķiniet uz **Funkcija** \> **Izveidot abonēšanas maksu**.</span><span class="sxs-lookup"><span data-stu-id="5fba0-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="5fba0-196">Formā **Izveidot abonēšanas maksu** ievadiet atbilstošo informāciju.</span><span class="sxs-lookup"><span data-stu-id="5fba0-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="5fba0-197">Plašāku informāciju skatiet tēmā [Abonēšanas maksu transakciju izveidošana](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="5fba0-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="5fba0-198">Abiem abonementiem tiek izveidotas abonēšanas maksas, kam ir pārdošanas cena 500 EUR, kā parādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="5fba0-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="5fba0-199">Projekta datums</span><span class="sxs-lookup"><span data-stu-id="5fba0-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="5fba0-200">Pakalpojuma abonements</span><span class="sxs-lookup"><span data-stu-id="5fba0-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="5fba0-201">Projekts</span><span class="sxs-lookup"><span data-stu-id="5fba0-201">Project</span></span></p></th>
<th><p><span data-ttu-id="5fba0-202">Kategorija</span><span class="sxs-lookup"><span data-stu-id="5fba0-202">Category</span></span></p></th>
<th><p><span data-ttu-id="5fba0-203">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="5fba0-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="5fba0-204">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="5fba0-204">End date</span></span></p></th>
<th><p><span data-ttu-id="5fba0-205">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="5fba0-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="5fba0-206">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="5fba0-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="5fba0-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="5fba0-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="5fba0-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="5fba0-209">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-209">9030</span></span></p></td>
<td><p><span data-ttu-id="5fba0-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="5fba0-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="5fba0-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="5fba0-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="5fba0-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="5fba0-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="5fba0-213">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-214">500</span><span class="sxs-lookup"><span data-stu-id="5fba0-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="5fba0-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="5fba0-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="5fba0-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="5fba0-217">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-217">9030</span></span></p></td>
<td><p><span data-ttu-id="5fba0-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="5fba0-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="5fba0-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="5fba0-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="5fba0-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="5fba0-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="5fba0-221">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-222">500</span><span class="sxs-lookup"><span data-stu-id="5fba0-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5fba0-223">Vēlāk jūs izlemjat, ka vēlaties norādīt pārdošanas cenas projekta 9030 kategorijai SubCat1.</span><span class="sxs-lookup"><span data-stu-id="5fba0-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="5fba0-224">Tāpēc jūs izveidojat jaunu pārdošanas cenu rindu, kuras pārdošanas cena ir 550 EUR projekta 9030 un maksu kategorijas SubCat1 kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="5fba0-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="5fba0-225">Tagad projektam 9030 ir divas abonementa pārdošanas cenu rindas, kā parādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="5fba0-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="5fba0-226">Derīgs no</span><span class="sxs-lookup"><span data-stu-id="5fba0-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="5fba0-227">Kategorija</span><span class="sxs-lookup"><span data-stu-id="5fba0-227">Category</span></span></p></th>
<th><p><span data-ttu-id="5fba0-228">Projekts</span><span class="sxs-lookup"><span data-stu-id="5fba0-228">Project</span></span></p></th>
<th><p><span data-ttu-id="5fba0-229">Abonements</span><span class="sxs-lookup"><span data-stu-id="5fba0-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="5fba0-230">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="5fba0-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="5fba0-231">Valūta</span><span class="sxs-lookup"><span data-stu-id="5fba0-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="5fba0-232">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="5fba0-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="5fba0-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5fba0-234">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5fba0-235">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="5fba0-235">Month</span></span></p></td>
<td><p><span data-ttu-id="5fba0-236">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-237">500</span><span class="sxs-lookup"><span data-stu-id="5fba0-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="5fba0-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="5fba0-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="5fba0-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="5fba0-240">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5fba0-241">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="5fba0-241">Month</span></span></p></td>
<td><p><span data-ttu-id="5fba0-242">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-243">550</span><span class="sxs-lookup"><span data-stu-id="5fba0-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5fba0-244">Jūs atkārtojat iepriekš aprakstīto procedūru, lai izveidotu abonēšanas maksas abiem abonementiem abonementu grupā Sub1.</span><span class="sxs-lookup"><span data-stu-id="5fba0-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="5fba0-245">Nākamajā tabulā ir parādītas transakcijas, kas tiek izveidotas katram abonementam, kurš ir pievienots abonementu grupai.</span><span class="sxs-lookup"><span data-stu-id="5fba0-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="5fba0-246">Projekta datums</span><span class="sxs-lookup"><span data-stu-id="5fba0-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="5fba0-247">Abonements</span><span class="sxs-lookup"><span data-stu-id="5fba0-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="5fba0-248">Projekts</span><span class="sxs-lookup"><span data-stu-id="5fba0-248">Project</span></span></p></th>
<th><p><span data-ttu-id="5fba0-249">Kategorija</span><span class="sxs-lookup"><span data-stu-id="5fba0-249">Category</span></span></p></th>
<th><p><span data-ttu-id="5fba0-250">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="5fba0-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="5fba0-251">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="5fba0-251">End date</span></span></p></th>
<th><p><span data-ttu-id="5fba0-252">Pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="5fba0-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="5fba0-253">Pārdošanas cena</span><span class="sxs-lookup"><span data-stu-id="5fba0-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fba0-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="5fba0-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="5fba0-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="5fba0-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="5fba0-256">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-256">9030</span></span></p></td>
<td><p><span data-ttu-id="5fba0-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="5fba0-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="5fba0-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="5fba0-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="5fba0-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="5fba0-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="5fba0-260">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-261">550</span><span class="sxs-lookup"><span data-stu-id="5fba0-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fba0-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="5fba0-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="5fba0-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="5fba0-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="5fba0-264">9030</span><span class="sxs-lookup"><span data-stu-id="5fba0-264">9030</span></span></p></td>
<td><p><span data-ttu-id="5fba0-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="5fba0-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="5fba0-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="5fba0-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="5fba0-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="5fba0-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="5fba0-268">EUR</span><span class="sxs-lookup"><span data-stu-id="5fba0-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="5fba0-269">500</span><span class="sxs-lookup"><span data-stu-id="5fba0-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5fba0-270">Pirmajā transakcijā abonementam 00020\_135 pārdošanas cena 550 EUR tiek atvasināta no abonementa pārdošanas cenas, kas ir iestatīta konkrētā projekta un kategorijas kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="5fba0-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="5fba0-271">Otrajā transakcijā abonementam 00021\_135 pārdošanas cena 500 EUR tiek izmantota kā projekta abonementa pārdošanas cena, jo projekta 9030 un kategorijas SubCat2 kombinācijai pārdošanas cena nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="5fba0-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fba0-272">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="5fba0-272">See also</span></span>

[<span data-ttu-id="5fba0-273">Abonementu pārdošanas cenu atjaunināšana un indeksēšana</span><span class="sxs-lookup"><span data-stu-id="5fba0-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


