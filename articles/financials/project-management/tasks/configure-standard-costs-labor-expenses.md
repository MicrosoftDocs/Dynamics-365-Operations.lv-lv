--- 
title: "Standarta darbaspēka un izdevumu izmaksu konfigurēšana"
description: "Šajā procedūrā ir parādīts, kā projektam iestatīt standarta izmaksas par darbaspēku un izdevumiem."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 432b5b195b29fb03786cb0560e277735b531b7d7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="f325b-103">Standarta darbaspēka un izdevumu izmaksu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="f325b-103">Configure standard costs for labor and expenses</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f325b-104">Šajā procedūrā ir parādīts, kā projektam iestatīt standarta izmaksas par darbaspēku un izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="f325b-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="f325b-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="f325b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f325b-106">Dodieties uz Projektu vadība un uzskaite > Iestatīšana > Cenas > Izmaksu cena (stunda).</span><span class="sxs-lookup"><span data-stu-id="f325b-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="f325b-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f325b-107">Click New.</span></span>
3. <span data-ttu-id="f325b-108">Laukā Spēkā stāšanās datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="f325b-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="f325b-109">Laukā Vienības cena, ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f325b-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="f325b-110">Standarta izmaksu cenu varat iestatīt projekta kategorijai vai iestatīt izmaksu cenu pēc nodarbinātā koda, projekta numura, kategorijas, datuma vai jebkuras to kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="f325b-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="f325b-111">Izmaksu cena, kas tiek piemērota, ir izmaksu cena ar augstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="f325b-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="f325b-112">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f325b-112">Click Save.</span></span>
6. <span data-ttu-id="f325b-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f325b-113">Close the page.</span></span>
7. <span data-ttu-id="f325b-114">Dodieties uz Projektu vadība un uzskaite > Iestatīšana > Cenas > Pārdošanas cena (stunda).</span><span class="sxs-lookup"><span data-stu-id="f325b-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="f325b-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f325b-115">Click New.</span></span>
9. <span data-ttu-id="f325b-116">Laukā Spēkā stāšanās datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="f325b-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="f325b-117">Atlasiet opciju laukā Derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="f325b-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="f325b-118">Laukā Cenu noteikšana ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f325b-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="f325b-119">Var iestatīt standarta pārdošanas cenu stundu darbībām vai projekta kategorijai.</span><span class="sxs-lookup"><span data-stu-id="f325b-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="f325b-120">Arī pārdošanas cenas varat iestatīt pēc nodarbinātā koda, projekta koda, kategorijas, transakcijas datuma vai jebkuras to kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="f325b-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="f325b-121">Faktiskā pārdošanas cena, kas tiek piemērota, kad nodarbinātais transakciju ievada stundu žurnālā, ir pārdošanas cena ar visaugstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="f325b-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f325b-122">Piemēram, ja ir iestatīta gan vispārējā pārdošanas cena, gan no nodarbinātā atkarīgā pārdošanas cena, tad tiek lietota no nodarbinātā atkarīgā pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="f325b-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="f325b-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f325b-123">Click Save.</span></span>
13. <span data-ttu-id="f325b-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f325b-124">Close the page.</span></span>
14. <span data-ttu-id="f325b-125">Dodieties uz Projektu vadība un uzskaite > Iestatīšana > Cenas > Izmaksu cena (izdevumi).</span><span class="sxs-lookup"><span data-stu-id="f325b-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="f325b-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f325b-126">Click New.</span></span>
16. <span data-ttu-id="f325b-127">Laukā Spēkā stāšanās datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="f325b-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="f325b-128">Laukā Vienības cena, ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f325b-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="f325b-129">Var aizpildīt vairākus laukus, bet šis ir obligātais minimums, lai ierakstu saglabātu.</span><span class="sxs-lookup"><span data-stu-id="f325b-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="f325b-130">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f325b-130">Click Save.</span></span>
19. <span data-ttu-id="f325b-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f325b-131">Close the page.</span></span>
20. <span data-ttu-id="f325b-132">Dodieties uz Projektu vadība un uzskaite > Iestatīšana > Cenas > Pārdošanas cena (izdevumi).</span><span class="sxs-lookup"><span data-stu-id="f325b-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="f325b-133">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f325b-133">Click New.</span></span>
22. <span data-ttu-id="f325b-134">Laukā Spēkā stāšanās datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="f325b-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="f325b-135">Atlasiet opciju laukā Derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="f325b-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="f325b-136">Laukā Cenu noteikšana ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f325b-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="f325b-137">Faktiskā pārdošanas cena, ko lieto, kad nodarbinātais transakciju ievada izdevumu žurnālā, ir pārdošanas cena ar visaugstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="f325b-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f325b-138">Piemēram, ja ir iestatīta gan vispārējā, gan no nodarbinātā atkarīgā pārdošanas cena, tad tiek lietota no nodarbinātā atkarīgā pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="f325b-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="f325b-139">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f325b-139">Click Save.</span></span>


