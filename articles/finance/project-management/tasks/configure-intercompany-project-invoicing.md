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
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174447"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="aa44a-103">Starpuzņēmumu projekta rēķinu izrakstīšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="aa44a-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa44a-104">Šajā tēma aprakstīts, kā iestatīt rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="aa44a-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="aa44a-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="aa44a-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="aa44a-106">Navigācijas rūtī pārejiet uz **Moduļi > Kreditori > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="aa44a-107">Sarakstā **Visi piegādātāji** atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="aa44a-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="aa44a-108">Darbību rūtī atlasiet **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="aa44a-109">Atlasiet **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="aa44a-110">Iestatiet **Aktīva** kā **Jā**, lai iespējotu starpuzņēmumu tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="aa44a-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="aa44a-111">Ievadiet vai atlasiet vērtību laukā **Klienta uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="aa44a-112">Ievadiet vai atlasiet vērtību laukā **Mans konts**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="aa44a-113">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-113">Select **Save**.</span></span>
9. <span data-ttu-id="aa44a-114">Aizveriet lapas, lai atgrieztos lapā sākuma lapā.</span><span class="sxs-lookup"><span data-stu-id="aa44a-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="aa44a-115">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Projektu pārvaldība un uzskaite > Iestatīšana > Projektu pārvaldības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="aa44a-116">Atlasiet cilni **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="aa44a-117">Velciet slīdni uz **Jā**, lai iespējotu starpuzņēmumu resursu plānošanu un laika uzskaites tabulas.</span><span class="sxs-lookup"><span data-stu-id="aa44a-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="aa44a-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="aa44a-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="aa44a-119">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-119">Select **New**.</span></span>
15. <span data-ttu-id="aa44a-120">Laukā **Juridiskā persona, kas aizņemas** atlasiet vai ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa44a-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="aa44a-121">Atzīmējiet izvēles rūtiņu **Uzkrāt ieņēmumus**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="aa44a-122">Laukā **Noklusējuma laika uzskaites kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa44a-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="aa44a-123">Laukā **Noklusējuma izdevumu hierarhija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa44a-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="aa44a-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-124">Select **Save**.</span></span>
20. <span data-ttu-id="aa44a-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="aa44a-125">Close the page.</span></span>
21. <span data-ttu-id="aa44a-126">Navigācijas rūtī ejiet uz sadaļu **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Publicēšana > Virsgrāmatas publicēšanas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="aa44a-127">Atlasiet opciju laukā **Virsgrāmatu kontu veidi**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="aa44a-128">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-128">Select **New**.</span></span>
24. <span data-ttu-id="aa44a-129">Jaunās rindas laukā **Galvenais konts** norādiet vajadzīgās vērtības.</span><span class="sxs-lookup"><span data-stu-id="aa44a-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="aa44a-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-130">Select **Save**.</span></span>
26. <span data-ttu-id="aa44a-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="aa44a-131">Close the page.</span></span>
27. <span data-ttu-id="aa44a-132">Navigācijas rūtī ejiet uz sadaļu **Moduļi > Projektu vadība un uzskaite > Iestatīšana > Cenas > Pārnešanas cena**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="aa44a-133">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-133">Select **New**.</span></span>
29. <span data-ttu-id="aa44a-134">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="aa44a-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="aa44a-135">Laukā **Juridiskā persona, kas aizņemas** atlasiet vai ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="aa44a-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="aa44a-136">Atlasiet opciju laukā **Pārnešanas cenas modelis**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="aa44a-137">Laukā **Cenošana** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="aa44a-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="aa44a-138">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="aa44a-138">Select **Save**.</span></span>

