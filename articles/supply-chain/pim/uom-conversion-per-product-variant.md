---
title: Mērvienību pārveidošana katram preces variantam
description: Šajā tēmā ir paskaidrots, kā var iestatīt mērvienību pārveidošanu preču variantiem.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935103"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="25681-103">Mērvienību pārveidošana katram preces variantam</span><span class="sxs-lookup"><span data-stu-id="25681-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25681-104">Šajā tēmā ir paskaidrots, kā var iestatīt mērvienību pārveidošanu preču variantiem.</span><span class="sxs-lookup"><span data-stu-id="25681-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="25681-105">Tajā ir ietverts iestatīšanas piemērs.</span><span class="sxs-lookup"><span data-stu-id="25681-105">It includes an example of the setup.</span></span>

<span data-ttu-id="25681-106">Šis līdzeklis ļauj uzņēmumiem definēt dažādu mērvienību pārveidošanu tās pašas preces variantiem.</span><span class="sxs-lookup"><span data-stu-id="25681-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="25681-107">Šajā tēmā ir izmantots tālāk minētais piemērs.</span><span class="sxs-lookup"><span data-stu-id="25681-107">The following example is used in this topic.</span></span> <span data-ttu-id="25681-108">Uzņēmums pārdod T-kreklus šādos izmēros: mazs, vidējs, liels un īpaši liels.</span><span class="sxs-lookup"><span data-stu-id="25681-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="25681-109">T-krekls ir definēts kā prece, un dažādi izmēri ir definēti kā preces varianti.</span><span class="sxs-lookup"><span data-stu-id="25681-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="25681-110">T-krekli tiek iepakoti kastēs, un katrā kastē var būt pieci T-krekli, izņemot īpaši liela izmēra izstrādājumus, kuru gadījumā kastē pietiek vietas tikai četriem T-krekliem.</span><span class="sxs-lookup"><span data-stu-id="25681-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="25681-111">Uzņēmums vēlas izsekot dažādiem T-kreklu variantiem, izmantojot mērvienību **Gabali**, bet pārdod tos, izmantojot mērvienību **Kastes**.</span><span class="sxs-lookup"><span data-stu-id="25681-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="25681-112">Pārveidojot no krājuma uzskaites vienībām uz pārdošanas vienībām, 1 kaste = 5 gabali, izņemot īpaši liela izmēra variantu, kura gadījumā 1 kaste = 4 gabali.</span><span class="sxs-lookup"><span data-stu-id="25681-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="25681-113">Iestatīt preci mērvienību pārveidošanai katram variantam</span><span class="sxs-lookup"><span data-stu-id="25681-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="25681-114">Preces variantus var izveidot tikai precēm, kurām atlasīts šāds iestatījums **Preces apakštips**: **Preces šablons**.</span><span class="sxs-lookup"><span data-stu-id="25681-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="25681-115">Papildinformāciju skatiet sadaļā [Preces šablona izveide](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="25681-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="25681-116">Līdzeklis nav iespējots precēm, kas ir iestatītas pieļaujamā svara procesiem.</span><span class="sxs-lookup"><span data-stu-id="25681-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="25681-117">Kad ir izveidots preces šablons ar izlaistajiem preču variantiem, var iestatīt mērvienību pārveidošanu katram variantam.</span><span class="sxs-lookup"><span data-stu-id="25681-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="25681-118">Izvēlnes vienumu, lai atvērtu mērvienību pārveidošanas lapu preces vai preces varianta kontekstā, var atrast šādās lapās.</span><span class="sxs-lookup"><span data-stu-id="25681-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="25681-119">Lapa **Informācija par preci**</span><span class="sxs-lookup"><span data-stu-id="25681-119">**Product details** page</span></span>
-   <span data-ttu-id="25681-120">Lapa **Informācija par izlaistajām precēm**</span><span class="sxs-lookup"><span data-stu-id="25681-120">**Released products details** page</span></span>
-   <span data-ttu-id="25681-121">Lapa **Izlaisto preču varianti**</span><span class="sxs-lookup"><span data-stu-id="25681-121">**Released product variants** page</span></span>

<span data-ttu-id="25681-122">Atverot lapu **Mērvienību pārveidošana** preces šablona vai izlaistās preces varianta kontekstā, var izvēlēties, vai vēlaties iestatīt mērvienības pārveidošanu precei vai preces variantam.</span><span class="sxs-lookup"><span data-stu-id="25681-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="25681-123">To var paveikt, atlasot vienumu **Preces variants** vai **Prece** laukā **Izveidot pārveidošanu šim:**.</span><span class="sxs-lookup"><span data-stu-id="25681-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="25681-124">Preces variants</span><span class="sxs-lookup"><span data-stu-id="25681-124">Product variant</span></span>

<span data-ttu-id="25681-125">Atlasot **Preces variants**, pēc tam var atlasīt, kuram variantam vēlaties iestatīt mērvienību pārveidošanu laukā **Preces variants**.</span><span class="sxs-lookup"><span data-stu-id="25681-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="25681-126">Prece</span><span class="sxs-lookup"><span data-stu-id="25681-126">Product</span></span>

<span data-ttu-id="25681-127">Atlasot **Prece**, pēc tam varat iestatīt mērvienību pārveidošanu preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="25681-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="25681-128">Šī mērvienību pārveidošana tiks lietota visiem preces variantiem, kuriem nav noteikta mērvienību pārveidošana.</span><span class="sxs-lookup"><span data-stu-id="25681-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="25681-129">Paraugs</span><span class="sxs-lookup"><span data-stu-id="25681-129">Example</span></span>

<span data-ttu-id="25681-130">Preces šablonam **T-krekls** ir četri izlaisti preces varianti: mazs, vidējs, liels un īpaši liels.</span><span class="sxs-lookup"><span data-stu-id="25681-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="25681-131">T-krekli tiek iepakoti kastēs, un katrā kastē var būt pieci T-krekli, izņemot īpaši liela izmēra izstrādājumus, kuru gadījumā kastē pietiek vietas tikai četriem T-krekliem.</span><span class="sxs-lookup"><span data-stu-id="25681-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="25681-132">Vispirms atveriet lapu **Mērvienību pārveidošana** no lapas Informācija par izlaistajām precēm attiecīgajam **T-kreklam.**</span><span class="sxs-lookup"><span data-stu-id="25681-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="25681-133">Lapā **Mērvienību pārveidošana** iestatiet mērvienības konvertēšanu šādam izlaistajam preces variantam: īpaši liels.</span><span class="sxs-lookup"><span data-stu-id="25681-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="25681-134">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="25681-134">**Field**</span></span>             | <span data-ttu-id="25681-135">**Iestatījums**</span><span class="sxs-lookup"><span data-stu-id="25681-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="25681-136">Izveidot konvertēšanu šim:</span><span class="sxs-lookup"><span data-stu-id="25681-136">Create conversion for</span></span> | <span data-ttu-id="25681-137">Preces variants</span><span class="sxs-lookup"><span data-stu-id="25681-137">Product variant</span></span>         |
| <span data-ttu-id="25681-138">Preces variants</span><span class="sxs-lookup"><span data-stu-id="25681-138">Product variant</span></span>       | <span data-ttu-id="25681-139">T-krekls : : Īpaši liels : :</span><span class="sxs-lookup"><span data-stu-id="25681-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="25681-140">No vienības</span><span class="sxs-lookup"><span data-stu-id="25681-140">From unit</span></span>             | <span data-ttu-id="25681-141">Kastes</span><span class="sxs-lookup"><span data-stu-id="25681-141">Boxes</span></span>                   |
| <span data-ttu-id="25681-142">Koeficients</span><span class="sxs-lookup"><span data-stu-id="25681-142">Factor</span></span>                | <span data-ttu-id="25681-143">4.</span><span class="sxs-lookup"><span data-stu-id="25681-143">4</span></span>                       |
| <span data-ttu-id="25681-144">Uz vienību</span><span class="sxs-lookup"><span data-stu-id="25681-144">To Unit</span></span>               | <span data-ttu-id="25681-145">Gabali</span><span class="sxs-lookup"><span data-stu-id="25681-145">Pieces</span></span>                  |

<span data-ttu-id="25681-146">Izlaistajiem preces variantiem Mazs, Vidējs un Liels ir tāda pati mērvienību pārveidošana starp vienību Kaste un Gabali, līdz ar to šiem preces variantiem var definēt mērvienību pārveidošanu preces šablonā.</span><span class="sxs-lookup"><span data-stu-id="25681-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="25681-147">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="25681-147">**Field**</span></span>             | <span data-ttu-id="25681-148">**Iestatījums**</span><span class="sxs-lookup"><span data-stu-id="25681-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="25681-149">Izveidot konvertēšanu šim:</span><span class="sxs-lookup"><span data-stu-id="25681-149">Create conversion for</span></span> | <span data-ttu-id="25681-150">Prece</span><span class="sxs-lookup"><span data-stu-id="25681-150">Product</span></span>     |
| <span data-ttu-id="25681-151">Prece</span><span class="sxs-lookup"><span data-stu-id="25681-151">Product</span></span>               | <span data-ttu-id="25681-152">T-krekls</span><span class="sxs-lookup"><span data-stu-id="25681-152">T-Shirt</span></span>     |
| <span data-ttu-id="25681-153">No vienības</span><span class="sxs-lookup"><span data-stu-id="25681-153">From unit</span></span>             | <span data-ttu-id="25681-154">Kastes</span><span class="sxs-lookup"><span data-stu-id="25681-154">Boxes</span></span>       |
| <span data-ttu-id="25681-155">Koeficients</span><span class="sxs-lookup"><span data-stu-id="25681-155">Factor</span></span>                | <span data-ttu-id="25681-156">5.</span><span class="sxs-lookup"><span data-stu-id="25681-156">5</span></span>           |
| <span data-ttu-id="25681-157">Uz vienību</span><span class="sxs-lookup"><span data-stu-id="25681-157">To Unit</span></span>               | <span data-ttu-id="25681-158">Gabali</span><span class="sxs-lookup"><span data-stu-id="25681-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="25681-159">Programmas Excel izmantošana, lai atjauninātu mērvienību pārveidošanu</span><span class="sxs-lookup"><span data-stu-id="25681-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="25681-160">Ja precei ir daudz preces variantu ar dažādām mērvienību pārveidošanām, ieteicams eksportēt mērvienību pārveidošanas no lapas **Mērvienību pārveidošana** uz Excel izklājlapu, atjaunināt pārveidošanas un pēc tam publicēt tās atpakaļ programmatūrā Supply Chain Mangement.</span><span class="sxs-lookup"><span data-stu-id="25681-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="25681-161">Opciju eksportēt uz programmu Excel un publicēt rediģētās vērtības atpakaļ programmatūrā Supply Chain Mangement iespējo, izmantojot vienumu izvēlnē **Atvērt, izmantojot Microsoft Office** lapas **Mērvienību pārveidošana** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="25681-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
