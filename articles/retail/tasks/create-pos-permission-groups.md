---
title: " POS atļauju grupu izveide"
description: Šajā procedūrā ir paskaidrots, kā izveidot POS atļauju grupu.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b30c9a1d7fe4598695423ba700ebc88a794a49c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "354464"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="9cfb1-103"> POS atļauju grupu izveide</span><span class="sxs-lookup"><span data-stu-id="9cfb1-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9cfb1-104">Šajā procedūrā ir paskaidrots, kā izveidot POS atļauju grupu.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="9cfb1-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="9cfb1-106">Šis uzdevums ir paredzēts mazumtirdzniecības operāciju pārvaldnieka lomai.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="9cfb1-107">Dodieties uz cilni Atļauju grupas.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="9cfb1-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-108">Click New.</span></span>
3. <span data-ttu-id="9cfb1-109">Laukā POS atļauju grupas ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="9cfb1-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9cfb1-111">Laukā Skatīt darba laika uzskaites ierakstus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="9cfb1-112">Tagad var iespējot vai atspējot dažādas atļaujas POS atļauju grupā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="9cfb1-113">Daļai atļauju var iestatīt vērtību, kas tiks izmantota, lai novērtētu, vaI POS lietotājs var veikt darbību.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="9cfb1-114">Šajā uzdevuma ceļvedī iespējosit dažas atļaujas, ko var piešķirt kasierim.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="9cfb1-115">Laukā Ļaut izveidot pasūtījumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="9cfb1-116">Laukā Ļaut rediģēt pasūtījumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="9cfb1-117">Laukā Ļaut izgūt pasūtījumu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="9cfb1-118">Laukā Atļaut paroles maiņu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="9cfb1-119">Laukā Atļaut neskaidri slēgt maiņu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="9cfb1-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-120">Click Save.</span></span>
    * <span data-ttu-id="9cfb1-121">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="9cfb1-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-122">Close the page.</span></span>
13. <span data-ttu-id="9cfb1-123">Dodieties uz cilni Darbi.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-123">Go to Jobs.</span></span>
    * <span data-ttu-id="9cfb1-124">Tagad POS atļauju grupu piešķirsim darbam.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="9cfb1-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9cfb1-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="9cfb1-127">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-127">Click Edit.</span></span>
17. <span data-ttu-id="9cfb1-128">Izvērsiet sadaļu Darbu klasifikācija.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="9cfb1-129">Laukā POS atļauju grupa ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="9cfb1-130">Šīs POS atļauju grupas iestatījumus izmantos visi darbinieki ar šim darbam atbilstošu amatu, ja vien darbinieku POS atļaujas netika ignorētas to amata līmenī.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="9cfb1-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-131">Click Save.</span></span>
    * <span data-ttu-id="9cfb1-132">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="9cfb1-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

