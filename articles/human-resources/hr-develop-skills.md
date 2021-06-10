---
title: Konfigurēt prasmes
description: Varat izsekot darbinieka prasmes programmā Dynamics 365 Human Resources. Varat arī norādīt prasmes, kas ir nepieciešamas konkrētam darbam.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076563"
---
# <a name="configure-skills"></a><span data-ttu-id="bd052-104">Konfigurēt prasmes</span><span class="sxs-lookup"><span data-stu-id="bd052-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bd052-105">Varat izsekot darbinieka prasmes programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bd052-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bd052-106">Varat arī norādīt prasmes, kas ir nepieciešamas konkrētam darbam.</span><span class="sxs-lookup"><span data-stu-id="bd052-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="bd052-107">Izsekojamo prasmju piemēri ietver:</span><span class="sxs-lookup"><span data-stu-id="bd052-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="bd052-108">Supervizora — spēja uzraudzīt citu darbu.</span><span class="sxs-lookup"><span data-stu-id="bd052-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="bd052-109">Vadības — spēja vadīt darbiniekus un uzņēmuma domēnus.</span><span class="sxs-lookup"><span data-stu-id="bd052-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="bd052-110">Plānošanas — spēja raudzīties nākotnē, formulēt redzējumu paziņojumus un īstenot tos dzīvē.</span><span class="sxs-lookup"><span data-stu-id="bd052-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="bd052-111">HTML — spēja rakstīt HTML kodu.</span><span class="sxs-lookup"><span data-stu-id="bd052-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="bd052-112">Ja vēl neesat iestatījis prasmju tipus un novērtējuma modeļus, daži ir jāpievieno pirms prasmju izveides.</span><span class="sxs-lookup"><span data-stu-id="bd052-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="bd052-113">Tālāk norādītās personas var ievadīt darbinieka prasmes:</span><span class="sxs-lookup"><span data-stu-id="bd052-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="bd052-114">Darbinieki var ievadīt prasmes paši Darbinieku pašapkalpošanās sistēmā.</span><span class="sxs-lookup"><span data-stu-id="bd052-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="bd052-115">Šīm prasmēm nepieciešams vadītāja apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="bd052-115">These skills require manager approval.</span></span>
- <span data-ttu-id="bd052-116">Vadītāji var ievadīt darbinieku prasmes.</span><span class="sxs-lookup"><span data-stu-id="bd052-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="bd052-117">Varat izveidot darbplūsmu, kas automātiski apstiprina šīs prasmes.</span><span class="sxs-lookup"><span data-stu-id="bd052-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="bd052-118">Prasmes tipa izveide</span><span class="sxs-lookup"><span data-stu-id="bd052-118">Create a skill type</span></span>

<span data-ttu-id="bd052-119">Prasmju tipi ir kategorijas, kurās ietilpst atsevišķas prasmes, piemēram, Administrēšana vai Pārdošana.</span><span class="sxs-lookup"><span data-stu-id="bd052-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="bd052-120">**Darbinieku attīstības** darbvietā atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="bd052-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="bd052-121">Zem **Kompetences iestatījumiem** atlasiet **Prasmju tipi**.</span><span class="sxs-lookup"><span data-stu-id="bd052-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="bd052-122">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bd052-122">Select **New**.</span></span>

4. <span data-ttu-id="bd052-123">Aizpildiet tālāk aprakstītos laukus:</span><span class="sxs-lookup"><span data-stu-id="bd052-123">Complete the following fields:</span></span>

   - <span data-ttu-id="bd052-124">**Prasmju tips**: ievadiet prasmju tipa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bd052-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="bd052-125">**Apraksts**: ievadiet prasmju tipa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="bd052-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="bd052-126">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bd052-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="bd052-127">Izveidot vērtēšanas modeli</span><span class="sxs-lookup"><span data-stu-id="bd052-127">Create a rating model</span></span>

<span data-ttu-id="bd052-128">Vērtēšanas modeļi palīdz novērtēt personas faktisko prasmju līmeni, to prasmju līmeni, ko šai personai būtu jācenšas sasniegt, vai prasmju līmeni, kas ir nepieciešams darbam.</span><span class="sxs-lookup"><span data-stu-id="bd052-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="bd052-129">Katram līmenim vērtēšanas modelī tiek piešķirts koeficients.</span><span class="sxs-lookup"><span data-stu-id="bd052-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="bd052-130">**Darbinieku attīstības** darbvietā atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="bd052-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="bd052-131">Zem **Kompetences iestatījumiem** atlasiet **Vērtēšanas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="bd052-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="bd052-132">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bd052-132">Select **New**.</span></span>

4. <span data-ttu-id="bd052-133">Aizpildiet tālāk aprakstītos laukus:</span><span class="sxs-lookup"><span data-stu-id="bd052-133">Complete the following fields:</span></span>

   - <span data-ttu-id="bd052-134">**Vērtējums**: ievadiet vērtēšanas modeļa nosaukumu, piemēram, **Prasmes**.</span><span class="sxs-lookup"><span data-stu-id="bd052-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="bd052-135">**Apraksts**: ievadiet vērtēšanas modeļa aprakstu, piemēram, **Prasmju novērtējumi**.</span><span class="sxs-lookup"><span data-stu-id="bd052-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="bd052-136">Sadaļā **Līmeņi** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bd052-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="bd052-137">Katram līmenim, kuru vēlaties pievienot, aizpildiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="bd052-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="bd052-138">**Līmenis**: ievadiet līmeņa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bd052-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="bd052-139">**Apraksts**: ievadiet līmeņa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="bd052-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="bd052-140">**Koeficients**: ievadiet koeficienta vērtību no 0 līdz 9.</span><span class="sxs-lookup"><span data-stu-id="bd052-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="bd052-141">Koeficienti palīdz normalizēt rādītājus prasmēm, kas izmanto dažādu vērtēšanas modeļus.</span><span class="sxs-lookup"><span data-stu-id="bd052-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="bd052-142">Katram līmenim jābūt unikālam koeficentam.</span><span class="sxs-lookup"><span data-stu-id="bd052-142">Each level must have a unique factor.</span></span> <span data-ttu-id="bd052-143">Līmeņiem ar augstākām koeficienta vērtībām ir lielāka nozīme vērtēšanas modelī.</span><span class="sxs-lookup"><span data-stu-id="bd052-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="bd052-144">Ja nepieciešams, turpiniet pievienot līmeņus.</span><span class="sxs-lookup"><span data-stu-id="bd052-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="bd052-145">Katram vērtējuma modelim var ievadīt ne vairāk kā 10 līmeņus.</span><span class="sxs-lookup"><span data-stu-id="bd052-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="bd052-146">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bd052-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="bd052-147">Prasmes izveide</span><span class="sxs-lookup"><span data-stu-id="bd052-147">Create a skill</span></span>

<span data-ttu-id="bd052-148">Lai varētu piešķirt kādu prasmi vai izveidot prasmju kartēšanas meklēšanu vai prasmju profilu, par šīm prasmēm ir jāievada informācija lapā **Prasmes**.</span><span class="sxs-lookup"><span data-stu-id="bd052-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="bd052-149">Katrai prasmei varat atlasīt prasmju tipu un vērtēšanas modeli.</span><span class="sxs-lookup"><span data-stu-id="bd052-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="bd052-150">**Darbinieku attīstības** darbvietā atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="bd052-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="bd052-151">Zem **Kompetences iestatījumiem** atlasiet **Prasmes**.</span><span class="sxs-lookup"><span data-stu-id="bd052-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="bd052-152">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bd052-152">Select **New**.</span></span>

4. <span data-ttu-id="bd052-153">Aizpildiet tālāk aprakstītos laukus:</span><span class="sxs-lookup"><span data-stu-id="bd052-153">Complete the following fields:</span></span>

   - <span data-ttu-id="bd052-154">**Prasme**: ievadiet prasmes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bd052-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="bd052-155">**Apraksts**: ievadiet prasmes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="bd052-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="bd052-156">**Vērtējums**: atlasiet vērtējuma modeli, ko vēlaties izmantot šai prasmei.</span><span class="sxs-lookup"><span data-stu-id="bd052-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="bd052-157">**Prasmes tips**: atlasiet no prasmju tipu saraksta.</span><span class="sxs-lookup"><span data-stu-id="bd052-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="bd052-158">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bd052-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd052-159">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="bd052-159">See also</span></span>

[<span data-ttu-id="bd052-160">Ievadīt prasmes</span><span class="sxs-lookup"><span data-stu-id="bd052-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="bd052-161">Kartēt prasmes</span><span class="sxs-lookup"><span data-stu-id="bd052-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]