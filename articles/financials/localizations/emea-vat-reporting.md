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
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: afcc2ea8c0ca3a5877b44fd758aec9d2caf92d92
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="f9475-103">PVN pārskati Eiropai</span><span class="sxs-lookup"><span data-stu-id="f9475-103">VAT reporting for Europe</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f9475-104">Šajā tēmā ir sniegta vispārīga informācija par pievienotās vērtības nodokļa (PVN) pārskatu iestatīšanu un ģenerēšanu noteiktām Eiropas valstīm.</span><span class="sxs-lookup"><span data-stu-id="f9475-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="f9475-105">Šajā tēmā ir aprakstīta vispārīga PVN deklarācijas iestatīšanas un ģenerēšanas metode.</span><span class="sxs-lookup"><span data-stu-id="f9475-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="f9475-106">Šo metodi izmanto lietotāji juridiskajās personās tālāk norādītajās valstīs/reģionos.</span><span class="sxs-lookup"><span data-stu-id="f9475-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="f9475-107">Austrija</span><span class="sxs-lookup"><span data-stu-id="f9475-107">Austria</span></span>
-   <span data-ttu-id="f9475-108">Beļģija</span><span class="sxs-lookup"><span data-stu-id="f9475-108">Belgium</span></span>
-   <span data-ttu-id="f9475-109">Čehija</span><span class="sxs-lookup"><span data-stu-id="f9475-109">Czech Republic</span></span>
-   <span data-ttu-id="f9475-110">Igaunija</span><span class="sxs-lookup"><span data-stu-id="f9475-110">Estonia</span></span>
-   <span data-ttu-id="f9475-111">Somija</span><span class="sxs-lookup"><span data-stu-id="f9475-111">Finland</span></span>
-   <span data-ttu-id="f9475-112">Vācija</span><span class="sxs-lookup"><span data-stu-id="f9475-112">Germany</span></span>
-   <span data-ttu-id="f9475-113">Latvija</span><span class="sxs-lookup"><span data-stu-id="f9475-113">Latvia</span></span>
-   <span data-ttu-id="f9475-114">Lietuva</span><span class="sxs-lookup"><span data-stu-id="f9475-114">Lithuania</span></span>
-   <span data-ttu-id="f9475-115">Nīderlande</span><span class="sxs-lookup"><span data-stu-id="f9475-115">Netherlands</span></span>
-   <span data-ttu-id="f9475-116">Zviedrija</span><span class="sxs-lookup"><span data-stu-id="f9475-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="f9475-117">PVN deklarācijas apskats</span><span class="sxs-lookup"><span data-stu-id="f9475-117">VAT statement overview</span></span>
<span data-ttu-id="f9475-118">PVN deklarācija ir balstīta uz nodokļu transakciju summām.</span><span class="sxs-lookup"><span data-stu-id="f9475-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="f9475-119">PVN deklarācijas ģenerēšanas process ietilpst PVN maksājuma procesā, kurš ir ieviests ar funkciju Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="f9475-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="f9475-120">Šī funkcija aprēķina PVN, kurš ir jāmaksā par attiecīgo periodu.</span><span class="sxs-lookup"><span data-stu-id="f9475-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="f9475-121">Nosegšanas aprēķinā ir iekļauts atlasītajam nosegšanas periodam nodokļu transakcijām grāmatotais PVN.</span><span class="sxs-lookup"><span data-stu-id="f9475-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="f9475-122">Process PVN deklarācijas datu aprēķināšanai ir balstīts uz attiecībām starp PVN kodiem un PVN pārskatu kodiem, kur PVN pārskatu kodi atbilst PVN deklarācijas lodziņiem (vai etiķetēm XML failā).</span><span class="sxs-lookup"><span data-stu-id="f9475-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="f9475-123">Attiecībā uz katru PVN kodu ir jāiestata PVN pārskatu kodi katram transakcijas tipam, piemēram, ar nodokli apliekamajai pārdošanai, ar nodokli apliekamajiem pirkumiem, ar nodokli apliekamajam importam.</span><span class="sxs-lookup"><span data-stu-id="f9475-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="f9475-124">Šie transakciju tipi ir aprakstīti tālāk šīs tēmas sadaļā PVN kodi PVN pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="f9475-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="f9475-125">Katram PVN pārskatu kodam ir jānorāda noteikts pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="f9475-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="f9475-126">Tajā pašā laikā PVN kodi ir saistīti ar noteiktu PVN iestādi, izmantojot PVN nosegšanas periodus.</span><span class="sxs-lookup"><span data-stu-id="f9475-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="f9475-127">Katrai PVN iestādei ir jānorāda noteikts pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="f9475-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="f9475-128">Tādējādi PVN koda pārskatu iestatīšanā var atlasīt tikai PVN pārskatu kodus ar vienādu pārskata izkārtojumu, kas attiecībā uz šo PVN kodu ir iestatīti PVN iestādei PVN nosegšanas periodos.</span><span class="sxs-lookup"><span data-stu-id="f9475-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="f9475-129">Ar pasūtījuma vai žurnāla grāmatošanu ģenerēta PVN transakcija ietver PVN kodu, PVN avotu, PVN virzienu un transakciju summas (nodokļu bāzes summu un nodokļu summu uzskaites valūtā, PVN valūtā un transakcijas valūtā).</span><span class="sxs-lookup"><span data-stu-id="f9475-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="f9475-130">Pamatojoties uz nodokļu transakciju atribūtu kombināciju, transakciju summas veido kopējās summas PVN pārskatu kodiem, kas norādīti PVN kodiem.</span><span class="sxs-lookup"><span data-stu-id="f9475-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="f9475-131">Nākamajā attēlā ir redzamas datu attiecības.</span><span class="sxs-lookup"><span data-stu-id="f9475-131">The following illustration shows the data relationship.</span></span>

![diagramma](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="f9475-133">PVN pārskata iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f9475-133">VAT statement setup</span></span>
<span data-ttu-id="f9475-134">Lai ģenerētu PVN pārskatu, ir jāiestata tālāk aprakstītie priekšnoteikumi.</span><span class="sxs-lookup"><span data-stu-id="f9475-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="f9475-135">PVN iestādes PVN pārskatiem</span><span class="sxs-lookup"><span data-stu-id="f9475-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="f9475-136">Lai varētu iestatīt PVN pārskatu kodus, ir jāatlasa attiecīgajai PVN iestādei atbilstošais pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="f9475-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="f9475-137">Lapā **PVN iestādes**, sadaļā **Vispārīgi** atlasiet vienumu **Pārskata izkārtojums**.</span><span class="sxs-lookup"><span data-stu-id="f9475-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="f9475-138">Šis izkārtojums tiek izmantots, kad iestatāt PVN pārskatu kodus.</span><span class="sxs-lookup"><span data-stu-id="f9475-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="f9475-139">PVN pārskatu kodi</span><span class="sxs-lookup"><span data-stu-id="f9475-139">Sales tax reporting codes</span></span>

<span data-ttu-id="f9475-140">PVN pārskatu kodi ir lodziņu kodi PVN deklarācijā vai etiķešu nosaukumi XML formātā.</span><span class="sxs-lookup"><span data-stu-id="f9475-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="f9475-141">Šie kodi tiek izmantoti, lai pārskatam apkopotu un sagatavotu summas.</span><span class="sxs-lookup"><span data-stu-id="f9475-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="f9475-142">Kad konfigurējat PVN deklarācijas elektroniskā pārskata formātu, tiek izmantoti rezultātu summu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="f9475-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="f9475-143">PVN pārskatu kodus varat izveidot un uzturēt lapā **PVN pārskatu kodi**.</span><span class="sxs-lookup"><span data-stu-id="f9475-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="f9475-144">Katram kodam ir jāpiešķir kāds pārskata izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="f9475-144">You must assign each code a report layout.</span></span> <span data-ttu-id="f9475-145">Pēc PVN pārskatu kodu izveidošanas šos kodus varat izvēlēties lapas **PVN kodi** sadaļā **Pārskata iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="f9475-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="f9475-146">PVN kodi PVN pārskatiem</span><span class="sxs-lookup"><span data-stu-id="f9475-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="f9475-147">Lapa <!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>PVN kodi</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="f9475-148">Nākamajā tabulā ir aprakstīti transakciju tipi pārskatu iestatīšanai PVN kodiem.</span><span class="sxs-lookup"><span data-stu-id="f9475-148">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="f9475-149">Šajā aprēķinā ir iekļautas transakcijas no visu tipu avotiem, izņemot PVN.</span><span class="sxs-lookup"><span data-stu-id="f9475-149">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9475-150"><strong>Transakcijas tips</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-150"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="f9475-151"><strong>Transakciju apraksts un summas, ko aprēķināt šim transakciju tipam</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-151"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-152"><strong>Ar nodokli apliekamā pārdošana</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-152"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="f9475-153">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-153">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-154">Transakcijas datums ietilpst atlasītajā periodā/</span><span class="sxs-lookup"><span data-stu-id="f9475-154">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="f9475-155">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-155">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-156">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-156">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-157"><strong>Pārdošana bez nodokļiem</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-157"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="f9475-158">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-158">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-159">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-159">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-160">Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-160">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="f9475-161">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-161">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-162"><strong>Maksājamais PVN</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-162"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="f9475-163">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-163">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-164">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-164">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-165">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-165">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-166">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-166">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-167"><strong>Ar nodokli apliekama pārdošanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-167"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-168">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-168">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-169">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-169">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-170">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-170">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-171">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-171">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-172"><strong>Ar nodokli neapliekama pārdošanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-172"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-173">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-173">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-174">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-174">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-175">Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-175">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="f9475-176">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-176">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-177"><strong>PVN pārdošanas kredīta notā</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-177"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-178">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-178">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-179">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-179">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-180">Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-180">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-181">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-181">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-182"><strong>Ar nodokļiem apliekamie pirkumi</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-182"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="f9475-183">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-183">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-184">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-184">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-185">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-185">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-186">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-186">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-187"><strong>Pirkšana bez nodokļiem</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-187"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="f9475-188">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-188">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-189">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-189">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-190">Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-190">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="f9475-191">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-191">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-192"><strong>Saņemtais PVN</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-192"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="f9475-193">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-193">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-194">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-194">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-195">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-195">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-196">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-196">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-197"><strong>Ar nodokli apliekama pirkšanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-197"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-198">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-198">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-199">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-199">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-200">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-200">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-201">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-201">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-202"><strong>Ar nodokli neapliekama pirkšanas kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-202"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-203">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-203">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-204">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-204">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-205">Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-205">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="f9475-206">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-206">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-207"><strong>PVN pirkšanas kredīta notā</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-207"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-208">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-208">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-209">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-209">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-210">Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</span><span class="sxs-lookup"><span data-stu-id="f9475-210">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f9475-211">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-211">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-212"><strong>Ar nodokli apliekams imports</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-212"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="f9475-213">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-213">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-214">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-214">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-215"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-215"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="f9475-216">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-216">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-217"><strong>Apliekamais imports</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-217"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="f9475-218">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-218">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-219">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-219">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-220"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-220"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f9475-221">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-221">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-222"><strong>Ar nodokli apliekama importa kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-222"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-223">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-223">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-224">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-224">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="f9475-225">e</span><span class="sxs-lookup"><span data-stu-id="f9475-225">e</span></span><li><span data-ttu-id="f9475-226"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-226"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f9475-227">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-227">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-228"><strong>Apliekamā importa kredīta nota</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-228"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="f9475-229">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-229">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-230">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-230">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-231">Nodokļu virziens ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-231">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="f9475-232">d</span><span class="sxs-lookup"><span data-stu-id="f9475-232">d</span></span><li><span data-ttu-id="f9475-233">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-233">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9475-234"><strong>Importa nodoklis</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-234"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="f9475-235">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-235">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-236">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-236">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-237"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-237"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f9475-238">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-238">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9475-239"><strong>Kompensēt importa nodokli</strong></span><span class="sxs-lookup"><span data-stu-id="f9475-239"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="f9475-240">Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu summas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-240">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f9475-241">Transakcijas datums ietilpst atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="f9475-241">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f9475-242"><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9475-242"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f9475-243">Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f9475-243">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f9475-244">Iepriekšējā tabulā tiek pieņems, ka tiek ievēroti tālāk aprakstītie kritēriji.</span><span class="sxs-lookup"><span data-stu-id="f9475-244">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="f9475-245">Nodokļu bāzes summa ir transakcijas summa no lauka **Izcelsme uzskaites valūtā**.</span><span class="sxs-lookup"><span data-stu-id="f9475-245">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="f9475-246">Nodokļu summa ir transakcijas summa no lauka **Reālā PVN summa uzskaites valūtā**.</span><span class="sxs-lookup"><span data-stu-id="f9475-246">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="f9475-247">Pārskatam konfigurēt ER modeli un formātu</span><span class="sxs-lookup"><span data-stu-id="f9475-247">Configure the ER model and format for the report</span></span>

<span data-ttu-id="f9475-248">Varat izmantot elektronisko pārskatu veidošanu (Electronic Reporting — ER), lai datus eksportētu dažādos elektroniskajos formātos, nemainot X++ kodu.</span><span class="sxs-lookup"><span data-stu-id="f9475-248">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="f9475-249">Papildinformāciju skatiet tālāk norādītajos resursos.</span><span class="sxs-lookup"><span data-stu-id="f9475-249">For additional information:</span></span>

-   [<span data-ttu-id="f9475-250">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="f9475-250">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="f9475-251">Lejupielādēt elektronisko pārskatu veidošanas konfigurāciju no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f9475-251">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="f9475-252">Lokalizācijas prasības — izveidot GER konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="f9475-252">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="f9475-253">Valstij specifiskie resursi PVN deklarācijām</span><span class="sxs-lookup"><span data-stu-id="f9475-253">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="f9475-254">Katras valsts PVN deklarācijai ir jāatbilst attiecīgās valsts likumdošanas prasībām.</span><span class="sxs-lookup"><span data-stu-id="f9475-254">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="f9475-255">Nākamajā tabulā uzskaitītajām valstīm pastāv sākotnēji definēti PVN deklarāciju vispārīgie modeļi un formāti.</span><span class="sxs-lookup"><span data-stu-id="f9475-255">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="f9475-256">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="f9475-256">Country</span></span>        | <span data-ttu-id="f9475-257">Papildinformācija</span><span class="sxs-lookup"><span data-stu-id="f9475-257">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f9475-258">Austrija</span><span class="sxs-lookup"><span data-stu-id="f9475-258">Austria</span></span>        |  [<span data-ttu-id="f9475-259">PVN deklarācijas informācija Austrijai</span><span class="sxs-lookup"><span data-stu-id="f9475-259">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="f9475-260">Beļģija</span><span class="sxs-lookup"><span data-stu-id="f9475-260">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="f9475-261">Čehija</span><span class="sxs-lookup"><span data-stu-id="f9475-261">Czech Republic</span></span> |  [<span data-ttu-id="f9475-262">PVN deklarācijas informācija Čehijai</span><span class="sxs-lookup"><span data-stu-id="f9475-262">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="f9475-263">Igaunija</span><span class="sxs-lookup"><span data-stu-id="f9475-263">Estonia</span></span>        |  [<span data-ttu-id="f9475-264">PVN deklarācijas informācija Igaunijai</span><span class="sxs-lookup"><span data-stu-id="f9475-264">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="f9475-265">Somija</span><span class="sxs-lookup"><span data-stu-id="f9475-265">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="f9475-266">Vācija</span><span class="sxs-lookup"><span data-stu-id="f9475-266">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="f9475-267">Itālija</span><span class="sxs-lookup"><span data-stu-id="f9475-267">Italy</span></span>          | [<span data-ttu-id="f9475-268">PVN deklarācijas informācija Itālijai</span><span class="sxs-lookup"><span data-stu-id="f9475-268">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="f9475-269">Latvija</span><span class="sxs-lookup"><span data-stu-id="f9475-269">Latvia</span></span>         | [<span data-ttu-id="f9475-270">PVN deklarācijas informācija Latvijai</span><span class="sxs-lookup"><span data-stu-id="f9475-270">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="f9475-271">Lietuva</span><span class="sxs-lookup"><span data-stu-id="f9475-271">Lithuania</span></span>      | [<span data-ttu-id="f9475-272">PVN deklarācijas informācija Lietuvai</span><span class="sxs-lookup"><span data-stu-id="f9475-272">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="f9475-273">Nīderlande</span><span class="sxs-lookup"><span data-stu-id="f9475-273">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="f9475-274">Zviedrija</span><span class="sxs-lookup"><span data-stu-id="f9475-274">Sweden</span></span>         |                                                                                 |






