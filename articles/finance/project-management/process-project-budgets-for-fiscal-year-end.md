---
title: Pārnest projektu budžetus fiskālā gada beigās
description: Šajā rakstā sniegta informācija par to, kā pārsūtīt atlikušās budžeta summas uz nākamajiem gadiem un izveidot budžeta reģistra informāciju.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172334"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="3699b-103">Pārnest projektu budžetus fiskālā gada beigās</span><span class="sxs-lookup"><span data-stu-id="3699b-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3699b-104">Strādājot pie daudzgadu projekta, iespējams, jums fiskālā gada beigās radies budžeta pārpalikums.</span><span class="sxs-lookup"><span data-stu-id="3699b-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="3699b-105">Varat pārvirzīt atlikušās budžeta summas uz gadu nākotnē un izveidot budžeta reģistra informāciju summām virsgrāmatas kontos.</span><span class="sxs-lookup"><span data-stu-id="3699b-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="3699b-106">Pirms atlikušo summu pārnešanas, pārskatiet un analizējiet atlikušās budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="3699b-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="3699b-107">Atlikušo budžeta summu pārskatīšana un analizēšana</span><span class="sxs-lookup"><span data-stu-id="3699b-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="3699b-108">Veiciet šādas darbības, lai pārskatītu gada beigu budžeta summas projektiem, taču šīs summas nepārnestu.</span><span class="sxs-lookup"><span data-stu-id="3699b-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="3699b-109">Dodieties uz **Projektu vadība un uzskaite** > **Periodiski** > **Budžeti** > **Pārnest budžetus**.</span><span class="sxs-lookup"><span data-stu-id="3699b-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="3699b-110">Lapā **Projekta budžeta pārnešanas process**, kas atrodas cilnē **Gada beigu opcijas**, pārbaudiet, vai nav aktivizēta opcija **Pārnest atlikušās projekta budžeta summas**.</span><span class="sxs-lookup"><span data-stu-id="3699b-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="3699b-111">Cilnes **Parametri** laukā **Projekta budžeta gads** atlasiet fiskālo gadu, kuram vēlaties skatīt atlikušo budžeta summu.</span><span class="sxs-lookup"><span data-stu-id="3699b-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="3699b-112">Laukā **Atvēršanas fiskālais gads** atlasiet finanšu gada sākumu, kuram vēlaties skatīt atlikušās budžeta summu.</span><span class="sxs-lookup"><span data-stu-id="3699b-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="3699b-113">Laukā **No prognozes modeļa** atlasiet **Atlikušais budžets**.</span><span class="sxs-lookup"><span data-stu-id="3699b-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="3699b-114">Lai iekļautu projektus, kas atbilst jūsu atlasītajiem kritērijiem un kuriem nav budžeta pārpalikuma, atlasiet **Rādīt nulles atlikumu**.</span><span class="sxs-lookup"><span data-stu-id="3699b-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="3699b-115">Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus**, lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem, un pēc atlasiet **Apstrādāt**.</span><span class="sxs-lookup"><span data-stu-id="3699b-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="3699b-116">Lai izveidotu datu bāzes vaicājumu, kas rūtī ielādē konkrētu budžetu kopu, atlasiet **Izgūt atlasītos budžetus**.</span><span class="sxs-lookup"><span data-stu-id="3699b-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="3699b-117">Lai iegūtu papildu informāciju par noteiktu rindu rūtī, atlasiet rindu un pēc tam atlasiet **Skatīt budžeta informāciju** vai **Skatīt kontus**.</span><span class="sxs-lookup"><span data-stu-id="3699b-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="3699b-118">Pārnest atlikušās budžeta summas</span><span class="sxs-lookup"><span data-stu-id="3699b-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="3699b-119">Apstrādājot atlikušās budžeta summas, varat Virsgrāmatā izveidot transakcijas summām, kuras pārnesat.</span><span class="sxs-lookup"><span data-stu-id="3699b-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="3699b-120">Lai izveidotu Virsgrāmatas darījumus, veiciet darbības, kas norādītas sadaļā [Pārnesiet budžeta summas un izveidojiet Virsgrāmatas transakcijas](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="3699b-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="3699b-121">Pārnestās budžeta summas tiek pārvirzītas uz prognozes modeli, ko atlasa lapā **Prognozes modeļi** kā pārnesamo prognozes modeli.</span><span class="sxs-lookup"><span data-stu-id="3699b-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="3699b-122">Budžeta summu pārnešana un virsgrāmatas darījumu izveidošana</span><span class="sxs-lookup"><span data-stu-id="3699b-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="3699b-123">Atlasiet **Projektu vadība un uzskaite** > **Periodiski** > **Budžeti** > **Pārnest budžetus**.</span><span class="sxs-lookup"><span data-stu-id="3699b-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="3699b-124">Lapā **Projekta budžeta pārneses process** atlasiet **Gada beigas**un pēc tam iespējojiet **Pārnest atlikušās projekta budžeta summas** un **Izveidot budžeta reģistra ierakstus Virsgrāmatā**.</span><span class="sxs-lookup"><span data-stu-id="3699b-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="3699b-125">Cilnē **Parametri**, kas atrodas lauku grupā **Projekta parametri**, atlasiet sekojošo:</span><span class="sxs-lookup"><span data-stu-id="3699b-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="3699b-126">**Projekta budžeta gads**: Atlasiet finanšu gada sākumu, kuram vēlaties skatīt atlikušās budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="3699b-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="3699b-127">**Peļņa un zaudējumi**: Izveidojiet peļņas un zaudējumu transakcijas Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="3699b-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="3699b-128">**NP**: Izveidojiet nepabeigto darbu (NP) transakcijas Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="3699b-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="3699b-129">**Alga**: Izveidojiet algas sadalījuma transakcijas Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="3699b-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="3699b-130">Lauka grupā **Virsgrāmata** norādiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="3699b-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="3699b-131">Laukā **Atvēršanas fiskālais gads** atlasiet finanšu gada sākumu, uz kuru vēlaties pārsūtīt projektiem atlikušās budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="3699b-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="3699b-132">Noklusētā vērtība ir viens gads pēc vērtības laukā **Projekta budžeta gads**.</span><span class="sxs-lookup"><span data-stu-id="3699b-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="3699b-133">Laukā **Pārneses periods** atlasiet periodu, kuram vēlaties izveidot budžeta reģistra informāciju virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="3699b-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="3699b-134">Parasti tas ir pirmais periods atvērtajā finanšu gadā.</span><span class="sxs-lookup"><span data-stu-id="3699b-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="3699b-135">Lauka grupā **Kopēt no/uz** norādiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="3699b-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="3699b-136">Laukā **No prognozes modeļa** atlasiet projekta budžeta modeli, kas ir saistīts ar atlikušajām budžeta summām, kuras vēlaties pārsūtīt projektiem.</span><span class="sxs-lookup"><span data-stu-id="3699b-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="3699b-137">Laukā **Uz Virsgrāmatas budžeta modeli** atlasiet virsgrāmatas budžeta modeli, kas ir saistīts ar budžeta summām, kuras vēlaties pārsūtīt uz virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="3699b-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="3699b-138">Lai izmantotu projekta pārdošanas valūtu virsgrāmatas darījumiem, kas tiek izveidoti, kad projektiem pārsūtāt budžeta summas, atlasiet **Pārvirzīt pārdošanas valūtu**.</span><span class="sxs-lookup"><span data-stu-id="3699b-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="3699b-139">Kad opcija nav atlasīta, transakcijas izmanto uzskaites valūtu.</span><span class="sxs-lookup"><span data-stu-id="3699b-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="3699b-140">Atlasiet **Rādīt nulles atlikumu**, lai iekļautu projektus, kuriem nav pārpalikušu budžeta summu, taču atbilst citiem kritērijiem, kurus atlasiet projektos, kas rādīti apakšējā rūtī.</span><span class="sxs-lookup"><span data-stu-id="3699b-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="3699b-141">Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus**, lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="3699b-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="3699b-142">ja labāk vēlaties izveidot datu bāzes vaicājumu, kas rūtī ielādē konkrētu projekta budžetu kopu, atlasiet **Izgūt atlasītos budžetus**.</span><span class="sxs-lookup"><span data-stu-id="3699b-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="3699b-143">Katram projektam, ko vēlaties apstrādāt, atzīmējiet opciju šī projekta rindas sākumā.</span><span class="sxs-lookup"><span data-stu-id="3699b-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="3699b-144">Lai atlasītu visus vai vairumu projektu, atzīmējiet izvēles rūtiņu augšējā kreisajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="3699b-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="3699b-145">Lai neiekļautu nevienu projektu, noņemiet atzīmi šim projektam.</span><span class="sxs-lookup"><span data-stu-id="3699b-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="3699b-146">Lai atlasītajiem projektiem atlikušās budžeta summas nodotu atlasītājam finanšu gadam un izveidotu budžeta reģistra informāciju Virsgrāmatā, noklikšķiniet **Apstrādāt**.</span><span class="sxs-lookup"><span data-stu-id="3699b-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="3699b-147">Budžeta summu pārnešana bez Virsgrāmatas darījumu izveidošanas</span><span class="sxs-lookup"><span data-stu-id="3699b-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="3699b-148">Dodieties uz **Projektu vadība un uzskaite** > **Periodiski** > **Budžeti** > **Pārnest budžetus**.</span><span class="sxs-lookup"><span data-stu-id="3699b-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="3699b-149">Lapas **Projekta budžeta pārnešanas process** laukā **Gada beigu opcijas** atlasiet opciju **Pārnest atlikušās projekta budžeta summas**.</span><span class="sxs-lookup"><span data-stu-id="3699b-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="3699b-150">Grupas **Parametri** laukā **Projekta budžeta gads** atlasiet fiskālo gadu, kuram vēlaties skatīt atlikušās budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="3699b-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="3699b-151">Grupā **Kopēt no/uz** norādiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="3699b-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="3699b-152">Laukā **No prognozes modeļa** atlasiet projekta budžeta modeli, kas ir saistīts ar atlikušajām budžeta summām, kuras vēlaties pārsūtīt projektiem.</span><span class="sxs-lookup"><span data-stu-id="3699b-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="3699b-153">Lai iekļautu projektus, kuriem nav budžeta pārpalikuma bet kas atbilst citiem jūsu atlasītajiem kritērijiem, atlasiet **Rādīt nulles atlikumu**.</span><span class="sxs-lookup"><span data-stu-id="3699b-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="3699b-154">Grupā **Atlasīt budžetus** atlasiet **Izgūt visus budžetus**, lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="3699b-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="3699b-155">Lai izveidotu datu bāzes vaicājumu, kas rūtī ielādē konkrētu projekta budžetu kopu, atlasiet **Izgūt atlasītos budžetus**.</span><span class="sxs-lookup"><span data-stu-id="3699b-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="3699b-156">Katram projektam, ko vēlaties apstrādāt, atzīmējiet opciju šī projekta rindas sākumā.</span><span class="sxs-lookup"><span data-stu-id="3699b-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="3699b-157">Atlasiet **Apstrādāt**, lai izvēlētajiem projektiem atlikušās budžeta summas nodotu atlasītājam finanšu gadam.</span><span class="sxs-lookup"><span data-stu-id="3699b-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

