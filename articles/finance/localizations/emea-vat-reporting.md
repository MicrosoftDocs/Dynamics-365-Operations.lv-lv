---
title: PVN pārskati Eiropai
description: Šajā tēmā ir sniegta vispārīga informācija par pievienotās vērtības nodokļa (PVN) pārskatu iestatīšanu un ģenerēšanu noteiktām Eiropas valstīm.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: efa9be4a5243444c2bf0b154836efbf8cfa76de9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894670"
---
# <a name="vat-reporting-for-europe"></a><span data-ttu-id="67d4a-103">PVN pārskati Eiropai</span><span class="sxs-lookup"><span data-stu-id="67d4a-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67d4a-104">Šajā tēmā ir sniegta vispārīga informācija par pievienotās vērtības nodokļa (PVN) pārskatu iestatīšanu un ģenerēšanu noteiktām Eiropas valstīm.</span><span class="sxs-lookup"><span data-stu-id="67d4a-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="67d4a-105">Šajā tēmā ir aprakstīta vispārīga PVN deklarācijas iestatīšanas un ģenerēšanas metode.</span><span class="sxs-lookup"><span data-stu-id="67d4a-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="67d4a-106">Šo metodi izmanto lietotāji juridiskajās personās tālāk norādītajās valstīs/reģionos.</span><span class="sxs-lookup"><span data-stu-id="67d4a-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="67d4a-107">Austrija</span><span class="sxs-lookup"><span data-stu-id="67d4a-107">Austria</span></span>
-   <span data-ttu-id="67d4a-108">Beļģija</span><span class="sxs-lookup"><span data-stu-id="67d4a-108">Belgium</span></span>
-   <span data-ttu-id="67d4a-109">Čehija</span><span class="sxs-lookup"><span data-stu-id="67d4a-109">Czech Republic</span></span>
-   <span data-ttu-id="67d4a-110">Igaunija</span><span class="sxs-lookup"><span data-stu-id="67d4a-110">Estonia</span></span>
-   <span data-ttu-id="67d4a-111">Somija</span><span class="sxs-lookup"><span data-stu-id="67d4a-111">Finland</span></span>
-   <span data-ttu-id="67d4a-112">Vācija</span><span class="sxs-lookup"><span data-stu-id="67d4a-112">Germany</span></span>
-   <span data-ttu-id="67d4a-113">Latvija</span><span class="sxs-lookup"><span data-stu-id="67d4a-113">Latvia</span></span>
-   <span data-ttu-id="67d4a-114">Lietuva</span><span class="sxs-lookup"><span data-stu-id="67d4a-114">Lithuania</span></span>
-   <span data-ttu-id="67d4a-115">Nīderlande</span><span class="sxs-lookup"><span data-stu-id="67d4a-115">Netherlands</span></span>
-   <span data-ttu-id="67d4a-116">Zviedrija</span><span class="sxs-lookup"><span data-stu-id="67d4a-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="67d4a-117">PVN deklarācijas apskats</span><span class="sxs-lookup"><span data-stu-id="67d4a-117">VAT statement overview</span></span>
<span data-ttu-id="67d4a-118">PVN deklarācija ir balstīta uz nodokļu transakciju summām.</span><span class="sxs-lookup"><span data-stu-id="67d4a-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="67d4a-119">PVN deklarācijas ģenerēšanas process ietilpst PVN maksājuma procesā, kurš ir ieviests ar funkciju Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="67d4a-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="67d4a-120">Šī funkcija aprēķina PVN, kurš ir jāmaksā par attiecīgo periodu.</span><span class="sxs-lookup"><span data-stu-id="67d4a-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="67d4a-121">Nosegšanas aprēķinā ir iekļauts atlasītajam nosegšanas periodam nodokļu transakcijām grāmatotais PVN.</span><span class="sxs-lookup"><span data-stu-id="67d4a-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="67d4a-122">Process PVN deklarācijas datu aprēķināšanai ir balstīts uz attiecībām starp PVN kodiem un PVN pārskatu kodiem, kur PVN pārskatu kodi atbilst PVN deklarācijas lodziņiem (vai etiķetēm XML failā).</span><span class="sxs-lookup"><span data-stu-id="67d4a-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="67d4a-123">Attiecībā uz katru PVN kodu ir jāiestata PVN pārskatu kodi katram transakcijas tipam, piemēram, ar nodokli apliekamajai pārdošanai, ar nodokli apliekamajiem pirkumiem, ar nodokli apliekamajam importam.</span><span class="sxs-lookup"><span data-stu-id="67d4a-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="67d4a-124">Šie transakciju tipi ir aprakstīti tālāk šīs tēmas sadaļā PVN kodi PVN pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="67d4a-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="67d4a-125">Katram PVN pārskatu kodam ir jānorāda noteikts pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="67d4a-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="67d4a-126">Tajā pašā laikā PVN kodi ir saistīti ar noteiktu PVN iestādi, izmantojot PVN nosegšanas periodus.</span><span class="sxs-lookup"><span data-stu-id="67d4a-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="67d4a-127">Katrai PVN iestādei ir jānorāda noteikts pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="67d4a-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="67d4a-128">Tādējādi PVN koda pārskatu iestatīšanā var atlasīt tikai PVN pārskatu kodus ar vienādu pārskata izkārtojumu, kas attiecībā uz šo PVN kodu ir iestatīti PVN iestādei PVN nosegšanas periodos.</span><span class="sxs-lookup"><span data-stu-id="67d4a-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="67d4a-129">Ar pasūtījuma vai žurnāla grāmatošanu ģenerēta PVN transakcija ietver PVN kodu, PVN avotu, PVN virzienu un transakciju summas (nodokļu bāzes summu un nodokļu summu uzskaites valūtā, PVN valūtā un transakcijas valūtā).</span><span class="sxs-lookup"><span data-stu-id="67d4a-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="67d4a-130">Pamatojoties uz nodokļu transakciju atribūtu kombināciju, transakciju summas veido kopējās summas PVN pārskatu kodiem, kas norādīti PVN kodiem.</span><span class="sxs-lookup"><span data-stu-id="67d4a-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="67d4a-131">Nākamajā attēlā ir redzamas datu attiecības.</span><span class="sxs-lookup"><span data-stu-id="67d4a-131">The following illustration shows the data relationship.</span></span>

![diagramma](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="67d4a-133">PVN pārskata iestatīšana</span><span class="sxs-lookup"><span data-stu-id="67d4a-133">VAT statement setup</span></span>
<span data-ttu-id="67d4a-134">Lai ģenerētu PVN pārskatu, ir jāiestata tālāk aprakstītie priekšnoteikumi.</span><span class="sxs-lookup"><span data-stu-id="67d4a-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="67d4a-135">PVN iestādes PVN pārskatiem</span><span class="sxs-lookup"><span data-stu-id="67d4a-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="67d4a-136">Lai varētu iestatīt PVN pārskatu kodus, ir jāatlasa attiecīgajai PVN iestādei atbilstošais pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="67d4a-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="67d4a-137">Lapā **PVN iestādes**, sadaļā **Vispārīgi** atlasiet vienumu **Pārskata izkārtojums**.</span><span class="sxs-lookup"><span data-stu-id="67d4a-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="67d4a-138">Šis izkārtojums tiek izmantots, kad iestatāt PVN pārskatu kodus.</span><span class="sxs-lookup"><span data-stu-id="67d4a-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="67d4a-139">PVN pārskatu kodi</span><span class="sxs-lookup"><span data-stu-id="67d4a-139">Sales tax reporting codes</span></span>

<span data-ttu-id="67d4a-140">PVN pārskatu kodi ir lodziņu kodi PVN deklarācijā vai etiķešu nosaukumi XML formātā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="67d4a-141">Šie kodi tiek izmantoti, lai pārskatam apkopotu un sagatavotu summas.</span><span class="sxs-lookup"><span data-stu-id="67d4a-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="67d4a-142">Kad konfigurējat PVN deklarācijas elektroniskā pārskata formātu, tiek izmantoti rezultātu summu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="67d4a-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="67d4a-143">PVN pārskatu kodus varat izveidot un uzturēt lapā **PVN pārskatu kodi**.</span><span class="sxs-lookup"><span data-stu-id="67d4a-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="67d4a-144">Katram kodam ir jāpiešķir kāds pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="67d4a-144">You must assign each code a report layout.</span></span> <span data-ttu-id="67d4a-145">Pēc PVN pārskatu kodu izveidošanas šos kodus varat izvēlēties lapas **PVN kodi** sadaļā **Pārskata iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="67d4a-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="67d4a-146">PVN kodi PVN pārskatiem</span><span class="sxs-lookup"><span data-stu-id="67d4a-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> <span data-ttu-id="67d4a-147">PVN transakciju bāzes summas un nodokļu summas PVN deklarācijā var apkopot pārskatu kodos (XML etiķetēs vai deklarācijas lodziņos).</span><span class="sxs-lookup"><span data-stu-id="67d4a-147">Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="67d4a-148">Šo iespēju varat iestatīt, saistot PVN pārskatu kodus dažādiem transakciju tipiem PVN kodos lapā <strong>PVN kodi</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="67d4a-149">Nākamajā tabulā ir aprakstīti transakciju tipi pārskatu iestatīšanai PVN kodiem.</span><span class="sxs-lookup"><span data-stu-id="67d4a-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="67d4a-150">Šajā aprēķinā ir iekļautas transakcijas no visu tipu avotiem, izņemot PVN.</span><span class="sxs-lookup"><span data-stu-id="67d4a-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67d4a-151"><strong>Transakcijas tips</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="67d4a-152"><strong>Transakciju apraksts un summas, ko aprēķināt šim transakciju tipam</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-153"><strong>Ar nodokli apliekamā pārdošana</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="67d4a-154">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-155">Transakcijas datums ietilpst atlasītajā periodā/</span><span class="sxs-lookup"><span data-stu-id="67d4a-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="67d4a-156">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-157">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-158"><strong>Pārdošana bez nodokļiem</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="67d4a-159">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-160">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-161">Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-162">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-163"><strong>Maksājamais PVN</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="67d4a-164">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-165">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-166">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-167">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-168"><strong>Ar nodokli apliekama pārdošanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-169">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-170">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-171">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-172">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-173"><strong>Ar nodokli neapliekama pārdošanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-174">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-175">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-176">Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-177">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-178"><strong>PVN pārdošanas kredīta notā</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-179">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-180">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-181">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-182">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-183"><strong>Ar nodokļiem apliekamie pirkumi</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="67d4a-184">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-185">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-186">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-187">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-188"><strong>Pirkšana bez nodokļiem</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="67d4a-189">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-190">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-191">Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-192">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-193"><strong>Saņemtais PVN</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="67d4a-194">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-195">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-196">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-197">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-198"><strong>Ar nodokli apliekama pirkšanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-199">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-200">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-201">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-202">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-203"><strong>Ar nodokli neapliekama pirkšanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-204">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-205">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-206">Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-207">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-208"><strong>PVN pirkšanas kredīta notā</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-209">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-210">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-211">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="67d4a-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="67d4a-212">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-213"><strong>Ar nodokli apliekams imports</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="67d4a-214">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-215">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-216"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="67d4a-217">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-218"><strong>Apliekamais imports</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="67d4a-219">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-220">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-221"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="67d4a-222">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-223"><strong>Ar nodokli apliekama importa kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-224">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-225">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="67d4a-226">e</span><span class="sxs-lookup"><span data-stu-id="67d4a-226">e</span></span><li><span data-ttu-id="67d4a-227"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="67d4a-228">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-229"><strong>Apliekamā importa kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="67d4a-230">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-231">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-232">Nodokļu virziens ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="67d4a-233">d</span><span class="sxs-lookup"><span data-stu-id="67d4a-233">d</span></span><li><span data-ttu-id="67d4a-234">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67d4a-235"><strong>Importa nodoklis</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="67d4a-236">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-237">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-238"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="67d4a-239">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67d4a-240"><strong>Kompensēt importa nodokli</strong></span><span class="sxs-lookup"><span data-stu-id="67d4a-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="67d4a-241">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="67d4a-242">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="67d4a-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="67d4a-243"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="67d4a-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="67d4a-244">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="67d4a-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="67d4a-245">Iepriekšējā tabulā tiek pieņems, ka tiek ievēroti tālāk aprakstītie kritēriji.</span><span class="sxs-lookup"><span data-stu-id="67d4a-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="67d4a-246">Nodokļu bāzes summa ir transakcijas summa no lauka **Izcelsme uzskaites valūtā**.</span><span class="sxs-lookup"><span data-stu-id="67d4a-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="67d4a-247">Nodokļu summa ir transakcijas summa no lauka **Reālā PVN summa uzskaites valūtā**.</span><span class="sxs-lookup"><span data-stu-id="67d4a-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="67d4a-248">Pārskatam konfigurēt ER modeli un formātu</span><span class="sxs-lookup"><span data-stu-id="67d4a-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="67d4a-249">Varat izmantot elektronisko pārskatu veidošanu (Electronic Reporting — ER), lai datus eksportētu dažādos elektroniskajos formātos, nemainot X++ kodu.</span><span class="sxs-lookup"><span data-stu-id="67d4a-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="67d4a-250">Papildinformāciju skatiet tālāk norādītajos resursos.</span><span class="sxs-lookup"><span data-stu-id="67d4a-250">For additional information:</span></span>

-   [<span data-ttu-id="67d4a-251">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="67d4a-251">Electronic reporting overview</span></span>](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="67d4a-252">Lejupielādēt elektronisko pārskatu veidošanas konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="67d4a-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="67d4a-253">Lokalizācijas prasības — izveidot GER konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="67d4a-253">Localization requirements – Create a GER configuration</span></span>](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="67d4a-254">Valstij specifiskie resursi PVN deklarācijām</span><span class="sxs-lookup"><span data-stu-id="67d4a-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="67d4a-255">Katras valsts PVN deklarācijai ir jāatbilst attiecīgās valsts likumdošanas prasībām.</span><span class="sxs-lookup"><span data-stu-id="67d4a-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="67d4a-256">Nākamajā tabulā uzskaitītajām valstīm pastāv sākotnēji definēti PVN deklarāciju vispārīgie modeļi un formāti.</span><span class="sxs-lookup"><span data-stu-id="67d4a-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="67d4a-257">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="67d4a-257">Country</span></span>        | <span data-ttu-id="67d4a-258">Papildinformācija</span><span class="sxs-lookup"><span data-stu-id="67d4a-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="67d4a-259">Austrija</span><span class="sxs-lookup"><span data-stu-id="67d4a-259">Austria</span></span>        |  [<span data-ttu-id="67d4a-260">PVN deklarācijas informācija Austrijai</span><span class="sxs-lookup"><span data-stu-id="67d4a-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="67d4a-261">Beļģija</span><span class="sxs-lookup"><span data-stu-id="67d4a-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="67d4a-262">Čehijas Republika</span><span class="sxs-lookup"><span data-stu-id="67d4a-262">Czech Republic</span></span> |  [<span data-ttu-id="67d4a-263">PVN deklarācija Čehijai</span><span class="sxs-lookup"><span data-stu-id="67d4a-263">VAT statement for the Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="67d4a-264">Igaunija</span><span class="sxs-lookup"><span data-stu-id="67d4a-264">Estonia</span></span>        |  [<span data-ttu-id="67d4a-265">PVN deklarācijas informācija Igaunijai</span><span class="sxs-lookup"><span data-stu-id="67d4a-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="67d4a-266">Somija</span><span class="sxs-lookup"><span data-stu-id="67d4a-266">Finland</span></span>        | [<span data-ttu-id="67d4a-267">Somijas PVN pārskats</span><span class="sxs-lookup"><span data-stu-id="67d4a-267">Sales tax report for Finland</span></span>](emea-fin-sales-tax-payment-report-finland.md)          |
| <span data-ttu-id="67d4a-268">Vācija</span><span class="sxs-lookup"><span data-stu-id="67d4a-268">Germany</span></span>        | [<span data-ttu-id="67d4a-269">PVN deklarācija Vācijai</span><span class="sxs-lookup"><span data-stu-id="67d4a-269">VAT declaration for Germany</span></span>](emea-de-vat-declaration.md)                       |
| <span data-ttu-id="67d4a-270">Itālija</span><span class="sxs-lookup"><span data-stu-id="67d4a-270">Italy</span></span>          | [<span data-ttu-id="67d4a-271">PVN deklarāciju informācija Itālijai</span><span class="sxs-lookup"><span data-stu-id="67d4a-271">VAT statements details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="67d4a-272">Latvija</span><span class="sxs-lookup"><span data-stu-id="67d4a-272">Latvia</span></span>         | [<span data-ttu-id="67d4a-273">PVN deklarācijas informācija Latvijai</span><span class="sxs-lookup"><span data-stu-id="67d4a-273">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="67d4a-274">Lietuva</span><span class="sxs-lookup"><span data-stu-id="67d4a-274">Lithuania</span></span>      | [<span data-ttu-id="67d4a-275">PVN deklarācijas informācija Lietuvai</span><span class="sxs-lookup"><span data-stu-id="67d4a-275">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="67d4a-276">Nīderlande</span><span class="sxs-lookup"><span data-stu-id="67d4a-276">Netherlands</span></span>    | [<span data-ttu-id="67d4a-277">PVN deklarācija Nīderlandei</span><span class="sxs-lookup"><span data-stu-id="67d4a-277">VAT declaration for the Netherlands</span></span>](emea-nl-vat-declaration.md)           |
| <span data-ttu-id="67d4a-278">Zviedrija</span><span class="sxs-lookup"><span data-stu-id="67d4a-278">Sweden</span></span>         | [<span data-ttu-id="67d4a-279">Zviedrijas PVN pārskats</span><span class="sxs-lookup"><span data-stu-id="67d4a-279">Sales tax report for Sweden</span></span>](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]