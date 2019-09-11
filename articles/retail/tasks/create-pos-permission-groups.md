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
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914817"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="5636f-103">POS atļauju grupu izveide</span><span class="sxs-lookup"><span data-stu-id="5636f-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5636f-104">Šajā tēmā ir paskaidrots, kā izveidot POS atļauju grupu.</span><span class="sxs-lookup"><span data-stu-id="5636f-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="5636f-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="5636f-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5636f-106">Šis uzdevums ir paredzēts mazumtirdzniecības operāciju pārvaldnieka lomai.</span><span class="sxs-lookup"><span data-stu-id="5636f-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="5636f-107">Navigācijas rūtī ejiet uz **Moduļi > Mazumtirdzniecība > Darbinieki > Atļauju grupas**.</span><span class="sxs-lookup"><span data-stu-id="5636f-107">In the navigation pane, go to **Modules > Retail > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="5636f-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5636f-108">Select **New**.</span></span>
3. <span data-ttu-id="5636f-109">Laukā **POS atļauju grupas ID** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5636f-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="5636f-110">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5636f-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5636f-111">Atlasiet **Jā** laukā **Skatīt pulksteņa ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="5636f-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="5636f-112">Tagad var iespējot vai atspējot dažādas atļaujas POS atļauju grupā.</span><span class="sxs-lookup"><span data-stu-id="5636f-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="5636f-113">Daļai atļauju var iestatīt vērtību, kas tiks izmantota, lai novērtētu, vaI POS lietotājs var veikt darbību.</span><span class="sxs-lookup"><span data-stu-id="5636f-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="5636f-114">Šajā uzdevuma ceļvedī iespējosit dažas atļaujas, ko var piešķirt kasierim.</span><span class="sxs-lookup"><span data-stu-id="5636f-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="5636f-115">Atlasiet **Jā** laukā **Atļaut izveidot pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="5636f-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="5636f-116">Atlasiet **Jā** laukā **Atļaut rediģēt pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="5636f-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="5636f-117">Atlasiet **Jā** laukā **Atļaut izgūt pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="5636f-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="5636f-118">Atlasiet **Jā** laukā **Atļaut paroles maiņu**.</span><span class="sxs-lookup"><span data-stu-id="5636f-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="5636f-119">Atlasiet **Jā** laukā **Atļaut aklo aizvēršanu**.</span><span class="sxs-lookup"><span data-stu-id="5636f-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="5636f-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5636f-120">Select **Save**.</span></span> <span data-ttu-id="5636f-121">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="5636f-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span> 
12. <span data-ttu-id="5636f-122">Navigācijas rūtī ejiet uz **Moduļi > Cilvēkresursi > Amati > Amati**.</span><span class="sxs-lookup"><span data-stu-id="5636f-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="5636f-123">Tagad POS atļauju grupu piešķirsim darbam.</span><span class="sxs-lookup"><span data-stu-id="5636f-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="5636f-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5636f-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5636f-125">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5636f-125">Select **Edit**.</span></span>
15. <span data-ttu-id="5636f-126">Izvērsiet sadaļu **Amata klasifikācija**.</span><span class="sxs-lookup"><span data-stu-id="5636f-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="5636f-127">Laukā POS atļauju grupa ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5636f-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="5636f-128">Šīs POS atļauju grupas iestatījumus izmantos visi darbinieki ar šim darbam atbilstošu amatu, ja vien darbinieku POS atļaujas netika ignorētas to amata līmenī.</span><span class="sxs-lookup"><span data-stu-id="5636f-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="5636f-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5636f-129">Select **Save**.</span></span> <span data-ttu-id="5636f-130">Pēc izmaiņu saglabāšanas ir jāpalaiž darbinieku sadales grafiks, lai izmaiņas tiktu lietotas mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="5636f-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

