---
title: "Masveida darbā pieņemšanas projekti"
description: "Masveida darbā pieņemšanas projekti ļauj personāla vadības speciālistiem izveidot vairākus amatus un efektīvi pieņemt uz šiem amatiem darbā darbiniekus."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e98e6b3baf57302804d9171833f2b48b60355b22
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="mass-hire-projects"></a>Masveida darbā pieņemšanas projekti

[!include [banner](../includes/banner.md)]

Masveida darbā pieņemšanas projekti ļauj personāla vadības speciālistiem izveidot vairākus amatus un efektīvi pieņemt uz šiem amatiem darbā darbiniekus.

<a name="overview"></a>Pārskats
--------

Nolīgstot darbā vairākus darbiniekus uzreiz, piemēram, nolīgstat darbiniekus sezonas pieprasījuma nodrošināšanai, izmantojiet masveida pieņemšanas darbā projektus. Masveida pieņemšanas darbā projekta izveidošana ir noderīga, jo vienā reizē ļauj izveidot pozīciju ierakstus, darbinieku ierakstus un pozīcijām paredzētos darbinieku uzdevumus. Izveidojot masveida pieņemšanas darbā projekta pozīcijas, var norādīt tālāk minēto informāciju.
-   Izveidojamo pozīciju skaits
-   Darbā paredzētajās pozīcijas pieņemamo cilvēku darbinieka tips
-   Ar konkrētajām pozīcijām saistītā nodaļa un darbs
-   Pozīcijai atbilstošā pilnas slodzes ekvivalenta vērtība

## <a name="example"></a>Piemērs
Vasaras periodā parasti tiek pieņemti darbā 15–20 studenti uz nepilnu slodzi, kas jūsu uzņēmumā aizpilda prakses vietas. Šogad vēlaties pieņemt darbā piecus grāmatvežus, piecus pasūtījumu apstrādātājus un piecus kasierus. Jūs neveidojat katru pozīcijas un darbinieka ierakstu atsevišķi, bet izveidojat vienu masveida pieņemšanas darbā projektu ar nosaukumu “Vasaras praktikanti”. Projekta sākuma un beigu datumi atbilst masveida pieņemšanas darbā projektā izveidoto pozīciju pastāvēšanas perioda sākuma un beigu datumiem. 

Lapā **Masveida pieņemšanas darbā projekti** atlasiet projektu “Vasaras praktikanti” un pēc tam noklikšķiniet uz **Atvērt projektu**. Atvērtajā masveida pieņemšanas darbā projektā noklikšķiniet uz **Izveidot pozīcijas** un ievadiet informāciju par grāmatveža pozīciju. Varat norādīt, ka ir jāizveido piecas grāmatveža pozīcijas, katrai pozīcijai izmantojot vienādu informāciju, un pēc tam noklikšķiniet uz Labi. Atkārtojiet šo darbību, izveidojot pasūtījuma apstrādātāja un kasiera pozīciju. 

Kad studenti ir pieņemti darbā prakses pozīcijās, ievadiet studentu datus pozīcijas, kurā pieņemat viņus darbā, laukā **Pozīcijas dati**. Kad visi pozīcijas dati ir ievadīti, atlasiet pozīciju lapā Masu darbā pieņemšanas projekti un noklikšķiniet uz **Pieņemt darbā**. Katrai pozīcijai tiek izveidots pozīcijas ieraksts, kā arī tiek izveidots darbinieka ieraksts, kas tiek piešķirts katras darba pieņemtās personas attiecīgai pozīcijai.

## <a name="mass-hire-project-statuses"></a>Masveida pieņemšanas darbā projekta statusi
Masveida pieņemšanas darbā projektam var piešķirt tālāk norādītos statusus.
-   Izveidota
-   Atvērta
-   Slēgts

Lai mainītu masveida pieņemšanas darbā projekta statusu, lapā **Masveida pieņemšanas darbā projekts** noklikšķiniet uz **Atvērt projektu** vai **Slēgt projektu**. Sekojošajā tabulā ir aprakstīts, ko varat darīt ar projektu, vadoties pēc tā statusa.

<table>
<thead>
<tr class="header">
<th>Statuss</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izveidota</td>
<td>Jūs varat izveidot un labot informāciju, bet nevarat izveidot projekta pozīcijas. Šis ir noklusējuma statuss jauniem projektiem.</td>
</tr>
<tr class="even">
<td>Atvērta</td>
<td>Jūs varat mainīt projekta datus, izveidot masveida pieņemšanas darbā projekta pozīcijas un pieņemt darbā cilvēkus konkrētās pozīcijās. Šis ir statuss aktīvajiem projektiem.</td>
</tr>
<tr class="odd">
<td>Slēgts</td>
<td>Jūs nevarat pievienot projektā pozīcijas. Lai pievienotu masveida pieņemšanas darbā projektā pozīcijas, atveriet vēlreiz projektu. Šis ir statuss pabeigtiem projektiem.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Piezīme. </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pirms masveida pieņemšanas darbā projekta slēgšanas visām projekta pozīcijām jābūt piešķirtam statusam vai nu Izveidots, vai Slēgts.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>








