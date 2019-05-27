---
title: Budžeta plānošanas datu sadalījums
description: Šajā rakstā ir aprakstītas dažādās sadalījuma metodes, kas ir pieejamas programmā Microsoft Dynamics 365 for Finance and Operations, un to lietošana.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 430040f7b3706aa1ad913d70c0dbcab9249ea222
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568147"
---
# <a name="budget-planning-data-allocation"></a><span data-ttu-id="cb13d-103">Budžeta plānošanas datu sadalījums</span><span class="sxs-lookup"><span data-stu-id="cb13d-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb13d-104">Šajā rakstā ir aprakstītas dažādās sadalījuma metodes, kas ir pieejamas programmā Microsoft Dynamics 365 for Finance and Operations, un to lietošana.</span><span class="sxs-lookup"><span data-stu-id="cb13d-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations and how they can be used.</span></span>  

<span data-ttu-id="cb13d-105">Varat sadalīt budžeta plāna datus vairākos veidos, lai precīzi attēlotu paredzamās summas.</span><span class="sxs-lookup"><span data-stu-id="cb13d-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="cb13d-106">Sadalījuma metodes</span><span class="sxs-lookup"><span data-stu-id="cb13d-106">Allocation methods</span></span>
<span data-ttu-id="cb13d-107">Trīs sadalījuma metodes (sadalīt periodos, sadalīt uz dimensijām un izmantot Virsgrāmatas sadalījuma kārtulas) var izveidot budžeta plāna rindas, kas balstās uz rindām vienā budžeta plānā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="cb13d-108">Trīs citas metodes (apkopot, izplatīt un kopēt no budžeta plāna) var izveidot budžeta plāna rindas citos budžeta plānos.</span><span class="sxs-lookup"><span data-stu-id="cb13d-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="cb13d-109">Visām sešām sadalījuma metodēm jānorāda mērķa scenārijs.</span><span class="sxs-lookup"><span data-stu-id="cb13d-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="cb13d-110">Mērķa scenārijs var būt vai nu tas pats avota scenārijs vai atšķirīgs no avota scenārija.</span><span class="sxs-lookup"><span data-stu-id="cb13d-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="cb13d-111">Papildus varat norādīt, vai jaunas rindas tiek pievienotas budžeta plānam vai aizstās esošās budžeta plāna rindas.</span><span class="sxs-lookup"><span data-stu-id="cb13d-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="cb13d-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Sadalīt pa periodiem** — lai budžeta plāna rindas no avota budžeta plāna scenārija sadalītu pa mērķa scenārija periodiem, tiek izmantota periodu sadalījuma kategorija.</span><span class="sxs-lookup"><span data-stu-id="cb13d-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="cb13d-113">Avota summa tiek piešķirta vairākām rindām mērķa scenārijā, pamatojoties uz procentuālo attiecību un datumu, kas ir noteikti perioda sadalījuma kategorijā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="cb13d-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Sadalījums uz dimensijām** — budžeta plāna rindas tiek sadalītas no avota budžeta plānošanas scenārija uz vienu vai vairākām rindām mērķa scenārijā, balstoties uz procentuālo sadalījumu un finanšu dimensijām, kas definētas atlasītajā budžeta sadalījuma noteikumā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="cb13d-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Apkopot** — budžeta plāna rindas tiek apkopotas no avota budžeta plāna scenārija saistītajos (pakārtotajos) budžeta plānos uz mērķa scenāriju pamata budžeta plānā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="cb13d-116">Šī metode ļauj budžeta summas, kas sagatavotas zemākā organizācijas līmenī, konsolidēt augstākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="cb13d-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="cb13d-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Izplatīt** — budžeta plāna rindas tiek izplatītas no avota budžeta plānošanas scenārija pamata budžeta plānā uz mērķa scenāriju saistītajos (pakārtotajos) budžeta plānos, pamatojoties uz saistīto plānu organizācijas vienību finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="cb13d-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="cb13d-118">Šī metode ļauj budžeta summas, kas sagatavotas augstākā organizācijas līmenī, izplatīt lokālai pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="cb13d-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="cb13d-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Izmantot Virsgrāmatas sadalījuma kārtulas** — budžeta plāna rindas tiek sadalītas no avota budžeta plānošanas scenārija uz mērķa scenāriju saskaņā ar atlasīto Virsgrāmatas sadalījuma kārtulu.</span><span class="sxs-lookup"><span data-stu-id="cb13d-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="cb13d-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopēt no budžeta plāna** — tāpat kā izplatīšanas sadalījuma metodē, budžeta plāna rindas tiek veidotas mērķa plānā, pamatojoties uz rindām saistītajā budžeta plānā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="cb13d-121">Tomēr šajā metodē avota budžeta plānam nav jābūt priekštecim, tas var būt jebkurā augstākā līmenī budžeta plānu hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="cb13d-122">Šī sadalījuma metode ir noderīga, ja konsolidētās summas sākotnēji tiek iekļautas budžetā daudz augstākā līmenī un tās jāpārsūta uz zemāku organizācijas līmeni sīkākai pārskatīšanai un pielāgošanai, pirms tās var saņemt augstāka līmeņa apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="cb13d-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="cb13d-123">Sadalījuma metožu izmantošana budžeta plānā</span><span class="sxs-lookup"><span data-stu-id="cb13d-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="cb13d-124">Lai veiktu sadalījumu budžeta plāna lapā, atlasiet sadalāmās rindas un pēc tam noklikšķiniet uz **Sadalīt budžetu**.</span><span class="sxs-lookup"><span data-stu-id="cb13d-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="cb13d-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="cb13d-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="cb13d-126">Pēc tam atlasiet sadalījuma metodi.</span><span class="sxs-lookup"><span data-stu-id="cb13d-126">Next, select an allocation method.</span></span> <span data-ttu-id="cb13d-127">Atlikušie lauki pēc tam tiek iestatīti, pamatojoties uz atlasītās metodes.</span><span class="sxs-lookup"><span data-stu-id="cb13d-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="cb13d-128">Šie lauki ietver avota un mērķa budžeta plānu datus un opciju, kas ļauj reizināt avotu ar norādīto koeficientu, izveidojot mērķa summas, lai vienkāršotu lielapjoma korekcijas.</span><span class="sxs-lookup"><span data-stu-id="cb13d-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="cb13d-129">Varat arī iestatīt opciju **Pievienot plānam**.</span><span class="sxs-lookup"><span data-stu-id="cb13d-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="cb13d-130">Atlasiet **Nē**, lai aizstātu esošās budžeta plāna rindas, vai atlasiet **Jā**, lai saglabātu esošās budžeta plāna rindas un pievienotu jaunas rindas sadalītajām summām.</span><span class="sxs-lookup"><span data-stu-id="cb13d-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="cb13d-131">Sadalījumu automatizācija darbplūsmas laikā</span><span class="sxs-lookup"><span data-stu-id="cb13d-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="cb13d-132">Jaudīga funkcija ļauj sadalījumus veikt automātiski kā daļu no budžeta plānošanas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="cb13d-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="cb13d-133">Budžeta plānam pārvietojoties pa tā darbplūsmu, automatizētie uzdevumi var uzsākt sadalījumu norādītajā budžeta plānošanas stadijā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="cb13d-134">Lai iestatītu automātisko sadalījumu, vispirms jāizveido sadalījuma grafiks lapā **Budžeta plānošanas konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="cb13d-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="cb13d-135">Sadalījuma grafiks nosaka sadalījuma metodi, kas tiks izmantota automatizētā sadalījuma izpildē un dažādu sadalījuma opciju vērtības (skatiet aprakstu iepriekšējā sadaļā).</span><span class="sxs-lookup"><span data-stu-id="cb13d-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="cb13d-136">Pēc tam izveidojiet stadijas sadalījumu lapā **Budžeta plānošanas konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="cb13d-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="cb13d-137">Stadijas sadalījums piešķir sadalījuma grafiku budžeta plānošanas darbplūsmai un stadijai.</span><span class="sxs-lookup"><span data-stu-id="cb13d-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="cb13d-138">Visbeidzot, pievienojiet automatizētu uzdevumu budžeta plānošanas stadijas sadalījumam vēlamajā darbplūsmas stadijā.</span><span class="sxs-lookup"><span data-stu-id="cb13d-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="cb13d-139">Šajā piemērā darbplūsmā ietverti divi budžeta plānošanas stadiju sadalījumi (apzīmēts ar sarkanu krāsu).</span><span class="sxs-lookup"><span data-stu-id="cb13d-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="cb13d-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="cb13d-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>



