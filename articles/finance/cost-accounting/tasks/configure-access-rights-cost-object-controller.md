---
title: Piekļuves tiesību konfigurēšana izmaksu objekta kontrolierim
description: Izmantojiet šo procedūru, lai konfigurētu izmaksu objekta kontroliera piekļuves tiesības.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88d6208e867bd322ddfc4e599856b1905fa8e19b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969382"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="33e5a-103">Piekļuves tiesību konfigurēšana izmaksu objekta kontrolierim</span><span class="sxs-lookup"><span data-stu-id="33e5a-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33e5a-104">Izmantojiet šo procedūru, lai konfigurētu izmaksu objekta kontroliera piekļuves tiesības.</span><span class="sxs-lookup"><span data-stu-id="33e5a-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="33e5a-105">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="33e5a-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="33e5a-106">Izmaksu objekta kontroliera lomas piešķire</span><span class="sxs-lookup"><span data-stu-id="33e5a-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="33e5a-107">Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.</span><span class="sxs-lookup"><span data-stu-id="33e5a-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="33e5a-108">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="33e5a-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="33e5a-109">Piemēram, filtrējiet pēc lauka Lietotājvārds, izmantojot vērtību "alicia".</span><span class="sxs-lookup"><span data-stu-id="33e5a-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="33e5a-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="33e5a-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="33e5a-111">Noklikšķiniet uz Piešķirt lomas.</span><span class="sxs-lookup"><span data-stu-id="33e5a-111">Click Assign roles.</span></span>
5. <span data-ttu-id="33e5a-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="33e5a-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="33e5a-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33e5a-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="33e5a-114">Piekļuves saraksta drošības iespējošana</span><span class="sxs-lookup"><span data-stu-id="33e5a-114">Enable access list security</span></span>
1. <span data-ttu-id="33e5a-115">Dodieties uz Izmaksu uzskaite > Dimensijas > Dimensiju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="33e5a-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="33e5a-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="33e5a-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="33e5a-117">Atlasiet Organizācija.</span><span class="sxs-lookup"><span data-stu-id="33e5a-117">Select Organization.</span></span>  
3. <span data-ttu-id="33e5a-118">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33e5a-118">Click Edit.</span></span>
4. <span data-ttu-id="33e5a-119">Laukā Piekļuves sarakstu hierarhija atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="33e5a-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="33e5a-120">Noklikšķiniet uz Skatīt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="33e5a-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="33e5a-121">Piekļuves tiesību piešķiršana lietotājam</span><span class="sxs-lookup"><span data-stu-id="33e5a-121">Assign access rights to user</span></span>
1. <span data-ttu-id="33e5a-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="33e5a-122">Click New.</span></span>
2. <span data-ttu-id="33e5a-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="33e5a-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="33e5a-124">Laukā Lietotāja ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="33e5a-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="33e5a-125">Atlasiet Administrators.</span><span class="sxs-lookup"><span data-stu-id="33e5a-125">Select Admin.</span></span>  
4. <span data-ttu-id="33e5a-126">Kokā atlasiet Organization\CEO\CFO\FIM.</span><span class="sxs-lookup"><span data-stu-id="33e5a-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="33e5a-127">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="33e5a-127">Click New.</span></span>
6. <span data-ttu-id="33e5a-128">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="33e5a-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="33e5a-129">Laukā Lietotāja ID ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="33e5a-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="33e5a-130">Atlasiet Alīsija.</span><span class="sxs-lookup"><span data-stu-id="33e5a-130">Select Alicia.</span></span>  
8. <span data-ttu-id="33e5a-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33e5a-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="33e5a-132">Piekļuves tiesību iespējošana vidē Izmaksu uzskaite</span><span class="sxs-lookup"><span data-stu-id="33e5a-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="33e5a-133">Dodieties uz Izmaksu uzskaite > Iestatījumi > Parametri.</span><span class="sxs-lookup"><span data-stu-id="33e5a-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="33e5a-134">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="33e5a-134">Click the General tab.</span></span>
3. <span data-ttu-id="33e5a-135">Laukā Iespējot skatīšanas piekļuvi izmaksu objekta dimensijas elementiem atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="33e5a-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="33e5a-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33e5a-136">Click Save.</span></span>
5. <span data-ttu-id="33e5a-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33e5a-137">Close the page.</span></span>
6. <span data-ttu-id="33e5a-138">Dodieties uz Izmaksu uzskaite > Iestatījumi > Izmaksu kontroles darbvietas konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="33e5a-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="33e5a-139">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33e5a-139">Click Edit.</span></span>
8. <span data-ttu-id="33e5a-140">Laukā Publicēts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="33e5a-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="33e5a-141">Atlasot Jā, lietotājs, kuram ir piešķirta viena no tālāk minētajām četrām lomām, var redzēt pārskatus izmaksu kontroles darbvietā: izmaksu uzskaites vadītājs, izmaksu grāmatvedis, izmaksu grāmatvedības darbinieks un izmaksu objekta kontrolieris.</span><span class="sxs-lookup"><span data-stu-id="33e5a-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="33e5a-142">Atlasot Nē, tikai lietotājs, kuram ir piešķirta viena no tālāk minētajām četrām lomām, var redzēt pārskatus: izmaksu uzskaites vadītājs un izmaksu grāmatvedības darbinieks.</span><span class="sxs-lookup"><span data-stu-id="33e5a-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="33e5a-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33e5a-143">Click Save.</span></span>

