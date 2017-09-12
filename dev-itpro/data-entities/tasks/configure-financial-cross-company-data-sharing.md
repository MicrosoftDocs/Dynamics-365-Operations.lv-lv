--- 
title: "Finansiālās datu koplietošanas uzņēmumos konfigurēšana"
description: "Šajā procedūrā ir parādīts, kā konfigurēt, iespējot, pārbaudīt un atrisināt konfliktus, koplietojot datus starp uzņēmumiem."
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d36f19b5fa617169d33e7720e6a7602581cb525a
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="a7c93-103">Finansiālās datu koplietošanas uzņēmumos konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a7c93-103">Configure financial cross-company data sharing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7c93-104">Šajā procedūrā ir parādīts, kā konfigurēt, iespējot, pārbaudīt un atrisināt konfliktus, koplietojot datus starp uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="a7c93-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="a7c93-105">Tajā tiek izmantots USMF uzņēmums un finanšu datu koplietošanas veidne.</span><span class="sxs-lookup"><span data-stu-id="a7c93-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="a7c93-106">Šim uzdevumu ceļvedim ir nepieciešama Dynamics AX platforma 7.1 vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="a7c93-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="a7c93-107">Dodieties uz Sistēmas administrēšana > Darbvietas > Datu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="a7c93-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="a7c93-108">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="a7c93-108">Click Import.</span></span>
3. <span data-ttu-id="a7c93-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7c93-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a7c93-110">Avota datu formāta laukā atlasiet tipu Iepakojums.</span><span class="sxs-lookup"><span data-stu-id="a7c93-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="a7c93-111">Klikšķiniet Augšupielādēt.</span><span class="sxs-lookup"><span data-stu-id="a7c93-111">Click Upload.</span></span> <span data-ttu-id="a7c93-112">Dodieties uz finanšu datu koplietošanas veidņu pakotnes faila atrašanās vietu un atlasiet šo failu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="a7c93-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a7c93-113">Click Save.</span></span>
6. <span data-ttu-id="a7c93-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a7c93-115">Atlasiet tikko izveidoto datu koplietošanas politiku.</span><span class="sxs-lookup"><span data-stu-id="a7c93-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="a7c93-116">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="a7c93-116">Click Import.</span></span>
8. <span data-ttu-id="a7c93-117">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="a7c93-117">Click Close.</span></span>
9. <span data-ttu-id="a7c93-118">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-118">Refresh the page.</span></span>
10. <span data-ttu-id="a7c93-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-119">Close the page.</span></span>
11. <span data-ttu-id="a7c93-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-120">Close the page.</span></span>
12. <span data-ttu-id="a7c93-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-121">Close the page.</span></span>
13. <span data-ttu-id="a7c93-122">Dodieties uz Sistēmas administrēšana > Iestatīšana > Konfigurēt starpuzņēmumu datu koplietošanu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="a7c93-123">Sarakstā atrodiet un atlasiet vienumu Maksāšanas dienas.</span><span class="sxs-lookup"><span data-stu-id="a7c93-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="a7c93-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a7c93-124">Click Add.</span></span>
16. <span data-ttu-id="a7c93-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="a7c93-126">Laukā Uzņēmums ierakstiet vērtību “USSI”.</span><span class="sxs-lookup"><span data-stu-id="a7c93-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="a7c93-127">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a7c93-127">Click Add.</span></span>
19. <span data-ttu-id="a7c93-128">Laukā Uzņēmums ierakstiet vērtību “USMF”.</span><span class="sxs-lookup"><span data-stu-id="a7c93-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="a7c93-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a7c93-129">Click Save.</span></span>
21. <span data-ttu-id="a7c93-130">Noklikšķiniet uz Iespējot.</span><span class="sxs-lookup"><span data-stu-id="a7c93-130">Click Enable.</span></span>
22. <span data-ttu-id="a7c93-131">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a7c93-131">Click Yes.</span></span>
23. <span data-ttu-id="a7c93-132">Noklikšķiniet uz Atrast koplietošanas problēmas.</span><span class="sxs-lookup"><span data-stu-id="a7c93-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="a7c93-133">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a7c93-133">Click Yes.</span></span>
25. <span data-ttu-id="a7c93-134">Noklikšķiniet uz Atjaunināt lauka vērtību.</span><span class="sxs-lookup"><span data-stu-id="a7c93-134">Click Update field value.</span></span>
26. <span data-ttu-id="a7c93-135">Noklikšķiniet uz Izmantot vērtību no uzņēmuma 1.</span><span class="sxs-lookup"><span data-stu-id="a7c93-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="a7c93-136">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-136">Refresh the page.</span></span>
28. <span data-ttu-id="a7c93-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a7c93-137">Close the page.</span></span>


