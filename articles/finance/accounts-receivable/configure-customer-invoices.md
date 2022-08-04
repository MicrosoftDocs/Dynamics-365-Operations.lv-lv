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
ms.openlocfilehash: 04c26eec8be61d60908bef67c75958287e7e1a01
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129518"
---
# <a name="create-a-customer-invoice"></a>Izveidot debitora rēķinu

[!include [banner](../includes/banner.md)]

Debitora **rēķins par pārdošanas pasūtījumu** ir rēķins, kas saistīts ar pārdošanu un ko organizācija piešķir debitoram. Šī tipa debitora rēķins tiek izveidots, pamatojoties uz pārdošanas pasūtījumu, kurā ir iekļautas pasūtījuma rindas un krājumu kodi. Krājumu numuri tiek noteikti un grāmatoti Virsgrāmatā. Debitora rēķinam par pārdošanas pasūtījumu nav pieejami apakšgrāmatas žurnāla ieraksti. Plašāku informāciju skatiet šeit: [Pārdošanas pasūtījumu rēķinu izveide](tasks/create-sales-order-invoices.md).

Brīva **teksta rēķins** nav saistīts ar pārdošanas pasūtījumu. Tajā ir pasūtījuma rindas, kurās ir iekļauti virsgrāmatas konti, brīva teksta apraksti un jūsu ievadītā pārdošanas summa. Šāda veida rēķinā jūs nevarat ievadīt krājuma kodu. Jums ir jāievada atbilstoša informācija par PVN. Galvenais konts pārdošanai ir norādīts katrā rēķina rindā, kuru varat izplatīt vairākiem virsgrāmatas kontiem, lapā **Brīva teksta rēķins** noklikšķinot uz **Sadalīt summas**. Turklāt debitora bilance tiek grāmatota kopsavilkuma kontā no grāmatošanas metodes, kas tiek izmantota brīva teksta rēķinam.

Plašāku informāciju skatiet:

[Izveidot brīva teksta rēķinus Izveidot brīva teksta rēķina veidni
](../accounts-receivable/create-free-text-invoice-new.md)[Piešķirt brīva teksta rēķina](../accounts-receivable/create-free-text-invoice-template-new.md)[
 veidni debitoram Ģenerēt un grāmatot periodiskus](tasks/assign-free-text-invoice-template-customer.md)
[brīva teksta rēķinus](tasks/post-recurring-free-text-invoices.md)


Pro **forma rēķins** ir rēķins, kas tiek sagatavots kā faktisko rēķina summu novērtējums pirms rēķina grāmatošanas. Pro forma rēķinu **var drukāt** debitora rēķinam par pārdošanas pasūtījumu vai brīva teksta rēķinam. 

>[!NOTE]
> Ja pārdošanas pro forma rēķina procesa laikā rodas sistēmas pārtraukums, pro forma rēķinu var saņemt bāreņrēķins. Bāreņforma rēķinu var dzēst, manuāli palaižot **periodisko darbu Dzēst** pro forma rēķinus. Pārejiet uz **Sadaļu Pārdošana > Periodiskie > nodzēsiet > manuāli izdzēsiet pro forma rēķinus**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Pārdošanas pasūtījuma debitora rēķina datu elementus izmantošana
Jūs varat izmantot datu elementus, lai importētu un eksportētu informāciju par debitora rēķinu pārdošanas pasūtījumam. Pārdošanas rēķina virsrakstā un pārdošanas rēķina rindās ir pieejami dažādi informācijas elementi.

Pārdošanas rēķina virsrakstā informācijai ir pieejami šādi elementi:

- **Pārdošanas rēķinu žurnāla virsraksta** elements (SalesInvoiceJournalHeaderEntity)
- **Pārdošanas rēķinu virsraksti V2** elementam (SalesInvoiceHeaderV2Entity)

Ieteicams izmantot pārdošanas rēķinu žurnāla virsraksta **elementu**, jo tā nodrošina lielāku pieredzi pārdošanas virsrakstu importā un eksportā. Šajā entītijā nav ietverta **kolonna PVN summa** (INVOICEHEADERTAXAMOUNT), kas norāda PVN vērtību pārdošanas rēķina galvenē. Ja jūsu biznesa scenārijā pieprasīta informācija, izmantojiet pārdošanas **rēķina galvenes V2** elementu, lai importētu un eksportētu pārdošanas rēķina galvenes informāciju.

Pārdošanas rēķina rindās informācijai ir pieejami šādi elementi:

- **Debitora rēķina rindu** elements (BusinessDocumentSalesInvoiceLineItemEntity)
- **Pārdošanas rēķina rindu V3** elements (SalesInvoiceLineV3Entity)

Nosakot, kuru rindas elementu izmantot eksportiem, apsveriet, vai tiks izmantots pilns pašpiegādes vai inkrementālais pašpiegādes. Papildus apsveriet datu kompozīciju. Pārdošanas **rēķina rindas V3 elements** atbalsta sarežģītākus scenārijus (piemēram, kartēšanu uz krājumu laukiem). Tas atbalsta arī pilnas pašpiegādes eksporta scenārijus. Inkrementālai spiež, mēs iesakām izmantot debitora **rēķina rindu** elementu. Šis elements ietver daudz vienkāršāku datu sastāvdaļas **nekā pārdošanas rēķina rindu V3** elementu, un tas ir vēlamais, it īpaši, ja nav nepieciešama krājumu lauku integrācija. Tā kā pastāv atšķirības kartēšanas atbalsta starp rindas elementiem, **·** **debitora rēķina rindu elementam parasti ir ātrāka veiktspēja nekā elementam Pārdošanas rēķina rindas V3.**

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Atsevišķu, uz pārdošanas pasūtījumiem balstītu debitoru rēķinu grāmatošana un drukāšana
Izmantojiet šo procesu, lai izveidotu rēķinu, kas ir balstīts uz pārdošanas pasūtījumu. To varat darīt, ja izlemjat debitoram rēķinu izrakstīt pirms preču vai pakalpojumu piegādes. 

Kad grāmatojat kādu rēķinu, katra krājuma daudzums **Rēķina atlikums** tiek atjaunināts ar kopējiem rēķinā iekļautajiem daudzumiem no atlasītā pārdošanas pasūtījuma. Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja daudzums **Rēķina atlikums** nav 0 (nulle), pārdošanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus.

Pārdošanas pasūtījumu statusu varat skatīt saraksta lapā **Visi pārdošanas pasūtījumi**. Lai skatītu rēķinus, kurus grāmatojāt, izmantojiet saraksta lapu **Atvērtie debitoru rēķini**.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Atsevišķu, uz pavadzīmēm un datumu balstītu debitoru rēķinu grāmatošana un drukāšana
Izmantojiet šo procesu, ja pārdošanas pasūtījumam ir grāmatota viena vai vairākas pavadzīmes. Debitora rēķins tiek pamatots ar šīm pavadzīmēm un atspoguļo tajās norādītos daudzumus. Rēķina finanšu informācija ir balstīta uz informāciju, kas tiek ievadīta, kad grāmatojat rēķinu. 

Varat izveidot debitora rēķinu, kas ir balstīts uz pavadzīmes rindas krājumiem, kas piegādāti līdz šim datumam, arī tad, ja nav nosūtīti visi noteikta pārdošanas pasūtījuma krājumi. To varat izdarīt, piemēram, ja jūsu juridiskā persona izsniedz vienu rēķinu katram debitoram mēnesī, kas sedz visas piegādes, kuras attiecīgā mēneša laikā piegādājat. Katra pavadzīme ataino daļēju vai pilnīgu krājumu piegādi pēc pārdošanas pasūtījuma. 

Kad grāmatojat rēķinu, daudzums **Rēķina atlikums** katram krājumam tiek atjaunināts ar kopīgo piegādāto daudzumu no atlasītajām pavadzīmēm. Ja gan daudzums **Rēķina atlikums**, gan daudzums **Piegādes atlikums** visiem krājumiem pārdošanas pasūtījumā ir 0 (nulle), tad pārdošanas pasūtījuma statuss mainās uz **Iekļauts rēķinā**. Ja daudzums **Rēķina atlikums** nav 0 (nulle), pārdošanas pasūtījuma statuss paliek nemainīgs, un tam var ievadīt papildu rēķinus. 

Inventāra transakcijas tiek atjauninātas ar rēķina numuru, un statuss pārdošanas pasūtījuma laukā **Rindas statuss** mainās uz **Iekļauts rēķinā**. 

Skatiet pārdošanas pasūtījumu statusu visu pārdošanas **pasūtījumu saraksta** lapā.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Pārdošanas pasūtījumu vai pavadzīmju konsolidēšana grāmatošanai
Izmantojiet šo procesu, kad viens vai vairāki pārdošanas pasūtījumi ir gatavi rēķina izrakstīšanai un vēlaties tos konsolidēt vienā rēķinā. 

Saraksta lapā **Pārdošanas pasūtījums** varat atlasīt vairākus rēķinus un pēc tam izmantot vienumu **Ģenerēt rēķinus**, lai tos konsolidētu. Lapā **Rēķina grāmatošana** varat mainīt iestatījumu **Koppasūtījums**, lai apkopotu pēc pasūtījuma numura (ja vienam pārdošanas pasūtījumam ir vairākas pavadzīmes) vai pēc rēķina konta (ja vienam rēķina kontam ir vairāki pārdošanas pasūtījumi). Izmantojiet pogu **Sakārtot**, lai pārdošanas pasūtījumus sakārtotu vienā rēķinā, pamatojoties uz iestatījumiem **Koppasūtījums**.

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Sadalīt pārdošanas pasūtījumu rēķinus pēc vietas un piegādes informācijas
Debitoru parādu parametru lapas cilnē Kopgrāmatošana **var konfigurēt pārdošanas pasūtījumu debitoru rēķinu sadali pēc vietas** **vai piegādes** adreses. 
 - Atlasiet opciju **Sadalīt, pamatojoties uz rēķina atrašanās** vietu, lai grāmatojot izveidotu vienu rēķinu no vienas vietas. 
 - Atlasiet opciju **Sadalīt, pamatojoties uz rēķina piegādes informāciju**, lai grāmatojot izveidotu vienu rēķinu pārdošanas pasūtījuma rindas piegādes adresei. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Grāmatot ieņēmumu kontā pārdošanas pasūtījuma rindām, kurās nav cenas un izmaksu
Ir pieejama opcija, lai **virsgrāmatā** **atjauninātu ieņēmumu kontu pārdošanas** pasūtījuma rindām, kurām nav cenas un izmaksu. Lai iestatītu vai skatītu šo informāciju, **·** **·** **dodieties** uz kontu Grāmatot ieņēmumu kontā nulles cenai un nulles izmaksu pārdošanas pasūtījuma rēķina rindu parametru cilnē Virsgrāmata un PVN lapā Debitoru parādu parametri. (**Debitoru parādi > debitoru > parametru iestatīšanai**). Atlasiet **Jā,** lai atjauninātu **ieņēmumu** kontu pārdošanas pasūtījuma rēķina rindām, kam nav cenas un nav izmaksu. Ja ir atlasīta šī opcija, dokumentā būs 0,00 ieraksti debitoru bilances **un ieņēmumu** grāmatošanas **tipiem**. Ieņēmumu konts ir definēts krājumu grāmatošanas **parametru** lapā pārdošanas **pasūtījuma konta** definīcijas cilnē. Ja nav atlasīta šī opcija, rindas, kurās nav cenas vai izmaksu informācijas, netiek grāmatotas ieņēmumu **kontā**. Tā vietā dokumentā būs 0,00 ieraksts debitora bilances **grāmatošanas** tipam.

## <a name="line-creation-sequence-number-information"></a>Informācija par rindu izveides secības numuru
Grāmatojot debitora rēķina rindas, būs iespēja izveidot secīgus rindu izveides sērijas numurus. Rindu izveides secības numuri tiek piešķirti grāmatošanas procesa laikā. Atļaujot nes secības numerāciju, jūs varat palīdzēt uzlabot debitora rēķinu grāmatošanas veiktspēju. Rindas izveides sērijas numurus var izmantot trešās puses integrācija, kas gaida secības secību. Konsultējieties ar IT nodaļu par visiem paplašinājumiem, kas var integrēties ar rindu izveides secības numuriem.

Lai iestatītu vai skatītu šo informāciju, **debitoru** parādu parametru lapā, **cilnē** Atjauninājumi iestatiet opciju Piešķirt secīgus rindu numurus, **grāmatojot debitora rēķina** rindas:

- Iestatiet opciju Nē, lai **rindu** izveides secības numuriem izmantotu ne sērijas numerāciju.
- Iestatiet opciju Jā **, lai** izmantotu secīgu numurēšanu. Juridisko personu, kurām ir primārā **adrese** Itālijā, opcija jāiestata kā Jā. Ja ir atspējots **vienums** **CustInvoiceTrans NoLineCreationSeqNumFlight,** tas ir jāiestata arī kā Jā.

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
<li><strong>Neviens</strong> – nav vajadzības pēc kredīta limita pārbaudes.</li>
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
