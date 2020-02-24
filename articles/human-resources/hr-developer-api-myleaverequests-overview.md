---
title: MyLeaveRequests pārskats
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009803"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="8f752-102">MyLeaveRequests pārskats</span><span class="sxs-lookup"><span data-stu-id="8f752-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="8f752-103">MyLeaveRequests elements programmā Microsoft Dynamics 365 Human Resources sniedz atvaļinājumu pieprasījumu sarakstu sistēmā, atlasītus (ierobežotus) līdz pieprasījumiem, kas pieejami pašreizējam lietotājam, kurš veic vaicājumus par elementu.</span><span class="sxs-lookup"><span data-stu-id="8f752-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="8f752-104">Taustiņš</span><span class="sxs-lookup"><span data-stu-id="8f752-104">Key</span></span>

  | <span data-ttu-id="8f752-105">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="8f752-105">Property Name</span></span> | <span data-ttu-id="8f752-106">Datu veids</span><span class="sxs-lookup"><span data-stu-id="8f752-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="8f752-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8f752-107">dataAreaId</span></span>    | <span data-ttu-id="8f752-108">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-108">String</span></span>    |
  | <span data-ttu-id="8f752-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="8f752-109">RequestId</span></span>     | <span data-ttu-id="8f752-110">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-110">String</span></span>    |
  | <span data-ttu-id="8f752-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8f752-111">LeaveType</span></span>     | <span data-ttu-id="8f752-112">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-112">String</span></span>    |
  | <span data-ttu-id="8f752-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8f752-113">LeaveDate</span></span>     | <span data-ttu-id="8f752-114">Datums</span><span class="sxs-lookup"><span data-stu-id="8f752-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="8f752-115">Rekvizīti</span><span class="sxs-lookup"><span data-stu-id="8f752-115">Properties</span></span>

  | <span data-ttu-id="8f752-116">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="8f752-116">Property Name</span></span>     | <span data-ttu-id="8f752-117">Datu veids</span><span class="sxs-lookup"><span data-stu-id="8f752-117">Data Type</span></span> | <span data-ttu-id="8f752-118">Pieprasīts</span><span class="sxs-lookup"><span data-stu-id="8f752-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="8f752-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8f752-119">dataAreaId</span></span>        | <span data-ttu-id="8f752-120">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-120">String</span></span>    | <span data-ttu-id="8f752-121">X</span><span class="sxs-lookup"><span data-stu-id="8f752-121">X</span></span>        |
  | <span data-ttu-id="8f752-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="8f752-122">RequestId</span></span>         | <span data-ttu-id="8f752-123">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-123">String</span></span>    | <span data-ttu-id="8f752-124">X</span><span class="sxs-lookup"><span data-stu-id="8f752-124">X</span></span>        |
  | <span data-ttu-id="8f752-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8f752-125">LeaveType</span></span>         | <span data-ttu-id="8f752-126">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-126">String</span></span>    | <span data-ttu-id="8f752-127">X</span><span class="sxs-lookup"><span data-stu-id="8f752-127">X</span></span>        |
  | <span data-ttu-id="8f752-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8f752-128">LeaveDate</span></span>         | <span data-ttu-id="8f752-129">Datums</span><span class="sxs-lookup"><span data-stu-id="8f752-129">Date</span></span>      | <span data-ttu-id="8f752-130">X</span><span class="sxs-lookup"><span data-stu-id="8f752-130">X</span></span>        |
  | <span data-ttu-id="8f752-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="8f752-131">ReasonCodeId</span></span>      | <span data-ttu-id="8f752-132">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-132">String</span></span>    |          |
  | <span data-ttu-id="8f752-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="8f752-133">PersonnelNumber</span></span>   | <span data-ttu-id="8f752-134">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-134">String</span></span>    | <span data-ttu-id="8f752-135">X</span><span class="sxs-lookup"><span data-stu-id="8f752-135">X</span></span>        |
  | <span data-ttu-id="8f752-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="8f752-136">RequestDate</span></span>       | <span data-ttu-id="8f752-137">Datums</span><span class="sxs-lookup"><span data-stu-id="8f752-137">Date</span></span>      | <span data-ttu-id="8f752-138">X</span><span class="sxs-lookup"><span data-stu-id="8f752-138">X</span></span>        |
  | <span data-ttu-id="8f752-139">Komentārs</span><span class="sxs-lookup"><span data-stu-id="8f752-139">Comment</span></span>           | <span data-ttu-id="8f752-140">Virkne</span><span class="sxs-lookup"><span data-stu-id="8f752-140">String</span></span>    |          |
  | <span data-ttu-id="8f752-141">Statuss</span><span class="sxs-lookup"><span data-stu-id="8f752-141">Status</span></span>            | <span data-ttu-id="8f752-142">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="8f752-142">Enum</span></span>      | <span data-ttu-id="8f752-143">X</span><span class="sxs-lookup"><span data-stu-id="8f752-143">X</span></span>        |
  | <span data-ttu-id="8f752-144">Apjoms</span><span class="sxs-lookup"><span data-stu-id="8f752-144">Amount</span></span>            | <span data-ttu-id="8f752-145">Reāls</span><span class="sxs-lookup"><span data-stu-id="8f752-145">Real</span></span>      |          |
  | <span data-ttu-id="8f752-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="8f752-146">HalfDayDefinition</span></span> | <span data-ttu-id="8f752-147">Uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="8f752-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="8f752-148">Darbības</span><span class="sxs-lookup"><span data-stu-id="8f752-148">Actions</span></span>

 | <span data-ttu-id="8f752-149">Darbības nosaukums</span><span class="sxs-lookup"><span data-stu-id="8f752-149">Action Name</span></span>                               | <span data-ttu-id="8f752-150">Apraksts</span><span class="sxs-lookup"><span data-stu-id="8f752-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="8f752-151">iesniegt</span><span class="sxs-lookup"><span data-stu-id="8f752-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="8f752-152">Iesniedziet darbplūsmā apstrādājamo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="8f752-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8f752-153">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="8f752-153">See also</span></span>

- [<span data-ttu-id="8f752-154">Atvaļinājuma pieprasījuma iesniegšana darbplūsmai</span><span class="sxs-lookup"><span data-stu-id="8f752-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="8f752-155">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="8f752-155">Authentication</span></span>](hr-developer-api-authentication.md)