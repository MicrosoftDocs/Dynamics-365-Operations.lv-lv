---
title: Reisa statusa iestatījumi
description: Šajā tēmā ir aprakstīts, kā izveidot statusa vērtības, ko lietotāji var piešķirt reisiem.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500890"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="77d47-103">Reisa statusa iestatījumi</span><span class="sxs-lookup"><span data-stu-id="77d47-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="77d47-104">Lapā **Reisu statusi** izveidojiet statusa vērtību kopu, ko lietotāji var piešķirt reisiem.</span><span class="sxs-lookup"><span data-stu-id="77d47-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="77d47-105">Lietotāji var piešķirt reisa statusa vērtības visiem reisa līmeņiem: reisa, nosūtīšanas konteinera, folio, pirkšanas pasūtījuma un krājuma (pirkšanas rindas un pārsūtīšanas pasūtījuma rindas).</span><span class="sxs-lookup"><span data-stu-id="77d47-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="77d47-106">Tos lieto diviem nolūkiem:</span><span class="sxs-lookup"><span data-stu-id="77d47-106">They are used for two purposes:</span></span>

- <span data-ttu-id="77d47-107">Informēt lietotāju par reisa, pārvadāšanas konteinera, folio, pirkšanas pasūtījuma vai krājuma statusu (pirkšanas rindas un pārsūtīšanas pasūtījuma rindas).</span><span class="sxs-lookup"><span data-stu-id="77d47-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="77d47-108">Ierobežojiet izmaksu zonas izmantošanu, novēršot modificēšanu vai dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="77d47-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="77d47-109">Lai iestatītu reisa statusus, dodieties uz **Kopējās izmaksas \> Iestatījumi \> Reisa statusi**.</span><span class="sxs-lookup"><span data-stu-id="77d47-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="77d47-110">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu statusus.</span><span class="sxs-lookup"><span data-stu-id="77d47-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="77d47-111">Katrai izmaksu zonai ir sava reisa statusu kopa un hierarhija.</span><span class="sxs-lookup"><span data-stu-id="77d47-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="77d47-112">Tādēļ **Reisa statusu** lapas **Izmaksu apgabala** laukā vispirms ir jāatlasa izmaksu zona, kurai vēlaties skatīt vai izveidot reisu statusus.</span><span class="sxs-lookup"><span data-stu-id="77d47-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="77d47-113">Pēc tam katram reisa statusam iestatiet tālāk sniegtajā tabulā aprakstītos laukus, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="77d47-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="77d47-114">Ņemiet vērā, ka reisa statusu var automātiski mainīt arī sistēmas notikumi, piemēram, noteikumi, kas izveidoti, izmantojot izsekošanas kontroles centru.</span><span class="sxs-lookup"><span data-stu-id="77d47-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="77d47-115">Lauks</span><span class="sxs-lookup"><span data-stu-id="77d47-115">Field</span></span> | <span data-ttu-id="77d47-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="77d47-116">Description</span></span> |
|---|---|
| <span data-ttu-id="77d47-117">Reisa statuss</span><span class="sxs-lookup"><span data-stu-id="77d47-117">Voyage status</span></span> | <span data-ttu-id="77d47-118">Ievadiet reisa statusa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="77d47-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="77d47-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="77d47-119">Description</span></span> | <span data-ttu-id="77d47-120">Ievadiet reisa statusa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="77d47-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="77d47-121">Modificē</span><span class="sxs-lookup"><span data-stu-id="77d47-121">Modify</span></span> | <span data-ttu-id="77d47-122">Atzīmējiet šo izvēles rūtiņu, ja lietotājiem ir atļauts modificēt reisus ar šo statusu.</span><span class="sxs-lookup"><span data-stu-id="77d47-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="77d47-123">Delete</span><span class="sxs-lookup"><span data-stu-id="77d47-123">Delete</span></span> | <span data-ttu-id="77d47-124">Atzīmējiet šo izvēles rūtiņu, ja lietotājiem ir atļauts dzēst reisus ar šo statusu.</span><span class="sxs-lookup"><span data-stu-id="77d47-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="77d47-125">Obligāts</span><span class="sxs-lookup"><span data-stu-id="77d47-125">Mandatory</span></span> | <span data-ttu-id="77d47-126">Atzīmējiet šo izvēles rūtiņu, lai padarītu reisa statusu par obligātu, lai to nevar izlaist.</span><span class="sxs-lookup"><span data-stu-id="77d47-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="77d47-127">Pamatelements</span><span class="sxs-lookup"><span data-stu-id="77d47-127">Parent</span></span> | <span data-ttu-id="77d47-128">Lietojiet šo lauku, lai izveidotu hierarhiju starp statusa vērtībām.</span><span class="sxs-lookup"><span data-stu-id="77d47-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="77d47-129">Reisu statusus (manuāli vai automātiski) hierarhijā var mainīt tikai uz leju no pamatobjekta statusa uz vienu no tā bērnu statusiem.</span><span class="sxs-lookup"><span data-stu-id="77d47-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="77d47-130">Jāiestata tikai konkrēti reisa statusi, ko izmanto jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="77d47-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="77d47-131">Tipiski reisu statusi ietver *Apstiprināts*, *Tranzīta preces*, *Saņemts*, *Gatavs izmaksu skaitīšanai* un *Izmaksas*.</span><span class="sxs-lookup"><span data-stu-id="77d47-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="77d47-132">Tomēr, iespējams, ir citi statusi.</span><span class="sxs-lookup"><span data-stu-id="77d47-132">However, other statuses might be present.</span></span>
