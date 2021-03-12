---
title: Kreditoru grāmatošanas metodes
description: Kreditoru grāmatošanas metodes kontrolē kreditoru transakciju grāmatošanu virsgrāmatā.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6447228f00d91fd2dddd43c1ceb57dff0c6df9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979193"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="c3350-103">Kreditoru grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="c3350-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3350-104">Kreditoru grāmatošanas metodes kontrolē kreditoru transakciju grāmatošanu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="c3350-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="c3350-105">Kreditoru grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="c3350-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="c3350-106">Kreditoru grāmatošanas metodes jums ļauj virsgrāmatas kontus un dokumentu iestatījumus piešķirt visiem kreditoriem, kreditoru grupai vai atsevišķam kreditoram.</span><span class="sxs-lookup"><span data-stu-id="c3350-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="c3350-107">Šie iestatījumi tiek izmantoti, kad izveidojat pirkšanas pasūtījumus, kreditoru rēķinus un maksājumus skaidrā naudā.</span><span class="sxs-lookup"><span data-stu-id="c3350-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="c3350-108">Noteiktām transakcijām varat atlasīt grāmatošanas metodi, kas atšķiras no šajā lapā iestatītajām transakciju grāmatošanas metodēm un kam ir prioritāte pār šajā lapā iestatītajām.</span><span class="sxs-lookup"><span data-stu-id="c3350-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="c3350-109">Noklusējuma grāmatošanas metode tiek definēta kopsavilkuma cilnē **Virsgrāmata un PVN**, lapā **Kreditoru moduļa parametri**.</span><span class="sxs-lookup"><span data-stu-id="c3350-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="c3350-110">Noklusējuma grāmatošanas metode pēc tam tiek automātiski iekļauta jaunu dokumentu virsrakstā, kur to varat mainīt uz citu grāmatošanas metodi, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="c3350-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="c3350-111">Grāmatošanas definīcijas varat arī saistīt ar transakciju grāmatošanas tipiem lapā **Transakciju grāmatošanas definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="c3350-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="c3350-112">Grāmatošanas definīcijas kontrolē kreditoru transakciju grāmatošanu virsgrāmatā grāmatošanas metožu vietā.</span><span class="sxs-lookup"><span data-stu-id="c3350-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="c3350-113">Grāmatošanas metodes izveidošana</span><span class="sxs-lookup"><span data-stu-id="c3350-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="c3350-114">**Iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="c3350-114">**Setup**</span></span>

<span data-ttu-id="c3350-115">Norādiet virsgrāmatas kontus, kas tiek lietoti, lai grāmatotu transakcijas, kuras izmanto atlasīto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="c3350-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="c3350-116">Atlasiet atlasītajai grāmatošanas metodei konta kodu un, ja iespējams, konta vai grupas numuru.</span><span class="sxs-lookup"><span data-stu-id="c3350-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="c3350-117">Grāmatošanas procesā katrai transakcijai tiek atrasta piemērotākā grāmatošanas metode, meklējot visspecifiskāko konta kodu, konta numuru vai grupas un numura kombināciju tālāk norādītajā prioritāšu secībā.</span><span class="sxs-lookup"><span data-stu-id="c3350-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="c3350-118">Lauka **Konta kods** vērtība</span><span class="sxs-lookup"><span data-stu-id="c3350-118">**Account code** field value</span></span> | <span data-ttu-id="c3350-119">Lauka **Konta/grupas numurs** vērtība</span><span class="sxs-lookup"><span data-stu-id="c3350-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="c3350-120">Meklēšanas prioritāte</span><span class="sxs-lookup"><span data-stu-id="c3350-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="c3350-121">**Tabula**</span><span class="sxs-lookup"><span data-stu-id="c3350-121">**Table**</span></span>                    | <span data-ttu-id="c3350-122">Specifisks kreditora konts</span><span class="sxs-lookup"><span data-stu-id="c3350-122">Specific vendor account</span></span>                     | <span data-ttu-id="c3350-123">1</span><span class="sxs-lookup"><span data-stu-id="c3350-123">1</span></span>               |
| <span data-ttu-id="c3350-124">**Grupa**</span><span class="sxs-lookup"><span data-stu-id="c3350-124">**Group**</span></span>                    | <span data-ttu-id="c3350-125">Kreditoru grupa, kas ir piesaistīta šim kreditoram</span><span class="sxs-lookup"><span data-stu-id="c3350-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="c3350-126">2</span><span class="sxs-lookup"><span data-stu-id="c3350-126">2</span></span>               |
| <span data-ttu-id="c3350-127">**Visi**</span><span class="sxs-lookup"><span data-stu-id="c3350-127">**All**</span></span>                      | <span data-ttu-id="c3350-128">Tukšs</span><span class="sxs-lookup"><span data-stu-id="c3350-128">Blank</span></span>                                       | <span data-ttu-id="c3350-129">3</span><span class="sxs-lookup"><span data-stu-id="c3350-129">3</span></span>               |

<span data-ttu-id="c3350-130">Ja vēlaties, lai visām kreditoru transakcijām būtu vienāda grāmatošanas metode, iestatiet tikai vienu grāmatošanas metodi, kurai laukā **Konta kods** ir vērtība **Visi**.</span><span class="sxs-lookup"><span data-stu-id="c3350-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="c3350-131">Lai iestatītu savu grāmatošanas metodi, norādiet tālāk uzskaitītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c3350-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c3350-132">Lauks</span><span class="sxs-lookup"><span data-stu-id="c3350-132">Field</span></span></th>
<th><span data-ttu-id="c3350-133">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c3350-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c3350-134"><strong>Grāmatošanas metode</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="c3350-135">Ievadiet grāmatošanas metodes kodu.</span><span class="sxs-lookup"><span data-stu-id="c3350-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="c3350-136">Piemēram, varat izveidot divas grāmatošanas metodes, lai iegūtu vienu kontu kreditoru bilancēm nacionālajā valūtā un otru — kreditoru bilancēm ārvalstu valūtā.</span><span class="sxs-lookup"><span data-stu-id="c3350-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="c3350-137">Vienu kontu varat nosaukt Nacionālais, bet otru — Ārvalstu.</span><span class="sxs-lookup"><span data-stu-id="c3350-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3350-138"><strong>Apraksts</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="c3350-139">Ievadiet grāmatošanas metodes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="c3350-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3350-140"><strong>Konta kods</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="c3350-141">Norādiet, vai grāmatošanas metode tiek lietota konkrētam kreditoram, kreditoru grupai vai visiem kreditoriem:</span><span class="sxs-lookup"><span data-stu-id="c3350-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="c3350-142"><strong>Tabula</strong> — grāmatošanas metode attiecas uz vienu kreditoru.</span><span class="sxs-lookup"><span data-stu-id="c3350-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="c3350-143">Atlasiet kreditora kontu laukā <strong>Konta/grupas numurs</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3350-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="c3350-144"><strong>Grupa</strong> — grāmatošanas metode attiecas uz kreditoru grupu.</span><span class="sxs-lookup"><span data-stu-id="c3350-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="c3350-145">Atlasiet kreditoru grupu laukā <strong>Konta/grupas numurs</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3350-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="c3350-146"><strong>Visi</strong> — grāmatošanas metode attiecas uz visiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="c3350-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="c3350-147">Lauku <strong>Konta/grupas numurs</strong> atstājiet tukšu.</span><span class="sxs-lookup"><span data-stu-id="c3350-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3350-148"><strong>Konta/grupas numurs</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="c3350-149">Ja laukā <strong>Konta kods</strong> ir atlasīta vērtība <strong>Tabula</strong>, atlasiet konta numuru tam kreditoram, kurš ir saistīts ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="c3350-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="c3350-150">Ja ir atlasīta vērtība <strong>Grupa</strong>, atlasiet kreditoru grupu.</span><span class="sxs-lookup"><span data-stu-id="c3350-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="c3350-151">Ja ir atlasīta vērtība <strong>Visi</strong>, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="c3350-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3350-152"><strong>Summu konts</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="c3350-153">Atlasiet virsgrāmatas kontu, kas tiks izmantots kā summu konts kreditoriem, ar kuriem ir saistīta šī grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="c3350-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="c3350-154">Šim galvenajam kontam būs atzīmēts parametrs <strong>Neļaut manuālu ievadi</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3350-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="c3350-155">Ja šo kontu vēlāk noņemat no grāmatošanas metodes, validējiet iestatījumu <strong>Neļaut manuālu ievadi</strong> lapā <strong>Galvenie konti</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3350-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="c3350-156"><strong>Piezīme.</strong> Ja lapā <strong>Virsgrāmatas parametri</strong> ir atlasīta opcija <strong>Izmantot grāmatošanas definīcijas</strong>, summu konta vietā kreditoru rēķiniem tiek izmantota transakcijas grāmatošanas definīcija.</span><span class="sxs-lookup"><span data-stu-id="c3350-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3350-157"><strong>Apmaksāt konta rēķinus</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="c3350-158">Atlasiet likviditātes virsgrāmatas kontu, kas tiek lietots naudas plūsmas prognozēm.</span><span class="sxs-lookup"><span data-stu-id="c3350-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="c3350-159">Šis lauks ir pieejams tikai tad, ja ir iespējota naudas plūsmas prognozēšana.</span><span class="sxs-lookup"><span data-stu-id="c3350-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3350-160"><strong>PVN priekšapmaksām</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="c3350-161">Atlasiet kontu tādiem pārdošanas nodokļa maksājumiem, kas tiek saņemti avansā.</span><span class="sxs-lookup"><span data-stu-id="c3350-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="c3350-162"><strong>Piezīme.</strong> Grāmatošanas metode, kas tiek izmantota, kad maksājums ir atzīmēts kā priekšapmaksa, tiek atlasīta profilā <strong>Grāmatošana</strong> ar lauku <strong>Priekšapmaksas žurnāla dokumenta summa</strong> lapas <strong>Kreditoru moduļa parametri</strong> apgabalā <strong>Virsgrāmata un PVN</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3350-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3350-163"><strong>Saņemšana</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="c3350-164">Atlasiet virsgrāmatas kontu, kurā tiek grāmatota informācija par neapstiprinātiem kreditoru rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="c3350-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="c3350-165">Šī informācija tiek ievadīta rēķinu reģistra žurnālā.</span><span class="sxs-lookup"><span data-stu-id="c3350-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="c3350-166">Piemēram, lietotājs ievada tikai pamatinformāciju par kreditoru rēķiniem, kad tie tiek saņemti rēķinu reģistrā.</span><span class="sxs-lookup"><span data-stu-id="c3350-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="c3350-167">Kad rēķinu reģistrs ir iegrāmatots, transakcijas tiek grāmatotas šeit ievadītajā kontā un laukā <strong>Korespondējošais konts</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3350-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="c3350-168">Kad rēķini ir apstiprināti, debets no saņemšanas konta tiek pārsūtīts uz kreditora summu kontu.</span><span class="sxs-lookup"><span data-stu-id="c3350-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3350-169"><strong>Korespondējošais konts</strong></span><span class="sxs-lookup"><span data-stu-id="c3350-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="c3350-170">Atlasiet virsgrāmatas kontu, kas tiek izmantots kreditoru neapstiprināto rēķinu kompensēšanai, kuri tiek atjaunināti ar rēķinu reģistru.</span><span class="sxs-lookup"><span data-stu-id="c3350-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="c3350-171">Korespondējošais konts darbojas kā korespondējošais konts transakcijām, kuras tiek grāmatotas saņemšanas kontos.</span><span class="sxs-lookup"><span data-stu-id="c3350-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="c3350-172">Tādēļ šis konts ietver kreditoru pirkumus, kas vēl nav apstiprināti.</span><span class="sxs-lookup"><span data-stu-id="c3350-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="c3350-173">**Tabulu ierobežojumi**</span><span class="sxs-lookup"><span data-stu-id="c3350-173">**Table restrictions**</span></span>

<span data-ttu-id="c3350-174">Transakcijām, kam ir atlasītā grāmatošanas metode, norādiet, vai šis transakcijas tiks segtas automātiski, vai tiks aprēķināta soda nauda, un vai tiks izveidotas atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="c3350-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="c3350-175">Varat arī atlasīt kontu, kas tiks izmantots, kad tiek slēgtas transakcijas ar atlasīto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="c3350-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="c3350-176">Lai iestatītu savu grāmatošanas metodi, norādiet tālāk uzskaitītās vērtības</span><span class="sxs-lookup"><span data-stu-id="c3350-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="c3350-177">Lauks</span><span class="sxs-lookup"><span data-stu-id="c3350-177">Field</span></span>          | <span data-ttu-id="c3350-178">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c3350-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3350-179">**Segums**</span><span class="sxs-lookup"><span data-stu-id="c3350-179">**Settlement**</span></span> | <span data-ttu-id="c3350-180">Atlasiet šo opciju, lai iespējotu automātisko nosegšanu transakcijām ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="c3350-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="c3350-181">Ja šīs opcijas atzīme ir notīrīta, transakciju nosegšana jums ir jāveic manuāli, izmantojot lapu **Nosegt atvērtās transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="c3350-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="c3350-182">**Atcelt**</span><span class="sxs-lookup"><span data-stu-id="c3350-182">**Cancel**</span></span>     | <span data-ttu-id="c3350-183">Atzīmējiet šo opciju, ja vēlaties iespēju atcelt transakcijas, kurām ir šī grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="c3350-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="c3350-184">**Aizvērt**</span><span class="sxs-lookup"><span data-stu-id="c3350-184">**Close**</span></span>      | <span data-ttu-id="c3350-185">Atlasiet kādu grāmatošanas metodi, kuru mainīt, kad tiek slēgtas transakcijas ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="c3350-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="c3350-186">Darbība tiek uzskatīta par aizvērtu, kad tā ir pilnībā nosegta.</span><span class="sxs-lookup"><span data-stu-id="c3350-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |
