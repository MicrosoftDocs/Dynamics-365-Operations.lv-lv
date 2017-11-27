--- 
title: "Bāzlīnijas prognozes izveide"
description: "Ražošanas plānotājs var izveidot bāzlīnijas prognozes, izmantojot laika sērijas prognozes modeļus vai kopējot vēsturisko pieprasījumu."
author: YuyuScheller
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: 6a712077fed4a94ae6ae6ce7ea2cfba8848e5fa5
ms.contentlocale: lv-lv
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="d92e9-103">Bāzlīnijas prognozes izveide</span><span class="sxs-lookup"><span data-stu-id="d92e9-103">Create a baseline forecast</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d92e9-104">Ražošanas plānotājs var izveidot bāzlīnijas prognozes, izmantojot laika sērijas prognozes modeļus vai kopējot vēsturisko pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="d92e9-105">Šajā procedūrā ir parādīts, kā kopēt vēsturisko pieprasījumu, lai izveidotu bāzlīnijas prognozi visām precēm, izmantojot vienu krājumu sadalījuma principu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="d92e9-106">Krājumu sadalījuma principa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d92e9-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="d92e9-107">Pārejiet uz sadaļu Vispārējā plānošana > Iestatījumi > Starpuzņēmumu plānošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="d92e9-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="d92e9-108">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d92e9-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d92e9-109">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".</span><span class="sxs-lookup"><span data-stu-id="d92e9-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="d92e9-110">Pieprasījuma prognozēšana darbojas visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="d92e9-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="d92e9-111">Tāpēc nepieciešams iestatīt visus uzņēmumus, kuriem vēlaties ģenerēt prognozes vienā starpuzņēmumu plānošanas grupā.</span><span class="sxs-lookup"><span data-stu-id="d92e9-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="d92e9-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d92e9-113">Noklikšķiniet uz Krājumu sadalījuma principi.</span><span class="sxs-lookup"><span data-stu-id="d92e9-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="d92e9-114">Atlasiet visus krājumu sadalījuma principus, kuriem vēlaties izveidot prognozes.</span><span class="sxs-lookup"><span data-stu-id="d92e9-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="d92e9-115">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d92e9-116">Atlasiet D_Aloc krājumu sadalījuma principu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="d92e9-117">Noklikšķiniet uz >.</span><span class="sxs-lookup"><span data-stu-id="d92e9-117">Click >.</span></span>
7. <span data-ttu-id="d92e9-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-118">Close the page.</span></span>
8. <span data-ttu-id="d92e9-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="d92e9-120">Pieprasījuma prognozēšanas parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d92e9-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="d92e9-121">Pārejiet uz sadaļu Vispārējā plānošana > Iestatījumi > Pieprasījuma prognozēšana > Pieprasījuma prognozēšanas parametri.</span><span class="sxs-lookup"><span data-stu-id="d92e9-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="d92e9-122">Izvērsiet prognozes algoritma parametru sadaļu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="d92e9-123">Laukā Prognozes ģenerēšanas stratēģija atlasiet Kopēt vēsturiskā pieprasījuma vietā.</span><span class="sxs-lookup"><span data-stu-id="d92e9-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="d92e9-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d92e9-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="d92e9-125">Bāzlīnijas prognozes izveide</span><span class="sxs-lookup"><span data-stu-id="d92e9-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="d92e9-126">Pārejiet uz sadaļu Vispārējā plānošana > Prognozēšana > Pieprasījuma prognozēšana > Ģenerēt statistisko bāzlīnijas prognozi.</span><span class="sxs-lookup"><span data-stu-id="d92e9-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="d92e9-127">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="d92e9-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="d92e9-128">Ja jums ir pārdošanas pasūtījumi, sākot ar 2015. gada 1. janvāri, ievadiet šo datumu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="d92e9-129">Ja tā nav, ievadiet agrāko datumu no saviem pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d92e9-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="d92e9-130">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="d92e9-131">Ievadiet jaunāko savu pārdošanas pasūtījumu datumu, piemēram, “2015-03-31”.</span><span class="sxs-lookup"><span data-stu-id="d92e9-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="d92e9-132">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="d92e9-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="d92e9-133">Ievadiet “2015-04-01”.</span><span class="sxs-lookup"><span data-stu-id="d92e9-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="d92e9-134">Šis datums tiks automātiski aprēķināts, lai izmantotu par nākamā prognozēšanas intervāla sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="d92e9-135">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="d92e9-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="d92e9-136">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="d92e9-136">Click Filter.</span></span>
7. <span data-ttu-id="d92e9-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d92e9-138">Iezīmējiet rindu, kur lauka vērtība ir starpuzņēmumu plānošanas grupa.</span><span class="sxs-lookup"><span data-stu-id="d92e9-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="d92e9-139">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d92e9-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="d92e9-140">Ierakstiet starpuzņēmumu plānošanas grupu, piemēram, 10, kuru izmantojāt pirmajā uzdevumā.</span><span class="sxs-lookup"><span data-stu-id="d92e9-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="d92e9-141">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d92e9-142">Atlasiet rindu, kurā lauka vērtība ir krājumu sadalījuma princips.</span><span class="sxs-lookup"><span data-stu-id="d92e9-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="d92e9-143">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d92e9-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="d92e9-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d92e9-144">Click OK.</span></span>
12. <span data-ttu-id="d92e9-145">Izvērsiet sadaļu Papildu parametri.</span><span class="sxs-lookup"><span data-stu-id="d92e9-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="d92e9-146">Laukā Prognozes intervāls atlasiet "Mēnesis".</span><span class="sxs-lookup"><span data-stu-id="d92e9-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="d92e9-147">Laukā Prognozes periods ievadiet "3".</span><span class="sxs-lookup"><span data-stu-id="d92e9-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="d92e9-148">Laukā Periods bez izmaiņām ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="d92e9-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="d92e9-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d92e9-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="d92e9-150">Pieprasījuma prognozes vizualizēšana</span><span class="sxs-lookup"><span data-stu-id="d92e9-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="d92e9-151">Pārejiet uz sadaļu Vispārējā plānošana > Prognozēšana > Pieprasījuma prognozēšana > Pielāgotā pieprasījuma prognoze.</span><span class="sxs-lookup"><span data-stu-id="d92e9-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="d92e9-152">Apkoptā skatījuma tabulā atlasiet šūnu 1. rindas 2. kolonnā.</span><span class="sxs-lookup"><span data-stu-id="d92e9-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="d92e9-153">Šis ir otrais mēnesis, kuram esat izveidojis prognozi.</span><span class="sxs-lookup"><span data-stu-id="d92e9-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="d92e9-154">Iestatiet QtyCell vērtību "400".</span><span class="sxs-lookup"><span data-stu-id="d92e9-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="d92e9-155">Šūnā ievadiet citu numuru, nevis prognozēto, piemēram, 400.</span><span class="sxs-lookup"><span data-stu-id="d92e9-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="d92e9-156">Esat veicis manuālās prognozes korekcijas.</span><span class="sxs-lookup"><span data-stu-id="d92e9-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="d92e9-157">Ievērojiet grafisko norādi nākamajā darbībā.</span><span class="sxs-lookup"><span data-stu-id="d92e9-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="d92e9-158">Noklikšķiniet uz Detalizēta informācija par prognozes rindu.</span><span class="sxs-lookup"><span data-stu-id="d92e9-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="d92e9-159">Šajā lapā var apskatīt precizitātes, vēsturiskā pieprasījuma un prognozes vērtības.</span><span class="sxs-lookup"><span data-stu-id="d92e9-159">On this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="d92e9-160">Varat arī veikt prognožu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="d92e9-160">You can make changes to the forecast as well.</span></span>  


