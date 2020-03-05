---
title: ADLS iespējošana Dynamics 365 Commerce vidē
description: Šajā tēmā paskaidrots, kā iespējot un pārbaudīt Azure Data Lake Storage (ADLS) Dynamics 365 Commerce videi, kas ir priekšnosacījums preču ieteikumu iespējošanai.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025263"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="91311-103">ADLS iespējošana Dynamics 365 Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="91311-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91311-104">Šajā tēmā paskaidrots, kā iespējot un pārbaudīt Azure Data Lake Storage (ADLS) Dynamics 365 Commerce videi, kas ir priekšnosacījums preču ieteikumu iespējošanai.</span><span class="sxs-lookup"><span data-stu-id="91311-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="91311-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="91311-105">Overview</span></span>

<span data-ttu-id="91311-106">Risinājumā Dynamics 365 Commerce visa informācija par preci un transakciju tiek izsekota vides elementu krātuvē.</span><span class="sxs-lookup"><span data-stu-id="91311-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="91311-107">Lai šos datus padarītu pieejamus citiem Dynamics 365 pakalpojumiem, piemēram, datu analīzei, biznesa informācijai un personalizētiem ieteikumiem, šī vide jāsavieno ar debitoram piederošu Azure Data Lake Storage Gen 2 (ADLS) risinājumu.</span><span class="sxs-lookup"><span data-stu-id="91311-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="91311-108">Tā kā ADLS ir konfigurēta vidē, visi nepieciešamie dati tiek atspoguļoti no elementu krātuves, tomēr tie joprojām tiek aizsargāti un atrodas klienta kontrolē.</span><span class="sxs-lookup"><span data-stu-id="91311-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="91311-109">Ja arī preču ieteikumi vai personalizētie ieteikumi vidē ir iespējoti, preču ieteikumu stekam tiks piešķirta piekļuve īpašajai ADLS mapei, lai izgūtu debitora datus un apstrādātu ieteikumus, pamatojoties uz to.</span><span class="sxs-lookup"><span data-stu-id="91311-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="91311-110">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="91311-110">Prerequisites</span></span>

<span data-ttu-id="91311-111">Debitoriem piederošajā Azure abonementā jābūt konfigurētai ADLS.</span><span class="sxs-lookup"><span data-stu-id="91311-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="91311-112">Šī tēma neattiecas uz Azure abonementa iegādi vai ADLS iespējota krātuves konta iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="91311-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="91311-113">Papildinformāciju par ADLS skatiet [ADLS oficiālajos dokumentos](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="91311-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="91311-114">Konfigurācijas darbības</span><span class="sxs-lookup"><span data-stu-id="91311-114">Configuration steps</span></span>

<span data-ttu-id="91311-115">Šajā sadaļā ir izskaidrotas konfigurācijas darbības, kas nepieciešamas ADLS iespējošanai vidē.</span><span class="sxs-lookup"><span data-stu-id="91311-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="91311-116">ADLS iespējošana vidē</span><span class="sxs-lookup"><span data-stu-id="91311-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="91311-117">Piesakieties vides iekšējās uzskaites daļas portālam.</span><span class="sxs-lookup"><span data-stu-id="91311-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="91311-118">Sameklējiet **Sistēmas parametri** un dodieties uz cilni **Datu savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="91311-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="91311-119">Iestatiet **Iespējot Data Lake integrāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="91311-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="91311-120">Iestatiet **Pakāpeniski atjaunināt Data Lake** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="91311-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="91311-121">Pēc tam ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="91311-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="91311-122">**Pieteikuma ID** // **Pieteikuma noslēpums** // **DNS nosaukums** — nepieciešams, lai izveidotu savienojumu ar KeyVault, kur tiek glabāts ADLS noslēpums.</span><span class="sxs-lookup"><span data-stu-id="91311-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="91311-123">**Slepenais nosaukums** — slepenais nosaukums, kas tiek glabāts KeyVault un tiek izmantots, lai veiktu autentifikāciju ar ADLS.</span><span class="sxs-lookup"><span data-stu-id="91311-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="91311-124">Saglabājiet izmaiņas lapas augšējā kreisajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="91311-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="91311-125">Tālāk redzamajā attēlā ir parādīts ADLS konfigurācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="91311-125">The following image shows an example ADLS configuration.</span></span>

![ADLS konfigurācijas piemērs](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="91311-127">ADLS savienojuma pārbaude</span><span class="sxs-lookup"><span data-stu-id="91311-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="91311-128">Pārbaudiet savienojumu ar KeyVault, izmantojot saiti **Pābaudīt Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="91311-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="91311-129">Pārbaudiet savienojumu ar ADLS, izmantojot saiti **Pābaudīt Azure krātuvi**.</span><span class="sxs-lookup"><span data-stu-id="91311-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="91311-130">Ja pārbaudes nav veiksmīgs, vēlreiz pārbaudiet, vai visa iepriekš pievienotā KeyVault informācija ir pareiza, un pēc tam mēģiniet vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="91311-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="91311-131">Kad savienojuma pārbaudes ir veiksmīgas, jāiespējo automātiska elementu krātuves atsvaidzināšana.</span><span class="sxs-lookup"><span data-stu-id="91311-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="91311-132">Lai iespējotu automātisku elementu krātuves atsvaidzināšanu, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="91311-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="91311-133">Sameklējiet **Elementu krātuvi**.</span><span class="sxs-lookup"><span data-stu-id="91311-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="91311-134">Kreisajā pusē esošajā sarakstā dodieties uz ierakstu **RetailSales** un atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="91311-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="91311-135">Pārliecinieties, ka opcija **Iespējota automātiskā atsvaidzināšana** ir iestatīta **Jā**, atlasiet **Atsvaidzināt** un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="91311-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="91311-136">Tālak redzamaja attēlā parādīts elementu veikala ar iespējotu automātisku atsvaidzināšanu piemērs.</span><span class="sxs-lookup"><span data-stu-id="91311-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Elementu krātuves ar iespējotu automātisku atsvaidzināšanu piemērs](./media/exampleADLSConfig2.png)

<span data-ttu-id="91311-138">Tagad ADLS ir konfigurēta videi.</span><span class="sxs-lookup"><span data-stu-id="91311-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="91311-139">Ja tas vēl nav pabeigts, sekojiet norādījumiem par [preču ieteikumu iespējošanu un personalizāciju](enable-product-recommendations.md) videi.</span><span class="sxs-lookup"><span data-stu-id="91311-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91311-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="91311-140">Additional resources</span></span>

[<span data-ttu-id="91311-141">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="91311-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="91311-142">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="91311-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="91311-143">Preču ieteikumu sarakstu pievienošana lapām</span><span class="sxs-lookup"><span data-stu-id="91311-143">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="91311-144">Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="91311-144">Add a recommendations control to the transaction screen on POS devices</span></span>](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)

