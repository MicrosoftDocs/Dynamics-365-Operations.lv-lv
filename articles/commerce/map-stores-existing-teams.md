---
title: 'Kartējiet veikalus un grupas, ja programmā Microsoft Teams ir iepriekšējas darba grupas '
description: Šajā tēmā ir apskatīts, kā kartēt veikalus un attiecīgās komandas galvenajā Dynamics 365 Commerce birojā, ja jūsu organizācija jau ir izveidojusi grupas Microsoft Teams pirms Commerce integrācijas.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a711c1057b87bd792755ef91a84d1c28879c590
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908499"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="379ba-103">Kartējiet veikalus un grupas, ja programmā Microsoft Teams ir iepriekšējas darba grupas </span><span class="sxs-lookup"><span data-stu-id="379ba-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="379ba-104">Šajā tēmā ir apskatīts, kā kartēt veikalus un attiecīgās komandas galvenajā Dynamics 365 Commerce birojā, ja jūsu organizācija jau ir izveidojusi grupas Microsoft Teams pirms Commerce integrācijas.</span><span class="sxs-lookup"><span data-stu-id="379ba-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="379ba-105">Iespējams, jūsu organizācijai ir izveidotas grupas dažiem vai visiem veikaliem pirms integrēšanas Dynamics 365 Commerce un Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="379ba-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="379ba-106">Ja tā ir, lai izveidotu uzdevumu sinhronizāciju starp Commerce POS un Microsoft Teams ir jānodrošina veikalu un atbilstošo grupu kartēšana Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="379ba-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="379ba-107">Kartēt veikalus un atbilstošās grupas programmā Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="379ba-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="379ba-108">Lai kartētu veikalus un attiecīgās komandas Commerce Headquarters, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="379ba-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="379ba-109">Dodieties uz **Sistēmas administrēšana \> Darbvieta \> Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="379ba-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="379ba-110">Atlasiet **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="379ba-110">Select **Export**.</span></span> 
1. <span data-ttu-id="379ba-111">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="379ba-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="379ba-112">Sadaļā **Grupas nosaukums** ievadiet "Eksportēt Teams kartēšanu".</span><span class="sxs-lookup"><span data-stu-id="379ba-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="379ba-113">Kopsavilkuma cilnē **Atlasītās entītijas** atlasiet **Pievienot entītiju**.</span><span class="sxs-lookup"><span data-stu-id="379ba-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="379ba-114">Tiek parādīts dialoglodziņš **Pievienot entītiju**.</span><span class="sxs-lookup"><span data-stu-id="379ba-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="379ba-115">Nolaižamajā sarakstā **Entītijas nosaukums** atlasiet **Teams kartēšana starp avotu un grupu**.</span><span class="sxs-lookup"><span data-stu-id="379ba-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="379ba-116">Nolaižamajā sarakstā **Mērķa datu formāts** atlasiet **CSV**.</span><span class="sxs-lookup"><span data-stu-id="379ba-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="379ba-117">Atlasiet **Pievienot** un pēc tam atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="379ba-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="379ba-118">Augšējā kreisajā stūrī zem Darbību rūts atlasiet **Eksportēt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="379ba-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="379ba-119">Sadaļā **Elementa apstrādes statuss** atlasiet **Lejupielādēt failu**.</span><span class="sxs-lookup"><span data-stu-id="379ba-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="379ba-120">Eksportētā CSV failā ievadiet šādas **SOURCETYPE**, **SOURCEID** un **TEAMID** vērtības:</span><span class="sxs-lookup"><span data-stu-id="379ba-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="379ba-121">**SOURCETYPE** vērtībā ievadiet "RetailStore".</span><span class="sxs-lookup"><span data-stu-id="379ba-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="379ba-122">Ievadiet **SOURCEID** veikala numuru (piemēram, "000135", kas paredzēts Sanfrancisko veikalam).</span><span class="sxs-lookup"><span data-stu-id="379ba-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="379ba-123">Veikalu numurus var atrast **Mazumtirdzniecība un komercija \> Kanāli \> Veikali**.</span><span class="sxs-lookup"><span data-stu-id="379ba-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="379ba-124">Ja tiek lietots **TEAMID**, ievadiet atbilstošo grupas ID no Microsoft Teams (piemēram, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span><span class="sxs-lookup"><span data-stu-id="379ba-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="379ba-125">Grupas ID informāciju varat atrast [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="379ba-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="379ba-126">Saglabājiet CSV failu lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="379ba-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="379ba-127">Dodieties uz **Sistēmas administrēšana \> Darbvieta \> Datu pārvaldība** un atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="379ba-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="379ba-128">Kopsavilkuma cilnē **Atlasītās entītijas** atlasiet **Pievienot failu**.</span><span class="sxs-lookup"><span data-stu-id="379ba-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="379ba-129">Tiek parādīts dialoglodziņš **Pievienot failu**.</span><span class="sxs-lookup"><span data-stu-id="379ba-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="379ba-130">Nolaižamajā sarakstā **Entītijas nosaukums** atlasiet **Teams kartēšana starp avotu un grupu**.</span><span class="sxs-lookup"><span data-stu-id="379ba-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="379ba-131">Nolaižamajā sarakstā **Avota datu formāts** atlasiet **CSV**.</span><span class="sxs-lookup"><span data-stu-id="379ba-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="379ba-132">Atlasiet **Augšupielādēt un pievienot**, atlasiet iepriekš saglabāto CSV failu un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="379ba-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="379ba-133">Dialoglodziņā **Pievienot** atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="379ba-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="379ba-134">Darbības rūtī atlasiet **Saglabāt** un pēc tam atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="379ba-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="379ba-135">Nākamajā piemēra attēlā ir parādīta **Eksporta darba grupu kartēšanas** grupa programmā Commerce ar elementiem **Pievienot entītiju** un izceltas eksportēto CSV failu galvenes.</span><span class="sxs-lookup"><span data-stu-id="379ba-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Eksporta darba grupu kartēšanas grupa programmā Commerce ar entītijas pievienošanas elementiem un izceltām eksportēto CSV failu galvenēm](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="379ba-137">Pēc tam, kad esiet pabeidzis (-usi) precei pa solim, sekojiet soļiem [Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un POS](synchronize-tasks-teams-pos.md), lai sinhronizētu uzdevumu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="379ba-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="379ba-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="379ba-138">Additional resources</span></span>

[<span data-ttu-id="379ba-139">Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="379ba-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="379ba-140">Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="379ba-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="379ba-141">Nodrošināt Microsoft Teams no Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="379ba-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="379ba-142">Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="379ba-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="379ba-143">Lietotāju lomu pārvaldība Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="379ba-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="379ba-144">Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ</span><span class="sxs-lookup"><span data-stu-id="379ba-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
