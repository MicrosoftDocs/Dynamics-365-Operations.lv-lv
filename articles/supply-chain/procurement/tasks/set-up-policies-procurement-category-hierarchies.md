---
title: Ierobežojumu iestatīšana sagādes kategoriju hierarhijai
description: Izmantojiet šo procedūru, lai iestatītu nosacījumus preču pasūtīšanai kategorijā.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "323161"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="460bb-103">Ierobežojumu iestatīšana sagādes kategoriju hierarhijai</span><span class="sxs-lookup"><span data-stu-id="460bb-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="460bb-104">Izmantojiet šo procedūru, lai iestatītu nosacījumus preču pasūtīšanai kategorijā.</span><span class="sxs-lookup"><span data-stu-id="460bb-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="460bb-105">Kārtulas ir definētas noteiktai pirkšanas politikai.</span><span class="sxs-lookup"><span data-stu-id="460bb-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="460bb-106">Kategorijas piekļuves kārtulas kontrolē to, kurām sagādes kategorijām darbinieki var piekļūt, kad viņi veido pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="460bb-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="460bb-107">Kad tiek veidots pieprasījums, piemērojamo pirkšanas politiku un kategoriju piekļuves kārtulu nosaka juridiskā persona un darbības struktūrvienība, kurai šis darbinieks pieder.</span><span class="sxs-lookup"><span data-stu-id="460bb-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="460bb-108">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="460bb-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="460bb-109">Šo uzdevumu parasti veic pirkšanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="460bb-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="460bb-110">Atrast sagādes politiku</span><span class="sxs-lookup"><span data-stu-id="460bb-110">Find the procurement policy</span></span>
1. <span data-ttu-id="460bb-111">Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas.</span><span class="sxs-lookup"><span data-stu-id="460bb-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="460bb-112">Noklikšķiniet uz saites uz Sagādes politika USMF politikas.</span><span class="sxs-lookup"><span data-stu-id="460bb-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="460bb-113">Šis ir politika, kurai pievienojat kārtulu.</span><span class="sxs-lookup"><span data-stu-id="460bb-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="460bb-114">Tai ir jābūt aktīvai politikai.</span><span class="sxs-lookup"><span data-stu-id="460bb-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="460bb-115">Kategorijas piekļuves kārtulas izveidošana</span><span class="sxs-lookup"><span data-stu-id="460bb-115">Create a category access rule</span></span>
1. <span data-ttu-id="460bb-116">Atlasiet vienumu Kategorijas piekļuves politikas kārtula.</span><span class="sxs-lookup"><span data-stu-id="460bb-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="460bb-117">Ja poga Izveidot politikas kārtulu ir pelēkota, tas nozīmē, ka kategorijas piekļuvei jau ir aktīva politikas kārtula.</span><span class="sxs-lookup"><span data-stu-id="460bb-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="460bb-118">Pārbaudiet laukus Spēkā stāšanās datums un Beigu datums, lai noteiktu, kura tā ir, un pēc tam atlasiet to un noklikšķiniet uz Noņemt politikas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="460bb-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="460bb-119">Ja poga Izveidot politikas kārtulu ir pieejama, jums nav jādara nekas.</span><span class="sxs-lookup"><span data-stu-id="460bb-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="460bb-120">Noklikšķiniet uz Izveidot politikas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="460bb-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="460bb-121">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="460bb-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="460bb-122">Šis laiks nedrīkst pārklāties ar citu kārtulu, kas jau ir aktīva.</span><span class="sxs-lookup"><span data-stu-id="460bb-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="460bb-123">Atlasiet kategoriju, uz kuru šī kārtula attieksies.</span><span class="sxs-lookup"><span data-stu-id="460bb-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="460bb-124">Ievērojiet, kāda tai ir kategorija — tā jums vēlāk būs nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="460bb-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="460bb-125">Kad atlasāt kategoriju, atlasīto kategoriju sarakstam tiek pievienota arī tās pamatkategorija vai pamatkategorijas.</span><span class="sxs-lookup"><span data-stu-id="460bb-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="460bb-126">Ja vēlaties, lai kārtula attiecas arī uz visām atlasītās kategorijas apakškategorijām, atzīmējiet izvēles rūtiņu Iekļaut apakškategorijas.</span><span class="sxs-lookup"><span data-stu-id="460bb-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="460bb-127">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="460bb-127">Click Add.</span></span>
    * <span data-ttu-id="460bb-128">Ja opciju Iekļaut vecākelementa kārtulu ir iestatāt uz Jā, tad politikas kārtula, ko definējat vecākelementa kategorijai, tiek piešķirta arī tās bērnelementa kategorijām, ja šīm bērnelementa kategorijām nav definēta neviena politikas kārtula.</span><span class="sxs-lookup"><span data-stu-id="460bb-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="460bb-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="460bb-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="460bb-130">Kategorijas politikas kārtulas izveidošana</span><span class="sxs-lookup"><span data-stu-id="460bb-130">Create a category policy rule</span></span>
1. <span data-ttu-id="460bb-131">Atlasīt kategorijas politikas kārtulu</span><span class="sxs-lookup"><span data-stu-id="460bb-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="460bb-132">Ja poga Izveidot politikas kārtulu ir pelēkota, atlasiet aktīvo politikas kārtulu un pēc tam noklikšķiniet uz Noņemt politikas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="460bb-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="460bb-133">Noklikšķiniet uz Izveidot politikas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="460bb-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="460bb-134">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="460bb-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="460bb-135">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="460bb-135">Click Add.</span></span>
5. <span data-ttu-id="460bb-136">Atlasiet to pašu kategoriju, ko lietojāt iestatījumam Kategorijas piekļuves kārtula.</span><span class="sxs-lookup"><span data-stu-id="460bb-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="460bb-137">Laukā Kreditora atlase atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="460bb-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="460bb-138">Atlasiet kārtulu, lai kontrolētu, kāda veida kreditorus var atlasīt kategorijai, kad tiek veidoti pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="460bb-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="460bb-139">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="460bb-139">Click Close.</span></span>
    * <span data-ttu-id="460bb-140">Jūsu definētās politikas kārtulas bija paredzētas pieprasījumiem ar tipu Patēriņš.</span><span class="sxs-lookup"><span data-stu-id="460bb-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="460bb-141">Ja vēlaties definēt politikas pieprasījumiem ar tipu Papildināšana, jums būtu jāizveido kārtula politikas kārtulas tipam ar nosaukumu “Papildināšanas kategorijas piekļuves politikas kārtula”.</span><span class="sxs-lookup"><span data-stu-id="460bb-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  

