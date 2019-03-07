---
title: Pilnīga izlaistās preces šablona pamata iestatīšana
description: Šajā procedūrā tiek parādīts, kā veikt minimālo uzstādīšanu, kas ir nepieciešama pirms preces šablonu varēs izmantot MK versijās.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "354786"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="0ceda-103">Pilnīga izlaistās preces šablona pamata iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0ceda-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ceda-104">Šajā procedūrā tiek parādīts, kā veikt minimālo uzstādīšanu, kas ir nepieciešama pirms preces šablonu varēs izmantot MK versijās.</span><span class="sxs-lookup"><span data-stu-id="0ceda-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="0ceda-105">Šī ir trešā procedūra no astoņām, kurā ir skaidrots, kā veidot kombinācijas konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0ceda-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="0ceda-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="0ceda-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="0ceda-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="0ceda-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0ceda-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0ceda-109">Atlasiet preces šablonu, kas tika izlaists otrajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="0ceda-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="0ceda-110">Šīs preces šablons tiek izveidots ar konfigurācijas atbilstoši dimensijām tehnoloģiju.</span><span class="sxs-lookup"><span data-stu-id="0ceda-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="0ceda-111">Darbību rūtī noklikšķiniet uz Prece.</span><span class="sxs-lookup"><span data-stu-id="0ceda-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="0ceda-112">Noklikšķiniet uz Dimensiju grupas, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="0ceda-113">Laukā Noliktavas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0ceda-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0ceda-115">Noliktavas dimensiju grupa nosaka, kādas noliktavas dimensijas tiek lietotas preces transakcijai.</span><span class="sxs-lookup"><span data-stu-id="0ceda-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="0ceda-116">Šai procedūrai atlasiet Vieta.</span><span class="sxs-lookup"><span data-stu-id="0ceda-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="0ceda-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0ceda-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0ceda-118">Laukā Izsekošanas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0ceda-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0ceda-120">Izsekošanas dimensiju grupa nosaka, kādas izsekošanas dimensijas tiek lietotas preces transakcijai.</span><span class="sxs-lookup"><span data-stu-id="0ceda-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="0ceda-121">Šai procedūrai atlasiet Nav.</span><span class="sxs-lookup"><span data-stu-id="0ceda-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="0ceda-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0ceda-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="0ceda-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0ceda-123">Click OK.</span></span>
12. <span data-ttu-id="0ceda-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0ceda-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="0ceda-125">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0ceda-125">Click Edit.</span></span>
    * <span data-ttu-id="0ceda-126">Atveriet formu Detalizēta informācija par izlaistajām precēm, lai turpinātu iestatīšanas uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="0ceda-127">Laukā Krājumu modeļu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0ceda-128">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0ceda-129">Krājumu modeļu grupās ir ietverti iestatījumi, kas nosaka krājumu kontroles un vadības veidu to saņemšanas un izsniegšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="0ceda-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="0ceda-130">Šie iestatījumi nosaka arī preču patēriņa aprēķināšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="0ceda-131">Šai procedūrai atlasiet FIFO.</span><span class="sxs-lookup"><span data-stu-id="0ceda-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="0ceda-132">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0ceda-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="0ceda-133">Izvērsiet vai sakļaujiet sadaļu Pārvaldīt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="0ceda-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="0ceda-134">Laukā Krājumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="0ceda-135">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0ceda-136">Krājumu grupas lieto, lai pārvaldītu krājumus, sadalot krājumus grupās.</span><span class="sxs-lookup"><span data-stu-id="0ceda-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="0ceda-137">Šai procedūrai atlasiet CarAudio.</span><span class="sxs-lookup"><span data-stu-id="0ceda-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="0ceda-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0ceda-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="0ceda-139">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="0ceda-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="0ceda-140">Noklikšķiniet uz Pasūtījuma noklusējuma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="0ceda-140">Click Default order settings.</span></span>
23. <span data-ttu-id="0ceda-141">Laukā Noklusējuma pasūtījuma tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="0ceda-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="0ceda-142">Atlasiet Ražošana, lai norādītu, ka noklusējuma piegādes opcija šim preces šablonam ir tā ražošana.</span><span class="sxs-lookup"><span data-stu-id="0ceda-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="0ceda-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0ceda-143">Close the page.</span></span>
25. <span data-ttu-id="0ceda-144">Aizveriet formu Detalizēta informācija par izlaistajām precēm.</span><span class="sxs-lookup"><span data-stu-id="0ceda-144">Close the Released product details form.</span></span>

