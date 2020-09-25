---
title: Izveidot jaunu projektu
description: Šajā sadaļā ir sniegta informācija par to, kā izveidot jaunu projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760603"
---
# <a name="create-a-new-project"></a><span data-ttu-id="b9156-103">Izveidot jaunu projektu</span><span class="sxs-lookup"><span data-stu-id="b9156-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9156-104">Lai izveidotu jaunu projektu, veiciet tālāk norādītās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="b9156-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="b9156-105">Lapā **Projektu vadība** atlasiet **Jauns projekts** un ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="b9156-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="b9156-106">**Projekta veids:** Laiks un materiāls</span><span class="sxs-lookup"><span data-stu-id="b9156-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="b9156-107">**Projekta nosaukums:** XYZ jaunināšanas fāze 2</span><span class="sxs-lookup"><span data-stu-id="b9156-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="b9156-108">**Projektu grupa:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="b9156-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="b9156-109">**Projekta līguma ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="b9156-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="b9156-110">Atlasiet **Izveidot projektu**.</span><span class="sxs-lookup"><span data-stu-id="b9156-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="b9156-111">Resursa piešķiršana projektam</span><span class="sxs-lookup"><span data-stu-id="b9156-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="b9156-112">Lapa **Nodarbinātie**, sarakstā **Nodarbinātie** atlasiet tāda nodarbinātā ierakstu, kuram iepriekš veicāt kompetenču iestatīšanu, un atveriet šī nodarbinātā ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b9156-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="b9156-113">Darbību rūts cilnē **Projekts**, grupā **Iestatījumi** atlasiet **Piešķirt projektus**.</span><span class="sxs-lookup"><span data-stu-id="b9156-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="b9156-114">Lapā **Resursa apstiprināšanas projektu piešķires**, cilnē **Projekti**, laukā **Pievienot projektu atlasītajiem projektiem** filtrējiet pēc projekta **XYZ jaunināšanas fāze 2**.</span><span class="sxs-lookup"><span data-stu-id="b9156-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="b9156-115">Rūtī **Atlikušie projekti** atlasiet kādu projektu un pēc tam atlasiet bultiņas pogu, lai to pievienotu rūtī **Atlasītie projekti**.</span><span class="sxs-lookup"><span data-stu-id="b9156-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="b9156-116">Ja nepieciešams, resursam varat piešķirt arī kategorijas.</span><span class="sxs-lookup"><span data-stu-id="b9156-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="b9156-117">Kategorijas tips ir **Izmaksas** vai **Ieņēmumi**.</span><span class="sxs-lookup"><span data-stu-id="b9156-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="b9156-118">Kategorijas tipu nosaka jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="b9156-118">The category type is determined by your organization.</span></span> <span data-ttu-id="b9156-119">Ja resursam nav piešķirta neviena kategorija, tad programmā Finance tiek uzmeklēta noklusējuma kategorija izmaksu un ieņēmumu stundu likmēm.</span><span class="sxs-lookup"><span data-stu-id="b9156-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="b9156-120">Projekta resursu un lomu īpašību iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b9156-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="b9156-121">Projekta vadītājs var izmantot projekta resursu sadalījuma funkcionalitāti, lai izveidotu lomas, kas nepieciešamas projektam.</span><span class="sxs-lookup"><span data-stu-id="b9156-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="b9156-122">Lomas var izmantot, ja resursu rezervēšanas laikā apstiprinātie resursi joprojām nav zināmi.</span><span class="sxs-lookup"><span data-stu-id="b9156-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="b9156-123">Lomas var uz laiku rezervēt kā ieplānotos resursus, lai varētu turpināt projekta plānošanas posmus.</span><span class="sxs-lookup"><span data-stu-id="b9156-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="b9156-124">[![Lomas piemērs](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="b9156-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="b9156-125">**Scenārijs:** Contoso tika nolīgts, lai pabeigtu laika un materiālu projektu, kuram ir apstiprināta projekta privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="b9156-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="b9156-126">Jaunākais projektu vadītājs joprojām strādā pie projekta darba apjoma pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="b9156-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="b9156-127">Resursu pārvaldnieks pašlaik norāda konkrētus resursus, kas tiks rezervēti darbam ar jauno projektu.</span><span class="sxs-lookup"><span data-stu-id="b9156-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="b9156-128">Tā kā attiecīgais projekts ir ļoti svarīgs, projekta sponsors kā vienu no lomām pieprasīja lomu Vecākais projektu vadītājs.</span><span class="sxs-lookup"><span data-stu-id="b9156-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="b9156-129">Resursu pārvaldniekam ir jāiegūst jaunais resurss un sistēmā jādefinē loma, lai tā būtu pieejama gadījumā, ja jaunākajam projektu vadītājam projekta plānošanas laikā ir nepieciešama resursa informācija.</span><span class="sxs-lookup"><span data-stu-id="b9156-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="b9156-130">Tālāk sniegtajos darbību aprakstos ir norādīts, kā resursu pārvaldnieks var iestatīt lomu Vecākais projektu vadītājs un piesaistīt tai resursa īpašības.</span><span class="sxs-lookup"><span data-stu-id="b9156-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="b9156-131">Pēc tam šo lomu var izmantot, lai meklētu pieejamos resursus, kas atbilst nepieciešamajām resursu kompetencēm.</span><span class="sxs-lookup"><span data-stu-id="b9156-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="b9156-132">Lapā **Lomu iestatīšana** atlasiet **Jauns** un ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="b9156-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b9156-133">**Lomas ID:** Vecākais projektu vadītājs</span><span class="sxs-lookup"><span data-stu-id="b9156-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="b9156-134">**Apraksts:** Vecākais projektu vadītājs</span><span class="sxs-lookup"><span data-stu-id="b9156-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="b9156-135">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="b9156-135">Select **Create**.</span></span>
3. <span data-ttu-id="b9156-136">Atlasiet lomu **Vecākais projektu vadītājs** un pēc tam atlasiet **Konfigurēt īpašības**.</span><span class="sxs-lookup"><span data-stu-id="b9156-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="b9156-137">Laukā **Īpašību veids** atlasiet **Prasme**.</span><span class="sxs-lookup"><span data-stu-id="b9156-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="b9156-138">Laukā **Pieejamās īpašības** ievadiet meklējamo prasmi.</span><span class="sxs-lookup"><span data-stu-id="b9156-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="b9156-139">Laukā **Īpašību veids** atlasiet **Sertifikāts**.</span><span class="sxs-lookup"><span data-stu-id="b9156-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="b9156-140">Laukā **Pieejamās īpašības** ievadiet meklējamo sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="b9156-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="b9156-141">Projekta resursa piešķiršana projektam</span><span class="sxs-lookup"><span data-stu-id="b9156-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="b9156-142">Lapā **Visi projekti** atlasiet projektu **XYZ jaunināšanas fāze 2**.</span><span class="sxs-lookup"><span data-stu-id="b9156-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="b9156-143">Cilnē **Projekta grupa un plānošana** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b9156-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="b9156-144">Laukā **Loma** atlasiet **Grupas dalībnieks**.</span><span class="sxs-lookup"><span data-stu-id="b9156-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="b9156-145">Atlasiet **Rezervēt no kalendāra**.</span><span class="sxs-lookup"><span data-stu-id="b9156-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="b9156-146">Lapā **Resursu pieejamība** atlasiet **Skata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b9156-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="b9156-147">Lapā **Pielāgojiet skata iestatījumus** ievadiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="b9156-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="b9156-148">**Datumu diapazona skata formāts:** Diena</span><span class="sxs-lookup"><span data-stu-id="b9156-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="b9156-149">**Parādīt pieejamības aprakstus:** Jā</span><span class="sxs-lookup"><span data-stu-id="b9156-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="b9156-150">**Rādīt atlikušo noslodzi:** Jā</span><span class="sxs-lookup"><span data-stu-id="b9156-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="b9156-151">Resursu sarakstā atlasiet resursu.</span><span class="sxs-lookup"><span data-stu-id="b9156-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="b9156-152">Atlasiet **Stingrā rezervēšana** un **Visa noslodze**.</span><span class="sxs-lookup"><span data-stu-id="b9156-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="b9156-153">Resursa piešķiršana noklusējuma lomai</span><span class="sxs-lookup"><span data-stu-id="b9156-153">Assign a resource to a default role</span></span>

<span data-ttu-id="b9156-154">Lai palīdzētu projektu vadītājiem vai resursu pārvaldniekiem, varat detalizētāk rādīt resursus, ko var rezervēt projektam.</span><span class="sxs-lookup"><span data-stu-id="b9156-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="b9156-155">Noklusējuma lomu var saistīt ar esošu resursu vai jauniegūtu resursu.</span><span class="sxs-lookup"><span data-stu-id="b9156-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="b9156-156">Piemēram, kad Rihards tika pieņemts darbā, viņa pieredze un prasmes bija piemērotas lomai Biznesa analītiķis.</span><span class="sxs-lookup"><span data-stu-id="b9156-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="b9156-157">Resursu pārvaldnieks piešķīra šo lomu kā Rihards noklusējuma lomu.</span><span class="sxs-lookup"><span data-stu-id="b9156-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="b9156-158">Tādējādi resursu pārvaldnieks pievienoja Danielu to biznesa analītiķu kopai, kuri ir pieejami darbam projektā.</span><span class="sxs-lookup"><span data-stu-id="b9156-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="b9156-159">Resursu rezervēšanas laikā projektu vadītāji var filtrēt lomu resursus, kas ir pieejami darbam projektos.</span><span class="sxs-lookup"><span data-stu-id="b9156-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="b9156-160">Viņi var izmantot šo informāciju kā vienu kritēriju, veicot vairāku kritēriju lēmumu analīzi resursu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="b9156-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="b9156-161">Viņi var pievienot arī citas resursa īpašības filtram, lai meklētu resursus, kuriem ir īpašas prasmes, izglītība un pieredze attiecīgajam projektam.</span><span class="sxs-lookup"><span data-stu-id="b9156-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="b9156-162">**Scenārijs:** ir uzsākts apstiprināts projekts, un loma Vecākais projektu vadītājs ir rezervēta kā ieplānots resurss projekta plānošanas posma laikā.</span><span class="sxs-lookup"><span data-stu-id="b9156-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="b9156-163">Resursu pārvaldnieks ir ieguvis resursu, lai aizpildītu lomu Vecākais projektu vadītājs.</span><span class="sxs-lookup"><span data-stu-id="b9156-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="b9156-164">Lapā **Resursu saraksts** atlasiet **Rihards Taurenis**.</span><span class="sxs-lookup"><span data-stu-id="b9156-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="b9156-165">Lapā **Resursa loma** atlasiet **Jauns** un ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="b9156-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b9156-166">**Ir spēkā:** ievadiet pašreizējo datumu.</span><span class="sxs-lookup"><span data-stu-id="b9156-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="b9156-167">**Termiņa beigas:** ievadiet **Nekad**.</span><span class="sxs-lookup"><span data-stu-id="b9156-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="b9156-168">**Loma:** ievadiet **Vecākais projektu vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="b9156-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="b9156-169">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="b9156-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="b9156-170">Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.</span><span class="sxs-lookup"><span data-stu-id="b9156-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
