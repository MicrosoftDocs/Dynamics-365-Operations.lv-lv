---
title: Preču ieteikumu iespējošana
description: Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127886"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="bd0c1-103">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="bd0c1-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd0c1-104">Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="bd0c1-105">Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="bd0c1-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="bd0c1-106">Ieteikumu iepriekšpārbaude</span><span class="sxs-lookup"><span data-stu-id="bd0c1-106">Recommendations pre-check</span></span>

<span data-ttu-id="bd0c1-107">Pirms iespējošanas, lūdzu, ievērojiet, ka preces ieteikumi tiek atbalstīti tikai tiem Commerce klientiem, kuri ir migrējuši savu krātuvi, lai izmantotu Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="bd0c1-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="bd0c1-108">Veicamās darbības ADLS iespējošanai skatiet [Kā iespējot ADLS programmas Dynamics 365 vidē.](enable-ADLS-environment.md)</span><span class="sxs-lookup"><span data-stu-id="bd0c1-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="bd0c1-109">Turklāt pārliecinieties, ka ir iespējoti RetailSale mērījumi.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="bd0c1-110">Lai uzzinātu vairāk par šo iestatīšanas procesu, dodieties [šeit.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="bd0c1-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="bd0c1-111">Ieteikumu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="bd0c1-111">Turn on recommendations</span></span>

<span data-ttu-id="bd0c1-112">Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="bd0c1-113">Pärejiet uz **Mazumtirdzniecība un komercija &gt; Preču ieteikumi &gt; Ieteikumu parametri**.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="bd0c1-114">Koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="bd0c1-115">Iestatiet opciju **Iespējot ieteikumus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Preču ieteikumu iespējošana](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="bd0c1-117">Šī procedūra uzsāk preču ieteikumu saraksta ģenerēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="bd0c1-118">Var paiet vairākas stundas pirms saraksts ir pieejams un redzams pārdošanas punktā (POS) vai Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="bd0c1-119">Ieteikumu saraksta parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bd0c1-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="bd0c1-120">Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="bd0c1-121">Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="bd0c1-122">Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="bd0c1-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="bd0c1-123">Parādīt ieteikumus POS ierīcēs</span><span class="sxs-lookup"><span data-stu-id="bd0c1-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="bd0c1-124">Pēc ieteikumu iespējošanas Commerce dokumentu apstrādes birojā, POS ekrānam jāpievieno ieteikumu panelis, izmantojot izkārtojuma rīku.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="bd0c1-125">Lai uzzinātu vairāk par šo procesu, skatiet sadaļu [Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="bd0c1-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="bd0c1-126">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="bd0c1-126">Enable personalized recommendations</span></span>

<span data-ttu-id="bd0c1-127">Papildinformāciju par personalizēto ieteikumu saņemšanu skatiet sadaļā [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="bd0c1-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd0c1-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bd0c1-128">Additional resources</span></span>

[<span data-ttu-id="bd0c1-129">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="bd0c1-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="bd0c1-130">ADLS iespējošana Dynamics 365 Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="bd0c1-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="bd0c1-131">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="bd0c1-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="bd0c1-132">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="bd0c1-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="bd0c1-133">Preču ieteikumu sarakstu pievienošana e-komercijas vietnei</span><span class="sxs-lookup"><span data-stu-id="bd0c1-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="bd0c1-134">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="bd0c1-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="bd0c1-135">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="bd0c1-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="bd0c1-136">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="bd0c1-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="bd0c1-137">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="bd0c1-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="bd0c1-138">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="bd0c1-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="bd0c1-139">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="bd0c1-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

