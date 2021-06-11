---
title: Displeja iestatījumu pielietošana preču dimensijām
description: Šajā tēmā ir aplūkoti preču dimensiju displeja iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117235"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="b897b-103">Displeja iestatījumu pielietošana preču dimensijām</span><span class="sxs-lookup"><span data-stu-id="b897b-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b897b-104">Šajā tēmā ir aplūkoti preču dimensiju displeja iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b897b-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b897b-105">Dynamics 365 Commerce atbalsta izmēru, stilu un krāsu izmērus, lai atšķirtu preces variantus.</span><span class="sxs-lookup"><span data-stu-id="b897b-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="b897b-106">Dimensijas parasti tiek rādītas kā teksta vērtības, piemēram, "Mazs", "Vidējs" un "Liels" izmēriem un "Melns" un "Brūns" krāsām.</span><span class="sxs-lookup"><span data-stu-id="b897b-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="b897b-107">Tomēr, ja prece atbalsta daudzas variācijas, var būt grūti pārlūkot preces variantus, jo, lai skatītu attēlu katram variantam, ir nepieciešamas vairākas atlases.</span><span class="sxs-lookup"><span data-stu-id="b897b-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="b897b-108">Lai atvieglotu preces variantu pārlūkošanu, Commerce versijas 10.0.20 laidienā var izmantot attēlus un heksadecimālos kodus, lai dimensijas parādītu kā paraugus.</span><span class="sxs-lookup"><span data-stu-id="b897b-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="b897b-109">Commerce vietnes veidotājā dimensiju iestatījumi tiek definēti **Vietas iestatījumi \> Paplašinājumi \> Dimensiju iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b897b-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="b897b-110">Nākamajā attēlā ir parādīts dimensiju iestatījumu piemērs vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="b897b-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Vietnes iestatījumu piemērs Commerce vietnes veidotājā](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="b897b-112">Ir pieejami divi dimensiju iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="b897b-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="b897b-113">**Dimensijas, kas jārāda kā attēls** - norādiet, kurām dimensijām jāparādās e-komercijas vietņu lapās, piemēram, preču informācijas lapās (PDP) un meklēšanas rezultātu saraksta lapās.</span><span class="sxs-lookup"><span data-stu-id="b897b-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="b897b-114">Jebkuru krāsu, izmēru un stila dimensiju kombināciju var parādīt kā paraugu.</span><span class="sxs-lookup"><span data-stu-id="b897b-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="b897b-115">Ja dimensija ir atlasīta parādīšanai kā paraugs, Commerce moduļa renderēšana meklēs pieejamu heksadecimālo koda parauga konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b897b-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="b897b-116">Ja heksadecimālais kods nav konfigurēts, sistēmas loģika meklēs attēla URL parauga konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b897b-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="b897b-117">Ja nav konfigurēts ne heksadecimālais kods, ne attēla URL, tiks parādīts teksts.</span><span class="sxs-lookup"><span data-stu-id="b897b-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="b897b-118">Nākamajā attēlā ir parādīts piemērs, kur e-komercijas vietnes PDP ietver krāsu un izmēru paraugus.</span><span class="sxs-lookup"><span data-stu-id="b897b-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="b897b-119">Šajā piemērā krāsu dimensijai ir konfigurēts heksadecimālais kods.</span><span class="sxs-lookup"><span data-stu-id="b897b-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="b897b-120">Tāpēc paraugi tiek parādīti kā krāsas.</span><span class="sxs-lookup"><span data-stu-id="b897b-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="b897b-121">Tomēr izmēra dimensijai nav konfigurēts ne heksadecimālais kods, ne attēla URL.</span><span class="sxs-lookup"><span data-stu-id="b897b-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="b897b-122">Tāpēc tiek parādīts teksts.</span><span class="sxs-lookup"><span data-stu-id="b897b-122">Therefore, text is shown.</span></span>

    ![Piemērs krāsu dimensijai, kas e-komercijas preču informācijas lapā tiek rādīti kā paraugi](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="b897b-124">**Preču kartē rādāmās dimensijas** — norādiet, kurām dimensijām jāparādās produktu kartēs, kas tiek rādītas sarakstos un saraksta lapās.</span><span class="sxs-lookup"><span data-stu-id="b897b-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="b897b-125">Lai dimensija varētu parādīties preču kartē, šai dimensijai ir jāiespējo šis iestatījums.</span><span class="sxs-lookup"><span data-stu-id="b897b-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="b897b-126">Ir jāiespējo arī iestatījums **Dimensijas, lai parādītu kā attēlu**.</span><span class="sxs-lookup"><span data-stu-id="b897b-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="b897b-127">Paraugu atlases darbība preču kartēs ir optimizēta krāsu dimensijai.</span><span class="sxs-lookup"><span data-stu-id="b897b-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="b897b-128">Citām dimensijām var būt nepieciešams skata paplašinājums, lai pielāgotu parauga atlases darbību.</span><span class="sxs-lookup"><span data-stu-id="b897b-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="b897b-129">Nākamajā attēlā ir parādīts piemērs, kur e-komercijas vietnes saraksta lapā ir preču kartes, kurās ir krāsu paraugi.</span><span class="sxs-lookup"><span data-stu-id="b897b-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Piemērs krāsu dimensijai, kas e-komercijas saraksta lapā tiek rādīti kā paraugi](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="b897b-131">Informāciju par to, kā konfigurēt preču dimensijas tā, lai tās vietnes lapās tiktu rādītas kā paraugi, skatiet [Konfigurēt preču dimensiju vērtības, lai tās tiktu rādītas kā paraugi](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="b897b-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b897b-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b897b-132">Additional resources</span></span>

[<span data-ttu-id="b897b-133">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="b897b-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b897b-134">Meklēšanas rezultātu modulis</span><span class="sxs-lookup"><span data-stu-id="b897b-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="b897b-135">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="b897b-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b897b-136">Konfigurēt preču dimensiju vērtības, lai tās tiktu rādītas kā paraugi</span><span class="sxs-lookup"><span data-stu-id="b897b-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
