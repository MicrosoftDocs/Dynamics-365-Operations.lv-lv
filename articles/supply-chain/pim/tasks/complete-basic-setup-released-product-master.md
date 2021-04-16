---
title: Pilnīga izlaistās preces šablona pamata iestatīšana
description: Šajā tēmā tiek parādīts, kā veikt minimālo uzstādīšanu, kas ir nepieciešama pirms preces šablonu varēs izmantot MK versijās.
author: ShylaThompson
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c41e9e3267f72a2452eddfeb15f8f5cba79b0b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820158"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="08934-103">Pilnīga izlaistās preces šablona pamata iestatīšana</span><span class="sxs-lookup"><span data-stu-id="08934-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08934-104">Šajā tēmā tiek parādīts, kā veikt minimālo uzstādīšanu, kas ir nepieciešama pirms preces šablonu varēs izmantot MK versijās.</span><span class="sxs-lookup"><span data-stu-id="08934-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="08934-105">Šī ir trešā procedūra no astoņām, kurā ir skaidrots, kā veidot kombinācijas konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="08934-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="08934-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="08934-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="08934-107">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="08934-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="08934-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="08934-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="08934-109">Atlasiet preces šablonu, kas tika izlaists otrajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="08934-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="08934-110">Šīs preces šablons tiek izveidots ar konfigurācijas atbilstoši dimensijām tehnoloģiju.</span><span class="sxs-lookup"><span data-stu-id="08934-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="08934-111">Darbību rūtī atlasiet **Prece**.</span><span class="sxs-lookup"><span data-stu-id="08934-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="08934-112">Atlasiet **Dimensiju grupas**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="08934-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="08934-113">Laukā **Noliktavas dimensiju grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="08934-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="08934-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="08934-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="08934-115">Noliktavas dimensiju grupa nosaka, kādas noliktavas dimensijas tiek lietotas preces transakcijai.</span><span class="sxs-lookup"><span data-stu-id="08934-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="08934-116">Šai procedūrai atlasiet **Vieta**.</span><span class="sxs-lookup"><span data-stu-id="08934-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="08934-117">Laukā **Izsekošanas dimensiju grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="08934-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="08934-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="08934-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="08934-119">Izsekošanas dimensiju grupa nosaka, kādas izsekošanas dimensijas tiek lietotas preces transakcijai.</span><span class="sxs-lookup"><span data-stu-id="08934-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="08934-120">Šai procedūrai atlasiet **Nav**.</span><span class="sxs-lookup"><span data-stu-id="08934-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="08934-121">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="08934-121">Click **OK**.</span></span>
10. <span data-ttu-id="08934-122">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="08934-122">Click **Edit**.</span></span>
11. <span data-ttu-id="08934-123">Laukā **Krājumu modeļu grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="08934-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="08934-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="08934-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="08934-125">Krājumu modeļu grupās ir ietverti iestatījumi, kas nosaka krājumu kontroles un vadības veidu to saņemšanas un izsniegšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="08934-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="08934-126">Šie iestatījumi nosaka arī preču patēriņa aprēķināšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="08934-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="08934-127">Šai procedūrai atlasiet **FIFO**.</span><span class="sxs-lookup"><span data-stu-id="08934-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="08934-128">Izvērsiet sadaļu **Pārvaldīt izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="08934-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="08934-129">Laukā **Krājumu grupa** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="08934-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="08934-130">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="08934-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="08934-131">Krājumu grupas lieto, lai pārvaldītu krājumus, sadalot krājumus grupās.</span><span class="sxs-lookup"><span data-stu-id="08934-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="08934-132">Šai procedūrai atlasiet **CarAudio**.</span><span class="sxs-lookup"><span data-stu-id="08934-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="08934-133">Darbību rūtī atlasiet **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="08934-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="08934-134">Atlasiet **Noklusējuma pasūtījuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="08934-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="08934-135">Laukā **Noklusējuma pasūtījuma tips** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="08934-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="08934-136">Atlasiet **Ražošana**, lai norādītu, ka noklusējuma piegādes opcija šim preces šablonam ir tā ražošana.</span><span class="sxs-lookup"><span data-stu-id="08934-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="08934-137">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="08934-137">Select **Save**.</span></span>
20. <span data-ttu-id="08934-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="08934-138">Close the page.</span></span>
21. <span data-ttu-id="08934-139">Aizveriet formu **Detalizēta informācija par izlaistajām precēm**.</span><span class="sxs-lookup"><span data-stu-id="08934-139">Close the **Released product details** form.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]