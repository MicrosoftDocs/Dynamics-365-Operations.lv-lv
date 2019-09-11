---
title: Tirgojošo vienību kārtošanas secības maiņa
description: Šajā tēmā paskaidroti jēdzieni saistība ar to, kā kontrolē parādīšanas secību dažādām tirgojošām vienībām pakalpojumā Microsoft Dynamics 365 for Retail.
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866165"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="feefa-103">Tirgojošo vienību kārtošanas secības maiņa</span><span class="sxs-lookup"><span data-stu-id="feefa-103">Change the sort order for merchandising entities</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="feefa-104">Mazumtirgotāji uzskata produkta pamanīšanu par primāro rīku mijiedarbībai ar klientiem visos mazumtirdzniecības kanālos.</span><span class="sxs-lookup"><span data-stu-id="feefa-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="feefa-105">Dažādas funkcionalitātes var palīdzēt viegli pamanīt produktus.</span><span class="sxs-lookup"><span data-stu-id="feefa-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="feefa-106">Piemēram, tie var pārlūkot kategorijas, meklēt un filtrēt.</span><span class="sxs-lookup"><span data-stu-id="feefa-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="feefa-107">Šajā tēmā paskaidroti jēdzieni saistībā ar to, kā kontrolē parādīšanas secību dažādām tirgojošām vienībām.</span><span class="sxs-lookup"><span data-stu-id="feefa-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="feefa-108">Tajā aprakstīts arī, kā mainīt kārtošanas secību.</span><span class="sxs-lookup"><span data-stu-id="feefa-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="feefa-109">Kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="feefa-109">Overview</span></span>

<span data-ttu-id="feefa-110">Atbalsts dažādu ar tirgojošo vienību saistītu šķirošanu ir ticis uzlabots.</span><span class="sxs-lookup"><span data-stu-id="feefa-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="feefa-111">Šis atbalsts tagad labāk saskaņots ar esošajiem klientu scenārijiem, kam iepriekš bija vajadzīgi paplašinājumi no ieviešanas partneriem.</span><span class="sxs-lookup"><span data-stu-id="feefa-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="feefa-112">Microsoft Dynamics 365 for Retail versijās, kas jaunākas par 10.0.5. versiju, kārtošanas secība kategorijām navigācijas hierarhijā bija alfabētiska.</span><span class="sxs-lookup"><span data-stu-id="feefa-112">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="feefa-113">Jaunā pielāgotā kārtošanas secība ļauj tirdzniecības vadītājiem konfigurēt kārtošanas secību dažādām tirgojošām vienībām starp visiem klientiem gala lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="feefa-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="feefa-114">Šie klienti ietver galvenās mītnes un zvanu centrus.</span><span class="sxs-lookup"><span data-stu-id="feefa-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="feefa-115">Konfigurēt parādīšanas secību kategorijām mazumtirdzniecības produkta hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="feefa-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="feefa-116">Pirms pabeigt šo procedūru, jūsu vidē jābūt instalētiem demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="feefa-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="feefa-117">Ejiet uz **Mazumtirdzniecība \> Produkti un kategorijas \> Mazumtirdzniecības produktu hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="feefa-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="feefa-118">Klikšķiniet uz **Rediģēt kategorijas hierarhiju**.</span><span class="sxs-lookup"><span data-stu-id="feefa-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="feefa-119">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="feefa-119">Click **Edit**.</span></span>
4. <span data-ttu-id="feefa-120">Kokā izvērsiet **VISI \> Aktīvais sports**.</span><span class="sxs-lookup"><span data-stu-id="feefa-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="feefa-121">Kokā izvērsiet **VISI \> Komandu sports**.</span><span class="sxs-lookup"><span data-stu-id="feefa-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="feefa-122">Laukā **Parādīšanas kārtība** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="feefa-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="feefa-123">(Skaitlis var būt negatīvs.)</span><span class="sxs-lookup"><span data-stu-id="feefa-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="feefa-124">Katrai papildu kategorijai, kam vēlaties mainīt secību, atkārtojiet 4.–6. darbību.</span><span class="sxs-lookup"><span data-stu-id="feefa-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="feefa-125">Rādīšanas secība kanāla navigācijas hierarhijai tiks rādīta galvenajā mītnē mazumtirdzniecības produkta hierarhijai un izlaistajiem produktiem pēc kategorijas.</span><span class="sxs-lookup"><span data-stu-id="feefa-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![Mazumtirdzniecības produktu hierarhija pielāgoti sakārtota ar negatīvām vērtībām.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Izlaistie produkti pēc kategorijas pielāgoti sakārtoti, balstoties uz mazumtirdzniecības produkta kategoriju.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="feefa-128">Konfigurējiet parādīšanas secību kategorijām kanālu navigācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="feefa-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="feefa-129">Pirms pabeigt šo procedūru, jūsu vidē jābūt instalētiem demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="feefa-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="feefa-130">Ejiet uz **Mazumtirdzniecība \> Produkti un kategorijas \> Kanāla navigācijas kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="feefa-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="feefa-131">Meklēšanas sarakstā atlasiet **Modes navigācija** hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="feefa-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="feefa-132">Klikšķiniet uz **Rediģēt kategorijas hierarhiju**.</span><span class="sxs-lookup"><span data-stu-id="feefa-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="feefa-133">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="feefa-133">Click **Edit**.</span></span>
5. <span data-ttu-id="feefa-134">Kokā atlasiet **Mode \> Sieviešu apģērbs \> Sieviešu kurpes**.</span><span class="sxs-lookup"><span data-stu-id="feefa-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="feefa-135">Laukā **Parādīšanas kārtība** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="feefa-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="feefa-136">Kokā atlasiet **Mode \> Sieviešu apģērbs \> Topi**.</span><span class="sxs-lookup"><span data-stu-id="feefa-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="feefa-137">Tāpat varat definēt kārtošanas secību apakškategorijām.</span><span class="sxs-lookup"><span data-stu-id="feefa-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="feefa-138">Kokā atlasiet **Mode \> Vīriešu apģērbs \> Brīvā stila krekli**.</span><span class="sxs-lookup"><span data-stu-id="feefa-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="feefa-139">Laukā **Parādīšanas kārtība** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="feefa-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="feefa-140">Kokā atlasiet **Mode \> Vīriešu apģērbs \> Mēteļi un jakas**.</span><span class="sxs-lookup"><span data-stu-id="feefa-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="feefa-141">Laukā **Parādīšanas kārtība** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="feefa-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="feefa-142">Atkārtojiet katrai papildu kategorijai, kam vēlaties mainīt secību.</span><span class="sxs-lookup"><span data-stu-id="feefa-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="feefa-143">Parādīšanas secība kanālu navigācijas hierarhijā ir parādīta galvenajā mītnē, katalogā un mazumtirdzniecības kanālos.</span><span class="sxs-lookup"><span data-stu-id="feefa-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![Kanālu navigācijas hierarhija pielāgoti sakārtota](./media/ChannelNavCustomSorted.png)

![Kataloga navigācijas hierarhija pielāgoti sakārtota, balstoties uz kanālu navigācijas hierarhiju.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS ar pielāgoti sakārtotām kategorijām](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="feefa-147">Pielāgotā kārtošanas secība pēc noklusējuma ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="feefa-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="feefa-148">Lai uzzinātu, kā ieslēgt šo un citas funkcijas, skatiet [Līdzekļu pārvaldība](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="feefa-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
