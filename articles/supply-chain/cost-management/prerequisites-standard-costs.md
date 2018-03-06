---
title: "Standarta izmaksu priekšnoteikumi"
description: "Šajā tēmā aprakstītas pamata darbības standarta izmaksu lietošanai."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e63f2b4289b640e601492425331ea8f3804d139a
ms.openlocfilehash: 4f505a2de89863d1a12d415795fdfb82b3557bc0
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="19c24-103">Standarta izmaksu priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="19c24-103">Prerequisites for standard costs</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="19c24-104">Šajā tēmā aprakstītas pamata darbības standarta izmaksu lietošanai.</span><span class="sxs-lookup"><span data-stu-id="19c24-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="19c24-105">Turpmākās darbības ir atkarīgas no uzņēmuma operācijām.</span><span class="sxs-lookup"><span data-stu-id="19c24-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="19c24-106">Piemēram, darbības atšķiras neražošanas videi, ražošanas videi, kurā netiek izmantota maršrutēšana, un ražošanas videi, kurā tiek izmantota maršrutēšana.</span><span class="sxs-lookup"><span data-stu-id="19c24-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="19c24-107">Lai iestatītu standarta izmaksas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="19c24-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="19c24-108">**1. Izveidojiet standarta izmaksu krājumu modeļa grupu.**</span><span class="sxs-lookup"><span data-stu-id="19c24-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="19c24-109">Izmantojiet lapu **Krājumu modeļu grupas**, lai izveidotu jaunu standarta izmaksu grupu, un piešķiriet vienuma **Standarta izmaksas** krājumu modeli.</span><span class="sxs-lookup"><span data-stu-id="19c24-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="19c24-110">Krājumu modeļu grupas identifikatoram ir jābūt jēgpilnam, piemēram, **Std izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="19c24-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="19c24-111">Atzīmējiet izvēles rūtiņas, lai norādītu, ka šai grupai jāatļauj negatīvi finanšu krājumi un jāgrāmato fiziskie krājumi un finanšu krājumi.</span><span class="sxs-lookup"><span data-stu-id="19c24-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="19c24-112">Šī standarta izmaksu grupa tiks piešķirta krājumiem.</span><span class="sxs-lookup"><span data-stu-id="19c24-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="19c24-113">**2. Definējiet ar standarta izmaksu novirzēm saistītos virsgrāmatas kontus.**</span><span class="sxs-lookup"><span data-stu-id="19c24-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="19c24-114">Izmantojiet lapu **Kontu plāns**, lai definētu virsgrāmatas kontus, kas ir saistīti ar standarta izmaksu novirzēm.</span><span class="sxs-lookup"><span data-stu-id="19c24-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="19c24-115">Šie virsgrāmatas konti jādefinē, pirms tos var piešķirti lapā **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="19c24-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="19c24-116">Virsgrāmatas konti var attēlot krājuma grupas un izmaksu grupas.</span><span class="sxs-lookup"><span data-stu-id="19c24-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="19c24-117">**3. Piešķiriet virsgrāmatas kontus krājumu grāmatojumiem, kas ir saistīti ar standarta izmaksu novirzēm.**</span><span class="sxs-lookup"><span data-stu-id="19c24-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="19c24-118">Izmantojiet lapu **Grāmatošana**, lai piešķirtu virsgrāmatas kontus, kas ir saistīti ar standarta izmaksu novirzēm.</span><span class="sxs-lookup"><span data-stu-id="19c24-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="19c24-119">Varat norādīt novirzes virsgrāmatas kontu pēc krājuma (vai krājumu grupas) un pēc izmaksu grupas (vai izmaksu grupas tipa) vai arī varat norādīt, ka virsgrāmatas konts attiecas uz visiem krājumiem un visām izmaksu grupām.</span><span class="sxs-lookup"><span data-stu-id="19c24-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="19c24-120">Šīs opcijas atbilst tabulu, grupu un visu elementu izmaksu relācijām.</span><span class="sxs-lookup"><span data-stu-id="19c24-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="19c24-121">Pirms definējat krājumu grāmatošanas kārtulas, izmantojiet lapu **Darbību kombinācijas**, lai iespējotu izmaksu relācijas (tabulām, grupām un visiem elementiem).</span><span class="sxs-lookup"><span data-stu-id="19c24-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="19c24-122">**4. Definējiet ar standarta izmaksām saistītos krājumu parametrus.**</span><span class="sxs-lookup"><span data-stu-id="19c24-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="19c24-123">Izmantojiet lapas **Krājumu parametri** cilni **Materiālu komplekti**, lai definētu izmaksu kontroles parametrus, kas ir saistīti ar standarta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="19c24-123">Use the **Bills of materials** tab on the **Inventory parameters** page to define two cost control parameters that are related to standard costs.</span></span> 

    -  <span data-ttu-id="19c24-124">Laukā **Izmaksu sadalījums** atlasiet opciju **Nav** vai **Apakšgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="19c24-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="19c24-125">Atlasot opciju **Apakšgrāmata**, izmaksu sadalījums ir *aktīvs* izmaksu sadalījums.</span><span class="sxs-lookup"><span data-stu-id="19c24-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="19c24-126">Aktīvs izmaksu sadalījums ir kritisks izmaksu grupu segmentācijas aprēķināšanai, atgūšanai un skatīšanai daudzlīmeņu struktūrā standarta izmaksu krājumiem.</span><span class="sxs-lookup"><span data-stu-id="19c24-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="19c24-127">Ja izmaksu sadalījums ir aktīvs, varat analizēt krājumus, nepabeigto ražošanu (NP) un pārdoto preču pašizmaksu (PPPI) uz izmaksu grupu vai sniegt par tiem pārskatu vienā līmenī, vairākos līmeņos vai visā sistēmā.</span><span class="sxs-lookup"><span data-stu-id="19c24-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="19c24-128">Ja izmaksu sadalījums ir aktīvs, aktivizējot ražotā krājuma izmaksas, izmaksu grupu segmentācija tiek saglabāta krājuma izmaksu ierakstā.</span><span class="sxs-lookup"><span data-stu-id="19c24-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="19c24-129">Atlasot opciju **Nav**, standarta izmaksu vienumiem netiks saglabāta izmaksu grupu segmentācija.</span><span class="sxs-lookup"><span data-stu-id="19c24-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="19c24-130">Citiem vārdiem sakot, ražotā vienuma standarta izmaksas tiks aprēķinātas un saglabātas kā viena summa bez izmaksu grupu segmentācijas.</span><span class="sxs-lookup"><span data-stu-id="19c24-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="19c24-131">Ražoto komponentu izmaksu ieguldījumi tiks apkopoti vienā summā.</span><span class="sxs-lookup"><span data-stu-id="19c24-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="19c24-132">Laukā **Novirzes no standarta** atlasiet opciju **Kopsavilkuma** vai **Uz izmaksu grupu**.</span><span class="sxs-lookup"><span data-stu-id="19c24-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="19c24-133">Atlasot opciju **Uz izmaksu grupu**, varat norādīt pirkšanas cenas novirzes un ražošanas novirzes pēc izmaksu grupas.</span><span class="sxs-lookup"><span data-stu-id="19c24-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="19c24-134">Varat arī norādīt četrus ražošanas noviržu tipus: laidiena lielumu, daudzumu, cenu un aizvietošanas novirzes.</span><span class="sxs-lookup"><span data-stu-id="19c24-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="19c24-135">Atlasot opciju **Kopsavilkuma**, nevarat norādīt novirzes pēc izmaksu grupas un četrus ražošanas noviržu tipus.</span><span class="sxs-lookup"><span data-stu-id="19c24-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="19c24-136">Ir iespējams skatīt tikai apkopotu ražošanas novirzi.</span><span class="sxs-lookup"><span data-stu-id="19c24-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="19c24-137">Ierobežojumi par novirzēm no standarta darbojas neatkarīgi no izmaksu sadalījuma ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="19c24-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="19c24-138">Citiem vārdiem sakot, varat atlasīt izmaksu sadalījuma politiku **Nav** un atlasīt novirzes pēc izmaksu grupas tā, lai ražošanas novirzes pēc izmaksu grupas joprojām tiktu paturētas.</span><span class="sxs-lookup"><span data-stu-id="19c24-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="19c24-139">**5. Izveidojiet izmaksu aprēķināšanas versijas standarta izmaksām.**</span><span class="sxs-lookup"><span data-stu-id="19c24-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="19c24-140">Izmantojiet lapu **Izmaksu aprēķināšanas versijas iestatījums**, lai izveidotu vienu vai vairākas izmaksu aprēķināšanas versijas standarta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="19c24-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="19c24-141">Katra izmaksu aprēķināšanas versija jāizveido ar izmaksu aprēķināšanas tipu **Standarta izmaksas**, un saturā jāļauj ietvert izmaksu datus.</span><span class="sxs-lookup"><span data-stu-id="19c24-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="19c24-142">**6. Sagatavojiet esošu klientu standarta izmaksu lietošanai.**</span><span class="sxs-lookup"><span data-stu-id="19c24-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="19c24-143">Klientiem, kas vēlas mainīt savus esošos krājumus uz standarta izmaksu krājumu modeli, jāizmanto lapa **Standarta izmaksu pārveidošana**.</span><span class="sxs-lookup"><span data-stu-id="19c24-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="19c24-144">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="19c24-144">Related topics</span></span>
--------

[<span data-ttu-id="19c24-145">Standarta izmaksu pārveidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="19c24-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

