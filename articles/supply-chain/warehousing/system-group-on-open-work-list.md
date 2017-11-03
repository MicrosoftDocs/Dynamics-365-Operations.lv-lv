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
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6403fea54be4036f7a15c05b46f70d258d97c3e2
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="7e679-103">Sistēmas grupēšana atvērtā darbu sarakstā</span><span class="sxs-lookup"><span data-stu-id="7e679-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7e679-104">Izmantojot sistēmas grupēšanas lauku, varat filtrēt atvērto darbu sarakstu, nerediģējot mobilās ierīces izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="7e679-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="7e679-105">Tādā gadījumā sistēmas grupēšana darbojas darbu saraksta filtrēšanai vienā darba virsraksta laukā.</span><span class="sxs-lookup"><span data-stu-id="7e679-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="7e679-106">Sistēmas grupēšanu nevar izmantot, lai filtrētu rindas līmeņa laukus.</span><span class="sxs-lookup"><span data-stu-id="7e679-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="7e679-107">Sistēmas grupēšanas atvērtā darbu sarakstā iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7e679-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="7e679-108">Izmantojiet tālāk aprakstītās darbības, lai iestatītu sistēmas grupēšanu atvērtā darbu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="7e679-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="7e679-109">No mobilās ierīces izvēlnes vienuma atlasiet **Režīms: netiešs** un **Aktivitātes kods: Parādīt atvērto darbu sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="7e679-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="7e679-110">Kļūst pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="7e679-110">The following options become available.</span></span> <span data-ttu-id="7e679-111">Šīs opcijas ir nepieciešamas sistēmas grupēšanai atvērtajā darbu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="7e679-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="7e679-112">Opcija</span><span class="sxs-lookup"><span data-stu-id="7e679-112">Option</span></span>        | <span data-ttu-id="7e679-113">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7e679-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="7e679-114">Sistēmas grupēšanas atļaušana</span><span class="sxs-lookup"><span data-stu-id="7e679-114">Allow system grouping</span></span>   | <span data-ttu-id="7e679-115">Iespējo sistēmas grupēšanu atlasītajam darbu saraksta izvēlnes vienumam.</span><span class="sxs-lookup"><span data-stu-id="7e679-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="7e679-116">Sistēmas grupēšanas lauks</span><span class="sxs-lookup"><span data-stu-id="7e679-116">System grouping field</span></span>   | <span data-ttu-id="7e679-117">Pieejams tikai tad, ja vienumam **Atļaut sistēmas darbu** ir iestatīta opcija **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7e679-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="7e679-118">Atlasiet lauku, kas nosaka, kā izdošanas darbs tiks grupēts darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="7e679-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="7e679-119">Piemēram, ja atlasīsiet lauku **ShipmentId**, darbinieks skenēs sūtījuma ID, lai grupētu izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="7e679-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="7e679-120">Pēc tam viss ar sūtījumu saistītais darbs tiks piešķirts darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="7e679-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="7e679-121">Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="7e679-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="7e679-122">Izmantojiet lauku **Sistēmas grupēšanas etiķete**, lai informētu darbiniekus, kas jāskenē.</span><span class="sxs-lookup"><span data-stu-id="7e679-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="7e679-123">Sistēmas grupēšanas etiķete</span><span class="sxs-lookup"><span data-stu-id="7e679-123">System grouping label</span></span>   | <span data-ttu-id="7e679-124">Pieejams tikai tad, ja vienumam **Atļaut sistēmas darbu** ir iestatīta opcija **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7e679-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="7e679-125">Ievadiet informāciju darbiniekam par to, kas jāskenē, kad tiek grupēts izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="7e679-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="7e679-126">Piemēram, ja izmantojat lauku **ShipmentId**, lai grupētu izdošanas darbu pēc sūtījuma, varat šajā laukā ievadīt vērtību Sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="7e679-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="7e679-127">Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="7e679-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="7e679-128">Turklāt laikā **Sistēmas grupēšanas lauks** ir jāatlasa lauks, pēc kura grupēt.</span><span class="sxs-lookup"><span data-stu-id="7e679-128">You must also select the field to group by in the **System grouping** field.</span></span>|

