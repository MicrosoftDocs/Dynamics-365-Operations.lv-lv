---
title: Standarta darbaspēka un izdevumu izmaksu konfigurēšana
description: Šajā tēmā paskaidrots, kā iestatīt standarta darbaspēka izmaksas un projekta izdevumus.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140097"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="2ebda-103">Standarta darbaspēka un izdevumu izmaksu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2ebda-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ebda-104">Šajā tēmā paskaidrots, kā iestatīt standarta darbaspēka izmaksas un projekta izdevumus.</span><span class="sxs-lookup"><span data-stu-id="2ebda-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="2ebda-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="2ebda-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2ebda-106">Navigācijas rūtī ejiet uz sadaļu **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Cenas > Pašizmaksa (stundā)**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="2ebda-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-107">Select **New**.</span></span>
3. <span data-ttu-id="2ebda-108">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2ebda-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="2ebda-109">Laukā **Pašizmaksa** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2ebda-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="2ebda-110">Standarta izmaksu cenu varat iestatīt projekta kategorijai vai iestatīt izmaksu cenu pēc nodarbinātā koda, projekta numura, kategorijas, datuma vai jebkuras to kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="2ebda-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="2ebda-111">Izmaksu cena, kas tiek piemērota, ir izmaksu cena ar augstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="2ebda-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="2ebda-112">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-112">Select **Save**.</span></span>
6. <span data-ttu-id="2ebda-113">Navigācijas rūtī ejiet uz sadaļu **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Cenas > Pārdošanas cena (stundā)**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="2ebda-114">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-114">Select **New**.</span></span>
8. <span data-ttu-id="2ebda-115">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2ebda-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="2ebda-116">Laukā **Spēkā kam** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2ebda-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="2ebda-117">Laukā **Cenošana** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2ebda-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="2ebda-118">Var iestatīt standarta pārdošanas cenu stundu darbībām vai projekta kategorijai.</span><span class="sxs-lookup"><span data-stu-id="2ebda-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="2ebda-119">Arī pārdošanas cenas varat iestatīt pēc nodarbinātā koda, projekta koda, kategorijas, transakcijas datuma vai jebkuras to kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="2ebda-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="2ebda-120">Faktiskā pārdošanas cena, kas tiek piemērota, kad nodarbinātais transakciju ievada stundu žurnālā, ir pārdošanas cena ar visaugstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="2ebda-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="2ebda-121">Piemēram, ja ir iestatīta gan vispārējā pārdošanas cena, gan no nodarbinātā atkarīgā pārdošanas cena, tad tiek lietota no nodarbinātā atkarīgā pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="2ebda-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="2ebda-122">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-122">Select **Save**.</span></span>
12. <span data-ttu-id="2ebda-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2ebda-123">Close the page.</span></span>
13. <span data-ttu-id="2ebda-124">Navigācijas rūtī ejiet uz sadaļu **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Cenas > Pašizmaksa (izdevumi)**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="2ebda-125">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-125">Select **New**.</span></span>
15. <span data-ttu-id="2ebda-126">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2ebda-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="2ebda-127">Laukā **Pašizmaksa** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2ebda-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="2ebda-128">Var aizpildīt vairākus laukus, bet šis ir obligātais minimums, lai ierakstu saglabātu.</span><span class="sxs-lookup"><span data-stu-id="2ebda-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="2ebda-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-129">Select **Save**.</span></span>
18. <span data-ttu-id="2ebda-130">Navigācijas rūtī ejiet uz **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Cenas > Pārdošanas cena (izdevumi)**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="2ebda-131">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-131">Select **New**.</span></span>
20. <span data-ttu-id="2ebda-132">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2ebda-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="2ebda-133">Laukā **Spēkā kam** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2ebda-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="2ebda-134">Laukā **Cenošana** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2ebda-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="2ebda-135">Faktiskā pārdošanas cena, ko lieto, kad nodarbinātais transakciju ievada izdevumu žurnālā, ir pārdošanas cena ar visaugstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="2ebda-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="2ebda-136">Piemēram, ja ir iestatīta gan vispārējā, gan no nodarbinātā atkarīgā pārdošanas cena, tad tiek lietota no nodarbinātā atkarīgā pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="2ebda-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="2ebda-137">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2ebda-137">Select **Save**.</span></span>

