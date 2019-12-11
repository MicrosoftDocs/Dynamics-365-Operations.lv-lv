---
title: Uz AI-ML balstītu preču ieteikumu rezultātu pārvaldība
description: Šajā tēmā izskaidrots, kā jūsu biznesam pielāgot preces ieteikumu rezultātus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML).
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770074"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="cba7c-103">Uz AI-ML balstītu preču ieteikumu rezultātu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="cba7c-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cba7c-104">Šajā tēmā izskaidrots, kā jūsu biznesam pielāgot preces ieteikumu rezultātus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML).</span><span class="sxs-lookup"><span data-stu-id="cba7c-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="cba7c-105">Pēc preču ieteikumu iespējošanas stāsies spēkā noklusējuma iestatījumi; šie parametri darbosies, lai varētu strādāt daudzām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="cba7c-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="cba7c-106">Ieteicams ieplānot kādu laiku, lai novērtētu, vai rezultāti atbilst preču pārdošanas kustībai.</span><span class="sxs-lookup"><span data-stu-id="cba7c-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="cba7c-107">Pirms atkārtotas testēšanas ieteicams dažas dienas novērtēt rezultātus pirms parametru mainīšanas pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="cba7c-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="cba7c-108">Ieteikumu saraksta parametru izprašana</span><span class="sxs-lookup"><span data-stu-id="cba7c-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="cba7c-109">Pirms mainīt parametrus, uzziniet, kā tie ietekmēs tālāk minētos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="cba7c-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="cba7c-110">Populāru preču saraksts</span><span class="sxs-lookup"><span data-stu-id="cba7c-110">Trending product list</span></span>

<span data-ttu-id="cba7c-111">Preču sarakstam **Populārs** ir divi parametri, ko var mainīt: ![Populāru preču saraksta noklusējuma parametru piemērs](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="cba7c-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="cba7c-112">**Iekļaut jaunas preces no pēdējām X dienām** — preces, kas ir pievienotas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai atlasītu preču kandidātus.</span><span class="sxs-lookup"><span data-stu-id="cba7c-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="cba7c-113">Attēla noklusētā vērtība norāda, ka preces, kas ir līdz 180 dienas vecas, var izmantot populāru preču sarakstā.</span><span class="sxs-lookup"><span data-stu-id="cba7c-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="cba7c-114">**Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces.</span><span class="sxs-lookup"><span data-stu-id="cba7c-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="cba7c-115">Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu populāru preču sarakstā.</span><span class="sxs-lookup"><span data-stu-id="cba7c-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="cba7c-116">Vispirktāko preču saraksts</span><span class="sxs-lookup"><span data-stu-id="cba7c-116">Best selling product list</span></span>

<span data-ttu-id="cba7c-117">Atkarībā no jūsu biznesa, vispirktākais var dot atšķirīgus rezultātus nekā populārs, kaut gan tie abi izmanto transakciju datus, lai pasūtītu preces.</span><span class="sxs-lookup"><span data-stu-id="cba7c-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="cba7c-118">Tā kā vispirktākajam nav izslēgšanas, pamatojoties uz sortimenta datumu, vispirktākais joprojām var izcelt ļoti populāras, vecākās preces, kas var būt izmestas no populāro preču saraksta.</span><span class="sxs-lookup"><span data-stu-id="cba7c-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="cba7c-119">Preču sarakstam **Vispirktākais** ir viens parametrs, ko var mainīt.</span><span class="sxs-lookup"><span data-stu-id="cba7c-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Vispirktāko preču saraksta noklusējuma parametra piemērs](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="cba7c-121">**Iekļaut pārdošanu no pēdējām X dienām** — pārdošanas transakcijas, kas notikušas noteiktu dienu skaitu pirms pašreizējā datuma, var izmantot, lai pasūtītu preces.</span><span class="sxs-lookup"><span data-stu-id="cba7c-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="cba7c-122">Iepriekš minētā noklusētā vērtība norāda, ka visi preces pirkumi, kas veikti pēdējo 30 dienu laikā, tiks izmantoti, lai noteiktu preces novietojumu vispirktāko preču sarakstā.</span><span class="sxs-lookup"><span data-stu-id="cba7c-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="cba7c-123">Preču manuāla pievienošana ieteikumu sarakstiem vai noņemšana no tiem</span><span class="sxs-lookup"><span data-stu-id="cba7c-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="cba7c-124">Sarakstiem Jauns, Populārs vai Vispirktākais</span><span class="sxs-lookup"><span data-stu-id="cba7c-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="cba7c-125">Dodieties uz **Mazumtirdzniecība** > **Preču ieteikumi** > **Ieteikuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="cba7c-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="cba7c-126">Mazumtirdzniecības koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="cba7c-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="cba7c-127">Atlasiet sarakstu, kuram pievienot vai noņemt preces.</span><span class="sxs-lookup"><span data-stu-id="cba7c-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="cba7c-128">Lai tabulai pievienotu preces, atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="cba7c-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="cba7c-129">Sadaļā preces kolonna meklējiet preci pēc **Nosaukums** vai **Preces numurs.**
![Piemērs preces meklēšanai preču sarakstā Jauns](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="cba7c-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="cba7c-130">Kolonnas rindas veidā atlasiet vienu no divām opcijām:</span><span class="sxs-lookup"><span data-stu-id="cba7c-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="cba7c-131">**Iekļaut** — forsē preci uz saraksta priekšgalu</span><span class="sxs-lookup"><span data-stu-id="cba7c-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="cba7c-132">**Izslēgt** — noņem preci no parādīšanās sarakstā ![Piemērs preces iekļaušanai vai izslēgšanai no preču saraksta Jauns](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="cba7c-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="cba7c-133">Mainot **Rādīšanas secība**, tiks mainīta secība, kādā prece, kas atzīmēta ar **Iekļaut**, parādīsies sarakstā.</span><span class="sxs-lookup"><span data-stu-id="cba7c-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="cba7c-134">Ja divām precēm ir tāda pati vērtība **Rādīšanas secība**, šo divu rezultātu galīgā secība var atšķirties no tās, kas ir birojā.</span><span class="sxs-lookup"><span data-stu-id="cba7c-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="cba7c-135">Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="cba7c-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="cba7c-136">Sarakstiem Pircējiem patīk vai Bieži iegādāts kopā</span><span class="sxs-lookup"><span data-stu-id="cba7c-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="cba7c-137">**Bieži iegādāts kopā** vai **Pircējiem patīk** sarakstu kontekstā mašīnmācība tiek izmantota, lai analizētu patērētāju pirkšanas paradumus un ieteiktu saistītās preces, kas parasti tiek iegādātas kopā, izveidojot unikālu sākuma preci.</span><span class="sxs-lookup"><span data-stu-id="cba7c-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="cba7c-138">**Sākuma prece** ir prece, kurai vēlaties ģenerēt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="cba7c-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="cba7c-139">Manuāli pielāgotu ieteikumu sarakstu kontekstā jūs pievienojat vai noņemat šīs preces rezultātus.</span><span class="sxs-lookup"><span data-stu-id="cba7c-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="cba7c-140">Veiciet tālāk minētās darbības, lai manuāli pievienotu vai noņemtu rezultātus sākuma precei.</span><span class="sxs-lookup"><span data-stu-id="cba7c-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="cba7c-141">Atlasiet **Sākuma prece**.</span><span class="sxs-lookup"><span data-stu-id="cba7c-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="cba7c-142">Kolonnā **Prece** meklējiet preci pēc **Nosaukums** vai **Preces numurs.**
![Piemērs preces meklēšanai sarakstā Bieži iegādāts kopā](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="cba7c-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="cba7c-143">Kolonnā **Rindas veids** atlasiet vienu no divām opcijām:</span><span class="sxs-lookup"><span data-stu-id="cba7c-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="cba7c-144">**Iekļaut** — forsē preci uz saraksta priekšgalu</span><span class="sxs-lookup"><span data-stu-id="cba7c-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="cba7c-145">**Izslēgt** — noņem preci no parādīšanās sarakstā</span><span class="sxs-lookup"><span data-stu-id="cba7c-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="cba7c-146">![Piemērs preces iekļaušanai vai izslēgšanai no saraksta Bieži iegādāts kopā](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="cba7c-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="cba7c-147">Lai noņemtu preces no tabulas: atlasiet noņemamo rindu un atlasiet Noņemt.</span><span class="sxs-lookup"><span data-stu-id="cba7c-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="cba7c-148">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cba7c-148">Additional resources</span></span>

[<span data-ttu-id="cba7c-149">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="cba7c-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="cba7c-150">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="cba7c-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="cba7c-151">Preču ieteikumu sarakstu pievienošana lapām</span><span class="sxs-lookup"><span data-stu-id="cba7c-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
