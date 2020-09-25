---
title: Projekta grupas izveide
description: Šajā sadaļā ir sniegta informācija par to, kā izveidot un pārvaldīt projekta grupas.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760604"
---
# <a name="create-a-project-team"></a><span data-ttu-id="e071c-103">Projekta grupas izveide</span><span class="sxs-lookup"><span data-stu-id="e071c-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e071c-104">Lai lietotu lomas, kas iepriekš tika iestatītas projektā, projektu vadītājam šīs lomas ir jāsaista ar projektu.</span><span class="sxs-lookup"><span data-stu-id="e071c-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="e071c-105">Projektam var piešķirt vairākas lomas.</span><span class="sxs-lookup"><span data-stu-id="e071c-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="e071c-106">Lai nerastos pārpratumi, rezervēšanas laikā šīm lomām etiķetes tiek piešķirtas automātiski.</span><span class="sxs-lookup"><span data-stu-id="e071c-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="e071c-107">Piemēram, ja projektu vadītājam ir nepieciešami trīs programmatūras inženieri, tiek automātiski ģenerētas trīs lomas Programmatūras inženieris, kuru etiķetes ir **1. programmatūras inženieris**, **2. programmatūras inženieris** un **3. programmatūras inženieris**.</span><span class="sxs-lookup"><span data-stu-id="e071c-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="e071c-108">Ja lomai iepriekš tika iestatītas lomas īpašības, tās tiek pielietotas kā filtrs resursu meklēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="e071c-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="e071c-109">Lai precizētu meklēšanu, nepieciešamības gadījumā var pievienot papildu īpašības.</span><span class="sxs-lookup"><span data-stu-id="e071c-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="e071c-110">Skata iestatījumus arī var pielāgot, lai nodrošinātu labāku pārskatu par resursu pieejamību.</span><span class="sxs-lookup"><span data-stu-id="e071c-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="e071c-111">Ir pieejamas iespējas stundu, dienu, nedēļu, ceturkšņu un gada pieejamības attēlošanai.</span><span class="sxs-lookup"><span data-stu-id="e071c-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="e071c-112">Pastāv arī iespēja rādīt pieejamo un atlikušo resursu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="e071c-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="e071c-113">Šī opcija ir noderīga laika pārvaldībai, kad novērtējat darbībām pieejamo laiku vai resursu pieejamību.</span><span class="sxs-lookup"><span data-stu-id="e071c-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="e071c-114">Projektu vadītājs var lapā atlasīt lomu un pēc tam, ja ir pieejams resurss, kas atbilst vajadzībai, viņš var rezervēt resursu šai lomai.</span><span class="sxs-lookup"><span data-stu-id="e071c-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="e071c-115">Ņemiet vērā, ka šajā plānošanas posmā resursi nav jārezervē.</span><span class="sxs-lookup"><span data-stu-id="e071c-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="e071c-116">Veidojot WBS, lomas var aizstāt ar projekta personāla resursiem.</span><span class="sxs-lookup"><span data-stu-id="e071c-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="e071c-117">Ja WBS ietvaros lomas tiek aizstātas ar personāla resursiem, resursu iestatījumos tiek automātiski atjaunināts projekta grupas saraksts un plānošana.</span><span class="sxs-lookup"><span data-stu-id="e071c-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="e071c-118">[![Projekta grupas saraksts, kurā ir ietvertas gan lomas, gan faktiskie resursi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="e071c-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="e071c-119">Projektu vadītājam ir dažādas iespējas projekta resursu rezervācijai, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes procentuālā daļa** un **Norādiet stundas**.</span><span class="sxs-lookup"><span data-stu-id="e071c-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="e071c-120">Šīs rezervēšanas iespējas var atcelt jebkurā laikā, ja mainās resursu piešķires.</span><span class="sxs-lookup"><span data-stu-id="e071c-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="e071c-121">Tiek atbalstīti divi rezervāciju tipi:</span><span class="sxs-lookup"><span data-stu-id="e071c-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="e071c-122">**Stingrā rezervācija** – resursa rezervācija ir apstiprināta darbam attiecīgajā iesaistē uz norādīto laiku.</span><span class="sxs-lookup"><span data-stu-id="e071c-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="e071c-123">**Vieglā rezervēšana** – resursu rezervācijas ir uz laiku iestatītas darbam attiecīgajā iesaistē uz norādīto laiku.</span><span class="sxs-lookup"><span data-stu-id="e071c-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="e071c-124">Tālāk esošajā procedūrā izskaidrots, kā izveidot projekta grupu.</span><span class="sxs-lookup"><span data-stu-id="e071c-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="e071c-125">Projekta grupas izveide</span><span class="sxs-lookup"><span data-stu-id="e071c-125">Create a project team</span></span>

1. <span data-ttu-id="e071c-126">Saraksta lapā **Visi projekti** atlasiet kādu projektu un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="e071c-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="e071c-127">Cilnes **Projekta grupa un plānošana** laukā **Grafika beigu datums** ievadiet grafika sākuma datumu, kam ir pieskaitīts viens mēnesis.</span><span class="sxs-lookup"><span data-stu-id="e071c-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="e071c-128">Piemēram, ja grafika sākuma datums ir 2017. gada 24. jūnijs (24/06/2017), ievadiet **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="e071c-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="e071c-129">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e071c-129">Select **Add**.</span></span>
4. <span data-ttu-id="e071c-130">Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Vecākais projektu vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="e071c-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="e071c-131">Atlasiet **Nepieciešamās kompetences**.</span><span class="sxs-lookup"><span data-stu-id="e071c-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="e071c-132">Lapā **Īpašību izvēle** īpašības, ko iepriekš iestatījāt lomai Vecākais projektu vadītājs, tiek atlasītas pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="e071c-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="e071c-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e071c-133">Select **OK**.</span></span>
7. <span data-ttu-id="e071c-134">Lapas **Pievienot projekta lomas** laukā **Resursu skaits** ievadiet **1**.</span><span class="sxs-lookup"><span data-stu-id="e071c-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="e071c-135">Laukā **Resursi** uzmeklēšana parāda visus resursus, kuriem ir nepieciešamās kompetences.</span><span class="sxs-lookup"><span data-stu-id="e071c-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="e071c-136">Atlasiet **Rihards Taurenis** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="e071c-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="e071c-137">Lapā **Projekts** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e071c-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="e071c-138">Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Grupas dalībnieks**.</span><span class="sxs-lookup"><span data-stu-id="e071c-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="e071c-139">Laukā **Resursu skaits** ievadiet **5**.</span><span class="sxs-lookup"><span data-stu-id="e071c-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="e071c-140">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="e071c-140">Select **Create**.</span></span>
12. <span data-ttu-id="e071c-141">Lapā **Projekti** atlasiet **Izpildīt resursu**.</span><span class="sxs-lookup"><span data-stu-id="e071c-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="e071c-142">Projektu grupu pārraudzība</span><span class="sxs-lookup"><span data-stu-id="e071c-142">Monitor project teams</span></span>
1. <span data-ttu-id="e071c-143">Lapā **Visi projekti** atlasiet saiti **Projekta ID** projektam **XYZ jaunināšanas fāze 2**.</span><span class="sxs-lookup"><span data-stu-id="e071c-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="e071c-144">Kopsavilkuma cilnē **Projekta grupa un plānošana** pārbaudiet, vai minētie projekta resursi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="e071c-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
