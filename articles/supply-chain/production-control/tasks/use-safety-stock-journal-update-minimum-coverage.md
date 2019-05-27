---
title: Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu
description: Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571431"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="4995e-103">Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu</span><span class="sxs-lookup"><span data-stu-id="4995e-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4995e-104">Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus.</span><span class="sxs-lookup"><span data-stu-id="4995e-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="4995e-105">Tas tiek darīts, izmantojot drošības krājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="4995e-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="4995e-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="4995e-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="4995e-107">Šis uzdevums ir paredzēts ražošanas plānotājam, lai palīdzētu uzturēt minimālo segumu.</span><span class="sxs-lookup"><span data-stu-id="4995e-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="4995e-108">Izveidot jaunu drošības krājumu žurnāla nosaukumu</span><span class="sxs-lookup"><span data-stu-id="4995e-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="4995e-109">Dodieties uz Drošības krājumu žurnālu nosaukumiem.</span><span class="sxs-lookup"><span data-stu-id="4995e-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="4995e-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4995e-110">Click New.</span></span>
3. <span data-ttu-id="4995e-111">Laukā Nosaukums ierakstiet “Materiāls”.</span><span class="sxs-lookup"><span data-stu-id="4995e-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="4995e-112">Laukā Apraksts ierakstiet “Materiāls”.</span><span class="sxs-lookup"><span data-stu-id="4995e-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="4995e-113">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4995e-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="4995e-114">Izveidot drošības krājumu žurnālu</span><span class="sxs-lookup"><span data-stu-id="4995e-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="4995e-115">Dodieties uz Drošības krājumu aprēķins.</span><span class="sxs-lookup"><span data-stu-id="4995e-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="4995e-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4995e-116">Click New.</span></span>
3. <span data-ttu-id="4995e-117">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4995e-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="4995e-118">Atlasiet drošības krājumu žurnāla nosaukumu, kurus jūs izveidojāt, piemēram, Materiāls.</span><span class="sxs-lookup"><span data-stu-id="4995e-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="4995e-119">Noklikšķiniet uz Izveidot rindas.</span><span class="sxs-lookup"><span data-stu-id="4995e-119">Click Create lines.</span></span>
5. <span data-ttu-id="4995e-120">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="4995e-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4995e-121">Iestatiet datumu uz “2015.01.02”.</span><span class="sxs-lookup"><span data-stu-id="4995e-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="4995e-122">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="4995e-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="4995e-123">Iestatiet datumu uz “2015.12.30”.</span><span class="sxs-lookup"><span data-stu-id="4995e-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="4995e-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-124">Click OK.</span></span>
    * <span data-ttu-id="4995e-125">Šādi tiks izveidotas rindas tām dimensijām, kurām ir krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="4995e-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="4995e-126">Aprēķināt priekšlikumu</span><span class="sxs-lookup"><span data-stu-id="4995e-126">Calculate proposal</span></span>
1. <span data-ttu-id="4995e-127">Noklikšķiniet uz Aprēķināt priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="4995e-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="4995e-128">Atlasiet opciju Izmantot vidējo izejas plūsmu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="4995e-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="4995e-129">Vienumu Reizināšanas koeficients iestatiet uz “10”.</span><span class="sxs-lookup"><span data-stu-id="4995e-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="4995e-130">Reizināšanas koeficients tiek lietots, lai koriģētu priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="4995e-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="4995e-131">Tā kā demonstrācijas datiem tikai dažas transakcijas, jums ir jāiestata šis koeficients, lai iegūtu reālistisku priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="4995e-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="4995e-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-132">Click OK.</span></span>
    * <span data-ttu-id="4995e-133">Ritiniet uz leju, lai atrastu M0002 un M0003.</span><span class="sxs-lookup"><span data-stu-id="4995e-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="4995e-134">Skatiet kolonnu Aprēķinātais minimālais daudzums.</span><span class="sxs-lookup"><span data-stu-id="4995e-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="4995e-135">Atjaunināt minimālo daudzumu</span><span class="sxs-lookup"><span data-stu-id="4995e-135">Update minimum quantity</span></span>
1. <span data-ttu-id="4995e-136">Laukā Jaunais minimālais daudzums ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="4995e-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="4995e-137">Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai.</span><span class="sxs-lookup"><span data-stu-id="4995e-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="4995e-138">Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību.</span><span class="sxs-lookup"><span data-stu-id="4995e-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="4995e-139">Piemēram, šajā laukā varat ievadīt vērtību Aprēķinātais minimālais daudzums tādam M0002, kam ir noliktava 12.</span><span class="sxs-lookup"><span data-stu-id="4995e-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="4995e-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4995e-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4995e-141">Piemēram, varat atlasīt M0002, kam ir noliktava 12.</span><span class="sxs-lookup"><span data-stu-id="4995e-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="4995e-142">Laukā Jaunais minimālais daudzums ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="4995e-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="4995e-143">Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai.</span><span class="sxs-lookup"><span data-stu-id="4995e-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="4995e-144">Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību.</span><span class="sxs-lookup"><span data-stu-id="4995e-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="4995e-145">Grāmatot jauno minimālo daudzumu un validēt rezultātu</span><span class="sxs-lookup"><span data-stu-id="4995e-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="4995e-146">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="4995e-146">Click Post.</span></span>
2. <span data-ttu-id="4995e-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-147">Click OK.</span></span>
3. <span data-ttu-id="4995e-148">Noklikšķiniet, lai sekotu saitei laukā Krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="4995e-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="4995e-149">Noklikšķiniet, lai sekotu saitei laukā Krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="4995e-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="4995e-150">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="4995e-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="4995e-151">Noklikšķiniet uz Krājumu vajadzība.</span><span class="sxs-lookup"><span data-stu-id="4995e-151">Click Item coverage.</span></span>
    * <span data-ttu-id="4995e-152">Ņemiet vērā, ka Minimālais daudzums ir atjaunināts ar jaunu minimālo daudzumu no drošības krājumu žurnāla.</span><span class="sxs-lookup"><span data-stu-id="4995e-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

