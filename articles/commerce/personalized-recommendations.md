---
title: Preču personalizētu ieteikumu iespējošana
description: Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f535cf0bc3c733426af22cf453ffe97f721f8d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000587"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="a1f7e-103">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="a1f7e-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1f7e-104">Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a1f7e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a1f7e-105">Overview</span></span>

<span data-ttu-id="a1f7e-106">Sistēmā Dynamics 365 Commerce mazumtirgotāji var padarīt personalizētus produktu ieteikumus (sauktus arī par personalizēšanu) pieejamus.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="a1f7e-107">Šādā veidā personificētus ieteikumus var iekļaut klientu tiešsaistes pieredzē un pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="a1f7e-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="a1f7e-108">Kad personalizācijas funkcionalitāte ir ieslēgta, sistēma var saistīt lietotāja pirkuma un preces informāciju, lai ģenerētu individualizētus preces ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="a1f7e-109">Personalizācijas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="a1f7e-109">Personalization prerequisites</span></span>

<span data-ttu-id="a1f7e-110">Pirms padarīt personalizētus preču ieteikumus pieejamus klientiem, ņemiet vērā, ka preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri migrēja to glabāšanu Azure Data Lake veikalā.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="a1f7e-111">Pirms klienti var saņemt personalizētus preču ieteikumus, mazumtirgotājiem ir [jāaktivizē preču ieteikumi](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a1f7e-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a1f7e-112">Ieslēdzot preču ieteikumus, varat ieslēgt arī personalizāciju.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="a1f7e-113">Tomēr, izslēdzot personalizāciju, netiek izslēgti citi preču ieteikumu veidi.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="a1f7e-114">Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a1f7e-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="a1f7e-115">Personalizācijas aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="a1f7e-115">Turn on personalization</span></span>

<span data-ttu-id="a1f7e-116">Lai aktivizētu personalizāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="a1f7e-117">Programmā Commerce Headquarters meklējiet **Funkciju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="a1f7e-118">Atlasiet **Visi**, lai skatītu pieejamo funkciju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="a1f7e-119">Meklēšanas lodziņā ievadiet **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="a1f7e-120">Atlasiet līdzekli **Personalizēto preču ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="a1f7e-121">**Personalizēto preču ieteikumi** rekvizītu rūtī atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Personalizācijas aktivizēšana](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="a1f7e-123">Ieslēdzot personalizāciju, tiek sākts personalizētu preču ieteikumu saraksta ģenerēšanas process.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="a1f7e-124">Var tikt pieprasīta līdz vienai dienai, pirms šie saraksti ir pieejami un redzami tiešsaistē un POS.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="a1f7e-125">Personalizēti saraksti</span><span class="sxs-lookup"><span data-stu-id="a1f7e-125">Personalized lists</span></span>

<span data-ttu-id="a1f7e-126">Līdztekus iespējai personalizēt esošus automātiski ģenerētus sarakstus, ieteikumu pakalpojums ļauj personalizēt produktu atklāšanas pieredzi gan tiešsaistē, gan POS.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="a1f7e-127">Pēc personalizācija ir ieslēgta, tirgotāji var rādīt pircējiem personalizētus "ieteikumu" sarakstus tiešsaistē vai "ieteicams klientam" sarakstiem POS termināļos.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="a1f7e-128">Turklāt mazumtirgotāji var piemērot personalizāciju esošajiem preču ieteikumu sarakstiem un nodrošināt Vispārējās datu aizsardzības regulas (VDAR) atteikšanās pieredzi autentificētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="a1f7e-129">Izslēdzot personalizāciju, arī šie līdzekļi tiek izslēgti.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="a1f7e-130">Tiešsaistes "ieteikumu" saraksti</span><span class="sxs-lookup"><span data-stu-id="a1f7e-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="a1f7e-131">"Tiešsaistes" saraksts ir mākslīgā intelekta, datormācīšanās (AI-ML) saraksts, kas parāda autentificētam lietotājam personalizētu ieteikto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="a1f7e-132">Šis saraksts ir balstīts uz lietotāja universālā kanāla pirkšanas vēsturi.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="a1f7e-133">Personalizētie ieteikumi tiek dinamiski atjaunināti, kad lietotājs veic vairāk pirkumu.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="a1f7e-134">Šis saraksta veids atbalsta arī kategoriju filtrēšanu, lai mazumtirgotāji varētu rādīt populārākos ieteikumus, pamatojoties uz navigācijas hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="a1f7e-135">Pirms "ieteikumu" sarakstu var parādīt jebkurā e-komercijas lapā, ir jāizpilda šādas lietotāju prasības:</span><span class="sxs-lookup"><span data-stu-id="a1f7e-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="a1f7e-136">Lietotājiem ir jāpiesakās sistēmā.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-136">Users must be signed in.</span></span> <span data-ttu-id="a1f7e-137">Anonīmie lietotāji neredzēs personalizētus ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="a1f7e-138">Lietotājiem ir jābūt vismaz vienam pirkumam viņu kontā.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="a1f7e-139">Lietotājiem ir jāizvēlas saņemt personalizētus ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="a1f7e-140">Sekojošajā attēlā ir parādīts saraksts "ieteikumu" saraksts tiešsaistes veikala lapā.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Tiešsaistes "ieteikumu" saraksts](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="a1f7e-142">"Klientu ieteikumu" saraksti POS</span><span class="sxs-lookup"><span data-stu-id="a1f7e-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="a1f7e-143">Lai uzlabotu savu klientu apkalpošanas pieredzi, mazumtirgotāji var personalizēt esošās detalizētās informācijas lapas par klientiem, pievienojot kontekstuālo "klientu ieteikumu" sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="a1f7e-144">Sekojošajā attēlā ir parādīts "klientu ieteikumu" saraksts POS terminālī.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Klientu ieteikumu saraksts POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="a1f7e-146">Lietot personalizāciju esošajiem ieteikumu sarakstiem</span><span class="sxs-lookup"><span data-stu-id="a1f7e-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="a1f7e-147">Mazumtirgotāji var piemērot personalizāciju esošajiem ieteikumu sarakstiem, piemēram, "Jaunas", "Populāri", "Pirktākās", "Cilvēkiem patīk arī" un "Bieži pirktas kopā".</span><span class="sxs-lookup"><span data-stu-id="a1f7e-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="a1f7e-148">Ja personalizācija tiek lietota esošajiem sarakstiem, vienumi, kurus iepriekš iegādājies pierakstījies lietotājs, tiek noņemti no šiem sarakstiem.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="a1f7e-149">Gan anonīmajiem lietotājiem, gan lietotājiem, kas izvēlējās nesaņemt personalizētus ieteikumus, tiek parādītas esošo sarakstu noklusētās versijas.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="a1f7e-150">Tāpēc mazumtirgotājiem nav manuāli jāuztur atsevišķas lapu iespējas.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="a1f7e-151">Piemēram, pierakstījies lietotājs jau ir iegādājies melnu rokaspulksteni un brūnus darba zābakus, kas parādās "populāri-noklusējuma" sarakstā nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="a1f7e-152">Tāpēc lietotājs redzēs jaunas preces, nevis šīs preces, kā norādīts sarakstā "populāri — personalizēts".</span><span class="sxs-lookup"><span data-stu-id="a1f7e-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Personalizācijas piemērošana](./media/applypersonalization.png)

<span data-ttu-id="a1f7e-154">Lai piemērotu personalizāciju esošam rekomendāciju sarakstam Commerce vietnes noformētājā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a1f7e-155">Atveriet esošu vietnes noformētāja lapu, kas satur preču ievākšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="a1f7e-156">Navigācijas rūtī kreisajā pusē atlasiet produkta ievākšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="a1f7e-157">Navigācijas rūtī labajā pusē sadaļā **Preces** atlasiet sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="a1f7e-158">Dialoglodziņā **Atlasīt preču saraksta konfigurāciju** sadaļā **Veids** atlasiet saraksta veidu.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="a1f7e-159">Atzīmējiet izvēles rūtiņu **Piemērot personalizāciju** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Personalizācijas piemērošana populāru preču sarakstam](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="a1f7e-161">Saglabājiet lapu, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="a1f7e-162">Kad lapa ir publicēta, pierakstītie lietotāji redzēs personalizētus populāru preču sarakstus.</span><span class="sxs-lookup"><span data-stu-id="a1f7e-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1f7e-163">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a1f7e-163">Additional resources</span></span>

[<span data-ttu-id="a1f7e-164">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="a1f7e-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a1f7e-165">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a1f7e-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a1f7e-166">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="a1f7e-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a1f7e-167">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="a1f7e-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="a1f7e-168">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="a1f7e-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a1f7e-169">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="a1f7e-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a1f7e-170">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="a1f7e-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a1f7e-171">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="a1f7e-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a1f7e-172">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="a1f7e-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a1f7e-173">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="a1f7e-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a1f7e-174">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="a1f7e-174">Product recommendations FAQ</span></span>](faq-recommendations.md)
