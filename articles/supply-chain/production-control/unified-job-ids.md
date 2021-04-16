---
title: Vienota darbu ID numuru secība
description: Šī funkcija nodrošina vienu unificētu numuru sēriju, kas ģenerē ražošanas kontroles, ražošanas izpildes, laika un apmeklētības moduļu darbu ID numurus.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824946"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="3b395-103">Vienota darbu ID numuru secība</span><span class="sxs-lookup"><span data-stu-id="3b395-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b395-104">Šī funkcija nodrošina vienu unificētu numuru sēriju, kas ģenerē ražošanas kontroles, ražošanas izpildes, laika un apmeklētības moduļu darbu ID numurus.</span><span class="sxs-lookup"><span data-stu-id="3b395-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="3b395-105">Iepriekš var izvēlēties atšķirīgu numuru sēriju katram no šiem moduļiem, kas var izraisīt konfliktējošus darba ID numurus, ja divas vai vairākas šīs sērijas izmantoja identisku formātu.</span><span class="sxs-lookup"><span data-stu-id="3b395-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="3b395-106">Šāds konflikts var izraisīt datu bojāšanu.</span><span class="sxs-lookup"><span data-stu-id="3b395-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="3b395-107">Līdzekļa ieslēgšana sistēmā</span><span class="sxs-lookup"><span data-stu-id="3b395-107">Turn on this feature for your system</span></span>

<span data-ttu-id="3b395-108">Ja sistēmā vēl nav ietverti šajā tēmā aprakstītie līdzekļi, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet līdzekli *Krājumu darbību arhīvs*.</span><span class="sxs-lookup"><span data-stu-id="3b395-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="3b395-109">Vienota darbu ID numuru secības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3b395-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="3b395-110">Pēc šīs funkcijas iespējošanas esošie **Darba identifikācijas** numuru sērijas iestatījumi, kas atrodas ražošanas kontroles, ražošanas izpildes un laika un apmeklētības moduļu parametru lapās, tiks noņemti un tiks pievienots jauns **Unificētais darba ID** lauks.</span><span class="sxs-lookup"><span data-stu-id="3b395-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="3b395-111">**Unificētā darba ID** vērtība tiek koplietota ar visiem trim moduļiem, tādējādi nodrošinot, ka visi moduļi atsaucas uz vienu un to pašu numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="3b395-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="3b395-112">Tāpēc darba ID būs unikāls visos trīs moduļos, un konflikts nekad nebūs.</span><span class="sxs-lookup"><span data-stu-id="3b395-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="3b395-113">Vienota darbu ID numuru secības iestatīšana:</span><span class="sxs-lookup"><span data-stu-id="3b395-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="3b395-114">Iespējojiet funkciju tā, kā tas ir aprakstīts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="3b395-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="3b395-115">Vai nu identificējiet numuru secību, ko vēlaties izmantot saviem vienotajam darba ID, vai izveidojiet jaunu.</span><span class="sxs-lookup"><span data-stu-id="3b395-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="3b395-116">Plašāku informāciju par numuru secību skatiet [Numuru sērijas pārskats](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3b395-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="3b395-117">Pārejiet uz lapu **Ražošanas kontroles parametri**, **Ražošanas izpildes parametri** vai **Laika un apmeklējuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="3b395-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="3b395-118">Nav svarīgi, kuru vēlaties, jo, veicot šo iestatījumu jebkurā no šīm lapām, visas pārējās lapas tiks atjauninātas automātiski.</span><span class="sxs-lookup"><span data-stu-id="3b395-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="3b395-119">Atveriet cilni **Numuru sērijas** atlasītajā parametru lapā.</span><span class="sxs-lookup"><span data-stu-id="3b395-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="3b395-120">Piešķiriet **Numuru sērijas kodu**, kuru iepriekš identificējāt **Unificētā darba ID** režģa rindai.</span><span class="sxs-lookup"><span data-stu-id="3b395-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
