---
title: "Finanšu pārskata data mart atiestatīšana pēc datu bāzes atjaunošanas"
description: "Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu data mart pēc Microsoft Dynamics 365 for Finance and Operations datu bāzes atjaunošanas."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="0713f-103">Finanšu pārskata data mart atiestatīšana pēc datu bāzes atjaunošanas</span><span class="sxs-lookup"><span data-stu-id="0713f-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0713f-104">Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu data mart pēc Microsoft Dynamics 365 for Finance and Operations datu bāzes atjaunošanas.</span><span class="sxs-lookup"><span data-stu-id="0713f-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="0713f-105">Ja atjaunojat Finance and Operations datu bāzi no dublējuma vai kopējat datu bāzi no citas vides, ir jāizpilda šajā tēmā norādītās darbības, lai nodrošinātu, ka finanšu pārskata data mart ir pareizi, izmantojot atjaunoto Finance and Operations datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="0713f-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="0713f-106">Šī procesa darbības tiek atbalstītas Dynamics 365 for Operations 2016. gada maija laidienā (programmas būvējums 7.0.1265.23014 un finanšu pārskatu būvējums 7.0.10000.4) un jaunākos laidienos.</span><span class="sxs-lookup"><span data-stu-id="0713f-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="0713f-107">Ja lietojat vecāku Dynamics 365 for Finance and Operations laidienu, sazinieties ar mūsu atbalsta dienestu, lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="0713f-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="0713f-108">Pārskatu definīciju eksportēšana</span><span class="sxs-lookup"><span data-stu-id="0713f-108">Export report definitions</span></span>
<span data-ttu-id="0713f-109">Vispirms eksportējiet pārskatu dizainus no pārskatu veidotāja, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0713f-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="0713f-110">Pārskatu veidotājā pārejiet uz sadaļu **Uzņēmums** &gt; **Veidošanas bloku grupas**.</span><span class="sxs-lookup"><span data-stu-id="0713f-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="0713f-111">Atlasiet eksportējamo veidošanas bloku grupu un noklikšķiniet uz **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="0713f-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="0713f-112">Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="0713f-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="0713f-113">Atlasiet eksportējamās pārskatu definīcijas, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0713f-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="0713f-114">Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.</span><span class="sxs-lookup"><span data-stu-id="0713f-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="0713f-115">Lai eksportētu noteiktas atskaites, rindas, kolonnas, koku struktūras vai dimensiju kopas, noklikšķiniet uz atbilstošās cilnes un pēc tam atlasiet eksportējamos vienumus.</span><span class="sxs-lookup"><span data-stu-id="0713f-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="0713f-116">Lai cilnē atlasītu vairākus vienumus, nospiediet un turiet taustiņu Ctrl. Kad eksportēšanai atlasāt pārskatus, tiek atlasītas arī saistītās rindas, kolonnas, koki un dimensiju kopas.</span><span class="sxs-lookup"><span data-stu-id="0713f-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="0713f-117">Noklikšķiniet uz **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="0713f-117">Click **Export**.</span></span>
5.  <span data-ttu-id="0713f-118">Ievadiet faila nosaukumu un atlasiet drošu atrašanās vietu, kur vēlaties saglabāt eksportētās pārskatu definīcijas.</span><span class="sxs-lookup"><span data-stu-id="0713f-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="0713f-119">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0713f-119">Click **Save**.</span></span>

<span data-ttu-id="0713f-120">Failu var kopēt vai augšupielādēt drošā atrašanās vietā, lai vēlāk to varētu importēt citā vidē.</span><span class="sxs-lookup"><span data-stu-id="0713f-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="0713f-121">Informācija par Microsoft Azure krātuves konta lietošanu ir pieejama tēmā [Datu pārsūtīšana, izmantojot komandrindas utilītu AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="0713f-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="0713f-122">Microsoft krātuves kontu nenodrošina Dynamics 365 for Finance and Operations līguma ietvaros.</span><span class="sxs-lookup"><span data-stu-id="0713f-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="0713f-123">Jums ir jāiegādājas krātuves konts vai jāizmanto atsevišķa Azure abonementa krātuves konts.</span><span class="sxs-lookup"><span data-stu-id="0713f-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="0713f-124">Ņemiet vērā D diska darbību Azure virtuālajās mašīnās.</span><span class="sxs-lookup"><span data-stu-id="0713f-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="0713f-125">Ilgstoši neglabājiet tajā eksportētās veidošanas bloku grupas.</span><span class="sxs-lookup"><span data-stu-id="0713f-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="0713f-126">Papildinformāciju par pagaidu diskiem skatiet tēmā [Izpratne par pagaidu disku Windows Azure virtuālajās mašīnās](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="0713f-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="0713f-127">Pakalpojumu apturēšana</span><span class="sxs-lookup"><span data-stu-id="0713f-127">Stop services</span></span>
<span data-ttu-id="0713f-128">Izmantojiet attālo darbvirsmu, lai izveidotu savienojumu ar visiem vidē ietvertajiem datoriem un apturētu tālāk norādītos Windows pakalpojumus, izmantojot failu services.msc.</span><span class="sxs-lookup"><span data-stu-id="0713f-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="0713f-129">Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)</span><span class="sxs-lookup"><span data-stu-id="0713f-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="0713f-130">Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)</span><span class="sxs-lookup"><span data-stu-id="0713f-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="0713f-131">Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)</span><span class="sxs-lookup"><span data-stu-id="0713f-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="0713f-132">Šiem pakalpojumiem ir atvērti savienojumi ar Dynamics 365 for Finance and Operations datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="0713f-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="0713f-133">Atcelt izmaiņas</span><span class="sxs-lookup"><span data-stu-id="0713f-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="0713f-134">Atrodiet un lejupielādējiet jaunāko MinorVersionDataUpgrade.zip pakotni</span><span class="sxs-lookup"><span data-stu-id="0713f-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="0713f-135">Atrodiet jaunāko MinorVersionDataUpgrade.zip pakotni, izmantojot norādījumus, kas ir sniegti tēmā [Lejupielādēt jaunāko izvietojamo datu jaunināšanas pakotni](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="0713f-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="0713f-136">Norādījumos ir paskaidrots, kā noteikt un lejupielādēt pareizo datu jaunināšanas pakotnes versiju.</span><span class="sxs-lookup"><span data-stu-id="0713f-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="0713f-137">Jauninājums nav nepieciešams, lai lejupielādētu MinorVersionDataUpgrade.zip pakotni.</span><span class="sxs-lookup"><span data-stu-id="0713f-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="0713f-138">Ir tikai jāizpilda sadaļā "Lejupielādēt jaunāko izvietojamo datu jaunināšanas pakotni" norādītās darbības, neveicot nekādas citas rakstā norādītās darbības MinorVersionDataUpgrade.zip pakotnes kopijas izgūšanai.</span><span class="sxs-lookup"><span data-stu-id="0713f-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="0713f-139">Skripta izpilde ar Dynamics 365 for Finance and Operations datu bāzi</span><span class="sxs-lookup"><span data-stu-id="0713f-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="0713f-140">Izpildiet tālāk norādītos skriptus ar Dynamics 365 for Finance and Operations datu bāzi (nevis ar finanšu pārskatu datu bāzi).</span><span class="sxs-lookup"><span data-stu-id="0713f-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="0713f-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="0713f-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="0713f-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="0713f-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="0713f-143">Šie skripti nodrošina to, ka lietotāju, lomu un izmaiņu izsekošanas iestatījumi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="0713f-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="0713f-144">PowerShell komandas izpilde, lai atiestatītu datu bāzi</span><span class="sxs-lookup"><span data-stu-id="0713f-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="0713f-145">Lai atiestatītu integrāciju starp Finance and Operations un finanšu pārskatiem, AOS datorā, platformā PowerShell kā administrators izpildiet tālāk norādītās komandas.</span><span class="sxs-lookup"><span data-stu-id="0713f-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="0713f-146">Pēc šo komandu izpildīšanas tiks prasīts ievadīt “Y”, lai apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="0713f-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="0713f-147">Tālāk ir sniegts parametru paskaidrojums.</span><span class="sxs-lookup"><span data-stu-id="0713f-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="0713f-148">Parametra -Reason derīgās vērtības ir: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="0713f-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="0713f-149">Parametra -ReasonDetail vērtība ir brīvs teksts.</span><span class="sxs-lookup"><span data-stu-id="0713f-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="0713f-150">Parametru Reason un ReasonDetail vērtības tiek reģistrētas telemetrijas/vides pārraudzības žurnālā.</span><span class="sxs-lookup"><span data-stu-id="0713f-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="0713f-151">Pakalpojumu startēšana</span><span class="sxs-lookup"><span data-stu-id="0713f-151">Start services</span></span>
<span data-ttu-id="0713f-152">Izmantojiet failu services.msc, lai atkal startētu pakalpojumus, ko iepriekš apturējāt.</span><span class="sxs-lookup"><span data-stu-id="0713f-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="0713f-153">Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)</span><span class="sxs-lookup"><span data-stu-id="0713f-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="0713f-154">Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)</span><span class="sxs-lookup"><span data-stu-id="0713f-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="0713f-155">Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)</span><span class="sxs-lookup"><span data-stu-id="0713f-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="0713f-156">Pārskatu definīciju importēšana</span><span class="sxs-lookup"><span data-stu-id="0713f-156">Import report definitions</span></span>
<span data-ttu-id="0713f-157">Importējiet pārskatu dizainus no pārskatu veidotāja, izmantojot eksportēšanas laikā izveidoto failu.</span><span class="sxs-lookup"><span data-stu-id="0713f-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="0713f-158">Pārskatu veidotājā pārejiet uz sadaļu **Uzņēmums** &gt; **Veidošanas bloku grupas**.</span><span class="sxs-lookup"><span data-stu-id="0713f-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="0713f-159">Atlasiet eksportējamo veidošanas bloku grupu un noklikšķiniet uz **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="0713f-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0713f-160">Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="0713f-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="0713f-161">Atlasiet veidošanas bloku **Noklusējuma** un noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="0713f-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="0713f-162">Atlasiet failu, kurā ir ietvertas eksportētās pārskatu definīcijas, un noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="0713f-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="0713f-163">Dialoglodziņā Importēt atlasiet importējamās pārskatu definīcijas.</span><span class="sxs-lookup"><span data-stu-id="0713f-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="0713f-164">Lai importētu visas atskaites definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.</span><span class="sxs-lookup"><span data-stu-id="0713f-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="0713f-165">Lai importētu atsevišķus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet importējamos pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas.</span><span class="sxs-lookup"><span data-stu-id="0713f-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="0713f-166">Noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="0713f-166">Click **Import**.</span></span>





