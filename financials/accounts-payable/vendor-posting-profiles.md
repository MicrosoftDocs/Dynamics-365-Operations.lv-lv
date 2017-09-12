---
title: "Kreditoru grāmatošanas metodes"
description: "Kreditoru grāmatošanas metodes kontrolē kreditoru transakciju grāmatošanu virsgrāmatā."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 540ad7be384e34054454cdc34c4945ed505b7963
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="a9a6f-103">Kreditoru grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="a9a6f-103">Vendor posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a9a6f-104">Kreditoru grāmatošanas metodes kontrolē kreditoru transakciju grāmatošanu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="a9a6f-105">Kreditoru grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="a9a6f-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="a9a6f-106">Kreditoru grāmatošanas metodes jums ļauj virsgrāmatas kontus un dokumentu iestatījumus piešķirt visiem kreditoriem, kreditoru grupai vai atsevišķam kreditoram.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="a9a6f-107">Šie iestatījumi tiek izmantoti, kad izveidojat pirkšanas pasūtījumus, kreditoru rēķinus un maksājumus skaidrā naudā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="a9a6f-108">Noteiktām transakcijām varat atlasīt grāmatošanas metodi, kas atšķiras no šajā lapā iestatītajām transakciju grāmatošanas metodēm un kam ir prioritāte pār tām.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="a9a6f-109">Noklusējuma grāmatošanas metode tiek definēta kopsavilkuma cilnē Virsgrāmata un Pārdošanas nodoklis, lapā Kreditoru moduļa parametri.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="a9a6f-110">Noklusējuma grāmatošanas metode pēc tam automātiski tiek iekļauta jaunu dokumentu virsrakstā, kur to varat mainīt uz citu grāmatošanas metodi, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="a9a6f-111">Grāmatošanas definīcijas varat arī saistīt ar transakciju grāmatošanas tipiem lapā Transakciju grāmatošanas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="a9a6f-112">Grāmatošanas definīcijas kontrolē kreditoru transakciju grāmatošanu virsgrāmatā grāmatošanas metožu vietā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="a9a6f-113">Grāmatošanas metodes izveidošana</span><span class="sxs-lookup"><span data-stu-id="a9a6f-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="a9a6f-114">**Iestatījumi**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-114">**Setup**</span></span>

<span data-ttu-id="a9a6f-115">Norādiet virsgrāmatas kontus, kas tiek lietoti, lai grāmatotu transakcijas, kuras izmanto atlasīto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="a9a6f-116">Atlasiet atlasītajai grāmatošanas metodei konta kodu un, ja iespējams, konta vai grupas numuru.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="a9a6f-117">Grāmatošanas procesā katrai transakcijai tiek atrasta piemērotākā grāmatošanas metode, meklējot visspecifiskāko konta kodu, konta numuru vai grupas un numura kombināciju šādā prioritārā secībā:</span><span class="sxs-lookup"><span data-stu-id="a9a6f-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="a9a6f-118">Lauka **Konta kods** vērtība</span><span class="sxs-lookup"><span data-stu-id="a9a6f-118">**Account code** field value</span></span> | <span data-ttu-id="a9a6f-119">Lauka **Konta/grupas numurs** vērtība</span><span class="sxs-lookup"><span data-stu-id="a9a6f-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="a9a6f-120">Meklēšanas prioritāte</span><span class="sxs-lookup"><span data-stu-id="a9a6f-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="a9a6f-121">**Tabula**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-121">**Table**</span></span>                    | <span data-ttu-id="a9a6f-122">Specifisks kreditora konts</span><span class="sxs-lookup"><span data-stu-id="a9a6f-122">Specific vendor account</span></span>                     | <span data-ttu-id="a9a6f-123">1</span><span class="sxs-lookup"><span data-stu-id="a9a6f-123">1</span></span>               |
| <span data-ttu-id="a9a6f-124">**Grupa**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-124">**Group**</span></span>                    | <span data-ttu-id="a9a6f-125">kreditoru grupa, kas ir piesaistīta kreditoram</span><span class="sxs-lookup"><span data-stu-id="a9a6f-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="a9a6f-126">2</span><span class="sxs-lookup"><span data-stu-id="a9a6f-126">2</span></span>               |
| <span data-ttu-id="a9a6f-127">**Visi**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-127">**All**</span></span>                      | <span data-ttu-id="a9a6f-128">Tukšs</span><span class="sxs-lookup"><span data-stu-id="a9a6f-128">Blank</span></span>                                       | <span data-ttu-id="a9a6f-129">3</span><span class="sxs-lookup"><span data-stu-id="a9a6f-129">3</span></span>               |

<span data-ttu-id="a9a6f-130">Ja vēlaties, lai visām kreditoru transakcijām būtu vienāda grāmatošanas metode, iestatiet tikai vienu grāmatošanas metodi, kurai laukā Konta kods ir vērtība Visi.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="a9a6f-131">Lai iestatītu savu grāmatošanas metodi, norādiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9a6f-131">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9a6f-132">Lauks</span><span class="sxs-lookup"><span data-stu-id="a9a6f-132">Field</span></span></th>
<th><span data-ttu-id="a9a6f-133">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a9a6f-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9a6f-134"><strong>Grāmatošanas metode</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="a9a6f-135">Ievadiet grāmatošanas metodes kodu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="a9a6f-136">Piemēram, varat izveidot divas grāmatošanas metodes, lai iegūtu vienu kontu kreditoru bilancēm nacionālajā valūtā un otru — kreditoru bilancēm ārvalstu valūtā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="a9a6f-137">Vienu kontu varat nosaukt Nacionālais, bet otru — Ārvalstu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9a6f-138"><strong>Apraksts</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="a9a6f-139">Ievadiet grāmatošanas metodes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9a6f-140"><strong>Konta kods</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="a9a6f-141">Norādiet, vai grāmatošanas metode tiek lietota konkrētam kreditoram, kreditoru grupai vai visiem kreditoriem:</span><span class="sxs-lookup"><span data-stu-id="a9a6f-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="a9a6f-142"><strong>Tabula</strong> — grāmatošanas metode attiecas uz vienu kreditoru.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="a9a6f-143">Atlasiet kreditora kontu laukā Konta/grupas numurs.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="a9a6f-144"><strong>Grupa</strong> — grāmatošanas metode attiecas uz kreditoru grupu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="a9a6f-145">Atlasiet kreditoru grupu laukā Konta/grupas numurs.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="a9a6f-146"><strong>Visi</strong> — grāmatošanas metode attiecas uz visiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="a9a6f-147">Lauku Konta/grupas numurs atstājiet tukšu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9a6f-148"><strong>Konta/grupas numurs</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="a9a6f-149">Ja laukā Konta kods ir atlasīta vērtība Tabula, atlasiet konta numuru kreditoram, kurš ir saistīts ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="a9a6f-150">Ja ir atlasīta vērtība Grupa, atlasiet kreditoru grupu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="a9a6f-151">Ja ir atlasīta vērtība Visi, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9a6f-152"><strong>Summu konts</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="a9a6f-153">Atlasiet virsgrāmatas kontu, kas tiks izmantots kā summu konts kreditoriem, ar kuriem ir saistīta šī grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a9a6f-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Piezīme</span><span class="sxs-lookup"><span data-stu-id="a9a6f-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="a9a6f-155"><strong>Piezīme</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9a6f-156">Ja lapā Virsgrāmatas parametri ir atlasīts pārslēgs Izmantot grāmatošanas definīcijas, summu konta vietā kreditoru rēķiniem tiek izmantota transakcijas grāmatošanas definīcija.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9a6f-157"><strong>Apmaksāt konta rēķinus</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="a9a6f-158">Atlasiet likviditātes virsgrāmatas kontu, kas tiek lietots naudas plūsmas prognozēm.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="a9a6f-159">Šis lauks ir pieejams tikai tad, ja ir iespējota naudas plūsmas prognozēšana.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9a6f-160"><strong>PVN priekšapmaksām</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="a9a6f-161">Atlasiet kontu tādiem pārdošanas nodokļa maksājumiem, kas tiek saņemti avansā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a9a6f-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Piezīme</span><span class="sxs-lookup"><span data-stu-id="a9a6f-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="a9a6f-163"><strong>Piezīme</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9a6f-164">Grāmatošanas metode, kas tiek izmantota, kad maksājums ir apzīmēts kā priekšapmaksa, lapā Kreditoru moduļa parametri, apgabalā Virsgrāmata un pārdošanas nodoklis ir atlasīta laukā Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9a6f-165"><strong>Atgriešana</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="a9a6f-166">Atlasiet virsgrāmatas kontu, kurā tiek grāmatota informācija par neapstiprinātiem kreditoru rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="a9a6f-167">Šī informācija tiek ievadīta rēķinu reģistra žurnālā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="a9a6f-168">Piemēram, lietotājs ievada tikai pamatinformāciju par kreditoru rēķiniem, kad tie tiek saņemti rēķinu reģistrā.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="a9a6f-169">Kad rēķinu reģistrs ir iegrāmatots, transakcijas tiek grāmatotas kontā, kurš ir ievadīts šeit un laukā šeit ievadītajā kontā un laukā Korespondējošais konts.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="a9a6f-170">Kad rēķini ir apstiprināti, parāds no saņemšanas konta tiek pārsūtīts uz kreditora summu kontu.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9a6f-171"><strong>Korespondējošais konts</strong></span><span class="sxs-lookup"><span data-stu-id="a9a6f-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="a9a6f-172">Atlasiet virsgrāmatas kontu, kas tiek izmantots kreditoru neapstiprināto rēķinu kompensēšanai, kuri tiek atjaunināti ar rēķinu reģistru.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="a9a6f-173">Korespondējošais konts darbojas kā korespondējošais konts transakcijām, kuras tiek grāmatotas saņemšanas kontos.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="a9a6f-174">Tādēļ šis konts ietver kreditoru pirkumus, kas vēl nav apstiprināti.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a><span data-ttu-id="a9a6f-175">**Tabulu ierobežojumi**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-175">**Table restrictions**</span></span>

<span data-ttu-id="a9a6f-176">Transakcijām, kam ir atlasītā grāmatošanas metode, norādiet, vai šis transakcijas tiks segtas automātiski, vai tiks aprēķināta soda nauda, un vai tiks izveidotas atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="a9a6f-177">Varat arī atlasīt kontu, kas tiks izmantots, kad tiek slēgtas transakcijas ar atlasīto grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="a9a6f-178">Lai iestatītu savu grāmatošanas metodi, norādiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a9a6f-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="a9a6f-179">Lauks</span><span class="sxs-lookup"><span data-stu-id="a9a6f-179">Field</span></span>          | <span data-ttu-id="a9a6f-180">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a9a6f-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a6f-181">**Segšana**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-181">**Settlement**</span></span> | <span data-ttu-id="a9a6f-182">Atlasiet šo opciju, lai iespējotu automātisko nosegšanu transakcijām ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="a9a6f-183">Ja šīs opcijas atzīme ir notīrīta, transakciju nosegšana jums ir jāveic manuāli, izmantojot lapu Nosegt atvērtās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="a9a6f-184">**Atcelt**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-184">**Cancel**</span></span>     | <span data-ttu-id="a9a6f-185">Atzīmējiet šo opciju, ja vēlaties iespēju atcelt transakcijas, kurām ir šī grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="a9a6f-186">**Aizvērt**</span><span class="sxs-lookup"><span data-stu-id="a9a6f-186">**Close**</span></span>      | <span data-ttu-id="a9a6f-187">Atlasiet kādu grāmatošanas metodi, kuru mainīt, kad tiek slēgtas transakcijas ar šo grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="a9a6f-188">Darbība tiek uzskatīta par aizvērtu, kad tā ir pilnībā nosegta.</span><span class="sxs-lookup"><span data-stu-id="a9a6f-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






