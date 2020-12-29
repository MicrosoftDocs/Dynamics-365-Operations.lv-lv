---
title: Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu
description: Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433008"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="482be-103">Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu</span><span class="sxs-lookup"><span data-stu-id="482be-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="482be-104">Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus.</span><span class="sxs-lookup"><span data-stu-id="482be-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="482be-105">Tas tiek darīts, izmantojot drošības krājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="482be-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="482be-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="482be-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="482be-107">Šis uzdevums ir paredzēts ražošanas plānotājam, lai palīdzētu uzturēt minimālo segumu.</span><span class="sxs-lookup"><span data-stu-id="482be-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="482be-108">Izveidot jaunu drošības krājumu žurnāla nosaukumu</span><span class="sxs-lookup"><span data-stu-id="482be-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="482be-109">**Navigācijas rūtī** pārejiet uz **Vispārējā plānošana > Iestatīšana > Drošības krājumu žurnāla nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="482be-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="482be-110">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="482be-110">Click **New**.</span></span>
3. <span data-ttu-id="482be-111">Laukā **Nosaukums** ierakstiet “Materiāls”.</span><span class="sxs-lookup"><span data-stu-id="482be-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="482be-112">Laukā **Apraksts** ierakstiet “Materiāls”.</span><span class="sxs-lookup"><span data-stu-id="482be-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="482be-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="482be-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="482be-114">Izveidot drošības krājumu žurnālu</span><span class="sxs-lookup"><span data-stu-id="482be-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="482be-115">**Navigācijas rūtī** pārejiet uz **Vispārējā plānošana > Vispārējā plānošana > Palaist > Drošības krājumu aprēķins**.</span><span class="sxs-lookup"><span data-stu-id="482be-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="482be-116">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="482be-116">Click **New**.</span></span>
3. <span data-ttu-id="482be-117">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="482be-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="482be-118">Atlasiet drošības krājumu žurnāla nosaukumu, kurus jūs izveidojāt, piemēram, Materiāls.</span><span class="sxs-lookup"><span data-stu-id="482be-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="482be-119">Noklikšķiniet uz **Izveidot rindas**.</span><span class="sxs-lookup"><span data-stu-id="482be-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="482be-120">Ievadiet datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="482be-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="482be-121">Ievadiet datumu laukā **Līdz datumam**.</span><span class="sxs-lookup"><span data-stu-id="482be-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="482be-122">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="482be-122">Click **OK**.</span></span> <span data-ttu-id="482be-123">Šādi tiks izveidotas rindas tām dimensijām, kurām ir krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="482be-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="482be-124">Aprēķināt priekšlikumu</span><span class="sxs-lookup"><span data-stu-id="482be-124">Calculate proposal</span></span>
1. <span data-ttu-id="482be-125">Noklikšķiniet uz **Aprēķināt priekšlikumu**.</span><span class="sxs-lookup"><span data-stu-id="482be-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="482be-126">Atlasiet opciju **Izmantot vidējo izejas plūsmu izpildes laikā**.</span><span class="sxs-lookup"><span data-stu-id="482be-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="482be-127">Vienumu **Reizināšanas koeficients iestatiet** uz “10”.</span><span class="sxs-lookup"><span data-stu-id="482be-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="482be-128">Reizināšanas koeficients tiek lietots, lai koriģētu priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="482be-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="482be-129">Tā kā demonstrācijas datiem tikai dažas transakcijas, jums ir jāiestata šis koeficients, lai iegūtu reālistisku priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="482be-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="482be-130">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="482be-130">Click **OK**.</span></span> <span data-ttu-id="482be-131">Ritiniet uz leju, lai atrastu M0002 un M0003.</span><span class="sxs-lookup"><span data-stu-id="482be-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="482be-132">Skatiet kolonnu **Aprēķinātais minimālais** daudzums.</span><span class="sxs-lookup"><span data-stu-id="482be-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="482be-133">Atjaunināt minimālo daudzumu</span><span class="sxs-lookup"><span data-stu-id="482be-133">Update minimum quantity</span></span>
1. <span data-ttu-id="482be-134">Laukā **Jaunais minimālais daudzums** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="482be-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="482be-135">Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai.</span><span class="sxs-lookup"><span data-stu-id="482be-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="482be-136">Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību.</span><span class="sxs-lookup"><span data-stu-id="482be-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="482be-137">Piemēram, šajā laukā varat ievadīt vērtību Aprēķinātais minimālais daudzums tādam M0002, kam ir noliktava 12.</span><span class="sxs-lookup"><span data-stu-id="482be-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="482be-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="482be-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="482be-139">Piemēram, varat atlasīt M0002, kam ir noliktava 12.</span><span class="sxs-lookup"><span data-stu-id="482be-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="482be-140">Laukā **Jaunais minimālais daudzums** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="482be-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="482be-141">Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai.</span><span class="sxs-lookup"><span data-stu-id="482be-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="482be-142">Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību.</span><span class="sxs-lookup"><span data-stu-id="482be-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="482be-143">Grāmatot jauno minimālo daudzumu un validēt rezultātu</span><span class="sxs-lookup"><span data-stu-id="482be-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="482be-144">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="482be-144">Click **Post**.</span></span>
2. <span data-ttu-id="482be-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="482be-145">Click **OK**.</span></span>
3. <span data-ttu-id="482be-146">Noklikšķiniet, lai sekotu saitei laukā **Krājuma numurs**.</span><span class="sxs-lookup"><span data-stu-id="482be-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="482be-147">Noklikšķiniet, lai sekotu saitei laukā **Krājuma numurs**.</span><span class="sxs-lookup"><span data-stu-id="482be-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="482be-148">**Darbību rūtī** noklikšķiniet uz Plāns.</span><span class="sxs-lookup"><span data-stu-id="482be-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="482be-149">Noklikšķiniet uz **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="482be-149">Click **Item coverage**.</span></span> <span data-ttu-id="482be-150">Ņemiet vērā, ka **Minimālais daudzums** ir atjaunināts ar jaunu minimālo daudzumu no drošības krājumu žurnāla.</span><span class="sxs-lookup"><span data-stu-id="482be-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

