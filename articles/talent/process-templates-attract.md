---
title: Procesa veidnes izveidošana programmā Attract
description: Šajā tēmā ir sniegta inf. par to, kā izveidot procesa veidni programmā Attract.
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 2b9cac68093be65584192757229c20b1a1546342
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2019
ms.locfileid: "305313"
---
# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="066ca-103">Procesa veidnes izveidošana programmā Attract</span><span class="sxs-lookup"><span data-stu-id="066ca-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="066ca-104">*Darbā pieņemšanas procesa veidnē* ir visas aktivitātes, kas ir jāietver kādas vakances darbā pieņemšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="066ca-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="066ca-105">Šajā tēmā ir aprakstīti procesa veidnes elementi programmā Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="066ca-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="066ca-106">Tajā ir arī paskaidrots, kā izveidot veidni.</span><span class="sxs-lookup"><span data-stu-id="066ca-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="066ca-107">Veidnes izveidošana veido daļu no visaptverošās darbā pieņemšanas pievienojumprogrammas programmai Attract.</span><span class="sxs-lookup"><span data-stu-id="066ca-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="066ca-108">Veidņu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="066ca-108">Template management</span></span>

<span data-ttu-id="066ca-109">Organizācijas var izlemt, vai procesu veidnes programmā Attract var izveidot darba grupas dalībnieki vai tikai administratori.</span><span class="sxs-lookup"><span data-stu-id="066ca-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="066ca-110">Lai konfigurētu veidņu pārvaldību, dodieties uz **Administrēšanas centrs** \> **Veidņu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="066ca-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="066ca-111">Lai ļautu darba grupas dalībniekiem veidot pašiem savas veidnes, ieslēdziet veidņu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="066ca-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="066ca-112">Ja neieslēdzat veidņu pārvaldību, veidnes var izveidot tikai administratori.</span><span class="sxs-lookup"><span data-stu-id="066ca-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="066ca-113">Noklusējuma veidne</span><span class="sxs-lookup"><span data-stu-id="066ca-113">Default template</span></span>

<span data-ttu-id="066ca-114">Noklusējuma veidni var iestatīt tikai administratori.</span><span class="sxs-lookup"><span data-stu-id="066ca-114">Only admins can set the default template.</span></span> <span data-ttu-id="066ca-115">Noklusējuma veidne tiek lietota, ja darba veidošanas laikā nav atlasīta neviena veidne.</span><span class="sxs-lookup"><span data-stu-id="066ca-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="066ca-116">Lai iestatītu noklusējuma veidni, dodieties uz **Administrēšanas centrs** \> **Veidņu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="066ca-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="066ca-117">Veidnei, kuru vēlaties izmantot kā noklusējuma veidni, veidnes kartītē atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Iestatīt kā noklusējumu**.</span><span class="sxs-lookup"><span data-stu-id="066ca-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="066ca-118">Procesa veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="066ca-118">Create a process template</span></span>

<span data-ttu-id="066ca-119">Procesu veidnes var izveidot administratori, personāla atlases darbinieki un par pieņemšanu darbā atbildīgie vadītāji.</span><span class="sxs-lookup"><span data-stu-id="066ca-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="066ca-120">Procesa veidni veido *posmi* un *aktivitātes*.</span><span class="sxs-lookup"><span data-stu-id="066ca-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="066ca-121">Posmos tiek grupētas viena vai vairākas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="066ca-121">Stages group together one or more activities.</span></span> <span data-ttu-id="066ca-122">Pēc noklusējuma ikvienai procesa veidnei ir aktivitātes Potenciālais klients, Pieteikums un Piedāvājums.</span><span class="sxs-lookup"><span data-stu-id="066ca-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="066ca-123">Posmus, kuros ir šīs aktivitātes, var pārdēvēt.</span><span class="sxs-lookup"><span data-stu-id="066ca-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="066ca-124">Varat pievienot papildu posmus, atlasot **+ Jauns posms**.</span><span class="sxs-lookup"><span data-stu-id="066ca-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="066ca-125">Aktivitātes posmam varat pievienot, tās velkot uz atbilstošo posmu vai veicot dubultklikšķi uz attiecīgajām aktivitātēm aktivitāšu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="066ca-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="066ca-126">Posmu nosaukumi kandidātiem ir redzami lapā **Pieteikuma statuss**.</span><span class="sxs-lookup"><span data-stu-id="066ca-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="066ca-127">Šo faktu jums vajadzētu ņemt vērā, kad izvēlaties posmu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="066ca-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="066ca-128">Plašāku informāciju par aktivitātēm skatiet šeit: [Darbā pieņemšanas procesa aktivitātes pakalpojumā Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="066ca-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="066ca-129">Lai izveidotu darbā pieņemšanas procesa veidni, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="066ca-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="066ca-130">Dodieties uz **Veidnes**.</span><span class="sxs-lookup"><span data-stu-id="066ca-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="066ca-131">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="066ca-131">Select **New**.</span></span>
3. <span data-ttu-id="066ca-132">Laukā **Veidnes nosaukums** ievadiet nosaukumu šai veidnei un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="066ca-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="066ca-133">Sarakstā **Izvēlēties apstiprināšanas procesu** atlasiet **Noklusējums**, lai darbam pieprasītu apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="066ca-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="066ca-134">Atlasiet iespējot vai atspējot potenciālos darba ņēmējus.</span><span class="sxs-lookup"><span data-stu-id="066ca-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="066ca-135">Neobligāti: pievienojiet vai noņemiet posmus.</span><span class="sxs-lookup"><span data-stu-id="066ca-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="066ca-136">Lai pievienotu posmu, atlasiet **+ jauns posms**.</span><span class="sxs-lookup"><span data-stu-id="066ca-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="066ca-137">Lai noņemtu kādu posmu, virziet peles rādītāju pār attiecīgo posmu un pēc tam atlasiet parādīto atkritnes pogu.</span><span class="sxs-lookup"><span data-stu-id="066ca-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="066ca-138">Posmus Potenciālais klients, Pieteikums un Piedāvājums nevar noņemt, bet tos var pārdēvēt.</span><span class="sxs-lookup"><span data-stu-id="066ca-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="066ca-139">Neobligāti: pievienojiet vai noņemiet aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="066ca-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="066ca-140">Lai pievienotu kādu aktivitāti, no aktivitāšu saraksta labajā pusē velciet to uz atbilstošo posmu.</span><span class="sxs-lookup"><span data-stu-id="066ca-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="066ca-141">Vai arī veiciet dubultklikšķi uz aktivitātes un pēc tam atlasiet posmu, kuram to pievienot.</span><span class="sxs-lookup"><span data-stu-id="066ca-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="066ca-142">Lai noņemtu kādu aktivitāti, izvērsiet to un pēc tam atlasiet atkritnes pogu šīs aktivitātes galvenē.</span><span class="sxs-lookup"><span data-stu-id="066ca-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="066ca-143">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="066ca-143">Select **Save**.</span></span>
