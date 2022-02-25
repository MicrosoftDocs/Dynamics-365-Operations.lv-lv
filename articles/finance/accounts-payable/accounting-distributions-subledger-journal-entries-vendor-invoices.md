---
title: Uzskaites sadales un žurnālu ieraksti kreditoru rēķiniem
description: Uzskaites sadales tiek izmantotas, lai definētu veidu, kā summa tiek uzskaitīta, piemēram, kā izdevumi, nodokļi vai izmaksas tiek uzskaitīti kreditora rēķinā. Katrai summai, kas ir jānorāda kreditora rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fecdafe8765121d6d54389a70e6c2e497a03611a
ms.sourcegitcommit: 43d0555c17a0643c9e5ba3bc2da3ce5f80754642
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/18/2022
ms.locfileid: "8325972"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Uzskaites sadales un žurnālu ieraksti kreditoru rēķiniem

[!include [banner](../includes/banner.md)]

Uzskaites sadales tiek izmantotas, lai definētu veidu, kā summa tiek uzskaitīta, piemēram, kā izdevumi, nodokļi vai izmaksas tiek uzskaitīti kreditora rēķinā. Katrai summai, kas ir jānorāda kreditora rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales. 

## <a name="accounting-distributions"></a>Uzskaites sadales 

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
<li>Galvenais **konta lauks**, ja lapā Grāmatošana ir atlasīti izdevumi par **preci**.</li>
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
<li>Galvenais **konta lauks**, ja pirkšanas izdevumi izdevumiem ir atlasīti grāmatošanas **lapā**.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Kreditora rēķinā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā **Kontu** plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Pamatlīdzeklis</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja kreditora rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Ja **iegāde** ir atlasīta **laukā** **Darbības** tips lapā Kreditora rēķins, lauks Galvenais konts, **·** **·** **kad lapā Pamatlīdzekļu grāmatošanas metodes ir atlasīta iegāde.**</li>
<li>Ja **laukā Darbības** tips ir atlasīts **iegādes** pielāgojums, **·** **tad** pamatlīdzekļu grāmatošanas profilu lapā ir **atlasīts lauks Galvenais** konts.</li>
</ol></td>
<td><ol>
<li>Izmantot konta sadali pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā **Kontu** plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kreditora rēķina rindā noteikts projekts</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Ja **bilance** ir atlasīta **laukā Grāmatot izmaksas -** **krājums** projektu grupu lapā, lauks Galvenais konts, **·** **·** **kad Izmaksas ir atlasītas Virsgrāmatas grāmatošanas iestatījuma** lapā.</li>
<li>Ja **Virsgrāmatas grāmatošanas iestatījuma** **lapā ir atlasīts Peļņas un zaudējumu lauks Grāmatot izmaksas -** **krājums**, lauks Galvenais konts, **·** **·** **ja Iestatījums Virsgrāmatā ir atlasīts** Krājums.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rindas atlaide</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Galvenais **konta lauks**, ja **grāmatošanas** lapā ir **atlasīta** atlaide.</li>
<li>Ja grāmatošanas metodē nav definēts atlaides galvenais konts, tad pilnās cenas uzskaites sadale pirkšanas pasūtījuma rindā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot uzskaites sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības kreditora rēķina rindām.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta **lapā Kontu** plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Pirkšanas maksa, kas ir ievadīta **pirkšanas pasūtījuma** rindas cilnē Cena un atlaide</td>
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
<li>Ja **Virsgrāmatas** konts ir atlasīts **laukā** Debeta **tips** izmaksu kodu lapā, lauks **Debeta** konts maksu **kodu** lapā.</li>
<li>Ja **krājums** ir atlasīts **laukā** Debeta **tips maksu kodu** lapā, tad paplašinātās cenas uzskaites sadale pirkšanas pasūtījuma rindā.</li>
<li>Ja debitors/kreditors ir **atlasīts** **laukā** Debeta tips maksu kodu lapā, **lauks** Kredīta konts maksu **kodu** lapā.**·**</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta **lapā Kontu** plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Nodokļi ar šādu nosacījumu:
<ul>
<li>Opcija Lietot ASV nodokļu nosacījumus ir atlasīta lapā **Virsgrāmatas parametri**.</li>
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
<li>Opcija Lietot ASV nodokļu nosacījumus ir notīrīta lapā **Virsgrāmatas** parametri.</li>
<li>PVN **grupas** laukā Izmantotais nodoklis tiek notīrīts **PVN grupu** lapā.</li>
</ul></td>
<td><ol>
<li>Ja nodokļa summa ir atgūstama, lauks **Saņemamais PVN** Virsgrāmatas **grāmatošanas grupu** lapā.</li>
<li>Ja nodokļu summa nav atgūstama, tad pilna cena vai maksas uzskaites sadale.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā **Kontu** plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Nodokļi ar šādiem nosacījumiem:
<ul>
<li>Opcija Lietot ASV nodokļu nosacījumus ir notīrīta lapā **Virsgrāmatas** parametri.</li>
<li>PVN **grupu** lapā tiek atlasīts PVN grupas lauks **Izmantot** nodokli.</li>
</ul></td>
<td><ol>
<li>Ja nodokļa summa ir atgūstama, lauks **Saņemamais PVN** Virsgrāmatas **grāmatošanas grupu** lapā.</li>
<li>Ja nodokļa summa nav atgūstama, lauks **Izmantot nodokļa** izdevumus Virsgrāmatas **grāmatošanas grupu** lapā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā **Kontu** plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Galvenā maksa</td>
<td><ol>
<li>Ja **laukā Debeta** tips ir atlasīts **Virsgrāmatas** konts maksu kodu **lapas laukā Debeta konts,** **maksu** kodu **lapā.**</li>
<li>Ja **debitora/kreditora** kods ir **atlasīts** **laukā** Debeta tips maksu kodu lapā, **lauks** Kredīta konts maksu **kodu** lapā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Izmantot finanšu dimensiju noklusēto veidņu vērtības no kreditora rēķina galvenes.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā **Kontu** plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Virsraksta atlaide</td>
<td><ol>
<li>Galvenā **konta lauks** kreditoru rēķinu **atlaižu grāmatošanas tipam** lapā **Automātisko darbību** konti.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā **Kontu** plāns.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Nodokļu sadalīšana

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
