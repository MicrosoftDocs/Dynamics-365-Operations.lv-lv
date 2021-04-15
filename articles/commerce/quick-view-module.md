---
title: Ātrā skata modulis
description: Šajā tēmā tiek stāstīts par ātrā skata moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d7e88163fd9b8dc4f5636ed29e2c4248aece52bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792175"
---
# <a name="quick-view-module"></a><span data-ttu-id="d77f8-103">Ātrā skata modulis</span><span class="sxs-lookup"><span data-stu-id="d77f8-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d77f8-104">Šajā tēmā tiek stāstīts par ātrā skata moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d77f8-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d77f8-105">Ātrā skata modulis ļauj lietotājiem ātri skatīt preču informāciju, kad tie pārlūko preces saraksta lapā, un pievienot vienu vai vairākas preces grozam no saraksta lapas, bez nepieciešamības atvērt preču informācijas lapu (PDP).</span><span class="sxs-lookup"><span data-stu-id="d77f8-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="d77f8-106">Ātrā skata modulis nodrošina preču informācijas pārskatu, kas lietotājiem nepieciešams, lai veiktu “pievienot grozam” lēmumu.</span><span class="sxs-lookup"><span data-stu-id="d77f8-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="d77f8-107">Tas nodrošina arī saiti uz PDP, lai lietotāji varētu skatīt preces papildu informāciju un pirkšanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="d77f8-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="d77f8-108">Ātrā skata modulis tiek atbalstīts [preču kolekcijas](product-collection-module-overview.md) un [meklēšanas rezultātu](search-result-module.md) moduļos.</span><span class="sxs-lookup"><span data-stu-id="d77f8-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d77f8-109">Ātrā skata modulis ir pieejams no Commerce versijas 10.0.17 laidiena.</span><span class="sxs-lookup"><span data-stu-id="d77f8-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="d77f8-110">Tālāk esošajā ilustrācijā redzams ātrā skata moduļa piemērs preču saraksta lapā.</span><span class="sxs-lookup"><span data-stu-id="d77f8-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Ātrā skata moduļa piemērs preču saraksta lapā](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="d77f8-112">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d77f8-112">Module properties</span></span>

<span data-ttu-id="d77f8-113">Ātrā skata modulis atbalsta dažas no tām pašām funkcijām, ko iegādes lodziņa modulis.</span><span class="sxs-lookup"><span data-stu-id="d77f8-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="d77f8-114">Tādēļ ātrā skata moduļa rekvizīti ir līdzīgi iegādes lodziņa moduļa rekvizītiem.</span><span class="sxs-lookup"><span data-stu-id="d77f8-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="d77f8-115">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="d77f8-115">Property</span></span> | <span data-ttu-id="d77f8-116">Vērtības</span><span class="sxs-lookup"><span data-stu-id="d77f8-116">Values</span></span> | <span data-ttu-id="d77f8-117">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d77f8-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d77f8-118">Virsraksta atzīme</span><span class="sxs-lookup"><span data-stu-id="d77f8-118">Heading tag</span></span> | <span data-ttu-id="d77f8-119">**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**</span><span class="sxs-lookup"><span data-stu-id="d77f8-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="d77f8-120">Šis rekvizīts definē virsraksta atzīmi preces nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="d77f8-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="d77f8-121">Ja ātrā skata modulis atrodas lapas augšā, šis rekvizīts ir jāiestata uz **H1**, lai atbilstu pieejamības standartiem.</span><span class="sxs-lookup"><span data-stu-id="d77f8-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="d77f8-122">Atļaut pielāgotu cenu</span><span class="sxs-lookup"><span data-stu-id="d77f8-122">Allow custom price</span></span> | <span data-ttu-id="d77f8-123">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="d77f8-123">**True** or **False**</span></span> | <span data-ttu-id="d77f8-124">Ja šis rekvizīts ir iestatīts kā **Patiess**, lietotājs var ievadīt pielāgoto cenu.</span><span class="sxs-lookup"><span data-stu-id="d77f8-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="d77f8-125">Minimālā cena</span><span class="sxs-lookup"><span data-stu-id="d77f8-125">Minimum price</span></span> | <span data-ttu-id="d77f8-126">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="d77f8-126">Integer</span></span> | <span data-ttu-id="d77f8-127">Šis rekvizīts ir piemērojams tikai tad, ja rekvizīts **Atļaut pielāgotu cenu** ir iestatīts kā **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="d77f8-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="d77f8-128">Tas definē minimālo cenu, ko lietotājs var ievadīt (piemēram, 1 $).</span><span class="sxs-lookup"><span data-stu-id="d77f8-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="d77f8-129">Maksimālā cena</span><span class="sxs-lookup"><span data-stu-id="d77f8-129">Maximum price</span></span> | <span data-ttu-id="d77f8-130">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="d77f8-130">Integer</span></span> | <span data-ttu-id="d77f8-131">Šis rekvizīts ir piemērojams tikai tad, ja rekvizīts **Atļaut pielāgotu cenu** ir iestatīts kā **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="d77f8-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="d77f8-132">Tas definē maksimālo cenu, ko lietotājs var ievadīt (piemēram, 1 000 $).</span><span class="sxs-lookup"><span data-stu-id="d77f8-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="d77f8-133">Commerce vietnes veidotāja iestatījumi</span><span class="sxs-lookup"><span data-stu-id="d77f8-133">Commerce site builder settings</span></span>

<span data-ttu-id="d77f8-134">Tāpat kā iegādes lodziņa modulī, ātrā skata modulī tiek ievēroti iestatījumi no **Vietnes iestatījumi \> Paplašinājumi \> Pievienot preci grozam**.</span><span class="sxs-lookup"><span data-stu-id="d77f8-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="d77f8-135">Tomēr iestatījums **Doties uz lapu Grozs** tiek ignorēts, jo tas neatbilst ātrā skata moduļa mērķim, proti, lai lietotāji varētu pārlūkot vairākas preces saraksta lapā un pievienot tās grozam, neizejot no saraksta lapas.</span><span class="sxs-lookup"><span data-stu-id="d77f8-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="d77f8-136">Ātrā skata moduļa pievienošana preču kolekcijas modulim</span><span class="sxs-lookup"><span data-stu-id="d77f8-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="d77f8-137">Ātrā skata modulis var tikt pievienots preču kolekciju un meklēšanas rezultātu moduļiem.</span><span class="sxs-lookup"><span data-stu-id="d77f8-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="d77f8-138">Lai pievienotu ātrā skata moduli preču kolekciju modulim programmā Commerce vietnes veidotājs, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d77f8-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d77f8-139">Dodieties uz **Lapas** un pēc tam atlasiet Fabrikam vietnes sakumlapu.</span><span class="sxs-lookup"><span data-stu-id="d77f8-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="d77f8-140">Dodieties uz **Preču kolekciju** moduli sākumlapā, atlasiet daudzpunktes (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d77f8-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d77f8-141">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Ātrais skats** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d77f8-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d77f8-142">Moduļa **Ātrais skats** rekvizītu rūtī atlasiet **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="d77f8-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="d77f8-143">Dialoglodziņā **Virsraksts** iestatiet lauka **Virsraksta līmenis** vērtību uz **H2** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d77f8-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="d77f8-144">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d77f8-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d77f8-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d77f8-145">Additional resources</span></span>

[<span data-ttu-id="d77f8-146">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="d77f8-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d77f8-147">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="d77f8-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d77f8-148">Preču kolekciju modulis</span><span class="sxs-lookup"><span data-stu-id="d77f8-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="d77f8-149">Meklēšanas rezultātu modulis</span><span class="sxs-lookup"><span data-stu-id="d77f8-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
