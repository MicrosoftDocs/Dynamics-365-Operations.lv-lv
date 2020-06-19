---
title: Preču ieteikumu apskats
description: Šajā tēmā ir sniegta vispārīga informācija par preču ieteikumiem. Preču ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, un pat tādas preces, kuras viņi sākotnēji neplānoja nopirkt.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1b01589322c26b6a7b69d1b992b03603f5f3d29a
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404352"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="6d21a-104">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="6d21a-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6d21a-105">Microsoft Dynamics 365 Commerce var izmantot, lai parādītu preces ieteikumus e-tirdzniecības vietnē un pārdošanas punkta (POS) ierīcē.</span><span class="sxs-lookup"><span data-stu-id="6d21a-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="6d21a-106">Preces ieteikumi ir preces, kas varētu interesēt klientu.</span><span class="sxs-lookup"><span data-stu-id="6d21a-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="6d21a-107">Ieteikumi ir balstīti uz citu klientu pirkšanas tendencēm citiem klientiem tiešsaistes un parastajos veikalos.</span><span class="sxs-lookup"><span data-stu-id="6d21a-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="6d21a-108">Preces ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, gūstot noderīgu pieredzi.</span><span class="sxs-lookup"><span data-stu-id="6d21a-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="6d21a-109">Papildu preču pārdošana un citu preču pārdošana var pat tikt izmantota, lai palīdzētu klientiem atrast papildu preces, ko viņi sākotnēji nebija iecerējuši pirkt.</span><span class="sxs-lookup"><span data-stu-id="6d21a-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="6d21a-110">Kad ieteikumi tiek izmantoti, lai uzlabotu preču atklāšanu, tie var izveidot vairāk pārvēršanas iespēju, palīdzēt palielināt pārdošanas ieņēmumus un pat palīdzēt uzlabot klientu apmierinātību un lojalitāti.</span><span class="sxs-lookup"><span data-stu-id="6d21a-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="6d21a-111">E-Commerce preces ieteikumi darbojas, plašā mērogā izmantojot Microsoft Recommendations mašīnmācības tehnoloģijas.</span><span class="sxs-lookup"><span data-stu-id="6d21a-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="6d21a-112">Recommendation pakalpojums</span><span class="sxs-lookup"><span data-stu-id="6d21a-112">Recommendation service</span></span>

<span data-ttu-id="6d21a-113">Preču ieteikumu pakalpojums izmanto mākslīgās izlūkošanas un mašīnu mācīšanās (AI-ML) tehnoloģijas, kas ir sekojošā veidā:</span><span class="sxs-lookup"><span data-stu-id="6d21a-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="6d21a-114">No Commerce operacionālās datu bāzes tiek izgūti Recommendation pakalpojumam nepieciešamā formāta dati, un šie dati tiek nosūtīti Azure Data Lake Storage vai elementu krātuvei.</span><span class="sxs-lookup"><span data-stu-id="6d21a-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="6d21a-115">Ieteikumu pakalpojums izmanto saglabātos datus, lai apmācītu ieteikumu modeļus sarakstiem **Pircējiem patīk arī**, **Bieži iegādāts kopā**, **Jauns**, **Vispirktākais** un **Populārs**.</span><span class="sxs-lookup"><span data-stu-id="6d21a-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="6d21a-116">Scenāriji</span><span class="sxs-lookup"><span data-stu-id="6d21a-116">Scenarios</span></span>

<span data-ttu-id="6d21a-117">Preču ieteikumi ir pieejami tālāk minētajiem POS scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="6d21a-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="6d21a-118">**Jebkurā veikala lapā, kas paredzēta pārlūkošanai vai kā mērķlapa e-tirdzniecībā:** ja klienti vai veikala partneri apmeklē veikala lapu, ieteikumu programma var ieteikt preces sarakstos **Jauns**, **Vispirktākais** un **Populārs**.</span><span class="sxs-lookup"><span data-stu-id="6d21a-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="6d21a-119">**Preces detalizētas informācijas lapā:** ja klienti vai veikala partneri apmeklē lapu **Preces detalizēta informācija**, ieteikumu programma iesaka papildu preces, kas arī iespējams tiks iegādātas.</span><span class="sxs-lookup"><span data-stu-id="6d21a-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="6d21a-120">Šīs preces parādās sarakstā **Pircējiem patīk arī**.</span><span class="sxs-lookup"><span data-stu-id="6d21a-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="6d21a-121">**Transakciju lapā vai izrakstīšanas lapā:** ieteikumu programma piedāvā preces, balstoties uz visu grozā esošo preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="6d21a-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="6d21a-122">Šie krājumi parādās sarakstā **Bieži iegādāts kopā**.</span><span class="sxs-lookup"><span data-stu-id="6d21a-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="6d21a-123">**Personalizētie ieteikumi:** Tirgotāji var nodrošināt pieteiktajiem klientiem personalizētu **ieteikumu** sarakstu līdztekus jaunajai funkcionalitātei, kas ļauj esošajiem saraksta scenārijiem tikt personalizētiem, pamatojoties uz šo klientu.</span><span class="sxs-lookup"><span data-stu-id="6d21a-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="6d21a-124">Lai uzzinātu vairāk, skatiet [Personalizētu ieteikumu iespējošana](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="6d21a-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="6d21a-125">Preču ieteikumu veidi</span><span class="sxs-lookup"><span data-stu-id="6d21a-125">Types of product recommendations</span></span>

<span data-ttu-id="6d21a-126">Sekojošajā tabulā ir aprakstīti dažādi automatizēto preču ieteikumu veidi, kas pieejami mazumtirgotājiem risinājumā Dynamics 365 Commerce, lai to varētu ieviest, izmantojot [preču kolekcijas moduli](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6d21a-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="6d21a-127">Mazumtirgotāji var parādīt lietotāja, kas ir pierakstījies, personalizētus rezultātus, ja vietnes autors izvēlas šo opciju.</span><span class="sxs-lookup"><span data-stu-id="6d21a-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="6d21a-128">Preču kolekcijas modulis</span><span class="sxs-lookup"><span data-stu-id="6d21a-128">Product collection module</span></span>  | <span data-ttu-id="6d21a-129">tips</span><span class="sxs-lookup"><span data-stu-id="6d21a-129">Type</span></span> | <span data-ttu-id="6d21a-130">apraksts</span><span class="sxs-lookup"><span data-stu-id="6d21a-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="6d21a-131">Jauna</span><span class="sxs-lookup"><span data-stu-id="6d21a-131">New</span></span>                        | <span data-ttu-id="6d21a-132">Algoritmisks</span><span class="sxs-lookup"><span data-stu-id="6d21a-132">Algorithmic</span></span> | <span data-ttu-id="6d21a-133">Šis modulis rāda sarakstu ar jaunākajām precēm, kas ir nesen sašķirotas kanālos un katalogos.</span><span class="sxs-lookup"><span data-stu-id="6d21a-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="6d21a-134">Vispirktākais</span><span class="sxs-lookup"><span data-stu-id="6d21a-134">Best selling</span></span>               | <span data-ttu-id="6d21a-135">Algoritmisks</span><span class="sxs-lookup"><span data-stu-id="6d21a-135">Algorithmic</span></span> | <span data-ttu-id="6d21a-136">Šis modulis rāda preču sarakstu, kas ir sarindotas pēc lielākā pārdošanas apjoma.</span><span class="sxs-lookup"><span data-stu-id="6d21a-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="6d21a-137">Populāri</span><span class="sxs-lookup"><span data-stu-id="6d21a-137">Trending</span></span>                   | <span data-ttu-id="6d21a-138">Algoritmisks</span><span class="sxs-lookup"><span data-stu-id="6d21a-138">Algorithmic</span></span> | <span data-ttu-id="6d21a-139">Šis preču kolekcijas moduļa veids parāda preču ar augstāku veiktspēju sarakstu noteiktā periodā, sarindota pēc lielākā pārdošanas skaita.</span><span class="sxs-lookup"><span data-stu-id="6d21a-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="6d21a-140">Bieži iegādāti kopā</span><span class="sxs-lookup"><span data-stu-id="6d21a-140">Frequently bought together</span></span> | <span data-ttu-id="6d21a-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="6d21a-141">AI-ML</span></span> | <span data-ttu-id="6d21a-142">Šis modulis rekomendē sarakstu ar ieteiktajiem produktiem, kuri parasti tiek iegādāti kopā ar patērētāja pašreizējā groza saturu.</span><span class="sxs-lookup"><span data-stu-id="6d21a-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="6d21a-143">Cilvēkiem patīk arī</span><span class="sxs-lookup"><span data-stu-id="6d21a-143">People also like</span></span>           | <span data-ttu-id="6d21a-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="6d21a-144">AI-ML</span></span> | <span data-ttu-id="6d21a-145">Šis modulis iesaka preces noteiktam sēklas produktam, pamatojoties uz patēriņa pirkšanas modeļiem.</span><span class="sxs-lookup"><span data-stu-id="6d21a-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="6d21a-146">Ieteikumi</span><span class="sxs-lookup"><span data-stu-id="6d21a-146">Picks for you</span></span>              | <span data-ttu-id="6d21a-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="6d21a-147">AI-ML</span></span> | <span data-ttu-id="6d21a-148">Šis modulis rekomendē personificētu preču sarakstu, pamatojoties uz pierakstītā lietotāja pirkšanas modeļiem.</span><span class="sxs-lookup"><span data-stu-id="6d21a-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="6d21a-149">Lietotājam-viesim šis saraksts tiks sakļauts.</span><span class="sxs-lookup"><span data-stu-id="6d21a-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="6d21a-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6d21a-150">Additional resources</span></span>

[<span data-ttu-id="6d21a-151">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6d21a-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="6d21a-152">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="6d21a-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6d21a-153">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="6d21a-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="6d21a-154">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="6d21a-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="6d21a-155">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="6d21a-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="6d21a-156">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="6d21a-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="6d21a-157">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="6d21a-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="6d21a-158">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="6d21a-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6d21a-159">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="6d21a-159">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="6d21a-160">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="6d21a-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
