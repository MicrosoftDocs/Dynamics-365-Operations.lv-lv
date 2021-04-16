---
title: Reisa statusa iestatījumi
description: Šajā tēmā ir aprakstīts, kā izveidot statusa vērtības, ko lietotāji var piešķirt reisiem.
author: sherry-zheng
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
ms.openlocfilehash: 80433c17ed9d790d88b20ecc253c8e4459ffea10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829792"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="fddad-103">Reisa statusa iestatījumi</span><span class="sxs-lookup"><span data-stu-id="fddad-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fddad-104">Lapā **Reisu statusi** izveidojiet statusa vērtību kopu, ko lietotāji var piešķirt reisiem.</span><span class="sxs-lookup"><span data-stu-id="fddad-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="fddad-105">Lietotāji var piešķirt reisa statusa vērtības visiem reisa līmeņiem: reisa, nosūtīšanas konteinera, folio, pirkšanas pasūtījuma un krājuma (pirkšanas rindas un pārsūtīšanas pasūtījuma rindas).</span><span class="sxs-lookup"><span data-stu-id="fddad-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="fddad-106">Tos lieto diviem nolūkiem:</span><span class="sxs-lookup"><span data-stu-id="fddad-106">They are used for two purposes:</span></span>

- <span data-ttu-id="fddad-107">Informēt lietotāju par reisa, pārvadāšanas konteinera, folio, pirkšanas pasūtījuma vai krājuma statusu (pirkšanas rindas un pārsūtīšanas pasūtījuma rindas).</span><span class="sxs-lookup"><span data-stu-id="fddad-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="fddad-108">Ierobežojiet izmaksu zonas izmantošanu, novēršot modificēšanu vai dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="fddad-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="fddad-109">Lai iestatītu reisa statusus, dodieties uz **Kopējās izmaksas \> Iestatījumi \> Reisa statusi**.</span><span class="sxs-lookup"><span data-stu-id="fddad-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="fddad-110">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu statusus.</span><span class="sxs-lookup"><span data-stu-id="fddad-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="fddad-111">Katrai izmaksu zonai ir sava reisa statusu kopa un hierarhija.</span><span class="sxs-lookup"><span data-stu-id="fddad-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="fddad-112">Tādēļ **Reisa statusu** lapas **Izmaksu apgabala** laukā vispirms ir jāatlasa izmaksu zona, kurai vēlaties skatīt vai izveidot reisu statusus.</span><span class="sxs-lookup"><span data-stu-id="fddad-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="fddad-113">Pēc tam katram reisa statusam iestatiet tālāk sniegtajā tabulā aprakstītos laukus, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="fddad-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="fddad-114">Ņemiet vērā, ka reisa statusu var automātiski mainīt arī sistēmas notikumi, piemēram, noteikumi, kas izveidoti, izmantojot izsekošanas kontroles centru.</span><span class="sxs-lookup"><span data-stu-id="fddad-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="fddad-115">Lauks</span><span class="sxs-lookup"><span data-stu-id="fddad-115">Field</span></span> | <span data-ttu-id="fddad-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fddad-116">Description</span></span> |
|---|---|
| <span data-ttu-id="fddad-117">Reisa statuss</span><span class="sxs-lookup"><span data-stu-id="fddad-117">Voyage status</span></span> | <span data-ttu-id="fddad-118">Ievadiet reisa statusa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="fddad-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="fddad-119">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fddad-119">Description</span></span> | <span data-ttu-id="fddad-120">Ievadiet reisa statusa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="fddad-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="fddad-121">Modificē</span><span class="sxs-lookup"><span data-stu-id="fddad-121">Modify</span></span> | <span data-ttu-id="fddad-122">Atzīmējiet šo izvēles rūtiņu, ja lietotājiem ir atļauts modificēt reisus ar šo statusu.</span><span class="sxs-lookup"><span data-stu-id="fddad-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="fddad-123">Delete</span><span class="sxs-lookup"><span data-stu-id="fddad-123">Delete</span></span> | <span data-ttu-id="fddad-124">Atzīmējiet šo izvēles rūtiņu, ja lietotājiem ir atļauts dzēst reisus ar šo statusu.</span><span class="sxs-lookup"><span data-stu-id="fddad-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="fddad-125">Obligāts</span><span class="sxs-lookup"><span data-stu-id="fddad-125">Mandatory</span></span> | <span data-ttu-id="fddad-126">Atzīmējiet šo izvēles rūtiņu, lai padarītu reisa statusu par obligātu, lai to nevar izlaist.</span><span class="sxs-lookup"><span data-stu-id="fddad-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="fddad-127">Pamatelements</span><span class="sxs-lookup"><span data-stu-id="fddad-127">Parent</span></span> | <span data-ttu-id="fddad-128">Lietojiet šo lauku, lai izveidotu hierarhiju starp statusa vērtībām.</span><span class="sxs-lookup"><span data-stu-id="fddad-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="fddad-129">Reisu statusus (manuāli vai automātiski) hierarhijā var mainīt tikai uz leju no pamatobjekta statusa uz vienu no tā bērnu statusiem.</span><span class="sxs-lookup"><span data-stu-id="fddad-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="fddad-130">Jāiestata tikai konkrēti reisa statusi, ko izmanto jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="fddad-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="fddad-131">Tipiski reisu statusi ietver *Apstiprināts*, *Tranzīta preces*, *Saņemts*, *Gatavs izmaksu skaitīšanai* un *Izmaksas*.</span><span class="sxs-lookup"><span data-stu-id="fddad-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="fddad-132">Tomēr, iespējams, ir citi statusi.</span><span class="sxs-lookup"><span data-stu-id="fddad-132">However, other statuses might be present.</span></span>
