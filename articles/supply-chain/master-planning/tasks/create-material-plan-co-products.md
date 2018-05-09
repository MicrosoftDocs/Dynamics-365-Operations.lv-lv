--- 
title: "Materiālu plāna izveide līdzproduktiem"
description: "Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f3a411e8fc773957b5ce3f24749242d9d0c6ffd0
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f1cd5-103">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="f1cd5-103">Create a material plan for co-products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1cd5-104">Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="f1cd5-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="f1cd5-106">Vajadzības izveide līdzproduktam</span><span class="sxs-lookup"><span data-stu-id="f1cd5-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="f1cd5-107">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="f1cd5-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="f1cd5-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-109">Click New.</span></span>
4. <span data-ttu-id="f1cd5-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-110">Click Sales order.</span></span>
5. <span data-ttu-id="f1cd5-111">Laukā Debitora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="f1cd5-112">Piemērs: US-001</span><span class="sxs-lookup"><span data-stu-id="f1cd5-112">Example: US-001</span></span>  
6. <span data-ttu-id="f1cd5-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-113">Click OK.</span></span>
7. <span data-ttu-id="f1cd5-114">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f1cd5-115">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="f1cd5-115">Example: P6003</span></span>  
8. <span data-ttu-id="f1cd5-116">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f1cd5-117">Piemērs: 50000</span><span class="sxs-lookup"><span data-stu-id="f1cd5-117">Example: 50000</span></span>  
9. <span data-ttu-id="f1cd5-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f1cd5-119">Materiālu plāna izveide līdzproduktiem</span><span class="sxs-lookup"><span data-stu-id="f1cd5-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="f1cd5-120">Noklikšķiniet uz Vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-120">Click Master planning.</span></span>
2. <span data-ttu-id="f1cd5-121">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f1cd5-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f1cd5-123">Piemērs: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="f1cd5-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="f1cd5-124">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-124">Click Run.</span></span>
5. <span data-ttu-id="f1cd5-125">Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="f1cd5-126">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-126">Click Filter.</span></span>
7. <span data-ttu-id="f1cd5-127">Sarakstā atlasiet rindu Lauks = Krājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="f1cd5-128">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f1cd5-129">Piemērs: P6003</span><span class="sxs-lookup"><span data-stu-id="f1cd5-129">Example: P6003</span></span>  
9. <span data-ttu-id="f1cd5-130">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-130">Click OK.</span></span>
10. <span data-ttu-id="f1cd5-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-131">Click OK.</span></span>
11. <span data-ttu-id="f1cd5-132">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-132">Click Planned orders.</span></span>
12. <span data-ttu-id="f1cd5-133">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f1cd5-134">Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".</span><span class="sxs-lookup"><span data-stu-id="f1cd5-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="f1cd5-135">Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="f1cd5-136">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f1cd5-137">Atlasiet jebkuru filtra atgriezto rindu.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="f1cd5-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="f1cd5-139">Izvērsiet vai sakļaujiet sadaļu Piesaiste.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="f1cd5-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f1cd5-141">Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="f1cd5-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f1cd5-142">Close the page.</span></span>


