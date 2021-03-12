---
title: Rēķinu un pavadzīmju numurēšana Latvijai un Lietuvai
description: Šajā tēmā ir paskaidrots, kā iestatīt numuru sērijas rēķiniem un pavadzīmēm un kā dokumentiem iestatīt pašnumerācijas diapazonus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LtInvoiceAutoNumberingGroups, LtInvoiceAutonumberingTable, NumberSequenceTableListPage
audience: Application User
ms.reviewer: kfend
ms.custom: 268484
ms.search.region: Latvia, Lithuania
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6329822b655351ea58aed31a5c8c35456ddcd44b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962653"
---
# <a name="invoice-and-packing-slip-numbering-for-latvia-and-lithuania"></a><span data-ttu-id="342f8-103">Rēķinu un pavadzīmju numurēšana Latvijai un Lietuvai</span><span class="sxs-lookup"><span data-stu-id="342f8-103">Invoice and packing slip numbering for Latvia and Lithuania</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="342f8-104">Šajā tēmā ir paskaidrots, kā iestatīt numuru sērijas rēķiniem un pavadzīmēm un kā dokumentiem iestatīt pašnumerācijas diapazonus.</span><span class="sxs-lookup"><span data-stu-id="342f8-104">This topic explains how to set up number sequences for invoices and packing slips, and how to set up self-numbering ranges for documents.</span></span>

<span data-ttu-id="342f8-105">Juridiskajām personām, kuru primārā adrese atrodas Latvijā vai Lietuvā, rēķiniem un pavadzīmēm varat iestatīt nosacījuma numerāciju, kas ir atkarīga no piešķirtā lietotāja vai lietotāju grupas.</span><span class="sxs-lookup"><span data-stu-id="342f8-105">For legal entities that have a primary address in Latvia or Lithuania, you can set up conditional numbering for invoices and packing slips that is based on the assigned user or user group.</span></span>

## <a name="set-up-number-sequences-for-invoices-and-packing-slips"></a><span data-ttu-id="342f8-106">Iestatīt numuru sērijas rēķiniem un pavadzīmēm</span><span class="sxs-lookup"><span data-stu-id="342f8-106">Set up number sequences for invoices and packing slips</span></span>
<span data-ttu-id="342f8-107">Pamatdatu ierakstiem un transakciju ierakstiem varat iestatīt unikālas dokumentu numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="342f8-107">You can set up unique document number sequences for master data records and transaction records.</span></span> <span data-ttu-id="342f8-108">Ja jūsu valsts vai reģiona nodokļu iestādes jūsu organizācijai piešķir specifisku dokumentu numuru sēriju vai formātu, šo numuru sēriju varat saistīt ar kādu dokumentu tipu.</span><span class="sxs-lookup"><span data-stu-id="342f8-108">If the tax authorities for your country or region assign your organization a specific document number sequence or format, you can associate the number sequence with a document type.</span></span> <span data-ttu-id="342f8-109">Katru dokumentu numuru sēriju varat piešķirt kādam lietotājam vai lietotāju grupai.</span><span class="sxs-lookup"><span data-stu-id="342f8-109">You can assign each document number sequence to a user or user group.</span></span> <span data-ttu-id="342f8-110">Šādi tikai norādītais lietotājs vai lietotāju grupa var dokumentam piešķirt sērijā iekļautos numurus.</span><span class="sxs-lookup"><span data-stu-id="342f8-110">In this way, only the designated user or user group can assign the numbers in the series to a document.</span></span> <span data-ttu-id="342f8-111">Numuru sērijas rēķiniem un pavadzīmēm varat iestatīt lapā **Rēķinu numerācijas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="342f8-111">You can set up number sequences for invoices and packing slips on the **Invoice numbering setup** page.</span></span> <span data-ttu-id="342f8-112">(Noklikšķiniet uz **Organizācijas administrēšana** &gt; **Numuru sērijas** &gt; **Rēķinu numerācijas iestatīšana**.) Izmantojiet nākamajā tabulā sniegto informāciju, lai aizpildītu laukus lapā **Rēķinu numerācijas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="342f8-112">(Click **Organization administration** &gt; **Number sequences** &gt; **Invoice numbering setup**.) Use the information in the following table to complete the fields on the **Invoice numbering setup** page.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="342f8-113">Lauks</span><span class="sxs-lookup"><span data-stu-id="342f8-113">Field</span></span></th>
<th><span data-ttu-id="342f8-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="342f8-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="342f8-115">Numerācija</span><span class="sxs-lookup"><span data-stu-id="342f8-115">Numbering</span></span></td>
<td><span data-ttu-id="342f8-116">Ievadiet dokumentu numuru sērijas prefiksu.</span><span class="sxs-lookup"><span data-stu-id="342f8-116">Enter the prefix for the document number sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="342f8-117">Modulis</span><span class="sxs-lookup"><span data-stu-id="342f8-117">Module</span></span></td>
<td><span data-ttu-id="342f8-118">Atlasiet moduli, ko izmantos numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="342f8-118">Select the module that will use the number series.</span></span> <span data-ttu-id="342f8-119">Jūsu atlasītais modulis nosaka, kādas opcijas ir pieejamas laukā <strong>Tips</strong>.</span><span class="sxs-lookup"><span data-stu-id="342f8-119">The module that you select determines the options that are available in the <strong>Type</strong> field.</span></span> <span data-ttu-id="342f8-120">Debitoru rēķiniem un debitoru pavadzīmēm šajā laukā atlasiet <strong>Pārdošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="342f8-120">For customer invoices and customer packing slips, select <strong>Sales</strong> in this field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="342f8-121">Numuru sērijas kods</span><span class="sxs-lookup"><span data-stu-id="342f8-121">Number sequence code</span></span></td>
<td><span data-ttu-id="342f8-122">Atlasiet numuru sērijas kodu datu apgabalam, kur šī numuru sērija tiek lietota.</span><span class="sxs-lookup"><span data-stu-id="342f8-122">Select the number sequence code for the data area where the number series is applied.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="342f8-123">Tips</span><span class="sxs-lookup"><span data-stu-id="342f8-123">Type</span></span></td>
<td><span data-ttu-id="342f8-124">Atlasiet, vai numuru sērija attiecas uz rēķiniem vai uz pavadzīmēm.</span><span class="sxs-lookup"><span data-stu-id="342f8-124">Select whether the number sequence applies to invoices or packing slips.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="342f8-125">Konta kods</span><span class="sxs-lookup"><span data-stu-id="342f8-125">Account code</span></span></td>
<td><span data-ttu-id="342f8-126">Atlasiet, kā šī numuru sērija tiek lietota rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="342f8-126">Select how the number series is applied to invoices.</span></span> <span data-ttu-id="342f8-127">Pieejamas šādas opcijas</span><span class="sxs-lookup"><span data-stu-id="342f8-127">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="342f8-128"><strong>Tabula</strong> — šī numuru sērija ir pieejama tikai lietotājam, kurš ir atlasīts laukā <strong>Kods</strong>.</span><span class="sxs-lookup"><span data-stu-id="342f8-128"><strong>Table</strong> – The number series is available only to the user that is selected in the <strong>Code</strong> field.</span></span></li>
<li><span data-ttu-id="342f8-129"><strong>Grupa</strong> — šī numuru sērija ir pieejama tikai grupai, kura ir atlasīta laukā <strong>Kods</strong>.</span><span class="sxs-lookup"><span data-stu-id="342f8-129"><strong>Group</strong> – The number series is available to the user group that is selected in the <strong>Code</strong> field.</span></span></li>
<li><span data-ttu-id="342f8-130"><strong>Visi</strong> — šī numuru sērija ir pieejama visiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="342f8-130"><strong>All</strong> – The number series is available to all users.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="342f8-131">Kods</span><span class="sxs-lookup"><span data-stu-id="342f8-131">Code</span></span></td>
<td><span data-ttu-id="342f8-132">Atlasiet tā lietotāja vai lietotāju grupas ID, kuriem šī numuru sērija ir piešķirta rēķinu numurēšanai.</span><span class="sxs-lookup"><span data-stu-id="342f8-132">Select the ID of the user or user group that the number series is assigned to for invoice numbering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="342f8-133">Pēdējais datums</span><span class="sxs-lookup"><span data-stu-id="342f8-133">Last date</span></span></td>
<td><span data-ttu-id="342f8-134">Datums, kad numuru sērija tika atjaunināta pēdējo reizi.</span><span class="sxs-lookup"><span data-stu-id="342f8-134">The date that the number series was last updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="342f8-135">Turpināt</span><span class="sxs-lookup"><span data-stu-id="342f8-135">Continue</span></span></td>
<td><span data-ttu-id="342f8-136">Atzīmējiet šo opciju, lai meklētu numuru sērijas, kas ir piešķirtas atlasītajam lietotājam vai lietotāju grupai.</span><span class="sxs-lookup"><span data-stu-id="342f8-136">Select this option to search for number series that are assigned to the selected user or user group.</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-document-self-numbering-ranges"></a><span data-ttu-id="342f8-137">Dokumentu pašnumerācijas diapazonu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="342f8-137">Set up document self-numbering ranges</span></span>
<span data-ttu-id="342f8-138">Rēķiniem un pavadzīmēm, kas tiek ģenerēti moduļos **Debitoru parādi**, **Parādi kreditoriem**, **Krājumu vadība** un **Projektu vadība un uzskaite**, varat piešķirt specifiskas numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="342f8-138">You can assign specific number sequences to invoices and packing slips that are generated in the **Accounts receivable**, **Accounts payable**, **Inventory management**, and **Project management and accounting** modules.</span></span> <span data-ttu-id="342f8-139">Atsevišķas numuru sērijas varat norādīt arī dažādiem lietotājiem un lietotāju grupām, debitoru grupām un kreditoru grupām, vai noliktavām.</span><span class="sxs-lookup"><span data-stu-id="342f8-139">You can also specify individual number sequences for different users and user groups, customer groups and vendor groups, or warehouses.</span></span> <span data-ttu-id="342f8-140">Lai iestatītu numuru sērijas debitoru rēķiniem un kreditoru rēķiniem, izmantojiet lapu **Skaitītāju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="342f8-140">To set up number sequences for customer invoices and vendor invoices, use the **Counters management** page.</span></span> <span data-ttu-id="342f8-141">(Noklikšķiniet uz **Organizācijas administrēšana** &gt; **Numuru sērijas** &gt; **Skaitītāju pārvaldība**.) Numuru sēriju varat definēt pēc lietotāja vai lietotāju grupas vai specifiskām debitoru grupām un kreditoru grupām.</span><span class="sxs-lookup"><span data-stu-id="342f8-141">(Click **Organization administration** &gt; **Number sequences** &gt; **Counters management**.) You can define the number sequence by user or user group, or for specific customer groups and vendor groups.</span></span> <span data-ttu-id="342f8-142">Lai aizpildītu laukus lapā **Skaitītāju pārvaldība**, izmantojiet nākamajā tabulā sniegto informāciju.</span><span class="sxs-lookup"><span data-stu-id="342f8-142">Use the information in the following table to complete the fields on the **Counters management** page.</span></span>

| <span data-ttu-id="342f8-143">Lauks</span><span class="sxs-lookup"><span data-stu-id="342f8-143">Field</span></span>          | <span data-ttu-id="342f8-144">Apraksts</span><span class="sxs-lookup"><span data-stu-id="342f8-144">Description</span></span>                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="342f8-145">Modulis</span><span class="sxs-lookup"><span data-stu-id="342f8-145">Module</span></span>         | <span data-ttu-id="342f8-146">Atlasiet moduli, uz ko attiecas atlasītā numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="342f8-146">Select the module that the selected number sequence applies to.</span></span>                                                                                 |
| <span data-ttu-id="342f8-147">Konta kods</span><span class="sxs-lookup"><span data-stu-id="342f8-147">Account code</span></span>   | <span data-ttu-id="342f8-148">Atlasiet, vai numuru sērijas kods attiecas uz visiem ierakstiem atlasītajā modulī vai tikai uz specifisku grupu šajā modulī.</span><span class="sxs-lookup"><span data-stu-id="342f8-148">Select whether the number sequence code applies to all records in the selected module or to a specific group in the module.</span></span>                     |
| <span data-ttu-id="342f8-149">Kods</span><span class="sxs-lookup"><span data-stu-id="342f8-149">Code</span></span>           | <span data-ttu-id="342f8-150">Atlasiet kodu atlasītajam modulim.</span><span class="sxs-lookup"><span data-stu-id="342f8-150">Select the code for the selected module.</span></span> <span data-ttu-id="342f8-151">**Piezīme.** Lauks **Kods** ir pieejams tikai tad, ja laukā **Konta kods** ir atlasīta opcija **Grupa**.</span><span class="sxs-lookup"><span data-stu-id="342f8-151">**Note:** The **Code** field is available only if **Group** is selected in the **Account code** field.</span></span> |
| <span data-ttu-id="342f8-152">Tips</span><span class="sxs-lookup"><span data-stu-id="342f8-152">Type</span></span>           | <span data-ttu-id="342f8-153">Atlasiet numurējamo dokumentu tipu: **Rēķins** vai **Pavadzīme**.</span><span class="sxs-lookup"><span data-stu-id="342f8-153">Select the type of document to number: **Invoice** or **Packing slip**.</span></span>                                                                         |
| <span data-ttu-id="342f8-154">Automātiska numerācija</span><span class="sxs-lookup"><span data-stu-id="342f8-154">Auto numbering</span></span> | <span data-ttu-id="342f8-155">Atzīmējiet šo opciju, lai numuru dokumentam piešķirtu automātiski.</span><span class="sxs-lookup"><span data-stu-id="342f8-155">Select this option to automatically assign a number to a document.</span></span> <span data-ttu-id="342f8-156">Atsevišķiem dokumentiem šo opciju varat manuāli atzīmēt vai noņemt tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="342f8-156">You can manually select or clear this option for individual documents.</span></span>       |

<span data-ttu-id="342f8-157">Papildinformāciju par to, ka manuāli numurēt rēķinus un pavadzīmes, skatiet rakstā [Labot rēķina ID pārdošanas pasūtījumos Austrumeiropai](emea-edit-invoice-id-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="342f8-157">For information about how to manually number invoices and packing slips, see [Edit invoice IDs on sales orders for Eastern Europe](emea-edit-invoice-id-sales-orders.md).</span></span>

## <a name="affected-processes"></a><span data-ttu-id="342f8-158">Ietekmētie procesi</span><span class="sxs-lookup"><span data-stu-id="342f8-158">Affected processes</span></span>
<span data-ttu-id="342f8-159">Izmantojot rēķinu un pavadzīmju numurēšanu, tiek atjauninātas tālāk uzskaitīto dokumentu galvenes.</span><span class="sxs-lookup"><span data-stu-id="342f8-159">The headers of the following documents are updated with invoice and packing slip numbering:</span></span>

-   <span data-ttu-id="342f8-160">Pārdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="342f8-160">Sales orders</span></span>
-   <span data-ttu-id="342f8-161">Pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="342f8-161">Purchase orders</span></span>
-   <span data-ttu-id="342f8-162">Brīvā teksta rēķini</span><span class="sxs-lookup"><span data-stu-id="342f8-162">Free text invoices</span></span>
-   <span data-ttu-id="342f8-163">Projekta rēķinu priekšlikumi</span><span class="sxs-lookup"><span data-stu-id="342f8-163">Project invoice proposals</span></span>

<span data-ttu-id="342f8-164">Kad grāmatojat tālāk norādītos dokumentus, laukā **Numerācija** varat atlasīt specifisku numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="342f8-164">When you post the following documents, you can select a specific number sequence in the **Numbering** field:</span></span>

-   <span data-ttu-id="342f8-165">Pārdošanas pavadzīme</span><span class="sxs-lookup"><span data-stu-id="342f8-165">Sales packing slip</span></span>
-   <span data-ttu-id="342f8-166">Pārdošanai grāmatojot rēķinu</span><span class="sxs-lookup"><span data-stu-id="342f8-166">Sales posting invoice</span></span>
-   <span data-ttu-id="342f8-167">Pirkšanai grāmatojot produktu ieejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="342f8-167">Purchasing posting product receipt</span></span>
-   <span data-ttu-id="342f8-168">Pirkšanas kreditora rēķini</span><span class="sxs-lookup"><span data-stu-id="342f8-168">Purchasing vendor invoices</span></span>
-   <span data-ttu-id="342f8-169">Grāmatojiet projekta rēķinu priekšlikumus</span><span class="sxs-lookup"><span data-stu-id="342f8-169">Post project invoice proposals</span></span>
-   <span data-ttu-id="342f8-170">Grāmatot brīva teksta rēķinu</span><span class="sxs-lookup"><span data-stu-id="342f8-170">Post free text invoice</span></span>

<span data-ttu-id="342f8-171">Turklāt tālāk norādītās formas tiek papildinātas ar lauku **Atjaunināmie dokumenti**.</span><span class="sxs-lookup"><span data-stu-id="342f8-171">Additionally, forms below are supplemented by the **Documents to update** field:</span></span>

-   <span data-ttu-id="342f8-172">Pirkšanas kreditora rēķinu forma</span><span class="sxs-lookup"><span data-stu-id="342f8-172">Purchasing Vendor invoices form,</span></span>
-   <span data-ttu-id="342f8-173">Pārdošanas pavadzīmes grāmatošanas forma</span><span class="sxs-lookup"><span data-stu-id="342f8-173">Sales Packing slip posting form,</span></span>
-   <span data-ttu-id="342f8-174">Pārdošanas rēķina grāmatošanas forma</span><span class="sxs-lookup"><span data-stu-id="342f8-174">Sales Posting invoice form,</span></span>
-   <span data-ttu-id="342f8-175">Pirkšanas produktu ieejas plūsmas grāmatošanas forma</span><span class="sxs-lookup"><span data-stu-id="342f8-175">Purchasing Posting product receipt form.</span></span>

<span data-ttu-id="342f8-176">Lauks **Atjaunināmie dokumenti** ietekmē lauku **Dokumenta statuss** žurnālā **Pavadzīmju žurnāls** un **Rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="342f8-176">The **Documents to update** field influences on the **Document status** field in **Packing slip journal** and **Invoice Journal**.</span></span> <span data-ttu-id="342f8-177">Veidojot dokumentu **Pavadzīme**, lauka **Dokumenta statuss** vērtība ir vienāda ar vērtību **Nav**.</span><span class="sxs-lookup"><span data-stu-id="342f8-177">On **Packing slip** creation, the **Document status** field value is equal to **None**.</span></span> <span data-ttu-id="342f8-178">Ja laukā **Atjaunināmie dokumenti** tika izvēlēta kāda **Pavadzīme**, tad tās **Dokumenta statuss** ir **Bojāts**, bet **Dokumenta statuss** tādam dokumentam **Pavadzīme**, kur tas tika izdarīts, ir **Atcelts**.</span><span class="sxs-lookup"><span data-stu-id="342f8-178">If any **Packing slip** was chosen in field **Documents to update** then its **Document status** would be **Broken** and the **Document status** of **Packing slip** where it was done will be **Canceled**.</span></span>



