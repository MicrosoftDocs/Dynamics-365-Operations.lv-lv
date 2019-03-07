---
title: Pozitīvo maksājumu failu iestatīšana un izveidošana
description: Šajā rakstā ir izskaidrots, kā iestatīt pozitīvo maksājumu un izveidot pozitīvo maksājumu failus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0a15669c477223b922d8892d675eaa1df2563714
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "346092"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="40b77-103">Pozitīvo maksājumu failu iestatīšana un izveidošana</span><span class="sxs-lookup"><span data-stu-id="40b77-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40b77-104">Šajā rakstā ir izskaidrots, kā iestatīt pozitīvo maksājumu un izveidot pozitīvo maksājumu failus.</span><span class="sxs-lookup"><span data-stu-id="40b77-104">This article explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="40b77-105">Iestatiet pozitīvo maksājumu, lai izveidotu elektronisku čeku sarakstu, kas tiek iesniegts bankai.</span><span class="sxs-lookup"><span data-stu-id="40b77-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="40b77-106">Kad čeks ir iesniegts bankai, banka to salīdzina ar čeku sarakstu.</span><span class="sxs-lookup"><span data-stu-id="40b77-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="40b77-107">Ja čeks atbilst čekam sarakstā, banka to dzēš.</span><span class="sxs-lookup"><span data-stu-id="40b77-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="40b77-108">Ja čeks neatbilst čekam sarakstā, banka to aiztur uz pārskatīšanu.</span><span class="sxs-lookup"><span data-stu-id="40b77-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="40b77-109">Pozitīvā maksājuma failu drošība</span><span class="sxs-lookup"><span data-stu-id="40b77-109">Security for positive pay files</span></span>
<span data-ttu-id="40b77-110">Pozitīvo maksājumu faili var saturēt konfidenciālu informāciju par maksājumu saņēmējiem un čeku summām.</span><span class="sxs-lookup"><span data-stu-id="40b77-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="40b77-111">Šī iemesla dēļ nodrošiniet, lai no failu ģenerēšanas, līdz to saņemšanai bankā, tiek veikti atbilstoši drošības pasākumi.</span><span class="sxs-lookup"><span data-stu-id="40b77-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="40b77-112">Pozitīvo maksājumu faili tiek lejupielādēti atrašanās vietā, kas ir norādīta tīmekļa pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="40b77-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="40b77-113">Tā kā pozitīvo maksājumu failos var būt ietverta sensitīva informācija, ir svarīgi nodrošināt, ka tikai autorizēti lietotāji var izveidot un skatīt šo informāciju programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="40b77-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="40b77-114">Izmantojiet nākamo tabulu, kas palīdzēs noskaidrot nepieciešamās privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="40b77-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40b77-115">Uzdevums</span><span class="sxs-lookup"><span data-stu-id="40b77-115">Task</span></span></th>
<th><span data-ttu-id="40b77-116">Privilēģija</span><span class="sxs-lookup"><span data-stu-id="40b77-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40b77-117">Izveidot pozitīvo maksājumu failus, izmantojot sarakstu lapu <strong>Bankas konti</strong> vai lapu <strong>Bankas konti</strong>.</span><span class="sxs-lookup"><span data-stu-id="40b77-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="40b77-118"><strong>Uzturēt bankas pozitīvo maksājumu datus</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="40b77-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="40b77-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="40b77-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40b77-120">Izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un bankas kontiem, izmantojot lapu <strong>Izveidot pozitīvā maksājuma failu</strong>.</span><span class="sxs-lookup"><span data-stu-id="40b77-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="40b77-121"><strong>Uzturēt bankas pozitīvo maksājumu datus</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="40b77-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="40b77-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="40b77-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40b77-123">Skatīt pozitīvo maksājumu failus lapā <strong>Pozitīvā maksājuma kopsavilkuma fails</strong>.</span><span class="sxs-lookup"><span data-stu-id="40b77-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="40b77-124"><strong>Skatīt vairākām juridiskām personām izveidotos bankas pozitīvo maksājumu datus</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="40b77-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40b77-125">Apstiprināt bankas pozitīvā maksājuma failu lapā <strong>Pozitīvā maksājuma kopsavilkuma fails</strong>.</span><span class="sxs-lookup"><span data-stu-id="40b77-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="40b77-126"><strong>Apstiprināt pozitīvā maksājuma failu</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="40b77-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40b77-127">Atsaukt bankas pozitīvā maksājuma failu lapā <strong>Pozitīvā maksājuma faila kopsavilkums</strong>.</span><span class="sxs-lookup"><span data-stu-id="40b77-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="40b77-128"><strong>Atsaukt pozitīvā maksājuma failu</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="40b77-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="40b77-129">Iestatīt pozitīvā maksājuma formātu</span><span class="sxs-lookup"><span data-stu-id="40b77-129">Set up a positive pay format</span></span>
<span data-ttu-id="40b77-130">Pozitīvā maksājuma faili tiek izveidoti, izmantojot datu elementus.</span><span class="sxs-lookup"><span data-stu-id="40b77-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="40b77-131">Lai varētu ģenerēt pozitīvā maksājuma failu, vispirms ir jāiestata transformācijas ievades formāts, kas tiks izmantots, lai pārvērstu čeka datus formātā, kas ir saprotams bankai.</span><span class="sxs-lookup"><span data-stu-id="40b77-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="40b77-132">Lapā **Pozitīvā maksājuma formāts** var izveidot faila formāta identifikatoru un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="40b77-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="40b77-133">Jāizmanto XML veida transformācijas ievades formāts</span><span class="sxs-lookup"><span data-stu-id="40b77-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="40b77-134">Konkrēts formāts ir atkarīgs no izmantotā transformācijas faila.</span><span class="sxs-lookup"><span data-stu-id="40b77-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="40b77-135">Piemēram, pieejamais parauga paplašināmās stila lapas valodas transformācijas (XSLT) fails izmanto formātu **XML elements**.</span><span class="sxs-lookup"><span data-stu-id="40b77-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="40b77-136">Izmantojiet darbību **Augšupielādēt transformācijai izmantojamo failu**, lai norādītu bankai nepieciešamā formāta transformācijas faila atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="40b77-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="40b77-137">Piemērs: pozitīvā maksājuma faila XSLT fails.</span><span class="sxs-lookup"><span data-stu-id="40b77-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BankPositivePayExportEntity">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="40b77-138">Piešķirt pozitīvā maksājuma formātu bankas kontam</span><span class="sxs-lookup"><span data-stu-id="40b77-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="40b77-139">Katram bankas kontam, kuram vēlaties izveidot pozitīvā maksājuma datus, ir jāpiešķir iepriekšējā sadaļā norādīto pozitīvā maksājuma formāts.</span><span class="sxs-lookup"><span data-stu-id="40b77-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="40b77-140">Lapā **Bankas konti** atlasiet pozitīvā maksājuma formātu, kas atbilst bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="40b77-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="40b77-141">Laukā **Pozitīvā maksājuma sākuma datums** ievadiet pozitīvo maksājumu failu izveides sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="40b77-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="40b77-142">Šajā laukā obligāti jāievada datums.</span><span class="sxs-lookup"><span data-stu-id="40b77-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="40b77-143">Pretējā gadījumā pirmais izveidotais pozitīvā maksājuma fails ietvers visus čekus, kas jebkad ir izveidoti šim bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="40b77-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="40b77-144">Piešķirt pozitīvo maksājumu failu numerāciju</span><span class="sxs-lookup"><span data-stu-id="40b77-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="40b77-145">Katram pozitīvo maksājumu failam ir nepieciešams unikāls numurs.</span><span class="sxs-lookup"><span data-stu-id="40b77-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="40b77-146">Izmantojiet cilni **Numerācija** lapā **Skaidras naudas un bankas pārvaldības parametri**, lai izveidotu pozitīvo maksājumu failu numerāciju.</span><span class="sxs-lookup"><span data-stu-id="40b77-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="40b77-147">Izveidot pozitīvā maksājuma failu vienam bankas kontam</span><span class="sxs-lookup"><span data-stu-id="40b77-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="40b77-148">Pozitīvā maksājuma failu var izveidot vienai juridiskajai personai un vienam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="40b77-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="40b77-149">Lai iegūtu informāciju par to, kā vienlaicīgi izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un banku kontiem, skatiet nākamo sadaļu.</span><span class="sxs-lookup"><span data-stu-id="40b77-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="40b77-150">Lai izveidotu pozitīvā maksājuma failu vienai juridiskajai personai un vienam bankas kontam, atveriet dialoglodziņu **Izveidot pozitīvā maksājuma failu** lapā **Bankas konti**.</span><span class="sxs-lookup"><span data-stu-id="40b77-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="40b77-151">Laukā **Pēdējais datums** ievadiet pēdējā čeka datumu, kas jāiekļauj pozitīvā maksājuma failā.</span><span class="sxs-lookup"><span data-stu-id="40b77-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="40b77-152">Failā tiek iekļauti visi čeki, kas nav iekļauti pozitīvā maksājuma failā līdz šī čeka datumam.</span><span class="sxs-lookup"><span data-stu-id="40b77-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="40b77-153">Izveidot pozitīvā maksājuma failu vairākiem bankas kontam</span><span class="sxs-lookup"><span data-stu-id="40b77-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="40b77-154">Lai izveidotu pozitīvā maksājuma failu vairākiem bankas kontiem, izmantojiet periodisko uzdevumu **Izveidot pozitīvā maksājuma failu**.</span><span class="sxs-lookup"><span data-stu-id="40b77-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="40b77-155">Atlasiet pozitīvā maksājuma faila formātu un norādiet, vai izveidot failu visām juridiskajām personām vai tikai atlasītajai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="40b77-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="40b77-156">Var izveidot arī pozitīvā maksājuma failu visiem bankas kontiem, kas izmanto norādīto pozitīvā maksājuma formātu, vai tikai atlasītajam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="40b77-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="40b77-157">Laukā **Pēdējais datums** ievadiet pēdējā čeka datumu, kas jāiekļauj pozitīvā maksājuma failā.</span><span class="sxs-lookup"><span data-stu-id="40b77-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="40b77-158">Failā tiek iekļauti visi čeki, kas nav iekļauti pozitīvā maksājuma failā līdz šī čeka datumam.</span><span class="sxs-lookup"><span data-stu-id="40b77-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="40b77-159">Skatīt pozitīvā maksājuma faila izveides rezultātus</span><span class="sxs-lookup"><span data-stu-id="40b77-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="40b77-160">Kad pozitīvā maksājuma fails ir izveidots, lapā **Pozitīvā maksājuma faila kopsavilkums** var skatīt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="40b77-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="40b77-161">Lai skatītu detalizētu informāciju par atsevišķiem čekiem, izmantojiet detalizētās informācijas lapu **Pozitīvā maksājuma fails**.</span><span class="sxs-lookup"><span data-stu-id="40b77-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="40b77-162">Pozitīvā maksājuma faila apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="40b77-162">Confirm a positive pay file</span></span>
<span data-ttu-id="40b77-163">Kad čeki ir ievietoti sarakstā un pozitīvā maksājuma fails ir apmaksāts, banka jums nosūta apstiprinājuma numuru.</span><span class="sxs-lookup"><span data-stu-id="40b77-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="40b77-164">Pēc tam pozitīvā maksājuma failu var apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="40b77-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="40b77-165">Lapā **Pozitīvā maksājuma faila kopsavilkums** atlasiet pozitīvā maksājuma failu ar statusu **Izveidots** un pēc tam atlasiet darbību **Ievadīt apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="40b77-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="40b77-166">Apstiprinot pozitīvā maksājuma failu, tiek reģistrēts no bankas saņemtais apstiprinājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="40b77-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="40b77-167">Pozitīva maksājuma faila atsaukšana</span><span class="sxs-lookup"><span data-stu-id="40b77-167">Recall a positive pay file</span></span>
<span data-ttu-id="40b77-168">Ja pozitīvā maksājuma fails ir jāmaina, to var atsaukt.</span><span class="sxs-lookup"><span data-stu-id="40b77-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="40b77-169">Lapā **Pozitīvā maksājuma faila kopsavilkums** atlasiet pozitīvā maksājuma failu ar statusu **Izveidots** un pēc tam atlasiet darbību **Atsaukt**.</span><span class="sxs-lookup"><span data-stu-id="40b77-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="40b77-170">Katrā pozitīvā maksājuma failā tiek atiestatīts lauks, kas norāda, vai šis čeks ir iekļauts pozitīvā maksājuma failā.</span><span class="sxs-lookup"><span data-stu-id="40b77-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="40b77-171">Pēc tam var izveidot jaunu pozitīvā maksājuma failu, kurā ir iekļauts atsauktais čeks.</span><span class="sxs-lookup"><span data-stu-id="40b77-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



