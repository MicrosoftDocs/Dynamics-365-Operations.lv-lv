---
title: Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam
description: Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 for Retail.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811220"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="e1ca5-103">Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="e1ca5-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e1ca5-104">Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmā Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="e1ca5-105">Lai iegūtu vairāk informācijas par preces ieteikumiem, lasiet [preces ieteikumus POS dokumentācijā](product.md).</span><span class="sxs-lookup"><span data-stu-id="e1ca5-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="e1ca5-106">Ja izmantojat programmu Microsoft Dynamics 365 Retail, varat parādīt preču ieteikumus savā POS ierīcē.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-106">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="e1ca5-107">Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="e1ca5-108">Atvērt izkārtojuma dizaineru</span><span class="sxs-lookup"><span data-stu-id="e1ca5-108">Open Layout designer</span></span>

1. <span data-ttu-id="e1ca5-109">Pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="e1ca5-110">Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="e1ca5-111">Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="e1ca5-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="e1ca5-113">Piemēram, atlasiet **Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="e1ca5-114">Noklikšķiniet uz **Izkārtojuma dizainers**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="e1ca5-115">Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="e1ca5-116">Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="e1ca5-117">Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="e1ca5-118">Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="e1ca5-119">[![Izkārtojuma veidotājs](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="e1ca5-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="e1ca5-120">Attēlojuma opcijas izvēle</span><span class="sxs-lookup"><span data-stu-id="e1ca5-120">Choose a display option</span></span>

<span data-ttu-id="e1ca5-121">Ir pieejamas divas konfigurācijas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-121">There are two configurations options available.</span></span> <span data-ttu-id="e1ca5-122">Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="e1ca5-123">Tālāk ir aprakstītas abas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-123">The two options are:</span></span>

- <span data-ttu-id="e1ca5-124">Ieteikumi ir redzami vienmēr.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="e1ca5-125">Ekrāna labās puses režģī parādās cilne **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="e1ca5-126">Izkārtojuma pielāgošana, lai ieteikumi būtu redzami vienmēr</span><span class="sxs-lookup"><span data-stu-id="e1ca5-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="e1ca5-127">Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="e1ca5-128">[![Transakcijas rindu informācijas apgabala augstums ir samazināts](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="e1ca5-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="e1ca5-129">No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="e1ca5-130">Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="e1ca5-131">[![Izkārtojumam ir pievienota ieteikumu vadīkla](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="e1ca5-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="e1ca5-132">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="e1ca5-133">Programmā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-133">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="e1ca5-134">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="e1ca5-135">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="e1ca5-136">Cilnes Ieteikumi pievienošana pogu režģim ekrāna labajā pusē</span><span class="sxs-lookup"><span data-stu-id="e1ca5-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="e1ca5-137">Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="e1ca5-138">Noklikšķiniet uz **Pielāgot**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-138">Click **Customize**.</span></span>

    <span data-ttu-id="e1ca5-139">[![Pielāgošana — cilnes vadīklas dialoglodziņš](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="e1ca5-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="e1ca5-140">Noklikšķiniet uz **Jauna cilne**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-140">Click **New tab**.</span></span>
4. <span data-ttu-id="e1ca5-141">Atrodiet jauno cilni, kuru tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-141">Find the new tab that you just added.</span></span> <span data-ttu-id="e1ca5-142">Iespējams, ir jāritina uz leju.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="e1ca5-143">Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="e1ca5-144">[![Ieteikto preču atlasīšana laukā Saturs](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="e1ca5-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="e1ca5-145">Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="e1ca5-146">Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="e1ca5-147">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-147">Click **OK**.</span></span> <span data-ttu-id="e1ca5-148">Jaunā cilne kļūst redzama pogu režģī.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="e1ca5-149">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="e1ca5-150">Programmā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-150">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="e1ca5-151">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="e1ca5-152">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="e1ca5-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1ca5-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e1ca5-153">Additional resources</span></span>

[<span data-ttu-id="e1ca5-154">Preču ieteikumi punktā POS</span><span class="sxs-lookup"><span data-stu-id="e1ca5-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e1ca5-155">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="e1ca5-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
