---
title: Izveidot debitora rēķinu
description: Debitora rēķins par pārdošanas pasūtījumu ir rēķins, kas ir saistīts ar pārdošanu un ko uzņēmums izsniedz debitoram.
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0d1221e07f6dc4a5a99aa205c4a7f6fb367f000
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780253"
---
# <a name="create-a-customer-invoice"></a>Izveidot debitora rēķinu

[!include [banner](../includes/banner.md)]

Debitora rēķins **pārdošanas pasūtījumam** ir rēķins, kas ir saistīts ar pārdošanu un ko organizācija izsniedz debitoram. Šī tipa debitora rēķins tiek izveidots, pamatojoties uz pārdošanas pasūtījumu, kurā ir iekļautas pasūtījuma rindas un krājumu kodi. Krājumu numuri tiek noteikti un grāmatoti Virsgrāmatā. Debitora rēķinam par pārdošanas pasūtījumu nav pieejami apakšgrāmatas žurnāla ieraksti. Plašāku informāciju skatiet šeit: [Pārdošanas pasūtījumu rēķinu izveide](tasks/create-sales-order-invoices.md).

Brīva teksta rēķins **nav** saistīts ar pārdošanas pasūtījumu. Tajā ir pasūtījuma rindas, kurās ir iekļauti virsgrāmatas konti, brīva teksta apraksti un jūsu ievadītā pārdošanas summa. Šāda veida rēķinā jūs nevarat ievadīt krājuma kodu. Jums ir jāievada atbilstoša informācija par PVN. Galvenais konts pārdošanai ir norādīts katrā rēķina rindā, kuru varat izplatīt vairākiem virsgrāmatas kontiem, lapā **Brīva teksta rēķins** noklikšķinot uz **Sadalīt summas**. Turklāt debitora bilance tiek grāmatota kopsavilkuma kontā no grāmatošanas metodes, kas tiek izmantota brīva teksta rēķinam.

Plašāku informāciju skatiet:
 - [Izveidot brīvā teksta rēķinus](../accounts-receivable/create-free-text-invoice-new.md)
 - [Brīva teksta rēķina veidnes izveide](../accounts-receivable/create-free-text-invoice-template-new.md)
 - [Brīva teksta rēķina veidnes piešķiršana debitoram](tasks/assign-free-text-invoice-template-customer.md)
 - [Periodisku brīva teksta rēķinu ģenerēšana un grāmatošana](tasks/post-recurring-free-text-invoices.md)


Pro forma rēķins ir **rēķins**, kas tiek sagatavots kā faktisko rēķina summu aprēķins pirms rēķina grāmatošanas. Pro forma rēķinu **varat izdrukāt** vai nu debitora rēķinam pārdošanas pasūtījumam, vai brīvā teksta rēķinam. 

>[!NOTE]
> Gadījumā, ja pārdošanas pro forma rēķina procesa laikā sistēma tiek pārtraukta, pro forma rēķins var būt bārenis. Bāreņa pro forma rēķinu var izdzēst, palaižot manuāli **periodisko** darbu Dzēst pro forma rēķinus. Pārejiet uz sadaļu **Pārdošana un mārketings > Periodiskie uzdevumi > Iztīrīt > Manuāli dzēst pro forma rēķinus**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Pārdošanas pasūtījuma debitora rēķina datu elementu izmantošana
Datu elementus var izmantot, lai importētu un eksportētu informāciju par debitora rēķinu pārdošanas pasūtījumam. Informācijai pārdošanas rēķina galvenē un pārdošanas rēķina rindās ir dažādas entītijas.

Tālāk norādītās entītijas ir pieejamas informācijai pārdošanas rēķina galvenē:

- **Pārdošanas rēķinu žurnāla galvenes** entītija (SalesInvoiceJournalHeaderEntity)
- **Pārdošanas rēķinu galvenes V2 entītija (SalesInvoiceHeaderV2Entity**)

Ieteicams izmantot **pārdošanas rēķinu žurnāla galvenes entītiju, jo tā nodrošina efektīvāku pieredzi pārdošanas galvenes** importēšanai un eksportēšanai. Šī entītija nesatur **kolonnu PVN summa** (INVOICEHEADERTAXAMOUNT), kas norāda PVN vērtību pārdošanas rēķina galvenē. Ja jūsu biznesa scenārijā ir nepieciešama šī informācija, izmantojiet entītiju **Pārdošanas rēķinu galvenes V2**, lai importētu un eksportētu pārdošanas rēķina galvenes informāciju.

Tālāk norādītās entītijas ir pieejamas informācijai pārdošanas rēķinu rindās:

- **Debitoru rēķinu rindu** entītija (BusinessDocumentSalesInvoiceLineItemEntity)
- **Pārdošanas rēķina rindu V3 entītija (SalesInvoiceLineV3Entity**)

Nosakot, kuru rindas entītiju izmantot eksportēšanai, apsveriet, vai tiks izmantota pilna vai pakāpeniska pašpiegādes ietekme. Turklāt apsveriet datu sastāvu. Entītija **Pārdošanas rēķina rindas V3** atbalsta sarežģītākus scenārijus (piemēram, kartēšanu uz krājumu laukiem). Tas atbalsta arī pilnas jaudas eksporta scenārijus. Lai veiktu pakāpeniskus spiedienus, ieteicams izmantot **entītiju Debitora rēķina rindas**. Šī entītija satur daudz vienkāršāku datu sastāvu nekā entītija **Pārdošanas rēķina rindas V3**, un tā ir ieteicama, it īpaši, ja krājumu lauku integrācija nav nepieciešama. Tā kā kartēšanas atbalsts starp rindu entītijām atšķiras, **debitora rēķina rindu** entītijai parasti ir ātrāka **veiktspēja nekā entītijai Pārdošanas rēķina rindas V3**.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Atsevišķu, uz pārdošanas pasūtījumiem balstītu debitoru rēķinu grāmatošana un drukāšana
Izmantojiet šo procesu, lai izveidotu rēķinu, kas ir balstīts uz pārdošanas pasūtījumu. To varat darīt, ja izlemjat debitoram rēķinu izrakstīt pirms preču vai pakalpojumu piegādes. 

Kad grāmatojat kādu rēķinu, katra krājuma daudzums **Rēķina atlikums** tiek atjaunināts ar kopējiem rēķinā iekļautajiem daudzumiem no atlasītā pārdošanas pasūtījuma. Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja daudzums **Rēķina atlikums** nav 0 (nulle), pārdošanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus.

Pārdošanas pasūtījumu statusu varat skatīt saraksta lapā **Visi pārdošanas pasūtījumi**. Lai skatītu rēķinus, kurus grāmatojāt, izmantojiet saraksta lapu **Atvērtie debitoru rēķini**.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Atsevišķu, uz pavadzīmēm un datumu balstītu debitoru rēķinu grāmatošana un drukāšana
Izmantojiet šo procesu, ja pārdošanas pasūtījumam ir grāmatota viena vai vairākas pavadzīmes. Debitora rēķins tiek pamatots ar šīm pavadzīmēm un atspoguļo tajās norādītos daudzumus. Rēķina finanšu informācija ir balstīta uz informāciju, kas tiek ievadīta, kad grāmatojat rēķinu. 

Varat izveidot debitora rēķinu, kura pamatā ir līdz šim nosūtītie pavadzīmes rindas krājumi, pat ja visi konkrēta pārdošanas pasūtījuma krājumi nav nosūtīti. To varat izdarīt, piemēram, ja jūsu juridiskā persona izsniedz vienu rēķinu katram debitoram mēnesī, kas sedz visas piegādes, kuras attiecīgā mēneša laikā piegādājat. Katra pavadzīme ataino daļēju vai pilnīgu krājumu piegādi pēc pārdošanas pasūtījuma. 

Kad grāmatojat rēķinu, daudzums **Rēķina atlikums** katram krājumam tiek atjaunināts ar kopīgo piegādāto daudzumu no atlasītajām pavadzīmēm. Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), tad pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja daudzums **Rēķina atlikums** nav 0 (nulle), pārdošanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus. 

Inventāra transakcijas tiek atjauninātas ar rēķina numuru, un statuss pārdošanas pasūtījuma laukā **Rindas statuss** mainās uz **Iekļauts rēķinā**. 

Skatiet pārdošanas pasūtījumu **statusu saraksta lapā Visi pārdošanas pasūtījumi**.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Pārdošanas pasūtījumu vai pavadzīmju konsolidēšana grāmatošanai
Izmantojiet šo procesu, kad viens vai vairāki pārdošanas pasūtījumi ir gatavi rēķina izrakstīšanai un vēlaties tos konsolidēt vienā rēķinā. 

Saraksta lapā **Pārdošanas pasūtījums** varat atlasīt vairākus rēķinus un pēc tam izmantot vienumu **Ģenerēt rēķinus**, lai tos konsolidētu. Lapā **Rēķina grāmatošana** varat mainīt iestatījumu **Koppasūtījums**, lai apkopotu pēc pasūtījuma numura (ja vienam pārdošanas pasūtījumam ir vairākas pavadzīmes) vai pēc rēķina konta (ja vienam rēķina kontam ir vairāki pārdošanas pasūtījumi). Izmantojiet pogu **Sakārtot**, lai pārdošanas pasūtījumus sakārtotu vienā rēķinā, pamatojoties uz iestatījumiem **Koppasūtījums**.

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Sadalīt pārdošanas pasūtījuma rēķinus pēc vietnes un piegādes informācijas
Pārdošanas pasūtījuma debitoru rēķinu sadalīšanu pēc vietnes vai piegādes adreses **varat konfigurēt lapas Debitoru parādu parametri** cilnē **Kopsavilkuma atjauninājums**. 
 - Atlasiet opciju Sadalīt, **pamatojoties uz rēķina vietni**, lai grāmatošanas laikā katrai vietnei izveidotu vienu rēķinu. 
 - Atlasiet opciju Sadalīt, pamatojoties uz rēķina piegādes informāciju **,** lai grāmatošanas laikā izveidotu vienu rēķinu par katru pārdošanas pasūtījuma rindas piegādes adresi. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Izlikt ieņēmumu kontā pārdošanas pasūtījuma rindas, kurām nav cenas un izmaksu
Jums būs iespēja atjaunināt **ieņēmumu** kontu **virsgrāmatā** pārdošanas pasūtījuma rindām, kurām nav cenas un izmaksu. 

Lai iestatītu vai skatītu šo informāciju:
1. Dodieties uz kontu Izlikt ieņēmumus, **lai iegūtu nulles cenas un nulles izmaksu pārdošanas pasūtījuma rēķina rindu** parametru lapas Debitoru parādu parametri **cilnē** Virsgrāmata un **PVN**. (**Debitoru parādi > Iestatīšana > debitoru parādu parametri**). 
2. Atlasiet **Jā**, lai atjauninātu **ieņēmumu** kontu pārdošanas pasūtījuma rēķina rindām, kurām nav cenas un izmaksu. 
 - Ja šī opcija ir atlasīta, kuponā būs 0,00 ierakstu tipiem Debitoru **bilance** un **Ieņēmumu** grāmatošana. Ieņēmumu konts ir definēts **lapas Krājumu grāmatošanas** parametrs cilnē **Pārdošanas pasūtījuma** konta definīcija. 
 - Ja šī opcija nav atlasīta, rindas, kurās nav informācijas par cenām vai izmaksām, netiks grāmatotas **ieņēmumu** kontā. Tā vietā kuponā būs 0,00 ieraksts debitora **bilances** grāmatošanas tipam.

## <a name="line-creation-sequence-number-information"></a>Rindas izveides kārtas numura informācija
Grāmatojot debitora rēķina rindas, jums būs iespēja izveidot secīgus rindu izveides kārtas numurus. Rindu izveides kārtas numuri tiek piešķirti grāmatošanas procesa laikā. Atļaujot nesekmīgu numerāciju, varat palīdzēt uzlabot debitora rēķinu grāmatošanas veiktspēju. Rindu izveides secības numurus var izmantot trešo pušu integrācijas, kas paredz secīgu secību. Sazinieties ar IT nodaļu par paplašinājumiem, kas varētu tikt integrēti ar līniju izveides secības numuriem.

Lai iestatītu vai skatītu šo informāciju, **lapas** Debitoru parādu parametri **cilnē Atjauninājumi** iestatiet opciju Grāmatojot debitoru rēķinu rindas **piešķirt secīgus** rindu numurus:

- Iestatiet opciju **Nē**, lai rindu izveides kārtas numuriem izmantotu ne-secīgu numerāciju.
- Iestatiet opciju **Jā**, lai izmantotu secīgo numerāciju. Opcijai ir jāiestata vērtība Jā **juridiskajām personām, kuru primārā adrese ir** Itālijā. Jums tas ir jāiestata arī uz **Jā, ja** CustInvoiceTransRandLineCreationSeqNumFlight **lidojums ir atspējots.**

## <a name="additional-settings-that-change-the-posting-behavior"></a>Papildu iestatījumi, kas maina grāmatošanas darbību
Grāmatošanas procesa darbību maina tālāk uzskaitītie lauki.

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
<td>Daudzums</td>
<td>Atlasiet daudzumus, uz ko balstīt dokumentu grāmatošanu. Pieejamās opcijas ir atkarīgas no grāmatojamā dokumenta tipa, piemēram, vai dokuments ir pavadzīme vai rēķins.
<ul>
<li><strong>Piegādāt tūlīt</strong> — atlasiet visus daudzumus, kas ir ievadīti laukā <strong>Piegādāt tūlīt</strong>. Izmantojiet šo opciju, lai apstiprinātu vai piegādātu daļēju pasūtījumu.</li>
<li><strong>Izdots</strong> — atlasiet visus daudzumus, kas ir izdoti.</li>
<li><strong>Visi</strong> — atlasiet visus pārdošanas pasūtījumā ietvertos daudzumus, kas vēl&#39;nav atjaunināti, izmantojot pašreizējo dokumenta tipu.</li>
<li><strong>Pavadzīme</strong> — atlasiet visus daudzumus, kas ir atjaunināti ar pavadzīmi.</li>
<li><strong>Izdotais daudzums un neuzkrātās preces</strong> — atlasiet visus daudzumus, kas ir izdoti, un visus preču daudzumus, kas nav&#39;uzkrāti.</li>
</ul></td>
</tr>
<tr class="even">
<td>Grāmatošana</td>
<td><ul>
<li>Atlasiet šo opciju, lai reģistrētu žurnālā pārdošanas pasūtījumu.</li>
<li>Notīriet šo opciju, lai drukātu pro forma pārdošanas pasūtījumu. <strong>Piezīme.</strong> Ja esat izveidojis maksājumu grafika līgumu, pro forma pārdošanas pasūtījumā netiek&#39;rādīts maksājumu grafiks. Maksājumu grafiki tiek rādīti tikai faktiskos pārdošanas pasūtījumos.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vēlā atlase</td>
<td>Atlasiet šo opciju, lai lietotu atlasīto vaicājumu vēlāk. Šī opcija tiek izmantota pakešuzdevumiem. Vaicājums tiek izpildīts, kad tiek veikts pakešuzdevums.</td>
</tr>
<tr class="even">
<td>Samazināt daudzumu</td>
<td>Atlasiet šo opciju, lai automātiski samazinātu piegādāto daudzumu, kad dokuments ir grāmatots, tādējādi piegādātais daudzums ir vienāds ar pieejamiem krājumiem.</td>
</tr>
<tr class="odd">
<td>Drukāt</td>
<td>Atlasiet, kad drukāt dokumentus:
<ul>
<li><strong>Pašreizējais</strong> — drukāt dokumentus pēc katra rēķina atjaunināšanas.</li>
<li><strong>Pēc</strong> — drukāt dokumentus pēc visu rēķinu atjaunināšanas.</li>
</ul>
<strong>Piezīme.</strong> Lauks <strong>Drukāt</strong> ir pieejams tikai tad, ja atlasāt opciju <strong>Drukāt rēķinu</strong>, <strong>Drukāt apstiprinājumu</strong>, <strong>Drukāt izdošanas sarakstu</strong> vai <strong>Drukāt pavadzīmi</strong>. Piemēram, lapā <strong>Formu kārtošana</strong> esat iestatījis sistēmu, lai informāciju kārtotu pēc rēķina konta. Pēc tam varat atlasīt <strong>Pēc</strong>, lai drukātu dokumentus partijā, kas tiek kārtota pēc rēķina konta. Pretējā gadījumā dokumenti tiek drukāti pirms apstrādes pabeigšanas un dokumenti netiek&#39;kārtoti secībā, kas ir norādīta lapā <strong>Formu kārtošana</strong>.</td>
</tr>
<tr class="even">
<td>Drukāt rēķinu</td>
<td>Atzīmējiet šo opciju, lai izdrukātu rēķinu. Ja šī opcija ir izslēgta, rēķinu varat grāmatot, to nedrukājot.</td>
</tr>
<tr class="odd">
<td>Nosūtīt e-pastu</td>
<td>Atlasiet šo opciju, lai pēc rēķina grāmatošanas šo rēķinu par pārdošanas pasūtījumu sūtītu debitoram kā e-pasta pielikumu. Pielikumi tiek sūtīti kā PDF un XML faili. Šī opcija ir pieejama tikai tad, ja lapā <strong>Elektroniskā rēķina parametri</strong> atlasāt opciju <strong>Iespējot CFD (elektroniskie rēķini)</strong>. <strong>Piezīme.</strong> (MEX) Šī vadīkla ir pieejama tikai juridiskām personām, kuru primārā adrese ir Meksikā.</td>
</tr>
<tr class="even">
<td>Lietot drukas pārvaldības adresātu</td>
<td>Atlasiet šo opciju, lai lietotu drukas iestatījumus, kas transakcijai, dokumentam vai modulim ir norādīti lapā <strong>Drukāšanas parametru iestatīšana</strong>.</td>
</tr>
<tr class="odd">
<td>Kredīta limita pārbaude</td>
<td>Atlasiet informāciju, kas ir jāanalizē, veicot kredīta limita pārbaudi.
<ul>
<li><strong>Nav</strong> - Kredītlimita pārbaude nav nepieciešama.</li>
<li><strong>Bilance</strong> — kredīta limits tiek pārbaudīts pret debitora bilanci.</li>
<li><strong>Bilance + pavadzīme vai produktu ieejas plūsma</strong> — kredīta limits tiek pārbaudīts pret debitora bilanci un piegādēm.</li>
<li><strong>Bilance+viss</strong> — kredīta limits tiek pārbaudīts pret debitora bilanci, piegādēm un atvērtajiem pasūtījumiem.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredīta korekcija</td>
<td>Atzīmējiet šo opciju, lai dokumentu transakcijās kredīta notu rādītu kā debetu.</td>
</tr>
<tr class="odd">
<td>Kreditēt atlikušo summu</td>
<td>Ja&#39;grāmatojat kredīta notu, atzīmējiet šo opciju, lai saglabātu atlikušo daudzumu pasūtījumā. Ja šī opcija ir notīrīta, atlikušais daudzums ir iestatīts uz 0 (nulle).</td>
</tr>
<tr class="even">
<td>Kopgrāmatojums, kas paredzēts:</td>
<td>Atlasiet, kā jāveic vairāku pārdošanas pasūtījumu apkopošana:
<ul>
<li><strong>Nav</strong> — neveik&#39;t pārdošanas pasūtījumu apkopošanu. Piemēram, katram pārdošanas pasūtījumam tiks veidots atsevišķs rēķins.</li>
<li><strong>Rēķina konts</strong> — apkopot visus atlasītos pasūtījumus, balstoties uz lapā <strong>Kopgrāmatošanas parametri</strong> iestatītajiem kritērijiem.</li>
<li><strong>Pasūtījums</strong> — atlasītu pasūtījumu diapazonu atkopot vienā, jūsu norādītā pasūtījumā. Pasūtījumu apkopošana ir atkarīga no kritērijiem, ko iestatāt lapā <strong>Kopgrāmatošanas parametri</strong>. Ja atlasāt šo opciju, ir jāatlasa kāda vērtība laukā <strong>Pārdošanas pasūtījums</strong>.</li>
<li><strong>Automātisks kopsavilkums</strong> — ja lapā <strong>Kopgrāmatošana</strong> ir norādīti kopgrāmatojumi, apkopojiet visus atlasītos pasūtījumus, pamatojoties uz lapā <strong>Kopgrāmatošanas parametri</strong> iestatītajiem kritērijiem. Ja na&#39;v norādīti kopgrāmatojumi, pasūtījums tiek grāmatots atsevišķi.</li>
<li><strong>Pavadzīme</strong> — atlasīto pasūtījumu diapazonu apkopo vienā rēķinā par katru pavadzīmi. Šī opcija ir pieejama tikai tad, ja laukā <strong>Daudzums</strong> ir atlasīta vērtība <strong>Pavadzīme</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
