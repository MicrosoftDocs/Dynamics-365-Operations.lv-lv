---
title: Atskaišu definīcijas finanšu atskaišu veidotājā
description: Šajā rakstā ir sniegta informācija par atskaišu definīcijām. Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti. Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 322f1cca32053224e1cd6dbaf29c098b983b5e1f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547058"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="7bcbd-105">Atskaišu definīcijas finanšu atskaišu veidotājā</span><span class="sxs-lookup"><span data-stu-id="7bcbd-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bcbd-106">Šajā rakstā ir sniegta informācija par atskaišu definīcijām.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-106">This article provides information about report definitions.</span></span> <span data-ttu-id="7bcbd-107">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="7bcbd-108">Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="7bcbd-109">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="7bcbd-110">Pārskata definīcijā arī ir papildu opcijas un iestatījumi, kurus varat izmantot pārskata pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="7bcbd-111">Pēc rindu un kolonnu definīciju izveides, tās ir jāapvieno pārskata definīcijā.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="7bcbd-112">Šajā brīdī jūs definējat arī citus definīcijas aspektus, piemēram detalizācijas līmeni un pārskata datumu.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="7bcbd-113">Tad varat saglabāt un izveidot atskaiti.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-113">You can then save and generate a report.</span></span> <span data-ttu-id="7bcbd-114">Finanšu atskaišu veidošana piedāvā šādus detalizētības līmeņus:</span><span class="sxs-lookup"><span data-stu-id="7bcbd-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="7bcbd-115">Finanšu</span><span class="sxs-lookup"><span data-stu-id="7bcbd-115">Financial</span></span>
- <span data-ttu-id="7bcbd-116">Finanšu un konta</span><span class="sxs-lookup"><span data-stu-id="7bcbd-116">Financial and Account</span></span>
- <span data-ttu-id="7bcbd-117">Finanšu, konta un darbības</span><span class="sxs-lookup"><span data-stu-id="7bcbd-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="7bcbd-118">Taču atkarībā no tā, kā dati tiek glabāti Microsoft Dynamics ERP sistēmā, pārskatos var nebūt pieejami darbību dati.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="7bcbd-119">Izveidojiet pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="7bcbd-119">Create a report definition</span></span>
1. <span data-ttu-id="7bcbd-120">Pārskatu veidotājā izvēlnē **Fails**, noklikšķiniet uz **Jauns**, un pēc tam atlasiet **Pārskata definīcija**.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="7bcbd-121">Norādiet atbilstošu informāciju cilnēs **Pārskats**, **Izvade un sadale**, **Galvenes un kājenes** un **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="7bcbd-122">Pārskata definīcijas saturs</span><span class="sxs-lookup"><span data-stu-id="7bcbd-122">Contents of a report definition</span></span>
<span data-ttu-id="7bcbd-123">Tālāk redzamajā tabulā ir aprakstītas pārskata definīcijas cilnes un informācijas izmantošanas veids.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7bcbd-124">Cilne</span><span class="sxs-lookup"><span data-stu-id="7bcbd-124">Tab</span></span></th>
<th><span data-ttu-id="7bcbd-125">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7bcbd-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7bcbd-126">Pārskats</span><span class="sxs-lookup"><span data-stu-id="7bcbd-126">Report</span></span></td>
<td><span data-ttu-id="7bcbd-127">Izveidojiet, konfigurējiet vai modificējiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7bcbd-128">Izvade un sadale</span><span class="sxs-lookup"><span data-stu-id="7bcbd-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="7bcbd-129">Mainiet pārskata izvades veidu un atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7bcbd-130">Galvenes un kājenes</span><span class="sxs-lookup"><span data-stu-id="7bcbd-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="7bcbd-131">Norādiet un formatējiet pārskata galvenes un kājenes.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="7bcbd-132">Piemēram, jūs varat pievienot tekstu vai attēlus galvenē vai kājenē.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="7bcbd-133">Finanšu atskaišu veidošana atbalsta .bmp, .jpg un .png failus attēliem.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="7bcbd-134">Jūs varat arī pievienot automātiskā teksta kodus, lai ievietotu citu informāciju, piemēram, uzņēmuma nosaukumu, pārskata nosaukumu vai lappuses numuru.</span><span class="sxs-lookup"><span data-stu-id="7bcbd-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7bcbd-135">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="7bcbd-135">Settings</span></span></td>
<td><span data-ttu-id="7bcbd-136">Norādiet pārskata definīcijas iestatījumu, piemēram:</span><span class="sxs-lookup"><span data-stu-id="7bcbd-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="7bcbd-137">Formatējums un noapaļošanas summas</span><span class="sxs-lookup"><span data-stu-id="7bcbd-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="7bcbd-138">Formatēt detalizētos pārskatus</span><span class="sxs-lookup"><span data-stu-id="7bcbd-138">Format detail reports</span></span></li>
<li><span data-ttu-id="7bcbd-139">Formatēt pārskatu kokus</span><span class="sxs-lookup"><span data-stu-id="7bcbd-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="7bcbd-140">Ģenerēt izņēmumu pārskatu</span><span class="sxs-lookup"><span data-stu-id="7bcbd-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="7bcbd-141">Norādiet valūtas konversiju</span><span class="sxs-lookup"><span data-stu-id="7bcbd-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="7bcbd-142">Apakšsummas un filtru konta detaļas</span><span class="sxs-lookup"><span data-stu-id="7bcbd-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="7bcbd-143">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7bcbd-143">Additional resources</span></span>

[<span data-ttu-id="7bcbd-144">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="7bcbd-144">Financial reporting</span></span>](financial-reporting-intro.md)
