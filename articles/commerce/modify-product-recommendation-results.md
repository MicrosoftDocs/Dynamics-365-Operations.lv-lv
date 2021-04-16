---
title: Uz AI-ML balstītu preču ieteikumu rezultātu pielāgošana
description: Šajā tēmā izskaidrots, kā jūsu biznesam pielāgot preces ieteikumu rezultātus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML).
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfe04881e71558ed326025d8f2545c3c611df3aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796974"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="483ab-103">Uz AI-ML balstītu preču ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="483ab-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="483ab-104">Šajā tēmā izskaidrots, kā jūsu biznesam pielāgot preces ieteikumu rezultātus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML).</span><span class="sxs-lookup"><span data-stu-id="483ab-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="483ab-105">Pēc preču ieteikumu iespējošanas stāsies spēkā noklusējuma iestatījumi; šie parametri darbosies, lai varētu strādāt daudzām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="483ab-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="483ab-106">Ieteicams ieplānot kādu laiku, lai novērtētu, vai rezultāti atbilst preču pārdošanas kustībai.</span><span class="sxs-lookup"><span data-stu-id="483ab-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="483ab-107">Pirms atkārtotas testēšanas ieteicams dažas dienas novērtēt rezultātus pirms parametru mainīšanas pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="483ab-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="483ab-108">Ieteikumu saraksta parametru izprašana</span><span class="sxs-lookup"><span data-stu-id="483ab-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="483ab-109">Pirms mainīt parametrus, uzziniet, kā tie ietekmēs tālāk minētos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="483ab-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="483ab-110">"Populāru" preču saraksts</span><span class="sxs-lookup"><span data-stu-id="483ab-110">"Trending" product list</span></span>

<span data-ttu-id="483ab-111">"Populāru" preču sarakstam ir divi maināmi parametri:</span><span class="sxs-lookup"><span data-stu-id="483ab-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Saraksta "Populāras" noklusējuma parametru piemērs](./media/exampletrendingparameters.png)

1. <span data-ttu-id="483ab-113">**Iekļaut jaunas preces no pēdējām X dienām** — preces, kas ir pievienotas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai atlasītu preču kandidātus.</span><span class="sxs-lookup"><span data-stu-id="483ab-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="483ab-114">Attēla noklusētā vērtība norāda, ka preces, kas ir līdz 180 dienas vecas, var izmantot populāru preču sarakstā.</span><span class="sxs-lookup"><span data-stu-id="483ab-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="483ab-115">**Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces.</span><span class="sxs-lookup"><span data-stu-id="483ab-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="483ab-116">Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu populāru preču sarakstā.</span><span class="sxs-lookup"><span data-stu-id="483ab-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="483ab-117">"Vispirktāko" preču saraksts</span><span class="sxs-lookup"><span data-stu-id="483ab-117">"Best selling" product list</span></span>

<span data-ttu-id="483ab-118">Atkarībā no jūsu biznesa, sarakts "Vispirktākās" var dot atšķirīgus rezultātus nekā populāro preču sarakstus, kaut gan tie abi izmanto transakciju datus, lai pasūtītu preces.</span><span class="sxs-lookup"><span data-stu-id="483ab-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="483ab-119">Tā kā vispirktākajam nav izslēgšanas, pamatojoties uz sortimenta datumu, vispirktākais joprojām var izcelt ļoti populāras, vecākās preces, kas var būt izmestas no populāro preču saraksta.</span><span class="sxs-lookup"><span data-stu-id="483ab-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="483ab-120">Preču sarakstam "Vispirktākās" ir viens parametrs, ko var mainīt.</span><span class="sxs-lookup"><span data-stu-id="483ab-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Vispirktāko preču saraksta noklusējuma parametra piemērs](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="483ab-122">**Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces.</span><span class="sxs-lookup"><span data-stu-id="483ab-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="483ab-123">Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu vispirktāko preču sarakstā.</span><span class="sxs-lookup"><span data-stu-id="483ab-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="483ab-124">Preču manuāla pievienošana ieteikumu sarakstiem vai noņemšana no tiem</span><span class="sxs-lookup"><span data-stu-id="483ab-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="483ab-125">Sarakstiem "Jaunas", "Populāras" vai "Vispirktākās"</span><span class="sxs-lookup"><span data-stu-id="483ab-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="483ab-126">Pārejiet uz **Retail un Commerce** > **Preču ieteikumi** > **Ieteikumu parametri**.</span><span class="sxs-lookup"><span data-stu-id="483ab-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="483ab-127">Koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="483ab-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="483ab-128">Atlasiet sarakstu, kuram pievienot vai noņemt preces.</span><span class="sxs-lookup"><span data-stu-id="483ab-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="483ab-129">Lai tabulai pievienotu preces, atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="483ab-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="483ab-130">Sadaļā Preces kolonna meklējiet preci pēc **Nosaukuma** vai **Preces numura.**</span><span class="sxs-lookup"><span data-stu-id="483ab-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Piemērs preces meklēšanai sarakstā Jauna prece](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="483ab-132">Kolonnas rindas veidā atlasiet vienu no divām opcijām:</span><span class="sxs-lookup"><span data-stu-id="483ab-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="483ab-133">**Iekļaut** — forsē preci uz saraksta priekšgalu</span><span class="sxs-lookup"><span data-stu-id="483ab-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="483ab-134">**Izslēgt** — noņem preci no parādīšanās sarakstā</span><span class="sxs-lookup"><span data-stu-id="483ab-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Piemērs preces iekļaušanai vai izņemšanai no Jaunas preces saraksta](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="483ab-136">Mainot **Rādīšanas secība**, tiks mainīta secība, kādā prece, kas atzīmēta ar **Iekļaut**, parādīsies sarakstā.</span><span class="sxs-lookup"><span data-stu-id="483ab-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="483ab-137">Ja divām precēm ir tāda pati vērtība **Rādīšanas secība**, šo divu rezultātu galīgā secība var atšķirties no tās, kas ir birojā.</span><span class="sxs-lookup"><span data-stu-id="483ab-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="483ab-138">Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="483ab-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="483ab-139">Sarakstiem "Pircējiem patīk" vai "Bieži iegādāts kopā"</span><span class="sxs-lookup"><span data-stu-id="483ab-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="483ab-140">"Bieži iegādāts kopā" vai "Pircējiem patīk" sarakstu kontekstā mašīnmācība tiek izmantota, lai analizētu patērētāju pirkšanas paradumus un ieteiktu saistītās preces, kas parasti tiek iegādātas kopā, izveidojot unikālu sākuma preci.</span><span class="sxs-lookup"><span data-stu-id="483ab-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="483ab-141">*Sākuma prece* ir prece, kurai vēlaties ģenerēt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="483ab-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="483ab-142">Manuāli pielāgotu ieteikumu sarakstu kontekstā jūs pievienojat vai noņemat šīs preces rezultātus.</span><span class="sxs-lookup"><span data-stu-id="483ab-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="483ab-143">Veiciet tālāk minētās darbības, lai manuāli pievienotu vai noņemtu rezultātus sākuma precei.</span><span class="sxs-lookup"><span data-stu-id="483ab-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="483ab-144">Atlasiet **Sākuma prece**.</span><span class="sxs-lookup"><span data-stu-id="483ab-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="483ab-145">Kolonnā **Prece** meklējiet preci pēc **Nosaukums** vai **Preces numurs.**
![Piemērs preces meklēšanai sarakstā Bieži iegādāts kopā](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="483ab-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="483ab-146">Kolonnā **Rindas veids** atlasiet vienu no divām opcijām:</span><span class="sxs-lookup"><span data-stu-id="483ab-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="483ab-147">**Iekļaut** — forsē preci uz saraksta priekšgalu</span><span class="sxs-lookup"><span data-stu-id="483ab-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="483ab-148">**Izslēgt** — noņem preci no parādīšanās sarakstā</span><span class="sxs-lookup"><span data-stu-id="483ab-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="483ab-149">![Piemērs preces iekļaušanai vai izslēgšanai no saraksta Bieži iegādāts kopā](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="483ab-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="483ab-150">Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet Noņemt.</span><span class="sxs-lookup"><span data-stu-id="483ab-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="483ab-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="483ab-151">Additional resources</span></span>

[<span data-ttu-id="483ab-152">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="483ab-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="483ab-153">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="483ab-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="483ab-154">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="483ab-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="483ab-155">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="483ab-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="483ab-156">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="483ab-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="483ab-157">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="483ab-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="483ab-158">Preču ieteikumu pievienošana punktā POS</span><span class="sxs-lookup"><span data-stu-id="483ab-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="483ab-159">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="483ab-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="483ab-160">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="483ab-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="483ab-161">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="483ab-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="483ab-162">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="483ab-162">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]