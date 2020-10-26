---
title: Degvielas rādītāja saistīšana ar pārvadātāju kā papildobjekta maksu
description: Šajā ceļvedī parādīts, kā izveidot papildobjekta piešķiri, pārvadātāja papildobjekta maksu, papildobjekta šablonu degvielas piemaksai un saistīt pārvadātāja degvielas rādītāju ar pārvadātāju.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfecdbd8ca2d6124906ef664493602a1d0ac0baf
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981925"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="caa65-103">Degvielas rādītāja saistīšana ar pārvadātāju kā papildobjekta maksu</span><span class="sxs-lookup"><span data-stu-id="caa65-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="caa65-104">Šajā ceļvedī parādīts, kā izveidot papildobjekta piešķiri, pārvadātāja papildobjekta maksu, papildobjekta šablonu degvielas piemaksai un saistīt pārvadātāja degvielas rādītāju ar pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="caa65-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="caa65-105">Pirms izpildīt šo ceļvedi ir jāiestata degvielas rādītājs.</span><span class="sxs-lookup"><span data-stu-id="caa65-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="caa65-106">To var izdarīt, izmantojot ceļvedi "Pārvadātāja degvielas rādītāja iestatīšana".</span><span class="sxs-lookup"><span data-stu-id="caa65-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="caa65-107">Šos iestatīšanas uzdevumus parasti veic loģistikas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="caa65-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="caa65-108">Demonstrācijas dati, kas tiek izmantoti, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="caa65-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="caa65-109">Papildobjekta šablona izveide</span><span class="sxs-lookup"><span data-stu-id="caa65-109">Create an accessorial master</span></span>
1. <span data-ttu-id="caa65-110">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Papildobjekta šabloni.</span><span class="sxs-lookup"><span data-stu-id="caa65-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="caa65-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="caa65-111">Click New.</span></span>
3. <span data-ttu-id="caa65-112">Laukā Papildobjekta šablons ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="caa65-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="caa65-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="caa65-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="caa65-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="caa65-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="caa65-115">Pārvadātāja papildobjekta maksas izveide</span><span class="sxs-lookup"><span data-stu-id="caa65-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="caa65-116">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Pārvadātāja papildobjekta maksas.</span><span class="sxs-lookup"><span data-stu-id="caa65-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="caa65-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="caa65-117">Click New.</span></span>
3. <span data-ttu-id="caa65-118">Laukā Pārvadātāja papildobjekta ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="caa65-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="caa65-119">Laukā Sūtījumu pārvadātājs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="caa65-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="caa65-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="caa65-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="caa65-121">Šajā piemērā izvēlieties Kravas pārvadātājs.</span><span class="sxs-lookup"><span data-stu-id="caa65-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="caa65-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="caa65-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="caa65-123">Laukā Pārvadātāja pakalpojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="caa65-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="caa65-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="caa65-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="caa65-125">Laukā Papildobjekta šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="caa65-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="caa65-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="caa65-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="caa65-127">Šajā piemērā izvēlieties jaunizveidoto Papildobjekta šablonu.</span><span class="sxs-lookup"><span data-stu-id="caa65-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="caa65-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="caa65-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="caa65-129">Papildobjekta piešķires izveide</span><span class="sxs-lookup"><span data-stu-id="caa65-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="caa65-130">Noklikšķiniet uz Papildobjekta piešķires.</span><span class="sxs-lookup"><span data-stu-id="caa65-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="caa65-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="caa65-131">Click New.</span></span>
3. <span data-ttu-id="caa65-132">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="caa65-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="caa65-133">Pārslēdziet sadaļas Kritēriji paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="caa65-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="caa65-134">Kritērijos var izvēlēties vienmēr lietot degvielas piemaksu vai šim piemēram izvēlēties, ka tā piemērojama tikai noteiktā reģionā.</span><span class="sxs-lookup"><span data-stu-id="caa65-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="caa65-135">Laukā Pasta indekss no ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="caa65-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="caa65-136">Laukā Pasta indekss līdz ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="caa65-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="caa65-137">Pārslēdziet sadaļas Aprēķins paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="caa65-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="caa65-138">Aprēķina sadaļā var norādīt, kā aprēķināt degvielas piemaksu.</span><span class="sxs-lookup"><span data-stu-id="caa65-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="caa65-139">Šis aprēķins ir atkarīgs no Papildobjekta vienības, kuru izvēlējāties kā bāzi aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="caa65-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="caa65-140">Laukā Papildobjekta maksas tips atlasiet "Degvielas piemaksa".</span><span class="sxs-lookup"><span data-stu-id="caa65-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="caa65-141">Laukā Papildobjekta vienība atlasiet "Nobraukums".</span><span class="sxs-lookup"><span data-stu-id="caa65-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="caa65-142">Laukā Reģions noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="caa65-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="caa65-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="caa65-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="caa65-144">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="caa65-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="caa65-145">Pārvadātāju novērtēšanas profila atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="caa65-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="caa65-146">Pārejiet uz sadaļu Transportēšanas pārvaldība > Iestatījumi > Pārvadātāji > Sūtījumu pārvadātāji.</span><span class="sxs-lookup"><span data-stu-id="caa65-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="caa65-147">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="caa65-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="caa65-148">Pārslēdziet sadaļas Novērtējuma profili izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="caa65-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="caa65-149">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="caa65-149">Click Edit.</span></span>
5. <span data-ttu-id="caa65-150">Laukā Pārvadātāja degvielas rādītājs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="caa65-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="caa65-151">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="caa65-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="caa65-152">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="caa65-152">Click Save.</span></span>

