---
title: Krājumu saņemšanas pārskata profila iestatīšana
description: Šī tēma koncentrējas uz ierašanās pārskata profila iestatīšanu.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49670e4287faf3e50a824a5cbedd83ea7dbb8152
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244355"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="23698-103">Krājumu saņemšanas pārskata profila iestatīšana</span><span class="sxs-lookup"><span data-stu-id="23698-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="23698-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="23698-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="23698-105">Šī tēma koncentrējas uz ierašanās pārskata profila iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="23698-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="23698-106">Saņemšanas pārskata profils ir noteikumu kopums, kas tiks izmantots, kad lietotājs atver saņemšanas pārskata lapu.</span><span class="sxs-lookup"><span data-stu-id="23698-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="23698-107">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="23698-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="23698-108">Šo procedūru parasti veic saņemšanas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="23698-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="23698-109">Navigācijas rūtī ejiet uz **Moduļi > Krājumu pārvaldība > Iestatīšana> Izplatīšana > Ierašanās pārskata profili**.</span><span class="sxs-lookup"><span data-stu-id="23698-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="23698-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="23698-110">Select **New**.</span></span> <span data-ttu-id="23698-111">Tā kā būs gandrīz vienmēr jāstrādā vienā noliktavā, izkraujot kravas no pilnām kravas automašīnām, jums vajadzētu izveidot saņemšanas pārskata profilu, lai vienkāršotu saņemto krājumu reģistrācijas procesu.</span><span class="sxs-lookup"><span data-stu-id="23698-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="23698-112">Laukā **Ierašanās pārskata profili** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="23698-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="23698-113">Laukā **Rādīt rindas** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="23698-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="23698-114">Atlasiet, kuras rindas parādīt kvītīs.</span><span class="sxs-lookup"><span data-stu-id="23698-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="23698-115">**Visas** — rādīt visas rindas neatkarīgi no statusa.</span><span class="sxs-lookup"><span data-stu-id="23698-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="23698-116">**Apstrādē** — rādīt kvītīs tās rindas, kuru progress ir Pabeigts vai Daļēji pabeigts.</span><span class="sxs-lookup"><span data-stu-id="23698-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="23698-117">Tas nozīmē, ka saņemšanas žurnālā katrai rindai tika reģistrēts pilns daudzums vai daļējais daudzums.</span><span class="sxs-lookup"><span data-stu-id="23698-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="23698-118">**Nepabeigts** — rādīt kvītīs tās rindas, kuru progress ir Nav vai Daļēji pabeigts.</span><span class="sxs-lookup"><span data-stu-id="23698-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="23698-119">Tas nozīmē, ka saņemšanas žurnālā katrai rindai daudzums netiek reģistrēts vispār vai tikai daļēji.</span><span class="sxs-lookup"><span data-stu-id="23698-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="23698-120">Izvērsiet vai sakļaujiet sadaļu **Ierašanās opcijas**.</span><span class="sxs-lookup"><span data-stu-id="23698-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="23698-121">Laukā **Dienas uz priekšu** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="23698-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="23698-122">Ar šo tiek iestatīts filtrs, lai parādītu saņemšanas rindas, ko paredzams saņemt tuvāko dienu laikā (atkarībā no iestatītā numura).</span><span class="sxs-lookup"><span data-stu-id="23698-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="23698-123">Laukā **Dienas atpakaļ** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="23698-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="23698-124">Ar šo tiek iestatīts filtrs, lai parādītu saņemšanas rindas, ko bija paredzēts saņemt vairākas dienas pirms šodienas datuma.</span><span class="sxs-lookup"><span data-stu-id="23698-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="23698-125">Laukā **Noliktavas** atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="23698-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="23698-126">Filtrējiet pēc vienas vai vairākām noliktavām.</span><span class="sxs-lookup"><span data-stu-id="23698-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="23698-127">Atlasiet vērtību laukā **Piegādes režīms**.</span><span class="sxs-lookup"><span data-stu-id="23698-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="23698-128">Šādi filtrs tiek iestatīts tā, lai parādītu tikai ieejas plūsmas rindas ar šo piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="23698-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="23698-129">Laukā **Nosaukums** atlasiet WHS.</span><span class="sxs-lookup"><span data-stu-id="23698-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="23698-130">Laukā **Noliktava** atkasiet 24. noliktavu.</span><span class="sxs-lookup"><span data-stu-id="23698-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="23698-131">Tā ir noklusētā noliktava, kas tiks izmantota reģistrētām ieejas plūsmas rindām, kas lieto šo profilu.</span><span class="sxs-lookup"><span data-stu-id="23698-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="23698-132">Laukā **Atrašanās vieta** atlasiet **Aizmugurējās durvis**.</span><span class="sxs-lookup"><span data-stu-id="23698-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="23698-133">Tas ir noklusētais novietojums, kas tiks izmantots reģistrētām ieejas plūsmas rindām, kas lieto šo profilu.</span><span class="sxs-lookup"><span data-stu-id="23698-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="23698-134">Izvērsiet vai sakļaujiet sadaļu **Ierašanās vaicājuma informācija**.</span><span class="sxs-lookup"><span data-stu-id="23698-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="23698-135">Laukā **Ierobežot vietā** atkasiet 2. vietu.</span><span class="sxs-lookup"><span data-stu-id="23698-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="23698-136">Šādi filtrs tiek iestatīts tā, lai parādītu tikai ieejas plūsmas rindas ar šo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="23698-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="23698-137">Opciju **Pirkuma pasūtījumi** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="23698-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="23698-138">Atlasiet ieejas plūsmas rindas no pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="23698-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="23698-139">Opciju **Pārsūtīšanas pasūtījumi** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="23698-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="23698-140">Atlasiet ieejas plūsmas rindas no pārsūtīšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="23698-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="23698-141">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="23698-141">Select **Save**.</span></span>
18. <span data-ttu-id="23698-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="23698-142">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]