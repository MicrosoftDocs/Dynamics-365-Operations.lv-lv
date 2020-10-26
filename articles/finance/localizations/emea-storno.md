---
title: Storno uzskaite
description: Storno uzskaite ir prakse, kurā tiek izmantoti negatīvie skaitļi, lai apgrieztu sākotnējos žurnāla konta ierakstus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 1219713
ms.search.region: Czech Republic, Germany, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ee8f3f5c850ad0ae519c83a689d12b9a1471712
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983093"
---
# <a name="storno-accounting"></a>Storno uzskaite

[!include [banner](../includes/banner.md)]

Storno uzskaite ir prakse, kurā tiek izmantoti negatīvie skaitļi, lai apgrieztu sākotnējos žurnāla konta ierakstus.

*Storno uzskaite* ir prakse, kurā tiek izmantotas negatīvas debeta vai kredīta summas, lai apgrieztu sākotnējos žurnāla konta ierakstus. Tā kā grāmatveži parasti Storno ierakstus veic ar sarkanu tinti, šī uzskaites prakse ir pazīstama arī kā *Sarkanais storno*. Izmantojot Storno uzskaiti, varat atcelt dokumentu, kurā ir norādīta nepareiza summa, taču pēc atcelšanas vienmēr ir jāievada pareizā dokumenta summa.

## <a name="example"></a>Paraugs
Grāmatvedis grāmato kreditora rēķinu par summu 120 USD. Maksāšanas procesa laikā tiek atklāts, ka grāmatvedis ir kļūdījies un ievadījis 120 USD, nevis 102 USD. Tagad grāmatvedim ir jāizveido Storno ieraksts sākotnējam dokumentam un pēc tam jāizveido pareizais rēķins par summu 102 USD. Plašāku informāciju skatiet šeit:  [Kreditora rēķinu pārskats](../accounts-payable/vendor-invoices-overview.md). Tālāk esošajā tabulā parādīts vispārējais Storno ieraksts.

| **Dokumenta ID** | **Konts** | **Debets** | **Kredīts** | **Komentārs**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Rēķins0001     | Pirkš. konts   | 120       |            | Sākotnējais rēķins (nepareizs) |
| Rēķins0001     | Kreditora konts  |           | 120        | Sākotnējais rēķins (nepareizs) |
|                 |             |           |            |                              |
| Storno0001      | Pirkš. konts   | -120     |            | Storno                       |
| Storno0001      | Kreditora konts  |           | -120      | Storno                       |
|                 |             |           |            |                              |
| Rēķins0002     | Pirkš. konts   | 102       |            | Pareizais rēķins              |
| Rēķins0002     | Kreditora konts  |           | 102        | Pareizais rēķins              |

Šajā piemērā bilances pārskatā redzami tālāk norādītie dati.

| Konts    | Debetkarte | Kredītkarte | Bilance |
|------------|-------|--------|---------|
| Pirkš. konts  | 102   | 0      | 102     |
| Kreditora konts | 0     | 102    | -102    |

## <a name="differences-between-storno-and-reverse-entries"></a>Atšķirības starp Storno un reversīvajiem ierakstiem
Grāmatošanas ierakstus var labot divos veidos — izmantojot reversīvos ierakstus un Storno. Ja izmantojat reversīvo ierakstu, tiek izveidota sākotnējā vispārējā ieraksta kopija, kurā debeta un kredīta konti ir apmainīti vietām un nav mainīta summu zīme. Ja izmantojat Storno, sistēma izveido sākotnējā vispārējā ieraksta kopiju, bet summas tiek reģistrētas ar negatīvu zīmi. Tālāk esošajā tabulā parādīts vispārējais Storno ieraksts.

| **Dokumenta ID** | **Konts** | **Debets** | **Kredīts** | **Komentārs**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Rēķins0001     | Pirkš. konts   | 120       |            | Sākotnējais rēķins (nepareizs) |
| Rēķins0001     | Kreditora konts  |           | 120        | Sākotnējais rēķins (nepareizs) |
|                 |             |           |            |                              |
| Reversīvais0001     | Pirkš. konts   |           | 120        | Apgriezt                      |
| Reversīvais0001     | Kreditora konts  | 120       |            | Apgriezt                      |
|                 |             |           |            |                              |
| Rēķins0002     | Pirkš. konts   | 102       |            | Pareizais rēķins              |
| Rēķins0002     | Kreditora konts  |           | 102        | Pareizais rēķins              |

Šajā piemērā bilances pārskatā redzami tālāk norādītie dati.

| Konts    | Debetkarte | Kredītkarte | Bilance |
|------------|-------|--------|---------|
| Pirkš. konts  | 222   | 120    | 102     |
| Kreditora konts | 120   | 222    | -102    |

Ņemiet vērā, ka bilances reversīvajiem ierakstiem un Storno ir vienādas. Pastāv atšķirība starp debeta apgrozījumu un kredīta apgrozījums, jo reversīvais ieraksts rada lieku debeta un kredīta apgrozījumu. Reversīvo ierakstu lieto valstīs/reģionos, kur apgrozījumu reti izmanto. Citās valstīs/reģionos izmanto Storno uzskaiti.

## <a name="partial-storno"></a>Daļējais Storno
*Daļējais Storno* ir uzskaites prakse, kurā tiek izmantotas negatīvas debeta vai kredīta summas, lai apgrieztu daļu no sākotnējiem žurnāla konta ierakstiem. Dažās valstīs/reģionos ir atļauts izmantot daļējo Storno. Piemēram, grāmatvedis grāmato kreditora rēķinu par summu 120 USD. Maksāšanas procesa laikā tiek atklāts, ka grāmatvedis ir kļūdījies un ievadījis nepareizu numuru sēriju. Sākotnējā rēķinā par summu 102 USD bija numuru sērijas kļūda. Izmantojot daļējo Storno, grāmatvedim ir jāizveido Storno ieraksts par 18 USD. Tālāk esošajā tabulā ir parādīts vispārējais daļējā Storno ieraksts.

| **Dokumenta ID** | **Konts** | **Debets** | **Kredīts** | **Komentārs**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Rēķins0001     | Pirkš. konts   | 120       |            | Sākotnējais rēķins (nepareizs) |
| Rēķins0001     | Kreditora konts  |           | 120        | Sākotnējais rēķins (nepareizs) |
|                 |             |           |            |                              |
| Storno0001      | Pirkš. konts   | \-18      |            | Daļējais Storno               |
| Storno0001      | Kreditora konts  |           | \-18       | Daļējais Storno               |

Šajā piemērā bilances pārskatā redzami tālāk norādītie dati.

| Konts    | Debetkarte | Kredītkarte | Bilance |
|------------|-------|--------|---------|
| Pirkš. konts  | 102   | 0      | 102     |
| Kreditora konts | 0     | 102    | -102    |

Daļējais Storno oriģināla formā var radīt problēmu. Ja sākotnējā dokumenta datums atšķiras no Storno ieraksta datuma, tas var apgrūtināt pareizas summas valūtā iegūšanu. Tāpēc daļējo Storno ir atļauts izmantot tikai noteiktiem dokumentiem. Dynamics 365 Finance nodrošina daļējā Storno funkcionalitāti dokumentiem un valstīm/reģioniem, kuriem tas ir atļauts.

## <a name="how-to-enter-stornoon-journal-lines"></a>Storno ieraksta ievadīšana žurnāla rindās
Lai veiktu Storno ierakstu, žurnāla rindā ievadiet debeta vai kredīta summu ar negatīvu zīmi. Grāmatošanas procesa laikā tiek iestatīts lauks **Labojums**. 

## <a name="how-storno-is-displayed"></a>Kā Storno tiek attēlots
Finance īpašā veidā apstrādā negatīvās summas žurnālā. Vispārējais žurnāla ieraksts, debitora transakcija, kreditora transakcija un citas transakcijas nodrošina Storno funkciju, kā tas ir parādīts tālāk.

<table>
<thead>
<tr class="row-1">
<th class="column-1" rowspan="2">Lietotāja ievade žurnāla rindā</th>
<th class="column-2" colspan="2">Saglabāšanas princips</th>
<th class="column-4" colspan="2">Princips</th>
<th class="column-6" colspan="3">Ietekme uz izraksta pārskatu</th>
</tr>
<tr class="row-1">
<th class="column-2">Labojuma lauks</th>
<th class="column-3">Summas lauks</th>
<th class="column-4">Summa darījuma valūtā</th>
<th class="column-5">Summa</th>
<th class="column-6">Debeta kolonna</th>
<th class="column-7">Kredīta kolonna</th>
<th class="column-8">Bilances kolonna</th>
</tr>
</thead>
<tbody>
<tr class="row-2">
<td class="column-1"> Debetkarte</td>
<td class="column-2">Nav</td>
<td class="column-3">&gt;0</td>
<td class="column-4" align="right">Summa</td>
<td class="column-5" align="right">Summa</td>
<td class="column-6">Pieaug</td>
<td class="column-7"></td>
<td class="column-8">Pieaug</td>
</tr>
<tr class="row-3">
<td class="column-1"> Kredītkarte</td>
<td class="column-2">Nav</td>
<td class="column-3">&lt;0</td>
<td class="column-4" align="right">-Summa</td>
<td class="column-5" align="right">Summa</td>
<td class="column-6"></td>
<td class="column-7">Pieaug</td>
<td class="column-8">Samazinās</td>
</tr>
<tr class="row-4">
<td class="column-1">-Debets</td>
<td class="column-2">Jā</td>
<td class="column-3">&gt;0</td>
<td class="column-4" align="right">+Summa</td>
<td class="column-5" align="right">-Summa</td>
<td class="column-6">Samazinās</td>
<td class="column-7"></td>
<td class="column-8">Pieaug</td>
</tr>
<tr class="row-5">
<td class="column-1">-Kredīts</td>
<td class="column-2">Jā</td>
<td class="column-3">&lt;0</td>
<td class="column-4" align="right">-Summa</td>
<td class="column-5" align="right">-Summa</td>
<td class="column-6"></td>
<td class="column-7">Samazinās</td>
<td class="column-8">Samazinās</td>
</tr>
</tbody>
</table>

Varat pielāgot Storno attēlojumu formās, režģos, kolonnās un laukos. Piemēram, varat izslēgt zīmes rādīšanu vai mainīt atkāpi negatīvajām summām. Varat arī izmantot lauku **Labojums** ar visiem rādīšanas iestatījumiem; ja ir iestatīta lauka **Labojums** vērtība Jā, tas ir Storno ieraksts.

![Žurnāla ieraksta Storno summas](./media/journal-storno.png)

## <a name="how-documents-create-storno"></a>Kā dokumenti izveido Storno
Noteikti dokumenti izraisa atcelšanas transakciju izveidi. Piemēram, ārvalstu valūtas pārvērtēšanas virsgrāmatai, kreditoru un debitoru parādu dokumenti atceļ nerealizēto peļņu un zaudējumus. Papildinformāciju skatiet rakstā [Ārvalstu valūtas pārvērtēšana virsgrāmatai](../general-ledger/foreign-currency-revaluation-general-ledger.md) vai [Ārvalstu valūtas pārvērtēšana kreditoriem un debitoriem](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md). Pēc atcelšanas transakcijas izveides tiek izveidotas jaunas transakcijas ar nerealizēto peļņu un zaudējumiem. Atcelšanas transakcijas tiek izveidotas arī krājumiem. Papildinformāciju skatiet rakstā [Krājumu slēgšana](../../supply-chain/cost-management/inventory-close.md). Ir dokumenti, kas ļauj atcelt iepriekš grāmatotu dokumentu. Piemēram, lietotājs var izveidot kredīta notu, lai atceltu iepriekš izveidotu rēķinu. Dokumentos tiek izmantoti īpaši parametri, lai izveidotu reversīvās vai Storno transakcijas. Piemēram, ārvalstu valūtas pārvērtēšana izraisa reversīvas vai Storno transakcijas izveidi, pamatojoties uz Virsgrāmatas labojuma parametru. Debitora kredīta nota izveido reversīvas vai Storno transakcijas, pamatojoties uz debitoru parādu kredīta notas labojuma parametru.

