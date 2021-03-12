---
title: Iespējot "pirkt līdzīgas preces" rekomendācijas
description: Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīgas preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 95e4246d6c5f9ac5bc86b626be0d971f756c5130
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985615"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="ade9d-103">Iespējot "pirkt līdzīgas preces" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="ade9d-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ade9d-104">Šajā tēmā aprakstīts, kā iespējot "pirkt līdzīgas preces" preču ieteikumus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ade9d-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ade9d-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ade9d-105">Overview</span></span>

<span data-ttu-id="ade9d-106">"Pirkt līdzīgas preces" ieteikumu līdzeklis Dynamics 365 Commerce izmanto mākslīgā intelekta un mašīnu mācīšanās spēku (AI-ML), lai sniegtu rekomendācijas par vizuāli līdzīgiem produktiem klientiem.</span><span class="sxs-lookup"><span data-stu-id="ade9d-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="ade9d-107">Veidojot "pirkt līdzīgas preces" ieteikumus pieejamus visiem mazumtirdzniecības kanāliem Commerce, mazumtirgotāji var palielināt klientu apmierinātību, palīdzot klientiem viegli atrast to, ko viņi vēlas.</span><span class="sxs-lookup"><span data-stu-id="ade9d-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="ade9d-108">"Pirkt līdzīgas preces" rekomendācijas izmanto sēklu preču variantu preču attēlus, lai atrastu un ieteiktu vizuāli līdzīgas preces mazumtirdzniecības preču katalogā.</span><span class="sxs-lookup"><span data-stu-id="ade9d-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="ade9d-109">"Pirkt līdzīgas preces" ieteikumi ir pieejami gan pārdošanas punktā (POS), gan e-komercijas notikumos.</span><span class="sxs-lookup"><span data-stu-id="ade9d-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="ade9d-110">Piemēra situācijas</span><span class="sxs-lookup"><span data-stu-id="ade9d-110">Example scenarios</span></span>

- <span data-ttu-id="ade9d-111">Klients aplūko melnu, svītrainu džemperi un saņem rekomendāciju līdzīgam džemperim sarkanā krāsā.</span><span class="sxs-lookup"><span data-stu-id="ade9d-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="ade9d-112">Klients atlasa ieteicamo preci, nevis sākotnēji skatīto preci, un pēc tam saņem ieteikumus par līdzīgiem produktiem sarkanā krāsā.</span><span class="sxs-lookup"><span data-stu-id="ade9d-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="ade9d-113">Klients izmanto "pirkt līdzīgas preces" ieteikumus, lai atklātu pieskaņotus auskarus gredzenam, ko klients vēlas iegādāties.</span><span class="sxs-lookup"><span data-stu-id="ade9d-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="ade9d-114">Iespējot "pirkt līdzīgas preces" ieteikumus Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="ade9d-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="ade9d-115">Preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri ir migrējuši savu krātuvi uz Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="ade9d-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ade9d-116">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="ade9d-116">Prerequisites</span></span>

<span data-ttu-id="ade9d-117">Pirms mazumtirgotāji var sākt rādīt "pirkt līdzīgas preces" ieteikumus klientiem, ir divi priekšnosacījumu soļi:</span><span class="sxs-lookup"><span data-stu-id="ade9d-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="ade9d-118">[Iespējot preču ieteikumus](enable-product-recommendations.md) programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ade9d-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="ade9d-119">Apstipriniet, ka multivides serveris atbalsta HTTPS izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="ade9d-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="ade9d-120">Lai ieteikumu programma varētu piekļūt preces attēliem, mazumtirgotājiem ir jāģenerē preču URL.</span><span class="sxs-lookup"><span data-stu-id="ade9d-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="ade9d-121">Lai izveidotu preču URL programmā Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ade9d-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ade9d-122">Dodieties uz **Preču attēli**.</span><span class="sxs-lookup"><span data-stu-id="ade9d-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="ade9d-123">Darbību rūtī atlasiet **Definēt multivides veidni**.</span><span class="sxs-lookup"><span data-stu-id="ade9d-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="ade9d-124">Rekvizītu rūtī **Definēt multivides veidni** sadaļā **Multivides URL**, atlasiet **Izveidot URL**.</span><span class="sxs-lookup"><span data-stu-id="ade9d-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="ade9d-125">Kad iespējojat "pirkt līdzīgas preces" ieteikumu funkciju, tiek sākts preču rekomendāciju saraksta ģenerēšanas process.</span><span class="sxs-lookup"><span data-stu-id="ade9d-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="ade9d-126">Var tikt pieprasīta līdz vienai dienai, pirms šie saraksti ir pieejami un redzami tiešsaistē un POS termināļos.</span><span class="sxs-lookup"><span data-stu-id="ade9d-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="ade9d-127">Lai iespējotu "pirkt līdzīgas preces" ieteikumus programmā Commerce Headquarters, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="ade9d-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ade9d-128">Dodieties uz **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="ade9d-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="ade9d-129">Pieejamo funkciju sarakstā meklējiet un atlasiet **pirkt līdzīgas preces**.</span><span class="sxs-lookup"><span data-stu-id="ade9d-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="ade9d-130">Labajā rūtī atlasiet **Iespējot**, lai ieslēgtu pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="ade9d-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="ade9d-131">Sekojošajā attēlā ir parādīts līdzeklis **pirkt līdzīgas preces** lapā **Līdzekļu pārvaldība** programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ade9d-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Pirkt līdzīgas preces līdzeklis lapā Līdzekļu pārvaldība programmā Commerce Headquarters](./media/enableshopsimilarlooks.png)

<span data-ttu-id="ade9d-133">Pēc tam, kad iepriekš norādītie uzdevumi ir pabeigti, POS termināļi tiek automātiski uzlaboti ar kontekstuālu **pirkt līdzīgas preces** paneli.</span><span class="sxs-lookup"><span data-stu-id="ade9d-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="ade9d-134">Atlasot **Skatīt vairāk**, POS termināļa lietotājus var aizvest uz "pirkt līdzīgas preces" lapu, ko var filtrēt tālāk.</span><span class="sxs-lookup"><span data-stu-id="ade9d-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="ade9d-135">Izslēdzot "pirkt līdzīgas preces" ieteikumu funkciju, netiek ietekmēti nekādi citi preces ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="ade9d-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="ade9d-136">Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ade9d-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="ade9d-137">Pievienot pogu Pirkt līdzīgas preces preču detalizētas informācijas lapām, izmantojot Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="ade9d-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="ade9d-138">Pēc tam, kad iespējojat "pirkt līdzīgas preces" ieteikumu līdzekli programmā Commerce Headquarters, opcija Commerce Site Builder ļauj mazumtirgotājiem pievienot pogu **pirkt līdzīgas preces** pirkšanas kastē jebkuras preču informācijas lapā (PDP).</span><span class="sxs-lookup"><span data-stu-id="ade9d-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="ade9d-139">Klients, kurš atlasa šo pogu, tiek nogādāts uz īpašu "pirkt līdzīgas preces" lapu, kas atgriež vizuāli līdzīgas preces.</span><span class="sxs-lookup"><span data-stu-id="ade9d-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="ade9d-140">Tur klients var izmantot atlasītāju, lai turpinātu filtrēt preces.</span><span class="sxs-lookup"><span data-stu-id="ade9d-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="ade9d-141">Lai pievienotu pogu **Pirkt līdzīgas preces** PDP, izmantojot Commerce Site Builder, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="ade9d-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ade9d-142">Atveriet esošu vietnes noformētāja lapu, kas satur pirkšanas kastes moduli.</span><span class="sxs-lookup"><span data-stu-id="ade9d-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="ade9d-143">Navigācijas rūtī kreisajā pusē atlasiet pirkšanas kastes moduli.</span><span class="sxs-lookup"><span data-stu-id="ade9d-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="ade9d-144">Labajā navigācijas rūtī atlasiet izvēles rūtiņu **Iespējot Pirkt līdzīgas preces saiti**.</span><span class="sxs-lookup"><span data-stu-id="ade9d-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="ade9d-145">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="ade9d-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="ade9d-146">Kad lapa ir publicēta, PDP ietvers **Pirkt līdzīgas preces** pogu.</span><span class="sxs-lookup"><span data-stu-id="ade9d-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="ade9d-147">Sekojošajā attēlā ir parādīta izvēles rūtiņa **Iespējot Pirkt līdzīgas preces saiti** un **Pirkt līdzīgas preces**, piemēram, PDP vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="ade9d-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Iespējot Pirkt līdzīgas preces saiti un Pirkt līdzīgas preces PDP vietnes veidotājā](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="ade9d-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ade9d-149">Additional resources</span></span>

[<span data-ttu-id="ade9d-150">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="ade9d-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ade9d-151">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ade9d-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ade9d-152">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="ade9d-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ade9d-153">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="ade9d-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ade9d-154">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="ade9d-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ade9d-155">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="ade9d-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ade9d-156">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="ade9d-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ade9d-157">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="ade9d-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ade9d-158">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="ade9d-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ade9d-159">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="ade9d-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
