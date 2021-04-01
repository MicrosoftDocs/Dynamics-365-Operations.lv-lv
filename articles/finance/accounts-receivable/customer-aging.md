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
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 384e44ef07771a174aaed4f8fb893e75b0206da7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236990"
---
# <a name="customer-aging-report"></a>Debitoru vecumstruktūra 

Pārskats **Debitoru vecumstruktūras** parāda debitoru apmaksājamās bilances, sakārtotas pēc datuma intervāla vai vecumstruktūras perioda.

Veidojot šo pārskatu, tiek rādīti tālāk norādītie noklusējuma parametri. Izmantojot šos parametrus, varat filtrēt pārskatā ietveramos datus. Papildinformācijai skatiet [Iestatīt iekasēšanu](set-up-collections.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Lauks</p></th>
<th><p>Apraksts</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Rēķinu klasificēšana</strong></p></td>
<td><p>Atlasiet vienu vai vairākas rēķinu klasifikācijas, ko iekļaut pārskatā.</p>
<div class="alert">

**Piezīme:** šī vadīkla ir pieejama tikai tad, ja ir atlasīta konfigurācijas atslēga <STRONG>Publiskais sektors</STRONG>.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Ietvert transakcijas bez rēķinu klasificēšanas grupas</strong></p></td>
<td><p>Ja šī izvēles rūtiņa ir atzīmēta, pārskatā tiks parādīti visi darījumi, kam nav piešķirta rēķinu klasifikācija.</p>
<div class="alert">

**Piezīme:** šī vadīkla ir pieejama tikai tad, ja ir atlasīta konfigurācijas atslēga <STRONG>Publiskais sektors</STRONG>.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Vecumstruktūras no</strong></p></td>
<td><p>Ievadiet datumu, kas izmantots pašreizējam vecumstruktūras intervālam.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bilance uz</strong></p></td>
<td><p>Ievadiet datumu, kuram skatīt debitoru bilances. To sauc arī par darījumu beigu datumu.</p></td>
</tr>
<tr class="even">
<td><p><strong>Sākuma datums</strong></p></td>
<td><p>Ievadiet pārskatā iekļaujamo datumu, kas atrodas pirmā perioda intervālā vai vecumstruktūras periodā.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Kritēriji</strong></p></td>
<td><p>Atlasiet datuma veidu, uz kā balstīt šo pārskatu.</p>
<ul>
<li><p><strong>Darījuma datums</strong> – darījumu grāmatošanas datums. Piemēram, tas var būt rēķina datums, kas ir izpildes datuma aprēķina pamats.</p></li>
<li><p><strong>Izpildes datums</strong> – darījumu izpildes datums, kas balstīts uz maksāšanas nosacījumiem.</p></li>
<li><p><strong>Dokumenta datums</strong> – lietotāja definēts dokumenta datums, kas ir izpildes datuma aprēķina pamats.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Vecumstruktūras perioda definīcija</strong></p></td>
<td><p>Atlasiet vecumstruktūras perioda definīciju. Lauks <strong>Intervāls</strong> netiek izmantots, atlasot vecumstruktūras perioda definīciju.</p>
<p>Vecumstruktūras perioda definīcijas, kurām ir vairāk nekā seši vecumstruktūras periodi, drukātā pārskatā nevar izmantot.</p>
<div class="alert">

**Piezīme:** vecumstruktūras periodus var iestatīt lapā <STRONG>Vecumstruktūras perioda definīcijas</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Drukāt vecumstruktūras perioda aprakstu</strong></p></td>
<td><p>Atlasiet <strong>Jā</strong>, lai pārskatā iekļautu vecumstruktūras periodu aprakstus katras vecumstruktūras perioda kolonnas galvenē. Atlasiet <strong>Nē</strong>, lai drukātu pārskatu bez kolonnu galvenēm.</p></td>
</tr>
<tr class="even">
<td><p><strong>Intervāls</strong></p></td>
<td><p>Definējiet izmantojamo periodu, ievadot dienas vai mēneša vienību skaitu katrā periodā. Piemēram, lai skatītu vecumstruktūras informāciju pa nedēļām, ievadiet 7 šajā laukā un atlasiet <strong>Diena</strong> laukā <strong>Diena/Mēnesis</strong>.</p>
<div class="alert">

**Piezīme:** šajā laukā ievadītā informācija tiek izmantota tikai tad, ja nav atlasīta vecumstruktūras perioda definīcija. Pretējā gadījumā drukas virziens tiek definēts vecumstruktūras perioda definīcijā.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Diena/Mēnesis</strong></p></td>
<td><p>Atlasiet vienību <strong>Diena</strong> vai <strong>Mēnesis</strong>, ko izmanto, lai definētu periodu laukā <strong>Intervāls</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Drukas virziens</strong></p></td>
<td><p>Atlasiet, vai aprēķināt bilances un drukāt vecumstruktūras pārskatu par pagājušajiem vai nākamajiem periodiem. Datumi tiek novērtēti attiecībā pret datumu, kas atlasīts laukā <strong>Bilance uz</strong>. Atlasiet <strong>Atpakaļ</strong>, lai parādītu informāciju par pagājušajiem periodiem. Atlasiet <strong>Uz priekšu</strong>, lai parādītu informāciju par nākamajiem periodiem.</p>
<div class="alert">
  
<STRONG>Piezīme:</STRONG> šajā laukā ievadītā informācija tiek izmantota tikai tad, ja nav atlasīta vecumstruktūras perioda definīcija.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Detalizēti</strong></p></td>
<td><p>Atlasiet, lai uzskaitītu darījumus, kas ir iekļauti pārskatā redzamajās bilancēs.</p></td>
</tr>
<tr class="even">
<td><p><strong>Iekļaut summas darījuma valūtā</strong></p></td>
<td><p>Atlasiet, lai iekļautu summas darījuma valūtā papildus summām uzskaites valūtā. Ja šī izvēles rūtiņa nav atzīmēta, pārskata summas tiek parādītas tikai uzskaites valūtā.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Negatīva bilance</strong></p></td>
<td><p>Atlasiet, lai ietvertu debitoru kontus ar negatīvām bilancēm.</p></td>
</tr>
<tr class="even">
<td><p><strong>Neiekļaut nulles bilances kontus</strong></p></td>
<td><p>Atlasiet, lai neiekļautu debitoru kontus ar nulles bilancēm.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Maksājumu pozicionēšana</strong></p></td>
<td><p>Atlasiet, lai parādītu nenokārtotos maksājumus. Tie tiek parādīti pārskata pirmajā kolonnā.</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]