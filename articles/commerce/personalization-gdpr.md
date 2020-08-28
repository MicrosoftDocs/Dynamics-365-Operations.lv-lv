---
title: Personalizētu ieteikumu izvēle
description: Šajā tēmā izskaidrots, kā varat ļaut klientiem izvēlēties, vai saņemt personalizētus ieteikumus risinājumā Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: a51c8c0e2743b67df9d66a8c45ab7a69597f4002
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664934"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="a6f56-103">Personalizētu ieteikumu izvēle</span><span class="sxs-lookup"><span data-stu-id="a6f56-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6f56-104">Šajā tēmā izskaidrots, kā varat ļaut klientiem izvēlēties, vai saņemt personalizētus ieteikumus risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6f56-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a6f56-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a6f56-105">Overview</span></span>

<span data-ttu-id="a6f56-106">Konta izveides laikā tiek automātiski iestatīts, ka jauni debitori saņems personalizētus ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="a6f56-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="a6f56-107">Tomēr Dynamics 365 Commerce piedāvā dažādus veidus, kā mazumtirgotāji ļauj lietotājiem izvēlēties nesaņemt šos ieteikumus un ierobežot savu personas datu apstrādi.</span><span class="sxs-lookup"><span data-stu-id="a6f56-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="a6f56-108">Autentificēti lietotāji, kas atsakās saņemt personalizētus ieteikumus, nekavējoties beigs redzēt personalizētos sarakstus.</span><span class="sxs-lookup"><span data-stu-id="a6f56-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="a6f56-109">Turklāt visi personiskie dati, kas tiek vākti personalizēšanai, tiks noņemti no personalizēto ieteikumu modeļiem.</span><span class="sxs-lookup"><span data-stu-id="a6f56-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="a6f56-110">Papildinformāciju par preču personalizēto ieteikumu saņemšanu skatiet sadaļā [Personalizēto ieteikumu iespējošana](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a6f56-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="a6f56-111">Veidi, kā mazumtirgotājiem ieviest atteikšanās iespēju</span><span class="sxs-lookup"><span data-stu-id="a6f56-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="a6f56-112">Mazumtirgotājiem ir trīs veidi, kādos ieviest atteikšanās iespēju.</span><span class="sxs-lookup"><span data-stu-id="a6f56-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="a6f56-113">Atteikšanās lietotāju vārdā</span><span class="sxs-lookup"><span data-stu-id="a6f56-113">Opting out on behalf of users</span></span>

<span data-ttu-id="a6f56-114">Kontu pārvaldībā Commerce atbalsta birojā tirgotāji var atteikties lietotāju vārdā.</span><span class="sxs-lookup"><span data-stu-id="a6f56-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="a6f56-115">Vadības sākumlapā meklējiet **visus debitorus**.</span><span class="sxs-lookup"><span data-stu-id="a6f56-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="a6f56-116">Meklējiet un atlasiet debitoru un pēc tam atlasiet **mazumtirdzniecības** kopsavilkuma cilni.</span><span class="sxs-lookup"><span data-stu-id="a6f56-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Mazumtirdzniecības kopsavilkuma cilnes](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="a6f56-118">Sadaļā **Konfidencialitāte** iestatiet opciju **Atspējot personalizāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a6f56-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Konfidencialitātes iestatījumi](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="a6f56-120">Atlasiet **Saglabāt** un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="a6f56-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="a6f56-121">Modulī balstīta atteikšanās iespēja</span><span class="sxs-lookup"><span data-stu-id="a6f56-121">Module-based opt-out experience</span></span>

<span data-ttu-id="a6f56-122">Mazumtirgotāji var ļaut autentificētiem lietotājiem pašiem atteikties no personalizētajiem ieteikumiem.</span><span class="sxs-lookup"><span data-stu-id="a6f56-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="a6f56-123">Lai nodrošinātu šo atteikšanās iespēju, pievienojiet lietotāja atteikšanās moduli klienta konta profila lapām.</span><span class="sxs-lookup"><span data-stu-id="a6f56-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="a6f56-124">Pielāgoti paplašinājumi</span><span class="sxs-lookup"><span data-stu-id="a6f56-124">Custom extensions</span></span>

<span data-ttu-id="a6f56-125">Mazumtirgotāji var izveidot savus paplašinājumus, lai pārvaldītu lietotāju atteikšanās pieredzi.</span><span class="sxs-lookup"><span data-stu-id="a6f56-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="a6f56-126">Papildinformāciju skatiet šeit [Retail Server API izsaukšana](e-commerce-extensibility/call-retail-server-apis.md) un [Tiešsaistes kanāla paplašināšana](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="a6f56-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="a6f56-127">Iegūstiet personalizēto ieteikumu datu digitālo kopiju autentificēta lietotāja vārdā</span><span class="sxs-lookup"><span data-stu-id="a6f56-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="a6f56-128">Klienti var vēlēties iegūt savu personas datu digitālo kopiju un arī skatīt eksportētus ieteikumu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="a6f56-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="a6f56-129">Ja debitors pieprasa šo informāciju, mazumtirgotājam ir jāizveido pielāgots paplašinājums, kas izsauc Retail Server pieteikuma programmēšanas interfeisu (API) un veic vaicājumus par visiem rezultātiem no **Ieteikumu** saraksta, pamatojoties uz klienta ID.</span><span class="sxs-lookup"><span data-stu-id="a6f56-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="a6f56-130">Pēc tam rezultātus var eksportēt ar komatu atdalītu vērtību (CSV) formātā un koplietot ar debitoru.</span><span class="sxs-lookup"><span data-stu-id="a6f56-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="a6f56-131">Šajā piemērā parādīts, kā mazumtirgotājs var izpildīt šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="a6f56-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="a6f56-132">Mazumtirgotājs izveido pielāgotu paplašinājumu, lai izvilktu personisku ieteikumu datus lietotāja vārdā.</span><span class="sxs-lookup"><span data-stu-id="a6f56-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="a6f56-133">Lai iegūtu informāciju par to, kā izveidot moduļus, klonēt esošos moduļus, izsaukt Retail Server API un izsaukt datu darbības, skatiet [Tiešsaistes kanāla paplašināmība](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="a6f56-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="a6f56-134">Pielāgotais paplašinājums veic zvanu **get-recommendations** pamatdatu darbībai, un nodod tai nepieciešamo informāciju, pamatojoties uz saraksta prasībām.</span><span class="sxs-lookup"><span data-stu-id="a6f56-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="a6f56-135">**Ieteikumu** saraksts gadījumā paplašinājumam ir jānodod pareizais saraksta nosaukums un klienta ID datu darbībai.</span><span class="sxs-lookup"><span data-stu-id="a6f56-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="a6f56-136">Viens no veidiem, kā izveidot pielāgotu paplašinājumu, ir klonēt esošo preču ievākšanas moduli, kas tiek izmantots ieteikumu rezultātu atgriešanai.</span><span class="sxs-lookup"><span data-stu-id="a6f56-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="a6f56-137">Klonējot šo esošo moduli, mazumtirgotājs var modificēt esošo kodu un pievienot jaunu pogu, kas eksportē ieteikumu rezultātus CSV failā.</span><span class="sxs-lookup"><span data-stu-id="a6f56-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="a6f56-138">Papildinformāciju skatiet šeitL [Sākuma komplekta moduļa klonēšana](e-commerce-extensibility/clone-starter-module.md) un [Preču ievākšanas moduļi](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a6f56-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="a6f56-139">Lai pilnībā skatītu Retail Server API bibliotēku, skatiet sadaļu [Retail Server klientu un patērētāju API](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="a6f56-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="a6f56-140">Pēc tam, kad ir izveidots pielāgots paplašinājums, tirgotājs var eksportēt CSV failu no visiem ieteikumu rezultātiem, balstoties uz autentificētā lietotāja unikālo klienta ID.</span><span class="sxs-lookup"><span data-stu-id="a6f56-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="a6f56-141">Mazumtirgotājs var koplietot eksportēto CSV failu, kurā ir ietverts pilns ieteikto preču saraksts ar autentificēto lietotāju.</span><span class="sxs-lookup"><span data-stu-id="a6f56-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6f56-142">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a6f56-142">Additional resources</span></span>

[<span data-ttu-id="a6f56-143">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="a6f56-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a6f56-144">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a6f56-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a6f56-145">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="a6f56-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a6f56-146">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="a6f56-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a6f56-147">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="a6f56-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="a6f56-148">Preču ieteikumu pievienošana punktā POS</span><span class="sxs-lookup"><span data-stu-id="a6f56-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a6f56-149">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="a6f56-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a6f56-150">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="a6f56-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a6f56-151">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="a6f56-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a6f56-152">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="a6f56-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a6f56-153">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="a6f56-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
