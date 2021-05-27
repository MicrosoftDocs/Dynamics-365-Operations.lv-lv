---
title: Kvalitātes pārvaldības testa mainīgie
description: Šajā tēmā ir aprakstīts, kā izveidot testa mainīgos, ko var izmantot kvalitātīvo pārbaudes pasūtījumu testēšanai Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021712"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="a2dd8-103">Kvalitātes pārvaldības testa mainīgie</span><span class="sxs-lookup"><span data-stu-id="a2dd8-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2dd8-104">Šajā tēmā ir aprakstīts, kā izveidot testa mainīgos, ko var izmantot kvalitātīvo pārbaudes pasūtījumu testēšanai Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a2dd8-105">Jums ir jādefinē testa mainīgais un tā iespējamie iznākumi katram kvalitatīvajam testam, kas ir definēts lapā **Testi**.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="a2dd8-106">(Kvalitatīvajiem testiem lauks **Veids** lapā **Testi** ir iestatīts uz *Opcija*.)</span><span class="sxs-lookup"><span data-stu-id="a2dd8-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="a2dd8-107">Izmantojiet lapu **Testa mainīgie**, lai iestatītu, rediģētu un skatītu iespējamos rezultātus ar kvalitatīvo testu saistītam testa mainīgajam.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="a2dd8-108">Katram rezultātam piešķiriet rezultāta statusu *Iztur* vai *Neiztur*, lai norādītu, vai tests ir nokārtots vai neizdevies, ja šis rezultāts ir atlasīts kā testa rezultāts.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="a2dd8-109">Lai testa mainīgo un noklusējuma iznākumu piešķirtu atsevišķam kvalitatīvajam testam, izmantojiet lapu **Testu grupas**.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="a2dd8-110">Katram testa mainīgajam ir ieteicams definēt vismaz divus iznākumus: vienu ar rezultāta statusu *Iztur* un vienu ar rezultāta statusu *Neiztur*.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="a2dd8-111">Mainīgo vai iznākumu kopskaitam nav ierobežojuma, ko var definēt.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="a2dd8-112">Turklāt vairāki testi var izmantot vienus un tos pašus testa mainīgos, lai ierakstītu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="a2dd8-113">Testa mainīgo piemēri</span><span class="sxs-lookup"><span data-stu-id="a2dd8-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="a2dd8-114">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a2dd8-114">Example 1</span></span>

<span data-ttu-id="a2dd8-115">Ražošanas uzņēmums veic divus testus ražotajiem materiāliem.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="a2dd8-116">Vienā testā pH līmenis ir saistīts ar krāsu joslu.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="a2dd8-117">Pieņemamie pH līmeņi ir gaišākās krāsās, un nepieņemamie pH līmeņi ir tumšākās krāsās.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="a2dd8-118">Citā testā tiek veiktas vairākas vizuālas pārbaudes un kvalitātes darbinieki izmanto savu vizuālu pārbaudi, lai noteiktu, vai krājums iztur vai neiztur vizuālo pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="a2dd8-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a2dd8-119">Example 2</span></span>

<span data-ttu-id="a2dd8-120">Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="a2dd8-121">Šajā pārbaudes testā ir vairāki mainīgie.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-121">This inspection test has several variables.</span></span> <span data-ttu-id="a2dd8-122">Viens mainīgais ir garša, un tā iespējamie iznākumi ir laba vai slikta.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="a2dd8-123">Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="a2dd8-124">Testa mainīgā izveide</span><span class="sxs-lookup"><span data-stu-id="a2dd8-124">Create a test variable</span></span>

<span data-ttu-id="a2dd8-125">Lai izveidotu testa mainīgo, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="a2dd8-126">Dodieties uz **Krājumu vadība \> Krājumu vadība \> Kvalitātes kontrole \> Kvalitātes kontrole**.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="a2dd8-127">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="a2dd8-128">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="a2dd8-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="a2dd8-129">**Mainīgais** – ievadiet unikālu ID vai nosaukumu mainīgām.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="a2dd8-130">**Apraksts** — ievadiet mainīgā detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="a2dd8-131">Kamēr jaunā rinda joprojām ir atlasīta, darbību rūtī atlasiet **Rezultātus**.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="a2dd8-132">Darbību rūts lapā **Testa mainīgo rezultāti** atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="a2dd8-133">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="a2dd8-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="a2dd8-134">**Rezultāts** – ievadiet unikālu ID vai nosaukumu rezultātam.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="a2dd8-135">**Apraksts** — ievadiet rezultāta detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="a2dd8-136">**Rezultāta statuss** - Atlasiet vai nu *Iztur*, vai *Neiztur*, lai norādītu, vai tests ir nokārtots vai neizdevies, ja rezultāts ir atlasīts kā testa rezultāts.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="a2dd8-137">Atkārtojiet iepriekšējo darbību katram papildu rezultātam.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="a2dd8-138">Pārliecinieties, vai vismaz vienam rezultātam ir rezultāta statuss - *Iztur* un vismaz vienam rezultāta statuss ir *Neiztur*.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="a2dd8-139">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="a2dd8-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2dd8-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a2dd8-140">Additional resources</span></span>

- [<span data-ttu-id="a2dd8-141">Kvalitātes pārvaldības testa instrumenti</span><span class="sxs-lookup"><span data-stu-id="a2dd8-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="a2dd8-142">Kvalitātes pārvaldības testi</span><span class="sxs-lookup"><span data-stu-id="a2dd8-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="a2dd8-143">Kvalitātes pārvaldības testa grupas</span><span class="sxs-lookup"><span data-stu-id="a2dd8-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
