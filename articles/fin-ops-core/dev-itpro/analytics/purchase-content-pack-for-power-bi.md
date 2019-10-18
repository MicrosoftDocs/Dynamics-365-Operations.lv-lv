---
title: Power BI satura pakotne Pirkšanas tēriņu analīze
description: Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pakotnē Pirkšanas tēriņu analīze. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182857"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="a1144-104">Power BI satura pakotne Pirkšanas tēriņu analīze</span><span class="sxs-lookup"><span data-stu-id="a1144-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1144-105">Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē **Pirkšanas tēriņu analīze**.</span><span class="sxs-lookup"><span data-stu-id="a1144-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="a1144-106">Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.</span><span class="sxs-lookup"><span data-stu-id="a1144-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="a1144-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a1144-107">Overview</span></span>

<span data-ttu-id="a1144-108">Power BI satura pakotne **Pirkšanas tēriņu analīze** ir izveidota, lai palīdzētu iepirkumu nodaļas vadītājiem un par budžetu atbildīgajiem sekot pirkšanas tēriņiem.</span><span class="sxs-lookup"><span data-stu-id="a1144-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="a1144-109">Vadītāji var analizēt pirkumu tēriņus šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="a1144-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="a1144-110">Līdzšinējā gada pirkumi (pēc kreditoru grupas, atsevišķa kreditora, sagādes kategorijas, atsevišķas preces un kreditora atrašanās vietas)</span><span class="sxs-lookup"><span data-stu-id="a1144-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="a1144-111">Pirkumu izmaiņas pa gadiem (pēc kreditoru grupas un sagādes kategorijas)</span><span class="sxs-lookup"><span data-stu-id="a1144-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="a1144-112">Saturam tiek izmantoti pirkumu transakciju dati, un tas nodrošina gan uzņēmuma līmeņa pirkumu rādītāju apkopošanas skatu, gan pirkumu tēriņu sadalījumu pēc kreditora vai preces.</span><span class="sxs-lookup"><span data-stu-id="a1144-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="a1144-113">Pārskatos ir izceltas pirkumu tēriņu izmaiņas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="a1144-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="a1144-114">Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tēriņu tendencēm saistībā ar atsevišķiem kreditoriem un precēm.</span><span class="sxs-lookup"><span data-stu-id="a1144-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="a1144-115">Turklāt diagrammas ataino pirkumu tēriņus dažādām sagādes kategorijām un kreditoru grupām.</span><span class="sxs-lookup"><span data-stu-id="a1144-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="a1144-116">Tādēļ kategoriju un reģionālie vadītāji var izmantot šīs diagrammas, lai palīdzētu noteikt tēriņu darbību izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="a1144-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="a1144-117">Piekļuve Power BI satura pakotnei</span><span class="sxs-lookup"><span data-stu-id="a1144-117">Accessing the Power BI content</span></span>
<span data-ttu-id="a1144-118">Power BI satura pakotne **Pirkšanas tēriņu analīze** tiek rādīta lapā **Pirkšanas un tēriņu rādītāju analīze** (**Sagāde un avoti** \> **Pieprasījumi un pārskati** \> **Pirkšanas rādītāju analīze** \> **Pirkšanas un tēriņu rādītāju analīze**).</span><span class="sxs-lookup"><span data-stu-id="a1144-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="a1144-119">Power BI satura pakotnē iekļautie rādītāji</span><span class="sxs-lookup"><span data-stu-id="a1144-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="a1144-120">Power BI satura pakotnē **Pirkšanas tēriņu analīze** ir iekļauts pārskats, kas sastāv no rādītāju kopas.</span><span class="sxs-lookup"><span data-stu-id="a1144-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="a1144-121">Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas.</span><span class="sxs-lookup"><span data-stu-id="a1144-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="a1144-122">Zemāk norādītajās sadaļās ir sniegts pārskats par vizualizācijām.</span><span class="sxs-lookup"><span data-stu-id="a1144-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="a1144-123">Pārskata lapa pirkumiem pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="a1144-123">Purchase by vendor report page</span></span>
<span data-ttu-id="a1144-124">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="a1144-124">**Charts**</span></span>
- <span data-ttu-id="a1144-125">Pirmie 10 kreditori pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="a1144-126">Pirkumu kopsumma pēc kreditoru grupas/valsts/nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="a1144-127">Pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="a1144-128">Vidējie pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="a1144-129">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="a1144-129">**Tiles**</span></span>
- <span data-ttu-id="a1144-130">Kopējā pirkšana</span><span class="sxs-lookup"><span data-stu-id="a1144-130">Total purchase</span></span>
- <span data-ttu-id="a1144-131">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="a1144-131">YOY purchase growth</span></span>
- <span data-ttu-id="a1144-132">Kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="a1144-132">Total # vendors</span></span>
- <span data-ttu-id="a1144-133">Aktīvo kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="a1144-133">Total # of active vendors</span></span>

<span data-ttu-id="a1144-134">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="a1144-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="a1144-135">Pārskata lapa pirkumiem pēc preces</span><span class="sxs-lookup"><span data-stu-id="a1144-135">Purchase by product report page</span></span>

<span data-ttu-id="a1144-136">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="a1144-136">**Charts**</span></span>
- <span data-ttu-id="a1144-137">Pirkumi pēc sagādes kategorijas/preces nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="a1144-138">Pirkumu kopsumma pēc sagādes kategorijas/preces nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="a1144-139">Pirmās 10 preces pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="a1144-140">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="a1144-140">**Tiles**</span></span>
- <span data-ttu-id="a1144-141">Preču kopskaits</span><span class="sxs-lookup"><span data-stu-id="a1144-141">Total # of products</span></span></li>
- <span data-ttu-id="a1144-142">Aktīvo preču kopskaits procentos no preču kopskaita</span><span class="sxs-lookup"><span data-stu-id="a1144-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="a1144-143">To preču skaits, kas veido 80% pirkumu</span><span class="sxs-lookup"><span data-stu-id="a1144-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="a1144-144">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="a1144-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="a1144-145">Pārskata lapa pirkumiem pēc perioda</span><span class="sxs-lookup"><span data-stu-id="a1144-145">Purchase by period report page</span></span>
<span data-ttu-id="a1144-146">Šajā lapā parādīti šī gada un pagājušā gada pirkumi un palielinājums pēc sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a1144-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="a1144-147">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="a1144-147">**Charts**</span></span> 
- <span data-ttu-id="a1144-148">Pirkumi pēc mēneša/dienas (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="a1144-149">Apkopotā pirkumu novirze pa gadiem (ūdenskrituma diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="a1144-150">Pirkumu kopsummas palielinājums pa gadiem (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="a1144-151">Sagādes izraksts (matrica)</span><span class="sxs-lookup"><span data-stu-id="a1144-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="a1144-152">**Elementi**</span><span class="sxs-lookup"><span data-stu-id="a1144-152">**Tiles**</span></span>
- <span data-ttu-id="a1144-153">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="a1144-153">YOY purchase growth</span></span>
- <span data-ttu-id="a1144-154">Pirkumu palielinājums (%)</span><span class="sxs-lookup"><span data-stu-id="a1144-154">YOY purchase growth %</span></span>

<span data-ttu-id="a1144-155">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="a1144-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="a1144-156">Pārskata lapa pirkumiem pēc vietas</span><span class="sxs-lookup"><span data-stu-id="a1144-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="a1144-157">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="a1144-157">**Charts**</span></span>
- <span data-ttu-id="a1144-158">Pirkumi pēc pilsētas</span><span class="sxs-lookup"><span data-stu-id="a1144-158">Purchase by city</span></span>
- <span data-ttu-id="a1144-159">Pirkumu palielinājums pa gadiem (%)</span><span class="sxs-lookup"><span data-stu-id="a1144-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="a1144-160">Pirkumi pēc valsts</span><span class="sxs-lookup"><span data-stu-id="a1144-160">Purchase by country</span></span>

<span data-ttu-id="a1144-161">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="a1144-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="a1144-162">Pārskata lapa pirkumu tēriņu analīzei pēc laika</span><span class="sxs-lookup"><span data-stu-id="a1144-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="a1144-163">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="a1144-163">**Charts**</span></span> 
- <span data-ttu-id="a1144-164">Pašreizējā gada pirkumi pēc mēneša/dienas (līniju diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="a1144-165">Pašreizējā un pagājušā gada pirkumi (līniju un stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="a1144-166">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="a1144-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="a1144-167">Pārskata lapa pirkumu tēriņu analīzei pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="a1144-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="a1144-168">**Diagrammas**</span><span class="sxs-lookup"><span data-stu-id="a1144-168">**Charts**</span></span> 
- <span data-ttu-id="a1144-169">Pirmo 10 kreditoru pirkumi procentos (%) no pirkumiem (piltuves diagramma)</span><span class="sxs-lookup"><span data-stu-id="a1144-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="a1144-170">Pirmie 10 kreditori ar palielinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="a1144-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="a1144-171">Pirmie 10 kreditori ar samazinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="a1144-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="a1144-172">**Piemērs** 
</span><span class="sxs-lookup"><span data-stu-id="a1144-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="a1144-173">Datu modelis un elementi</span><span class="sxs-lookup"><span data-stu-id="a1144-173">Data model and entities</span></span>
<span data-ttu-id="a1144-174">Power BI satura pakotnes **Pirkšanas tēriņu analīze** pārskatu lapu aizpildīšanai tiek izmantoti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="a1144-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="a1144-175">Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="a1144-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="a1144-176">Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze.</span><span class="sxs-lookup"><span data-stu-id="a1144-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="a1144-177">Papildinformāciju skatiet rakstā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="a1144-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="a1144-178">Šajā satura pakotnē ietvertie apkopošanas mērījumi ir to apkopošanas mērījumu apakškopa, kas ir pieejami pirkšanas kubā programmās Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="a1144-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="a1144-179">Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami.</span><span class="sxs-lookup"><span data-stu-id="a1144-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="a1144-180">Papildinformāciju skatiet emuāra ieraksta [Apskats par Power BI integrāciju elementu krātuvi](power-bi-integration-entity-store.md) sadaļā par procedūru apkopošanas mērījumu sagatavošanai elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="a1144-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="a1144-181">Tālāk norādītie galvenie apkopošanas mērījumi ir tieši pieejami no elementa Rēķina rindas, un tie tiek izmantoti kā satura pamatdati.</span><span class="sxs-lookup"><span data-stu-id="a1144-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="a1144-182">Elements</span><span class="sxs-lookup"><span data-stu-id="a1144-182">Entity</span></span>        | <span data-ttu-id="a1144-183">Galvenie apkopošanas mērījumi</span><span class="sxs-lookup"><span data-stu-id="a1144-183">Key aggregate measurements</span></span> | <span data-ttu-id="a1144-184">Datu avots</span><span class="sxs-lookup"><span data-stu-id="a1144-184">Data source</span></span>                                 | <span data-ttu-id="a1144-185">Lauks</span><span class="sxs-lookup"><span data-stu-id="a1144-185">Field</span></span>              | <span data-ttu-id="a1144-186">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a1144-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="a1144-187">Rēķina rindas</span><span class="sxs-lookup"><span data-stu-id="a1144-187">Invoice lines</span></span> | <span data-ttu-id="a1144-188">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="a1144-188">Purchase</span></span>                   | <span data-ttu-id="a1144-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="a1144-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="a1144-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="a1144-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="a1144-191">Summa uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="a1144-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="a1144-192">Tālāk esošajā tabulā ir norādīti galvenie satura mērījumi, kas tiek aprēķināti no elementa Rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="a1144-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="a1144-193">Mērs</span><span class="sxs-lookup"><span data-stu-id="a1144-193">Measure</span></span>               | <span data-ttu-id="a1144-194">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="a1144-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1144-195">Pašreizējā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="a1144-195">Purchase current year</span></span> | <span data-ttu-id="a1144-196">Pašreizējā gada pirkumi = SUM('Rēģina rindas'\[Pirkšana\])</span><span class="sxs-lookup"><span data-stu-id="a1144-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="a1144-197">Pagājušā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="a1144-197">Purchase last year</span></span>    | <span data-ttu-id="a1144-198">Pagājušā gada pirkumi = CALCULATE(SUM('Rēķina rindas'\[Pirkšana\]), SAMEPERIODLASTYEAR(Datumi\[Datums\]))</span><span class="sxs-lookup"><span data-stu-id="a1144-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="a1144-199">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="a1144-199">YOY purchase growth</span></span>   | <span data-ttu-id="a1144-200">Pirkumu palielinājums pa gadiem = \[Pašreizējā gada pirkumi\] – \[Pagājušā gada pirkumi\]</span><span class="sxs-lookup"><span data-stu-id="a1144-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="a1144-201">Tālāk norādītās galvenās dimensijas saturam tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.</span><span class="sxs-lookup"><span data-stu-id="a1144-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="a1144-202">Elements</span><span class="sxs-lookup"><span data-stu-id="a1144-202">Entity</span></span>                 | <span data-ttu-id="a1144-203">Atribūtu piemēri</span><span class="sxs-lookup"><span data-stu-id="a1144-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="a1144-204">Kreditori</span><span class="sxs-lookup"><span data-stu-id="a1144-204">Vendors</span></span>                | <span data-ttu-id="a1144-205">Kreditoru grupas, Kreditora valsts vai reģions, Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="a1144-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="a1144-206">Preces</span><span class="sxs-lookup"><span data-stu-id="a1144-206">Products</span></span>               | <span data-ttu-id="a1144-207">Preces numurs, Preces nosaukums, Krājumu grupas nosaukums</span><span class="sxs-lookup"><span data-stu-id="a1144-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="a1144-208">Sagādes kategorijas</span><span class="sxs-lookup"><span data-stu-id="a1144-208">Procurement categories</span></span> | <span data-ttu-id="a1144-209">Sagādes kategorija, Sagādes kategoriju nosaukumi</span><span class="sxs-lookup"><span data-stu-id="a1144-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="a1144-210">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="a1144-210">Legal entities</span></span>         | <span data-ttu-id="a1144-211">Juridiskās personas nosaukums</span><span class="sxs-lookup"><span data-stu-id="a1144-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="a1144-212">Datumi</span><span class="sxs-lookup"><span data-stu-id="a1144-212">Dates</span></span>                  | <span data-ttu-id="a1144-213">Datumi, Gada nobīde</span><span class="sxs-lookup"><span data-stu-id="a1144-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="a1144-214">Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu.</span><span class="sxs-lookup"><span data-stu-id="a1144-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="a1144-215">Taču varat mainīt datumu filtru pārskata filtru sadaļā.</span><span class="sxs-lookup"><span data-stu-id="a1144-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="a1144-216">Varat mainīt arī uzņēmuma filtru.</span><span class="sxs-lookup"><span data-stu-id="a1144-216">You can also change the company filter.</span></span>
