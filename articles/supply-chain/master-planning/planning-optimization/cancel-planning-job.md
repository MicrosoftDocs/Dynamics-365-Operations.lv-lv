---
title: Plānošanas darba atcelšana
description: Šajā tēmā izskaidrots, kā atcelt aktīvu plānošanas darbu, kas izmanto funkcionalitāti Plānošanas optimizācija.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 5aadf7fb94bb2d836892064837f9cb1c5790d657
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238018"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="e3347-103">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="e3347-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3347-104">Programmā Microsoft Dynamics 365 Supply Chain Management varat atcelt aktīvu plānošanas darbu, kas izmanto funkcionalitāti Plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="e3347-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="e3347-105">Atlasot opciju **Atcelt** dialoglodziņā, kad plānošanas optimizācijas darbs tiek parādīts tieši no lietotāja interfeisa (nevis fonā), tas neatcels plānošanas optimizācijas darbu.</span><span class="sxs-lookup"><span data-stu-id="e3347-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="e3347-106">Pat ja saņemat brīdinājumu, piemēram, "Operācija atcelta", jums joprojām būs jāveic šīs darbības, lai atceltu plānošanas darbu ar plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="e3347-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="e3347-107">Lai atceltu aktīvu plānošanas darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e3347-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="e3347-108">Atcelt var tikai aktīvus darbus.</span><span class="sxs-lookup"><span data-stu-id="e3347-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="e3347-109">Pārejiet uz **Vispārējā plānošana \> Iestatīšana \> Plāni**.</span><span class="sxs-lookup"><span data-stu-id="e3347-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="e3347-110">Atlasiet atbilstošu plānu izpildes plānošanai.</span><span class="sxs-lookup"><span data-stu-id="e3347-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="e3347-111">Atlasiet **Vēsture**.</span><span class="sxs-lookup"><span data-stu-id="e3347-111">Select **History**.</span></span>
4. <span data-ttu-id="e3347-112">Atlasīt plānošanas darbu, kuru atcelt.</span><span class="sxs-lookup"><span data-stu-id="e3347-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="e3347-113">Atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="e3347-113">Select **Cancel**.</span></span>

<span data-ttu-id="e3347-114">Darba statuss būs **Atcelšana**, līdz pakalpojums Plānošanas optimizācija apstiprinās, ka darbs ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="e3347-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="e3347-115">Pēc tam statuss tiks mainīts uz **Atcelts**.</span><span class="sxs-lookup"><span data-stu-id="e3347-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="e3347-116">Lai skatītu statusa izmaiņas, ir jāatsvaidzina lapa, atlasot pogu **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="e3347-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3347-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e3347-117">Additional resources</span></span>

[<span data-ttu-id="e3347-118">Plānošanas optimizācijas apskats</span><span class="sxs-lookup"><span data-stu-id="e3347-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e3347-119">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="e3347-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="e3347-120">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="e3347-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e3347-121">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="e3347-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e3347-122">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="e3347-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]