---
title: Krājumu un izejmateriālu izsekošana krājumos, ražošanā un pārdošanā
description: Šajā tēmā ir aprakstīts, kā jūs varat izmantot krājuma izsekošanu, lai identificētu, kur krājumi vai izejmateriāli ir izmantoti, tiek izmantoti vai tiks izmantoti ražošanas un pārdošanas procesos.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa1be4970f1106bf4b87eeaa428bac07c645b4f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433032"
---
# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Krājumu un izejmateriālu izsekošana krājumos, ražošanā un pārdošanā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā jūs varat izmantot krājuma izsekošanu, lai identificētu, kur krājumi vai izejmateriāli ir izmantoti, tiek izmantoti vai tiks izmantoti ražošanas un pārdošanas procesos.

Krājumu izsekošanas funkcionalitāte ir pieejama lapā **Krājumu izsekošana**. Nākamajās sadaļās aprakstīts, kā var izmantot krājumu izsekošanas funkcionalitāti un kādas ir iespējas un ierobežojumi.

## <a name="what-is-item-tracing"></a>Kas ir krājuma izsekošana?
Krājumu izsekošana ir biznesa inteliģences (BI) rīks, kas nodrošina krājumu un izejmateriālu izcelsmes avota un mērķa redzamību piegādes ķēdē. Ražotāji var izsekot krājumiem, izejmateriāliem vai sastāvdaļām sākot no piegādātāja un uz priekšu līdz preces ražošana un pārdošana ir pabeigta. Krājumu izsekošana palīdz ražotājiem ievērot regulatīvās prasības, kā arī palīdz kvalitātes darbiniekiem un ražošanas vadītājiem analizēt un rīkoties, lai noteiktu preču un materiālu kvalitātes novirzes. Tālāk ir sniegti daži tādu metožu piemēri, kuras ražotāji var izmantot krājuma izsekošanai.

-   Norādiet krājumu vai izejmateriālu daudzumu, kas pašlaik atrodas krājumos, un kur tie tiek glabāti.
-   Nosakiet, cik daudz un kuriem klientiem krājumi vai izejmateriāli ir nosūtīti.
-   Norādiet jebkuru plānoto kravu, kas ietver krājumu vai izejmateriālu.
-   Atrodiet ražošanas pasūtījumus, kas attiecas uz krājumiem vai izejmateriāliem, kas ir plānoti, ražoti vai reģistrēti kā pabeigti.
-   Uzziniet, kur krājumi vai izejmateriāli tika nopirkti.
-   Izpētiet, kur krājumi vai izejmateriāli tika patērēti citu krājumu ražošanā.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Ko es varu izsekot un vai ir kādi ierobežojumi?
Notikušās krājumu un izejmateriālu transakcijas var izsekot pēc krājuma numura un izsekošanas dimensijas, piemēram, sērijas numura, partijas numura vai kreditora partijas numura. Krājumu vai izejmateriālu var izsekot tikai tad, ja tam ir piešķirta izsekošanas dimensija. Tā kā izsekošanas pamatā ir krājumu transakcijas, uz krājumu izsekošanu attiecas daži ierobežojumi. Piemēram, pastāv ierobežojumi, kas saistīti ar projektu, pamatlīdzekļu un komercijas transakcijām. Turklāt informācija par līdzproduktiem ir redzama izsekošanas dotos, bet informācija par blakusproduktiem nav iekļauta. Izsekošana iekļauj visas noliktavas transakcijas no viena novietojuma uz citu. Tāpēc lietotājiem var būt pieejams milzīgs informācijas apjoms. Vienlaicīgi tiek parādīti izsekošanas dati par vienu juridisku personu. Starpuzņēmumu kontekstā nav pieejamas starpuzņēmumu izsekošanas iespējas. Katram uzņēmumam, kas ir saņēmis vai izsniedzis krājumu, ir jāsāk jauna izsekošana.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Kādus kritērijus var norādīt krājumu izsekošanai?
Nepieciešamie krājuma izsekošanas kritēriji ir krājuma numurs, izsekošanas dimensija (piemēram, partijas numurs vai sērijas numurs) un virziens. Tabulā ir aprakstīti kritēriji, kurus varat izmantot krājuma izsekošanā.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauku grupa</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Krājuma kods</td>
<td>Ievadiet izsekojamā krājuma vai izejmateriāla identifikatoru.</td>
</tr>
<tr class="even">
<td>Preces dimensijas</td>
<td>Nav obligāti: izsekošanai īpaši nozīmīga ir preces definīcija, piemēram, konfigurācija, izmērs, krāsa vai modelis.</td>
</tr>
<tr class="odd">
<td>Izsekošanas dimensijas</td>
<td>Ievadiet partijas numuru, kreditora partijas numuru vai izsekošanas dimensijas sērijas numuru. Ja kā kritērijs tiek izmantots partijas numurs un šī informācija ir reģistrēta, tiek parādīts kreditora partijas numurs.</td>
</tr>
<tr class="even">
<td>Noliktavas dimensijas</td>
<td>Nav obligāti: izsekot krājumus, kas tika glabāti noteiktā atrašanās vietā.</td>
</tr>
<tr class="odd">
<td>Periods</td>
<td>Nav obligāti: ievadiet datumus, lai ierobežotu izsekošanas periodu. Izsekošanas datos tiek parādīti tikai tie dokumenti un transakcijas, kas ir izveidotas starp šiem datumiem.</td>
</tr>
<tr class="even">
<td>Uz priekšu vai atpakaļ</td>
<td>Izvēlieties izsekošanas virzienu. Varat izsekot uz priekšu vai atpakaļ:
<ul>
<li><strong>Atpakaļ</strong> — veiciet lejpusēju izsekošanu, lai noteiktu avotu, atlikušo rīcībā esošo daudzumu un visus ražošanas pasūtījumus, kas ir vismaz daļēji reģistrēti kā pabeigti.</li>
<li><strong>Uz priekšu</strong> — veiciet augšpusēju izsekošanu, lai noteiktu galamērķi. Var atrast pārdošanas pasūtījumus un debitorus, kam kaut vai daļēji ir nosūtīts izsekojamais krājums vai izejmateriāls.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Kāda informācija tiek iekļauta detalizētajā izsekošanas informācijā?
Izsekošanas rezultāti tiek parādīti hronoloģiskā secībā kokveida skatā lapas **Krājumu izsekošana** kopsavilkuma cilnē **Detalizēta informācija**. Pasūtījums atšķiras atkarībā no izsekošanas virziena. Detalizēta informācija iekļauj visas transakcijas no krājuma iegādes no kreditora līdz tā pārdošanai debitoram. Izsekošanas rezultātos iekļauj arī pagaidu preces, kas ir saistītas ar krājumu vai izsekošanas dimensiju, kas tika norādīta izsekošanas kritērijos. Augšējā līmenī ir redzams rīcībā esošais krājuma daudzums krājumu uzskaites vienībās pēc noliktavas dimensijām, kas tika norādītas izsekošanas kritērijos. **Piezīme.** Izsekošanas dati nodrošina tās informācijas momentuzņēmumu, kas bija pieejama, kad izsekošana tika pabeigta. Izsekošanas dati netiek atjaunināti, ja informācija mainās pēc tam, kad izsekošana ir pabeigta.

## <a name="why-dont-some-nodes-contain-any-details"></a>Kāpēc daži līmeņi nesatur nekādu informāciju?
Lai samazinātu informācijas apjomu izsekošanas detalizētajā informācijā, tikai pirmais līmenis ietver detalizētu informāciju par krājuma vai izejmateriāla vienību. Ja atlasītajā līmenī nav ietverta detalizēta informācija, noklikšķinot uz **Doties uz izsekoto rindu**, var skatīt līmeni, kurā ir ietverta informācija. Pēc tam var atgriezties iepriekšējā līmenī, noklikšķinot uz **Atgriezties**.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Vai es varu apskatīt tikai noteikta veida dokumentu? Piemēram, vai es varu apskatīt tikai ražošanas pasūtījumus, klientus vai piegādātājus?
Jā, izmantojot izsekošanas datus, var atvērt saraksta lapas, kas ietver tikai noteikta veida dokumentu vai transakciju. Lai piekļūtu šīm lapām, izmantojiet darbību rūtī izvēlnes vienumu **Izsekošana** grupā **Krājums**, **Pārdošana**, **Pirkšana**, **Ražošana** un **Kvalitāte**. Piemēram, lai skatītu kreditoru sarakstu izsekošanas datos, noklikšķiniet uz **Izsekošana** &gt; **Pirkšana** &gt; **Kreditori**. Saraksta lapas apkopo dokumentus vai darījumus no izsekošanas detalizētās informācijas. Saraksta lapā **Neapstiprinātie darījumi**, **Neapstiprinātie pasūtījumi** un **Nenosūtītie pārdošanas pasūtījumi** tiek parādīta arī informācija, kas nav ietverta izsekošanas datos. Turklāt tajās vienmēr ir redzami pašreizējā datuma rezultāti arī tad, ja ir norādīts datumu diapazons. Šajā tabulā ir aprakstīta papildu informācija, kas var tikt iekļauta šajās lapās.

| Saraksti                    | Apraksts                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nav nosūtītu pārdošanas pasūtījumu | Skatiet pārdošanas pasūtījuma rindas, kas vēl nav izdotas un tādēļ nav redzamas izsekošanas datos.                                                                                                                                                                                                                        |
| Gaidošie pasūtījumi           | Apskatiet visus nenokārtotos izsekojamā krājuma ražošanas pasūtījumus, neatkarīgi no izsekošanas dimensijām, kas tika izmantotas izsekošanas kritērijos. Var skatīt arī vēl neapstiprinātos ražošanas pasūtījumus, kuru izsekojamais krājums ir komponents, kuru reģistrācija nav veikta un kuru pasūtījuma transakcijas nav reģistrētas kā pabeigtas. |
| Nepabeigtie darījumi     | Apskatiet nenokārtotos izsekojamā krājuma darījumus, kas ietver norādītās izsekošanas dimensijas vai neaizpildītu izsekošanas dimensiju. Jūs varat arī apskatīt nenokārtoto krājumu darījumu un izsekošanas dimensijas kombinācijas vai tukšu vērtību izsekošanas detalizētajā informācijā.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Cik līmeņus uz augšu vai uz leju var izsekot materiālu komplektā vai formulā?
Materiālu komplektā (MK) vai formulā var izsekot var vienu līmeni uz augšu vai uz leju. Piemēram, ja jūs palaižat izejmateriālu izsekošanu, varat redzēt pabeigtās preces un līdzproduktus. Tomēr, ja tiek izsekots līdzprodukts, izsekošanas datos nav neiekļauta gala prece.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Kā es varu apskatīt papildu informāciju par dokumentu vai darījumu izsekošanas detalizētajā informācijā?
Kopsavilkuma cilnē **Detalizēta informācija** plašāku informāciju par atlasīto dokumentu vai transakciju izsekošanas datos var skatīt divējādi.

-   Ja tiek atlasīts līmenis izsekošanas datos kopsavilkuma cilnē **Detalizēta informācija**, citās lapas kopsavilkuma cilnēs tiek parādīta informācija par līmenī ietverto dokumentu vai transakciju.
-   Lai atvērtu atlasītajā mezglā ietvertā dokumenta detalizētās informācijas lapu, noklikšķiniet uz **Skatīt detalizētu informāciju**. Piemēram, ja ir atlasīts līmenis, kas attiecas uz ražošanas pasūtījumu, un noklikšķina uz **Skatīt detalizētu informāciju**, tiek parādīta lapa **Detalizēta informācija par ražošanas pasūtījumiem**.

Dažas kopsavilkuma cilnes nodrošina piekļuvi papildu informācijai par atlasīto līmeni. Piemēram, kopsavilkuma cilnē **Neatbilstības** varat noskaidrot, vai pastāv neatbilstību vēsture, noklikšķinot uz **Pieprasījumi**. Kopsavilkuma cilnē **Partija** var noklikšķināt uz **Rīcībā esošs**, lai skatītu rīcībā esošo fizisko krājumu daudzumu un visas krājumu transakcijas, kas ir saistītas ar partiju.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Vai var palaist vairāk nekā vienu izsekošanas darbību un pēc tam salīdzināt datus?
Kad ir izsekošana ir palaista, var izmantot pogas **Izsekošana no līmeņa** tālāk norādītās opcijas, lai palaistu jaunu atlasītā līmeņa transakcijas izsekošanu.

-   **Atpakaļ** vai **Tālāk** — sākt jaunu atlasītā līmeņa izsekošanu un pārrakstīt pašreizējās izsekošanas datus.
-   **Jauna atpakaļ vērsta izsekošana** vai **Jauna uz priekšu vērsta izsekošana** — sākt jaunu izsekošanu jaunā logā un saglabāt pašreizējās izsekošanas datus.

Ja vēlaties izmantot opciju **Jauna atpakaļ vērsta izsekošana** vai **Jauna uz priekšu vērsta izsekošana**, jāizmanto funkcionalitāte **Atvērt jaunā logā**, lai jaunā izsekošana tiek parādīta jaunā logā.

## <a name="can-i-save-the-trace-details"></a>Vai es varu saglabāt izsekošanas detalizēto informāciju?
Cilnē <strong>Detalizēta informācija</strong> pieejamos datus var saglabāt XML faila formātā, darbību rūtī zem darbības *<strong><em>Izsekošana</em></strong>* noklikšķinot uz <strong>Eksportēt</strong>. Papildus izsekošanas datiem XML formāta failā ir iekļauti dati par izsekošanas kritērijiem, pamatlīmeni un rīcībā esošo daudzumu. Detalizētās informācijas par izsekošanu saglabāšanas iespēja ir noderīga, piemēram, ja vēlaties pievienot informāciju kvalitātes pārbaudes pasūtījumam vai citos atbilstības novērtēšanas dokumentos. Varat norādīt faila saglabāšanas vietu. Lai tūlītēji skatītu failu, atlasiet opciju <strong>Parādīt dokumentu</strong>. <strong>Piezīme.</strong> Fails tiek saglabāts arī tad, ja vēlaties to tikai apskatīt. Pēc noklusējuma pārlūkprogrammas logā tiek atvērts XML fails. Taču var arī noklikšķināt ar peles labo pogu uz faila un atlasīt <strong>Atvērt ar</strong> un pēc tam atlasīt programmu, kura jāizmanto satura parādīšanai.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Vai es varu aprēķināt bilanci noteiktam krājumam vai komponentei?
Informāciju varat eksportēt no kopsavilkuma lapām uz Microsoft Excel. Atveriet attiecīgo lapu, noklikšķiniet uz ikonas **Atvērt programmā Microsoft Office** un pēc tam atlasiet **Eksportēt programmā Microsoft Excel**. Šī funkcionalitāte ir īpaši noderīga, ja vēlaties aprēķināt krājuma vai komponenta masas bilanci lapā **Transakciju kopsavilkums**. Lapā **Transakciju kopsavilkums** var filtrēt pēc krājuma vai komponenta un papildus arī pēc partijas un pēc tam eksportēt datus programmā Excel. Programmā Excel varat, piemēram, atdalīt rīcībā esošo daudzumu, pārdoto daudzumu un ražošanā izmantoto summu.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Vai var noskaidrot, vai ar krājumu vai izejmateriālu ir bijušas problēmas?
Izsekošanas datos ir iekļauta informācija par kvalitātes pasūtījumiem un neatbilstībām, kas saistītas ar krājumu vai izejmateriālu. Lai skatītu kopsavilkumu par kvalitātes pārbaudes pasūtījumiem un neatbilstībām, darbību rūtī noklikšķinot uz **Kvalitātes pasūtījumi** vai **Neatbilstības**. **Piezīme.** Destruktīvi kvalitātes pasūtījumi izsekošanas datos var būt redzami vairāk nekā vienu reizi. Izveidojot dokumentam, piemēram, pirkšanas pasūtījumam, destruktīvu kvalitātes pasūtījumu, tas tiek parādīts katrai dokumenta transakcijai.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Vai pastāv ar krājumu izsekošanu saistītas reģistrēšanas iespējas?
Var izveidot pārskatu **Nosūtīts debitoriem**, lai noskaidrotu nosūtīto krājuma vai izejmateriāla daudzumu un debitorus, kuriem tie ir nosūtīti. Ja pieprasījums ir saistīts ar atbilstību, varat izveidot visiem debitoriem paredzētu pārskatu. Tāda pieprasījuma gadījumā, kas saistīts ar debitora pakalpojumu, var izveidot atlasītajam debitoram paredzētu pārskatu. Ja prece bija izejmateriāls, kas tika izmantots ražošanā krājuma izveidošanai, pabeigtais krājums arī tiek iekļauts. **Piezīme.** Ja tiek izmantoti līdzekļi pārdošanas pasūtījumu dzēšanai vai arhivēšanai, pārskata rezultātos ir iekļauti arī izdzēsti vai arhivēti pārdošanas pasūtījumi.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Vai es varu izsekot līdzproduktus un blakusproduktus?
Izsekot var arī līdzproduktus, bet nevar izsekot blakusprodukts, jo parasti tiem netiek piešķirtas izsekošanas dimensijas. Krājuma izsekošanas gadījumā izsekošanas dati iekļauj visus saistītos līdzproduktus. Detalizētajā informācijā līmenis, kas satur līdzproduktu, ietver vārdu "līdzprodukts". Skatīt var arī detalizētu informāciju par līdzproduktu, atlasot līmeni izsekošanas datos un pēc tam noklikšķinot uz kopsavilkuma cilnes **Ražošana**.
