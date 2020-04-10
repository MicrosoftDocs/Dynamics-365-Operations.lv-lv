---
title: Izveidot ieteikumus ar demo datiem
description: Šis dokuments sniedz vadlīnijas par to, kā gūt labumu no daudzkanālu preču ieteikumiem 1. līmeņa atsevišķa lodziņa vidēs, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.
author: bebeale
manager: AnnBe
ms.date: 03/19/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 59cb5e5c9b59ff2127149e3e47b6c30c9c938a27
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154253"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="1425b-103">Izveidot ieteikumus ar demo datiem</span><span class="sxs-lookup"><span data-stu-id="1425b-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1425b-104">Šis dokuments sniedz vadlīnijas par to, kā gūt labumu no daudzkanālu preču ieteikumiem 1. līmeņa atsevišķa lodziņa vidēs, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="1425b-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="1425b-105">Daudzkanālu preces ieteikumi sniedz redakcionāli pārraudzītu vai programmiski ģenerētu preču sarakstu kopu.</span><span class="sxs-lookup"><span data-stu-id="1425b-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="1425b-106">Šos sarakstus var izmantot vairākos scenārijos atkarībā no biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="1425b-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="1425b-107">Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1425b-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="1425b-108">2. līmeņa un augstākās Dynamics 365 vidēs preces ieteikumi tiek automātiski aprēķinātas, pamatojoties uz klienta datiem.</span><span class="sxs-lookup"><span data-stu-id="1425b-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="1425b-109">Preču ieteikumu demonstrācijas datu izmantošana neatspējo nevienu produkta rekomendāciju risinājumu, kas jau ir nodrošināts vidē, un visas ar tā izmantošanu saistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="1425b-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="1425b-110">1. līmeņa vidēs preces ieteikumi ir balstīti tikai uz nemainīgajiem demonstrācijas datiem, kas saglabāti .scv failā.</span><span class="sxs-lookup"><span data-stu-id="1425b-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="1425b-111">Produkta rekomendāciju demonstrāciju datu aktivizēšana vidē</span><span class="sxs-lookup"><span data-stu-id="1425b-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="1425b-112">Lai iespējotu preču ieteikumu demonstrācijas datus, ir jāizvieto Dynamics 365 Commerce priekšskatījuma demonstrācijas paplašinājums attiecīgajai videi.</span><span class="sxs-lookup"><span data-stu-id="1425b-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="1425b-113">Tas automātiski iespējo preces ieteikumu demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="1425b-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="1425b-114">Noklusējuma demonstrācijas dati</span><span class="sxs-lookup"><span data-stu-id="1425b-114">Default demo data</span></span>
<span data-ttu-id="1425b-115">Katrai Onebox veida videi komplektā ir ietverts iepriekš ielādēts preces ieteikumu demonstrācijas datu kopums, kas tiek glabāts ar komatu atdalītā ‘reco_demo_data.csv’ failā, kas atrodas Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1425b-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="1425b-116">Dati ir strukturēti tālāk redzamajās kolonnās.</span><span class="sxs-lookup"><span data-stu-id="1425b-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="1425b-117">Kolonnas nosaukums</span><span class="sxs-lookup"><span data-stu-id="1425b-117">Column name</span></span>         | <span data-ttu-id="1425b-118">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1425b-118">Mandatory</span></span>          | <span data-ttu-id="1425b-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1425b-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="1425b-120">Iespējamās vērtības</span><span class="sxs-lookup"><span data-stu-id="1425b-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1425b-121">IeteikumuSaraksts</span><span class="sxs-lookup"><span data-stu-id="1425b-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="1425b-123">Īpašais preču ieteikumu saraksta veids, kas ir jāģenerē demonstrācijas datu punktam.</span><span class="sxs-lookup"><span data-stu-id="1425b-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="1425b-124">IeteikumiVislabākPārdotais</span><span class="sxs-lookup"><span data-stu-id="1425b-124">RecoBestSelling</span></span></li><li><span data-ttu-id="1425b-125">IeteikumiJauns</span><span class="sxs-lookup"><span data-stu-id="1425b-125">RecoNew</span></span></li><li><span data-ttu-id="1425b-126">IeteikumiTendences</span><span class="sxs-lookup"><span data-stu-id="1425b-126">RecoTrending</span></span></li><li><span data-ttu-id="1425b-127">IeteikumiGrozs</span><span class="sxs-lookup"><span data-stu-id="1425b-127">RecoCart</span></span></li><li><span data-ttu-id="1425b-128">IeteikumiCilvēkiArīPērk</span><span class="sxs-lookup"><span data-stu-id="1425b-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="1425b-129">PārvaldībasStruktūrvienībuNumurs</span><span class="sxs-lookup"><span data-stu-id="1425b-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="1425b-131">Konkrētais pārvaldības struktūrvienības numurs, kurā ir paredzēts uzrasties preču ieteikumiem.</span><span class="sxs-lookup"><span data-stu-id="1425b-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="1425b-132">Kategorija</span><span class="sxs-lookup"><span data-stu-id="1425b-132">Category</span></span>            |                    |    <span data-ttu-id="1425b-133">Kategorija, kurai jāatgriež konkrētais saraksts.</span><span class="sxs-lookup"><span data-stu-id="1425b-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="1425b-134">Ja kategorija nav norādīta, saraksts ir paredzēts tikai augšējai navigācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="1425b-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="1425b-135">AtlasesPrecesId</span><span class="sxs-lookup"><span data-stu-id="1425b-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="1425b-136">Sarakstiem, kam ir nepieciešams sākums (RecoPeopleAlsoBuy un RecoCart), preces, kurām šiem sarakstiem jāparāda papildu preces.</span><span class="sxs-lookup"><span data-stu-id="1425b-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="1425b-137">PrecesId</span><span class="sxs-lookup"><span data-stu-id="1425b-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="1425b-139">Viena vai vairākas preces, kas jāatgriež kā rezultāts, kas atdalīts ar ';'.</span><span class="sxs-lookup"><span data-stu-id="1425b-139">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="1425b-140">Pielāgot demonstrācijas datus</span><span class="sxs-lookup"><span data-stu-id="1425b-140">Customize demo data</span></span>
<span data-ttu-id="1425b-141">Varat rediģēt noklusējuma demonstrācijas datus ar jebkuru preču un kategoriju informāciju, kas ir konfigurēta HQ.</span><span class="sxs-lookup"><span data-stu-id="1425b-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="1425b-142">Kad atjaunināt .csv, preču ieteikumi, kas tiek sniegti klientiem, nekavējoties atspoguļos izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="1425b-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="1425b-143">Paplašinājums ietver datu faila ar nosaukumu 'RecoMockDataset.csv', kas ļauj jums kontrolēt datu kopu, kas tiek izmantota, lai darbinātu neīstos ieteikumu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="1425b-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="1425b-144">Faila nosaukumu var kontrolēt, izmantojot paplašinājumu konfigurāciju, izmantojot **ext.Recommendations.DemoFilePath** iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="1425b-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="1425b-145">Minētais iespējo to, ka jums var būt pieejamas vairākas datu kopas, kuras var ērti pārslēgt, izmantojot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="1425b-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="1425b-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1425b-146">Additional Resources</span></span>

[<span data-ttu-id="1425b-147">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="1425b-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1425b-148">ADLS iespējošana Dynamics 365 Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="1425b-148">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1425b-149">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="1425b-149">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="1425b-150">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="1425b-150">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1425b-151">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="1425b-151">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1425b-152">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="1425b-152">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1425b-153">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="1425b-153">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1425b-154">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="1425b-154">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1425b-155">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="1425b-155">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1425b-156">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="1425b-156">Product recommendations FAQ</span></span>](faq-recommendations.md)
