---
title: Personāla atlases pieprasījuma statuss
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125958"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="b6aa1-103">Personāla atlases pieprasījuma statuss</span><span class="sxs-lookup"><span data-stu-id="b6aa1-103">Recruiting request status</span></span>

<span data-ttu-id="b6aa1-104">Šajā tēmā aprakstīta personāla atlases pieprasījuma statusa opcija, kas iestatīta programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b6aa1-105">Fiziskais nosaukums: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="b6aa1-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="b6aa1-106">Šis uzskaitījums sniedz vienuma RecruitingRequest statusa vērtību opciju kopu.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="b6aa1-107">Vērtība</span><span class="sxs-lookup"><span data-stu-id="b6aa1-107">Value</span></span> | <span data-ttu-id="b6aa1-108">Iezīme</span><span class="sxs-lookup"><span data-stu-id="b6aa1-108">Label</span></span> | <span data-ttu-id="b6aa1-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b6aa1-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b6aa1-110">200000000</span><span class="sxs-lookup"><span data-stu-id="b6aa1-110">200000000</span></span> | <span data-ttu-id="b6aa1-111">Melnraksts</span><span class="sxs-lookup"><span data-stu-id="b6aa1-111">Draft</span></span> | <span data-ttu-id="b6aa1-112">Pieprasījums ir melnrakstā un nav gatavs aktīvai personāla atlasei.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="b6aa1-113">200000001</span><span class="sxs-lookup"><span data-stu-id="b6aa1-113">200000001</span></span> | <span data-ttu-id="b6aa1-114">Pārskatīšanā</span><span class="sxs-lookup"><span data-stu-id="b6aa1-114">In Review</span></span> | <span data-ttu-id="b6aa1-115">Pieprasījums ir iesniegts un tiek maršrutēts apstiprināšanai ar darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="b6aa1-116">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="b6aa1-117">200000002</span><span class="sxs-lookup"><span data-stu-id="b6aa1-117">200000002</span></span> | <span data-ttu-id="b6aa1-118">Gaida</span><span class="sxs-lookup"><span data-stu-id="b6aa1-118">Pending</span></span> | <span data-ttu-id="b6aa1-119">Pieprasījums gaida darbplūsmas darbību.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-119">The request is pending workflow action.</span></span> <span data-ttu-id="b6aa1-120">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="b6aa1-121">200000003</span><span class="sxs-lookup"><span data-stu-id="b6aa1-121">200000003</span></span> | <span data-ttu-id="b6aa1-122">Atcelts</span><span class="sxs-lookup"><span data-stu-id="b6aa1-122">Canceled</span></span> | <span data-ttu-id="b6aa1-123">Pieprasījums ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-123">The request has been canceled.</span></span> <span data-ttu-id="b6aa1-124">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="b6aa1-125">200000004</span><span class="sxs-lookup"><span data-stu-id="b6aa1-125">200000004</span></span> | <span data-ttu-id="b6aa1-126">Liegts</span><span class="sxs-lookup"><span data-stu-id="b6aa1-126">Denied</span></span> | <span data-ttu-id="b6aa1-127">Pieprasījums ir noraidīts.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-127">The request has been denied.</span></span> <span data-ttu-id="b6aa1-128">Pieejams tikai tad, ja darbplūsma ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="b6aa1-129">200000005</span><span class="sxs-lookup"><span data-stu-id="b6aa1-129">200000005</span></span> | <span data-ttu-id="b6aa1-130">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="b6aa1-130">Active</span></span> | <span data-ttu-id="b6aa1-131">Darbplūsma tiek pabeigta un apstiprināta, un pieprasījums ir gatavs aktīvai personāla atlasei.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="b6aa1-132">200000006</span><span class="sxs-lookup"><span data-stu-id="b6aa1-132">200000006</span></span> | <span data-ttu-id="b6aa1-133">Slēgtas</span><span class="sxs-lookup"><span data-stu-id="b6aa1-133">Closed</span></span> | <span data-ttu-id="b6aa1-134">Personāla atlases pieprasījums ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="b6aa1-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b6aa1-135">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="b6aa1-135">See also</span></span>

[<span data-ttu-id="b6aa1-136">Kandidāta izsekošanas sistēmas integrācijas API ievads</span><span class="sxs-lookup"><span data-stu-id="b6aa1-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b6aa1-137">Piemērs personāla atlases pieprasījuma vaicājumam</span><span class="sxs-lookup"><span data-stu-id="b6aa1-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
