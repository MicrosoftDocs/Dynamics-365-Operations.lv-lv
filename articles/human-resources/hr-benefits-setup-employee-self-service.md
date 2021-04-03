---
title: Konfigurēt darbinieku patstāvīgi izmantojamo pakalpojumu
description: Microsoft Dynamics 365 Human Resources varat konfigurēt darbinieku patstāvīgi izmantojamā pakalpojuma augšējā līmeņa navigācijas elementus.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c4fe8f7afd4b77636ce77e58a2e75196fddae132
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466114"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="3a543-103">Konfigurēt darbinieku patstāvīgi izmantojamo pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="3a543-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3a543-104">Microsoft Dynamics 365 Human Resources varat konfigurēt darbinieku patstāvīgi izmantojamā pakalpojuma augšējā līmeņa navigācijas elementus.</span><span class="sxs-lookup"><span data-stu-id="3a543-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="3a543-105">Atvieglojumu plāna elementi novirza lietotājus uz atvieglojumu plāniem, kuros tie ir tiesīgi reģistrēties.</span><span class="sxs-lookup"><span data-stu-id="3a543-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="3a543-106">Atvieglojumu plānu elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3a543-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="3a543-107">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="3a543-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="3a543-108">Atlasiet cilni **Atvieglojumu plānu elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3a543-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="3a543-109">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="3a543-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3a543-110">Lauks</span><span class="sxs-lookup"><span data-stu-id="3a543-110">Field</span></span> | <span data-ttu-id="3a543-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="3a543-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3a543-112">**Elementa ID**</span><span class="sxs-lookup"><span data-stu-id="3a543-112">**Tile ID**</span></span> | <span data-ttu-id="3a543-113">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="3a543-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="3a543-114">**Elementa etiķetes teksts**</span><span class="sxs-lookup"><span data-stu-id="3a543-114">**Tile label text**</span></span> | <span data-ttu-id="3a543-115">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="3a543-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="3a543-116">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="3a543-116">**Description**</span></span> | <span data-ttu-id="3a543-117">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="3a543-117">A description of the tile.</span></span> |
   | <span data-ttu-id="3a543-118">**Interneta adrese**</span><span class="sxs-lookup"><span data-stu-id="3a543-118">**Internet address**</span></span> | <span data-ttu-id="3a543-119">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="3a543-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="3a543-120">**Elementa lielums**</span><span class="sxs-lookup"><span data-stu-id="3a543-120">**Tile size**</span></span> | <span data-ttu-id="3a543-121">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="3a543-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="3a543-122">**Adresāts**</span><span class="sxs-lookup"><span data-stu-id="3a543-122">**Target**</span></span> | <span data-ttu-id="3a543-123">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="3a543-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="3a543-124">**Elementa fona attēls**</span><span class="sxs-lookup"><span data-stu-id="3a543-124">**Tile background image**</span></span> | <span data-ttu-id="3a543-125">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="3a543-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="3a543-126">**Sākšana**</span><span class="sxs-lookup"><span data-stu-id="3a543-126">**Start**</span></span> | <span data-ttu-id="3a543-127">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="3a543-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="3a543-128">**End**</span><span class="sxs-lookup"><span data-stu-id="3a543-128">**End**</span></span> | <span data-ttu-id="3a543-129">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="3a543-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="3a543-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3a543-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="3a543-131">Brīvā režīma kredīta plāna elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3a543-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="3a543-132">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="3a543-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="3a543-133">Atlasiet cilni **Brīvā režīma kredīta plāna elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3a543-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="3a543-134">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="3a543-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3a543-135">Lauks</span><span class="sxs-lookup"><span data-stu-id="3a543-135">Field</span></span> | <span data-ttu-id="3a543-136">Apraksts</span><span class="sxs-lookup"><span data-stu-id="3a543-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3a543-137">**Elementa ID**</span><span class="sxs-lookup"><span data-stu-id="3a543-137">**Tile ID**</span></span> | <span data-ttu-id="3a543-138">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="3a543-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="3a543-139">**Elementa etiķetes teksts**</span><span class="sxs-lookup"><span data-stu-id="3a543-139">**Tile label text**</span></span> | <span data-ttu-id="3a543-140">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="3a543-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="3a543-141">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="3a543-141">**Description**</span></span> | <span data-ttu-id="3a543-142">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="3a543-142">A description of the tile.</span></span> |
   | <span data-ttu-id="3a543-143">**Interneta adrese**</span><span class="sxs-lookup"><span data-stu-id="3a543-143">**Internet address**</span></span> | <span data-ttu-id="3a543-144">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="3a543-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="3a543-145">**Elementa lielums**</span><span class="sxs-lookup"><span data-stu-id="3a543-145">**Tile size**</span></span> | <span data-ttu-id="3a543-146">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="3a543-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="3a543-147">**Adresāts**</span><span class="sxs-lookup"><span data-stu-id="3a543-147">**Target**</span></span> | <span data-ttu-id="3a543-148">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="3a543-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="3a543-149">**Elementa fona attēls**</span><span class="sxs-lookup"><span data-stu-id="3a543-149">**Tile background image**</span></span> | <span data-ttu-id="3a543-150">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="3a543-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="3a543-151">**Sākšana**</span><span class="sxs-lookup"><span data-stu-id="3a543-151">**Start**</span></span> | <span data-ttu-id="3a543-152">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="3a543-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="3a543-153">**End**</span><span class="sxs-lookup"><span data-stu-id="3a543-153">**End**</span></span> | <span data-ttu-id="3a543-154">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="3a543-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="3a543-155">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3a543-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]