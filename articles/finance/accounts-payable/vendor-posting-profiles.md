---
title: Kreditoru grāmatošanas metodes
description: Kreditoru grāmatošanas metodes kontrolē kreditoru transakciju grāmatošanu virsgrāmatā.
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8ebb67bddf6fa9aae8ba6c6ed290c94bb2e0a047ca6157aa1325f4cf21f148f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777220"
---
# <a name="vendor-posting-profiles"></a>Kreditoru grāmatošanas metodes

[!include [banner](../includes/banner.md)]

Kreditoru grāmatošanas metodes kontrolē kreditoru transakciju grāmatošanu virsgrāmatā.

## <a name="vendor-posting-profiles"></a>Kreditoru grāmatošanas metodes

Kreditoru grāmatošanas metodes jums ļauj virsgrāmatas kontus un dokumentu iestatījumus piešķirt visiem kreditoriem, kreditoru grupai vai atsevišķam kreditoram. Šie iestatījumi tiek izmantoti, kad izveidojat pirkšanas pasūtījumus, kreditoru rēķinus un maksājumus skaidrā naudā. Noteiktām transakcijām varat atlasīt grāmatošanas metodi, kas atšķiras no šajā lapā iestatītajām transakciju grāmatošanas metodēm un kam ir prioritāte pār šajā lapā iestatītajām. Noklusējuma grāmatošanas metode tiek definēta kopsavilkuma cilnē **Virsgrāmata un PVN**, lapā **Kreditoru moduļa parametri**. Noklusējuma grāmatošanas metode pēc tam tiek automātiski iekļauta jaunu dokumentu virsrakstā, kur to varat mainīt uz citu grāmatošanas metodi, ja nepieciešams.

Grāmatošanas definīcijas varat arī saistīt ar transakciju grāmatošanas tipiem lapā **Transakciju grāmatošanas definīcijas**. Grāmatošanas definīcijas kontrolē kreditoru transakciju grāmatošanu virsgrāmatā grāmatošanas metožu vietā.

## <a name="creating-a-posting-profile"></a>Grāmatošanas metodes izveidošana
### <a name="setup"></a>**Iestatījumi**

Norādiet virsgrāmatas kontus, kas tiek lietoti, lai grāmatotu transakcijas, kuras izmanto atlasīto grāmatošanas metodi. Atlasiet atlasītajai grāmatošanas metodei konta kodu un, ja iespējams, konta vai grupas numuru. Grāmatošanas procesā katrai transakcijai tiek atrasta piemērotākā grāmatošanas metode, meklējot visspecifiskāko konta kodu, konta numuru vai grupas un numura kombināciju tālāk norādītajā prioritāšu secībā.

| Lauka **Konta kods** vērtība | Lauka **Konta/grupas numurs** vērtība        | Meklēšanas prioritāte |
|------------------------------|---------------------------------------------|-----------------|
| **Tabula**                    | Specifisks kreditora konts                     | 1               |
| **Grupa**                    | Kreditoru grupa, kas ir piesaistīta šim kreditoram | 2               |
| **Visi**                      | Tukšs                                       | 3               |

Ja vēlaties, lai visām kreditoru transakcijām būtu vienāda grāmatošanas metode, iestatiet tikai vienu grāmatošanas metodi, kurai laukā **Konta kods** ir vērtība **Visi**. Lai iestatītu savu grāmatošanas metodi, norādiet tālāk uzskaitītās vērtības.

<table>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Grāmatošanas metode</strong></td>
<td>Ievadiet grāmatošanas metodes kodu. Piemēram, varat izveidot divas grāmatošanas metodes, lai iegūtu vienu kontu kreditoru bilancēm nacionālajā valūtā un otru — kreditoru bilancēm ārvalstu valūtā. Vienu kontu varat nosaukt Nacionālais, bet otru — Ārvalstu.</td>
</tr>
<tr class="even">
<td><strong>Apraksts</strong></td>
<td>Ievadiet grāmatošanas metodes aprakstu.</td>
</tr>
<tr class="odd">
<td><strong>Konta kods</strong></td>
<td>Norādiet, vai grāmatošanas metode tiek lietota konkrētam kreditoram, kreditoru grupai vai visiem kreditoriem:
<ul>
<li><strong>Tabula</strong> — grāmatošanas metode attiecas uz vienu kreditoru. Atlasiet kreditora kontu laukā <strong>Konta/grupas numurs</strong>.</li>
<li><strong>Grupa</strong> — grāmatošanas metode attiecas uz kreditoru grupu. Atlasiet kreditoru grupu laukā <strong>Konta/grupas numurs</strong>.</li>
<li><strong>Visi</strong> — grāmatošanas metode attiecas uz visiem kreditoriem. Lauku <strong>Konta/grupas numurs</strong> atstājiet tukšu.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konta/grupas numurs</strong></td>
<td>Ja laukā <strong>Konta kods</strong> ir atlasīta vērtība <strong>Tabula</strong>, atlasiet konta numuru tam kreditoram, kurš ir saistīts ar šo grāmatošanas metodi. Ja ir atlasīta vērtība <strong>Grupa</strong>, atlasiet kreditoru grupu. Ja ir atlasīta vērtība <strong>Visi</strong>, atstājiet šo lauku tukšu.</td>
</tr>
<tr class="odd">
<td><strong>Summu konts</strong></td>
<td>Atlasiet virsgrāmatas kontu, kas tiks izmantots kā summu konts kreditoriem, ar kuriem ir saistīta šī grāmatošanas metode. Šim galvenajam kontam būs atzīmēts parametrs <strong>Neļaut manuālu ievadi</strong>. Ja šo kontu vēlāk noņemat no grāmatošanas metodes, validējiet iestatījumu <strong>Neļaut manuālu ievadi</strong> lapā <strong>Galvenie konti</strong>. 
<p><strong>Piezīme.</strong> Ja lapā <strong>Virsgrāmatas parametri</strong> ir atlasīta opcija <strong>Izmantot grāmatošanas definīcijas</strong>, summu konta vietā kreditoru rēķiniem tiek izmantota transakcijas grāmatošanas definīcija.</p>
</td>
</tr>
<tr class="even">
<td><strong>Apmaksāt konta rēķinus</strong></td>
<td>Atlasiet likviditātes virsgrāmatas kontu, kas tiek lietots naudas plūsmas prognozēm. Šis lauks ir pieejams tikai tad, ja ir iespējota naudas plūsmas prognozēšana.</td>
</tr>
<tr class="odd">
<td><strong>PVN priekšapmaksām</strong></td>
<td>Atlasiet kontu tādiem pārdošanas nodokļa maksājumiem, kas tiek saņemti avansā.
<p><strong>Piezīme.</strong> Grāmatošanas metode, kas tiek izmantota, kad maksājums ir atzīmēts kā priekšapmaksa, tiek atlasīta profilā <strong>Grāmatošana</strong> ar lauku <strong>Priekšapmaksas žurnāla dokumenta summa</strong> lapas <strong>Kreditoru moduļa parametri</strong> apgabalā <strong>Virsgrāmata un PVN</strong>.</p>
</td>
</tr>
<tr class="even">
<td><strong>Saņemšana</strong></td>
<td>Atlasiet virsgrāmatas kontu, kurā tiek grāmatota informācija par neapstiprinātiem kreditoru rēķiniem. Šī informācija tiek ievadīta rēķinu reģistra žurnālā. Piemēram, lietotājs ievada tikai pamatinformāciju par kreditoru rēķiniem, kad tie tiek saņemti rēķinu reģistrā. Kad rēķinu reģistrs ir iegrāmatots, transakcijas tiek grāmatotas šeit ievadītajā kontā un laukā <strong>Korespondējošais konts</strong>. Kad rēķini ir apstiprināti, debets no saņemšanas konta tiek pārsūtīts uz kreditora summu kontu.</td>
</tr>
<tr class="odd">
<td><strong>Korespondējošais konts</strong></td>
<td>Atlasiet virsgrāmatas kontu, kas tiek izmantots kreditoru neapstiprināto rēķinu kompensēšanai, kuri tiek atjaunināti ar rēķinu reģistru. Korespondējošais konts darbojas kā korespondējošais konts transakcijām, kuras tiek grāmatotas saņemšanas kontos. Tādēļ šis konts ietver kreditoru pirkumus, kas vēl nav apstiprināti.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tabulu ierobežojumi**

Transakcijām, kam ir atlasītā grāmatošanas metode, norādiet, vai šis transakcijas tiks segtas automātiski, vai tiks aprēķināta soda nauda, un vai tiks izveidotas atgādinājuma vēstules. Varat arī atlasīt kontu, kas tiks izmantots, kad tiek slēgtas transakcijas ar atlasīto grāmatošanas metodi.

Lai iestatītu savu grāmatošanas metodi, norādiet tālāk uzskaitītās vērtības

| Lauks          | Apraksts                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Segums** | Atlasiet šo opciju, lai iespējotu automātisko nosegšanu transakcijām ar šo grāmatošanas metodi. Ja šīs opcijas atzīme ir notīrīta, transakciju nosegšana jums ir jāveic manuāli, izmantojot lapu **Nosegt atvērtās transakcijas**. |
| **Atcelt**     | Atzīmējiet šo opciju, ja vēlaties iespēju atcelt transakcijas, kurām ir šī grāmatošanas metode.                                                                                                               |
| **Aizvērt**      | Atlasiet kādu grāmatošanas metodi, kuru mainīt, kad tiek slēgtas transakcijas ar šo grāmatošanas metodi. Darbība tiek uzskatīta par aizvērtu, kad tā ir pilnībā nosegta.                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]