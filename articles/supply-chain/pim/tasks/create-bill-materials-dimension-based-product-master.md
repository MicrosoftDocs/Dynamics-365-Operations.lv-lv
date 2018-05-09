--- 
title: "Materiālu komplekta izveide uz dimensiju balstītas preces šablonam"
description: "Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
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
ms.openlocfilehash: 3a3aeae7e8012282ec9e57314a128a60c1a80a68
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="456b4-103">Materiālu komplekta izveide uz dimensiju balstītas preces šablonam</span><span class="sxs-lookup"><span data-stu-id="456b4-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="456b4-104">Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā.</span><span class="sxs-lookup"><span data-stu-id="456b4-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="456b4-105">Ar pirmajiem 4 ierakstiem tiek iestatīti dati, kas ir nepieciešami šīs procedūras izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="456b4-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="456b4-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="456b4-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="456b4-107">Šo uzdevumu parasti veic preču noformētājs.</span><span class="sxs-lookup"><span data-stu-id="456b4-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="456b4-108">Atlasīt preci</span><span class="sxs-lookup"><span data-stu-id="456b4-108">Select the product</span></span>
1. <span data-ttu-id="456b4-109">Noklikšķiniet uz Izlaisto preču uzturēšana.</span><span class="sxs-lookup"><span data-stu-id="456b4-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="456b4-110">Noklikšķiniet uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="456b4-110">Click Released products.</span></span>
3. <span data-ttu-id="456b4-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="456b4-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="456b4-112">Atrodiet izlaisto preces šablonu ar dimensijām atbilstošas konfigurācijas tehnoloģiju, kuru izveidojāt šīs procedūras pirmajā uzdevumu ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="456b4-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="456b4-113">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="456b4-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="456b4-114">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="456b4-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="456b4-115">Izveidot jaunu MK un MK versiju</span><span class="sxs-lookup"><span data-stu-id="456b4-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="456b4-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="456b4-116">Click New.</span></span>
2. <span data-ttu-id="456b4-117">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="456b4-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="456b4-118">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="456b4-119">Vietas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="456b4-119">Setting a site</span></span>  
    * <span data-ttu-id="456b4-120">Šajā procedūrā mēs šim MK neiestatām noteiktu vietu.</span><span class="sxs-lookup"><span data-stu-id="456b4-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="456b4-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="456b4-121">Click OK.</span></span>
5. <span data-ttu-id="456b4-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="456b4-122">Click New.</span></span>
    * <span data-ttu-id="456b4-123">Šajā procedūrā mēs MK pievienosim četras rindas.</span><span class="sxs-lookup"><span data-stu-id="456b4-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="456b4-124">Divas rindas apzīmē opcijas Cable, un divas rindas apzīmē opcijas Cabinet.</span><span class="sxs-lookup"><span data-stu-id="456b4-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="456b4-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="456b4-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="456b4-126">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="456b4-127">Atlasiet krājumu kodu A0001, HDMI 6' Cables.</span><span class="sxs-lookup"><span data-stu-id="456b4-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="456b4-128">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="456b4-129">Atlasiet konfigurācijas grupu Cable, kas tika izveidota šīs procedūras 4. ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="456b4-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="456b4-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="456b4-130">Click New.</span></span>
    * <span data-ttu-id="456b4-131">Atlasiet krājumu kodu A0002, HDMI 12' Cables.</span><span class="sxs-lookup"><span data-stu-id="456b4-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="456b4-132">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="456b4-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="456b4-133">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="456b4-134">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="456b4-135">Vēlreiz atlasiet konfigurācijas grupu Cable.</span><span class="sxs-lookup"><span data-stu-id="456b4-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="456b4-136">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="456b4-136">Click New.</span></span>
14. <span data-ttu-id="456b4-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="456b4-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="456b4-138">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="456b4-139">Atlasiet krājumu kodu D0002 Cable.</span><span class="sxs-lookup"><span data-stu-id="456b4-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="456b4-140">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="456b4-141">Šai MK rindai atlasiet konfigurācijas grupu Cabinet.</span><span class="sxs-lookup"><span data-stu-id="456b4-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="456b4-142">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="456b4-142">Click New.</span></span>
18. <span data-ttu-id="456b4-143">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="456b4-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="456b4-144">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="456b4-145">Kā pēdējo MK rindu atlasiet krājumu kodu M0007 StandardCabinet.</span><span class="sxs-lookup"><span data-stu-id="456b4-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="456b4-146">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="456b4-147">Pēdējai MK rindai atlasiet konfigurācijas grupu Cabinet.</span><span class="sxs-lookup"><span data-stu-id="456b4-147">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="456b4-148">Apstiprināt un aktivizēt</span><span class="sxs-lookup"><span data-stu-id="456b4-148">Approve and activate</span></span>
1. <span data-ttu-id="456b4-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="456b4-149">Close the page.</span></span>
2. <span data-ttu-id="456b4-150">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="456b4-150">Click Approve.</span></span>
3. <span data-ttu-id="456b4-151">Laukā Apstiprināja ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="456b4-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="456b4-152">Laukā Vai vēlaties arī apstiprināt materiālu komplektu? atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="456b4-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="456b4-153">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="456b4-153">Click OK.</span></span>
6. <span data-ttu-id="456b4-154">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="456b4-154">Click Activate.</span></span>


