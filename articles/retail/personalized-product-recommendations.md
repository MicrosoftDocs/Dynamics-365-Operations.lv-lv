---
title: "Personalizētu preču ieteikumu apskats"
description: "Izmantojot programmatūru Dynamics 365 for Retail, pārdošanas punkta (POS) ierīcē var tikt rādīti preču ieteikumi. Ieteikumi ir krājumi, kas debitoru varētu interesēt, pamatojoties uz debitora pirkumu vēsturi, krājumiem debitora vēlmju sarakstā, kā arī krājumiem, ko citi debitori ir nopirkuši tiešsaistes un fiziskajos veikalos. Ja mazumtirgotājam ir plašs katalogs, ieteikumi palīdz debitoram atklāt preces. Preču ieteikumi nodrošina, ka debitoram tiek piedāvātas viņa interesēm un iepirkumu vēsturei atbilstošas preces, un tādējādi var palīdzēt mazumtirgotājiem veikt papildu pārdošanu un šķērspārdošanu un uzlabot klientu lojalitātes saglabāšanas rādītājus. Programmatūrā Dynamics 365 for Retail preču ieteikumi tiek nodrošināti, izmantojot pakalpojumu Cognitive Services un Microsoft Azure algoritmisko mācīšanos."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 42ffb375d9786b2ac506d6ef06e9da9ee22652a6
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="0a95b-107">Personalizētu preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="0a95b-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="0a95b-108">Šis līdzeklis pašlaik ir pieejams tikai smilškastes un ražošanas (augstas pieejamības) izvietojumu topoloģijām.</span><span class="sxs-lookup"><span data-stu-id="0a95b-108">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="0a95b-109">Izmantojot programmatūru Dynamics 365 for Retail, pārdošanas punkta (POS) ierīcē var tikt rādīti preču ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="0a95b-109">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="0a95b-110">Ieteikumi ir krājumi, kas debitoru varētu interesēt, pamatojoties uz debitora pirkumu vēsturi, krājumiem debitora vēlmju sarakstā, kā arī krājumiem, ko citi debitori ir nopirkuši tiešsaistes un fiziskajos veikalos.</span><span class="sxs-lookup"><span data-stu-id="0a95b-110">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="0a95b-111">Ja mazumtirgotājam ir plašs katalogs, ieteikumi palīdz debitoram atklāt preces.</span><span class="sxs-lookup"><span data-stu-id="0a95b-111">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="0a95b-112">Preču ieteikumi nodrošina, ka debitoram tiek piedāvātas viņa interesēm un iepirkumu vēsturei atbilstošas preces, un tādējādi var palīdzēt mazumtirgotājiem veikt papildu pārdošanu un šķērspārdošanu un uzlabot klientu lojalitātes saglabāšanas rādītājus.</span><span class="sxs-lookup"><span data-stu-id="0a95b-112">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="0a95b-113">Programmatūrā Dynamics 365 for Retail preču ieteikumi tiek nodrošināti, izmantojot pakalpojumu Cognitive Services un Microsoft Azure algoritmisko mācīšanos.</span><span class="sxs-lookup"><span data-stu-id="0a95b-113">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="0a95b-114">Scenāriji</span><span class="sxs-lookup"><span data-stu-id="0a95b-114">Scenarios</span></span>
---------

<span data-ttu-id="0a95b-115">Preču ieteikumi ir iespējoti tālāk norādītajos POS scenārijos.</span><span class="sxs-lookup"><span data-stu-id="0a95b-115">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="0a95b-116">Tie ir pieejami programmā Cloud POS vai Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="0a95b-116">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="0a95b-117">Lapā **Detalizēta informācija par preci**.</span><span class="sxs-lookup"><span data-stu-id="0a95b-117">On the **Product details** page:</span></span>

-   <span data-ttu-id="0a95b-118">Ja veikala darbinieks apmeklē lapu **Detalizēta informācija par precei**, skatot iepriekšējās transakcijas dažādos kanālos, ieteikumu programma piedāvā papildu preces, kas var tikt nopirktas kopā.</span><span class="sxs-lookup"><span data-stu-id="0a95b-118">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="0a95b-119">Ja veikala darbinieks pievieno transakcijai debitoru un pēc tam apmeklē lapu **Detalizēta informācija par preci**, ieteikumu programma nodrošina personalizētus ieteikumus, izmantojot debitora transakciju vēsturi.</span><span class="sxs-lookup"><span data-stu-id="0a95b-119">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="0a95b-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="0a95b-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="0a95b-121">Lapā **Transakcija**.</span><span class="sxs-lookup"><span data-stu-id="0a95b-121">On the **Transaction** page:</span></span>

-   <span data-ttu-id="0a95b-122">Ieteikumu programma iesaka preces, pamatojoties uz visu grozam pievienoto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0a95b-122">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="0a95b-123">Ja veikala darbinieks pievieno transakcijai debitoru, ieteikumu programma nodrošina personalizētus ieteikumus, izmantojot debitora transakciju vēsturi un grozam pievienoto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0a95b-123">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="0a95b-124">Lai lapā **Transakcija** tiktu rādīti ieteikumi, mazumtirgotājam ir jāatjaunina ekrāna izkārtojums programmatūrā Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0a95b-124">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="0a95b-125">Lapā **Transakcijas** ir jāaktivizē vadīkla **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="0a95b-125">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="0a95b-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="0a95b-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="0a95b-127">Lapā **Detalizēta informācija par debitoru**.</span><span class="sxs-lookup"><span data-stu-id="0a95b-127">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="0a95b-128">Ieteikumu programma iesaka preces, pamatojoties uz lietotāja ID un precēm debitora velmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="0a95b-128">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="0a95b-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="0a95b-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="0a95b-130">Dynamics 365 for Retail konfigurēšana, lai iespējotu POS ieteikumus</span><span class="sxs-lookup"><span data-stu-id="0a95b-130">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="0a95b-131">Lai iestatītu preču ieteikumus, ir jāveic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0a95b-131">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="0a95b-132">Pārliecinieties, ka laukā **Juridiskā persona** ir atlasīta vajadzīgā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="0a95b-132">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="0a95b-133">Pārejiet uz sadaļu **Elementu krātuve**, atlasiet vienumu **Pārdošana mazumtirdzniecībā** un pēc tam noklikšķiniet uz **Atsvaidzināt**. Šai funkcijai tiek izmantoti demonstrācijas dati (vai jūsu dati) no jūsu operāciju datu bāzes, un šie dati tiek pārvietoti uz elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="0a95b-133">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="0a95b-134">Pēc izvēles. Lai transakciju ekrānā tiktu rādīti ieteikumi, pārejiet uz sadaļu **Ekrāna izkārtojums**, izvēlieties savu ekrāna izkārtojumu, palaidiet līdzekli **Ekrāna izkārtojuma dizainers** un pēc tam aktivizējiet vadīklu **ieteikumi**, kur nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="0a95b-134">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**,and then drop the **recommendations** control where needed.</span></span>
4.  <span data-ttu-id="0a95b-135">Pārejiet uz sadaļu **Mazumtirdzniecības parametri**, atlasiet vienumu **Algoritmiskā mācīšanās** un sadaļā **Iespējot POS ieteikumus** atlasiet vienumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0a95b-135">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="0a95b-136">Lai POS tiktu rādīti ieteikumi, palaidiet globālās konfigurācijas darbu Nr. **1110**.</span><span class="sxs-lookup"><span data-stu-id="0a95b-136">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="0a95b-137">Lai atainotu POS ekrāna izkārtojuma dizainerī veiktās izmaiņas, palaidiet kanāla konfigurācijas darbu Nr. **1070**.</span><span class="sxs-lookup"><span data-stu-id="0a95b-137">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="0a95b-138">[]()Kā tas notiek?</span><span class="sxs-lookup"><span data-stu-id="0a95b-138">[]()How does it work?</span></span>
<span data-ttu-id="0a95b-139">Kad atsvaidzināt elementu **Elementu krātuve**, tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0a95b-139">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="0a95b-140">No programmatūras Dynamics 365 for Retail operāciju datu bāzes tiek izgūti dati, kuru formāts atbilst Cognitive Services nepieciešamajam formātam, un šie dati tiek nosūtīti uz elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="0a95b-140">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="0a95b-141">Šie dati tiek izmantoti pakalpojumā Azure Data Factory (ADF), lai ADF aktivitāšu ietvaros attīrītu datus, izmantojot Hive skriptus.</span><span class="sxs-lookup"><span data-stu-id="0a95b-141">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="0a95b-142">Attīrītie dati tiek uzglabāti BLOB krātuvē.</span><span class="sxs-lookup"><span data-stu-id="0a95b-142">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="0a95b-143">Dati no BLOB krātuves tiek izmantoti Cognitive Services API, lai apmācītu ieteikumu modeli.</span><span class="sxs-lookup"><span data-stu-id="0a95b-143">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="0a95b-144">Ja aktivizējat opciju **Iespējot ieteikumus** un palaižat konfigurācijas darbus, tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0a95b-144">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="0a95b-145">No API tiek izgūti modeļa akreditācijas dati un ID, un tie tiek saglabāti Dynamics 365 for Retail operāciju datu bāzē (AOS failā web.config), kā arī mazumtirdzniecības serverī.</span><span class="sxs-lookup"><span data-stu-id="0a95b-145">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="0a95b-146">Modeļa akreditācijas dati un ID tiek padarīti pieejami CRT, lai varētu izpildīt tiešsaistes preču ieteikumu izsaukumus no programmām Cloud POS un MPOS.</span><span class="sxs-lookup"><span data-stu-id="0a95b-146">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="0a95b-147">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="0a95b-147">See also</span></span>
--------

[<span data-ttu-id="0a95b-148">Ieteikumu vadīklas pievienošana POS ierīces lapā Transakcijas</span><span class="sxs-lookup"><span data-stu-id="0a95b-148">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




