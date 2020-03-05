---
title: POS atļauju grupu izveide
description: Šajā tēmā ir paskaidrots, kā izveidot POS atļauju grupu.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
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
ms.openlocfilehash: e6f9f8f970f336a0cce6bcac78e32a1b7fe0a252
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023284"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="62dc9-103">POS atļauju grupu izveide</span><span class="sxs-lookup"><span data-stu-id="62dc9-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="62dc9-104">Šajā tēmā ir paskaidrots, kā izveidot POS atļauju grupu.</span><span class="sxs-lookup"><span data-stu-id="62dc9-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="62dc9-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="62dc9-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="62dc9-106">Šis uzdevums ir paredzēts tirdzniecības operāciju pārvaldnieka lomai.</span><span class="sxs-lookup"><span data-stu-id="62dc9-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="62dc9-107">Navigācijas rūtī ejiet uz **Moduļi > Mazumtirdzniecība un tirdzniecība > Darbinieki > Atļauju grupas**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="62dc9-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-108">Select **New**.</span></span>
3. <span data-ttu-id="62dc9-109">Laukā **POS atļauju grupas ID** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="62dc9-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="62dc9-110">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="62dc9-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="62dc9-111">Atlasiet **Jā** laukā **Skatīt pulksteņa ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="62dc9-112">Tagad var iespējot vai atspējot dažādas atļaujas POS atļauju grupā.</span><span class="sxs-lookup"><span data-stu-id="62dc9-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="62dc9-113">Daļai atļauju var iestatīt vērtību, kas tiks izmantota, lai novērtētu, vaI POS lietotājs var veikt darbību.</span><span class="sxs-lookup"><span data-stu-id="62dc9-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="62dc9-114">Šajā uzdevuma ceļvedī iespējosit dažas atļaujas, ko var piešķirt kasierim.</span><span class="sxs-lookup"><span data-stu-id="62dc9-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="62dc9-115">Atlasiet **Jā** laukā **Atļaut izveidot pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="62dc9-116">Atlasiet **Jā** laukā **Atļaut rediģēt pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="62dc9-117">Atlasiet **Jā** laukā **Atļaut izgūt pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="62dc9-118">Atlasiet **Jā** laukā **Atļaut paroles maiņu**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="62dc9-119">Atlasiet **Jā** laukā **Atļaut aklo aizvēršanu**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="62dc9-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-120">Select **Save**.</span></span> <span data-ttu-id="62dc9-121">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas tirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="62dc9-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="62dc9-122">Navigācijas rūtī ejiet uz **Moduļi > Cilvēkresursi > Amati > Amati**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="62dc9-123">Tagad POS atļauju grupu piešķirsim darbam.</span><span class="sxs-lookup"><span data-stu-id="62dc9-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="62dc9-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="62dc9-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="62dc9-125">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-125">Select **Edit**.</span></span>
15. <span data-ttu-id="62dc9-126">Izvērsiet sadaļu **Amata klasifikācija**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="62dc9-127">Laukā POS atļauju grupa ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="62dc9-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="62dc9-128">Šīs POS atļauju grupas iestatījumus izmantos visi darbinieki ar šim darbam atbilstošu amatu, ja vien darbinieku POS atļaujas netika ignorētas to amata līmenī.</span><span class="sxs-lookup"><span data-stu-id="62dc9-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="62dc9-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="62dc9-129">Select **Save**.</span></span> <span data-ttu-id="62dc9-130">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas kanāliem.</span><span class="sxs-lookup"><span data-stu-id="62dc9-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  
