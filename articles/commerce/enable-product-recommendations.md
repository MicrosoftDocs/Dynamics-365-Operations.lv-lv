---
title: Preču ieteikumu iespējošana
description: Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2dacd4a94f706be5aa65947c0b6a92e281733ca
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665030"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="5eed5-103">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="5eed5-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5eed5-104">Šajā tēmā izskaidrots, kā sniegt preces ieteikumus, kas balstīti uz mākslīgo intelektu – mašīnmācību (AI-ML), kas pieejama Microsoft Dynamics 365 Commerce klientiem.</span><span class="sxs-lookup"><span data-stu-id="5eed5-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="5eed5-105">Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5eed5-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="5eed5-106">Ieteikumu iepriekšpārbaude</span><span class="sxs-lookup"><span data-stu-id="5eed5-106">Recommendations pre-check</span></span>

<span data-ttu-id="5eed5-107">Pirms iespējošanas ievērojiet, ka preces ieteikumi tiek atbalstīti tikai tiem Commerce klientiem, kuri ir migrējuši savu krātuvi, lai izmantotu Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="5eed5-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="5eed5-108">Pirms ieteikumu iespējošanas birojā ir jābūt iespējotām šādām konfigurācijām:</span><span class="sxs-lookup"><span data-stu-id="5eed5-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="5eed5-109">Pārliecinieties, ka Azure Data Lake Storage ir iegādāta un sekmīgi pārbaudīta vidē.</span><span class="sxs-lookup"><span data-stu-id="5eed5-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="5eed5-110">Papildinformācijai skatiet [EPārliecinieties, ka Azure Data Lake Storage ir iegādāta un sekmīgi pārbaudīta vidē](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5eed5-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="5eed5-111">Pārliecinieties, ka elementa krātuves atsvaidzināšana ir automatizēta.</span><span class="sxs-lookup"><span data-stu-id="5eed5-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="5eed5-112">Papildinformāciju skatiet [Pārliecinieties, ka elementa krātuves atsvaidzināšana ir automatizēta](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="5eed5-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="5eed5-113">Apstipriniet, ka Azure AD identitātes konfigurācija ietver ievadni ieteikumiem.</span><span class="sxs-lookup"><span data-stu-id="5eed5-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="5eed5-114">Papildinformāciju par to, kā veikt šo darbību, skatīt zemāk.</span><span class="sxs-lookup"><span data-stu-id="5eed5-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="5eed5-115">Turklāt pārliecinieties, ka ir iespējoti RetailSale mērījumi.</span><span class="sxs-lookup"><span data-stu-id="5eed5-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="5eed5-116">Lai uzzinātu vairāk par šo iestatīšanas procesu, skatiet [Darbs ar mērvienībām](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="5eed5-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="5eed5-117">Azure AD identitātes konfigurācija</span><span class="sxs-lookup"><span data-stu-id="5eed5-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="5eed5-118">Šis solis ir nepieciešams visiem klientiem, kas izmanto infra-structure kā pakalpojuma (IaaS) konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="5eed5-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="5eed5-119">Klientiem, kas darbojas Service Fabric (SF), šim solim ir jābūt automātiskam, un ieteicams pārbaudīt, vai iestatījums ir konfigurēts, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="5eed5-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="5eed5-120">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="5eed5-120">Setup</span></span>

1. <span data-ttu-id="5eed5-121">Birojā meklējiet **Azure Active Directory pieteikumu** lapu.</span><span class="sxs-lookup"><span data-stu-id="5eed5-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="5eed5-122">Pārbaudiet, vai pastāv ieraksts "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="5eed5-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="5eed5-123">Ja ieraksts nepastāv, pievienojiet jaunu ierakstu ar šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="5eed5-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="5eed5-124">**Klienta ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="5eed5-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="5eed5-125">**Nosaukums** -RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="5eed5-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="5eed5-126">**Lietotāja ID** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="5eed5-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="5eed5-127">Saglabājiet un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="5eed5-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="5eed5-128">Ieteikumu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="5eed5-128">Turn on recommendations</span></span>

<span data-ttu-id="5eed5-129">Lai ieslēgtu preču ieteikumus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="5eed5-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="5eed5-130">Pärejiet uz **Mazumtirdzniecība un komercija &gt; Preču ieteikumi &gt; Ieteikumu parametri**.</span><span class="sxs-lookup"><span data-stu-id="5eed5-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="5eed5-131">Koplietojamo parametru sarakstā atlasiet **Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="5eed5-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="5eed5-132">Iestatiet opciju **Iespējot ieteikumus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5eed5-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Ieteikumu ieslēgšana](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="5eed5-134">Šī procedūra uzsāk preču ieteikumu saraksta ģenerēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="5eed5-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="5eed5-135">Var paiet vairākas stundas pirms saraksts ir pieejams un var tikt redzams pārdošanas punktā (POS) vai Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5eed5-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="5eed5-136">Ieteikumu saraksta parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5eed5-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="5eed5-137">Pēc noklusējuma AI–ML balstīts preču ieteikumu saraksts nodrošina ieteiktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="5eed5-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="5eed5-138">Varat mainīt ieteiktās noklusējuma vērtības, lai tās atbilstu jūsu biznesa plūsmai.</span><span class="sxs-lookup"><span data-stu-id="5eed5-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="5eed5-139">Lai uzzinātu vairāk par to, kā mainīt noklusējuma parametrus, dodieties uz [AI–ML balstītu preces ieteikuma rezultātu pārvaldīšana](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="5eed5-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="5eed5-140">Parādīt ieteikumus POS ierīcēs</span><span class="sxs-lookup"><span data-stu-id="5eed5-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="5eed5-141">Pēc ieteikumu iespējošanas Commerce dokumentu apstrādes birojā, POS ekrānam jāpievieno ieteikumu panelis, izmantojot izkārtojuma rīku.</span><span class="sxs-lookup"><span data-stu-id="5eed5-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="5eed5-142">Lai uzzinātu vairāk par šo procesu, skatiet sadaļu [Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="5eed5-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="5eed5-143">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="5eed5-143">Enable personalized recommendations</span></span>

<span data-ttu-id="5eed5-144">Sistēmā Dynamics 365 Commerce mazumtirgotāji var padarīt personalizētus produktu ieteikumus (sauktus arī par personalizēšanu) pieejamus.</span><span class="sxs-lookup"><span data-stu-id="5eed5-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="5eed5-145">Šādā veidā personalizētus ieteikumus var iekļaut klientu tiešsaistes pieredzē un pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="5eed5-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="5eed5-146">Kad personalizācijas funkcionalitāte ir ieslēgta, sistēma var saistīt lietotāja pirkuma un preces informāciju, lai ģenerētu individualizētus preces ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="5eed5-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="5eed5-147">Papildinformāciju par personalizēto ieteikumu saņemšanu skatiet [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5eed5-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eed5-148">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5eed5-148">Additional resources</span></span>

[<span data-ttu-id="5eed5-149">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="5eed5-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="5eed5-150">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5eed5-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="5eed5-151">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="5eed5-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="5eed5-152">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="5eed5-152">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="5eed5-153">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="5eed5-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="5eed5-154">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="5eed5-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="5eed5-155">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="5eed5-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="5eed5-156">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="5eed5-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="5eed5-157">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="5eed5-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="5eed5-158">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="5eed5-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="5eed5-159">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="5eed5-159">Product recommendations FAQ</span></span>](faq-recommendations.md)

