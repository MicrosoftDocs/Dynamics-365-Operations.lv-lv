---
title: "Atskaišu definīcijas finanšu atskaišu veidotājā"
description: "Šajā rakstā ir sniegta informācija par atskaišu definīcijām. Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti. Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 96090a3ae15294d98d6207c8eb4a1e58429ca9eb
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="d2562-105">Atskaišu definīcijas finanšu atskaišu veidotājā</span><span class="sxs-lookup"><span data-stu-id="d2562-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2562-106">Šajā rakstā ir sniegta informācija par atskaišu definīcijām.</span><span class="sxs-lookup"><span data-stu-id="d2562-106">This article provides information about report definitions.</span></span> <span data-ttu-id="d2562-107">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="d2562-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="d2562-108">Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="d2562-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="d2562-109">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="d2562-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="d2562-110">Pārskata definīcija nodrošina arī opcijas un iestatījumus, ko varat izmantot, lai pielāgotu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="d2562-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="d2562-111">Pēc tam, kad jūs nosakiet rindu definīcijas un kolonnu definīcijas, tās nedrīkst kombinēt pārskata definīcijā.</span><span class="sxs-lookup"><span data-stu-id="d2562-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="d2562-112">Šajā brīdī jūs definējat arī citus definīcijas aspektus, piemēram detalizācijas līmeni un pārskata datumu.</span><span class="sxs-lookup"><span data-stu-id="d2562-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="d2562-113">Tad varat saglabāt un izveidot atskaiti.</span><span class="sxs-lookup"><span data-stu-id="d2562-113">You can then save and generate a report.</span></span> <span data-ttu-id="d2562-114">Finanšu atskaišu veidošana piedāvā šādus detalizētības līmeņus:</span><span class="sxs-lookup"><span data-stu-id="d2562-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="d2562-115">Finanšu</span><span class="sxs-lookup"><span data-stu-id="d2562-115">Financial</span></span>
-   <span data-ttu-id="d2562-116">Finanšu un konta</span><span class="sxs-lookup"><span data-stu-id="d2562-116">Financial and Account</span></span>
-   <span data-ttu-id="d2562-117">Finanšu, konta un darbības</span><span class="sxs-lookup"><span data-stu-id="d2562-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="d2562-118">Tomēr, atkarībā no tā, kā dati tiek saglabāti Microsoft Dynamics ERP sistēmā, darbības detaļas var nebūt pieejamas pārskatos.</span><span class="sxs-lookup"><span data-stu-id="d2562-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="d2562-119">Izveidojiet pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="d2562-119">Create a report definition</span></span>
1.  <span data-ttu-id="d2562-120">Pārskatu veidotājā izvēlnē **Fails**, noklikšķiniet uz **Jauns**, un pēc tam atlasiet **Pārskata definīcija**.</span><span class="sxs-lookup"><span data-stu-id="d2562-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="d2562-121">Norādiet atbilstošu informāciju cilnēs **Pārskats**, **Izvade un sadale**, **Galvenes un kājenes** un **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="d2562-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="d2562-122">Pārskata definīcijas saturs</span><span class="sxs-lookup"><span data-stu-id="d2562-122">Contents of a report definition</span></span>
<span data-ttu-id="d2562-123">Šajā tabulā ir aprakstītas pārskata definīcijas cilnes un tas, kā tiek izmantota informācija.</span><span class="sxs-lookup"><span data-stu-id="d2562-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2562-124">Cilne</span><span class="sxs-lookup"><span data-stu-id="d2562-124">Tab</span></span></th>
<th><span data-ttu-id="d2562-125">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d2562-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2562-126">Pārskats</span><span class="sxs-lookup"><span data-stu-id="d2562-126">Report</span></span></td>
<td><span data-ttu-id="d2562-127">Izveidojiet pārskatu, konfigurējiet pārskatu vai modificējiet esošu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="d2562-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2562-128">Izvade un sadale</span><span class="sxs-lookup"><span data-stu-id="d2562-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="d2562-129">Mainiet izvades tipu un pārskata adresātu.</span><span class="sxs-lookup"><span data-stu-id="d2562-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2562-130">Galvenes un kājenes</span><span class="sxs-lookup"><span data-stu-id="d2562-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="d2562-131">Definējiet un formatējiet galvenes un kājenes pārskatam.</span><span class="sxs-lookup"><span data-stu-id="d2562-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="d2562-132">Piemēram, jūs varat pievienot tekstu vai attēlus galvenē vai kājenē.</span><span class="sxs-lookup"><span data-stu-id="d2562-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="d2562-133">Finanšu atskaišu veidošana atbalsta .bmp, .jpg un .png failus attēliem.</span><span class="sxs-lookup"><span data-stu-id="d2562-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="d2562-134">Jūs varat arī pievienot automātiskā teksta kodus, lai ievietotu citu informāciju, piemēram, uzņēmuma nosaukumu, pārskata nosaukumu vai lappuses numuru.</span><span class="sxs-lookup"><span data-stu-id="d2562-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2562-135">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="d2562-135">Settings</span></span></td>
<td><span data-ttu-id="d2562-136">Norādiet pārskata definīcijas iestatījumus, piemēram, šādus iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="d2562-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="d2562-137">Formatēšanas un noapaļošanas summas</span><span class="sxs-lookup"><span data-stu-id="d2562-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="d2562-138">Detalizētu pārskatu formatēšana</span><span class="sxs-lookup"><span data-stu-id="d2562-138">Format detail reports</span></span></li>
<li><span data-ttu-id="d2562-139">Pārskata veidošanas koka formatēšana</span><span class="sxs-lookup"><span data-stu-id="d2562-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="d2562-140">Ģenerēt izņēmumu pārskatu</span><span class="sxs-lookup"><span data-stu-id="d2562-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="d2562-141">Norādīt valūtas konvertēšanu</span><span class="sxs-lookup"><span data-stu-id="d2562-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="d2562-142">Apakšsumma un filtra konta detalizēta informācija</span><span class="sxs-lookup"><span data-stu-id="d2562-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="d2562-143">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d2562-143">See also</span></span>
--------

[<span data-ttu-id="d2562-144">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="d2562-144">Financial reporting</span></span>](financial-reporting-intro.md)




