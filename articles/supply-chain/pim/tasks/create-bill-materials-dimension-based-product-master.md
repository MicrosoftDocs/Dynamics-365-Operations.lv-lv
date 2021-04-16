---
title: Materiālu komplekta izveide uz dimensiju balstītas preces šablonam
description: Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820086"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="66fb0-103">Materiālu komplekta izveide uz dimensiju balstītas preces šablonam</span><span class="sxs-lookup"><span data-stu-id="66fb0-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66fb0-104">Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā.</span><span class="sxs-lookup"><span data-stu-id="66fb0-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="66fb0-105">Ar pirmajiem 4 ierakstiem tiek iestatīti dati, kas ir nepieciešami šīs procedūras izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="66fb0-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="66fb0-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="66fb0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="66fb0-107">Šo uzdevumu parasti veic preču noformētājs.</span><span class="sxs-lookup"><span data-stu-id="66fb0-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="66fb0-108">Atlasīt preci</span><span class="sxs-lookup"><span data-stu-id="66fb0-108">Select the product</span></span>
1. <span data-ttu-id="66fb0-109">Noklikšķiniet uz Izlaisto preču uzturēšana.</span><span class="sxs-lookup"><span data-stu-id="66fb0-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="66fb0-110">Noklikšķiniet uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="66fb0-110">Click Released products.</span></span>
3. <span data-ttu-id="66fb0-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="66fb0-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="66fb0-112">Atrodiet izlaisto preces šablonu ar dimensijām atbilstošas konfigurācijas tehnoloģiju, kuru izveidojāt šīs procedūras pirmajā uzdevumu ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="66fb0-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="66fb0-113">Darbību rūtī noklikšķiniet uz Inženieris.</span><span class="sxs-lookup"><span data-stu-id="66fb0-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="66fb0-114">Noklikšķiniet uz MK versijas.</span><span class="sxs-lookup"><span data-stu-id="66fb0-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="66fb0-115">Izveidot jaunu MK un MK versiju</span><span class="sxs-lookup"><span data-stu-id="66fb0-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="66fb0-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66fb0-116">Click New.</span></span>
2. <span data-ttu-id="66fb0-117">Noklikšķiniet uz MK un MK versija.</span><span class="sxs-lookup"><span data-stu-id="66fb0-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="66fb0-118">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="66fb0-119">Vietas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="66fb0-119">Setting a site</span></span>  
    * <span data-ttu-id="66fb0-120">Šajā procedūrā mēs šim MK neiestatām noteiktu vietu.</span><span class="sxs-lookup"><span data-stu-id="66fb0-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="66fb0-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="66fb0-121">Click OK.</span></span>
5. <span data-ttu-id="66fb0-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66fb0-122">Click New.</span></span>
    * <span data-ttu-id="66fb0-123">Šajā procedūrā mēs MK pievienosim četras rindas.</span><span class="sxs-lookup"><span data-stu-id="66fb0-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="66fb0-124">Divas rindas apzīmē opcijas Cable, un divas rindas apzīmē opcijas Cabinet.</span><span class="sxs-lookup"><span data-stu-id="66fb0-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="66fb0-125">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="66fb0-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="66fb0-126">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="66fb0-127">Atlasiet krājumu kodu A0001, HDMI 6' Cables.</span><span class="sxs-lookup"><span data-stu-id="66fb0-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="66fb0-128">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="66fb0-129">Atlasiet konfigurācijas grupu Cable, kas tika izveidota šīs procedūras 4. ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="66fb0-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="66fb0-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66fb0-130">Click New.</span></span>
    * <span data-ttu-id="66fb0-131">Atlasiet krājumu kodu A0002, HDMI 12' Cables.</span><span class="sxs-lookup"><span data-stu-id="66fb0-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="66fb0-132">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="66fb0-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="66fb0-133">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="66fb0-134">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="66fb0-135">Vēlreiz atlasiet konfigurācijas grupu Cable.</span><span class="sxs-lookup"><span data-stu-id="66fb0-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="66fb0-136">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66fb0-136">Click New.</span></span>
14. <span data-ttu-id="66fb0-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="66fb0-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="66fb0-138">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="66fb0-139">Atlasiet krājumu kodu D0002 Cable.</span><span class="sxs-lookup"><span data-stu-id="66fb0-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="66fb0-140">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="66fb0-141">Šai MK rindai atlasiet konfigurācijas grupu Cabinet.</span><span class="sxs-lookup"><span data-stu-id="66fb0-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="66fb0-142">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66fb0-142">Click New.</span></span>
18. <span data-ttu-id="66fb0-143">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="66fb0-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="66fb0-144">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="66fb0-145">Kā pēdējo MK rindu atlasiet krājumu kodu M0007 StandardCabinet.</span><span class="sxs-lookup"><span data-stu-id="66fb0-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="66fb0-146">Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="66fb0-147">Pēdējai MK rindai atlasiet konfigurācijas grupu Cabinet.</span><span class="sxs-lookup"><span data-stu-id="66fb0-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="66fb0-148">Apstiprināt un aktivizēt</span><span class="sxs-lookup"><span data-stu-id="66fb0-148">Approve and activate</span></span>
1. <span data-ttu-id="66fb0-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="66fb0-149">Close the page.</span></span>
2. <span data-ttu-id="66fb0-150">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="66fb0-150">Click Approve.</span></span>
3. <span data-ttu-id="66fb0-151">Laukā Apstiprināja ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66fb0-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="66fb0-152">Laukā Vai vēlaties arī apstiprināt materiālu komplektu? atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="66fb0-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="66fb0-153">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="66fb0-153">Click OK.</span></span>
6. <span data-ttu-id="66fb0-154">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="66fb0-154">Click Activate.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]