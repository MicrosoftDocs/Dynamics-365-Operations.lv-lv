---
title: Preces dimensijas
description: 'Pastāv četras preču dimensijas: Krāsa, Konfigurācija, Izmērs un Stils. Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem. Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti.'
author: cvocph
manager: tfehr
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5e9b10fa18ada9534ce5e279d4f1f09973a802b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208436"
---
# <a name="product-dimensions"></a><span data-ttu-id="3da20-105">Preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="3da20-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3da20-106">Pastāv četras preču dimensijas: Krāsa, Konfigurācija, Izmērs un Stils.</span><span class="sxs-lookup"><span data-stu-id="3da20-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="3da20-107">Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem.</span><span class="sxs-lookup"><span data-stu-id="3da20-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="3da20-108">Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti.</span><span class="sxs-lookup"><span data-stu-id="3da20-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="3da20-109">Preču dimensijas ir īpašības, ko izmanto, lai identificētu preces variantu.</span><span class="sxs-lookup"><span data-stu-id="3da20-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="3da20-110">Preču variantu definēšanai vai izmantot preču dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="3da20-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="3da20-111">Lai izveidotu preces variantu, ir jādefinē vismaz viena preces dimensija preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="3da20-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>

## <a name="product-variants"></a><span data-ttu-id="3da20-112">Preces varianti</span><span class="sxs-lookup"><span data-stu-id="3da20-112">Product variants</span></span>

<span data-ttu-id="3da20-113">Preču varianti tiek saukti arī par krājumiem.</span><span class="sxs-lookup"><span data-stu-id="3da20-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="3da20-114">Krājums ir materiāla prece, kas nav tāds pats kā pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="3da20-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="3da20-115">Var arī definēt preces šablonu, kura veids ir Pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="3da20-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="3da20-116">Izmantojot tipu Pakalpojums, varat norādīt preču variantus, kas ietver pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="3da20-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="3da20-117">Piemēram, var norādīt preces šablonu konsultāciju darbam un preču variantus darbam, ko veic vecākie konsultanti un jaunākie konsultanti.</span><span class="sxs-lookup"><span data-stu-id="3da20-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="3da20-118">Preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="3da20-118">Product dimensions</span></span>
<span data-ttu-id="3da20-119">Ir pieejamas šādas preču dimensijas: Konfigurācija, Krāsa, Izmērs un Stils.</span><span class="sxs-lookup"><span data-stu-id="3da20-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="3da20-120">Pamatojoties uz preces dimensijas vērtībām, var ģenerēt preces variantu.</span><span class="sxs-lookup"><span data-stu-id="3da20-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="3da20-121">Tādu preču dimensiju kā Izmērs, Krāsa un Stils vērtības var izveidot lapās **Izmērs**, **Krāsa** un **Stils**, kam var piekļūt šajās vietās: **Preču informācijas pārvaldība** &gt; **Iestatījumi** &gt; **Dimensiju un variantu grupas** &gt; **Izmēri/Krāsas/Stili**.</span><span class="sxs-lookup"><span data-stu-id="3da20-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="3da20-122">Preces dimensijas Konfigurācija vērtības parasti tiek izveidotas, izmantojot preču konfiguratoru vai dimensiju konfiguratoru.</span><span class="sxs-lookup"><span data-stu-id="3da20-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="3da20-123">Preces dimensijas var izveidot un uzturēt arī lapā **Preces dimensijas**, kam var piekļūt tālāk norādītajās vietās.</span><span class="sxs-lookup"><span data-stu-id="3da20-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="3da20-124">Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Preces** &gt; **Preču šabloni**.</span><span class="sxs-lookup"><span data-stu-id="3da20-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="3da20-125">**Darbību rūtī** noklikšķiniet uz **Preču dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="3da20-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3da20-126">Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Preces** &gt; **Visas preces un preču šabloni**.</span><span class="sxs-lookup"><span data-stu-id="3da20-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="3da20-127">Atlasiet preces šablonu.</span><span class="sxs-lookup"><span data-stu-id="3da20-127">Select a product master.</span></span> <span data-ttu-id="3da20-128">**Darbību rūtī** noklikšķiniet uz **Preču dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="3da20-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3da20-129">Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="3da20-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="3da20-130">Atlasiet preces šablonu.</span><span class="sxs-lookup"><span data-stu-id="3da20-130">Select a product master.</span></span> <span data-ttu-id="3da20-131">**Darbību rūtī** noklikšķiniet uz**Prece**.</span><span class="sxs-lookup"><span data-stu-id="3da20-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="3da20-132">Grupā **Preces šablons** noklikšķiniet uz **Preces dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="3da20-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="3da20-133">Krājumam izveidojamo variantu skaitu ierobežo iespējamo preču dimensiju kombināciju skaits.</span><span class="sxs-lookup"><span data-stu-id="3da20-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="3da20-134">**Padoms**</span><span class="sxs-lookup"><span data-stu-id="3da20-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da20-135">Ja izmantojat preci, piemēram, pasūtījuma rindā, izvēlieties preču dimensijas, lai norādītu preces variantu, ar ko vēlaties strādāt.</span><span class="sxs-lookup"><span data-stu-id="3da20-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="3da20-136">Paraugs</span><span class="sxs-lookup"><span data-stu-id="3da20-136">Example</span></span>
<span data-ttu-id="3da20-137">Uzņēmums pārdod džinsus.</span><span class="sxs-lookup"><span data-stu-id="3da20-137">A company sells denim jeans.</span></span> <span data-ttu-id="3da20-138">Krājumam Džinsi tiek izmantotas preces dimensijas Krāsa un Izmērs.</span><span class="sxs-lookup"><span data-stu-id="3da20-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="3da20-139">Džinsi tiek pārdoti trīs dažādās krāsas un sešos dažādos izmēros.</span><span class="sxs-lookup"><span data-stu-id="3da20-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="3da20-140">Krāsas: zila, melna, brūna. Izmēri: XS, S, M, L, XL, XXL. Noteikti izmēti nav pieejami visās trīs krāsās.</span><span class="sxs-lookup"><span data-stu-id="3da20-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="3da20-141">Ja būtu pieejamas visas kombinācijas, tā rezultātā būtu 18 dažādi džinsu veidi.</span><span class="sxs-lookup"><span data-stu-id="3da20-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="3da20-142">Šajā piemērā tiek iegūtas tikai šādas deviņās preču variantu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="3da20-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="3da20-143">Krāsa</span><span class="sxs-lookup"><span data-stu-id="3da20-143">Color</span></span> | <span data-ttu-id="3da20-144">Izmēri</span><span class="sxs-lookup"><span data-stu-id="3da20-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="3da20-145">Zila</span><span class="sxs-lookup"><span data-stu-id="3da20-145">Blue</span></span>  | <span data-ttu-id="3da20-146">XS</span><span class="sxs-lookup"><span data-stu-id="3da20-146">XS</span></span>   |
| <span data-ttu-id="3da20-147">Zila</span><span class="sxs-lookup"><span data-stu-id="3da20-147">Blue</span></span>  | <span data-ttu-id="3da20-148">S</span><span class="sxs-lookup"><span data-stu-id="3da20-148">S</span></span>    |
| <span data-ttu-id="3da20-149">Zila</span><span class="sxs-lookup"><span data-stu-id="3da20-149">Blue</span></span>  | <span data-ttu-id="3da20-150">P</span><span class="sxs-lookup"><span data-stu-id="3da20-150">M</span></span>    |
| <span data-ttu-id="3da20-151">melna</span><span class="sxs-lookup"><span data-stu-id="3da20-151">Black</span></span> | <span data-ttu-id="3da20-152">P</span><span class="sxs-lookup"><span data-stu-id="3da20-152">M</span></span>    |
| <span data-ttu-id="3da20-153">melna</span><span class="sxs-lookup"><span data-stu-id="3da20-153">Black</span></span> | <span data-ttu-id="3da20-154">L</span><span class="sxs-lookup"><span data-stu-id="3da20-154">L</span></span>    |
| <span data-ttu-id="3da20-155">melna</span><span class="sxs-lookup"><span data-stu-id="3da20-155">Black</span></span> | <span data-ttu-id="3da20-156">XL</span><span class="sxs-lookup"><span data-stu-id="3da20-156">XL</span></span>   |
| <span data-ttu-id="3da20-157">brūna</span><span class="sxs-lookup"><span data-stu-id="3da20-157">Brown</span></span> | <span data-ttu-id="3da20-158">L</span><span class="sxs-lookup"><span data-stu-id="3da20-158">L</span></span>    |
| <span data-ttu-id="3da20-159">brūna</span><span class="sxs-lookup"><span data-stu-id="3da20-159">Brown</span></span> | <span data-ttu-id="3da20-160">XL</span><span class="sxs-lookup"><span data-stu-id="3da20-160">XL</span></span>   |
| <span data-ttu-id="3da20-161">brūna</span><span class="sxs-lookup"><span data-stu-id="3da20-161">Brown</span></span> | <span data-ttu-id="3da20-162">XXL</span><span class="sxs-lookup"><span data-stu-id="3da20-162">XXL</span></span>  |





