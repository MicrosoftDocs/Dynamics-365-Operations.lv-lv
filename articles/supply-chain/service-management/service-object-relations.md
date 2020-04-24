---
title: Pakalpojumu objektu saistības
description: Ir iespējams izveidot pakalpojuma objekta relāciju starp pakalpojuma objektu un pakalpojumu līgumu vai pakalpojuma pasūtījumu.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c196a070d1e18b2cc14c54eda0fe0aad5346d93
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215129"
---
# <a name="service-object-relations"></a><span data-ttu-id="d28c9-103">Pakalpojumu objektu saistības</span><span class="sxs-lookup"><span data-stu-id="d28c9-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d28c9-104">Ir iespējams izveidot pakalpojuma objekta relāciju starp pakalpojuma objektu un pakalpojumu līgumu vai pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d28c9-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="d28c9-105">Kad tiek izveidota relācija, pakalpojumu līgumam vai pakalpojuma pasūtījumam ir jāpievieno pakalpojuma objekts.</span><span class="sxs-lookup"><span data-stu-id="d28c9-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="d28c9-106">Pēc relācijas izveidošanas jebkurai pakalpojumu līguma vai pakalpojuma pasūtījuma rindai var pievienot pakalpojuma objektu.</span><span class="sxs-lookup"><span data-stu-id="d28c9-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="d28c9-107">Veidnes MK</span><span class="sxs-lookup"><span data-stu-id="d28c9-107">Template BOMs</span></span>

<span data-ttu-id="d28c9-108">Objektu relācijai ir arī iespējams noteikt veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="d28c9-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="d28c9-109">Veidnes MK ir materiālu komplekts objektam, kuram tiem veikts pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="d28c9-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="d28c9-110">Ja apkopes laikā tiek nomainīta kāda pakalpojumu objekta sastāvdaļa, šo nomaiņu iespējams reģistrēt pakalpojuma MK, izmantojot veidlapu Pakalpojumu objekti.</span><span class="sxs-lookup"><span data-stu-id="d28c9-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="d28c9-111">Paraugs</span><span class="sxs-lookup"><span data-stu-id="d28c9-111">Example</span></span>

<span data-ttu-id="d28c9-112">Tiek izveidots pakalpojumu līgums divu celtņu apkalpošanai klienta būvlaukumā.</span><span class="sxs-lookup"><span data-stu-id="d28c9-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="d28c9-113">Pakalpojumu līguma identifikators ir ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="d28c9-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="d28c9-114">Veidlapā Pakalpojumu objekti celtņi tikuši uzstādīti kā objekti EL-S/1000 un EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="d28c9-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="d28c9-115">Pakalpojuma objekti (EL-S/1000 un EL-L/1000) tiek pievienoti pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="d28c9-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="d28c9-116">Lietotājs vēlas reģistrēt pakalpojuma objekta izmaiņas MK, jo tikusi nomainīta kāda objekta sastāvdaļa, tad pakalpojuma objekta relācijai tiek pievienots pakalpojuma MK kā aprakstīts sekojošajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="d28c9-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="d28c9-117">Pakalpojumu objekts</span><span class="sxs-lookup"><span data-stu-id="d28c9-117">Service object</span></span> | <span data-ttu-id="d28c9-118">Relācija – Pakalpojumu līgums</span><span class="sxs-lookup"><span data-stu-id="d28c9-118">Relation – Service agreement</span></span> | <span data-ttu-id="d28c9-119">Pakalpojumu MK</span><span class="sxs-lookup"><span data-stu-id="d28c9-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="d28c9-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-120">EL-S/1000</span></span>      | <span data-ttu-id="d28c9-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d28c9-121">ID SAL-001</span></span>                   | <span data-ttu-id="d28c9-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="d28c9-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-123">EL-L/1000</span></span>      | <span data-ttu-id="d28c9-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d28c9-124">ID SAL-001</span></span>                   | <span data-ttu-id="d28c9-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="d28c9-126">Pateicoties tam, ka līgumam ir pakalpojumu objekts, tagad var izveidot pakalpojumu līguma rindas ar šiem objektiem kā parādīts tālāk esošajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="d28c9-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="d28c9-127">Darbības veids</span><span class="sxs-lookup"><span data-stu-id="d28c9-127">Transaction type</span></span> | <span data-ttu-id="d28c9-128">Kategorija</span><span class="sxs-lookup"><span data-stu-id="d28c9-128">Category</span></span>           | <span data-ttu-id="d28c9-129">Pakalpojumu objekts</span><span class="sxs-lookup"><span data-stu-id="d28c9-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="d28c9-130">Stunda</span><span class="sxs-lookup"><span data-stu-id="d28c9-130">Hour</span></span>             | <span data-ttu-id="d28c9-131">Pārbaude</span><span class="sxs-lookup"><span data-stu-id="d28c9-131">Inspection</span></span>         | <span data-ttu-id="d28c9-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-132">EL-S/1000</span></span>      |
| <span data-ttu-id="d28c9-133">Stunda</span><span class="sxs-lookup"><span data-stu-id="d28c9-133">Hour</span></span>             | <span data-ttu-id="d28c9-134">Ātrumkārbas tīrīšana</span><span class="sxs-lookup"><span data-stu-id="d28c9-134">Gear box cleaning</span></span>  | <span data-ttu-id="d28c9-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-135">EL-S/1000</span></span>      |
| <span data-ttu-id="d28c9-136">Krājums</span><span class="sxs-lookup"><span data-stu-id="d28c9-136">Item</span></span>             | <span data-ttu-id="d28c9-137">Tīrīšanas materiāli</span><span class="sxs-lookup"><span data-stu-id="d28c9-137">Cleaning materials</span></span> | <span data-ttu-id="d28c9-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-138">EL-S/1000</span></span>      |
| <span data-ttu-id="d28c9-139">Stunda</span><span class="sxs-lookup"><span data-stu-id="d28c9-139">Hour</span></span>             | <span data-ttu-id="d28c9-140">Pārbaude</span><span class="sxs-lookup"><span data-stu-id="d28c9-140">Inspection</span></span>         | <span data-ttu-id="d28c9-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-141">EL-L/1000</span></span>      |
| <span data-ttu-id="d28c9-142">Stunda</span><span class="sxs-lookup"><span data-stu-id="d28c9-142">Hour</span></span>             | <span data-ttu-id="d28c9-143">Ātrumkārbas tīrīšana</span><span class="sxs-lookup"><span data-stu-id="d28c9-143">Gearbox cleaning</span></span>   | <span data-ttu-id="d28c9-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-144">EL-L/1000</span></span>      |
| <span data-ttu-id="d28c9-145">Krājums</span><span class="sxs-lookup"><span data-stu-id="d28c9-145">Item</span></span>             | <span data-ttu-id="d28c9-146">Tīrīšanas materiāli</span><span class="sxs-lookup"><span data-stu-id="d28c9-146">Cleaning materials</span></span> | <span data-ttu-id="d28c9-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d28c9-147">EL-L/1000</span></span>      |

<span data-ttu-id="d28c9-148">Apkopes veikšanas laikā tikusi nomainīta celtņa EL-S/1000 ātrumkārba.</span><span class="sxs-lookup"><span data-stu-id="d28c9-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="d28c9-149">Lai nomainītu objekta sastāvdaļu, ir iespējams piekļūt BOM Designer izmantojot pakalpojumu objekta relāciju, kura tika iestatīta pašreizējam pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="d28c9-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="d28c9-150">Piekļūstiet BOM Designer ar pakalpojumu objektu relācijas palīdzību.</span><span class="sxs-lookup"><span data-stu-id="d28c9-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="d28c9-151">Pakalpojumu līgumi</span><span class="sxs-lookup"><span data-stu-id="d28c9-151">Service agreements</span></span>
2. <span data-ttu-id="d28c9-152">Veiciet dubultklikšķi uz pakalpojumu līguma, vai noklikšķiniet uz Pakalpojumu līgums, lai izveidotu pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="d28c9-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="d28c9-153">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="d28c9-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="d28c9-154">Lai pakalpojumu līgumam pievienotu veidnes MK, nokliksķiniet uz Pakalpojumu objekti.</span><span class="sxs-lookup"><span data-stu-id="d28c9-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="d28c9-155">Veidlapā Pakalpojumu objekti noklikšķiniet uz Noformētājs, lai atvērtu veidotāja veidlapu un modificētu veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="d28c9-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="d28c9-156">Automātiski izveidoti pakalpojumu pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="d28c9-156">Automatically created service orders</span></span>

<span data-ttu-id="d28c9-157">Ja pakalpojumu līgumam tiek automātiski izveidoti pakalpojuma pasūtījumi, tad pakalpojumu objektu relācijas līgumā tiek izveidotas arī pakalpojumu pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="d28c9-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

