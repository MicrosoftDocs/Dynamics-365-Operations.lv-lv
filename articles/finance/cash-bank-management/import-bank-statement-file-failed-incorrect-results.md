---
title: Bankas izraksta faila importēšanas problēmu novēršana
description: Ir svarīgi, lai no bankas saņemtais bankas izrakstu fails atbilstu programmā Microsoft Dynamics 365 Finance atbalstītajam izkārtojumam. Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi. Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti. Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā. Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188564"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="9e14f-107">Bankas izraksta faila importēšanas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="9e14f-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e14f-108">Ir svarīgi, lai no bankas saņemtais bankas izrakstu fails atbilstu programmā Microsoft Dynamics 365 Finance atbalstītajam izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="9e14f-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="9e14f-109">Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi.</span><span class="sxs-lookup"><span data-stu-id="9e14f-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="9e14f-110">Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti.</span><span class="sxs-lookup"><span data-stu-id="9e14f-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="9e14f-111">Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā.</span><span class="sxs-lookup"><span data-stu-id="9e14f-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="9e14f-112">Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.</span><span class="sxs-lookup"><span data-stu-id="9e14f-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="9e14f-113">Kāda kļūda radusies?</span><span class="sxs-lookup"><span data-stu-id="9e14f-113">What is the error?</span></span>

<span data-ttu-id="9e14f-114">Pēc bankas pārskata faila importēšanas mēģinājuma atveriet sadaļu Datu pārvaldības uzdevumu vēsture un tās detalizēto izpildes informāciju, lai atrastu kļūdu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="9e14f-115">Kļūda var palīdzēt, norādot uz izrakstu, bilanci vai izraksta rindu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="9e14f-116">Tomēr ir maz ticams, ka tā nodrošinās pietiekami daudz informācijas, lai palīdzētu noteikt lauku vai elementu, kas radīja problēmu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="9e14f-117">Importētie bankas izraksti var pārklāties tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="9e14f-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="9e14f-118">Piemēram, ja pārskats beidzas 2021. gada 1. janvārī plkst. 12:00, tad nākamā pārskata sākuma datums var būt 2021. gada 1. janvāris plkst. 12:00, 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="9e14f-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="9e14f-119">Kādas ir galvenās atšķirības?</span><span class="sxs-lookup"><span data-stu-id="9e14f-119">What are the differences?</span></span>
<span data-ttu-id="9e14f-120">Bankas faila izkārtojuma definīciju salīdziniet ar Finance importa definīciju un pievērsiet uzmanību atšķirībām laukos un elementos.</span><span class="sxs-lookup"><span data-stu-id="9e14f-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="9e14f-121">Bankas izraksta failu salīdziniet ar saistīto Finance faila paraugu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="9e14f-122">ISO20022 failos var viegli pamanīt jebkādas atšķirības.</span><span class="sxs-lookup"><span data-stu-id="9e14f-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="9e14f-123">Laika joslu atšķirības importētajos bankas izrakstos</span><span class="sxs-lookup"><span data-stu-id="9e14f-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="9e14f-124">Datuma-laika vērtības importa failā var atšķirties no datuma/laika vērtībām, kas tiek rādītas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9e14f-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="9e14f-125">Lai novērstu šo neatbilstību, ievadiet laika joslas preferences lapā **Datu avotu konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="9e14f-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="9e14f-126">Papildinformāciju par to, kā ievadīt laika zonas preferenci, skatiet tēmā [Papildu bankas darbību saskaņošanas importēšanas procesa iestatīšana](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="9e14f-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="9e14f-127">Transformācijas</span><span class="sxs-lookup"><span data-stu-id="9e14f-127">Transformations</span></span>
<span data-ttu-id="9e14f-128">Parasti izmaiņas ir jāveic, izmantojot vienu no trīs transformācijām.</span><span class="sxs-lookup"><span data-stu-id="9e14f-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="9e14f-129">Katra transformācija ir rakstīta konkrētam standartam.</span><span class="sxs-lookup"><span data-stu-id="9e14f-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="9e14f-130">Resursa nosaukums</span><span class="sxs-lookup"><span data-stu-id="9e14f-130">Resource name</span></span>                                         | <span data-ttu-id="9e14f-131">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="9e14f-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="9e14f-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="9e14f-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="9e14f-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="9e14f-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="9e14f-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="9e14f-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="9e14f-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="9e14f-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="9e14f-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="9e14f-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="9e14f-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="9e14f-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="9e14f-138">Atkļūdošanas transformācijas</span><span class="sxs-lookup"><span data-stu-id="9e14f-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="9e14f-139">BAI2 un MT940 failu korekcija</span><span class="sxs-lookup"><span data-stu-id="9e14f-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="9e14f-140">BAI2 un MT940 faili ir teksta faili, un tiem nepieciešama korekcija, lai iespējotu paplašināmo stila lapas valodas transformāciju (XSLT) atkļūdošanu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="9e14f-141">Programma veic šo korekciju, importējot failu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="9e14f-142">Izveidojiet XML failu un iekopējiet tajā šo tekstu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="9e14f-143">Kopējiet bankas izraksta faila saturu un ielīmējiet to XML failā tā, lai tas aizstātu **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="9e14f-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="9e14f-144">XSLT atkļūdošana</span><span class="sxs-lookup"><span data-stu-id="9e14f-144">Debug the XSLT</span></span>

<span data-ttu-id="9e14f-145">Lai iegūtu papildus informāciju, skatiet <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="9e14f-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="9e14f-146">Palaidiet Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9e14f-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="9e14f-147">Izveidojiet konsoles pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-147">Create a console application.</span></span>
3.  <span data-ttu-id="9e14f-148">Atveriet atbilstošo XSLT.</span><span class="sxs-lookup"><span data-stu-id="9e14f-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="9e14f-149">Noklikšķiniet uz XLST un tās rekvizītu lapas.</span><span class="sxs-lookup"><span data-stu-id="9e14f-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="9e14f-150">Iestatiet ievadi bankas izraksta faila atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="9e14f-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="9e14f-151">Norādiet izvades atrašanās vietu un faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="9e14f-152">Iestatiet nepieciešamos pārtraukumpunktus.</span><span class="sxs-lookup"><span data-stu-id="9e14f-152">Set the required break points.</span></span>
8.  <span data-ttu-id="9e14f-153">Izvēlnē noklikšķiniet uz **XML** &gt; **Sākt XSLT atkļūdošanu**.</span><span class="sxs-lookup"><span data-stu-id="9e14f-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="9e14f-154">XSLT izvades formatēšana</span><span class="sxs-lookup"><span data-stu-id="9e14f-154">Format the XSLT output</span></span>

<span data-ttu-id="9e14f-155">Transformācijas izpildes laikā tiek izveidots izvades fails, ko varat skatīt programmā Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9e14f-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="9e14f-156">Izmantojiet Ctrl+A, Ctrl+K un Ctrl+D, lai ātri formatētu izvades failu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="9e14f-157">Transformācijas korekcija</span><span class="sxs-lookup"><span data-stu-id="9e14f-157">Adjust the transformation</span></span>

<span data-ttu-id="9e14f-158">Koriģējiet transformāciju, lai iegūtu atbilstošo lauku vai elementu bankas pārskata failā.</span><span class="sxs-lookup"><span data-stu-id="9e14f-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="9e14f-159">Pēc tam attiecīgo lauku vai elementu kartējiet uz atbilstošo Finance elementu.</span><span class="sxs-lookup"><span data-stu-id="9e14f-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="9e14f-160">Debeta/kredīta indikators</span><span class="sxs-lookup"><span data-stu-id="9e14f-160">Debit/credit indicator</span></span>

<span data-ttu-id="9e14f-161">Dažreiz debets var tikt importēts kā kredīts un kredīts var tikt importēts kā debets.</span><span class="sxs-lookup"><span data-stu-id="9e14f-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="9e14f-162">Lai atrisinātu šo problēmu, ir jāmaina atbilstošā XSLT.</span><span class="sxs-lookup"><span data-stu-id="9e14f-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="9e14f-163">Ja bankas izraksti ir no vairākām bankām, pārliecinieties, ka tajos visos ir izmantota tā pati debeta/kredīta pieeja, vai izveidojiet atsevišķas transformācijas.</span><span class="sxs-lookup"><span data-stu-id="9e14f-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="9e14f-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator veidne</span><span class="sxs-lookup"><span data-stu-id="9e14f-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="9e14f-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit veidne</span><span class="sxs-lookup"><span data-stu-id="9e14f-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="9e14f-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator veidne</span><span class="sxs-lookup"><span data-stu-id="9e14f-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="9e14f-167">Bankas izrakstu formātu un tehnisko izkārtojumu paraugi</span><span class="sxs-lookup"><span data-stu-id="9e14f-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="9e14f-168">Šajā tabulā ir minēti detalizētās bankas darbību saskaņošanas importa failu tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili.</span><span class="sxs-lookup"><span data-stu-id="9e14f-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="9e14f-169">Piemēra failus un tehniskos izkārtojumus var lejupielādēt šeit: [Importēt faila piemērus](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="9e14f-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="9e14f-170">Tehniskā izkārtojuma definīcija</span><span class="sxs-lookup"><span data-stu-id="9e14f-170">Technical layout definition</span></span>                             | <span data-ttu-id="9e14f-171">Bankas izraksta parauga fails</span><span class="sxs-lookup"><span data-stu-id="9e14f-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="9e14f-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="9e14f-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="9e14f-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="9e14f-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="9e14f-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="9e14f-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="9e14f-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="9e14f-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="9e14f-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="9e14f-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="9e14f-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="9e14f-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
