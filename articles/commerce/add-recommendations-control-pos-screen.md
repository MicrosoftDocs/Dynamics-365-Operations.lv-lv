---
title: Ieteikumu pievienošana transakciju ekrānam
description: Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: af2450b27106325a86f6db68f9791637694cda63
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413934"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="deaeb-103">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="deaeb-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="deaeb-104">Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="deaeb-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="deaeb-105">Lai iegūtu vairāk informācijas par preces ieteikumiem, lasiet  [preces ieteikumus POS dokumentācijā](product.md).</span><span class="sxs-lookup"><span data-stu-id="deaeb-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="deaeb-106">Ja izmantojat programmu Commerce , varat parādīt preču ieteikumus savā POS ierīcē.</span><span class="sxs-lookup"><span data-stu-id="deaeb-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="deaeb-107">Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="deaeb-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="deaeb-108">Atvērt izkārtojuma dizaineru</span><span class="sxs-lookup"><span data-stu-id="deaeb-108">Open Layout designer</span></span>

1. <span data-ttu-id="deaeb-109">Dodieties uz **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="deaeb-110">Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu.</span><span class="sxs-lookup"><span data-stu-id="deaeb-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="deaeb-111">Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="deaeb-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="deaeb-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="deaeb-113">Piemēram, atlasiet **Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="deaeb-114">Noklikšķiniet uz **Izkārtojuma dizainers**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="deaeb-115">Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="deaeb-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="deaeb-116">Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="deaeb-117">Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa.</span><span class="sxs-lookup"><span data-stu-id="deaeb-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="deaeb-118">Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.</span><span class="sxs-lookup"><span data-stu-id="deaeb-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="deaeb-119">[![Izkārtojuma veidotājs](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="deaeb-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="deaeb-120">Attēlojuma opcijas izvēle</span><span class="sxs-lookup"><span data-stu-id="deaeb-120">Choose a display option</span></span>

<span data-ttu-id="deaeb-121">Ir pieejamas divas konfigurācijas opcijas.</span><span class="sxs-lookup"><span data-stu-id="deaeb-121">There are two configurations options available.</span></span> <span data-ttu-id="deaeb-122">Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="deaeb-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="deaeb-123">Tālāk ir aprakstītas abas opcijas.</span><span class="sxs-lookup"><span data-stu-id="deaeb-123">The two options are:</span></span>

- <span data-ttu-id="deaeb-124">Ieteikumi ir redzami vienmēr.</span><span class="sxs-lookup"><span data-stu-id="deaeb-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="deaeb-125">Ekrāna labās puses režģī parādās cilne **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="deaeb-126">Izkārtojuma pielāgošana, lai ieteikumi būtu redzami vienmēr</span><span class="sxs-lookup"><span data-stu-id="deaeb-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="deaeb-127">Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="deaeb-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="deaeb-128">[![Transakcijas rindu informācijas apgabala augstums ir samazināts](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="deaeb-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="deaeb-129">No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā.</span><span class="sxs-lookup"><span data-stu-id="deaeb-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="deaeb-130">Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.</span><span class="sxs-lookup"><span data-stu-id="deaeb-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="deaeb-131">[![Izkārtojumam ir pievienota ieteikumu vadīkla](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="deaeb-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="deaeb-132">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="deaeb-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="deaeb-133">Pakalpojumā Commerce pārejiet uz **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecība un komercija IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="deaeb-134">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="deaeb-135">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="deaeb-136">Cilnes Ieteikumi pievienošana pogu režģim ekrāna labajā pusē</span><span class="sxs-lookup"><span data-stu-id="deaeb-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="deaeb-137">Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="deaeb-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="deaeb-138">Noklikšķiniet uz **Pielāgot**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-138">Click **Customize**.</span></span>

    <span data-ttu-id="deaeb-139">[![Pielāgošana — cilnes vadīklas dialoglodziņš](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="deaeb-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="deaeb-140">Noklikšķiniet uz **Jauna cilne**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-140">Click **New tab**.</span></span>
4. <span data-ttu-id="deaeb-141">Atrodiet jauno cilni, kuru tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="deaeb-141">Find the new tab that you just added.</span></span> <span data-ttu-id="deaeb-142">Iespējams, ir jāritina uz leju.</span><span class="sxs-lookup"><span data-stu-id="deaeb-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="deaeb-143">Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="deaeb-144">[![Ieteikto preču atlasīšana laukā Saturs](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="deaeb-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="deaeb-145">Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.</span><span class="sxs-lookup"><span data-stu-id="deaeb-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="deaeb-146">Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.</span><span class="sxs-lookup"><span data-stu-id="deaeb-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="deaeb-147">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-147">Click **OK**.</span></span> <span data-ttu-id="deaeb-148">Jaunā cilne kļūst redzama pogu režģī.</span><span class="sxs-lookup"><span data-stu-id="deaeb-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="deaeb-149">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="deaeb-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="deaeb-150">Pakalpojumā Commerce pārejiet uz **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecība un komercija IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="deaeb-151">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="deaeb-152">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="deaeb-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="deaeb-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="deaeb-153">Additional resources</span></span>

[<span data-ttu-id="deaeb-154">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="deaeb-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="deaeb-155">Iespējojiet Azure Data Lake Storage Dynamics 365 Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="deaeb-155">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="deaeb-156">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="deaeb-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="deaeb-157">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="deaeb-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="deaeb-158">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="deaeb-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="deaeb-159">Iespējot "veikala līdzīgie izskati" rekomendācijas</span><span class="sxs-lookup"><span data-stu-id="deaeb-159">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="deaeb-160">Preču ieteikumu pievienošana punktā POS</span><span class="sxs-lookup"><span data-stu-id="deaeb-160">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="deaeb-161">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="deaeb-161">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="deaeb-162">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="deaeb-162">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="deaeb-163">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="deaeb-163">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="deaeb-164">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="deaeb-164">Product recommendations FAQ</span></span>](faq-recommendations.md)
