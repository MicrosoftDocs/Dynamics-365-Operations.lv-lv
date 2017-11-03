---
title: "Tās pašas partijas rezervēšana pārdošanas pasūtījumam"
description: "Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aef3a52f4cb2d5af47a8c25a67e6c2076fa1ff03
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="ba5f2-103">Tās pašas partijas rezervēšana pārdošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="ba5f2-103">Reserve the same batch for a sales order</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ba5f2-104">Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="ba5f2-105">Tās pašas partijas rezervēšana ļauj rezervēt krājumus pārdošanas pasūtījuma rindai no vienas krājumu partijas.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="ba5f2-106">Piemēram, debitors, kurš pasūta tapetes, var pieprasīt, lai viss pasūtījums tiktu izpildīts, izmantojot vienu partiju vai laidienu, lai izvairītos no neatbilstībām tapešu ruļļos.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="ba5f2-107">Lai iestatītu to, ka precei tiks izmantota tās pašas partijas rezervēšana, precei piešķirtajai krājumu modeļu grupai, izsekošanas dimensiju grupai un noliktavas dimensiju grupai jābūt aktīviem šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="ba5f2-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="ba5f2-108">**Krājumu modeļu grupas** — krājumu modeļu grupai ir jābūt atlasītiem laukiem **Tās pašas partijas atlasīšana** un **Konsolidēt vajadzību** krājumu politiku lauku grupā **Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="ba5f2-109">**Izsekošanas dimensiju grupas** — izsekošanas dimensiju grupai ir jāatlasa lauks **Vajadzības plāns pa dimensijām** partijas numuram.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="ba5f2-110">**Noliktavas dimensiju grupas** — noliktavas dimensiju grupai vienumam **Vieta** un **Noliktava** jābūt atlasītam laukam **Vajadzības plāns pa dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="ba5f2-111">Rezervējot krājumus precei pārdošanas pasūtījuma rindā, kurai ir iestatīta tās pašas partijas atlasīšana, programma Microsoft Dynamics 365 for Finance and Operations mēģina rezervēt pasūtīto daudzumu no vienas krājumu partijas.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="ba5f2-112">Tiek ņemtas vērā arī konkrētas partijas atribūta prasības.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="ba5f2-113">Ja daudzumu nevar aizpildīt no vienas partijas, tiek parādīta lapa **Tās pašas partijas rezervēšanas konflikts**.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="ba5f2-114">Šajā lapā ir aprakstītas problēmas, kā arī darbības, ko varat veikt, lai turpinātu rezervēšanu.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="ba5f2-115">Partijas rezervēšanu var liegt šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="ba5f2-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="ba5f2-116">Partijas atgriešanas metodes kodam vienums **Bloķēt rezervāciju** pārdošanai ir atzīmēts kā **Bloķēts**.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="ba5f2-117">Partijai ir beidzies derīguma termiņš, uz beigu datumu un attiecīgajām pārdošanas debitoriem dienām.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="ba5f2-118">Krājums joprojām var būt derīgs rezervēšanai, ja attiecīgā krājuma gadījumā uz krājumu modeļu grupu attiecas datuma kontroles princips “pirmais beidzies, pirmais ārā” un ja kā izdošanas kritērijs ir atlasīts derīguma termiņa datums.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="ba5f2-119">Partijas atlikušais glabāšanas laika dienu skaits nav pietiekams, pamatojoties uz beigu datumu un derīguma termiņa datumu, pie kura pieskaita pārdošanas debitoriem dienas.</span><span class="sxs-lookup"><span data-stu-id="ba5f2-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





