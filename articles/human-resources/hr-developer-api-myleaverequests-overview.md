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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465514"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="24839-103">MyLeaveRequests pārskats</span><span class="sxs-lookup"><span data-stu-id="24839-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="24839-104">MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.</span><span class="sxs-lookup"><span data-stu-id="24839-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="24839-105">Taustiņš</span><span class="sxs-lookup"><span data-stu-id="24839-105">Key</span></span>

  | <span data-ttu-id="24839-106">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="24839-106">Property Name</span></span> | <span data-ttu-id="24839-107">Datu veids</span><span class="sxs-lookup"><span data-stu-id="24839-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="24839-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="24839-108">dataAreaId</span></span>    | <span data-ttu-id="24839-109">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-109">String</span></span>    |
  | <span data-ttu-id="24839-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="24839-110">RequestId</span></span>     | <span data-ttu-id="24839-111">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-111">String</span></span>    |
  | <span data-ttu-id="24839-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="24839-112">LeaveType</span></span>     | <span data-ttu-id="24839-113">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-113">String</span></span>    |
  | <span data-ttu-id="24839-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="24839-114">LeaveDate</span></span>     | <span data-ttu-id="24839-115">Datums</span><span class="sxs-lookup"><span data-stu-id="24839-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="24839-116">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="24839-116">Properties</span></span>

  | <span data-ttu-id="24839-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="24839-117">Property Name</span></span>     | <span data-ttu-id="24839-118">Datu veids</span><span class="sxs-lookup"><span data-stu-id="24839-118">Data Type</span></span> | <span data-ttu-id="24839-119">Pieprasīts</span><span class="sxs-lookup"><span data-stu-id="24839-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="24839-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="24839-120">dataAreaId</span></span>        | <span data-ttu-id="24839-121">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-121">String</span></span>    | <span data-ttu-id="24839-122">X</span><span class="sxs-lookup"><span data-stu-id="24839-122">X</span></span>        |
  | <span data-ttu-id="24839-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="24839-123">RequestId</span></span>         | <span data-ttu-id="24839-124">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-124">String</span></span>    | <span data-ttu-id="24839-125">X</span><span class="sxs-lookup"><span data-stu-id="24839-125">X</span></span>        |
  | <span data-ttu-id="24839-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="24839-126">LeaveType</span></span>         | <span data-ttu-id="24839-127">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-127">String</span></span>    | <span data-ttu-id="24839-128">X</span><span class="sxs-lookup"><span data-stu-id="24839-128">X</span></span>        |
  | <span data-ttu-id="24839-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="24839-129">LeaveDate</span></span>         | <span data-ttu-id="24839-130">Datums</span><span class="sxs-lookup"><span data-stu-id="24839-130">Date</span></span>      | <span data-ttu-id="24839-131">X</span><span class="sxs-lookup"><span data-stu-id="24839-131">X</span></span>        |
  | <span data-ttu-id="24839-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="24839-132">ReasonCodeId</span></span>      | <span data-ttu-id="24839-133">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-133">String</span></span>    |          |
  | <span data-ttu-id="24839-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="24839-134">PersonnelNumber</span></span>   | <span data-ttu-id="24839-135">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-135">String</span></span>    | <span data-ttu-id="24839-136">X</span><span class="sxs-lookup"><span data-stu-id="24839-136">X</span></span>        |
  | <span data-ttu-id="24839-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="24839-137">RequestDate</span></span>       | <span data-ttu-id="24839-138">Datums</span><span class="sxs-lookup"><span data-stu-id="24839-138">Date</span></span>      | <span data-ttu-id="24839-139">X</span><span class="sxs-lookup"><span data-stu-id="24839-139">X</span></span>        |
  | <span data-ttu-id="24839-140">Komentārs</span><span class="sxs-lookup"><span data-stu-id="24839-140">Comment</span></span>           | <span data-ttu-id="24839-141">Virkne</span><span class="sxs-lookup"><span data-stu-id="24839-141">String</span></span>    |          |
  | <span data-ttu-id="24839-142">Statuss</span><span class="sxs-lookup"><span data-stu-id="24839-142">Status</span></span>            | <span data-ttu-id="24839-143">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="24839-143">Enum</span></span>      | <span data-ttu-id="24839-144">X</span><span class="sxs-lookup"><span data-stu-id="24839-144">X</span></span>        |
  | <span data-ttu-id="24839-145">Apjoms</span><span class="sxs-lookup"><span data-stu-id="24839-145">Amount</span></span>            | <span data-ttu-id="24839-146">Reāls</span><span class="sxs-lookup"><span data-stu-id="24839-146">Real</span></span>      |          |
  | <span data-ttu-id="24839-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="24839-147">HalfDayDefinition</span></span> | <span data-ttu-id="24839-148">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="24839-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="24839-149">Darbības</span><span class="sxs-lookup"><span data-stu-id="24839-149">Actions</span></span>

 | <span data-ttu-id="24839-150">Darbības nosaukums</span><span class="sxs-lookup"><span data-stu-id="24839-150">Action Name</span></span>                               | <span data-ttu-id="24839-151">Apraksts</span><span class="sxs-lookup"><span data-stu-id="24839-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="24839-152">iesniegt</span><span class="sxs-lookup"><span data-stu-id="24839-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="24839-153">Iesniedziet darbplūsmā apstrādājamo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="24839-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="24839-154">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="24839-154">See also</span></span>

- [<span data-ttu-id="24839-155">Atvaļinājuma pieprasījuma iesniegšana darbplūsmai</span><span class="sxs-lookup"><span data-stu-id="24839-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="24839-156">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="24839-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]