---
title: "Debitoru grāmatošanas metodes"
description: "Debitoru grāmatošanas profili kontrolē debitoru transakciju grāmatošanu virsgrāmatā."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: b36e75a5f527b41d50cc73e28a0b4e7e5df67e5c
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2017

---

# <a name="customer-posting-profiles"></a>Debitoru grāmatošanas metodes

[!include[banner](../includes/banner.md)]


Debitoru grāmatošanas profili kontrolē debitoru transakciju grāmatošanu virsgrāmatā.

<a name="customer-posting-profiles"></a>Debitoru grāmatošanas metodes
-------------------------

Debitoru grāmatošanas metodes jums ļauj virsgrāmatas kontus un dokumentu iestatījumus piešķirt visiem debitoriem, debitoru grupai vai atsevišķam debitoram. Šie iestatījumi tiks lietoti, kad veidojat pārdošanas pasūtījumus, brīva teksta rēķinus, maksājumus skaidrā naudā, atgādinājuma vēstules un procentu paziņojumus. Noteiktām transakcijām varat atlasīt grāmatošanas metodi, kas atšķiras no šajā lapā iestatītajām transakciju grāmatošanas metodēm un kam ir prioritāte pār tām. 

Noklusējuma grāmatošanas metode tiek definēta kopsavilkuma cilnē Virsgrāmata un Pārdošanas nodoklis, lapā Debitoru moduļa parametri. Noklusējuma grāmatošanas metode pēc tam automātiski tiek iekļauta jaunu dokumentu virsrakstā, kur to varat mainīt uz citu grāmatošanas metodi, ja nepieciešams.

Grāmatošanas definīcijas varat arī saistīt ar transakciju grāmatošanas tipiem lapā Transakciju grāmatošanas definīcijas. Grāmatošanas definīcijas kontrolē debitoru transakciju grāmatošanu virsgrāmatā grāmatošanas metožu vietā.

## <a name="creating-a-posting-profile"></a>Grāmatošanas metodes izveidošana
Norādiet virsgrāmatas kontus, kas tiek lietoti, lai grāmatotu transakcijas, kuras izmanto atlasīto grāmatošanas metodi. Atlasiet atlasītajai grāmatošanas metodei konta kodu un, ja iespējams, konta vai grupas numuru. Grāmatošanas procesā katrai transakcijai tiek atrasta piemērotākā grāmatošanas metode, meklējot visspecifiskāko konta kodu, konta numuru vai grupas un numura kombināciju šādā prioritārā secībā:

| Lauka **Konta kods** vērtība | Lauka **Konta/grupas numurs** vērtība            | Meklēšanas prioritāte |
|------------------------------|-------------------------------------------------|-----------------|
| **Tabula**                    | Specifisks debitora konts                       | 1               |
| **Grupa**                    | Debitoru grupa, kas ir piešķirta šim debitoram | 2               |
| **Visi**                      | Tukšs                                           | 3               |

Ja vēlaties, lai visu debitoru transakcijām būtu vienāda grāmatošanas metode, iestatiet tikai vienu grāmatošanas metodi, kurai laukā Konta kods ir vērtība Visi. Lai iestatītu savu grāmatošanas metodi, norādiet šādas vērtības:

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
<td><strong>Grāmatošanas metode</strong></td>
<td>Ievadiet grāmatošanas metodes kodu. Piemēram, varat izveidot divas grāmatošanas metodes, lai iegūtu vienu kontu debitoru bilancēm nacionālajā valūtā un otru — debitoru bilancēm ārvalstu valūtā. Vienu kontu varat nosaukt Nacionālais, bet otru — Ārvalstu.</td>
</tr>
<tr class="even">
<td><strong>Apraksts</strong></td>
<td>Ievadiet grāmatošanas metodes aprakstu. Šis tiek izmantots tikai ar mērķi labāk identificēt grāmatošanas metodi, kad to skatāt šajā lapā.</td>
</tr>
<tr class="odd">
<td><strong>Konta kods</strong></td>
<td>Norādiet, vai grāmatošanas metode tiek izmantota vienam debitoram, debitoru grupai vai visiem debitoriem:
<ul>
<li><strong>Tabula</strong> — grāmatošanas metode attiecas uz vienu debitoru. Atlasiet debitora kontu laukā Konta/grupas numurs.</li>
<li><strong>Grupa</strong> — grāmatošanas metode attiecas uz debitoru grupu. Atlasiet debitoru grupu laukā Konta/grupas numurs.</li>
<li><strong>Visi</strong> — grāmatošanas metode attiecas uz visiem debitoriem. Lauku Konta/grupas numurs atstājiet tukšu.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konta/grupas numurs</strong></td>
<td>Ja laukā Konta kods ir atlasīta vērtība Tabula, atlasiet konta numuru debitoram, kurš ir saistīts ar šo grāmatošanas metodi. Ja ir atlasīta vērtība Grupa, atlasiet debitoru grupu. Ja ir atlasīta vērtība Visi, atstājiet šo lauku tukšu.</td>
</tr>
<tr class="odd">
<td><strong>Summu konts</strong></td>
<td>Atlasiet virsgrāmatas kontu, kurš tiks lietots kā debitoru summu konts tiem debitoriem, kas ir saistīti ar šo grāmatošanas metodi.</td>
</tr>
<tr class="even">
<td><strong>Apmaksāt konta rēķinus</strong></td>
<td>Atlasiet likviditātes virsgrāmatas kontu, kas tiek lietots naudas plūsmas prognozēm. Šis lauks būs redzams tikai tad, ja ir iespējotas naudas plūsmas prognozes.</td>
</tr>
<tr class="odd">
<td><strong>PVN priekšapmaksām</strong></td>
<td>Atlasiet kontu pārdošanas nodoklim tādiem maksājumiem, kas tiek saņemti avansā.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Piezīme" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Piezīme</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izmantojiet lapu Debitoru moduļa parametri, lai norādītu grāmatošanas metodi, ko izmantot, kad maksājums ir apzīmēts kā priekšapmaksa.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Atlaižu konta saistības</strong></td>
<td>Atlasiet virsgrāmatas kontu atlaižu saistībām.</td>
</tr>
<tr class="odd">
<td><strong>Atgādinājuma vēstuļu sērija</strong></td>
<td>Atlasiet identifikatoru atgādinājuma vēstuļu sērijai, ko izmantot debitoriem, kuriem ir piešķirta šī grāmatošanas metode.</td>
</tr>
<tr class="even">
<td><strong>Soda naudas kods</strong></td>
<td>Atlasiet soda naudas kodu, ko izmantot soda naudas aprēķināšanai debitoriem, kuriem ir piešķirta šī grāmatošanas metode.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Tabulu ierobežojumi**

Transakcijām, kam ir atlasītā grāmatošanas metode, norādiet, vai šis transakcijas tiks segtas automātiski, vai tiks aprēķināta soda nauda, un vai tiks izveidotas atgādinājuma vēstules. Varat arī atlasīt kontu, kas tiks izmantots, kad tiek slēgtas transakcijas ar atlasīto grāmatošanas metodi.

Lai iestatītu savu grāmatošanas metodi, norādiet šādas vērtības:

| Lauks                 | Apraksts                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Segšana**        | Atlasiet šo pārslēgu, lai iespējotu automātisko nosegšanu transakcijām ar šo grāmatošanas metodi. Ja šī pārslēga atzīme ir notīrīta, transakciju nosegšana jums ir jāveic manuāli, izmantojot lapu Nosegt atvērtās transakcijas vai lapu Ievadīt debitora maksājumus. |
| **Intereses**          | Atzīmējiet šo pārslēgu, ja debitoru kontiem, kas izmanto šo metodi, soda nauda ir jāaprēķina nenokārtotām bilancēm. Ja šī pārslēga atzīme ir notīrīta, soda nauda šiem debitoriem netiks aprēķināta.                                           |
| **Atgādinājuma vēstule** | Atzīmējiet šo pārslēgu, ja debitoru kontiem, kas izmanto šo metodi, ir nepieciešams ģenerēt atgādinājuma vēstules. Ja šī pārslēga atzīme ir notīrīta, atgādinājuma vēstules šiem debitoriem netiks ģenerētas.                                                 |
| **Aizvērt**             | Atlasiet kādu grāmatošanas metodi, kuru mainīt, kad tiek slēgtas transakcijas ar šo grāmatošanas metodi. Darbība tiek uzskatīta par aizvērtu, kad tā ir pilnībā nosegta.                                                                           |



Plašāku informāciju skatiet šeit: [Debitoru maksājumu pārskats](../cash-bank-management/tasks/customer-payment-overview.md).


