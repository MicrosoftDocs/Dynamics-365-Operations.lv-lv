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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 26b03b6712c97b12e1221598de308813c7986179
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="d9bd5-103">Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="d9bd5-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d9bd5-104">Mēs noņemam preču ieteikumu pakalpojuma pašreizējo versiju, jo pārveidojam šo līdzekli, pievienojot tam uzlabotu algoritmu un jaunākas uz mazumtirdzniecību orientētas iespējas.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="d9bd5-105">Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="d9bd5-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="d9bd5-106">Šajā tēmā ir aprakstīts, kā pārdošanas punkta (point of sale — POS) ierīces transakciju ekrānam pievienot ieteikumu vadīklu, izmantojot ekrāna izkārtojuma dizaineru programmatūrā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="d9bd5-107">Ja izmantojat programmatūru Microsoft Dynamics 365 for Retail, savā POS ierīcē varat rādīt preču ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d9bd5-108">*Ieteikumi* ir krājumi, kas jūsu klientam varētu interesēt, ņemot vērā klienta pirkumu vēsturi, krājumus šī klienta vēlmju sarakstā, kā arī krājumus, ko citi klienti iegādājās tiešsaistē un fiziskajos veikalos.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="d9bd5-109">Lai rādītu preču ieteikumus, transakciju ekrānam ir jāpievieno vadīkla, izmantojot ekrāna izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="d9bd5-110">Atvērt izkārtojuma dizaineru</span><span class="sxs-lookup"><span data-stu-id="d9bd5-110">Open Layout designer</span></span>
1.  <span data-ttu-id="d9bd5-111">Pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="d9bd5-112">Izmantojiet ātro filtru, lai atrastu ekrānu, kuram vēlaties pievienot šo vadīklu.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="d9bd5-113">Piemēram, filtrējiet pēc lauka **Ekrāna izkārtojuma ID**, izmantojot vērtību “F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="d9bd5-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="d9bd5-115">Piemēram, atlasiet “Nosaukums: F2CP16:9M Ekrāna izkārtojuma ID: F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="d9bd5-116">Noklikšķiniet uz **Izkārtojuma dizainers**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="d9bd5-117">Izpildiet uzvednēs sniegtos norādījumus, lai palaistu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="d9bd5-118">Kad tiek prasīti akreditācijas dati, ievadiet tos pašus akreditācijas datus, kurus izmantojāt, kad izkārtojuma dizainers tika palaists no lapas **Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="d9bd5-119">Kad esat pieteicies, tiek parādīta tālāk redzamajai lapai līdzīga lapa.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="d9bd5-120">Izkārtojums atšķiras atkarībā no jūsu veikalam veiktajiem pielāgojumiem.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="d9bd5-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Izvēlieties rādīšanas opciju</span><span class="sxs-lookup"><span data-stu-id="d9bd5-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="d9bd5-122">Ir pieejamas divas konfigurācijas opcijas.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-122">There are two configurations options available.</span></span> <span data-ttu-id="d9bd5-123">Izvēlieties savam veikalam vispiemērotāko opciju un izpildiet atlikušos norādījumus, lai pabeigtu šīs vadīklas iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="d9bd5-124">Tālāk ir aprakstītas abas opcijas.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-124">The two options are:</span></span>
-   <span data-ttu-id="d9bd5-125">Ieteikumi ir redzami vienmēr.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="d9bd5-126">Ekrāna labās puses režģī kļūst redzama cilne **Ieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="d9bd5-127">Lai ieteikumus padarītu redzamus vienmēr</span><span class="sxs-lookup"><span data-stu-id="d9bd5-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="d9bd5-128">Samaziniet transakcijas rindu informācijas apgabala augstumu, lai tas būtu vienāds ar debitora paneli kreisajā pusē.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="d9bd5-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="d9bd5-129">No kreisajā pusē esošās izvēlnes velciet un nometiet ieteikumu vadīklu apgabalā starp transakcijas rindas informāciju un pogu režģi transakcijas ekrāna apakšēja vidusdaļā.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="d9bd5-130">Mainiet vadīklas izmērus, lai tā ietilptu šajā laukumā.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="d9bd5-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="d9bd5-131">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="d9bd5-132">Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="d9bd5-133">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="d9bd5-134">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="d9bd5-135">Lai cilni Ieteikumi pievienotu pogu režģim ekrāna labajā pusē</span><span class="sxs-lookup"><span data-stu-id="d9bd5-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="d9bd5-136">Ar peles labo pogu noklikšķiniet uz tukšā laukuma zem pēdējās cilnes pogu režģī, kurš atrodas lapas labajā pusē.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="d9bd5-137">Noklikšķiniet uz **Pielāgot**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="d9bd5-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="d9bd5-138">Noklikšķiniet uz **Jauna cilne**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="d9bd5-139">Atrodiet jauno cilni, kuru tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-139">Find the new tab that you just added.</span></span> <span data-ttu-id="d9bd5-140">Iespējams, ir jāritina uz leju.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="d9bd5-141">Nolaižamajā sarakstā **Saturs** atlasiet vienumu **Ieteicamās preces**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="d9bd5-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="d9bd5-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="d9bd5-143">Laukā **Etiķete** ierakstiet ieteikumu cilnes nosaukumu. Ierakstiet, piemēram, “Ieteiktās preces”.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="d9bd5-144">Laukā **Attēls** atlasiet attēlu, kas ir jārāda šajā cilnē.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="d9bd5-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-145">Click **OK**.</span></span> <span data-ttu-id="d9bd5-146">Jaunā cilne kļūst redzama pogu režģī.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="d9bd5-147">Noklikšķiniet uz **X**, lai saglabātu un aizvērtu izkārtojuma dizaineru.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="d9bd5-148">Programmatūrā Dynamics 365 for Retail pārejiet uz sadaļu **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiki**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="d9bd5-149">Sarakstā atlasiet vienumu **1090 reģistri**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="d9bd5-150">Noklikšķiniet uz **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="d9bd5-150">Click **Run now**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="d9bd5-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d9bd5-151">Additional resources</span></span>
--------

[<span data-ttu-id="d9bd5-152">Personalizētu preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="d9bd5-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




