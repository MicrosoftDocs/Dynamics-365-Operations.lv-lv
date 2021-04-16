---
title: Preču personalizētu ieteikumu iespējošana
description: Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: dc0fbff437bfa948d70a03479561542106805bdb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804433"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="2e32c-103">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="2e32c-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2e32c-104">Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e32c-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2e32c-105">Sistēmā Dynamics 365 Commerce mazumtirgotāji var padarīt personalizētus produktu ieteikumus (sauktus arī par personalizēšanu) pieejamus.</span><span class="sxs-lookup"><span data-stu-id="2e32c-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="2e32c-106">Šādā veidā personificētus ieteikumus var iekļaut klientu tiešsaistes pieredzē un pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="2e32c-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="2e32c-107">Kad personalizācijas funkcionalitāte ir ieslēgta, sistēma var saistīt lietotāja pirkuma un preces informāciju, lai ģenerētu individualizētus preces ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="2e32c-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="2e32c-108">Personalizācijas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="2e32c-108">Personalization prerequisites</span></span>

<span data-ttu-id="2e32c-109">Pirms padarīt personalizētus preču ieteikumus pieejamus klientiem, ņemiet vērā, ka preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri migrēja to glabāšanu Azure Data Lake veikalā.</span><span class="sxs-lookup"><span data-stu-id="2e32c-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="2e32c-110">Pirms klienti var saņemt personalizētus preču ieteikumus, mazumtirgotājiem ir [jāaktivizē preču ieteikumi](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="2e32c-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2e32c-111">Ieslēdzot preču ieteikumus, varat ieslēgt arī personalizāciju.</span><span class="sxs-lookup"><span data-stu-id="2e32c-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="2e32c-112">Tomēr, izslēdzot personalizāciju, netiek izslēgti citi preču ieteikumu veidi.</span><span class="sxs-lookup"><span data-stu-id="2e32c-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="2e32c-113">Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="2e32c-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="2e32c-114">Personalizācijas aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="2e32c-114">Turn on personalization</span></span>

<span data-ttu-id="2e32c-115">Lai aktivizētu personalizāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="2e32c-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="2e32c-116">Programmā Commerce Headquarters meklējiet **Funkciju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="2e32c-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="2e32c-117">Atlasiet **Visi**, lai skatītu pieejamo funkciju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="2e32c-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="2e32c-118">Meklēšanas lodziņā ievadiet **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="2e32c-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="2e32c-119">Atlasiet līdzekli **Personalizēto preču ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="2e32c-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="2e32c-120">**Personalizēto preču ieteikumi** rekvizītu rūtī atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="2e32c-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Personalizācijas aktivizēšana](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="2e32c-122">Ieslēdzot personalizāciju, tiek sākts personalizētu preču ieteikumu saraksta ģenerēšanas process.</span><span class="sxs-lookup"><span data-stu-id="2e32c-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="2e32c-123">Var tikt pieprasīta līdz vienai dienai, pirms šie saraksti ir pieejami un redzami tiešsaistē un POS.</span><span class="sxs-lookup"><span data-stu-id="2e32c-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="2e32c-124">Personalizēti saraksti</span><span class="sxs-lookup"><span data-stu-id="2e32c-124">Personalized lists</span></span>

<span data-ttu-id="2e32c-125">Līdztekus iespējai personalizēt esošus automātiski ģenerētus sarakstus, ieteikumu pakalpojums ļauj personalizēt produktu atklāšanas pieredzi gan tiešsaistē, gan POS.</span><span class="sxs-lookup"><span data-stu-id="2e32c-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="2e32c-126">Pēc personalizācija ir ieslēgta, tirgotāji var rādīt pircējiem personalizētus "ieteikumu" sarakstus tiešsaistē vai "ieteicams klientam" sarakstiem POS termināļos.</span><span class="sxs-lookup"><span data-stu-id="2e32c-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="2e32c-127">Turklāt mazumtirgotāji var piemērot personalizāciju esošajiem preču ieteikumu sarakstiem un nodrošināt Vispārējās datu aizsardzības regulas (VDAR) atteikšanās pieredzi autentificētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="2e32c-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="2e32c-128">Izslēdzot personalizāciju, arī šie līdzekļi tiek izslēgti.</span><span class="sxs-lookup"><span data-stu-id="2e32c-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="2e32c-129">Tiešsaistes "ieteikumu" saraksti</span><span class="sxs-lookup"><span data-stu-id="2e32c-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="2e32c-130">"Tiešsaistes" saraksts ir mākslīgā intelekta, datormācīšanās (AI-ML) saraksts, kas parāda autentificētam lietotājam personalizētu ieteikto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="2e32c-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="2e32c-131">Šis saraksts ir balstīts uz lietotāja universālā kanāla pirkšanas vēsturi.</span><span class="sxs-lookup"><span data-stu-id="2e32c-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="2e32c-132">Personalizētie ieteikumi tiek dinamiski atjaunināti, kad lietotājs veic vairāk pirkumu.</span><span class="sxs-lookup"><span data-stu-id="2e32c-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="2e32c-133">Šis saraksta veids atbalsta arī kategoriju filtrēšanu, lai mazumtirgotāji varētu rādīt populārākos ieteikumus, pamatojoties uz navigācijas hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="2e32c-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="2e32c-134">Pirms "ieteikumu" sarakstu var parādīt jebkurā e-komercijas lapā, ir jāizpilda šādas lietotāju prasības:</span><span class="sxs-lookup"><span data-stu-id="2e32c-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="2e32c-135">Lietotājiem ir jāpiesakās sistēmā.</span><span class="sxs-lookup"><span data-stu-id="2e32c-135">Users must be signed in.</span></span> <span data-ttu-id="2e32c-136">Anonīmie lietotāji neredzēs personalizētus ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="2e32c-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="2e32c-137">Lietotājiem ir jābūt vismaz vienam pirkumam viņu kontā.</span><span class="sxs-lookup"><span data-stu-id="2e32c-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="2e32c-138">Lietotājiem ir jāizvēlas saņemt personalizētus ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="2e32c-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="2e32c-139">Sekojošajā attēlā ir parādīts saraksts "ieteikumu" saraksts tiešsaistes veikala lapā.</span><span class="sxs-lookup"><span data-stu-id="2e32c-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Tiešsaistes "ieteikumu" saraksts](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="2e32c-141">"Klientu ieteikumu" saraksti POS</span><span class="sxs-lookup"><span data-stu-id="2e32c-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="2e32c-142">Lai uzlabotu savu klientu apkalpošanas pieredzi, mazumtirgotāji var personalizēt esošās detalizētās informācijas lapas par klientiem, pievienojot kontekstuālo "klientu ieteikumu" sarakstu.</span><span class="sxs-lookup"><span data-stu-id="2e32c-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="2e32c-143">Sekojošajā attēlā ir parādīts "klientu ieteikumu" saraksts POS terminālī.</span><span class="sxs-lookup"><span data-stu-id="2e32c-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Klientu ieteikumu saraksts POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="2e32c-145">Lietot personalizāciju esošajiem ieteikumu sarakstiem</span><span class="sxs-lookup"><span data-stu-id="2e32c-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="2e32c-146">Mazumtirgotāji var piemērot personalizāciju esošajiem ieteikumu sarakstiem, piemēram, "Jaunas", "Populāri", "Pirktākās", "Cilvēkiem patīk arī" un "Bieži pirktas kopā".</span><span class="sxs-lookup"><span data-stu-id="2e32c-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="2e32c-147">Ja personalizācija tiek lietota esošajiem sarakstiem, vienumi, kurus iepriekš iegādājies pierakstījies lietotājs, tiek noņemti no šiem sarakstiem.</span><span class="sxs-lookup"><span data-stu-id="2e32c-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="2e32c-148">Gan anonīmajiem lietotājiem, gan lietotājiem, kas izvēlējās nesaņemt personalizētus ieteikumus, tiek parādītas esošo sarakstu noklusētās versijas.</span><span class="sxs-lookup"><span data-stu-id="2e32c-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="2e32c-149">Tāpēc mazumtirgotājiem nav manuāli jāuztur atsevišķas lapu iespējas.</span><span class="sxs-lookup"><span data-stu-id="2e32c-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="2e32c-150">Piemēram, pierakstījies lietotājs jau ir iegādājies melnu rokaspulksteni un brūnus darba zābakus, kas parādās "populāri-noklusējuma" sarakstā nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="2e32c-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="2e32c-151">Tāpēc lietotājs redzēs jaunas preces, nevis šīs preces, kā norādīts sarakstā "populāri — personalizēts".</span><span class="sxs-lookup"><span data-stu-id="2e32c-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Personalizācijas piemērošana](./media/applypersonalization.png)

<span data-ttu-id="2e32c-153">Lai piemērotu personalizāciju esošam rekomendāciju sarakstam Commerce vietnes noformētājā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="2e32c-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2e32c-154">Atveriet esošu vietnes noformētāja lapu, kas satur preču ievākšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="2e32c-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="2e32c-155">Navigācijas rūtī kreisajā pusē atlasiet produkta ievākšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="2e32c-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="2e32c-156">Navigācijas rūtī labajā pusē sadaļā **Preces** atlasiet sarakstu.</span><span class="sxs-lookup"><span data-stu-id="2e32c-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="2e32c-157">Dialoglodziņā **Atlasīt preču saraksta konfigurāciju** sadaļā **Veids** atlasiet saraksta veidu.</span><span class="sxs-lookup"><span data-stu-id="2e32c-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="2e32c-158">Atzīmējiet izvēles rūtiņu **Piemērot personalizāciju** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2e32c-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Personalizācijas piemērošana populāru preču sarakstam](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="2e32c-160">Saglabājiet lapu, pabeidziet to rediģēt un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="2e32c-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="2e32c-161">Kad lapa ir publicēta, pierakstītie lietotāji redzēs personalizētus populāru preču sarakstus.</span><span class="sxs-lookup"><span data-stu-id="2e32c-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e32c-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2e32c-162">Additional resources</span></span>

[<span data-ttu-id="2e32c-163">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="2e32c-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="2e32c-164">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2e32c-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="2e32c-165">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="2e32c-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="2e32c-166">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="2e32c-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="2e32c-167">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="2e32c-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="2e32c-168">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="2e32c-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="2e32c-169">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="2e32c-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="2e32c-170">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="2e32c-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="2e32c-171">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="2e32c-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="2e32c-172">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="2e32c-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="2e32c-173">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="2e32c-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
