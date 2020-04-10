---
title: Divkāršās valūtas atbalsts nodokļiem
description: Šajā tēmā skaidrots, kā paplašināt divkāršas valūtu uzskaites funkciju nodokļu jomā, un ietekme uz nodokļu aprēķināšanu un grāmatošanu
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 863403dc3b2444f00f0cac27a494fc49d3d70de7
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161596"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="dc41e-103">Divkāršās valūtas atbalsts PVN</span><span class="sxs-lookup"><span data-stu-id="dc41e-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc41e-104">Šajā tēmā skaidrots, kā paplašināt divkāršas valūtu uzskaites attiecībā uz PVN, un ietekme uz PVN aprēķiniem, grāmatošanu un apmaksu.</span><span class="sxs-lookup"><span data-stu-id="dc41e-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="dc41e-105">Divkāršās valūtas līdzeklis programmai Dynamics 365 Finance tika ieviests versijā 8,1 (2018. gada oktobris).</span><span class="sxs-lookup"><span data-stu-id="dc41e-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="dc41e-106">Tas maina veidu, kādā tiek aprēķināti uzskaites ieraksti pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="dc41e-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="dc41e-107">Iepriekšējās versijās transakcijas tika konvertētas pārskata valūtā šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="dc41e-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="dc41e-108">Transakcijas kopsumma tika aprēķināta transakcijas valūtā > Transakcijas summa tika konvertēta uzskaites valūtā > Uzskaites valūtas summa tika konvertēta pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="dc41e-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="dc41e-109">Pēc divkāršās valūtas funkcijas iespējošanas transakcijas tika konvertētas pārskata valūtā šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="dc41e-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="dc41e-110">Transakcijas valūtas summa > Pārskata valūtas summa</span><span class="sxs-lookup"><span data-stu-id="dc41e-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="dc41e-111">Lai iegūtu vairāk informācijas par divkāršo valūtu, lūdzu, skatiet [Divkāršā valūta](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="dc41e-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="dc41e-112">Divkāršu valūtu atbalsta rezultātā ir pieejami divi jauni līdzekļi līdzekļu pārvaldībā:</span><span class="sxs-lookup"><span data-stu-id="dc41e-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="dc41e-113">PVN konvertēšana (laidiens versijā 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="dc41e-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="dc41e-114">Nodokļu apmaksas automātiskā bilance pārskata valūtā (laidiens versijā 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="dc41e-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="dc41e-115">Divkāršu valūtu atbalsts PVN nodrošina, ka nodokļi tiek aprēķināti precīzi nodokļu valūtā un ka PVN apmaksas bilance tiek aprēķināta precīzi gan uzskaites valūtā, gan pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="dc41e-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="dc41e-116">PVN konvertēšana</span><span class="sxs-lookup"><span data-stu-id="dc41e-116">Sales tax conversion</span></span>

<span data-ttu-id="dc41e-117">**PVN konvertēšanas** parametrs nodrošina divas opcijas nodokļa summas konvertēšanai no transakcijas valūtas nodokļa valūtā.</span><span class="sxs-lookup"><span data-stu-id="dc41e-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="dc41e-118">Uzskaites valūta: Ceļš būs "Summa transakcijas valūtā > Summa uzskaites valūtā > Summa nodokļa valūtā".</span><span class="sxs-lookup"><span data-stu-id="dc41e-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="dc41e-119">Valūtas konvertēšanai tiks izmantots uzskaites valūtas maiņas kursa tips (konfigurēts Virsgrāmatas uzstādījumos).</span><span class="sxs-lookup"><span data-stu-id="dc41e-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="dc41e-120">Pārskata valūta: Ceļš būs "Summa transakcijas valūtā > Summa pārskata valūtā > Summa nodokļa valūtā".</span><span class="sxs-lookup"><span data-stu-id="dc41e-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="dc41e-121">Valūtas konvertēšanai tiks izmantots pārskata valūtas maiņas kursa tips (konfigurēts Virsgrāmatas uzstādījumos).</span><span class="sxs-lookup"><span data-stu-id="dc41e-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="dc41e-122">Paraugs</span><span class="sxs-lookup"><span data-stu-id="dc41e-122">Example</span></span>

<span data-ttu-id="dc41e-123">Vienkāršs piemērs, lai parādītu šo funkcionalitāti:</span><span class="sxs-lookup"><span data-stu-id="dc41e-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="dc41e-124">Valūtas iestatījums virsgrāmatai un nodoklim</span><span class="sxs-lookup"><span data-stu-id="dc41e-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="dc41e-125">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-125">Transaction currency</span></span> | <span data-ttu-id="dc41e-126">Uzskaites valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-126">Accounting currency</span></span> | <span data-ttu-id="dc41e-127">Pārskata valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-127">Reporting currency</span></span> | <span data-ttu-id="dc41e-128">Nodokļu valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="dc41e-129">EUR</span><span class="sxs-lookup"><span data-stu-id="dc41e-129">EUR</span></span>                  | <span data-ttu-id="dc41e-130">USD</span><span class="sxs-lookup"><span data-stu-id="dc41e-130">USD</span></span>                 | <span data-ttu-id="dc41e-131">GBP</span><span class="sxs-lookup"><span data-stu-id="dc41e-131">GBP</span></span>                | <span data-ttu-id="dc41e-132">GBP</span><span class="sxs-lookup"><span data-stu-id="dc41e-132">GBP</span></span>          |

<span data-ttu-id="dc41e-133">Maiņas kurss</span><span class="sxs-lookup"><span data-stu-id="dc41e-133">Exchange rate</span></span>

| <span data-ttu-id="dc41e-134">No valūtas</span><span class="sxs-lookup"><span data-stu-id="dc41e-134">From currency</span></span> | <span data-ttu-id="dc41e-135">Uz valūtu</span><span class="sxs-lookup"><span data-stu-id="dc41e-135">To currency</span></span> | <span data-ttu-id="dc41e-136">Koeficients</span><span class="sxs-lookup"><span data-stu-id="dc41e-136">Factor</span></span> | <span data-ttu-id="dc41e-137">Maiņas kurss</span><span class="sxs-lookup"><span data-stu-id="dc41e-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="dc41e-138">EUR</span><span class="sxs-lookup"><span data-stu-id="dc41e-138">EUR</span></span>           | <span data-ttu-id="dc41e-139">USD</span><span class="sxs-lookup"><span data-stu-id="dc41e-139">USD</span></span>         | <span data-ttu-id="dc41e-140">1.</span><span class="sxs-lookup"><span data-stu-id="dc41e-140">1</span></span>      | <span data-ttu-id="dc41e-141">1.11</span><span class="sxs-lookup"><span data-stu-id="dc41e-141">1.11</span></span>          |
| <span data-ttu-id="dc41e-142">EUR</span><span class="sxs-lookup"><span data-stu-id="dc41e-142">EUR</span></span>           | <span data-ttu-id="dc41e-143">GBP</span><span class="sxs-lookup"><span data-stu-id="dc41e-143">GBP</span></span>         | <span data-ttu-id="dc41e-144">1.</span><span class="sxs-lookup"><span data-stu-id="dc41e-144">1</span></span>      | <span data-ttu-id="dc41e-145">0.83</span><span class="sxs-lookup"><span data-stu-id="dc41e-145">0.83</span></span>          |
| <span data-ttu-id="dc41e-146">USD</span><span class="sxs-lookup"><span data-stu-id="dc41e-146">USD</span></span>           | <span data-ttu-id="dc41e-147">GBP</span><span class="sxs-lookup"><span data-stu-id="dc41e-147">GBP</span></span>         | <span data-ttu-id="dc41e-148">1.</span><span class="sxs-lookup"><span data-stu-id="dc41e-148">1</span></span>      | <span data-ttu-id="dc41e-149">0.75</span><span class="sxs-lookup"><span data-stu-id="dc41e-149">0.75</span></span>          |

<span data-ttu-id="dc41e-150">Nodokļu summas aprēķināšana atšķirīgās parametru opcijās</span><span class="sxs-lookup"><span data-stu-id="dc41e-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="dc41e-151">Nodokļu summa = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="dc41e-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="dc41e-152">PVN konvertēšanas parametri</span><span class="sxs-lookup"><span data-stu-id="dc41e-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="dc41e-153">Transakcijas valūta (EUR)</span><span class="sxs-lookup"><span data-stu-id="dc41e-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="dc41e-154">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="dc41e-154">Accounting currency (USD)</span></span> | <span data-ttu-id="dc41e-155">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="dc41e-156">Nodokļa valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="dc41e-157">Uzskaites valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-157">Accounting currency</span></span>             | <span data-ttu-id="dc41e-158">100</span><span class="sxs-lookup"><span data-stu-id="dc41e-158">100</span></span>                        | <span data-ttu-id="dc41e-159">111</span><span class="sxs-lookup"><span data-stu-id="dc41e-159">111</span></span>                       | <span data-ttu-id="dc41e-160">83</span><span class="sxs-lookup"><span data-stu-id="dc41e-160">83</span></span>                       | <span data-ttu-id="dc41e-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="dc41e-161">**83.25**</span></span>          |
| <span data-ttu-id="dc41e-162">Pārskata valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-162">Reporting currency</span></span>              | <span data-ttu-id="dc41e-163">100</span><span class="sxs-lookup"><span data-stu-id="dc41e-163">100</span></span>                        | <span data-ttu-id="dc41e-164">111</span><span class="sxs-lookup"><span data-stu-id="dc41e-164">111</span></span>                       | <span data-ttu-id="dc41e-165">83</span><span class="sxs-lookup"><span data-stu-id="dc41e-165">83</span></span>                       | <span data-ttu-id="dc41e-166">**83**</span><span class="sxs-lookup"><span data-stu-id="dc41e-166">**83**</span></span>             |

<span data-ttu-id="dc41e-167">Šo parametru var konfigurēt, pamatojoties uz atbilstības nepieciešamību no nodokļu iestādes.</span><span class="sxs-lookup"><span data-stu-id="dc41e-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="dc41e-168">Atjaunināt apsvērumu</span><span class="sxs-lookup"><span data-stu-id="dc41e-168">Upgrade Consideration</span></span>

<span data-ttu-id="dc41e-169">Šis līdzeklis attieksies tikai uz jaunām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="dc41e-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="dc41e-170">Nodokļa transakcijai, kas jau ir saglabāta tabulā TAXTRANS, bet nav apmaksāta, sistēma neveiks nodokļu summas pārrēķinu nodokļu valūtā, jo nav norādīts valūtas maiņas kurss ar grāmatošanas nodokļa laika punktu.</span><span class="sxs-lookup"><span data-stu-id="dc41e-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="dc41e-171">Lai novērstu iepriekšējo scenāriju, ieteicams mainīt šo parametra vērtību jaunā (tīrā) nodokļu apmaksas periodā, kas nesatur neapmaksātas nodokļu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="dc41e-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="dc41e-172">Lai mainītu šo vērtību nodokļa apmaksas perioda vidū, pirms šī parametra vērtības maiņas, lūdzu, palaidiet "nosegt un grāmatot PVN" programmu pašreizējam nodokļu apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="dc41e-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="dc41e-173">Pārskata valūtas nodokļu summas izsekošana</span><span class="sxs-lookup"><span data-stu-id="dc41e-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="dc41e-174">Tika pievienoti trīs jauni lauki ar nodokļiem saistītām tabulām, lai izsekotu summas pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="dc41e-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="dc41e-175">Šie lauki atrodas tabulās TAXUNCOMMITTED un TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="dc41e-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="dc41e-176">TaxAmountRep: nodokļu summa pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="dc41e-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="dc41e-177">TaxAmountRep: bāzes summa pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="dc41e-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="dc41e-178">TaxInCostPriceRep: neapliekamā summa pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="dc41e-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="dc41e-179">Nodokļiem, kas saglabāti tikai TAXUNCOMMITTED tabulā, bet vēl nav grāmatoti, sistēma pārrēķinās nodokļu summu pārskata valūtā grāmatošanas laikā un saglabās TAXTRANS tabulā.</span><span class="sxs-lookup"><span data-stu-id="dc41e-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="dc41e-180">Šajā laidienā netiks iekļautas izmaiņas pārskatos un veidlapās, kas uzrāda nodokļa summu pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="dc41e-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="dc41e-181">Izmaiņas pārskatos un veidlapās tiks nodrošinātas nākotnes laidienos.</span><span class="sxs-lookup"><span data-stu-id="dc41e-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="dc41e-182">Nodokļu apmaksas automātiskā bilance pārskata valūtā</span><span class="sxs-lookup"><span data-stu-id="dc41e-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="dc41e-183">Ja nodokļu apmaksa nav kāda iemesla dēļ iekļauta pārskata valūtas bilancē, piemēram, PVN konvertēšanas ceļš ir "Uzskaites valūta", vai ir radušās maiņas kursa izmaiņas vienā nodokļu apmaksas periodā, sistēma automātiski ģenerēs uzskaites ierakstus, lai koriģētu nodokļu summas novirzi un to kompensētu ar realizēto valūtas peļņas/zaudējumu kontu, kas ir konfigurēts Virsgrāmatas iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="dc41e-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="dc41e-184">Izmantojot iepriekšējo piemēru, lai parādītu šo līdzekli, pieņemsim, ka tabulā TAXTRANS dati grāmatošanas laikā ir šādi.</span><span class="sxs-lookup"><span data-stu-id="dc41e-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="dc41e-185">PVN konvertēšanas parametri</span><span class="sxs-lookup"><span data-stu-id="dc41e-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="dc41e-186">Transakcijas valūta (EUR)</span><span class="sxs-lookup"><span data-stu-id="dc41e-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="dc41e-187">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="dc41e-187">Accounting currency (USD)</span></span> | <span data-ttu-id="dc41e-188">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="dc41e-189">Nodokļa valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="dc41e-190">Uzskaites valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-190">Accounting currency</span></span>             | <span data-ttu-id="dc41e-191">100</span><span class="sxs-lookup"><span data-stu-id="dc41e-191">100</span></span>                        | <span data-ttu-id="dc41e-192">111</span><span class="sxs-lookup"><span data-stu-id="dc41e-192">111</span></span>                       | <span data-ttu-id="dc41e-193">83</span><span class="sxs-lookup"><span data-stu-id="dc41e-193">83</span></span>                       | <span data-ttu-id="dc41e-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="dc41e-194">**83.25**</span></span>          |
| <span data-ttu-id="dc41e-195">Pārskata valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-195">Reporting currency</span></span>              | <span data-ttu-id="dc41e-196">100</span><span class="sxs-lookup"><span data-stu-id="dc41e-196">100</span></span>                        | <span data-ttu-id="dc41e-197">111</span><span class="sxs-lookup"><span data-stu-id="dc41e-197">111</span></span>                       | <span data-ttu-id="dc41e-198">83</span><span class="sxs-lookup"><span data-stu-id="dc41e-198">83</span></span>                       | <span data-ttu-id="dc41e-199">**83**</span><span class="sxs-lookup"><span data-stu-id="dc41e-199">**83**</span></span>             |

<span data-ttu-id="dc41e-200">Palaižot PVN apmaksas programmu mēneša beigās, uzskaites ieraksts būs šāds:.</span><span class="sxs-lookup"><span data-stu-id="dc41e-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="dc41e-201">Scenārijs: PVN konvertēšana = "Uzskaites valūta"</span><span class="sxs-lookup"><span data-stu-id="dc41e-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="dc41e-202">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="dc41e-202">Main account</span></span>           | <span data-ttu-id="dc41e-203">Transakcijas valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="dc41e-204">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="dc41e-204">Accounting currency (USD)</span></span> | <span data-ttu-id="dc41e-205">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="dc41e-206">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="dc41e-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="dc41e-207">-83.25</span><span class="sxs-lookup"><span data-stu-id="dc41e-207">-83.25</span></span>                     | <span data-ttu-id="dc41e-208">-111</span><span class="sxs-lookup"><span data-stu-id="dc41e-208">-111</span></span>                      | <span data-ttu-id="dc41e-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="dc41e-209">-83.25</span></span>                   |
| <span data-ttu-id="dc41e-210">Nodokļa apmaksa</span><span class="sxs-lookup"><span data-stu-id="dc41e-210">Tax Settlement</span></span>         | <span data-ttu-id="dc41e-211">83.25</span><span class="sxs-lookup"><span data-stu-id="dc41e-211">83.25</span></span>                      | <span data-ttu-id="dc41e-212">111</span><span class="sxs-lookup"><span data-stu-id="dc41e-212">111</span></span>                       | <span data-ttu-id="dc41e-213">83.25</span><span class="sxs-lookup"><span data-stu-id="dc41e-213">83.25</span></span>                    |
| <span data-ttu-id="dc41e-214">Realizētā peļņa / zaudējumi</span><span class="sxs-lookup"><span data-stu-id="dc41e-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="dc41e-215">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-215">0</span></span>                          | <span data-ttu-id="dc41e-216">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-216">0</span></span>                         | <span data-ttu-id="dc41e-217">-0.25</span><span class="sxs-lookup"><span data-stu-id="dc41e-217">-0.25</span></span>                    |
| <span data-ttu-id="dc41e-218">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="dc41e-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="dc41e-219">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-219">0</span></span>                          | <span data-ttu-id="dc41e-220">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-220">0</span></span>                         | <span data-ttu-id="dc41e-221">0.25</span><span class="sxs-lookup"><span data-stu-id="dc41e-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="dc41e-222">Scenārijs: PVN konvertēšana = "Pārskata valūta"</span><span class="sxs-lookup"><span data-stu-id="dc41e-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="dc41e-223">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="dc41e-223">Main account</span></span>           | <span data-ttu-id="dc41e-224">Transakcijas valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="dc41e-225">Uzskaites valūta (USD)</span><span class="sxs-lookup"><span data-stu-id="dc41e-225">Accounting currency (USD)</span></span> | <span data-ttu-id="dc41e-226">Pārskata valūta (GBP)</span><span class="sxs-lookup"><span data-stu-id="dc41e-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="dc41e-227">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="dc41e-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="dc41e-228">-83</span><span class="sxs-lookup"><span data-stu-id="dc41e-228">-83</span></span>                        | <span data-ttu-id="dc41e-229">-110.67</span><span class="sxs-lookup"><span data-stu-id="dc41e-229">-110.67</span></span>                   | <span data-ttu-id="dc41e-230">-83</span><span class="sxs-lookup"><span data-stu-id="dc41e-230">-83</span></span>                      |
| <span data-ttu-id="dc41e-231">Nodokļa apmaksa</span><span class="sxs-lookup"><span data-stu-id="dc41e-231">Tax Settlement</span></span>         | <span data-ttu-id="dc41e-232">83</span><span class="sxs-lookup"><span data-stu-id="dc41e-232">83</span></span>                         | <span data-ttu-id="dc41e-233">110.67</span><span class="sxs-lookup"><span data-stu-id="dc41e-233">110.67</span></span>                    | <span data-ttu-id="dc41e-234">83</span><span class="sxs-lookup"><span data-stu-id="dc41e-234">83</span></span>                       |
| <span data-ttu-id="dc41e-235">Realizētā peļņa / zaudējumi</span><span class="sxs-lookup"><span data-stu-id="dc41e-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="dc41e-236">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-236">0</span></span>                          | <span data-ttu-id="dc41e-237">0.33</span><span class="sxs-lookup"><span data-stu-id="dc41e-237">0.33</span></span>                      | <span data-ttu-id="dc41e-238">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-238">0</span></span>                        |
| <span data-ttu-id="dc41e-239">Maksājamais / saņemamais nodoklis</span><span class="sxs-lookup"><span data-stu-id="dc41e-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="dc41e-240">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-240">0</span></span>                          | <span data-ttu-id="dc41e-241">-0.33</span><span class="sxs-lookup"><span data-stu-id="dc41e-241">-0.33</span></span>                     | <span data-ttu-id="dc41e-242">0</span><span class="sxs-lookup"><span data-stu-id="dc41e-242">0</span></span>                        |



<span data-ttu-id="dc41e-243">Papildinformāciju skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="dc41e-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="dc41e-244">Divkāršā valūta</span><span class="sxs-lookup"><span data-stu-id="dc41e-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="dc41e-245">PVN pārskats</span><span class="sxs-lookup"><span data-stu-id="dc41e-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

