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
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 86b527b72ef0c9af71e70fe280bcdfe3992a36b1
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="report-definitions-in-financial-report-designer"></a>Atskaišu definīcijas finanšu atskaišu veidotājā

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par atskaišu definīcijām. Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti. Atskaites definīcija arī sniedz opcijas un iestatījumus, kas noder atskaites pielāgošanai. 

Atskaites definīcija ir atskaites komponents (jeb veidošanas bloks), kas izmanto rindas definīciju, kolonnas definīciju un papildu atskaišu koka definīciju, lai izveidotu atskaiti. Pārskata definīcija nodrošina arī opcijas un iestatījumus, ko varat izmantot, lai pielāgotu pārskatu. Pēc tam, kad jūs nosakiet rindu definīcijas un kolonnu definīcijas, tās nedrīkst kombinēt pārskata definīcijā. Šajā brīdī jūs definējat arī citus definīcijas aspektus, piemēram detalizācijas līmeni un pārskata datumu. Tad varat saglabāt un izveidot atskaiti. Finanšu atskaišu veidošana piedāvā šādus detalizētības līmeņus:

-   Finanšu
-   Finanšu un konta
-   Finanšu, konta un darbības

Tomēr, atkarībā no tā, kā dati tiek saglabāti Microsoft Dynamics ERP sistēmā, darbības detaļas var nebūt pieejamas pārskatos.

## <a name="create-a-report-definition"></a>Izveidojiet pārskata definīciju
1.  Pārskatu veidotājā izvēlnē **Fails**, noklikšķiniet uz **Jauns**, un pēc tam atlasiet **Pārskata definīcija**.
2.  Norādiet atbilstošu informāciju cilnēs **Pārskats**, **Izvade un sadale**, **Galvenes un kājenes** un **Iestatījumi**.

## <a name="contents-of-a-report-definition"></a>Pārskata definīcijas saturs
Šajā tabulā ir aprakstītas pārskata definīcijas cilnes un tas, kā tiek izmantota informācija.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Cilne</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pārskats</td>
<td>Izveidojiet pārskatu, konfigurējiet pārskatu vai modificējiet esošu pārskatu.</td>
</tr>
<tr class="even">
<td>Izvade un sadale</td>
<td>Mainiet izvades tipu un pārskata adresātu.</td>
</tr>
<tr class="odd">
<td>Galvenes un kājenes</td>
<td>Definējiet un formatējiet galvenes un kājenes pārskatam. Piemēram, jūs varat pievienot tekstu vai attēlus galvenē vai kājenē. Finanšu atskaišu veidošana atbalsta .bmp, .jpg un .png failus attēliem. Jūs varat arī pievienot automātiskā teksta kodus, lai ievietotu citu informāciju, piemēram, uzņēmuma nosaukumu, pārskata nosaukumu vai lappuses numuru.</td>
</tr>
<tr class="even">
<td>Iestatījumi</td>
<td>Norādiet pārskata definīcijas iestatījumus, piemēram, šādus iestatījumus:
<ul>
<li>Formatēšanas un noapaļošanas summas</li>
<li>Detalizētu pārskatu formatēšana</li>
<li>Pārskata veidošanas koka formatēšana</li>
<li>Ģenerēt izņēmumu pārskatu</li>
<li>Norādīt valūtas konvertēšanu</li>
<li>Apakšsumma un filtra konta detalizēta informācija</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Skatiet arī
--------

[Finanšu pārskati](financial-reporting-intro.md)



