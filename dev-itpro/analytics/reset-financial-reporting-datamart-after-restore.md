---
title: "Finanšu pārskata data mart atiestatīšana pēc datu bāzes atjaunošanas"
description: "Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu data mart pēc Microsoft Dynamics 365 for Finance and Operations datu bāzes atjaunošanas."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: lv-lv
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="ec2ed-103">Finanšu pārskata data mart atiestatīšana pēc datu bāzes atjaunošanas</span><span class="sxs-lookup"><span data-stu-id="ec2ed-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ec2ed-104">Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu data mart pēc Microsoft Dynamics 365 for Finance and Operations datu bāzes atjaunošanas.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="ec2ed-105">Ja atjaunojat Finance and Operations datu bāzi no dublējuma vai kopējat datu bāzi no citas vides, ir jāizpilda šajā tēmā norādītās darbības, lai nodrošinātu, ka finanšu pārskata data mart ir pareizi, izmantojot atjaunoto Finance and Operations datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="ec2ed-106">Šī procesa darbības tiek atbalstītas Dynamics 365 for Operations 2016. gada maija laidienā (programmas būvējums 7.0.1265.23014 un finanšu pārskatu būvējums 7.0.10000.4) un jaunākos laidienos.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="ec2ed-107">Ja lietojat vecāku Dynamics 365 for Finance and Operations laidienu, sazinieties ar mūsu atbalsta dienestu, lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="ec2ed-108">Pārskatu definīciju eksportēšana</span><span class="sxs-lookup"><span data-stu-id="ec2ed-108">Export report definitions</span></span>
<span data-ttu-id="ec2ed-109">Vispirms eksportējiet pārskatu dizainus no pārskatu veidotāja, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="ec2ed-110">Pārskatu veidotājā pārejiet uz sadaļu **Uzņēmums** &gt; **Veidošanas bloku grupas**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="ec2ed-111">Atlasiet eksportējamo veidošanas bloku grupu un noklikšķiniet uz **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="ec2ed-112">Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="ec2ed-113">Atlasiet eksportējamās pārskatu definīcijas, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="ec2ed-114">Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="ec2ed-115">Lai eksportētu noteiktas atskaites, rindas, kolonnas, koku struktūras vai dimensiju kopas, noklikšķiniet uz atbilstošās cilnes un pēc tam atlasiet eksportējamos vienumus.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="ec2ed-116">Lai atlasītu vairākas cilnes vienības, piespiediet un turiet taustiņu Ctrl.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="ec2ed-117">Atlasot eksportējamos pārskatus, tiek atlasītas saistītās rindas, kolonnas, koku struktūras un dimensiju kopas.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="ec2ed-118">Noklikšķiniet uz **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-118">Click **Export**.</span></span>
5.  <span data-ttu-id="ec2ed-119">Ievadiet faila nosaukumu un atlasiet drošu atrašanās vietu, kur vēlaties saglabāt eksportētās pārskatu definīcijas.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="ec2ed-120">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-120">Click **Save**.</span></span>

<span data-ttu-id="ec2ed-121">Failu var kopēt vai augšupielādēt drošā atrašanās vietā, lai vēlāk to varētu importēt citā vidē.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="ec2ed-122">Informācija par Microsoft Azure krātuves konta lietošanu ir pieejama tēmā [Datu pārsūtīšana, izmantojot komandrindas utilītu AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="ec2ed-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="ec2ed-123">Microsoft krātuves kontu nenodrošina Dynamics 365 for Finance and Operations līguma ietvaros.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="ec2ed-124">Jums ir jāiegādājas krātuves konts vai jāizmanto atsevišķa Azure abonementa krātuves konts.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="ec2ed-125">Ņemiet vērā D diska darbību Azure virtuālajās mašīnās.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="ec2ed-126">Ilgstoši neglabājiet tajā eksportētās veidošanas bloku grupas.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="ec2ed-127">Papildinformāciju par pagaidu diskiem skatiet tēmā [Izpratne par pagaidu disku Windows Azure virtuālajās mašīnās](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="ec2ed-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="ec2ed-128">Pakalpojumu apturēšana</span><span class="sxs-lookup"><span data-stu-id="ec2ed-128">Stop services</span></span>
<span data-ttu-id="ec2ed-129">Izmantojiet attālo darbvirsmu, lai izveidotu savienojumu ar visiem vidē ietvertajiem datoriem un apturētu tālāk norādītos Windows pakalpojumus, izmantojot failu services.msc.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="ec2ed-130">Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="ec2ed-131">Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="ec2ed-132">Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="ec2ed-133">Šiem pakalpojumiem ir atvērti savienojumi ar Dynamics 365 for Finance and Operations datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="ec2ed-134">Atcelt izmaiņas</span><span class="sxs-lookup"><span data-stu-id="ec2ed-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="ec2ed-135">Atrodiet un lejupielādējiet jaunāko MinorVersionDataUpgrade.zip pakotni</span><span class="sxs-lookup"><span data-stu-id="ec2ed-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="ec2ed-136">Atrodiet jaunāko MinorVersionDataUpgrade.zip pakotni, izmantojot norādījumus, kas ir sniegti tēmā [Lejupielādēt jaunāko izvietojamo datu jaunināšanas pakotni](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="ec2ed-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="ec2ed-137">Norādījumos ir paskaidrots, kā noteikt un lejupielādēt pareizo datu jaunināšanas pakotnes versiju.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="ec2ed-138">Jauninājums nav nepieciešams, lai lejupielādētu MinorVersionDataUpgrade.zip pakotni.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="ec2ed-139">Ir tikai jāizpilda sadaļā "Lejupielādēt jaunāko izvietojamo datu jaunināšanas pakotni" norādītās darbības, neveicot nekādas citas rakstā norādītās darbības MinorVersionDataUpgrade.zip pakotnes kopijas izgūšanai.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="ec2ed-140">Skripta izpilde ar Dynamics 365 for Finance and Operations datu bāzi</span><span class="sxs-lookup"><span data-stu-id="ec2ed-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="ec2ed-141">Izpildiet tālāk norādītos skriptus ar Dynamics 365 for Finance and Operations datu bāzi (nevis ar finanšu pārskatu datu bāzi).</span><span class="sxs-lookup"><span data-stu-id="ec2ed-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="ec2ed-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="ec2ed-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="ec2ed-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="ec2ed-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="ec2ed-144">Šie skripti nodrošina to, ka lietotāju, lomu un izmaiņu izsekošanas iestatījumi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="ec2ed-145">PowerShell komandas izpilde, lai atiestatītu datu bāzi</span><span class="sxs-lookup"><span data-stu-id="ec2ed-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="ec2ed-146">AOS datorā tiešā veidā izpildiet tālāk norādīto komandu, lai atiestatītu Dynamics 365 for Finance and Operations un finanšu pārskatu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="ec2ed-147">Atveriet čaulu Windows PowerShell, izmantojot lomu Administrators.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="ec2ed-148">Izpildiet šo komandu: F:</span><span class="sxs-lookup"><span data-stu-id="ec2ed-148">Execute: F:</span></span>
3.  <span data-ttu-id="ec2ed-149">Izpildiet šo komandu: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="ec2ed-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="ec2ed-150">Izpildiet šo komandu: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="ec2ed-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="ec2ed-151">Izpildiet šo komandu: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;mans atiestatīšanas iemesls&gt;”</span><span class="sxs-lookup"><span data-stu-id="ec2ed-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="ec2ed-152">Tiek prasīts ievadīt “Y”, lai apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="ec2ed-153">Tālāk ir sniegts parametru paskaidrojums.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="ec2ed-154">Parametra -Reason derīgās vērtības ir: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="ec2ed-155">Parametra -ReasonDetail vērtība ir brīvs teksts.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="ec2ed-156">Parametru Reason un ReasonDetail vērtības tiek reģistrētas telemetrijas/vides pārraudzības žurnālā.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="ec2ed-157">Pakalpojumu startēšana</span><span class="sxs-lookup"><span data-stu-id="ec2ed-157">Start services</span></span>
<span data-ttu-id="ec2ed-158">Izmantojiet failu services.msc, lai atkal startētu pakalpojumus, ko iepriekš apturējāt.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="ec2ed-159">Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="ec2ed-160">Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="ec2ed-161">Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)</span><span class="sxs-lookup"><span data-stu-id="ec2ed-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="ec2ed-162">Pārskatu definīciju importēšana</span><span class="sxs-lookup"><span data-stu-id="ec2ed-162">Import report definitions</span></span>
<span data-ttu-id="ec2ed-163">Importējiet pārskatu dizainus no pārskatu veidotāja, izmantojot eksportēšanas laikā izveidoto failu.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="ec2ed-164">Pārskatu veidotājā pārejiet uz sadaļu **Uzņēmums** &gt; **Veidošanas bloku grupas**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="ec2ed-165">Atlasiet eksportējamo veidošanas bloku grupu un noklikšķiniet uz **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ec2ed-166">Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="ec2ed-167">Atlasiet veidošanas bloku **Noklusējuma** un noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="ec2ed-168">Atlasiet failu, kurā ir ietvertas eksportētās pārskatu definīcijas, un noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="ec2ed-169">Dialoglodziņā Importēt atlasiet importējamās pārskatu definīcijas.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="ec2ed-170">Lai importētu visas atskaites definīcijas un saistītos veidošanas blokus, noklikšķiniet uz **Atlasīt visu**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="ec2ed-171">Lai importētu atsevišķus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet importējamos pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="ec2ed-172">Noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-172">Click **Import**.</span></span>





