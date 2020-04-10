---
title: " Kategorijas cenu noteikšanas kārtulas, lai izveidotu tirdzniecības līgumus"
description: Šajā procedūra ir aprakstīts, kā izveidot pārdošanas cenas tirdzniecības līgumus, izmantojot kategorijas cenu noteikšanas kārtulu.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21b1986aa36aab23f50a5af434435f9e93318e45
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141087"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="9e4ea-103"> Kategorijas cenu noteikšanas kārtulas, lai izveidotu tirdzniecības līgumus</span><span class="sxs-lookup"><span data-stu-id="9e4ea-103">Category pricing rules to create trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e4ea-104">Šajā procedūra ir aprakstīts, kā izveidot pārdošanas cenas tirdzniecības līgumus, izmantojot kategorijas cenu noteikšanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="9e4ea-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="9e4ea-106">Šis uzdevums ir paredzēts lomai Commerce preču pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="9e4ea-107">Noklikšķiniet uz Izcenojuma un atlaižu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="9e4ea-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-108">Click New.</span></span>
3. <span data-ttu-id="9e4ea-109">Noklikšķiniet uz Kategorijas cenu kārtula.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-109">Click Category price rule.</span></span>
4. <span data-ttu-id="9e4ea-110">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9e4ea-111">Lauka Konta kods atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="9e4ea-112">Konta koda veids Grupa tiek izmantots, lai iestatītu pārdošanas cenas tirdzniecības līgumus noteiktiem Kanāliem, Lojalitātes programmām, Katalogiem un Piederībām.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="9e4ea-113">Lauka Konta atlase ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="9e4ea-114">Laukā Kategorija ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="9e4ea-115">Laukā Summa/procenti ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="9e4ea-116">Laukā Noapaļošanas versija ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="9e4ea-117">Noklikšķiniet uz Ģenerēt tirdzniecības līgumus.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="9e4ea-118">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-118">Click Next.</span></span>
12. <span data-ttu-id="9e4ea-119">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="9e4ea-120">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="9e4ea-121">Laukā Meklēt nākamo atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="9e4ea-122">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-122">Click Next.</span></span>
16. <span data-ttu-id="9e4ea-123">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-123">Click Finish.</span></span>
    * <span data-ttu-id="9e4ea-124">Tādējādi tiek izveidots tirdzniecības līgumu žurnāls, kas tiek atvērts pārskatīšanai.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="9e4ea-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e4ea-126">Tirdzniecības līgumu žurnāli, kas izveidoti, izmantojot kategorijas cenu noteikšanas nosacījumus, netiek grāmatoti.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="9e4ea-127">Varat pārskatīt un rediģēt cenas, kas ģenerētas pirms to grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="9e4ea-128">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-128">Click Edit.</span></span>
19. <span data-ttu-id="9e4ea-129">Laukā Summa valūtā ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="9e4ea-130">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-130">Click Post.</span></span>
21. <span data-ttu-id="9e4ea-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-131">Click OK.</span></span>
22. <span data-ttu-id="9e4ea-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-132">Close the page.</span></span>
23. <span data-ttu-id="9e4ea-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-133">Close the page.</span></span>
24. <span data-ttu-id="9e4ea-134">Noklikšķiniet uz cilnes Kategorijas cenu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="9e4ea-135">Kanāla kategorijas cenu noteikšanas noteikumi būs redzami šajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="9e4ea-135">Channel specific Category pricing rules will show in this list.</span></span>  

