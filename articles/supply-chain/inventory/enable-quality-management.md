---
title: Kvalitātes pārvaldības apskats
description: Šajā tēmā ir aprakstīts, kā varat izmantot kvalitātes pārvaldību programmā Dynamics 365 Supply Chain Management, lai palīdzētu uzlabot preču kvalitāti savā piegādes ķēdē.
author: perlynne
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23406f68e6ed317025a072eb3377392f0b129626
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829936"
---
# <a name="quality-management-overview"></a>Kvalitātes pārvaldības apskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā varat izmantot kvalitātes pārvaldību programmā Dynamics 365 Supply Chain Management, lai palīdzētu uzlabot preču kvalitāti savā piegādes ķēdē.

Kvalitātes pārvaldība jums var palīdzēt pārvaldīt apgrozījumu laikus, kad strādājat ar nekondīcijas precēm, neatkarīgi no to izcelsmes vietas. Tā kā diagnostikas tipi ir saistīti ar korekciju ziņošanu, Supply Chain Management var plānot uzdevumus, lai izlabotu problēmas un novērstu to atkārtošanos.

Papildus neatbilstības pārvaldības funkcionalitātei kvalitātes pārvaldība ietver arī funkcionalitāti problēmu izsekošanai pēc problēmas tipa (pat iekšējām problēmām) un risinājumu identificēšanai īstermiņā vai ilgtermiņā. Statistika par galvenajiem darba kvalitātes rādītājiem (KPI) sniedz ieskatu par iepriekšējām neatbilstības problēmām un risinājumiem, kas tika izmantoti to labošanai. Vēsturiskos datus varat izmantot, lai pārskatītu iepriekšējo kvalitātes pasākumu efektivitāti un noteiktu, kuri pasākumi ir piemēroti turpmākai izmantošanai.

Kad iestatāt kvalitātes saistību, Supply Chain Management var ģenerēt kvalitātes pārbaudes pasūtījumus dažādiem biznesa procesiem, notikumiem un nosacījumiem. Šāda kvalitātes saistība var attiekties uz noteiktu krājumu, noteiktu krājumu grupu vai visiem krājumiem.

## <a name="examples-of-the-use-of-quality-management"></a>Kvalitātes pārvaldības lietošanas piemēri
Kvalitātes pārvaldība ir elastīga, un to var ieviest dažādos veidos, lai atbilstu noteiktu piegādes ķēdes darbību līmeņu prasībām. Nākamajos piemēros ir parādīti šādu līdzekļu iespējamie lietojumi:

-   Automātiski uzsākt kvalitātes kontroles procesu, pamatojoties uz iepriekš definētiem kritērijiem (noliktavā reģistrējot kādu pirkšanas pasūtījumu no specifiska kreditora).
-   Bloķēt krājumus pārbaudes laikā, lai nepieļautu, ka tiek lietoti neapstiprināti krājumi (pirkšanas pasūtījuma daudzumu pilnīga bloķēšana).
-   Kā daļu no kvalitātes saistības lietot krājuma iztveršanu, lai definētu pašreizējo fizisko krājumu daudzumu, kas ir jāpārbauda. Paraugu nodošana var būt balstīta uz fiksētiem daudzumiem, procentiem vai pilnu numura zīmi.

> [!NOTE]
> _Noliktavas procesu kvalitātes pārvaldības_ līdzeklis paplašina kvalitātes pārvaldības iespējas. Ja lietojat šo līdzekli, skatiet sadaļu [Noliktavas procesu kvalitātes pārvaldība](quality-management-for-warehouses-processes.md) kā piemēu, kā kvalitātes pārvaldība darbojas, kad tā ir iespējota.

-   Izveidot kvalitātes pārbaudes pasūtījumus daļējām ieejas plūsmām. Lai izveidotu kvalitātes pārbaudes pasūtījumu, kura pamatā ir daudzums, kas ir fiziski saņemts ar pasūtījumu, formā **Krājumu iztveršana** ir jāatzīmē izvēles rūtiņa **Pēc atjauninātā daudzuma**.
-   Izveidot testa tipus, kas ietver minimālās, maksimālās un mērķa testa vērtības, un veikt testēšanu kvalitātei pret kvantitāti, kur ir iepriekš definēti validēšanas rezultāti.
-   Norādīt pieņemamu kvalitātes līmeni (Acceptable Quality Level — AQL), lai kontrolētu kvalitātes mērījumu tolerances.
-   Norādīt pārbaudes operācijai nepieciešamos resursus, piemēram, testa apgabalu un testa instrumentus.

## <a name="working-with-quality-associations"></a>Darbs ar kvalitātes saistībām
Biznesa process, kas izmanto kvalitātes saistību, var būt saistīts ar dažādiem avota dokumentiem, piemēram, pirkšanas pasūtījumiem, pārdošanas pasūtījumiem vai ražošanas pasūtījumiem.

Katrs kvalitātes saistības ieraksts nosaka testu kopu, pieņemamās kvalitātes līmeni (AQL) un iztveršanas plānu, kas tiek lietoti ģenerētajiem kvalitātes pārbaudes pasūtījumiem. Katrai biznesa procesa variācijai jums ir jādefinē kvalitātes saistības ieraksts. Piemēram, varat iestatīt kvalitātes saistību, kas ģenerē kvalitātes pārbaudes pasūtījumu, kad tiek atjaunināta pirkšanas pasūtījuma produktu ieejas plūsma. Atkarībā no izpildes plāna iestatījumiem pašu aktivizēšanas procesu var bloķēt, kamēr pastāv atvērts kvalitātes pārbaudes pasūtījums, vai iespējams bloķēt nākamos procesus, piemēram, pirkšanas pasūtījumu rēķinu izrakstīšanu.

**Piezīme.** Kamēr pastāv atvērti kvalitātes pārbaudes pasūtījumi, krājumu daudzumi tiek automātiski bloķēti no izsniegšanas. Atkarībā no iestatījuma **Pilna bloķēšana** lapā **Krājumu iztveršana**, šis daudzums ir vai nu kvalitātes pasūtījumā norādītais daudzums, vai pirmdokumenta rindā norādītais daudzums.

Noteiktam biznesa procesam kvalitātes saistības ieraksts identificē notikumu un nosacījumus, kādiem tiek ģenerēts kvalitātes pārbaudes pasūtījums. Nosacījumi var attiekties uz vietu vai juridisko personu. Kvalitātes pārbaudes pasūtījumu, kur ir iesaistīti destruktīvie testi, var ģenerēt tikai tad, ja attiecīgajam notikumam pastāv rīcībā esoši krājumi.

Nākamajos piemēros ir parādīts, kā kvalitātes saistības ieraksts tiek definēts katra darījumu procesa variācijām. Katram piemēram nākamajā tabulā ir sniegts kopsavilkums par kvalitātes saistības ieraksta definētajiem notikumiem un nosacījumiem.

<table>
<tbody>
<tr>
<th>Atsauces veids</th>
<th>Notikuma veids</th>
<th>Izpilde</th>
<th>Notikumu aizturēšana</th>
<th>Dokumenta atsauce</th>
</tr>
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
<td rowspan="3">Reģistrēt pabeigšanu</td>
<td rowspan="2">Pirms</td>
<td>Nav</td>
<td rowspan="3">Noteikts ID, Grupa vai Visi, un Resursam raksturīgs, Grupa vai Visi</td>
</tr>
<tr>
<td>Reģistrēt pabeigšanu</td>
</tr>
<tr>
<td>Pēc</td>
<td>Nav</td>
</tr>
<tr>
<td rowspan="3">Līdzprodukta ražošana</td>
<td>Reģistrācija</td>
<td>Nav attiecināms</td>
<td rowspan="3">Nav</td>
<td rowspan="3">Visi</td>
</tr>
<tr>
<td rowspan="2">Reģistrēt pabeigšanu</td>
<td>Pirms</td>
</tr>
<tr>
<td>Pēc</td>
</tr>
</tbody>
</table>

Nākamajā tabulā ir plašāka informācija par to, kā kvalitātes pārbaudes pasūtījumus var ģenerēt specifiskiem procesu tipiem.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Procesa tips</th>
<th>Kad kvalitātes pārbaudes pasūtījumus var ģenerēt automātiski</th>
<th>Kad kvalitātes pārbaudes pasūtījums var ģenerēt, ja ir nepieciešama destruktīvā testēšana</th>
<th>Nosacījuma informācija</th>
<th>Manuālas ģenerēšanas informācija</th>
</tr>
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
<td>Nevar&#39;ģenerēt kvalitātes pārbaudes pasūtījumus, kam ir nepieciešami destruktīvi testi. Tiek&#39;pieņemts, ka karantīnas pasūtījuma funkcionalitāte nodrošina atbrīvošanos no iznīcinātā materiāla.</td>
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
<td>Kvalitātes pārbaudes pasūtījuma pieprasījums var atainot noteiktu vietu vai krājumu, vai arī šo abu nosacījumu kombināciju.</td>
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
<td>Krājumi</td>
<td>Kvalitātes pārbaudes pasūtījumu nevar automātiski ģenerēt transakcijai krājumu žurnālā vai arī pārsūtīšanas pasūtījuma transakcijām.</td>
<td></td>
<td></td>
<td>Krājuma&#39;daudzumam noliktavā ir manuāli jāizveido kvalitātes pārbaudes pasūtījums. Fiziski rīcībā esošie krājumi ir obligāti.</td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a>Kvalitātes pārbaudes pasūtījuma automātiskās ģenerēšanas piemēri

### <a name="purchasing"></a>Pirkšana

Pirkšanā, ja iestatāt lauku **Notikuma veids** uz **Produktu ieejas plūsma** un lauku **Izpilde**, kas atrodas lapā **Kvalitātes piesaistes** uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus. 

- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Jā**, katrai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu un iestatījumiem krājumu iztveršanā. Katru reizi, kad tiek saņemts daudzums atbilstoši pirkšanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko saņemto daudzumu.
- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Nē**, pirmajai saņemšanai atbilstoši pirkšanas pasūtījumam tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz saņemto daudzumu. Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no izsekošanas dimensijām. Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākām ieejas plūsmām atbilstoši pirkšanas pasūtījumam.

### <a name="production"></a>Ražošana

Ražošanā, ja iestatāt lauku **Notikuma veids** uz **Norādīts kā pabeigts** un lauku **Izpilde**, kas atrodas lapā **Kvalitātes piesaistes** uz **Pēc**, jūs iegūstat tālāk norādītos rezultātus.

- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Jā**, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz katru pabeigto daudzumu un iestatījumiem krājumu iztveršanā. Katru reizi, kad tiek daudzums tiek norādīts kā pabeigts atbilstoši ražošanas pasūtījumam, tiek ģenerēti jauni kvalitātes pārbaudes pasūtījumi, pamatojoties uz tikko pabeigto daudzumu. Šī ģenerēšanas loģika ir saskaņota ar pirkšanu.
- Ja opcija **Pēc atjauninātā daudzuma** ir iestatīta uz **Nē**, pirmajā reizē, kad daudzums tiek norādīts kā pabeigts, tiek ģenerēts kvalitātes pārbaudes pasūtījums, pamatojoties uz pabeigto daudzumu. Turklāt viens vai vairāki kvalitātes pārbaudes pasūtījumi tiek izveidoti, pamatojoties uz atlikušo daudzumu atkarībā no krājumu iztveršanas izsekošanas dimensijām. Kvalitātes pārbaudes pasūtījumi netiek ģenerēti turpmākajiem pabeigtajiem daudzumiem.

<table>
<tbody>
<tr>
<th>Kvalitātes specifikācija</th>
<th>Pēc atjauninātā daudzuma</th>
<th>Pēc izsekošanas dimensijas</th>
<th>Rezultāts</th>
</tr>
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
<li>Kvalitātes pārbaudes pasūtījums #1 3 vienumiem (10 % no 30)</li>
</ul>
</li>
<li>Pabeigto krājumu daudzums 70
<ul>
<li>Kvalitātes pārbaudes pasūtījums #2 7 vienumiem (10 % no atlikušā pasūtījuma daudzuma, kas šajā gadījumā ir vienāds ar 70)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fiksēts daudzums: 1</td>
<td>Nē</td>
<td>
<p>Paketes numurs: Nr.</p>
<p>Sērijas numurs: Nr.</p>
</td>
<td>Pasūtījuma daudzums: 100
<ol>
<li>Pabeigto krājumu daudzums 30
<ul>
<li>Kvalitātes pārbaudes pasūtījums #1 vienumam 1 (pirmajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība ir 1)</li>
<li>Kvalitātes pārbaudes pasūtījums #2 vienumam 1 (atlikušajam daudzumam, kas ir norādīts kā pabeigts, kura fiksētā vērtība joprojām ir 1)</li>
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
<li>Norādīt kā pabeigtu vienumam 3: 1 #b1 #s1; 1 #b2, #s2; un 1 #b3, #s3
<ul>
<li>Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1</li>
<li>Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2</li>
<li>Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3</li>
</ul>
</li>
<li>Norādīt kā pabeigtu vienumam 2: 1 #b4, #s4 un 1 #b5, #s5
<ul>
<li>Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4</li>
<li>Kvalitātes pārbaudes pasūtījums #5 1 vienumam no partijas #b5, sērijas #s5</li>
</ul>
</li>
</ol>
<p><strong>Piezīme:</strong> partiju var izmantot atkārtoti.</p>
</td>
</tr>
<tr>
<td>Fiksēts daudzums: 2</td>
<td>Nē</td>
<td>
<p>Partijas numurs: Jā</p>
<p>Sērijas numurs: Jā</p>
</td>
<td>
<p>Pasūtījuma daudzums: 10</p>
<ol>
<li>Norādīt kā pabeigtu vienumam 4: 1 #b1 #s1; 1 #b2, #s2; un 1 #b3, #s3 un 1 #b4, #s4
<ul>
<li>Kvalitātes pārbaudes pasūtījums #1 1 vienumam no partijas #b1, sērijas #s1</li>
<li>Kvalitātes pārbaudes pasūtījums #2 1 vienumam no partijas #b2, sērijas #s2</li>
<li>Kvalitātes pārbaudes pasūtījums #3 1 vienumam no partijas #b3, sērijas #s3</li>
<li>Kvalitātes pārbaudes pasūtījums #4 1 vienumam no partijas #b4, sērijas #s4</li>
</ul>
<ul>
<li>Kvalitātes pārbaudes pasūtījums #5 vienumam 2 bez atsauces uz partijas un sērijas numuru</li>
</ul>
</li>
<li>Norādīt kā pabeigtu vienumam 6: 1 #b5 #s5; 1 #b6, #s6; 1 #b7, #s7; 1 #b8, #s8; 1 #b9, #s9 un 1 #b10, #s10
<ul>
<li>Nav izveidoti kvalitātes pārbaudes pasūtījumi.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> *Noliktavas procesu kvalitātes pārvaldības* līdzeklis pievieno iespējas kvalitātes pārbaudes pasūtījumu apstrādei ražošanai ar **Notikuma veidu**, kas iestatīts uz *Ziņot, kad pabeigts* un **Izpilde** iestatīts uz *Pēc*, un pirkšanai ar **Notikuma veidu**, kas iestatīts uz *Reģistrāciju*. Detalizētu informāciju skatiet [Noliktavas procesu kvalitātes pārvaldība](quality-management-for-warehouses-processes.md).

## <a name="quality-management-pages"></a>Kvalitātes pārvaldības lapas
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Lapa</th>
<th>apraksts</th>
<th>Paraugs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kvalitātes piesaistes</td>
<td>Skatiet šī raksta iepriekšējās sadaļas.</td>
<td>Kvalitātes saistība ģenerētajam kvalitātes pārbaudes pasūtījumam definē visu tālāk norādīto informāciju.
<ul>
<li>Transakcijas notikums</li>
<li>Testu kopa, kas šiem krājumiem ir jāveic</li>
<li>Pieņemamais kvalitātes līmenis (AQL)</li>
<li>Iztveršanas plāns</li>
</ul>
Ir jādefinē kvalitātes piesaiste katrai biznesa procesā ietvertajai variācijai, kam ir automātiski jāveido kvalitātes pārbaudes pasūtījumi. Piemēram, kvalitātes pārbaudes pasūtījumu var ģenerēt biznesa procesos, kas paredzēti pirkšanas pasūtījumiem, karantīnas pasūtījumiem, pārdošanas pasūtījumiem un ražošanas pasūtījumiem.</td>
</tr>
<tr class="even">
<td>Testi</td>
<td>Izmantojiet šo lapu, lai definētu un skatītu atsevišķos testus, kas nosaka, vai preces atbilst kvalitātes specifikācijām. Vienu vai vairākus atsevišķus testus varat piešķirt testu grupai. Šajā gadījumā jums ir jānorāda arī testa specifiskā informācija, piemēram, pieņemamās mērījumu vērtības. Mērījumu vērtības tiek izmantotas kvantitatīvajiem testiem, un testa mainīgie tiek lietoti kvalitatīvajiem testiem.
<ul>
<li>Kvantitatīvajam testam testa tips ir <strong>Vesels skaitlis</strong> vai <strong>Daļskaitlis</strong>, un tam ir arī norādīta mērvienība. Kvalitātes specifikācijas un testa rezultāti tiek izteikti kā skaitļi.</li>
<li>Kvalitatīvajam testam testa tips ir <strong>Opcija</strong>. Kvalitatīvajiem testiem ir nepieciešama papildinformācija par testa mainīgo, kas tiek mērīts, un tā uzskaitīšanas iespējam. Kvalitātes specifikācijas un testa rezultāti tiek izteikti atbilstoši rezultātam.</li>
</ul></td>
<td>Ražošanas uzņēmums iepirktajam materiālam veic divus testus: kvantitatīvo testu par materiāla kvalitāti un kvalitatīvo testu par iepakojuma bojājumu. Uzņēmums definē papildu informāciju par kvalitātes testu, lai identificētu testa mainīgo (bojāto iepakojumu) un tā rezultātus. Uzņēmums izmanto lapu <strong>Testu grupas</strong>, lai abus testus piešķirtu testu grupai un norādītu testa specifisko informāciju. Kvalitātes pasūtījumam tiek piešķirta testa grupā, tādējādi uzņēmums var ziņot testa rezultātus par diviem testiem.</td>
</tr>
<tr class="odd">
<td>Testa grupas</td>
<td>Izmantojiet šo lapu, lai iestatītu, rediģētu un apskatītu testu grupas un atsevišķus testus, kas ir piešķirti kādai testu grupai. Augšējā rūtī ir atainotas testu grupas, bet apakšējā rūtī ir atainoti testi, kas piešķirti atlasītajai testu grupai. Jūs testu grupai piešķirat vairākus ierobežojumus, piemēram, iztveršanas plānu, pieņemamo kvalitātes līmeni (AQL) un destruktīvās testēšanas pieprasījumu. Kad atsevišķu testu piešķirat testu grupai, jūs definējat papildu informāciju, piemēram, secību, dokumentus un derīguma datumus. Kvantitatīvam testam jūsu definēta informācija ietver arī pieņemamās mērījumu vērtības. Kvalitatīvam testam šī informācija ietver testa mainīgo un noklusējuma iznākumu. Testa grupa, kas ir piešķirta kādam kvalitātes pārbaudes pasūtījumam, nosaka noklusējuma kopu ar testiem, kas ir jāizpilda norādītajam krājumam. Taču kvalitātes pārbaudes pasūtījumā testus varat pievienot, dzēst vai mainīt. Katra testa rezultāti tiek uzrādīti kvalitātes pasūtījumā.</td>
<td>Ražošanas uzņēmums definē testu grupu katrai tās kvalitātes vadlīniju variācijai. Dažādās testu grupas parāda atšķirības iztveršanas plānos, kopā izpildāmo testu kopās, pieņemamajos kvalitātes līmeņos AQL un citos faktoros. Kvantitatīvajiem testiem pastāv arī pieņemamo mērījumu vērtību atšķirības. Lai īstenotu savas kvalitātes vadlīnijas, automātiski ģenerētiem kvalitātes pārbaudes pasūtījumiem lapā <strong>Kvalitātes saistības</strong> uzņēmums piešķir testu grupu katrai kārtulai, kā arī piešķir testu grupu manuāli izveidotajiem kvalitātes pārbaudes pasūtījumiem.</td>
</tr>
<tr class="even">
<td>Krājumu kvalitātes grupas</td>
<td>Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu krājumus, kas ir piešķirti kvalitātes grupai vai kvalitātes grupām, kuras ir piešķirtas kādam krājumam. Kvalitātes grupa norāda kopējās testēšanas vajadzības krājumam. Kad lapā <strong>Testu grupas</strong> ir definētas testa prasības, varat definēt kārtulas automātiskai kvalitātes pārbaudes pasūtījumu ģenerēšanai. Lai vienkāršotu šo procesu, netiek&#39;definētas kārtulas atsevišķiem krājumiem. Tā vietā jūs definējat kārtulas kvalitātes grupai, izmantojot lapu <strong>Kvalitātes saistības</strong>. Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītai kvalitātes grupai, lai šai grupai piešķirtu atbilstošos krājumus. Varat arī izmantot lapu <strong>Krājuma kvalitātes grupas</strong> atlasītam krājumam, lai šim krājumam piešķirtu atbilstošās kvalitātes grupas.</td>
<td>Ražošanas uzņēmums iegādājas vairākus izejmateriālus, kuriem ir tādas pašas testēšanas vajadzības ienākošajai pārbaudei. Uzņēmums definē kvalitātes grupu un pēc tam piešķir krājumu numurus, kas ir saistīti ar izejmateriāliem šai grupai. Vēlāk uzņēmums iegādājas jauna tipa izejmateriālu, kuram ir tādas pašas testēšanas vajadzības. Tā vietā, lai jaunajam materiālam iestatītu jaunas testēšanas vajadzības, jaunā materiāla krājumu kodu uzņēmums pievieno jau esošajai kvalitātes grupai. Tas pats ražošanas uzņēmums ražo arī krājumus, kuriem ir tādas pašas ražošanas testēšanas vajadzības, un krājumus, kuriem ir tādas pašas vajadzības, sūta uz testēšanu pirms sūtīšanas. Uzņēmums definē divas papildu kvalitātes grupas un pēc tam piešķir atbilstošos krājumu numurus katrai grupai.</td>
</tr>
<tr class="odd">
<td>Testa mainīgie lielumi</td>
<td>Izmantojiet šo lapu, lai definētu un skatītu mainīgos, kas ir saistīti ar kādu kvalitātes testu. Katram mainīgajam varat definēt uzskaitītos iznākumus, kas apzīmē iespējamās opcijas. Testus jūs definējat lapā <strong>Testi</strong>. Kvalitatīvajiem testiem testa tipu jūs iestatāt uz <strong>Opcija</strong>. Izmantojiet lapu <strong>Testu grupas</strong>, lai testa mainīgo piešķirtu atsevišķam testam.</td>
<td>Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu. Šajā pārbaudes testā ir vairāki mainīgie. Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta. Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza.</td>
</tr>
<tr class="even">
<td>Testa mainīgo lielumu iznākumi</td>
<td>Izmantojiet šo lapu, lai iestatītu, rediģētu un skatītu iespējamos testa rezultātus ar kvalitatīvo testu saistītam testa mainīgajam. Katram iznākumam jums ir jāpiešķir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>. Jums ir jādefinē mainīgais un tā iznākumi katram kvalitatīvajam testam, kas ir definēts lapā <strong>Testi</strong>. (Kvalitatīvajiem testiem testa tips lapā <strong>Testi</strong> ir iestatīts uz <strong>Opcija</strong>.) Lai testa mainīgo un noklusējuma iznākumu piešķirtu atsevišķam kvalitatīvajam testam, izmantojiet lapu <strong>Testu grupas</strong>.</td>
<td>Ražošanas uzņēmums, kas ražo cepumus, pabeigtajam produktam izmanto pārbaudes testu. Šajā pārbaudes testā ir vairāki mainīgie. Viens mainīgais ir garša, un šī mainīgā iespējamie iznākumi ir laba vai slikta. Otrais mainīgais ir krāsa, un tā iespējamie iznākumi ir pārāk tumša, pārāk gaiša vai pareiza. Katram iznākumam tiek piešķirts ir statuss <strong>sekmīgs</strong> vai <strong>nesekmīgs</strong>. Katra mainīgā pārbaudes testa laikā pārbaudītājs ziņo testa rezultātu, izvēloties vienu no rezultātiem.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Papildu resursi
--------

[Kvalitātes pārvaldības procesi](quality-management-processes.md)

[Neatbilstības pārvaldība](enable-nonconformance-management.md)

[Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]