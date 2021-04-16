---
title: Mērvienību konvertēšana katram preces variantam
description: Šajā tēmā ir paskaidrots, kā iestatīt mērvienību pārveidošanu preču variantiem. Tajā ir ietverts iestatīšanas piemērs.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: eaa20f9a8f145fa8d44bfe77cc85f4dc565c2d27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841507"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="763f4-104">Mērvienību konvertēšana katram preces variantam</span><span class="sxs-lookup"><span data-stu-id="763f4-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="763f4-105">Šajā tēmā ir paskaidrots, kā iestatīt mērvienību pārveidošanu dažādiem preču variantiem.</span><span class="sxs-lookup"><span data-stu-id="763f4-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="763f4-106">Tā vietā, lai izveidotu vairākus atsevišķus produktus, kas jāsaglabā, varat izmantot preces variantus, lai izveidotu viena produkta variantus.</span><span class="sxs-lookup"><span data-stu-id="763f4-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="763f4-107">Piemēram, preces variants varētu būt konkrēta izmēra un krāsas T-krekls.</span><span class="sxs-lookup"><span data-stu-id="763f4-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="763f4-108">Iepriekš mērvienību pārveidošanu varēja iestatīt tikai preču šablonā.</span><span class="sxs-lookup"><span data-stu-id="763f4-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="763f4-109">Tādēļ visiem preces variantiem bija vienādi vienību pārveidošanas noteikumi.</span><span class="sxs-lookup"><span data-stu-id="763f4-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="763f4-110">Tomēr, ja ir ieslēgta *Preces variantu mērvienību pārveidošana* funkcija, ja T-krekli tiek pārdoti kastēs un to T-kreklu skaits, ko var iepakot kastē, ir atkarīgs no T-kreklu izmēra, tagad varat iestatīt mērvienību pārveidošanu starp dažādiem krekla izmēriem un kastēm, kas tiek izmantoti iepakošanai.</span><span class="sxs-lookup"><span data-stu-id="763f4-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="763f4-111">Līdzekļa ieslēgšana sistēmā</span><span class="sxs-lookup"><span data-stu-id="763f4-111">Turn on the feature in your system</span></span>

<span data-ttu-id="763f4-112">Ja jūsu sistēmā šis līdzeklis nav redzams, dodieties uz [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Preces variantu mērvienību pārveidošana* funkcijai.</span><span class="sxs-lookup"><span data-stu-id="763f4-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="763f4-113">Iestatīt preci mērvienību pārveidošanai katram variantam</span><span class="sxs-lookup"><span data-stu-id="763f4-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="763f4-114">Preces variantus var izveidot tikai precēm, kuras ir preču šabloni.</span><span class="sxs-lookup"><span data-stu-id="763f4-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="763f4-115">Papildinformāciju skatiet sadaļā [Preces šablona izveide](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="763f4-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="763f4-116">Līdzeklis *Preces variantu mērvienību pārveidošana* nav pieejama precēm, kas iestatītas noslodzes procesiem.</span><span class="sxs-lookup"><span data-stu-id="763f4-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="763f4-117">Lai konfigurētu preces šablonu, lai atbalstītu mērvienību pārveidošanu katram variantam, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="763f4-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="763f4-118">Dodieties uz **Preču informācijas pārvaldība \> Produkts \> Preces šabloni**.</span><span class="sxs-lookup"><span data-stu-id="763f4-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="763f4-119">Izveidojiet vai atveriet preces šablonu, lai dotos uz tā **Produkta informācijas** lapu.</span><span class="sxs-lookup"><span data-stu-id="763f4-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="763f4-120">Iestatiet opciju **Iespējot mērvienību pārveidošanu** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="763f4-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="763f4-121">Darbību rūtī cilnē **Prece** grupā **Iestatīt**, atlasiet **Mērvienību pārveidošana**.</span><span class="sxs-lookup"><span data-stu-id="763f4-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="763f4-122">Tiek atvērta lapa **Mērvienību pārveidošana**.</span><span class="sxs-lookup"><span data-stu-id="763f4-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="763f4-123">Atlasiet vienu no šīm cilnēm:</span><span class="sxs-lookup"><span data-stu-id="763f4-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="763f4-124">**Starpklases reklāmguvumi** – Atlasiet šo cilni, lai konvertētu no vienībām, kas pieder vienai mērvienību kategorijai.</span><span class="sxs-lookup"><span data-stu-id="763f4-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="763f4-125">**Starpklases reklāmguvumi** – atlasiet šo cilni, lai konvertētu starp vienībām, kas pieder dažādām mērvienību kategorijām.</span><span class="sxs-lookup"><span data-stu-id="763f4-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="763f4-126">Lai pievienotu jaunu pārveidi, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="763f4-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="763f4-127">Iestatiet **Izveidot konvertēšanu šim** uz lauku uz vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="763f4-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="763f4-128">**Prece** – atlasot šo vērtību, varat iestatīt mērvienību pārveidošanu preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="763f4-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="763f4-129">Šī mērvienību pārveidošana tiks izmantota kā atkāpšanās metode visiem preču variantiem, kam nav definēta neviena vienības pārvēršana.</span><span class="sxs-lookup"><span data-stu-id="763f4-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="763f4-130">**Preces variants** – atlasot šo vērtību, varat iestatīt mērvienību pārveidošanu konkrētam preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="763f4-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="763f4-131">Izmantojiet lauku **Preces variants**, lai atlasītu variantu.</span><span class="sxs-lookup"><span data-stu-id="763f4-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="763f4-132">![Jaunas pārveides pievienošana](media/uom-new-conversion.png "Jaunas pārveides pievienošana")</span><span class="sxs-lookup"><span data-stu-id="763f4-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="763f4-133">Izmantojiet citus laukus, kas tiek sniegti, lai iestatītu mērvienību pārveidošanu.</span><span class="sxs-lookup"><span data-stu-id="763f4-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="763f4-134">Atlasiet **Labi**, lai saglabātu jauno mērvienību pārveidošanu.</span><span class="sxs-lookup"><span data-stu-id="763f4-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="763f4-135">Varat atvērt lapu **Mērvienību pārveidošana** produktam vai preces variantam no jebkuras no šīm lapām:</span><span class="sxs-lookup"><span data-stu-id="763f4-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="763f4-136">Detalizēta informācija par preci</span><span class="sxs-lookup"><span data-stu-id="763f4-136">Product details</span></span>
> - <span data-ttu-id="763f4-137">Informācija par izlaistajām precēm</span><span class="sxs-lookup"><span data-stu-id="763f4-137">Released products details</span></span>
> - <span data-ttu-id="763f4-138">Izlaistie preces varianti</span><span class="sxs-lookup"><span data-stu-id="763f4-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="763f4-139">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="763f4-139">Example scenario</span></span>

<span data-ttu-id="763f4-140">Šajā scenārijā uzņēmums pārdod T-kreklus šādos izmēros: mazs, vidējs, liels un īpaši liels.</span><span class="sxs-lookup"><span data-stu-id="763f4-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="763f4-141">T-krekls ir definēts kā prece, un dažādi izmēri ir definēti kā šīs preces varianti.</span><span class="sxs-lookup"><span data-stu-id="763f4-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="763f4-142">Krekli ir iepakoti kastēs.</span><span class="sxs-lookup"><span data-stu-id="763f4-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="763f4-143">Izmēram mazs, vidējs un liels, katrā kastē var būt pieci krekli.</span><span class="sxs-lookup"><span data-stu-id="763f4-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="763f4-144">Tomēr īpaši lielajam izmēram ir vieta tikai četriem krekliem katrā kastē.</span><span class="sxs-lookup"><span data-stu-id="763f4-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="763f4-145">Uzņēmums vēlas izsekot dažādiem T-kreklu variantiem, izmantojot mērvienību *Gabali*, bet pārdod tos, izmantojot mērvienību *Kastes*.</span><span class="sxs-lookup"><span data-stu-id="763f4-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="763f4-146">Mazu, vidēju un lielu izmēru krājumu vienības un pārdošanas vienības pārveidošana ir 1 kaste = 5 gabali.</span><span class="sxs-lookup"><span data-stu-id="763f4-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="763f4-147">Īpaši lielajam izmēram, pārveidošana ir 1 kaste = 4 gabali.</span><span class="sxs-lookup"><span data-stu-id="763f4-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="763f4-148">Vispirms atveriet lapu **Mērvienību pārveidošana** no lapas **Izlaistās preces detalizēta informācija** attiecīgajam **T-kreklam**.</span><span class="sxs-lookup"><span data-stu-id="763f4-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="763f4-149">Lapā **Mērvienību pārveidošana** iestatiet mērvienības pārveidošanu šādam izlaistajam preces variantam: **īpaši liels**.</span><span class="sxs-lookup"><span data-stu-id="763f4-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="763f4-150">Lauks</span><span class="sxs-lookup"><span data-stu-id="763f4-150">Field</span></span>                 | <span data-ttu-id="763f4-151">Iestatījums</span><span class="sxs-lookup"><span data-stu-id="763f4-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="763f4-152">Izveidot konvertēšanu šim:</span><span class="sxs-lookup"><span data-stu-id="763f4-152">Create conversion for</span></span> | <span data-ttu-id="763f4-153">Preces variants</span><span class="sxs-lookup"><span data-stu-id="763f4-153">Product variant</span></span>         |
    | <span data-ttu-id="763f4-154">Preces variants</span><span class="sxs-lookup"><span data-stu-id="763f4-154">Product variant</span></span>       | <span data-ttu-id="763f4-155">T-krekls : : Īpaši liels : :</span><span class="sxs-lookup"><span data-stu-id="763f4-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="763f4-156">No vienības</span><span class="sxs-lookup"><span data-stu-id="763f4-156">From unit</span></span>             | <span data-ttu-id="763f4-157">Kastes</span><span class="sxs-lookup"><span data-stu-id="763f4-157">Boxes</span></span>                   |
    | <span data-ttu-id="763f4-158">Koeficients</span><span class="sxs-lookup"><span data-stu-id="763f4-158">Factor</span></span>                | <span data-ttu-id="763f4-159">4.</span><span class="sxs-lookup"><span data-stu-id="763f4-159">4</span></span>                       |
    | <span data-ttu-id="763f4-160">Uz vienību</span><span class="sxs-lookup"><span data-stu-id="763f4-160">To Unit</span></span>               | <span data-ttu-id="763f4-161">Gabali</span><span class="sxs-lookup"><span data-stu-id="763f4-161">Pieces</span></span>                  |

1. <span data-ttu-id="763f4-162">Izlaistajiem preces variantiem **Mazs**, **Vidējs** un **Liels** ir tāda pati mērvienību pārveidošana starp vienību *Kaste* un *Gabali*, līdz ar to šiem preces variantiem var definēt šādu mērvienību pārveidošanu preces šablonā.</span><span class="sxs-lookup"><span data-stu-id="763f4-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="763f4-163">Lauks</span><span class="sxs-lookup"><span data-stu-id="763f4-163">Field</span></span>                 | <span data-ttu-id="763f4-164">Iestatījums</span><span class="sxs-lookup"><span data-stu-id="763f4-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="763f4-165">Izveidot konvertēšanu šim:</span><span class="sxs-lookup"><span data-stu-id="763f4-165">Create conversion for</span></span> | <span data-ttu-id="763f4-166">Prece</span><span class="sxs-lookup"><span data-stu-id="763f4-166">Product</span></span> |
    | <span data-ttu-id="763f4-167">Prece</span><span class="sxs-lookup"><span data-stu-id="763f4-167">Product</span></span>               | <span data-ttu-id="763f4-168">T-krekls</span><span class="sxs-lookup"><span data-stu-id="763f4-168">T-Shirt</span></span> |
    | <span data-ttu-id="763f4-169">No vienības</span><span class="sxs-lookup"><span data-stu-id="763f4-169">From unit</span></span>             | <span data-ttu-id="763f4-170">Kastes</span><span class="sxs-lookup"><span data-stu-id="763f4-170">Boxes</span></span>   |
    | <span data-ttu-id="763f4-171">Koeficients</span><span class="sxs-lookup"><span data-stu-id="763f4-171">Factor</span></span>                | <span data-ttu-id="763f4-172">5.</span><span class="sxs-lookup"><span data-stu-id="763f4-172">5</span></span>       |
    | <span data-ttu-id="763f4-173">Uz vienību</span><span class="sxs-lookup"><span data-stu-id="763f4-173">To Unit</span></span>               | <span data-ttu-id="763f4-174">Gabali</span><span class="sxs-lookup"><span data-stu-id="763f4-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="763f4-175">Programmas Excel izmantošana, lai atjauninātu mērvienību pārveidošanu</span><span class="sxs-lookup"><span data-stu-id="763f4-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="763f4-176">Ja precei ir daudz preču variantu, kam ir dažādas mērvienību pārveidošanas, ir ieteicams eksportēt mērvienību pārveidošanu uz Microsoft Excel darbgrāmatu, atjaunināt tās un pēc tam tās publicēt Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="763f4-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="763f4-177">Lai eksportētu mērvienību pārveidošanu uz Excel, lapā **Mērvienību pārveidošana**, kas atrodas darbību rūtī, atlasiet **Atvērt objektā Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="763f4-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="763f4-178">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="763f4-178">Additional resources</span></span>

[<span data-ttu-id="763f4-179">Mērvienības pārvaldība</span><span class="sxs-lookup"><span data-stu-id="763f4-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]