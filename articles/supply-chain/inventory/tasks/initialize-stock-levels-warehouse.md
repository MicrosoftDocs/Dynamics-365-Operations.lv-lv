---
title: Krājumu līmeņu inicializēšana noliktavā
description: Šajā procedūrā parādīts, kā manuāli atjaunot rīcībā esošo krājumu, izmantojot krājumu kustības žurnālu.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c1e5ca96919acde7e850292a73ebd00185f1f7a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244479"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="e31bc-103">Krājumu līmeņu inicializēšana noliktavā</span><span class="sxs-lookup"><span data-stu-id="e31bc-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e31bc-104">Šajā procedūrā parādīts, kā manuāli atjaunot rīcībā esošo krājumu, izmantojot krājumu kustības žurnālu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="e31bc-105">(Ir iespējams atjaunināt rīcībā esošos krājumus, importējot transakcijas datu elementos.) Šo ceļvedi var palaist demonstrācijas datu uzņēmumā USMF, kur ir pieejami visi nepieciešamie priekšnosacījumi, piemēram, žurnāla nosaukums, krājuma iestatījumi, grāmatošanas metodes un konti.</span><span class="sxs-lookup"><span data-stu-id="e31bc-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="e31bc-106">Šajā ceļvedī ir ieteiktas noteiktas vērtības krājumam un izmantotās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e31bc-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="e31bc-107">Ja jūs izvēlēsieties citu krājumu, jums var būt nepieciešams ievadīt vērtības citām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="e31bc-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="e31bc-108">Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumi > Kustība.</span><span class="sxs-lookup"><span data-stu-id="e31bc-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="e31bc-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e31bc-109">Click New.</span></span>
3. <span data-ttu-id="e31bc-110">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e31bc-111">Atlasiet IMov.</span><span class="sxs-lookup"><span data-stu-id="e31bc-111">Select IMov.</span></span>
    * <span data-ttu-id="e31bc-112">Dažādiem uzņēmējdarbības nolūkiem ieteicams izmantot atšķirīgas žurnāla nosaukuma veidnes.</span><span class="sxs-lookup"><span data-stu-id="e31bc-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="e31bc-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e31bc-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e31bc-114">Laukā Korespondējošais konts norādiet vērtības "140200".</span><span class="sxs-lookup"><span data-stu-id="e31bc-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="e31bc-115">Tas ir korespondējošais konts, kas būs noklusējuma korespondējošais konts žurnāla rindās.</span><span class="sxs-lookup"><span data-stu-id="e31bc-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="e31bc-116">Ir iespējams ignorēt noklusējumu, piešķirot dažādus korespondējošos kontus katrai rindai.</span><span class="sxs-lookup"><span data-stu-id="e31bc-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="e31bc-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e31bc-117">Click OK.</span></span>
8. <span data-ttu-id="e31bc-118">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e31bc-118">Click New.</span></span>
9. <span data-ttu-id="e31bc-119">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e31bc-120">Atlasiet krājumu A0001.</span><span class="sxs-lookup"><span data-stu-id="e31bc-120">Select item A0001.</span></span>
11. <span data-ttu-id="e31bc-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e31bc-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e31bc-122">Noklikšķiniet uz cilnes Krājumu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e31bc-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="e31bc-123">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="e31bc-124">Atlasiet vietu 1.</span><span class="sxs-lookup"><span data-stu-id="e31bc-124">Select site 1.</span></span>
15. <span data-ttu-id="e31bc-125">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e31bc-126">Atlasiet noliktavu 13.</span><span class="sxs-lookup"><span data-stu-id="e31bc-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="e31bc-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e31bc-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="e31bc-128">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="e31bc-129">Atlasiet novietojumu 13.</span><span class="sxs-lookup"><span data-stu-id="e31bc-129">Select location 13.</span></span>
20. <span data-ttu-id="e31bc-130">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="e31bc-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="e31bc-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e31bc-131">Click Save.</span></span>
22. <span data-ttu-id="e31bc-132">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="e31bc-132">Click Post.</span></span>
23. <span data-ttu-id="e31bc-133">Atzīmējiet vai notīriet izvēles rūtiņu Visas grāmatošanas kļūdas pārsūtīt uz jaunu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="e31bc-134">Ja iespējosiet šo opciju, jebkuras neiegrāmatotas rindas tiks kopētas uz jaunu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="e31bc-135">Žurnāla informāciju var izmantot, lai labotu problēmas un pēc tam vēlreiz grāmatot rindas.</span><span class="sxs-lookup"><span data-stu-id="e31bc-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="e31bc-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e31bc-136">Click OK.</span></span>
25. <span data-ttu-id="e31bc-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-137">Close the page.</span></span>
26. <span data-ttu-id="e31bc-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e31bc-138">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]