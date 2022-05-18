---
title: Debitoru grāmatošanas metodes
description: Šajā tēmā aprakstītas debitoru grāmatošanas metodes, kas kontrolē debitoru darbību grāmatošanu Virsgrāmatā.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ed5ab24e37c75222080bd242aa72a39ecb476bf
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734637"
---
# <a name="customer-posting-profiles"></a>Debitoru grāmatošanas metodes

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstītas debitoru grāmatošanas metodes, kas kontrolē debitoru darbību grāmatošanu Virsgrāmatā.

## <a name="customer-posting-profiles"></a>Debitoru grāmatošanas metodes

Debitoru grāmatošanas metodes ļauj piešķirt virsgrāmatas kontus un dokumentu iestatījumus visiem debitoriem, debitoru grupai vai vienam debitoram. Šie iestatījumi tiks izmantoti, veidojot pārdošanas pasūtījumu rēķinus, brīvā teksta rēķinus, projekta rēķinus, maksājumu žurnālus, atgādinājuma vēstules un procentu paziņojumus. 

Noklusētā grāmatošanas metode ir definēta virsgrāmatas **un PVN** cilnē debitoru **parādu parametru** lapā. Pēc tam tā tiek automātiski iekļauta jauno dokumentu galvenē. To var mainīt, ja nepieciešama atšķirīga grāmatošanas metode. 

Organizācijas, kas pieņem priekšapmaksas no debitoriem, bieži konfigurē otru priekšapmaksas grāmatošanas metodi un saista to ar parametriem kā noklusējuma grāmatošanas metodi priekšapmaksām. Papildinformāciju skatiet debitoru [priekšapmaksu](customer-prepayments.md).

Grāmatošanas definīcijas varat arī saistīt ar transakciju grāmatošanas tipiem lapā **Transakciju grāmatošanas definīcijas**. Grāmatošanas definīcijas lieto grāmatošanas metožu vietā, lai kontrolētu debitoru darbību grāmatošanu Virsgrāmatā. Papildinformāciju skatiet tēmā [Grāmatošanas definīcijas](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Grāmatošanas metodes izveidošana
Norādiet virsgrāmatas kontus, kas tiek lietoti, lai grāmatotu transakcijas, kuras izmanto atlasīto grāmatošanas metodi. Atlasiet atlasītajai grāmatošanas metodei konta kodu un, ja iespējams, konta vai grupas numuru. Grāmatošanas procesā katrai transakcijai tiek atrasta piemērotākā grāmatošanas metode, meklējot visspecifiskāko konta kodu, konta numuru vai grupas un numura kombināciju šādā prioritārā secībā:

| Lauka Konta kods vērtība | Lauka Konta/grupas numurs vērtība                | Meklēšanas prioritāte |
|--------------------------|-------------------------------------------------|-----------------|
| Tabula                    | Specifisks debitora konts                       | 1               |
| Grupa                    | Debitoru grupa, kas ir piešķirta šim debitoram | 2               |
| Visus                      | Tukšs                                           | 3               |

Ja vēlaties, lai visu debitoru darbībām būtu viena un tā pati grāmatošanas metode, iestatiet tikai vienu grāmatošanas metodi, **kur** Viss tiek ievadīts **laukā Konta** kods. Lai iestatītu savu grāmatošanas metodi, norādiet tālāk uzskaitītās vērtības.

<table>
<thead>
<tr>
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr>
<td>Grāmatošanas profils</td>
<td>Ievadiet grāmatošanas metodes kodu. Piemēram, varat izveidot divas grāmatošanas metodes, lai iegūtu vienu kontu debitoru bilancēm nacionālajā valūtā un otru — debitoru bilancēm ārvalstu valūtā. Vienu kontu varat nosaukt Nacionālais, bet otru — Ārvalstu.</td>
</tr>
<tr>
<td>Apraksts</td>
<td>Ievadiet grāmatošanas metodes aprakstu. Šis tiek izmantots tikai ar mērķi labāk identificēt grāmatošanas metodi, kad to skatāt šajā lapā.</td>
</tr>
<tr>
<td>Konta kods</td>
<td>Norādiet, vai grāmatošanas metode tiek izmantota vienam debitoram, debitoru grupai vai visiem debitoriem:
<ul>
<li><b>Tabula</b> – grāmatošanas metode attiecas uz vienu debitoru. Atlasiet debitora kontu laukā <b>Konta/grupas</b> numurs.</li>
<li><b>Grupa</b> – grāmatošanas metode attiecas uz debitoru grupu. Atlasiet debitoru grupu laukā <b>Konta/grupas</b> numurs.</li>
<li><b>Visi</b> – grāmatošanas metode attiecas uz visiem debitoriem. Lauku <b>Konta/grupas numurs</b> atstājiet tukšu.</li>
</ul>
</td>
</tr>
<tr>
<td>Konta/grupas numurs</td>
<td><b>Ja</b> laukā Konta kods <b>atlasīta tabula</b>, atlasiet tā debitora konta numuru, kurš ir saistīts ar grāmatošanas metodi. Ja <b>ir</b> atlasīta Grupa, atlasiet debitoru grupu. Ja ir atlasīta vērtība <b>Visi</b>, atstājiet šo lauku tukšu.</td>
</tr>
<tr>
<td>Summu konts</td>
<td>Atlasiet galveno kontu, kas tiks izmantots kā debitoru tirdzniecības konts debitoriem, kuri ir saistīti ar grāmatošanas metodi. Šis konts ir konts debitora bilances <b>grāmatošanas</b> tipam.</td>
</tr>
<tr>
<td>Likviditātes konts maksājumiem</td>
<td>Atlasiet likviditātes virsgrāmatas kontu, kas tiek lietots naudas plūsmas prognozēm. Šis lauks tiks parādīts tikai tad, ja ir iespējotas naudas plūsmas prognozes.</td>
</tr>
<tr>
<td>PVN priekšapmaksām</td>
<td><p>Atlasiet kontu pārdošanas nodoklim tādiem maksājumiem, kas tiek saņemti avansā.</p>
<p><strong>Piezīme.</strong> Izmantojiet lapu Debitoru <b>parādu parametri,</b> lai norādītu grāmatošanas metodi, kas tiek izmantota, kad maksājums ir atzīmēts kā priekšapmaksa.</p>
</td>
</tr>
<tr>
<td>Atlaižu konta saistības</td>
<td>Atlasiet virsgrāmatas kontu atlaižu saistībām.</td>
</tr>
<tr>
<td>Atgādinājuma vēstuļu sērija</td>
<td>Atlasiet identifikatoru atgādinājuma vēstuļu sērijai, ko izmantot debitoriem, kuriem ir piešķirta šī grāmatošanas metode.</td>
</tr>
<tr>
<td>Soda naudas kods</td>
<td>Atlasiet soda naudas kodu, ko izmantot soda naudas aprēķināšanai debitoriem, kuriem ir piešķirta šī grāmatošanas metode.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Grāmatošanas piemēri

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri ar galvenajiem kontiem un aprakstiem. Kolonna **Debets** /kredīts norāda, vai darbība parasti ir debets vai kredīts, vai arī dažos gadījumos var grāmatot. Kolonna **Klīringa** konts norāda, ka grāmatošanas tips ir klīringa konts. Tas nozīmē, ka šajā kontā grāmatotā summa tiek automātiski atcelta, grāmatojot vēlāku darbību. 

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Debets/kredīts | Dzēšanas konts | Apraksts |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Debitora bilance | 130100 | Debitoru parādu tirdzniecība | Līdzeklis | Abi | Nē | Norādiet kontu laukā **Summu** konts.|
| Nav | 110110 | Bankas konts | Līdzeklis | Abi | Nē | Norādiet galveno kontu maksājumu **likviditātes kontā**. Šis konts netiek izmantots grāmatošanai. To izmanto tikai naudas plūsmas prognozēšanai. |
| PVN priekšapmaksām | 202900 | PVN klīrings | Saistības | Abi | Jā | Atlasiet kontu pārdošanas nodoklim tādiem maksājumiem, kas tiek saņemti avansā. |
| Atlaižu konta saistības | 250600 | Atliktie ieņēmumi un atlaides | Saistības | Abi | Jā | Atlasiet Virsgrāmatas kontu atlaižu saistībām.|     

### <a name="table-restrictions"></a>Tabulu ierobežojumi

Transakcijām, kam ir atlasītā grāmatošanas metode, norādiet, vai šis transakcijas tiks segtas automātiski, vai tiks aprēķināta soda nauda, un vai tiks izveidotas atgādinājuma vēstules. Varat arī atlasīt kontu, kas tiks izmantots, kad tiek slēgtas transakcijas ar atlasīto grāmatošanas metodi.

Lai iestatītu savu grāmatošanas metodi, norādiet šādas vērtības:

| Lauks                 | Apraksts                                           |
|-----------------------|-------------------------------------------------------|
| Segšana        | Atlasiet šo pārslēgu, lai iespējotu automātisko nosegšanu transakcijām ar šo grāmatošanas metodi. Ja šī pārslēgs ir notīrīts, manuāli jānosedz darbības, **izmantojot** lapu Nosegt atvērtās darbības vai **Ievadīt debitoru maksājumus**. |
| Intereses          | Atzīmējiet šo pārslēgu, ja debitoru kontiem, kas izmanto šo metodi, soda nauda ir jāaprēķina nenokārtotām bilancēm. Ja šī pārslēga atzīme ir notīrīta, soda nauda šiem debitoriem netiks aprēķināta.                                           |
| Parādu piedziņas vēstule | Atzīmējiet šo pārslēgu, ja debitoru kontiem, kas izmanto šo metodi, ir nepieciešams ģenerēt atgādinājuma vēstules. Ja šī pārslēga atzīme ir notīrīta, atgādinājuma vēstules šiem debitoriem netiks ģenerētas.                                                 |
| Aizvērt             | Atlasiet kādu grāmatošanas metodi, kuru mainīt, kad tiek slēgtas transakcijas ar šo grāmatošanas metodi. Darbība tiek uzskatīta par aizvērtu, kad tā ir pilnībā nosegta.             |



Plašāku informāciju skatiet šeit: [Debitoru maksājumu pārskats](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
