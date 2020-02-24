---
title: Preču personalizētu ieteikumu iespējošana
description: Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b3c6140b8bd3ea15458223c0f61810421d0b2bc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025265"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="b2c70-103">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="b2c70-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2c70-104">Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2c70-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b2c70-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b2c70-105">Overview</span></span>

<span data-ttu-id="b2c70-106">Sistēmā Dynamics 365 Commerce mazumtirgotāji var padarīt personalizētus produktu ieteikumus (sauktus arī par personalizēšanu) pieejamus.</span><span class="sxs-lookup"><span data-stu-id="b2c70-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="b2c70-107">Šādā veidā personificētus ieteikumus var iekļaut klientu tiešsaistes pieredzē un pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="b2c70-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="b2c70-108">Kad personalizācijas funkcionalitāte ir ieslēgta, sistēma var saistīt lietotāja pirkuma un preces informāciju, lai ģenerētu individualizētus preces ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="b2c70-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="b2c70-109">Personalizācijas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="b2c70-109">Personalization prerequisites</span></span>

<span data-ttu-id="b2c70-110">Pirms padarīt personalizētus preču ieteikumus pieejamus klientiem, ņemiet vērā, ka preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri migrēja to glabāšanu Azure Data Lake veikalā.</span><span class="sxs-lookup"><span data-stu-id="b2c70-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="b2c70-111">Pirms klienti var saņemt personalizētus preču ieteikumus, mazumtirgotājiem ir [jāaktivizē preču ieteikumi](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="b2c70-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b2c70-112">Ieslēdzot preču ieteikumus, varat ieslēgt arī personalizāciju.</span><span class="sxs-lookup"><span data-stu-id="b2c70-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="b2c70-113">Tomēr, izslēdzot personalizāciju, netiek izslēgti citi preču ieteikumu veidi.</span><span class="sxs-lookup"><span data-stu-id="b2c70-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="b2c70-114">Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="b2c70-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="b2c70-115">Personalizācijas aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="b2c70-115">Turn on personalization</span></span>

<span data-ttu-id="b2c70-116">Lai aktivizētu personalizāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="b2c70-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="b2c70-117">Pärejiet uz **Mazumtirdzniecība un komercija \> Preču ieteikumi \> Ieteikumu parametri**.</span><span class="sxs-lookup"><span data-stu-id="b2c70-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="b2c70-118">Retail koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="b2c70-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="b2c70-119">Atlasiet opcijai **Iespējot personalizāciju** iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b2c70-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Personalizācijas aktivizēšana](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="b2c70-121">Ieslēdzot personalizāciju, tiek sākts personalizētu preču ieteikumu saraksta ģenerēšanas process.</span><span class="sxs-lookup"><span data-stu-id="b2c70-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="b2c70-122">Var tikt pieprasīta līdz vienai dienai, pirms šie saraksti ir pieejami un redzami tiešsaistē un POS.</span><span class="sxs-lookup"><span data-stu-id="b2c70-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="b2c70-123">Personalizēti saraksti</span><span class="sxs-lookup"><span data-stu-id="b2c70-123">Personalized lists</span></span>

<span data-ttu-id="b2c70-124">Līdztekus iespējai personalizēt esošus automātiski ģenerētus sarakstus, ieteikumu pakalpojums ļauj personalizēt produktu atklāšanas pieredzi gan tiešsaistē, gan POS.</span><span class="sxs-lookup"><span data-stu-id="b2c70-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="b2c70-125">Pēc personalizācija ir ieslēgta, tirgotāji var rādīt pircējiem personalizētus "ieteikumu" sarakstus tiešsaistē vai "ieteicams klientam" sarakstiem POS termināļos.</span><span class="sxs-lookup"><span data-stu-id="b2c70-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="b2c70-126">Turklāt mazumtirgotāji var piemērot personalizāciju esošajiem preču ieteikumu sarakstiem un nodrošināt Vispārējās datu aizsardzības regulas (VDAR) atteikšanās pieredzi autentificētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="b2c70-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="b2c70-127">Izslēdzot personalizāciju, arī šie līdzekļi tiek izslēgti.</span><span class="sxs-lookup"><span data-stu-id="b2c70-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="b2c70-128">Tiešsaistes "ieteikumu" saraksti</span><span class="sxs-lookup"><span data-stu-id="b2c70-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="b2c70-129">"Tiešsaistes" saraksts ir mākslīgā intelekta, datormācīšanās (AI-ML) saraksts, kas parāda autentificētam lietotājam personalizētu ieteikto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="b2c70-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="b2c70-130">Šis saraksts ir balstīts uz lietotāja universālā kanāla pirkšanas vēsturi.</span><span class="sxs-lookup"><span data-stu-id="b2c70-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="b2c70-131">Personalizētie ieteikumi tiek dinamiski atjaunināti, kad lietotājs veic vairāk pirkumu.</span><span class="sxs-lookup"><span data-stu-id="b2c70-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="b2c70-132">Šis saraksta veids atbalsta arī kategoriju filtrēšanu, lai mazumtirgotāji varētu rādīt populārākos ieteikumus, pamatojoties uz navigācijas hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="b2c70-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="b2c70-133">Pirms "ieteikumu" sarakstu var parādīt jebkurā e-komercijas lapā, ir jāizpilda šādas lietotāju prasības:</span><span class="sxs-lookup"><span data-stu-id="b2c70-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="b2c70-134">Lietotājiem ir jāpiesakās sistēmā.</span><span class="sxs-lookup"><span data-stu-id="b2c70-134">Users must be signed in.</span></span> <span data-ttu-id="b2c70-135">Anonīmie lietotāji neredzēs personalizētus ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="b2c70-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="b2c70-136">Lietotājiem ir jābūt vismaz vienam pirkumam viņu kontā.</span><span class="sxs-lookup"><span data-stu-id="b2c70-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="b2c70-137">Lietotājiem ir jāizvēlas saņemt personalizētus ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="b2c70-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="b2c70-138">Sekojošajā attēlā ir parādīts saraksts "ieteikumu" saraksts tiešsaistes veikala lapā.</span><span class="sxs-lookup"><span data-stu-id="b2c70-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Tiešsaistes "ieteikumu" saraksts](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="b2c70-140">"Klientu ieteikumu" saraksti POS</span><span class="sxs-lookup"><span data-stu-id="b2c70-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="b2c70-141">Lai uzlabotu savu klientu apkalpošanas pieredzi, mazumtirgotāji var personalizēt esošās detalizētās informācijas lapas par klientiem, pievienojot kontekstuālo "klientu ieteikumu" sarakstu.</span><span class="sxs-lookup"><span data-stu-id="b2c70-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="b2c70-142">Sekojošajā attēlā ir parādīts "klientu ieteikumu" saraksts POS terminālī.</span><span class="sxs-lookup"><span data-stu-id="b2c70-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Klientu ieteikumu saraksts POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="b2c70-144">Lietot personalizāciju esošajiem ieteikumu sarakstiem</span><span class="sxs-lookup"><span data-stu-id="b2c70-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="b2c70-145">Mazumtirgotāji var piemērot personalizāciju esošajiem ieteikumu sarakstiem, piemēram, "Jaunas", "Populāri", "Pirktākās", "Cilvēkiem patīk arī" un "Bieži pirktas kopā".</span><span class="sxs-lookup"><span data-stu-id="b2c70-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="b2c70-146">Ja personalizācija tiek lietota esošajiem sarakstiem, vienumi, kurus iepriekš iegādājies pierakstījies lietotājs, tiek noņemti no šiem sarakstiem.</span><span class="sxs-lookup"><span data-stu-id="b2c70-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="b2c70-147">Gan anonīmajiem lietotājiem, gan lietotājiem, kas izvēlējās nesaņemt personalizētus ieteikumus, tiek parādītas esošo sarakstu noklusētās versijas.</span><span class="sxs-lookup"><span data-stu-id="b2c70-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="b2c70-148">Tāpēc mazumtirgotājiem nav manuāli jāuztur atsevišķas lapu iespējas.</span><span class="sxs-lookup"><span data-stu-id="b2c70-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="b2c70-149">Piemēram, pierakstījies lietotājs jau ir iegādājies melnu rokaspulksteni un brūnus darba zābakus, kas parādās "populāri-noklusējuma" sarakstā nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="b2c70-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="b2c70-150">Tāpēc lietotājs redzēs jaunas preces, nevis šīs preces, kā norādīts sarakstā "populāri — personalizēts".</span><span class="sxs-lookup"><span data-stu-id="b2c70-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Personalizācijas piemērošana](./media/applypersonalization.png)

<span data-ttu-id="b2c70-152">Lai piemērotu personalizāciju esošam rekomendāciju sarakstam Commerce vietnes noformētājā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="b2c70-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2c70-153">Atveriet esošu vietnes noformētāja lapu, kas satur preču ievākšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="b2c70-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="b2c70-154">Navigācijas rūtī kreisajā pusē atlasiet produkta ievākšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="b2c70-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="b2c70-155">Navigācijas rūtī labajā pusē sadaļā **Preces** atlasiet sarakstu.</span><span class="sxs-lookup"><span data-stu-id="b2c70-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="b2c70-156">Dialoglodziņā **Atlasīt preču saraksta konfigurāciju** sadaļā **Veids**atlasiet saraksta veidu.</span><span class="sxs-lookup"><span data-stu-id="b2c70-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="b2c70-157">Atzīmējiet izvēles rūtiņu **Piemērot personalizāciju** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b2c70-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Personalizācijas piemērošana populāru preču sarakstam](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="b2c70-159">Saglabājiet lapu, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="b2c70-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="b2c70-160">Kad lapa ir publicēta, pierakstītie lietotāji redzēs personalizētus populāru preču sarakstus.</span><span class="sxs-lookup"><span data-stu-id="b2c70-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2c70-161">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b2c70-161">Additional resources</span></span>

[<span data-ttu-id="b2c70-162">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="b2c70-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b2c70-163">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="b2c70-163">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b2c70-164">VDAR un preču ieteikumi</span><span class="sxs-lookup"><span data-stu-id="b2c70-164">GDPR and product recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b2c70-165">Preču ieteikumu sarakstu pievienošana lapām</span><span class="sxs-lookup"><span data-stu-id="b2c70-165">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b2c70-166">Ieteikumu paneļa pievienošana POS ierīcēm</span><span class="sxs-lookup"><span data-stu-id="b2c70-166">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b2c70-167">Preču kolekcijas moduļa apskats</span><span class="sxs-lookup"><span data-stu-id="b2c70-167">Product collection module overview</span></span>](product-collection-module-overview.md)
