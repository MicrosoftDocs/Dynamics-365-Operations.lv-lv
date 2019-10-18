---
title: Debitoru grāmatošanas metodes
description: Debitoru grāmatošanas profili kontrolē debitoru transakciju grāmatošanu virsgrāmatā.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb2784d70e99c3c3443bed1b8cb040552b5b6f6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189066"
---
# <a name="customer-posting-profiles"></a><span data-ttu-id="4d673-103">Debitoru grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="4d673-103">Customer posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d673-104">Debitoru grāmatošanas profili kontrolē debitoru transakciju grāmatošanu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="4d673-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="4d673-105">Debitoru grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="4d673-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="4d673-106">Debitoru grāmatošanas metodes jums ļauj virsgrāmatas kontus un dokumentu iestatījumus piešķirt visiem debitoriem, debitoru grupai vai atsevišķam debitoram.</span><span class="sxs-lookup"><span data-stu-id="4d673-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="4d673-107">Šie iestatījumi tiks lietoti, kad veidojat pārdošanas pasūtījumus, brīva teksta rēķinus, maksājumus skaidrā naudā, atgādinājuma vēstules un procentu paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="4d673-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="4d673-108">Noteiktām transakcijām varat atlasīt grāmatošanas metodi, kas atšķiras no šajā lapā iestatītajām transakciju grāmatošanas metodēm un kam ir prioritāte pār tām.</span><span class="sxs-lookup"><span data-stu-id="4d673-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="4d673-109">Noklusējuma grāmatošanas metode tiek definēta kopsavilkuma cilnē Virsgrāmata un Pārdošanas nodoklis, lapā Debitoru moduļa parametri.</span><span class="sxs-lookup"><span data-stu-id="4d673-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="4d673-110">Noklusējuma grāmatošanas metode pēc tam automātiski tiek iekļauta jaunu dokumentu virsrakstā, kur to varat mainīt uz citu grāmatošanas metodi, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="4d673-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="4d673-111">Grāmatošanas definīcijas varat arī saistīt ar transakciju grāmatošanas tipiem lapā Transakciju grāmatošanas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="4d673-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="4d673-112">Grāmatošanas definīcijas kontrolē debitoru transakciju grāmatošanu virsgrāmatā grāmatošanas metožu vietā.</span><span class="sxs-lookup"><span data-stu-id="4d673-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="4d673-113">Grāmatošanas metodes izveidošana</span><span class="sxs-lookup"><span data-stu-id="4d673-113">Creating a posting profile</span></span>
<span data-ttu-id="4d673-114">Norādiet virsgrāmatas kontus, kas tiek lietoti, lai grāmatotu transakcijas, kuras izmanto atlasīto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="4d673-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="4d673-115">Atlasiet atlasītajai grāmatošanas metodei konta kodu un, ja iespējams, konta vai grupas numuru.</span><span class="sxs-lookup"><span data-stu-id="4d673-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="4d673-116">Grāmatošanas procesā katrai transakcijai tiek atrasta piemērotākā grāmatošanas metode, meklējot visspecifiskāko konta kodu, konta numuru vai grupas un numura kombināciju šādā prioritārā secībā:</span><span class="sxs-lookup"><span data-stu-id="4d673-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="4d673-117">Lauka **Konta kods** vērtība</span><span class="sxs-lookup"><span data-stu-id="4d673-117">**Account code** field value</span></span> | <span data-ttu-id="4d673-118">Lauka **Konta/grupas numurs** vērtība</span><span class="sxs-lookup"><span data-stu-id="4d673-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="4d673-119">Meklēšanas prioritāte</span><span class="sxs-lookup"><span data-stu-id="4d673-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="4d673-120">**Tabula**</span><span class="sxs-lookup"><span data-stu-id="4d673-120">**Table**</span></span>                    | <span data-ttu-id="4d673-121">Specifisks debitora konts</span><span class="sxs-lookup"><span data-stu-id="4d673-121">Specific customer account</span></span>                       | <span data-ttu-id="4d673-122">1</span><span class="sxs-lookup"><span data-stu-id="4d673-122">1</span></span>               |
| <span data-ttu-id="4d673-123">**Grupa**</span><span class="sxs-lookup"><span data-stu-id="4d673-123">**Group**</span></span>                    | <span data-ttu-id="4d673-124">Debitoru grupa, kas ir piešķirta šim debitoram</span><span class="sxs-lookup"><span data-stu-id="4d673-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="4d673-125">2</span><span class="sxs-lookup"><span data-stu-id="4d673-125">2</span></span>               |
| <span data-ttu-id="4d673-126">**Visi**</span><span class="sxs-lookup"><span data-stu-id="4d673-126">**All**</span></span>                      | <span data-ttu-id="4d673-127">Tukšs</span><span class="sxs-lookup"><span data-stu-id="4d673-127">Blank</span></span>                                           | <span data-ttu-id="4d673-128">3</span><span class="sxs-lookup"><span data-stu-id="4d673-128">3</span></span>               |

<span data-ttu-id="4d673-129">Ja vēlaties, lai visu debitoru transakcijām būtu vienāda grāmatošanas metode, iestatiet tikai vienu grāmatošanas metodi, kurai laukā Konta kods ir vērtība Visi.</span><span class="sxs-lookup"><span data-stu-id="4d673-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="4d673-130">Lai iestatītu savu grāmatošanas metodi, norādiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="4d673-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4d673-131">Lauks</span><span class="sxs-lookup"><span data-stu-id="4d673-131">Field</span></span></th>
<th><span data-ttu-id="4d673-132">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4d673-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d673-133"><strong>Grāmatošanas metode</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="4d673-134">Ievadiet grāmatošanas metodes kodu.</span><span class="sxs-lookup"><span data-stu-id="4d673-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="4d673-135">Piemēram, varat izveidot divas grāmatošanas metodes, lai iegūtu vienu kontu debitoru bilancēm nacionālajā valūtā un otru — debitoru bilancēm ārvalstu valūtā.</span><span class="sxs-lookup"><span data-stu-id="4d673-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="4d673-136">Vienu kontu varat nosaukt Nacionālais, bet otru — Ārvalstu.</span><span class="sxs-lookup"><span data-stu-id="4d673-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d673-137"><strong>Apraksts</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="4d673-138">Ievadiet grāmatošanas metodes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="4d673-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="4d673-139">Šis tiek izmantots tikai ar mērķi labāk identificēt grāmatošanas metodi, kad to skatāt šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="4d673-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d673-140"><strong>Konta kods</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="4d673-141">Norādiet, vai grāmatošanas metode tiek izmantota vienam debitoram, debitoru grupai vai visiem debitoriem:</span><span class="sxs-lookup"><span data-stu-id="4d673-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="4d673-142"><strong>Tabula</strong> — grāmatošanas metode attiecas uz vienu debitoru.</span><span class="sxs-lookup"><span data-stu-id="4d673-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="4d673-143">Atlasiet debitora kontu laukā Konta/grupas numurs.</span><span class="sxs-lookup"><span data-stu-id="4d673-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="4d673-144"><strong>Grupa</strong> — grāmatošanas metode attiecas uz debitoru grupu.</span><span class="sxs-lookup"><span data-stu-id="4d673-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="4d673-145">Atlasiet debitoru grupu laukā Konta/grupas numurs.</span><span class="sxs-lookup"><span data-stu-id="4d673-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="4d673-146"><strong>Visi</strong> — grāmatošanas metode attiecas uz visiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="4d673-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="4d673-147">Lauku Konta/grupas numurs atstājiet tukšu.</span><span class="sxs-lookup"><span data-stu-id="4d673-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d673-148"><strong>Konta/grupas numurs</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="4d673-149">Ja laukā Konta kods ir atlasīta vērtība Tabula, atlasiet konta numuru debitoram, kurš ir saistīts ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="4d673-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="4d673-150">Ja ir atlasīta vērtība Grupa, atlasiet debitoru grupu.</span><span class="sxs-lookup"><span data-stu-id="4d673-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="4d673-151">Ja ir atlasīta vērtība Visi, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="4d673-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d673-152"><strong>Summu konts</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="4d673-153">Atlasiet virsgrāmatas kontu, kurš tiks lietots kā debitoru summu konts tiem debitoriem, kas ir saistīti ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="4d673-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d673-154"><strong>Apmaksāt konta rēķinus</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="4d673-155">Atlasiet likviditātes virsgrāmatas kontu, kas tiek lietots naudas plūsmas prognozēm.</span><span class="sxs-lookup"><span data-stu-id="4d673-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="4d673-156">Šis lauks būs redzams tikai tad, ja ir iespējotas naudas plūsmas prognozes.</span><span class="sxs-lookup"><span data-stu-id="4d673-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d673-157"><strong>PVN priekšapmaksām</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="4d673-158">Atlasiet kontu pārdošanas nodoklim tādiem maksājumiem, kas tiek saņemti avansā.</span><span class="sxs-lookup"><span data-stu-id="4d673-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Piezīme" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="4d673-160"><strong>Piezīme</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d673-161">Izmantojiet lapu Debitoru moduļa parametri, lai norādītu grāmatošanas metodi, ko izmantot, kad maksājums ir apzīmēts kā priekšapmaksa.</span><span class="sxs-lookup"><span data-stu-id="4d673-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d673-162"><strong>Atlaižu konta saistības</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="4d673-163">Atlasiet virsgrāmatas kontu atlaižu saistībām.</span><span class="sxs-lookup"><span data-stu-id="4d673-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d673-164"><strong>Atgādinājuma vēstuļu sērija</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="4d673-165">Atlasiet identifikatoru atgādinājuma vēstuļu sērijai, ko izmantot debitoriem, kuriem ir piešķirta šī grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="4d673-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d673-166"><strong>Soda naudas kods</strong></span><span class="sxs-lookup"><span data-stu-id="4d673-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="4d673-167">Atlasiet soda naudas kodu, ko izmantot soda naudas aprēķināšanai debitoriem, kuriem ir piešķirta šī grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="4d673-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="4d673-168">**Tabulu ierobežojumi**</span><span class="sxs-lookup"><span data-stu-id="4d673-168">**Table restrictions**</span></span>

<span data-ttu-id="4d673-169">Transakcijām, kam ir atlasītā grāmatošanas metode, norādiet, vai šis transakcijas tiks segtas automātiski, vai tiks aprēķināta soda nauda, un vai tiks izveidotas atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="4d673-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="4d673-170">Varat arī atlasīt kontu, kas tiks izmantots, kad tiek slēgtas transakcijas ar atlasīto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="4d673-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="4d673-171">Lai iestatītu savu grāmatošanas metodi, norādiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="4d673-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="4d673-172">Lauks</span><span class="sxs-lookup"><span data-stu-id="4d673-172">Field</span></span>                 | <span data-ttu-id="4d673-173">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4d673-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d673-174">**Segšana**</span><span class="sxs-lookup"><span data-stu-id="4d673-174">**Settlement**</span></span>        | <span data-ttu-id="4d673-175">Atlasiet šo pārslēgu, lai iespējotu automātisko nosegšanu transakcijām ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="4d673-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="4d673-176">Ja šī pārslēga atzīme ir notīrīta, transakciju nosegšana jums ir jāveic manuāli, izmantojot lapu Nosegt atvērtās transakcijas vai lapu Ievadīt debitora maksājumus.</span><span class="sxs-lookup"><span data-stu-id="4d673-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="4d673-177">**Intereses**</span><span class="sxs-lookup"><span data-stu-id="4d673-177">**Interest**</span></span>          | <span data-ttu-id="4d673-178">Atzīmējiet šo pārslēgu, ja debitoru kontiem, kas izmanto šo metodi, soda nauda ir jāaprēķina nenokārtotām bilancēm.</span><span class="sxs-lookup"><span data-stu-id="4d673-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="4d673-179">Ja šī pārslēga atzīme ir notīrīta, soda nauda šiem debitoriem netiks aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="4d673-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="4d673-180">**Atgādinājuma vēstule**</span><span class="sxs-lookup"><span data-stu-id="4d673-180">**Collection letter**</span></span> | <span data-ttu-id="4d673-181">Atzīmējiet šo pārslēgu, ja debitoru kontiem, kas izmanto šo metodi, ir nepieciešams ģenerēt atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="4d673-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="4d673-182">Ja šī pārslēga atzīme ir notīrīta, atgādinājuma vēstules šiem debitoriem netiks ģenerētas.</span><span class="sxs-lookup"><span data-stu-id="4d673-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="4d673-183">**Aizvērt**</span><span class="sxs-lookup"><span data-stu-id="4d673-183">**Close**</span></span>             | <span data-ttu-id="4d673-184">Atlasiet kādu grāmatošanas metodi, kuru mainīt, kad tiek slēgtas transakcijas ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="4d673-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="4d673-185">Darbība tiek uzskatīta par aizvērtu, kad tā ir pilnībā nosegta.</span><span class="sxs-lookup"><span data-stu-id="4d673-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="4d673-186">Plašāku informāciju skatiet šeit: [Debitoru maksājumu pārskats](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4d673-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>

