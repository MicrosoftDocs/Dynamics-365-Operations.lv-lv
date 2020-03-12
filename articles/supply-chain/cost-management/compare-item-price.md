---
title: Krājumu cenu uzglabāšanas salīdzināšanas pārskats
description: Uzziniet, kā ģenerēt krājumu cenu uzglabāšanas salīdzinājuma pārskatu un pēc tam pārlūkot un/vai eksportēt rezultātu.
author: AndersGirke
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 80e376db3616af27d94ee55480cd2f56441db93b
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2020
ms.locfileid: "3072119"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="39707-103">Krājumu cenu uzglabāšanas salīdzināšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="39707-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39707-104">Šajā tēmā skaidrots, kā palaist pārskatu **Krājumu cenas uzglabāšanas salīdzināšana** un padarīt rezultātu pieejamu digitāli vai nu kā interaktīvu lapu programmā Dynamics 365 Supply Chain Management, vai kā eksportētu dokumentu jebkurā no vairākiem formātiem.</span><span class="sxs-lookup"><span data-stu-id="39707-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="39707-105">Skatot pārskatu pārlūkā, kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no konfigurētā izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="39707-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="39707-106">Varat sakārtot rezultātus, filtrēt tos, detalizēt datus un veikts citas darbības.</span><span class="sxs-lookup"><span data-stu-id="39707-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="39707-107">Pārskata rezultāti tiek uzglabāti datu elementā **Preču cenu salīdzināšana**, kas ļauj filtrēt un eksportēt rezultātus tādos formātos kā, piemēram, CSV vai Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="39707-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="39707-108">Pārskats **Krājumu uzglabāšanas cenu salīdzināšana** noder gadījumos, ja izlaidē ir daudz rindu.</span><span class="sxs-lookup"><span data-stu-id="39707-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="39707-109">Piemēram, izlaide saturēs daudzas rindas, ja jums ir vairāk nekā 40 000 krājumu, kam ir gaidoša krājuma cena izmaksu aprēķināšanas versijā.</span><span class="sxs-lookup"><span data-stu-id="39707-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="39707-110">Krājumu cenu uzglabāšanas salīdzināšanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="39707-110">Enable compare item prices storage</span></span>

<span data-ttu-id="39707-111">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo sistēmā.</span><span class="sxs-lookup"><span data-stu-id="39707-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="39707-112">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="39707-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="39707-113">Šeit līdzeklis tiek norādīts kā:</span><span class="sxs-lookup"><span data-stu-id="39707-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="39707-114">**Modulis** - Izmaksu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="39707-114">**Module** - Cost management</span></span>
- <span data-ttu-id="39707-115">**Līdzekļa nosaukums** — Krājumu cenu uzglabāšanas salīdzināšana</span><span class="sxs-lookup"><span data-stu-id="39707-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="39707-116">Ģenerēt pārskatu Krājumu cenu uzglabāšanas salīdzināšana</span><span class="sxs-lookup"><span data-stu-id="39707-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="39707-117">Veiciet šīs darbības, lai ģenerētu un uzglabātu pārskatu **Krājumu cenu glabāšanas salīdzināšana**:</span><span class="sxs-lookup"><span data-stu-id="39707-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="39707-118">Dodieties uz **Izmaksu pārvaldība > Vaicājumi un atskaites > Iepriekš noteikti izmaksu pārskati > Krājumu cenu glabāšanas salīdzināšana**.</span><span class="sxs-lookup"><span data-stu-id="39707-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="39707-119">Atlasiet **Jauns**, lai atvērtu rūti **Salīdzināt krājumu cenas**.</span><span class="sxs-lookup"><span data-stu-id="39707-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="39707-120">Iestatiet šādas opcijas, lai definētu, kuras cenas salīdzināt savā pārskatā:</span><span class="sxs-lookup"><span data-stu-id="39707-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="39707-121">Kopsavilkuma cilnē **Parametri** piešķiriet pārskatam unikālu **Nosaukumu** un lietojiet laukus sadaļās **Gaidošās salīdzināmās cenas** un **Salīdzinājumam izmantotās cenas**, lai noteiktu, kuras cenas un datumus salīdzināt.</span><span class="sxs-lookup"><span data-stu-id="39707-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="39707-122">Kopsavilkuma cilnē **Iekļaujamie ieraksti** iestatiet filtrus un ierobežojumus, lai noteiktu, kurus datus iekļaut pārskatā.</span><span class="sxs-lookup"><span data-stu-id="39707-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="39707-123">Kopsavilkuma cilnē **Palaist fonā** iestatiet kā, kad un cik bieži vēlaties ģenerēt pārskatu.</span><span class="sxs-lookup"><span data-stu-id="39707-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="39707-124">Šis pārskats vienmēr tiek izpildīts kā daļa no pakešuzdevuma.</span><span class="sxs-lookup"><span data-stu-id="39707-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="39707-125">Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu rūti.</span><span class="sxs-lookup"><span data-stu-id="39707-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="39707-126">Kad pakešuzdevums ir pabeigts, tas tiks uzskaitīts lapā **Krājumu cenu glabāšanas salīdzināšana**.</span><span class="sxs-lookup"><span data-stu-id="39707-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="39707-127">Lai skatītu jaunāko pārskatu, lapu var nākties atsvaidzināt.</span><span class="sxs-lookup"><span data-stu-id="39707-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="39707-128">Krājumu cenu uzglabāšanas salīdzināšanas pārskata izpēte</span><span class="sxs-lookup"><span data-stu-id="39707-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="39707-129">Pēc pārskata izveidošanas to var apskatīt un izpētīt jebkurā laikā šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="39707-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="39707-130">Dodieties uz **Izmaksu pārvaldība > Vaicājumi un atskaites > Iepriekš noteikti izmaksu pārskati > Krājumu cenu glabāšanas salīdzināšana**.</span><span class="sxs-lookup"><span data-stu-id="39707-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="39707-131">No saraksta atlasiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="39707-131">Select a report from the list.</span></span>

1. <span data-ttu-id="39707-132">Veiciet vienu no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="39707-132">Do one of the following:</span></span>

    - <span data-ttu-id="39707-133">Atlasiet **Apskats**, lai apskatu par sava pārskata rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="39707-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="39707-134">Atlasīt **Skatīt informāciju**, lai iegūtu detalizētāku pārskata skatu</span><span class="sxs-lookup"><span data-stu-id="39707-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="39707-135">Pēc tam, kad ir atvērts atlasītais skats, varat veikt šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="39707-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="39707-136">Atlasiet gandrīz jebkuru kolonnas virsrakstu, lai kārtotu vai filtrētu tabulu pēc vērtībām šajā kolonnā, tāpat kā vairumam standarta veidlapu pakalpojumā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="39707-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="39707-137">Ņemiet vērā, ka nevarat filtrēt kolonnu **Neto izmaiņu cenas %**, jo tas ir aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="39707-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="39707-138">Atlasiet **Parādāmās dimensijas**, lai atvērtu rūti, kurā var izvēlēties, kuru dimensijas kolonnu iekļaut veidlapā.</span><span class="sxs-lookup"><span data-stu-id="39707-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="39707-139">Iestatiet **Saglabāt iestatījumus** uz **Jā**, ja vēlaties saglabāt šos iestatījumus, lai tie tiktu saglabāti nākamreiz, kad atvērsit pārskatu.</span><span class="sxs-lookup"><span data-stu-id="39707-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="39707-140">Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu.</span><span class="sxs-lookup"><span data-stu-id="39707-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="39707-141">Atlasiet jebkuru rindu veidlapā un pēc tam atlasiet **Skatīt detalizētu informāciju**, lai skatītu vairāk informācijas par atlasīto krājumu.</span><span class="sxs-lookup"><span data-stu-id="39707-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="39707-142">No turienes varēsit skatīt datus detalizētāk.</span><span class="sxs-lookup"><span data-stu-id="39707-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="39707-143">Atlasiet jebkuru rindu veidlapā un pēc tam atlasiet **Skatīt salīdzinājuma diagrammu**, lai redzētu savu rezultātu interaktīvo grafisku attēlojumu, rezultātiem saistoties ar jūsu atlasīto krājumu.</span><span class="sxs-lookup"><span data-stu-id="39707-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="39707-144">Šos rezultātus var izpētīt, atlasot dažādus grafiskos elementus diagrammā un diagrammas apzīmējumos.</span><span class="sxs-lookup"><span data-stu-id="39707-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="39707-145">Atlasiet jebkuru rindu veidlapā un pēc tam atlasiet **Skatīt aprēķina detalizētu informāciju**, lai skatītu vairāk informācijas par aprēķiniem, kas saistīti ar atlasīto krājumu.</span><span class="sxs-lookup"><span data-stu-id="39707-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="39707-146">No turienes varēsit skatīt datus detalizētāk.</span><span class="sxs-lookup"><span data-stu-id="39707-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="39707-147">Krājumu cenu uzglabāšanas salīdzināšanas pārskata eksportēšana</span><span class="sxs-lookup"><span data-stu-id="39707-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="39707-148">Katrs pārskats, ko izveidojat, tiek saglabāts datu elementā **Salīdzināt krājuma cenas**.</span><span class="sxs-lookup"><span data-stu-id="39707-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="39707-149">Varat izmantot Supply Chain Management standarta datu pārvaldības līdzekļus, lai eksportētu datus no šīs entītijas uz jebkuru atbalstīto datu formātu, tostarp CSV vai Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="39707-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="39707-150">Tālāk ir sniegts piemērs, kā eksportēt **Krājuma cenu glabāšanas salīdzināšanas** pārskatu:</span><span class="sxs-lookup"><span data-stu-id="39707-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="39707-151">Dodieties uz **Sistēmas administrēšana > Darbvietas > Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="39707-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="39707-152">Atlasiet pogu **Eksportēt** sadaļā **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="39707-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="39707-153">Tiek atvērta lapa **Eksports**, kuru izmantosit, lai iestatītu eksportēšanas darbu.</span><span class="sxs-lookup"><span data-stu-id="39707-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="39707-154">Sāciet, piešķirot darbam **Grupas nosaukumu**.</span><span class="sxs-lookup"><span data-stu-id="39707-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="39707-155">Sadaļā **Atlasītie elementi** atlasiet **Pievienot elementu**, lai atvērtu dialoglodziņu, kurā var iestatīt šādas opcijas:</span><span class="sxs-lookup"><span data-stu-id="39707-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="39707-156">**Elementa nosaukums** — atlasiet **Salīdzināt krājumu cenas**.</span><span class="sxs-lookup"><span data-stu-id="39707-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="39707-157">**Mērķa datu formāts** — izvēlieties formātu, uz kuru vēlaties eksportēt.</span><span class="sxs-lookup"><span data-stu-id="39707-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="39707-158">Atlasiet **Pievienot**, lai pievienotu jaunu rindu, un pēc tam atlasiet **Aizvērt**, lai dialoglodziņu aizvērtu.</span><span class="sxs-lookup"><span data-stu-id="39707-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="39707-159">Parasti katru reizi tiks eksportēts viens pārskats.</span><span class="sxs-lookup"><span data-stu-id="39707-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="39707-160">Lai to izdarītu, iestatiet **Filtru** rindai, kuru tikko pievienojāt rūtij **Pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="39707-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="39707-161">Tas ļaus jums definēt, kurus pārskatu no elementa **Krājumu cenu salīdzināšana** vēlaties iekļaut savā eksportā.</span><span class="sxs-lookup"><span data-stu-id="39707-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="39707-162">Iestatiet šādas filtra opcijas, lai eksportētu vienu pārskatu:</span><span class="sxs-lookup"><span data-stu-id="39707-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="39707-163">Cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="39707-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="39707-164">Iestatiet **Tabula** uz **Salīdzināt krājumu cenas**.</span><span class="sxs-lookup"><span data-stu-id="39707-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="39707-165">Iestatiet **Atveidotā tabula** uz **Salīdzināt krājumu cenas**.</span><span class="sxs-lookup"><span data-stu-id="39707-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="39707-166">Iestatiet **Lauks** uz lauku, pēc kura vēlaties filtrēt.</span><span class="sxs-lookup"><span data-stu-id="39707-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="39707-167">Parasti jūs izmantosit **Izpildes nosaukums** vai **Izpildes laiks**.</span><span class="sxs-lookup"><span data-stu-id="39707-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="39707-168">Iestatiet **Kritērijus** vērtībai atlasītajā laukā, ko vēlaties meklēt (vai nu pārskata nosaukums, vai pārskata izveides laiks).</span><span class="sxs-lookup"><span data-stu-id="39707-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="39707-169">Ja nepieciešams, pievienojiet tabulai **Diapazons** papildu rindas, līdz esat unikāli identificējis pārskatu, kuru meklējat.</span><span class="sxs-lookup"><span data-stu-id="39707-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="39707-170">Atlasiet **Labi**, lai saglabātu iestatījumus un aizvērtu.</span><span class="sxs-lookup"><span data-stu-id="39707-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="39707-171">Atlasiet **Saglabāt**, lai saglabātu eksporta iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="39707-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="39707-172">Atveriet cilni **Eksporta opcijas** un atlasiet **Eksportēt tūlīt**, lai ģenerētu eksporta failu.</span><span class="sxs-lookup"><span data-stu-id="39707-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="39707-173">Tiek atvērta lapa **Izpildes kopsavilkums**, kurā ir redzams eksportētā darba statuss un eksportēto elementu saraksts.</span><span class="sxs-lookup"><span data-stu-id="39707-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="39707-174">Atlasiet elementu **Krājuma cenu salīdzināšana**, kas ir uzskaitīts apgabalā **Elementa apstrādes statuss**, un pēc tam atlasiet **Lejupielādēt failu**, lai no šī elementa lejupielādētu eksportētos datus.</span><span class="sxs-lookup"><span data-stu-id="39707-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="39707-175">Papildinformāciju par to, kā izmantot datu pārvaldību, lai eksportētu datus, skatiet šeit: [Datu importēšanas un eksportēšanas darbu apskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="39707-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
