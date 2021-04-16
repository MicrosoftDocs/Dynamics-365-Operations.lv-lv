---
title: MyLeaveRequests pārskats
description: MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803637"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="b8a8e-103">MyLeaveRequests pārskats</span><span class="sxs-lookup"><span data-stu-id="b8a8e-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b8a8e-104">MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.</span><span class="sxs-lookup"><span data-stu-id="b8a8e-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="b8a8e-105">Taustiņš</span><span class="sxs-lookup"><span data-stu-id="b8a8e-105">Key</span></span>

  | <span data-ttu-id="b8a8e-106">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-106">Property Name</span></span> | <span data-ttu-id="b8a8e-107">Datu veids</span><span class="sxs-lookup"><span data-stu-id="b8a8e-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="b8a8e-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="b8a8e-108">dataAreaId</span></span>    | <span data-ttu-id="b8a8e-109">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-109">String</span></span>    |
  | <span data-ttu-id="b8a8e-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="b8a8e-110">RequestId</span></span>     | <span data-ttu-id="b8a8e-111">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-111">String</span></span>    |
  | <span data-ttu-id="b8a8e-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="b8a8e-112">LeaveType</span></span>     | <span data-ttu-id="b8a8e-113">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-113">String</span></span>    |
  | <span data-ttu-id="b8a8e-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="b8a8e-114">LeaveDate</span></span>     | <span data-ttu-id="b8a8e-115">Datums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="b8a8e-116">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="b8a8e-116">Properties</span></span>

  | <span data-ttu-id="b8a8e-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-117">Property Name</span></span>     | <span data-ttu-id="b8a8e-118">Datu veids</span><span class="sxs-lookup"><span data-stu-id="b8a8e-118">Data Type</span></span> | <span data-ttu-id="b8a8e-119">Pieprasīts</span><span class="sxs-lookup"><span data-stu-id="b8a8e-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="b8a8e-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="b8a8e-120">dataAreaId</span></span>        | <span data-ttu-id="b8a8e-121">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-121">String</span></span>    | <span data-ttu-id="b8a8e-122">X</span><span class="sxs-lookup"><span data-stu-id="b8a8e-122">X</span></span>        |
  | <span data-ttu-id="b8a8e-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="b8a8e-123">RequestId</span></span>         | <span data-ttu-id="b8a8e-124">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-124">String</span></span>    | <span data-ttu-id="b8a8e-125">X</span><span class="sxs-lookup"><span data-stu-id="b8a8e-125">X</span></span>        |
  | <span data-ttu-id="b8a8e-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="b8a8e-126">LeaveType</span></span>         | <span data-ttu-id="b8a8e-127">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-127">String</span></span>    | <span data-ttu-id="b8a8e-128">X</span><span class="sxs-lookup"><span data-stu-id="b8a8e-128">X</span></span>        |
  | <span data-ttu-id="b8a8e-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="b8a8e-129">LeaveDate</span></span>         | <span data-ttu-id="b8a8e-130">Datums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-130">Date</span></span>      | <span data-ttu-id="b8a8e-131">X</span><span class="sxs-lookup"><span data-stu-id="b8a8e-131">X</span></span>        |
  | <span data-ttu-id="b8a8e-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="b8a8e-132">ReasonCodeId</span></span>      | <span data-ttu-id="b8a8e-133">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-133">String</span></span>    |          |
  | <span data-ttu-id="b8a8e-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="b8a8e-134">PersonnelNumber</span></span>   | <span data-ttu-id="b8a8e-135">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-135">String</span></span>    | <span data-ttu-id="b8a8e-136">X</span><span class="sxs-lookup"><span data-stu-id="b8a8e-136">X</span></span>        |
  | <span data-ttu-id="b8a8e-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="b8a8e-137">RequestDate</span></span>       | <span data-ttu-id="b8a8e-138">Datums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-138">Date</span></span>      | <span data-ttu-id="b8a8e-139">X</span><span class="sxs-lookup"><span data-stu-id="b8a8e-139">X</span></span>        |
  | <span data-ttu-id="b8a8e-140">Komentārs</span><span class="sxs-lookup"><span data-stu-id="b8a8e-140">Comment</span></span>           | <span data-ttu-id="b8a8e-141">Virkne</span><span class="sxs-lookup"><span data-stu-id="b8a8e-141">String</span></span>    |          |
  | <span data-ttu-id="b8a8e-142">Statuss</span><span class="sxs-lookup"><span data-stu-id="b8a8e-142">Status</span></span>            | <span data-ttu-id="b8a8e-143">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-143">Enum</span></span>      | <span data-ttu-id="b8a8e-144">X</span><span class="sxs-lookup"><span data-stu-id="b8a8e-144">X</span></span>        |
  | <span data-ttu-id="b8a8e-145">Apjoms</span><span class="sxs-lookup"><span data-stu-id="b8a8e-145">Amount</span></span>            | <span data-ttu-id="b8a8e-146">Reāls</span><span class="sxs-lookup"><span data-stu-id="b8a8e-146">Real</span></span>      |          |
  | <span data-ttu-id="b8a8e-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="b8a8e-147">HalfDayDefinition</span></span> | <span data-ttu-id="b8a8e-148">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="b8a8e-149">Darbības</span><span class="sxs-lookup"><span data-stu-id="b8a8e-149">Actions</span></span>

 | <span data-ttu-id="b8a8e-150">Darbības nosaukums</span><span class="sxs-lookup"><span data-stu-id="b8a8e-150">Action Name</span></span>                               | <span data-ttu-id="b8a8e-151">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b8a8e-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="b8a8e-152">iesniegt</span><span class="sxs-lookup"><span data-stu-id="b8a8e-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="b8a8e-153">Iesniedziet darbplūsmā apstrādājamo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="b8a8e-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b8a8e-154">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="b8a8e-154">See also</span></span>

- [<span data-ttu-id="b8a8e-155">Atvaļinājuma pieprasījuma iesniegšana darbplūsmai</span><span class="sxs-lookup"><span data-stu-id="b8a8e-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="b8a8e-156">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="b8a8e-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]