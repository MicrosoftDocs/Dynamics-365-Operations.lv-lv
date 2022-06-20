---
title: Iestatīt un ģenerēt pozitīvo maksājumu failus, izmantojot elektroniskos pārskatus
description: Šajā rakstā skaidrots, kā iestatīt pozitīvo maksājumu, izmantojot elektroniskos pārskatus.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 491048c7274ba6bb52e0a4b7a6ea5cd0f5ff4741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878223"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Iestatīt pozitīvo maksājumu failus, izmantojot elektroniskos pārskatus

Šajā rakstā ir izskaidrots, kā iestatīt pozitīvo maksājumu un ģenerēt pozitīvo maksājumu failus, izmantojot elektroniskos pārskatus.

> [!NOTE] 
> Pirms bankas **pozitīvā maksājuma faila funkcijas ģenerēšanas** vispirms jāatsvaidzina elementu saraksts.
> Pārejiet uz sadaļu **Datu pārvaldība > Importēšana/eksportēšana > Struktūras parametri** 
> **Elementa iestatījumu** kopsavilkuma cilni, atlasiet **Atsvaidzināt elementu sarakstu**.


Iestatiet pozitīvo maksājumu, lai izveidotu elektronisku čeku sarakstu, kas tiek iesniegts bankai. Kad čeki tiek uzrādīti bankai, banka to salīdzina ar čeku sarakstu. Ja čeks atbilst čekam sarakstā, banka to dzēš. Ja čeks neatbilst čekam sarakstā, banka to aiztur uz pārskatīšanu.

## <a name="security-for-positive-pay-files"></a>Pozitīvā maksājuma failu drošība
Pozitīvo maksājumu faili var saturēt konfidenciālu informāciju par maksājumu saņēmējiem un čeku summām. Šī iemesla dēļ nodrošiniet, lai no failu ģenerēšanas, līdz to saņemšanai bankā, tiek veikti atbilstoši drošības pasākumi. Pozitīvo maksājumu faili tiek lejupielādēti atrašanās vietā, kas ir norādīta tīmekļa pārlūkprogrammā. Tā kā pozitīvo maksājumu faili var saturēt jutīgu informāciju, ir svarīgi, lai tikai autorizētiem lietotājiem būtu piekļuve šīs Microsoft Dynamics informācijas ģenerēšanu un skatīšanu 365 Finansēs. Izmantojiet nākamo tabulu, kas palīdzēs noskaidrot nepieciešamās privilēģijas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Uzdevums</th>
<th>Privilēģija</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izveidot pozitīvo maksājumu failus, izmantojot sarakstu lapu <strong>Bankas konti</strong> vai lapu <strong>Bankas konti</strong>.</td>
<td><ul>
<li><strong>Uzturēt bankas pozitīvo maksājumu datus</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un bankas kontiem, izmantojot lapu <strong>Izveidot pozitīvā maksājuma failu</strong>.</td>
<td><ul>
<li><strong>Uzturēt bankas pozitīvo maksājumu datus</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skatīt pozitīvo maksājumu failus lapā <strong>Pozitīvā maksājuma kopsavilkuma fails</strong>.</td>
<td><strong>Skatīt vairākām juridiskām personām izveidotos bankas pozitīvo maksājumu datus</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Apstiprināt bankas pozitīvā maksājuma failu lapā <strong>Pozitīvā maksājuma kopsavilkuma fails</strong>.</td>
<td><strong>Apstiprināt pozitīvā maksājuma failu</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Atsaukt bankas pozitīvā maksājuma failu lapā <strong>Pozitīvā maksājuma faila kopsavilkums</strong>.</td>
<td><strong>Atsaukt pozitīvā maksājuma failu</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektronisko pārskatu izveides konfigurācijas iestatīšana

1. Dodieties uz **elektronisko darbvietu \> pārskatu**.
2. Microsoft konfigurācijas nodrošinātāja **elementā atlasiet Repositories** **.**
3. Atlasiet **Globāls** un pēc tam atlasiet **Atvērt**.
4. Ja ir jāizveido savienojums ar repozitoriju, dialoglodziņā atlasiet zilo saiti.
5. Konfigurācijas sarakstā atrodiet un atlasiet Pozitīvā maksājuma **modeļa pozitīvā \> maksājuma formātu**.
6. Kopsavilkuma cilnē **Versijas** atlasiet jaunāko versiju un pēc tam atlasiet **Importēt**.

## <a name="set-up-a-positive-pay-format"></a>Iestatīt pozitīvā maksājuma formātu

1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldības \> iestatījuma \> pozitīvajiem maksājuma formātiem**.
2. Atlasiet **Jauna**.
3. Iestatiet maksājuma **formāta un** apraksta **laukus**.
4. Atzīmējiet **izvēles rūtiņu Vispārējs elektroniskā** eksporta formāts.
5. Iestatiet eksporta **formāta konfigurācijas lauku** pozitīvā **maksājuma formātā**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Pozitīvā maksājuma formāta piešķiršana bankas kontam
Katram bankas kontam, kuram vēlaties izveidot pozitīvā maksājuma datus, ir jāpiešķir iepriekšējā sadaļā norādīto pozitīvā maksājuma formāts. Lapā Bankas konti atlasiet pozitīvā maksājuma formātu, kas atbilst bankas kontam. Laukā **Pozitīvā maksājuma sākuma datums** ievadiet pozitīvo maksājumu failu izveides sākuma datumu. 

>[!Important]
> Laukā Pozitīvā maksājuma sākuma datums **ievadiet** datumu. Ja lauks ir atstāts tukšs, pirmajā izveidotajā pozitīvā maksājuma failā tiks ietverti visi čeki, kas ir izveidoti šim bankas kontam.

1. Dodieties uz **skaidras naudas un bankas pārvaldības \> banku kontiem \> Bankas konti**.
2. Atveriet bankas kontu.
3. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku Pozitīvā **maksājuma formāts** uz iepriekš izveidoto formātu.
4. Laukā Pozitīvā **maksājuma sākuma datums** iestatiet pašreizējo datumu.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Piešķirt pozitīvo maksājumu failu numerāciju
Katram pozitīvo maksājumu failam ir nepieciešams unikāls numurs. Lapā Kases **un bankas vadības** parametri izveidojiet numuru sēriju pozitīvā maksājuma failiem cilnē **Numuru sērijas**.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Izveidot pozitīvā maksājuma failu vienam bankas kontam
Pozitīvā maksājuma failu var izveidot vienai juridiskajai personai un vienam bankas kontam. Lai iegūtu informāciju par to, kā vienlaicīgi izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un banku kontiem, skatiet nākamo sadaļu. Lai izveidotu pozitīvā maksājuma failu vienai juridiskajai personai un vienam bankas kontam, atveriet dialoglodziņu **Izveidot pozitīvā maksājuma failu** lapā **Bankas konti**. Laukā **Pēdējais datums** ievadiet pēdējā čeka datumu, kas jāiekļauj pozitīvā maksājuma failā. Failā tiek iekļauti visi čeki, kas nav iekļauti pozitīvā maksājuma failā līdz šī čeka datumam.

1. Dodieties uz **skaidras naudas un bankas pārvaldības \> bankas kontu \> bankas kontiem**.
2. Atveriet bankas kontu, kam ir iestatīti pozitīvais pārskaitījums.
3. Atlasiet Pārvaldīt **maksājumu pozitīvā \> maksājuma \> pozitīvā maksājuma failu**.
4. **Iestatiet beigu datuma** lauku. Tiks iekļauti čeki, kas tika ģenerēti pirms šī datuma.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Izveidot pozitīvā maksājuma failu vairākiem bankas kontam
Lai ģenerētu pozitīvā maksājuma failu vairākiem bankas kontiem, izmantojiet periodisko **uzdevumu Pozitīvā** maksājuma failam. Atlasiet pozitīvā maksājuma faila formātu un norādiet, vai izveidot failu visām juridiskajām personām vai tikai atlasītajai juridiskajai personai. Var izveidot arī pozitīvā maksājuma failu visiem bankas kontiem, kas izmanto norādīto pozitīvā maksājuma formātu, vai tikai atlasītajam bankas kontam. Laukā **Pēdējais datums** ievadiet pēdējā čeka datumu, kas jāiekļauj pozitīvā maksājuma failā. Failā tiek iekļauti visi čeki, kas nav iekļauti pozitīvā maksājuma failā līdz šī čeka datumam.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Skatīt pozitīvā maksājuma faila izveides rezultātus
Kad pozitīvā maksājuma fails ir izveidots, lapā **Pozitīvā maksājuma faila kopsavilkums** var skatīt rezultātus. Lai apskatītu detalizētu informāciju par atsevišķiem čekiem, dodieties uz lapu **Detalizēta informācija par pozitīvā maksājuma** failu.

## <a name="confirm-a-positive-pay-file"></a>Pozitīvā maksājuma faila apstiprināšana
Kad čeki ir ievietoti sarakstā un pozitīvā maksājuma fails ir apmaksāts, banka jums nosūta apstiprinājuma numuru. Pēc tam pozitīvā maksājuma failu var apstiprināt. Lapā **Pozitīvā maksājuma faila kopsavilkums** atlasiet pozitīvā maksājuma failu ar statusu **Izveidots** un pēc tam atlasiet darbību **Ievadīt apstiprinājumu**. Apstiprinot pozitīvā maksājuma failu, tiek reģistrēts no bankas saņemtais apstiprinājuma numurs.

## <a name="recall-a-positive-pay-file"></a>Pozitīva maksājuma faila atsaukšana
Ja pozitīvā maksājuma fails ir jāmaina, to var atsaukt. Lapā **Pozitīvā maksājuma faila kopsavilkums** atlasiet pozitīvā maksājuma failu ar statusu **Izveidots** un pēc tam atlasiet darbību **Atsaukt**. Katrā pozitīvā maksājuma failā tiek atiestatīts lauks, kas norāda, vai šis čeks ir iekļauts pozitīvā maksājuma failā. Pēc tam var izveidot jaunu pozitīvā maksājuma failu, kurā ir iekļauts atsauktais čeks.


Rezultātā iegūtais XML fails tiks lejupielādēts.
