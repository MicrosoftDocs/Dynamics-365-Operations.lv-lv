---
title: Debitoru vecumstruktūra
description: Debitoru vecumstruktūras pārskats parāda debitoru apmaksājamās bilances, sakārtotas pēc datuma intervāla vai vecumstruktūras perioda.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2020
ms.locfileid: "4445757"
---
# <a name="customer-aging-report"></a><span data-ttu-id="ff799-103">Debitoru vecumstruktūra</span><span class="sxs-lookup"><span data-stu-id="ff799-103">Customer aging report</span></span> 

<span data-ttu-id="ff799-104">Pārskats **Debitoru vecumstruktūras** parāda debitoru apmaksājamās bilances, sakārtotas pēc datuma intervāla vai vecumstruktūras perioda.</span><span class="sxs-lookup"><span data-stu-id="ff799-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="ff799-105">Veidojot šo pārskatu, tiek rādīti tālāk norādītie noklusējuma parametri.</span><span class="sxs-lookup"><span data-stu-id="ff799-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="ff799-106">Izmantojot šos parametrus, varat filtrēt pārskatā ietveramos datus.</span><span class="sxs-lookup"><span data-stu-id="ff799-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="ff799-107">Papildinformācijai skatiet [Iestatīt iekasēšanu](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="ff799-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff799-108">Lauks</span><span class="sxs-lookup"><span data-stu-id="ff799-108">Field</span></span></p></th>
<th><p><span data-ttu-id="ff799-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ff799-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff799-110"><strong>Rēķinu klasificēšana</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-111">Atlasiet vienu vai vairākas rēķinu klasifikācijas, ko iekļaut pārskatā.</span><span class="sxs-lookup"><span data-stu-id="ff799-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ff799-112">**Piezīme:** šī vadīkla ir pieejama tikai tad, ja ir atlasīta konfigurācijas atslēga <STRONG>Publiskais sektors</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ff799-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff799-113"><strong>Ietvert transakcijas bez rēķinu klasificēšanas grupas</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-114">Ja šī izvēles rūtiņa ir atzīmēta, pārskatā tiks parādīti visi darījumi, kam nav piešķirta rēķinu klasifikācija.</span><span class="sxs-lookup"><span data-stu-id="ff799-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ff799-115">**Piezīme:** šī vadīkla ir pieejama tikai tad, ja ir atlasīta konfigurācijas atslēga <STRONG>Publiskais sektors</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ff799-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-116"><strong>Vecumstruktūras no</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-117">Ievadiet datumu, kas izmantots pašreizējam vecumstruktūras intervālam.</span><span class="sxs-lookup"><span data-stu-id="ff799-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-118"><strong>Bilance uz</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-119">Ievadiet datumu, kuram skatīt debitoru bilances.</span><span class="sxs-lookup"><span data-stu-id="ff799-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="ff799-120">To sauc arī par darījumu beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="ff799-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff799-121"><strong>Sākuma datums</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-122">Ievadiet pārskatā iekļaujamo datumu, kas atrodas pirmā perioda intervālā vai vecumstruktūras periodā.</span><span class="sxs-lookup"><span data-stu-id="ff799-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-123"><strong>Kritēriji</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-124">Atlasiet datuma veidu, uz kā balstīt šo pārskatu.</span><span class="sxs-lookup"><span data-stu-id="ff799-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="ff799-125"><strong>Darījuma datums</strong> – darījumu grāmatošanas datums.</span><span class="sxs-lookup"><span data-stu-id="ff799-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="ff799-126">Piemēram, tas var būt rēķina datums, kas ir izpildes datuma aprēķina pamats.</span><span class="sxs-lookup"><span data-stu-id="ff799-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="ff799-127"><strong>Izpildes datums</strong> – darījumu izpildes datums, kas balstīts uz maksāšanas nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ff799-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="ff799-128"><strong>Dokumenta datums</strong> – lietotāja definēts dokumenta datums, kas ir izpildes datuma aprēķina pamats.</span><span class="sxs-lookup"><span data-stu-id="ff799-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff799-129"><strong>Vecumstruktūras perioda definīcija</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-130">Atlasiet vecumstruktūras perioda definīciju.</span><span class="sxs-lookup"><span data-stu-id="ff799-130">Select an aging period definition.</span></span> <span data-ttu-id="ff799-131">Lauks <strong>Intervāls</strong> netiek izmantots, atlasot vecumstruktūras perioda definīciju.</span><span class="sxs-lookup"><span data-stu-id="ff799-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="ff799-132">Vecumstruktūras perioda definīcijas, kurām ir vairāk nekā seši vecumstruktūras periodi, drukātā pārskatā nevar izmantot.</span><span class="sxs-lookup"><span data-stu-id="ff799-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="ff799-133">**Piezīme:** vecumstruktūras periodus var iestatīt lapā <STRONG>Vecumstruktūras perioda definīcijas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ff799-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-134"><strong>Drukāt vecumstruktūras perioda aprakstu</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-135">Atlasiet <strong>Jā</strong>, lai pārskatā iekļautu vecumstruktūras periodu aprakstus katras vecumstruktūras perioda kolonnas galvenē.</span><span class="sxs-lookup"><span data-stu-id="ff799-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="ff799-136">Atlasiet <strong>Nē</strong>, lai drukātu pārskatu bez kolonnu galvenēm.</span><span class="sxs-lookup"><span data-stu-id="ff799-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff799-137"><strong>Intervāls</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-138">Definējiet izmantojamo periodu, ievadot dienas vai mēneša vienību skaitu katrā periodā.</span><span class="sxs-lookup"><span data-stu-id="ff799-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="ff799-139">Piemēram, lai skatītu vecumstruktūras informāciju pa nedēļām, ievadiet 7 šajā laukā un atlasiet <strong>Diena</strong> laukā <strong>Diena/Mēnesis</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff799-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="ff799-140">**Piezīme:** šajā laukā ievadītā informācija tiek izmantota tikai tad, ja nav atlasīta vecumstruktūras perioda definīcija.</span><span class="sxs-lookup"><span data-stu-id="ff799-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="ff799-141">Pretējā gadījumā drukas virziens tiek definēts vecumstruktūras perioda definīcijā.</span><span class="sxs-lookup"><span data-stu-id="ff799-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-142"><strong>Diena/Mēnesis</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-143">Atlasiet vienību <strong>Diena</strong> vai <strong>Mēnesis</strong>, ko izmanto, lai definētu periodu laukā <strong>Intervāls</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff799-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff799-144"><strong>Drukas virziens</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-145">Atlasiet, vai aprēķināt bilances un drukāt vecumstruktūras pārskatu par pagājušajiem vai nākamajiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="ff799-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="ff799-146">Datumi tiek novērtēti attiecībā pret datumu, kas atlasīts laukā <strong>Bilance uz</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff799-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="ff799-147">Atlasiet <strong>Atpakaļ</strong>, lai parādītu informāciju par pagājušajiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="ff799-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="ff799-148">Atlasiet <strong>Uz priekšu</strong>, lai parādītu informāciju par nākamajiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="ff799-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="ff799-149">
  
<STRONG>Piezīme:</STRONG> šajā laukā ievadītā informācija tiek izmantota tikai tad, ja nav atlasīta vecumstruktūras perioda definīcija.</span><span class="sxs-lookup"><span data-stu-id="ff799-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-150"><strong>Detalizēti</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-151">Atlasiet, lai uzskaitītu darījumus, kas ir iekļauti pārskatā redzamajās bilancēs.</span><span class="sxs-lookup"><span data-stu-id="ff799-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff799-152"><strong>Iekļaut summas darījuma valūtā</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-153">Atlasiet, lai iekļautu summas darījuma valūtā papildus summām uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="ff799-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="ff799-154">Ja šī izvēles rūtiņa nav atzīmēta, pārskata summas tiek parādītas tikai uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="ff799-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-155"><strong>Negatīva bilance</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-156">Atlasiet, lai ietvertu debitoru kontus ar negatīvām bilancēm.</span><span class="sxs-lookup"><span data-stu-id="ff799-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff799-157"><strong>Neiekļaut nulles bilances kontus</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-158">Atlasiet, lai neiekļautu debitoru kontus ar nulles bilancēm.</span><span class="sxs-lookup"><span data-stu-id="ff799-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff799-159"><strong>Maksājumu pozicionēšana</strong></span><span class="sxs-lookup"><span data-stu-id="ff799-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="ff799-160">Atlasiet, lai parādītu nenokārtotos maksājumus.</span><span class="sxs-lookup"><span data-stu-id="ff799-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="ff799-161">Tie tiek parādīti pārskata pirmajā kolonnā.</span><span class="sxs-lookup"><span data-stu-id="ff799-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

