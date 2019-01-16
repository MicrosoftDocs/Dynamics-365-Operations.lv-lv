---
title: "Personalizēti preču ieteikumi"
description: "Šajā tēmā ir sniegta informācija par Dynamics 365 for Retail preču ieteikumiem, kas var tikt rādīti pārdošanas punkta (POS) ierīcē."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: d6706cbb7630aeb230bc9eb1c187397897c9de68
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="personalized-product-recommendations"></a><span data-ttu-id="8a689-103">Personalizēti preču ieteikumi</span><span class="sxs-lookup"><span data-stu-id="8a689-103">Personalized product recommendations</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="8a689-104">Mēs noņemam preču ieteikumu pakalpojuma pašreizējo versiju, jo pārveidojam šo līdzekli, pievienojot tam uzlabotu algoritmu un jaunākas uz mazumtirdzniecību orientētas iespējas.</span><span class="sxs-lookup"><span data-stu-id="8a689-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="8a689-105">Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi](../dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="8a689-105">For more information see [Removed or deprecated features](../dev-itpro/migration-upgrade/deprecated-features.md).</span></span>

<span data-ttu-id="8a689-106">Izmantojot programmatūru Dynamics 365 for Retail, pārdošanas punkta (POS) ierīcē var tikt rādīti preču ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="8a689-106">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="8a689-107">Ieteikumi ir krājumi, kas debitoru varētu interesēt, pamatojoties uz debitora pirkumu vēsturi, krājumiem debitora vēlmju sarakstā, kā arī krājumiem, ko citi debitori ir nopirkuši tiešsaistes un fiziskajos veikalos.</span><span class="sxs-lookup"><span data-stu-id="8a689-107">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="8a689-108">Ja mazumtirgotājam ir plašs katalogs, ieteikumi palīdz debitoram atklāt preces.</span><span class="sxs-lookup"><span data-stu-id="8a689-108">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="8a689-109">Preču ieteikumi nodrošina, ka debitoram tiek piedāvātas viņa interesēm un iepirkumu vēsturei atbilstošas preces, un tādējādi var palīdzēt mazumtirgotājiem veikt papildu pārdošanu un šķērspārdošanu un uzlabot klientu lojalitātes saglabāšanas rādītājus.</span><span class="sxs-lookup"><span data-stu-id="8a689-109">By showcasing products targeted to a customer's interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="8a689-110">Programmatūrā Dynamics 365 for Retail preču ieteikumi tiek nodrošināti, izmantojot pakalpojumu Cognitive Services un Microsoft Azure algoritmisko mācīšanos.</span><span class="sxs-lookup"><span data-stu-id="8a689-110">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

## <a name="scenarios"></a><span data-ttu-id="8a689-111">Scenāriji</span><span class="sxs-lookup"><span data-stu-id="8a689-111">Scenarios</span></span>

<span data-ttu-id="8a689-112">Preču ieteikumi ir iespējoti tālāk norādītajos POS scenārijos.</span><span class="sxs-lookup"><span data-stu-id="8a689-112">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="8a689-113">Tie ir pieejami programmā Cloud POS vai Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="8a689-113">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="8a689-114">Lapā **Detalizēta informācija par preci**.</span><span class="sxs-lookup"><span data-stu-id="8a689-114">On the **Product details** page:</span></span>

    - <span data-ttu-id="8a689-115">Ja veikala darbinieks apmeklē lapu **Detalizēta informācija par precei**, skatot iepriekšējās transakcijas dažādos kanālos, ieteikumu programma piedāvā papildu preces, kas var tikt nopirktas kopā.</span><span class="sxs-lookup"><span data-stu-id="8a689-115">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
    - <span data-ttu-id="8a689-116">Ja veikala darbinieks pievieno transakcijai debitoru un pēc tam apmeklē lapu **Detalizēta informācija par preci**, ieteikumu programma nodrošina personalizētus ieteikumus, izmantojot debitora transakciju vēsturi.</span><span class="sxs-lookup"><span data-stu-id="8a689-116">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

    <span data-ttu-id="8a689-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="8a689-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="8a689-118">Lapā **Transakcija**.</span><span class="sxs-lookup"><span data-stu-id="8a689-118">On the **Transaction** page:</span></span>

    - <span data-ttu-id="8a689-119">Ieteikumu programma iesaka preces, pamatojoties uz visu grozam pievienoto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="8a689-119">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
    - <span data-ttu-id="8a689-120">Ja veikala darbinieks pievieno transakcijai debitoru, ieteikumu programma nodrošina personalizētus ieteikumus, izmantojot debitora transakciju vēsturi un grozam pievienoto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="8a689-120">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer's transaction history and the list of items in the basket.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a689-121">Lai lapā **Transakcija** tiktu rādīti ieteikumi, mazumtirgotājam ir jāatjaunina ekrāna izkārtojums programmatūrā Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="8a689-121">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="8a689-122">Lapā **Transakcijas** ir jāaktivizē vadīkla **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="8a689-122">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span>

    <span data-ttu-id="8a689-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="8a689-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3. <span data-ttu-id="8a689-124">Lapā **Detalizēta informācija par debitoru**.</span><span class="sxs-lookup"><span data-stu-id="8a689-124">On the **Customer details** page:</span></span>

    - <span data-ttu-id="8a689-125">Ieteikumu programma iesaka preces, pamatojoties uz lietotāja ID un precēm debitora velmju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="8a689-125">The recommendation engine suggests items based on the user ID and items in the customer's wish list.</span></span>

    <span data-ttu-id="8a689-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="8a689-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="8a689-127">Dynamics 365 for Retail konfigurēšana, lai iespējotu POS ieteikumus</span><span class="sxs-lookup"><span data-stu-id="8a689-127">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>

<span data-ttu-id="8a689-128">Lai iestatītu preču ieteikumus, ir jāveic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8a689-128">To set up product recommendations, you need to do the following.</span></span>

1. <span data-ttu-id="8a689-129">Pārliecinieties, ka laukā **Juridiskā persona** ir atlasīta vajadzīgā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="8a689-129">Make sure that you have selected the correct **Legal entity**.</span></span>
2. <span data-ttu-id="8a689-130">Pārejiet uz sadaļu **Elementu krātuve**, atlasiet **Pārdošana mazumtirdzniecībā** un pēc tam noklikšķiniet uz **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="8a689-130">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="8a689-131">Šai funkcijai tiek izmantoti demonstrācijas dati (vai jūsu dati) no jūsu operāciju datu bāzes, un šie dati tiek pārvietoti uz elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="8a689-131">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3. <span data-ttu-id="8a689-132">Pēc izvēles. Lai transakciju ekrānā tiktu rādīti ieteikumi, pārejiet uz sadaļu **Ekrāna izkārtojums**, izvēlieties savu ekrāna izkārtojumu, palaidiet līdzekli **Ekrāna izkārtojuma dizainers** un pēc tam aktivizējiet vadīklu **ieteikumi**, kur nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="8a689-132">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="8a689-133">Pārejiet uz sadaļu **Mazumtirdzniecības parametri**, atlasiet vienumu **Algoritmiskā mācīšanās** un sadaļā **Iespējot POS ieteikumus** atlasiet vienumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8a689-133">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="8a689-134">Lai POS tiktu rādīti ieteikumi, palaidiet globālās konfigurācijas darbu Nr. **1110**.</span><span class="sxs-lookup"><span data-stu-id="8a689-134">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="8a689-135">Lai atainotu POS ekrāna izkārtojuma dizainerī veiktās izmaiņas, palaidiet kanāla konfigurācijas darbu Nr. **1070**.</span><span class="sxs-lookup"><span data-stu-id="8a689-135">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="8a689-136">Kā tas notiek?</span><span class="sxs-lookup"><span data-stu-id="8a689-136">How does it work?</span></span>

<span data-ttu-id="8a689-137">Kad atsvaidzināt elementu **Elementu krātuve**, tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8a689-137">When you refresh the **Entity store** entity, the following actions take place.</span></span>

- <span data-ttu-id="8a689-138">No programmatūras Dynamics 365 for Retail operāciju datu bāzes tiek izgūti dati, kuru formāts atbilst Cognitive Services nepieciešamajam formātam, un šie dati tiek nosūtīti uz elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="8a689-138">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="8a689-139">Šie dati tiek izmantoti pakalpojumā Azure Data Factory (ADF), lai ADF aktivitāšu ietvaros attīrītu datus, izmantojot Hive skriptus.</span><span class="sxs-lookup"><span data-stu-id="8a689-139">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="8a689-140">Attīrītie dati tiek uzglabāti BLOB krātuvē.</span><span class="sxs-lookup"><span data-stu-id="8a689-140">Cleansed data is stored in blob storage.</span></span>
- <span data-ttu-id="8a689-141">Dati no BLOB krātuves tiek izmantoti Cognitive Services API, lai apmācītu ieteikumu modeli.</span><span class="sxs-lookup"><span data-stu-id="8a689-141">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="8a689-142">Ja aktivizējat opciju **Iespējot ieteikumus** un palaižat konfigurācijas darbus, tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8a689-142">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

- <span data-ttu-id="8a689-143">No API tiek izgūti modeļa akreditācijas dati un ID, un tie tiek saglabāti Dynamics 365 for Retail operāciju datu bāzē (AOS failā web.config), kā arī mazumtirdzniecības serverī.</span><span class="sxs-lookup"><span data-stu-id="8a689-143">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
- <span data-ttu-id="8a689-144">Modeļa akreditācijas dati un ID tiek padarīti pieejami CRT, lai varētu izpildīt tiešsaistes preču ieteikumu izsaukumus no programmām Cloud POS un MPOS.</span><span class="sxs-lookup"><span data-stu-id="8a689-144">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="8a689-145">Problēmu novēršana, ja preču ieteikumi jau ir iespējoti</span><span class="sxs-lookup"><span data-stu-id="8a689-145">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="8a689-146">Pārejiet uz **Mazumtirdzniecības rekvizīti** \> **Algoritmiskā mācīšanās** \> **Atspējot preču ieteikumus** un palaidiet darbu **Globālais konfigurācijas darbs \[1110\]**.</span><span class="sxs-lookup"><span data-stu-id="8a689-146">Navigate to **Retail Parameters** \> **Machine learning** \> **Disable product recommendations** and run **Global configuration job \[1110\]**.</span></span> <span data-ttu-id="8a689-147">Ja nevarat atrast cilni **Algoritmiskā mācīšanās**, lūdzu, sazinieties ar Dynamics atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="8a689-147">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span>
- <span data-ttu-id="8a689-148">Ja darbību ekrānam pievienojāt vadīklu **Ieteikumus pārvaldība**, izmantojot **Ekrāna izkārtojuma dizainers**, lūdzu, noņemiet arī to.</span><span class="sxs-lookup"><span data-stu-id="8a689-148">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a689-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8a689-149">Additional resources</span></span>

[<span data-ttu-id="8a689-150">Ieteikumu vadīklas pievienošana POS ierīces lapā Transakcijas</span><span class="sxs-lookup"><span data-stu-id="8a689-150">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)

