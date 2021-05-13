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
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920709"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="36baa-103">Materiālu komplekta izveide uz dimensiju balstītas preces šablonam</span><span class="sxs-lookup"><span data-stu-id="36baa-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36baa-104">Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā.</span><span class="sxs-lookup"><span data-stu-id="36baa-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="36baa-105">Ar pirmajiem 4 ierakstiem tiek iestatīti dati, kas ir nepieciešami šīs procedūras izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="36baa-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="36baa-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="36baa-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="36baa-107">Šo uzdevumu parasti veic preču noformētājs.</span><span class="sxs-lookup"><span data-stu-id="36baa-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="36baa-108">Atlasīt preci</span><span class="sxs-lookup"><span data-stu-id="36baa-108">Select the product</span></span>

1. <span data-ttu-id="36baa-109">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="36baa-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="36baa-110">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="36baa-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="36baa-111">Atrodiet izlaisto preces šablonu ar dimensijām atbilstošas konfigurācijas tehnoloģiju, kuru izveidojāt šīs procedūras pirmajā uzdevumu ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="36baa-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="36baa-112">Darbību rūtī atlasiet **Inženieris**.</span><span class="sxs-lookup"><span data-stu-id="36baa-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="36baa-113">Atlasīt **MK versijas**.</span><span class="sxs-lookup"><span data-stu-id="36baa-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="36baa-114">Izveidot jaunu MK un MK versiju</span><span class="sxs-lookup"><span data-stu-id="36baa-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="36baa-115">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="36baa-115">Select **New**.</span></span>
1. <span data-ttu-id="36baa-116">Atlasiet **MK un MK versiju**.</span><span class="sxs-lookup"><span data-stu-id="36baa-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="36baa-117">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="36baa-118">Vietas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="36baa-118">Setting a site</span></span>  
    * <span data-ttu-id="36baa-119">Šajā procedūrā mēs šim MK neiestatām noteiktu vietu.</span><span class="sxs-lookup"><span data-stu-id="36baa-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="36baa-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="36baa-120">Select **OK**.</span></span>
1. <span data-ttu-id="36baa-121">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="36baa-121">Select **New**.</span></span>
    * <span data-ttu-id="36baa-122">Šajā procedūrā mēs MK pievienosim četras rindas.</span><span class="sxs-lookup"><span data-stu-id="36baa-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="36baa-123">Divas rindas apzīmē opcijas Cable, un divas rindas apzīmē opcijas Cabinet.</span><span class="sxs-lookup"><span data-stu-id="36baa-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="36baa-124">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="36baa-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="36baa-125">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="36baa-126">Atlasiet krājumu kodu A0001, HDMI 6' Cables.</span><span class="sxs-lookup"><span data-stu-id="36baa-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="36baa-127">Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="36baa-128">Atlasiet kabeļa konfigurācijas grupu, kas tika izveidota šīs procedūras 4. ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="36baa-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="36baa-129">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="36baa-129">Select **New**.</span></span>
    * <span data-ttu-id="36baa-130">Atlasiet krājumu kodu A0002, HDMI 12' Cables.</span><span class="sxs-lookup"><span data-stu-id="36baa-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="36baa-131">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="36baa-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="36baa-132">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="36baa-133">Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="36baa-134">Vēlreiz atlasiet kabeļa konfigurācijas grupu.</span><span class="sxs-lookup"><span data-stu-id="36baa-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="36baa-135">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="36baa-135">Select **New**.</span></span>
1. <span data-ttu-id="36baa-136">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="36baa-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="36baa-137">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="36baa-138">Atlasiet krājumu kodu D0002 Cable.</span><span class="sxs-lookup"><span data-stu-id="36baa-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="36baa-139">Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="36baa-140">Šai MK rindai atlasiet kabineta konfigurācijas grupu.</span><span class="sxs-lookup"><span data-stu-id="36baa-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="36baa-141">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="36baa-141">Select **New**.</span></span>
1. <span data-ttu-id="36baa-142">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="36baa-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="36baa-143">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="36baa-144">Kā pēdējo MK rindu atlasiet krājumu kodu M0007 StandardCabinet.</span><span class="sxs-lookup"><span data-stu-id="36baa-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="36baa-145">Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="36baa-146">Pēdējai MK rindai atlasiet kabineta konfigurācijas grupu.</span><span class="sxs-lookup"><span data-stu-id="36baa-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="36baa-147">Apstiprināt un aktivizēt</span><span class="sxs-lookup"><span data-stu-id="36baa-147">Approve and activate</span></span>

1. <span data-ttu-id="36baa-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="36baa-148">Close the page.</span></span>
1. <span data-ttu-id="36baa-149">Atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="36baa-149">Select **Approve**.</span></span>
1. <span data-ttu-id="36baa-150">Laukā **Apstiprināt pēc** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="36baa-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="36baa-151">Laukā **Vai vēlaties arī apstiprināt materiālu komplektu?** atlasiet *Jā*.</span><span class="sxs-lookup"><span data-stu-id="36baa-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="36baa-152">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="36baa-152">Select **OK**.</span></span>
1. <span data-ttu-id="36baa-153">Atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="36baa-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]