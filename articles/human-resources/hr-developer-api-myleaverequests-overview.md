---
title: MyLeaveRequests pārskats
description: MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419477"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="67a72-103">MyLeaveRequests pārskats</span><span class="sxs-lookup"><span data-stu-id="67a72-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="67a72-104">MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.</span><span class="sxs-lookup"><span data-stu-id="67a72-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="67a72-105">Taustiņš</span><span class="sxs-lookup"><span data-stu-id="67a72-105">Key</span></span>

  | <span data-ttu-id="67a72-106">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="67a72-106">Property Name</span></span> | <span data-ttu-id="67a72-107">Datu veids</span><span class="sxs-lookup"><span data-stu-id="67a72-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="67a72-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="67a72-108">dataAreaId</span></span>    | <span data-ttu-id="67a72-109">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-109">String</span></span>    |
  | <span data-ttu-id="67a72-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="67a72-110">RequestId</span></span>     | <span data-ttu-id="67a72-111">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-111">String</span></span>    |
  | <span data-ttu-id="67a72-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="67a72-112">LeaveType</span></span>     | <span data-ttu-id="67a72-113">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-113">String</span></span>    |
  | <span data-ttu-id="67a72-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="67a72-114">LeaveDate</span></span>     | <span data-ttu-id="67a72-115">Datums</span><span class="sxs-lookup"><span data-stu-id="67a72-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="67a72-116">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="67a72-116">Properties</span></span>

  | <span data-ttu-id="67a72-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="67a72-117">Property Name</span></span>     | <span data-ttu-id="67a72-118">Datu veids</span><span class="sxs-lookup"><span data-stu-id="67a72-118">Data Type</span></span> | <span data-ttu-id="67a72-119">Pieprasīts</span><span class="sxs-lookup"><span data-stu-id="67a72-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="67a72-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="67a72-120">dataAreaId</span></span>        | <span data-ttu-id="67a72-121">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-121">String</span></span>    | <span data-ttu-id="67a72-122">X</span><span class="sxs-lookup"><span data-stu-id="67a72-122">X</span></span>        |
  | <span data-ttu-id="67a72-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="67a72-123">RequestId</span></span>         | <span data-ttu-id="67a72-124">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-124">String</span></span>    | <span data-ttu-id="67a72-125">X</span><span class="sxs-lookup"><span data-stu-id="67a72-125">X</span></span>        |
  | <span data-ttu-id="67a72-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="67a72-126">LeaveType</span></span>         | <span data-ttu-id="67a72-127">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-127">String</span></span>    | <span data-ttu-id="67a72-128">X</span><span class="sxs-lookup"><span data-stu-id="67a72-128">X</span></span>        |
  | <span data-ttu-id="67a72-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="67a72-129">LeaveDate</span></span>         | <span data-ttu-id="67a72-130">Datums</span><span class="sxs-lookup"><span data-stu-id="67a72-130">Date</span></span>      | <span data-ttu-id="67a72-131">X</span><span class="sxs-lookup"><span data-stu-id="67a72-131">X</span></span>        |
  | <span data-ttu-id="67a72-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="67a72-132">ReasonCodeId</span></span>      | <span data-ttu-id="67a72-133">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-133">String</span></span>    |          |
  | <span data-ttu-id="67a72-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="67a72-134">PersonnelNumber</span></span>   | <span data-ttu-id="67a72-135">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-135">String</span></span>    | <span data-ttu-id="67a72-136">X</span><span class="sxs-lookup"><span data-stu-id="67a72-136">X</span></span>        |
  | <span data-ttu-id="67a72-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="67a72-137">RequestDate</span></span>       | <span data-ttu-id="67a72-138">Datums</span><span class="sxs-lookup"><span data-stu-id="67a72-138">Date</span></span>      | <span data-ttu-id="67a72-139">X</span><span class="sxs-lookup"><span data-stu-id="67a72-139">X</span></span>        |
  | <span data-ttu-id="67a72-140">Komentārs</span><span class="sxs-lookup"><span data-stu-id="67a72-140">Comment</span></span>           | <span data-ttu-id="67a72-141">Virkne</span><span class="sxs-lookup"><span data-stu-id="67a72-141">String</span></span>    |          |
  | <span data-ttu-id="67a72-142">Statuss</span><span class="sxs-lookup"><span data-stu-id="67a72-142">Status</span></span>            | <span data-ttu-id="67a72-143">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="67a72-143">Enum</span></span>      | <span data-ttu-id="67a72-144">X</span><span class="sxs-lookup"><span data-stu-id="67a72-144">X</span></span>        |
  | <span data-ttu-id="67a72-145">Apjoms</span><span class="sxs-lookup"><span data-stu-id="67a72-145">Amount</span></span>            | <span data-ttu-id="67a72-146">Reāls</span><span class="sxs-lookup"><span data-stu-id="67a72-146">Real</span></span>      |          |
  | <span data-ttu-id="67a72-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="67a72-147">HalfDayDefinition</span></span> | <span data-ttu-id="67a72-148">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="67a72-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="67a72-149">Darbības</span><span class="sxs-lookup"><span data-stu-id="67a72-149">Actions</span></span>

 | <span data-ttu-id="67a72-150">Darbības nosaukums</span><span class="sxs-lookup"><span data-stu-id="67a72-150">Action Name</span></span>                               | <span data-ttu-id="67a72-151">Apraksts</span><span class="sxs-lookup"><span data-stu-id="67a72-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="67a72-152">iesniegt</span><span class="sxs-lookup"><span data-stu-id="67a72-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="67a72-153">Iesniedziet darbplūsmā apstrādājamo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="67a72-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="67a72-154">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="67a72-154">See also</span></span>

- [<span data-ttu-id="67a72-155">Atvaļinājuma pieprasījuma iesniegšana darbplūsmai</span><span class="sxs-lookup"><span data-stu-id="67a72-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="67a72-156">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="67a72-156">Authentication</span></span>](hr-developer-api-authentication.md)