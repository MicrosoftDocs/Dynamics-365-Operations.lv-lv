---
title: "Iestatīt parakstītājus drukātajām formām"
description: "Juridiskajām personām Čehijā, Igaunijā, Ungārijā, Lietuvā, Latvijā, Polijā un Krievijā varat iestatīt parakstītājus un amatus debitoriem un kreditoriem, kas drukā tādus dokumentus kā rēķini un kases orderi."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 263464
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 51449f2f8448a493ebf7e4496cebdb90d902869a
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-signers-for-print-forms"></a>Iestatīt parakstītājus drukātajām formām

[!include [banner](../includes/banner.md)]

Juridiskajām personām Čehijā, Igaunijā, Ungārijā, Lietuvā, Latvijā, Polijā un Krievijā varat iestatīt parakstītājus un amatus debitoriem un kreditoriem, kas drukā tādus dokumentus kā rēķini un kases orderi.

<a name="set-up-default-values"></a>Noklusēto vērtību iestatīšana
---------------------

Lai iestatītu parakstītājus tādiem dokumentiem, ko uzņēmums drukā, izmantojiet lapu **Amatpersonas**. Parakstītājus un viņu amatos varat iestatīt gan uzņēmumam, gan debitoriem vai kreditoriem, ņemot vērā dokumenta tipu. Nākamajā tabulā ir aprakstītas cilnes lapā **Amatpersonas**.

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
<td>Vispārīgi</td>
<td>Pievienojiet amatus un saistīto informāciju par parakstītājiem (Direktors un Galvenais grāmatvedis), kuri var parakstīt visu tipu drukātos dokumentus.</td>
</tr>
<tr class="even">
<td>Virsgrāmata</td>
<td>Pievienojiet amatu un saistīto informāciju par parakstītājiem, kuri var parakstīt tālāk norādītos iekšējos finanšu dokumentus, kas ir saistīti ar naudas plūsmu.
<ul>
<li>Kases orderi</li>
<li>Avansa pārskats</li>
<li>Kases grāmatas lapa</li>
<li>Inventarizācijas akts</li>
<li>Atliktie maksājumi<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Pārdošanas pasūtījumi</td>
<td>Pievienojiet amatus un saistīto informāciju par parakstītājiem, kuri var parakstīt tālāk norādītos izejošos primāros dokumentus, kas ir saistīti ar debitoriem.
<ul>
<li>Apmaksājams rēķins</em></li>
<li>Rēķins</li>
<li>Faktūrrēķins<em></li>
<li>Rēķins — kredīta nota</li>
<li>Faktūrrēķins — kredīta nota</em></li>
<li>Nodokļu darbības faktūrrēķins (debitors)<em></li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkšanas pasūtījumi</td>
<td>Pievienojiet amatus un saistīto informāciju par parakstītājiem, kuri var parakstīt tālāk norādītos ienākošos primāros dokumentus, kas ir saistīti ar kreditoriem.
<ul>
<li>Rēķins</li>
<li>Faktūrrēķins</em></li>
<li>Rēķins — kredīta nota</li>
<li>Faktūrrēķins — kredīta nota<em></li>
<li>Apmaksājams rēķins</em></li>
<li>Nodokļu darbības faktūrrēķins (kreditors)<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Krājumu pārvaldība</td>
<td>Pievienojiet amatus un saistīto informāciju par parakstītājiem, kuri var parakstīt tālāk norādītos noliktavas dokumentus, kad materiāli aktīvi tiek izsniegti debitoram vai saņemti no kreditora.
<ul>
<li>Pārdošanas pasūtījuma izsniegšanas pavadzīme (M-15)</em></li>
<li>Ieņēmumu orderis/pieņemšanas akts</li>
<li>Pārsūtīšanas pasūtījuma izsniegšanas pavadzīme (M-15)*</li>
</ul></td>
</tr>
</tbody>
</table>

\* Šis dokumenta tips ir pieejams tikai juridiskām personām, kuru primārā adrese ir Krievijā. Nākamajā tabulā ir aprakstīti lauki lapā **Amatpersonas**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Amats</td>
<td>Atlasiet parakstītāja amata nosaukumu.</td>
</tr>
<tr class="even">
<td>Vārds, uzvārds</td>
<td>Atlasiet parakstītāja vārdu un uzvārdu. Sarakstā esošie vārdi tiek ņemti no tabulas Kontaktpersonas vai tabulas Darbinieki, ņemot vērā parakstītāja tipu (tas ir, atkarībā no tā, vai ir atzīmēta izvēles rūtiņa <strong>Mūsu</strong>). Ja parakstītāja vārds nav iekļauts šajā sarakstā, ievadiet parakstītāja pilno vārdu manuāli.</td>
</tr>
<tr class="odd">
<td>Amata nosaukums</td>
<td>Atlasiet parakstītāja darba nosaukumu. Ja parakstītāja amats nav iekļauts šajā sarakstā, ievadiet parakstītāja amatu manuāli.</td>
</tr>
<tr class="even">
<td>Konta kods</td>
<td>Atlasiet, vai parakstītājs var parakstīt visus atlasītā dokumentu tipa dokumentus vai tikai dokumentus kādam konkrētam debitoram vai kreditoram.</td>
</tr>
<tr class="odd">
<td>Kontu saistība</td>
<td>Atlasiet debitora vai kreditora kontu, kurš ir saistīts ar atlasīto konta kodu. Šis lauks ir pieejams tikai tad, ja laukā <strong>Konta kods</strong> atlasāt <strong>Ieraksts</strong>.</td>
</tr>
<tr class="even">
<td>Mūsu</td>
<td>Ja izvēles rūtiņa ir atzīmēta, tas nozīmē, ka šis amats ir iekšējs.</td>
</tr>
<tr class="odd">
<td>Saistība ar noliktavu</td>
<td>Atlasiet, vai parakstītājs ir piešķirts visām noliktavām vai tikai konkrētai noliktavai. Pieejamas šādas opcijas
<ul>
<li><strong>Visi</strong> — parakstītājs ir piešķirts visām noliktavām.</li>
<li><strong>Ieraksts</strong> — parakstītājs ir piešķirts konkrētai noliktavai.</li>
</ul></td>
</tr>
<tr class="even">
<td>Noliktava</td>
<td>Atlasiet noliktavas kodu, kas atbilst tai noliktavai, kurai šis parakstītājs ir piešķirts. Šis lauks ir pieejams tikai tad, ja laukā <strong>Saistība ar noliktavu</strong> atlasāt <strong>Ieraksts</strong>.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Iestatīt numuru sēriju kodu amatpersonām
Lapas **Juridiskās personas** sadaļā **Numuru sērijas** amatpersonām varat piešķirt numuru sērijas kodu. Atsaucei **Amatpersonu sesijas ID** atlasiet kādu numuru sērijas kodu.

## <a name="modify-signers-in-primary-documents"></a>Modificēt parakstītājus primārajos dokumentos
Funkcionalitāte Amatpersonas rāda noklusējuma sākotnēji definētos parakstītājus no tabulas Amatpersonas. Lapas **Rēķina grāmatošana** cilnē **Amatpersonas** varat modificēt parakstītāja vārdu un amatu primārajā dokumentā tālāk uzskaitītajiem dokumentu tipiem.

-   Rēķins debitoram
-   Kreditora rēķins
-   Nosūtīšanas pārsūtīšanas pasūtījums
-   Kases orderis

**Piezīme.** Pēc dokumenta grāmatošanas amatpersonas vairs nevar rediģēt.




