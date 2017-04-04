---
title: "Iestatītu parakstītāji drukas formas"
description: "Juridiskām personām ar Čehijas, Igaunijas, Ungārijas, Lietuvas, Latvija, Polija un Krievija, varat uzstādīt parakstītājus un virsraksti debitorus un kreditorus, kas drukāt dokumentus, piemēram, rēķinos un naudas pasūtījumiem."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 263464
ms.assetid: 7213914a-ecb6-4711-99fe-4e11867aaf4d
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 45d2facde1e5502f4a5863863554a486916c26cd
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-signers-for-print-forms"></a>Iestatītu parakstītāji drukas formas

Juridiskām personām ar Čehijas, Igaunijas, Ungārijas, Lietuvas, Latvija, Polija un Krievija, varat uzstādīt parakstītājus un virsraksti debitorus un kreditorus, kas drukāt dokumentus, piemēram, rēķinos un naudas pasūtījumiem.

<a name="set-up-default-values"></a>Noklusēto vērtību iestatīšana
---------------------

Iestatīt parakstītāji dokumentiem, kurus uzņēmums izdrukā, izmantojiet **ierēdņu** lapā. Parakstītāji un to nosaukumi var uzstādīt gan par uzņēmuma debitorus vai kreditorus, atkarībā no dokumenta tipa. Sekojošajā tabulā ir aprakstītas cilnes uz **ierēdņu** lapā.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Cilne</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vispārējs</td>
<td>Pievienotu pozīcijām un saistīto informāciju par parakstītāju (direktors un galvenais grāmatvedis) kas var parakstīt visu veidu dokumentu drukāšanu.</td>
</tr>
<tr class="even">
<td>Virsgrāmata</td>
<td>Pievienot pozīciju un saistīto informāciju par parakstītāju, kurš var parakstīt šādu iekšējo finanšu dokumentus, kas ir saistīti naudas plūsma:
<ul>
<li>Kases orderi</li>
<li>Avansa pārskats</li>
<li>Kases grāmatas lapa</li>
<li>Inventarizācijas akts</li>
<li>Atlikto maksājumu *</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pārdošanas pasūtījumi</td>
<td>Pievienojiet parakstītāju, kurš var parakstīt šādu izejošo primāro dokumentus, kas saistīti ar debitoriem pozīcijas un saistītu informāciju:
<ul>
<li>Rēķinu apmaksas *</li>
<li>Rēķins</li>
<li>Faktūrrēķina *</li>
<li>Rēķins — kredīta nota</li>
<li>Faktūrrēķins - kredīts-Piezīme *</li>
<li>Nodokļu darbības faktūrrēķins (klienta) *</li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkšanas pasūtījumi</td>
<td>Pievienojiet pozīcijas un saistītu informāciju par parakstītāju, kurš var parakstīt šādu ienākošo primāro dokumentus, kas saistīti ar kreditoriem:
<ul>
<li>Rēķins</li>
<li>Faktūrrēķina *</li>
<li>Rēķins — kredīta nota</li>
<li>Faktūrrēķins - kredīts-Piezīme *</li>
<li>Rēķinu apmaksas *</li>
<li>Nodokļu darbības faktūrrēķins (kreditora) *</li>
</ul></td>
</tr>
<tr class="odd">
<td>Krājumu pārvaldība</td>
<td>Pievienojiet parakstītāju, kurš var parakstīt šādu noliktavas dokumenti, kad materiālie aktīvi ir izsniegusi klientam vai saņēmis no piegādātāja pozīcijas un saistītu informāciju:
<ul>
<li>Izdot pavadzīmi pārdošanas pasūtījumā (M-15) *</li>
<li>RMB. slīdēšanas/saņemšanas kārtībā</li>
<li>Izdot slīdēšanas pārsūtīšanas pasūtījumam (M-15) *</li>
</ul></td>
</tr>
</tbody>
</table>

\*Šī tipa dokuments ir pieejams tikai juridiskas personas, kas ir viņu primāro adresi Krievijā. Sekojošajā tabulā ir aprakstītas laukus uz **ierēdņu** lapā.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pozīcija</td>
<td>Atlasiet parakstītāja amata nosaukumu.</td>
</tr>
<tr class="even">
<td>Vārds, uzvārds</td>
<td>Atlasiet parakstītāja vārdu. Vārdu sarakstu, kas nāk no kontaktpersonu tabulas vai tabulas Employees, atkarībā no parakstītāja (tas ir, atkarībā no tā, vai <strong>mūsu</strong> ir atzīmēta izvēles rūtiņa). Ja parakstītāja vārds nav sarakstā, manuāli ievadīt parakstītāja vārdu un uzvārdu.</td>
</tr>
<tr class="odd">
<td>Amats</td>
<td>Atlasiet parakstītāja amats. Ja sarakstā nav parakstītāja nosaukums, manuāli ievadīt parakstītāja nosaukums.</td>
</tr>
<tr class="even">
<td>Konta kods</td>
<td>Atlasiet, vai parakstītājam var parakstīt visas atlasītā dokumentu tipa dokumenti vai tikai dokumenti noteiktam debitoram vai kreditoram.</td>
</tr>
<tr class="odd">
<td>Kontu saistība</td>
<td>Atlasiet debitora vai kreditora kontu, kas saistīts ar izvēlēto konta kods. Šis lauks ir pieejams, tikai atlasot <strong>ierakstu</strong>, <strong>konta kods</strong> lauks.</td>
</tr>
<tr class="even">
<td>Mūsu</td>
<td>Ir atzīmēta izvēles rūtiņa norāda, ka iekšējo stāvokli.</td>
</tr>
<tr class="odd">
<td>Saistība ar noliktavu</td>
<td>Atlasiet, vai parakstītājs ir piešķirts visām noliktavām vai tikai konkrētai noliktavai. Pieejamas šādas opcijas
<ul>
<li><strong>Visas</strong> -parakstītājs tiek piešķirts uz visām noliktavām.</li>
<li><strong>Ieraksts</strong> -parakstītājam ir piešķirts konkrētai noliktavai.</li>
</ul></td>
</tr>
<tr class="even">
<td>Noliktava</td>
<td>Atlasiet noliktavas kodu, kas atbilst uz noliktavu, kas katram parakstītājam ir piešķirta. Šis lauks ir pieejams, tikai atlasot <strong>ierakstu</strong>, <strong>sasaisti ar noliktavu</strong> lauks.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Iestatiet numuru sērijas kodu, ierēdņu
Numuru sērijas kodu var piešķirt ierēdņu **numuru sērijas** sadaļā **juridiskajām personām** lapā. Atlasiet numuru sērijas kodu **amatpersonu sesijas ID** atsauci.

## <a name="modify-signers-in-primary-documents"></a>Mainīt primāro dokumentu parakstītāji
Amatpersonu funkcionalitāti rāda iepriekš definētu noklusējuma parakstītāji no amatpersonu galda. Par **rēķina grāmatošanas** lapa par **amatpersonas** tab, var modificēt parakstītāja vārds un amats uz primārais dokuments attiecas uz šādiem dokumentu veidiem:

-   Rēķins debitoram
-   Kreditora rēķins
-   Nosūtīšanas pārsūtīšanas pasūtījums
-   Kases orderis

**Piezīme:** pēc tam, kad dokuments ir iegrāmatots, ierēdņi nevar rediģēt.


