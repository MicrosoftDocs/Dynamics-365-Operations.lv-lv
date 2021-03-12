---
title: Intrastat pārskats
description: Šajā tēmā ir sniegta informācija par Intrastat pārskatu veidošanu preču — un noteiktos gadījumos arī pakalpojumu — tirdzniecībai starp dažādām Eiropas Savienības (ES) valstīm/reģioniem. Tajā ir sniegts pārskats par atskaišu veidošanas procesu, kā arī aprakstīti nepieciešamie iestatījumi un priekšnosacījumi.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9396637c27707f1732d06ec704c7e609aa6c170b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962728"
---
# <a name="intrastat-overview"></a>Intrastat pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par Intrastat pārskatu veidošanu preču — un noteiktos gadījumos arī pakalpojumu — tirdzniecībai starp dažādām Eiropas Savienības (ES) valstīm/reģioniem. Tajā ir sniegts pārskats par atskaišu veidošanas procesu, kā arī aprakstīti nepieciešamie iestatījumi un priekšnosacījumi.

Intrastat ir sistēma informācijas vākšanai un statistikas ģenerēšanai par preču tirdzniecību starp dažādām Eiropas Savienības (ES) valstīm/reģioniem. Intrastat atskaites ir nepieciešamas vienmēr, kad prece šķērso citas ES valsts/reģiona robežu. Vairākās valstīs/reģionos Intrastat atskaites attiecas arī uz pakalpojumiem. Intrastat atskaitēs var vākt obligātus un neobligātus elementus. Obligāti ir šādi elementi: tās puses pievienotās vērtības nodokļa (PVN) numurs, kas ir atbildīga par informācijas sniegšanu, atsauces periods, plūsma (saņemšana vai nosūtīšana), astoņu ciparu preču kods, partnera dalībvalsts (saņemamo preču nosūtīšanas dalībvalsts un nosūtāmo preču saņemšanas dalībvalsts), preču vērtība, preču daudzums (neto masa un papildu vienības) un transakcijas veids. Valstis/reģioni saskaņā ar dažādiem nosacījumiem var vākt arī neobligātus elementus. Daži no neobligātajiem elementiem ir izcelsmes valsts/reģions, piegādes nosacījumi, transportēšanas veids un detalizētāks preču kods nekā CN8, nosūtāmo preču izcelsmes reģions un saņemamo preču mērķa reģions, statistiskā procedūra, statistiskā vērtība, preču apraksts un iekraušanas/izkraušanas osta/lidosta.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat atskaišu veidošanas procesa apskats
Nākamajās sadaļās ir aprakstīta vispārējā informācijas plūsma, kas tiek izmantota Intrastat atskaitēm.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Ievadiet transakciju, kas šķērso citas ES valsts/reģiona robežu

Debitora rēķins, brīva teksta rēķins, pirkšanas rēķins, projekta rēķins, debitora pavadzīme, kreditora produktu ieejas plūsma vai pārsūtīšanas pasūtījums tiek pārsūtīti uz Intrastat žurnālu tikai tad, ja mērķa (nosūtīšanai) vai nosūtīšanas (saņemšanai) valsts/reģiona tips ir **ES**. Programmā Microsoft Dynamics 365 for Operations (1611) šis līdzeklis ir paplašināts un sniedz iespēju norādīt EK iekšējo transakciju iekraušanas adreses. Ja iekraušanas adrese atšķiras no kreditora uzņēmuma adreses (vai ja atšķiras debitora uzņēmuma adrese atgriešanas pasūtījumam), tad Intrastat pārskatu veidošana strādā ar šo informāciju. Kad veidojat kādu pārdošanas pasūtījumu, brīva teksta rēķinu, pirkšanas pasūtījumu, kreditora rēķinu, projekta rēķinu vai pārsūtīšanas pasūtījumu, dažiem laukiem, kas ir saistīti ar ārējo tirdzniecību, dokumenta virsrakstā vai rindā ir noklusējuma vērtības. Noklusējuma transakcijas kods tiek ņemts no atbilstošā lauka lapā **Ārējās tirdzniecības parametri**. Noklusējuma preču kods, izcelsmes valsts/reģions un izcelsmes novads tiek ņemti no krājuma. Šīs noklusējuma vērtības varat mainīt, ka arī varat aizpildīt citu ar ārējo tirdzniecību saistīto informāciju: statistisko procedūru, transportēšanas metodi un ostu.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Lietojiet Intrastat žurnālu, lai ģenerētu informāciju par tirdzniecību starp ES valstīm/reģioniem

Statistiskiem nolūkiem informāciju par tirdzniecību starp ES valstīm/reģioniem varat ģenerēt katru mēnesi. Transakcijas no brīva teksta rēķina, debitora rēķina, debitora pavadzīmes, kreditora rēķina, kreditora pavadzīmes, projekta rēķina vai pārsūtīšanas pasūtījuma varat pārsūtīt saskaņā ar pārsūtīšanas kritērijiem, kas ir iestatīti lapā **Ārējās tirdzniecības parametri**. Alternatīvi transakcijas varat ievadīt manuāli. Pārsūtītās transakcijas Intrastat žurnālā varat atjaunināt manuāli, ja ir nepieciešami atjauninājumi. Noteiktos apstākļos, kas ir iestatīti lapā **Intrastat arhivēšana**, varat saspiest transakcijas Intrastat žurnālā. Dažās valstīs/reģionos jums ir ļauts piemērot mazu transakciju slieksni. Pēc tam par transakcijām, kuras atrodas zem šī sliekšņa, varat ziņot saskaņā ar norādīto preču kodu. Preču kodu atbilstošajās Intrastat žurnāla rindās varat atjaunināt, pamatojoties uz iestatījumu **Minimālā robeža** lapā **Ārējās tirdzniecības parametri**. Šīs transakcijas varat arī saspiest, pamatojoties uz iestatījumu **Intrastat arhivēšana**. Intrastat žurnālā iekļauto transakciju pilnību varat pārbaudīt, pamatojoties uz iestatījumu **Pārbaudīt iestatījumu** lapā **Ārējās tirdzniecības parametri**. Iespējams, atbilstošajos laukos var pārbaudīt datu pilnību: valsts/reģions, novads, svars, preču kods, transakcijas kods, papildu vienība, osta, izcelsme, piegādes nosacījumi, transportēšanas metode un PVN reģistrācijas numurs. Transakcijas, kas nav pabeigtas, tiks atzīmētas kā nederīgas.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Lietojiet Intrastat žurnālu, lai ziņotu informāciju par tirdzniecību starp ES valstīm/reģioniem

Statistiskiem nolūkiem informāciju par tirdzniecību starp ES valstīm/reģioniem varat ziņot katru mēnesi. Intrastat atskaiti varat drukāt, pamatojoties uz iestatījumiem **Atskaites formāta kartēšana** lapā **Ārējās tirdzniecības parametri**. Varat arī ģenerēt elektronisku failu, pamatojoties uz iestatījumiem **Faila formāta kartēšana** lapā **Ārējās tirdzniecības parametri**. Papildinformāciju par Intrastat pārskatu veidošanu, tostarp nepieciešamajiem priekšnosacījumiem, skatiet Intrastat pārskatu veidošanas uzdevumu ierakstos:

-   Ģenerēt ES Intrastat deklarāciju;
-   Pārsūtīt transakcijas uz Intrastat;
-   EK iekšējo transakciju iekraušanas adreses norādīšana.

## <a name="prerequisites"></a>Priekšnosacījumi
Nākamajā tabulā ir uzskaitīti priekšnosacījumi Intrastat pārskatu veidošanai.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Priekšnoteikumi</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Adreses iestatīšana</td>
<td>Iestatiet Starptautiskā Standartizācijas organizācijas (ISO) kodus valstīm/reģioniem.</td>
</tr>
<tr class="even">
<td>Juridiska persona</td>
<td>Iestatiet PVN reģistrācijas numurus importēšanai/eksportēšanai, filiāles numura paplašinājumu importēšanai/eksportēšanai un Intrastat kodu, kas ir piešķirts juridiskajai personai.</td>
</tr>
<tr class="odd">
<td>Preču kategoriju hierarhija (pārdošanas hierarhija, sagādes hierarhija)</td>
<td>Piešķiriet Intrastat preču kodus kategoriju mezgliem cilnē <strong>Preču kodi</strong>, lapā <strong>Kategoriju hierarhija</strong>. Kad kādu preču kodu piešķirat pamatkategorijas zaram, šis kods ir attiecināms uz visiem apakškategoriju zariem. Atlasītie preču kodi būs pieejami skatā <strong>Atlasīts</strong>, kad atlasāt preču kodu izlaisto preču detalizētajā informācijā, kā arī pārdošanas pasūtījuma, pirkšanas pasūtījuma un pārsūtīšanas pasūtījuma rindās.</td>
</tr>
<tr class="even">
<td>Detalizēta informācija par izlaistajām precēm</td>
<td>Izlaistajām precēm iestatiet šādus ārējās tirdzniecības datus:
<ul>
<li><strong>Preču kods</strong> — atlasiet no atlasīto preču saraksta, kas ir izgūts no piešķirtajām preču kategorijām vai no pilnā Intrastat preču kodu saraksta.</li>
<li><strong>Statistiskie maksu procenti</strong></li>
<li><strong>Izcelsmes valsts/reģions</strong> — atlasiet noklusējuma valsti/reģionu, kur preces tika pilnībā iegūtas vai saražotas.</li>
<li><strong>Izcelsmes/adresāta novads</strong> — saņemamajām precēm atlasiet mērķa noklusējuma novadu un nosūtāmajam precēm atlasiet izcelsmes noklusējuma novadu.</li>
<li><strong>Neto svars (kg)</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Debitori</td>
<td>Iestatiet debitora piegādes adresi ES valstī/reģionā.</td>
</tr>
<tr class="even">
<td>Kreditori</td>
<td>Iestatiet kreditora adresi ES valstī/reģionā.</td>
</tr>
<tr class="odd">
<td>Papildmaksas</td>
<td>Iestatiet papildmaksu kodu, ko iekļaut rēķina summā, statistiskajā summā vai abās. Lapā <strong>Maksu kodi</strong>, cilnē <strong>Ārējā tirdzniecība</strong> iespējojiet opciju <strong>Intrastat rēķina vērtība</strong>, lai maksu summu iekļautu rēķina vērtībā, un iespējojiet opciju <strong>Intrastat statistiska vērtība</strong>, lai šo maksu summu iekļautu statistiskajā vērtībā.</td>
</tr>
<tr class="even">
<td>Elektroniskie pārskati</td>
<td>Iestatiet elektronisko pārskatu izveides konfigurācijas, lai eksportētu Intrastat datus uz elektronisku failu, kura formāts atbilst attiecīgo iestāžu prasībām, un priekšskatītu Intrastat datus lietotājam draudzīgā, lasāmā formātā (piemēram, Microsoft Excel formātā).</td>
</tr>
<tr class="even">
<td>Noliktavas</td>
<td>Kreditoru kontus saistiet ar noliktavu kodiem, lai aizpildītu PVN reģistrācijas numuru, kad veicat pārsūtīšanas pasūtījuma pārsūtīšanu.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Iestatījumi
Nākamajās sadaļās ir aprakstīti Intrastat atskaitēm nepieciešamie iestatījumi.

### <a name="set-up-all-required-intrastat-related-lists"></a>Iestatiet visus nepieciešamos ar Intrastat saistītos sarakstus

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Saraksts</th>
<th>Papildinformācija</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Preču kodi</td>
<td>Iestatiet kategoriju hierarhiju ar tipu <strong>Preču kods</strong> un ievadiet visus preču kodus saskaņā ar kombinētās nomenklatūru sarakstu. Katrai precei jūs iestatāt šādu informāciju:
<ul>
<li>Preces nosaukums un preces kods</li>
<li>Draudzīgais nosaukums un/vai tulkotais nosaukums</li>
<li>Iestatījumi papildu vienību ziņošanai cilnē <strong>Ārējā tirdzniecība</strong>. Šo papildu vienību varat atlasīt vienību sarakstā. Varat arī norādīt, vai preču svars ir jāziņo papildus atlasītajai papildu vienībai.</li>
</ul></td>
</tr>
<tr class="even">
<td>Darbību kodi</td>
<td>Iestatiet transakcijas veidu saskaņā ar jūsu valsts/reģiona prasībām. Katram jūsu iestatītajam transakcijas kodam jums ir jāiestata kārtulas rēķinu summu un statistisko summu aprēķināšanai pārsūtīšanas pasūtījumiem un pārdošanas/pirkšanas pasūtījumiem.
<ul>
<li>Pārsūtīšanas pasūtījumiem rēķina summu un statistisko summu aprēķināšanai jūs iestatāt vienu no šādām kārtulām:
<ul>
<li><strong>Tukšs</strong> — summa būs 0 (nulle).</li>
<li><strong>Finanšu izmaksu summa</strong> — summa būs vienāda ar finanšu izmaksām.</li>
<li><strong>Kopējās izmaksas</strong> — summa būs vienāda ar transakcijas kopējām izmaksām.</li>
<li><strong>Manuāls</strong> — summa būs vienāda ar summu, kas ir manuāli norādīta pārsūtīšanas pasūtījuma rindā.</li>
</ul></li>
<li>Pārdošanas pasūtījumiem un pirkšanas pasūtījumiem rēķina summu un statistisko summu aprēķināšanai jūs iestatāt vienu no šādām kārtulām:
<ul>
<li><strong>Tukšs</strong> — summa būs 0 (nulle).</li>
<li><strong>Rēķina summa</strong> — summa būs vienāda ar summu, kas ir iekļauta rēķinā par šo preci.</li>
<li><strong>Pamatsumma</strong> — summa būs vienāda ar summu, par kādu tiktu izrakstīts rēķins, pirms tiek piemērotas jebkādas atlaides.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Transportēšanas metodes</td>
<td>Iestatiet transportēšanas režīmu saskaņā ar jūsu valsts/reģiona prasībām. Katram piegādes režīmam varat iestatīt noklusējuma transportēšanas metodi cilnē <strong>Ārējā tirdzniecība</strong>.</td>
</tr>
<tr class="even">
<td>Ostas</td>
<td>Iestatiet iekraušanas/izkraušanas ostu/lidostu, ja jūsu valsts/reģions vāc šo informāciju.</td>
</tr>
<tr class="odd">
<td>Statistikas procedūras</td>
<td>Iestatiet statistikas procedūru, ja jūsu valsts/reģions vāc šo informāciju.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Iestatiet kārtulas Intrastat transakciju arhivēšanai

Lapā **Intrastat arhivēšana** varat atlasīt laukus, kurus izmantot saspiešanai. Visas transakcijas, kurām atlasītajiem laukiem Intrastat žurnālā ir tāda pati vērtību kombinācija, tiks saspiestas vienā transakcijā, kad Intrastat žurnālā palaižat saspiešanas funkciju.

### <a name="set-up-foreign-trade-parameters"></a>Iestatīt starptautiskās tirdzniecības parametrus

Lai iestatītu parametrus nākamajā tabulā, izmantojiet lapu **Ārējās tirdzniecības parametri**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Cilne</th>
<th>Parametri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vispārīgi</td>
<td><ul>
<li><strong>Vispārīgi</strong> — norādiet tālāk aprakstīto informāciju.
<ul>
<li>Noklusējuma transakcijas kodi pārdošanas pasūtījumiem, pirkšanas pasūtījumiem, kredīta notām un pārsūtīšanas pasūtījumiem. Transakcijas kods, kas ir iestatīts kredīta notām, tiek izmantots arī kā kods fizisko preču atgriešanai, un tas tiek izmantots noviržu fiziskajās atgriešanās pret labojumu kredīta notām. Par fizisko preču atgriešanu tiek ziņots Intrastat pārsūtīšanā ar atšķirīgu virzienu. Tiek ziņots, ka saņemšanas atgriešana ir ziņota kā nosūtīšana, un nosūtīšanas atgriešana tiek ziņota kā saņemšana.</li>
<li>Darbinieks, kas ir atbildīgs par Intrastat atskaišu sagatavošanu.</li>
</ul></li>
<li><strong>Minimālā robeža</strong> — norādiet iestatījumus tādu transakciju atjaunināšanai, kas ir zem sliekšņa.
<ul>
<li>Sliekšņa summa un svars</li>
<li>Preču kods, ko lietot transakcijām, kuras atrodas zem sliekšņa</li>
</ul></li>
<li><strong>Pārsūtīt</strong> — norādiet kritērijus transakciju pārsūtīšanai uz Intrastat žurnālu. Varat norādīt, ka transakcijas tiek pārsūtītas tikai tad, ja krājumi atbilst vienam vai visiem no tālāk norādītajiem kritērijiem.
<ul>
<li>Krājumi nav pakalpojumu krājumi.</li>
<li>Krājumiem nav preces koda.</li>
<li>Krājumiem ir svars.</li>
<li>Krājumiem ir papildu vienības.</li>
</ul></li>
<li><strong>Pārbaudīt iestatījumus</strong> — norādiet kārtulas Intrastat datu pilnīguma pārbaudīšanai. Varat atlasīt, kuri dati tiek pārbaudīti.</li>
<li><strong>Noapaļošanas nosacījumi</strong> — norādiet tālāk uzskaitītos iestatījumus attiecībā uz summu un svaru noapaļošanu Intrastat atskaitēs.
<ul>
<li>Noapaļošanas nosacījums (precizitāte)</li>
<li>Noapaļošanas metode: uz augšu, uz leju vai parastā</li>
<li>Decimāldaļskaitļu vietu skaits summām un svariem</li>
<li>Instrukcijas par tādu svaru noapaļošanu, kas ir mazāk par 1 kilogramu (kg): uz augšu līdz 1 kg, parastā, vai bez noapaļošanas</li>
</ul></li>
<li><strong>Elektronisko atskaišu veidošana</strong> — norādiet atsauces uz elektronisko atskaišu konfigurācijām, lai varētu ģenerēt elektronisku failu un atskaiti.</li>
<li><strong>Preču kodu hierarhija</strong> — norādiet kategoriju hierarhiju ar tipu <strong>Preču kods</strong>, kas apzīmē Intrastat preču kodu CN8.</li>
  <li> <strong>Maiņas kursa tips</strong> — ja vēlaties, norādiet maiņas kursu, ko izmantot, lai ziņotu par Intrastat pārdošanas un pirkšanas transakcijām ārvalstu valūtās. Šis vienums tiek izmantots arī tad, ja kurss atšķiras no maiņas kursa, kas tiek lietots transakcijas grāmatošanai.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Aģenta kontaktinformācija</td>
<td>Norādiet aģenta nosaukumu/vārdu un uzvārdu, adresi, PVN reģistrācijas numuru, tālruņa numuru un faksa numuru.</td>
</tr>
<tr class="odd">
<td>Valsts/reģiona rekvizīti</td>
<td>Pašreizējās juridiskās personas valsti/reģionu iestatiet uz <strong>Iekšzemes</strong>. ES valstīm/reģioniem, kas piedalās ES tirdzniecībā ar pašreizējo juridisko personu, valsti/reģionu iestatiet uz <strong>ES</strong>. Katrai valstij/reģionam jūs norādāt arī valsts/reģiona kodu ārējās tirdzniecības nolūkiem.</td>
</tr>
<tr class="even">
<td>Numuru sērija</td>
<td>Norādiet numuru secību Intrastat žurnālam.</td>
</tr>
</tbody>
</table>

