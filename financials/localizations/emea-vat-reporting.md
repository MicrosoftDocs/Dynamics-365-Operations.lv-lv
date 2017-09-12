---
title: "PVN pārskati Eiropai"
description: "Šajā tēmā ir sniegta vispārīga informācija par pievienotās vērtības nodokļa (PVN) pārskatu iestatīšanu un ģenerēšanu noteiktām Eiropas valstīm."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c0be253e80636d659027f69cbac58062cb28269e
ms.contentlocale: lv-lv
ms.lasthandoff: 07/21/2017

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="767cb-103">PVN pārskati Eiropai</span><span class="sxs-lookup"><span data-stu-id="767cb-103">VAT reporting for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="767cb-104">Šajā tēmā ir sniegta vispārīga informācija par pievienotās vērtības nodokļa (PVN) pārskatu iestatīšanu un ģenerēšanu noteiktām Eiropas valstīm.</span><span class="sxs-lookup"><span data-stu-id="767cb-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="767cb-105">Šajā tēmā ir aprakstīta vispārīga PVN deklarācijas iestatīšanas un ģenerēšanas metode.</span><span class="sxs-lookup"><span data-stu-id="767cb-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="767cb-106">Šo metodi izmanto lietotāji juridiskajās personās tālāk norādītajās valstīs/reģionos.</span><span class="sxs-lookup"><span data-stu-id="767cb-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="767cb-107">Austrija</span><span class="sxs-lookup"><span data-stu-id="767cb-107">Austria</span></span>
-   <span data-ttu-id="767cb-108">Beļģija</span><span class="sxs-lookup"><span data-stu-id="767cb-108">Belgium</span></span>
-   <span data-ttu-id="767cb-109">Čehija</span><span class="sxs-lookup"><span data-stu-id="767cb-109">Czech Republic</span></span>
-   <span data-ttu-id="767cb-110">Igaunija</span><span class="sxs-lookup"><span data-stu-id="767cb-110">Estonia</span></span>
-   <span data-ttu-id="767cb-111">Somija</span><span class="sxs-lookup"><span data-stu-id="767cb-111">Finland</span></span>
-   <span data-ttu-id="767cb-112">Vācija</span><span class="sxs-lookup"><span data-stu-id="767cb-112">Germany</span></span>
-   <span data-ttu-id="767cb-113">Latvija</span><span class="sxs-lookup"><span data-stu-id="767cb-113">Latvia</span></span>
-   <span data-ttu-id="767cb-114">Lietuva</span><span class="sxs-lookup"><span data-stu-id="767cb-114">Lithuania</span></span>
-   <span data-ttu-id="767cb-115">Nīderlande</span><span class="sxs-lookup"><span data-stu-id="767cb-115">Netherlands</span></span>
-   <span data-ttu-id="767cb-116">Zviedrija</span><span class="sxs-lookup"><span data-stu-id="767cb-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="767cb-117">PVN deklarācijas apskats</span><span class="sxs-lookup"><span data-stu-id="767cb-117">VAT statement overview</span></span>
<span data-ttu-id="767cb-118">PVN deklarācija ir balstīta uz nodokļu transakciju summām.</span><span class="sxs-lookup"><span data-stu-id="767cb-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="767cb-119">PVN deklarācijas ģenerēšanas process ietilpst PVN maksājuma procesā, kurš ir ieviests ar funkciju Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="767cb-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="767cb-120">Šī funkcija aprēķina PVN, kurš ir jāmaksā par attiecīgo periodu.</span><span class="sxs-lookup"><span data-stu-id="767cb-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="767cb-121">Nosegšanas aprēķinā ir iekļauts atlasītajam nosegšanas periodam nodokļu transakcijām grāmatotais PVN.</span><span class="sxs-lookup"><span data-stu-id="767cb-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="767cb-122">Process PVN deklarācijas datu aprēķināšanai ir balstīts uz attiecībām starp PVN kodiem un PVN pārskatu kodiem, kur PVN pārskatu kodi atbilst PVN deklarācijas lodziņiem (vai etiķetēm XML failā).</span><span class="sxs-lookup"><span data-stu-id="767cb-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="767cb-123">Attiecībā uz katru PVN kodu ir jāiestata PVN pārskatu kodi katram transakcijas tipam, piemēram, ar nodokli apliekamajai pārdošanai, ar nodokli apliekamajiem pirkumiem, ar nodokli apliekamajam importam.</span><span class="sxs-lookup"><span data-stu-id="767cb-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="767cb-124">Šie transakciju tipi ir aprakstīti tālāk šīs tēmas sadaļā PVN kodi PVN pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="767cb-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="767cb-125">Katram PVN pārskatu kodam ir jānorāda noteikts pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="767cb-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="767cb-126">Tajā pašā laikā PVN kodi ir saistīti ar noteiktu PVN iestādi, izmantojot PVN nosegšanas periodus.</span><span class="sxs-lookup"><span data-stu-id="767cb-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="767cb-127">Katrai PVN iestādei ir jānorāda noteikts pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="767cb-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="767cb-128">Tādējādi PVN koda pārskatu iestatīšanā var atlasīt tikai PVN pārskatu kodus ar vienādu pārskata izkārtojumu, kas attiecībā uz šo PVN kodu ir iestatīti PVN iestādei PVN nosegšanas periodos.</span><span class="sxs-lookup"><span data-stu-id="767cb-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="767cb-129">Ar pasūtījuma vai žurnāla grāmatošanu ģenerēta PVN transakcija ietver PVN kodu, PVN avotu, PVN virzienu un transakciju summas (nodokļu bāzes summu un nodokļu summu uzskaites valūtā, PVN valūtā un transakcijas valūtā).</span><span class="sxs-lookup"><span data-stu-id="767cb-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="767cb-130">Pamatojoties uz nodokļu transakciju atribūtu kombināciju, transakciju summas veido kopējās summas PVN pārskatu kodiem, kas norādīti PVN kodiem.</span><span class="sxs-lookup"><span data-stu-id="767cb-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="767cb-131">Nākamajā attēlā ir redzamas datu attiecības.</span><span class="sxs-lookup"><span data-stu-id="767cb-131">The following illustration shows the data relationship.</span></span>

![diagramma](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="767cb-133">PVN pārskata iestatīšana</span><span class="sxs-lookup"><span data-stu-id="767cb-133">VAT statement setup</span></span>
<span data-ttu-id="767cb-134">Lai ģenerētu PVN pārskatu, ir jāiestata tālāk aprakstītie priekšnoteikumi.</span><span class="sxs-lookup"><span data-stu-id="767cb-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="767cb-135">PVN iestādes PVN pārskatiem</span><span class="sxs-lookup"><span data-stu-id="767cb-135">Sales tax authorities for VAT reporting</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-authorities). -->
<span data-ttu-id="767cb-136">Lai varētu iestatīt PVN pārskatu kodus, ir jāatlasa attiecīgajai PVN iestādei atbilstošais pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="767cb-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="767cb-137">Lapā **PVN iestādes**, sadaļā **Vispārīgi** atlasiet vienumu **Pārskata izkārtojums**.</span><span class="sxs-lookup"><span data-stu-id="767cb-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="767cb-138">Šis izkārtojums tiek izmantots, kad iestatāt PVN pārskatu kodus.</span><span class="sxs-lookup"><span data-stu-id="767cb-138">This layout will be used when you set up sales tax reporting codes.</span></span>

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="767cb-139">PVN pārskatu kodi</span><span class="sxs-lookup"><span data-stu-id="767cb-139">Sales tax reporting codes</span></span>

<span data-ttu-id="767cb-140">PVN pārskatu kodi ir lodziņu kodi PVN deklarācijā vai etiķešu nosaukumi XML formātā.</span><span class="sxs-lookup"><span data-stu-id="767cb-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="767cb-141">Šie kodi tiek izmantoti, lai pārskatam apkopotu un sagatavotu summas.</span><span class="sxs-lookup"><span data-stu-id="767cb-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="767cb-142">Kad konfigurējat PVN deklarācijas elektroniskā pārskata formātu, tiek izmantoti rezultātu summu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="767cb-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="767cb-143">PVN pārskatu kodus varat izveidot un uzturēt lapā **PVN pārskatu kodi**.</span><span class="sxs-lookup"><span data-stu-id="767cb-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="767cb-144">Katram kodam ir jāpiešķir kāds pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="767cb-144">You must assign each code a report layout.</span></span> <span data-ttu-id="767cb-145">Pēc PVN pārskatu kodu izveidošanas šos kodus varat izvēlēties lapas **PVN kodi** sadaļā **Pārskata iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="767cb-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-reporting-codes).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="767cb-146">PVN kodi PVN pārskatiem</span><span class="sxs-lookup"><span data-stu-id="767cb-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-codes).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="767cb-147"><strong>Transakcijas tips</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-147"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="767cb-148"><strong>Transakciju apraksts un summas, ko aprēķināt šim transakciju tipam</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-148"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-149"><strong>Ar nodokli apliekamā pārdošana</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-149"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="767cb-150">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-150">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-151">Transakcijas datums ietilpst atlasītajā periodā/</span><span class="sxs-lookup"><span data-stu-id="767cb-151">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="767cb-152">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-152">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-153">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-153">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-154"><strong>Pārdošana bez nodokļiem</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-154"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="767cb-155">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-155">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-156">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-156">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-157">Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-157">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="767cb-158">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-158">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-159"><strong>Maksājamais PVN</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-159"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="767cb-160">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-160">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-161">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-161">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-162">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-162">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-163">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-163">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-164"><strong>Ar nodokli apliekama pārdošanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-164"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-165">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-165">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-166">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-166">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-167">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-167">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-168">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-168">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-169"><strong>Ar nodokli neapliekama pārdošanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-169"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-170">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-170">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-171">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-171">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-172">Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-172">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="767cb-173">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-173">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-174"><strong>PVN pārdošanas kredīta notā</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-174"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-175">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-175">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-176">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-176">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-177">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-177">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-178">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-178">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-179"><strong>Ar nodokļiem apliekamie pirkumi</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-179"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="767cb-180">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-180">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-181">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-181">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-182">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-182">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-183">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-183">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-184"><strong>Pirkšana bez nodokļiem</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-184"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="767cb-185">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-185">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-186">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-186">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-187">Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-187">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="767cb-188">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-188">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-189"><strong>Saņemtais PVN</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-189"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="767cb-190">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-190">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-191">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-191">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-192">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-192">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-193">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-193">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-194"><strong>Ar nodokli apliekama pirkšanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-194"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-195">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-195">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-196">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-196">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-197">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-197">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-198">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-198">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-199"><strong>Ar nodokli neapliekama pirkšanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-199"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-200">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-200">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-201">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-201">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-202">Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-202">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="767cb-203">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-203">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-204"><strong>PVN pirkšanas kredīta notā</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-204"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-205">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-205">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-206">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-206">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-207">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="767cb-207">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="767cb-208">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-208">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-209"><strong>Ar nodokli apliekams imports</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-209"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="767cb-210">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-210">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-211">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-211">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-212"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-212"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="767cb-213">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-213">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-214"><strong>Apliekamais imports</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-214"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="767cb-215">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-215">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-216">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-216">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-217"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-217"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="767cb-218">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-218">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-219"><strong>Ar nodokli apliekama importa kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-219"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-220">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-220">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-221">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-221">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="767cb-222">e</span><span class="sxs-lookup"><span data-stu-id="767cb-222">e</span></span><li><span data-ttu-id="767cb-223"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-223"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="767cb-224">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-224">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-225"><strong>Apliekamā importa kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-225"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="767cb-226">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-226">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-227">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-227">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-228">Nodokļu virziens ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-228">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="767cb-229">d</span><span class="sxs-lookup"><span data-stu-id="767cb-229">d</span></span><li><span data-ttu-id="767cb-230">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-230">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="767cb-231"><strong>Importa nodoklis</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-231"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="767cb-232">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-232">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-233">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-233">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-234"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-234"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="767cb-235">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-235">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="767cb-236"><strong>Kompensēt importa nodokli</strong></span><span class="sxs-lookup"><span data-stu-id="767cb-236"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="767cb-237">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-237">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="767cb-238">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="767cb-238">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="767cb-239"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="767cb-239"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="767cb-240">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="767cb-240">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="767cb-241">Iepriekšējā tabulā tiek pieņems, ka tiek ievēroti tālāk aprakstītie kritēriji.</span><span class="sxs-lookup"><span data-stu-id="767cb-241">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="767cb-242">Nodokļu bāzes summa ir transakcijas summa no lauka **Izcelsme uzskaites valūtā**.</span><span class="sxs-lookup"><span data-stu-id="767cb-242">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="767cb-243">Nodokļu summa ir transakcijas summa no lauka **Reālā PVN summa uzskaites valūtā**.</span><span class="sxs-lookup"><span data-stu-id="767cb-243">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="767cb-244">Pārskatam konfigurēt ER modeli un formātu</span><span class="sxs-lookup"><span data-stu-id="767cb-244">Configure the ER model and format for the report</span></span>

<span data-ttu-id="767cb-245">Varat izmantot elektronisko pārskatu veidošanu (Electronic Reporting — ER), lai datus eksportētu dažādos elektroniskajos formātos, nemainot X++ kodu.</span><span class="sxs-lookup"><span data-stu-id="767cb-245">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="767cb-246">Papildinformāciju skatiet tālāk norādītajos resursos.</span><span class="sxs-lookup"><span data-stu-id="767cb-246">For additional information:</span></span>

-   [<span data-ttu-id="767cb-247">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="767cb-247">Electronic reporting overview</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)
-   [<span data-ttu-id="767cb-248">Lejupielādēt elektronisko pārskatu veidošanas konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="767cb-248">Download Electronic reporting configurations from Lifecycle Services</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [<span data-ttu-id="767cb-249">Lokalizācijas prasības — izveidot GER konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="767cb-249">Localization requirements – Create a GER configuration</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="767cb-250">Valstij specifiskie resursi PVN deklarācijām</span><span class="sxs-lookup"><span data-stu-id="767cb-250">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="767cb-251">Katras valsts PVN deklarācijai ir jāatbilst attiecīgās valsts likumdošanas prasībām.</span><span class="sxs-lookup"><span data-stu-id="767cb-251">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="767cb-252">Nākamajā tabulā uzskaitītajām valstīm pastāv sākotnēji definēti PVN deklarāciju vispārīgie modeļi un formāti.</span><span class="sxs-lookup"><span data-stu-id="767cb-252">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="767cb-253">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="767cb-253">Country</span></span>        | <span data-ttu-id="767cb-254">Papildinformācija</span><span class="sxs-lookup"><span data-stu-id="767cb-254">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="767cb-255">Austrija</span><span class="sxs-lookup"><span data-stu-id="767cb-255">Austria</span></span>        |  [<span data-ttu-id="767cb-256">PVN deklarācijas informācija Austrijai</span><span class="sxs-lookup"><span data-stu-id="767cb-256">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="767cb-257">Beļģija</span><span class="sxs-lookup"><span data-stu-id="767cb-257">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="767cb-258">Čehija</span><span class="sxs-lookup"><span data-stu-id="767cb-258">Czech Republic</span></span> |  [<span data-ttu-id="767cb-259">PVN deklarācijas informācija Čehijai</span><span class="sxs-lookup"><span data-stu-id="767cb-259">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="767cb-260">Igaunija</span><span class="sxs-lookup"><span data-stu-id="767cb-260">Estonia</span></span>        |  [<span data-ttu-id="767cb-261">PVN deklarācijas informācija Igaunijai</span><span class="sxs-lookup"><span data-stu-id="767cb-261">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="767cb-262">Somija</span><span class="sxs-lookup"><span data-stu-id="767cb-262">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="767cb-263">Vācija</span><span class="sxs-lookup"><span data-stu-id="767cb-263">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="767cb-264">Itālija</span><span class="sxs-lookup"><span data-stu-id="767cb-264">Italy</span></span>          | [<span data-ttu-id="767cb-265">PVN deklarācijas informācija Itālijai</span><span class="sxs-lookup"><span data-stu-id="767cb-265">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="767cb-266">Latvija</span><span class="sxs-lookup"><span data-stu-id="767cb-266">Latvia</span></span>         | [<span data-ttu-id="767cb-267">PVN deklarācijas informācija Latvijai</span><span class="sxs-lookup"><span data-stu-id="767cb-267">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="767cb-268">Lietuva</span><span class="sxs-lookup"><span data-stu-id="767cb-268">Lithuania</span></span>      | [<span data-ttu-id="767cb-269">PVN deklarācijas informācija Lietuvai</span><span class="sxs-lookup"><span data-stu-id="767cb-269">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="767cb-270">Nīderlande</span><span class="sxs-lookup"><span data-stu-id="767cb-270">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="767cb-271">Zviedrija</span><span class="sxs-lookup"><span data-stu-id="767cb-271">Sweden</span></span>         |                                                                                 |






