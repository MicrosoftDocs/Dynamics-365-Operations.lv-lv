---
title: Darbinieku patstāvīgi izmantojamā pakalpojuma konfigurēšana
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009817"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="6cfb5-102">Darbinieku patstāvīgi izmantojamā pakalpojuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6cfb5-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="6cfb5-103">Microsoft Dynamics 365 Human Resources varat konfigurēt darbinieku patstāvīgi izmantojamā pakalpojuma augšējā līmeņa navigācijas elementus.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="6cfb5-104">Atvieglojumu plāna elementi novirza lietotājus uz atvieglojumu plāniem, kuros tie ir tiesīgi reģistrēties.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="6cfb5-105">Lomu centra elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6cfb5-105">Set up a role center tile</span></span>

1. <span data-ttu-id="6cfb5-106">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="6cfb5-107">Atlasiet cilni **Lomu centra elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="6cfb5-108">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6cfb5-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="6cfb5-109">Field</span></span> | <span data-ttu-id="6cfb5-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6cfb5-111">Elementa ID</span><span class="sxs-lookup"><span data-stu-id="6cfb5-111">Tile ID</span></span> | <span data-ttu-id="6cfb5-112">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="6cfb5-113">Elementa etiķetes teksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-113">Tile label text</span></span> | <span data-ttu-id="6cfb5-114">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="6cfb5-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-115">Description</span></span> | <span data-ttu-id="6cfb5-116">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-116">A description of the tile.</span></span> |
   | <span data-ttu-id="6cfb5-117">Interneta adrese</span><span class="sxs-lookup"><span data-stu-id="6cfb5-117">Internet address</span></span> | <span data-ttu-id="6cfb5-118">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="6cfb5-119">Elementa lielums</span><span class="sxs-lookup"><span data-stu-id="6cfb5-119">Tile size</span></span> | <span data-ttu-id="6cfb5-120">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="6cfb5-121">Adresāts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-121">Target</span></span> | <span data-ttu-id="6cfb5-122">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="6cfb5-123">Elementa fona attēls</span><span class="sxs-lookup"><span data-stu-id="6cfb5-123">Tile background image</span></span> | <span data-ttu-id="6cfb5-124">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="6cfb5-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="6cfb5-125">Sākšana</span><span class="sxs-lookup"><span data-stu-id="6cfb5-125">Start</span></span> | <span data-ttu-id="6cfb5-126">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="6cfb5-127">End</span><span class="sxs-lookup"><span data-stu-id="6cfb5-127">End</span></span> | <span data-ttu-id="6cfb5-128">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="6cfb5-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="6cfb5-130">Atvieglojumu plānu elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6cfb5-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="6cfb5-131">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="6cfb5-132">Atlasiet cilni **Atvieglojumu plānu elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="6cfb5-133">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6cfb5-134">Lauks</span><span class="sxs-lookup"><span data-stu-id="6cfb5-134">Field</span></span> | <span data-ttu-id="6cfb5-135">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6cfb5-136">Elementa ID</span><span class="sxs-lookup"><span data-stu-id="6cfb5-136">Tile ID</span></span> | <span data-ttu-id="6cfb5-137">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="6cfb5-138">Elementa etiķetes teksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-138">Tile label text</span></span> | <span data-ttu-id="6cfb5-139">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="6cfb5-140">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-140">Description</span></span> | <span data-ttu-id="6cfb5-141">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-141">A description of the tile.</span></span> |
   | <span data-ttu-id="6cfb5-142">Interneta adrese</span><span class="sxs-lookup"><span data-stu-id="6cfb5-142">Internet address</span></span> | <span data-ttu-id="6cfb5-143">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="6cfb5-144">Elementa lielums</span><span class="sxs-lookup"><span data-stu-id="6cfb5-144">Tile size</span></span> | <span data-ttu-id="6cfb5-145">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="6cfb5-146">Adresāts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-146">Target</span></span> | <span data-ttu-id="6cfb5-147">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="6cfb5-148">Elementa fona attēls</span><span class="sxs-lookup"><span data-stu-id="6cfb5-148">Tile background image</span></span> | <span data-ttu-id="6cfb5-149">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="6cfb5-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="6cfb5-150">Sākšana</span><span class="sxs-lookup"><span data-stu-id="6cfb5-150">Start</span></span> | <span data-ttu-id="6cfb5-151">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="6cfb5-152">End</span><span class="sxs-lookup"><span data-stu-id="6cfb5-152">End</span></span> | <span data-ttu-id="6cfb5-153">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="6cfb5-154">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="6cfb5-155">Brīvā režīma kredīta plāna elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6cfb5-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="6cfb5-156">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="6cfb5-157">Atlasiet cilni **Brīvā režīma kredīta plāna elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="6cfb5-158">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6cfb5-159">Lauks</span><span class="sxs-lookup"><span data-stu-id="6cfb5-159">Field</span></span> | <span data-ttu-id="6cfb5-160">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6cfb5-161">Elementa ID</span><span class="sxs-lookup"><span data-stu-id="6cfb5-161">Tile ID</span></span> | <span data-ttu-id="6cfb5-162">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="6cfb5-163">Elementa etiķetes teksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-163">Tile label text</span></span> | <span data-ttu-id="6cfb5-164">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="6cfb5-165">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-165">Description</span></span> | <span data-ttu-id="6cfb5-166">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-166">A description of the tile.</span></span> |
   | <span data-ttu-id="6cfb5-167">Interneta adrese</span><span class="sxs-lookup"><span data-stu-id="6cfb5-167">Internet address</span></span> | <span data-ttu-id="6cfb5-168">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="6cfb5-169">Elementa lielums</span><span class="sxs-lookup"><span data-stu-id="6cfb5-169">Tile size</span></span> | <span data-ttu-id="6cfb5-170">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="6cfb5-171">Adresāts</span><span class="sxs-lookup"><span data-stu-id="6cfb5-171">Target</span></span> | <span data-ttu-id="6cfb5-172">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="6cfb5-173">Elementa fona attēls</span><span class="sxs-lookup"><span data-stu-id="6cfb5-173">Tile background image</span></span> | <span data-ttu-id="6cfb5-174">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="6cfb5-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="6cfb5-175">Sākšana</span><span class="sxs-lookup"><span data-stu-id="6cfb5-175">Start</span></span> | <span data-ttu-id="6cfb5-176">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="6cfb5-177">End</span><span class="sxs-lookup"><span data-stu-id="6cfb5-177">End</span></span> | <span data-ttu-id="6cfb5-178">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="6cfb5-179">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6cfb5-179">Select **Save**.</span></span>
