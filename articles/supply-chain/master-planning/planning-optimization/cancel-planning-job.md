---
title: Atcelt plānošanas darbu
description: Šajā tēmā izskaidrots, kā atcelt aktīvu plānošanas darbu, kas izmanto funkcionalitāti Plānošanas optimizācija.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774008"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="36fb9-103">Atcelt plānošanas darbu</span><span class="sxs-lookup"><span data-stu-id="36fb9-103">Cancel a planning job</span></span>

<span data-ttu-id="36fb9-104">Programmā Microsoft Dynamics 365 Supply Chain Management varat atcelt aktīvu plānošanas darbu, kas izmanto funkcionalitāti Plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="36fb9-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="36fb9-105">Lai atceltu aktīvu plānošanas darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="36fb9-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="36fb9-106">Atcelt var tikai aktīvus darbus.</span><span class="sxs-lookup"><span data-stu-id="36fb9-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="36fb9-107">Pārejiet uz **Vispārējā plānošana \> Iestatīšana \> Plāni**.</span><span class="sxs-lookup"><span data-stu-id="36fb9-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="36fb9-108">Atlasiet atbilstošu plānu izpildes plānošanai.</span><span class="sxs-lookup"><span data-stu-id="36fb9-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="36fb9-109">Atlasiet **Vēsture**.</span><span class="sxs-lookup"><span data-stu-id="36fb9-109">Select **History**.</span></span>
4. <span data-ttu-id="36fb9-110">Atlasīt plānošanas darbu, kuru atcelt.</span><span class="sxs-lookup"><span data-stu-id="36fb9-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="36fb9-111">Atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="36fb9-111">Select **Cancel**.</span></span>

<span data-ttu-id="36fb9-112">Darba statuss būs **Atcelšana**, līdz pakalpojums Plānošanas optimizācija apstiprinās, ka darbs ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="36fb9-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="36fb9-113">Pēc tam statuss tiks mainīts uz **Atcelts**.</span><span class="sxs-lookup"><span data-stu-id="36fb9-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="36fb9-114">Lai skatītu statusa izmaiņas, ir jāatsvaidzina lapa, atlasot pogu **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="36fb9-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="36fb9-115">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="36fb9-115">Related resources</span></span>

[<span data-ttu-id="36fb9-116">Plānošanas optimizācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="36fb9-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="36fb9-117">Darba sākšana ar Plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="36fb9-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="36fb9-118">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="36fb9-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="36fb9-119">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="36fb9-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="36fb9-120">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="36fb9-120">Apply filters to a plan</span></span>](plan-filters.md)
