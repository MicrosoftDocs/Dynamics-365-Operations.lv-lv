---
title: Uzskaites sadales un žurnālu ieraksti brīva teksta rēķiniem
description: Uzskaites sadales tiek izmantotas, lai definētu, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīva teksta rēķinā. Katrai summai, kas ir jānorāda brīva teksta rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5120c4e75e821776201d5add2d498feb94d0297
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778416"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>Uzskaites sadales un apakšgrāmatas ieraksti brīva teksta rēķiniem

[!include [banner](../includes/banner.md)]

Uzskaites sadales tiek izmantotas, lai definētu, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīva teksta rēķinā. Katrai summai, kas ir jānorāda brīva teksta rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.

## <a name="accounting-distributions"></a>Uzskaites sadales

Jūs varat izmantot šādas pogas **brīvā teksta rēķina** lapā, lai skatītu un, iespējams, mainītu grāmatvedības sadalījumus katrai summai brīvā teksta rēķinā.

-   **Sadalīt summas**— skatiet un mainiet uzskaites sadales atsevišķai rindai un jebkurai apakšrindai, piemēram, nodokļiem vai izmaksām. Varat arī skatīt un mainīt pakārtotās rindas uzskaites sadalījumus tieši **lapā PVN transakcijas vai** lapā Maksas **transakcijas**.
    -   Mainiet brīva teksta rēķina galvenes summas, piemēram, izmaksas vai valūtas noapaļošanas summas.
    -   Mainiet brīva teksta rēķina rindas summas.
-   **Skatīt sadales**— skatiet visu dokumenta rindu uzskaites sadales. No šī skata uzskaites sadales nevar mainīt.
    -   Skatiet galveni un rindu summas.

## <a name="distributing-amounts"></a>Summu sadalīšana
Kad ievadāt brīva teksta rēķinu, katra summa tiek sadalīta tālāk aprakstītajā veidā.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Naudas summas tips</th>
<th>Kur tiek ņemts rādītais galvenais konts</th>
<th>Prioritāšu secība, kas nosaka, kuras noklusējuma finanšu dimensijas tiek parādītas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Brīvā teksta rēķina rinda</td>
<td>Virsgrāmatas konts brīva teksta rēķina rindā.</td>
<td><ol>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Ja galvenais konts nav sadalījuma konts, brīva teksta rēķina rindā izmantot finanšu dimensijas noklusējuma veidni.</li>
<li>Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no Virsgrāmatas konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Brīva teksta rēķina rinda pamatlīdzekļa numura un vērtības modeļa kombinācijai
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Piezīme</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Galvenais konts brīvā teksta rēķina rindā būs pamatlīdzekļu izslēgšanas konts.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Virsgrāmatas konts brīva teksta rēķina rindā.</td>
<td><ol>
<li>Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no Virsgrāmatas konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Brīva teksta rēķina atlaides summa</td>
<td>Lauks Debitoru atlaižu galvenais konts lapā Termiņatlaides.</td>
<td><ol>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Ja galvenais konts nav sadalījuma konts, brīva teksta rēķina rindā izmantot finanšu dimensijas noklusējuma veidni.</li>
<li>Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no Virsgrāmatas konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Brīva teksta rēķina pārdošanas nodokļa summa</td>
<td>Lauks Maksājamais PVN lapā Grāmatošanas grupas Virsgrāmatā.</td>
<td><ol>
<li>Izmantot finanšu dimensijas, kas ir definētas brīva teksta rēķina rindas summai, vai sadales maksa rindas summai.</li>
<li>Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no Virsgrāmatas konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Brīva teksta rēķina maksas rindas summa</td>
<td>Lauks Kredīta konts lapā Maksas kods.</td>
<td><ol>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Ja galvenais konts nav sadalījuma konts, brīva teksta rēķina rindā izmantot finanšu dimensijas noklusējuma veidni.</li>
<li>Brīva teksta rēķina rindā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no Virsgrāmatas konta lapā Kontu plāns.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Nodokļu sadalīšana
Nodokļu uzskaites sadales var izveidot tikai pēc nodokļu aprēķināšanas. Lai aprēķinātu tirdzniecības nodokļus, lapā Brīvs **teksts ir** jāizpilda viens no šiem uzdevumiem:
-   Apskatiet PVN.
-   Apskatiet rēķina kopsummu.
-   Apskatiet skaidras naudas plūsmu.
-   Apskatiet uzskaites sadales visam brīva teksta rēķinam.
-   Apskatiet apakšgrāmatas žurnālu.

## <a name="subledger-journals-for-free-text-invoices"></a>Apakšgrāmatas žurnāli brīva teksta rēķiniem
Pirms grāmatojat brīva teksta rēķinu, varat apskatīt pilnu uzskaites ierakstu šim rēķinam, kas ietver debetu un kredītu, lai pārliecinātos, ka rēķins tiek grāmatots pareizajos kontos. Šis pilnās uzskaites ieraksta skats tiek saukts par apakšgrāmatas žurnālu. Ja pirms brīva teksta rēķina reģistrēšanas žurnālā priekšskatāt apakšgrāmatas žurnāla ierakstu un tas ir nepareizs, šo apakšgrāmatas žurnāla ierakstu nevar mainīt. Tā vietā ir jāmaina uzskaites sadales vai grāmatošanas metode. Uzskaites sadales tiek izmantotas, lai noteiktu uzskaites ieraksta vienu pusi, debetu vai kredītu. Korespondējošais apakšgrāmatas žurnāla konta ieraksts tiek izveidots no grāmatošanas metodēm, piemēram, no debitora konta vai nodokļiem.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
