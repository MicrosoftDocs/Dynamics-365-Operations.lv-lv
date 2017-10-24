---
title: "Pievienot ieteikumu vadīklu POS ierīces transakciju lapai"
description: "Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmatūrā Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cdfcbdcafdbbbab21c398ebc8002a45742e33e6
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="32b62-103">Pievienot ieteikumu vadīklu POS ierīces transakciju lapai</span><span class="sxs-lookup"><span data-stu-id="32b62-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="32b62-104">Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmatūrā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="32b62-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="32b62-105">Ja izmantojat programmatūru Microsoft Dynamics 365 for Retail, savā POS ierīcē varat rādīt preču ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="32b62-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="32b62-106">*Ieteikumi* ir krājumi, kas jūsu klientam varētu interesēt, ņemot vērā klienta pirkumu vēsturi, krājumus šī klienta vēlmju sarakstā, kā arī krājumus, ko citi klienti iegādājās tiešsaistē un fiziskajos veikalos.</span><span class="sxs-lookup"><span data-stu-id="32b62-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="32b62-107">Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="32b62-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="32b62-108">Atvērt izkārtojuma dizaineru</span><span class="sxs-lookup"><span data-stu-id="32b62-108">Open Layout designer</span></span>
1.  <span data-ttu-id="32b62-109">Pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="32b62-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="32b62-110">Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu.</span><span class="sxs-lookup"><span data-stu-id="32b62-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="32b62-111">Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību “F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="32b62-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="32b62-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="32b62-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="32b62-113">Piemēram, atlasiet “Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="32b62-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="32b62-114">Noklikšķiniet uz **Izkārtojuma dizainers**.</span><span class="sxs-lookup"><span data-stu-id="32b62-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="32b62-115">Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="32b62-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="32b62-116">Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="32b62-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="32b62-117">Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa.</span><span class="sxs-lookup"><span data-stu-id="32b62-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="32b62-118">Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.</span><span class="sxs-lookup"><span data-stu-id="32b62-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="32b62-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Izvēlieties rādīšanas opciju</span><span class="sxs-lookup"><span data-stu-id="32b62-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="32b62-120">Ir pieejamas divas konfigurācijas opcijas.</span><span class="sxs-lookup"><span data-stu-id="32b62-120">There are two configurations options available.</span></span> <span data-ttu-id="32b62-121">Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="32b62-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="32b62-122">Tālāk ir aprakstītas abas opcijas.</span><span class="sxs-lookup"><span data-stu-id="32b62-122">The two options are:</span></span>
-   <span data-ttu-id="32b62-123">Ieteikumi ir redzami vienmēr.</span><span class="sxs-lookup"><span data-stu-id="32b62-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="32b62-124">Ekrāna labās puses režģī kļūst redzama cilne **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="32b62-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="32b62-125">Lai ieteikumus padarītu redzamus vienmēr</span><span class="sxs-lookup"><span data-stu-id="32b62-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="32b62-126">Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="32b62-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="32b62-127">No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā.</span><span class="sxs-lookup"><span data-stu-id="32b62-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="32b62-128">Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="32b62-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="32b62-129">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="32b62-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="32b62-130">Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="32b62-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="32b62-131">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="32b62-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="32b62-132">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="32b62-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="32b62-133">Lai cilni Ieteikumi pievienotu pogu režģim ekrāna labajā pusē</span><span class="sxs-lookup"><span data-stu-id="32b62-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="32b62-134">Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="32b62-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="32b62-135">Noklikšķiniet uz **Pielāgot**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="32b62-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="32b62-136">Noklikšķiniet uz **Jauna cilne**.</span><span class="sxs-lookup"><span data-stu-id="32b62-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="32b62-137">Atrodiet jauno cilni, kuru tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="32b62-137">Find the new tab that you just added.</span></span> <span data-ttu-id="32b62-138">Iespējams, ir jāritina uz leju.</span><span class="sxs-lookup"><span data-stu-id="32b62-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="32b62-139">Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**.</span><span class="sxs-lookup"><span data-stu-id="32b62-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="32b62-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="32b62-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="32b62-141">Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.</span><span class="sxs-lookup"><span data-stu-id="32b62-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="32b62-142">Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.</span><span class="sxs-lookup"><span data-stu-id="32b62-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="32b62-143">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="32b62-143">Click **OK**.</span></span> <span data-ttu-id="32b62-144">Jaunā cilne kļūst redzama pogu režģī.</span><span class="sxs-lookup"><span data-stu-id="32b62-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="32b62-145">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="32b62-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="32b62-146">Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="32b62-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="32b62-147">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="32b62-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="32b62-148">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="32b62-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="32b62-149">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="32b62-149">See also</span></span>
--------

[<span data-ttu-id="32b62-150">Personalizētu preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="32b62-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




