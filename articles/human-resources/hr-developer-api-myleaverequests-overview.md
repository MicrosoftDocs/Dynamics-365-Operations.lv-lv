---
title: MyLeaveRequests pārskats
description: MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115540"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="220f3-103">MyLeaveRequests pārskats</span><span class="sxs-lookup"><span data-stu-id="220f3-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="220f3-104">MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.</span><span class="sxs-lookup"><span data-stu-id="220f3-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="220f3-105">Taustiņš</span><span class="sxs-lookup"><span data-stu-id="220f3-105">Key</span></span>

  | <span data-ttu-id="220f3-106">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="220f3-106">Property Name</span></span> | <span data-ttu-id="220f3-107">Datu veids</span><span class="sxs-lookup"><span data-stu-id="220f3-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="220f3-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="220f3-108">dataAreaId</span></span>    | <span data-ttu-id="220f3-109">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-109">String</span></span>    |
  | <span data-ttu-id="220f3-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="220f3-110">RequestId</span></span>     | <span data-ttu-id="220f3-111">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-111">String</span></span>    |
  | <span data-ttu-id="220f3-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="220f3-112">LeaveType</span></span>     | <span data-ttu-id="220f3-113">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-113">String</span></span>    |
  | <span data-ttu-id="220f3-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="220f3-114">LeaveDate</span></span>     | <span data-ttu-id="220f3-115">Datums</span><span class="sxs-lookup"><span data-stu-id="220f3-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="220f3-116">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="220f3-116">Properties</span></span>

  | <span data-ttu-id="220f3-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="220f3-117">Property Name</span></span>     | <span data-ttu-id="220f3-118">Datu veids</span><span class="sxs-lookup"><span data-stu-id="220f3-118">Data Type</span></span> | <span data-ttu-id="220f3-119">Pieprasīts</span><span class="sxs-lookup"><span data-stu-id="220f3-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="220f3-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="220f3-120">dataAreaId</span></span>        | <span data-ttu-id="220f3-121">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-121">String</span></span>    | <span data-ttu-id="220f3-122">X</span><span class="sxs-lookup"><span data-stu-id="220f3-122">X</span></span>        |
  | <span data-ttu-id="220f3-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="220f3-123">RequestId</span></span>         | <span data-ttu-id="220f3-124">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-124">String</span></span>    | <span data-ttu-id="220f3-125">X</span><span class="sxs-lookup"><span data-stu-id="220f3-125">X</span></span>        |
  | <span data-ttu-id="220f3-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="220f3-126">LeaveType</span></span>         | <span data-ttu-id="220f3-127">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-127">String</span></span>    | <span data-ttu-id="220f3-128">X</span><span class="sxs-lookup"><span data-stu-id="220f3-128">X</span></span>        |
  | <span data-ttu-id="220f3-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="220f3-129">LeaveDate</span></span>         | <span data-ttu-id="220f3-130">Datums</span><span class="sxs-lookup"><span data-stu-id="220f3-130">Date</span></span>      | <span data-ttu-id="220f3-131">X</span><span class="sxs-lookup"><span data-stu-id="220f3-131">X</span></span>        |
  | <span data-ttu-id="220f3-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="220f3-132">ReasonCodeId</span></span>      | <span data-ttu-id="220f3-133">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-133">String</span></span>    |          |
  | <span data-ttu-id="220f3-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="220f3-134">PersonnelNumber</span></span>   | <span data-ttu-id="220f3-135">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-135">String</span></span>    | <span data-ttu-id="220f3-136">X</span><span class="sxs-lookup"><span data-stu-id="220f3-136">X</span></span>        |
  | <span data-ttu-id="220f3-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="220f3-137">RequestDate</span></span>       | <span data-ttu-id="220f3-138">Datums</span><span class="sxs-lookup"><span data-stu-id="220f3-138">Date</span></span>      | <span data-ttu-id="220f3-139">X</span><span class="sxs-lookup"><span data-stu-id="220f3-139">X</span></span>        |
  | <span data-ttu-id="220f3-140">Komentārs</span><span class="sxs-lookup"><span data-stu-id="220f3-140">Comment</span></span>           | <span data-ttu-id="220f3-141">Virkne</span><span class="sxs-lookup"><span data-stu-id="220f3-141">String</span></span>    |          |
  | <span data-ttu-id="220f3-142">Statuss</span><span class="sxs-lookup"><span data-stu-id="220f3-142">Status</span></span>            | <span data-ttu-id="220f3-143">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="220f3-143">Enum</span></span>      | <span data-ttu-id="220f3-144">X</span><span class="sxs-lookup"><span data-stu-id="220f3-144">X</span></span>        |
  | <span data-ttu-id="220f3-145">Apjoms</span><span class="sxs-lookup"><span data-stu-id="220f3-145">Amount</span></span>            | <span data-ttu-id="220f3-146">Reāls</span><span class="sxs-lookup"><span data-stu-id="220f3-146">Real</span></span>      |          |
  | <span data-ttu-id="220f3-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="220f3-147">HalfDayDefinition</span></span> | <span data-ttu-id="220f3-148">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="220f3-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="220f3-149">Darbības</span><span class="sxs-lookup"><span data-stu-id="220f3-149">Actions</span></span>

 | <span data-ttu-id="220f3-150">Darbības nosaukums</span><span class="sxs-lookup"><span data-stu-id="220f3-150">Action Name</span></span>                               | <span data-ttu-id="220f3-151">Apraksts</span><span class="sxs-lookup"><span data-stu-id="220f3-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="220f3-152">iesniegt</span><span class="sxs-lookup"><span data-stu-id="220f3-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="220f3-153">Iesniedziet darbplūsmā apstrādājamo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="220f3-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="220f3-154">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="220f3-154">See also</span></span>

- [<span data-ttu-id="220f3-155">Atvaļinājuma pieprasījuma iesniegšana darbplūsmai</span><span class="sxs-lookup"><span data-stu-id="220f3-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="220f3-156">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="220f3-156">Authentication</span></span>](hr-developer-api-authentication.md)