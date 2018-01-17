---
title: "Sistēmas grupēšana atvērtā darbu sarakstā"
description: "Šajā tēmā ir aprakstīts, kā filtrēt atvērto darbu sarakstu mobilajā ierīcē."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3592094d09a8596f88c44d869b22035a126fab69
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="243e9-103">Sistēmas grupēšana atvērtā darbu sarakstā</span><span class="sxs-lookup"><span data-stu-id="243e9-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="243e9-104">Izmantojot sistēmas grupēšanas lauku, varat filtrēt atvērto darbu sarakstu, nerediģējot mobilās ierīces izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="243e9-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="243e9-105">Tādā gadījumā sistēmas grupēšana darbojas darbu saraksta filtrēšanai vienā darba virsraksta laukā.</span><span class="sxs-lookup"><span data-stu-id="243e9-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="243e9-106">Sistēmas grupēšanu nevar izmantot, lai filtrētu rindas līmeņa laukus.</span><span class="sxs-lookup"><span data-stu-id="243e9-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="243e9-107">Sistēmas grupēšanas atvērtā darbu sarakstā iestatīšana</span><span class="sxs-lookup"><span data-stu-id="243e9-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="243e9-108">Izmantojiet tālāk aprakstītās darbības, lai iestatītu sistēmas grupēšanu atvērtā darbu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="243e9-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="243e9-109">No mobilās ierīces izvēlnes vienuma atlasiet **Režīms: netiešs** un **Aktivitātes kods: Parādīt atvērto darbu sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="243e9-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="243e9-110">Kļūst pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="243e9-110">The following options become available.</span></span> <span data-ttu-id="243e9-111">Šīs opcijas ir nepieciešamas sistēmas grupēšanai atvērtajā darbu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="243e9-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="243e9-112">Opcija</span><span class="sxs-lookup"><span data-stu-id="243e9-112">Option</span></span>        | <span data-ttu-id="243e9-113">Apraksts</span><span class="sxs-lookup"><span data-stu-id="243e9-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="243e9-114">Sistēmas grupēšanas atļaušana</span><span class="sxs-lookup"><span data-stu-id="243e9-114">Allow system grouping</span></span>   | <span data-ttu-id="243e9-115">Iespējo sistēmas grupēšanu atlasītajam darbu saraksta izvēlnes vienumam.</span><span class="sxs-lookup"><span data-stu-id="243e9-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="243e9-116">Sistēmas grupēšanas lauks</span><span class="sxs-lookup"><span data-stu-id="243e9-116">System grouping field</span></span>   | <span data-ttu-id="243e9-117">Pieejams tikai tad, ja vienumam **Atļaut sistēmas darbu** ir iestatīta opcija **Jā**.</span><span class="sxs-lookup"><span data-stu-id="243e9-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="243e9-118">Atlasiet lauku, kas nosaka, kā izdošanas darbs tiks grupēts darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="243e9-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="243e9-119">Piemēram, ja atlasīsiet lauku **ShipmentId**, darbinieks skenēs sūtījuma ID, lai grupētu izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="243e9-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="243e9-120">Pēc tam viss ar sūtījumu saistītais darbs tiks piešķirts darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="243e9-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="243e9-121">Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="243e9-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="243e9-122">Izmantojiet lauku **Sistēmas grupēšanas etiķete**, lai informētu darbiniekus, kas jāskenē.</span><span class="sxs-lookup"><span data-stu-id="243e9-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="243e9-123">Sistēmas grupēšanas etiķete</span><span class="sxs-lookup"><span data-stu-id="243e9-123">System grouping label</span></span>   | <span data-ttu-id="243e9-124">Pieejams tikai tad, ja vienumam **Atļaut sistēmas darbu** ir iestatīta opcija **Jā**.</span><span class="sxs-lookup"><span data-stu-id="243e9-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="243e9-125">Ievadiet informāciju darbiniekam par to, kas jāskenē, kad tiek grupēts izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="243e9-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="243e9-126">Piemēram, ja izmantojat lauku **ShipmentId**, lai grupētu izdošanas darbu pēc sūtījuma, varat šajā laukā ievadīt vērtību Sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="243e9-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="243e9-127">Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="243e9-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="243e9-128">Turklāt laikā **Sistēmas grupēšanas lauks** ir jāatlasa lauks, pēc kura grupēt.</span><span class="sxs-lookup"><span data-stu-id="243e9-128">You must also select the field to group by in the **System grouping** field.</span></span>|

