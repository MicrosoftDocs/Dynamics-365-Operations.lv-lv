---
title: Ievadīt prasmes
description: Darbi un vadītāji var ievadīt prasmes programmā Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193981"
---
# <a name="enter-skills"></a><span data-ttu-id="5ae4e-103">Ievadīt prasmes</span><span class="sxs-lookup"><span data-stu-id="5ae4e-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5ae4e-104">Darbiniekiem, kandidātiem vai kontaktpersonām varat ievadīt mērķa prasmes vai faktiskās prasmes programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5ae4e-105">Mērķa prasme ir prasme, ko persona plāno sasniegt.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="5ae4e-106">Faktiskā prasme ir prasme, kas personai piemīt pašlaik.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="5ae4e-107">Izveidot darbplūsmu, lai automātiski apstiprinātu prasmes</span><span class="sxs-lookup"><span data-stu-id="5ae4e-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="5ae4e-108">Lai ievadītu prasmes bez apstiprinājuma, jāizveido darbplūsma, lai automātiski apstiprinātu prasmes.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="5ae4e-109">Darbinieku ievadītās prasmes vienmēr pieprasa vadītāja apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="5ae4e-110">Šī darbplūsma automātiski apstiprina tikai tās prasmes, ko ievada vadītāji savu darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="5ae4e-111">Darbvietā **Personāla vadība** atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="5ae4e-112">Sadaļā **Iestatījumi** atlasiet **Personāla vadības darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="5ae4e-113">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-113">Select **New**.</span></span>

4. <span data-ttu-id="5ae4e-114">Darbības rūtī **Izveidot darbplūsmu** atlasiet **Darbinieka prasmes**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="5ae4e-115">[![Atlasīt Darbinieka prasmju darbplūsmu](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="5ae4e-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="5ae4e-116">Dialoglodziņā **Atvērt šo failu?** atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="5ae4e-117">Kad tiek piedāvāts, ievadiet savus akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="5ae4e-118">Darbplūsmas redaktorā atlasiet darbplūsmas elementu **Apstiprināt prasmes** un velciet to uz kanvu.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="5ae4e-119">[![Atlasīt Apstiprināt prasmes darbplūsmas elementu](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="5ae4e-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="5ae4e-120">Saistiet **Sākuma** elementu ar **Apstiprināt prasmes 1** elementu un pēc tam saistiet **Apstiprināt prasmes 1** elementu ar **Beigu** elementu.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="5ae4e-121">Jums var būt nepieciešams ritināt uz leju, lai skatītu **Beigu** elementu.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="5ae4e-122">Varat to vilkt tuvāk citiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="5ae4e-123">[![Saistīt darbplūsmas elementus](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="5ae4e-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="5ae4e-124">Veiciet dubultklikšķi uz **Apstiprināt prasmes 1** darbplūsmas elementu, un pēc tam ar peles labo pogu noklikšķiniet uz **1. solis** elementu.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="5ae4e-125">Ar peles labo pogu noklikšķiniet uz elementu **1. solis** un pēc tam atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="5ae4e-126">Logā **Rekvizīti** atlasiet **Nosacījums**, kas atrodas kreisās puses navigācijas joslā.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="5ae4e-127">Atlasiet **Izpildīt šo soli, ja ir spēkā šāds nosacījums**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="5ae4e-128">Atlasīt **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-128">Select **Add condition**.</span></span> <span data-ttu-id="5ae4e-129">Pēc **Kur** atlasiet **Darbinieku pašapkalpošanās prasmes**, un pēc tam atlasiet **Darbinieku pašapkalpošanās prasmes.Persona**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="5ae4e-130">Pēc **ir** atlasiet **lauku** un pēc tam atlasiet **Lietotāja attiecības ar personu.Persona**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="5ae4e-131">[![Norādīt nosacījumu](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="5ae4e-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="5ae4e-132">Atlasiet **Piešķire** navigācijas joslā pa kreisi.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="5ae4e-133">Cilnē **Piešķires tips** atlasiet **Hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="5ae4e-134">Cilnes **Hierarhijas atlase** laukā **Hierarhijas tips:** atlasiet **Vadības hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="5ae4e-135">[![Norādīt vadības hierarhiju](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="5ae4e-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="5ae4e-136">Atlasiet **Aizvērt**, atlasiet **Darbplūsma** kanvas navigācijā un pēc tam atlasiet **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="5ae4e-137">Lai iegūtu vairāk informācijas par darbplūsmu izveidi, skatiet [Darbplūsmas sistēmas apskats](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="5ae4e-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="5ae4e-138">Ievadīt darbinieka prasmes</span><span class="sxs-lookup"><span data-stu-id="5ae4e-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="5ae4e-139">Atlasīt darbinieku.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-139">Select a worker.</span></span>

2. <span data-ttu-id="5ae4e-140">Lapas **Darbinieks** darbību joslā atlasiet **Persona** un pēc tam atlasiet **Prasmes**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="5ae4e-141">Lapā **Prasmes** aizpildiet šādus laukus katrai prasmei:</span><span class="sxs-lookup"><span data-stu-id="5ae4e-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="5ae4e-142">**Prasme**: atlasiet prasmi.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="5ae4e-143">**Līmeņa tips**: atlasiet **Faktiski** prasmei, kas darbiniekam jau ir, vai atlasiet **Mērķis** prasmei, uz kuru darbinieks strādā.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="5ae4e-144">**Līmenis**: atlasiet līmeni darbinieka prasmēm.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="5ae4e-145">**Līmeņa datums**: atlasiet datumu, noklikšķiniet uz kalendāra rīku.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="5ae4e-146">**Eksaminētājs**: ja nepieciešams, atlasiet eksaminētāju no saraksta.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="5ae4e-147">Savu meklēšanu var filtrēt.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-147">You can filter your search.</span></span>
   - <span data-ttu-id="5ae4e-148">**Gadu pieredze**: ievadiet pieredzes gadus.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="5ae4e-149">**Pārbaudīts**: ja prasme ir pārbaudīta, atzīmējiet izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="5ae4e-150">**Pārbaudīja**: ievadiet pārbaudītāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="5ae4e-151">Kad prasmes ir ievadītas, atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ae4e-152">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="5ae4e-152">See also</span></span>

[<span data-ttu-id="5ae4e-153">Konfigurēt prasmes</span><span class="sxs-lookup"><span data-stu-id="5ae4e-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="5ae4e-154">Kartēt prasmes</span><span class="sxs-lookup"><span data-stu-id="5ae4e-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]