---
title: Kvalitātes pārvaldības testi
description: Šajā tēmā ir aprakstīts, kā izveidot testus, ko var izmantot kvalitātes pārbaudes pasūtījumiem Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956743"
---
# <a name="quality-management-tests"></a><span data-ttu-id="91657-103">Kvalitātes pārvaldības testi</span><span class="sxs-lookup"><span data-stu-id="91657-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91657-104">Šajā tēmā ir aprakstīts, kā izveidot testus, ko var izmantot kvalitātes pārbaudes pasūtījumiem Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="91657-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="91657-105">Lapu **Testi** izmantojiet, lai definētu un skatītu atsevišķus testus, kas nosaka, vai produkti atbilst kvalitātes specifikācijām.</span><span class="sxs-lookup"><span data-stu-id="91657-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="91657-106">Vienu vai vairākus atsevišķus testus varat piešķirt testu grupai.</span><span class="sxs-lookup"><span data-stu-id="91657-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="91657-107">Šajā gadījumā jums ir jānorāda arī testa specifiskā informācija, piemēram, pieņemamās mērījumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="91657-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="91657-108">Mērījuma vērtības tiek izmantotas kvantitatīvajiem testiem.</span><span class="sxs-lookup"><span data-stu-id="91657-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="91657-109">Kvalitatīvajiem testiem tiek izmantoti testa mainīgie.</span><span class="sxs-lookup"><span data-stu-id="91657-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="91657-110">Kvantitatīviem testiem lauks **Veids** ir iestatīts uz *Vesels skaitlis* vai *Daļskaitlis*.</span><span class="sxs-lookup"><span data-stu-id="91657-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="91657-111">Ir norādīta arī mērvienība.</span><span class="sxs-lookup"><span data-stu-id="91657-111">A unit of measure is also specified.</span></span> <span data-ttu-id="91657-112">Kvalitātes specifikācijas un testa rezultāti tiek izteikti kā skaitļi.</span><span class="sxs-lookup"><span data-stu-id="91657-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="91657-113">Kvalitatīvajiem testiem lauks **Veids** ir iestatīts uz *Opcija*.</span><span class="sxs-lookup"><span data-stu-id="91657-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="91657-114">Kvalitatīvajiem testiem ir nepieciešama papildinformācija par testa mainīgo, kas tiek mērīts, un tā uzskaitīšanas iespējam.</span><span class="sxs-lookup"><span data-stu-id="91657-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="91657-115">Kvalitātes specifikācijas un testa rezultāti tiek izteikti atbilstoši rezultātam.</span><span class="sxs-lookup"><span data-stu-id="91657-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="91657-116">Testam var piešķirt arī pārbaudes instrumentu.</span><span class="sxs-lookup"><span data-stu-id="91657-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="91657-117">Tomēr, testa instrumenti nav nepieciešami, lai izveidotu un izmantotu testus ar kvalitātes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="91657-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="91657-118">Papildinformāciju skatiet [Kvalitātes pārvaldības testa instrumenti](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="91657-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="91657-119">Pēc izvēles var arī norādīt testa vienību, lai norādītu mērvienību, kādā tiek ierakstīti testa rezultāti.</span><span class="sxs-lookup"><span data-stu-id="91657-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="91657-120">Piemēram, temperatūras tests var ietvert Fahrenheita vai Celsija grādu vienību.</span><span class="sxs-lookup"><span data-stu-id="91657-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="91657-121">Testa piemērs</span><span class="sxs-lookup"><span data-stu-id="91657-121">Example of a test</span></span>

<span data-ttu-id="91657-122">Ražošanas uzņēmums iepirktajam materiālam veic divus testus: kvantitatīvo testu materiāla kvalitātei un kvalitatīvo testu iepakojuma bojājumam.</span><span class="sxs-lookup"><span data-stu-id="91657-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="91657-123">Uzņēmums norāda papildu informāciju par kvalitātes testu, lai definētu testa mainīgo (piemēram, bojāto iepakojumu) un tā rezultātus.</span><span class="sxs-lookup"><span data-stu-id="91657-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="91657-124">Uzņēmums izmanto lapu **Testu grupas**, lai abus testus piešķirtu testu grupai un norādītu testa specifisko informāciju.</span><span class="sxs-lookup"><span data-stu-id="91657-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="91657-125">Kvalitātes pasūtījumam tiek piešķirta testa grupā, tādējādi uzņēmums var ziņot testa rezultātus par diviem testiem.</span><span class="sxs-lookup"><span data-stu-id="91657-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="91657-126">Testa izveide</span><span class="sxs-lookup"><span data-stu-id="91657-126">Create a test</span></span>

<span data-ttu-id="91657-127">Lai izveidotu testu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="91657-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="91657-128">Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Kvalitātes kontrole \> Testi**.</span><span class="sxs-lookup"><span data-stu-id="91657-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="91657-129">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="91657-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="91657-130">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="91657-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="91657-131">**Tests** – ievadiet unikālu ID vai nosaukumu testam.</span><span class="sxs-lookup"><span data-stu-id="91657-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="91657-132">**Apraksts** — ievadiet testa detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="91657-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="91657-133">**Veids** – atlasiet testa rezultātu veidu.</span><span class="sxs-lookup"><span data-stu-id="91657-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="91657-134">Kvantitatīviem testiem atlasiet *Daļskaitlis* vai *Vesels skaitlis*.</span><span class="sxs-lookup"><span data-stu-id="91657-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="91657-135">Kvalitatīvajiem testiem atlasiet *Opciju*.</span><span class="sxs-lookup"><span data-stu-id="91657-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="91657-136">**Testa instruments** – atlasiet [testa instrumentu](quality-test-instruments.md), kas jāizmanto testam.</span><span class="sxs-lookup"><span data-stu-id="91657-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="91657-137">**Vienība** – ja jūs atlasījāt *Daļskaitlis* vai *Vesels skaitlis* laukā **Veids** (t.i., ja tests ir kvantitātes tests), atlasiet mērvienību, kurā jāieraksta testa rezultāti.</span><span class="sxs-lookup"><span data-stu-id="91657-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="91657-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="91657-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="91657-139">Pēc testa saglabāšanas režģī vairs nevar rediģēt lauku **Veids**.</span><span class="sxs-lookup"><span data-stu-id="91657-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="91657-140">Ja jāmaina testa rezultātu veids, kas tiks ierakstīts testam, darbību rūtī atlasiet **Mainīt kvalitātes testa veidu**.</span><span class="sxs-lookup"><span data-stu-id="91657-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="91657-141">Dialoglodziņā iestatiet lauku Jauns tips **Mainīt kvalitātes testa veidu** iestatiet lauku **Jauns veids** uz vajadzīgo veidu un pēc tam atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="91657-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91657-142">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="91657-142">Additional resources</span></span>

- [<span data-ttu-id="91657-143">Kvalitātes pārvaldības testa instrumenti</span><span class="sxs-lookup"><span data-stu-id="91657-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="91657-144">Kvalitātes pārvaldības testa grupas</span><span class="sxs-lookup"><span data-stu-id="91657-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="91657-145">Kvalitātes pārvaldības testa mainīgie</span><span class="sxs-lookup"><span data-stu-id="91657-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="91657-146">Kvalitātes piesaistes</span><span class="sxs-lookup"><span data-stu-id="91657-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
