---
title: Instances kopēšana
description: ''
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
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009760"
---
# <a name="copy-an-instance"></a><span data-ttu-id="8f99d-102">Instances kopēšana</span><span class="sxs-lookup"><span data-stu-id="8f99d-102">Copy an instance</span></span>

<span data-ttu-id="8f99d-103">Varat izmantot Microsoft Dynamics Lifecycle Services (LCS), lai kopētu Microsoft Dynamics 365 Human Resources datu bāzi uz smilškastes vidi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="8f99d-104">Ja jums ir cita smilškastes vide, varat arī kopēt datu bāzi no šīs vides uz mērķtiecīgu smilškastes vidi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="8f99d-105">Lai kopētu instanci, jāpārliecinās, ka ievērots tālāk minētais.</span><span class="sxs-lookup"><span data-stu-id="8f99d-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="8f99d-106">Human Resources instancei, ko vēlaties pārrakstīt, jābūt smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="8f99d-107">Vidēm, no kurām un uz kurām kopējat, jābūt tajā pašā reģionā.</span><span class="sxs-lookup"><span data-stu-id="8f99d-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="8f99d-108">Nevar kopēt starp reģioniem.</span><span class="sxs-lookup"><span data-stu-id="8f99d-108">You can't copy across regions.</span></span>

- <span data-ttu-id="8f99d-109">Jums ir jābūt administratoram mērķa vidē, lai varētu pierakstīties tajā pēc instances kopēšanas.</span><span class="sxs-lookup"><span data-stu-id="8f99d-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="8f99d-110">Kopējot Human Resources datu bāzi, netiek kopēti Microsoft PowerApps vidē esošie elementi (programmas vai dati).</span><span class="sxs-lookup"><span data-stu-id="8f99d-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="8f99d-111">Informāciju par to, kā kopēt elementus PowerApps vidē, skatiet [Vides kopēšana](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="8f99d-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="8f99d-112">PowerApps videi, ko vēlaties pārrakstīt, jābūt smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="8f99d-113">Jums ir jābūt globālā nomnieka administratoram, lai mainītu PowerApps ražošanas vidi uz smilškastes vidi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="8f99d-114">Papildinformāciju par PowerApps vides mainīšanu skatiet [Instances pārslēgšana](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="8f99d-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="8f99d-115">Human Resources datu bāzes kopēšanas sekas</span><span class="sxs-lookup"><span data-stu-id="8f99d-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="8f99d-116">Kopējot Human Resources datu bāzi, notiek tālāk minētie notikumi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="8f99d-117">Kopēšanas process izdzēš esošo datu bāzi mērķa vidē.</span><span class="sxs-lookup"><span data-stu-id="8f99d-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="8f99d-118">Kad kopēšanas process ir pabeigts, esošo datu bāzi nevar atgūt.</span><span class="sxs-lookup"><span data-stu-id="8f99d-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="8f99d-119">Mērķa vide nebūs pieejama, kamēr kopēšanas process nebūs pabeigts.</span><span class="sxs-lookup"><span data-stu-id="8f99d-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="8f99d-120">Dokumenti Microsoft Azure Blob krātuvē netiek kopēti no vienas vides uz citu.</span><span class="sxs-lookup"><span data-stu-id="8f99d-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="8f99d-121">Tādējādi visi pievienotie dokumenti un veidnes netiks kopētas un paliks avota vidē.</span><span class="sxs-lookup"><span data-stu-id="8f99d-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="8f99d-122">Nebūs pieejami visi lietotāji, izņemot administratora un citu iekšējo pakalpojumu lietotāju kontus.</span><span class="sxs-lookup"><span data-stu-id="8f99d-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="8f99d-123">Tādējādi administrators var dzēst vai aptumšot datus, pirms citi lietotāji drīkst ienākt atpakaļ sistēmā.</span><span class="sxs-lookup"><span data-stu-id="8f99d-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="8f99d-124">Administratoram ir jāveic nepieciešamās konfigurācijas izmaiņas, piemēram, integrācijas galapunktu atkārtota pieslēgšana noteiktiem pakalpojumiem vai URL.</span><span class="sxs-lookup"><span data-stu-id="8f99d-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="8f99d-125">Human Resources datu bāzes kopēšana</span><span class="sxs-lookup"><span data-stu-id="8f99d-125">Copy the Human Resources database</span></span>

<span data-ttu-id="8f99d-126">Lai pabeigtu šo uzdevumu, vispirms kopējiet instanci un pēc tam pierakstieties Microsoft Power Platform administrēšanas centrā, lai kopētu savu PowerApps vidi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="8f99d-127">Kopējot instanci, mērķa instancē datu bāze tiek dzēsta.</span><span class="sxs-lookup"><span data-stu-id="8f99d-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="8f99d-128">Šī procesa laikā mērķa instance nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="8f99d-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="8f99d-129">Pierakstieties LCS un atlasiet LCS projektu, kas satur instanci, ko vēlaties kopēt.</span><span class="sxs-lookup"><span data-stu-id="8f99d-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="8f99d-130">Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="8f99d-131">Atlasiet instanci, kas jākopē, un pēc atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="8f99d-132">Uzdevumrūtī **Kopēt instanci** atlasiet instanci, kuru pārrakstīt, un pēc tam atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="8f99d-133">Uzgaidiet, līdz lauka **Kopēšanas statuss** vērtība tiek atjaunināta uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="8f99d-134">Instances atlasīšana pārrakstīšanai</span><span class="sxs-lookup"><span data-stu-id="8f99d-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="8f99d-135">Atlasiet **Power Platform** un pierakstieties Microsoft Power Platform administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="8f99d-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="8f99d-136">Atlasiet Power Platform</span><span class="sxs-lookup"><span data-stu-id="8f99d-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="8f99d-137">Atlasiet PowerApps vidi, kas jākopē, un pēc atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="8f99d-138">Kad kopēšanas process ir pabeigts, pierakstieties mērķa instancē un iespējojiet Common Data Service integrāciju.</span><span class="sxs-lookup"><span data-stu-id="8f99d-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="8f99d-139">Papildinformāciju un instrukcijas skatiet [Common Data Service integrācijas konfigurēšana](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="8f99d-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="8f99d-140">Datu elementi un statusi</span><span class="sxs-lookup"><span data-stu-id="8f99d-140">Data elements and statuses</span></span>

<span data-ttu-id="8f99d-141">Kopējot Human Resources instanci, tālāk minētie datu elementi netiek kopēti:</span><span class="sxs-lookup"><span data-stu-id="8f99d-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="8f99d-142">E-pasta adreses tabulā **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="8f99d-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="8f99d-143">Pakešuzdevumu vēsture tabulās **BatchJobHistory**, **BatchHistory** un **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="8f99d-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="8f99d-144">Vienkāršā pasta pārsūtīšanas protokola (Simple Mail Transfer Protocol — SMTP) parole tabulā **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="8f99d-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="8f99d-145">SMTP releja serveris tabulā **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="8f99d-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="8f99d-146">Drukas pārvaldības iestatījumi tabulās **PrintMgmtSettings** un **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="8f99d-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="8f99d-147">Videi specifiski ieraksti tabulās **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** un **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="8f99d-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="8f99d-148">Dokumentu pielikumi tabulā DocuValue.</span><span class="sxs-lookup"><span data-stu-id="8f99d-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="8f99d-149">Šie pielikumi ietver jebkuras Microsoft Office veidnes, kas tika pārrakstītas avota vidē</span><span class="sxs-lookup"><span data-stu-id="8f99d-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="8f99d-150">Savienojuma virkne tabulā **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8f99d-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="8f99d-151">Daži no šiem elementiem netiek kopēti, jo tie ir videi specifiski.</span><span class="sxs-lookup"><span data-stu-id="8f99d-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="8f99d-152">Piemēram, ieraksti **BatchServerConfig** un **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="8f99d-153">Citi elementi netiek kopēti atbalsta biļešu apjoma dēļ.</span><span class="sxs-lookup"><span data-stu-id="8f99d-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="8f99d-154">Piemēram, var tikt nosūtīti dublēti e-pasta ziņojumi, jo lietotāja pieņemšanas testēšanas (smilškastes) vidē joprojām ir iespējots SMTP; var tikt nosūtīti nederīgi integrācijas ziņojumi, jo aizvien ir iespējoti pakešuzdevumi, un lietotāji var būt iespējoti pirms administratori var veikt pēcatsvaidzināšanas dzēšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="8f99d-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="8f99d-155">Turklāt, kopējot instanci, mainās tālāk minētie statusi.</span><span class="sxs-lookup"><span data-stu-id="8f99d-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="8f99d-156">Visi lietotāji, izņemot administratorus, ir iestatīti uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="8f99d-157">Visi pakešuzdevumi, izņemot dažus sistēmas uzdevumus, ir iestatīti uz **Aizturēt**.</span><span class="sxs-lookup"><span data-stu-id="8f99d-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="8f99d-158">Vides administrators</span><span class="sxs-lookup"><span data-stu-id="8f99d-158">Environment admin</span></span>

<span data-ttu-id="8f99d-159">Visi mērķa smilškastes vides lietotāji, ieskaitot administratorus, tiek aizstāti ar avota vides lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8f99d-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="8f99d-160">Pirms instances kopēšanas, pārliecinieties, ka esat administrators mērķa vidē.</span><span class="sxs-lookup"><span data-stu-id="8f99d-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="8f99d-161">Ja neesat, nevarēsiet pierakstīties mērķa smilškastes vidē pēc tam, kad kopēšana tiks pabeigta.</span><span class="sxs-lookup"><span data-stu-id="8f99d-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="8f99d-162">Visi lietotāji, kuri nav administratori, ir atspējoti mērķa smilškastes vidē, lai novērstu neatļautu pierakstīšanos smilškastes vidē.</span><span class="sxs-lookup"><span data-stu-id="8f99d-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="8f99d-163">Ja, nepieciešams, administratori var no jauna iespējot lietotājus.</span><span class="sxs-lookup"><span data-stu-id="8f99d-163">Administrators can reenable users if needed.</span></span>