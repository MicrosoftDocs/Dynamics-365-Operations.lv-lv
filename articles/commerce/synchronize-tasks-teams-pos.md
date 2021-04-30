---
title: Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS
description: Šajā tēmā ir aprakstīts, kā sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce pārdošanas punktu un pārdošanas punktu (POS).
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
ms.openlocfilehash: 3b4a9ad561e3bff67720a08d6e4184a81e01f734
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908273"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="40081-103">Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="40081-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="40081-104">Šajā tēmā ir aprakstīts, kā sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce pārdošanas punktu un pārdošanas punktu (POS).</span><span class="sxs-lookup"><span data-stu-id="40081-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="40081-105">Viens no Teams integrācijas galvenajiem nolūkiem ir iespējot uzdevumu pārvaldības sinhronizāciju starp POS programmu un Teams.</span><span class="sxs-lookup"><span data-stu-id="40081-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="40081-106">Šādā veidā veikala darbinieki uzdevumu pārvaldīšanai var izmantot vai nu POS programmu, vai Teams, un programmas nav jāpārslēdz.</span><span class="sxs-lookup"><span data-stu-id="40081-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="40081-107">Tā kā Plānotājs tiek izmantots kā brigādes uzdevumu repozitorijs, ir jābūt saitei starp Teams un Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40081-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="40081-108">Šī saite ir izveidota, izmantojot noteiktai veikala grupai noteiktu plāna ID.</span><span class="sxs-lookup"><span data-stu-id="40081-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="40081-109">Šīs procedūras parāda, kā iestatīt uzdevumu pārvaldības sinhronizāciju starp POS un Teams programmām.</span><span class="sxs-lookup"><span data-stu-id="40081-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="40081-110">Publicēt pārbaudes uzdevumu sarakstu Teams</span><span class="sxs-lookup"><span data-stu-id="40081-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="40081-111">Šajā procedūrā tiek pieņemts, ka jūsu veikalu grupas Microsoft Teams pirmo reizi izmanto uzdevumu pārvaldības integrāciju ar Commerce.</span><span class="sxs-lookup"><span data-stu-id="40081-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="40081-112">Lai publicētu pārbaudes uzdevumu sarakstu Teams, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="40081-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="40081-113">Piesakieties Teams kā saziņas pārvaldītājs.</span><span class="sxs-lookup"><span data-stu-id="40081-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="40081-114">Parasti saziņas vadītāji ir lietotāji, kuriem ir Loma **Reģionā pārvaldnieka** programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="40081-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="40081-115">Navigācijas rūtī pa kreisi atlasiet **Uzdevumi pēc plānotāja**.</span><span class="sxs-lookup"><span data-stu-id="40081-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="40081-116">Cilnē **Publicētie saraksti** apakšējā kreisajā pusē atlasiet **Jauns saraksts** un nosauciet jauno sarakstu **Testa uzdevumu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="40081-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="40081-117">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="40081-117">Select **Create**.</span></span> <span data-ttu-id="40081-118">Jaunais saraksts tiek parādīts zem **Melnraksti**.</span><span class="sxs-lookup"><span data-stu-id="40081-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="40081-119">Zem **Uzdevuma nosaukums** piešķiriet pirmajam uzdevumam nosaukumu **Teams integrācijas testēšana**.</span><span class="sxs-lookup"><span data-stu-id="40081-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="40081-120">Pēc tam atlasiet **Ievadīt**.</span><span class="sxs-lookup"><span data-stu-id="40081-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="40081-121">**Melnrakstu** sarakstā izvēlieties uzdevumu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="40081-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="40081-122">Pēc tam augšējā labajā stūrī atlasiet  **Publicēt** .</span><span class="sxs-lookup"><span data-stu-id="40081-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="40081-123">Dialoglodziņā **Atlasīt, kas tiks publicēts** dialoglodziņā atlasiet grupas, kurām jāsaņem testa uzdevumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="40081-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="40081-124">Atlasiet **Tālāk**, lai pārskatītu publicēšanas plānu.</span><span class="sxs-lookup"><span data-stu-id="40081-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="40081-125">Ja jāveic izmaiņas, atlasiet  **Atpakaļ**.</span><span class="sxs-lookup"><span data-stu-id="40081-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="40081-126">Atlasiet **Apstiprināt**, lai turpinātu, un pēc tam atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="40081-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="40081-127">Pēc publicēšanas pabeigšanas ziņojums **Publicēto sarakstu** cilnes augšpusē norāda, vai uzdevumu saraksts ir veiksmīgi piegādāts.</span><span class="sxs-lookup"><span data-stu-id="40081-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="40081-128">Papildinformāciju skatiet sadaļā [Uzdevumu sarakstu publicēšana, lai izveidotu un izsekotu darbu uzņēmumā](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="40081-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="40081-129">Saistīt POS un Teams uzdevumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="40081-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="40081-130">Lai programmā Commerce Headquarters saistītu POS un Microsoft Teams uzdevumu pārvaldībai, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="40081-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="40081-131">Ejiet uz **Mazumtirdzniecība un komercija \> Uzdevumu pārvaldība \> Uzdevumu integrācija ar Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="40081-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="40081-132">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="40081-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="40081-133">Iestatiet opciju **Iespējot Uzdevumu pārvaldības integrāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="40081-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="40081-134">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="40081-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="40081-135">Darbību rūtī atlasiet **Iestatīšanas uzdevumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="40081-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="40081-136">Jums jāsaņem paziņojums, kas norāda, ka tiek izveidots pakešuzdevums ar nosaukumu **Teams nodrošināšana**.</span><span class="sxs-lookup"><span data-stu-id="40081-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="40081-137">Dodieties uz **Sistēmas administrēšana \> Uzziņas \> Pakešdarbi** un atrodiet pēdējo darbu ar aprakstu **Teams nodrošināšana**.</span><span class="sxs-lookup"><span data-stu-id="40081-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="40081-138">Uzgaidiet, kamēr šis darbs tiks pabeigts.</span><span class="sxs-lookup"><span data-stu-id="40081-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="40081-139">Palaidiet **CDX darbu 1070**, lai publicētu plāna ID un veikala atsauces uz mazumtirdzniecības serveri.</span><span class="sxs-lookup"><span data-stu-id="40081-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40081-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="40081-140">Additional resources</span></span>

[<span data-ttu-id="40081-141">Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="40081-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="40081-142">Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju</span><span class="sxs-lookup"><span data-stu-id="40081-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="40081-143">Nodrošināt Microsoft Teams no Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="40081-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="40081-144">Lietotāju lomu pārvaldība Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="40081-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="40081-145">Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="40081-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="40081-146">Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ</span><span class="sxs-lookup"><span data-stu-id="40081-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
