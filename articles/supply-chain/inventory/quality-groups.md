---
title: Krājumu kvalitātes grupas
description: Šajā tēmā aprakstīts, kā izmantot un veidot krājumu kvalitātes grupas, lai loģiski sagrupētu preces, lai tās varētu piešķirt kvalitātes saistībām automātiskai kvalitātes pasūtījumu veidošanai.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022256"
---
# <a name="item-quality-groups"></a><span data-ttu-id="fcbf9-103">Krājumu kvalitātes grupas</span><span class="sxs-lookup"><span data-stu-id="fcbf9-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcbf9-104">Kvalitātes grupa norāda kopējās testēšanas vajadzības krājumam.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="fcbf9-105">Šajā tēmā aprakstīts, kā izmantot un veidot krājumu kvalitātes grupas, lai loģiski sagrupētu preces, lai tās varētu piešķirt kvalitātes saistībām automātiskai kvalitātes pasūtījumu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="fcbf9-106">Lai iestatītu, rediģētu un skatītu krājumus, kas ir piešķirti kvalitātes grupai vai kvalitātes grupām, kuras ir piešķirtas kādam krājumam, atveriet **Krājumu pārvaldība \> Iestatījums \> Kvalitātes grupas**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="fcbf9-107">Kad lapā **Testu grupas** ir definētas testa prasības, varat definēt kārtulas automātiskai kvalitātes pārbaudes pasūtījumu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="fcbf9-108">Lai vienkāršotu šo procesu, jūs nedefinējat kārtulas atsevišķiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="fcbf9-109">Tā vietā var definēt kārtulas kvalitātes grupai, lapā **Kvalitātes saistības**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="fcbf9-110">Krājumu kvalitātes grupas piemērs</span><span class="sxs-lookup"><span data-stu-id="fcbf9-110">Example of an item quality group</span></span>

<span data-ttu-id="fcbf9-111">Ražošanas uzņēmums iegādājas vairākus izejmateriālus, kuriem ir tādas pašas testēšanas vajadzības ienākošajai pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="fcbf9-112">Tāpēc uzņēmums definē kvalitātes grupu un pēc tam piešķir krājumu numurus, kas ir saistīti ar izejmateriāliem šai grupai.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="fcbf9-113">Vēlāk uzņēmums iegādājas jauna tipa izejmateriālu, kuram ir tādas pašas testēšanas vajadzības.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="fcbf9-114">Tā vietā, lai jaunajam materiālam iestatītu jaunas testēšanas vajadzības, jaunā materiāla krājumu kodu uzņēmums pievieno jau esošajai kvalitātes grupai.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="fcbf9-115">Tas pats uzņēmums ražo arī krājumus, kuriem ir tādas pašas ražošanas testēšanas vajadzības, un krājumus, kuriem ir tādas pašas vajadzības, sūta uz testēšanu pirms sūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="fcbf9-116">Tāpēc uzņēmums definē divas papildu kvalitātes grupas un pēc tam piešķir atbilstošos krājumu numurus katrai grupai.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="fcbf9-117">Kvalitātes grupas izveide</span><span class="sxs-lookup"><span data-stu-id="fcbf9-117">Create a quality group</span></span>

<span data-ttu-id="fcbf9-118">Lai izveidotu kvalitātes grupu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="fcbf9-119">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Kvalitātes grupas**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="fcbf9-120">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="fcbf9-121">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="fcbf9-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="fcbf9-122">**Kvalitātes grupa** – ievadiet unikālu ID vai nosaukumu kvalitātes grupai.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="fcbf9-123">**Apraksts** — ievadiet kvalitātes grupas detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="fcbf9-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="fcbf9-125">Krājumu manuālā pievienošana kvalitātes grupai</span><span class="sxs-lookup"><span data-stu-id="fcbf9-125">Manually add items to a quality group</span></span>

<span data-ttu-id="fcbf9-126">Lai manuāli pievienotu krājumus kvalitātes grupai, sekojiet šiem darbībām.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="fcbf9-127">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Kvalitātes grupas**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="fcbf9-128">Atlasiet kvalitātes grupu, kurai vēlaties pievienot krājumus.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="fcbf9-129">Darbību rūtī atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="fcbf9-130">Darbību rūts lapā **Krājuma kvalitātes grupās** atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="fcbf9-131">Pēc tam jaunajai rindai iestatiet lauku **Krājuma numurs** tā krājuma numuram, kuru vēlaties pievienot.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="fcbf9-132">Atkārtojiet iepriekšējo darbību katrai papildu precei, kas jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="fcbf9-133">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="fcbf9-134">Vairāku krājumu pievienošana kvalitātes grupai</span><span class="sxs-lookup"><span data-stu-id="fcbf9-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="fcbf9-135">Lai manuāli pievienotu vairākus krājumus kvalitātes grupai, sekojiet šiem darbībām.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="fcbf9-136">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Kvalitātes grupas**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="fcbf9-137">Izveidojiet vai atlasiet kvalitātes grupu, kurai vēlaties pievienot krājumus.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="fcbf9-138">Darbību rūtī atlasiet **Pievienot krājumus**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="fcbf9-139">Dialoglodziņā **Uzziņa** ievadiet krājumu filtra kritērijus, kurus vēlaties pievienot.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="fcbf9-140">Piemēram, varat filtrēt visus noteiktā krājumu grupā esošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="fcbf9-141">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-141">Select **OK**.</span></span>
1. <span data-ttu-id="fcbf9-142">Dialoglodziņā **Pievienot krājumus** režģis rāda visus vaicājumam atbilstošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="fcbf9-143">Rezultātu pārskatīšana.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-143">Review the results.</span></span>

    <span data-ttu-id="fcbf9-144">Ja nepieciešamas izmaiņas, atlasiet **Atlasīt**, lai atgrieztos dialoglodziņā **Uzziņa**, un pielāgojiet vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="fcbf9-145">Ja rezultātos ir iekļauti visi krājumi, ko vēlaties pievienot, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="fcbf9-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="fcbf9-147">Manuāli saistīt krājumu ar kvalitātes grupu</span><span class="sxs-lookup"><span data-stu-id="fcbf9-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="fcbf9-148">Lai manuāli saistītu krājumu ar kvalitātes grupu, sekojiet šiem darbībām.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="fcbf9-149">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Krajuma kvalitātes grupas**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="fcbf9-150">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="fcbf9-151">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="fcbf9-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="fcbf9-152">**Krājuma numurs** – izvēlieties pievienojamā krājuma numuru.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="fcbf9-153">**Kvalitātes grupa** – atlasiet kvalitātes grupu, kuru piešķirt krājumam.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="fcbf9-154">Atkārtojiet iepriekšējo darbību katrai papildu krājuma kombinācijai un kvalitātes grupai, kas jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="fcbf9-155">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="fcbf9-156">Manuāli pievienojiet kvalitātes grupu no Izlaisto preču lapas</span><span class="sxs-lookup"><span data-stu-id="fcbf9-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="fcbf9-157">Lai manuāli pievienotu kvalitātes grupu no lapas **Izlaistās preces**, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="fcbf9-158">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="fcbf9-159">Atlasiet preci, kurai vēlaties piešķirt kvalitātes grupu.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="fcbf9-160">Grupas **Kvalitāte** cilnes **Pārvaldīt krājumus** darbību rūtī atlasiet vienumu **Krajuma kvalitātes grupas**.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="fcbf9-161">Darbību rūts lapā **Krājuma kvalitātes grupās** atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="fcbf9-162">Pēc tam jaunajai rindai iestatiet lauku **Kvalitātes grupa** kvalitātes grupai, kuru vēlaties piešķirt produktam.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="fcbf9-163">Atkārtojiet iepriekšējo darbību katrai papildu kvalitātes grupai, ko vēlaties piešķirt precei.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="fcbf9-164">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="fcbf9-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcbf9-165">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fcbf9-165">Additional resources</span></span>

- [<span data-ttu-id="fcbf9-166">Kvalitātes pārvaldības testa instrumenti</span><span class="sxs-lookup"><span data-stu-id="fcbf9-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="fcbf9-167">Kvalitātes pārvaldības testi</span><span class="sxs-lookup"><span data-stu-id="fcbf9-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="fcbf9-168">Kvalitātes pārvaldības testa grupas</span><span class="sxs-lookup"><span data-stu-id="fcbf9-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="fcbf9-169">Kvalitātes pārvaldības testa mainīgie</span><span class="sxs-lookup"><span data-stu-id="fcbf9-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="fcbf9-170">Kvalitātes piesaistes</span><span class="sxs-lookup"><span data-stu-id="fcbf9-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
