---
title: Papildu filtrēšanas un vaicājumu sintakse
description: Šajā tēmā ir aprakstītas filtrēšanas un vaicājumu opcijas, kas ir pieejamas, ja rūts Filtrēšana dialoglodziņā Detalizētā filtrēšana/kārtošana vai režģa kolonnas filtros izmantojat operatoru atbilst.
author: jasongre
manager: AnnBe
ms.date: 01/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5a96921436311440ba60c3fa31135457cf9f291
ms.sourcegitcommit: 8585de8acf579bcc033671ef270fa9d92230121b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/02/2020
ms.locfileid: "2931292"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="28d0a-103">Papildu filtrēšanas un vaicājumu sintakse</span><span class="sxs-lookup"><span data-stu-id="28d0a-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28d0a-104">Šajā tēmā ir aprakstītas filtrēšanas un vaicājumu opcijas, kas ir pieejamas, ja rūts Filtrēšana dialoglodziņā Detalizētā filtrēšana/kārtošana vai režģa kolonnas filtros izmantojat operatoru **atbilst**.</span><span class="sxs-lookup"><span data-stu-id="28d0a-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="28d0a-105">Papildu vaicājumu sintakse</span><span class="sxs-lookup"><span data-stu-id="28d0a-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="28d0a-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="28d0a-106">Syntax</span></span></th>
<th><span data-ttu-id="28d0a-107">Simbolu apraksts</span><span class="sxs-lookup"><span data-stu-id="28d0a-107">Character description</span></span></th>
<th><span data-ttu-id="28d0a-108">apraksts</span><span class="sxs-lookup"><span data-stu-id="28d0a-108">Description</span></span></th>
<th><span data-ttu-id="28d0a-109">Piemērs</span><span class="sxs-lookup"><span data-stu-id="28d0a-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="28d0a-110"><em>vērtība</em></span><span class="sxs-lookup"><span data-stu-id="28d0a-110"><em>value</em></span></span></td>
<td><span data-ttu-id="28d0a-111">Vienāds ar ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-112">Ierakstiet meklējamo vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="28d0a-113"><strong>Smits</strong> atrod &quot;Smits&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-114">!<em>vērtība</em> (izsaukuma zīme)</span><span class="sxs-lookup"><span data-stu-id="28d0a-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="28d0a-115">Nav vienāds ar ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-116">Ierakstiet izsaukuma zīmi un tad vērtību, kas jāizslēdz.</span><span class="sxs-lookup"><span data-stu-id="28d0a-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="28d0a-117"><strong>!Smits</strong> atrod visas vērtības, izņemot vērtību &quot;Smits&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-118"><em>vērtība no</em>..<em>vērtība līdz</em> (divpunkte)</span><span class="sxs-lookup"><span data-stu-id="28d0a-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="28d0a-119">Starp divām vērtībām, kas atdalītas ar divpunkti</span><span class="sxs-lookup"><span data-stu-id="28d0a-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="28d0a-120">Ierakstiet, no kuras vērtības, pēc tam divus punktus un līdz kurai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="28d0a-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="28d0a-121"><strong>1..10</strong> atrod visas vērtības no 1 līdz 10.</span><span class="sxs-lookup"><span data-stu-id="28d0a-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="28d0a-122">Tomēr virknes laukā <strong>A..C</strong> atrod visas vērtības, kas sākas ar &quot;A&quot; un &quot;B&quot;, un vērtības, kas ir pilnīgi vienādas ar &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="28d0a-123">Piemēram, šis vaicājums neatradīs &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="28d0a-124">Lai atrastu visas vērtības no &quot;A<em>&quot; līdz &quot;C</em>&quot;, ierakstiet <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-125">..<em>vērtība</em> (divpunkte)</span><span class="sxs-lookup"><span data-stu-id="28d0a-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="28d0a-126">Mazāks vai vienāds ar ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-127">Ierakstiet divus punktus un pēc tam vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="28d0a-128"><strong>..1000</strong> atrod visus skaitļus, kas ir mazāki par vai vienādi ar 1000, piemēram, &quot;100&quot;, &quot;999,95&quot; un &quot;1000&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-129"><em>vērtība</em>..</span><span class="sxs-lookup"><span data-stu-id="28d0a-129"><em>value</em>..</span></span> <span data-ttu-id="28d0a-130">(divpunkte)</span><span class="sxs-lookup"><span data-stu-id="28d0a-130">(double period)</span></span></td>
<td><span data-ttu-id="28d0a-131">Lielāks vai vienāds ar ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-132">Ierakstiet vērtību un tad divus punktu.</span><span class="sxs-lookup"><span data-stu-id="28d0a-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="28d0a-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="28d0a-133"><strong>1000..</strong></span></span> <span data-ttu-id="28d0a-134">atrod visus skaitļus, kas ir lielāki par vai vienādi ar 1000, piemēram, &quot;1000&quot;, &quot;1000,01&quot; un &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-135">&gt;<em>vērtība</em> (zīme “lielāks par”)</span><span class="sxs-lookup"><span data-stu-id="28d0a-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="28d0a-136">Lielāka par ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-137">Ierakstiet zīmi “lielāks par” (<strong>&gt;</strong>) un pēc tam vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="28d0a-138"><strong>&gt;1000</strong> atrod visus skaitļus, kas ir lielāki par 1000, piemēram, &quot;1000,01&quot;, &quot;20 000&quot; un &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-139">&lt;<em>vērtība</em> (zīme “mazāks par”)</span><span class="sxs-lookup"><span data-stu-id="28d0a-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="28d0a-140">Mazāka par ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-141">Ierakstiet zīmi “mazāks par” (<strong>&lt;</strong>) un pēc tam vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="28d0a-142"><strong>&lt;1000</strong> atrod visus skaitļus, kas ir mazāki 1000, piemēram, &quot;999,99&quot;, &quot;1&quot; un &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-143"><em>vērtība</em>\* (zvaigznīte)</span><span class="sxs-lookup"><span data-stu-id="28d0a-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="28d0a-144">Sākot no ievadītas vērtības.</span><span class="sxs-lookup"><span data-stu-id="28d0a-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-145">Ierakstiet sākuma vērtību un pēc tam zvaigznīti (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="28d0a-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="28d0a-146"><strong>S\*</strong> atrod jebkuru virkni, kas sākas ar &quot;S&quot;, piemēram, &quot;Stokholma&quot;, &quot;Sidneja&quot; un &quot;Sanfrancisko&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-147">\*<em>vērtība</em> (zvaigznīte)</span><span class="sxs-lookup"><span data-stu-id="28d0a-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="28d0a-148">Beidzas ar ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-149">Ierakstiet zvaigznīti un pēc tam beidzamo vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="28d0a-150"><strong>\*austrumi</strong> atrod jebkuru virkni, kas beidzas ar &quot;austrumi&quot;, piemēram, &quot;ziemeļaustrumi&quot; un &quot;dienvidaustrumi&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-151">*<em>vērtība</em>* (zvaigznīte)</span><span class="sxs-lookup"><span data-stu-id="28d0a-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="28d0a-152">Satur ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="28d0a-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="28d0a-153">Ierakstiet zvaigznīti, pēc tam vērtību un vēl vienu zvaigznīti.</span><span class="sxs-lookup"><span data-stu-id="28d0a-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="28d0a-154"><strong>*au*</strong> atrod jebkādu virkni, kas ietver &quot;au&quot;, piemēram, &quot;ziemeļaustrumi&quot; un &quot;dienvidaustrumi&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-155">?</span><span class="sxs-lookup"><span data-stu-id="28d0a-155">?</span></span> <span data-ttu-id="28d0a-156">(jautājuma zīme)</span><span class="sxs-lookup"><span data-stu-id="28d0a-156">(question mark)</span></span></td>
<td><span data-ttu-id="28d0a-157">Satur vienu vai vairākas nezināmas zīmes.</span><span class="sxs-lookup"><span data-stu-id="28d0a-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="28d0a-158">Ierakstiet jautājuma zīmi nezināmās zīmes vietā vērtībā.</span><span class="sxs-lookup"><span data-stu-id="28d0a-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="28d0a-159"><strong>Sm?ts</strong> atrod &quot;Smits&quot; un &quot;Smats&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-160"><em>vērtība</em>,<em>vērtība</em> (komats)</span><span class="sxs-lookup"><span data-stu-id="28d0a-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="28d0a-161">Atbilst vērtībām, kas atdalītas ar komatiem.</span><span class="sxs-lookup"><span data-stu-id="28d0a-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="28d0a-162">Ierakstiet visus kritērijus un atdaliet tās ar komatiem.</span><span class="sxs-lookup"><span data-stu-id="28d0a-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="28d0a-163"><strong>A, D, F, G</strong> atrod &quot;A&quot;, &quot;D&quot;, &quot;F&quot; un &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="28d0a-164"><strong>10, 20, 30, 100</strong> atrod &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="28d0a-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-165">"" (divas dubultpēdiņas)</span><span class="sxs-lookup"><span data-stu-id="28d0a-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="28d0a-166">Atbilst tukšai vērtībai</span><span class="sxs-lookup"><span data-stu-id="28d0a-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="28d0a-167">Ierakstiet divas secīgas dubultās pēdiņas, lai filtrētu tukšas vērtības šajā laukā.</span><span class="sxs-lookup"><span data-stu-id="28d0a-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="28d0a-168">Divas secīgas dubultās pēdiņas (<strong>""</strong>) atrod rindas, kurām pašreizējai kolonnai nav vērtības.</span><span class="sxs-lookup"><span data-stu-id="28d0a-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-169">(<span class="code">SQL priekšraksts</span>) (SQL priekšraksts iekavās)</span><span class="sxs-lookup"><span data-stu-id="28d0a-169">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="28d0a-170">Atbilst definētajam vaicājumam.</span><span class="sxs-lookup"><span data-stu-id="28d0a-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="28d0a-171">Ierakstiet vaicājumu kā SQL priekšraksts apaļās iekavās.</span><span class="sxs-lookup"><span data-stu-id="28d0a-171">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="28d0a-172"><strong><span class="code">(datu avots.Lauka nosaukums != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="28d0a-172"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-173">O</span><span class="sxs-lookup"><span data-stu-id="28d0a-173">T</span></span></td>
<td><span data-ttu-id="28d0a-174">Šodienas datums</span><span class="sxs-lookup"><span data-stu-id="28d0a-174">Today's date</span></span></td>
<td><span data-ttu-id="28d0a-175"><strong>T</strong> veida.</span><span class="sxs-lookup"><span data-stu-id="28d0a-175">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="28d0a-176"><strong>T</strong> atbilst šodienas datumam.</span><span class="sxs-lookup"><span data-stu-id="28d0a-176"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-177">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metode iekavās)</span><span class="sxs-lookup"><span data-stu-id="28d0a-177">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="28d0a-178">Atbilstība metodes <strong>SysQueryRangeUtil</strong> parametru norādītajai vērtībai vai vērtību diapazonam</span><span class="sxs-lookup"><span data-stu-id="28d0a-178">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="28d0a-179">Ierakstiet metodi <strong>SysQueryRangeUtil</strong>, kurai ir parametri, kas norāda vērtību vai vērtību diapazonu.</span><span class="sxs-lookup"><span data-stu-id="28d0a-179">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="28d0a-180">Noklikšķiniet uz <strong>Debitoru parādi</strong> &gt; <strong>Rēķini</strong> &gt; <strong>Atvērtie debitoru rēķini</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-180">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-181">Nospiediet taustiņu kombināciju Ctrl+Shift+F3, lai atvērtu lapu <strong>Uzziņas</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-181">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="28d0a-182">Cilnē <strong>Diapazons</strong> noklikšķiniet uz <strong>Pievienot</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-182">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-183">Laukā <strong>Tabula</strong> atlasiet <strong>Neapmaksātās debitora darbības</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-183">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-184">Laukā <strong>Lauks</strong> atlasiet <strong>Izpildes datums</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-184">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-185">Laukā <strong>Kritēriji</strong> ievadiet <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-185">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-186">Noklikšķiniet uz <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-186">Click <strong>OK</strong>.</span></span> <span data-ttu-id="28d0a-187">Saraksta lapa tiek atjaunināta, un tajā ir uzskaitīti kritērijiem atbilstoši ievadītie rēķini.</span><span class="sxs-lookup"><span data-stu-id="28d0a-187">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="28d0a-188">Šajā piemērā ir uzskaitīti rēķini, kas bija jāmaksā iepriekšējo divu gadu laikā.</span><span class="sxs-lookup"><span data-stu-id="28d0a-188">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="28d0a-189">Papildinformāciju, kā arī vairākus piemērus par <strong>SysQueryRangeUtil</strong> datuma metodēm skatiet tabulā nākamajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="28d0a-189">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="28d0a-190">Papildu datumu vaicājumi, kas lieto SysQueryRangeUtil metodes</span><span class="sxs-lookup"><span data-stu-id="28d0a-190">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="28d0a-191">Metode</span><span class="sxs-lookup"><span data-stu-id="28d0a-191">Method</span></span></th>
<th><span data-ttu-id="28d0a-192">Apraksts</span><span class="sxs-lookup"><span data-stu-id="28d0a-192">Description</span></span></th>
<th><span data-ttu-id="28d0a-193">Piemērs</span><span class="sxs-lookup"><span data-stu-id="28d0a-193">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="28d0a-194">Diena (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="28d0a-194">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="28d0a-195">Atrodiet datumu, kas atbilst sesijas datumam.</span><span class="sxs-lookup"><span data-stu-id="28d0a-195">Find a date relative to the session date.</span></span> <span data-ttu-id="28d0a-196">Pozitīvās vērtības norāda turpmākos datumus, bet negatīvas vērtības norāda iepriekšējos datumus.</span><span class="sxs-lookup"><span data-stu-id="28d0a-196">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-197"><strong>Rīt</strong> — ievadiet <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-197"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-198"><strong>Šodien</strong> — ievadiet <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-198"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-199"><strong>Vakar</strong> — ievadiet <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-199"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-200">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="28d0a-200">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="28d0a-201">Atrodiet datumu diapazonu, kas atbilst sesijas datumam.</span><span class="sxs-lookup"><span data-stu-id="28d0a-201">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="28d0a-202">Pozitīvās vērtības norāda turpmākos datumus, bet negatīvas vērtības norāda iepriekšējos datumus.</span><span class="sxs-lookup"><span data-stu-id="28d0a-202">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-203"><strong>Pēdējās 30 dienas</strong> — ievadiet <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-203"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-204"><strong>Iepriekšējās 30 dienas un nākamās 30 dienas</strong> — ievadiet <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-204"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-205">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="28d0a-205">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="28d0a-206">Atrast visus datumus pēc norādītā atbilstošā datuma.</span><span class="sxs-lookup"><span data-stu-id="28d0a-206">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-207"><strong>Vairāk nekā 30 dienas no šodienas</strong> — ievadiet <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-207"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-208">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="28d0a-208">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="28d0a-209">Atrodiet visus datumu/laika ierakstus pēc pašreizējā laika.</span><span class="sxs-lookup"><span data-stu-id="28d0a-209">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-210"><strong>Visi turpmākie datumi/laiki</strong> — ievadiet <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-210"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-211">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="28d0a-211">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="28d0a-212">Atrodiet visus datumus pirms norādītā atbilstošā datuma.</span><span class="sxs-lookup"><span data-stu-id="28d0a-212">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-213"><strong>Mazāk nekā septiņas dienas no šodienas</strong> — ievadiet <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-213"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-214">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="28d0a-214">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="28d0a-215">Atrodiet visus datumu/laika ierakstus pirms pašreizējā laika.</span><span class="sxs-lookup"><span data-stu-id="28d0a-215">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-216"><strong>Vis iepriekšējie datumi/laiki</strong> — ievadiet <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-216"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-217">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="28d0a-217">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="28d0a-218">Atrodiet pašreizējo mēnesi datumu diapazonā, kurā norādīti mēneši.</span><span class="sxs-lookup"><span data-stu-id="28d0a-218">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-219"><strong>Iepriekšējie divi mēneši</strong> — ievadiet <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-219"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-220"><strong>Nākamie trīs mēneši</strong> — ievadiet <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-220"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="28d0a-221">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="28d0a-221">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="28d0a-222">Atrodiet pašreizējo gadu datumu diapazonā, kurā norādīti gadi.</span><span class="sxs-lookup"><span data-stu-id="28d0a-222">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="28d0a-223"><strong>Nākamais gads</strong> — ievadiet <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-223"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="28d0a-224"><strong>Iepriekšējais gads</strong> — ievadiet <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="28d0a-224"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
