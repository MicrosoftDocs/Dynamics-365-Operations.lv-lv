---
title: Power BI satura pakotne Pirkšanas tēriņu analīze
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Pirkšanas tēriņu analīze.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9741b5f30f5e62b9e80000953113377fe016253
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749373"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="b5a1b-103">Power BI satura pakotne Pirkšanas tēriņu analīze</span><span class="sxs-lookup"><span data-stu-id="b5a1b-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5a1b-104">Šajā tēmā ir aprakstīts, kas ir iekļauts satura pakotnē **Pirkšanas tēriņu analīze** programmā Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="b5a1b-105">Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b5a1b-106">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b5a1b-106">Overview</span></span>

<span data-ttu-id="b5a1b-107">Power BI satura pakotne **Pirkšanas tēriņu analīze** ir izveidota, lai palīdzētu iepirkumu nodaļas vadītājiem un par budžetu atbildīgajiem sekot pirkšanas tēriņiem.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="b5a1b-108">Vadītāji var analizēt pirkumu tēriņus šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="b5a1b-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="b5a1b-109">Līdzšinējā gada pirkumi (pēc kreditoru grupas, atsevišķa kreditora, sagādes kategorijas, atsevišķas preces un kreditora atrašanās vietas)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="b5a1b-110">Pirkumu izmaiņas pa gadiem (pēc kreditoru grupas un sagādes kategorijas)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="b5a1b-111">Saturam tiek izmantoti pirkumu transakciju dati, un tas nodrošina gan uzņēmuma līmeņa pirkumu rādītāju apkopošanas skatu, gan pirkumu tēriņu sadalījumu pēc kreditora vai preces.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="b5a1b-112">Pārskatos ir izceltas pirkumu tēriņu izmaiņas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="b5a1b-113">Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tēriņu tendencēm saistībā ar atsevišķiem kreditoriem un precēm.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="b5a1b-114">Turklāt diagrammas ataino pirkumu tēriņus dažādām sagādes kategorijām un kreditoru grupām.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="b5a1b-115">Tādēļ kategoriju un reģionālie vadītāji var izmantot šīs diagrammas, lai palīdzētu noteikt tēriņu darbību izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b5a1b-116">Piekļuve Power BI satura pakotnei</span><span class="sxs-lookup"><span data-stu-id="b5a1b-116">Accessing the Power BI content</span></span>
<span data-ttu-id="b5a1b-117">Power BI satura pakotne **Pirkšanas tēriņu analīze** tiek rādīta lapā **Pirkšanas un tēriņu rādītāju analīze** (**Sagāde un avoti** \> **Pieprasījumi un pārskati** \> **Pirkšanas rādītāju analīze** \> **Pirkšanas un tēriņu rādītāju analīze**).</span><span class="sxs-lookup"><span data-stu-id="b5a1b-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b5a1b-118">Power BI satura pakotnē iekļautie rādītāji</span><span class="sxs-lookup"><span data-stu-id="b5a1b-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="b5a1b-119">Power BI satura pakotnē **Pirkšanas tēriņu analīze** ir iekļauts pārskats, kas sastāv no rādītāju kopas.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="b5a1b-120">Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="b5a1b-121">Zemāk norādītajās sadaļās ir sniegts pārskats par vizualizācijām.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="b5a1b-122">Pārskata lapa pirkumiem pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="b5a1b-122">Purchase by vendor report page</span></span>
<span data-ttu-id="b5a1b-123">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-123">**Charts**</span></span>
- <span data-ttu-id="b5a1b-124">Pirmie 10 kreditori pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="b5a1b-125">Pirkumu kopsumma pēc kreditoru grupas/valsts/nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="b5a1b-126">Pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="b5a1b-127">Vidējie pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="b5a1b-128">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-128">**Tiles**</span></span>
- <span data-ttu-id="b5a1b-129">Kopējā pirkšana</span><span class="sxs-lookup"><span data-stu-id="b5a1b-129">Total purchase</span></span>
- <span data-ttu-id="b5a1b-130">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="b5a1b-130">YOY purchase growth</span></span>
- <span data-ttu-id="b5a1b-131">Kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="b5a1b-131">Total # vendors</span></span>
- <span data-ttu-id="b5a1b-132">Aktīvo kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="b5a1b-132">Total # of active vendors</span></span>

<span data-ttu-id="b5a1b-133">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="b5a1b-134">Pārskata lapa pirkumiem pēc preces</span><span class="sxs-lookup"><span data-stu-id="b5a1b-134">Purchase by product report page</span></span>

<span data-ttu-id="b5a1b-135">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-135">**Charts**</span></span>
- <span data-ttu-id="b5a1b-136">Pirkumi pēc sagādes kategorijas/preces nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="b5a1b-137">Pirkumu kopsumma pēc sagādes kategorijas/preces nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="b5a1b-138">Pirmās 10 preces pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="b5a1b-139">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-139">**Tiles**</span></span>
- <span data-ttu-id="b5a1b-140">Preču kopskaits</span><span class="sxs-lookup"><span data-stu-id="b5a1b-140">Total # of products</span></span></li>
- <span data-ttu-id="b5a1b-141">Aktīvo preču kopskaits procentos no preču kopskaita</span><span class="sxs-lookup"><span data-stu-id="b5a1b-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="b5a1b-142">To preču skaits, kas veido 80% pirkumu</span><span class="sxs-lookup"><span data-stu-id="b5a1b-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="b5a1b-143">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="b5a1b-144">Pārskata lapa pirkumiem pēc perioda</span><span class="sxs-lookup"><span data-stu-id="b5a1b-144">Purchase by period report page</span></span>
<span data-ttu-id="b5a1b-145">Šajā lapā parādīti šī gada un pagājušā gada pirkumi un palielinājums pēc sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="b5a1b-146">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-146">**Charts**</span></span> 
- <span data-ttu-id="b5a1b-147">Pirkumi pēc mēneša/dienas (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="b5a1b-148">Apkopotā pirkumu novirze pa gadiem (ūdenskrituma diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="b5a1b-149">Pirkumu kopsummas palielinājums pa gadiem (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="b5a1b-150">Sagādes izraksts (matrica)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="b5a1b-151">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-151">**Tiles**</span></span>
- <span data-ttu-id="b5a1b-152">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="b5a1b-152">YOY purchase growth</span></span>
- <span data-ttu-id="b5a1b-153">Pirkumu palielinājums (%)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-153">YOY purchase growth %</span></span>

<span data-ttu-id="b5a1b-154">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="b5a1b-155">Pārskata lapa pirkumiem pēc vietas</span><span class="sxs-lookup"><span data-stu-id="b5a1b-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="b5a1b-156">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-156">**Charts**</span></span>
- <span data-ttu-id="b5a1b-157">Pirkumi pēc pilsētas</span><span class="sxs-lookup"><span data-stu-id="b5a1b-157">Purchase by city</span></span>
- <span data-ttu-id="b5a1b-158">Pirkumu palielinājums pa gadiem (%)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="b5a1b-159">Pirkumi pēc valsts</span><span class="sxs-lookup"><span data-stu-id="b5a1b-159">Purchase by country</span></span>

<span data-ttu-id="b5a1b-160">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="b5a1b-161">Pārskata lapa pirkumu tēriņu analīzei pēc laika</span><span class="sxs-lookup"><span data-stu-id="b5a1b-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="b5a1b-162">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-162">**Charts**</span></span> 
- <span data-ttu-id="b5a1b-163">Pašreizējā gada pirkumi pēc mēneša/dienas (līniju diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="b5a1b-164">Pašreizējā un pagājušā gada pirkumi (līniju un stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="b5a1b-165">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="b5a1b-166">Pārskata lapa pirkumu tēriņu analīzei pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="b5a1b-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="b5a1b-167">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="b5a1b-167">**Charts**</span></span> 
- <span data-ttu-id="b5a1b-168">Pirmo 10 kreditoru pirkumi procentos (%) no pirkumiem (piltuves diagramma)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="b5a1b-169">Pirmie 10 kreditori ar palielinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="b5a1b-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="b5a1b-170">Pirmie 10 kreditori ar samazinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="b5a1b-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="b5a1b-171">**Piemērs** 
</span><span class="sxs-lookup"><span data-stu-id="b5a1b-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="b5a1b-172">Datu modelis un elementi</span><span class="sxs-lookup"><span data-stu-id="b5a1b-172">Data model and entities</span></span>
<span data-ttu-id="b5a1b-173">Power BI satura pakotnes **Pirkšanas tēriņu analīze** pārskatu lapu aizpildīšanai tiek izmantoti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="b5a1b-174">Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="b5a1b-175">Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="b5a1b-176">Papildinformāciju skatiet rakstā [Power BI integrācija elementu krātuvē](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="b5a1b-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="b5a1b-177">Šajā satura pakotnē ietvertie apkopošanas mērījumi ir to apkopošanas mērījumu apakškopa, kas ir pieejami pirkšanas kubā programmās Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="b5a1b-178">Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="b5a1b-179">Papildinformāciju skatiet emuāra ieraksta [Power BI integrāciju elementu krātuve](power-bi-integration-entity-store.md) sadaļā par procedūru apkopošanas mērījumu sagatavošanai elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="b5a1b-180">Tālāk norādītie galvenie apkopošanas mērījumi ir tieši pieejami no elementa Rēķina rindas, un tie tiek izmantoti kā satura pamatdati.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="b5a1b-181">Elements</span><span class="sxs-lookup"><span data-stu-id="b5a1b-181">Entity</span></span>        | <span data-ttu-id="b5a1b-182">Galvenie apkopošanas mērījumi</span><span class="sxs-lookup"><span data-stu-id="b5a1b-182">Key aggregate measurements</span></span> | <span data-ttu-id="b5a1b-183">Datu avots</span><span class="sxs-lookup"><span data-stu-id="b5a1b-183">Data source</span></span>                                 | <span data-ttu-id="b5a1b-184">Lauks</span><span class="sxs-lookup"><span data-stu-id="b5a1b-184">Field</span></span>              | <span data-ttu-id="b5a1b-185">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b5a1b-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="b5a1b-186">Rēķina rindas</span><span class="sxs-lookup"><span data-stu-id="b5a1b-186">Invoice lines</span></span> | <span data-ttu-id="b5a1b-187">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="b5a1b-187">Purchase</span></span>                   | <span data-ttu-id="b5a1b-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="b5a1b-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="b5a1b-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="b5a1b-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="b5a1b-190">Summa uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="b5a1b-191">Tālāk esošajā tabulā ir norādīti galvenie satura mērījumi, kas tiek aprēķināti no elementa Rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="b5a1b-192">Mērs</span><span class="sxs-lookup"><span data-stu-id="b5a1b-192">Measure</span></span>               | <span data-ttu-id="b5a1b-193">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="b5a1b-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a1b-194">Pašreizējā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="b5a1b-194">Purchase current year</span></span> | <span data-ttu-id="b5a1b-195">Pašreizējā gada pirkumi = SUM('Rēģina rindas'\[Pirkšana\])</span><span class="sxs-lookup"><span data-stu-id="b5a1b-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="b5a1b-196">Pagājušā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="b5a1b-196">Purchase last year</span></span>    | <span data-ttu-id="b5a1b-197">Pagājušā gada pirkumi = CALCULATE(SUM('Rēķina rindas'\[Pirkšana\]), SAMEPERIODLASTYEAR(Datumi\[Datums\]))</span><span class="sxs-lookup"><span data-stu-id="b5a1b-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="b5a1b-198">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="b5a1b-198">YOY purchase growth</span></span>   | <span data-ttu-id="b5a1b-199">Pirkumu palielinājums pa gadiem = \[Pašreizējā gada pirkumi\] – \[Pagājušā gada pirkumi\]</span><span class="sxs-lookup"><span data-stu-id="b5a1b-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="b5a1b-200">Tālāk norādītās galvenās dimensijas saturam tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="b5a1b-201">Elements</span><span class="sxs-lookup"><span data-stu-id="b5a1b-201">Entity</span></span>                 | <span data-ttu-id="b5a1b-202">Atribūtu piemēri</span><span class="sxs-lookup"><span data-stu-id="b5a1b-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b5a1b-203">Kreditori</span><span class="sxs-lookup"><span data-stu-id="b5a1b-203">Vendors</span></span>                | <span data-ttu-id="b5a1b-204">Kreditoru grupas, Kreditora valsts vai reģions, Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="b5a1b-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="b5a1b-205">Preces</span><span class="sxs-lookup"><span data-stu-id="b5a1b-205">Products</span></span>               | <span data-ttu-id="b5a1b-206">Preces numurs, Preces nosaukums, Krājumu grupas nosaukums</span><span class="sxs-lookup"><span data-stu-id="b5a1b-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="b5a1b-207">Sagādes kategorijas</span><span class="sxs-lookup"><span data-stu-id="b5a1b-207">Procurement categories</span></span> | <span data-ttu-id="b5a1b-208">Sagādes kategorija, Sagādes kategoriju nosaukumi</span><span class="sxs-lookup"><span data-stu-id="b5a1b-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="b5a1b-209">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="b5a1b-209">Legal entities</span></span>         | <span data-ttu-id="b5a1b-210">Juridiskās personas nosaukums</span><span class="sxs-lookup"><span data-stu-id="b5a1b-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="b5a1b-211">Datumi</span><span class="sxs-lookup"><span data-stu-id="b5a1b-211">Dates</span></span>                  | <span data-ttu-id="b5a1b-212">Datumi, Gada nobīde</span><span class="sxs-lookup"><span data-stu-id="b5a1b-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="b5a1b-213">Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="b5a1b-214">Taču varat mainīt datumu filtru pārskata filtru sadaļā.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="b5a1b-215">Varat mainīt arī uzņēmuma filtru.</span><span class="sxs-lookup"><span data-stu-id="b5a1b-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]