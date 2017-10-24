--- 
title: " POS atļauju grupu izveide"
description: "Šajā procedūrā ir paskaidrots, kā izveidot POS atļauju grupu."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e924dc59c3e4cb9b6979014852512453dd3d70db
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="41b2f-103"> POS atļauju grupu izveide</span><span class="sxs-lookup"><span data-stu-id="41b2f-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="41b2f-104">Šajā procedūrā ir paskaidrots, kā izveidot POS atļauju grupu.</span><span class="sxs-lookup"><span data-stu-id="41b2f-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="41b2f-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="41b2f-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="41b2f-106">Šis uzdevums ir paredzēts mazumtirdzniecības operāciju pārvaldnieka lomai.</span><span class="sxs-lookup"><span data-stu-id="41b2f-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="41b2f-107">Dodieties uz cilni Atļauju grupas.</span><span class="sxs-lookup"><span data-stu-id="41b2f-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="41b2f-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="41b2f-108">Click New.</span></span>
3. <span data-ttu-id="41b2f-109">Laukā POS atļauju grupas ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="41b2f-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="41b2f-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="41b2f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="41b2f-111">Laukā Skatīt darba laika uzskaites ierakstus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="41b2f-112">Tagad var iespējot vai atspējot dažādas atļaujas POS atļauju grupā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="41b2f-113">Daļai atļauju var iestatīt vērtību, kas tiks izmantota, lai novērtētu, vaI POS lietotājs var veikt darbību.</span><span class="sxs-lookup"><span data-stu-id="41b2f-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="41b2f-114">Šajā uzdevuma ceļvedī iespējosit dažas atļaujas, ko var piešķirt kasierim.</span><span class="sxs-lookup"><span data-stu-id="41b2f-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="41b2f-115">Laukā Ļaut izveidot pasūtījumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="41b2f-116">Laukā Ļaut rediģēt pasūtījumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="41b2f-117">Laukā Ļaut izgūt pasūtījumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="41b2f-118">Laukā Atļaut paroles maiņu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="41b2f-119">Laukā Atļaut neskaidri slēgt maiņu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="41b2f-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="41b2f-120">Click Save.</span></span>
    * <span data-ttu-id="41b2f-121">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="41b2f-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="41b2f-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="41b2f-122">Close the page.</span></span>
13. <span data-ttu-id="41b2f-123">Dodieties uz cilni Darbi.</span><span class="sxs-lookup"><span data-stu-id="41b2f-123">Go to Jobs.</span></span>
    * <span data-ttu-id="41b2f-124">Tagad POS atļauju grupu piešķirsim darbam.</span><span class="sxs-lookup"><span data-stu-id="41b2f-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="41b2f-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="41b2f-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="41b2f-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="41b2f-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="41b2f-127">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="41b2f-127">Click Edit.</span></span>
17. <span data-ttu-id="41b2f-128">Izvērsiet sadaļu Darbu klasifikācija.</span><span class="sxs-lookup"><span data-stu-id="41b2f-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="41b2f-129">Laukā POS atļauju grupa ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="41b2f-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="41b2f-130">Šīs POS atļauju grupas iestatījumus izmantos visi darbinieki ar šim darbam atbilstošu amatu, ja vien darbinieku POS atļaujas netika ignorētas to amata līmenī.</span><span class="sxs-lookup"><span data-stu-id="41b2f-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="41b2f-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="41b2f-131">Click Save.</span></span>
    * <span data-ttu-id="41b2f-132">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="41b2f-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


