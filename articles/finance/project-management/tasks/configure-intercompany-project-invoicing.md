---
title: Starpuzņēmumu projekta rēķinu izrakstīšanas konfigurēšana
description: Šajā tēma aprakstīts, kā iestatīt rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144283"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="4ce52-103">Starpuzņēmumu projekta rēķinu izrakstīšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="4ce52-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ce52-104">Šajā tēma aprakstīts, kā iestatīt rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="4ce52-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="4ce52-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="4ce52-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4ce52-106">Navigācijas rūtī pārejiet uz **Moduļi > Kreditori > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="4ce52-107">Sarakstā **Visi piegādātāji** atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4ce52-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="4ce52-108">Darbību rūtī atlasiet **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="4ce52-109">Atlasiet **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="4ce52-110">Iestatiet **Aktīva** kā **Jā**, lai iespējotu starpuzņēmumu tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="4ce52-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="4ce52-111">Ievadiet vai atlasiet vērtību laukā **Klienta uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="4ce52-112">Ievadiet vai atlasiet vērtību laukā **Mans konts**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="4ce52-113">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-113">Select **Save**.</span></span>
9. <span data-ttu-id="4ce52-114">Aizveriet lapas, lai atgrieztos lapā sākuma lapā.</span><span class="sxs-lookup"><span data-stu-id="4ce52-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="4ce52-115">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Projektu pārvaldība un uzskaite > Iestatīšana > Projektu pārvaldības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="4ce52-116">Atlasiet cilni **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="4ce52-117">Velciet slīdni uz **Jā**, lai iespējotu starpuzņēmumu resursu plānošanu un laika uzskaites tabulas.</span><span class="sxs-lookup"><span data-stu-id="4ce52-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="4ce52-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="4ce52-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4ce52-119">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-119">Select **New**.</span></span>
15. <span data-ttu-id="4ce52-120">Laukā **Juridiskā persona, kas aizņemas** atlasiet vai ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4ce52-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="4ce52-121">Atzīmējiet izvēles rūtiņu **Uzkrāt ieņēmumus**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="4ce52-122">Laukā **Noklusējuma laika uzskaites kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4ce52-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="4ce52-123">Laukā **Noklusējuma izdevumu hierarhija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4ce52-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="4ce52-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-124">Select **Save**.</span></span>
20. <span data-ttu-id="4ce52-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4ce52-125">Close the page.</span></span>
21. <span data-ttu-id="4ce52-126">Navigācijas rūtī ejiet uz sadaļu **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Publicēšana > Virsgrāmatas publicēšanas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="4ce52-127">Atlasiet opciju laukā **Virsgrāmatu kontu veidi**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="4ce52-128">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-128">Select **New**.</span></span>
24. <span data-ttu-id="4ce52-129">Jaunās rindas laukā **Galvenais konts** norādiet vajadzīgās vērtības.</span><span class="sxs-lookup"><span data-stu-id="4ce52-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="4ce52-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-130">Select **Save**.</span></span>
26. <span data-ttu-id="4ce52-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4ce52-131">Close the page.</span></span>
27. <span data-ttu-id="4ce52-132">Navigācijas rūtī ejiet uz sadaļu **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Cenas > Pārnešanas cena**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="4ce52-133">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-133">Select **New**.</span></span>
29. <span data-ttu-id="4ce52-134">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="4ce52-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="4ce52-135">Laukā **Juridiskā persona, kas aizņemas** atlasiet vai ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4ce52-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="4ce52-136">Atlasiet opciju laukā **Pārnešanas cenas modelis**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="4ce52-137">Laukā **Cenošana** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="4ce52-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="4ce52-138">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4ce52-138">Select **Save**.</span></span>

