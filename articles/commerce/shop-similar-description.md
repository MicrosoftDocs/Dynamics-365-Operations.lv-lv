---
title: Ieteikumu “pirkt līdzīga apraksta preces” iespējošana
description: Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīga apraksta preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234393"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="9a501-103">Ieteikumu “pirkt līdzīgus aprakstus” iespējošana</span><span class="sxs-lookup"><span data-stu-id="9a501-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a501-104">Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīga apraksta preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9a501-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9a501-105">"Pirkt līdzīga apraksta preces" ieteikumu līdzeklis Dynamics 365 Commerce izmanto mākslīgā intelekta un mašīnu mācīšanās spēku (AI-ML), lai sniegtu rekomendācijas par precēm, kuru apraksts ir līdzīgs klienta meklētajām precēm.</span><span class="sxs-lookup"><span data-stu-id="9a501-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="9a501-106">Veidojot "pirkt līdzīga apraksta preces" ieteikumus pieejamus visiem mazumtirdzniecības kanāliem Commerce, mazumtirgotāji var palielināt klientu apmierinātību, palīdzot klientiem viegli atrast to, ko viņi vēlas.</span><span class="sxs-lookup"><span data-stu-id="9a501-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="9a501-107">"Pirkt līdzīga apraksta preces" rekomendācijas izmanto sēklu preču variantu preču nosaukumu un aprakstu, lai atrastu un ieteiktu vizuāli līdzīgas preces mazumtirdzniecības preču katalogā.</span><span class="sxs-lookup"><span data-stu-id="9a501-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="9a501-108">"Pirkt līdzīga apraksta preces" ieteikumi ir pieejami gan pārdošanas punktā (POS), gan e-komercijas notikumos.</span><span class="sxs-lookup"><span data-stu-id="9a501-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="9a501-109">Piemēra situācijas</span><span class="sxs-lookup"><span data-stu-id="9a501-109">Example scenarios</span></span>

<span data-ttu-id="9a501-110">Turpmākie piemēru scenāriji parāda rekomendāciju veidus, ko var nodrošināt funkcionalitāte "līdzīga apraksta prece":</span><span class="sxs-lookup"><span data-stu-id="9a501-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="9a501-111">Klients apskata retro stila raga briļļu pāri un saņem ieteikumu komplektu citām brillēm, kam ir līdzīgs dizains, mazumtirgotāja industrijas kontekstā.</span><span class="sxs-lookup"><span data-stu-id="9a501-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="9a501-112">Klients izmanto “pirkt līdzīga apraksta preces” ieteikumus, lai atklātu kafijas aromātus, kas ir līdzīgi aromatizētājam, ko tas iepriekš iegādājies no mazumtirgotāja.</span><span class="sxs-lookup"><span data-stu-id="9a501-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="9a501-113">Ieteikumu “pirkt līdzīga apraksta preces” iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9a501-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="9a501-114">Preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri ir migrējuši savu krātuvi uz 2. paaudzes Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="9a501-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9a501-115">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="9a501-115">Prerequisites</span></span>

<span data-ttu-id="9a501-116">Pirms “pirkt līdzīga apraksta preces” ieteikumus var parādīt klientiem, jāizpilda šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="9a501-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="9a501-117">[Iespējot preču ieteikumus](enable-product-recommendations.md) programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9a501-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="9a501-118">Apstipriniet, ka multivides serveris atbalsta HTTPS izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="9a501-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="9a501-119">Līdzekļa “pirkt līdzīga apraksta preces” ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="9a501-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="9a501-120">Lai ieslēgtu "pirkt līdzīga apraksta preces" ieteikumus programmā Commerce Headquarters, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="9a501-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9a501-121">Darbvietā **Līdzekļu pārvaldība** pieejamo līdzekļu sarakstā meklējiet un atlasiet **Pirkt līdzīga apraksta preces**.</span><span class="sxs-lookup"><span data-stu-id="9a501-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="9a501-122">Labās puses rūtī atlasiet **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="9a501-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="9a501-123">Ieslēdzot šo līdzekli, sistēma sāk ģenerēt preču ieteikumu sarakstus.</span><span class="sxs-lookup"><span data-stu-id="9a501-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="9a501-124">Var paiet laiks līdz vienai dienai, pirms šie saraksti kļūst pieejami un redzami tiešsaistē un POS termināļos.</span><span class="sxs-lookup"><span data-stu-id="9a501-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="9a501-125">Ja izslēdzat šo līdzekli, netiek ietekmēti citi preču ieteikumu veidi.</span><span class="sxs-lookup"><span data-stu-id="9a501-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="9a501-126">Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9a501-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="9a501-127">Pogas Pirkt līdzīga apraksta preces pievienošana preču informācijas lapām</span><span class="sxs-lookup"><span data-stu-id="9a501-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="9a501-128">Pēc tam, kad ieslēdzat "pirkt līdzīga apraksta preces" ieteikumu līdzekli programmā Commerce Headquarters, varat pievienot pogu **pirkt līdzīga apraksta preces** pirkšanas kastē jebkuras preču informācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="9a501-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="9a501-129">Klients, kurš atlasa šo pogu, tiek novirzīts uz īpašu lapu **Pirkt līdzīga apraksta preces**, kas parāda vizuāli līdzīgas preces.</span><span class="sxs-lookup"><span data-stu-id="9a501-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="9a501-130">Tad klients var izmantot atlasītājus, lai turpinātu filtrēt preces.</span><span class="sxs-lookup"><span data-stu-id="9a501-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="9a501-131">Lai pievienotu pogu **Pirkt līdzīga apraksta preces** PDP, izmantojot Commerce Site Builder, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9a501-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9a501-132">Atveriet esošu vietnes noformētāja lapu, kas satur pirkšanas kastes moduli.</span><span class="sxs-lookup"><span data-stu-id="9a501-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="9a501-133">Navigācijas rūtī kreisajā pusē atlasiet pirkšanas kastes moduli.</span><span class="sxs-lookup"><span data-stu-id="9a501-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="9a501-134">Labās puses rūtī atlasiet izvēles rūtiņu **Iespējot Pirkt līdzīga apraksta preces saiti**.</span><span class="sxs-lookup"><span data-stu-id="9a501-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="9a501-135">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9a501-135">Select **Save**.</span></span>
1. <span data-ttu-id="9a501-136">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="9a501-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="9a501-137">Kad lapa ir publicēta, PDP ietvers **Pirkt līdzīga apraksta preces** pogu.</span><span class="sxs-lookup"><span data-stu-id="9a501-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="9a501-138">Sekojošajā attēlā ir parādīta izvēles rūtiņa **Iespējot Pirkt līdzīga apraksta preces saiti** un poga **Pirkt līdzīga apraksta preces** piemēra PDP vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="9a501-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Pirkt līdzīga apraksta preces saites izvēles rūtiņas un Pirkt līdzīga apraksta preces pogas iespējošana PDP vietnes veidotājā](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="9a501-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9a501-140">Additional resources</span></span>

[<span data-ttu-id="9a501-141">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="9a501-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9a501-142">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="9a501-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9a501-143">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="9a501-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9a501-144">Ieteikumu “pirkt līdzīgus modeļus” iespējošana</span><span class="sxs-lookup"><span data-stu-id="9a501-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9a501-145">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="9a501-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9a501-146">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="9a501-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9a501-147">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="9a501-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]