---
title: Integrācija ar LinkedIn Talent Hub
description: Šajā tēmā ir paskaidrots, kā iestatīt pintegrāciju starp Microsoft Dynamics 365 Human Resources un LinkedIn Talent Hub.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fda9d85b459d233e6239f3fcffbb48e596d4085
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113475"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="38ca9-103">Integrācija ar LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="38ca9-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="38ca9-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) ir kandidātu izsekošanas sistēmas (ATS) platforma.</span><span class="sxs-lookup"><span data-stu-id="38ca9-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="38ca9-105">Tā ļauj jums izveidot, pārvaldīt un nolīgt darbiniekus vienuviet.</span><span class="sxs-lookup"><span data-stu-id="38ca9-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="38ca9-106">Integrējot Microsoft Dynamics 365 Human Resources ar LinkedIn Talent Hub, varat viegli izveidot darbinieku ierakstus Human Resources kandidātiem, kuri ir nolīgti amatam.</span><span class="sxs-lookup"><span data-stu-id="38ca9-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="38ca9-107">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="38ca9-107">Setup</span></span>

<span data-ttu-id="38ca9-108">Sistēmas administratoram ir jāaizpilda iestatījumi, lai iespējotu integrāciju ar LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="38ca9-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="38ca9-109">Vispirms Power Apps vidē jums ir jāiestata lietotājs un drošības loma, lai piešķirtu LinkedIn Talent Hub atbilstošās atļaujas datu rakstīšanai Human Resources.</span><span class="sxs-lookup"><span data-stu-id="38ca9-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="38ca9-110">Sasaistiet savu vidi ar LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="38ca9-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="38ca9-111">Atveriet [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="38ca9-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="38ca9-112">Lietotāja nolaižamajā izvēlnē atlasiet **Preces iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="38ca9-113">Sadaļas papildu navigācijas rūtī kreisajā pusē sadaļas **Papildu** atlasiet **Integrācija**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="38ca9-114">Atlasiet **Autorizēšana** Microsoft Dynamics 365 Human Resources integrācijai.</span><span class="sxs-lookup"><span data-stu-id="38ca9-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="38ca9-115">Lapā **Dynamics 365 Human Resources** atlasiet vidi, lai sasaistītu LinkedIn Talent Hub, un pēc tam atlasiet **Sasaistīt**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hub pievienošana](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="38ca9-117">Var sasaistīt tikai ar vidēm, kurās jūsu lietotāja kontam ir administratora piekļuve gan Human Resources videi, gan saistītajai Power Apps videi.</span><span class="sxs-lookup"><span data-stu-id="38ca9-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="38ca9-118">Ja saites lapā Human Resources nav norādīta neviena vide, pārliecinieties, vai jums ir licencētas Human Resources vides šajā nomniekā un vai lietotājam, ar kuru pierakstījāties saites lapā, ir administratora atļaujas gan Human Resources vidē, gan Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="38ca9-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="38ca9-119">Izveidojiet Power Apps drošības lomu</span><span class="sxs-lookup"><span data-stu-id="38ca9-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="38ca9-120">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="38ca9-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="38ca9-121">Sarakstā **Vides** atlasiet vidi, kas saistīta ar Human Resources vidi, ko vēlaties saistīt ar savu LinkedIn Talent Hub instanci.</span><span class="sxs-lookup"><span data-stu-id="38ca9-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="38ca9-122">Atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-122">Select **Settings**.</span></span>

4. <span data-ttu-id="38ca9-123">Izvērsiet mezglu **Lietotāji + atļaujas** un atlasiet **Drošības loma**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="38ca9-124">Lapas **Drošības lomas** rīkjoslā atlasiet **Jauna loma**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="38ca9-125">Cilnē **Detalizēta informācija** ievadiet lomas nosaukumu, piemēram, **LinkedIn Talent Hub HRIS integrācija**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="38ca9-126">Cilnē **Pielāgošana** atlasiet organizācijas līmeņa **Lasīšanas** tālāk minētajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="38ca9-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="38ca9-127">Elements</span><span class="sxs-lookup"><span data-stu-id="38ca9-127">Entity</span></span>
    - <span data-ttu-id="38ca9-128">Lauks</span><span class="sxs-lookup"><span data-stu-id="38ca9-128">Field</span></span>
    - <span data-ttu-id="38ca9-129">Saistība</span><span class="sxs-lookup"><span data-stu-id="38ca9-129">Relationship</span></span>

8. <span data-ttu-id="38ca9-130">Saglabājiet un aizveriet drošības lomu.</span><span class="sxs-lookup"><span data-stu-id="38ca9-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="38ca9-131">Izveidojiet Power Apps programmas lietotāju</span><span class="sxs-lookup"><span data-stu-id="38ca9-131">Create a Power Apps application user</span></span>

<span data-ttu-id="38ca9-132">Programmas lietotājam jāizveido LinkedIn Talent Hub adapteris, lai piešķirtu atļaujas adapterim rakstīt kandidātu ierakstus Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="38ca9-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="38ca9-133">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="38ca9-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="38ca9-134">Sarakstā **Vides** atlasiet vidi, kas saistīta ar Human Resources vidi, ko vēlaties saistīt ar savu LinkedIn Talent Hub instanci.</span><span class="sxs-lookup"><span data-stu-id="38ca9-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="38ca9-135">Atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-135">Select **Settings**.</span></span>

4. <span data-ttu-id="38ca9-136">Izvērsiet mezglu **Lietotāji + atļaujas** un atlasiet **Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="38ca9-137">Atlasiet **Pārvaldīt lietotājus Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="38ca9-138">Izmantojiet nolaižamo izvēlni virs saraksta, lai mainītu skatu no noklusējuma **Iespējot lietotājus** skata uz **Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Programmas lietotāju skats](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="38ca9-140">Rīkjoslā atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="38ca9-141">Lapā **Jauns lietotājs** izpildiet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="38ca9-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="38ca9-142">Mainiet lauka **Lietotāja veids** vērtību uz **Programmas lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="38ca9-143">Iestatiet lauku **Lietotāja nosaukums** uz **Dynamics365 HR LinkedIn HRIS Integration**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="38ca9-144">Iestatiet lauku **Programmas ID** uz **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="38ca9-145">Ievadiet jebkuru vērtību laukos **Vārds**, **Uzvārds** un **Primārais e-pasts**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="38ca9-146">Rīkjoslā atlasiet **Saglabāt \& Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="38ca9-147">Drošības lomas piešķiršana jaunajam lietotājam</span><span class="sxs-lookup"><span data-stu-id="38ca9-147">Assign a security role to the new user</span></span>

<span data-ttu-id="38ca9-148">Kad esat saglabājis un aizvēris jauno programmas lietotāju iepriekšējā sadaļā, jūs tiekat atgriezts lapā **Lietotāju saraksts**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="38ca9-149">Lapā **Lietotāju saraksts** mainiet skatu uz **Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="38ca9-150">Atlasiet programmas lietotāju, ko izveidojāt iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="38ca9-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="38ca9-151">Rīkjoslā atlasiet **Pārvaldīt lomas**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="38ca9-152">Atlasiet drošības lomu, ko iepriekš izveidojāt integrācijai.</span><span class="sxs-lookup"><span data-stu-id="38ca9-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="38ca9-153">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="38ca9-154">Pievienojiet programmu Azure Active Directory programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="38ca9-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="38ca9-155">Programmā Dynamics 365 Human Resources atveriet lapu **Azure Active Directory programmas**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="38ca9-156">Pievienojiet jaunu ierakstu sarakstam iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="38ca9-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="38ca9-157">**Klienta ID**: ievadiet **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="38ca9-158">**Nosaukums**: ievadiet Power Apps iepriekš izveidotās drošības lomas nosaukumu, piemēram, **LinkedIn Talent Hub HRIS integrācija**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="38ca9-159">**Lietotāja ID**: atlasiet lietotāju, kuram ir atļauja rakstīt datus Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="38ca9-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="38ca9-160">Tabulas izveide sistēmā Dataverse</span><span class="sxs-lookup"><span data-stu-id="38ca9-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38ca9-161">Integrācija ar LinkedIn Talent Hub ir atkarīga no virtuālajām tabulām pakalpojumā Dataverse programmai Human Resources.</span><span class="sxs-lookup"><span data-stu-id="38ca9-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="38ca9-162">Kā priekšnosacījums šai darbībai iestatījumā jums ir jākonfigurē virtuālās tabulas.</span><span class="sxs-lookup"><span data-stu-id="38ca9-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="38ca9-163">Papildinformāciju par to, kā konfigurēt virtuālās tabulas, skatiet sadaļā [Dataverse virtuālo tabulu konfigurēšana](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="38ca9-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="38ca9-164">Human Resources atveriet lapu **Dataverse integrācija**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="38ca9-165">Atlasiet cilni **Virtuālās tabulas**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="38ca9-166">Filtrējiet elementa sarakstu pēc elementa etiķetes, lai atrastu **LinkedIn eksportētais kandidāts**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="38ca9-167">Atlasiet elementu un pēc tam atlasiet **Ģenerēt/atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="38ca9-168">Kandidāta ierakstu eksportēšana</span><span class="sxs-lookup"><span data-stu-id="38ca9-168">Exporting candidate records</span></span>

<span data-ttu-id="38ca9-169">Kad iestatīšana ir pabeigta, personāla atlases darbinieki un cilvēkresursu (HR) speciālisti var izmantot funkciju **Eksportēt uz HRIS** LinkedIn Talent Hub, lai eksportētu nolīgto kandidātu ierakstus no LinkedIn Talent Hub uz programmu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="38ca9-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="38ca9-170">Ierakstu eksportēšana no LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="38ca9-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="38ca9-171">Kad kandidāts ir izgājis personāla atlases procesu un ir nolīgts, varat eksportēt kandidāta ierakstu no LinkedIn Talent Hub uz programmu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="38ca9-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="38ca9-172">LinkedIn Talent Hub atveriet projektu, kuram esat nolīdzis jauno darbinieku.</span><span class="sxs-lookup"><span data-stu-id="38ca9-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="38ca9-173">Atlasiet kandidāta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="38ca9-173">Select a candidate record.</span></span>

3. <span data-ttu-id="38ca9-174">Atlasiet **Mainīt posmu** un pēc tam atlasiet **Nolīgts**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="38ca9-175">Kandidāta izvēlnē Daudzpunkte (**...**) atlasiet opciju **Eksportēt uz HRIS**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="38ca9-176">Rūtī **Eksportēt uz HRIS** ievadiet informāciju, kas ir jāeksportē:</span><span class="sxs-lookup"><span data-stu-id="38ca9-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="38ca9-177">Laukā **HRIS nodrošinātājs** atlasiet **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="38ca9-178">Laukā **Sākuma datums** atlasiet vērtību jaunajam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="38ca9-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="38ca9-179">Laukā **Amats** ievadiet jaunā darbinieka darba amata nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="38ca9-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="38ca9-180">Laukā **Atrašanās vieta** ievadiet vietu, kur darbinieks atradīsies.</span><span class="sxs-lookup"><span data-stu-id="38ca9-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="38ca9-181">Ievadiet vai apstipriniet darbinieka e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="38ca9-181">Enter or verify the employee's email address.</span></span>

![Eksportēšana uz HRIS rūti LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="38ca9-183">Darbā pieņemšanas pabeigšana programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="38ca9-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="38ca9-184">Kandidāta ieraksti, kas tiek eksportēti no LinkedIn Talent Hub uz programmu Human Resources, tiek parādīti lapas **Personāla vadība** sadaļā **Kandidāti nolīgšanai**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="38ca9-185">Human Resources atveriet lapu **Personāla vadība**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="38ca9-186">Sadaļā **Kandidāti nolīgšanai** atlasītajam kandidātam atlasiet **Nolīgt**.</span><span class="sxs-lookup"><span data-stu-id="38ca9-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="38ca9-187">Dialoglodziņā **Nolīgt jaunu darbinieku** pārskatiet ierakstu un pievienojiet visu nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="38ca9-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="38ca9-188">Varat arī atlasīt amata numuru, uz kuru kandidāts ir nolīgts.</span><span class="sxs-lookup"><span data-stu-id="38ca9-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="38ca9-189">Kad vajadzīgā informācija ir ievadīta, varat turpināt standarta procesus, lai izveidotu darbinieka ierakstus un pieņemtu darbiniekus darbā.</span><span class="sxs-lookup"><span data-stu-id="38ca9-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="38ca9-190">Tālāk norādītā informācija tiek importēta un iekļauta jaunā darbinieka ierakstā:</span><span class="sxs-lookup"><span data-stu-id="38ca9-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="38ca9-191">Vārds</span><span class="sxs-lookup"><span data-stu-id="38ca9-191">First name</span></span>
- <span data-ttu-id="38ca9-192">Uzvārds</span><span class="sxs-lookup"><span data-stu-id="38ca9-192">Last name</span></span>
- <span data-ttu-id="38ca9-193">Darba attiecību uzsākšanas datums</span><span class="sxs-lookup"><span data-stu-id="38ca9-193">Employment start date</span></span>
- <span data-ttu-id="38ca9-194">E-pasta adrese</span><span class="sxs-lookup"><span data-stu-id="38ca9-194">Email address</span></span>
- <span data-ttu-id="38ca9-195">Tālruņa numurs</span><span class="sxs-lookup"><span data-stu-id="38ca9-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="38ca9-196">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="38ca9-196">See also</span></span>

[<span data-ttu-id="38ca9-197">Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="38ca9-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="38ca9-198">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="38ca9-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
