---
title: Mērvienību pārveidošana katram preces variantam
description: Šajā tēmā ir paskaidrots, kā var iestatīt mērvienību pārveidošanu preču variantiem.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: a47f705976b7a5b34492294e28aa8cd47ea38825
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/22/2019
ms.locfileid: "345931"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="c53ab-103">Mērvienību pārveidošana katram preces variantam</span><span class="sxs-lookup"><span data-stu-id="c53ab-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="c53ab-104">Šajā tēmā ir paskaidrots, kā var iestatīt mērvienību pārveidošanu preču variantiem.</span><span class="sxs-lookup"><span data-stu-id="c53ab-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="c53ab-105">Tajā ir ietverts iestatīšanas piemērs.</span><span class="sxs-lookup"><span data-stu-id="c53ab-105">It includes an example of the setup.</span></span>

<span data-ttu-id="c53ab-106">Šis līdzeklis ļauj uzņēmumiem definēt dažādu mērvienību pārveidošanu tās pašas preces variantiem.</span><span class="sxs-lookup"><span data-stu-id="c53ab-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="c53ab-107">Šajā tēmā ir izmantots tālāk minētais piemērs.</span><span class="sxs-lookup"><span data-stu-id="c53ab-107">The following example is used in this topic.</span></span> <span data-ttu-id="c53ab-108">Uzņēmums pārdod T-kreklus šādos izmēros: mazs, vidējs, liels un īpaši liels.</span><span class="sxs-lookup"><span data-stu-id="c53ab-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="c53ab-109">T-krekls ir definēts kā prece, un dažādi izmēri ir definēti kā preces varianti.</span><span class="sxs-lookup"><span data-stu-id="c53ab-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="c53ab-110">T-krekli tiek iepakoti kastēs, un katrā kastē var būt pieci T-krekli, izņemot īpaši liela izmēra izstrādājumus, kuru gadījumā kastē pietiek vietas tikai četriem T-krekliem.</span><span class="sxs-lookup"><span data-stu-id="c53ab-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="c53ab-111">Uzņēmums vēlas izsekot dažādiem T-kreklu variantiem, izmantojot mērvienību **Gabali**, bet pārdod tos, izmantojot mērvienību **Kastes**.</span><span class="sxs-lookup"><span data-stu-id="c53ab-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="c53ab-112">Pārveidojot no krājuma uzskaites vienībām uz pārdošanas vienībām, 1 kaste = 5 gabali, izņemot īpaši liela izmēra variantu, kura gadījumā 1 kaste = 4 gabali.</span><span class="sxs-lookup"><span data-stu-id="c53ab-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="c53ab-113">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="c53ab-113">Setup</span></span>

<span data-ttu-id="c53ab-114">Var konfigurēt parametrus, lai izmantotu šo līdzekli precēm, kurām ir iespējots iestatījums **Visi procesi**, vai tikai precei, kurai ir iespējots iestatījums **Noliktavas procesi**, izmantojot opciju **Iespējot mērvienību pārveidošanu** lapā **Preces informācijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="c53ab-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="c53ab-115">Iestatīt preci mērvienību pārveidošanai katram variantam</span><span class="sxs-lookup"><span data-stu-id="c53ab-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="c53ab-116">Preces variantus var izveidot tikai precēm, kurām atlasīts šāds iestatījums **Preces apakštips**: **Preces šablons**.</span><span class="sxs-lookup"><span data-stu-id="c53ab-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="c53ab-117">Papildinformāciju skatiet sadaļā [Preces šablona izveide](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="c53ab-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="c53ab-118">Līdzeklis nav iespējots precēm, kas ir iestatītas pieļaujamā svara procesiem.</span><span class="sxs-lookup"><span data-stu-id="c53ab-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="c53ab-119">Preces šablona izveides laikā iespējojiet mērvienības pārveidošanu, izmantojot opciju **Iespējot mērvienību pārveidošanu** lapā **Papildinformācija par preci**.</span><span class="sxs-lookup"><span data-stu-id="c53ab-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="c53ab-120">Kad ir izveidots preces šablons ar izlaistajiem preču variantiem, var iestatīt mērvienību pārveidošanu katram variantam.</span><span class="sxs-lookup"><span data-stu-id="c53ab-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="c53ab-121">Izvēlnes vienumu, lai atvērtu mērvienību pārveidošanas lapu preces vai preces varianta kontekstā, var atrast šādās lapās.</span><span class="sxs-lookup"><span data-stu-id="c53ab-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="c53ab-122">Lapa **Informācija par preci**</span><span class="sxs-lookup"><span data-stu-id="c53ab-122">**Product details** page</span></span>
-   <span data-ttu-id="c53ab-123">Lapa **Informācija par izlaistajām precēm**</span><span class="sxs-lookup"><span data-stu-id="c53ab-123">**Released products details** page</span></span>
-   <span data-ttu-id="c53ab-124">Lapa **Izlaisto preču varianti**</span><span class="sxs-lookup"><span data-stu-id="c53ab-124">**Released product variants** page</span></span>

<span data-ttu-id="c53ab-125">Atverot lapu **Mērvienību pārveidošana** preces šablona vai izlaistās preces varianta kontekstā, var izvēlēties, vai vēlaties iestatīt mērvienības pārveidošanu precei vai preces variantam.</span><span class="sxs-lookup"><span data-stu-id="c53ab-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="c53ab-126">To var paveikt, atlasot vienumu **Preces variants** vai **Prece** laukā **Izveidot pārveidošanu šim:**.</span><span class="sxs-lookup"><span data-stu-id="c53ab-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="c53ab-127">Preces variants</span><span class="sxs-lookup"><span data-stu-id="c53ab-127">Product variant</span></span>

<span data-ttu-id="c53ab-128">Atlasot **Preces variants**, pēc tam var atlasīt, kuram variantam vēlaties iestatīt mērvienību pārveidošanu laukā **Preces variants**.</span><span class="sxs-lookup"><span data-stu-id="c53ab-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="c53ab-129">Prece</span><span class="sxs-lookup"><span data-stu-id="c53ab-129">Product</span></span>

<span data-ttu-id="c53ab-130">Atlasot **Prece**, pēc tam varat iestatīt mērvienību pārveidošanu preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="c53ab-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="c53ab-131">Šī mērvienību pārveidošana tiks lietota visiem preces variantiem, kuriem nav noteikta mērvienību pārveidošana.</span><span class="sxs-lookup"><span data-stu-id="c53ab-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="c53ab-132">Paraugs</span><span class="sxs-lookup"><span data-stu-id="c53ab-132">Example</span></span>

<span data-ttu-id="c53ab-133">Preces šablonam **T-krekls** ir četri izlaisti preces varianti: mazs, vidējs, liels un īpaši liels.</span><span class="sxs-lookup"><span data-stu-id="c53ab-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="c53ab-134">T-krekli tiek iepakoti kastēs, un katrā kastē var būt pieci T-krekli, izņemot īpaši liela izmēra izstrādājumus, kuru gadījumā kastē pietiek vietas tikai četriem T-krekliem.</span><span class="sxs-lookup"><span data-stu-id="c53ab-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="c53ab-135">Vispirms atveriet lapu **Mērvienību pārveidošana** no lapas Informācija par izlaistajām precēm attiecīgajam **T-kreklam.**</span><span class="sxs-lookup"><span data-stu-id="c53ab-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="c53ab-136">Lapā **Mērvienību pārveidošana** iestatiet mērvienības konvertēšanu šādam izlaistajam preces variantam: īpaši liels.</span><span class="sxs-lookup"><span data-stu-id="c53ab-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="c53ab-137">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="c53ab-137">**Field**</span></span>             | <span data-ttu-id="c53ab-138">**Iestatījums**</span><span class="sxs-lookup"><span data-stu-id="c53ab-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="c53ab-139">Izveidot konvertēšanu šim:</span><span class="sxs-lookup"><span data-stu-id="c53ab-139">Create conversion for</span></span> | <span data-ttu-id="c53ab-140">Preces variants</span><span class="sxs-lookup"><span data-stu-id="c53ab-140">Product variant</span></span>         |
| <span data-ttu-id="c53ab-141">Preces variants</span><span class="sxs-lookup"><span data-stu-id="c53ab-141">Product variant</span></span>       | <span data-ttu-id="c53ab-142">T-krekls : : Īpaši liels : :</span><span class="sxs-lookup"><span data-stu-id="c53ab-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="c53ab-143">No vienības</span><span class="sxs-lookup"><span data-stu-id="c53ab-143">From unit</span></span>             | <span data-ttu-id="c53ab-144">Kastes</span><span class="sxs-lookup"><span data-stu-id="c53ab-144">Boxes</span></span>                   |
| <span data-ttu-id="c53ab-145">Koeficients</span><span class="sxs-lookup"><span data-stu-id="c53ab-145">Factor</span></span>                | <span data-ttu-id="c53ab-146">4.</span><span class="sxs-lookup"><span data-stu-id="c53ab-146">4</span></span>                       |
| <span data-ttu-id="c53ab-147">Uz vienību</span><span class="sxs-lookup"><span data-stu-id="c53ab-147">To Unit</span></span>               | <span data-ttu-id="c53ab-148">Gabali</span><span class="sxs-lookup"><span data-stu-id="c53ab-148">Pieces</span></span>                  |

<span data-ttu-id="c53ab-149">Izlaistajiem preces variantiem Mazs, Vidējs un Liels ir tāda pati mērvienību pārveidošana starp vienību Kaste un Gabali, līdz ar to šiem preces variantiem var definēt mērvienību pārveidošanu preces šablonā.</span><span class="sxs-lookup"><span data-stu-id="c53ab-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="c53ab-150">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="c53ab-150">**Field**</span></span>             | <span data-ttu-id="c53ab-151">**Iestatījums**</span><span class="sxs-lookup"><span data-stu-id="c53ab-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c53ab-152">Izveidot konvertēšanu šim:</span><span class="sxs-lookup"><span data-stu-id="c53ab-152">Create conversion for</span></span> | <span data-ttu-id="c53ab-153">Prece</span><span class="sxs-lookup"><span data-stu-id="c53ab-153">Product</span></span>     |
| <span data-ttu-id="c53ab-154">Prece</span><span class="sxs-lookup"><span data-stu-id="c53ab-154">Product</span></span>               | <span data-ttu-id="c53ab-155">T-krekls</span><span class="sxs-lookup"><span data-stu-id="c53ab-155">T-Shirt</span></span>     |
| <span data-ttu-id="c53ab-156">No vienības</span><span class="sxs-lookup"><span data-stu-id="c53ab-156">From unit</span></span>             | <span data-ttu-id="c53ab-157">Kastes</span><span class="sxs-lookup"><span data-stu-id="c53ab-157">Boxes</span></span>       |
| <span data-ttu-id="c53ab-158">Koeficients</span><span class="sxs-lookup"><span data-stu-id="c53ab-158">Factor</span></span>                | <span data-ttu-id="c53ab-159">5.</span><span class="sxs-lookup"><span data-stu-id="c53ab-159">5</span></span>           |
| <span data-ttu-id="c53ab-160">Uz vienību</span><span class="sxs-lookup"><span data-stu-id="c53ab-160">To Unit</span></span>               | <span data-ttu-id="c53ab-161">Gabali</span><span class="sxs-lookup"><span data-stu-id="c53ab-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="c53ab-162">Programmas Excel izmantošana, lai atjauninātu mērvienību pārveidošanu</span><span class="sxs-lookup"><span data-stu-id="c53ab-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="c53ab-163">Ja precei ir daudz preces variantu ar dažādām mērvienību pārveidošanām, ieteicams eksportēt mērvienību pārveidošanas no lapas **Mērvienību pārveidošana** uz Excel izklājlapu, atjaunināt pārveidošanas un pēc tam publicēt tās atpakaļ programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c53ab-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="c53ab-164">Opciju eksportēt uz programmu Excel un publicēt rediģētās vērtības atpakaļ programmā Finance and Operations iespējo, izmantojot vienumu izvēlnē **Atvērt, izmantojot Microsoft Office** lapas **Mērvienību pārveidošana** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="c53ab-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
