---
title: Bankas izraksta faila importēšanas problēmu novēršana
description: Ir svarīgi, lai no bankas saņemtais bankas izraksta fails atbilstu programmā Microsoft Dynamics 365 Finance atbalstītajam izkārtojumam. Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi. Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti. Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā. Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 612ded1f68cc8e1b26b8046501bae1707175e23a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188330"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="82a89-107">Bankas izraksta faila importēšanas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="82a89-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82a89-108">Ir svarīgi, lai no bankas saņemtais bankas izraksta fails atbilstu programmā Microsoft Dynamics 365 Finance atbalstītajam izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="82a89-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="82a89-109">Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi.</span><span class="sxs-lookup"><span data-stu-id="82a89-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="82a89-110">Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti.</span><span class="sxs-lookup"><span data-stu-id="82a89-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="82a89-111">Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā.</span><span class="sxs-lookup"><span data-stu-id="82a89-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="82a89-112">Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.</span><span class="sxs-lookup"><span data-stu-id="82a89-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="82a89-113">Kāda kļūda radusies?</span><span class="sxs-lookup"><span data-stu-id="82a89-113">What is the error?</span></span>
------------------

<span data-ttu-id="82a89-114">Pēc bankas pārskata faila importēšanas mēģinājuma atveriet sadaļu Datu pārvaldības uzdevumu vēsture un tās detalizēto izpildes informāciju, lai atrastu kļūdu.</span><span class="sxs-lookup"><span data-stu-id="82a89-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="82a89-115">Kļūda var palīdzēt, norādot uz izrakstu, bilanci vai izraksta rindu.</span><span class="sxs-lookup"><span data-stu-id="82a89-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="82a89-116">Tomēr ir maz ticams, ka tā nodrošinās pietiekami daudz informācijas, lai palīdzētu noteikt lauku vai elementu, kas radīja problēmu.</span><span class="sxs-lookup"><span data-stu-id="82a89-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="82a89-117">Kādas ir galvenās atšķirības?</span><span class="sxs-lookup"><span data-stu-id="82a89-117">What are the differences?</span></span>
<span data-ttu-id="82a89-118">Bankas faila izkārtojuma definīciju salīdziniet ar Finance importa definīciju un pievērsiet uzmanību atšķirībām laukos un elementos.</span><span class="sxs-lookup"><span data-stu-id="82a89-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="82a89-119">Bankas izraksta failu salīdziniet ar saistīto Finance faila paraugu.</span><span class="sxs-lookup"><span data-stu-id="82a89-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="82a89-120">ISO20022 failos var viegli pamanīt jebkādas atšķirības.</span><span class="sxs-lookup"><span data-stu-id="82a89-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="82a89-121">Laika joslu atšķirības importētajos bankas izrakstos</span><span class="sxs-lookup"><span data-stu-id="82a89-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="82a89-122">Datuma-laika vērtības importa failā var atšķirties no datuma/laika vērtībām, kas tiek rādītas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="82a89-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="82a89-123">Lai novērstu šo neatbilstību, ievadiet laika joslas preferences lapā **Datu avotu konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="82a89-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="82a89-124">Papildinformāciju par to, kā ievadīt laika zonas preferenci, skatiet tēmā [Papildu bankas darbību saskaņošanas importēšanas procesa iestatīšana](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="82a89-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="82a89-125">Transformācijas</span><span class="sxs-lookup"><span data-stu-id="82a89-125">Transformations</span></span>
<span data-ttu-id="82a89-126">Parasti izmaiņas ir jāveic, izmantojot vienu no trīs transformācijām.</span><span class="sxs-lookup"><span data-stu-id="82a89-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="82a89-127">Katra transformācija ir rakstīta konkrētam standartam.</span><span class="sxs-lookup"><span data-stu-id="82a89-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="82a89-128">Resursa nosaukums</span><span class="sxs-lookup"><span data-stu-id="82a89-128">Resource name</span></span>                                         | <span data-ttu-id="82a89-129">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="82a89-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="82a89-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="82a89-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="82a89-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="82a89-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="82a89-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="82a89-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="82a89-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="82a89-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="82a89-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="82a89-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="82a89-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="82a89-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="82a89-136">Atkļūdošanas transformācijas</span><span class="sxs-lookup"><span data-stu-id="82a89-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="82a89-137">BAI2 un MT940 failu korekcija</span><span class="sxs-lookup"><span data-stu-id="82a89-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="82a89-138">BAI2 un MT940 faili ir teksta faili, un tiem nepieciešama korekcija, lai iespējotu paplašināmo stila lapas valodas transformāciju (XSLT) atkļūdošanu.</span><span class="sxs-lookup"><span data-stu-id="82a89-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="82a89-139">Programma veic šo korekciju, importējot failu.</span><span class="sxs-lookup"><span data-stu-id="82a89-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="82a89-140">Izveidojiet XML failu un iekopējiet tajā šo tekstu.</span><span class="sxs-lookup"><span data-stu-id="82a89-140">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="82a89-141">Kopējiet bankas izraksta faila saturu un ielīmējiet to XML failā tā, lai tas aizstātu **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="82a89-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="82a89-142">XSLT atkļūdošana</span><span class="sxs-lookup"><span data-stu-id="82a89-142">Debug the XSLT</span></span>

<span data-ttu-id="82a89-143">Lai iegūtu papildus informāciju, skatiet <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="82a89-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="82a89-144">Palaidiet Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="82a89-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="82a89-145">Izveidojiet konsoles pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="82a89-145">Create a console application.</span></span>
3.  <span data-ttu-id="82a89-146">Atveriet atbilstošo XSLT.</span><span class="sxs-lookup"><span data-stu-id="82a89-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="82a89-147">Noklikšķiniet uz XLST un tās rekvizītu lapas.</span><span class="sxs-lookup"><span data-stu-id="82a89-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="82a89-148">Iestatiet ievadi bankas izraksta faila atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="82a89-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="82a89-149">Norādiet izvades atrašanās vietu un faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="82a89-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="82a89-150">Iestatiet nepieciešamos pārtraukumpunktus.</span><span class="sxs-lookup"><span data-stu-id="82a89-150">Set the required break points.</span></span>
8.  <span data-ttu-id="82a89-151">Izvēlnē noklikšķiniet uz **XML** &gt; **Sākt XSLT atkļūdošanu**.</span><span class="sxs-lookup"><span data-stu-id="82a89-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="82a89-152">XSLT izvades formatēšana</span><span class="sxs-lookup"><span data-stu-id="82a89-152">Format the XSLT output</span></span>

<span data-ttu-id="82a89-153">Transformācijas izpildes laikā tiek izveidots izvades fails, ko varat skatīt programmā Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="82a89-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="82a89-154">Izmantojiet Ctrl+A, Ctrl+K un Ctrl+D, lai ātri formatētu izvades failu.</span><span class="sxs-lookup"><span data-stu-id="82a89-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="82a89-155">Transformācijas korekcija</span><span class="sxs-lookup"><span data-stu-id="82a89-155">Adjust the transformation</span></span>

<span data-ttu-id="82a89-156">Koriģējiet transformāciju, lai iegūtu atbilstošo lauku vai elementu bankas pārskata failā.</span><span class="sxs-lookup"><span data-stu-id="82a89-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="82a89-157">Pēc tam attiecīgo lauku vai elementu kartējiet uz atbilstošo Finance elementu.</span><span class="sxs-lookup"><span data-stu-id="82a89-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="82a89-158">Debeta/kredīta indikators</span><span class="sxs-lookup"><span data-stu-id="82a89-158">Debit/credit indicator</span></span>

<span data-ttu-id="82a89-159">Dažreiz debets var tikt importēts kā kredīts un kredīts var tikt importēts kā debets.</span><span class="sxs-lookup"><span data-stu-id="82a89-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="82a89-160">Lai atrisinātu šo problēmu, ir jāmaina atbilstošā XSLT.</span><span class="sxs-lookup"><span data-stu-id="82a89-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="82a89-161">Ja bankas izraksti ir no vairākām bankām, pārliecinieties, ka tajos visos ir izmantota tā pati debeta/kredīta pieeja, vai izveidojiet atsevišķas transformācijas.</span><span class="sxs-lookup"><span data-stu-id="82a89-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="82a89-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator veidne</span><span class="sxs-lookup"><span data-stu-id="82a89-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="82a89-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit veidne</span><span class="sxs-lookup"><span data-stu-id="82a89-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="82a89-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator veidne</span><span class="sxs-lookup"><span data-stu-id="82a89-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="82a89-165">Bankas izrakstu formātu un tehnisko izkārtojumu paraugi</span><span class="sxs-lookup"><span data-stu-id="82a89-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="82a89-166">Šajā tabulā ir minēti detalizētās bankas darbību saskaņošanas importa failu tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili.</span><span class="sxs-lookup"><span data-stu-id="82a89-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="82a89-167">Piemēra failus un tehniskos izkārtojumus var lejupielādēt šeit: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="82a89-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="82a89-168">Tehniskā izkārtojuma definīcija</span><span class="sxs-lookup"><span data-stu-id="82a89-168">Technical layout definition</span></span>                             | <span data-ttu-id="82a89-169">Bankas izraksta parauga fails</span><span class="sxs-lookup"><span data-stu-id="82a89-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="82a89-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="82a89-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="82a89-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="82a89-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="82a89-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="82a89-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="82a89-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="82a89-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="82a89-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="82a89-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="82a89-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="82a89-175">BAI2StatementExample</span></span>                 |





