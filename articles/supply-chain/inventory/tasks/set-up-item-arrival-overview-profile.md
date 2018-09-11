--- 
title: "Krājumu saņemšanas pārskata profila iestatīšana"
description: "Šis uzdevums fokusējas uz saņemšanas pārskata profila iestatīšanu."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 2f5176ddbf9a28f76b37d20c7b354f3c3939e1e8
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="a0d21-103">Krājumu saņemšanas pārskata profila iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a0d21-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0d21-104">Šis uzdevums fokusējas uz saņemšanas pārskata profila iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="a0d21-105">Saņemšanas pārskata profils ir noteikumu kopums, kas tiks izmantots, kad lietotājs atver saņemšanas pārskata lapu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="a0d21-106">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="a0d21-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="a0d21-107">Šo procedūru parasti veic saņemšanas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="a0d21-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="a0d21-108">Dodieties uz Krājumu pārvaldība > Iestatīšana > Sadale > Saņemšanas pārskata profili.</span><span class="sxs-lookup"><span data-stu-id="a0d21-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="a0d21-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a0d21-109">Click New.</span></span>
    * <span data-ttu-id="a0d21-110">Tā kā būs gandrīz vienmēr jāstrādā vienā noliktavā, izkraujot kravas no pilnām kravas automašīnām, jums vajadzētu izveidot saņemšanas pārskata profilu, lai vienkāršotu saņemto krājumu reģistrācijas procesu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="a0d21-111">Laukā Saņemšanas pārskata profila nosaukums ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a0d21-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="a0d21-112">Laukā Rādīt rindas atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="a0d21-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="a0d21-113">Atlasiet, kuras rindas vēlaties skatīt saņemšanām: Visas — Skatīt visas rindas, neatkarīgi no statusa.</span><span class="sxs-lookup"><span data-stu-id="a0d21-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="a0d21-114">Notiek — Skatīt rindas saņemšanām, kuru izpilde ir Pabeigta vai Daļēji.</span><span class="sxs-lookup"><span data-stu-id="a0d21-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="a0d21-115">Tas nozīmē, ka saņemšanas žurnālā katrai rindai tika reģistrēts pilns daudzums vai daļējais daudzums.</span><span class="sxs-lookup"><span data-stu-id="a0d21-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="a0d21-116">Nepabeigta — Skatīt rindas saņemšanām, kuru izpilde ir Nav vai Daļēji.</span><span class="sxs-lookup"><span data-stu-id="a0d21-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="a0d21-117">Tas nozīmē, ka saņemšanas žurnālā katrai rindai daudzums netiek reģistrēts vispār vai tikai daļēji.</span><span class="sxs-lookup"><span data-stu-id="a0d21-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="a0d21-118">Izvērsiet vai sakļaujiet sadaļu Saņemšanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="a0d21-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="a0d21-119">Laukā Dienas turpmāk ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a0d21-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="a0d21-120">Ar šo tiek iestatīts filtrs, lai parādītu saņemšanas rindas, ko paredzams saņemt tuvāko dienu laikā (atkarībā no iestatītā numura).</span><span class="sxs-lookup"><span data-stu-id="a0d21-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="a0d21-121">Laukā Dienas iepriekš ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a0d21-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="a0d21-122">Ar šo tiek iestatīts filtrs, lai parādītu saņemšanas rindas, ko bija paredzēts saņemt vairākas dienas pirms šodienas datuma.</span><span class="sxs-lookup"><span data-stu-id="a0d21-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="a0d21-123">Laukā Noliktavas ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a0d21-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="a0d21-124">Filtrējiet pēc vienas vai vairākām noliktavām.</span><span class="sxs-lookup"><span data-stu-id="a0d21-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="a0d21-125">Laukā Piegādes veids atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a0d21-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="a0d21-126">Šādi filtrs tiek iestatīts tā, lai parādītu tikai ieejas plūsmas rindas ar šo piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="a0d21-127">Laukā Nosaukums atlasiet WHS.</span><span class="sxs-lookup"><span data-stu-id="a0d21-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="a0d21-128">Laukā Noliktava atlasiet noliktavu 24.</span><span class="sxs-lookup"><span data-stu-id="a0d21-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="a0d21-129">Tā ir noklusētā noliktava, kas tiks izmantota reģistrētām ieejas plūsmas rindām, kas lieto šo profilu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="a0d21-130">Laukā Novietojums atlasiet Baydoor.</span><span class="sxs-lookup"><span data-stu-id="a0d21-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="a0d21-131">Tas ir noklusētais novietojums, kas tiks izmantots reģistrētām ieejas plūsmas rindām, kas lieto šo profilu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="a0d21-132">Izvērsiet vai sakļaujiet sadaļu Saņemšanas vaicājuma dati.</span><span class="sxs-lookup"><span data-stu-id="a0d21-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="a0d21-133">Laukā Ierobežot ar atrašanās vietu atlasiet vietu 2.</span><span class="sxs-lookup"><span data-stu-id="a0d21-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="a0d21-134">Šādi filtrs tiek iestatīts tā, lai parādītu tikai ieejas plūsmas rindas ar šo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="a0d21-135">Opciju Pirkšanas pasūtījumi iestatiet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a0d21-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="a0d21-136">Atlasiet ieejas plūsmas rindas no pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="a0d21-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="a0d21-137">Opciju Pārsūtīšanas pasūtījumi iestatiet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a0d21-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="a0d21-138">Atlasiet ieejas plūsmas rindas no pārsūtīšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="a0d21-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="a0d21-139">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a0d21-139">Click Save.</span></span>
18. <span data-ttu-id="a0d21-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a0d21-140">Close the page.</span></span>


