--- 
title: "Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci"
description: "Šajā procedūrā parādīts, kā piešķirt pareizas lomas darbinieka lietotāja kontam un pēc tam ļaut darbiniekam veikt ražotnes ražotnes reģistrācijas."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5322d77af470c25f0849cbbfbbfbc4a50a7e859b
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="cc81a-103">Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci</span><span class="sxs-lookup"><span data-stu-id="cc81a-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc81a-104">Šajā procedūrā parādīts, kā piešķirt pareizas lomas darbinieka lietotāja kontam un pēc tam ļaut darbiniekam veikt ražotnes ražotnes reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="cc81a-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="cc81a-105">Lomu piešķiršana lietotāja kontam</span><span class="sxs-lookup"><span data-stu-id="cc81a-105">Assign roles to user account</span></span>
1. <span data-ttu-id="cc81a-106">Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.</span><span class="sxs-lookup"><span data-stu-id="cc81a-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="cc81a-107">Izmantojiet ātro filtru, lai filtrētu pēc darbinieka vārda, ja lietotāja konts ir saistīts ar mašīnas operatora lomu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="cc81a-108">Parauga datos vārds ir Šenona.</span><span class="sxs-lookup"><span data-stu-id="cc81a-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="cc81a-109">Iezīmējiet lietotāja konta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="cc81a-110">Sarakstā noklikšķiniet uz saites "Vārds" atlasītajā rindā, lai skatītu detalizētu informāciju par lietotāja kontu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="cc81a-111">Kokā atlasiet Lomas\Mašīnu operators.</span><span class="sxs-lookup"><span data-stu-id="cc81a-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="cc81a-112">Aizveriet detalizētas lietotāja informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-112">Close the user account details page.</span></span>
7. <span data-ttu-id="cc81a-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="cc81a-114">Konfigurējiet lietotāja kontu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-114">Configure worker account.</span></span>
1. <span data-ttu-id="cc81a-115">Pārejiet uz sadaļu Personāla vadība > Darbinieki > Darbinieki.</span><span class="sxs-lookup"><span data-stu-id="cc81a-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="cc81a-116">Izmantojiet ātro filtru, lai filtrētu pēc darbinieka vārda, ja lietotāja konts ir saistīts ar mašīnas operatora lomu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="cc81a-117">Parauga datos vārds ir Šenona.</span><span class="sxs-lookup"><span data-stu-id="cc81a-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="cc81a-118">Iezīmējiet lietotāja konta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="cc81a-119">Sarakstā noklikšķiniet uz saites "Vārds" atlasītajā rindā, lai skatītu detalizētu informāciju par lietotāja kontu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="cc81a-120">Noklikšķiniet uz cilnes Nodarbinātība.</span><span class="sxs-lookup"><span data-stu-id="cc81a-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="cc81a-121">Izvērsiet kopsavilkuma cilni Laika reģistrēšana un noklikšķiniet uz Aktivizēt reģistrācijas terminālos.</span><span class="sxs-lookup"><span data-stu-id="cc81a-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="cc81a-122">Noklikšķiniet uz Aktivizēt reģistrācijas terminālos.</span><span class="sxs-lookup"><span data-stu-id="cc81a-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="cc81a-123">Ievadiet vai atlasiet vērtību laukā Aprēķinu grupa.</span><span class="sxs-lookup"><span data-stu-id="cc81a-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="cc81a-124">Ievadiet vai atlasiet vērtību laukā Noklusējuma aprēķinu grupa.</span><span class="sxs-lookup"><span data-stu-id="cc81a-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="cc81a-125">Laukā Apstiprinājumu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc81a-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="cc81a-126">Laukā Standarta profils ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc81a-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="cc81a-127">Laukā Profilu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc81a-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="cc81a-128">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="cc81a-128">Click OK.</span></span>
14. <span data-ttu-id="cc81a-129">Noklikšķiniet uz Rediģēt, lai ievadītu jauna laika reģistrācijas darbinieka žetona numuru.</span><span class="sxs-lookup"><span data-stu-id="cc81a-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="cc81a-130">Laukā Žetona ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc81a-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="cc81a-131">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cc81a-131">Click Save.</span></span>
17. <span data-ttu-id="cc81a-132">Lietojiet saīsni SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="cc81a-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="cc81a-133">Aizveriet darbinieku detalizētas informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-133">Close the worker details page.</span></span>
19. <span data-ttu-id="cc81a-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="cc81a-135">Piešķiriet darbinieku ierīču grupai.</span><span class="sxs-lookup"><span data-stu-id="cc81a-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="cc81a-136">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Ražošanas izpilde > Konfigurēt ierīču darba karti.</span><span class="sxs-lookup"><span data-stu-id="cc81a-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="cc81a-137">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="cc81a-137">Click Add.</span></span>
3. <span data-ttu-id="cc81a-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cc81a-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cc81a-139">Click OK.</span></span>
5. <span data-ttu-id="cc81a-140">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="cc81a-140">Click Edit.</span></span>
6. <span data-ttu-id="cc81a-141">Laukā Ražošanas vienība var iestatīt noklusējuma filtru darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="cc81a-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="cc81a-142">Tas nodrošinās, ka, darbiniekam piesakoties ierīcē, tiek rādīti tikai ražošanas darbi atlasītajai ražošanas vienībai.</span><span class="sxs-lookup"><span data-stu-id="cc81a-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="cc81a-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cc81a-143">Close the page.</span></span>

