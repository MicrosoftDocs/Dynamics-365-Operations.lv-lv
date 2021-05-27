---
title: Izmaksu un datuma kontrole
description: Šajā tēmā ir paskaidrota izmaksu un datuma kontrole programmā Asset Management.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c09dee94891fb78c22e8cf9f203cb7f5531bb968
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6016139"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="3947d-103">Izmaksu un datuma kontrole</span><span class="sxs-lookup"><span data-stu-id="3947d-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3947d-104">Programmā Asset Management varat aprēķināt faktisko līdzekļu kļūmju izmaksas, lai iegūtu pārskatu salīdzinājumā ar kļūmju, funkcionālo novietojumu un darba pasūtījumu budžetētajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="3947d-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="3947d-105">Faktiskās izmaksas ir balstītas uz publicētajiem darījumiem.</span><span class="sxs-lookup"><span data-stu-id="3947d-105">Actual costs are based on posted transactions.</span></span>

<span data-ttu-id="3947d-106">Varat veikt datuma aprēķinu, arī ja vēlaties salīdzināt plānoto sākuma datumu un beigu datumu ar faktisko sākuma un beigu datumu darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="3947d-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="3947d-107">Līdzekļu izmaksu kontrole, funkcionālie novietojumi un darba pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="3947d-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="3947d-108">Aprēķini, kas veikti līdzekļiem, funkcionālajam novietojumam un darba pasūtījumiem, ir gandrīz identiski.</span><span class="sxs-lookup"><span data-stu-id="3947d-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="3947d-109">Vienīgā atšķirība ir tā, ka līdzekļiem un funkcionālajam novietojumam aprēķinā var iekļaut arī pakārtotus līdzekļus un pakārtotas atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="3947d-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="3947d-110">Datums ir transakcijas datums, kad reģistrācija tika ierakstīta.</span><span class="sxs-lookup"><span data-stu-id="3947d-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="3947d-111">Klikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu izmaksu kontrole** vai **Funkcionālā novietojuma izmaksu kontrole**, vai **Aktīvu pārvaldība** > **Pieprasījumi** > **Darba pasūtījumi** > **Darba pasūtījumu izmaksu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="3947d-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="3947d-112">Dialog­ā **Līdzekļu izmaksu kontrole** / **Funkcionālā novietojuma izmaksu kontrole** / **Darba pasūtījuma izmaksu kontrole** atlasiet aprēķina laika diapazonu.</span><span class="sxs-lookup"><span data-stu-id="3947d-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="3947d-113">Ja vajadzīgs, izvēlieties finansiālo parametru kopu, ko iekļaut aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="3947d-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="3947d-114">Pārslēgšanas pogā **Izlaist nulli** atlasiet „Jā”, ja nevēlaties, lai rāda rezultātus, kas satur nulles izmaksas.</span><span class="sxs-lookup"><span data-stu-id="3947d-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="3947d-115">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties izmaksu kontroles rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="3947d-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="3947d-116">Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma hierarhija, visas izmaksu kontroles rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="3947d-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span>

    <span data-ttu-id="3947d-117">Ja laukā **Līmenis** ievadāt ciparu „„0””, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas izmaksu kontroles rindas visos funkcionālā novietojuma līmeņos, ar kuriem tās ir saistītas.</span><span class="sxs-lookup"><span data-stu-id="3947d-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="3947d-118">Pārslēgšanas pogā **Parādīt atvērto saistību izmaksas** atlasiet "Jā", ja vēlaties iekļaut aprēķinā to sleju.</span><span class="sxs-lookup"><span data-stu-id="3947d-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="3947d-119">Atlasiet “Jā” pārslēgšanas pogā **Ietvert pakārtotos līdzekļus**, lai parādītu izmaksas, kas saistītas ar pakārtotajiem līdzekļiem kā atsevišķas rindas.</span><span class="sxs-lookup"><span data-stu-id="3947d-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="3947d-120">Ja vēlaties ierobežot meklēšanu, varat atlasīt konkrētus līdzekļus/funkcionālos novietojumus/darba pasūtījumus, lai iekļautu kopsavilkuma cilnē **Ieraksti, kas jāiekļauj**.</span><span class="sxs-lookup"><span data-stu-id="3947d-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="3947d-121">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="3947d-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="3947d-122">Zemāk esošajā attēlā ir parādīts **Līdzekļu izmaksu kontroles** dialogs.</span><span class="sxs-lookup"><span data-stu-id="3947d-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Līdzekļu izmaksu kontroles dialoglodziņš](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="3947d-124">Lapā **Līdzekļu izmaksu kontrole** noklikšķiniet uz attiecīgās pogas **Grupēt pēc..**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="3947d-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="3947d-125">Atlasītās **Grupēt pēc** pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="3947d-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="3947d-126">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="3947d-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example-of-calculation-results-in-asset-cost-control"></a><span data-ttu-id="3947d-127">Aprēķina rezultāta piemērs līdzekļu izmaksu kontrolē</span><span class="sxs-lookup"><span data-stu-id="3947d-127">Example of calculation results in asset cost control</span></span>

<span data-ttu-id="3947d-128">Tālāk esošajā ekrānuzņēmumā ir parādīts līdzekļu aprēķina rezultātu piemērs **Līdzekļu izmaksu kontrolē**.</span><span class="sxs-lookup"><span data-stu-id="3947d-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="3947d-129">Laukā **Sākotnējais budžets** rāda budžetētās izmaksas no darba pasūtījuma prognozes.</span><span class="sxs-lookup"><span data-stu-id="3947d-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="3947d-130">**Saistību izmaksu** lauks rāda kopējās izmaksas, kuras juridiskā persona uzņēmusies maksāt.</span><span class="sxs-lookup"><span data-stu-id="3947d-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="3947d-131">Laukā **Atvērtās saistību izmaksa** redzamas saistība par maksājumiem par vienumiem, stundām un pakalpojumiem, ko esat pasūtījis vai saņēmis, bet vēl neesat apmaksājis.</span><span class="sxs-lookup"><span data-stu-id="3947d-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="3947d-132">Kad ir grāmatotas visas patēriņa reģistrācijas, saistītās izmaksas tiek iekļautas laukā **Faktiskās izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="3947d-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Piemēram, aprēķina rezultāts ir Līdzekļu izmaksu kontrolē](media/02-controlling-and-reporting.png)

<span data-ttu-id="3947d-134">Cits veids, kā veikt izmaksu aprēķinu, ir atzīmēt vairākus līdzekļus sadaļā **Visi līdzekļi** vai **Aktīvie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="3947d-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="3947d-135">Tad klikšķiniet uz pogas **Izmaksu kontrole** cilnē **Vispārēji**. Dialogā **Līdzekļu izmaksu kontrole** atlasītie līdzekļi tiek automātiski ievietoti laukā **Līdzekļi** kopsavilkuma cilnē **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="3947d-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="3947d-136">Klikšķiniet uz **Labi**, tiks parādīts atlasīto līdzekļu izmaksu aprēķins.</span><span class="sxs-lookup"><span data-stu-id="3947d-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="3947d-137">To pašu procedūru var veikt funkcionālajiem novietojumiem sadaļās **Visi funkcionālie novietojumi** vai **Aktīvie funkcionālie novietojumi** un darba pasūtījumiem sadaļās **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3947d-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="3947d-138">Darba pasūtījuma datuma kontrole</span><span class="sxs-lookup"><span data-stu-id="3947d-138">Work order date control</span></span>

<span data-ttu-id="3947d-139">Izmantojiet šo lapu, lai redzētu pārskatu par plānoto sākuma datumu un beigu datumu, salīdzinot ar faktisko sākuma un beigu datumu darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="3947d-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="3947d-140">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Darba pasūtījumi** > **Darba pasūtījumu datuma kontrole**.</span><span class="sxs-lookup"><span data-stu-id="3947d-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="3947d-141">Noklikšķiniet uz **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="3947d-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="3947d-142">Laukā **Funkcionālais novietojums** atlasiet funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="3947d-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="3947d-143">Ievadiet diapazonu, kuram vēlaties veikt aprēķinu, laukos **Datums no** un **Datums līdz**.</span><span class="sxs-lookup"><span data-stu-id="3947d-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="3947d-144">Tiks iekļauti visi darba pasūtījumi ar paredzamo sākuma datumu diapazonā.</span><span class="sxs-lookup"><span data-stu-id="3947d-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="3947d-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3947d-145">Click **OK**.</span></span>

6. <span data-ttu-id="3947d-146">Noklikšķiniet uz pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="3947d-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="3947d-147">Atlasītās **Grupēt pēc** pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="3947d-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="3947d-148">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="3947d-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example-of-calculation-results-in-work-order-date-control"></a><span data-ttu-id="3947d-149">Aprēķina rezultāta piemērs darba pasūtījuma datuma kontrolē</span><span class="sxs-lookup"><span data-stu-id="3947d-149">Example of calculation results in work order date control</span></span>

<span data-ttu-id="3947d-150">Tālāk esošajā ekrānuzņēmumā ir parādīts līdzekļu aprēķina rezultātu piemērs **Darba pasūtījumu datumu kontrolē**.</span><span class="sxs-lookup"><span data-stu-id="3947d-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="3947d-151">Laukā **Vidējais sākuma kavējums** tiks parādīta starpība dienās starp darba pasūtījuma ieplānoto sākuma datumu un faktisko sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="3947d-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="3947d-152">Ja, piemēram, faktiskais sākuma datums bijis divas dienas pirms ieplānotā datuma, šajā laukā rādīs „-2”.</span><span class="sxs-lookup"><span data-stu-id="3947d-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="3947d-153">Laukā **Vidējais beigu kavējums** tiks parādīta starpība starp darba pasūtījuma ieplānoto beigu datumu un faktisko beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="3947d-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="3947d-154">Ja, piemēram, faktiskais beigu datums bijis trīs dienas pēc ieplānotā datuma, šajā laukā rādīs „3”.</span><span class="sxs-lookup"><span data-stu-id="3947d-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="3947d-155">Laukā **Gadījumi** parāda skaitli, cik bieži notikušas novirzes attiecībā uz plānoto un faktisko sākuma datumu un plānoto un faktisko darba pasūtījuma datumu.</span><span class="sxs-lookup"><span data-stu-id="3947d-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Piemēram, aprēķina rezultāts ir Darba pasūtījuma datuma kontrole](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]