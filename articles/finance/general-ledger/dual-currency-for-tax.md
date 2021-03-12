---
title: Divkāršās valūtas atbalsts nodokļiem
description: Šajā tēmā skaidrots, kā paplašināt divkāršas valūtu uzskaites funkciju nodokļu jomā, un ietekme uz nodokļu aprēķināšanu un grāmatošanu
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2e3e7ff93ca3c6a2266ba0f33c8eac7ceade0d4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978608"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="bc2a2-103">Divkāršās valūtas atbalsts PVN</span><span class="sxs-lookup"><span data-stu-id="bc2a2-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc2a2-104">Šajā tēmā skaidrots, kā paplašināt divkāršas valūtu uzskaites attiecībā uz PVN, un ietekme uz PVN aprēķiniem, grāmatošanu un apmaksu.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="bc2a2-105">Divkāršās valūtas līdzeklis programmai Dynamics 365 Finance tika ieviests versijā 8,1 (2018. gada oktobris).</span><span class="sxs-lookup"><span data-stu-id="bc2a2-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="bc2a2-106">Tas maina veidu, kādā tiek aprēķināti uzskaites ieraksti pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="bc2a2-107">Iepriekšējās versijās transakcijas tika konvertētas pārskata valūtā šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="bc2a2-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="bc2a2-108">Transakcijas kopsumma tika aprēķināta transakcijas valūtā > Transakcijas summa tika konvertēta uzskaites valūtā > Uzskaites valūtas summa tika konvertēta pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="bc2a2-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="bc2a2-109">Pēc divkāršās valūtas funkcijas iespējošanas transakcijas tika konvertētas pārskata valūtā šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="bc2a2-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="bc2a2-110">Transakcijas valūtas summa > Pārskata valūtas summa</span><span class="sxs-lookup"><span data-stu-id="bc2a2-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="bc2a2-111">Lai iegūtu vairāk informācijas par divkāršo valūtu, lūdzu, skatiet [Divkāršā valūta](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="bc2a2-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="bc2a2-112">Divkāršu valūtu atbalsta rezultātā ir pieejami divi jauni līdzekļi līdzekļu pārvaldībā:</span><span class="sxs-lookup"><span data-stu-id="bc2a2-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="bc2a2-113">PVN konvertēšana (jauns versijā 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="bc2a2-114">Divkāršu valūtu atbalsts PVN nodrošina, ka nodokļi tiek aprēķināti precīzi nodokļu valūtā un ka PVN apmaksas bilance tiek aprēķināta precīzi gan uzskaites valūtā, gan pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="bc2a2-115">PVN konvertēšana</span><span class="sxs-lookup"><span data-stu-id="bc2a2-115">Sales tax conversion</span></span>

<span data-ttu-id="bc2a2-116">**PVN konvertēšanas** parametrs nodrošina divas opcijas nodokļa summas konvertēšanai no transakcijas valūtas nodokļa valūtā.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="bc2a2-117">Uzskaites valūta: Ceļš būs "Summa transakcijas valūtā > Summa uzskaites valūtā > Summa nodokļa valūtā".</span><span class="sxs-lookup"><span data-stu-id="bc2a2-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="bc2a2-118">Valūtas konvertēšanai tiks izmantots uzskaites valūtas maiņas kursa tips (konfigurēts Virsgrāmatas uzstādījumos).</span><span class="sxs-lookup"><span data-stu-id="bc2a2-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="bc2a2-119">Pārskata valūta: Ceļš būs "Summa transakcijas valūtā > Summa pārskata valūtā > Summa nodokļa valūtā".</span><span class="sxs-lookup"><span data-stu-id="bc2a2-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="bc2a2-120">Valūtas konvertēšanai tiks izmantots pārskata valūtas maiņas kursa tips (konfigurēts Virsgrāmatas uzstādījumos).</span><span class="sxs-lookup"><span data-stu-id="bc2a2-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="bc2a2-121">Paraugs</span><span class="sxs-lookup"><span data-stu-id="bc2a2-121">Example</span></span>

<span data-ttu-id="bc2a2-122">Vienkāršs piemērs, lai parādītu šo funkcionalitāti:</span><span class="sxs-lookup"><span data-stu-id="bc2a2-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="bc2a2-123">Valūtas iestatījums virsgrāmatai un nodoklim</span><span class="sxs-lookup"><span data-stu-id="bc2a2-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="bc2a2-124">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-124">Transaction currency</span></span> | <span data-ttu-id="bc2a2-125">Uzskaites valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-125">Accounting currency</span></span> | <span data-ttu-id="bc2a2-126">Pārskata valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-126">Reporting currency</span></span> | <span data-ttu-id="bc2a2-127">Nodokļu valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="bc2a2-128">EUR</span><span class="sxs-lookup"><span data-stu-id="bc2a2-128">EUR</span></span>                  | <span data-ttu-id="bc2a2-129">USD</span><span class="sxs-lookup"><span data-stu-id="bc2a2-129">USD</span></span>                 | <span data-ttu-id="bc2a2-130">GBP</span><span class="sxs-lookup"><span data-stu-id="bc2a2-130">GBP</span></span>                | <span data-ttu-id="bc2a2-131">GBP</span><span class="sxs-lookup"><span data-stu-id="bc2a2-131">GBP</span></span>          |

<span data-ttu-id="bc2a2-132">Maiņas kurss</span><span class="sxs-lookup"><span data-stu-id="bc2a2-132">Exchange rate</span></span>

| <span data-ttu-id="bc2a2-133">No valūtas</span><span class="sxs-lookup"><span data-stu-id="bc2a2-133">From currency</span></span> | <span data-ttu-id="bc2a2-134">Uz valūtu</span><span class="sxs-lookup"><span data-stu-id="bc2a2-134">To currency</span></span> | <span data-ttu-id="bc2a2-135">Koeficients</span><span class="sxs-lookup"><span data-stu-id="bc2a2-135">Factor</span></span> | <span data-ttu-id="bc2a2-136">Maiņas kurss</span><span class="sxs-lookup"><span data-stu-id="bc2a2-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="bc2a2-137">EUR</span><span class="sxs-lookup"><span data-stu-id="bc2a2-137">EUR</span></span>           | <span data-ttu-id="bc2a2-138">USD</span><span class="sxs-lookup"><span data-stu-id="bc2a2-138">USD</span></span>         | <span data-ttu-id="bc2a2-139">1.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-139">1</span></span>      | <span data-ttu-id="bc2a2-140">1.11</span><span class="sxs-lookup"><span data-stu-id="bc2a2-140">1.11</span></span>          |
| <span data-ttu-id="bc2a2-141">EUR</span><span class="sxs-lookup"><span data-stu-id="bc2a2-141">EUR</span></span>           | <span data-ttu-id="bc2a2-142">GBP</span><span class="sxs-lookup"><span data-stu-id="bc2a2-142">GBP</span></span>         | <span data-ttu-id="bc2a2-143">1.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-143">1</span></span>      | <span data-ttu-id="bc2a2-144">0.83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-144">0.83</span></span>          |
| <span data-ttu-id="bc2a2-145">USD</span><span class="sxs-lookup"><span data-stu-id="bc2a2-145">USD</span></span>           | <span data-ttu-id="bc2a2-146">GBP</span><span class="sxs-lookup"><span data-stu-id="bc2a2-146">GBP</span></span>         | <span data-ttu-id="bc2a2-147">1.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-147">1</span></span>      | <span data-ttu-id="bc2a2-148">0.75</span><span class="sxs-lookup"><span data-stu-id="bc2a2-148">0.75</span></span>          |

<span data-ttu-id="bc2a2-149">Nodokļu summas aprēķināšana atšķirīgās parametru opcijās</span><span class="sxs-lookup"><span data-stu-id="bc2a2-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="bc2a2-150">Nodokļu summa = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="bc2a2-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="bc2a2-151">PVN konvertēšanas parametri</span><span class="sxs-lookup"><span data-stu-id="bc2a2-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="bc2a2-152">Transakcijas valūta (EUR)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="bc2a2-153">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-153">Accounting currency (USD)</span></span> | <span data-ttu-id="bc2a2-154">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="bc2a2-155">Nodokļa valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="bc2a2-156">Uzskaites valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-156">Accounting currency</span></span>             | <span data-ttu-id="bc2a2-157">100</span><span class="sxs-lookup"><span data-stu-id="bc2a2-157">100</span></span>                        | <span data-ttu-id="bc2a2-158">111</span><span class="sxs-lookup"><span data-stu-id="bc2a2-158">111</span></span>                       | <span data-ttu-id="bc2a2-159">83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-159">83</span></span>                       | <span data-ttu-id="bc2a2-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="bc2a2-160">**83.25**</span></span>          |
| <span data-ttu-id="bc2a2-161">Pārskata valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-161">Reporting currency</span></span>              | <span data-ttu-id="bc2a2-162">100</span><span class="sxs-lookup"><span data-stu-id="bc2a2-162">100</span></span>                        | <span data-ttu-id="bc2a2-163">111</span><span class="sxs-lookup"><span data-stu-id="bc2a2-163">111</span></span>                       | <span data-ttu-id="bc2a2-164">83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-164">83</span></span>                       | <span data-ttu-id="bc2a2-165">**83**</span><span class="sxs-lookup"><span data-stu-id="bc2a2-165">**83**</span></span>             |

<span data-ttu-id="bc2a2-166">Šo parametru var konfigurēt, pamatojoties uz atbilstības nepieciešamību no nodokļu iestādes.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="bc2a2-167">Atjaunināt apsvērumu</span><span class="sxs-lookup"><span data-stu-id="bc2a2-167">Upgrade Consideration</span></span>

<span data-ttu-id="bc2a2-168">Šis līdzeklis attieksies tikai uz jaunām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="bc2a2-169">Nodokļa transakcijai, kas jau ir saglabāta tabulā TAXTRANS, bet nav apmaksāta, sistēma neveiks nodokļu summas pārrēķinu nodokļu valūtā, jo nav norādīts valūtas maiņas kurss ar grāmatošanas nodokļa laika punktu.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="bc2a2-170">Lai novērstu iepriekšējo scenāriju, ieteicams mainīt šo parametra vērtību jaunā (tīrā) nodokļu apmaksas periodā, kas nesatur neapmaksātas nodokļu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="bc2a2-171">Lai mainītu šo vērtību nodokļa apmaksas perioda vidū, pirms šī parametra vērtības maiņas, lūdzu, palaidiet "nosegt un grāmatot PVN" programmu pašreizējam nodokļu apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="bc2a2-172">Pārskata valūtas nodokļu summas izsekošana</span><span class="sxs-lookup"><span data-stu-id="bc2a2-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="bc2a2-173">Tika pievienoti trīs jauni lauki ar nodokļiem saistītām tabulām, lai izsekotu summas pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="bc2a2-174">Šie lauki atrodas tabulās TAXUNCOMMITTED un TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="bc2a2-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="bc2a2-175">TaxAmountRep: nodokļu summa pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="bc2a2-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="bc2a2-176">TaxAmountRep: bāzes summa pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="bc2a2-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="bc2a2-177">TaxInCostPriceRep: neapliekamā summa pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="bc2a2-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="bc2a2-178">Nodokļiem, kas saglabāti tikai TAXUNCOMMITTED tabulā, bet vēl nav grāmatoti, sistēma pārrēķinās nodokļu summu pārskata valūtā grāmatošanas laikā un saglabās TAXTRANS tabulā.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="bc2a2-179">Šajā laidienā netiks iekļautas izmaiņas pārskatos un veidlapās, kas uzrāda nodokļa summu pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="bc2a2-180">Izmaiņas pārskatos un veidlapās tiks nodrošinātas nākotnes laidienos.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="bc2a2-181">Nodokļu apmaksas automātiskā bilance pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="bc2a2-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="bc2a2-182">Ja nodokļu apmaksa nav kāda iemesla dēļ iekļauta pārskata valūtas bilancē, piemēram, PVN konvertēšanas ceļš ir "Uzskaites valūta", vai ir radušās maiņas kursa izmaiņas vienā nodokļu apmaksas periodā, sistēma automātiski ģenerēs uzskaites ierakstus, lai koriģētu nodokļu summas novirzi un to kompensētu ar realizēto valūtas peļņas/zaudējumu kontu, kas ir konfigurēts Virsgrāmatas iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="bc2a2-183">Izmantojot iepriekšējo piemēru, lai parādītu šo līdzekli, pieņemsim, ka tabulā TAXTRANS dati grāmatošanas laikā ir šādi.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="bc2a2-184">PVN konvertēšanas parametri</span><span class="sxs-lookup"><span data-stu-id="bc2a2-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="bc2a2-185">Transakcijas valūta (EUR)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="bc2a2-186">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-186">Accounting currency (USD)</span></span> | <span data-ttu-id="bc2a2-187">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="bc2a2-188">Nodokļa valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="bc2a2-189">Uzskaites valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-189">Accounting currency</span></span>             | <span data-ttu-id="bc2a2-190">100</span><span class="sxs-lookup"><span data-stu-id="bc2a2-190">100</span></span>                        | <span data-ttu-id="bc2a2-191">111</span><span class="sxs-lookup"><span data-stu-id="bc2a2-191">111</span></span>                       | <span data-ttu-id="bc2a2-192">83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-192">83</span></span>                       | <span data-ttu-id="bc2a2-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="bc2a2-193">**83.25**</span></span>          |
| <span data-ttu-id="bc2a2-194">Pārskata valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-194">Reporting currency</span></span>              | <span data-ttu-id="bc2a2-195">100</span><span class="sxs-lookup"><span data-stu-id="bc2a2-195">100</span></span>                        | <span data-ttu-id="bc2a2-196">111</span><span class="sxs-lookup"><span data-stu-id="bc2a2-196">111</span></span>                       | <span data-ttu-id="bc2a2-197">83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-197">83</span></span>                       | <span data-ttu-id="bc2a2-198">**83**</span><span class="sxs-lookup"><span data-stu-id="bc2a2-198">**83**</span></span>             |

<span data-ttu-id="bc2a2-199">Palaižot PVN apmaksas programmu mēneša beigās, uzskaites ieraksts būs šāds:.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="bc2a2-200">Scenārijs: PVN konvertēšana = "Uzskaites valūta"</span><span class="sxs-lookup"><span data-stu-id="bc2a2-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="bc2a2-201">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="bc2a2-201">Main account</span></span>           | <span data-ttu-id="bc2a2-202">Transakcijas valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="bc2a2-203">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-203">Accounting currency (USD)</span></span> | <span data-ttu-id="bc2a2-204">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="bc2a2-205">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="bc2a2-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="bc2a2-206">-83.25</span><span class="sxs-lookup"><span data-stu-id="bc2a2-206">-83.25</span></span>                     | <span data-ttu-id="bc2a2-207">-111</span><span class="sxs-lookup"><span data-stu-id="bc2a2-207">-111</span></span>                      | <span data-ttu-id="bc2a2-208">-83.25</span><span class="sxs-lookup"><span data-stu-id="bc2a2-208">-83.25</span></span>                   |
| <span data-ttu-id="bc2a2-209">Nodokļa apmaksa</span><span class="sxs-lookup"><span data-stu-id="bc2a2-209">Tax Settlement</span></span>         | <span data-ttu-id="bc2a2-210">83.25</span><span class="sxs-lookup"><span data-stu-id="bc2a2-210">83.25</span></span>                      | <span data-ttu-id="bc2a2-211">111</span><span class="sxs-lookup"><span data-stu-id="bc2a2-211">111</span></span>                       | <span data-ttu-id="bc2a2-212">83.25</span><span class="sxs-lookup"><span data-stu-id="bc2a2-212">83.25</span></span>                    |
| <span data-ttu-id="bc2a2-213">Realizētā peļņa / zaudējumi</span><span class="sxs-lookup"><span data-stu-id="bc2a2-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="bc2a2-214">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-214">0</span></span>                          | <span data-ttu-id="bc2a2-215">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-215">0</span></span>                         | <span data-ttu-id="bc2a2-216">-0.25</span><span class="sxs-lookup"><span data-stu-id="bc2a2-216">-0.25</span></span>                    |
| <span data-ttu-id="bc2a2-217">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="bc2a2-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="bc2a2-218">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-218">0</span></span>                          | <span data-ttu-id="bc2a2-219">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-219">0</span></span>                         | <span data-ttu-id="bc2a2-220">0.25</span><span class="sxs-lookup"><span data-stu-id="bc2a2-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="bc2a2-221">Scenārijs: PVN konvertēšana = "Pārskata valūta"</span><span class="sxs-lookup"><span data-stu-id="bc2a2-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="bc2a2-222">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="bc2a2-222">Main account</span></span>           | <span data-ttu-id="bc2a2-223">Transakcijas valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="bc2a2-224">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-224">Accounting currency (USD)</span></span> | <span data-ttu-id="bc2a2-225">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="bc2a2-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="bc2a2-226">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="bc2a2-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="bc2a2-227">-83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-227">-83</span></span>                        | <span data-ttu-id="bc2a2-228">-110.67</span><span class="sxs-lookup"><span data-stu-id="bc2a2-228">-110.67</span></span>                   | <span data-ttu-id="bc2a2-229">-83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-229">-83</span></span>                      |
| <span data-ttu-id="bc2a2-230">Nodokļa apmaksa</span><span class="sxs-lookup"><span data-stu-id="bc2a2-230">Tax Settlement</span></span>         | <span data-ttu-id="bc2a2-231">83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-231">83</span></span>                         | <span data-ttu-id="bc2a2-232">110.67</span><span class="sxs-lookup"><span data-stu-id="bc2a2-232">110.67</span></span>                    | <span data-ttu-id="bc2a2-233">83</span><span class="sxs-lookup"><span data-stu-id="bc2a2-233">83</span></span>                       |
| <span data-ttu-id="bc2a2-234">Realizētā peļņa / zaudējumi</span><span class="sxs-lookup"><span data-stu-id="bc2a2-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="bc2a2-235">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-235">0</span></span>                          | <span data-ttu-id="bc2a2-236">0.33</span><span class="sxs-lookup"><span data-stu-id="bc2a2-236">0.33</span></span>                      | <span data-ttu-id="bc2a2-237">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-237">0</span></span>                        |
| <span data-ttu-id="bc2a2-238">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="bc2a2-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="bc2a2-239">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-239">0</span></span>                          | <span data-ttu-id="bc2a2-240">-0.33</span><span class="sxs-lookup"><span data-stu-id="bc2a2-240">-0.33</span></span>                     | <span data-ttu-id="bc2a2-241">0</span><span class="sxs-lookup"><span data-stu-id="bc2a2-241">0</span></span>                        |



<span data-ttu-id="bc2a2-242">Papildinformāciju skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="bc2a2-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="bc2a2-243">Divkāršā valūta</span><span class="sxs-lookup"><span data-stu-id="bc2a2-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="bc2a2-244">PVN pārskats</span><span class="sxs-lookup"><span data-stu-id="bc2a2-244">Sales tax overview</span></span>](indirect-taxes-overview.md)

