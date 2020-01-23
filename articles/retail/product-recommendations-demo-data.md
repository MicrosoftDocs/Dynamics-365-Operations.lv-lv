---
title: Omni-Channel preču ieteikumu demonstrācijas dati
description: Šī dokumenta mērķis ir sniegt vadlīnijas par to, kā līdzekļu Omni-Channel preces rekomendācijas 1. līmeņa Onebox vidē, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872330"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="53ec0-103">Omni-Channel preču ieteikumu demonstrācijas dati</span><span class="sxs-lookup"><span data-stu-id="53ec0-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="53ec0-104">Šī dokumenta mērķis ir sniegt vadlīnijas par to, kā līdzekļu Omni-Channel preces rekomendācijas 1. līmeņa Onebox vidē, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="53ec0-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="53ec0-105">Omni-Channel preces ieteikumi sniedz redakcionāli pārraudzītu vai programmatiski ģenerētu paredzētu preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="53ec0-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="53ec0-106">Šos sarakstus var izmantot vairākos scenārijos atkarībā no biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="53ec0-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="53ec0-107">Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, lasiet [Preču ieteikumu pārskats.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="53ec0-107">For more information about product recommendation lists, see [Product recommendations overview.](../commerce/product-recommendations.md)</span></span>

<span data-ttu-id="53ec0-108">2. līmeņa un augstākas Dynamics vides preces rekomendācijas tiek automātiski aprēķinātas, pamatojoties uz klienta datiem.</span><span class="sxs-lookup"><span data-stu-id="53ec0-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="53ec0-109">Preču ieteikumu demonstrācijas datu izmantošana neatspējo nevienu produkta rekomendāciju risinājumu, kas jau ir nodrošināts vidē, un visas ar tā izmantošanu saistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="53ec0-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="53ec0-110">1. līmeņa vides preces ieteikumi ir balstīti tikai uz nemainīgajiem demonstrācijas datiem, kas saglabāti CSV failā.</span><span class="sxs-lookup"><span data-stu-id="53ec0-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="53ec0-111">Produkta rekomendāciju demonstrāciju datu aktivizēšana vidē</span><span class="sxs-lookup"><span data-stu-id="53ec0-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="53ec0-112">Klientiem ir jāizvieto **Dynamics 365 Commerce priekšskatījuma demonstrācijas paplašinājums** attiecīgajai videi, kas automātiski aktivizē preces rekomendāciju demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="53ec0-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="53ec0-113">Noklusējuma demonstrācijas dati</span><span class="sxs-lookup"><span data-stu-id="53ec0-113">Default demo data</span></span>
<span data-ttu-id="53ec0-114">Katrai Onebox tipa videi komplektā ir ietverts iepriekš ielādēts preces rekomendāciju demonstrācijas datu kopums, kas tiek glabāts **‘reco_demo_data.csv’** failā, kas atrodas tajā pašā mapē, kur šis dokuments, mazumtirdzniecības serverī.</span><span class="sxs-lookup"><span data-stu-id="53ec0-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="53ec0-115">Šie dati ir iedalīti šādās kolonnās</span><span class="sxs-lookup"><span data-stu-id="53ec0-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="53ec0-116">Kolonnas nosaukums</span><span class="sxs-lookup"><span data-stu-id="53ec0-116">Column name</span></span>         | <span data-ttu-id="53ec0-117">Obligāts</span><span class="sxs-lookup"><span data-stu-id="53ec0-117">Mandatory</span></span>          | <span data-ttu-id="53ec0-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="53ec0-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="53ec0-119">Iespējamās vērtības</span><span class="sxs-lookup"><span data-stu-id="53ec0-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="53ec0-120">IeteikumuSaraksts</span><span class="sxs-lookup"><span data-stu-id="53ec0-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="53ec0-122">Īpašais preču ieteikumu saraksta veids, kas ir jāģenerē demonstrācijas datu punktam.</span><span class="sxs-lookup"><span data-stu-id="53ec0-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="53ec0-123">IeteikumiVislabākPārdotais</span><span class="sxs-lookup"><span data-stu-id="53ec0-123">RecoBestSelling</span></span></li><li><span data-ttu-id="53ec0-124">IeteikumiJauns</span><span class="sxs-lookup"><span data-stu-id="53ec0-124">RecoNew</span></span></li><li><span data-ttu-id="53ec0-125">IeteikumiTendences</span><span class="sxs-lookup"><span data-stu-id="53ec0-125">RecoTrending</span></span></li><li><span data-ttu-id="53ec0-126">IeteikumiGrozs</span><span class="sxs-lookup"><span data-stu-id="53ec0-126">RecoCart</span></span></li><li><span data-ttu-id="53ec0-127">IeteikumiCilvēkiArīPērk</span><span class="sxs-lookup"><span data-stu-id="53ec0-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="53ec0-128">PārvaldībasStruktūrvienībuNumurs</span><span class="sxs-lookup"><span data-stu-id="53ec0-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="53ec0-130">Konkrētais pārvaldības struktūrvienības numurs, kurā ir paredzēts, ka preču ieteikumi tiks saklāti.</span><span class="sxs-lookup"><span data-stu-id="53ec0-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="53ec0-131">Kategorija</span><span class="sxs-lookup"><span data-stu-id="53ec0-131">Category</span></span>            |                    |    <span data-ttu-id="53ec0-132">Kategorija, kurai jāatgriež konkrētais saraksts.</span><span class="sxs-lookup"><span data-stu-id="53ec0-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="53ec0-133">Ja kategorija nav norādīta, saraksts ir paredzēts tikai augšajai navigācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="53ec0-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="53ec0-134">AtlasesPrecesId</span><span class="sxs-lookup"><span data-stu-id="53ec0-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="53ec0-135">Saraksti, kuriem ir vajadzīga atlase (IeteikumiCilvēkiArīPērk un IeteikumiGrozs), prese, kurai šiem sarakstiem ir jāuzrāda papildu preces.</span><span class="sxs-lookup"><span data-stu-id="53ec0-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="53ec0-136">PrecesId</span><span class="sxs-lookup"><span data-stu-id="53ec0-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="53ec0-138">Viena vai vairākas preces, kas jāatgriež kā rezultāts, kas ir atdalītas ar **";"**.</span><span class="sxs-lookup"><span data-stu-id="53ec0-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="53ec0-139">Pielāgot demonstrācijas datus</span><span class="sxs-lookup"><span data-stu-id="53ec0-139">Customize demo data</span></span>
<span data-ttu-id="53ec0-140">Klienti var rediģēt noklusējuma demonstrācijas datus ar jebkuru preču un kategorijas informāciju, kas ir konfigurēta HQ.</span><span class="sxs-lookup"><span data-stu-id="53ec0-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="53ec0-141">Kad CSV ir atjaunināts, klientiem Atgrieztie preces ieteikumi nekavējoties parādīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="53ec0-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="53ec0-142">Paplašinājums ietver datu faila nosaukumu RecoMockDataset.csv, kas ļauj klientam kontrolēt datu kopu, ko izmanto, lai darbinātu pārbaudes objekta ieteikumu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="53ec0-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="53ec0-143">Faila nosaukumu var kontrolēt, izmantojot paplašinājumu konfigurāciju, izmantojot **ext.Recommendations.DemoFilePath** iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="53ec0-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="53ec0-144">Tas ļauj klientiem ipieeju vairākiem datu kopam, kuras var ērti pārslēgt, izmantojot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="53ec0-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="53ec0-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="53ec0-145">Additional resources</span></span>

[<span data-ttu-id="53ec0-146">Preču ieteikumu pārskats</span><span class="sxs-lookup"><span data-stu-id="53ec0-146">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="53ec0-147">Vides plānošana</span><span class="sxs-lookup"><span data-stu-id="53ec0-147">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
