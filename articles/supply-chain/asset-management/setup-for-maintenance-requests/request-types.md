---
title: Uzturēšanas pieprasījumu veidi
description: Šajā tēmā izskaidrots, kā iestatīt uzturēšanas pieprasījumu veidus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ff80b2f3e23f46467b8a2fe7a2abd805e5e3a20
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808500"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="95eec-103">Uzturēšanas pieprasījumu veidi</span><span class="sxs-lookup"><span data-stu-id="95eec-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="95eec-104">Uzturēšanas pieprasījumu veidi tiek izmantoti, lai kategorizētu uzturēšanas pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="95eec-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="95eec-105">Piemēram, jums var būt uzturēšanas pieprasījumu veidi, kas saistīti ar profilaktisko uzturēšanu un koriģējošo uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="95eec-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="95eec-106">Vai arī jums var būt īpašs uzturēšanas pieprasījuma veids, ko izmanto, lai pārvaldītu līdzekļu labošanu (labošana noliktavā).</span><span class="sxs-lookup"><span data-stu-id="95eec-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="95eec-107">Uzturēšanas pieprasījuma veids definē piederību uzturēšanas pieprasījuma dzīves cikla stāvokļa grupai (uzturēšanas dzīves cikla modelis).</span><span class="sxs-lookup"><span data-stu-id="95eec-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="95eec-108">Uzturēšanas pieprasījuma dzīves cikla modeļi definē dzīves cikla stāvokļus, kuri var būt iestatīti uzturēšanas pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="95eec-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="95eec-109">(Uzturēšanas pieprasījuma dzīves cikla stāvokļi ietver **Izveidots**, **Aktīvs** un **Pabeigts**.)</span><span class="sxs-lookup"><span data-stu-id="95eec-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="95eec-110">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Uzturēšanas pieprasījumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="95eec-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="95eec-111">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="95eec-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="95eec-112">Laukā **Uzturēšanas pieprasījuma veids** ievadiet uzturēšanas pieprasījuma veida ID.</span><span class="sxs-lookup"><span data-stu-id="95eec-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="95eec-113">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="95eec-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="95eec-114">Kopsavilkuma cilnē **Vispārīgi** laukā **Uzturēšanas pieprasījuma dzīves cikla modelis** atlasiet uzturēšanas pieprasījuma dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="95eec-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="95eec-115">Laukā **Darba pasūtījuma veids** atlasiet darba pasūtījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="95eec-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="95eec-116">Kad uzturēšanas pieprasījums tiek pārvērsts par darba pasūtījumu, darba pasūtījums automātiski iegūst darba pasūtījuma veidu, kas ir saistīts ar uzturēšanas pieprasījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="95eec-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="95eec-117">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu veidi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="95eec-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Uzturēšanas pieprasījumu tipu lapa](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]