--- 
title: "Papildu kārtulu struktūru izveide un piešķiršana"
description: "Šajā uzdevuma ceļvedī tiek aprakstīts, kā izveidot un piešķirt detalizētās kārtulas struktūru konta struktūrai."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a371e2bd08ee3f65658e015990d46a430267add2
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="5756c-103">Papildu kārtulu struktūru izveide un piešķiršana</span><span class="sxs-lookup"><span data-stu-id="5756c-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5756c-104">Šajā uzdevuma ceļvedī tiek aprakstīts, kā izveidot un piešķirt detalizētās kārtulas struktūru konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="5756c-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="5756c-105">Šajā ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="5756c-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="5756c-106">Izveidot papildu nosacījumu struktūru</span><span class="sxs-lookup"><span data-stu-id="5756c-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="5756c-107">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Struktūras > Detalizēto kārtulu struktūras.</span><span class="sxs-lookup"><span data-stu-id="5756c-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="5756c-108">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="5756c-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="5756c-109">Laukā Detalizētās kārtulas struktūra ierakstiet nosaukumu, lai aprakstītu kārtulas struktūru.</span><span class="sxs-lookup"><span data-stu-id="5756c-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="5756c-110">Laukā Apraksts ievadiet vērtību, lai aprakstītu struktūru.</span><span class="sxs-lookup"><span data-stu-id="5756c-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="5756c-111">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="5756c-111">Click OK.</span></span>
6. <span data-ttu-id="5756c-112">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="5756c-112">Click Add segment.</span></span>
7. <span data-ttu-id="5756c-113">Segmentu sarakstā atlasiet finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="5756c-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="5756c-114">Piemēram, Veikals.</span><span class="sxs-lookup"><span data-stu-id="5756c-114">For example, Store.</span></span>  
8. <span data-ttu-id="5756c-115">Noklikšķiniet uz Pievienot segmentu.</span><span class="sxs-lookup"><span data-stu-id="5756c-115">Click Add segment.</span></span>
9. <span data-ttu-id="5756c-116">Sarakstā, noklikšķiniet uz detalizētās kārtulas struktūras saites, lai to skatītu.</span><span class="sxs-lookup"><span data-stu-id="5756c-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="5756c-117">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="5756c-117">Click Activate.</span></span>
11. <span data-ttu-id="5756c-118">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="5756c-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="5756c-119">Detalizētās kārtulas struktūras lietošana konta struktūrai</span><span class="sxs-lookup"><span data-stu-id="5756c-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="5756c-120">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="5756c-120">Close the form.</span></span>
2. <span data-ttu-id="5756c-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5756c-121">Close the page.</span></span>
3. <span data-ttu-id="5756c-122">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Struktūras > Konfigurēt kontu struktūras.</span><span class="sxs-lookup"><span data-stu-id="5756c-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="5756c-123">Sarakstā atrodiet un atlasiet konta struktūru, kurai vēlaties lietot detalizēto kārtulu.</span><span class="sxs-lookup"><span data-stu-id="5756c-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="5756c-124">Noklikšķiniet uz konta struktūras nosaukuma, lai to atvērtu.</span><span class="sxs-lookup"><span data-stu-id="5756c-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="5756c-125">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="5756c-125">Click Edit.</span></span>
    * <span data-ttu-id="5756c-126">Varat arī noklikšķināt uz Detalizētā kārtula un jums tiks piedāvāts ievietot kontu struktūru melnraksta režīmā.</span><span class="sxs-lookup"><span data-stu-id="5756c-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="5756c-127">Noklikšķiniet uz Detalizētās kārtulas.</span><span class="sxs-lookup"><span data-stu-id="5756c-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="5756c-128">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="5756c-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="5756c-129">Laukā Detalizētā kārtula ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5756c-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="5756c-130">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5756c-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="5756c-131">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="5756c-131">Click Create.</span></span>
12. <span data-ttu-id="5756c-132">Noklikšķiniet uz Pievienot jaunus kritērijus.</span><span class="sxs-lookup"><span data-stu-id="5756c-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="5756c-133">Laukā Kur atlasiet galveno kontu vai finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="5756c-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="5756c-134">Laukā Operators atlasiet kādu opciju, piemēram, ir starp un ietver.</span><span class="sxs-lookup"><span data-stu-id="5756c-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="5756c-135">Laukā Vērtība ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5756c-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="5756c-136">Laukā Caur ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5756c-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="5756c-137">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="5756c-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="5756c-138">Sarakstā atrodiet detalizētās kārtulas struktūru, kuru vēlaties izmantot, kad ievadītie kritēriji būs izpildīti.</span><span class="sxs-lookup"><span data-stu-id="5756c-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="5756c-139">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="5756c-139">Click Add.</span></span>
20. <span data-ttu-id="5756c-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5756c-140">Close the page.</span></span>
21. <span data-ttu-id="5756c-141">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="5756c-141">Click Activate.</span></span>
22. <span data-ttu-id="5756c-142">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="5756c-142">Click Activate.</span></span>


