---
title: Pārvadātāju grupas
description: Šajā tēmā ir aprakstīts, kā iestatīt datus pārvadātāju grupām.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646414"
---
# <a name="carrier-groups"></a><span data-ttu-id="88fa5-103">Pārvadātāju grupas</span><span class="sxs-lookup"><span data-stu-id="88fa5-103">Carrier groups</span></span>

<span data-ttu-id="88fa5-104">Pārvadātāju grupa ir nosūtījuma pārvadātāju un pārvadātāju pakalpojumu kolekcija.</span><span class="sxs-lookup"><span data-stu-id="88fa5-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="88fa5-105">Katra pārvadātāju grupa norāda tai piederošo nosūtījuma pārvadātāju un pārvadātāja pakalpojumu vēlamo secību.</span><span class="sxs-lookup"><span data-stu-id="88fa5-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="88fa5-106">Ja vienam maršruta segmentam ir vairāki nosūtījuma pārvadātāji un pārvadātāja pakalpojumi, maršruta plānā vai maršruta ceļvedī varat norādīt pārvadātāju grupu, nevis noteiktu nosūtījuma pārvadātāju un pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="88fa5-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="88fa5-107">Pārvadātāju grupas izveide</span><span class="sxs-lookup"><span data-stu-id="88fa5-107">Create a carrier group</span></span>

1. <span data-ttu-id="88fa5-108">Dodieties uz **Transportēšanas pārvaldība &gt; Iestatījumi &gt; Pārvadātāji &gt; Pārvadātāju grupa**.</span><span class="sxs-lookup"><span data-stu-id="88fa5-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="88fa5-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="88fa5-109">Select **New**.</span></span>
1. <span data-ttu-id="88fa5-110">Laukā **Pārvadātāju grupa** ievadiet grupas unikālu identifikatoru (ID).</span><span class="sxs-lookup"><span data-stu-id="88fa5-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="88fa5-111">Laukā **Nosaukums** ievadiet aprakstošu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="88fa5-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="88fa5-112">Kopsavilkuma cilnē **Detalizēta informācija** pievienojiet rindu un atlasiet nosūtīšanas pārvadātāju un pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="88fa5-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="88fa5-113">Atkārtojiet šo darbību, līdz esat pievienojis tik daudzus pārvadātājus, cik nepieciešams šai grupai.</span><span class="sxs-lookup"><span data-stu-id="88fa5-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="88fa5-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="88fa5-114">Close the page.</span></span>
