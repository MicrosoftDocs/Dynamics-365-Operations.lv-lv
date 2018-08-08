---
title: "Pakalpojumu objektu saistības"
description: "Ir iespējams izveidot pakalpojuma objekta relāciju starp pakalpojuma objektu un pakalpojumu līgumu vai pakalpojuma pasūtījumu."
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 03047b3eccf3c90d4cf7426ddaec83f10dbea1b0
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="96c80-103">Pakalpojumu objektu saistības</span><span class="sxs-lookup"><span data-stu-id="96c80-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96c80-104">Ir iespējams izveidot pakalpojuma objekta relāciju starp pakalpojuma objektu un pakalpojumu līgumu vai pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="96c80-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="96c80-105">Kad tiek izveidota relācija, pakalpojumu līgumam vai pakalpojuma pasūtījumam ir jāpievieno pakalpojuma objekts.</span><span class="sxs-lookup"><span data-stu-id="96c80-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="96c80-106">Pēc relācijas izveidošanas jebkurai pakalpojumu līguma vai pakalpojuma pasūtījuma rindai var pievienot pakalpojuma objektu.</span><span class="sxs-lookup"><span data-stu-id="96c80-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="96c80-107">Veidnes MK</span><span class="sxs-lookup"><span data-stu-id="96c80-107">Template BOMs</span></span>

<span data-ttu-id="96c80-108">Objektu relācijai ir arī iespējams noteikt veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="96c80-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="96c80-109">Veidnes MK ir materiālu komplekts objektam, kuram tiem veikts pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="96c80-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="96c80-110">Ja apkopes laikā tiek nomainīta kāda pakalpojumu objekta sastāvdaļa, šo nomaiņu iespējams reģistrēt pakalpojuma MK, izmantojot veidlapu Pakalpojumu objekti.</span><span class="sxs-lookup"><span data-stu-id="96c80-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="96c80-111">Paraugs</span><span class="sxs-lookup"><span data-stu-id="96c80-111">Example</span></span>

<span data-ttu-id="96c80-112">Tiek izveidots pakalpojumu līgums divu celtņu apkalpošanai klienta būvlaukumā.</span><span class="sxs-lookup"><span data-stu-id="96c80-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="96c80-113">Pakalpojumu līguma identifikators ir ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="96c80-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="96c80-114">Veidlapā Pakalpojumu objekti celtņi tikuši uzstādīti kā objekti EL-S/1000 un EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="96c80-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="96c80-115">Pakalpojuma objekti (EL-S/1000 un EL-L/1000) tiek pievienoti pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="96c80-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="96c80-116">Lietotājs vēlas reģistrēt pakalpojuma objekta izmaiņas MK, jo tikusi nomainīta kāda objekta sastāvdaļa, tad pakalpojuma objekta relācijai tiek pievienots pakalpojuma MK kā aprakstīts sekojošajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="96c80-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="96c80-117">Pakalpojumu objekts</span><span class="sxs-lookup"><span data-stu-id="96c80-117">Service object</span></span> | <span data-ttu-id="96c80-118">Relācija – Pakalpojumu līgums</span><span class="sxs-lookup"><span data-stu-id="96c80-118">Relation – Service agreement</span></span> | <span data-ttu-id="96c80-119">Pakalpojumu MK</span><span class="sxs-lookup"><span data-stu-id="96c80-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="96c80-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-120">EL-S/1000</span></span>      | <span data-ttu-id="96c80-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="96c80-121">ID SAL-001</span></span>                   | <span data-ttu-id="96c80-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="96c80-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-123">EL-L/1000</span></span>      | <span data-ttu-id="96c80-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="96c80-124">ID SAL-001</span></span>                   | <span data-ttu-id="96c80-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="96c80-126">Pateicoties tam, ka līgumam ir pakalpojumu objekts, tagad var izveidot pakalpojumu līguma rindas ar šiem objektiem kā parādīts tālāk esošajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="96c80-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="96c80-127">Darbības veids</span><span class="sxs-lookup"><span data-stu-id="96c80-127">Transaction type</span></span> | <span data-ttu-id="96c80-128">Kategorija</span><span class="sxs-lookup"><span data-stu-id="96c80-128">Category</span></span>           | <span data-ttu-id="96c80-129">Pakalpojumu objekts</span><span class="sxs-lookup"><span data-stu-id="96c80-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="96c80-130">Stunda</span><span class="sxs-lookup"><span data-stu-id="96c80-130">Hour</span></span>             | <span data-ttu-id="96c80-131">Pārbaude</span><span class="sxs-lookup"><span data-stu-id="96c80-131">Inspection</span></span>         | <span data-ttu-id="96c80-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-132">EL-S/1000</span></span>      |
| <span data-ttu-id="96c80-133">Stunda</span><span class="sxs-lookup"><span data-stu-id="96c80-133">Hour</span></span>             | <span data-ttu-id="96c80-134">Ātrumkārbas tīrīšana</span><span class="sxs-lookup"><span data-stu-id="96c80-134">Gear box cleaning</span></span>  | <span data-ttu-id="96c80-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-135">EL-S/1000</span></span>      |
| <span data-ttu-id="96c80-136">Krājums</span><span class="sxs-lookup"><span data-stu-id="96c80-136">Item</span></span>             | <span data-ttu-id="96c80-137">Tīrīšanas materiāli</span><span class="sxs-lookup"><span data-stu-id="96c80-137">Cleaning materials</span></span> | <span data-ttu-id="96c80-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-138">EL-S/1000</span></span>      |
| <span data-ttu-id="96c80-139">Stunda</span><span class="sxs-lookup"><span data-stu-id="96c80-139">Hour</span></span>             | <span data-ttu-id="96c80-140">Pārbaude</span><span class="sxs-lookup"><span data-stu-id="96c80-140">Inspection</span></span>         | <span data-ttu-id="96c80-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-141">EL-L/1000</span></span>      |
| <span data-ttu-id="96c80-142">Stunda</span><span class="sxs-lookup"><span data-stu-id="96c80-142">Hour</span></span>             | <span data-ttu-id="96c80-143">Ātrumkārbas tīrīšana</span><span class="sxs-lookup"><span data-stu-id="96c80-143">Gearbox cleaning</span></span>   | <span data-ttu-id="96c80-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-144">EL-L/1000</span></span>      |
| <span data-ttu-id="96c80-145">Krājums</span><span class="sxs-lookup"><span data-stu-id="96c80-145">Item</span></span>             | <span data-ttu-id="96c80-146">Tīrīšanas materiāli</span><span class="sxs-lookup"><span data-stu-id="96c80-146">Cleaning materials</span></span> | <span data-ttu-id="96c80-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="96c80-147">EL-L/1000</span></span>      |

<span data-ttu-id="96c80-148">Apkopes veikšanas laikā tikusi nomainīta celtņa EL-S/1000 ātrumkārba.</span><span class="sxs-lookup"><span data-stu-id="96c80-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="96c80-149">Lai nomainītu objekta sastāvdaļu, ir iespējams piekļūt BOM Designer izmantojot pakalpojumu objekta relāciju, kura tika iestatīta pašreizējam pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="96c80-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="96c80-150">Piekļūstiet BOM Designer ar pakalpojumu objektu relācijas palīdzību.</span><span class="sxs-lookup"><span data-stu-id="96c80-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="96c80-151">Pakalpojumu līgumi</span><span class="sxs-lookup"><span data-stu-id="96c80-151">Service agreements</span></span>
2. <span data-ttu-id="96c80-152">Veiciet dubultklikšķi uz pakalpojumu līguma, vai noklikšķiniet uz Pakalpojumu līgums, lai izveidotu pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="96c80-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="96c80-153">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="96c80-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="96c80-154">Lai pakalpojumu līgumam pievienotu veidnes MK, nokliksķiniet uz Pakalpojumu objekti.</span><span class="sxs-lookup"><span data-stu-id="96c80-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="96c80-155">Veidlapā Pakalpojumu objekti noklikšķiniet uz Noformētājs, lai atvērtu veidotāja veidlapu un modificētu veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="96c80-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="96c80-156">Automātiski izveidoti pakalpojumu pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="96c80-156">Automatically created service orders</span></span>

<span data-ttu-id="96c80-157">Ja pakalpojumu līgumam tiek automātiski izveidoti pakalpojuma pasūtījumi, tad pakalpojumu objektu relācijas līgumā tiek izveidotas arī pakalpojumu pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="96c80-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


