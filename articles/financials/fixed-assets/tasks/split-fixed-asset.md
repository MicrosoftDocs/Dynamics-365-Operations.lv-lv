--- 
title: "Pamatlīdzekļa sadalīšana"
description: "Šis uzdevuma ceļvedis parādīs, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 86d07f07bd15d8b2dbbc987027b2e6976001f554
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="1e852-103">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="1e852-103">Split a fixed asset</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e852-104">Šis uzdevuma ceļvedis parādīs, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="1e852-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="1e852-105">Tas izmanto grāmatveža lomu un USMF demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="1e852-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="1e852-106">Izveidojiet jaunu pamatlīdzekli</span><span class="sxs-lookup"><span data-stu-id="1e852-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="1e852-107">Pārejiet uz sadaļu Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="1e852-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="1e852-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1e852-108">Click New.</span></span>
3. <span data-ttu-id="1e852-109">Ievadiet vai atlasiet vērtību laukā Pamatlīdzekļu grupa.</span><span class="sxs-lookup"><span data-stu-id="1e852-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="1e852-110">Ievērojiet pamatlīdzekļa numuru, kuru būs nepieciešams izmantot vēlāk sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="1e852-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="1e852-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1e852-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="1e852-112">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="1e852-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="1e852-113">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="1e852-113">Split a fixed asset</span></span>
1. <span data-ttu-id="1e852-114">Sarakstā atrodiet un atlasiet sadalāmo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="1e852-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="1e852-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1e852-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="1e852-116">Noklikšķiniet uz Grāmatas.</span><span class="sxs-lookup"><span data-stu-id="1e852-116">Click Books.</span></span>
    * <span data-ttu-id="1e852-117">Atlasiet grāmatu, kuru nodalīt jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="1e852-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="1e852-118">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1e852-118">Click Functions.</span></span>
5. <span data-ttu-id="1e852-119">Noklikšķiniet uz Sadalīt pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="1e852-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="1e852-120">Laukā Uz pamatlīdzekli, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1e852-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="1e852-121">Laukā Uz grāmatu, noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1e852-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1e852-122">Ievadiet datumu laukā Transakcijas datums.</span><span class="sxs-lookup"><span data-stu-id="1e852-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="1e852-123">Ievadiet skaitli laukā Procenti.</span><span class="sxs-lookup"><span data-stu-id="1e852-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="1e852-124">Laukā Žurnāla nosaukums, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1e852-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="1e852-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1e852-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="1e852-126">Žurnāla transakcijas grāmatošana</span><span class="sxs-lookup"><span data-stu-id="1e852-126">Post the journal transaction</span></span>
1. <span data-ttu-id="1e852-127">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="1e852-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="1e852-128">Sarakstā atlasiet žurnālu, kas izveidots sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="1e852-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="1e852-129">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="1e852-129">Click Lines.</span></span>
    * <span data-ttu-id="1e852-130">Pārbaudiet izveidotās žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="1e852-130">Verify the journal lines created.</span></span>  <span data-ttu-id="1e852-131">Oriģinālajam aktīvam izveidota Iegādes pielāgošanas transakcija, lai samazinātu vērtību par sadalīšanas procesā norādīto procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="1e852-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="1e852-132">Jaunajam aktīvam tiek izveidota Iegādes transakcija par tādu pašu summu.</span><span class="sxs-lookup"><span data-stu-id="1e852-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="1e852-133">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="1e852-133">Click Post.</span></span>


