---
title: Personāla atlases pieprasījuma statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059188"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="aa2e2-103">Personāla atlases pieprasījuma statuss</span><span class="sxs-lookup"><span data-stu-id="aa2e2-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aa2e2-104">Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="aa2e2-105">Fiziskais nosaukums: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="aa2e2-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="aa2e2-106">Šis uzskaitījums sniedz vienuma RecruitingRequest statusa vērtību opciju kopu.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="aa2e2-107">Vērtība</span><span class="sxs-lookup"><span data-stu-id="aa2e2-107">Value</span></span> | <span data-ttu-id="aa2e2-108">Iezīme</span><span class="sxs-lookup"><span data-stu-id="aa2e2-108">Label</span></span> | <span data-ttu-id="aa2e2-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="aa2e2-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="aa2e2-110">200000000</span><span class="sxs-lookup"><span data-stu-id="aa2e2-110">200000000</span></span> | <span data-ttu-id="aa2e2-111">Melnraksts</span><span class="sxs-lookup"><span data-stu-id="aa2e2-111">Draft</span></span> | <span data-ttu-id="aa2e2-112">Pieprasījums ir melnrakstā un nav gatavs aktīvai personāla atlasei.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="aa2e2-113">200000001</span><span class="sxs-lookup"><span data-stu-id="aa2e2-113">200000001</span></span> | <span data-ttu-id="aa2e2-114">Pārskatīšanā</span><span class="sxs-lookup"><span data-stu-id="aa2e2-114">In Review</span></span> | <span data-ttu-id="aa2e2-115">Pieprasījums ir iesniegts un tiek maršrutēts apstiprināšanai ar darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="aa2e2-116">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="aa2e2-117">200000002</span><span class="sxs-lookup"><span data-stu-id="aa2e2-117">200000002</span></span> | <span data-ttu-id="aa2e2-118">Gaida</span><span class="sxs-lookup"><span data-stu-id="aa2e2-118">Pending</span></span> | <span data-ttu-id="aa2e2-119">Pieprasījums gaida darbplūsmas darbību.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-119">The request is pending workflow action.</span></span> <span data-ttu-id="aa2e2-120">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="aa2e2-121">200000003</span><span class="sxs-lookup"><span data-stu-id="aa2e2-121">200000003</span></span> | <span data-ttu-id="aa2e2-122">Atcelts</span><span class="sxs-lookup"><span data-stu-id="aa2e2-122">Canceled</span></span> | <span data-ttu-id="aa2e2-123">Pieprasījums ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-123">The request has been canceled.</span></span> <span data-ttu-id="aa2e2-124">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="aa2e2-125">200000004</span><span class="sxs-lookup"><span data-stu-id="aa2e2-125">200000004</span></span> | <span data-ttu-id="aa2e2-126">Liegts</span><span class="sxs-lookup"><span data-stu-id="aa2e2-126">Denied</span></span> | <span data-ttu-id="aa2e2-127">Pieprasījums ir noraidīts.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-127">The request has been denied.</span></span> <span data-ttu-id="aa2e2-128">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="aa2e2-129">200000005</span><span class="sxs-lookup"><span data-stu-id="aa2e2-129">200000005</span></span> | <span data-ttu-id="aa2e2-130">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="aa2e2-130">Active</span></span> | <span data-ttu-id="aa2e2-131">Darbplūsma tiek pabeigta un apstiprināta, un pieprasījums ir gatavs aktīvai personāla atlasei.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="aa2e2-132">200000006</span><span class="sxs-lookup"><span data-stu-id="aa2e2-132">200000006</span></span> | <span data-ttu-id="aa2e2-133">Slēgtas</span><span class="sxs-lookup"><span data-stu-id="aa2e2-133">Closed</span></span> | <span data-ttu-id="aa2e2-134">Personāla atlases pieprasījums ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="aa2e2-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="aa2e2-135">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="aa2e2-135">See also</span></span>

[<span data-ttu-id="aa2e2-136">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="aa2e2-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="aa2e2-137">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="aa2e2-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]