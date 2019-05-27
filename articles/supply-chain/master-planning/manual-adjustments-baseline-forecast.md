---
title: Manuāla bāzlīnijas prognozes korekciju veikšana
description: Šajā tēmā ir paskaidrots, kā var manuāli veikt bāzlīnijas prognozes korekcijas un skatīt detalizētu informāciju par prognozi.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7c7d1fcaaeef7a01b43886e4d69458dbd942439
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556879"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="a841b-103">Manuāla bāzlīnijas prognozes korekciju veikšana</span><span class="sxs-lookup"><span data-stu-id="a841b-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a841b-104">Šajā tēmā ir paskaidrots, kā var manuāli veikt bāzlīnijas prognozes korekcijas un skatīt detalizētu informāciju par prognozi.</span><span class="sxs-lookup"><span data-stu-id="a841b-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="a841b-105">Pirms manuālu korekciju veikšanas ir jāizprot daži dažādu lapu principi.</span><span class="sxs-lookup"><span data-stu-id="a841b-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="a841b-106">Lapas Koriģēta pieprasījuma apjoma prognoze režģis</span><span class="sxs-lookup"><span data-stu-id="a841b-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="a841b-107">Lapā **Koriģēta pieprasījuma apjoma prognoze** ir iekļauts režģis, kam ir tālāk norādītā struktūra.</span><span class="sxs-lookup"><span data-stu-id="a841b-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="a841b-108">Pirmajā kolonnā ir redzami krājumi, krājumu sadalījuma principi, uzņēmumi un citi elementi, par kuriem ir ģenerēta prognoze.</span><span class="sxs-lookup"><span data-stu-id="a841b-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="a841b-109">Lapas apakšvirsraksts norāda pašreizējo prognozes dimensiju, kas redzamas režģī, aprakstu.</span><span class="sxs-lookup"><span data-stu-id="a841b-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="a841b-110">Piemēram, ja lapas apakšvirsraksts ir **Uzņēmums/Vieta/Krājumu sadalījuma princips** un kāda no rindu galvenēm režģī ir **USMF/1/\_Alloc**, šajā rindā ir redzama prognoze, kas attiecas uz uzņēmumu USMF, vietu Nr. 1 un krājumu sadalījuma principu **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="a841b-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="a841b-111">Nākamās kolonnas attiecas uz prognožu intervāliem, kuriem prognoze ir ģenerēta.</span><span class="sxs-lookup"><span data-stu-id="a841b-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="a841b-112">Katras kolonnas galvene ir pirmais prognozes intervāla datums, kas ir redzams kolonnā.</span><span class="sxs-lookup"><span data-stu-id="a841b-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="a841b-113">Vērtības šūnās norāda viena krājuma, krājumu sadalījuma principa un citu šī konkrētā prognozes intervāla elementu prognozi.</span><span class="sxs-lookup"><span data-stu-id="a841b-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="a841b-114">Prognozes apkopošana un apkopojuma sadalīšana</span><span class="sxs-lookup"><span data-stu-id="a841b-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="a841b-115">Lapas apakšvirsraksts norāda prognozes apkopojuma līmenī.</span><span class="sxs-lookup"><span data-stu-id="a841b-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="a841b-116">Piemēram, ja lapas apakšvirsraksts ir **Uzņēmums / Vieta / Sadalījuma princips / Krājuma kods / Krāsa / Izmērs / Konfigurācija / Stils**, nav veikta prognozes apkopošana, un prognoze tiek parādīta krājuma un tā dimensiju līmenī.</span><span class="sxs-lookup"><span data-stu-id="a841b-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="a841b-117">Lai mainītu apkopošanas iestatījumu, izmantojiet lapu **Mainīt prognozes dimensijas**, kuru var atvērt lietojumprogrammas izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="a841b-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="a841b-118">Lai mainītu prognozi, noklikšķiniet uz jebkuras pieejamās šūnas un ierakstiet koriģētās prognozes vērtību.</span><span class="sxs-lookup"><span data-stu-id="a841b-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="a841b-119">Rediģētā šūna nekavējoties tiek parādīta treknrakstā, norādot, ka tajā redzamā prognoze nav prognoze, kas ir izveidota, izmantojot pieprasījuma prognozēšanas pakalpojumu, bet ir manuāli koriģēta.</span><span class="sxs-lookup"><span data-stu-id="a841b-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="a841b-120">Ja apkopojums tiek mainīts, lai lapā parādītu vairāk apkopotos datus, var izmantot lapu **Pieprasījuma apjoma prognozes rindas**, lai skatītu atsevišķas prognozes rindas, kuras veido apkopoto prognozi.</span><span class="sxs-lookup"><span data-stu-id="a841b-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="a841b-121">Piemēram, prognoze ir ģenerēta krājuma līmenī, bet ir zināms, ka reklamēšanas vai citu līdzīgu notikumu dēļ šī krājuma pieprasījums palielinās visās vietās.</span><span class="sxs-lookup"><span data-stu-id="a841b-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="a841b-122">Šajā gadījumā var iestatīt apkopošanu dimensijām **Uzņēmums / Krājuma sadalījuma parametrs / Krājums** lapā **Mainīt prognozes dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="a841b-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="a841b-123">Var koriģēt vispārējo visās vietās pieejamo krājumu prognozi režģī **Koriģētā pieprasījuma apjoma prognoze**.</span><span class="sxs-lookup"><span data-stu-id="a841b-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="a841b-124">Lai redzētu veikto izmaiņu ietekmi visās vietās, atveriet lapu **Pieprasījuma apjoma prognozes rindas**.</span><span class="sxs-lookup"><span data-stu-id="a841b-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="a841b-125">Šajā lapā var redzēt vienu rindu katras vietas krājumam, koriģētās prognozes daudzumu un sākotnēji prognozēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a841b-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="a841b-126">Ja apkopotā līmenī tiek veikta prognozētā daudzuma korekcija, sistēmā tiek izmantots svērtais sadalījums, lai nodotu izmaiņas uz rindām, kas veido apkopojumu.</span><span class="sxs-lookup"><span data-stu-id="a841b-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="a841b-127">Korekcijas var veikt arī manuāli lapā **Pieprasījuma apjoma prognozes rindas**, mainot vai nu vienuma **Kopējais daudzums** vērtību, vai vienuma **Daudzums** šūnas apkopošanas noņemšanas režģī.</span><span class="sxs-lookup"><span data-stu-id="a841b-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="a841b-128">Detalizētu prognozes datu skatīšana</span><span class="sxs-lookup"><span data-stu-id="a841b-128">Viewing details of the forecast</span></span>
<span data-ttu-id="a841b-129">Lai skatītu sīkāku informāciju par prognozi, var atvērt lapu **Detalizēti pieprasījuma apjoma prognozes dati**.</span><span class="sxs-lookup"><span data-stu-id="a841b-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="a841b-130">Lapā **Detalizēti pieprasījuma apjoma prognozes dati** grafiskā un tabulas formātā tiek parādīta tālāk norādītā informācija.</span><span class="sxs-lookup"><span data-stu-id="a841b-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="a841b-131">Vēsturiskais pieprasījums, kas ir prognozes datu pamatā.</span><span class="sxs-lookup"><span data-stu-id="a841b-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="a841b-132">Pašreizējā prognoze, kas tiek izmantota vispārējā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="a841b-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="a841b-133">Jaunas pieprasījumu apjoma prognozes vērtības un summas, kurām tās ir manuāli koriģētas.</span><span class="sxs-lookup"><span data-stu-id="a841b-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="a841b-134">Prognozēto vērtību ticamības intervāls.</span><span class="sxs-lookup"><span data-stu-id="a841b-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="a841b-135">Prognozes ģenerēšanai izmantotais prognozes modelis.</span><span class="sxs-lookup"><span data-stu-id="a841b-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="a841b-136">Ja tiek skatīti apkopotie dati, ir redzams visu to metožu saraksts, kuras tika izmantotas visām apkopotajām laika sērijām.</span><span class="sxs-lookup"><span data-stu-id="a841b-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="a841b-137">Iekšējā modeļa precizitāte (MAPE).</span><span class="sxs-lookup"><span data-stu-id="a841b-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="a841b-138">Lai iegūtu sīkāku informāciju par prognozes precizitāti, skatiet sadaļu [Prognozes precizitātes pārraudzīšana](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="a841b-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="a841b-139">**Piezīmes.**</span><span class="sxs-lookup"><span data-stu-id="a841b-139">**Notes:**</span></span>

-   <span data-ttu-id="a841b-140">Ticamības intervāls, kas ir redzams lapas sadaļā **Prognoze**, norāda starpību starp ticamības intervāla augšējo robežu un ticamības intervāla apakšējā robežu.</span><span class="sxs-lookup"><span data-stu-id="a841b-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="a841b-141">Lai redzētu augšējās un apakšējās robežas vērtības, novietojiet kursoru virs diagrammas sadaļā **Grafisks vēsturiskā pieprasījuma un prognozes attēlojums**.</span><span class="sxs-lookup"><span data-stu-id="a841b-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="a841b-142">Ja lietojat Microsoft Azure algoritmiskās mācīšanās pakalpojumu Finance and Operations pieprasījuma prognozēšana, varat norādīt ģenerētās prognozes ticamības līmeni procentos.</span><span class="sxs-lookup"><span data-stu-id="a841b-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="a841b-143">Ticamības intervālu veido vairākas vērtības, kas darbojas kā labs pieprasījuma apjoma prognozes aprēķins.</span><span class="sxs-lookup"><span data-stu-id="a841b-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="a841b-144">Ticamības līmenis 95 % norāda, ka pastāv 5 % risks, ka pieprasījuma apjoma prognoze nav ticamības intervāla diapazonā.</span><span class="sxs-lookup"><span data-stu-id="a841b-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="a841b-145">Lapā **Detalizēti pieprasījuma apjoma prognozes dati** var veikt arī manuālas korekcijas, mainot vērtības rindā **Prognoze** sadaļā **Prognoze**.</span><span class="sxs-lookup"><span data-stu-id="a841b-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a841b-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a841b-146">Additional resources</span></span>
--------

[<span data-ttu-id="a841b-147">Prognozes precizitātes pārraudzība</span><span class="sxs-lookup"><span data-stu-id="a841b-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="a841b-148">Statistiskās bāzlīnijas prognozes ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="a841b-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



