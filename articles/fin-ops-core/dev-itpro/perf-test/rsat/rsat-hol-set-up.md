---
title: Regression Suite Automation Tool apmācības iestatīšana un instalēšana
description: Šajā tēmā ir ietverta apmācība, kurā parādīts, kā iestatīt un instalēt Regression Suite Automation Tool (RSAT).
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c6e4dcbd854cfadbc34f0040dcffd277d32a8d9
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909038"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="c6395-103">Regression Suite Automation Tool apmācības iestatīšana un instalēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="c6395-104">Šajā tēmā ietvertā apmācība palīdzēs iestatīt RSAT un ar RSAT lietošanu saistītos rīkus un sākt darbu ar tiem.</span><span class="sxs-lookup"><span data-stu-id="c6395-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c6395-105">Izmantojiet interneta pārlūka rīkus, lai lejupielādētu un saglabātu šo lapu PDF formātā.</span><span class="sxs-lookup"><span data-stu-id="c6395-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="c6395-106">Galvenie principi</span><span class="sxs-lookup"><span data-stu-id="c6395-106">Key concepts</span></span>

- <span data-ttu-id="c6395-107">Uzziniet par instalēšanu un priekšnosacījumu iestatīšanu, kas nepieciešama dažādajām programmām, lai atbalstītu Regression Suite Automation Tool (RSAT).</span><span class="sxs-lookup"><span data-stu-id="c6395-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="c6395-108">Izprotiet, kā uzdevumu ierakstītāja līdzeklis kopā ar pakalpojumu Microsoft Dynamics Lifecycle Services (LCS) un Microsoft Azure DevOps ļauj izveidot, konfigurēt, palaist un izmeklēt testa gadījumus un sniegt pārskatus par tiem.</span><span class="sxs-lookup"><span data-stu-id="c6395-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="c6395-109">Sniedziet funkcionālajiem lietotājiem iespēju reģistrēt biznesa uzdevumus, izmantojot uzdevumu ierakstītāju, un pēc tam pārveidot uzdevumu ierakstus automātisku testu komplektā bez nepieciešamības rakstīt pirmkodu.</span><span class="sxs-lookup"><span data-stu-id="c6395-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="c6395-110">Pirms sākšanas</span><span class="sxs-lookup"><span data-stu-id="c6395-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c6395-111">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="c6395-111">Prerequisites</span></span>

- <span data-ttu-id="c6395-112">Šai apmācībai ir nepieciešama vide, kurā darbojas Microsoft Dynamics 365 for Finance and Operations versija 10.0 (2019. gada aprīlis) vai jaunāka tās versija.</span><span class="sxs-lookup"><span data-stu-id="c6395-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="c6395-113">Klientiem, kuri izmanto Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3, tiek nodrošināts arī Platform update 20 (PU20) vai jaunākas versijas atbalsts.</span><span class="sxs-lookup"><span data-stu-id="c6395-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="c6395-114">Lietotājam ir nepieciešamas administratora tiesības vidē.</span><span class="sxs-lookup"><span data-stu-id="c6395-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="c6395-115">Jums ir nepieciešama piekļuve klienta nomnieka LCS un Azure DevOps (iepriekš zināms kā Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="c6395-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="c6395-116">Lietotājam, kas veido un pārvalda testu komplektus, ir nepieciešama Azure DevOps testēšanas plānu vai testu pārvaldnieka licence.</span><span class="sxs-lookup"><span data-stu-id="c6395-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="c6395-117">Piekļuvi testēšanas plāniem nodrošina arī šādas licence:</span><span class="sxs-lookup"><span data-stu-id="c6395-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="c6395-118">Visual Studio Enterprise licence;</span><span class="sxs-lookup"><span data-stu-id="c6395-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="c6395-119">Visual Studio Test Professional licence;</span><span class="sxs-lookup"><span data-stu-id="c6395-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="c6395-120">MSDN Platforms abonenta licence.</span><span class="sxs-lookup"><span data-stu-id="c6395-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="c6395-121">RSAT ir nepieciešama piekļuve testa videi, izmantojot tīmekļa pārlūku.</span><span class="sxs-lookup"><span data-stu-id="c6395-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="c6395-122">Lai ģenerētu un rediģētu testa parametrus, ir jābūt instalētai programmai Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c6395-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="c6395-123">Konfigurēt Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="c6395-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="c6395-124">Lietotāju atbilstība</span><span class="sxs-lookup"><span data-stu-id="c6395-124">User eligibility</span></span>

<span data-ttu-id="c6395-125">Pārliecinieties, ka lietotājs ir izveidots pakalpojumā Azure DevOps un ka tam ir abonementa līmenis, kas nodrošina piekļuvi Azure testēšanas plāniem.</span><span class="sxs-lookup"><span data-stu-id="c6395-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="c6395-126">Azure DevOps testēšanas plānu licence ir nepieciešama tikai tad, ja lietotājs izveidos un pārvaldīs testa gadījumus (t. i., ne visiem RSAT lietotājiem ir nepieciešama šī licence).</span><span class="sxs-lookup"><span data-stu-id="c6395-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="c6395-127">Informāciju par licenču prasībām skatiet sadaļā [Licenču prasības](/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="c6395-127">For information about the license requirements, see [License requirements](/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="c6395-128">Jauna Azure DevOps projekta izveide</span><span class="sxs-lookup"><span data-stu-id="c6395-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="c6395-129">RSAT izmanto Azure Devops testa gadījumu un testu komplektu pārvaldībai, pārskatu veidošanai un testu un rezultātu izmeklēšanai.</span><span class="sxs-lookup"><span data-stu-id="c6395-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="c6395-130">Varat izmantot esošu Azure DevOps projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="c6395-131">Tomēr, ja esošais Azure DevOps projekts ir iestatīts tā, ka tam ir pielāgota veidne, tad, sinhronizējot testa gadījumus no biznesa procesu modelētāja (BPM) ar Azure DevOps (skatiet sadaļu [Testu sinhronizēšana no BPM ar Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) ), tiks parādīts kļūdas ziņojums “VSTS sinhronizēšanas kļūme”.</span><span class="sxs-lookup"><span data-stu-id="c6395-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="c6395-132">Ja pielāgotajā veidnē tiek ievērota tālāk norādītā paraugprakse, ir iespējams sinhronizēt pārbaudes gadījumus ar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="c6395-133">(Šie paraugprakses ieteikumi ir uzskaitīti kļūdas ziņojumā.)</span><span class="sxs-lookup"><span data-stu-id="c6395-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="c6395-134">Neizdzēsiet nevienu darba krājuma veidu vai iebūvētos laukus.</span><span class="sxs-lookup"><span data-stu-id="c6395-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="c6395-135">Neizdzēsiet nevienu darba krājuma stāvokļa veidu.</span><span class="sxs-lookup"><span data-stu-id="c6395-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="c6395-136">Nepievienojiet nevienu obligāto lauku darba krājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="c6395-136">Do not add any required fields to a work item type.</span></span>

![Kļūdas ziņojums ar paraugprakses ieteikumu sarakstu](./media/setup_rsa_tool_02.png)

<span data-ttu-id="c6395-138">Pretējā gadījumā šīs apmācības nolūkos ieteicams izveidot jaunu Azure DevOps projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="c6395-139">Papildinformāciju skatiet sadaļā [Problēmas saistībā ar sinhronizāciju uz BPM, izmantojot pielāgotu Azure DevOps (VSTS) procesu veidni](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="c6395-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="c6395-140">Atveriet Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="c6395-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="c6395-141">Azure DevOps lapas augšējā labajā stūrī atlasiet pogu **Izveidot projektu**.</span><span class="sxs-lookup"><span data-stu-id="c6395-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Poga Izveidot projektu](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="c6395-143">Aizpildiet tālāk norādītos laukus un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="c6395-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="c6395-144">**Projekta nosaukums**</span><span class="sxs-lookup"><span data-stu-id="c6395-144">**Project name**</span></span>
    - <span data-ttu-id="c6395-145">**Versiju kontrole**— atlasiet **Team Foundation versijas kontrole**.</span><span class="sxs-lookup"><span data-stu-id="c6395-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="c6395-146">Ņemiet vērā, ka noklusētā opcija **Git** netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="c6395-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="c6395-147">**Darba vienuma process**</span><span class="sxs-lookup"><span data-stu-id="c6395-147">**Work item process**</span></span>

    ![Dialoglodziņš Izveidot jaunu projektu](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="c6395-149">Personiskās piekļuves pilnvaras izveide</span><span class="sxs-lookup"><span data-stu-id="c6395-149">Create a personal access token</span></span>

<span data-ttu-id="c6395-150">Šajā apmācībā jūs izmantosiet LCS biznesa procesu modelētāju (BPM), lai izveidotu testa gadījumu bibliotēku un sinhronizētu jūsu testa gadījumus ar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="c6395-151">Jums būs nepieciešama personiskās piekļuves pilnvara, lai sinhronizētu BPM ar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="c6395-152">Atlasiet profila ikonu Azure DevOps projekta lapas augšējā labajā stūrī un pēc tam atlasiet **Drošība**.</span><span class="sxs-lookup"><span data-stu-id="c6395-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Drošības komanda](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="c6395-154">Kreisajā rūtī sadaļā **Drošība** atlasiet **Personiskās piekļuves pilnvaras**.</span><span class="sxs-lookup"><span data-stu-id="c6395-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="c6395-155">Pēc tam atlasiet **Jauna pilnvara**.</span><span class="sxs-lookup"><span data-stu-id="c6395-155">Then select **New Token**.</span></span>

    ![Poga Jauna pilnvara sadaļas Lietotāja iestatījumi cilnē Personiskās piekļuves pilnvaras](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="c6395-157">Aizpildiet tālāk norādītos laukus un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="c6395-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="c6395-158">**Vārds**</span><span class="sxs-lookup"><span data-stu-id="c6395-158">**Name**</span></span>
    - <span data-ttu-id="c6395-159">**Termiņa beigas (UTC)**— atlasiet **Pielāgots** un pēc tam izmantojiet datuma atlasītāju, lai atlasītu pēdējo pieejamo datumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="c6395-160">**Tvērumi**— atlasiet opciju **Pilna piekļuve**.</span><span class="sxs-lookup"><span data-stu-id="c6395-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Dialoglodziņš Izveidot jaunu personiskās piekļuves pilnvaru](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="c6395-162">Pierakstiet izveidoto personiskās piekļuves pilnvaru.</span><span class="sxs-lookup"><span data-stu-id="c6395-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="c6395-163">Tā jums būs nepieciešama vēlāk, iestatot RSAT konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c6395-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Personiskās piekļuves pilnvara](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="c6395-165">LCS projekta konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-165">Configure the LCS project</span></span>

<span data-ttu-id="c6395-166">Jūsu galvenajai testu bibliotēkai ir nepieciešams Lifecycle Services (LCS) projekts.</span><span class="sxs-lookup"><span data-stu-id="c6395-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="c6395-167">LCS biznesa procesu modelētājs (BPM) tiek izmantots kā galvenā jūsu testa gadījumu bibliotēka.</span><span class="sxs-lookup"><span data-stu-id="c6395-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="c6395-168">BPM tiek izmantots, lai pārvaldītu un izplatītu testa bibliotēkas vairākos LCS projektos.</span><span class="sxs-lookup"><span data-stu-id="c6395-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="c6395-169">Piemēram, Microsoft partneris vai neatkarīgs programmatūras piegādātājs, kas veido testa bibliotēkas, izlaiž testa gadījumus BPM bibliotēku formā.</span><span class="sxs-lookup"><span data-stu-id="c6395-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="c6395-170">BPM testa gadījumi tiek organizēti pēc biznesa procesa.</span><span class="sxs-lookup"><span data-stu-id="c6395-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="c6395-171">BPM nedefinē izpildes secību vai testu izpildes biežumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="c6395-172">Šīs detaļas tiek pārvaldītas pakalpojumā Azure DevOps, kā aprakstīts šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="c6395-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="c6395-173">Savam LCS projektam varat izmantot esošu debitoru ieviešanu vai partnera projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="c6395-174">LCS valodas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="c6395-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="c6395-175">Lai lietotāja interfeiss (UI) pareizi rādītu biznesa procesus, kā vēlamā LCS valoda ir jāiestata **Angļu (ASV)**.</span><span class="sxs-lookup"><span data-stu-id="c6395-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="c6395-176">Atveriet LCS ieviešanas projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="c6395-177">Atlasiet pogu **Iestatījumi** (zobrata simbols) labajā augšējā stūrī un pēc tam atlasiet **Valodas preference**.</span><span class="sxs-lookup"><span data-stu-id="c6395-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Atjaunināt valodas preferenci](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="c6395-179">Laukā **Vēlamā valoda** atlasiet **Angļu (ASV)** un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Cilne Valodas preference sadaļā Lietotāja iestatījumi](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="c6395-181">LCS konfigurēšana savienošanai ar Azure DevOps projektu</span><span class="sxs-lookup"><span data-stu-id="c6395-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="c6395-182">Ja iepriekš izveidojāt jaunu Azure DevOps projektu, konfigurējiet LCS projektu, lai izveidotu savienojumu ar to.</span><span class="sxs-lookup"><span data-stu-id="c6395-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="c6395-183">Ja LCS projekts jau ir savienots ar Azure DevOps projektu, varat pāriet uz nākamo sadaļu.</span><span class="sxs-lookup"><span data-stu-id="c6395-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="c6395-184">Atveriet LCS ieviešanas projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="c6395-185">Atlasiet pogu **Izvēlne** un pēc tam atlasiet **Projekta iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c6395-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Komanda Projekta iestatījumi](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="c6395-187">Kreisajā rūtī atlasiet **Visual Studio Team Services** un pēc tam atlasiet **Iestatīt Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="c6395-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Cilne Visual Studio Team Services projekta iestatījumos](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="c6395-189">Laukā **Azure DevOps vietnes URL** ievadiet Azure DevOps vietnes URL.</span><span class="sxs-lookup"><span data-stu-id="c6395-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="c6395-190">Laukā **Personiskās piekļuves pilnvara** ievadiet iepriekš izveidoto personiskās piekļuves pilnvaru.</span><span class="sxs-lookup"><span data-stu-id="c6395-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-191">Lai gan VSTS tagad ir zināms kā Azure DevOps, LCS savienošanai ar Azure DevOps projektu izmantojiet iepriekšējo URL.</span><span class="sxs-lookup"><span data-stu-id="c6395-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="c6395-192">Piemēram, šajā apmācībā izmantotais Azure DevOps URL ir `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="c6395-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="c6395-193">Tomēr tālāk redzamajā attēlā tas ir ievadīts kā `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="c6395-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![1. darbība Visual Studio Team Services iestatīšanā](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="c6395-195">Atlasiet **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-195">Select **Continue**.</span></span>
6. <span data-ttu-id="c6395-196">Laukā **Visual Studio Team Services projekts** atlasiet VSTS projektu atlasītajā vietnē, lai saistītu ar LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="c6395-197">Lauka **Procesa veidne** noklusējuma iestatījums ir **Dinamisks**.</span><span class="sxs-lookup"><span data-stu-id="c6395-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="c6395-198">Pielāgotai veidnei pārskatiet labākās prakses ieteikumus sadaļā [Jauna Azure DevOps projekta izveide](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="c6395-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="c6395-199">Pēc tam atlasiet **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-199">Then select **Continue**.</span></span>

    ![2. darbība Visual Studio Team Services iestatīšanā](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="c6395-201">Pārskatiet iestatījumus un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-201">Review your settings, and then select **Save**.</span></span>

    ![3. darbība Visual Studio Team Services iestatīšanā](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="c6395-203">Atlasiet **Autorizēt**, lai autorizētu LCS piekļuvi konfigurētajai Azure DevOps vietnei jūsu vārdā un aktivizētu līdzekļus, kas integrējas ar VSTS.</span><span class="sxs-lookup"><span data-stu-id="c6395-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Poga Autorizēt](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="c6395-205">Tiek parādīts ziņojuma lodziņš ar tekstu “Jūs tiksit novirzīts uz ārēju vietni, lai autorizētu pakalpojumus LCS, lai tie jūsu vārdā varētu izveidot savienojumu ar Visual Studio Team Services.</span><span class="sxs-lookup"><span data-stu-id="c6395-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="c6395-206">Vai turpināt?”.</span><span class="sxs-lookup"><span data-stu-id="c6395-206">Proceed?"</span></span> <span data-ttu-id="c6395-207">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c6395-207">Select **Yes**.</span></span>

    ![Ziņojuma lodziņš](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="c6395-209">Atlasiet **Pieņemt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-209">Select **Accept**.</span></span>

    ![Piekļuves autorizēšana](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="c6395-211">Ja esat autorizēts kā lietotājs, UI atkal atver LCS projekta iestatījumu lapu.</span><span class="sxs-lookup"><span data-stu-id="c6395-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Autorizēts lietotājs](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="c6395-213">Jaunas BPM bibliotēkas izveide</span><span class="sxs-lookup"><span data-stu-id="c6395-213">Create a new BPM library</span></span>

1. <span data-ttu-id="c6395-214">Atveriet LCS ieviešanas projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="c6395-215">Atlasiet pogu **Izvēlne** un pēc tam atlasiet **Biznesa procesu modelētājs**.</span><span class="sxs-lookup"><span data-stu-id="c6395-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Biznesa procesu modelētāja komanda](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="c6395-217">Atlasiet **Jauna bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="c6395-217">Select **New library**.</span></span>

    ![Poga Jauna bibliotēka](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="c6395-219">Laukā **Bibliotēkas nosaukums** ievadiet nosaukumu un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="c6395-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="c6395-220">Šajā apmācībā piešķiriet BPM bibliotēkai nosaukumu **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="c6395-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Dialoglodziņš Izveidot jaunu bibliotēku](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="c6395-222">Atveriet jauno BPM bibliotēku **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="c6395-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="c6395-223">Atlasiet procesu **Galvenā biznesa procesa paraugs** un pēc tam labajā pusē atlasiet **Rediģēšanas režīms**.</span><span class="sxs-lookup"><span data-stu-id="c6395-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Poga Rediģēšanas režīms](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="c6395-225">Nomainiet lauka **Nosaukums** un lauka **Apraksts** vērtību uz **Preces izveide**.</span><span class="sxs-lookup"><span data-stu-id="c6395-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="c6395-226">Pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-226">Then select **Save**.</span></span>

    ![Lauki Nosaukums un Apraksts](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="c6395-228">Vide</span><span class="sxs-lookup"><span data-stu-id="c6395-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="c6395-229">Versijas prasība</span><span class="sxs-lookup"><span data-stu-id="c6395-229">Version requirement</span></span>

<span data-ttu-id="c6395-230">Ir nepieciešama testa vai smilškastes vide, kurā darbojas versija 10.</span><span class="sxs-lookup"><span data-stu-id="c6395-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="c6395-231">Klientiem, kuri izmanto versiju 7.3, tiek nodrošināts arī Platform update 20 vai jaunākas versijas atbalsts.</span><span class="sxs-lookup"><span data-stu-id="c6395-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="c6395-232">RSAT ir nepieciešama piekļuve jūsu testa videi, izmantojot tīmekļa pārlūku.</span><span class="sxs-lookup"><span data-stu-id="c6395-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="c6395-233">Lietotāju kritēriji</span><span class="sxs-lookup"><span data-stu-id="c6395-233">User criteria</span></span>

<span data-ttu-id="c6395-234">Lietotājam ir nepieciešamas administratora tiesības šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="c6395-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="c6395-235">Palīdzības iestatījumu iestatīšana savienojuma izveidei ar LCS</span><span class="sxs-lookup"><span data-stu-id="c6395-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="c6395-236">Šī darbība ir nepieciešama savienojuma izveidei ar LCS, lai uzdevumu ierakstus varētu saglabāt atbilstošajā BPM bibliotēkā pakalpojumā LCS, izmantojot klientu.</span><span class="sxs-lookup"><span data-stu-id="c6395-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="c6395-237">Atveriet klientu.</span><span class="sxs-lookup"><span data-stu-id="c6395-237">Open the client.</span></span>
2. <span data-ttu-id="c6395-238">Dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="c6395-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="c6395-239">Cilnes **Palīdzība** laukā **Lifecycle Services palīdzības konfigurācija** atlasiet attiecīgo LCS projektu (**RSAT** šajā apmācībā).</span><span class="sxs-lookup"><span data-stu-id="c6395-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Lauks Lifecycle Services palīdzības konfigurācija cilnē Palīdzība](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="c6395-241">BPM bibliotēkas tiek aizpildītas saskaņā ar atbilstošo LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="c6395-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="c6395-242">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-242">Select **Save**.</span></span>
5. <span data-ttu-id="c6395-243">Iespējams, būs nepieciešams atsvaidzināt pārlūku, lai redzētu atjaunināto palīdzības saturu.</span><span class="sxs-lookup"><span data-stu-id="c6395-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Paziņojums par pārlūka atsvaidzināšanu](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="c6395-245">Uzdevumu ieraksti</span><span class="sxs-lookup"><span data-stu-id="c6395-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="c6395-246">Pārliecinieties, ka visi uzdevumu ieraksti tiek sākti galvenajā informācijas panelī.</span><span class="sxs-lookup"><span data-stu-id="c6395-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="c6395-247">Raugieties, lai atsevišķi ieraksti būtu īsi, un koncentrējieties uz vienu biznesa uzdevumu, piemēram, pārdošanas pasūtījuma izveidi.</span><span class="sxs-lookup"><span data-stu-id="c6395-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="c6395-248">Uzdevuma ieraksta izveide un saglabāšana BPM bibliotēkā</span><span class="sxs-lookup"><span data-stu-id="c6395-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="c6395-249">Izveidojiet atbilstošu uzdevuma ierakstu, ko varat pievienot vienkāršajam biznesa procesam, kas tika izveidots jaunajā BPM bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="c6395-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="c6395-250">Atveriet klientu.</span><span class="sxs-lookup"><span data-stu-id="c6395-250">Open the client.</span></span>
2. <span data-ttu-id="c6395-251">Galvenajā informācijas panelī atlasiet pogu **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Uzdevuma reģistrētājs**.</span><span class="sxs-lookup"><span data-stu-id="c6395-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Atlasīt Uzdevumu ierakstītāju izvēlnē Iestatījumi](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="c6395-253">Atlasiet **Izveidot ierakstu**.</span><span class="sxs-lookup"><span data-stu-id="c6395-253">Select **Create recording**.</span></span>

    ![Poga Izveidot ierakstu](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="c6395-255">Aizpildiet laukus **Ieraksta nosaukums** un **Ieraksta apraksts** un pēc tam atlasiet **Sākt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Lauki Ieraksta nosaukums un ieraksta apraksts](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="c6395-257">Reģistrējiet preces izveides darbības.</span><span class="sxs-lookup"><span data-stu-id="c6395-257">Record the steps for creating a product.</span></span> <span data-ttu-id="c6395-258">Kad ieraksts ir pabeigts, atlasiet **Apturēt**, lai apturētu ierakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="c6395-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Preces izveides darbības](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="c6395-260">Atlasiet **Saglabāt pakalpojumos Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="c6395-260">Select **Save to Lifecycle Services**.</span></span>

    ![Saglabāt Uzdevuma ierakstu pakalpojumos Lifecycle Services](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="c6395-262">Bibliotēkas informācija tiek ielādēta no LCS.</span><span class="sxs-lookup"><span data-stu-id="c6395-262">Library information is loaded from LCS.</span></span>

    ![Notiek bibliotēkas informācijas ielāde](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="c6395-264">Atlasiet BPM bibliotēku, kuru saistīt ar uzdevuma ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c6395-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="c6395-265">Šajā apmācībā atlasiet BPM bibliotēku **RSAT**, kas tika izveidota iepriekš, un biznesa procesu **Preces izveide** zem tās.</span><span class="sxs-lookup"><span data-stu-id="c6395-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="c6395-266">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c6395-266">Then select **OK**.</span></span>

    ![Uzdevuma ieraksta saistīšana ar BPM bibliotēku un biznesa procesu](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="c6395-268">Tiek parādīts ziņojums “Saglabāšana pakalpojumā Lifecycle Services bija sekmīga”.</span><span class="sxs-lookup"><span data-stu-id="c6395-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Ziņojums par sekmīgu saglabāšanu LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="c6395-270">Ja vēlaties saglabāt uzdevuma ierakstu lokāli un pēc tam augšupielādēt to BPM, izmantojot LCS, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c6395-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="c6395-271">Kad ieraksts ir pabeigts, atlasiet **Saglabāt šajā datorā**.</span><span class="sxs-lookup"><span data-stu-id="c6395-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Saglabāt šajā datorā](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="c6395-273">Pārlūka paziņojumu joslā atlasiet **Saglabāt** vai **Saglabāt kā**, lai saglabātu failu lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="c6395-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Paziņojumu josla](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="c6395-275">Dodieties uz BPM bibliotēku **RSAT** un atlasiet biznesa procesu, kura uzdevuma ierakstu saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c6395-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="c6395-276">Cilnē **Pārskats** atlasiet **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Poga Augšupielādēt](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="c6395-278">Atlasiet **Pārlūkot** un atlasiet .axtr failu, kuru saglabājāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="c6395-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="c6395-279">Atlasiet **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-279">Then select **Upload**.</span></span>

        ![Augšupielādējamā faila .axtr atlase](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="c6395-281">Sinhronizācijas testēšana no BPM ar Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="c6395-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="c6395-282">Tagad, kad uzdevuma ieraksts ir pievienots biznesa procesam, ir jāpārbauda, vai biznesa procesu un saistīto uzdevuma ierakstu var sinhronizēt ar Azure DevOps kā līdzekli un testa gadījumu (attiecīgi), izmantojot VSTS sinhronizācijas līdzekli pakalpojumā LCS.</span><span class="sxs-lookup"><span data-stu-id="c6395-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="c6395-283">Atbilstošais darba vienuma veids, kas izveidots pakalpojumā Azure DevOps, mainās atkarībā no procesa veidnes, kuru atlasījāt, kad konfigurējāt LCS projektu ar Azure DevOps, kā aprakstīts sadaļā [Jauna Azure DevOps projekta izveide](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="c6395-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="c6395-284">Dodieties uz BPM bibliotēku un atveriet bibliotēku **RSAT**, ko izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="c6395-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="c6395-285">Atlasiet daudzpunktes pogu (**...**) un atlasiet **VSTS sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="c6395-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![Komanda VSTS sinhronizācija daudzpunktes izvēlnē](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="c6395-287">Kad VSTS sinhronizācija ir pabeigta, kreisajā pusē parādās cilne **Prasības**, kurā ietverts atbilstošais Azure DevOps darbplūsmas vienums.</span><span class="sxs-lookup"><span data-stu-id="c6395-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-288">Darba vienumam, kas tiek izveidots pakalpojumā Azure DevOps, kā prefikss tiek piešķirts BPM bibliotēkas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="c6395-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Cilne Prasības](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="c6395-290">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="c6395-290">Refresh the page.</span></span>
4. <span data-ttu-id="c6395-291">Atlasiet daudzpunktes pogu (**...**). Tiek parādīta papildu opcija **Sinhronizēt testa gadījumus**.</span><span class="sxs-lookup"><span data-stu-id="c6395-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="c6395-292">Atlasiet šo opciju.</span><span class="sxs-lookup"><span data-stu-id="c6395-292">Select this option.</span></span>

    ![Komanda Sinhronizēt testa gadījumus daudzpunktes izvēlnē](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="c6395-294">Ja opcija **Sinhronizēt testa gadījumus** nav pieejama pēc lapas atsvaidzināšanas, dodieties uz BPM galveno lapu un atlasiet **Sinhronizēt testa gadījumus** visai bibliotēkai.</span><span class="sxs-lookup"><span data-stu-id="c6395-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="c6395-295">Šādā veidā varat efektīvi iespējot visas bibliotēkas piespiedu sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="c6395-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![Opcijas Sinhronizēt testa gadījumus atlasīšana visai bibliotēkai](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="c6395-297">Kad komanda Sinhronizēt testa gadījumus ir pabeigta, cilnē **Prasības** tiek izveidots jauns testa gadījums.</span><span class="sxs-lookup"><span data-stu-id="c6395-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Jauns testa gadījums cilnē Prasības](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="c6395-299">Dodieties uz Azure DevOps projektu un atlasiet **Paneļi \> Darba vienumi**.</span><span class="sxs-lookup"><span data-stu-id="c6395-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Komanda Darba vienumi sadaļā Paneļi](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="c6395-301">Pārbaudiet, vai pastāv darba vienums un testa gadījums, ko izveidojāt, izmantojot BPM sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="c6395-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Darba vienums un testa gadījums](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="c6395-303">RSAT instalēšana un konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-303">Install and Configure RSAT</span></span>

<span data-ttu-id="c6395-304">RSAT var instalēt jebkurā datorā, kurā darbojas Windows 10 un ko var savienot ar vidi, izmantojot tīmekļa pārlūku (Internet Explorer vai Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="c6395-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="c6395-305">Pirms rīka jaunās versijas instalēšanas ieteicams atinstalēt iepriekšējo versiju.</span><span class="sxs-lookup"><span data-stu-id="c6395-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="c6395-306">Autentifikācijas sertifikāta instalēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-306">Install an authentication certificate</span></span>

<span data-ttu-id="c6395-307">Lai iespējotu autentifikāciju, sertifikāts ir jāģenerē un jāinstalē tajā pašā datorā, kurā darbojas RSAT.</span><span class="sxs-lookup"><span data-stu-id="c6395-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="c6395-308">Sertifikāta ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-308">Generate a certificate</span></span>

1. <span data-ttu-id="c6395-309">Lai ģenerētu sertifikāta failu, atveriet Microsoft Windows PowerShell logu kā administrators un izpildiet tālāk norādīto komandu.</span><span class="sxs-lookup"><span data-stu-id="c6395-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="c6395-310">Atveriet sertifikātu pārvaldnieku, ievadot **certlm.msc** dialoglodziņā **Palaist**, un pārliecinieties, ka sertifikāts **D365 automātiskās testēšanas sertifikāts** mapē **Personiski \> Sertifikāti** ir izveidots.</span><span class="sxs-lookup"><span data-stu-id="c6395-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-311">Pārliecinieties, ka ievadāt **certlm.msc**, nevis **certmgr.msc**, jo sertifikāti tiek glabāti lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="c6395-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Sertifikāts D365 automatizētās testēšanas sertifikāts](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="c6395-313">Ar peles labo pogu noklikšķiniet uz sertifikāta un pēc tam atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="c6395-314">Dodieties uz **Uzticamās saknes sertifikātu iestādes \> Sertifikāti**.</span><span class="sxs-lookup"><span data-stu-id="c6395-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Mape Sertifikāti mapē Uzticamās saknes sertifikātu iestādes](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="c6395-316">Izvēlnē **Darbība** atlasiet **Ielīmēt**, lai iekopētu sertifikātu atrašanās vietā **Uzticamās saknes sertifikātu iestādes**.</span><span class="sxs-lookup"><span data-stu-id="c6395-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Komanda Ielīmēt izvēlnē Darbība](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="c6395-318">Lai iegūtu instalētā sertifikāta nospiedumu bez atstarpēm vai speciālajām rakstzīmēm, atveriet Windows PowerShell logu kā administrators un palaidiet tālāk norādītās komandas.</span><span class="sxs-lookup"><span data-stu-id="c6395-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="c6395-319">Saglabājiet nospiedumu, jo tas būs nepieciešams vēlāk, atjauninot lietojumprogrammas objektu servera (AOS) failus .wif un iestatot RSAT konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c6395-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="c6395-320">AOS datora konfigurēšana uzticama savienojuma izveidei</span><span class="sxs-lookup"><span data-stu-id="c6395-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="c6395-321">Ja vide ir 2+ pakāpes vide, sertifikāta nospiedums ir jāatjaunina failā wif.config **visiem** vides AOS datoriem.</span><span class="sxs-lookup"><span data-stu-id="c6395-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="c6395-322">Izveidojiet attālās darbvirsmas protokola (RDP) savienojumu ar AOS datoru.</span><span class="sxs-lookup"><span data-stu-id="c6395-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="c6395-323">Pierakstīšanās informācija ir pieejama LCS vides informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="c6395-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="c6395-324">Atveriet Microsoft interneta informācijas pakalpojumus (IIS) un vietņu sarakstā meklējiet **AOSService**.</span><span class="sxs-lookup"><span data-stu-id="c6395-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService vietņu sarakstā](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="c6395-326">Ar peles labo pogu noklikšķiniet uz **Pārlūkot**, lai atvērtu mapi **\<Drive\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="c6395-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="c6395-327">Atrodiet failu **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="c6395-327">Find the **wif.config** file.</span></span>

    ![Fails wif.config mapē WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="c6395-329">Atjauniniet failu **wif.config**, sertifikātu un iestādes nosaukumam pievienojot jaunu iestādes ierakstu, kā norādīts tālāk redzamajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="c6395-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="c6395-330">Ja vairāki lietotāji izmanto vienu un to pašu programmu, katram lietotājam ir jāizveido atsevišķi nospiedumi, un katrs no šiem nospiedumiem ir jāpievieno sadaļā **\<keys\>**.</span><span class="sxs-lookup"><span data-stu-id="c6395-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="c6395-331">Ja ir vairāk nekā viens AOS dators, atkārtojiet 3.–4. darbību katram papildu datoram.</span><span class="sxs-lookup"><span data-stu-id="c6395-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-332">Atšķirībā no vecākām 2. pakāpes vidēm jaunās 2. pakāpes vides tiek izvietotas ar divām AOS instancēm.</span><span class="sxs-lookup"><span data-stu-id="c6395-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="c6395-333">Palaidiet **iisreset** visos AOS datoros.</span><span class="sxs-lookup"><span data-stu-id="c6395-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-334">Ja jums nav administratora tiesību **iisreset** palaišanai 1. pakāpes datorā, LCS lapā Informācija par vidi atlasiet Uzturēt > Restartēt pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="c6395-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="c6395-335">2+ pakāpes vide</span><span class="sxs-lookup"><span data-stu-id="c6395-335">Tier 2+ environment</span></span>

<span data-ttu-id="c6395-336">Ja tiek izmantota 2+ pakāpes (standarta pieņemšanas testu smilškaste vai jaunāka versija) vide, pārbaudiet vai iestatiet tālāk norādīto reģistra iestatījumu datorā, kurā ir instalēts RSAT.</span><span class="sxs-lookup"><span data-stu-id="c6395-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="c6395-337">Šī darbība ir nepieciešama, jo tā palīdz izvairīties no autentifikācijas vai RSAT savienojuma kļūdām.</span><span class="sxs-lookup"><span data-stu-id="c6395-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="c6395-338">RSAT instalēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-338">Install RSAT</span></span>

1. <span data-ttu-id="c6395-339">Dodieties uz <https://www.microsoft.com/download/details.aspx?id=57357> un atlasiet **Lejupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="c6395-340">Atlasiet visus failus un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="c6395-340">Select all the files, and then select **Next**.</span></span>

    ![Visu failu atlasīšana](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="c6395-342">Veiciet dubultklikšķi uz .msi pakotnes, lai palaistu instalēšanas programmu.</span><span class="sxs-lookup"><span data-stu-id="c6395-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="c6395-343">Pēc tam, kad instalēšana ir pabeigta, atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT instalēšanas programmas fails](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="c6395-345">Selenium un pārlūka draiveru instalēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="c6395-346">Vecākās RSAT versijās bija nepieciešams instalēt Selenium un pārlūka draiverus.</span><span class="sxs-lookup"><span data-stu-id="c6395-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="c6395-347">Tagad šie draiveri vairs nav jāinstalē, jo tie ir instalēti automātiski.</span><span class="sxs-lookup"><span data-stu-id="c6395-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="c6395-348">Pirmo reizi atverot RSAT, tiek parādīta uzvedne ar aicinājumu automātiski lejupielādēt un instalēt Selenium.</span><span class="sxs-lookup"><span data-stu-id="c6395-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="c6395-349">Papildinformāciju skatiet sadaļā [RSAT konfigurēšana](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="c6395-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="c6395-350">Lai varētu palaist testa gadījumu, vispirms tiek parādīta uzvedne ar aicinājumu automātiski lejupielādēt un instalēt pārlūka draiveri, kas atbilst noklusējuma pārlūkam, kurš atlasīts RSAT konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="c6395-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="c6395-351">Papildinformāciju skatiet sadaļā [Testa gadījumu ielādēšana un palaišana](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="c6395-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="c6395-352">Darba sākšana ar RSAT</span><span class="sxs-lookup"><span data-stu-id="c6395-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="c6395-353">Testēšanas plāna un testu komplektu izveide</span><span class="sxs-lookup"><span data-stu-id="c6395-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="c6395-354">Dodieties uz Azure DevOps projektu un atlasiet **Testēšanas plāni**.</span><span class="sxs-lookup"><span data-stu-id="c6395-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Testēšanas plānu komanda](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="c6395-356">Atlasiet **Jauns testēšanas plāns**.</span><span class="sxs-lookup"><span data-stu-id="c6395-356">Select **New Test Plan**.</span></span>

    ![Poga Jauns testēšanas plāns](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="c6395-358">Aizpildiet lauku **Nosaukums** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="c6395-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="c6395-359">Šajā apmācībā piešķiriet testēšanas plānam nosaukumu **RSAT testēšanas plāns**.</span><span class="sxs-lookup"><span data-stu-id="c6395-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Dialoglodziņš Jauns testēšanas plāns](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="c6395-361">Atlasiet plus zīmi (**+**) un pēc tam atlasiet **Statisks komplekts**, lai izveidotu statisku komplektu atbilstoši jaunajam testēšanas plānam.</span><span class="sxs-lookup"><span data-stu-id="c6395-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="c6395-362">Piešķiriet jaunajam testu komplektam nosaukumu **T01 – Veikt uz krājumiem**.</span><span class="sxs-lookup"><span data-stu-id="c6395-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-363">Varat arī izveidot uz vaicājumiem balstītu komplektu, ja vēlaties, lai jaunie testa gadījumi no BPM tiktu automātiski ievietoti RSAT testu komplektā.</span><span class="sxs-lookup"><span data-stu-id="c6395-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Statiska komplekta izveide](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="c6395-365">Testa gadījumu pievienošana testu komplektiem</span><span class="sxs-lookup"><span data-stu-id="c6395-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="c6395-366">Atlasiet **Pievienot esošu**, kas atrodas labajā pusē, lai pievienotu testu komplektam esošos testa gadījumus.</span><span class="sxs-lookup"><span data-stu-id="c6395-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Poga Pievienot esošu](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="c6395-368">Lapā **Pievienot testa gadījumus komplektam** atlasiet **Izpildīt vaicājumu** un pēc tam atlasiet testa gadījumu, ko pievienot testu komplektam.</span><span class="sxs-lookup"><span data-stu-id="c6395-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="c6395-369">Šajā apmācībā atlasiet testa gadījumu **Jaunas preces izveide**.</span><span class="sxs-lookup"><span data-stu-id="c6395-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="c6395-370">Pēc tam atlasiet **Pievienot testa gadījumus** lapas labajā apakšējā stūrī (šī poga nākamajā attēlā nav parādīta).</span><span class="sxs-lookup"><span data-stu-id="c6395-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Poga Izpildīt vaicājumu](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="c6395-372">Testa gadījums ir pievienots testu komplektam **T01 – Veikt uz krājumiem**.</span><span class="sxs-lookup"><span data-stu-id="c6395-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testu komplektam pievienots testa gadījums](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="c6395-374">Konfigurēt RSAT</span><span class="sxs-lookup"><span data-stu-id="c6395-374">Configure RSAT</span></span>

1. <span data-ttu-id="c6395-375">Atveriet RSAT.</span><span class="sxs-lookup"><span data-stu-id="c6395-375">Open RSAT.</span></span>

    ![RSAT ikona](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="c6395-377">Tiek parādīts brīdinājuma ziņojums ar tekstu “Rīkam Regression Suite Automation Tool ir nepieciešama platforma Selenium; vai vēlaties tūlīt automātiski lejupielādēt un instalēt to?”.</span><span class="sxs-lookup"><span data-stu-id="c6395-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="c6395-378">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c6395-378">Select **Yes**.</span></span>

    ![Brīdinājuma ziņojums, ka Regression Suite Automation Tool pieprasa platformu Selenium](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="c6395-380">Atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī un pēc tam atvērtajā dialoglodziņā aizpildiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="c6395-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="c6395-381">**Azure DevOps URL**— ievadiet jūsu Azure DevOps projekta URL, piemēram, `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="c6395-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="c6395-382">**Piekļuves pilnvara**— ievadiet piekļuves pilnvaru, kas ļauj izveidot savienojumu ar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="c6395-383">Izmantojiet personiskās piekļuves pilnvaru, ko izveidojāt iepriekš šajā pamācībā.</span><span class="sxs-lookup"><span data-stu-id="c6395-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="c6395-384">Papildinformāciju skatiet sadaļā [Piekļuves autentificēšana ar personiskās piekļuves tiesībām](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="c6395-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="c6395-385">**Projekta nosaukums**— atlasiet Azure DevOps projekta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="c6395-386">**Testēšanas plāns**— atlasiet Azure DevOps testēšanas plānu, kas satur jūsu testa gadījumus.</span><span class="sxs-lookup"><span data-stu-id="c6395-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="c6395-387">Papildinformāciju skatiet sadaļā [Testēšanas plānu un testu komplektu izveide](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="c6395-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="c6395-388">Pēc testa plāna atlasīšanas atlasiet **Testēt savienojumu**, lai testētu savienojumu ar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="c6395-389">**Resursdatora nosaukums** — ievadiet testa vides resursdatora nosaukumu, piemēram, **\<myaos\>myaos.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="c6395-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="c6395-390">Neiekļaujiet prefiksu **https://** vai **http://**.</span><span class="sxs-lookup"><span data-stu-id="c6395-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="c6395-391">**SOAP resursdatora nosaukums**— ievadiet testa vides SOAP resursdatora nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="c6395-392">Parasti SOAP resursdatora nosaukums ir tāds pats kā resursdatora nosaukums, bet tam ir sufikss **soap**.</span><span class="sxs-lookup"><span data-stu-id="c6395-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="c6395-393">Šeit ir piemērs: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="c6395-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="c6395-394">Neiekļaujiet prefiksu **https://** vai **http://**.</span><span class="sxs-lookup"><span data-stu-id="c6395-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c6395-395">Lai atrastu resursdatora nosaukumu un SOAP resursdatora nosaukumu, atveriet IIS pārvaldnieku, ar peles labo pogu noklikšķiniet uz **Vietnes \> AOSService** un pēc tam atlasiet **Rediģēt saistījumus**.</span><span class="sxs-lookup"><span data-stu-id="c6395-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="c6395-396">Vērtības kolonnā **Resursdatora nosaukums** norāda resursdatora nosaukumu un SOAP resursdatora nosaukumu (SOAP resursdatora nosaukuma URL satur sufiksu **soap** ).</span><span class="sxs-lookup"><span data-stu-id="c6395-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Resursdatora nosaukums un SOAP resursdatora nosaukums kolonnā Resursdatora nosaukums](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="c6395-398">**Administratora lietotājvārds**— ievadiet administratora lietotāja e-pasta adresi testa vidē.</span><span class="sxs-lookup"><span data-stu-id="c6395-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="c6395-399">**Īssavilkums**— ievadiet autentifikācijas sertifikāta nospiedumu, kā aprakstīts iepriekš šajā pamācībā.</span><span class="sxs-lookup"><span data-stu-id="c6395-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="c6395-400">**Darba direktorijs**— norādiet mapes atrašanās vietu, kur saglabāt testu automatizācijas failus, piemēram, Excel testu datu failus.</span><span class="sxs-lookup"><span data-stu-id="c6395-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="c6395-401">Piemēram, ievadiet vai atlasiet **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="c6395-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c6395-402">Ja mapes nosaukumā ir atstarpes, izpilde neizdodas, jo mapi nevar atrast.</span><span class="sxs-lookup"><span data-stu-id="c6395-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="c6395-403">Šī problēma ir zināma, un jaunākajā rīka versijā tai jābūt labotai.</span><span class="sxs-lookup"><span data-stu-id="c6395-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="c6395-404">**Noklusējuma pārlūks**— atlasiet **Internet Explorer** vai **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="c6395-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="c6395-405">Pārliecinieties, ka ir instalēti atbilstošie pārlūka draiveri.</span><span class="sxs-lookup"><span data-stu-id="c6395-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="c6395-406">**Testa izpildes taimauts**— norādiet testa izpilžu taimauta periodu minūtēs.</span><span class="sxs-lookup"><span data-stu-id="c6395-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="c6395-407">Kad taimauta periods ir beidzies, visi aktīvie logi tiek aizvērti, un gaidoši testa gadījumi ir nesekmīgi.</span><span class="sxs-lookup"><span data-stu-id="c6395-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="c6395-408">**Testa darbības taimauts**— šis lauks kontrolē Finance and Operation vides servera pieprasījumu taimauta periodu minūtēs.</span><span class="sxs-lookup"><span data-stu-id="c6395-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="c6395-409">Parasti noklusējuma vērtība (2 minūtes) ir pietiekama.</span><span class="sxs-lookup"><span data-stu-id="c6395-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="c6395-410">Tomēr lēnākās vidēs šo vērtību var būt nepieciešams palielināt, ja rodas ar taimautu saistītas problēmas.</span><span class="sxs-lookup"><span data-stu-id="c6395-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="c6395-411">**Uzņēmuma nosaukums**— ievadiet tā uzņēmuma nosaukumu, ko izmantot kā noklusējuma uzņēmumu, kad tiek izveidoti Excel parametru faili.</span><span class="sxs-lookup"><span data-stu-id="c6395-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="c6395-412">Vēlāk varat nomainīt uzņēmumu, rediģējot Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="c6395-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Dialoglodziņš Iestatījumi](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="c6395-414">Atlasiet **Lietot**, lai lietotu un saglabātu iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c6395-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="c6395-415">Lai pašreizējos iestatījumus saglabātu konfigurācijas failā datorā, atlasiet **Saglabāt kā**.</span><span class="sxs-lookup"><span data-stu-id="c6395-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="c6395-416">Lai pašreizējos iestatījumus atjaunotu no konfigurācijas faila datorā, atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="c6395-417">Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="c6395-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="c6395-418">Testa gadījumu ielāde un izpilde</span><span class="sxs-lookup"><span data-stu-id="c6395-418">Load and run test cases</span></span>

1. <span data-ttu-id="c6395-419">Atlasiet **Ielādēt**, lai ielādētu testēšanas plānu **RSAT testēšanas plāns** no Azure DevOps projekta.</span><span class="sxs-lookup"><span data-stu-id="c6395-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Poga Ielādēt](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="c6395-421">Testu komplektā atlasiet testa gadījumu **Jaunas preces izveide** un pēc tam atlasiet **Jauns \> Ģenerēt testa izpildes un parametru failus**.</span><span class="sxs-lookup"><span data-stu-id="c6395-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Komanda Ģenerēt testa izpildes un parametru failus izvēlnē Jauns](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="c6395-423">Excel parametru fails tiek izveidots lokālajā mapē, kas norādīta RSAT konfigurācijā (piemēram, **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="c6395-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Excel parametru faila izveide](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="c6395-425">Ja vēlaties saglabāt parametru failus, atlasiet **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="c6395-426">Visu atlasīto testa gadījumu testu automatizācijas faili tiek augšupielādēti pakalpojumā Azure DevOps turpmākai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="c6395-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="c6395-427">(Šie faili ietver Excel testa parametru failus.)</span><span class="sxs-lookup"><span data-stu-id="c6395-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="c6395-428">Šādā veidā varat atlasīt **Ielādēt**, lai ielādētu testa gadījuma parametru failus (un automatizācijas failus) tieši no Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="c6395-429">Nav nepieciešams ģenerēt parametru failus atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="c6395-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="c6395-430">Šī pieeja kļūs svarīga vēlāk, ja vēlēsities saglabāt modifikācijas parametru failā un nevēlēsities tos pārrakstīt.</span><span class="sxs-lookup"><span data-stu-id="c6395-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="c6395-431">Lai pārbaudītu, vai automatizācijas faili un parametru faili tiek saglabāti Azure DevOps, dodieties uz Azure DevOps projektu, atlasiet **Paneļi \> Darba vienumi** un atlasiet testa gadījumu **Jaunas preces izveide**.</span><span class="sxs-lookup"><span data-stu-id="c6395-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="c6395-432">Cilnē **Pielikumi** ir jābūt redzamiem četriem failiem:</span><span class="sxs-lookup"><span data-stu-id="c6395-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="c6395-433">**.cs**— C\# automatizācijas fails</span><span class="sxs-lookup"><span data-stu-id="c6395-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="c6395-434">**.dll**— kompilētais automatizācijas fails kā komplektācija</span><span class="sxs-lookup"><span data-stu-id="c6395-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="c6395-435">**.xlsx**— Excel parametru fails</span><span class="sxs-lookup"><span data-stu-id="c6395-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="c6395-436">**.xml**— ieraksta fails</span><span class="sxs-lookup"><span data-stu-id="c6395-436">**.xml** – Recording file</span></span>

    ![Faili cilnē Pielikumi](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="c6395-438">Atlasiet testa gadījumu, ko izpildīt, un pēc tam atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="c6395-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-439">Ja kā pārlūku izmantojat Internet Explorer, pirms testa gadījumu izpildīšanas pārliecinieties, ka darbvirsmas izšķirtspēja ir iestatīta uz **100%** sadaļā **Windows displeja iestatījumi \> Mērogs un izkārtojums**.</span><span class="sxs-lookup"><span data-stu-id="c6395-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="c6395-440">Ja nevarat mainīt šo iestatījumu virtuālajā mašīnā (VM), nomainiet to klientā (klēpjdatorā), no kura mēģināt piekļūt VM.</span><span class="sxs-lookup"><span data-stu-id="c6395-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="c6395-441">Pēc tam VM displeja iestatījumi pārmanto izšķirtspējas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c6395-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Darbvirsmas izšķirtspēja ir iestatīta uz 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="c6395-443">Ja pārlūka draiveri sistēmā nav instalēti, tiek parādīts brīdinājuma ziņojums ar tekstu “Šai operācijai ir nepieciešams \<browser name\> draiveris.</span><span class="sxs-lookup"><span data-stu-id="c6395-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="c6395-444">Vai vēlaties tagad automātiski lejupielādēt un instalēt to?”.</span><span class="sxs-lookup"><span data-stu-id="c6395-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="c6395-445">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c6395-445">Select **Yes**.</span></span>

    ![Brīdinājuma ziņojums pārlūkam Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Brīdinājuma ziņojums pārlūkam Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="c6395-448">Ja kā pārlūku izmantojat Chrome un saņemat kļūdas ziņojumu, kurā norādīts, ka sesija netika izveidota, jo Chrome versija nav pareiza, lejupielādējiet jaunāko Chrome draiveri no vietnes <http://chromedriver.chromium.org/downloads> mapē **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="c6395-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Kļūdas ziņojums pārlūkam Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="c6395-450">Testa gadījums tiek izpildīts, un lauks **Rezultāts** tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="c6395-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Lauks Atjauninātais rezultāts](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="c6395-452">Ja izpildījāt šo apmācību atbilstoši norādījumiem, testa gadījums **Jaunas preces izveide** būs nesekmīgs, jo preces izveides uzdevuma ieraksts saglabāja preces nosaukumu kā stingri kodētu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6395-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="c6395-453">Izpildot šo testa gadījumu atkārtoti, tiek parādīts kļūdas ziņojums, jo prece jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="c6395-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Lauks Rezultāts ir iestatīts kā Nesekmīgs](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="c6395-455">Testa rezultātu skatīšana</span><span class="sxs-lookup"><span data-stu-id="c6395-455">View the test results</span></span>

1. <span data-ttu-id="c6395-456">Veiciet dubultklikšķi uz nesekmīgā testa gadījuma.</span><span class="sxs-lookup"><span data-stu-id="c6395-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="c6395-457">Tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="c6395-457">You receive an error message.</span></span>

    ![Kļūdas ziņojums](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="c6395-459">Atlasiet **Detalizēti**, lai skatītu pilnu kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-459">Select **Details** to view the whole error message.</span></span>

    ![Pilns kļūdas ziņojums](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="c6395-461">Lai skatītu detalizētu kļūdas ziņojuma versiju pakalpojumā Azure DevOps, atlasiet **Atvērt pakalpojumā Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="c6395-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="c6395-462">Pakalpojumā Azure DevOps var skatīt testa gadījuma statusu un detalizētu kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Detalizēts kļūdas ziņojums pakalpojumā Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="c6395-464">Lai skatītu testa rezultātus tieši Azure DevOps projektā, dodieties uz **Testēšanas plāni \> Testēšanas plāni \> Izpildes**.</span><span class="sxs-lookup"><span data-stu-id="c6395-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="c6395-465">Veiciet dubultklikšķi uz testa izpildes, par kuru vēlaties skatīt detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="c6395-465">Double-click the test run that you want to see more details for.</span></span>

    ![Testa izpilžu saraksts pakalpojumā Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="c6395-467">Cilnē **Izpildes kopsavilkums** ir norādīts, ka testa gadījums ir nesekmīgs, bet nav sniegts faktiskais kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="c6395-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="c6395-468">Lai skatītu detalizētu kļūdas ziņojumu, atlasiet cilni **Testa rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="c6395-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Cilne Izpildes kopsavilkums](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="c6395-470">Cilnē **Testa rezultāti** ir sniegta informācija par testa gadījumu, iznākums un kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="c6395-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Cilne Testa rezultāti](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="c6395-472">Veiciet dubultklikšķi uz atbilstošā ieraksta, lai skatītu detalizētu kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Detalizēts kļūdas ziņojums](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="c6395-474">Visi kļūdu ziņojumi ir pieejami arī lokāli direktorijā **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="c6395-475">Varat arī eksportēt testa izpildes rezultātus no testēšanas plāna līmeņa, atlasot **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Testēšanas plāna eksportēšana](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="c6395-477">Excel parametru faila modificēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="c6395-478">Atveriet RSAT.</span><span class="sxs-lookup"><span data-stu-id="c6395-478">Open RSAT.</span></span>
2. <span data-ttu-id="c6395-479">Atlasiet testa gadījumu un pēc tam atlasiet **Rediģēt**, lai atvērtu Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="c6395-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="c6395-480">Lapā **EcoResProductCreate** ievērojiet, ka lauka **Preces numurs** vērtība ir stingri kodēta.</span><span class="sxs-lookup"><span data-stu-id="c6395-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="c6395-481">Pirms atkārtotas testa gadījuma palaišanas preces numurs šajā laukā ir jāatjaunina uz jaunās preces numuru.</span><span class="sxs-lookup"><span data-stu-id="c6395-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="c6395-482">Lai ģenerētu unikālu preces numuru katrai izpildei bez vajadzības atkārtoti atvērt Excel parametru failu un manuāli atjaunināt preces numuru katru reizi, izmantojiet šādu Excel formulu.</span><span class="sxs-lookup"><span data-stu-id="c6395-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="c6395-483">Papildus cilnei **Vispārīgi** Excel parametru failā ir ietverta datu cilne katrai veidlapas lapai, kura tiek pārskatīta testa gadījuma izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="c6395-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Lauks Preces numurs](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="c6395-485">Atlasiet **Saglabāt** un pēc tam aizveriet Excel darbgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="c6395-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="c6395-486">Atlasiet **Augšupielādēt**, lai saglabātu Excel parametru failu pakalpojumā Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Ziņojums par sekmīgu augšupielādēšanu](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="c6395-488">Lai palaistu testa gadījumus noteikta lietotāja kontekstā, ievadiet lietotāja e-pasta ID Excel parametru faila laukā **Testēt lietotāju**, kas atrodas cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="c6395-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="c6395-489">Jaunākajā RSAT versijā Excel parametru faila lauku izkārtojums ir atjaunināts, bet koncepcija paliek tāda pati.</span><span class="sxs-lookup"><span data-stu-id="c6395-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Lauks Testēt lietotāju](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="c6395-491">Rezultātu pārbaude</span><span class="sxs-lookup"><span data-stu-id="c6395-491">Validate the results</span></span>

- <span data-ttu-id="c6395-492">Atlasiet **Palaist**, lai palaistu testa gadījumu, un pārbaudiet, vai testa gadījums ir sekmīgs.</span><span class="sxs-lookup"><span data-stu-id="c6395-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="c6395-493">Varat skatīt testa rezultātus, kā aprakstīts sadaļā [Testa rezultātu skatīšana](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="c6395-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Lauks Rezultāts ir iestatīts kā Sekmīgs](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="c6395-495">Testa gadījumu ķēde</span><span class="sxs-lookup"><span data-stu-id="c6395-495">Chaining of test cases</span></span>

<span data-ttu-id="c6395-496">Viens no RSAT svarīgākajiem līdzekļiem ir testa gadījumu savienošana ķēdē (jeb iespēja nodot testa vērtības citiem testiem).</span><span class="sxs-lookup"><span data-stu-id="c6395-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="c6395-497">Testa gadījumi tiek palaisti atbilstoši secībai, kas noteikta Azure DevOps testēšanas plānā.</span><span class="sxs-lookup"><span data-stu-id="c6395-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="c6395-498">(Šo secību var atjaunināt pašā testēšanas rīkā.) Tādēļ, ja vēlaties pārnest mainīgos no viena testa gadījuma uz citu, ir ļoti svarīgi, lai testi būtu pareizā secībā.</span><span class="sxs-lookup"><span data-stu-id="c6395-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="c6395-499">Šajā sadaļā parādīts, kā izveidot saglabātu mainīgo pirmajā testa gadījumā, izveidot otru testa gadījumu un pārnest saglabāto mainīgo no pirmā testa gadījuma uz otro testa gadījumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="c6395-500">Pēc tam testa gadījumi tiek izpildīti kā testa gadījumu ķēde rīkā RSAT.</span><span class="sxs-lookup"><span data-stu-id="c6395-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="c6395-501">Esoša uzdevuma ieraksta modificēšana saglabāta mainīgā izveidei</span><span class="sxs-lookup"><span data-stu-id="c6395-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="c6395-502">Atveriet klientu.</span><span class="sxs-lookup"><span data-stu-id="c6395-502">Open the client.</span></span>
2. <span data-ttu-id="c6395-503">Atlasiet pogu **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Uzdevuma reģistrētājs**.</span><span class="sxs-lookup"><span data-stu-id="c6395-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="c6395-504">Atlasiet **Rediģēt ierakstu**.</span><span class="sxs-lookup"><span data-stu-id="c6395-504">Select **Edit Recording**.</span></span>

    ![Poga Rediģēt ierakstu](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="c6395-506">Atlasiet **Atvērt no Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="c6395-506">Select **Open from Lifecycle Services**.</span></span>

    ![Poga Atvērt no Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="c6395-508">Atlasiet **Atlasīt Lifecycle Services bibliotēku**.</span><span class="sxs-lookup"><span data-stu-id="c6395-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Poga Atlasīt Lifecycle Services bibliotēku](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="c6395-510">BPM bibliotēkas tiek ielādētas no LCS.</span><span class="sxs-lookup"><span data-stu-id="c6395-510">BPM libraries are loaded from LCS.</span></span>

    ![BPM bibliotēku ielāde](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="c6395-512">Pēc BPM bibliotēku ielādēšanas no LCS atlasiet BPM bibliotēku **RSAT** un biznesa procesu **Jaunas preces izveide**, ar kuru bija saistīts uzdevuma ieraksts.</span><span class="sxs-lookup"><span data-stu-id="c6395-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="c6395-513">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c6395-513">Then select **OK**.</span></span>

    ![BPM bibliotēkas un biznesa procesa atlase](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="c6395-515">Atbilstošā uzdevuma ieraksta nosaukums tiek ievadīts laukā **Ieraksta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="c6395-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="c6395-516">Atlasiet **Sākt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-516">Select **Start**.</span></span>

    ![Uzdevuma ieraksta nosaukums laukā Ieraksta nosaukums](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="c6395-518">Dodieties uz **Preču informācijas pārvaldība \> Preces** un atlasiet **Jauns**, lai atvērtu lapu, kurā tika reģistrēts sākotnējais uzdevuma ieraksts **Preces izveide**.</span><span class="sxs-lookup"><span data-stu-id="c6395-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="c6395-519">Atlasiet **Ievietot darbību**.</span><span class="sxs-lookup"><span data-stu-id="c6395-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-520">Jaunā darbība tiek ievietota **pēc** darbības, kuru atlasījāt rūtī.</span><span class="sxs-lookup"><span data-stu-id="c6395-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Poga Ievietot darbību](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="c6395-522">Ar peles labo pogu noklikšķiniet uz lauka **Preces numurs** un pēc tam atlasiet **Uzdevuma reģistrētājs \> Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Komanda Kopēt](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="c6395-524">Rūtī tiek pievienota jauna darbība.</span><span class="sxs-lookup"><span data-stu-id="c6395-524">A new step is added in the pane.</span></span> <span data-ttu-id="c6395-525">Pierakstiet laukā **Preces numurs** redzamo vērtību, jo tā būs nepieciešama vēlāk.</span><span class="sxs-lookup"><span data-stu-id="c6395-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Pievienota jauna darbība](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="c6395-527">Atlasiet **Rediģēšana pabeigta**.</span><span class="sxs-lookup"><span data-stu-id="c6395-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="c6395-528">Atlasiet **Saglabāt pakalpojumos Lifecycle Services** un saistiet jauno uzdevuma ierakstu ar to pašu BPM bibliotēku un biznesa procesu, ar kuru tika saistīts sākotnējais uzdevuma ieraksts.</span><span class="sxs-lookup"><span data-stu-id="c6395-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="c6395-529">Papildinformāciju skatiet sadaļā [Uzdevuma ieraksta izveide un saglabāšana BPM bibliotēkā](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="c6395-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="c6395-530">Dodieties uz BPM bibliotēku un atlasiet **Sinhronizēt testa piemērus**, lai pārrakstītu uzdevuma ierakstu, kas ir pievienots testa gadījumam pakalpojumā Azure DevOps, kā aprakstīts sadaļā [Sinhronizācijas testēšana no BPM ar Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="c6395-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="c6395-531">Atveriet RSAT un atlasiet **Ielādēt**, lai atkārtoti ielādētu visus testa gadījumus testu komplektā.</span><span class="sxs-lookup"><span data-stu-id="c6395-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="c6395-532">Ir nepieciešams atkārtoti ģenerēt atbilstošā testa gadījuma automatizācijas un parametru failus, atlasot testa gadījumu un pēc tam atlasot **Jauns \> Ģenerēt testa izpildes un parametru failus**, kā aprakstīts sadaļā [Testa gadījumu ielāde un izpilde](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="c6395-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-533">Ja Excel parametru fails ir atstāts atvērts, atkārtota ģenerēšana ir nesekmīga.</span><span class="sxs-lookup"><span data-stu-id="c6395-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="c6395-534">Tāpēc pirms jaunā Excel parametru faila ģenerēšanas pārliecinieties, ka testa gadījuma Excel parametru fails ir aizvērts.</span><span class="sxs-lookup"><span data-stu-id="c6395-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="c6395-535">Atlasiet **Rediģēt**, lai atvērtu jauno Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="c6395-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="c6395-536">9. rindā ir redzams jauns ieraksts **Saglabāts mainīgais**.</span><span class="sxs-lookup"><span data-stu-id="c6395-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="c6395-537">Šis mainīgais **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** tiek saglabāts uzdevuma ieraksta XML failā, un to var izmantot nākamajos testos.</span><span class="sxs-lookup"><span data-stu-id="c6395-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Ieraksts Saglabāts mainīgais](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="c6395-539">Jauna testa gadījuma izveide</span><span class="sxs-lookup"><span data-stu-id="c6395-539">Create a new test case</span></span>

1. <span data-ttu-id="c6395-540">Dodieties uz BPM bibliotēku **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="c6395-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="c6395-541">Atlasiet procesu **Atbalsta biznesa procesa paraugs** un pēc tam labajā pusē atlasiet **Rediģēšanas režīms**.</span><span class="sxs-lookup"><span data-stu-id="c6395-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="c6395-542">Nomainiet lauka **Nosaukums** un lauka **Apraksts** vērtību uz **Preces izlaišana**.</span><span class="sxs-lookup"><span data-stu-id="c6395-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="c6395-543">Pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-543">Then select **Save**.</span></span>

    ![Nosaukums un apraksts ir mainīts uz Preces izlaišana](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="c6395-545">Jauna uzdevuma ieraksta izveide, kam ir funkcija Validēt</span><span class="sxs-lookup"><span data-stu-id="c6395-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="c6395-546">Izveidojiet uzdevuma ierakstu, lai izlaistu preci, kas iepriekš tika izveidota USRT juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="c6395-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="c6395-547">Papildinformāciju skatiet sadaļā [Uzdevuma ieraksta izveide un saglabāšana BPM bibliotēkā](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="c6395-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6395-548">Ķēdē savienotiem testa gadījumiem vienmēr ieteicams atrast vai filtrēt nepieciešamo ierakstu, *ierakstot lauka vērtību manuāli*.</span><span class="sxs-lookup"><span data-stu-id="c6395-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="c6395-549">Šādā veidā rīks var noteikt ierakstu, ar kuru ir jāveic darbība attiecībā pret nākamo testa gadījumu.</span><span class="sxs-lookup"><span data-stu-id="c6395-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Jauns uzdevuma ieraksts, kam ir funkcija Validēt](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="c6395-551">Kā redzams iepriekšējā attēlā, pēc produkta atrašanas, izmantojot ātro filtru, bet pirms vienuma **Izlaist preces** atlasīšanas ir jāvalidē lauka **Preces numurs** vērtība, lai pārliecinātos, ka preces ID ir iepriekš izveidotais preces ID.</span><span class="sxs-lookup"><span data-stu-id="c6395-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="c6395-552">Lai validētu vērtību, ar peles labo pogu noklikšķiniet uz lauka **Preces numurs** un pēc tam atlasiet **Uzdevuma reģistrētājs \> Validēt \> Pašreizējā vērtība**.</span><span class="sxs-lookup"><span data-stu-id="c6395-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Pašreizējās vērtības validēšana](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="c6395-554">Uzdevuma ieraksta saglabāšana BPM</span><span class="sxs-lookup"><span data-stu-id="c6395-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="c6395-555">Kad uzdevuma ieraksts ir pabeigts, atlasiet **Saglabāt pakalpojumos Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="c6395-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Saglabāt Uzdevuma ierakstu pakalpojumos Lifecycle Services](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="c6395-557">Bibliotēkas informācija tiek ielādēta no LCS.</span><span class="sxs-lookup"><span data-stu-id="c6395-557">Library information is loaded from LCS.</span></span>

    ![Notiek bibliotēkas informācijas ielāde](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="c6395-559">Atlasiet BPM bibliotēku, kuru saistīt ar uzdevuma ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c6395-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="c6395-560">Šajā apmācībā atlasiet BPM bibliotēku **RSAT**, kas tika izveidota iepriekš, un biznesa procesu **Preces izlaišana** zem tās.</span><span class="sxs-lookup"><span data-stu-id="c6395-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="c6395-561">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c6395-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="c6395-562">BPM sinhronizēšana ar Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="c6395-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="c6395-563">Dodieties uz BPM bibliotēku un atveriet bibliotēku **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="c6395-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="c6395-564">Atlasiet **VSTS sinhronizācija** un pēc tam atlasiet **Sinhronizēt testa gadījumus**.</span><span class="sxs-lookup"><span data-stu-id="c6395-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="c6395-565">Papildinformāciju skatiet sadaļā [Sinhronizācijas testēšana no BPM ar Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="c6395-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="c6395-566">Kad sinhronizācija ir pabeigta, jaunais darba vienums un atbilstošais testa gadījums biznesa procesam **Preces izlaišana** tiek parādīts pakalpojumā Azure DevOps šeit: **Paneļi \> Darba vienumi**.</span><span class="sxs-lookup"><span data-stu-id="c6395-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="c6395-567">Jauna testa gadījuma pievienošana esošajam testu komplektam</span><span class="sxs-lookup"><span data-stu-id="c6395-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="c6395-568">Dodieties uz **Testēšanas plāni \> Testēšanas plāni** un atlasiet plānu **RSAT testēšanas plāns**.</span><span class="sxs-lookup"><span data-stu-id="c6395-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="c6395-569">Atlasiet **Pievienot esošu**.</span><span class="sxs-lookup"><span data-stu-id="c6395-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="c6395-570">Lapā **Pievienot testa gadījumus komplektam** atlasiet **Izpildīt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="c6395-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="c6395-571">Atlasiet jauno testa gadījumu, kas tika izveidots procesam **Preces izlaišana**, un pēc tam atlasiet **Pievienot testa gadījumus** lapas apakšējā labajā stūrī (šī poga nākamajā attēlā nav redzama).</span><span class="sxs-lookup"><span data-stu-id="c6395-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Lapa Pievienot testa gadījumus komplektam](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="c6395-573">Tagad testu komplektā ir divi testa gadījumi.</span><span class="sxs-lookup"><span data-stu-id="c6395-573">The test suite now has two test cases.</span></span>

    ![Divi testa gadījumi testu komplektā](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="c6395-575">Testa gadījumu ielādēšana rīkā RSAT</span><span class="sxs-lookup"><span data-stu-id="c6395-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="c6395-576">Atveriet RSAT un atlasiet **Ielādēt**.</span><span class="sxs-lookup"><span data-stu-id="c6395-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="c6395-577">Testa gadījumi tiek ielādēti, un tiek parādīts brīdinājums ar tekstu “Veicot šo darbību, tiks pārrakstīti Excel testa datu faili, un lokālās izmaiņas tiks zaudētas.</span><span class="sxs-lookup"><span data-stu-id="c6395-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="c6395-578">Vai vēlaties turpināt?”.</span><span class="sxs-lookup"><span data-stu-id="c6395-578">Do you want to proceed?"</span></span> <span data-ttu-id="c6395-579">Atlasiet **Jā**, lai atjauninātu Excel parametru failus lokālajā sistēmā, bet ne tos Excel parametru failus, kas tika augšupielādēti pakalpojumā Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Ar šo darbību tiks pārrakstīti Excel testa datu faili](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="c6395-581">Abi testa gadījumi tiek ielādēti kopā ar pirmā testa gadījuma Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="c6395-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="c6395-582">Pēdējā izpildē jūs atlasījāt **Augšupielādēt**, tādēļ parametru faili tiek ņemti no Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="c6395-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Ielādētie testa gadījumi](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="c6395-584">Atlasiet tikai otro testa gadījumu un pēc tam atlasiet **Jauns \> Ģenerēt testa izpildes un parametru failus**.</span><span class="sxs-lookup"><span data-stu-id="c6395-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="c6395-585">Excel parametru faila rediģēšana</span><span class="sxs-lookup"><span data-stu-id="c6395-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="c6395-586">Atlasiet tikai otro testa gadījumu un pēc tam atlasiet **Rediģēt**, lai atvērtu atbilstošo Excel parametru failu.</span><span class="sxs-lookup"><span data-stu-id="c6395-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="c6395-587">Kopējiet saglabāto mainīgo **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (skatiet sadaļu [Esoša uzdevuma ieraksta modificēšana, lai izveidotu saglabātu mainīgo](#modify-an-existing-task-recording-to-create-a-saved-variable) ) no pirmā testa gadījuma visos laukos, kur tiek izmantots preces numurs.</span><span class="sxs-lookup"><span data-stu-id="c6395-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="c6395-588">Šajā gadījumā mainīgais ir jākopē laukos **Preces numurs** un **Validēt preces numuru** lapā **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="c6395-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Lauki Preces numurs un Validēt preces numuru](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="c6395-590">Mainīgie var tikt nodoti starp testiem tikai tās pašas testa izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="c6395-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="c6395-591">Mainīgo nosaukumiem ir precīzi jāsakrīt.</span><span class="sxs-lookup"><span data-stu-id="c6395-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="c6395-592">Atlasiet **Saglabāt** un pēc tam aizveriet Excel darbgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="c6395-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="c6395-593">Atlasiet **Augšupielādēt**, lai saglabātu izmaiņas, kuras veicāt Excel parametru failā.</span><span class="sxs-lookup"><span data-stu-id="c6395-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="c6395-594">Ķēdē savienoto testa gadījumu palaišana</span><span class="sxs-lookup"><span data-stu-id="c6395-594">Run the chained test cases</span></span>

1. <span data-ttu-id="c6395-595">Atlasiet abus testa gadījumus un pēc tam atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="c6395-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="c6395-596">Pārbaudiet, vai abi testa gadījumi ir sekmīgi.</span><span class="sxs-lookup"><span data-stu-id="c6395-596">Verify that both test cases have passed.</span></span>

    ![Rezultātu lauks ir iestatīts kā sekmīgs abiem testa gadījumiem](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]