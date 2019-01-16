---
title: "Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam"
description: "Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmatūrā Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="1fef5-103">Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="1fef5-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1fef5-104">Mēs noņemam preču ieteikumu pakalpojuma pašreizējo versiju, jo pārveidojam šo līdzekli, pievienojot tam uzlabotu algoritmu un jaunākas uz mazumtirdzniecību orientētas iespējas.</span><span class="sxs-lookup"><span data-stu-id="1fef5-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="1fef5-105">Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="1fef5-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="1fef5-106">Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmatūrā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1fef5-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1fef5-107">Ja izmantojat programmatūru Microsoft Dynamics 365 for Retail, savā POS ierīcē varat rādīt preču ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="1fef5-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1fef5-108">*Ieteikumi* ir krājumi, kas jūsu klientam varētu interesēt, ņemot vērā klienta pirkumu vēsturi, krājumus šī klienta vēlmju sarakstā, kā arī krājumus, ko citi klienti iegādājās tiešsaistē un fiziskajos veikalos.</span><span class="sxs-lookup"><span data-stu-id="1fef5-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="1fef5-109">Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="1fef5-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="1fef5-110">Atvērt izkārtojuma dizaineru</span><span class="sxs-lookup"><span data-stu-id="1fef5-110">Open Layout designer</span></span>

1. <span data-ttu-id="1fef5-111">Pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="1fef5-112">Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu.</span><span class="sxs-lookup"><span data-stu-id="1fef5-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="1fef5-113">Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību “F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="1fef5-113">For example, filter on the **Screen layout ID** field using a value of 'F2CP16:9M'.</span></span>
3. <span data-ttu-id="1fef5-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1fef5-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="1fef5-115">Piemēram, atlasiet “Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="1fef5-115">For example, select 'Name: F2CP16:9M Screen Layout ID: F2CP16:9M'.</span></span>
4. <span data-ttu-id="1fef5-116">Noklikšķiniet uz **Izkārtojuma dizainers**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="1fef5-117">Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="1fef5-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="1fef5-118">Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="1fef5-119">Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa.</span><span class="sxs-lookup"><span data-stu-id="1fef5-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="1fef5-120">Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.</span><span class="sxs-lookup"><span data-stu-id="1fef5-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="1fef5-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="1fef5-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="1fef5-122">Attēlojuma opcijas izvēle</span><span class="sxs-lookup"><span data-stu-id="1fef5-122">Choose a display option</span></span>

<span data-ttu-id="1fef5-123">Ir pieejamas divas konfigurācijas opcijas.</span><span class="sxs-lookup"><span data-stu-id="1fef5-123">There are two configurations options available.</span></span> <span data-ttu-id="1fef5-124">Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="1fef5-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="1fef5-125">Tālāk ir aprakstītas abas opcijas.</span><span class="sxs-lookup"><span data-stu-id="1fef5-125">The two options are:</span></span>

- <span data-ttu-id="1fef5-126">Ieteikumi ir redzami vienmēr.</span><span class="sxs-lookup"><span data-stu-id="1fef5-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="1fef5-127">Ekrāna labās puses režģī parādās cilne **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="1fef5-128">Izkārtojuma pielāgošana, lai ieteikumi būtu redzami vienmēr</span><span class="sxs-lookup"><span data-stu-id="1fef5-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="1fef5-129">Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="1fef5-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="1fef5-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="1fef5-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="1fef5-131">No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā.</span><span class="sxs-lookup"><span data-stu-id="1fef5-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="1fef5-132">Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.</span><span class="sxs-lookup"><span data-stu-id="1fef5-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="1fef5-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="1fef5-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="1fef5-134">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="1fef5-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="1fef5-135">Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="1fef5-136">Sarakstā atlasiet vienumu  **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="1fef5-137">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="1fef5-138">Cilnes Ieteikumi pievienošana pogu režģim ekrāna labajā pusē</span><span class="sxs-lookup"><span data-stu-id="1fef5-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="1fef5-139">Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="1fef5-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="1fef5-140">Noklikšķiniet uz **Pielāgot**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-140">Click **Customize**.</span></span>

    <span data-ttu-id="1fef5-141">[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="1fef5-141">[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="1fef5-142">Noklikšķiniet uz **Jauna cilne**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-142">Click **New tab**.</span></span>
4. <span data-ttu-id="1fef5-143">Atrodiet jauno cilni, kuru tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="1fef5-143">Find the new tab that you just added.</span></span> <span data-ttu-id="1fef5-144">Iespējams, ir jāritina uz leju.</span><span class="sxs-lookup"><span data-stu-id="1fef5-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="1fef5-145">Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="1fef5-146">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="1fef5-146">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="1fef5-147">Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.</span><span class="sxs-lookup"><span data-stu-id="1fef5-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="1fef5-148">Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.</span><span class="sxs-lookup"><span data-stu-id="1fef5-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="1fef5-149">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-149">Click **OK**.</span></span> <span data-ttu-id="1fef5-150">Jaunā cilne kļūst redzama pogu režģī.</span><span class="sxs-lookup"><span data-stu-id="1fef5-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="1fef5-151">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="1fef5-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="1fef5-152">Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="1fef5-153">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="1fef5-154">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="1fef5-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1fef5-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1fef5-155">Additional resources</span></span>

[<span data-ttu-id="1fef5-156">Personalizētu preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="1fef5-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)

