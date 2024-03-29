---
title: Noklusējuma korespondējošie konti kreditoru rēķinam un rēķinu apstiprinājumu žurnāliem
description: Šis raksts palīdzēs izlemt, kur rēķinu žurnāliem jāpiešķir noklusējuma konti.
author: abruer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.form: LedgerJournalTable
ms.openlocfilehash: ed75e0a3b9994d061e94d07ffcc43e3b73bec55e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281678"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a>Noklusējuma korespondējošie konti kreditoru rēķinam un rēķinu apstiprinājumu žurnāliem

[!include [banner](../includes/banner.md)]

Noklusējuma korespondējošie konti tiek izmantoti tālāk norādītajās kreditoru rēķinu žurnālu lapās.

-   Rēķinu žurnāls
-   Rēķinu apstiprināšanas žurnāls

Izmantojiet tālāk esošo tabulu, lai izlemtu, kur ir jāpiešķir rēķinu žurnālu noklusējuma konti.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Noklusējuma kontu iestatīšanas vieta</th>
<th>Noklusējuma kontu nodrošināšanas vieta</th>
<th>Šīs opcijas ietekme uz apstrādi</th>
<th>Šis opcijas izmantošanas gadījumi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Kreditoru grupa</strong> — iestatiet kreditoru grupu noklusējuma korespondējošos kontus lapā <strong>Noklusētie konta iestatījumi</strong>, ko varat atvērt lapā <strong>Kreditoru grupas</strong>.</td>
<td><ul>
<li>Kreditora konts</li>
<li>Kreditoru kontu žurnāla ieraksti kreditoru grupā, ja kreditoru kontiem nav norādīti noklusējuma konti</li>
</ul></td>
<td>Kreditoru grupu noklusējuma korespondējošie konti tiek rādītas kā kreditoru noklusējuma korespondējošie konti lapā <strong>Noklusētie konta iestatījumi</strong>. Šo lapu varat atvērt saraksta lapā <strong>Visi kreditori</strong>.</td>
<td>Izmantojiet šo opciju, ja parasti maksājat par viena veida precēm, ko nodrošina vienas un tās pašas kreditoru grupas.</td>
</tr>
<tr class="even">
<td><strong>Kreditora konts</strong> — iestatiet kreditoru kontu noklusējuma kontus lapā <strong>Noklusētie konta iestatījumi</strong>, ko varat atvērt lapā <strong>Kreditori</strong>.</td>
<td>Kreditoru konta žurnāla ieraksti</td>
<td>Kreditoru noklusējuma korespondējošie konti tiek rādīti kā kreditora konta žurnāla ierakstu noklusējuma korespondējošie konti.</td>
<td>Izmantojiet šo opciju, ja parasti maksājat par viena veida precēm, ko nodrošina vieni un tie paši kreditori.</td>
</tr>
<tr class="odd">
<td><strong>Žurnālu nosaukumi</strong> — iestatiet žurnālu noklusējuma korespondējošos kontus lapā <strong>Žurnālu nosaukumi</strong>. Atlasiet opciju <strong>Fiksēts korespondējošais konts</strong>. Ņemiet vērā, ka nevara&#39;t norādīt žurnālu nosaukumu noklusējuma korespondējošos kontus, ja žurnālu nosaukumiem atbilstošais žurnāla veids ir <strong>Rēķinu reģistrs</strong> vai <strong>Apstiprinājums</strong>.</td>
<td><ul>
<li>Žurnāla virsraksts, kurā tiek izmantots žurnāla nosaukums</li>
<li>Žurnāla ieraksti žurnālos, kuros tiek lietots žurnāla nosaukums</li>
</ul></td>
<td>Ja lapā <strong>Žurnālu nosaukumi</strong> ir atlasīta opcija <strong>Fiksēts korespondējošais konts</strong>, žurnāla nosaukuma noklusējuma korespondējošais konts tiek izmantots kreditora vai kreditoru grupas noklusējuma korespondējošā konta vieta.</td>
<td>Izmantojiet šo opciju, lai iestatītu žurnālus noteiktām maksām vai izdevumiem, kas tiek iekasēti no konkrētiem kontiem neatkarīgi no kreditora vai kreditoru grupas, kurā ir ietverts kreditors.</td>
</tr>
<tr class="even">
<td><strong>Žurnālu nosaukumi</strong> — iestatiet žurnālu noklusējuma korespondējošos kontus lapā <strong>Žurnālu nosaukumi</strong>. Noņemiet atzīmi no opcijas <strong>Fiksēts korespondējošais konts</strong>. Ņemiet vērā, ka nevara&#39;t norādīt žurnālu nosaukumu noklusējuma korespondējošos kontus, ja žurnālu nosaukumiem atbilstošais žurnāla veids ir <strong>Rēķinu reģistrs</strong> vai <strong>Apstiprinājums</strong>.</td>
<td><ul>
<li>Žurnāla virsraksts</li>
<li>Žurnāla ieraksti žurnālos, kuros tiek lietots žurnāla nosaukums</li>
</ul></td>
<td>Šie noklusējuma ierakstu tiek izmantoti žurnālu virsrakstu lapās, un žurnāla virsraksta lapā norādītais korespondējošais konts tiek izmantots kā noklusējuma ieraksts žurnālu dokumentu lapās. Lapā <strong>Žurnālu nosaukumi </strong>norādītie noklusējuma konti tiek izmantoti tikai tad, ja nav iestatīti kreditora konta noklusējuma konti.</td>
<td>Izmantojiet šo opciju, lai iestatītu noklusējuma kontus, kas tiek izmatoti tad, ja nav&#39;piešķirts kreditora noklusējuma korespondējošais konts.</td>
</tr>
<tr class="odd">
<td><strong>Žurnāla virsraksts</strong> — iestatiet žurnāla noklusējuma korespondējošo kontu, kas tiks izmantots kā noklusējuma ieraksts žurnālu dokumentu lapās. Ņemiet vērā, ka nevara&#39;t norādīt žurnāla virsraksta noklusējuma korespondējošos kontus, ja žurnālu nosaukumiem atbilstošais žurnāla veids ir <strong>Rēķinu reģistrs</strong> vai <strong>Apstiprinājums</strong>.</td>
<td>Žurnāla ieraksti žurnālā</td>
<td>Žurnāla noklusējuma korespondējošais konts tiek izmantots kā noklusējuma ieraksts žurnālu dokumentu lapās.</td>
<td>Izmantojiet šo opciju, lai paātrinātu datu ievadi, ja vairumā žurnāla ierakstu tiek izmantots viens un tas pats korespondējošais konts.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
