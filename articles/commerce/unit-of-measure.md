---
title: Lietot mērvienības iestatījumus
description: Šajā tēmā ir ietverti mērvienību iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022378"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="a6574-103">Lietot mērvienības iestatījumus</span><span class="sxs-lookup"><span data-stu-id="a6574-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a6574-104">Šajā tēmā ir ietverti mērvienību iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6574-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a6574-105">Preci var pārdot dažādās vienībās, piemēram, "katrs", "pāris" un "ducis."</span><span class="sxs-lookup"><span data-stu-id="a6574-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="a6574-106">Programmā Commerce Headquarters precei var definēt mērvienību pēc pārdošanas un parādīt e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="a6574-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="a6574-107">Piemēram, ja mazumtirgotājs pārdod preci gan atsevišķi, gan dučos, pieejamās mērvienības var rādīt kopā ar citu informāciju par preci.</span><span class="sxs-lookup"><span data-stu-id="a6574-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="a6574-108">Šajā ilustrācijā parādīts, ka precei programmā Commerce Headquarters ir konfigurēta pārdošanas mērvienība **kt** (katrs).</span><span class="sxs-lookup"><span data-stu-id="a6574-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Tās preces piemērs, kas ir konfigurēta ar mērvienību programmā Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="a6574-110">Atbalsts mērvienības pielietošanai un rādīšanai ir pieejams Commerce versijā 10.0.19 laidienā.</span><span class="sxs-lookup"><span data-stu-id="a6574-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="a6574-111">Mērvienības iestatījumi</span><span class="sxs-lookup"><span data-stu-id="a6574-111">Unit of measure settings</span></span>

<span data-ttu-id="a6574-112">Mērvienības rādīšanas iestatījumi ir noteikti Commerce vietņu veidotājā **Vietnes iestatījumu \> Paplašinājumi \> Parādīt mērvienību precēm**.</span><span class="sxs-lookup"><span data-stu-id="a6574-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="a6574-113">Pastāv trīs atbalstīti iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="a6574-113">There are three supported settings:</span></span>

- <span data-ttu-id="a6574-114">**Nerādīt** - ja šis iestatījums ir atlasīts, e-komercijas vietne nerādīs preces mērvienību.</span><span class="sxs-lookup"><span data-stu-id="a6574-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="a6574-115">Šī darbība ir noklusējuma darbība.</span><span class="sxs-lookup"><span data-stu-id="a6574-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="a6574-116">**Rādīt preču iepirkšanas pieredzi** – ja ir atlasīts šis iestatījums, mērvienība tiek parādīta detalizētā informācijā par preci, grozu, norēķināšanos, pasūtījumu vēsturi un pasūtījumu detalizētās informācijas lapām.</span><span class="sxs-lookup"><span data-stu-id="a6574-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="a6574-117">**Rādīt preču pārlūkošanas un pirkšanas pieredzi** – ja ir atlasīts šis iestatījums, mērvienība tiek parādīta preču pirkšanas pieredzes lapās un arī preču pārlūkošanas pieredzes laikā.</span><span class="sxs-lookup"><span data-stu-id="a6574-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="a6574-118">Kā daļa no šīs uzvedības mērvienības tiek parādītas meklēšanas rezultātos un preču kolekcijas moduļos.</span><span class="sxs-lookup"><span data-stu-id="a6574-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6574-119">Mērvienības rādīšanas iestatījumi ir pieejami Commerce versijā 10.0.19 laidienā.</span><span class="sxs-lookup"><span data-stu-id="a6574-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="a6574-120">Ja veicat atjaunināšanu no vecākas Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="a6574-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="a6574-121">Instrukcijas skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="a6574-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="a6574-122">Moduļi, kas izmanto mērvienības iestatījumus</span><span class="sxs-lookup"><span data-stu-id="a6574-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="a6574-123">Moduļi, kas izmanto mērvienības iestatījumus, ietver pirkšanas kasti, vēlmju sarakstu, grozu, groza ikonu, meklēšanas rezultātu konteineru, preču kolekciju, pārbaudi un pasūtījuma informācijas moduļus.</span><span class="sxs-lookup"><span data-stu-id="a6574-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="a6574-124">Piemērā šajā attēlā, preču informācijas lapa (product details page - PDP) parāda preces mērvienību (**kt**).</span><span class="sxs-lookup"><span data-stu-id="a6574-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![PDP piemērs, kurā parādīta mērvienība](./media/Productunit-PDP.png)

<span data-ttu-id="a6574-126">Piemērā šajā attēlā, preču kolekcijas modulis parāda preces mērvienību (**kt**).</span><span class="sxs-lookup"><span data-stu-id="a6574-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Preču kolekcijas moduļa piemērs, kurā parādīta mērvienība](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="a6574-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a6574-128">Additional resources</span></span>

[<span data-ttu-id="a6574-129">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="a6574-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a6574-130">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="a6574-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a6574-131">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="a6574-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a6574-132">Konta pārvaldības lapas un moduļi</span><span class="sxs-lookup"><span data-stu-id="a6574-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="a6574-133">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="a6574-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
