---
title: Papildu kārtulu struktūru izveide un piešķiršana
description: Šajā tēmā ir paskaidrots, kā izveidot un piešķirt papildu kārtulu struktūru konta struktūrai.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175533"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="96642-103">Papildu kārtulu struktūru izveide un piešķiršana</span><span class="sxs-lookup"><span data-stu-id="96642-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96642-104">Šajā tēmā ir paskaidrots, kā izveidot un piešķirt papildu kārtulu struktūru konta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="96642-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="96642-105">Šajā ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="96642-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="96642-106">Izveidot papildu nosacījumu struktūru</span><span class="sxs-lookup"><span data-stu-id="96642-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="96642-107">Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu plāns > Struktūras > Detalizēto kārtulu struktūras**.</span><span class="sxs-lookup"><span data-stu-id="96642-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="96642-108">Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="96642-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="96642-109">Laukā **Detalizētās kārtulas struktūra** ierakstiet nosaukumu, lai aprakstītu kārtulas struktūru.</span><span class="sxs-lookup"><span data-stu-id="96642-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="96642-110">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96642-110">Select **OK**.</span></span>
5. <span data-ttu-id="96642-111">Atlasiet **Pievienot segmentu**.</span><span class="sxs-lookup"><span data-stu-id="96642-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="96642-112">Segmentu sarakstā atlasiet finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="96642-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="96642-113">Piemēram, **Veikals**.</span><span class="sxs-lookup"><span data-stu-id="96642-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="96642-114">Atlasiet **Pievienot segmentu**.</span><span class="sxs-lookup"><span data-stu-id="96642-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="96642-115">Atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="96642-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="96642-116">Detalizētās kārtulas struktūras lietošana konta struktūrai</span><span class="sxs-lookup"><span data-stu-id="96642-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="96642-117">Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu plāns > Struktūras > Konfigurēt kontu struktūras**.</span><span class="sxs-lookup"><span data-stu-id="96642-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="96642-118">Sarakstā atrodiet un atlasiet konta struktūru, kurai vēlaties lietot detalizēto kārtulu.</span><span class="sxs-lookup"><span data-stu-id="96642-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="96642-119">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="96642-119">Select **Edit**.</span></span> <span data-ttu-id="96642-120">Varat arī atlasīt **Detalizētā kārtula** un jums tiks piedāvāts ievietot kontu struktūru **Melnraksta režīmā**.</span><span class="sxs-lookup"><span data-stu-id="96642-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="96642-121">Atlasiet **Detalizētās kārtulas**.</span><span class="sxs-lookup"><span data-stu-id="96642-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="96642-122">Atalsiet **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="96642-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="96642-123">Laukā **Detalizētā kārtula** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="96642-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="96642-124">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="96642-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="96642-125">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="96642-125">Select **Create**.</span></span>
9. <span data-ttu-id="96642-126">Atlasiet **Pievienot jaunus kritērijus**.</span><span class="sxs-lookup"><span data-stu-id="96642-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="96642-127">Laukā **Kur** atlasiet galveno kontu vai finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="96642-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="96642-128">Laukā **Operators** atlasiet kādu opciju, piemēram, **ir starp** un **ietver**.</span><span class="sxs-lookup"><span data-stu-id="96642-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="96642-129">Laukā **Vērtība** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="96642-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="96642-130">Laukā **Caur** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="96642-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="96642-131">Atlasiet **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="96642-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="96642-132">Sarakstā atrodiet detalizētās kārtulas struktūru, kuru vēlaties izmantot, kad ievadītie kritēriji būs izpildīti.</span><span class="sxs-lookup"><span data-stu-id="96642-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="96642-133">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="96642-133">Select **Add**.</span></span>
17. <span data-ttu-id="96642-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="96642-134">Close the page.</span></span>
18. <span data-ttu-id="96642-135">Atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="96642-135">Select **Activate**.</span></span>

