---
title: Darba laika veidņu izveide
description: Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46c1e871133b51105386ac3b647432d0c36a6998
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551887"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="1c719-103">Darba laika veidņu izveide</span><span class="sxs-lookup"><span data-stu-id="1c719-103">Create working time templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c719-104">Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam.</span><span class="sxs-lookup"><span data-stu-id="1c719-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="1c719-105">Šajā procedūrā ir parādīts, kā definēt darba laika veidni, izmantojot darba laika plānošanas rekvizītus darba laika intervālu kategorizēšanai.</span><span class="sxs-lookup"><span data-stu-id="1c719-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="1c719-106">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="1c719-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="1c719-107">Pārejiet uz sadaļu Visas darbvietas > Resursu darbmūža pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="1c719-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="1c719-108">Noklikšķiniet uz Darba laika veidnes.</span><span class="sxs-lookup"><span data-stu-id="1c719-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="1c719-109">Darba laika veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="1c719-109">Create working time template</span></span>
1. <span data-ttu-id="1c719-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1c719-110">Click New.</span></span>
2. <span data-ttu-id="1c719-111">Laukā Darba laika veidne ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c719-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="1c719-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c719-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1c719-113">Izvērsiet sadaļu Pirmdiena.</span><span class="sxs-lookup"><span data-stu-id="1c719-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="1c719-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1c719-114">Click Add.</span></span>
6. <span data-ttu-id="1c719-115">Laukā No ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="1c719-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="1c719-116">Norādiet darba sākuma laiku no rīta.</span><span class="sxs-lookup"><span data-stu-id="1c719-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="1c719-117">Laukā Līdz ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="1c719-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="1c719-118">Norādiet laiku, kad sākas darbinieku pusdienu pārtraukums.</span><span class="sxs-lookup"><span data-stu-id="1c719-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="1c719-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1c719-119">Click Add.</span></span>
9. <span data-ttu-id="1c719-120">Laukā No ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="1c719-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="1c719-121">Norādiet laiku, kad darbs tiek atsākts pēc pusdienām.</span><span class="sxs-lookup"><span data-stu-id="1c719-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="1c719-122">Laukā Līdz ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="1c719-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="1c719-123">Norādiet darba dienas beigas.</span><span class="sxs-lookup"><span data-stu-id="1c719-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="1c719-124">Dublējiet darba laikus visām nedēļas dienām</span><span class="sxs-lookup"><span data-stu-id="1c719-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="1c719-125">Noklikšķiniet uz Kopēt dienu.</span><span class="sxs-lookup"><span data-stu-id="1c719-125">Click Copy day.</span></span>
    * <span data-ttu-id="1c719-126">Kopējiet darba laiku definīcijas no pirmdienas līdz otrdienai.</span><span class="sxs-lookup"><span data-stu-id="1c719-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="1c719-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1c719-127">Click OK.</span></span>
3. <span data-ttu-id="1c719-128">Noklikšķiniet uz Kopēt dienu.</span><span class="sxs-lookup"><span data-stu-id="1c719-128">Click Copy day.</span></span>
    * <span data-ttu-id="1c719-129">Kopējiet darba laiku definīcijas no pirmdienas līdz trešdienai.</span><span class="sxs-lookup"><span data-stu-id="1c719-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="1c719-130">Laukā Līdz nedēļas dienai atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="1c719-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="1c719-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1c719-131">Click OK.</span></span>
6. <span data-ttu-id="1c719-132">Noklikšķiniet uz Kopēt dienu.</span><span class="sxs-lookup"><span data-stu-id="1c719-132">Click Copy day.</span></span>
    * <span data-ttu-id="1c719-133">Kopējiet darba laiku definīcijas no pirmdienas līdz ceturtdienai.</span><span class="sxs-lookup"><span data-stu-id="1c719-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="1c719-134">Laukā Līdz nedēļas dienai atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="1c719-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="1c719-135">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1c719-135">Click OK.</span></span>
9. <span data-ttu-id="1c719-136">Noklikšķiniet uz Kopēt dienu.</span><span class="sxs-lookup"><span data-stu-id="1c719-136">Click Copy day.</span></span>
    * <span data-ttu-id="1c719-137">Kopējiet darba laiku definīcijas no pirmdienas līdz piektdienai.</span><span class="sxs-lookup"><span data-stu-id="1c719-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="1c719-138">Laukā Līdz nedēļas dienai atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="1c719-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="1c719-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1c719-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="1c719-140">Laikspraugu definēšana īpašām operācijām</span><span class="sxs-lookup"><span data-stu-id="1c719-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="1c719-141">Izvērsiet sadaļu Piektdiena.</span><span class="sxs-lookup"><span data-stu-id="1c719-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="1c719-142">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1c719-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1c719-143">Laukā Rekvizīts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c719-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="1c719-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1c719-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1c719-145">Laukā Rekvizīts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c719-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="1c719-146">Nedēļas nogales dienu atzīmēšana kā slēgtas izsniegšanai</span><span class="sxs-lookup"><span data-stu-id="1c719-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="1c719-147">Izvērsiet sadaļu Sestdiena.</span><span class="sxs-lookup"><span data-stu-id="1c719-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="1c719-148">Laukā Slēgts izsniegšanai atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="1c719-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="1c719-149">Izvērsiet sadaļu Svētdiena.</span><span class="sxs-lookup"><span data-stu-id="1c719-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="1c719-150">Laukā Slēgts izsniegšanai atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="1c719-150">Select Yes in the Closed for pickup field.</span></span>

