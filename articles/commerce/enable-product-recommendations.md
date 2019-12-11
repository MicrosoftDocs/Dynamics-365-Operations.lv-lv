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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770143"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="02e13-103">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="02e13-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="02e13-104">Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.</span><span class="sxs-lookup"><span data-stu-id="02e13-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="02e13-105">Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="02e13-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="02e13-106">Ieteikumu iepriekšpārbaude</span><span class="sxs-lookup"><span data-stu-id="02e13-106">Recommendations pre-check</span></span>
<span data-ttu-id="02e13-107">Pirms iespējošanas, lūdzu, ievērojiet, ka preces ieteikumi tiek atbalstīti tikai nākotnes līgumu un iespēju līgumu klientiem, kas atbalsta veidojumu 10.0.6 un ir migrējuši savu krātuvi, lai izmantotu BDL.</span><span class="sxs-lookup"><span data-stu-id="02e13-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="02e13-108">Turklāt pārliecinieties, ka ir iespējoti RetailSale mērījumi.</span><span class="sxs-lookup"><span data-stu-id="02e13-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="02e13-109">Lai uzzinātu vairāk par šo iestatīšanas procesu, dodieties [šeit.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="02e13-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="02e13-110">Ieteikumu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="02e13-110">Turn on recommendations</span></span>

<span data-ttu-id="02e13-111">Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="02e13-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="02e13-112">Dodieties uz **Mazumtirdzniecība** &gt; **Preču ieteikumi** &gt; **Ieteikuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="02e13-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="02e13-113">Mazumtirdzniecības koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="02e13-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="02e13-114">Iestatiet opciju **Iespējot ieteikumus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="02e13-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![Preču ieteikumu iespējošana](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="02e13-116">Šī procedūra uzsāk preču ieteikumu saraksta ģenerēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="02e13-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="02e13-117">Var paiet vairākas stundas pirms saraksts ir pieejams un redzams pārdošanas punktā (POS) vai Dynamics 365 for Commerce.</span><span class="sxs-lookup"><span data-stu-id="02e13-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="02e13-118">Ieteikumu saraksta parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="02e13-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="02e13-119">Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="02e13-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="02e13-120">Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai.</span><span class="sxs-lookup"><span data-stu-id="02e13-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="02e13-121">Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="02e13-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="02e13-122">Parādīt ieteikumus POS ierīcēs</span><span class="sxs-lookup"><span data-stu-id="02e13-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="02e13-123">Pēc ieteikumu iespējošanas birojā, POS ekrānam jāpievieno ieteikumu panelis, izmantojot izkārtojuma rīku.</span><span class="sxs-lookup"><span data-stu-id="02e13-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="02e13-124">Lai uzzinātu vairāk par šo procesu, dodieties [šeit.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="02e13-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="02e13-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="02e13-125">Additional resources</span></span>

[<span data-ttu-id="02e13-126">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="02e13-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="02e13-127">Preču ieteikumu sarakstu pievienošana lapām</span><span class="sxs-lookup"><span data-stu-id="02e13-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="02e13-128">Ieteikumu paneļa pievienošana POS ierīcēm</span><span class="sxs-lookup"><span data-stu-id="02e13-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


