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
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 322f1cca32053224e1cd6dbaf29c098b983b5e1f
ms.contentlocale: lv-lv
ms.lasthandoff: 08/13/2018

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="a4206-105">Atskaišu definīcijas finanšu atskaišu veidotājā</span><span class="sxs-lookup"><span data-stu-id="a4206-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4206-106">Šajā rakstā ir sniegta informācija par atskaišu definīcijām.</span><span class="sxs-lookup"><span data-stu-id="a4206-106">This article provides information about report definitions.</span></span> <span data-ttu-id="a4206-107">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="a4206-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a4206-108">Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="a4206-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="a4206-109">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="a4206-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a4206-110">Pārskata definīcijā arī ir papildu opcijas un iestatījumi, kurus varat izmantot pārskata pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="a4206-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="a4206-111">Pēc rindu un kolonnu definīciju izveides, tās ir jāapvieno pārskata definīcijā.</span><span class="sxs-lookup"><span data-stu-id="a4206-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="a4206-112">Šajā brīdī jūs definējat arī citus definīcijas aspektus, piemēram detalizācijas līmeni un pārskata datumu.</span><span class="sxs-lookup"><span data-stu-id="a4206-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="a4206-113">Tad varat saglabāt un izveidot atskaiti.</span><span class="sxs-lookup"><span data-stu-id="a4206-113">You can then save and generate a report.</span></span> <span data-ttu-id="a4206-114">Finanšu atskaišu veidošana piedāvā šādus detalizētības līmeņus:</span><span class="sxs-lookup"><span data-stu-id="a4206-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="a4206-115">Finanšu</span><span class="sxs-lookup"><span data-stu-id="a4206-115">Financial</span></span>
- <span data-ttu-id="a4206-116">Finanšu un konta</span><span class="sxs-lookup"><span data-stu-id="a4206-116">Financial and Account</span></span>
- <span data-ttu-id="a4206-117">Finanšu, konta un darbības</span><span class="sxs-lookup"><span data-stu-id="a4206-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="a4206-118">Taču atkarībā no tā, kā dati tiek glabāti Microsoft Dynamics ERP sistēmā, pārskatos var nebūt pieejama detalizēta darījuma informācija.</span><span class="sxs-lookup"><span data-stu-id="a4206-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="a4206-119">Izveidojiet pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="a4206-119">Create a report definition</span></span>
1. <span data-ttu-id="a4206-120">Pārskatu veidotājā izvēlnē **Fails**, noklikšķiniet uz **Jauns**, un pēc tam atlasiet **Pārskata definīcija**.</span><span class="sxs-lookup"><span data-stu-id="a4206-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="a4206-121">Norādiet atbilstošu informāciju cilnēs **Pārskats**, **Izvade un sadale**, **Galvenes un kājenes** un **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="a4206-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="a4206-122">Pārskata definīcijas saturs</span><span class="sxs-lookup"><span data-stu-id="a4206-122">Contents of a report definition</span></span>
<span data-ttu-id="a4206-123">Tālāk redzamajā tabulā ir aprakstītas pārskata definīcijas cilnes un informācijas izmantošanas veids.</span><span class="sxs-lookup"><span data-stu-id="a4206-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4206-124">Cilne</span><span class="sxs-lookup"><span data-stu-id="a4206-124">Tab</span></span></th>
<th><span data-ttu-id="a4206-125">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a4206-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4206-126">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a4206-126">Report</span></span></td>
<td><span data-ttu-id="a4206-127">Izveidojiet, konfigurējiet vai modificējiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="a4206-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4206-128">Izvade un sadale</span><span class="sxs-lookup"><span data-stu-id="a4206-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="a4206-129">Mainiet pārskata izvades veidu un atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="a4206-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4206-130">Galvenes un kājenes</span><span class="sxs-lookup"><span data-stu-id="a4206-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="a4206-131">Norādiet un formatējiet pārskata galvenes un kājenes.</span><span class="sxs-lookup"><span data-stu-id="a4206-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="a4206-132">Piemēram, jūs varat pievienot tekstu vai attēlus galvenē vai kājenē.</span><span class="sxs-lookup"><span data-stu-id="a4206-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="a4206-133">Finanšu atskaišu veidošana atbalsta .bmp, .jpg un .png failus attēliem.</span><span class="sxs-lookup"><span data-stu-id="a4206-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="a4206-134">Jūs varat arī pievienot automātiskā teksta kodus, lai ievietotu citu informāciju, piemēram, uzņēmuma nosaukumu, pārskata nosaukumu vai lappuses numuru.</span><span class="sxs-lookup"><span data-stu-id="a4206-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4206-135">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="a4206-135">Settings</span></span></td>
<td><span data-ttu-id="a4206-136">Norādiet pārskata definīcijas iestatījumu, piemēram:</span><span class="sxs-lookup"><span data-stu-id="a4206-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="a4206-137">Formatējums un noapaļošanas summas</span><span class="sxs-lookup"><span data-stu-id="a4206-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="a4206-138">Formatēt detalizētos pārskatus</span><span class="sxs-lookup"><span data-stu-id="a4206-138">Format detail reports</span></span></li>
<li><span data-ttu-id="a4206-139">Formatēt pārskatu kokus</span><span class="sxs-lookup"><span data-stu-id="a4206-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="a4206-140">Ģenerēt izņēmumu pārskatu</span><span class="sxs-lookup"><span data-stu-id="a4206-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="a4206-141">Norādiet valūtas konversiju</span><span class="sxs-lookup"><span data-stu-id="a4206-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="a4206-142">Apakšsummas un filtru konta detaļas</span><span class="sxs-lookup"><span data-stu-id="a4206-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="a4206-143">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a4206-143">Additional resources</span></span>

[<span data-ttu-id="a4206-144">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="a4206-144">Financial reporting</span></span>](financial-reporting-intro.md)

