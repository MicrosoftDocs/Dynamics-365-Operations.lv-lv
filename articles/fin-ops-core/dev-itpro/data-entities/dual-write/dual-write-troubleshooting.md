---
title: Vispārējā problēmu novēršana
description: Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172695"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="55840-103">Vispārējā problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="55840-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="55840-104">Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="55840-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55840-105">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="55840-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="55840-106">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="55840-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="55840-107">Mēģinot instalēt duālā ieraksta pakotni, izmantojot pakotnes izvietošanas rīku, netiek rādīti pieejami risinājumi</span><span class="sxs-lookup"><span data-stu-id="55840-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="55840-108">Dažas pakotnes izvietošanas rīka versijas nav saderīgas ar duālā ieraksta risinājuma pakotni.</span><span class="sxs-lookup"><span data-stu-id="55840-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="55840-109">Lai veiksmīgi instalētu pakotni, pārliecinieties, vai izmantojat pakotnes izvietošanas rīka [versiju 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="55840-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="55840-110">Pēc pakotnes izvietošanas rīka instalēšanas, instalējiet risinājumu pakotni, izpildot šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="55840-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="55840-111">Lejupielādējiet jaunāko risinājumu pakotnes failu no Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="55840-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="55840-112">Kad pakotnes ZIP fails ir lejupielādēts, ar peles labo pogu noklikšķiniet uz tā un atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="55840-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="55840-113">Atzīmējiet izvēles rūtiņu **Atbloķēt** un pēc tam atlasiet **Piemērot**.</span><span class="sxs-lookup"><span data-stu-id="55840-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="55840-114">Ja nav redzama izvēles rūtiņa **Atbloķēt**, ZIP fails jau ir atbloķēts, un šo darbību var izlaist.</span><span class="sxs-lookup"><span data-stu-id="55840-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Rekvizītu dialoglodziņš](media/unblock_option.png)

2. <span data-ttu-id="55840-116">Izvelciet pakotnes ZIP failu un iekopējiet visus failus mapē **Dynamics365FinanceAndOperationsCommon. ackageDeployer. 2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="55840-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Mapes Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 saturs](media/extract_package.png)

3. <span data-ttu-id="55840-118">Ielīmējiet visus kopētos failus pakotnes izvietošanas rīka mapē **Rīki**.</span><span class="sxs-lookup"><span data-stu-id="55840-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="55840-119">Palaidiet **PackageDeployer.exe**, lai atlasītu Common Data Service vidi un instalētu risinājumus.</span><span class="sxs-lookup"><span data-stu-id="55840-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Rīku mapes saturs](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="55840-121">Spraudņa trasēšanas žurnāla iespējošana un skatīšana sistēmā Common Data Service, lai skatītu kļūdas informāciju</span><span class="sxs-lookup"><span data-stu-id="55840-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="55840-122">**Nepieciešamā loma, lai ieslēgtu trasēšanas žurnālu un skatītu kļūdas:** sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="55840-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="55840-123">Lai aktivizētu trasēšanas žurnālu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="55840-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="55840-124">Piesakieties Finance and Operations programmā, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Sistēma**atlasiet **Administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="55840-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="55840-125">Lapā **Administrēšana** atlasiet opciju **Sistēmas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="55840-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="55840-126">Cilnes **Pielāgošana** laukā **Spraudņa un pielāgotās darbplūsmas aktivitātes izsekošana** atlasiet **Visi**, lai iespējotu spraudņa izsekošanas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="55840-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="55840-127">Ja vēlaties izsekot trasēšanas žurnāliem tikai tad, ja rodas izņēmumi, varat tā vietā izvēlēties opciju **Izņēmums**.</span><span class="sxs-lookup"><span data-stu-id="55840-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="55840-128">Lai skatītu trasēšanas žurnālu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="55840-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="55840-129">Piesakieties Finance and Operations programmā, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Pielāgošana**atlasiet **Spraudņa trasēšanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="55840-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="55840-130">Atrodiet trasēšanas žurnālus, kur lauks **Veida nosaukums** ir iestatīts uz **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="55840-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="55840-131">Veiciet dubultklikšķi uz elementa, lai apskatītu pilno žurnālu, un pēc tam kopsavilkuma cilnē **Izpilde** pārskatiet **Ziņojuma bloka** tekstu.</span><span class="sxs-lookup"><span data-stu-id="55840-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="55840-132">Atkļūdošanas režīma iespējošana, lai novērstu tiešsaistes sinhronizācijas problēmas Finance and Operations programmās</span><span class="sxs-lookup"><span data-stu-id="55840-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="55840-133">**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="55840-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="55840-134">Common Data Service radušās duālā ieraksta kļūdas var parādīties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="55840-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="55840-135">Dažos gadījumos pilns kļūdas ziņojuma teksts nav pieejams, jo ziņojums ir pārāk garš vai satur personu identificējošu informāciju (PII).</span><span class="sxs-lookup"><span data-stu-id="55840-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="55840-136">Varat ieslēgt izvērsto kļūdu reģistrēšanu, izpildot tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="55840-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="55840-137">Visām projekta konfigurācijām Finance and Operations programmās ir **IsDebugMode** rekvizīts elementā **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="55840-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="55840-138">Atveriet elementu **DualWriteProjectConfiguration**, izmantojot Excel pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="55840-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="55840-139">Vienkāršs veids, kā atvērt entītiju, ir ieslēgt režīmu **Noformēšana** Excel pievienojumprogrammā un pēc tam darblapai pievienot **DualWriteProjectConfigurationEntity**.</span><span class="sxs-lookup"><span data-stu-id="55840-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="55840-140">Papildinformāciju skatiet rakstā [Elementa datu atvēršana programmā Excel un to atjaunināšana, izmantojot Excel pievienojumprogrammu](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="55840-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="55840-141">Iestatiet rekvizītu **IsDebugMode** projektam uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="55840-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="55840-142">Palaidiet scenāriju, kas ģenerē kļūdas.</span><span class="sxs-lookup"><span data-stu-id="55840-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="55840-143">Izvērstie žurnāli ir pieejami DualWriteErrorLog tabulā.</span><span class="sxs-lookup"><span data-stu-id="55840-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="55840-144">Lai meklētu datus tabulas pārlūkā, izmantojiet tālāk minēto vietrādi URL (ja nepieciešams, nomainiet **XXX**):</span><span class="sxs-lookup"><span data-stu-id="55840-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="55840-145">Sinhronizācijas kļūdu pārbaude Finance and Operations programmas virtuālajā mašīnā</span><span class="sxs-lookup"><span data-stu-id="55840-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="55840-146">**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="55840-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="55840-147">Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="55840-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="55840-148">Atveriet LCS projektu, kuram izvēlējāties veikt duālā ieraksta pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="55840-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="55840-149">Atlasiet elementu **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="55840-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="55840-150">Izmantojiet attālo darbvirsmu, lai pieteiktos Finance and Operations programmas virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="55840-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="55840-151">Izmantojiet lokālo kontu, kas tiek parādīts LCS.</span><span class="sxs-lookup"><span data-stu-id="55840-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="55840-152">Atveriet Notikumu skatītāju,</span><span class="sxs-lookup"><span data-stu-id="55840-152">Open Event viewer.</span></span>
6. <span data-ttu-id="55840-153">Atlasiet **Lietojumprogrammu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> AX-DualWriteSync \> Darbību**.</span><span class="sxs-lookup"><span data-stu-id="55840-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="55840-154">Pārskatiet neseno kļūdu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="55840-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="55840-155">Atsaistīt un saistīt citu Common Data Service vidi no Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="55840-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="55840-156">**Vides atsaistīšanai nepieciešamie akreditācijas dati:** Azure AD nomnieka administrators</span><span class="sxs-lookup"><span data-stu-id="55840-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="55840-157">Piesakieties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="55840-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="55840-158">Dodieties uz **Darbvietas \>Datu pārvaldība**un atlasiet elementu **Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="55840-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="55840-159">Atlasiet visus darbojošos kartējumus, pēc tam atlasiet **Apturēt**.</span><span class="sxs-lookup"><span data-stu-id="55840-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="55840-160">Atlasiet **Atsaistīt vidi**.</span><span class="sxs-lookup"><span data-stu-id="55840-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="55840-161">Atlasiet **Jā**, lai apstiprinātu darbību.</span><span class="sxs-lookup"><span data-stu-id="55840-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="55840-162">Tagad varat saistīt jaunu vidi.</span><span class="sxs-lookup"><span data-stu-id="55840-162">You can now link a new environment.</span></span>
