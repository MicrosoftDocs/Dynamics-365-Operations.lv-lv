---
title: "Bankas izraksta faila importēšanas problēmu novēršana"
description: "Ir svarīgi, lai no bankas saņemtais bankas izraksta fails atbilst programmā Microsoft Dynamics 365 for Finance and Operations atbalstītajam izkārtojumam. Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi. Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti. Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā. Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas."
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a4006bf35673e3bb61bcf11619ecc68d295f29eb
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="b3247-107">Bankas izraksta faila importēšanas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="b3247-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3247-108">Ir svarīgi, lai no bankas saņemtais bankas izraksta fails atbilst programmā Microsoft Dynamics 365 for Finance and Operations atbalstītajam izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="b3247-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="b3247-109">Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi.</span><span class="sxs-lookup"><span data-stu-id="b3247-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="b3247-110">Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti.</span><span class="sxs-lookup"><span data-stu-id="b3247-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="b3247-111">Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā.</span><span class="sxs-lookup"><span data-stu-id="b3247-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="b3247-112">Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.</span><span class="sxs-lookup"><span data-stu-id="b3247-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="b3247-113">Kāda kļūda radusies?</span><span class="sxs-lookup"><span data-stu-id="b3247-113">What is the error?</span></span>
------------------

<span data-ttu-id="b3247-114">Pēc bankas pārskata faila importēšanas mēģinājuma atveriet sadaļu Datu pārvaldības uzdevumu vēsture un tās detalizēto izpildes informāciju, lai atrastu kļūdu.</span><span class="sxs-lookup"><span data-stu-id="b3247-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="b3247-115">Kļūda var palīdzēt, norādot uz izrakstu, bilanci vai izraksta rindu.</span><span class="sxs-lookup"><span data-stu-id="b3247-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="b3247-116">Tomēr ir maz ticams, ka tā nodrošinās pietiekami daudz informācijas, lai palīdzētu noteikt lauku vai elementu, kas radīja problēmu.</span><span class="sxs-lookup"><span data-stu-id="b3247-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="b3247-117">Kādas ir galvenās atšķirības?</span><span class="sxs-lookup"><span data-stu-id="b3247-117">What are the differences?</span></span>
<span data-ttu-id="b3247-118">Bankas faila izkārtojuma definīciju salīdziniet ar Finance and Operations importa definīciju un pievērsiet uzmanību atšķirībām laukos un elementos.</span><span class="sxs-lookup"><span data-stu-id="b3247-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="b3247-119">Bankas izraksta failu salīdziniet ar saistīto Finance and Operations faila paraugu.</span><span class="sxs-lookup"><span data-stu-id="b3247-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="b3247-120">ISO20022 failos var viegli pamanīt jebkādas atšķirības.</span><span class="sxs-lookup"><span data-stu-id="b3247-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="b3247-121">Transformācijas</span><span class="sxs-lookup"><span data-stu-id="b3247-121">Transformations</span></span>
<span data-ttu-id="b3247-122">Parasti izmaiņas ir jāveic, izmantojot vienu no trīs transformācijām.</span><span class="sxs-lookup"><span data-stu-id="b3247-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="b3247-123">Katra transformācija ir rakstīta konkrētam standartam.</span><span class="sxs-lookup"><span data-stu-id="b3247-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="b3247-124">Resursa nosaukums</span><span class="sxs-lookup"><span data-stu-id="b3247-124">Resource name</span></span>                                         | <span data-ttu-id="b3247-125">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="b3247-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="b3247-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="b3247-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="b3247-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="b3247-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="b3247-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="b3247-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="b3247-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="b3247-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="b3247-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="b3247-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="b3247-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="b3247-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="b3247-132">Atkļūdošanas transformācijas</span><span class="sxs-lookup"><span data-stu-id="b3247-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="b3247-133">BAI2 un MT940 failu korekcija</span><span class="sxs-lookup"><span data-stu-id="b3247-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="b3247-134">BAI2 un MT940 faili ir teksta faili, un tiem nepieciešama korekcija, lai iespējotu paplašināmo stila lapas valodas transformāciju (XSLT) atkļūdošanu.</span><span class="sxs-lookup"><span data-stu-id="b3247-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="b3247-135">Programma veic šo korekciju, importējot failu.</span><span class="sxs-lookup"><span data-stu-id="b3247-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="b3247-136">Izveidojiet XML failu un iekopējiet tajā šo tekstu.</span><span class="sxs-lookup"><span data-stu-id="b3247-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="b3247-137">Kopējiet bankas izraksta faila saturu un ielīmējiet to XML failā tā, lai tas aizstātu **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="b3247-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="b3247-138">XSLT atkļūdošana</span><span class="sxs-lookup"><span data-stu-id="b3247-138">Debug the XSLT</span></span>

<span data-ttu-id="b3247-139">Lai iegūtu papildus informāciju, skatiet <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="b3247-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="b3247-140">Startējiet Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b3247-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="b3247-141">Izveidojiet konsoles pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="b3247-141">Create a console application.</span></span>
3.  <span data-ttu-id="b3247-142">Atveriet atbilstošo XSLT.</span><span class="sxs-lookup"><span data-stu-id="b3247-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="b3247-143">Noklikšķiniet uz XLST un tās rekvizītu lapas.</span><span class="sxs-lookup"><span data-stu-id="b3247-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="b3247-144">Iestatiet ievadi bankas izraksta faila atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="b3247-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="b3247-145">Norādiet izvades atrašanās vietu un faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b3247-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="b3247-146">Iestatiet nepieciešamos pārtraukumpunktus.</span><span class="sxs-lookup"><span data-stu-id="b3247-146">Set the required break points.</span></span>
8.  <span data-ttu-id="b3247-147">Izvēlnē noklikšķiniet uz **XML** &gt; **Sākt XSLT atkļūdošanu**.</span><span class="sxs-lookup"><span data-stu-id="b3247-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="b3247-148">XSLT izvades formatēšana</span><span class="sxs-lookup"><span data-stu-id="b3247-148">Format the XSLT output</span></span>

<span data-ttu-id="b3247-149">Transformācijas darbības laikā tiek izveidots izvades fails, kuru var skatīt programmā Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b3247-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="b3247-150">Izmantojiet Ctrl+A, Ctrl+K un Ctrl+D, lai ātri formatētu izvades failu.</span><span class="sxs-lookup"><span data-stu-id="b3247-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="b3247-151">Transformācijas korekcija</span><span class="sxs-lookup"><span data-stu-id="b3247-151">Adjust the transformation</span></span>

<span data-ttu-id="b3247-152">Koriģējiet transformāciju, lai iegūtu atbilstošo lauku vai elementu bankas pārskata failā.</span><span class="sxs-lookup"><span data-stu-id="b3247-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="b3247-153">Pēc tam attiecīgo lauku vai elementu kartējiet uz atbilstošo Finance and Operations elementu.</span><span class="sxs-lookup"><span data-stu-id="b3247-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="b3247-154">Debeta/kredīta indikators</span><span class="sxs-lookup"><span data-stu-id="b3247-154">Debit/credit indicator</span></span>

<span data-ttu-id="b3247-155">Dažreiz debets var tikt importēts kā kredīts un kredīts var tikt importēts kā debets.</span><span class="sxs-lookup"><span data-stu-id="b3247-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="b3247-156">Lai atrisinātu šo problēmu, ir jāmaina atbilstošā XSLT.</span><span class="sxs-lookup"><span data-stu-id="b3247-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="b3247-157">Ja bankas izraksti ir no vairākām bankām, pārliecinieties, ka tajos visos ir izmantota tā pati debeta/kredīta pieeja, vai izveidojiet atsevišķas transformācijas.</span><span class="sxs-lookup"><span data-stu-id="b3247-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="b3247-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator veidne</span><span class="sxs-lookup"><span data-stu-id="b3247-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="b3247-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit veidne</span><span class="sxs-lookup"><span data-stu-id="b3247-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="b3247-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator veidne</span><span class="sxs-lookup"><span data-stu-id="b3247-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="b3247-161">Bankas izrakstu formātu un tehnisko izkārtojumu paraugi</span><span class="sxs-lookup"><span data-stu-id="b3247-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="b3247-162">Šajā tabulā ir minēti detalizētās bankas darbību saskaņošanas importa failu tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili.</span><span class="sxs-lookup"><span data-stu-id="b3247-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="b3247-163">Piemēra failus un tehniskos izkārtojumus var lejupielādēt šeit: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="b3247-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="b3247-164">Tehniskā izkārtojuma definīcija</span><span class="sxs-lookup"><span data-stu-id="b3247-164">Technical layout definition</span></span>                             | <span data-ttu-id="b3247-165">Bankas izraksta parauga fails</span><span class="sxs-lookup"><span data-stu-id="b3247-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="b3247-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="b3247-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="b3247-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="b3247-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="b3247-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="b3247-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="b3247-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="b3247-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="b3247-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="b3247-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="b3247-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="b3247-171">BAI2StatementExample</span></span>                 |






