---
title: Starpuzņēmumu projekta rēķinu izrakstīšanas konfigurēšana
description: Šajā procedūrā ir parādīts, kā iestatīt projekta rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53871db9223eef6ba78f2e327e60f45110891478
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838275"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="21aab-103">Starpuzņēmumu projekta rēķinu izrakstīšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="21aab-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21aab-104">Šajā procedūrā ir parādīts, kā iestatīt projekta rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="21aab-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="21aab-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="21aab-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="21aab-106">Pārejiet uz sadaļu Kreditori > Kreditori > Visi kreditori.</span><span class="sxs-lookup"><span data-stu-id="21aab-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="21aab-107">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="21aab-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="21aab-108">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="21aab-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="21aab-109">Noklikšķiniet uz Starpuzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="21aab-109">Click Intercompany.</span></span>
5. <span data-ttu-id="21aab-110">Vienumam Aktīvs iestatiet vērtību Jā, lai iespējotu starpuzņēmumu darījumus.</span><span class="sxs-lookup"><span data-stu-id="21aab-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="21aab-111">Laukā Debitora uzņēmums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="21aab-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="21aab-112">Laukā Mans konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="21aab-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="21aab-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="21aab-113">Click Save.</span></span>
9. <span data-ttu-id="21aab-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="21aab-114">Close the page.</span></span>
10. <span data-ttu-id="21aab-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="21aab-115">Close the page.</span></span>
11. <span data-ttu-id="21aab-116">Dodieties uz Projektu vadība un uzskaite > Iestatīšana > Projektu vadības un uzskaites parametri.</span><span class="sxs-lookup"><span data-stu-id="21aab-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="21aab-117">Noklikšķiniet uz cilnes Starpuzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="21aab-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="21aab-118">Slīdni pārvietojiet pozīcijā Jā, lai iespējotu starpuzņēmumu resursu plānošanu un laika uzskaites tabulas.</span><span class="sxs-lookup"><span data-stu-id="21aab-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="21aab-119">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="21aab-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="21aab-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="21aab-120">Click New.</span></span>
16. <span data-ttu-id="21aab-121">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="21aab-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="21aab-122">Laukā Juridiskā persona, kas aizņemas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="21aab-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="21aab-123">Atzīmējiet izvēles rūtiņu Uzkrāt ieņēmumus.</span><span class="sxs-lookup"><span data-stu-id="21aab-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="21aab-124">Laukā Noklusējuma darba laika uzskaites tabulas kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="21aab-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="21aab-125">Laukā Noklusējuma izdevumu kategorija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="21aab-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="21aab-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="21aab-126">Click Save.</span></span>
22. <span data-ttu-id="21aab-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="21aab-127">Close the page.</span></span>
23. <span data-ttu-id="21aab-128">Dodieties uz Projektu vadība un uzskaite > Iestatīšana > Grāmatošana > Grāmatošanas iestatījumi virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="21aab-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="21aab-129">Laukā Virsgrāmatas kontu tipi atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="21aab-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="21aab-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="21aab-130">Click New.</span></span>
26. <span data-ttu-id="21aab-131">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="21aab-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="21aab-132">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="21aab-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="21aab-133">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="21aab-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="21aab-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="21aab-134">Click Save.</span></span>
30. <span data-ttu-id="21aab-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="21aab-135">Close the page.</span></span>
31. <span data-ttu-id="21aab-136">Dodieties uz Projektu vadība un uzskaite > Iestatīšana > Cenas > Transfertcena.</span><span class="sxs-lookup"><span data-stu-id="21aab-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="21aab-137">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="21aab-137">Click New.</span></span>
33. <span data-ttu-id="21aab-138">Laukā Spēkā stāšanās datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="21aab-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="21aab-139">Laukā Juridiskā persona, kas aizņemas ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="21aab-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="21aab-140">Laukā Transfertcenas modelis atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="21aab-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="21aab-141">Laukā Cenu noteikšana ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="21aab-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="21aab-142">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="21aab-142">Click Save.</span></span>

