---
title: "Preces variantu numuru no nosaukumu nomenklatūra"
description: "Šajā tēmā ir aprakstīts, kā iestatīt preču numuru nomenklatūru, lai aizstātu fiksēto formātu [preces šablona numurs-konfigurācija-izmērs-krāsa-stils]. Jaunajai nomenklatūrai ir mērķim pielāgots formāts, kurā ir ietverts preces šablona numurs, aktīvās preces dimensijas un jūsu izvēles teksta atdalītāji. Varat arī izveidot preču nosaukumu nomenklatūru. Varat arī izveidot nomenklatūru, lai norādītu konfigurācijas, kas ir izveidotas, izmantojot ierobežojumiem atbilstošo preču konfiguratoru. Šajās nomenklatūrās var būt jūsu izvēlētie atribūti."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: db01d26376ec3ca6997b1ad2cb62e7b3ecc4b330
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="74bce-107">Preces variantu numuru no nosaukumu nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="74bce-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="74bce-108">Šajā tēmā ir aprakstīts, kā iestatīt preču numuru nomenklatūru, lai aizstātu fiksēto formātu [preces šablona numurs-konfigurācija-izmērs-krāsa-stils].</span><span class="sxs-lookup"><span data-stu-id="74bce-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="74bce-109">Jaunajai nomenklatūrai ir mērķim pielāgots formāts, kurā ir ietverts preces šablona numurs, aktīvās preces dimensijas un jūsu izvēles teksta atdalītāji.</span><span class="sxs-lookup"><span data-stu-id="74bce-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="74bce-110">Varat arī izveidot preču nosaukumu nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="74bce-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="74bce-111">Varat arī izveidot nomenklatūru, lai norādītu konfigurācijas, kas ir izveidotas, izmantojot ierobežojumiem atbilstošo preču konfiguratoru.</span><span class="sxs-lookup"><span data-stu-id="74bce-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="74bce-112">Šajās nomenklatūrās var būt jūsu izvēlētie atribūti.</span><span class="sxs-lookup"><span data-stu-id="74bce-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="74bce-113">Jaunās preces variantu numuru un preces variantu nosaukumu nomenklatūras sniedz iespēju iekļaut segmentus preces variantu identifikatoros.</span><span class="sxs-lookup"><span data-stu-id="74bce-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="74bce-114">Šajos segmentos var būt ietverts preces šablona numurs un nosaukums, preces dimensijas ID un nosaukums, numuru sērijas, teksta konstantes un atribūti.</span><span class="sxs-lookup"><span data-stu-id="74bce-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="74bce-115">Šī funkcija sniedz iespēju ātri atrast noteiktu preces variantu, kad veidojat pārdošanas pasūtījumu vai pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="74bce-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="74bce-116">Gan preces variantu numuru, gan preces variantu nosaukumu nomenklatūras varat izveidot, izmantojot lapu **Preču nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="74bce-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="74bce-117">Lai atvērtu šo lapu, noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="74bce-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="74bce-118">Iepriekš definētu preces variantu nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="74bce-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="74bce-119">Preces varianti tiek ģenerēti preces šabloniem saskaņā ar vienu no trim konfigurācijas tehnoloģijām:</span><span class="sxs-lookup"><span data-stu-id="74bce-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="74bce-120">Iepriekš definēti varianti</span><span class="sxs-lookup"><span data-stu-id="74bce-120">Predefined variants</span></span>
-   <span data-ttu-id="74bce-121">Atbilstoši ierobežojumam</span><span class="sxs-lookup"><span data-stu-id="74bce-121">Constraint-based</span></span>
-   <span data-ttu-id="74bce-122">Atbilstoši dimensijai</span><span class="sxs-lookup"><span data-stu-id="74bce-122">Dimension-based</span></span>

<span data-ttu-id="74bce-123">Katram preces variantam ir numurs un nosaukums, un preces variantu identifikācijas nomenklatūras sniedz iespēju atlasīt segmentus, kas ir jāiekļauj katrā preces varianta numurā vai nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="74bce-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="74bce-124">Lapā **Preču nomenklatūra** varat atlasīt tālāk norādīto segmentus.</span><span class="sxs-lookup"><span data-stu-id="74bce-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="74bce-125">Preces šablona numurs</span><span class="sxs-lookup"><span data-stu-id="74bce-125">Product master number</span></span>
-   <span data-ttu-id="74bce-126">Preces šablona nosaukums</span><span class="sxs-lookup"><span data-stu-id="74bce-126">Product master name</span></span>
-   <span data-ttu-id="74bce-127">Numuru sērijas vērtība</span><span class="sxs-lookup"><span data-stu-id="74bce-127">Number sequence value</span></span>
-   <span data-ttu-id="74bce-128">Teksta konstante</span><span class="sxs-lookup"><span data-stu-id="74bce-128">Text constant</span></span>
-   <span data-ttu-id="74bce-129">Preces dimensijas</span><span class="sxs-lookup"><span data-stu-id="74bce-129">Product dimensions</span></span>
    -   <span data-ttu-id="74bce-130">Konfigurācijas ID vai nosaukums</span><span class="sxs-lookup"><span data-stu-id="74bce-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="74bce-131">Krāsas ID vai nosaukums</span><span class="sxs-lookup"><span data-stu-id="74bce-131">Color ID or name</span></span>
    -   <span data-ttu-id="74bce-132">Izmēra ID vai nosaukums</span><span class="sxs-lookup"><span data-stu-id="74bce-132">Size ID or name</span></span>
    -   <span data-ttu-id="74bce-133">Stila ID vai nosaukums</span><span class="sxs-lookup"><span data-stu-id="74bce-133">Style ID or name</span></span>

<span data-ttu-id="74bce-134">Pēc preces variantu identifikācijas numuru nomenklatūras definēšanas varat to saistīt ar preces dimensiju grupu.</span><span class="sxs-lookup"><span data-stu-id="74bce-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="74bce-135">Pēc tam visiem preču šabloniem, kuros ir ietvertas atsauces uz šo preces dimensiju grupu, tiek piešķirti preces variantu numuri atbilstoši šai nomenklatūrai.</span><span class="sxs-lookup"><span data-stu-id="74bce-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="74bce-136">Taču preces variantu nosaukumu nomenklatūras nevar saistīt ar preces dimensiju grupām.</span><span class="sxs-lookup"><span data-stu-id="74bce-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="74bce-137">Preces variantu identifikācijas nomenklatūru var arī tiešā veidā saistīt ar preces šablonu.</span><span class="sxs-lookup"><span data-stu-id="74bce-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="74bce-138">Šādā gadījumā ar preces šablonu saistītajiem preces variantiem tiek piešķirti preces variantu numuri un nosaukumi atbilstoši nomenklatūrām.</span><span class="sxs-lookup"><span data-stu-id="74bce-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="74bce-139">Paraugs</span><span class="sxs-lookup"><span data-stu-id="74bce-139">Example</span></span>

<span data-ttu-id="74bce-140">Tiek ražoti trīs izmēru (S, M, L), četru krāsu (sarkans, zaļš, zils, dzeltens) un divu stilu (polo, V) t-krekli (TS1234).</span><span class="sxs-lookup"><span data-stu-id="74bce-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="74bce-141">Tāpēc ir iespējami 24 preces varianti (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="74bce-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="74bce-142">Jūs izveidojat preces variantu numuru nomenklatūru ar tālāk norādītajiem segmentiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="74bce-143">Preces šablona numurs</span><span class="sxs-lookup"><span data-stu-id="74bce-143">Product master number</span></span>
2.  <span data-ttu-id="74bce-144">Teksta konstante: “-”</span><span class="sxs-lookup"><span data-stu-id="74bce-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="74bce-145">krāsa</span><span class="sxs-lookup"><span data-stu-id="74bce-145">Color</span></span>
4.  <span data-ttu-id="74bce-146">Teksta konstante: “-”</span><span class="sxs-lookup"><span data-stu-id="74bce-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="74bce-147">izmērs</span><span class="sxs-lookup"><span data-stu-id="74bce-147">Size</span></span>
6.  <span data-ttu-id="74bce-148">Teksta konstante: “-”</span><span class="sxs-lookup"><span data-stu-id="74bce-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="74bce-149">Stils</span><span class="sxs-lookup"><span data-stu-id="74bce-149">Style</span></span>

<span data-ttu-id="74bce-150">Šādā gadījumā sarkana, maza, polo stila t-krekla preces varianta numurs ir TS1234-sarkans-mazs-polo</span><span class="sxs-lookup"><span data-stu-id="74bce-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="74bce-151">Ierobežojumiem atbilstošu konfigurāciju nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="74bce-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="74bce-152">Ierobežojumiem atbilstošu konfigurāciju gadījumā varat izvedot īpašu nomenklatūru, kas ir paredzēta konfigurācijas preces dimensijai.</span><span class="sxs-lookup"><span data-stu-id="74bce-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="74bce-153">Lapā **Preču nomenklatūra** varat atlasīt tālāk norādīto segmentus.</span><span class="sxs-lookup"><span data-stu-id="74bce-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="74bce-154">Numuru sērijas vērtība</span><span class="sxs-lookup"><span data-stu-id="74bce-154">Number sequence value</span></span>
-   <span data-ttu-id="74bce-155">Teksta konstante</span><span class="sxs-lookup"><span data-stu-id="74bce-155">Text constant</span></span>
-   <span data-ttu-id="74bce-156">Atribūta vērtība</span><span class="sxs-lookup"><span data-stu-id="74bce-156">Attribute value</span></span>

<span data-ttu-id="74bce-157">Katram komponentam preču konfigurācijas modelī var būt sava konfigurāciju nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="74bce-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="74bce-158">Var izmantot tikai komponenta atribūtus.</span><span class="sxs-lookup"><span data-stu-id="74bce-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="74bce-159">Apakškomponentu vai lietotāju prasību atribūtus nevar izmantot.</span><span class="sxs-lookup"><span data-stu-id="74bce-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="74bce-160">Paraugs</span><span class="sxs-lookup"><span data-stu-id="74bce-160">Example</span></span>

<span data-ttu-id="74bce-161">Preces konfigurācijas modelim ir saknes komponents ar diviem tālāk norādītajiem atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="74bce-162">Materiāls (plastmasa, koks, tērauds)</span><span class="sxs-lookup"><span data-stu-id="74bce-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="74bce-163">Garums (10...100)</span><span class="sxs-lookup"><span data-stu-id="74bce-163">Length (10...100)</span></span>

<span data-ttu-id="74bce-164">Jūs izveidojat konfigurāciju nomenklatūru ar tālāk norādītajiem segmentiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="74bce-165">Atribūta vērtība: Materiāls</span><span class="sxs-lookup"><span data-stu-id="74bce-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="74bce-166">Teksta konstante: “AAA”</span><span class="sxs-lookup"><span data-stu-id="74bce-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="74bce-167">Atribūta vērtība: Garums</span><span class="sxs-lookup"><span data-stu-id="74bce-167">Attribute value: Length</span></span>

<span data-ttu-id="74bce-168">Šādā gadījumā koka materiāla, kura garums ir 78, konfigurācijas ID ir WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="74bce-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="74bce-169">Dimensijām atbilstošu konfigurāciju nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="74bce-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="74bce-170">Dimensijām atbilstošu konfigurāciju gadījumā varat izvedot īpašu nomenklatūru, kas ir paredzēta konfigurācijas preces dimensijai.</span><span class="sxs-lookup"><span data-stu-id="74bce-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="74bce-171">Lapā **Preču nomenklatūra** varat atlasīt tālāk norādīto segmentus.</span><span class="sxs-lookup"><span data-stu-id="74bce-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="74bce-172">Numuru sērijas vērtība</span><span class="sxs-lookup"><span data-stu-id="74bce-172">Number sequence value</span></span>
-   <span data-ttu-id="74bce-173">Teksta konstante</span><span class="sxs-lookup"><span data-stu-id="74bce-173">Text constant</span></span>
-   <span data-ttu-id="74bce-174">Konfigurācijas grupas krājums</span><span class="sxs-lookup"><span data-stu-id="74bce-174">Configuration group item</span></span>

<span data-ttu-id="74bce-175">Varat definēt materiālu komplekta (MK) konfigurāciju nomenklatūru.</span><span class="sxs-lookup"><span data-stu-id="74bce-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="74bce-176">Paraugs</span><span class="sxs-lookup"><span data-stu-id="74bce-176">Example</span></span>

<span data-ttu-id="74bce-177">MK ir iekļautas četras MK rindas, kas ir sadalītas divās konfigurāciju grupās.</span><span class="sxs-lookup"><span data-stu-id="74bce-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="74bce-178">MK rinda: M0007, Standarta korpuss</span><span class="sxs-lookup"><span data-stu-id="74bce-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="74bce-179">Konfigurācijas grupa: Korpuss</span><span class="sxs-lookup"><span data-stu-id="74bce-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="74bce-180">MK rinda: M0008, Augstas kvalitātes korpuss</span><span class="sxs-lookup"><span data-stu-id="74bce-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="74bce-181">Konfigurācijas grupa: Korpuss</span><span class="sxs-lookup"><span data-stu-id="74bce-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="74bce-182">MK rinda: M0021, Auduma priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="74bce-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="74bce-183">Konfigurācijas grupa: Priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="74bce-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="74bce-184">MK rinda: M0022, Metāla priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="74bce-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="74bce-185">Konfigurācijas grupa: Priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="74bce-185">Configuration group: Front grill</span></span>

<span data-ttu-id="74bce-186">Jūs izveidojat konfigurāciju nomenklatūru ar tālāk norādītajiem segmentiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="74bce-187">Konfigurācijas grupa: Korpuss</span><span class="sxs-lookup"><span data-stu-id="74bce-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="74bce-188">Teksta konstante: “&”</span><span class="sxs-lookup"><span data-stu-id="74bce-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="74bce-189">Konfigurācijas grupa: Priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="74bce-189">Configuration group: Front grill</span></span>

<span data-ttu-id="74bce-190">Šādā gadījumā ar auduma priekšējo režģi aprīkota standarta korpusa konfigurācijas ID ir M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="74bce-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="74bce-191">Preces variantu un konfigurāciju kombinācijas nomenklatūra</span><span class="sxs-lookup"><span data-stu-id="74bce-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="74bce-192">Ja preces šablona preces variantu konfigurēšanai izmantojat ierobežojumiem vai dimensijām atbilstošās konfigurācijas tehnoloģiju, preces variantu numuros var tikt ietverta konfigurācijas dimensijas nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="74bce-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="74bce-193">Lai konfigurētu variantus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="74bce-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="74bce-194">Lapā **Preču nomenklatūra** definējiet preces variantu numuru nomenklatūru, kurā ir ietverta konfigurācijas dimensija.</span><span class="sxs-lookup"><span data-stu-id="74bce-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="74bce-195">Piešķiriet nomenklatūru preces dimensiju grupai, kurā ir ietverta konfigurācijas dimensija.</span><span class="sxs-lookup"><span data-stu-id="74bce-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="74bce-196">Definējiet konfigurāciju nomenklatūru komponentiem vai MK, kas tiks izmantoti preces variantu konfigurēšanai.</span><span class="sxs-lookup"><span data-stu-id="74bce-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="74bce-197">Varat arī izveidot preču nosaukumu nomenklatūras.</span><span class="sxs-lookup"><span data-stu-id="74bce-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="74bce-198">Preces variantu nosaukumus var konfigurēt tā, lai tajos tiktu ietverts konfigurācijas ID vai nosaukums.</span><span class="sxs-lookup"><span data-stu-id="74bce-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="74bce-199">Ierobežojumiem atbilstošu konfigurāciju piemērs</span><span class="sxs-lookup"><span data-stu-id="74bce-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="74bce-200">Šī piemēra ietvaros tiek izmantota preces variantu numuru nomenklatūra, kas sastāv no tālāk norādītajiem segmentiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="74bce-201">Preces šablona numurs</span><span class="sxs-lookup"><span data-stu-id="74bce-201">Product master number</span></span>
2.  <span data-ttu-id="74bce-202">Teksta konstante: “\_”</span><span class="sxs-lookup"><span data-stu-id="74bce-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="74bce-203">Konfigurācija</span><span class="sxs-lookup"><span data-stu-id="74bce-203">Configuration</span></span>

<span data-ttu-id="74bce-204">Konfigurāciju nomenklatūra sastāv no tālāk norādītajiem segmentiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="74bce-205">Atribūta vērtība: Materiāls</span><span class="sxs-lookup"><span data-stu-id="74bce-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="74bce-206">Teksta konstante: “AAA”</span><span class="sxs-lookup"><span data-stu-id="74bce-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="74bce-207">Atribūta vērtība: Garums</span><span class="sxs-lookup"><span data-stu-id="74bce-207">Attribute value: Length</span></span>

<span data-ttu-id="74bce-208">Jūs ievadāt šādas segmentu vērtības.</span><span class="sxs-lookup"><span data-stu-id="74bce-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="74bce-209">Preces šablona numurs = **M0099**</span><span class="sxs-lookup"><span data-stu-id="74bce-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="74bce-210">Materiāls = **Plastmasa**</span><span class="sxs-lookup"><span data-stu-id="74bce-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="74bce-211">Garums = **12**</span><span class="sxs-lookup"><span data-stu-id="74bce-211">Length = **12**</span></span>

<span data-ttu-id="74bce-212">Šādā gadījumā preces varianta numurs ir M0099\_PlastmasaAAA12.</span><span class="sxs-lookup"><span data-stu-id="74bce-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="74bce-213">Dimensijām atbilstošu konfigurāciju piemērs</span><span class="sxs-lookup"><span data-stu-id="74bce-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="74bce-214">Šī piemēra ietvaros tiek izmantota preces variantu numuru nomenklatūra, kas sastāv no tālāk norādītajiem segmentiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="74bce-215">Preces šablona numurs</span><span class="sxs-lookup"><span data-stu-id="74bce-215">Product master number</span></span>
2.  <span data-ttu-id="74bce-216">Teksta konstante: “//”</span><span class="sxs-lookup"><span data-stu-id="74bce-216">Text constant "//"</span></span>
3.  <span data-ttu-id="74bce-217">Konfigurācija</span><span class="sxs-lookup"><span data-stu-id="74bce-217">Configuration</span></span>

<span data-ttu-id="74bce-218">Konfigurāciju nomenklatūra sastāv no tālāk norādītajiem segmentiem.</span><span class="sxs-lookup"><span data-stu-id="74bce-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="74bce-219">Konfigurācijas grupa: Korpuss</span><span class="sxs-lookup"><span data-stu-id="74bce-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="74bce-220">Teksta konstante: “&”</span><span class="sxs-lookup"><span data-stu-id="74bce-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="74bce-221">Konfigurācijas grupa: Priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="74bce-221">Configuration group: Front grill</span></span>

<span data-ttu-id="74bce-222">Jūs ievadāt šādas segmentu vērtības.</span><span class="sxs-lookup"><span data-stu-id="74bce-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="74bce-223">Preces šablona numurs = **D0123**</span><span class="sxs-lookup"><span data-stu-id="74bce-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="74bce-224">Korpuss = **M0008**</span><span class="sxs-lookup"><span data-stu-id="74bce-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="74bce-225">Priekšējais režģis = **M0022**</span><span class="sxs-lookup"><span data-stu-id="74bce-225">Front grill = **M0022**</span></span>

<span data-ttu-id="74bce-226">Šādā gadījumā preces varianta numurs ir D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="74bce-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="74bce-227">Numerācijas konflikti</span><span class="sxs-lookup"><span data-stu-id="74bce-227">Numbering conflicts</span></span>
<span data-ttu-id="74bce-228">Dažos gadījumos iestatītā preces variantu numuru nomenklatūra var nenodrošināt unikālus preces variantu numurus.</span><span class="sxs-lookup"><span data-stu-id="74bce-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="74bce-229">Piemēram, preces variantu numuri nav unikāli, ja preces šablonam tiek izmantota iepriekš definēta variantu konfigurēšanas tehnoloģija un šī šablona nomenklatūrā nav ietverta viena aktīva preces dimensija.</span><span class="sxs-lookup"><span data-stu-id="74bce-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="74bce-230">Konfliktu novēršanas veids ir atkarīgs no konfigurēšanas tehnoloģijas.</span><span class="sxs-lookup"><span data-stu-id="74bce-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="74bce-231">Iepriekš definēti varianti</span><span class="sxs-lookup"><span data-stu-id="74bce-231">Predefined variants</span></span>

<span data-ttu-id="74bce-232">Ja mēģināt manuāli izveidot vai automātiski ģenerēt preces variantus un vairākiem preces variantiem tiek piešķirts viens un tas pats preces varianta numurs, rodas kļūda.</span><span class="sxs-lookup"><span data-stu-id="74bce-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="74bce-233">Lai to nepieļautu, ir jāizmanto visas preces dimensijas grupā ietvertās aktīvās preces dimensijas.</span><span class="sxs-lookup"><span data-stu-id="74bce-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="74bce-234">Varat arī ietvert numuru sēriju, lai palīdzētu nodrošināt, ka preces variantu numuri ir unikāli.</span><span class="sxs-lookup"><span data-stu-id="74bce-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="74bce-235">Konfigurācijas atbilstoši ierobežojumam</span><span class="sxs-lookup"><span data-stu-id="74bce-235">Constraint-based configurations</span></span>

<span data-ttu-id="74bce-236">Atkarībā no nomenklatūras sistēma var tikt mēģināts piešķirt konfigurācijai preces varianta numuru, kas nav unikāls.</span><span class="sxs-lookup"><span data-stu-id="74bce-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="74bce-237">Šajā gadījumā sistēmā preces varianta numura vietā tiek izmantota konfigurācijas dimensijas numuru sērija un tiek parādīts brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="74bce-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="74bce-238">Lai to nepieļautu, nomenklatūrā ir jāietver pietiekami daudz atribūtu, kas nodrošina, ka preces variantu numuri ir unikāli.</span><span class="sxs-lookup"><span data-stu-id="74bce-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="74bce-239">Ir arī jāpārliecinās, ka komponentam ir ieslēgta opcija **Atkārtoti izmantot**.</span><span class="sxs-lookup"><span data-stu-id="74bce-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="74bce-240">Konfigurācijas atbilstoši dimensijām</span><span class="sxs-lookup"><span data-stu-id="74bce-240">Dimension-based configurations</span></span>

<span data-ttu-id="74bce-241">Vienas konfigurācijas procesa darbības laikā sistēmā tiek ieteikta konfigurācijas vērtību atbilstoši nomenklatūrai.</span><span class="sxs-lookup"><span data-stu-id="74bce-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="74bce-242">Šajā darbībā varat manuāli mainīt konfigurācijas vērtību.</span><span class="sxs-lookup"><span data-stu-id="74bce-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="74bce-243">Saglabājot konfigurāciju, sistēmā tiek pārbaudīts, vai konfigurācijas vērtība ir unikāla.</span><span class="sxs-lookup"><span data-stu-id="74bce-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="74bce-244">Ja ievadītā vērtība nav unikāla, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="74bce-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="74bce-245">Lai saglabātu konfigurāciju, ir jāievada unikāla konfigurācijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="74bce-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="74bce-246">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="74bce-246">See also</span></span>
--------

[<span data-ttu-id="74bce-247">Preces variantu nomenklatūras izveide iepriekš definētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="74bce-247">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="74bce-248">Preces variantu nomenklatūras izveide konfigurētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="74bce-248">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


