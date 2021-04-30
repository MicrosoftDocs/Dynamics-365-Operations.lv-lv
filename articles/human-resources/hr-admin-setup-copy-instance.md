---
title: Instances kopēšana
description: Varat izmantot Microsoft Dynamics Lifecycle Services (LCS), lai kopētu Microsoft Dynamics 365 Human Resources datu bāzi uz smilškastes vidi.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44df05083cd3c91e5dcbdb3062665c2145d92a7e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889816"
---
# <a name="copy-an-instance"></a><span data-ttu-id="bb32a-103">Instances kopēšana</span><span class="sxs-lookup"><span data-stu-id="bb32a-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bb32a-104">Varat izmantot Microsoft Dynamics Lifecycle Services (LCS), lai kopētu Microsoft Dynamics 365 Human Resources datu bāzi uz smilškastes vidi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="bb32a-105">Ja jums ir cita smilškastes vide, varat arī kopēt datu bāzi no šīs vides uz mērķtiecīgu smilškastes vidi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="bb32a-106">Lai kopētu instanci, ņemiet vērā šādus padomus:</span><span class="sxs-lookup"><span data-stu-id="bb32a-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="bb32a-107">Human Resources instancei, ko vēlaties pārrakstīt, jābūt smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="bb32a-108">Vidēm, no kurām un uz kurām kopējat, jābūt tajā pašā reģionā.</span><span class="sxs-lookup"><span data-stu-id="bb32a-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="bb32a-109">Nevar kopēt starp reģioniem.</span><span class="sxs-lookup"><span data-stu-id="bb32a-109">You can't copy across regions.</span></span>

- <span data-ttu-id="bb32a-110">Jums ir jābūt administratoram mērķa vidē, lai varētu pierakstīties tajā pēc instances kopēšanas.</span><span class="sxs-lookup"><span data-stu-id="bb32a-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="bb32a-111">Kopējot Human Resources datu bāzi, netiek kopēti Microsoft Power Apps vidē esošie elementi (programmas vai dati).</span><span class="sxs-lookup"><span data-stu-id="bb32a-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="bb32a-112">Informāciju par to, kā kopēt elementus Power Apps vidē, skatiet [Vides kopēšana](/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="bb32a-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="bb32a-113">Power Apps videi, ko vēlaties pārrakstīt, jābūt smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="bb32a-114">Jums ir jābūt globālā nomnieka administratoram, lai mainītu Power Apps ražošanas vidi uz smilškastes vidi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="bb32a-115">Papildinformāciju par Power Apps vides mainīšanu skatiet [Instances pārslēgšana](/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="bb32a-115">For more information about changing a Power Apps environment, see [Switch an instance](/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="bb32a-116">Ja nokopējat instanci savā smilškastes vidē un vēlaties integrēt smilškastes vidi ar Dataverse, ir atkārtoti jāizmanto pielāgoti lauki Dataverse tabulām.</span><span class="sxs-lookup"><span data-stu-id="bb32a-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="bb32a-117">Skatiet [Lietot pielāgotus laukus Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="bb32a-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="bb32a-118">Human Resources datu bāzes kopēšanas sekas</span><span class="sxs-lookup"><span data-stu-id="bb32a-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="bb32a-119">Kopējot Human Resources datu bāzi, notiek tālāk minētie notikumi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="bb32a-120">Kopēšanas process izdzēš esošo datu bāzi mērķa vidē.</span><span class="sxs-lookup"><span data-stu-id="bb32a-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="bb32a-121">Kad kopēšanas process ir pabeigts, esošo datu bāzi nevar atgūt.</span><span class="sxs-lookup"><span data-stu-id="bb32a-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="bb32a-122">Mērķa vide nebūs pieejama, kamēr kopēšanas process nebūs pabeigts.</span><span class="sxs-lookup"><span data-stu-id="bb32a-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="bb32a-123">Dokumenti Microsoft Azure Blob krātuvē netiek kopēti no vienas vides uz citu.</span><span class="sxs-lookup"><span data-stu-id="bb32a-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="bb32a-124">Kā rezultātā visi pievienotie dokumenti un veidnes netiks kopētas un paliks avota vidē.</span><span class="sxs-lookup"><span data-stu-id="bb32a-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="bb32a-125">Nebūs pieejami visi lietotāji, izņemot administratora un citu iekšējo pakalpojumu lietotāju kontus.</span><span class="sxs-lookup"><span data-stu-id="bb32a-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="bb32a-126">Administrators var dzēst vai aptumšot datus, pirms citi lietotāji drīkst ienākt atpakaļ sistēmā.</span><span class="sxs-lookup"><span data-stu-id="bb32a-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="bb32a-127">Administratoram ir jāveic nepieciešamās konfigurācijas izmaiņas, piemēram, integrācijas galapunktu atkārtota pieslēgšana noteiktiem pakalpojumiem vai URL.</span><span class="sxs-lookup"><span data-stu-id="bb32a-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="bb32a-128">Human Resources datu bāzes kopēšana</span><span class="sxs-lookup"><span data-stu-id="bb32a-128">Copy the Human Resources database</span></span>

<span data-ttu-id="bb32a-129">Lai pabeigtu šo uzdevumu, vispirms kopējiet instanci un pēc tam pierakstieties Microsoft Power Platform administrēšanas centrā, lai kopētu savu Power Apps vidi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="bb32a-130">Kopējot instanci, mērķa instancē datu bāze tiek dzēsta.</span><span class="sxs-lookup"><span data-stu-id="bb32a-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="bb32a-131">Šī procesa laikā mērķa instance nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="bb32a-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="bb32a-132">Pierakstieties LCS un atlasiet LCS projektu, kas satur instanci, ko vēlaties kopēt.</span><span class="sxs-lookup"><span data-stu-id="bb32a-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="bb32a-133">Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="bb32a-134">Atlasiet instanci, kas jākopē, un pēc atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="bb32a-135">Uzdevumrūtī **Kopēt instanci** atlasiet instanci, kuru pārrakstīt, un pēc tam atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="bb32a-136">Uzgaidiet, līdz lauka **Kopēšanas statuss** vērtība tiek atjaunināta uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="bb32a-137">Instances atlasīšana pārrakstīšanai</span><span class="sxs-lookup"><span data-stu-id="bb32a-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="bb32a-138">Atlasiet **Power Platform** un pierakstieties Microsoft Power Platform administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="bb32a-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="bb32a-139">Atlasiet Power Platform</span><span class="sxs-lookup"><span data-stu-id="bb32a-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="bb32a-140">Atlasiet Power Apps vidi, kas jākopē, un pēc atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="bb32a-141">Kad kopēšanas process ir pabeigts, pierakstieties mērķa instancē un iespējojiet Dataverse integrāciju.</span><span class="sxs-lookup"><span data-stu-id="bb32a-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="bb32a-142">Papildinformāciju un instrukcijas skatiet [Pakalpojuma Dataverse integrācijas konfigurēšana](./hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="bb32a-142">For more information and instructions, see [Configure Dataverse integration](./hr-admin-integration-common-data-service.md).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="bb32a-143">Datu elementi un statusi</span><span class="sxs-lookup"><span data-stu-id="bb32a-143">Data elements and statuses</span></span>

<span data-ttu-id="bb32a-144">Kopējot Human Resources instanci, tālāk minētie datu elementi netiek kopēti:</span><span class="sxs-lookup"><span data-stu-id="bb32a-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="bb32a-145">E-pasta adreses tabulā **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="bb32a-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="bb32a-146">Pakešuzdevumu vēsture tabulās **BatchJobHistory**, **BatchHistory** un **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="bb32a-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="bb32a-147">Vienkāršā pasta pārsūtīšanas protokola (Simple Mail Transfer Protocol — SMTP) parole tabulā **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="bb32a-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="bb32a-148">SMTP releja serveris tabulā **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="bb32a-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="bb32a-149">Drukas pārvaldības iestatījumi tabulās **PrintMgmtSettings** un **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="bb32a-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="bb32a-150">Videi specifiski ieraksti tabulās **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** un **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="bb32a-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="bb32a-151">Dokumentu pielikumi tabulā DocuValue.</span><span class="sxs-lookup"><span data-stu-id="bb32a-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="bb32a-152">Šie pielikumi ietver jebkuras Microsoft Office veidnes, kas tika pārrakstītas avota vidē</span><span class="sxs-lookup"><span data-stu-id="bb32a-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="bb32a-153">Savienojuma virkne tabulā **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="bb32a-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="bb32a-154">Daži no šiem elementiem netiek kopēti, jo tie ir videi specifiski.</span><span class="sxs-lookup"><span data-stu-id="bb32a-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="bb32a-155">Piemēram, ieraksti **BatchServerConfig** un **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="bb32a-156">Citi elementi netiek kopēti atbalsta biļešu apjoma dēļ.</span><span class="sxs-lookup"><span data-stu-id="bb32a-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="bb32a-157">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="bb32a-157">For example:</span></span>

- <span data-ttu-id="bb32a-158">E-pasta kopijas var tikt nosūtītas, jo SMTP joprojām ir iespējots lietotāja pieņemšanas testēšanas (smilškastes) vidē.</span><span class="sxs-lookup"><span data-stu-id="bb32a-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="bb32a-159">Nederīgi integrācijas ziņojumi var tikt nosūtīti, jo pakešuzdevumi joprojām ir iespējoti.</span><span class="sxs-lookup"><span data-stu-id="bb32a-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="bb32a-160">Lietotāji var būt iespējoti, pirms administratori var veikt pēcatsvaidzināšanas tīrīšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="bb32a-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="bb32a-161">Turklāt, kopējot instanci, mainās tālāk minētie statusi.</span><span class="sxs-lookup"><span data-stu-id="bb32a-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="bb32a-162">Visi lietotāji, izņemot administratorus, ir iestatīti uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="bb32a-163">Visi pakešuzdevumi, izņemot dažus sistēmas uzdevumus, ir iestatīti uz **Aizturēt**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="bb32a-164">Vides administrators</span><span class="sxs-lookup"><span data-stu-id="bb32a-164">Environment admin</span></span>

<span data-ttu-id="bb32a-165">Visi mērķa smilškastes vides lietotāji, ieskaitot administratorus, tiek aizstāti ar avota vides lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="bb32a-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="bb32a-166">Pirms instances kopēšanas, pārliecinieties, ka esat administrators avota vidē.</span><span class="sxs-lookup"><span data-stu-id="bb32a-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="bb32a-167">Ja neesat, nevarēsiet pierakstīties mērķa smilškastes vidē pēc tam, kad kopēšana tiks pabeigta.</span><span class="sxs-lookup"><span data-stu-id="bb32a-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="bb32a-168">Visi lietotāji, kuri nav administratori, ir atspējoti mērķa smilškastes vidē, lai novērstu neatļautu pierakstīšanos smilškastes vidē.</span><span class="sxs-lookup"><span data-stu-id="bb32a-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="bb32a-169">Ja, nepieciešams, administratori var no jauna iespējot lietotājus.</span><span class="sxs-lookup"><span data-stu-id="bb32a-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="bb32a-170">Lietot pielāgotus laukus Dataverse</span><span class="sxs-lookup"><span data-stu-id="bb32a-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="bb32a-171">Ja nokopējat instanci savā smilškastes vidē un vēlaties integrēt smilškastes vidi ar Dataverse, ir atkārtoti jāizmanto pielāgoti lauki Dataverse tabulām.</span><span class="sxs-lookup"><span data-stu-id="bb32a-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="bb32a-172">Katram pielāgotajam laukam, kas ir pakļauts Dataverse tabulām, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="bb32a-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="bb32a-173">Dodieties uz pielāgoto lauku un atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="bb32a-174">Noņemiet opciju **Iespējots** lauks katrai cdm_\* entītijai, kurai ir iespējots pielāgots lauks.</span><span class="sxs-lookup"><span data-stu-id="bb32a-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="bb32a-175">Atlasiet **Lietot izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="bb32a-176">Vēlreiz atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="bb32a-177">Atlasiet opciju **Iespējots** lauks katrai cdm_\* entītijai, kurai ir iespējots pielāgots lauks.</span><span class="sxs-lookup"><span data-stu-id="bb32a-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="bb32a-178">Vēlreiz atlasiet **Lietot izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="bb32a-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="bb32a-179">Noņemšana, izmaiņu lietošana, atkārtota atlase un atkārtota izmaiņu veikšana pieprasa atjaunināt shēmu Dataverse, lai iekļautu pielāgotos laukus.</span><span class="sxs-lookup"><span data-stu-id="bb32a-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="bb32a-180">Plašāku informāciju par pielāgotajiem laukiem, skatiet rakstā [Darbs ar pielāgotiem laukiem un to izveide](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).</span><span class="sxs-lookup"><span data-stu-id="bb32a-180">For more information about custom fields, see [Create and work with custom fields](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bb32a-181">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="bb32a-181">See also</span></span>

[<span data-ttu-id="bb32a-182">Human Resources nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="bb32a-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="bb32a-183">Noņemt instanci</span><span class="sxs-lookup"><span data-stu-id="bb32a-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="bb32a-184">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="bb32a-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]