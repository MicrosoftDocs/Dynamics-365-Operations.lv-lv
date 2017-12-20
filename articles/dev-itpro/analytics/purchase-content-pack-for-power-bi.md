---
title: "Power BI satura pakotne Pirkumu tēriņu analīze"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pirkumu tēriņu analīzē. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: FrankDahl
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: f38f82b4275599a6b958c495f32b72778b400024
ms.contentlocale: lv-lv
ms.lasthandoff: 12/01/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="5a5c0-104">Power BI satura pakotne Pirkumu tēriņu analīze</span><span class="sxs-lookup"><span data-stu-id="5a5c0-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5a5c0-105">Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura **pirkumu tēriņu analīzē**.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="5a5c0-106">Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="5a5c0-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="5a5c0-107">Overview</span></span>

<span data-ttu-id="5a5c0-108">**Pirkumu tēriņu analīzes** Power BI saturs tika veidots, lai iepirkumu nodaļas vadītājiem un vadītājiem, kuri ir atbildīgi par budžetu, palīdzētu sekot pirkuma tēriņiem.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="5a5c0-109">Vadītāji var analizēt pirkumu tēriņus šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="5a5c0-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="5a5c0-110">Līdzšinējā gada pirkumi (pēc kreditoru grupas, atsevišķa kreditora, sagādes kategorijas, atsevišķas preces un kreditora atrašanās vietas)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="5a5c0-111">Pirkumu izmaiņas pa gadiem (pēc kreditoru grupas un sagādes kategorijas)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="5a5c0-112">Saturam tiek izmantoti pirkumu transakciju dati, un tas nodrošina gan uzņēmuma līmeņa pirkumu rādītāju apkopošanas skatu, gan pirkumu tēriņu sadalījumu pēc kreditora vai preces.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="5a5c0-113">Pārskatos ir izceltas pirkumu tēriņu izmaiņas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="5a5c0-114">Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tēriņu tendencēm saistībā ar atsevišķiem kreditoriem un precēm.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="5a5c0-115">Turklāt diagrammas ataino pirkumu tēriņus dažādām sagādes kategorijām un kreditoru grupām.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="5a5c0-116">Tādēļ kategoriju un reģionālie vadītāji var izmantot šīs diagrammas, lai palīdzētu noteikt tēriņu darbību izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="5a5c0-117">Piekļūšana Power BI saturam</span><span class="sxs-lookup"><span data-stu-id="5a5c0-117">Accessing the Power BI content</span></span>
<span data-ttu-id="5a5c0-118">Power BI satura pakotne **Pirkšanas tēriņu analīze** tiek rādīta lapā **Pirkšanas un tēriņu rādītāju analīze** (**Sagāde un avoti** > **Pieprasījumi un pārskati** > **Pirkšanas rādītāju analīze** > **Pirkšanas un tēriņu rādītāju analīze**).</span><span class="sxs-lookup"><span data-stu-id="5a5c0-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="5a5c0-119">Power BI saturā iekļautā metrika</span><span class="sxs-lookup"><span data-stu-id="5a5c0-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="5a5c0-120">**Pirkumu tēriņu analīzes** Power BI satura pakotnē ir iekļauts pārskats, kas sastāv no rādītāju kopas.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="5a5c0-121">Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="5a5c0-122">Zemāk norādītajā tabulā ir sniegts pārskats par vizualizācijām.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a5c0-123">Pārskata lapa</span><span class="sxs-lookup"><span data-stu-id="5a5c0-123">Report page</span></span></th>
<th><span data-ttu-id="5a5c0-124">Diagrammas</span><span class="sxs-lookup"><span data-stu-id="5a5c0-124">Charts</span></span></th>
<th><span data-ttu-id="5a5c0-125">Elementi</span><span class="sxs-lookup"><span data-stu-id="5a5c0-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a5c0-126">Pirkumi pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="5a5c0-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="5a5c0-127">Pirmie 10 kreditori pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="5a5c0-128">Pirkumu kopsumma pēc kreditoru grupas/valsts/nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="5a5c0-129">Pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="5a5c0-130">Vidējie pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a5c0-131">Kopējā pirkšana</span><span class="sxs-lookup"><span data-stu-id="5a5c0-131">Total purchase</span></span></li>
<li><span data-ttu-id="5a5c0-132">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="5a5c0-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="5a5c0-133">Kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="5a5c0-133">Total # vendors</span></span></li>
<li><span data-ttu-id="5a5c0-134">Aktīvo kreditoru kopskaits</span><span class="sxs-lookup"><span data-stu-id="5a5c0-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a5c0-135">Pirkumi pēc preces</span><span class="sxs-lookup"><span data-stu-id="5a5c0-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="5a5c0-136">Pirkumi pēc sagādes kategorijas/preces nosaukuma (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="5a5c0-137">Pirkumu kopsumma pēc sagādes kategorijas/preces nosaukuma (sektoru diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="5a5c0-138">Pirmās 10 preces pēc pirkšanas (joslu grēdu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a5c0-139">Preču kopskaits</span><span class="sxs-lookup"><span data-stu-id="5a5c0-139">Total # of products</span></span></li>
<li><span data-ttu-id="5a5c0-140">Aktīvo preču kopskaits procentos no preču kopskaita</span><span class="sxs-lookup"><span data-stu-id="5a5c0-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="5a5c0-141">To preču skaits, kas veido 80% pirkumu</span><span class="sxs-lookup"><span data-stu-id="5a5c0-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a5c0-142">Pirkumi pēc perioda*</span><span class="sxs-lookup"><span data-stu-id="5a5c0-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="5a5c0-143">Pirkumi pēc mēneša/dienas (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="5a5c0-144">Apkopotā pirkumu novirze pa gadiem (ūdenskrituma diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="5a5c0-145">Pirkumu kopsummas palielinājums pa gadiem (stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="5a5c0-146">Sagādes izraksts (matrica)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a5c0-147">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="5a5c0-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="5a5c0-148">Pirkumu palielinājums (%)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a5c0-149">Pirkumi pēc kreditora atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="5a5c0-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="5a5c0-150">Pirkumi pēc pilsētas</span><span class="sxs-lookup"><span data-stu-id="5a5c0-150">Purchase by city</span></span></li>
<li><span data-ttu-id="5a5c0-151">Pirkumu palielinājums pa gadiem (%)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="5a5c0-152">Pirkumi pēc valsts</span><span class="sxs-lookup"><span data-stu-id="5a5c0-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a5c0-153">Pirkumu tēriņu analīze pēc laika</span><span class="sxs-lookup"><span data-stu-id="5a5c0-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="5a5c0-154">Pašreizējā gada pirkumi pēc mēneša/dienas (līniju diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="5a5c0-155">Pašreizējā un pagājušā gada pirkumi (līniju un stabiņu diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a5c0-156">Pirkumu tēriņu analīze pēc kreditora</span><span class="sxs-lookup"><span data-stu-id="5a5c0-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="5a5c0-157">Pirmo 10 kreditoru pirkumi procentos (%) no pirkumiem (piltuves diagramma)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="5a5c0-158">Pirmie 10 kreditori ar palielinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="5a5c0-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="5a5c0-159">Pirmie 10 kreditori ar samazinātiem tēriņiem pa gadiem</span><span class="sxs-lookup"><span data-stu-id="5a5c0-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5a5c0-160">\* Šī gada un pagājušā gada pirkumi un palielinājums pēc sagādes kategorijas</span><span class="sxs-lookup"><span data-stu-id="5a5c0-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="5a5c0-161">Power BI satura paplašināšana</span><span class="sxs-lookup"><span data-stu-id="5a5c0-161">Extending the Power BI content</span></span>
<span data-ttu-id="5a5c0-162">Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="5a5c0-163">Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="5a5c0-164">**Pirkumu tēriņu analīzes** Power BI saturs ir pieejams LCS koplietojamo līdzekļu bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="5a5c0-165">Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="5a5c0-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="5a5c0-166">Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).</span><span class="sxs-lookup"><span data-stu-id="5a5c0-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="5a5c0-167">Noteikti lejupielādējiet **pirkumu tēriņu analīzes** saturu, kas attiecas uz izmantoto Dynamics 365 versiju.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="5a5c0-168">Ja izmantojat Microsoft Dynamics 365 for Operations versiju 1611, šī Power BI satura izmantošanas priekšnosacījums ir KB 4011327.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="5a5c0-169">Ja esat pierakstījies LCS, tad KB varat piekļūt šeit: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="5a5c0-170">Datu modelis un elementi</span><span class="sxs-lookup"><span data-stu-id="5a5c0-170">Data model and entities</span></span>
<span data-ttu-id="5a5c0-171">**Pirkumu tēriņu analīzes** Power BI satura pārskatu lapu aizpildīšanai tiek izmantoti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="5a5c0-172">Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="5a5c0-173">Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="5a5c0-174">Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="5a5c0-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="5a5c0-175">Šajā saturā ietvertie apkopošanas mērījumi ir apakškopa tiem apkopošanas mērījumiem, kas ir pieejami pirkšanas kubā programmatūrā Microsoft Dynamics AX 2012 un Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="5a5c0-176">Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="5a5c0-177">Papildinformāciju skatiet emuāra ieraksta [Pārskats par Power BI integrāciju, izmantojot elementu krātuvi](power-bi-integration-entity-store.md) sadaļā par apkopošanas mērījumu izvietošanas elementu krātuvē procedūru.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="5a5c0-178">Tālāk norādītie galvenie apkopošanas mērījumi ir tieši pieejami no elementa Rēķina rindas, un tie tiek izmantoti kā satura pamatdati.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="5a5c0-179">Elements</span><span class="sxs-lookup"><span data-stu-id="5a5c0-179">Entity</span></span>        | <span data-ttu-id="5a5c0-180">Galvenie apkopošanas mērījumi</span><span class="sxs-lookup"><span data-stu-id="5a5c0-180">Key aggregate measurements</span></span> | <span data-ttu-id="5a5c0-181">Datu avots</span><span class="sxs-lookup"><span data-stu-id="5a5c0-181">Data source</span></span>                                 | <span data-ttu-id="5a5c0-182">Lauks</span><span class="sxs-lookup"><span data-stu-id="5a5c0-182">Field</span></span>              | <span data-ttu-id="5a5c0-183">Apraksts</span><span class="sxs-lookup"><span data-stu-id="5a5c0-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="5a5c0-184">Rēķina rindas</span><span class="sxs-lookup"><span data-stu-id="5a5c0-184">Invoice lines</span></span> | <span data-ttu-id="5a5c0-185">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="5a5c0-185">Purchase</span></span>                   | <span data-ttu-id="5a5c0-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="5a5c0-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="5a5c0-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="5a5c0-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="5a5c0-188">Summa uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="5a5c0-189">Tālāk esošajā tabulā ir norādīti galvenie satura mērījumi, kas tiek aprēķināti no elementa Rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="5a5c0-190">Mērs</span><span class="sxs-lookup"><span data-stu-id="5a5c0-190">Measure</span></span>               | <span data-ttu-id="5a5c0-191">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="5a5c0-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a5c0-192">Pašreizējā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="5a5c0-192">Purchase current year</span></span> | <span data-ttu-id="5a5c0-193">Pašreizējā gada pirkumi = SUM('Rēģina rindas'\[Pirkšana\])</span><span class="sxs-lookup"><span data-stu-id="5a5c0-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="5a5c0-194">Pagājušā gada pirkumi</span><span class="sxs-lookup"><span data-stu-id="5a5c0-194">Purchase last year</span></span>    | <span data-ttu-id="5a5c0-195">Pagājušā gada pirkumi = CALCULATE(SUM('Rēķina rindas'\[Pirkšana\]), SAMEPERIODLASTYEAR(Datumi\[Datums\]))</span><span class="sxs-lookup"><span data-stu-id="5a5c0-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="5a5c0-196">Pirkumu palielinājums pa gadiem</span><span class="sxs-lookup"><span data-stu-id="5a5c0-196">YOY purchase growth</span></span>   | <span data-ttu-id="5a5c0-197">Pirkumu palielinājums pa gadiem = \[Pašreizējā gada pirkumi\] – \[Pagājušā gada pirkumi\]</span><span class="sxs-lookup"><span data-stu-id="5a5c0-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="5a5c0-198">Tālāk norādītās galvenās dimensijas saturam tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="5a5c0-199">Elements</span><span class="sxs-lookup"><span data-stu-id="5a5c0-199">Entity</span></span>                 | <span data-ttu-id="5a5c0-200">Atribūtu piemēri</span><span class="sxs-lookup"><span data-stu-id="5a5c0-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="5a5c0-201">Kreditori</span><span class="sxs-lookup"><span data-stu-id="5a5c0-201">Vendors</span></span>                | <span data-ttu-id="5a5c0-202">Kreditoru grupas, Kreditora valsts vai reģions, Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="5a5c0-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="5a5c0-203">Preces</span><span class="sxs-lookup"><span data-stu-id="5a5c0-203">Products</span></span>               | <span data-ttu-id="5a5c0-204">Preces numurs, Preces nosaukums, Krājumu grupas nosaukums</span><span class="sxs-lookup"><span data-stu-id="5a5c0-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="5a5c0-205">Sagādes kategorijas</span><span class="sxs-lookup"><span data-stu-id="5a5c0-205">Procurement categories</span></span> | <span data-ttu-id="5a5c0-206">Sagādes kategorija, Sagādes kategoriju nosaukumi</span><span class="sxs-lookup"><span data-stu-id="5a5c0-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="5a5c0-207">Juridiskas personas</span><span class="sxs-lookup"><span data-stu-id="5a5c0-207">Legal entities</span></span>         | <span data-ttu-id="5a5c0-208">Juridiskās personas nosaukums</span><span class="sxs-lookup"><span data-stu-id="5a5c0-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="5a5c0-209">Datumi</span><span class="sxs-lookup"><span data-stu-id="5a5c0-209">Dates</span></span>                  | <span data-ttu-id="5a5c0-210">Datumi, Gada nobīde</span><span class="sxs-lookup"><span data-stu-id="5a5c0-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="5a5c0-211">Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="5a5c0-212">Taču varat mainīt datumu filtru pārskata filtru sadaļā.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="5a5c0-213">Varat mainīt arī uzņēmuma filtru.</span><span class="sxs-lookup"><span data-stu-id="5a5c0-213">You can also change the company filter.</span></span>

