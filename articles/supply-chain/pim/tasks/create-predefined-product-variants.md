---
title: Iepriekš definētu preces variantu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f78441445baecba279f96eb3935d9ebbb4ff03f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021912"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="e2ee2-103">Iepriekš definēts preces variants</span><span class="sxs-lookup"><span data-stu-id="e2ee2-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="e2ee2-104">Piemērs: Iepriekš definētu preces variantu izveide</span><span class="sxs-lookup"><span data-stu-id="e2ee2-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="e2ee2-105">Šajā piemērā parādīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e2ee2-106">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="e2ee2-106">Make demo data available</span></span>

<span data-ttu-id="e2ee2-107">Lai sekotu šim scenārijam, izmantojot šeit ieteiktās vērtības, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa *USMF* juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="e2ee2-108">1. darbība: Preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="e2ee2-108">Step 1: Create a product master</span></span>

<span data-ttu-id="e2ee2-109">Lai izveidotu preces šablonu:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-109">To create a product master:</span></span>

1. <span data-ttu-id="e2ee2-110">Pārejiet uz sadaļu **Preču informācijas pārvaldība > Preces > Preces šabloni**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="e2ee2-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-111">Select **New**.</span></span>
1. <span data-ttu-id="e2ee2-112">Ja laukā **Preces numurs** nav norādīts skaitlis, tad ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="e2ee2-113">Tas ir nepieciešams, ja šim laukam nav iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="e2ee2-114">Ievadiet nosaukumu laukā **Preces nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="e2ee2-115">Laukā **Preces dimensijas grupa** atlasiet preces dimensiju grupu *SizeCol* (Izmērs un Krāsa).</span><span class="sxs-lookup"><span data-stu-id="e2ee2-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="e2ee2-116">Atlasiet **Labi**, lai izveidotu un atvērtu jauno preces šablonu.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="e2ee2-117">2. darbība: Pievienot preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="e2ee2-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="e2ee2-118">Šajā piemērā parādīts, kā manuāli ievadīt preču dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="e2ee2-119">Jūs varat arī atlasīt izmēru, krāsu un stilu grupu, kurā ietilpst preces dimensiju vērtības, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="e2ee2-120">Lai pievienotu preces dimensijas:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-120">To add product dimensions:</span></span>

1. <span data-ttu-id="e2ee2-121">Kad jaunais preces šablons joprojām ir atvērts, darbību rūtī atlasiet **Preces dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="e2ee2-122">Atveriet cilni **Izmērs** un rīkjoslā atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="e2ee2-123">Jaunajai rindai veiciet šādus iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="e2ee2-124">**Izmērs:** atlasiet lieluma vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="e2ee2-125">**Nosaukums:** ievadiet elementa izmēru.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="e2ee2-126">Rīkjoslā atlasiet **Jauns** un pievienojiet režģim otru izmēru ar jaunu **Izmēru** un **Nosaukumu**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="e2ee2-127">Atveriet cilni **Krāsas** un rīkjoslā atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="e2ee2-128">Jaunajai rindai veiciet šādus iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="e2ee2-129">**Krāsa:** atlasiet krāsas vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="e2ee2-130">**Nosaukums:** ievadiet elementa krāsu.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="e2ee2-131">Rīkjoslā atlasiet **Jauns** un pievienojiet režģim otru krāsu ar jaunu **Krāsu** un **Nosaukumu**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="e2ee2-132">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-132">Select **Save**.</span></span>
1. <span data-ttu-id="e2ee2-133">Aizveriet lapu, lai atgrieztos pie jaunā preces šablona.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="e2ee2-134">3. darbība: Ģenerēt preces variantus</span><span class="sxs-lookup"><span data-stu-id="e2ee2-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="e2ee2-135">Šajā sadaļā ir aprakstīts, kā ģenerēt preču variantus, ja nav iespējots līdzeklis *Variantu ieteikumu lapas uzlabojumi*.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="e2ee2-136">Skatiet nākošo sadaļu, lai iegūtu detalizētu informāciju par to, kā izveidot preču variantus, kad šis līdzeklis ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="e2ee2-137">Lai ģenerētu preces variantus:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-137">To generate product variants:</span></span>

1. <span data-ttu-id="e2ee2-138">Kad jaunais preces šablons joprojām ir atvērts, darbību rūtī atlasiet **Preču vavianti**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="e2ee2-139">Darbību rūtī atlasiet **Variantu ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="e2ee2-140">Sistēma izveido sarakstu ar visām iespējamām produkta lielumu un krāsu kombinācijām.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="e2ee2-141">Atlasiet **Atlasīt visu** rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="e2ee2-142">Šajā piemērā atlasiet visus iespējamos variantus.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="e2ee2-143">Ja vēlaties izmantot tikai iespējamo preces dimensiju kombināciju apakškopu, atzīmējiet tikai nepieciešamās izvēles rūtiņas pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="e2ee2-144">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-144">Select **Create**.</span></span>
1. <span data-ttu-id="e2ee2-145">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="e2ee2-146">Uzlaboti variantu ieteikumi</span><span class="sxs-lookup"><span data-stu-id="e2ee2-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="e2ee2-147">Līdzeklis *Variantu ieteikumu lapas uzlabojumi* uzlabo lapu **Variantu ieteikumi**, lai novērstu veiktspējas un lietojamības problēmas uzņēmumiem, kuriem ir liels preču dimensiju kombināciju skaits.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="e2ee2-148">Uzlabotais produktu dimensiju vērtību atlases process, kuram ģenerēt varianta ieteikumus, ļauj ātrāk un vieglāk identificēt un atbrīvot attiecīgos produkta variantus.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="e2ee2-149">Šim līdzeklim ir pievienoti šādi uzlabojumi:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="e2ee2-150">**Variantu ieteikumu atliktā ģenerēšana:** atverot lapu **Variantu ieteikumi**, tajā vairs netiek rādīti ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="e2ee2-151">Tā vietā ir skaidri jāizvēlas, kuras vērtības būs nepieciešamas, un pēc tam jāatlasa poga **Ieteikt**, lai ģenerētu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="e2ee2-152">Tas padara procesu redzamu un interaktīvu.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="e2ee2-153">**Dimensiju vērtību atlase:** Ja jums ir daudz dimensiju vērtību, jūs parasti interesējaties par variantu ieteikumu ģenerēšanu, kas ietver tikai dažas no tām (piemēram, ieviešot jaunu krāsu vai stilu kopu).</span><span class="sxs-lookup"><span data-stu-id="e2ee2-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="e2ee2-154">Ar uzlaboto dizainu varat atlasīt dimensiju vērtības, kurām vēlaties ģenerēt preču variantu ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="e2ee2-155">Tas lielā veidā palielina ieteikto variantu atbilstību un uzlabo gan sistēmas veiktspēju, gan lietotāja produktivitāti.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="e2ee2-156">Ieslēgt lapas Variantu ieteikumi uzlabojumu līdzekli</span><span class="sxs-lookup"><span data-stu-id="e2ee2-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="e2ee2-157">Lai varētu izmantot līdzekli *Variantu ieteikumu lapas uzlabojumi*, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="e2ee2-158">Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e2ee2-159">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e2ee2-160">**Modulis:** *Preču informācijas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="e2ee2-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="e2ee2-161">**Līdzekļa nosaukums:** *Variantu ieteikumu lapas uzlabojumi*</span><span class="sxs-lookup"><span data-stu-id="e2ee2-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="e2ee2-162">Darbs ar uzlabotajiem variantu ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="e2ee2-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="e2ee2-163">Lai ģenerētu preču variantu ieteikumus, ja ir iespējots līdzeklis *Variantu ieteikumu lapas uzlabojumi*:</span><span class="sxs-lookup"><span data-stu-id="e2ee2-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="e2ee2-164">Atveriet vai izveidojiet preces šablonu un pievienojiet tam nepieciešamās preču dimensijas, kā aprakstīts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="e2ee2-165">Kad preces šablons ir atvērts, darbību rūtī atlasiet **Preču vavianti**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="e2ee2-166">Darbību rūtī atlasiet **Variantu ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="e2ee2-167">Atlasiet vērtības, kuras vēlaties lietot katrai dimensijai.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="e2ee2-168">Augšējā rīkjoslā atlasiet **Ieteikt**.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="e2ee2-169">Sistēma izveido sarakstu ar visām iespējamām atlasīto izmēru un krāsu kombinācijām.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="e2ee2-170">Kopsavilkuma cilnē **Ieteiktie varianti** atzīmējiet izvēles rūtiņu katrai preces dimensijas kombinācijai, ko vēlaties izmantot, vai rīkjoslā atlasiet **Atlasīt visu**, lai atlasītu visus no tiem.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="e2ee2-171">Atlasiet **Izveidot**, lai pašreizējam preces šablonam pievienotu variantus.</span><span class="sxs-lookup"><span data-stu-id="e2ee2-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
