---
title: Biznesa dokumenta veidnes struktūras atjaunināšana
description: Šajā tēmā paskaidrots, kā atjaunināt biznesa dokumenta veidnes struktūru, izmantojot biznesa dokumentu pārvaldības līdzekli.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cb0188e372b5f6275472cf040d10bb796eed1858
ms.sourcegitcommit: 95d2fc0fa7d17d3a96f7969f12c985b018b4ff94
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/12/2020
ms.locfileid: "4728093"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="e2d00-103">Biznesa dokumenta veidnes struktūras atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="e2d00-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2d00-104">Rūtī **Veidnes struktūra**, kas atrodas veidnes redaktorā [Biznesa dokumentu pārvaldība](er-business-document-management.md), varat modificēt biznesa dokumenta veidni, [pievienojot jaunus laukus](er-bdm-add-field-to-excel-template.md) veidnei Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e2d00-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="e2d00-105">Tad veidnes struktūra tiek automātiski atjaunināta Dynamics 365 Finance, lai tā atspoguļotu izmaiņas, ko veicāt rūtī **Veidnes struktūra**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="e2d00-106">Varat arī modificēt veidni, izmantojot Office 365 tiešsaistes funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="e2d00-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="e2d00-107">Piemēram, rediģējamajā darblapā varat pievienot jaunu nosauktu krājumu, piemēram, attēlu vai formu.</span><span class="sxs-lookup"><span data-stu-id="e2d00-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="e2d00-108">Šādā gadījumā veidnes struktūra netiek automātiski atjaunināta Finance, un pievienotais krājums netiek parādīts rūtī **Veidnes struktūra**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="e2d00-109">Manuāli atjauniniet veidnes struktūru Finance, veidnes redaktora lapā atlasot **Atjaunināt struktūru**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="e2d00-110">Lai iegūtu vairāk informācijas par šo līdzekli, izpildiet tālāk minēto piemēru.</span><span class="sxs-lookup"><span data-stu-id="e2d00-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="e2d00-111">Piemērs: biznesa dokumenta veidnes struktūras atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="e2d00-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="e2d00-112">Šis piemērs parāda, kā sistēmas administrators var atjaunināt biznesa dokumenta veidnes struktūru Finance pēc veidnes modificēšanas Office Online.</span><span class="sxs-lookup"><span data-stu-id="e2d00-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="e2d00-113">Turpmākajās sadaļās ir izskaidrotas tam nepieciešamās darbības.</span><span class="sxs-lookup"><span data-stu-id="e2d00-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="e2d00-114">Biznesa dokumenta veidnes sagatavošana rediģēšanai</span><span class="sxs-lookup"><span data-stu-id="e2d00-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="e2d00-115">Veiciet procedūras, kas norādītas [Biznesa dokumentu pārvaldības pārskatā](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="e2d00-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="e2d00-116">Konfigurējiet ER parametrus</span><span class="sxs-lookup"><span data-stu-id="e2d00-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="e2d00-117">ER risinājumu importēšana</span><span class="sxs-lookup"><span data-stu-id="e2d00-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="e2d00-118">Biznesa dokumentu pārvaldības iespējošana</span><span class="sxs-lookup"><span data-stu-id="e2d00-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="e2d00-119">Konfigurēt parametrus</span><span class="sxs-lookup"><span data-stu-id="e2d00-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="e2d00-120">Biznesa dokumenta veidnes rediģēšana</span><span class="sxs-lookup"><span data-stu-id="e2d00-120">Edit a business document template</span></span>

1. <span data-ttu-id="e2d00-121">Darbvietā **Biznesa dokumentu pārvaldība** atlasiet **Jauns dokuments**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="e2d00-122">Lapā **Izveidot jaunu veidni** atlasiet veidni **Brīva teksta rēķins (ER paraugs)(Excel)**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="e2d00-123">Atlasiet **Izveidot dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-123">Select **Create document**.</span></span>
4. <span data-ttu-id="e2d00-124">Laukā **Nosaukums** ievadiet **FTI paraugs Litware**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="e2d00-125">Atlasiet **Labi**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="e2d00-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2d00-126">Ja vēl neesat pierakstījies Office Online, jūs tiekat [novirzīts uz Office 365 pierakstīšanās lapu](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="e2d00-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="e2d00-127">Lai atgrieztos savā Finance vidē, pārlūkprogrammā atlasiet pogu **Atpakaļ**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="e2d00-128">Jaunā veidne tiek atvērta rediģēšanai Excel Online iegultajā vadīklā veidnes redaktora lapā.</span><span class="sxs-lookup"><span data-stu-id="e2d00-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="e2d00-129">[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai sāktu biznesa dokumenta veidnes rediģēšanu](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="e2d00-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="e2d00-130">Pašreizējās rediģējamās veidnes struktūras pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="e2d00-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="e2d00-131">Excel Online lentē, kas atrodas cilnē **Skats**, grupā **Rādīt** atlasiet **Režģlīnijas**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="e2d00-132">Rediģējamajā veidnē atlasiet taisnstūri virs veidnes virsraksta.</span><span class="sxs-lookup"><span data-stu-id="e2d00-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="e2d00-133">Šis taisnstūris ir attēls, kura nosaukums ir **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="e2d00-134">Ja rūts **Veidnes struktūra** ir paslēpta, atlasiet **Rādīt struktūru**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="e2d00-135">Rūtī **Veidnes struktūra** izvērsiet **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="e2d00-136">Ņemiet vērā, ka Finance veidnes struktūrā krājums **rptHeaderCompLogo** tiek parādīts kā pakārtotais krājums **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="e2d00-137">[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai pārskatītu rediģējamas veidnes pašreizējo struktūru](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="e2d00-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="e2d00-138">Biznesa dokumenta veidnes struktūras atjaunināšana, dzēšot attēlu</span><span class="sxs-lookup"><span data-stu-id="e2d00-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="e2d00-139">Excel Online rediģējamajā veidnē atlasiet attēlu **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="e2d00-140">Izpildiet vienu no norādītajām darbībām, lai dzēstu atlasīto attēlu no rediģējamās veidnes.</span><span class="sxs-lookup"><span data-stu-id="e2d00-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="e2d00-141">Atlasiet taustiņu **Dzēst** uz tastatūras.</span><span class="sxs-lookup"><span data-stu-id="e2d00-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="e2d00-142">Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) attēlu, un pēc tam atlasiet **Izgriezt**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e2d00-143">Krājums **rptHeaderCompLogo** pašlaik joprojām atrodas Finance veidnes struktūrā, pat ja attēls vairs nav iekļauts Excel veidnē.</span><span class="sxs-lookup"><span data-stu-id="e2d00-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="e2d00-144">Atlasiet **Atjaunināt struktūru**, lai sinhronizētu rediģējamās veidnes struktūru Excel un Finance.</span><span class="sxs-lookup"><span data-stu-id="e2d00-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="e2d00-145">Rūtī **Veidnes struktūra** izvērsiet **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="e2d00-146">Ņemiet vērā, ka krājums **rptHeaderCompLogo** vairs nav iekļauts Finance veidnes struktūrā.</span><span class="sxs-lookup"><span data-stu-id="e2d00-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="e2d00-147">[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai dzēstu attēlu no biznesa dokumenta veidnes](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="e2d00-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="e2d00-148">Biznesa dokumenta veidnes struktūras atjaunināšana, pievienojot attēlu</span><span class="sxs-lookup"><span data-stu-id="e2d00-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="e2d00-149">Excel Online lentē, kas atrodas cilnē **Ievietot**, grupā **Ilustrācijas** atlasiet **Attēls**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="e2d00-150">Atlasiet **Izvēlēties failu**, atrodiet attēlu, ko vēlaties pievienot, atlasiet to un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="e2d00-151">Atlasiet **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-151">Select **Insert**.</span></span>
4. <span data-ttu-id="e2d00-152">Pārvietojiet jauno attēlu, līdz tas ir pareizajā vietā.</span><span class="sxs-lookup"><span data-stu-id="e2d00-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="e2d00-153">Pēc noklusējuma Excel piešķir nosaukumu attēlam.</span><span class="sxs-lookup"><span data-stu-id="e2d00-153">By default, Excel names the picture.</span></span> <span data-ttu-id="e2d00-154">Piemēram, tas var piešķirt attēlam nosaukumu **Attēls 2**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="e2d00-155">Atlasiet **Atjaunināt struktūru**, lai sinhronizētu rediģējamās veidnes struktūru Excel un Finance.</span><span class="sxs-lookup"><span data-stu-id="e2d00-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="e2d00-156">Rūtī **Veidnes struktūra** izvērsiet **Pārskats \> Rēķins \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e2d00-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="e2d00-157">Ņemiet vērā, ka jaunais attēls tagad ir iekļauts Finance veidnes struktūrā kā krājums.</span><span class="sxs-lookup"><span data-stu-id="e2d00-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="e2d00-158">[![Biznesa dokumentu pārvaldības darbvietas izmantošana, lai pievienotu attēlu biznesa dokumenta veidnei](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="e2d00-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="e2d00-159">Saistītās saites</span><span class="sxs-lookup"><span data-stu-id="e2d00-159">Related links</span></span>

[<span data-ttu-id="e2d00-160">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="e2d00-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="e2d00-161">Biznesa dokumentu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="e2d00-161">Business document management overview</span></span>](er-business-document-management.md)
