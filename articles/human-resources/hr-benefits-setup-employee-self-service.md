---
title: Konfigurēt darbinieku patstāvīgi izmantojamo pakalpojumu
description: Microsoft Dynamics 365 Human Resources varat konfigurēt darbinieku patstāvīgi izmantojamā pakalpojuma augšējā līmeņa navigācijas elementus.
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
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092664"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="1bfe9-103">Konfigurēt darbinieku patstāvīgi izmantojamo pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="1bfe9-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1bfe9-104">Microsoft Dynamics 365 Human Resources varat konfigurēt darbinieku patstāvīgi izmantojamā pakalpojuma augšējā līmeņa navigācijas elementus.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="1bfe9-105">Atvieglojumu plāna elementi novirza lietotājus uz atvieglojumu plāniem, kuros tie ir tiesīgi reģistrēties.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="1bfe9-106">Lomu centra elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1bfe9-106">Set up a role center tile</span></span>

1. <span data-ttu-id="1bfe9-107">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1bfe9-108">Atlasiet cilni **Lomu centra elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1bfe9-109">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1bfe9-110">Lauks</span><span class="sxs-lookup"><span data-stu-id="1bfe9-110">Field</span></span> | <span data-ttu-id="1bfe9-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1bfe9-112">Elementa ID</span><span class="sxs-lookup"><span data-stu-id="1bfe9-112">Tile ID</span></span> | <span data-ttu-id="1bfe9-113">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1bfe9-114">Elementa etiķetes teksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-114">Tile label text</span></span> | <span data-ttu-id="1bfe9-115">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1bfe9-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-116">Description</span></span> | <span data-ttu-id="1bfe9-117">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-117">A description of the tile.</span></span> |
   | <span data-ttu-id="1bfe9-118">Interneta adrese</span><span class="sxs-lookup"><span data-stu-id="1bfe9-118">Internet address</span></span> | <span data-ttu-id="1bfe9-119">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1bfe9-120">Elementa lielums</span><span class="sxs-lookup"><span data-stu-id="1bfe9-120">Tile size</span></span> | <span data-ttu-id="1bfe9-121">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1bfe9-122">Adresāts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-122">Target</span></span> | <span data-ttu-id="1bfe9-123">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1bfe9-124">Elementa fona attēls</span><span class="sxs-lookup"><span data-stu-id="1bfe9-124">Tile background image</span></span> | <span data-ttu-id="1bfe9-125">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="1bfe9-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1bfe9-126">Sākšana</span><span class="sxs-lookup"><span data-stu-id="1bfe9-126">Start</span></span> | <span data-ttu-id="1bfe9-127">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1bfe9-128">End</span><span class="sxs-lookup"><span data-stu-id="1bfe9-128">End</span></span> | <span data-ttu-id="1bfe9-129">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1bfe9-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="1bfe9-131">Atvieglojumu plānu elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1bfe9-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="1bfe9-132">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1bfe9-133">Atlasiet cilni **Atvieglojumu plānu elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1bfe9-134">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1bfe9-135">Lauks</span><span class="sxs-lookup"><span data-stu-id="1bfe9-135">Field</span></span> | <span data-ttu-id="1bfe9-136">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1bfe9-137">Elementa ID</span><span class="sxs-lookup"><span data-stu-id="1bfe9-137">Tile ID</span></span> | <span data-ttu-id="1bfe9-138">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1bfe9-139">Elementa etiķetes teksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-139">Tile label text</span></span> | <span data-ttu-id="1bfe9-140">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1bfe9-141">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-141">Description</span></span> | <span data-ttu-id="1bfe9-142">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-142">A description of the tile.</span></span> |
   | <span data-ttu-id="1bfe9-143">Interneta adrese</span><span class="sxs-lookup"><span data-stu-id="1bfe9-143">Internet address</span></span> | <span data-ttu-id="1bfe9-144">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1bfe9-145">Elementa lielums</span><span class="sxs-lookup"><span data-stu-id="1bfe9-145">Tile size</span></span> | <span data-ttu-id="1bfe9-146">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1bfe9-147">Adresāts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-147">Target</span></span> | <span data-ttu-id="1bfe9-148">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1bfe9-149">Elementa fona attēls</span><span class="sxs-lookup"><span data-stu-id="1bfe9-149">Tile background image</span></span> | <span data-ttu-id="1bfe9-150">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="1bfe9-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1bfe9-151">Sākšana</span><span class="sxs-lookup"><span data-stu-id="1bfe9-151">Start</span></span> | <span data-ttu-id="1bfe9-152">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1bfe9-153">End</span><span class="sxs-lookup"><span data-stu-id="1bfe9-153">End</span></span> | <span data-ttu-id="1bfe9-154">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1bfe9-155">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="1bfe9-156">Brīvā režīma kredīta plāna elementa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1bfe9-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="1bfe9-157">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1bfe9-158">Atlasiet cilni **Brīvā režīma kredīta plāna elementa iestatīšana** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1bfe9-159">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1bfe9-160">Lauks</span><span class="sxs-lookup"><span data-stu-id="1bfe9-160">Field</span></span> | <span data-ttu-id="1bfe9-161">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1bfe9-162">Elementa ID</span><span class="sxs-lookup"><span data-stu-id="1bfe9-162">Tile ID</span></span> | <span data-ttu-id="1bfe9-163">Elementa unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1bfe9-164">Elementa etiķetes teksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-164">Tile label text</span></span> | <span data-ttu-id="1bfe9-165">Teksts, kas būs redzams patstāvīgi izmantojamā pakalpojuma elementā.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1bfe9-166">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-166">Description</span></span> | <span data-ttu-id="1bfe9-167">Elementa apraksts.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-167">A description of the tile.</span></span> |
   | <span data-ttu-id="1bfe9-168">Interneta adrese</span><span class="sxs-lookup"><span data-stu-id="1bfe9-168">Internet address</span></span> | <span data-ttu-id="1bfe9-169">Ievadiet URL uz darbinieku patstāvīgi izmantojamo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1bfe9-170">Elementa lielums</span><span class="sxs-lookup"><span data-stu-id="1bfe9-170">Tile size</span></span> | <span data-ttu-id="1bfe9-171">Elementa lielums: mazs, vidējs vai liels.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1bfe9-172">Adresāts</span><span class="sxs-lookup"><span data-stu-id="1bfe9-172">Target</span></span> | <span data-ttu-id="1bfe9-173">Norāda, vai lapa ir jāatver jaunā logā vai esošajā logā.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1bfe9-174">Elementa fona attēls</span><span class="sxs-lookup"><span data-stu-id="1bfe9-174">Tile background image</span></span> | <span data-ttu-id="1bfe9-175">Elementam izmantojamā attēla URL (nav obligāts).</span><span class="sxs-lookup"><span data-stu-id="1bfe9-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1bfe9-176">Sākšana</span><span class="sxs-lookup"><span data-stu-id="1bfe9-176">Start</span></span> | <span data-ttu-id="1bfe9-177">Elementa pieejamības sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1bfe9-178">End</span><span class="sxs-lookup"><span data-stu-id="1bfe9-178">End</span></span> | <span data-ttu-id="1bfe9-179">Elementa pieejamības beigu datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1bfe9-180">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-180">Select **Save**.</span></span>
