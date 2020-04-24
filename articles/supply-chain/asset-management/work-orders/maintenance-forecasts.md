---
title: Uzturēšanas prognozes
description: Šajā tēmā ir paskaidrotas uzturēšanas prognozes programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0b9fb9265e93f27035e3770c6edbc9bb84d7a4df
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214831"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="a372e-103">Uzturēšanas prognozes</span><span class="sxs-lookup"><span data-stu-id="a372e-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a372e-104">Izveidojot darba pasūtījumu, jūs izveidojat darba pasūtījuma darbus, kam ir saistītie līdzekļi un uzturēšanas darba veidi.</span><span class="sxs-lookup"><span data-stu-id="a372e-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="a372e-105">Atlasot uzturēšanas darba veidu, kas satur uzturēšanas prognozes, prognozes tiek automātiski iekopētas darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="a372e-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="a372e-106">Iespējams, ka varat pievienot prognozes rindas darba pasūtījumam vai dzēst tās no darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="a372e-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="a372e-107">Darba pasūtījuma dzīves cikla stāvokļa iestatījums, saistītais projekta veids un stadijas noteikumi, kas ir saistīti ar projekta veidu, nosaka, vai varat pievienot vai rediģēt prognozes rindas.</span><span class="sxs-lookup"><span data-stu-id="a372e-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="a372e-108">Lai iegūtu vairāk informācijas par darba pasūtījumu dzīves cikla stāvokļiem un saistītiem projekta posmiem, skatiet sadaļu [Prognozes, darba pasūtījumi un projekti](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="a372e-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="a372e-109">Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**</span><span class="sxs-lookup"><span data-stu-id="a372e-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a372e-110">Atlasiet darba pasūtījumu no saraksta un pēc tam darbības rūtī > **Darba pasūtījums** cilnē > grupā **Projekti** atlasiet **Prognoze**.</span><span class="sxs-lookup"><span data-stu-id="a372e-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="a372e-111">Lapā **Darba pasūtījuma uzturēšanas prognoze** ir parādītas prognozes rindas no uzturēšanas darba veida, kas ir atlasīts darba pasūtījuma darbā.</span><span class="sxs-lookup"><span data-stu-id="a372e-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="a372e-112">Pievienot stundu prognozi darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="a372e-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="a372e-113">Lapā **Darba pasūtījuma uzturēšanas prognoze** atlasiet darba pasūtījuma darbu, lai pievienotu prognozi.</span><span class="sxs-lookup"><span data-stu-id="a372e-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="a372e-114">Kopsavilkuma cilnē **Stundas** atlasiet **Pievienot**, lai izveidotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="a372e-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="a372e-115">Atlasiet kategoriju laukā **Kategorija**.</span><span class="sxs-lookup"><span data-stu-id="a372e-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="a372e-116">Ievadiet prognozēto stundu skaitu laukā **Stundas**.</span><span class="sxs-lookup"><span data-stu-id="a372e-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="a372e-117">Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas veidu.</span><span class="sxs-lookup"><span data-stu-id="a372e-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="a372e-118">Pievienot vienumu prognozi darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="a372e-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="a372e-119">Ir trīs veidi, kā pievienot vienumus darba pasūtījuma uzturēšanas prognozei.</span><span class="sxs-lookup"><span data-stu-id="a372e-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="a372e-120">Jūs varat izveidot rindas vienumiem (rezerves daļas), kuras nav iekļautas rezerves daļu sarakstā vai līdzekļa materiālu komplekts (MK), jūs varat pievienot rezerves daļas no apstiprinātā rezerves daļu saraksta vai jūs varat atlasīt vienumus no līdzekļa MK.</span><span class="sxs-lookup"><span data-stu-id="a372e-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="a372e-121">Lai pievienotu prognozi, lapā **Darba pasūtījuma uzturēšanas prognoze** atlasiet darba pasūtījuma darbu.</span><span class="sxs-lookup"><span data-stu-id="a372e-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="a372e-122">Kopsavilkuma cilnē **Vienumi** pievienojiet vienumus uzturēšanas prognozei, izmantojot atbilstošo metodi.</span><span class="sxs-lookup"><span data-stu-id="a372e-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="a372e-123">Lai izveidotu rindu rezerves daļai, kura neatrodas rezerves daļu sarakstā vai līdzekļa MK sarakstā, veiciet šīs darbības:</span><span class="sxs-lookup"><span data-stu-id="a372e-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="a372e-124">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a372e-124">Select **Add**.</span></span>
2. <span data-ttu-id="a372e-125">Laukā **Vienības numurs** atlasiet vienību.</span><span class="sxs-lookup"><span data-stu-id="a372e-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="a372e-126">Ievadiet daudzumu laukā **Pārdošanas daudzums**.</span><span class="sxs-lookup"><span data-stu-id="a372e-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="a372e-127">Laukā **Vienība** atlasiet šim daudzumam izmantojamo mērvienību.</span><span class="sxs-lookup"><span data-stu-id="a372e-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="a372e-128">Laukā **Izmaksu cena** un laukā **Valūta** ievadiet atbilstošās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a372e-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="a372e-129">Laukā **Rindas rekvizīts** atlasiet rindas rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="a372e-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="a372e-130">Lai mainītu vienuma rindās uzrādīto dimensiju sarakstu, atlasiet **Inventārs** > **Rādīt dimensijas**, atlasiet dimensijas un tad iestatiet **Saglabāt uzstādījumu** opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a372e-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="a372e-131">Lai pievienotu rezerves daļu no apstiprinātu rezerves daļu saraksta, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="a372e-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="a372e-132">Atlasiet **Pievienot rezerves daļas**.</span><span class="sxs-lookup"><span data-stu-id="a372e-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="a372e-133">Atlasiet rezerves daļu un rediģējiet saistīto informāciju, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a372e-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="a372e-134">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a372e-134">Select **OK**.</span></span>

<span data-ttu-id="a372e-135">Lai pievienotu vienumu no pamatlīdzekļu MK, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="a372e-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="a372e-136">Atlasiet **Pievienot MK vienumus**.</span><span class="sxs-lookup"><span data-stu-id="a372e-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="a372e-137">Atlasiet vienumu un rediģējiet saistīto informāciju, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a372e-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="a372e-138">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a372e-138">Select **OK**.</span></span>

<span data-ttu-id="a372e-139">Lai iegūtu pārskatu par to, kur tiek izmantots atlasītās rindas vienība saistībā ar līdzekļiem, uzturēšanas darba veidu noklusējumiem, rezerves daļām un darba pasūtījumiem Līdzekļu pārvaldībā, atlasiet **Vienība tika izmantota**.</span><span class="sxs-lookup"><span data-stu-id="a372e-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="a372e-140">Papildinformāciju par šo pārskatu skatiet [Vienums, kurā izmantots](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="a372e-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="a372e-141">Pievienot izdevumu prognozi darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="a372e-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="a372e-142">Lapā **Darba pasūtījuma uzturēšanas prognoze** atlasiet darba pasūtījuma darbu, lai pievienotu prognozi.</span><span class="sxs-lookup"><span data-stu-id="a372e-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="a372e-143">Kopsavilkuma cilnē **Izdevumi** atlasiet **Pievienot**, lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="a372e-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="a372e-144">Atlasiet kategoriju laukā **Kategorija**.</span><span class="sxs-lookup"><span data-stu-id="a372e-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="a372e-145">Ievadiet daudzumu laukā **Daudzums**.</span><span class="sxs-lookup"><span data-stu-id="a372e-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="a372e-146">Laukos **Izmaksu cena**, **Pārdošanas valūta** un **Pārdošanas cena** ievadiet atbilstošas vērtības.</span><span class="sxs-lookup"><span data-stu-id="a372e-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="a372e-147">Laukā **Rindas rekvizīti** atlasiet rindai izmantojamo maksas veidu.</span><span class="sxs-lookup"><span data-stu-id="a372e-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="a372e-148">Kopsavilkuma cilnē **Uzturēšanas prognozes kopsumma** ir parādīts pārskats par vairākām rindām, kas tika izveidotas, atlasītajam darba pasūtījuma darbam un darba pasūtījumam katrā kopsavilkuma cilnē.</span><span class="sxs-lookup"><span data-stu-id="a372e-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="a372e-149">Tas arī parāda prognozēto darba stundu skaitu darba pasūtījuma darbam un darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a372e-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="a372e-150">Attēlā tālāk ir parādīts sarakstu lapas **Darba pasūtījumu uzturēšanas prognoze** piemērs.</span><span class="sxs-lookup"><span data-stu-id="a372e-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![1. attēls](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="a372e-152">Automātiska darba pasūtījuma prognožu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="a372e-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="a372e-153">Ja stundu izmaksas, vienumu izmaksas un izdevumi ir atjaunināti citos moduļos programmā Microsoft Dynamics 365 for Finance and Operations, darba pasūtījuma prognozes Līdzekļu pārvaldībā var būt automātiski atjauninātās, lai atspoguļotu šīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="a372e-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="a372e-154">Šī spēja palīdz garantēt, ka jūsu darba pasūtījuma prognozēs vienmēr tiek izmantotas jaunākās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="a372e-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="a372e-155">Varat arī veikt līdzīgus atjauninājumus [uzturēšanas darba tipa prognozēm](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="a372e-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="a372e-156">Atlasiet **Līdzekļu pārvaldība** > **Periodiski** > **Prognoze** > **Atjaunināt darba pasūtījuma prognozi**.</span><span class="sxs-lookup"><span data-stu-id="a372e-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="a372e-157">Dialogā **Atjaunināt darba pasūtījuma prognozi** kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** jūs varat pievienot izvēles attiecībā uz konkrētiem darba pasūtījumiem vai darba pasūtījuma darbiem, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a372e-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="a372e-158">Noklikšķiniet uz **Filtrēt**, lai veikt atbilstošās atlases.</span><span class="sxs-lookup"><span data-stu-id="a372e-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="a372e-159">Ātrajā cilnē **Palaist fonā** jūs varat pēc vajadzības uzstādīt automātisko atjauninājumu kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="a372e-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="a372e-160">Atlasiet **Labi**, lai sāktu prognozes atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="a372e-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="a372e-161">Attēlā tālāk ir parādīts sarakstu dialoga **Atjaunināt darba pasūtījumu prognozi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="a372e-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![2. attēls](media/07-work-orders.png)
