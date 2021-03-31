---
title: Bieži uzdotie jautājumi par preču ieteikumiem
description: Šajā tēmā sniegta informācija par procesiem un rīkiem, ko varat izmantot, lai meklētu traucējumus problēmās, kas saistītas ar preču ieteikumiem vai to rezultātiem.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f0140f798e000ca66c67afa00f788abc560c8a07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216703"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="bab28-103">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="bab28-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bab28-104">Šajā tēmā sniegta informācija par procesiem un rīkiem, ko varat izmantot, lai meklētu traucējumus problēmās, kas saistītas ar [preču ieteikumiem](product-recommendations.md) vai to rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="bab28-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="bab28-105">Labākās prakses</span><span class="sxs-lookup"><span data-stu-id="bab28-105">Best practices</span></span>
<span data-ttu-id="bab28-106">Ir ļoti svarīgi izmantot preces šablonu un variantu koncepciju.</span><span class="sxs-lookup"><span data-stu-id="bab28-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="bab28-107">Saprātīga variantu grupēšana pamata preces šablonā palīdz saraksta algoritmam un pakalpojumam izveidot labākus modeļus.</span><span class="sxs-lookup"><span data-stu-id="bab28-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="bab28-108">Turklāt pakalpojumu var izmantot tikai vienam preces gadījumam, nevis ievietojot sarakstā visus cieši saistītos variantus.</span><span class="sxs-lookup"><span data-stu-id="bab28-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="bab28-109">Kad visi cieši saistītie varianti tiek ievietoti sarakstā, var rasties kļūdaini vai dubulti rezultāti.</span><span class="sxs-lookup"><span data-stu-id="bab28-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="bab28-110">Kāpēc manos ieteikumu sarakstos trūkst preces?</span><span class="sxs-lookup"><span data-stu-id="bab28-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="bab28-111">Parasti, ja preču ieteikumu sarakstā trūkst preces, iespējama preces konfigurācijas problēma.</span><span class="sxs-lookup"><span data-stu-id="bab28-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="bab28-112">Piemēram, iespējams, ka ir nepareizs preces sākuma vai beigu datums, ir nepareizi konfigurēta dimensija vai arī prece nav pareizā kanāla klāstā utt.</span><span class="sxs-lookup"><span data-stu-id="bab28-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="bab28-113">Ja preces trūkst ieteikumu sarakstā, kas balstīts uz mākslīgo intelektu – mašīnmācību (AI-ML), iespējams, prece neatbilst ieteikumu saraksta kritērijiem, vai arī tai var nebūt pietiekami daudz pirkšanas transakciju, lai ieteikumu saraksts to parādītu.</span><span class="sxs-lookup"><span data-stu-id="bab28-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="bab28-114">Ieteicams pārbaudīt tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="bab28-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="bab28-115">**Pārliecinieties, vai HQ ir iespējoti preces ieteikumi.**</span><span class="sxs-lookup"><span data-stu-id="bab28-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="bab28-116">Lai iegūtu vairāk informācijas par to, kā iespējot šo pakalpojumu, skatiet [Preču ieteikumu iespējošana](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="bab28-117">**Pārliecinieties, vai ir iestatīti galvenie preces rekvizīti.**</span><span class="sxs-lookup"><span data-stu-id="bab28-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="bab28-118">Piemēram, preču klāsts ir jāiestata uz **Iekļauts**.</span><span class="sxs-lookup"><span data-stu-id="bab28-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="bab28-119">**No jauna sašķirotām precēm var paiet līdz pat 3 stundām pirms prece sāks parādīties jaunajā sarakstā.**</span><span class="sxs-lookup"><span data-stu-id="bab28-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="bab28-120">**Ja prece joprojām neparādās kategorijās "Populārs", "Vispirktākais", "Pircējiem patīk arī" vai "Bieži iegādāts kopā", tad šai precei, iespējams, nav pietiekami daudz transakciju.**</span><span class="sxs-lookup"><span data-stu-id="bab28-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="bab28-121">Šādā gadījumā varat vai nu gaidīt, kamēr tiks veikts vairāk transakciju, atjaunināt noklusējuma ieteikumu saraksta parametrus vai izmantot manuālu iejaukšanos, lai modificētu ieteikuma preču saraksta rezultātus.</span><span class="sxs-lookup"><span data-stu-id="bab28-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="bab28-122">Lai iegūtu vairāk informācijas par ieteikumu parametriem, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="bab28-123">**Pārliecinieties, vai prece atbilst saraksta ieteikumu kritērijiem.**</span><span class="sxs-lookup"><span data-stu-id="bab28-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="bab28-124">Lai iegūtu vairāk informācijas par preces ieteikumu parametriem, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="bab28-125">Kā iespējams novērst sliktu ieteikumu rezultātu atgriešanu?</span><span class="sxs-lookup"><span data-stu-id="bab28-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="bab28-126">Lai iegūtu rezultātus, ieteikumu sarakstiem ir nepieciešama liela apjoma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="bab28-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="bab28-127">Tāpēc ir svarīgi, ka lietotāji sniedz visus vēsturiskos transakciju datus.</span><span class="sxs-lookup"><span data-stu-id="bab28-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="bab28-128">Turklāt preces, kurām nav nevienas transakcijas vai tikai dažas transakcijas, parasti nav **Pircējiem patīk arī** vai **Bieži iegādāts kopā** rezultātos, un neparādās **Populārs** vai **Vispirktākais** ieteikumu sarakstos.</span><span class="sxs-lookup"><span data-stu-id="bab28-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="bab28-129">Šī situācija bieži var rasties ļoti jaunām precēm vai arī vecām precēm, kurām ir neliels pirkumu skaits.</span><span class="sxs-lookup"><span data-stu-id="bab28-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="bab28-130">Populāras jaunas preces viegli pārvarēs šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="bab28-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="bab28-131">Ieteicams veikt tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="bab28-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="bab28-132">**Pārliecinieties, vai prece atbilst šī saraksta ieteikumu kritērijiem.**</span><span class="sxs-lookup"><span data-stu-id="bab28-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="bab28-133">Lai iegūtu vairāk informācijas par preces ieteikumu parametriem, skatiet uz AI-ML balstītu ieteikumu rezultātu modificēšana.</span><span class="sxs-lookup"><span data-stu-id="bab28-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="bab28-134">**Ja prece ir jauna, apsveriet iespēju modificēt ieteikumu sarakstu, līdz precei būs vairāk transakciju.**</span><span class="sxs-lookup"><span data-stu-id="bab28-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="bab28-135">Lai iegūtu vairāk informācijas par to, kā modificēt ieteikumu saraksta rezultātus, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="bab28-136">**Pārliecinieties, vai prece atbilst šī saraksta ieteikumu kritērijiem.**</span><span class="sxs-lookup"><span data-stu-id="bab28-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="bab28-137">Lai iegūtu vairāk informācijas par preces ieteikumu parametriem, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="bab28-138">**Ja prece ir jauna, apsveriet iespēju modificēt ieteikumu sarakstu, līdz precei būs vairāk transakciju**.</span><span class="sxs-lookup"><span data-stu-id="bab28-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="bab28-139">Lai iegūtu vairāk informācijas par to, kā modificēt ieteikumu saraksta rezultātus, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="bab28-140">Vai preci var noņemt, bet joprojām to redzēt veikalā?</span><span class="sxs-lookup"><span data-stu-id="bab28-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="bab28-141">Varat pielāgot algoritmiski ģenerētus sarakstus, ja biznesam pēc tā rodas nepieciešamība.</span><span class="sxs-lookup"><span data-stu-id="bab28-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="bab28-142">Tomēr, ja prece ir noņemta no ieteikumu saraksta, prece paliks redzama veikalā.</span><span class="sxs-lookup"><span data-stu-id="bab28-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="bab28-143">Lai iegūtu vairāk informācijas par to, kā modificēt preču ieteikumu rezultātus, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="bab28-144">Ja ir jāaiztur prece, lai to nevarētu redzēt veikalā, vērtība **Preču sortiments** jāmaina uz **Izslēgt**.</span><span class="sxs-lookup"><span data-stu-id="bab28-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="bab28-145">Kā pievienot sarakstu e-tirdzniecības lapai?</span><span class="sxs-lookup"><span data-stu-id="bab28-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="bab28-146">Lai iegūtu informāciju par to, kā pievienot preču ieteikumu lapas savai e-tirdzniecības tīmekļa lapai, skatiet [Preču ieteikumu sarakstu pievienošana lapām](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="bab28-147">Kā iespējot ieteikumus POS?</span><span class="sxs-lookup"><span data-stu-id="bab28-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="bab28-148">Pēc preču ieteikumu iespējošanas kontroles POS ekrānam ir jāpievieno ieteikumu panelis.</span><span class="sxs-lookup"><span data-stu-id="bab28-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="bab28-149">Papildinformācijai skatiet [Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bab28-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bab28-150">Additional resources</span></span>

[<span data-ttu-id="bab28-151">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="bab28-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="bab28-152">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bab28-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="bab28-153">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="bab28-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="bab28-154">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="bab28-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="bab28-155">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="bab28-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="bab28-156">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="bab28-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="bab28-157">Preču ieteikumu pievienošana punktā POS</span><span class="sxs-lookup"><span data-stu-id="bab28-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="bab28-158">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="bab28-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="bab28-159">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="bab28-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="bab28-160">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="bab28-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="bab28-161">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="bab28-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]