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
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358185"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Uzskaites sadales un žurnālu ieraksti kreditoru rēķiniem

[!include [banner](../includes/banner.md)]

Uzskaites sadales tiek izmantotas, lai definētu veidu, kā summa tiek uzskaitīta, piemēram, kā izdevumi, nodokļi vai izmaksas tiek uzskaitīti kreditora rēķinā. Katrai summai, kas ir jānorāda kreditora rēķina reģistrēšanai žurnālā, ir viena vai vairākas uzskaites sadales. 

## <a name="accounting-distributions"></a>Uzskaites sadales 

Lapā Kreditora rēķins varat izmantot tālāk norādītās pogas, lai skatītu un, iespējams, modificētu katras kreditora rēķinā ietvertās summas uzskaites sadales.
-   **Sadales summas** — skatiet un mainiet uzskaites sadales atsevišķai rindai un jebkurai apakšrindai, piemēram, nodokļiem un izmaksām. Jūs varat arī apskatīt un modificēt uzskaites sadales pakārtotās rindas tieši no **PVN darbību lapas** vai Maksu **darbību** lapas.
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
<li>Galvenais <strong>konta lauks</strong>, ja lapā Grāmatošana ir atlasīti izdevumi par preci<strong></strong>.</li>
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
<li>Galvenais <strong>konta lauks</strong>, ja pirkšanas izdevumi izdevumiem ir atlasīti grāmatošanas<strong></strong> lapā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Kreditora rēķinā izmantot noklusējuma finanšu dimensiju vērtības.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Pamatlīdzeklis</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja kreditora rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Ja <strong>iegāde</strong> ir atlasīta <strong>laukā</strong><strong></strong> Darbības tips lapā Kreditora rēķins, lauks Galvenais konts, <strong></strong><strong></strong><strong>kad lapā Pamatlīdzekļu grāmatošanas metodes ir atlasīta iegāde.</strong></li>
<li>Ja <strong>laukā Darbības</strong> tips ir atlasīts <strong>iegādes</strong> pielāgojums, <strong></strong><strong></strong> tad pamatlīdzekļu grāmatošanas profilu lapā ir <strong>atlasīts lauks Galvenais</strong> konts.</li>
</ol></td>
<td><ol>
<li>Izmantot konta sadali pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kreditora rēķina rindā noteikts projekts</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Ja <strong>bilance</strong> ir atlasīta <strong>laukā Grāmatot izmaksas -</strong><strong></strong> krājums projektu grupu lapā, lauks Galvenais konts, <strong></strong><strong></strong><strong>kad Izmaksas ir atlasītas Virsgrāmatas grāmatošanas iestatījuma</strong> lapā.</li>
<li>Ja <strong>Virsgrāmatas grāmatošanas iestatījuma</strong><strong>lapā ir atlasīts Peļņas un zaudējumu lauks Grāmatot izmaksas -</strong><strong></strong> krājums, lauks Galvenais konts,<strong></strong><strong></strong><strong>ja Iestatījums Virsgrāmatā ir atlasīts</strong> Krājums.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rindas atlaide</td>
<td><ol>
<li>Uzskaites sadale pirkšanas pasūtījuma rindai, ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu.</li>
<li>Galvenais <strong>konta lauks</strong>, ja <strong></strong> grāmatošanas lapā ir <strong>atlasīta</strong> atlaide.</li>
<li>Ja grāmatošanas metodē nav definēts atlaides galvenais konts, tad pilnās cenas uzskaites sadale pirkšanas pasūtījuma rindā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot uzskaites sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības kreditora rēķina rindām.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Pirkšanas maksa, kas ir ievadīta <strong>pirkšanas pasūtījuma</strong> rindas cilnē Cena un atlaide</td>
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
<li>Ja <strong>laukā</strong> Debeta <strong>tips ir atlasīts</strong> Virsgrāmatas <strong>konts maksu kodu</strong> lapas laukā Debeta konts,<strong></strong> maksu <strong>kodu</strong> lapā.</li>
<li>Ja <strong>krājums</strong> ir atlasīts <strong>laukā</strong> Debeta <strong>tips maksu kodu</strong> lapā, tad paplašinātās cenas uzskaites sadale pirkšanas pasūtījuma rindā.</li>
<li>Ja <strong>debitora/kreditora</strong> kods ir atlasīts <strong></strong><strong></strong> laukā Debeta tips<strong></strong> maksu kodu lapā, lauks Kredīta konts maksu <strong>kodu</strong> lapā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Nodokļi ar šādu nosacījumu:
<ul>
<li>Opcija <strong>Lietot ASV nodokļu nosacījumus ir</strong> atlasīta lapā <strong>Virsgrāmatas parametri</strong>.</li>
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
<li>Opcija <strong>Lietot ASV nodokļu nosacījumus ir</strong> notīrīta lapā <strong>Virsgrāmatas</strong> parametri.</li>
<li>PVN <strong>grupas</strong> laukā Izmantotais nodoklis tiek notīrīts <strong>PVN grupu</strong> lapā.</li>
</ul></td>
<td><ol>
<li>Ja nodokļa summa ir atgūstama, lauks <strong>Saņemamais PVN</strong> Virsgrāmatas <strong>grāmatošanas grupu</strong> lapā.</li>
<li>Ja nodokļu summa nav atgūstama, tad pilna cena vai maksas uzskaites sadale.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Nodokļi ar šādiem nosacījumiem:
<ul>
<li>Opcija Lietot ASV nodokļu nosacījumus ir notīrīta lapā <strong>Virsgrāmatas</strong> parametri.</li>
<li>PVN <strong>grupu</strong> lapā tiek atlasīts PVN grupas lauks <strong>Izmantot</strong> nodokli.</li>
</ul></td>
<td><ol>
<li>Ja nodokļa summa ir atgūstama, lauks <strong>Saņemamais PVN</strong> Virsgrāmatas <strong>grāmatošanas grupu</strong> lapā.</li>
<li>Ja nodokļa summa nav atgūstama, lauks <strong>Izmantot nodokļa</strong> izdevumus Virsgrāmatas <strong>grāmatošanas grupu</strong> lapā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no pilnās cenas vai uzskaites sadales kreditora rēķina rindā norādītajai maksai.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Galvenā maksa</td>
<td><ol>
<li>Ja <strong>laukā Debeta</strong> tips ir atlasīts<strong>Virsgrāmatas</strong> konts maksu kodu<strong>lapas laukā Debeta konts,</strong><strong>maksu</strong> kodu<strong>lapā.</strong></li>
<li>Ja <strong>debitora/kreditora</strong> kods ir atlasīts <strong></strong><strong></strong> laukā Debeta tips<strong></strong> maksu kodu lapā, lauks Kredīta konts maksu <strong>kodu</strong> lapā.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Ja galvenais konts ir sadalījuma konts, izmantot noklusējuma vērtību no sadalījuma konta definīcijas.</li>
<li>Izmantot finanšu dimensiju noklusēto veidņu vērtības no kreditora rēķina galvenes.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
<tr class="even">
<td>Virsraksta atlaide</td>
<td><ol>
<li>Galvenā <strong>konta lauks</strong> kreditoru rēķinu <strong>atlaižu grāmatošanas tipam</strong> lapā <strong>Automātisko darbību</strong> konti.</li>
</ol></td>
<td><ol>
<li>Ja rēķina rindā ir atsauce uz pirkšanas pasūtījuma rindu, izmantot konta sadali pirkšanas pasūtījuma rindai.</li>
<li>Izmantot finanšu dimensijas no uzskaites sadalēm pilnajai cenai kreditora rēķina rindā.</li>
<li>Izmantot finanšu dimensiju vērtības no kreditora rēķina rindas.</li>
<li>Izmantojiet noklusējuma finanšu dimensiju vērtības no galvenā konta lapā <strong>Kontu</strong> plāns.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Nodokļu sadalīšana

Nodokļu uzskaites sadales var izveidot tikai pēc nodokļu aprēķināšanas. Lai aprēķinātu PVN, kreditoru rēķinu lapā pabeidziet vienu no **šiem** uzdevumiem:
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
