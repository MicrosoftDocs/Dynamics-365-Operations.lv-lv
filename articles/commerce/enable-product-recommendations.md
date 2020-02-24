---
title: Preču ieteikumu iespējošana
description: Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024960"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="0000b-103">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="0000b-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0000b-104">Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.</span><span class="sxs-lookup"><span data-stu-id="0000b-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="0000b-105">Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="0000b-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="0000b-106">Ieteikumu iepriekšpārbaude</span><span class="sxs-lookup"><span data-stu-id="0000b-106">Recommendations pre-check</span></span>

<span data-ttu-id="0000b-107">Pirms iespējošanas, lūdzu, ievērojiet, ka preces ieteikumi tiek atbalstīti tikai tiem Commerce klientiem, kuri ir migrējuši savu krātuvi, lai izmantotu Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="0000b-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="0000b-108">Veicamās darbības ADLS iespējošanai skatiet [Kā iespējot ADLS programmas Dynamics 365 vidē.](enable-ADLS-environment.md)</span><span class="sxs-lookup"><span data-stu-id="0000b-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="0000b-109">Turklāt pārliecinieties, ka ir iespējoti RetailSale mērījumi.</span><span class="sxs-lookup"><span data-stu-id="0000b-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="0000b-110">Lai uzzinātu vairāk par šo iestatīšanas procesu, dodieties [šeit.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="0000b-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="0000b-111">Ieteikumu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="0000b-111">Turn on recommendations</span></span>

<span data-ttu-id="0000b-112">Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="0000b-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="0000b-113">Pärejiet uz **Mazumtirdzniecība un komercija &gt; Preču ieteikumi &gt; Ieteikumu parametri**.</span><span class="sxs-lookup"><span data-stu-id="0000b-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="0000b-114">Koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="0000b-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="0000b-115">Iestatiet opciju **Iespējot ieteikumus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0000b-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Preču ieteikumu iespējošana](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="0000b-117">Šī procedūra uzsāk preču ieteikumu saraksta ģenerēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="0000b-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="0000b-118">Var paiet vairākas stundas pirms saraksts ir pieejams un redzams pārdošanas punktā (POS) vai Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0000b-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="0000b-119">Ieteikumu saraksta parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0000b-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="0000b-120">Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="0000b-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="0000b-121">Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai.</span><span class="sxs-lookup"><span data-stu-id="0000b-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="0000b-122">Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="0000b-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="0000b-123">Parādīt ieteikumus POS ierīcēs</span><span class="sxs-lookup"><span data-stu-id="0000b-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="0000b-124">Pēc ieteikumu iespējošanas Commerce dokumentu apstrādes birojā, POS ekrānam jāpievieno ieteikumu panelis, izmantojot izkārtojuma rīku.</span><span class="sxs-lookup"><span data-stu-id="0000b-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="0000b-125">Lai uzzinātu vairāk par šo procesu, skatiet sadaļu [Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="0000b-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="0000b-126">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="0000b-126">Enable personalized recommendations</span></span>

<span data-ttu-id="0000b-127">Papildinformāciju par personalizēto ieteikumu saņemšanu skatiet sadaļā [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="0000b-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0000b-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0000b-128">Additional resources</span></span>

[<span data-ttu-id="0000b-129">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="0000b-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="0000b-130">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="0000b-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="0000b-131">Preču ieteikumu sarakstu pievienošana lapām</span><span class="sxs-lookup"><span data-stu-id="0000b-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="0000b-132">Ieteikumu paneļa pievienošana POS ierīcēm</span><span class="sxs-lookup"><span data-stu-id="0000b-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="0000b-133">Preču kolekcijas moduļa apskats</span><span class="sxs-lookup"><span data-stu-id="0000b-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="0000b-134">ADLS iespējošana Dynamics 365 vidē</span><span class="sxs-lookup"><span data-stu-id="0000b-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

