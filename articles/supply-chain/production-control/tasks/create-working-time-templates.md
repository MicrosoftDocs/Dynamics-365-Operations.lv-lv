---
title: Darba laika veidņu izveide
description: Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920933"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="3fbcd-103">Darba laika veidņu izveide</span><span class="sxs-lookup"><span data-stu-id="3fbcd-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3fbcd-104">Darba laiku veidnes nosaka darba stundas visā nedēļā un tiek izmantotas, lai ģenerētu darba laikus noteiktam laika periodam.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="3fbcd-105">Šajā procedūrā ir parādīts, kā definēt darba laika veidni, izmantojot darba laika plānošanas rekvizītus darba laika intervālu kategorizēšanai.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="3fbcd-106">Šo procedūru var izmēģināt, izmantojot paraugdatu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="3fbcd-107">Pārejiet uz sadaļu **Darbvietas > Resursu darbmūža pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="3fbcd-108">Atlasiet **Darba laika veidnes**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="3fbcd-109">Darba laika veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="3fbcd-109">Create working time template</span></span>

1. <span data-ttu-id="3fbcd-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-110">Select **New**.</span></span>
1. <span data-ttu-id="3fbcd-111">Laukā **Darba laika veidne** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="3fbcd-112">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="3fbcd-113">Izvērsiet sadaļu **Pirmdiena**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="3fbcd-114">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-114">Select **Add**.</span></span>
1. <span data-ttu-id="3fbcd-115">Laukā **No** ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="3fbcd-116">Norādiet darba sākuma laiku no rīta.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="3fbcd-117">Laukā **Līdz** ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="3fbcd-118">Norādiet laiku, kad sākas darbinieku pusdienu pārtraukums.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="3fbcd-119">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-119">Select **Add**.</span></span>
1. <span data-ttu-id="3fbcd-120">Laukā **No** ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="3fbcd-121">Norādiet laiku, kad darbs tiek atsākts pēc pusdienām.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="3fbcd-122">Laukā **Līdz** ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="3fbcd-123">Norādiet darba dienas beigas.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="3fbcd-124">Dublējiet darba laikus visām nedēļas dienām</span><span class="sxs-lookup"><span data-stu-id="3fbcd-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="3fbcd-125">Atlasiet **Kopēt dienu**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="3fbcd-126">Kopējiet darba laiku definīcijas no pirmdienas līdz otrdienai.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="3fbcd-127">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-127">Select **OK**.</span></span>
1. <span data-ttu-id="3fbcd-128">Atlasiet **Kopēt dienu**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="3fbcd-129">Kopējiet darba laiku definīcijas no pirmdienas līdz trešdienai.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="3fbcd-130">Laukā **Līdz nedēļas dienai** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="3fbcd-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-131">Select **OK**.</span></span>
1. <span data-ttu-id="3fbcd-132">Atlasiet **Kopēt dienu**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="3fbcd-133">Kopējiet darba laiku definīcijas no pirmdienas līdz ceturtdienai.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="3fbcd-134">Laukā **Līdz nedēļas dienai** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="3fbcd-135">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-135">Select **OK**.</span></span>
1. <span data-ttu-id="3fbcd-136">Atlasiet **Kopēt dienu**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="3fbcd-137">Kopējiet darba laiku definīcijas no pirmdienas līdz piektdienai.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="3fbcd-138">Laukā **Līdz nedēļas dienai** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="3fbcd-139">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="3fbcd-140">Laikspraugu definēšana īpašām operācijām</span><span class="sxs-lookup"><span data-stu-id="3fbcd-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="3fbcd-141">Izvērsiet sadaļu **Piektdiena**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="3fbcd-142">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="3fbcd-143">Laukā **Rekvizīts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="3fbcd-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="3fbcd-145">Laukā **Rekvizīts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="3fbcd-146">Nedēļas nogales dienu atzīmēšana kā slēgtas izsniegšanai</span><span class="sxs-lookup"><span data-stu-id="3fbcd-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="3fbcd-147">Izvērsiet sadaļu **Sestdiena**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="3fbcd-148">Laukā **Slēgts izsniegšanai** atlasiet *Jā*.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="3fbcd-149">Izvērsiet sadaļu **Svētdiena**.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="3fbcd-150">Laukā **Slēgts izsniegšanai** atlasiet *Jā*.</span><span class="sxs-lookup"><span data-stu-id="3fbcd-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]