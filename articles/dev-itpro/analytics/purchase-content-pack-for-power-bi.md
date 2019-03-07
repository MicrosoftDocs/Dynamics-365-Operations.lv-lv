---
title: Power BI satura pakotne Pirkšanas tēriņu analīze
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Pirkšanas tēriņu analīze. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "313846"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="600e9-104">Power BI satura pakotne Pirkšanas tēriņu analīze</span><span class="sxs-lookup"><span data-stu-id="600e9-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="600e9-105">Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Pirkšanas tēriņu analīze**.</span><span class="sxs-lookup"><span data-stu-id="600e9-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="600e9-106">Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.</span><span class="sxs-lookup"><span data-stu-id="600e9-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="600e9-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="600e9-107">Overview</span></span>

<span data-ttu-id="600e9-108">Power BI satura pakotne **Pirkšanas tēriņu analīze** ir izveidota, lai palīdzētu iepirkumu nodaļas vadītājiem un par budžetu atbildīgajiem sekot pirkšanas tēriņiem.</span><span class="sxs-lookup"><span data-stu-id="600e9-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="600e9-109">Vadītāji var analizēt pirkumu tēriņus šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="600e9-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="600e9-110">Līdzšinējā gada pirkumi (pēc kreditoru grupas, atsevišķa kreditora, sagādes kategorijas, atsevišķas preces un kreditora atrašanās vietas)</span><span class="sxs-lookup"><span data-stu-id="600e9-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="600e9-111">Pirkumu izmaiņas pa gadiem (pēc kreditoru grupas un sagādes kategorijas)</span><span class="sxs-lookup"><span data-stu-id="600e9-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="600e9-112">Saturam tiek izmantoti pirkumu transakciju dati, un tas nodrošina gan uzņēmuma līmeņa pirkumu rādītāju apkopošanas skatu, gan pirkumu tēriņu sadalījumu pēc kreditora vai preces.</span><span class="sxs-lookup"><span data-stu-id="600e9-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="600e9-113">Pārskatos ir izceltas pirkumu tēriņu izmaiņas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="600e9-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="600e9-114">Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tēriņu tendencēm saistībā ar atsevišķiem kreditoriem un precēm.</span><span class="sxs-lookup"><span data-stu-id="600e9-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="600e9-115">Turklāt diagrammas ataino pirkumu tēriņus dažādām sagādes kategorijām un kreditoru grupām.</span><span class="sxs-lookup"><span data-stu-id="600e9-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="600e9-116">Tādēļ kategoriju un reģionālie vadītāji var izmantot šīs diagrammas, lai palīdzētu noteikt tēriņu darbību izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="600e9-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="600e9-117">Piekļuve Power BI satura pakotnei</span><span class="sxs-lookup"><span data-stu-id="600e9-117">Accessing the Power BI content</span></span>
<span data-ttu-id="600e9-118">Power BI satura pakotne **Pirkšanas tēriņu analīze** tiek rādīta lapā **Pirkšanas un tēriņu rādītāju analīze** (**Sagāde un avoti** \> **Pieprasījumi un pārskati** \> **Pirkšanas rādītāju analīze** \> **Pirkšanas un tēriņu rādītāju analīze**).</span><span class="sxs-lookup"><span data-stu-id="600e9-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="600e9-119">Power BI satura pakotnē iekļautie rādītāji</span><span class="sxs-lookup"><span data-stu-id="600e9-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="600e9-120">Power BI satura pakotnē **Pirkšanas tēriņu analīze** ir iekļauts pārskats, kas sastāv no rādītāju kopas.</span><span class="sxs-lookup"><span data-stu-id="600e9-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="600e9-121">Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas.</span><span class="sxs-lookup"><span data-stu-id="600e9-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="600e9-122">Zemāk norādītajā tabulā ir sniegts pārskats par vizualizācijām.</span><span class="sxs-lookup"><span data-stu-id="600e9-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="600e9-123">Pārskata lapa</span><span class="sxs-lookup"><span data-stu-id="600e9-123">Report page</span></span></th>
<th><span data-ttu-id="600e9-124">Diagrammas</span><span class="sxs-lookup"><span data-stu-id="600e9-124">Charts</span></span></th>
<th><span data-ttu-id="600e9-125">Elementi</span><span class="sxs-lookup"><span data-stu-id="600e9-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="600e9-126">Pirkumi pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="600e9-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="600e9-127">Pirmie 10 kreditori pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="600e9-128">Pirkumu kopsumma pēc kreditoru grupas/valsts/nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="600e9-129">Pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="600e9-130">Vidējie pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="600e9-131">Kopējā pirkšana</span><span class="sxs-lookup"><span data-stu-id="600e9-131">Total purchase</span></span></li>
<li><span data-ttu-id="600e9-132">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="600e9-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="600e9-133">Kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="600e9-133">Total # vendors</span></span></li>
<li><span data-ttu-id="600e9-134">Aktīvo kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="600e9-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="600e9-135">Pirkumi pēc preces</span><span class="sxs-lookup"><span data-stu-id="600e9-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="600e9-136">Pirkumi pēc sagādes kategorijas/preces nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="600e9-137">Pirkumu kopsumma pēc sagādes kategorijas/preces nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="600e9-138">Pirmās 10 preces pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="600e9-139">Preču kopskaits</span><span class="sxs-lookup"><span data-stu-id="600e9-139">Total # of products</span></span></li>
<li><span data-ttu-id="600e9-140">Aktīvo preču kopskaits procentos no preču kopskaita</span><span class="sxs-lookup"><span data-stu-id="600e9-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="600e9-141">To preču skaits, kas veido 80% pirkumu</span><span class="sxs-lookup"><span data-stu-id="600e9-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="600e9-142">Pirkumi pēc perioda\*</span><span class="sxs-lookup"><span data-stu-id="600e9-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="600e9-143">Pirkumi pēc mēneša/dienas (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="600e9-144">Apkopotā pirkumu novirze pa gadiem (ūdenskrituma diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="600e9-145">Pirkumu kopsummas palielinājums pa gadiem (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="600e9-146">Sagādes izraksts (matrica)</span><span class="sxs-lookup"><span data-stu-id="600e9-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="600e9-147">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="600e9-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="600e9-148">Pirkumu palielinājums (%)</span><span class="sxs-lookup"><span data-stu-id="600e9-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="600e9-149">Pirkumi pēc kreditora atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="600e9-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="600e9-150">Pirkumi pēc pilsētas</span><span class="sxs-lookup"><span data-stu-id="600e9-150">Purchase by city</span></span></li>
<li><span data-ttu-id="600e9-151">Pirkumu palielinājums pa gadiem (%)</span><span class="sxs-lookup"><span data-stu-id="600e9-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="600e9-152">Pirkumi pēc valsts</span><span class="sxs-lookup"><span data-stu-id="600e9-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="600e9-153">Pirkumu tēriņu analīze pēc laika</span><span class="sxs-lookup"><span data-stu-id="600e9-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="600e9-154">Pašreizējā gada pirkumi pēc mēneša/dienas (līniju diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="600e9-155">Pašreizējā un pagājušā gada pirkumi (līniju un stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="600e9-156">Pirkumu tēriņu analīze pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="600e9-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="600e9-157">Pirmo 10 kreditoru pirkumi procentos (%) no pirkumiem (piltuves diagramma)</span><span class="sxs-lookup"><span data-stu-id="600e9-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="600e9-158">Pirmie 10 kreditori ar palielinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="600e9-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="600e9-159">Pirmie 10 kreditori ar samazinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="600e9-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="600e9-160">\* Šī gada un pagājušā gada pirkumi un palielinājums pēc sagādes kategorijas</span><span class="sxs-lookup"><span data-stu-id="600e9-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="600e9-161">Datu modelis un elementi</span><span class="sxs-lookup"><span data-stu-id="600e9-161">Data model and entities</span></span>
<span data-ttu-id="600e9-162">Power BI satura pakotnes **Pirkšanas tēriņu analīze** pārskatu lapu aizpildīšanai tiek izmantoti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="600e9-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="600e9-163">Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="600e9-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="600e9-164">Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze.</span><span class="sxs-lookup"><span data-stu-id="600e9-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="600e9-165">Papildinformāciju skatiet rakstā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="600e9-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="600e9-166">Šajā satura pakotnē ietvertie apkopošanas mērījumi ir to apkopošanas mērījumu apakškopa, kas ir pieejami pirkšanas kubā programmās Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="600e9-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="600e9-167">Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami.</span><span class="sxs-lookup"><span data-stu-id="600e9-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="600e9-168">Papildinformāciju skatiet emuāra ieraksta [Apskats par Power BI integrāciju elementu krātuvi](power-bi-integration-entity-store.md) sadaļā par procedūru apkopošanas mērījumu sagatavošanai elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="600e9-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="600e9-169">Tālāk norādītie galvenie apkopošanas mērījumi ir tieši pieejami no elementa Rēķina rindas, un tie tiek izmantoti kā satura pamatdati.</span><span class="sxs-lookup"><span data-stu-id="600e9-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="600e9-170">Elements</span><span class="sxs-lookup"><span data-stu-id="600e9-170">Entity</span></span>        | <span data-ttu-id="600e9-171">Galvenie apkopošanas mērījumi</span><span class="sxs-lookup"><span data-stu-id="600e9-171">Key aggregate measurements</span></span> | <span data-ttu-id="600e9-172">Datu avots</span><span class="sxs-lookup"><span data-stu-id="600e9-172">Data source</span></span>                                 | <span data-ttu-id="600e9-173">Lauks</span><span class="sxs-lookup"><span data-stu-id="600e9-173">Field</span></span>              | <span data-ttu-id="600e9-174">Apraksts</span><span class="sxs-lookup"><span data-stu-id="600e9-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="600e9-175">Rēķina rindas</span><span class="sxs-lookup"><span data-stu-id="600e9-175">Invoice lines</span></span> | <span data-ttu-id="600e9-176">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="600e9-176">Purchase</span></span>                   | <span data-ttu-id="600e9-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="600e9-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="600e9-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="600e9-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="600e9-179">Summa uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="600e9-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="600e9-180">Tālāk esošajā tabulā ir norādīti galvenie satura mērījumi, kas tiek aprēķināti no elementa Rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="600e9-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="600e9-181">Mērs</span><span class="sxs-lookup"><span data-stu-id="600e9-181">Measure</span></span>               | <span data-ttu-id="600e9-182">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="600e9-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600e9-183">Pašreizējā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="600e9-183">Purchase current year</span></span> | <span data-ttu-id="600e9-184">Pašreizējā gada pirkumi = SUM('Rēģina rindas'\[Pirkšana\])</span><span class="sxs-lookup"><span data-stu-id="600e9-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="600e9-185">Pagājušā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="600e9-185">Purchase last year</span></span>    | <span data-ttu-id="600e9-186">Pagājušā gada pirkumi = CALCULATE(SUM('Rēķina rindas'\[Pirkšana\]), SAMEPERIODLASTYEAR(Datumi\[Datums\]))</span><span class="sxs-lookup"><span data-stu-id="600e9-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="600e9-187">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="600e9-187">YOY purchase growth</span></span>   | <span data-ttu-id="600e9-188">Pirkumu palielinājums pa gadiem = \[Pašreizējā gada pirkumi\] – \[Pagājušā gada pirkumi\]</span><span class="sxs-lookup"><span data-stu-id="600e9-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="600e9-189">Tālāk norādītās galvenās dimensijas saturam tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.</span><span class="sxs-lookup"><span data-stu-id="600e9-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="600e9-190">Elements</span><span class="sxs-lookup"><span data-stu-id="600e9-190">Entity</span></span>                 | <span data-ttu-id="600e9-191">Atribūtu piemēri</span><span class="sxs-lookup"><span data-stu-id="600e9-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="600e9-192">Kreditori</span><span class="sxs-lookup"><span data-stu-id="600e9-192">Vendors</span></span>                | <span data-ttu-id="600e9-193">Kreditoru grupas, Kreditora valsts vai reģions, Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="600e9-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="600e9-194">Preces</span><span class="sxs-lookup"><span data-stu-id="600e9-194">Products</span></span>               | <span data-ttu-id="600e9-195">Preces numurs, Preces nosaukums, Krājumu grupas nosaukums</span><span class="sxs-lookup"><span data-stu-id="600e9-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="600e9-196">Sagādes kategorijas</span><span class="sxs-lookup"><span data-stu-id="600e9-196">Procurement categories</span></span> | <span data-ttu-id="600e9-197">Sagādes kategorija, Sagādes kategoriju nosaukumi</span><span class="sxs-lookup"><span data-stu-id="600e9-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="600e9-198">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="600e9-198">Legal entities</span></span>         | <span data-ttu-id="600e9-199">Juridiskās personas nosaukums</span><span class="sxs-lookup"><span data-stu-id="600e9-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="600e9-200">Datumi</span><span class="sxs-lookup"><span data-stu-id="600e9-200">Dates</span></span>                  | <span data-ttu-id="600e9-201">Datumi, Gada nobīde</span><span class="sxs-lookup"><span data-stu-id="600e9-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="600e9-202">Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu.</span><span class="sxs-lookup"><span data-stu-id="600e9-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="600e9-203">Taču varat mainīt datumu filtru pārskata filtru sadaļā.</span><span class="sxs-lookup"><span data-stu-id="600e9-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="600e9-204">Varat mainīt arī uzņēmuma filtru.</span><span class="sxs-lookup"><span data-stu-id="600e9-204">You can also change the company filter.</span></span>
