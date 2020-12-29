---
title: Darbs ar iepriekš iestatītiem izkārtojumiem
description: Šajā tēmā ir aprakstīts, kā strādāt ar iepriekš iestatītiem izkārtojumiem programmā Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f31dfa1fdbb3732610748abe4a9de851033f2b89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414068"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="4e231-103">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="4e231-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4e231-104">Šajā tēmā ir aprakstīts, kā strādāt ar iepriekš iestatītiem izkārtojumiem programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e231-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4e231-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="4e231-105">Overview</span></span>

<span data-ttu-id="4e231-106">Pirms izpildāt šajā tēmā aprakstītās procedūras, pārliecinieties, ka esat izlasījis sadaļu [Iepriekš iestatītie un pielāgotie izkārtojumi](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="4e231-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="4e231-107">Vispārīgam pārskatam skatiet sadaļu [Veidnes un izkārtojumu pārskats](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4e231-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="4e231-108">Jauna iepriekš iestatīta izkārtojuma izveide</span><span class="sxs-lookup"><span data-stu-id="4e231-108">Create a new preset layout</span></span>

<span data-ttu-id="4e231-109">Iepriekš iestatīta izkārtojuma izveidošanai ir pieejamas divas metodes.</span><span class="sxs-lookup"><span data-stu-id="4e231-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="4e231-110">Varat saglabāt esošu pielāgotu izkārtojumu kā jaunu iepriekš iestatītu izkārtojumu vai arī izveidot iepriekš iestatītu izkārtojumu no jauna.</span><span class="sxs-lookup"><span data-stu-id="4e231-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="4e231-111">Iepriekš iestatīta izkārtojuma izveidošana no esoša pielāgota izkārtojuma</span><span class="sxs-lookup"><span data-stu-id="4e231-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="4e231-112">Lai izveidotu iepriekš iestatītu izkārtojumu no esoša pielāgota izkārtojuma, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4e231-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="4e231-113">Atveriet esošu lapu, kas pašlaik neizmanto iepriekš iestatītu izkārtojumu un kurai ir moduļa struktūra, ko vēlaties atkārtoti izmantot citām jūsu vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="4e231-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="4e231-114">Atlasiet **Rediģēt**, lai paņemtu lapu.</span><span class="sxs-lookup"><span data-stu-id="4e231-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="4e231-115">Atlasiet **Saglabāt kā jaunu izkārtojumu**.</span><span class="sxs-lookup"><span data-stu-id="4e231-115">Select **Save as new layout**.</span></span> <span data-ttu-id="4e231-116">Tiek parādīts dialoglodziņš **Saglabāt kā jaunu izkārtojumu**.</span><span class="sxs-lookup"><span data-stu-id="4e231-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="4e231-117">Ievadiet iepriekš iestatītā izkārtojuma nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="4e231-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="4e231-118">Vērtības, ko ievadāt, tiks rādītas citiem autoriem, kad tie izveido jaunas lapas no jūsu izkārtojuma vai pārslēdzas uz to.</span><span class="sxs-lookup"><span data-stu-id="4e231-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="4e231-119">Tāpēc ievadiet vērtības, kas noderēs lapu autoriem.</span><span class="sxs-lookup"><span data-stu-id="4e231-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="4e231-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4e231-120">Select **OK**.</span></span>

<span data-ttu-id="4e231-121">Iepriekš iestatītais izkārtojums tagad būs pieejams, veidojot jaunas lapas vai arī izvēloties citu izkārtojumu lapai tajā pašā veidnes hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="4e231-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="4e231-122">Lai ātri apskatītu, vai konkrēta lapa pašlaik ir saistīta ar iepriekš iestatītu izkārtojumu, atlasiet lapu no lapu saraksta skata un pārbaudiet izkārtojuma metadatus rekvizītu rūtī labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="4e231-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="4e231-123">Jauna iepriekš iestatīta izkārtojuma izveide</span><span class="sxs-lookup"><span data-stu-id="4e231-123">Create a new preset layout</span></span>

<span data-ttu-id="4e231-124">Lai izveidotu iepriekš iestatītu izkārtojumu no jauna, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4e231-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="4e231-125">Navigācijas rūtī kreisajā pusē atlasiet **Izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="4e231-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="4e231-126">Atlasiet **Jauns izkārtojums**.</span><span class="sxs-lookup"><span data-stu-id="4e231-126">Select **New Layout**.</span></span> <span data-ttu-id="4e231-127">Tiek parādīts dialoglodziņš **Jauns izkārtojums**.</span><span class="sxs-lookup"><span data-stu-id="4e231-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="4e231-128">Atlasiet veidni, ko izmantot iepriekš iestatītajam izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="4e231-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="4e231-129">Ievadiet iepriekš iestatītā izkārtojuma nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="4e231-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="4e231-130">Vērtības, ko ievadāt, tiks rādītas citiem autoriem, kad tie izveido jaunas lapas no jūsu izkārtojuma vai pārslēdzas uz to.</span><span class="sxs-lookup"><span data-stu-id="4e231-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="4e231-131">Tāpēc ievadiet vērtības, kas noderēs lapu autoriem.</span><span class="sxs-lookup"><span data-stu-id="4e231-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="4e231-132">Atlasiet **Labi**, lai izveidotu jaunu iepriekš iestatīto izkārtojumu un atvērtu izkārtojuma redaktoru.</span><span class="sxs-lookup"><span data-stu-id="4e231-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="4e231-133">Izkārtojuma redaktorā pievienojiet un konfigurējiet moduļus, izmantojot struktūras koku kreisajā pusē un rekvizītu rūti labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="4e231-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="4e231-134">(Šis process ir līdzīgs moduļu pievienošanas un konfigurēšanas procesam veidnes redaktorā.) Moduļu izkārtojums un visi bloķētie noklusējuma iestatījumi kļūst par centralizētu moduļa konfigurāciju visām lapām, kurās tiek izmantots šis iepriekš iestatītais izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="4e231-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="4e231-135">Iepriekš iestatīta izkārtojuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="4e231-135">Modify a preset layout</span></span>

<span data-ttu-id="4e231-136">Lai modificētu iepriekš iestatītu izkārtojumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4e231-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="4e231-137">Navigācijas rūtī kreisajā pusē atlasiet **Izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="4e231-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="4e231-138">Izkārtojuma redaktorā struktūras kokā pa kreisi atlasiet moduli, ko modificēt.</span><span class="sxs-lookup"><span data-stu-id="4e231-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="4e231-139">Pēc tam izpildiet jebkuru no norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="4e231-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="4e231-140">Lai moduli pārvietotu uz augšu vai uz leju, atlasiet daudzpunktes pogu (**...**) modulim un pēc tam atlasiet **Pārvietot uz augšu** vai **Pārvietot uz leju**.</span><span class="sxs-lookup"><span data-stu-id="4e231-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="4e231-141">Lai mainītu moduļa noklusējuma iestatījumus, izmantojiet rekvizītu rūti, lai ievadītu noklusējuma vērtības un pēc izvēles bloķētu tās visām pakārtotajām lapām.</span><span class="sxs-lookup"><span data-stu-id="4e231-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="4e231-142">Lai pievienotu jaunus moduļus vai fragmentus konteineru moduļiem, atlasiet daudzpunktes pogu un pēc tam atlasiet **Pievienot moduli** vai **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="4e231-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="4e231-143">Lai moduli noņemtu no izkārtojuma, atlasiet daudzpunktes pogu un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="4e231-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="4e231-144">Iepriekš iestatīta izkārtojuma dizaina maiņa</span><span class="sxs-lookup"><span data-stu-id="4e231-144">Change a preset layout theme</span></span>

<span data-ttu-id="4e231-145">Parasta prakse ir iestatīt noklusējuma dizainu visām lappusēm, kas izmanto iepriekš iestatītu izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="4e231-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="4e231-146">Lai iestatītu vai mainītu dizainu visām pakārtotajām lapām, kas izmanto jūsu iepriekš iestatīto izkārtojumu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="4e231-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="4e231-147">Izkārtojuma redaktorā struktūras kokā pa kreisi atlasiet lapas konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="4e231-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="4e231-148">(Parasti šis modulis ir otrais mezgls un ir nosaukts **Noklusējuma lapu**.)</span><span class="sxs-lookup"><span data-stu-id="4e231-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="4e231-149">Rekvizītu rūtī labajā pusē, lauka **Dizains** atlasiet dizainu.</span><span class="sxs-lookup"><span data-stu-id="4e231-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="4e231-150">Saglabājiet, atdodiet, priekšskatiet un publicējiet iepriekš iestatīto izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="4e231-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="4e231-151">Lai saglabātu un atdotu iepriekš iestatīto izkārtojumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4e231-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="4e231-152">Izkārtojuma redaktora augšā atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4e231-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="4e231-153">Saglabātās izmaiņas neietekmē lejupstraumes lapas, kamēr tās nav atdotas.</span><span class="sxs-lookup"><span data-stu-id="4e231-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="4e231-154">Atlasiet **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="4e231-154">Select **Finish editing**.</span></span> <span data-ttu-id="4e231-155">Jūsu veiktās izmaiņas tagad ir redzamas lejupstraumes darbplūsmām.</span><span class="sxs-lookup"><span data-stu-id="4e231-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="4e231-156">Lai priekšskatītu izmaiņas, vai nu atveriet esošu lapu, kas izmanto iepriekš iestatīto izkārtojumu, vai izveidojiet jaunu lapu no šī izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="4e231-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="4e231-157">Pēc tam, kad iepriekš iestatītā izkārtojuma izmaiņas ir priekšskatītas, veiciet vienu no tālāk norādītajām darbībām, lai publicētu izkārtojumu jūsu tiešsaistes vietnē.</span><span class="sxs-lookup"><span data-stu-id="4e231-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="4e231-158">Dodieties uz **Izkārtojumi**, atlasiet izkārtojumu un pēc tam atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="4e231-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="4e231-159">Atlasiet izkārtojuma nosaukumu, lai atvērtu izkārtojuma redaktoru, un tad atlasiet **Publlicēt**.</span><span class="sxs-lookup"><span data-stu-id="4e231-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="4e231-160">Publicējiet lapu, kurā ir atsauce uz nepublicēto izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="4e231-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="4e231-161">Izkārtojums tiks automātiski publicēts.</span><span class="sxs-lookup"><span data-stu-id="4e231-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="4e231-162">Uz iepriekš iestatītajiem izkārtojumiem var atsaukties vairākas lapas.</span><span class="sxs-lookup"><span data-stu-id="4e231-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="4e231-163">Publicējot iepriekš iestatītu izkārtojumu, ņemiet vērā, ka var tikt ietekmēts vairāku lappušu izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="4e231-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e231-164">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4e231-164">Additional resources</span></span>

[<span data-ttu-id="4e231-165">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="4e231-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="4e231-166">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="4e231-166">Work with templates</span></span>](work-with-templates.md)
