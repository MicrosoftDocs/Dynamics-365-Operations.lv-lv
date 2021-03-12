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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 14a2f4c7d8d053ffd7b4b5d090113e1d9c3294c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974114"
---
# <a name="carrier-groups"></a><span data-ttu-id="ac449-103">Pārvadātāju grupas</span><span class="sxs-lookup"><span data-stu-id="ac449-103">Carrier groups</span></span>

<span data-ttu-id="ac449-104">Pārvadātāju grupa ir nosūtījuma pārvadātāju un pārvadātāju pakalpojumu kolekcija.</span><span class="sxs-lookup"><span data-stu-id="ac449-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="ac449-105">Katra pārvadātāju grupa norāda tai piederošo nosūtījuma pārvadātāju un pārvadātāja pakalpojumu vēlamo secību.</span><span class="sxs-lookup"><span data-stu-id="ac449-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="ac449-106">Ja vienam maršruta segmentam ir vairāki nosūtījuma pārvadātāji un pārvadātāja pakalpojumi, maršruta plānā vai maršruta ceļvedī varat norādīt pārvadātāju grupu, nevis noteiktu nosūtījuma pārvadātāju un pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="ac449-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="ac449-107">Pārvadātāju grupas izveide</span><span class="sxs-lookup"><span data-stu-id="ac449-107">Create a carrier group</span></span>

1. <span data-ttu-id="ac449-108">Dodieties uz **Transportēšanas pārvaldība &gt; Iestatījumi &gt; Pārvadātāji &gt; Pārvadātāju grupa**.</span><span class="sxs-lookup"><span data-stu-id="ac449-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="ac449-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ac449-109">Select **New**.</span></span>
1. <span data-ttu-id="ac449-110">Laukā **Pārvadātāju grupa** ievadiet grupas unikālu identifikatoru (ID).</span><span class="sxs-lookup"><span data-stu-id="ac449-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="ac449-111">Laukā **Nosaukums** ievadiet aprakstošu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ac449-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="ac449-112">Kopsavilkuma cilnē **Detalizēta informācija** pievienojiet rindu un atlasiet nosūtīšanas pārvadātāju un pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="ac449-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="ac449-113">Atkārtojiet šo darbību, līdz esat pievienojis tik daudzus pārvadātājus, cik nepieciešams šai grupai.</span><span class="sxs-lookup"><span data-stu-id="ac449-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="ac449-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ac449-114">Close the page.</span></span>
