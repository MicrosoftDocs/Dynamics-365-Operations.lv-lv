---
title: Personāla atlases pieprasījuma statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806046"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="e55dc-103">Personāla atlases pieprasījuma statuss</span><span class="sxs-lookup"><span data-stu-id="e55dc-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e55dc-104">Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e55dc-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e55dc-105">Fiziskais nosaukums: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="e55dc-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="e55dc-106">Šis uzskaitījums sniedz vienuma RecruitingRequest statusa vērtību opciju kopu.</span><span class="sxs-lookup"><span data-stu-id="e55dc-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="e55dc-107">Vērtība</span><span class="sxs-lookup"><span data-stu-id="e55dc-107">Value</span></span> | <span data-ttu-id="e55dc-108">Iezīme</span><span class="sxs-lookup"><span data-stu-id="e55dc-108">Label</span></span> | <span data-ttu-id="e55dc-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e55dc-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e55dc-110">200000000</span><span class="sxs-lookup"><span data-stu-id="e55dc-110">200000000</span></span> | <span data-ttu-id="e55dc-111">Melnraksts</span><span class="sxs-lookup"><span data-stu-id="e55dc-111">Draft</span></span> | <span data-ttu-id="e55dc-112">Pieprasījums ir melnrakstā un nav gatavs aktīvai personāla atlasei.</span><span class="sxs-lookup"><span data-stu-id="e55dc-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="e55dc-113">200000001</span><span class="sxs-lookup"><span data-stu-id="e55dc-113">200000001</span></span> | <span data-ttu-id="e55dc-114">Pārskatīšanā</span><span class="sxs-lookup"><span data-stu-id="e55dc-114">In Review</span></span> | <span data-ttu-id="e55dc-115">Pieprasījums ir iesniegts un tiek maršrutēts apstiprināšanai ar darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="e55dc-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="e55dc-116">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="e55dc-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e55dc-117">200000002</span><span class="sxs-lookup"><span data-stu-id="e55dc-117">200000002</span></span> | <span data-ttu-id="e55dc-118">Gaida</span><span class="sxs-lookup"><span data-stu-id="e55dc-118">Pending</span></span> | <span data-ttu-id="e55dc-119">Pieprasījums gaida darbplūsmas darbību.</span><span class="sxs-lookup"><span data-stu-id="e55dc-119">The request is pending workflow action.</span></span> <span data-ttu-id="e55dc-120">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="e55dc-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e55dc-121">200000003</span><span class="sxs-lookup"><span data-stu-id="e55dc-121">200000003</span></span> | <span data-ttu-id="e55dc-122">Atcelts</span><span class="sxs-lookup"><span data-stu-id="e55dc-122">Canceled</span></span> | <span data-ttu-id="e55dc-123">Pieprasījums ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="e55dc-123">The request has been canceled.</span></span> <span data-ttu-id="e55dc-124">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="e55dc-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e55dc-125">200000004</span><span class="sxs-lookup"><span data-stu-id="e55dc-125">200000004</span></span> | <span data-ttu-id="e55dc-126">Liegts</span><span class="sxs-lookup"><span data-stu-id="e55dc-126">Denied</span></span> | <span data-ttu-id="e55dc-127">Pieprasījums ir noraidīts.</span><span class="sxs-lookup"><span data-stu-id="e55dc-127">The request has been denied.</span></span> <span data-ttu-id="e55dc-128">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="e55dc-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e55dc-129">200000005</span><span class="sxs-lookup"><span data-stu-id="e55dc-129">200000005</span></span> | <span data-ttu-id="e55dc-130">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="e55dc-130">Active</span></span> | <span data-ttu-id="e55dc-131">Darbplūsma tiek pabeigta un apstiprināta, un pieprasījums ir gatavs aktīvai personāla atlasei.</span><span class="sxs-lookup"><span data-stu-id="e55dc-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="e55dc-132">200000006</span><span class="sxs-lookup"><span data-stu-id="e55dc-132">200000006</span></span> | <span data-ttu-id="e55dc-133">Slēgtas</span><span class="sxs-lookup"><span data-stu-id="e55dc-133">Closed</span></span> | <span data-ttu-id="e55dc-134">Personāla atlases pieprasījums ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="e55dc-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e55dc-135">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="e55dc-135">See also</span></span>

[<span data-ttu-id="e55dc-136">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="e55dc-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e55dc-137">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="e55dc-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]