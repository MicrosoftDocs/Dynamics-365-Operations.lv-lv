---
title: Atskaišu definīcijas finanšu atskaišu veidotājā
description: Šajā rakstā ir sniegta informācija par atskaišu definīcijām.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7d5531112cfb803912849af3af785b2a69a79f3d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093418"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="d78c6-103">Atskaišu definīcijas finanšu atskaišu veidotājā</span><span class="sxs-lookup"><span data-stu-id="d78c6-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d78c6-104">Šajā rakstā ir sniegta informācija par atskaišu definīcijām.</span><span class="sxs-lookup"><span data-stu-id="d78c6-104">This article provides information about report definitions.</span></span> <span data-ttu-id="d78c6-105">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="d78c6-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="d78c6-106">Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="d78c6-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="d78c6-107">Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="d78c6-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="d78c6-108">Pārskata definīcijā arī ir papildu opcijas un iestatījumi, kurus varat izmantot pārskata pielāgošanai.</span><span class="sxs-lookup"><span data-stu-id="d78c6-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="d78c6-109">Pēc rindu un kolonnu definīciju izveides, tās ir jāapvieno pārskata definīcijā.</span><span class="sxs-lookup"><span data-stu-id="d78c6-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="d78c6-110">Šajā brīdī jūs definējat arī citus definīcijas aspektus, piemēram detalizācijas līmeni un pārskata datumu.</span><span class="sxs-lookup"><span data-stu-id="d78c6-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="d78c6-111">Tad varat saglabāt un izveidot atskaiti.</span><span class="sxs-lookup"><span data-stu-id="d78c6-111">You can then save and generate a report.</span></span> <span data-ttu-id="d78c6-112">Finanšu atskaišu veidošana piedāvā šādus detalizētības līmeņus:</span><span class="sxs-lookup"><span data-stu-id="d78c6-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="d78c6-113">Finanšu</span><span class="sxs-lookup"><span data-stu-id="d78c6-113">Financial</span></span>
- <span data-ttu-id="d78c6-114">Finanšu un konta</span><span class="sxs-lookup"><span data-stu-id="d78c6-114">Financial and Account</span></span>
- <span data-ttu-id="d78c6-115">Finanšu, konta un darbības</span><span class="sxs-lookup"><span data-stu-id="d78c6-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="d78c6-116">Taču atkarībā no tā, kā dati tiek glabāti Microsoft Dynamics ERP sistēmā, pārskatos var nebūt pieejami darbību dati.</span><span class="sxs-lookup"><span data-stu-id="d78c6-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="d78c6-117">Izveidojiet pārskata definīciju</span><span class="sxs-lookup"><span data-stu-id="d78c6-117">Create a report definition</span></span>
1. <span data-ttu-id="d78c6-118">Pārskatu veidotājā izvēlnē **Fails**, noklikšķiniet uz **Jauns**, un pēc tam atlasiet **Pārskata definīcija**.</span><span class="sxs-lookup"><span data-stu-id="d78c6-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="d78c6-119">Norādiet atbilstošu informāciju cilnēs **Pārskats**, **Izvade un sadale**, **Galvenes un kājenes** un **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="d78c6-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="d78c6-120">Pārskata definīcijas saturs</span><span class="sxs-lookup"><span data-stu-id="d78c6-120">Contents of a report definition</span></span>
<span data-ttu-id="d78c6-121">Tālāk redzamajā tabulā ir aprakstītas pārskata definīcijas cilnes un informācijas izmantošanas veids.</span><span class="sxs-lookup"><span data-stu-id="d78c6-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d78c6-122">Cilne</span><span class="sxs-lookup"><span data-stu-id="d78c6-122">Tab</span></span></th>
<th><span data-ttu-id="d78c6-123">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d78c6-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d78c6-124">Pārskats</span><span class="sxs-lookup"><span data-stu-id="d78c6-124">Report</span></span></td>
<td><span data-ttu-id="d78c6-125">Izveidojiet, konfigurējiet vai modificējiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="d78c6-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d78c6-126">Izvade un sadale</span><span class="sxs-lookup"><span data-stu-id="d78c6-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="d78c6-127">Mainiet pārskata izvades veidu un atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="d78c6-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d78c6-128">Galvenes un kājenes</span><span class="sxs-lookup"><span data-stu-id="d78c6-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="d78c6-129">Norādiet un formatējiet pārskata galvenes un kājenes.</span><span class="sxs-lookup"><span data-stu-id="d78c6-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="d78c6-130">Piemēram, jūs varat pievienot tekstu vai attēlus galvenē vai kājenē.</span><span class="sxs-lookup"><span data-stu-id="d78c6-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="d78c6-131">Finanšu atskaišu veidošana atbalsta .bmp, .jpg un .png failus attēliem.</span><span class="sxs-lookup"><span data-stu-id="d78c6-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="d78c6-132">Jūs varat arī pievienot automātiskā teksta kodus, lai ievietotu citu informāciju, piemēram, uzņēmuma nosaukumu, pārskata nosaukumu vai lappuses numuru.</span><span class="sxs-lookup"><span data-stu-id="d78c6-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d78c6-133">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="d78c6-133">Settings</span></span></td>
<td><span data-ttu-id="d78c6-134">Norādiet pārskata definīcijas iestatījumu, piemēram:</span><span class="sxs-lookup"><span data-stu-id="d78c6-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="d78c6-135">Formatējums un noapaļošanas summas</span><span class="sxs-lookup"><span data-stu-id="d78c6-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="d78c6-136">Formatēt detalizētos pārskatus</span><span class="sxs-lookup"><span data-stu-id="d78c6-136">Format detail reports</span></span></li>
<li><span data-ttu-id="d78c6-137">Formatēt pārskatu kokus</span><span class="sxs-lookup"><span data-stu-id="d78c6-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="d78c6-138">Ģenerēt izņēmumu pārskatu</span><span class="sxs-lookup"><span data-stu-id="d78c6-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="d78c6-139">Norādiet valūtas konversiju</span><span class="sxs-lookup"><span data-stu-id="d78c6-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="d78c6-140">Apakšsummas un filtru konta detaļas</span><span class="sxs-lookup"><span data-stu-id="d78c6-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="d78c6-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d78c6-141">Additional resources</span></span>

[<span data-ttu-id="d78c6-142">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="d78c6-142">Financial reporting</span></span>](financial-reporting-intro.md)
