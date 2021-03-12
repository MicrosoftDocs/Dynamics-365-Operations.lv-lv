---
title: Tās pašas partijas rezervēšana pārdošanas pasūtījumam
description: Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fb1f9e017de71d01fbf7a05b579d68b702aa7c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001503"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="549ae-103">Tās pašas partijas rezervēšana pārdošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="549ae-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="549ae-104">Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju.</span><span class="sxs-lookup"><span data-stu-id="549ae-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="549ae-105">Tās pašas partijas rezervēšana ļauj rezervēt krājumus pārdošanas pasūtījuma rindai no vienas krājumu partijas.</span><span class="sxs-lookup"><span data-stu-id="549ae-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="549ae-106">Piemēram, debitors, kurš pasūta tapetes, var pieprasīt, lai viss pasūtījums tiktu izpildīts, izmantojot vienu partiju vai laidienu, lai izvairītos no neatbilstībām tapešu ruļļos.</span><span class="sxs-lookup"><span data-stu-id="549ae-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="549ae-107">Lai iestatītu to, ka precei tiks izmantota tās pašas partijas rezervēšana, precei piešķirtajai krājumu modeļu grupai, izsekošanas dimensiju grupai un noliktavas dimensiju grupai jābūt aktīviem šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="549ae-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="549ae-108">**Krājumu modeļu grupas** — krājumu modeļu grupai ir jābūt atlasītiem laukiem **Tās pašas partijas atlasīšana** un **Konsolidēt vajadzību** krājumu politiku lauku grupā **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="549ae-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="549ae-109">**Izsekošanas dimensiju grupas** — izsekošanas dimensiju grupai ir jāatlasa lauks **Vajadzības plāns pa dimensijām** partijas numuram.</span><span class="sxs-lookup"><span data-stu-id="549ae-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="549ae-110">**Noliktavas dimensiju grupas** — noliktavas dimensiju grupai vienumam **Vieta** un **Noliktava** jābūt atlasītam laukam **Vajadzības plāns pa dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="549ae-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="549ae-111">Ja rezervējat krājumus precei pārdošanas pasūtījuma rindā, kas ir iestatīta tās pašas partijas atlasei, sistēma mēģina rezervēt pasūtīto daudzumu no vienas krājumu partijas.</span><span class="sxs-lookup"><span data-stu-id="549ae-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="549ae-112">Tiek ņemtas vērā arī konkrētas partijas atribūta prasības.</span><span class="sxs-lookup"><span data-stu-id="549ae-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="549ae-113">Ja daudzumu nevar aizpildīt no vienas partijas, tiek parādīta lapa **Tās pašas partijas rezervēšanas konflikts**.</span><span class="sxs-lookup"><span data-stu-id="549ae-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="549ae-114">Šajā lapā ir aprakstītas problēmas, kā arī darbības, ko varat veikt, lai turpinātu rezervēšanu.</span><span class="sxs-lookup"><span data-stu-id="549ae-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="549ae-115">Partijas rezervēšanu var liegt šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="549ae-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="549ae-116">Partijas atgriešanas metodes kodam vienums **Bloķēt rezervāciju** pārdošanai ir atzīmēts kā **Bloķēts**.</span><span class="sxs-lookup"><span data-stu-id="549ae-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="549ae-117">Partijai ir beidzies derīguma termiņš, uz beigu datumu un attiecīgajām pārdošanas debitoriem dienām.</span><span class="sxs-lookup"><span data-stu-id="549ae-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="549ae-118">Krājums joprojām var būt derīgs rezervēšanai, ja attiecīgā krājuma gadījumā uz krājumu modeļu grupu attiecas datuma kontroles princips “pirmais beidzies, pirmais ārā” un ja kā izdošanas kritērijs ir atlasīts derīguma termiņa datums.</span><span class="sxs-lookup"><span data-stu-id="549ae-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="549ae-119">Partijas atlikušais glabāšanas laika dienu skaits nav pietiekams, pamatojoties uz beigu datumu un derīguma termiņa datumu, pie kura pieskaita pārdošanas debitoriem dienas.</span><span class="sxs-lookup"><span data-stu-id="549ae-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="549ae-120">Krājumiem, kas saistīti ar noliktavas dimensiju grupu, kurai ir iespējota opcija **Izmantot noliktavas vadības procesus**, varat rezervēt konkrētus partijas numurus, izmantojot rezervāciju hierarhiju ar partijas numura krājuma dimensiju, kas noteikta virs novietojuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="549ae-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="549ae-121">Lapa **Partijas rezervācija** pārsūtīšanas pasūtījuma rindām ļauj izvēlēties un rezervēt vairākas rindas, pamatojoties uz pieejamiem partijas numuriem.</span><span class="sxs-lookup"><span data-stu-id="549ae-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="549ae-122">Papildinformāciju par to, kā rīkoties, ja izmantojat rezervāciju hierarhiju, kurai ir partijas numura dimensija zem vietas, skatiet rakstā [Elastīga noliktavas līmeņa dimensiju rezervācijas politika](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="549ae-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>
