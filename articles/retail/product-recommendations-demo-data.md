---
title: Omni-Channel preču ieteikumu demonstrācijas dati
description: Šī dokumenta mērķis ir sniegt vadlīnijas par to, kā līdzekļu Omni-Channel preces rekomendācijas 1. līmeņa Onebox vidē, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2226185"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="1b93d-103">Omni-Channel preču ieteikumu demonstrācijas dati</span><span class="sxs-lookup"><span data-stu-id="1b93d-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="1b93d-104">Šī dokumenta mērķis ir sniegt vadlīnijas par to, kā līdzekļu Omni-Channel preces rekomendācijas 1. līmeņa Onebox vidē, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="1b93d-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="1b93d-105">Omni-Channel preces ieteikumi sniedz redakcionāli pārraudzītu vai programmatiski ģenerētu paredzētu preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="1b93d-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="1b93d-106">Šos sarakstus var izmantot vairākos scenārijos atkarībā no biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="1b93d-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="1b93d-107">Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, lasiet [Preču ieteikumu pārskats.](product-recommendaitons-overview.md)</span><span class="sxs-lookup"><span data-stu-id="1b93d-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="1b93d-108">2. līmeņa un augstākas Dynamics vides preces rekomendācijas tiek automātiski aprēķinātas, pamatojoties uz klienta datiem.</span><span class="sxs-lookup"><span data-stu-id="1b93d-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="1b93d-109">Preču ieteikumu demonstrācijas datu izmantošana neatspējo nevienu produkta rekomendāciju risinājumu, kas jau ir nodrošināts vidē, un visas ar tā izmantošanu saistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="1b93d-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="1b93d-110">1. līmeņa vides preces ieteikumi ir balstīti tikai uz nemainīgajiem demonstrācijas datiem, kas saglabāti CSV failā.</span><span class="sxs-lookup"><span data-stu-id="1b93d-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="1b93d-111">Produkta rekomendāciju demonstrāciju datu aktivizēšana vidē</span><span class="sxs-lookup"><span data-stu-id="1b93d-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="1b93d-112">Klientiem ir jāizvieto **Dynamics 365 Commerce priekšskatījuma demonstrācijas paplašinājums** attiecīgajai videi, kas automātiski aktivizē preces rekomendāciju demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="1b93d-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="1b93d-113">Noklusējuma demonstrācijas dati</span><span class="sxs-lookup"><span data-stu-id="1b93d-113">Default demo data</span></span>
<span data-ttu-id="1b93d-114">Katrai Onebox tipa videi komplektā ir ietverts iepriekš ielādēts preces rekomendāciju demonstrācijas datu kopums, kas tiek glabāts **‘reco_demo_data.csv’** failā, kas atrodas tajā pašā mapē, kur šis dokuments, mazumtirdzniecības serverī.</span><span class="sxs-lookup"><span data-stu-id="1b93d-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="1b93d-115">Šie dati ir iedalīti šādās kolonnās</span><span class="sxs-lookup"><span data-stu-id="1b93d-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="1b93d-116">Kolonnas nosaukums</span><span class="sxs-lookup"><span data-stu-id="1b93d-116">Column name</span></span>         | <span data-ttu-id="1b93d-117">Obligāts</span><span class="sxs-lookup"><span data-stu-id="1b93d-117">Mandatory</span></span>          | <span data-ttu-id="1b93d-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1b93d-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="1b93d-119">Iespējamās vērtības</span><span class="sxs-lookup"><span data-stu-id="1b93d-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1b93d-120">IeteikumuSaraksts</span><span class="sxs-lookup"><span data-stu-id="1b93d-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="1b93d-122">Īpašais preču ieteikumu saraksta veids, kas ir jāģenerē demonstrācijas datu punktam.</span><span class="sxs-lookup"><span data-stu-id="1b93d-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="1b93d-123">IeteikumiVislabākPārdotais</span><span class="sxs-lookup"><span data-stu-id="1b93d-123">RecoBestSelling</span></span></li><li><span data-ttu-id="1b93d-124">IeteikumiJauns</span><span class="sxs-lookup"><span data-stu-id="1b93d-124">RecoNew</span></span></li><li><span data-ttu-id="1b93d-125">IeteikumiTendences</span><span class="sxs-lookup"><span data-stu-id="1b93d-125">RecoTrending</span></span></li><li><span data-ttu-id="1b93d-126">IeteikumiGrozs</span><span class="sxs-lookup"><span data-stu-id="1b93d-126">RecoCart</span></span></li><li><span data-ttu-id="1b93d-127">IeteikumiCilvēkiArīPērk</span><span class="sxs-lookup"><span data-stu-id="1b93d-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="1b93d-128">PārvaldībasStruktūrvienībuNumurs</span><span class="sxs-lookup"><span data-stu-id="1b93d-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="1b93d-130">Konkrētais pārvaldības struktūrvienības numurs, kurā ir paredzēts, ka preču ieteikumi tiks saklāti.</span><span class="sxs-lookup"><span data-stu-id="1b93d-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="1b93d-131">Kategorija</span><span class="sxs-lookup"><span data-stu-id="1b93d-131">Category</span></span>            |                    |    <span data-ttu-id="1b93d-132">Kategorija, kurai jāatgriež konkrētais saraksts.</span><span class="sxs-lookup"><span data-stu-id="1b93d-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="1b93d-133">Ja kategorija nav norādīta, saraksts ir paredzēts tikai augšajai navigācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="1b93d-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="1b93d-134">AtlasesPrecesId</span><span class="sxs-lookup"><span data-stu-id="1b93d-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="1b93d-135">Saraksti, kuriem ir vajadzīga atlase (IeteikumiCilvēkiArīPērk un IeteikumiGrozs), prese, kurai šiem sarakstiem ir jāuzrāda papildu preces.</span><span class="sxs-lookup"><span data-stu-id="1b93d-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="1b93d-136">PrecesId</span><span class="sxs-lookup"><span data-stu-id="1b93d-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="1b93d-138">Viena vai vairākas preces, kas jāatgriež kā rezultāts, kas ir atdalītas ar **";"**.</span><span class="sxs-lookup"><span data-stu-id="1b93d-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="1b93d-139">Pielāgot demonstrācijas datus</span><span class="sxs-lookup"><span data-stu-id="1b93d-139">Customize demo data</span></span>
<span data-ttu-id="1b93d-140">Klienti var rediģēt noklusējuma demonstrācijas datus ar jebkuru preču un kategorijas informāciju, kas ir konfigurēta HQ.</span><span class="sxs-lookup"><span data-stu-id="1b93d-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="1b93d-141">Kad CSV ir atjaunināts, klientiem Atgrieztie preces ieteikumi nekavējoties parādīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="1b93d-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="1b93d-142">Paplašinājums ietver datu faila nosaukumu RecoMockDataset.csv, kas ļauj klientam kontrolēt datu kopu, ko izmanto, lai darbinātu pārbaudes objekta ieteikumu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="1b93d-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="1b93d-143">Faila nosaukumu var kontrolēt, izmantojot paplašinājumu konfigurāciju, izmantojot **ext.Recommendations.DemoFilePath** iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="1b93d-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="1b93d-144">Tas ļauj klientiem ipieeju vairākiem datu kopam, kuras var ērti pārslēgt, izmantojot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="1b93d-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="1b93d-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1b93d-145">Additional resources</span></span>

[<span data-ttu-id="1b93d-146">Preču ieteikumu pārskats</span><span class="sxs-lookup"><span data-stu-id="1b93d-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="1b93d-147">Vides plānošana</span><span class="sxs-lookup"><span data-stu-id="1b93d-147">Environment planning</span></span>](environment-planning.md)
