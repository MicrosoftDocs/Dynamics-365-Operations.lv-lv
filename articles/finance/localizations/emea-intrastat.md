---
title: Intrastat pārskats
description: Šajā rakstā ir sniegta informācija par Intrastat atskaišu veidošanu preču — un noteiktos gadījumos arī pakalpojumu — tirdzniecībai starp dažādām Eiropas Savienības (ES) valstīm/reģioniem.
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9360f97506ac7bdf67bb2f1b296f01b6ed49b39f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894782"
---
# <a name="intrastat-overview"></a>Intrastat pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par Intrastat atskaišu veidošanu preču — un noteiktos gadījumos arī pakalpojumu — tirdzniecībai starp dažādām Eiropas Savienības (ES) valstīm/reģioniem. Šajā rakstā ir sniegts arī pārskatu veidošanas procesa apskats un aprakstīti nepieciešamie iestatījumi un priekšnosacījumi.

Intrastat ir sistēma informācijas vākšanai un statistikas ģenerēšanai par preču tirdzniecību starp dažādām Eiropas Savienības (ES) valstīm/reģioniem. Intrastat atskaites ir nepieciešamas vienmēr, kad prece šķērso citas ES valsts/reģiona robežu. Vairākās valstīs/reģionos Intrastat atskaites attiecas arī uz pakalpojumiem. Intrastat atskaitēs var vākt obligātus un neobligātus elementus. Obligāti ir šādi elementi: tās puses pievienotās vērtības nodokļa (PVN) numurs, kas ir atbildīga par informācijas sniegšanu, atsauces periods, plūsma (saņemšana vai nosūtīšana), astoņu ciparu preču kods, partnera dalībvalsts (saņemamo preču nosūtīšanas dalībvalsts un nosūtāmo preču saņemšanas dalībvalsts), preču vērtība, preču daudzums (neto masa un papildu vienības) un transakcijas veids. Valstis/reģioni saskaņā ar dažādiem nosacījumiem var vākt arī neobligātus elementus. Daži no neobligātajiem elementiem ir izcelsmes valsts/reģions, piegādes nosacījumi, transportēšanas veids un detalizētāks preču kods nekā CN8, nosūtāmo preču izcelsmes reģions un saņemamo preču mērķa reģions, statistiskā procedūra, statistiskā vērtība, preču apraksts un iekraušanas/izkraušanas osta/lidosta.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat atskaišu veidošanas procesa apskats
Nākamajās sadaļās ir aprakstīta vispārējā informācijas plūsma, kas tiek izmantota Intrastat atskaitēm.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Ievadiet transakciju, kas šķērso citas ES valsts/reģiona robežu

Debitora rēķins, brīva teksta rēķins, pirkšanas rēķins, projekta rēķins, debitora pavadzīme, kreditora produktu ieejas plūsma vai pārsūtīšanas pasūtījums tiek pārsūtīti uz Intrastat žurnālu tikai tad, ja mērķa (nosūtīšanai) vai nosūtīšanas (saņemšanai) valsts/reģiona tips ir **ES**. Programmā Microsoft Dynamics 365 for Operations (1611) šis līdzeklis ir paplašināts un sniedz iespēju norādīt EK iekšējo transakciju iekraušanas adreses. Ja iekraušanas adrese atšķiras no kreditora uzņēmuma adreses (vai ja atšķiras debitora uzņēmuma adrese atgriešanas pasūtījumam), tad Intrastat pārskatu veidošana strādā ar šo informāciju. Kad veidojat kādu pārdošanas pasūtījumu, brīva teksta rēķinu, pirkšanas pasūtījumu, kreditora rēķinu, projekta rēķinu vai pārsūtīšanas pasūtījumu, dažiem laukiem, kas ir saistīti ar ārējo tirdzniecību, dokumenta virsrakstā vai rindā ir noklusējuma vērtības. Noklusējuma transakcijas kods tiek ņemts no atbilstošā lauka lapā **Ārējās tirdzniecības parametri**. Noklusējuma preču kods, izcelsmes valsts/reģions un izcelsmes novads tiek ņemti no krājuma. Šīs noklusējuma vērtības varat mainīt, ka arī varat aizpildīt citu ar ārējo tirdzniecību saistīto informāciju: statistisko procedūru, transportēšanas metodi un ostu.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Lietojiet Intrastat žurnālu, lai ģenerētu informāciju par tirdzniecību starp ES valstīm/reģioniem

Statistiskiem nolūkiem informāciju par tirdzniecību starp ES valstīm/reģioniem varat ģenerēt katru mēnesi. Transakcijas no brīva teksta rēķina, debitora rēķina, debitora pavadzīmes, kreditora rēķina, kreditora pavadzīmes, projekta rēķina vai pārsūtīšanas pasūtījuma varat pārsūtīt saskaņā ar pārsūtīšanas kritērijiem, kas ir iestatīti lapā **Ārējās tirdzniecības parametri**. Alternatīvi transakcijas varat ievadīt manuāli. Pārsūtītās transakcijas Intrastat žurnālā varat atjaunināt manuāli, ja ir nepieciešami atjauninājumi. Noteiktos apstākļos, kas ir iestatīti lapā **Intrastat arhivēšana**, varat saspiest transakcijas Intrastat žurnālā. Dažās valstīs/reģionos jums ir ļauts piemērot mazu transakciju slieksni. Pēc tam par transakcijām, kuras atrodas zem šī sliekšņa, varat ziņot saskaņā ar norādīto preču kodu. Preču kodu atbilstošajās Intrastat žurnāla rindās varat atjaunināt, pamatojoties uz iestatījumu **Minimālā robeža** lapā **Ārējās tirdzniecības parametri**. Šīs transakcijas varat arī saspiest, pamatojoties uz iestatījumu **Intrastat arhivēšana**. Intrastat žurnālā iekļauto transakciju pilnību varat pārbaudīt, pamatojoties uz iestatījumu **Pārbaudīt iestatījumu** lapā **Ārējās tirdzniecības parametri**. Iespējams, atbilstošajos laukos var pārbaudīt datu pilnību: valsts/reģions, novads, svars, preču kods, transakcijas kods, papildu vienība, osta, izcelsme, piegādes nosacījumi, transportēšanas metode un PVN reģistrācijas numurs. Transakcijas, kas nav pabeigtas, tiks atzīmētas kā nederīgas.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Lietojiet Intrastat žurnālu, lai ziņotu informāciju par tirdzniecību starp ES valstīm/reģioniem

Statistiskiem nolūkiem informāciju par tirdzniecību starp ES valstīm/reģioniem varat ziņot katru mēnesi. Intrastat atskaiti varat drukāt, pamatojoties uz iestatījumiem **Atskaites formāta kartēšana** lapā **Ārējās tirdzniecības parametri**. Varat arī ģenerēt elektronisku failu, pamatojoties uz iestatījumiem **Faila formāta kartēšana** lapā **Ārējās tirdzniecības parametri**. Papildinformāciju par Intrastat pārskatu veidošanu, tostarp nepieciešamajiem priekšnosacījumiem, skatiet Intrastat pārskatu veidošanas uzdevumu ierakstos:

  - Ģenerēt ES Intrastat deklarāciju;
  - Pārsūtīt transakcijas uz Intrastat;
  - EK iekšējo transakciju iekraušanas adreses norādīšana.

## <a name="prerequisites"></a>Priekšnosacījumi
Nākamajā tabulā ir uzskaitīti priekšnosacījumi Intrastat pārskatu veidošanai.

|  Priekšnoteikumi  |  Apraksts  |
|-------------------------|-------------------------|
| Adreses iestatīšana | Iestatiet Starptautiskā Standartizācijas organizācijas (ISO) kodus valstīm/reģioniem. |
| Juridiska persona | Iestatiet PVN reģistrācijas numurus importēšanai/eksportēšanai, filiāles numura paplašinājumu importēšanai/eksportēšanai un Intrastat kodu, kas ir piešķirts juridiskajai personai. |
| Preču kategoriju hierarhija (pārdošanas hierarhija, sagādes hierarhija) | Piešķiriet Intrastat preču kodus kategoriju mezgliem cilnē **Preču kodi**, lapā **Kategoriju hierarhija**. Kad kādu preču kodu piešķirat pamatkategorijas zaram, šis kods ir attiecināms uz visiem apakškategoriju zariem. Atlasītie preču kodi būs pieejami skatā **Atlasīts**, kad atlasāt preču kodu preču detalizētajā informācijā, kā arī pārdošanas pasūtījuma, pirkšanas pasūtījuma un pārsūtīšanas pasūtījuma rindās. |
| Detalizēta informācija par izlaistajām precēm | Izlaistajām precēm iestatiet šādus ārējās tirdzniecības datus:<ul><li>**Preču kods** — atlasiet no atlasīto preču saraksta, kas ir izgūts no piešķirtajām preču kategorijām vai no pilnā Intrastat preču kodu saraksta.</li><li>**Statistiskie maksu procenti**</li><li>**Izcelsmes valsts/reģions** — atlasiet noklusējuma valsti/reģionu, kur preces tika pilnībā iegūtas vai saražotas.</li><li>**Izcelsmes/adresāta novads** — saņemamajām precēm atlasiet mērķa noklusējuma novadu un nosūtāmajam precēm atlasiet izcelsmes noklusējuma novadu.</li><li>**Neto svars (kg)**</li><li>**Izslēgt** - aktivizējiet šo parametru, lai nepārsūta darījumus ar šo preci uz Intrastat</li></ul> |
| Debitori | Iestatiet debitora piegādes adresi ES valstī/reģionā. |
| Kreditori | Iestatiet kreditora adresi ES valstī/reģionā. |
| Papildmaksas | Iestatiet papildmaksu kodu, ko iekļaut rēķina summā, statistiskajā summā vai abās. Lapā **Maksu kodi**, cilnē **Ārējā tirdzniecība** iespējojiet opciju **Intrastat rēķina vērtība**, lai maksu summu iekļautu rēķina vērtībā, un iespējojiet opciju **Intrastat statistiska vērtība**, lai šo maksu summu iekļautu statistiskajā vērtībā.</br>Lai iegūtu papildu informāciju, pārskatiet [Darbību kodu un papildmaksu](#transaction-codes-and-miscellaneous-charges) piemērus. |
| Elektroniskie pārskati | Iestatiet elektronisko pārskatu izveides konfigurācijas, lai eksportētu Intrastat datus uz elektronisku failu, kura formāts atbilst attiecīgo iestāžu prasībām, un priekšskatītu Intrastat datus lietotājam draudzīgā, lasāmā formātā (piemēram, Microsoft Excelformātā). |
| Noliktavas | Kreditoru kontus saistiet ar noliktavu kodiem, lai aizpildītu PVN reģistrācijas numuru, kad veicat pārsūtīšanas pasūtījuma pārsūtīšanu.</br>Lai iegūtu papildu informāciju, skatiet [Pārsūtīšanas pasūtījuma](#transfer-order) piemēru.|

## <a name="setup"></a>Iestatīt
Nākamajās sadaļās ir aprakstīti Intrastat atskaitēm nepieciešamie iestatījumi.

### <a name="set-up-all-required-intrastat-related-lists"></a>Iestatiet visus nepieciešamos ar Intrastat saistītos sarakstus

|   Saraksts   |   Papildinformācija   |
|-------------------------|-------------------------|
| Preču kodi | Iestatiet kategoriju hierarhiju ar tipu **Preču kods** un ievadiet visus preču kodus saskaņā ar kombinētās nomenklatūru sarakstu. Katrai precei jūs iestatāt šādu informāciju:<ul><li>Preces nosaukums un preces kods</li><li>Draudzīgais nosaukums un/vai tulkotais nosaukums</li><li>Iestatījumi papildu vienību ziņošanai cilnē **Ārējā tirdzniecība**. Šo papildu vienību varat atlasīt vienību sarakstā. Varat arī norādīt, vai preču svars ir jāziņo papildus atlasītajai papildu vienībai.</li></ul>Lai iegūtu papildu informāciju, skatiet [Papildu vienību](#additional-units) piemērus.|
| Darbību kodi | Iestatiet transakcijas veidu saskaņā ar jūsu valsts/reģiona prasībām. Katram jūsu iestatītajam transakcijas kodam jums ir jāiestata kārtulas rēķinu summu un statistisko summu aprēķināšanai pārsūtīšanas pasūtījumiem un pārdošanas/pirkšanas pasūtījumiem.<ul><li>Pārsūtīšanas pasūtījumiem rēķina summu un statistisko summu aprēķināšanai jūs iestatāt vienu no šādām kārtulām:<ul><li>**Tukšs** — summa būs 0 (nulle).</li><li>**Finanšu izmaksu summa** — summa būs vienāda ar finanšu izmaksām.</li><li>**Kopējās izmaksas** — summa būs vienāda ar transakcijas kopējām izmaksām.</li><li>**Manuāls** — summa būs vienāda ar summu, kas ir manuāli norādīta pārsūtīšanas pasūtījuma rindā.</li></ul></li><li>Pārdošanas pasūtījumiem un pirkšanas pasūtījumiem rēķina summu un statistisko summu aprēķināšanai jūs iestatāt vienu no šādām kārtulām:<ul><li>**Tukšs** — summa būs 0 (nulle).</li><li>**Rēķina summa** — summa būs vienāda ar summu, kas ir iekļauta rēķinā par šo preci.</li><li>**Pamatsumma** — summa būs vienāda ar summu, par kādu tiktu izrakstīts rēķins, pirms tiek piemērotas jebkādas atlaides.</li></ul></ul>Lai iegūtu papildu informāciju, pārskatiet [Darbību kodu un papildmaksu](#transaction-codes-and-miscellaneous-charges) piemērus. |
| Transportēšanas metodes | Iestatiet transportēšanas režīmu saskaņā ar jūsu valsts/reģiona prasībām. Katram piegādes režīmam varat iestatīt noklusējuma transportēšanas metodi cilnē **Ārējā tirdzniecība**. |
| Ostas | Iestatiet iekraušanas/izkraušanas ostu/lidostu, ja jūsu valsts/reģions vāc šo informāciju. |
| Statistikas procedūras | Iestatiet statistikas procedūru, ja jūsu valsts/reģions vāc šo informāciju. |



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
<li><strong>Vispārīgi</strong> — norādiet tālāk aprakstīto informāciju.
<ul>
<li>Noklusējuma transakcijas kodi pārdošanas pasūtījumiem, pirkšanas pasūtījumiem, kredīta notām un pārsūtīšanas pasūtījumiem. Transakcijas kods, kas ir iestatīts kredīta notām, tiek izmantots arī kā kods fizisko preču atgriešanai, un tas tiek izmantots noviržu fiziskajās atgriešanās pret labojumu kredīta notām. Par fizisko preču atgriešanu tiek ziņots Intrastat pārsūtīšanā ar atšķirīgu virzienu. Tiek ziņots, ka saņemšanas atgriešana ir ziņota kā nosūtīšana, un nosūtīšanas atgriešana tiek ziņota kā saņemšana.</li>
<li>Darbinieks, kas ir atbildīgs par Intrastat atskaišu sagatavošanu.</li>
</ul></li>
<li><strong>Minimālā robeža</strong> — norādiet iestatījumus tādu transakciju atjaunināšanai, kas ir zem sliekšņa.
<ul>
<li>Sliekšņa summa un svars</li>
<li>Preču kods, ko lietot transakcijām, kuras atrodas zem sliekšņa</li>
</ul></li>
<li><strong>Pārsūtīt</strong> — norādiet kritērijus transakciju pārsūtīšanai uz Intrastat žurnālu. Varat norādīt, ka transakcijas tiek pārsūtītas tikai tad, ja krājumi atbilst vienam vai visiem no tālāk norādītajiem kritērijiem.
<ul>
<li>Krājumi nav&#39;pakalpojumu krājumi.</li>
<li>Krājumiem nav preces koda.</li>
<li>Krājumiem ir svars.</li>
<li>Krājumiem ir papildu vienības.</li>
</ul></li>
<li><strong>Pārbaudīt iestatījumus</strong> — norādiet kārtulas Intrastat datu pilnīguma pārbaudīšanai. Varat atlasīt, kuri dati tiek pārbaudīti.</li>
<li><strong>Noapaļošanas nosacījumi</strong> — norādiet tālāk uzskaitītos iestatījumus attiecībā uz summu un svaru noapaļošanu Intrastat atskaitēs.
<ul>
<li>Noapaļošanas nosacījums (precizitāte)</li>
<li>Noapaļošanas metode: uz augšu, uz leju vai parastā</li>
<li>Decimāldaļskaitļu vietu skaits summām un svariem</li>
<li>Instrukcijas par tādu svaru noapaļošanu, kas ir mazāk par 1 kilogramu (kg): uz augšu līdz 1 kg, parastā, vai bez noapaļošanas</li>
</ul></li>
<li><strong>Elektronisko atskaišu veidošana</strong> — norādiet atsauces uz elektronisko atskaišu konfigurācijām, lai varētu ģenerēt elektronisku failu un atskaiti.</li>
<li><strong>Preču kodu hierarhija</strong> — norādiet kategoriju hierarhiju ar tipu <strong>Preču kods</strong>, kas apzīmē Intrastat preču kodu CN8.</li>
  <li> <strong>Maiņas kursa tips</strong> — ja vēlaties, norādiet maiņas kursu, ko izmantot, lai ziņotu par Intrastat pārdošanas un pirkšanas transakcijām ārvalstu valūtās. Šis vienums tiek izmantots arī tad, ja kurss atšķiras no maiņas kursa, kas tiek lietots transakcijas grāmatošanai.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Aģenta kontaktinformācija</td>
<td>Norādiet aģenta&#39;nosaukumu/vārdu un uzvārdu, adresi, PVN reģistrācijas numuru, tālruņa numuru un faksa numuru.</td>
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

## <a name="example"></a>Paraugs

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a> Darbību kodi un papildmaksas

Šis raksts sedz scenāriju, kad uzņēmumam Vācijā jāiegādājas preces no uzņēmuma Itālijā. Lai veiktu šo pirkumu, Vācijas uzņēmumam jāiestata jauni darbību kodi un jākonfigurē aprēķina noteikumi rēķina summai un statistiskai summai šiem darbību kodiem. Turklāt, kad uzņēmums veido rēķinu, tam jānorāda papildmaksas un to procenti. Šīs vērtības tiks izskatītas, kad tiek aprēķināta statistiskā vērtība.

Šajā scenārijā tiek izmantota **PRETVG** juridiskā persona.

#### <a name="preliminary-setup"></a>Iepriekšēja iestatīšana

1. Dodieties **uz organizācijas** > **administrēšanas** > **organizācijas juridiskajām** personām un atlasiet **NOROBEŽOTAS.**
2. Kopsavilkuma cilnē **Adreses** pārbaudiet, vai valsts/reģiona **lauks ir** iestatīts uz **DEU(Vācija).**
3. Dodieties uz **Kreditoru parādiem** > **visiem kreditoriem** > **·**.
4. Režģī atlasiet **DE-001**.
5. Kopsavilkuma cilnē **Adrese** atlasiet **Rediģēt**.
6. Dialoglodziņā **Rediģēt adresi** laukā **Valsts/reģions** atlasiet **ITA**.
7. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

#### <a name="set-up-transaction-codes"></a>Iestatīt darbību kodus

1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transakciju kodi**.
2. Režģī atlasiet **11**. Pēc tam Darbību rūtī atlasiet **Dzēst**.
3. Darbību rūtī atlasiet **Jauns**.
4. Kopsavilkuma cilnes **Darbības kodi** laukā Darbības **kods** **ievadiet** **11.**
5. Laukā **Nosaukums** ievadiet Outright **purchase/sale**.
6. **Sadaļā Pārdošana un pirkumi**, laukā **Rēķina summa** atlasiet **Rēķina summa**.
7. Laukā **Statistiskā** summa atlasiet **Rēķina summa**.
8. Darbību rūtī atlasiet **Saglabāt**.

#### <a name="set-up-miscellaneous-charges"></a>Papildmaksu iestatīšana

1. Dodieties uz **sadaļu Parādu kreditoriem** > **maksu iestatījuma** > **izmaksu kods**.
2. Režģī atlasiet **Transports**.
3. Darbību rūtī atlasiet **Rediģēt**.
4. Kopsavilkuma cilnē **Ārējā tirdzniecība** iestatiet Intrastat rēķina vērtību **un** Intrastat statistiskās **vērtības opcijas** uz **Jā**.

#### <a name="set-up-foreign-trade-parameters"></a>Iestatīt starptautiskās tirdzniecības parametrus

1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
2. Kopsavilkuma cilnes **Vispārīgi** cilnes **Intrastat** laukā **Darījuma** **kods** atlasiet **11**.
3. Kopsavilkuma cilnē **Preču kodu hierarhija** pārbaudiet, vai kategoriju **hierarhijas lauks** ir iestatīts uz **Intrastat**.

#### <a name="create-a-purchase-order"></a>Pirkuma pasūtījuma izveide

1. Atveriet **Kreditori** > **Pirkšanas pasūtījumi** > **Visi pirkšanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņa **Pirkšanas pasūtījuma izveide** laukā **Kreditora konts** atlasiet **DE-001**.
4. Atlasiet **Labi**.
5. Cilnē **Virsraksts** kopsavilkuma cilnē **Ārējā** **tirdzniecība** laukam **Transakcijas kods** jābūt **11**.
6. Cilnē **Rindas** kopsavilkuma cilnes **Pirkšanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **D0003**. Laukā **Daudzums** ievadiet **10**.
7. Kopsavilkuma cilnes **Ārējā tirdzniecība kopsavilkuma** **cilnē Ārējā tirdzniecība pārbaudiet,** **·** **vai darbības koda lauks ir iestatīts automātiski.**
8. Kopsavilkuma cilnes **Pirkšanas** pasūtījuma rindas izvēlnē **Finanšu sadaļas** Maksas **atlasiet** Uzturēt **maksas**.
9. Maksas koda **laukā** atlasiet **TRANSPORTS**.
10. Laukā **Izmaksu vērtība** ievadiet **30**.
11. Darbību rūtī atlasiet **Saglabāt**. Tad aizveriet lapu.
12. Darbību rūts cilnē **Pirkšana**, grupā **Darbības** atlasiet **Apstiprināt**.
13. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
14. Darbību rūtī atlasiet **Noklusējuma vērtība No**. Laukā **Noklusējuma daudzums rindām** atlasiet **Pasūtītais daudzums**. Pēc tam atlasiet **Labi**.
15. Kopsavilkuma cilnes **Kreditora rēķina virsraksts** sadaļā **Rēķina identifikācija** laukā **Numurs** ievadiet **00100**.
16. Sadaļā Rēķina **datumi** laukā Rēķina **datums** **atlasiet 2021. gada 11. aprīli (2021**. gada 24. novembris).
17. Darbību rūtī atlasiet **Grāmatot**, lai grāmatotu žurnālu.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Pārsūtīt kreditora rēķinu uz Intrastat žurnālu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Pārsūtīt**.
3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Kreditora rēķins** uz **Jā**.
4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu.

   ![Rinda, kas attēlo pirkšanas pasūtījumu Intrastat lapā ar papildmaksām](media/intrastat_overview_1.png)

5. Pārskatiet pirkšanas pasūtījuma cilni **Vispārīgi**. Ņemiet vērā **,** **·** **·** **·** **·** **ka laukā Rēķina vērtība ir parādīta lauku Rēķina summa un Rēķina papildmaksu summa un lauks Statistiskā vērtība rāda lauku Statistiskā summa un Statistiskās summas** summa summu.

   ![Pirkšanas pasūtījuma detaļas ar papildmaksām Intrastat lapas cilnē Vispārīgi](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>Pārsūtīšanas pasūtījums

Šajā piemērā uzņēmumam Vācijā jāpārvieto divas preču vienības no Vācijas noliktavas uz Itālijas noliktavu. Maksas ar likmi 20 procenti arī jānorāda šai precei uzskaitei laukā **Statistiskā** vērtība. Šajā piemērā tiek lietota **DEMF** juridiska persona.

#### <a name="preliminary-setup"></a>Iepriekšēja iestatīšana

1. Dodieties **uz organizācijas** > **administrēšanas** > **organizācijas juridiskajām** personām un atlasiet **NOROBEŽOTAS.**
2. Kopsavilkuma cilnē **Adreses** pārbaudiet, vai valsts/reģiona **lauks ir** iestatīts uz **DEU(Vācija).**
3. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
4. Kopsavilkuma cilnē **Preču kodu hierarhija** pārbaudiet, vai kategoriju **hierarhijas lauks** ir iestatīts uz **Intrastat**.
5. Dodieties uz **Kreditoru parādiem** > **visiem kreditoriem** > **·**.
6. Režģī atlasiet **DE-001**.
7. Kopsavilkuma cilnē **Adrese** atlasiet **Rediģēt**.
8. Dialoglodziņā **Rediģēt adresi** laukā **Valsts/reģions** atlasiet **ITA**.
9. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

#### <a name="set-up-transaction-codes"></a>Iestatīt darbību kodus

1. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Transakciju kodi**.
2. Režģī atlasiet **11**. Pēc tam Darbību rūtī atlasiet **Dzēst**.
3. Darbību rūtī atlasiet **Jauns**.
4. Kopsavilkuma cilnes **Darbības kodi** laukā Darbības **kods** **ievadiet** **11.**
5. Laukā **Nosaukums** ievadiet Outright **purchase/sale**.
6. Sadaļā Pārsūtīšanas **pasūtījums**, laukā **Rēķina summa** atlasiet **Kopējās izmaksas**.
7. Laukā **Statistiskā** summa atlasiet **Kopējās izmaksas**.
8. Darbību rūtī atlasiet **Saglabāt**.
9. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
10. Cilnes Intrastat kopsavilkuma cilnē Vispārīgi **laukā** Pārsūtīšanas pasūtījums **atlasiet** **11**.**·**

#### <a name="set-up-charges-for-an-item"></a>Krājuma izmaksu iestatīšana

1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
2. Režģī atlasiet **D0001**.
3. Kopsavilkuma cilnes **Ārējā** tirdzniecība sadaļā **Intrastat** laukā Maksas procenti **ievadiet** **20**.

#### <a name="change-the-site-address"></a>Vietnes adreses maiņa

1. Atveriet **Noliktavas pārvaldība** > **Iestatīšana** > **Noliktava** > **Vietnes**.
2. Režģī atlasiet **1**.
3. Kopsavilkuma cilnē **Adreses** atlasiet **Rediģēt**.
4. Dialoglodziņā **Rediģēt adresi** laukā **Valsts/reģions** atlasiet **DEU**.
5. Atlasiet **Labi**.
6. Režģī atlasiet **2**.
7. Kopsavilkuma cilnē **Adreses** atlasiet **Rediģēt**.
8. Dialoglodziņā **Rediģēt adresi** laukā **Valsts/reģions** atlasiet **ITA**.
9. Atlasiet **Labi**.
10. Dodieties uz **Noliktavas pārvaldība** > **Iestatīšana** > **Noliktava** > **Noliktavas**.
11. Režģī atlasiet **21**.
12. Kopsavilkuma cilnes **Vispārējā** daļa atsauces **sadaļā**, laukā **Kreditora konts** atlasiet **DE-001**.

#### <a name="create-a-transfer-order"></a>Izveidot pārsūtīšanas pasūtījumu

1. Dodieties uz **Krājumu pārvaldības Izejošie** > **pasūtījumi Pārsūtīšanas** > **pasūtījums**.
2. Darbību rūtī atlasiet **Jauns**.
3. Cilnes Rindas **kopsavilkuma** cilnes Pārsūtīšanas **pasūtījuma virsraksts** sadaļas **Pārskats** **laukā No** noliktavas atlasiet **11**. **Noliktavas laukā Uz** atlasiet **21**.
4. Kopsavilkuma cilnes **Rindas** cilnē Pārsūtīšanas **pasūtījuma rindas** atlasiet **Pievienot**.
5. Laukā **Krājuma numurs** atlasiet **D0001**. Pēc tam laukā **Pārsūtīt daudzumu** ievadiet **2**.
6. Kopsavilkuma cilnes **Ārējā tirdzniecība kopsavilkuma** **cilnē Ārējā tirdzniecība pārbaudiet,** **·** **vai darbības koda lauks ir iestatīts automātiski.**
7. Darbību rūts cilnē Nosūtīšana **, kas atrodas operāciju grupā** **, atlasiet Pārsūtīšanas** pārsūtīšanas pasūtījumu **.**
8. **Dialoglodziņa Krava** cilnē **Pārskats**, laukā **Atjaunināt** atlasiet **Visi**.
9. Atlasiet **Labi,** lai sūtītu pasūtījumu.
10. Darbību rūts cilnē **Saņemt** operāciju grupā **atlasiet** **Saņemt**.
11. **Dialoglodziņa Saņemt** cilnes Pārskats **laukā** Atjaunināt **atlasiet** **Visi**.
12. Atlasiet **Labi,** lai sūtītu pasūtījumu.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>Pārsūtīt pārsūtīšanas pasūtījumu uz Intrastat žurnālu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Pārsūtīt**.
3. **Dialoglodziņā Intrastat (Pārsūtīšana)** iestatiet opciju Pārsūtīšanas pasūtījums **uz** Jā **un** visas pārējās opcijas uz **Nē**.
4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu.

   ![Rinda, kas attēlo pārsūtīšanas pasūtījumu Intrastat lapā](media/intrastat_overview_3.png)

5.  Pārskatiet **pārsūtīšanas** pasūtījuma cilni Vispārīgi.

    Ievērojiet, ka automātiski ir iestatīti **lauki sadaļās** Rēķina **vērtība un** Statistiskā vērtība. Rēķina summas un **statistiskās** summas **lauku** vērtības ir balstītas uz darbību kodu **lapas** iestatījumiem. **Vērtība 20** laukā Papildmaksas **procentos** ir vērtība, kas ir iestatīta lapā **Izlaistās** preces. Vērtība laukā **Statistikas** maksu summa ir maksu kvantitātes izteiksme (jo 107,24 ir vienāda ar 20 536,18). Lauka Statistiskā **vērtība** vērtība ir vērtību summa no laukiem Statistiskā **summa** un **Statistiskās maksas** summa.

  ![Pārsūtīšanas pasūtījuma detaļas Intrastat lapas cilnē Vispārīgi](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Papildu vienības

Šajā piemērā uzņēmumam Vācijā jāiegādājas 10 preču vienības no Itālijas uzņēmuma. Papildus preču kodiem šīm precēm ir jānorāda papildu vienības. Piemērs parāda, kā veidot jaunas mērvienības, piešķirt papildu vienības Intrastat preču kodam, grāmatot darbības ar papildu vienībām un pārskatīt Intrastat žurnālu, kur iestatīts papildu vienību lauks.

#### <a name="preliminary-setup"></a>Iepriekšēja iestatīšana

1. Dodieties **uz organizācijas** > **administrēšanas** > **organizācijas juridiskajām** personām un atlasiet **NOROBEŽOTAS.**
2. Kopsavilkuma cilnē **Adreses** pārbaudiet, vai valsts/reģiona **lauks ir** iestatīts uz **DEU(Vācija).**
3. Dodieties uz **Nodokļi** > **Iestatījumi** > **Ārējā tirdzniecība** > **Ārējās tirdzniecības parametri**.
4. Kopsavilkuma cilnes **Vispārīgi** cilnes **Intrastat** laukā **Darījuma** **kods** atlasiet **11**.
5. Kopsavilkuma cilnē **Preču kodu hierarhija** pārbaudiet, vai kategoriju **hierarhijas lauks** ir iestatīts uz **Intrastat**.
6. Dodieties uz **Kreditoru parādiem** > **visiem kreditoriem** > **·**.
7. Režģī atlasiet **DE-001**.
8. Kopsavilkuma cilnē **Adrese** atlasiet **Rediģēt**.
9. Dialoglodziņā **Rediģēt adresi** laukā **Valsts/reģions** atlasiet **ITA**.
10. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

#### <a name="create-a-unit-of-measure"></a>Mērvienības izveide

1. Dodieties uz **organizācijas administrēšanas** > **iestatījumu** > **vienību** > **vienībām**.
2. Darbību rūtī atlasiet **Jauns**.
3. **Laukā** Vienība ievadiet mērvienības nosaukumu. Šajā piemērā ievadiet **GRM**.
4. Kopsavilkuma cilnes **Klasifikācija** laukā **Mērvienība** atlasiet **rekvizītu**, ko mērvienība mērvienība ir atlasa. Šajā piemērā izvēlieties **Masa**.
5. **Laukā Mērvienību** sistēma atlasiet mērvienību sistēmu, kurai pieder vienība. Piemēram, atlasiet metriskās **mērvienības**.

#### <a name="set-up-unit-conversions"></a>Iestatīt vienību pārveidošanu

1. Dodieties uz **organizācijas administrēšanas** > **iestatījumu** > **vienību** > **vienību pārveidošanu**.
2. **Cilnē Starpklases pārveidošanas** atlasiet **Jauns**.
3. Dialoglodziņa Vienības **pārvēršana laukā Prece** **atlasiet** F00007 **.**
4. Laukā **No vienības** atlasiet **s**.
5. Laukā **Uz vienību** atlasiet **GRM**.
6. Pārbaudiet, vai konvertēšanas kurss ir **1 = 1**.
7. Atlasiet **Labi**.
8. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
9. Režģī atlasiet **F00007**.
10. Kopsavilkuma cilnes **Pārvaldīt** krājumus sadaļas **Krājumi** laukā **Vienība** atlasiet **GRM**.
11. Darbību rūtī atlasiet **Saglabāt**.

#### <a name="set-up-product-information"></a>Preces informācijas iestatīšana

1. Pārejiet uz **Preču informācijas pārvaldība** > **Preces** > **Izlaistās preces**.
2. Režģī atlasiet **F00007**.
3. Kopsavilkuma cilnes **Ārējā tirdzniecība** sadaļas **Intrastat** laukā **Izcelsmes valsts** izvēlieties **920 20 34**.
4. Darbību rūtī atlasiet **Saglabāt**.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>Piešķirt papildu vienību Intrastat preces kodam

1. Atveriet **Preču informācijas pārvaldība** > **Iestatīšana** > **Kategorijas un atribūti** > **Kategoriju hierarhijas**.
2. Sarakstā izvēlieties **Intrastat**.
3. Režģī atlasiet **Statīvs**.
4. Kopsavilkuma cilnes **Ārējā** tirdzniecība laukā **Papildu** vienības atlasiet **GRM**.
5. Darbību rūtī atlasiet **Saglabāt**.

   Papildinformāciju skatiet sadaļā [Mērvienību pārvaldība](../../supply-chain/pim/tasks/manage-unit-measure.md).

#### <a name="create-a-purchase-order"></a>Pirkuma pasūtījuma izveide

1. Atveriet **Kreditori** > **Pirkšanas pasūtījumi** > **Visi pirkšanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**.
3. Dialoglodziņa **Pirkšanas pasūtījuma izveide** laukā **Kreditora konts** atlasiet **DE-001**.
4. Atlasiet **Labi**.
5. Cilnē **Virsraksts** kopsavilkuma cilnē **Ārējā** **tirdzniecība** laukam **Transakcijas kods** jābūt **11**.
6. Cilnē **Rindas** kopsavilkuma cilnes **Pirkšanas pasūtījuma rindas** laukā **Preces numurs** atlasiet **F00007**. Laukā **Daudzums** ievadiet **10**.
7. Kopsavilkuma cilnes **Ārējā tirdzniecība kopsavilkuma** **cilnē Ārējā tirdzniecība pārbaudiet,** **·** **·** **vai darbības kods un preces lauki ir iestatīti automātiski.**
8. Darbību rūts cilnē **Pirkšana**, grupā **Darbības** atlasiet **Apstiprināt**.
9. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
10. Darbību rūtī atlasiet **Noklusējuma vērtība No**. Laukā **Noklusējuma daudzums rindām** atlasiet **Pasūtītais daudzums**. Pēc tam atlasiet **Labi**.
11. Kopsavilkuma cilnes **Kreditora rēķina virsraksts** kopsavilkuma **cilnē Rēķina identifikācija**, **laukā** Numurs ievadiet **VE-0010**.
12. Sadaļā Rēķina **datumi** laukā Rēķina **datums** **atlasiet 10/5/2021 (2021**. gada 5. oktobris).
13. Darbību rūtī atlasiet **Grāmatot**, lai grāmatotu žurnālu.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Pārsūtīt kreditora rēķinu uz Intrastat žurnālu

1. Dodieties uz **Nodokļi** > **Deklarācijas** > **Ārējā tirdzniecība** > **Intrastat**.
2. Darbību rūtī atlasiet **Pārsūtīt**.
3. Dialoglodziņā **Intrastat (pārsūtīšana)** iestatiet opciju **Kreditora rēķins** uz **Jā**.
4. Atlasiet **Labi**, lai pārsūtītu transakcijas un pēc tam pārskatītu Intrastat žurnālu.

   ![Rinda, kas attēlo pirkšanas pasūtījumu Intrastat lapā](media/intrastat_overview_5.png)

5. Pārskatiet pirkšanas pasūtījuma cilni **Vispārīgi**. Ievērojiet **, ka automātiski ir iestatīti** **papildu vienību daudzums** un papildu **vienību** lauki sadaļā Vienība.

   ![Pirkšanas pasūtījuma detaļas Intrastat lapas cilnē Vispārīgi](media/intrastat_overview_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
