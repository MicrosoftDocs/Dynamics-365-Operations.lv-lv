---
title: Iepriekš definētu preces variantu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.
author: t-benebo
manager: tfehr
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
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938206"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="d974f-103">Iepriekš definēts preces variants</span><span class="sxs-lookup"><span data-stu-id="d974f-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="d974f-104">Piemērs: Iepriekš definētu preces variantu izveide</span><span class="sxs-lookup"><span data-stu-id="d974f-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="d974f-105">Šajā piemērā parādīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="d974f-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="d974f-106">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="d974f-106">Make demo data available</span></span>

<span data-ttu-id="d974f-107">Lai sekotu šim scenārijam, izmantojot šeit ieteiktās vērtības, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa *USMF* juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="d974f-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="d974f-108">1. darbība: Preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="d974f-108">Step 1: Create a product master</span></span>

<span data-ttu-id="d974f-109">Lai izveidotu preces šablonu:</span><span class="sxs-lookup"><span data-stu-id="d974f-109">To create a product master:</span></span>

1. <span data-ttu-id="d974f-110">Pārejiet uz sadaļu **Preču informācijas pārvaldība > Preces > Preces šabloni**.</span><span class="sxs-lookup"><span data-stu-id="d974f-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="d974f-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d974f-111">Select **New**.</span></span>
1. <span data-ttu-id="d974f-112">Ja laukā **Preces numurs** nav norādīts skaitlis, tad ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d974f-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="d974f-113">Tas ir nepieciešams, ja šim laukam nav iestatīta numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="d974f-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="d974f-114">Ievadiet nosaukumu laukā **Preces nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="d974f-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="d974f-115">Laukā **Preces dimensijas grupa** atlasiet preces dimensiju grupu *SizeCol* (Izmērs un Krāsa).</span><span class="sxs-lookup"><span data-stu-id="d974f-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="d974f-116">Atlasiet **Labi**, lai izveidotu un atvērtu jauno preces šablonu.</span><span class="sxs-lookup"><span data-stu-id="d974f-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="d974f-117">2. darbība: Pievienot preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="d974f-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="d974f-118">Šajā piemērā parādīts, kā manuāli ievadīt preču dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d974f-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="d974f-119">Jūs varat arī atlasīt izmēru, krāsu un stilu grupu, kurā ietilpst preces dimensiju vērtības, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="d974f-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="d974f-120">Lai pievienotu preces dimensijas:</span><span class="sxs-lookup"><span data-stu-id="d974f-120">To add product dimensions:</span></span>

1. <span data-ttu-id="d974f-121">Kad jaunais preces šablons joprojām ir atvērts, darbību rūtī atlasiet **Preces dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="d974f-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="d974f-122">Atveriet cilni **Izmērs** un rīkjoslā atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="d974f-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="d974f-123">Jaunajai rindai veiciet šādus iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="d974f-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="d974f-124">**Izmērs:** atlasiet lieluma vērtību.</span><span class="sxs-lookup"><span data-stu-id="d974f-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="d974f-125">**Nosaukums:** ievadiet elementa izmēru.</span><span class="sxs-lookup"><span data-stu-id="d974f-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="d974f-126">Rīkjoslā atlasiet **Jauns** un pievienojiet režģim otru izmēru ar jaunu **Izmēru** un **Nosaukumu**.</span><span class="sxs-lookup"><span data-stu-id="d974f-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="d974f-127">Atveriet cilni **Krāsas** un rīkjoslā atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="d974f-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="d974f-128">Jaunajai rindai veiciet šādus iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="d974f-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="d974f-129">**Krāsa:** atlasiet krāsas vērtību.</span><span class="sxs-lookup"><span data-stu-id="d974f-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="d974f-130">**Nosaukums:** ievadiet elementa krāsu.</span><span class="sxs-lookup"><span data-stu-id="d974f-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="d974f-131">Rīkjoslā atlasiet **Jauns** un pievienojiet režģim otru krāsu ar jaunu **Krāsu** un **Nosaukumu**.</span><span class="sxs-lookup"><span data-stu-id="d974f-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="d974f-132">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d974f-132">Select **Save**.</span></span>
1. <span data-ttu-id="d974f-133">Aizveriet lapu, lai atgrieztos pie jaunā preces šablona.</span><span class="sxs-lookup"><span data-stu-id="d974f-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="d974f-134">3. darbība: Ģenerēt preces variantus</span><span class="sxs-lookup"><span data-stu-id="d974f-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="d974f-135">Šajā sadaļā ir aprakstīts, kā ģenerēt preču variantus, ja nav iespējots līdzeklis *Variantu ieteikumu lapas uzlabojumi*.</span><span class="sxs-lookup"><span data-stu-id="d974f-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="d974f-136">Skatiet nākošo sadaļu, lai iegūtu detalizētu informāciju par to, kā izveidot preču variantus, kad šis līdzeklis ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="d974f-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="d974f-137">Lai ģenerētu preces variantus:</span><span class="sxs-lookup"><span data-stu-id="d974f-137">To generate product variants:</span></span>

1. <span data-ttu-id="d974f-138">Kad jaunais preces šablons joprojām ir atvērts, darbību rūtī atlasiet **Preču vavianti**.</span><span class="sxs-lookup"><span data-stu-id="d974f-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="d974f-139">Darbību rūtī atlasiet **Variantu ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="d974f-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="d974f-140">Sistēma izveido sarakstu ar visām iespējamām produkta lielumu un krāsu kombinācijām.</span><span class="sxs-lookup"><span data-stu-id="d974f-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="d974f-141">Atlasiet **Atlasīt visu** rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="d974f-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="d974f-142">Šajā piemērā atlasiet visus iespējamos variantus.</span><span class="sxs-lookup"><span data-stu-id="d974f-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="d974f-143">Ja vēlaties izmantot tikai iespējamo preces dimensiju kombināciju apakškopu, atzīmējiet tikai nepieciešamās izvēles rūtiņas pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="d974f-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="d974f-144">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="d974f-144">Select **Create**.</span></span>
1. <span data-ttu-id="d974f-145">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d974f-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="d974f-146">Uzlaboti variantu ieteikumi</span><span class="sxs-lookup"><span data-stu-id="d974f-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="d974f-147">Līdzeklis *Variantu ieteikumu lapas uzlabojumi* uzlabo lapu **Variantu ieteikumi**, lai novērstu veiktspējas un lietojamības problēmas uzņēmumiem, kuriem ir liels preču dimensiju kombināciju skaits.</span><span class="sxs-lookup"><span data-stu-id="d974f-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="d974f-148">Uzlabotais produktu dimensiju vērtību atlases process, kuram ģenerēt varianta ieteikumus, ļauj ātrāk un vieglāk identificēt un atbrīvot attiecīgos produkta variantus.</span><span class="sxs-lookup"><span data-stu-id="d974f-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="d974f-149">Šim līdzeklim ir pievienoti šādi uzlabojumi:</span><span class="sxs-lookup"><span data-stu-id="d974f-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="d974f-150">**Variantu ieteikumu atliktā ģenerēšana:** atverot lapu **Variantu ieteikumi**, tajā vairs netiek rādīti ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="d974f-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="d974f-151">Tā vietā ir skaidri jāizvēlas, kuras vērtības būs nepieciešamas, un pēc tam jāatlasa poga **Ieteikt**, lai ģenerētu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="d974f-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="d974f-152">Tas padara procesu redzamu un interaktīvu.</span><span class="sxs-lookup"><span data-stu-id="d974f-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="d974f-153">**Dimensiju vērtību atlase:** Ja jums ir daudz dimensiju vērtību, jūs parasti interesējaties par variantu ieteikumu ģenerēšanu, kas ietver tikai dažas no tām (piemēram, ieviešot jaunu krāsu vai stilu kopu).</span><span class="sxs-lookup"><span data-stu-id="d974f-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="d974f-154">Ar uzlaboto dizainu varat atlasīt dimensiju vērtības, kurām vēlaties ģenerēt preču variantu ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="d974f-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="d974f-155">Tas lielā veidā palielina ieteikto variantu atbilstību un uzlabo gan sistēmas veiktspēju, gan lietotāja produktivitāti.</span><span class="sxs-lookup"><span data-stu-id="d974f-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="d974f-156">Ieslēgt lapas Variantu ieteikumi uzlabojumu līdzekli</span><span class="sxs-lookup"><span data-stu-id="d974f-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="d974f-157">Lai varētu izmantot līdzekli *Variantu ieteikumu lapas uzlabojumi*, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d974f-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="d974f-158">Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="d974f-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d974f-159">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="d974f-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d974f-160">**Modulis:** *Preču informācijas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="d974f-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="d974f-161">**Līdzekļa nosaukums:** *Variantu ieteikumu lapas uzlabojumi*</span><span class="sxs-lookup"><span data-stu-id="d974f-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="d974f-162">Darbs ar uzlabotajiem variantu ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="d974f-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="d974f-163">Lai ģenerētu preču variantu ieteikumus, ja ir iespējots līdzeklis *Variantu ieteikumu lapas uzlabojumi*:</span><span class="sxs-lookup"><span data-stu-id="d974f-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="d974f-164">Atveriet vai izveidojiet preces šablonu un pievienojiet tam nepieciešamās preču dimensijas, kā aprakstīts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="d974f-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="d974f-165">Kad preces šablons ir atvērts, darbību rūtī atlasiet **Preču vavianti**.</span><span class="sxs-lookup"><span data-stu-id="d974f-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="d974f-166">Darbību rūtī atlasiet **Variantu ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="d974f-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="d974f-167">Atlasiet vērtības, kuras vēlaties lietot katrai dimensijai.</span><span class="sxs-lookup"><span data-stu-id="d974f-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="d974f-168">Augšējā rīkjoslā atlasiet **Ieteikt**.</span><span class="sxs-lookup"><span data-stu-id="d974f-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="d974f-169">Sistēma izveido sarakstu ar visām iespējamām atlasīto izmēru un krāsu kombinācijām.</span><span class="sxs-lookup"><span data-stu-id="d974f-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="d974f-170">Kopsavilkuma cilnē **Ieteiktie varianti** atzīmējiet izvēles rūtiņu katrai preces dimensijas kombinācijai, ko vēlaties izmantot, vai rīkjoslā atlasiet **Atlasīt visu**, lai atlasītu visus no tiem.</span><span class="sxs-lookup"><span data-stu-id="d974f-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="d974f-171">Atlasiet **Izveidot**, lai pašreizējam preces šablonam pievienotu variantus.</span><span class="sxs-lookup"><span data-stu-id="d974f-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
