---
title: Vispārējā problēmu novēršana
description: Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b01ef3da908739d17f2a03398ae56f35191e8db6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744545"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="495b9-103">Vispārējā problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="495b9-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="495b9-104">Šajā rakstā ir sniegta informācija par vispārējo problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="495b9-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="495b9-105">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="495b9-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="495b9-106">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="495b9-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="495b9-107">Mēģinot instalēt duālā ieraksta pakotni, izmantojot pakotnes izvietošanas rīku, netiek rādīti pieejami risinājumi</span><span class="sxs-lookup"><span data-stu-id="495b9-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="495b9-108">Dažas pakotnes izvietošanas rīka versijas nav saderīgas ar duālā ieraksta risinājuma pakotni.</span><span class="sxs-lookup"><span data-stu-id="495b9-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="495b9-109">Lai veiksmīgi instalētu pakotni, pārliecinieties, vai izmantojat pakotnes izvietošanas rīka [versiju 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="495b9-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="495b9-110">Pēc pakotnes izvietošanas rīka instalēšanas, instalējiet risinājumu pakotni, izpildot šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="495b9-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="495b9-111">Lejupielādējiet jaunāko risinājumu pakotnes failu no Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="495b9-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="495b9-112">Kad pakotnes ZIP fails ir lejupielādēts, ar peles labo pogu noklikšķiniet uz tā un atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="495b9-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="495b9-113">Atzīmējiet izvēles rūtiņu **Atbloķēt** un pēc tam atlasiet **Piemērot**.</span><span class="sxs-lookup"><span data-stu-id="495b9-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="495b9-114">Ja nav redzama izvēles rūtiņa **Atbloķēt**, ZIP fails jau ir atbloķēts, un šo darbību var izlaist.</span><span class="sxs-lookup"><span data-stu-id="495b9-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Rekvizītu dialoglodziņš](media/unblock_option.png)

2. <span data-ttu-id="495b9-116">Izvelciet pakotnes ZIP failu un iekopējiet visus failus mapē **Dynamics365FinanceAndOperationsCommon. ackageDeployer. 2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="495b9-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Mapes Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 saturs](media/extract_package.png)

3. <span data-ttu-id="495b9-118">Ielīmējiet visus kopētos failus pakotnes izvietošanas rīka mapē **Rīki**.</span><span class="sxs-lookup"><span data-stu-id="495b9-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="495b9-119">Palaidiet **PackageDeployer.exe**, lai atlasītu Dataverse vidi un instalētu risinājumus.</span><span class="sxs-lookup"><span data-stu-id="495b9-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![Rīku mapes saturs](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="495b9-121">Spraudņa trasēšanas žurnāla iespējošana un skatīšana Dataverse, lai skatītu kļūdas informāciju</span><span class="sxs-lookup"><span data-stu-id="495b9-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="495b9-122">**Nepieciešamā loma, lai ieslēgtu trasēšanas žurnālu un skatītu kļūdas:** sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="495b9-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="495b9-123">Lai aktivizētu trasēšanas žurnālu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="495b9-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="495b9-124">Piesakieties ar modeli vadītā programmā Dynamics 365, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Sistēma** atlasiet **Administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="495b9-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="495b9-125">Lapā **Administrēšana** atlasiet opciju **Sistēmas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="495b9-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="495b9-126">Cilnes **Pielāgošana** laukā **Spraudņa un pielāgotās darbplūsmas aktivitātes izsekošana** atlasiet **Visi**, lai iespējotu spraudņa izsekošanas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="495b9-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** column, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="495b9-127">Ja vēlaties izsekot trasēšanas žurnāliem tikai tad, ja rodas izņēmumi, varat tā vietā izvēlēties opciju **Izņēmums**.</span><span class="sxs-lookup"><span data-stu-id="495b9-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="495b9-128">Lai skatītu trasēšanas žurnālu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="495b9-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="495b9-129">Piesakieties ar modeli vadītā programmā Dynamics 365, atveriet lapu **Iestatījumi** un pēc tam sadaļā **Pielāgošana** atlasiet **Spraudņa izsekošanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="495b9-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="495b9-130">Atrodiet trasēšanas žurnālus, kur lauks **Veida nosaukums** ir iestatīts uz **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="495b9-130">Find the trace logs where the **Type Name** column is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="495b9-131">Veiciet dubultklikšķi uz elementa, lai apskatītu pilno žurnālu, un pēc tam kopsavilkuma cilnē **Izpilde** pārskatiet **Ziņojuma bloka** tekstu.</span><span class="sxs-lookup"><span data-stu-id="495b9-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="495b9-132">Atkļūdošanas režīma iespējošana, lai novērstu tiešsaistes sinhronizācijas problēmas Finance and Operations programmās</span><span class="sxs-lookup"><span data-stu-id="495b9-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="495b9-133">**Nepieciešamās lomas, lai apskatītu kļūdas:** sistēmas administratora duālās rakstīšanas kļūdas, kas radušās programmā Dataverse, var parādīties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="495b9-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="495b9-134">Dažos gadījumos pilns kļūdas ziņojuma teksts nav pieejams, jo ziņojums ir pārāk garš vai satur personu identificējošu informāciju (PII).</span><span class="sxs-lookup"><span data-stu-id="495b9-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="495b9-135">Varat ieslēgt izvērsto kļūdu reģistrēšanu, izpildot tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="495b9-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="495b9-136">Visām projekta konfigurācijām Finance and Operations programmās ir **IsDebugMode** rekvizīts tabulā **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="495b9-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** table.</span></span> <span data-ttu-id="495b9-137">Atveriet elementu **DualWriteProjectConfiguration**, izmantojot Excel pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="495b9-137">Open the **DualWriteProjectConfiguration** table by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="495b9-138">Vienkāršs veids, kā atvērt tabulu, ir ieslēgt režīmu **Noformēšana** Excel pievienojumprogrammā un pēc tam darblapai pievienot **DualWriteProjectConfigurationEntity**.</span><span class="sxs-lookup"><span data-stu-id="495b9-138">An easy way to open the table is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="495b9-139">Papildinformāciju skatiet rakstā [Elementa datu atvēršana programmā Excel un to atjaunināšana, izmantojot Excel pievienojumprogrammu](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="495b9-139">For more information, see [Open table data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="495b9-140">Iestatiet rekvizītu **IsDebugMode** projektam uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="495b9-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="495b9-141">Palaidiet scenāriju, kas ģenerē kļūdas.</span><span class="sxs-lookup"><span data-stu-id="495b9-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="495b9-142">Izvērstie žurnāli ir pieejami DualWriteErrorLog tabulā.</span><span class="sxs-lookup"><span data-stu-id="495b9-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="495b9-143">Lai meklētu datus tabulas pārlūkā, izmantojiet tālāk minēto vietrādi URL (ja nepieciešams, nomainiet **XXX**):</span><span class="sxs-lookup"><span data-stu-id="495b9-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="495b9-144">Sinhronizācijas kļūdu pārbaude Finance and Operations programmas virtuālajā mašīnā</span><span class="sxs-lookup"><span data-stu-id="495b9-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="495b9-145">**Kļūdu skatīšanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="495b9-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="495b9-146">Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="495b9-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="495b9-147">Atveriet LCS projektu, kuram izvēlējāties veikt duālā ieraksta pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="495b9-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="495b9-148">Atlasiet elementu **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="495b9-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="495b9-149">Izmantojiet attālo darbvirsmu, lai pieteiktos Finance and Operations programmas virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="495b9-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="495b9-150">Izmantojiet lokālo kontu, kas tiek parādīts LCS.</span><span class="sxs-lookup"><span data-stu-id="495b9-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="495b9-151">Atveriet Notikumu skatītāju,</span><span class="sxs-lookup"><span data-stu-id="495b9-151">Open Event viewer.</span></span>
6. <span data-ttu-id="495b9-152">Atlasiet **Lietojumprogrammu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> AX-DualWriteSync \> Darbību**.</span><span class="sxs-lookup"><span data-stu-id="495b9-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="495b9-153">Pārskatiet neseno kļūdu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="495b9-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="495b9-154">Atsaistīt un saistīt citu Dataverse vidi no Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="495b9-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="495b9-155">**Nepieciešamā loma, lai atsaistītu vidi:** sistēmas administrators vai nu Finance and Operations programmai, vai Dataverse.</span><span class="sxs-lookup"><span data-stu-id="495b9-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="495b9-156">Piesakieties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="495b9-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="495b9-157">Dodieties uz **Darbvietas \>Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="495b9-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="495b9-158">Atlasiet visus darbojošos kartējumus, pēc tam atlasiet **Apturēt**.</span><span class="sxs-lookup"><span data-stu-id="495b9-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="495b9-159">Atlasiet **Atsaistīt vidi**.</span><span class="sxs-lookup"><span data-stu-id="495b9-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="495b9-160">Atlasiet **Jā**, lai apstiprinātu darbību.</span><span class="sxs-lookup"><span data-stu-id="495b9-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="495b9-161">Tagad varat saistīt jaunu vidi.</span><span class="sxs-lookup"><span data-stu-id="495b9-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="495b9-162">Nevar skatīt pārdošanas pasūtījuma rindas informācijas veidlapu</span><span class="sxs-lookup"><span data-stu-id="495b9-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="495b9-163">Veidojot pārdošanas pasūtījumu Dynamics 365 Sales, noklikšķinot uz **+ pievienot preces**, varat tikt novirzīts uz Dynamics 365 Project Operations pasūtījuma rindas veidlapu.</span><span class="sxs-lookup"><span data-stu-id="495b9-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="495b9-164">No šīs veidlapas nav iespējams skatīt pārdošanas pasūtījuma rindas **Informācijas** veidlapu.</span><span class="sxs-lookup"><span data-stu-id="495b9-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="495b9-165">**Informācijas** opcija neparādās nolaižamajā sarakstā zem **Jaunas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="495b9-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="495b9-166">Tas notiek tāpēc, ka projekta operācijas ir uzstādītas jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="495b9-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="495b9-167">Lai atkārtoti iespējotu **Informācijas** veidlapas opciju, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="495b9-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="495b9-168">Pārejiet uz **Pasūtījuma rindas** tabulu.</span><span class="sxs-lookup"><span data-stu-id="495b9-168">Navigate to the **Order Line** table.</span></span>
2. <span data-ttu-id="495b9-169">Atrodiet **Informācijas** veidlapu zem veidlapas zara.</span><span class="sxs-lookup"><span data-stu-id="495b9-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="495b9-170">Atlasiet **Informācijas** veidlapu un noklikšķiniet uz **Iespējot drošības lomas**.</span><span class="sxs-lookup"><span data-stu-id="495b9-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="495b9-171">Mainiet drošības iestatījumu uz **Parādīt visiem**.</span><span class="sxs-lookup"><span data-stu-id="495b9-171">Change the security setting to **Display to everyone**.</span></span>
