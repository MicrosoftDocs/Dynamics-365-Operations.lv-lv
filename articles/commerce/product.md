---
title: Pievienot preču ieteikumi punktā POS
description: Šajā tēmā ir aprakstīts, kā lietot preču ieteikumus pārdošanas punkta (POS) ierīcē.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a1a25e3d5bc1cc5c1c7509186451fdfef50dd6cf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792343"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="3b9af-103">Pievienot preču ieteikumi punktā POS</span><span class="sxs-lookup"><span data-stu-id="3b9af-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b9af-104">To pašos pamatos, preču ieteikumi ir transformējoša biznesa programma, kas aptver visas komercijas vietas, lai izveidotu bagātīgu, saistošu un pielāgotu preču atklāšanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="3b9af-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="3b9af-105">Lai šo funkciju ieviestu POS, izpildiet norādījumus [kā pievienot ieteikumus jūsu POS ierīcēm.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="3b9af-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="3b9af-106">Lai iegūtu vairāk informācijas par preču ieteikumu līdzekļiem, lasiet [preču ieteikumu pārskats.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="3b9af-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="3b9af-107">Scenāriji</span><span class="sxs-lookup"><span data-stu-id="3b9af-107">Scenarios</span></span>

<span data-ttu-id="3b9af-108">Preču ieteikumi ir iespējoti tālāk norādītajos POS scenārijos.</span><span class="sxs-lookup"><span data-stu-id="3b9af-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="3b9af-109">Tie ir pieejami programmā Cloud POS vai Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="3b9af-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="3b9af-110">Lapā **Detalizēta informācija par preci**.</span><span class="sxs-lookup"><span data-stu-id="3b9af-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="3b9af-111">Ja veikala darbinieks apmeklē lapu **Detalizēta informācija par preci**, skatot iepriekšējās transakcijas dažādos kanālos, ieteikumu serviss piedāvā papildu preces, kas var tikt nopirktas kopā.</span><span class="sxs-lookup"><span data-stu-id="3b9af-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="3b9af-112">[![Ieteikumi lapā Informācija par preci](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="3b9af-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="3b9af-113">Lapā **Transakcija**.</span><span class="sxs-lookup"><span data-stu-id="3b9af-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="3b9af-114">Ieteikumu programma iesaka preces, kuras bieži pērk kopā, pamatojoties uz visu grozam pievienoto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="3b9af-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3b9af-115">Lai lapā **Transakcija** tiktu rādīti ieteikumi, mazumtirgotājam ir jāatjaunina ekrāna izkārtojums programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b9af-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3b9af-116">Lapā **Transakcijas** ir jāaktivizē vadīkla **Ieteikumi** lapā.</span><span class="sxs-lookup"><span data-stu-id="3b9af-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="3b9af-117">[![Ieteikumi lapā Transakcija](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="3b9af-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="3b9af-118">Commerce konfigurēšana, lai iespējotu POS ieteikumus</span><span class="sxs-lookup"><span data-stu-id="3b9af-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="3b9af-119">Lai iestatītu preču ieteikumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="3b9af-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="3b9af-120">Pārliecinieties, ka jūsu serviss ir atjaunināts uz **10.0.6 būvējumu.**</span><span class="sxs-lookup"><span data-stu-id="3b9af-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="3b9af-121">Sekojiet instrukcijām, kā [iespējot produktu ieteikumus](../commerce/enable-product-recommendations.md) jūsu biznesam.</span><span class="sxs-lookup"><span data-stu-id="3b9af-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="3b9af-122">Pēc izvēles. Lai transakciju ekrānā tiktu rādīti ieteikumi, pārejiet uz sadaļu **Ekrāna izkārtojums**, izvēlieties savu ekrāna izkārtojumu, palaidiet līdzekli **Ekrāna izkārtojuma dizainers** un pēc tam aktivizējiet vadīklu **ieteikumi**, kur nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="3b9af-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="3b9af-123">Pārejiet uz sadaļu **Commerce parametri**, atlasiet vienumu **Algoritmiskā mācīšanās** un sadaļā **Iespējot POS ieteikumus** atlasiet vienumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3b9af-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="3b9af-124">Lai POS tiktu rādīti ieteikumi, palaidiet globālās konfigurācijas darbu Nr. **1110**.</span><span class="sxs-lookup"><span data-stu-id="3b9af-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="3b9af-125">Lai atainotu POS ekrāna izkārtojuma dizainerī veiktās izmaiņas, palaidiet kanāla konfigurācijas darbu Nr. **1070**.</span><span class="sxs-lookup"><span data-stu-id="3b9af-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="3b9af-126">Problēmu novēršana, ja preču ieteikumi jau ir iespējoti</span><span class="sxs-lookup"><span data-stu-id="3b9af-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="3b9af-127">Pārejiet uz **Commerce parametri** \> **Ieteikumu saraksti** \> **Atspējot preču ieteikumus** un palaidiet darbu **Globālais konfigurācijas darbs \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="3b9af-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="3b9af-128">Ja darbību ekrānam pievienojāt vadīklu **Ieteikumus pārvaldība**, izmantojot **Ekrāna izkārtojuma dizainers**, lūdzu, noņemiet arī to.</span><span class="sxs-lookup"><span data-stu-id="3b9af-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="3b9af-129">Ja jums ir papildu jautājumi, skatiet [Bieži uzdotos jautājumus par preču ieteikumiem](../commerce/faq-recommendations.md), lai iegūtu vairāk informācijas.</span><span class="sxs-lookup"><span data-stu-id="3b9af-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b9af-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3b9af-130">Additional resources</span></span>

[<span data-ttu-id="3b9af-131">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="3b9af-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="3b9af-132">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3b9af-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="3b9af-133">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="3b9af-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="3b9af-134">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="3b9af-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="3b9af-135">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="3b9af-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="3b9af-136">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="3b9af-136">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="3b9af-137">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="3b9af-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3b9af-138">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="3b9af-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="3b9af-139">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="3b9af-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="3b9af-140">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="3b9af-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="3b9af-141">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="3b9af-141">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]