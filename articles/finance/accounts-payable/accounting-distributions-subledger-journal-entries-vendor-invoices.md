---
title: Uzskaites sadales un žurnālu ieraksti kreditoru rēķiniem
description: Uzskaites sadales tiek izmantotas, lai definētu veidu, kā summa tiek uzskaitīta, piemēram, kā izdevumi, nodokļi vai izmaksas tiek uzskaitīti kreditora rēķinā. Katrai summai, kas ir jānorāda kreditora rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0ad3124963dda33f44cf8ba6e6bb466029b2651
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252197"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Uzskaites sadales un žurnālu ieraksti kreditoru rēķiniem

[!include [banner](../includes/banner.md)]

Uzskaites sadales tiek izmantotas, lai definētu veidu, kā summa tiek uzskaitīta, piemēram, kā izdevumi, nodokļi vai izmaksas tiek uzskaitīti kreditora rēķinā. Katrai summai, kas ir jānorāda kreditora rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales. 

<a name="accounting-distributions"></a>Uzskaites sadales 
-------------------------

Lapā Kreditora rēķins varat izmantot tālāk norādītās pogas, lai skatītu un, iespējams, modificētu katras kreditora rēķinā ietvertās summas uzskaites sadales.
-   **Sadales summas** — skatiet un mainiet uzskaites sadales atsevišķai rindai un jebkurai apakšrindai, piemēram, nodokļiem un izmaksām. Apakšrindas uzskaites sadales varat arī skatīt un modificēt tieši lapā PVN darbības vai Maksu darbības.
    -   Mainiet kreditora rēķina galvenes summas, piemēram, izmaksas vai valūtas noapaļošanas summas.
    -   Modificējiet kreditora rēķina rindu summas.
-   **Skatīt sadales** — skatiet visu dokumenta rindu uzskaites sadales. No šī skata uzskaites sadales nevar modificēt.
    -   Skatiet galveni un rindu summas.

Ja kreditora rēķinā ir atsauces uz pirkšanas pasūtījumu, uzskaites sadales varat sadalīt un modificēt tām rindām, kas ietver uzkrāto krājumu. Ja kreditora rēķina rindā nav atsauces uz pirkšanas pasūtījuma rindu, uzskaites sadali varat arī dzēst. Nevar sadalīt vai dzēst maksu, nodokļu un rindas atlaižu rindas. Jūs varat modificēt virsgrāmatas kontu, bet nav iespējams mainīt summas vai procentus.
> [!NOTE]                                                                                                                                 
> Ja pamatrinda satur krājumu, kas netiek uzkrāts, un uzskaites sadales ir sadalītas, apakšrinda tiek sadalīta automātiski, lai atbilstu pamatrindas finanšu dimensijām. Apakšrindas uzskaites sadales nevar papildus sadalīt vai dzēst, bet atkarībā no apakšrindas iestatījumiem, iespējams, varat mainīt virsgrāmatas kontu apakšrindas uzskaites sadalē.

## <a name="distributing-amounts"></a>Summu sadalīšana
Ievadot kreditora rēķinu, katra summa tiek sadalīta tālāk aprakstītajā veidā.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Kreditora rēķina rindas tips</th>
<th>Prioritāšu secība, kas nosaka, no kāda avota tiek parādīts galvenais konts</th>
<th>Prioritāšu secība, kas nosaka, kuras noklusējuma finanšu dimensijas tiek parādītas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Uzkrātā prece</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai.</li>
<li>Lauks Galvenais konts, kad lapā Grāmatošana ir atlasīta opcija Produkta pirkšanas izdevumi.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Kreditora rēķinā izmantot noklusējuma finanšu dimensiju vērtības.</li>
</ol></td>
</tr>
<tr class="even">
<td>Sagādes kategorija vai prece, kas netiek uzkrāta</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja kreditora rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Lauks Galvenais konts, kad lapā Grāmatošana ir atlasīta opcija Pirkšanas tēriņi izdevumu sadaļai.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Kreditora rēķinā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Pamatlīdzeklis</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja kreditora rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Ja veidlapā Kreditora rēķins ir atlasīta lauka Darījuma veids vērtība Iegāde, tad lauks Galvenais konts, kad lapā Pamatlīdzekļu grāmatošanas metodes ir atlasīta opcija Iegāde.</li>
<li>Ja veidlapā Kreditora rēķins ir atlasīta lauka Darījuma veids vērtība Kapitālās izmaksas, tad lauks Galvenais konts, kad lapā Pamatlīdzekļu grāmatošanas metodes ir atlasīta opcija Kapitālās izmaksas.</li>
</ol></td>
<td><ol>
<li>Izmantot konta sadali pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kreditora rēķina rindā noteikts projekts</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Ja lapā Projektu grupas ir atlasīta lauka Izmaksu grāmatošana — krājumi vērtība Bilance, tad lauks Galvenais konts, kad lapā Grāmatošanas iestatījumi virsgrāmatā ir atlasīta opcija Izmaksas.</li>
<li>Ja lapā Projektu grupas ir atlasīta lauka Izmaksu grāmatošana — krājumi vērtība Peļņa un zaudējumi, tad lauks Galvenais konts, kad lapā Grāmatošanas iestatījumi virsgrāmatā ir atlasīta opcija Izmaksas — krājumi.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rindas atlaide</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Lauks Galvenais konts, kad lapā Grāmatošana ir atlasīta opcija Atlaide.</li>
<li>Ja grāmatošanas metodē nav definēts atlaides galvenais konts, tad pilnās cenas uzskaites sadale pirkšanas pasūtījuma rindā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot uzskaites sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības kreditora rēķina rindām.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Pirkšanas izmaksas, kas ir ievadītas pirkšanas pasūtījuma rindas cilnē Cena un atlaide.</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Uzskaites sadale pilnai cenai pirkšanas pasūtījuma rindā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rindu maksas</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Virsgrāmatas konts, tad lauks Debeta konts lapā Maksas kods.</li>
<li>Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Krājums, tad pirkšanas pasūtījuma rindā norādītās pilnās cenas uzskaites sadale.</li>
<li>Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Debitors/kreditors, tad lauks Kredīta konts lapā Maksas kods.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Nodokļi ar šādu nosacījumu:
<ul>
<li>Lapā Virsgrāmatas parametri ir atlasīta opcija Lietot ASV nodokļu nosacījumus.</li>
</ul></td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Pilnās cenas vai maksas uzskaites sadale.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Nodokļi ar šādiem nosacījumiem:
<ul>
<li>Lapā Virsgrāmatas parametri ir noņemta atzīme no opcijas Lietot ASV nodokļu nosacījumus.</li>
<li>PVN grupai lapā PVN grupas ir noņemta atzīme no opcijas Importa nodoklis.</li>
</ul></td>
<td><ol>
<li>Ja nodokļu summa ir atgūstama, tad lauks Saņemtais PVN lapā Virsgrāmatas grāmatošanas grupas.</li>
<li>Ja nodokļu summa nav atgūstama, tad pilna cena vai maksas uzskaites sadale.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Nodokļi ar šādiem nosacījumiem:
<ul>
<li>Lapā Virsgrāmatas parametri ir noņemta atzīme no opcijas Lietot ASV nodokļu nosacījumus.</li>
<li>PVN grupai lapā PVN grupas ir atlasīta opcija Importa nodoklis.</li>
</ul></td>
<td><ol>
<li>Ja nodokļu summa ir atgūstama, tad lauks Saņemtais PVN lapā Virsgrāmatas grāmatošanas grupas.</li>
<li>Ja nodokļu summa nav atgūstama, tad lauks Importa nodokļa izdevumi lapā Virsgrāmatas grāmatošanas grupas.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Galvenā maksa</td>
<td><ol>
<li>Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Virsgrāmatas konts, tad lauks Debeta konts lapā Maksas kods.</li>
<li>Ja veidlapā Maksas kods ir atlasīta lauka Debeta tips vērtība Debitors/kreditors, tad lauks Kredīta konts lapā Maksas kods.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Izmantot finanšu dimensiju noklusēto veidņu vērtības no kreditora rēķina galvenes.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Virsraksta atlaide</td>
<td><ol>
<li>Kreditora rēķina atlaides grāmatošanas veida lauks Galvenais konts lapā Automātisko darījumu konti.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantot noklusējuma finanšu dimensiju vērtības no galvenā konta lapā Kontu plāns.</li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a>Nodokļu sadalīšana
------------------

Nodokļu uzskaites sadales var izveidot tikai pēc nodokļu aprēķināšanas. Lai aprēķinātu PVN, lapā Kreditora rēķins ir jāizpilda viens no tālāk aprakstītajiem uzdevumiem.
-   Apskatiet rēķina kopsummu.
-   Apskatiet PVN.
-   Apskatiet apakšgrāmatas žurnālu.
-   Apskatiet uzskaites sadales visam kreditora rēķinam.
-   Aizturiet kreditora rēķinu.
-   Grāmatojiet kreditora rēķinu.

## <a name="subledger-journals-for-vendor-invoices"></a>Apakšgrāmatas žurnāli kreditoru rēķiniem
Pirms grāmatojat kreditora rēķinu, varat apskatīt pilnu uzskaites ierakstu šim rēķinam, kas ietver debetu un kredītu, lai pārliecinātos, ka rēķins tiek grāmatots pareizajos kontos. Šis pilnās uzskaites ieraksta skats tiek saukts par apakšgrāmatas žurnālu. 

Ja pirms kreditora rēķina reģistrēšanas žurnālā priekšskatāt apakšgrāmatas žurnāla ierakstu un tas ir nepareizs, šo apakšgrāmatas žurnāla ierakstu nevar mainīt. Tā vietā ir jāmodificē uzskaites sadales vai grāmatošanas metode. Uzskaites sadales tiek izmantotas, lai noteiktu uzskaites ieraksta vienu pusi, debetu vai kredītu. Korespondējošais apakšgrāmatas žurnāla konta ieraksts tiek izveidots, izmantojot grāmatošanas metodes, piemēram, no kreditora konta vai nodokļiem.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]