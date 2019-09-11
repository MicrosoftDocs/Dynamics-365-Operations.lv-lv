---
title: Uzturēšanas prognozes
description: Šajā tēmā ir paskaidrotas uzturēšanas prognozes programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875780"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="bcf68-103">Uzturēšanas prognozes</span><span class="sxs-lookup"><span data-stu-id="bcf68-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="bcf68-104">Izveidojot darba pasūtījumu, jūs izveidojat darba pasūtījuma darbus ar saistītiem līdzekļiem un uzturēšanas darba tipiem.</span><span class="sxs-lookup"><span data-stu-id="bcf68-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="bcf68-105">Atlasot uzturēšanas darba tipu, kas satur uzturēšanas prognozes, prognozes tiek automātiski iekopētas darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="bcf68-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="bcf68-106">Iespējams, jūs varat pievienot vai dzēst prognozes rindas darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="bcf68-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="bcf68-107">Darba pasūtījuma dzīves cikla stāvokļa uzstādījums, saistītais projekta tips un posma noteikumi, kas attiecas uz projekta tipu, nosaka, vai jūs varat pievienot vai rediģēt prognozes rindas.</span><span class="sxs-lookup"><span data-stu-id="bcf68-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="bcf68-108">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="bcf68-109">Sarakstā atlasiet darba pasūtījumu un noklikšķiniet uz **Prognoze**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="bcf68-110">Sadaļā **Darba pasūtījuma uzturēšanas prognoze** tiek atlasītas prognozes rindas no uzturēšanas darba tipa, kas atlasīts darba pasūtījuma darbā.</span><span class="sxs-lookup"><span data-stu-id="bcf68-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="bcf68-111">Stundu prognozes pievienošana darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="bcf68-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="bcf68-112">Atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot prognozi.</span><span class="sxs-lookup"><span data-stu-id="bcf68-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="bcf68-113">Kopsavilkuma cilnē **Stundas** noklikšķiniet **Pievienot**, lai izveidotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="bcf68-114">Laukā **Kategorija** atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="bcf68-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="bcf68-115">Laukā **Stundas** ievadiet prognozēto stundu skaitu. </span><span class="sxs-lookup"><span data-stu-id="bcf68-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="bcf68-116">Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas tipu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="bcf68-117">Vienumu prognozes pievienošana darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="bcf68-117">Add items forecast to a work order</span></span>

<span data-ttu-id="bcf68-118">Ir trīs veidi, kādos pievienot vienumus darba pasūtījuma uzturēšanas prognozei: jūs varat izveidot rindas vienumiem (rezerves daļas), kuras nav iekļautas rezerves daļu sarakstā vai līdzekļa MK, jūs varat pievienot rezerves daļas no apstiprinātā rezerves daļu saraksta un jūs varat atlasīt vienumus no līdzekļa MK.</span><span class="sxs-lookup"><span data-stu-id="bcf68-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="bcf68-119">Atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot prognozi.</span><span class="sxs-lookup"><span data-stu-id="bcf68-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="bcf68-120">Atlasiet kopsavilkuma cilni **Vienumi**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="bcf68-121">Noklikšķiniet uz **Pievienot**, lai izveidotu jaunu rindu rezerves daļai, kura neatrodas rezerves daļu sarakstā vai līdzekļa MK sarakstā.</span><span class="sxs-lookup"><span data-stu-id="bcf68-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="bcf68-122">Atlasiet vienību laukā **Vienības kods**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="bcf68-123">Laukā **Pārdošanas daudzums** ievadiet daudzumu un laukā **Vienība** ievadiet daudzuma vienību. </span><span class="sxs-lookup"><span data-stu-id="bcf68-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="bcf68-124">Atbilstošajos laukos ievadies izmaksas un valūtu un atlasiet **Rindas rekvizītu**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="bcf68-125">Ja vēlaties mainīt vienuma rindās uzrādīto dimensiju sarakstu, noklikšķiniet uz **Inventārs** > **Rādīt dimensijas**, atlasiet dimensijas un atlasiet "Jā" pārslēgšanas pogā **Saglabāt uzstādījumu**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="bcf68-126">Ja vēlaties uzturēšanas prognozei pievienot apstiprinātu rezerves daļu, noklikšķiniet uz **Pievienot rezerves daļas**, atlasiet rezerves daļu, rediģējiet saistīto informāciju, ja nepieciešams, un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="bcf68-127">Ja vēlaties uzturēšanas prognozei pievienot līdzekļa MK vienumus, noklikšķiniet uz **Pievienot MK vienumus**, atlasiet vienumu, rediģējiet saistīto informāciju, ja nepieciešams, un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="bcf68-128">Noklikšķiniet uz **Vienums, kurā izmantots**, ja vēlaties iegūt pārskatu par to, kur Asset Management atlasītajā rindā vienums ir izmantots attiecībā uz līdzekļiem, uzturēšanas darba tipa noklusējumu, rezerves daļām un darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="bcf68-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="bcf68-129">Izdevumu prognozes pievienošana darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="bcf68-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="bcf68-130">Šajā tēmā ir paskaidrots, kā pievienot izdevumu prognozi darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="bcf68-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="bcf68-131">Veidlapas kreisajā pusē atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot prognozi.</span><span class="sxs-lookup"><span data-stu-id="bcf68-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="bcf68-132">Atlasiet kopsavilkuma cilni **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="bcf68-133">Noklikšķiniet uz **Pievienot**, lai izveidotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="bcf68-134">Laukā **Kategorija** atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="bcf68-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="bcf68-135">Laukā **Daudzums** ievadiet daudzumu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="bcf68-136">Atbilstošajos laukos ievadies izmaksas, pārdošanas valūtu un pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="bcf68-137">Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas tipu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="bcf68-138">Kopsavilkuma cilnē **Uzturēšanas prognozes kopsumma** jūs varat aplūkot pārskatu par vairākām rindām, kas izveidotas katrā cilnē, atlasītajam darba pasūtījuma darbam un darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="bcf68-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="bcf68-139">Jūs varat arī redzēt prognozēto darba stundu skaitu darba pasūtījuma darbam un darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="bcf68-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![1. attēls](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="bcf68-141">Automātiska darba pasūtījuma prognožu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="bcf68-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="bcf68-142">Lietojot Asset Management, jūs varat automātiski atjaunināt jebkādas izmaiņas darba pasūtījuma prognozēs attiecībā uz stundu izmaksām, vienumu izmaksām un izmaksām, kas ir atjauninātas citos moduļos programmā Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bcf68-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="bcf68-143">Tas tiek darīts, lai nodrošinātu to, ka jūsu darba pasūtījuma prognozēs vienmēr tiek izmantotas jaunākās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="bcf68-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="bcf68-144">Ir arī iespējams veikt līdzīgus atjauninājumus [uzturēšanas darba tipa prognozēm](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="bcf68-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="bcf68-145">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Prognoze** > **Atjaunināt darba pasūtījuma prognozi**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="bcf68-146">Nolaižamajā dialogā **Atjaunināt darba pasūtījuma prognozi** jūs varat pievienot izvēles attiecībā uz konkrētiem darba pasūtījumiem vai darba pasūtījuma darbiem, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="bcf68-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="bcf68-147">Lai veiktu šīs izvēles, noklikšķiniet uz **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="bcf68-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="bcf68-148">Ja nepieciešams, jūs varat ātrajā cilnē **Palaist fonā** uzstādīt automātisku atjauninājumu kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="bcf68-149">Noklikšķiniet uz **Labi**, lai sāktu prognozes atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="bcf68-149">Click **OK** to start the forecast update.</span></span>


![2. attēls](media/07-work-orders.png)

