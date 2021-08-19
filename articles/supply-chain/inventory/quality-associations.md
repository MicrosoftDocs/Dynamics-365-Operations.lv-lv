---
title: Kvalitātes piesaistes
description: Šajā tēmā aprakstīts, kā jūs varat izmantot kvalitātes saistības Microsoft Dynamics 365 Supply Chain Management, lai automātiski izveidotu kvalitātes pasūtījumus, kas ir saistīti ar jūsu pārdošanas, pirkšanas un ražošanas procesiem.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0705af8f8c40db82e412f294f45f704b7a628c1ced679cef25ce77d49642feb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724848"
---
# <a name="quality-associations"></a>Kvalitātes piesaistes

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā jūs varat izmantot kvalitātes saistības Microsoft Dynamics 365 Supply Chain Management, lai automātiski izveidotu kvalitātes pasūtījumus, kas ir saistīti ar jūsu pārdošanas, pirkšanas un ražošanas procesiem.

Kvalitātes saistība ģenerētajam kvalitātes pārbaudes pasūtījumam definē visu tālāk norādīto informāciju.

- Transakcijas notikums
- Testu kopa, kas šiem krājumiem ir jāveic
- Pieņemamais kvalitātes līmenis (acceptable quality level - AQL)
- Iztveršanas plāns

Ir jādefinē kvalitātes piesaiste katrai biznesa procesā ietvertajai variācijai, kam ir automātiski jāveido kvalitātes pārbaudes pasūtījumi. Piemēram, kvalitātes pārbaudes pasūtījumu var ģenerēt biznesa procesos, kas paredzēti pirkšanas pasūtījumiem, karantīnas pasūtījumiem, pārdošanas pasūtījumiem un ražošanas pasūtījumiem.

## <a name="working-with-quality-associations"></a>Darbs ar kvalitātes saistībām

Biznesa process, kas izmanto kvalitātes saistību, var būt saistīts ar dažādiem avota dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem vai ražošanas pasūtījumiem.

Katrs kvalitātes saistības ieraksts nosaka testu kopu, pieņemamās kvalitātes līmeni (AQL) un iztveršanas plānu, kas tiek lietoti ģenerētajiem kvalitātes pārbaudes pasūtījumiem. Katrai biznesa procesa variācijai jums ir jādefinē kvalitātes saistības ieraksts. Piemēram, varat iestatīt kvalitātes saistību, kas ģenerē kvalitātes pārbaudes pasūtījumu, kad tiek atjaunināta pirkšanas pasūtījuma produktu ieejas plūsma. Atkarībā no izpildes plāna iestatījumiem pats aktivizēšanas process var tikt bloķēts, kamēr ir atvērts kvalitātes pasūtījums. Alternatīvi sekojošie procesi, piemēram, pirkšanas pasūtījuma rēķina izrakstīšana, var tikt bloķēti.

> [!NOTE]
> Kamēr pastāv atvērti kvalitātes pārbaudes pasūtījumi, krājumu daudzumi tiek automātiski bloķēti no izsniegšanas. Atkarībā no lauka **Pilna bloķēšana** iestatījuma lapā **Krājumu iztveršana**, šis daudzums ir vai nu kvalitātes pasūtījumā norādītais daudzums, vai pirmdokumenta rindā norādītais daudzums. Papildinformāciju skatiet [Kvalitātes pārvaldības krājumu iztveršana](quality-item-sampling.md).

Noteiktam biznesa procesam kvalitātes saistības ieraksts identificē notikumu un nosacījumus, kādiem tiek ģenerēts kvalitātes pārbaudes pasūtījums. Nosacījumi var attiekties uz vietu vai juridisko personu. Kvalitātes pārbaudes pasūtījumu, kur ir iesaistīti destruktīvie testi, var ģenerēt tikai tad, ja attiecīgajam notikumam pastāv rīcībā esoši krājumi.

Lai strādātu ar kvalitātes saistībām, dodieties uz **Krājumu pārvaldība \> Iestatījums \> Kvalitātes kontrole \> Kvalitātes saistības**. Nākamajos piemēros ir parādīts, kā kvalitātes saistības ieraksts tiek definēts katra darījumu procesa variācijām. Katram piemēram nākamajā tabulā ir sniegts kopsavilkums par kvalitātes saistības ieraksta definētajiem notikumiem un nosacījumiem.

<table>
<thead>
<tr>
<th>Atsauces veids</th>
<th>Notikuma veids</th>
<th>Izpilde</th>
<th>Notikumu aizturēšana</th>
<th>Dokumenta atsauce</th>
</tr>
</thead>
<tbody>
<tr>
<td>Krājumi</td>
<td>Nav attiecināms</td>
<td>Nav attiecināms</td>
<td>Nav</td>
<td>Visi</td>
</tr>
<tr>
<td rowspan="7">Pārdošana</td>
<td rowspan="4">Izdošanas process ir ieplānots</td>
<td rowspan="4">Pirms</td>
<td>Nav</td>
<td rowspan="22">Konkrēts ID, Grupa vai tikai Visi</td>
</tr>
<tr>
<td>Izdošanas process</td>
</tr>
<tr>
<td>Pavadzīme</td>
</tr>
<tr>
<td>Rēķins</td>
</tr>
<tr>
<td rowspan="3">Pavadzīme</td>
<td rowspan="3">Pirms</td>
<td>Nav</td>
</tr>
<tr>
<td>Pavadzīme</td>
</tr>
<tr>
<td>Rēķins</td>
</tr>
<tr>
<td rowspan="15">Pirkšana</td>
<td rowspan="7">Saņemšanas saraksts</td>
<td rowspan="4">Pirms</td>
<td>Nav</td>
</tr>
<tr>
<td>Saņemšanas saraksts</td>
</tr>
<tr>
<td>Produktu ieejas plūsma</td>
</tr>
<tr>
<td>Rēķins</td>
</tr>
<tr>
<td rowspan="3">Pēc</td>
<td>Nav</td>
</tr>
<tr>
<td>Produktu ieejas plūsma</td>
</tr>
<tr>
<td>Rēķins</td>
</tr>
<tr>
<td rowspan="3">Reģistrācija</td>
<td rowspan="3">Nav attiecināms</td>
<td>Nav</td>
</tr>
<tr>
<td>Produktu ieejas plūsma</td>
</tr>
<tr>
<td>Rēķins</td>
</tr>
<tr>
<td rowspan="5">Produktu ieejas plūsma</td>
<td rowspan="3">Pirms</td>
<td>Nav</td>
</tr>
<tr>
<td>Produktu ieejas plūsma</td>
</tr>
<tr>
<td>Rēķins</td>
</tr>
<tr>
<td rowspan="2">Pēc</td>
<td>Nav</td>
</tr>
<tr>
<td>Rēķins</td>
</tr>
<tr>
<td rowspan="8">Ražošana</td>
<td rowspan="3">Reģistrācija</td>
<td rowspan="3">Nav attiecināms</td>
<td>Nav</td>
<td rowspan="12">Visi</td>
</tr>
<tr>
<td>Reģistrēt pabeigšanu</td>
</tr>
<tr>
<td>Beigt</td>
</tr>
<tr>
<td rowspan="5">Reģistrēt pabeigšanu</td>
<td rowspan="3">Pirms</td>
<td>Nav</td>
</tr>
<tr>
<td>Reģistrēt pabeigšanu</td>
</tr>
<tr>
<td>Beigt</td>
</tr>
<tr>
<td rowspan="2">Pēc</td>
<td>Nav</td>
</tr>
<tr>
<td>Beigt</td>
</tr>
<tr>
<td rowspan="4">Karantīna</td>
<td rowspan="3">Reģistrēt pabeigšanu</td>
<td rowspan="2">Pirms</td>
<td>Reģistrēt pabeigšanu</td>
</tr>
<tr>
<td>Beigt</td>
</tr>
<tr>
<td>Pēc</td>
<td>Beigt</td>
</tr>
<tr>
<td>Beigt</td>
<td>Pirms</td>
<td>Beigt</td>
</tr>
<tr>
<td rowspan="3">Maršruta operācija</td>
<td rowspan="3">Ziņot kā pabeigtu</td>
<td rowspan="2">Pirms</td>
<td>Neviens</td>
<td rowspan="3">Noteikts ID, Grupa vai Visi, un raksturīgs Resurss, Grupa vai Visi</td>
</tr>
<tr>
<td>Ziņot kā pabeigtu</td>
</tr>
<tr>
<td>Pēc</td>
<td>Neviens</td>
</tr>
<tr>
<td rowspan="3">Līdzprodukta ražošana</td>
<td>Reģistrācija</td>
<td>Nav attiecināms</td>
<td rowspan="3">Neviens</td>
<td rowspan="3">Visu</td>
</tr>
<tr>
<td rowspan="2">Ziņot kā pabeigtu</td>
<td>Pirms</td>
</tr>
<tr>
<td>Pēc</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Līdzeklis *Noliktavas procesu kvalitātes pārvaldība* pievieno iespējas kvalitātes pārbaudes pasūtījumu apstrādei ražošanai, kur lauks **Notikuma veids**, kas iestatīts uz *Ziņot, kad pabeigts* un lauks **Izpilde** iestatīts uz *Pēc*, un pirkšanai, kur lauks **Notikuma veids**, kas iestatīts uz *Reģistrāciju*. Papildinformāciju skatiet [Noliktavas procesu kvalitātes pārvaldība](quality-management-for-warehouses-processes.md).

Nākamajā tabulā ir plašāka informācija par to, kā kvalitātes pārbaudes pasūtījumus var ģenerēt specifiskiem procesu tipiem.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Procesa tips</th>
<th>Kad kvalitātes pārbaudes pasūtījumus var ģenerēt automātiski</th>
<th>Kad kvalitātes pārbaudes pasūtījums var ģenerēt, ja ir nepieciešama destruktīvā testēšana</th>
<th>Nosacījuma informācija</th>
<th>Manuālas ģenerēšanas informācija</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pirkšanas pasūtījums</td>
<td>Pirms vai pēc tam, kad saņemtajam materiālam tiek grāmatots saņemšanas saraksts vai produktu ieejas plūsma</td>
<td>Pēc tam, kad saņemtajam materiālam tiek grāmatota produktu ieejas plūsma, jo šim materiālam ir jābūt pieejamam destruktīvajai testēšanai</td>
<td>Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</td>
<td>Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pirkšanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</td>
</tr>
<tr>
<td>Karantīnas pasūtījums</td>
<td>Pirms vai pēc tam, kad karantīnas pasūtījums tiek ziņots kā pabeigts vai beidzies</td>
<td>Nevar ģenerēt kvalitātes pārbaudes pasūtījumus, kam ir nepieciešami destruktīvie testi. Tiek pieņemts, ka karantīnas pasūtījuma funkcionalitāte veic atbrīvošanos no iznīcinātā materiāla.</td>
<td>Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu, krājumu vai kreditoru, vai šo nosacījumu kombināciju.</td>
<td>Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst karantīnas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</td>
</tr>
<tr>
<td>Pārdošanas pasūtījums</td>
<td>Pirms plānotas izdošanas procesa vai pavadzīmes atjaunināšanas krājumiem, kas tiek sūti</td>
<td>Jebkurā posmā</td>
<td>Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu, krājumu vai debitoru, vai šo nosacījumu kombināciju.</td>
<td>Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst pārdošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</td>
</tr>
<tr>
<td>Ražošanas pasūtījums</td>
<td>Pirms vai pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</td>
<td>Pēc tam, kad ražošanas pasūtījumam tiek ziņota pabeigta kvalitāte</td>
<td>Kvalitātes pārbaudes pasūtījuma pieprasījums var norādīt noteiktu vietu vai krājumu, vai kreditoru, vai šo nosacījumu kombināciju.</td>
<td>Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst ražošanas pasūtījumam, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</td>
</tr>
<tr>
<td>Ražošanas pasūtījums, kuram ir maršruta operācija</td>
<td>Pirms vai pēc tam, kad kādai operācijai ir pabeigta atskaite</td>
<td>Pēc tam, kad pēdējai operācijai ražošana ir ziņota kā pabeigta</td>
<td>Kvalitātes pārbaudes pasūtījuma pieprasījums ar norādīt noteiktu vietu, krājumu vai operācijas resursu, vai arī šo nosacījumu kombināciju.</td>
<td>Manuāli ģenerēts kvalitātes pārbaudes pasūtījums, kas atbilst maršruta operācijai, var izmantot informāciju kvalitātes saistības ierakstā, piemēram, testēšanas iztveršanas plānu.</td>
</tr>
<tr>
<td>Krājums</td>
<td>Kvalitātes pārbaudes pasūtījumu nevar automātiski ģenerēt transakcijai krājumu žurnālā vai arī pārsūtīšanas pasūtījuma transakcijām.</td>
<td></td>
<td></td>
<td>Krājumadaudzumam noliktavā ir manuāli jāizveido kvalitātes pārbaudes pasūtījums. Fiziski rīcībā esošie krājumi ir obligāti.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Automātisku kvalitātes pasūtījumu izveidošanas piemēri

### <a name="purchasing"></a>Pirkšana

Pirkšanā, ja iestatāt lauku **Notikuma veids** uz *Produktu ieejas plūsma* un lauku **Izpilde**, kas atrodas lapā *Kvalitātes piesaistes* uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.

- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Jā*, katrai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu un iestatījumiem krājumu iztveršanā. Katru reizi, kad tiek saņemts daudzums atbilstoši pirkšanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko saņemto daudzumu.
- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Nē*, pirmajai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu. Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no izsekošanas dimensijām. Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākām ieejas plūsmām atbilstoši pirkšanas pasūtījumam.

### <a name="production"></a>Ražošana

Ražošanā, ja iestatāt lauku **Notikuma veids** uz *Norādīts kā pabeigts* un lauku **Izpilde**, kas atrodas lapā *Kvalitātes piesaistes* uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.

- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Jā*, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz katru pabeigto daudzumu un iestatījumiem krājumu iztveršanā. Katru reizi, kad tiek daudzums tiek norādīts kā pabeigts atbilstoši ražošanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko pabeigto daudzumu. Šī ģenerēšanas loģika ir saskaņota ar pirkšanu.
- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz *Nē*, pirmajā reizē, kad daudzums tiek norādīts kā pabeigts, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz pabeigto daudzumu. Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no krājumu iztveršanas izsekošanas dimensijām. Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākajiem pabeigtajiem daudzumiem.

<table>
<thead>
<tr>
<th>Kvalitātes specifikācija</th>
<th>Pēc atjauninātā daudzuma</th>
<th>Pēc izsekošanas dimensijas</th>
<th>Rezultāts</th>
</tr>
</thead>
<tbody>
<tr>
<td>Procentuālā attiecība: 10 %</td>
<td>Jā</td>
<td>
<p>Paketes numurs: Nr.</p>
<p>Sērijas numurs: Nr.</p>
</td>
<td>
<p>Pasūtījuma daudzums: 100</p>
<ol>
<li>Pabeigto krājumu daudzums 30
<ul>
<li>1. kvalitātes pārbaudes pasūtījums 3 vienumiem (10 % no 30)</li>
</ul>
</li>
<li>Pabeigto krājumu daudzums 70
<ul>
<li>2. kvalitātes pārbaudes pasūtījums 7 vienumiem (10 % no atlikušā pasūtījuma daudzuma, kas šajā gadījumā ir 70)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fiksēts daudzums: 1</td>
<td>Nr.</td>
<td>
<p>Paketes numurs: Nr.</p>
<p>Sērijas numurs: Nr.</p>
</td>
<td>Pasūtījuma daudzums: 100
<ol>
<li>Pabeigto krājumu daudzums 30
<ul>
<li>1. kvalitātes pārbaudes pasūtījums vienumam 1 (pirmajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība ir 1)</li>
<li>2. kvalitātes pārbaudes pasūtījums vienumam 1 (atlikušajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība joprojām ir 1)</li>
</ul>
</li>
<li>Pabeigto krājumu daudzums 10
<ul>
<li>Nav izveidoti kvalitātes pārbaudes pasūtījumi.</li>
</ul>
</li>
<li>Pabeigto krājumu daudzums 60
<ul>
<li>Nav izveidoti kvalitātes pārbaudes pasūtījumi.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fiksēts daudzums: 1</td>
<td>Jā</td>
<td>
<p>Partijas numurs: Jā</p>
<p>Sērijas numurs: Jā</p>
</td>
<td>
<p>Pasūtījuma daudzums: 10</p>
<ol>
<li>Pabeigts 3: 1 partijas numuram b1, sērijas numuram s1; 1 partijas numuram b2, sērijas numuram s2 un 1 partijas numuram b3, sērijas numuram s3
<ul>
<li>1. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b1, sērijas numura s1</li>
<li>2. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b2, sērijas numura s2</li>
<li>3. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b3, sērijas numura s3</li>
</ul>
</li>
<li>Pabeigts 2: 1 partijas numuram b4, sērijas numuram s4 un 1 partijas numuram b5, sērijas numuram s5
<ul>
<li>4. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b4, sērijas numura s4</li>
<li>5. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b5, sērijas numura s5</li>
</ul>
</li>
</ol>
<p><strong>Piezīme:</strong> partiju var izmantot atkārtoti.</p>
</td>
</tr>
<tr>
<td>Fiksēts daudzums: 2</td>
<td>Nr.</td>
<td>
<p>Partijas numurs: Jā</p>
<p>Sērijas numurs: Jā</p>
</td>
<td>
<p>Pasūtījuma daudzums: 10</p>
<ol>
<li>Pabeigts 4: 1 partijas numuram b1, sērijas numuram s1; 1 partijas numuram b2, sērijas numuram s2 un 1 partijas numuram b3, sērijas numuram s3; un 1 partijas numuram b4, sērijas numuram s4
<ul>
<li>1. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b1, sērijas numura s1</li>
<li>2. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b2, sērijas numura s2</li>
<li>3. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b3, sērijas numura s3</li>
<li>4. kvalitātes pārbaudes pasūtījums 1 vienumam no partijas numura b4, sērijas numura s4</li>
</ul>
<ul>
<li>Kvalitātes pārbaudes pasūtījums 5 vienumam 2 bez atsauces uz partijas numuru un sērijas numuru</li>
</ul>
</li>
<li>Pabeigts 6: 1 partijas numuram b5, sērijas numuram s5; 1 partijas numuram b6, sērijas numuram s6; 1 partijas numuram b7, sērijas numuram s7; 1 partijas numuram b8, sērijas numuram s8; 1 partijas numuram b9, sērijas numuram s9; un 1 partijas numuram b10, sērijas numuram s10
<ul>
<li>Nav izveidoti kvalitātes pārbaudes pasūtījumi.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības procesi](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
