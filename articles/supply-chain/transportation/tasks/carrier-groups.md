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
ms.openlocfilehash: 95517153dda06cecf8e57b1f9b080aa07966c111
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247266"
---
# <a name="carrier-groups"></a><span data-ttu-id="7b45d-103">Pārvadātāju grupas</span><span class="sxs-lookup"><span data-stu-id="7b45d-103">Carrier groups</span></span>

<span data-ttu-id="7b45d-104">Pārvadātāju grupa ir nosūtījuma pārvadātāju un pārvadātāju pakalpojumu kolekcija.</span><span class="sxs-lookup"><span data-stu-id="7b45d-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="7b45d-105">Katra pārvadātāju grupa norāda tai piederošo nosūtījuma pārvadātāju un pārvadātāja pakalpojumu vēlamo secību.</span><span class="sxs-lookup"><span data-stu-id="7b45d-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="7b45d-106">Ja vienam maršruta segmentam ir vairāki nosūtījuma pārvadātāji un pārvadātāja pakalpojumi, maršruta plānā vai maršruta ceļvedī varat norādīt pārvadātāju grupu, nevis noteiktu nosūtījuma pārvadātāju un pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="7b45d-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="7b45d-107">Pārvadātāju grupas izveide</span><span class="sxs-lookup"><span data-stu-id="7b45d-107">Create a carrier group</span></span>

1. <span data-ttu-id="7b45d-108">Dodieties uz **Transportēšanas pārvaldība &gt; Iestatījumi &gt; Pārvadātāji &gt; Pārvadātāju grupa**.</span><span class="sxs-lookup"><span data-stu-id="7b45d-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="7b45d-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7b45d-109">Select **New**.</span></span>
1. <span data-ttu-id="7b45d-110">Laukā **Pārvadātāju grupa** ievadiet grupas unikālu identifikatoru (ID).</span><span class="sxs-lookup"><span data-stu-id="7b45d-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="7b45d-111">Laukā **Nosaukums** ievadiet aprakstošu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7b45d-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="7b45d-112">Kopsavilkuma cilnē **Detalizēta informācija** pievienojiet rindu un atlasiet nosūtīšanas pārvadātāju un pārvadātāja pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="7b45d-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="7b45d-113">Atkārtojiet šo darbību, līdz esat pievienojis tik daudzus pārvadātājus, cik nepieciešams šai grupai.</span><span class="sxs-lookup"><span data-stu-id="7b45d-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="7b45d-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7b45d-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]