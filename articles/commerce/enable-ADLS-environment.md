---
title: Azure Data Lake Storage iespējošana Dynamics 365 Commerce vidē
description: Šajā tēmā paskaidrots, kā iespējot un pārbaudīt Azure Data Lake Storage Dynamics 365 Commerce videi, kas ir priekšnosacījums preču ieteikumu iespējošanai.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 5887ae7983fd817a929a185327671b301808b354
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478240"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="3cbdb-103">Azure Data Lake Storage iespējošana Dynamics 365 Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="3cbdb-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3cbdb-104">Šajā tēmā paskaidrots, kā iespējot un pārbaudīt Azure Data Lake Storage Dynamics 365 Commerce videi, kas ir priekšnosacījums preču ieteikumu iespējošanai.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="3cbdb-105">Risinājumā Dynamics 365 Commerce visa informācija par preci un transakciju tiek izsekota vides elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="3cbdb-106">Lai šos datus padarītu pieejamus citiem Dynamics 365 pakalpojumiem, piemēram, datu analīzei, biznesa informācijai un personalizētiem ieteikumiem, šī vide jāsavieno ar debitoram piederošu Azure Data Lake Storage Gen 2 risinājumu.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="3cbdb-107">Tā kā Azure Data Lake Storage ir konfigurēta vidē, visi nepieciešamie dati tiek atspoguļoti no elementu krātuves, tomēr tie joprojām tiek aizsargāti un atrodas klienta kontrolē.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="3cbdb-108">Ja arī preču ieteikumi vai personalizētie ieteikumi vidē ir iespējoti, preču ieteikumu stekam tiks piešķirta piekļuve īpašajai mapei Azure Data Lake Storage, lai izgūtu debitora datus un apstrādātu ieteikumus, pamatojoties uz to.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3cbdb-109">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="3cbdb-109">Prerequisites</span></span>

<span data-ttu-id="3cbdb-110">Debitoriem piederošajā Azure abonementā jābūt konfigurētai Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="3cbdb-111">Šī tēma neattiecas uz Azure abonementa iegādi vai Azure Data Lake Storage iespējota krātuves konta iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="3cbdb-112">Papildinformāciju par Azure Data Lake Storage skatiet [Azure Data Lake Storage Gen2 oficiālajos dokumentos](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="3cbdb-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="3cbdb-113">Konfigurācijas darbības</span><span class="sxs-lookup"><span data-stu-id="3cbdb-113">Configuration steps</span></span>

<span data-ttu-id="3cbdb-114">Šajā sadaļā ir aprakstītas konfigurācijas darbības, kas nepieciešamas Azure Data Lake Storage iespējošanai vidē, jo tā attiecas uz preces ieteikumiem.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="3cbdb-115">Lai iegūtu padziļinātu pārskatu par darbībām, kas nepieciešamas Azure Data Lake Storage iespējošanai, skatiet [Elementu krātuves pārvēršana par Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="3cbdb-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="3cbdb-116">Azure Data Lake Storage iespējošana vidē</span><span class="sxs-lookup"><span data-stu-id="3cbdb-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="3cbdb-117">Piesakieties vides iekšējās uzskaites daļas portālam.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="3cbdb-118">Sameklējiet **Sistēmas parametri** un dodieties uz cilni **Datu savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="3cbdb-119">Iestatiet **Iespējot Data Lake integrāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="3cbdb-120">Iestatiet **Pakāpeniski atjaunināt Data Lake** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="3cbdb-121">Pēc tam ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="3cbdb-122">**Pieteikuma ID** // **Pieteikuma noslēpums** // **DNS nosaukums** — jāizveido savienojums ar KeyVault, kur tiek glabāts Azure Data Lake Storage noslēpums.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="3cbdb-123">**Slepenais nosaukums** — slepenais nosaukums, kas tiek glabāts KeyVault un tiek izmantots, lai veiktu autentifikāciju ar Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="3cbdb-124">Saglabājiet izmaiņas lapas augšējā kreisajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="3cbdb-125">Tālāk redzamajā attēlā ir parādīts Azure Data Lake Storage konfigurācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Azure Data Lake Storage konfigurācijas piemērs](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="3cbdb-127">Azure Data Lake Storage savienojuma pārbaude</span><span class="sxs-lookup"><span data-stu-id="3cbdb-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="3cbdb-128">Pārbaudiet savienojumu ar KeyVault, izmantojot saiti **Pābaudīt Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="3cbdb-129">Pārbaudiet savienojumu ar Azure Data Lake Storage, izmantojot saiti **Pābaudīt Azure krātuvi**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="3cbdb-130">Ja pārbaudes nav veiksmīgs, vēlreiz pārbaudiet, vai visa iepriekš pievienotā KeyVault informācija ir pareiza, un pēc tam mēģiniet vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="3cbdb-131">Kad savienojuma pārbaudes ir veiksmīgas, jāiespējo automātiska elementu krātuves atsvaidzināšana.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="3cbdb-132">Lai iespējotu automātisku elementu krātuves atsvaidzināšanu, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="3cbdb-133">Sameklējiet **Elementu krātuvi**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="3cbdb-134">Kreisajā pusē esošajā sarakstā dodieties uz ierakstu **RetailSales** un atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="3cbdb-135">Pārliecinieties, ka opcija **Iespējota automātiskā atsvaidzināšana** ir iestatīta **Jā**, atlasiet **Atsvaidzināt** un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="3cbdb-136">Tālak redzamaja attēlā parādīts elementu veikala ar iespējotu automātisku atsvaidzināšanu piemērs.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Elementu krātuves ar iespējotu automātisku atsvaidzināšanu piemērs](./media/exampleADLSConfig2.png)

<span data-ttu-id="3cbdb-138">Azure Data Lake Storage tagad ir konfigurēta videi.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="3cbdb-139">Ja tas vēl nav pabeigts, sekojiet norādījumiem par [preču ieteikumu iespējošanu un personalizāciju](enable-product-recommendations.md) videi.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3cbdb-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3cbdb-140">Additional resources</span></span>

[<span data-ttu-id="3cbdb-141">Elementu krātuves pārvēršana par Data Lake</span><span class="sxs-lookup"><span data-stu-id="3cbdb-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="3cbdb-142">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="3cbdb-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="3cbdb-143">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="3cbdb-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="3cbdb-144">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="3cbdb-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="3cbdb-145">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="3cbdb-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="3cbdb-146">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="3cbdb-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="3cbdb-147">Preču ieteikumu pievienošana punktā POS</span><span class="sxs-lookup"><span data-stu-id="3cbdb-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="3cbdb-148">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="3cbdb-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3cbdb-149">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="3cbdb-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="3cbdb-150">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="3cbdb-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="3cbdb-151">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="3cbdb-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="3cbdb-152">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="3cbdb-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
