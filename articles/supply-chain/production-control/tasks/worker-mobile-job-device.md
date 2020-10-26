---
title: Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci
description: Šajā tēmā ir paskaidrots, kā piešķirt pareizas lomas darbinieka lietotāja kontam un pēc tam ļaut darbiniekam veikt ražotnes ražotnes reģistrācijas.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ada42a98a8a87e377f939d063b17f9904f6b3408
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978238"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="b9f7a-103">Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci</span><span class="sxs-lookup"><span data-stu-id="b9f7a-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9f7a-104">Šajā tēmā ir paskaidrots, kā piešķirt pareizas lomas darbinieka lietotāja kontam un pēc tam ļaut darbiniekam veikt ražotnes ražotnes reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="b9f7a-105">Pārbaudiet, vai darbiniekam ir piešķirta noteikta loma</span><span class="sxs-lookup"><span data-stu-id="b9f7a-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="b9f7a-106">Šajā piemērā, pirms konfigurējat darbinieka kontu, pārbaudiet, vai lietotājam "SHANNON" ir piešķirta mašīnas operatora loma.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="b9f7a-107">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Lietotāji > Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="b9f7a-108">Meklējiet lietotāju ātrajā filtrā.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="b9f7a-109">Šim piemēram ievadiet `shannon`.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="b9f7a-110">Atlasiet saiti parādītajā lietotāja konta kolonnā **Lietotāja ID**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="b9f7a-111">Kokā **Lietotāja lomas** atlasiet **Lomas > Mašīnas operators**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="b9f7a-112">Aizveriet lapas **Lietotāja informācija** un **Lietotāji**, lai atgrieztos sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="b9f7a-113">Darbinieka konta konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b9f7a-113">Configure worker account</span></span>
1. <span data-ttu-id="b9f7a-114">Dodieties uz **Navigācijas rūts > Moduļi > Cilvēkresursi > Darbinieki > Darbinieki**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="b9f7a-115">Meklējiet lietotāju ātrajā filtrā.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="b9f7a-116">Šim piemēram ievadiet `shannon`.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="b9f7a-117">Atlasiet saiti parādītajā lietotāja konta kolonnā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="b9f7a-118">Atlasiet cilni **Laika reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="b9f7a-119">Atlasiet **Aktivizēt reģistrācijas terminālos**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="b9f7a-120">Ievadiet vai atlasiet vērtības šādos laukos:</span><span class="sxs-lookup"><span data-stu-id="b9f7a-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="b9f7a-121">**Aprēķinu grupa**</span><span class="sxs-lookup"><span data-stu-id="b9f7a-121">**Calculation group**</span></span>  
    - <span data-ttu-id="b9f7a-122">**Noklusējuma aprēķinu grupa**</span><span class="sxs-lookup"><span data-stu-id="b9f7a-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="b9f7a-123">**Apstiprinājumu grupa**</span><span class="sxs-lookup"><span data-stu-id="b9f7a-123">**Approval group**</span></span>  
    - <span data-ttu-id="b9f7a-124">**Standarta profils**</span><span class="sxs-lookup"><span data-stu-id="b9f7a-124">**Standard profile**</span></span>  
    - <span data-ttu-id="b9f7a-125">**Profilu grupa**</span><span class="sxs-lookup"><span data-stu-id="b9f7a-125">**Profile group**</span></span>  

7. <span data-ttu-id="b9f7a-126">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-126">Select **OK**.</span></span>
8. <span data-ttu-id="b9f7a-127">Noklikšķiniet uz **Rediģēt**, lai ievadītu jauna laika reģistrācijas darbinieka žetona numuru.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="b9f7a-128">Ievadiet vērtību laukā **Žetona ID**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="b9f7a-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-129">Select **Save**.</span></span>
10. <span data-ttu-id="b9f7a-130">Aizveriet lapas **Nodarbinātā papildinformācija** un **Nodarbinātie**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="b9f7a-131">Nodarbinātā piešķiršana ierīču grupai</span><span class="sxs-lookup"><span data-stu-id="b9f7a-131">Assign worker to device group</span></span>
1. <span data-ttu-id="b9f7a-132">Pārejiet uz sadaļu **Ražošanas kontrole > Iestatīšana > Ražošanas izpilde > Konfigurēt ierīču darba karti**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="b9f7a-133">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-133">Select **Add**.</span></span>
3. <span data-ttu-id="b9f7a-134">Sarakstā atlasiet vēlamo nodarbināto.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-134">In the list, select the desired worker.</span></span> <span data-ttu-id="b9f7a-135">Šajā piemērā atlasiet **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="b9f7a-136">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-136">Select **OK**.</span></span>
5. <span data-ttu-id="b9f7a-137">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-137">Select **Edit**.</span></span>
6. <span data-ttu-id="b9f7a-138">Laukā **Ražošanas vienība** var iestatīt noklusējuma filtru nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="b9f7a-139">Tas nodrošinās, ka, darbiniekam piesakoties ierīcē, tiek rādīti tikai ražošanas darbi atlasītajai ražošanas vienībai.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="b9f7a-140">Ievadiet vēlamo vērtību.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-140">Enter the desired value.</span></span>
7. <span data-ttu-id="b9f7a-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b9f7a-141">Close the page.</span></span>

