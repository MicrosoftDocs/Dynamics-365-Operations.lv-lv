---
title: "Kanālam raksturīgo atlaižu definēšana"
description: "Bieži vien mazumtirgotāji dažādos kanālos iestata dažādas atlaides. Šajā tēmā ir pārskatītas koncepcijas, kas jums ir jāzina, lai izveidotu atlaidi noteiktam kanālam."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f68400bf10b6235decc7ac5cb82e58b369c7c0c7
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="cc2e6-104">Kanālam raksturīgo atlaižu definēšana</span><span class="sxs-lookup"><span data-stu-id="cc2e6-104">Define channel-specific discounts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="cc2e6-105">Bieži vien mazumtirgotāji dažādos kanālos iestata dažādas atlaides.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="cc2e6-106">Šajā tēmā ir pārskatītas koncepcijas, kas jums ir jāzina, lai izveidotu atlaidi noteiktam kanālam.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span> 

<a name="channel-specific-discounts"></a><span data-ttu-id="cc2e6-107">Kanālam raksturīgās atlaides</span><span class="sxs-lookup"><span data-stu-id="cc2e6-107">Channel-specific discounts</span></span>
--------------------------

<span data-ttu-id="cc2e6-108">Bieži vien mazumtirgotāji dažādos kanālos piedāvā dažādas atlaides.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="cc2e6-109">Iespējams, tas tiek darīts ar mērķi strādāt atbilstoši vietējā tirgus apstākļiem vai tikt galā ar konkurējošiem mazumtirgotājiem.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="cc2e6-110">Programmatūrā Dynamics 365 for Retail kanālam raksturīgās atlaides tiek definētas, izmantojot cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="cc2e6-111">Cenu grupas var piešķirt vienam vai vairākiem no šiem elementiem: kanāli, katalogi, piederības un lojalitātes programmas.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="cc2e6-112">Šajā rakstā ir aprakstīti kanāli, bet šie paši principi attiecas uz katalogu atlaidēm, piederības atlaidēm un lojalitātes atlaidēm.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="cc2e6-113">Cenu grupas</span><span class="sxs-lookup"><span data-stu-id="cc2e6-113">Price groups</span></span>

<span data-ttu-id="cc2e6-114">[![Cenu grupas](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="cc2e6-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="cc2e6-115">Iepriekšējā diagrammā ir parādītas attiecības starp elementiem, kas var būt transakcijā (kanāls, katalogs, piederība, debitors, lojalitātes programmas karte), un dažādiem atlaižu tipiem, kurus iespējams konfigurēt.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="cc2e6-116">Visas transakcijas notiek kādā kanālā, tāpēc ir garantēts, ka transakcijā atrodas kanāls.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="cc2e6-117">Atlikušie elementi nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-117">The remaining entities are optional.</span></span> <span data-ttu-id="cc2e6-118">Katrā pamatdatu lapā ir saite uz saistīto cenu grupu lapu, kur pēc nepieciešamības var apskatīt un pievienot cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="cc2e6-119">Cenu grupa tiek lietota, lai četru dažādu tipu elementus saistītu ar atlaidēm, cenu korekcijām un tirdzniecības līgumiem.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="cc2e6-120">Iesakām plānot stratēģiju veidam, kā piešķirt nosaukumu savām cenu grupām, lai tās uzturētu kārtībā.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="cc2e6-121">Viena iespēja — izmantot burtu vai numuru prefiksu vai sufiksu, lai atšķirtu dažādus tipus.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="cc2e6-122">Piemēram, izmantot nosaukumu 1-xxxxx kanāla cenu grupām un izmantot nosaukumu 2-xxxxx kataloga cenu grupām.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="cc2e6-123">Pastāv četras pieprasījumu lapas, kas ir koncentrētas uz katru no mazumtirdzniecības elementiem, ar kuriem var būt saistītas atlaides.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

-   <span data-ttu-id="cc2e6-124">**Mazumtirdzniecības kanāla cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts kanālu un atlaižu saraksts.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-124">**Retail channel price groups** - This page shows a list of channels and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="cc2e6-125">**Kataloga cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts katalogu un atlaižu saraksts.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-125">**Catalog price groups** - This page shows a list of catalogs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="cc2e6-126">**Lojalitātes programmas cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts lojalitātes programmu un atlaižu saraksts.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-126">**Loyalty price groups** - This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="cc2e6-127">**Piederības cenu grupas** — šajā lapā katrai cenu grupai tiek rādīts saistīts piederību un atlaižu saraksts.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-127">**Affiliation price groups** - This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="cc2e6-128">Kanāla atlaižu iestatīšanas piemērs</span><span class="sxs-lookup"><span data-stu-id="cc2e6-128">Example channel discount set up</span></span>
<span data-ttu-id="cc2e6-129">Nākamajā piemērā ir parādīti kanāla atlaižu iestatīšanas procedūrā iesaistītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1.  <span data-ttu-id="cc2e6-130">Šim piemēram jums ir kanāls ar nosaukumu **Houston**, un jūs grasāties izveidot jaunu atlaidi ar nosaukumu **Back-to-School.**</span><span class="sxs-lookup"><span data-stu-id="cc2e6-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School.**</span></span>
2.  <span data-ttu-id="cc2e6-131">Tā kā cenu noteikšanas un atlaižu stratēģija ietver kanāla atlaižu iespēju, kad veidojat kanālu, vienmēr varat izveidot kanālam raksturīgu cenu grupu.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3.  <span data-ttu-id="cc2e6-132">Jums ir cenu grupa **Houston-PG**, un tā ir piešķirta kanālam **Houston**.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4.  <span data-ttu-id="cc2e6-133">Kad ir izveidota jaunā atlaide **Back-to-School**, jums ir jānoklikšķina uz vienuma **Cenu grupas**, kas atrodas lapas **Atlaide** augšpusē.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="cc2e6-134">Tiek atvērta lapa **Atlaides cenu grupas**.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="cc2e6-135">Pēc tam noklikšķiniet uz **Jauns** un atlasiet cenu grupu **Houston-PG**.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5.  <span data-ttu-id="cc2e6-136">Tagad šo atlaidi varat iespējot un sākt to izmantot kanālā.</span><span class="sxs-lookup"><span data-stu-id="cc2e6-136">Now you can enable the discount and push it to the channel.</span></span>

 

<a name="see-also"></a><span data-ttu-id="cc2e6-137">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="cc2e6-137">See also</span></span>
--------

[<span data-ttu-id="cc2e6-138">Cenu korekcijas un atlaides</span><span class="sxs-lookup"><span data-stu-id="cc2e6-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)




