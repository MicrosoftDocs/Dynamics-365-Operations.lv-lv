---
title: Finansiālās datu koplietošanas uzņēmumos konfigurēšana
description: Šajā procedūrā ir parādīts, kā konfigurēt, iespējot, pārbaudīt un atrisināt konfliktus, koplietojot datus starp uzņēmumiem.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35ec8fc809841c0830224646fb57b0e4e4d40ef4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752296"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="204d9-103">Finansiālās datu koplietošanas uzņēmumos konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="204d9-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="204d9-104">Šajā procedūrā ir parādīts, kā konfigurēt, iespējot, pārbaudīt un atrisināt konfliktus, koplietojot datus starp uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="204d9-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="204d9-105">Tajā tiek izmantots USMF uzņēmums un finanšu datu koplietošanas veidne.</span><span class="sxs-lookup"><span data-stu-id="204d9-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="204d9-106">Šim uzdevumu ceļvedim ir nepieciešama platforma Dynamics AX 7.1 vai jaunāka tās versija.</span><span class="sxs-lookup"><span data-stu-id="204d9-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="204d9-107">Pārejiet uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Darbvietas > Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="204d9-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="204d9-108">Noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="204d9-108">Click **Import**.</span></span>
3. <span data-ttu-id="204d9-109">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="204d9-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="204d9-110">Laukā **Avota datu formāts** atlasiet tipu Iepakojums.</span><span class="sxs-lookup"><span data-stu-id="204d9-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="204d9-111">Noklikšķiniet uz **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="204d9-111">Click **Upload**.</span></span> <span data-ttu-id="204d9-112">Dodieties uz finanšu datu koplietošanas veidņu pakotnes faila atrašanās vietu un atlasiet šo failu.</span><span class="sxs-lookup"><span data-stu-id="204d9-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="204d9-113">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="204d9-113">Click **Save**.</span></span>
6. <span data-ttu-id="204d9-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="204d9-114">In the list, mark the selected row.</span></span> <span data-ttu-id="204d9-115">Atlasiet tikko izveidoto datu koplietošanas politiku.</span><span class="sxs-lookup"><span data-stu-id="204d9-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="204d9-116">Noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="204d9-116">Click **Import**.</span></span>
8. <span data-ttu-id="204d9-117">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="204d9-117">Click **Close**.</span></span>
9. <span data-ttu-id="204d9-118">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="204d9-118">Refresh the page.</span></span>
10. <span data-ttu-id="204d9-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="204d9-119">Close the page.</span></span>
11. <span data-ttu-id="204d9-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="204d9-120">Close the page.</span></span>
12. <span data-ttu-id="204d9-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="204d9-121">Close the page.</span></span>
13. <span data-ttu-id="204d9-122">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Iestatīšana > Konfigurēt starpuzņēmumu datu koplietošanu**.</span><span class="sxs-lookup"><span data-stu-id="204d9-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="204d9-123">Sarakstā atrodiet un atlasiet vienumu **Maksāšanas dienas**.</span><span class="sxs-lookup"><span data-stu-id="204d9-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="204d9-124">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="204d9-124">Click **Add**.</span></span>
16. <span data-ttu-id="204d9-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="204d9-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="204d9-126">Laukā **Uzņēmums** ierakstiet vērtību “USSI”.</span><span class="sxs-lookup"><span data-stu-id="204d9-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="204d9-127">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="204d9-127">Click **Add**.</span></span>
19. <span data-ttu-id="204d9-128">Laukā **Uzņēmums** ierakstiet vērtību “USMF”.</span><span class="sxs-lookup"><span data-stu-id="204d9-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="204d9-129">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="204d9-129">Click **Save**.</span></span>
21. <span data-ttu-id="204d9-130">Noklikšķiniet uz **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="204d9-130">Click **Enable**.</span></span>
22. <span data-ttu-id="204d9-131">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="204d9-131">Click **Yes**.</span></span>
23. <span data-ttu-id="204d9-132">Noklikšķiniet uz **Atrast koplietošanas problēmas**.</span><span class="sxs-lookup"><span data-stu-id="204d9-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="204d9-133">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="204d9-133">Click **Yes**.</span></span>
25. <span data-ttu-id="204d9-134">Noklikšķiniet uz **Atjaunināt lauka vērtību**.</span><span class="sxs-lookup"><span data-stu-id="204d9-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="204d9-135">Noklikšķiniet uz **Izmantot vērtību no uzņēmuma 1**.</span><span class="sxs-lookup"><span data-stu-id="204d9-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="204d9-136">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="204d9-136">Refresh the page.</span></span>
28. <span data-ttu-id="204d9-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="204d9-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]