---
title: Uzturēšanas pieprasījumu veidi
description: Šajā tēmā izskaidrots, kā iestatīt uzturēšanas pieprasījumu veidus Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 430e475b52638dd80512ffd79d42aac6f5f340e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571143"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="bb1aa-103">Uzturēšanas pieprasījumu veidi</span><span class="sxs-lookup"><span data-stu-id="bb1aa-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="bb1aa-104">Uzturēšanas pieprasījumu veidi tiek izmantoti, lai kategorizētu uzturēšanas pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="bb1aa-105">Piemēram, jums var būt uzturēšanas pieprasījumu veidi, kas saistīti ar profilaktisko uzturēšanu un koriģējošo uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="bb1aa-106">Vai arī jums var būt īpašs uzturēšanas pieprasījuma veids, ko izmanto, lai pārvaldītu līdzekļu labošanu (labošana noliktavā).</span><span class="sxs-lookup"><span data-stu-id="bb1aa-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="bb1aa-107">Uzturēšanas pieprasījuma veids definē piederību uzturēšanas pieprasījuma dzīves cikla stāvokļa grupai (uzturēšanas dzīves cikla modelis).</span><span class="sxs-lookup"><span data-stu-id="bb1aa-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="bb1aa-108">Uzturēšanas pieprasījuma dzīves cikla modeļi definē dzīves cikla stāvokļus, kuri var būt iestatīti uzturēšanas pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="bb1aa-109">(Uzturēšanas pieprasījuma dzīves cikla stāvokļi ietver **Izveidots**, **Aktīvs** un **Pabeigts**.)</span><span class="sxs-lookup"><span data-stu-id="bb1aa-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="bb1aa-110">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Uzturēšanas pieprasījumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="bb1aa-111">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="bb1aa-112">Laukā **Uzturēšanas pieprasījuma veids** ievadiet uzturēšanas pieprasījuma veida ID.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="bb1aa-113">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="bb1aa-114">Kopsavilkuma cilnē **Vispārīgi** laukā **Uzturēšanas pieprasījuma dzīves cikla modelis** atlasiet uzturēšanas pieprasījuma dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="bb1aa-115">Laukā **Darba pasūtījuma veids** atlasiet darba pasūtījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="bb1aa-116">Kad uzturēšanas pieprasījums tiek pārvērsts par darba pasūtījumu, darba pasūtījums automātiski iegūst darba pasūtījuma veidu, kas ir saistīts ar uzturēšanas pieprasījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="bb1aa-117">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu veidi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Uzturēšanas pieprasījumu tipu lapa](media/07-setup-for-requests.png)
