---
title: "Jaunumi un izmaiņas versijā Dynamics 365 for Operations version 1611 (2016. gada novembris)"
description: "Šajā tēmā ir aprakstītas funkcijas, kas Dynamics 365 for Operations programmas versijā 1611 ir jaunas vai ir mainītas."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 09addfd9e4a5c601970b5c8c24a3d39b041e07e6
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Jaunumi un izmaiņas versijā Dynamics 365 for Operations version 1611 (2016. gada novembris)

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstītas funkcijas, kas Dynamics 365 for Operations programmas versijā 1611 ir jaunas vai ir mainītas.

<a name="cost-accounting"></a>Izmaksu uzskaite
---------------

<table>




<thead>
<tr class="header">
<th>Ko iespējams izdarīt</th>
<th>Kāpēc tas ir svarīgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Definēt izmaksu elementu dimensijas, un importēt izmaksu elementu dimensijas dalībniekus.</td>
<td>Izmaksu elementi tiek izmantoti Izmaksu uzskaitē, izmaksu kategorizēšanai un dokumentētu izmaksu plūsmu. Primāro izmaksu elementi tiek importēti, izmantojot Microsoft Dynamics 365 for Operations datu savienotāju, lai iegūtu galvenos kontus tieši no Operations vai, izmantojot vispārēju datu savienotāju, kur var iegūt galveno kontu, izmantojot Microsoft Excel no cita veida avota sistēmas. Pēc tam, kad galvenie konti ir importēti Izmaksu uzskaitē, tie tiek izmantoti kā izmaksu elementa dimensijas dalībnieki. Sekundāro izmaksu elementi ir lietotāja definēti, un tiek izmantoti sadalījumos, lai dokumentētu izmaksu plūsmu.</td>
</tr>
<tr class="even">
<td>Kartēt izmaksu elementu dimensijas.</td>
<td>Ja galvenie konti jūsu juridiskajās personās nevar būt koplietoti likumā noteikto grāmatvedības prasību dēļ, jūs varat tos kartēt pēc to importēšanas Izmaksu uzskaitē, lai iegūtu vienotu skatījumu visā organizācijā.</td>
</tr>
<tr class="odd">
<td>Definēt izmaksu objektu dimensijas, un importēt izmaksu objektu dimensijas dalībniekus.</td>
<td>Izmaksu objekti ir jebkura veida objekti, kuriem tiek piešķirtas izmaksas. Tipiski izmaksu objekti ietver preces, projektus, resursus, nodaļas, izmaksu centrus un ģeogrāfiskus reģionus. Jūs varat izmantot Microsoft Dynamics 365 for Operations datu savienotāju, lai saņemtu finanšu dimensijas un vērtības no Operations, vai izmantot vispārēju datu savienotāju, kur var iegūt dimensijas un vērtības, izmantojot Microsoft Excel no cita veida avota sistēmas. Piemēram, ja izmantojat Izmaksu centra finanšu dimensiju kā objekta dimensija, visi izmaksu centri, kas tiek importēti ir dimensijas dalībnieki izmaksu objektam.</td>
</tr>
<tr class="even">
<td>Definējiet vai importējiet statistikas dimensijas.</td>
<td>Statistikas dimensijas dalībnieki tiek mērīti beznaudas vienībās, piemēram, mašīnstundas, darbinieku skaits un laukums. Tās tiek izmantotas izrakstos vai kā pamats sadalījumos un sadalēs.</td>
</tr>
<tr class="odd">
<td>Izveidot statistisko mērījumu nodrošinātāja veidnes.</td>
<td>Statistisko mērījumu nodrošinātāja veidne tiek lietota, lai pārveidotu Dynamics 365 for Operations datus statistiskos mēros. Veidne tad tiek saistīta ar doto statistikas dimensijas dalībnieku. Veidnes ir iepriekš filtrētas tā, lai tās parāda tikai tabulas, kas ir saistītas ar finanšu dimensijām.</td>
</tr>
<tr class="even">
<td>Izveidot izmaksu uzskaites virsgrāmatas.</td>
<td>Izmaksu uzskaites virsgrāmata ir neatkarīga virsgrāmata, kas izmanto savu kalendāru un valūtu. Tai ir liela nozīme visu izmaksu darbību apstrādē. Piemēram, izmaksu uzskaites virsgrāmata klasificē izmaksas, pamatojoties uz saviem izmaksu elementiem, un uzkrāj izmaksas, pamatojoties savām objekta dimensijām. Jūs varat izveidot tik daudz izmaksu uzskaites virsgrāmatu, cik jums ir nepieciešams, lai veiktu pārvaldības pārskatu no dažādām perspektīvām.</td>
</tr>
<tr class="odd">
<td>Izveidot žurnāla izmaksu kontroles vienības.</td>
<td>Izmaksu kontroles vienības veido izmaksu struktūru un definē izmaksu plūsmu izmaksu uzskaites virsgrāmatā. Tām ir jābūt saistītām ar izmaksu objekta dimensijām, lai pārstāvētu izmaksu objektu dimensijas virsgrāmatā.</td>
</tr>
<tr class="even">
<td>Apstrādāt virsgrāmatas ierakstus.</td>
<td>Lai izmērītu faktisko veiktspēju, ir nepieciešami dati. Dati tiek importēti, izmantojot savienotājus, ko jūs definējat izmaksu uzskaites virsgrāmatā. Apstrādājot virsgrāmatas ierakstus, pakāpeniski tiek importēti dati.</td>
</tr>
<tr class="odd">
<td>Apstrādāt budžeta ierakstus.</td>
<td>Lai izmērītu budžeta veiktspēju, ir nepieciešami dati. Dati tiek importēti, izmantojot savienotājus, ko jūs definējat izmaksu uzskaites virsgrāmatā. Apstrādājot budžeta ierakstus, pakāpeniski tiek importēti dati.</td>
</tr>
<tr class="even">
<td>Izveidot un lietot izmaksu izturēšanās politiku.</td>
<td>Izmaksu izturēšanās politika tiek izmantota, lai klasificētu izmaksas kā fiksētas, mainīgas vai daļēji mainīgas. Politika ir atbilstoša nosacījumiem un ar spēkā stāšanos datumu. Pēc noklusējuma visas izmaksas tiek atzīmētas kā neklasificētas līdz jūs pielietojat izmaksu izturēšanās politiku, un aprēķināt noteikuma ietekmi. Pēc aprēķina, izmaksas tiek klasificētas.</td>
</tr>
<tr class="odd">
<td>Izsekot izmaksas.</td>
<td>Lai palīdzētu jums izprast izmaksu politiku ietekmi, Izmaksu uzskaite ļauj jums izsekot izmaksas līdz avota vērtībām, un to izcelsmes piemērotajiem noteikumiem. Šī funkcionalitāte nodrošina pilnu izsekojamību par to, kad notika izmaksas, kādi izmaksu tipi notika, kas radās, kādi izmaksu izturēšanās noteikumi tika pielietoti.</td>
</tr>
<tr class="even">
<td>Definēt dimensiju hierarhijas.</td>
<td>Jūs varat izveidot dimensiju hierarhijas kategorizēšanas vai klasifikācijas nolūkiem. Piemēram, jūs varat definēt kategorizēšanas hierarhiju, kuras pamatā ir izmaksu elementa dimensija un tās locekļi. Alternatīvi jūs varat definēt klasifikācijas hierarhiju, kuras pamatā ir izmaksu objekta dimensija un tās locekļi. Pārskata struktūras tiek izmantotas šādos gadījumos:
<ul>
<li>Jūs definējat sadalījumus, izmaksu likmes un izmaksu apkopojuma noteikumus.</li>
<li>Jūs skatāt izrakstus, izmantojot darbvietu.</li>
<li>Jūs definējat piekļuvi, lai skatītu apkopotos datus.</li>
<li>Jūs skatāt datus programmā Excel.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Izveidot izrakstus, kurus var skatīt darbvietā.</td>
<td>Izmantojiet šo darbvietu, lai iegūtu ātru pārskatu par faktiskajām un budžeta izmaksām, kā arī novirzēm. Jūs varat filtrēt datus pēc perioda vai izmaksu līmeņa. Darbvieta ir paredzēts vadītājiem, kas ir atbildīgi par izmaksu kontroli. Tā ievēro piekļuves noteikumus, kas ir definēti dimensiju hierarhijām.</td>
</tr>
<tr class="even">
<td>Izveidojiet pārskatus, izmantojot programmu Excel. <strong>Piezīme:</strong> ir jāpalaiž programma Microsoft Excel 2016.</td>
<td>Jūs varat eksportēt Izmaksu uzskaites datus pa tiešo uz Excel, izmantojot datu struktūras, un izmantojiet Microsoft PivotTable pārskatu veidošanai.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Izmaksu pārvaldība
| Ko iespējams izdarīt                                                            | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Atkārtoti piešķirt atlaistā darbinieka kredītkaršu darījumus.                     | Dažreiz, kad darbinieks tiek atlaists, viņa vai viņas Active Directory domēna pakalpojumu (AD DS) konts tiek atspējots, importējot aktīvās kredītkartes darbības, kuras nepieciešams iekļaut izdevumos. Iepriekš, jūs nevarējāt piešķirt pārstāvi izdevumu ierakstam vai pievienot kredītkartes darbības izdevumu pārskatam. Tagad jūs varat izmantot lapu **Kredītkaršu darbības**, lai atkārtoti piešķirtu darbinieku jebkurai kredītkartes darbībai, kurā saistītais darbinieks tika atlaists. Pēc tam, kad jūs atkārtoti piešķirat kredītkartes darbības, darbību var atlasīt izdevumu pārskatam, un apmaksāt ar regulāru procesu izdevumu pārskata kompensācijai. |
| Mainīt izdevumu kredītkartes informāciju turpmākajiem un bijušajiem darbiniekiem. | Jūs varat mainīt Izdevumu pārvaldības kredītkartes informāciju turpmākajiem un bijušajiem darbiniekiem. Iepriekš, jūs varējāt mainīt izdevumu kredītkartes informāciju tikai tad, ja darbinieks ir aktīvs darbinieks.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kopēt izdevumu pārskatu.                                                    | Tagad jūs varat kopēt esošos izdevumus, veidojot jaunus izdevumus vienā izdevumu pārskatā. Jūs varat kopēt izdevumu pārskatu un visus saistītos ne-kredītkartes izdevumus jaunā izdevumu pārskatā. Jums joprojām jāveic visu nepieciešamo uzskaitīšanu, un jāpievieno nepieciešamās ieejas plūsmas, pamatojoties uz definēto izdevumu politikām un kategorijām. Jūs varat pievienot kredītkaršu darbības izdevumu pārskatam, atlasot pievienošanai nesaskaņotos izdevumus.                                                                                                                                                                                                                        |
| Rediģēt izdevumus lielā apjomā.                                                        | Dažas kredītkartes darbības nevar kartēt uz izdevumu kategoriju, vai tās varētu būt nepareizi kartētas, importēšanas laikā. Šajā gadījumā darbiniekiem ir manuāli jānomaina saistīto izdevumu kategoriju. Pārvaldot nesaskaņotos izdevumus, jūs varat veikt izdevumu kategoriju lielapjoma-rediģēšanu atlasītajiem izdevumiem. Turklāt, pārvaldot atlasītos izdevumus specifiskam izdevumu pārskatam, jūs varat veikt projekta un papildinformācijas lielapjoma-rediģēšanu.                                                                                                                                                                                    |
| Mainīt maiņas kursu kredītkartes darbībām.                     | Faktiskais maiņas kurss, ko tiek izmantots kredītkartes darbības var atšķirties no valūtas kursa, kas ir iestatīts sistēmā. Iepriekš darbinieki nevarēja mainīt valūtas maiņas kursu kredītkartes darījumiem, kas tika importēti Izmaksu pārvaldībā. Tagad jūs varat iestatīt parametru lapā **izdevumu pārvaldības parametri**, lai atļaut mainīt maiņas kursu kredītkaršu darījumiem.                                                                                                                                                                                                                                            |
| Iestatiet korupcijas novēršanas apliecinājumu izdevumiem.                            | Dažiem darbiniekiem organizācijā var būt darījumi ar valdības amatpersonām, un daži izdevumi, kas rodas kā daļu no šiem darījumiem varētu tikt uztverta kā uzpirkšana. Izdevumu pārvaldībā jūs varat iestatīt korupcijas novēršanas apliecinājumu, ka tiek parādīts atlasītajām izdevumu kategorijām, piemēram, maltītes un dāvanas. Darbiniekiem ir jāatlasa vai izdevumi, kas tiek iestatīti korupcijas novēršanas apliecinājumam atbilst kritērijiem, kas ir definēti jūsu organizācijas ierobežojumos.                                                                                                                                                                                     |
| Novērst manuālu izdevumu ievadīšanu specifiskām izdevumu kategorijām.          | Izdevumu kategoriju var iestatīt, lai atspoguļotu kredītkartes darbību, kuras kategoriju nevar mainīt. Piemēram, maksa par kredītkartes novēlotu maksājumu. Tagad jūs varat iestatīt izmaksu kategorija, kas ļauj izdevumus veidot tikai izmantojot importēšanu. Šis līdzeklis neļauj darbiniekiem manuāli izveidot izdevumu kategorijai. Tas neļauj arī mainīt kategoriju darbībām, kas tika importētas, un kas izmanto šo kategoriju.                                                                                                                                                                                   |
| Pievienojiet ieejas plūsmu vairākiem izdevumiem.                                     | Ieejas plūsma, kas tiek augšupielādēta Izdevumu pārvaldībā var būt saistīta ar vairākiem izdevumiem. Iepriekš, ieejas plūsmu, kas bija saistīta ar vairākiem izdevumiem, bija nepieciešams augšupielādēt vienu reizi katram izdevumu. Tagad jūs varat pievienot ieejas plūsmu izdevumam, kas jau ir augšupielādēts un pievienots citam izdevumam vienā izdevumu pārskatā. Turklāt, ja jūs augšupielādējat ieejas plūsmu izdevumu pārskata virsrakstā, jūs varat atlasīt vienu vai vairākas rindas, kurām pievienot ieejas plūsmu.                                                                                                                                                                                        |
| Izveidojiet izdevumus ar nākotnes datumiem.                                              | Kopējot izdevumu pārskatu, piemēram, izdevumu darbībai varētu būt nākotnes datums. Iepriekšējos laidienos netiek atļauti izdevumi ar nākotnes datumiem. Tagad jūs varat izveidot un saglabāt izdevumus ar nākotnes datumu. Taču jūs nevarat iesniegt izdevumu ar nākotnes datumu.                                                                                                                                                                                                                                                                                                                                                                                 |
| Konfigurēt izdevumu nodokļus pavalstij/provincei.                              | Dažās valstīs/reģionos izdevumiem, kas rodas dažādās pavalstīs/provincēs var būt dažādas PVN likmes. Izdevumu nodokļu konfigurācijas jūs varat iestatīt arī pavalsts/provinces līmenī, ne tikai valsts/reģiona līmenī. Ja atstājat lauku **Pavalsts/Province** tukšu lapā **Nodokļu konfigurācija**, PVN grupa attiecas uz visām pavalstīm/provincēm norādītajā valstī/reģionā.                                                                                                                                                                                                                                       |
| Iestatīt izmaksu kredītkaršu veidus.                                          | Iepriekš, nebija lapas, kur varētu izveidot jaunu kredītkaršu veidus, piemēram, Visa, MasterCard vai AMEX, ko varētu izmantot Izmaksu pārvaldībā. Tagad jūs varat veidot kredītkaršu veidus izmantošanai Izmaksu pārvaldībā. Lapas atrodas apgabalā **Iestatījumi**, sadaļā **Aprēķini un kodi**.                                                                                                                                                                                                                                                                                                                                                 |
| Definējiet vairāklīmeņu apstiprinājuma darbplūsmu izdevumu pārskatiem.                 | Jauna darbplūsma izdevumu pārskatiem atbalsta daudzlīmeņu apstiprināšanas procesu. Darbinieki ievada pagaidu apstiprinātājus un galīgos apstiprinātājus, veidojot izdevumu pārskatu. Darbplūsma pēc tam maršrutē izdevumu pārskatu uz pagaidu apstiprinātājiem. Pēc izdevumu pārskata apstiprināšanas tajā līmenī, darbplūsma maršrutē to uz gala apstiprinātājiem galējai apstiprināšanai.                                                                                                                                                                                                                                                                                          |
| Izveidot un uzturēt izdevumus, kas nav pievienoti izdevumu pārskatam.    | Lietotājs tagad var izveidot izdevumus un uzturēt tos (piemēram, pēc ieejas plūsmu pievienošanas vai uzskaitīšanas, vai viesu piešķiršanas) bez nepieciešamības vispirms izveidot izdevumu pārskatu. Vienu vai vairākus izdevumus var atlasīt un pievienot jaunam izdevumu pārskatam, lai tos varētu iesniegt apstiprināšanai. Sadaļā **Izmaksu pārvaldība** &gt; **Mani izdevumi** &gt; **Izdevumi** ir pieejama jauna izmaksu pārvaldības lapa.                                                                                                                                                                                                                                                       |

## <a name="financial-management"></a>Finanšu pārvaldība
<table>




<thead>
<tr class="header">
<th>Ko iespējams izdarīt</th>
<th>Kāpēc tas ir svarīgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izsekot pamatlīdzekļu novērtējumus, izmantojot vienas "grāmatošanas" jēdzienu.</td>
<td>Iepriekš, tika izmantoti divi atsevišķi novērtēšanas veidi, lai izsekotu pamatlīdzekļu vērtības: vērtību modeļi vai nolietojuma grāmatas. Pašreizējā versijā šie divi jēdzieni ir sapludināti vienā novērtēšanas jēdzienā, kas ir nosaukts grāmatas. Grāmatām ir visa vērtību modeļu un nolietojuma grāmatu funkcionalitāte. Piemēram, jūs varat izslēgt grāmatošanu virsgrāmatā. Grāmatas, kas tiek grāmatotas virsgrāmatā parasti tiek izmantotas uzņēmuma finanšu pārskatu veidošanai. Grāmatas, kas netiek grāmatotas virsgrāmatā, var būt izmantotas nodokļu pārskatu veidošanai.</td>
</tr>
<tr class="even">
<td>Veikt Virsgrāmatas gada beigu slēgšana vairākām juridiskajām personām.</td>
<td>Lai paātrinātu gada beigu slēgšanas procesu, jūs varat palaist gada beigu slēgšanu vairākām juridiskajām personām no koplietotās gada beigu slēgšanas lapas. Juridisko personu grupas var definēt ar iestatījumiem, kas ir jāsaglabā no viena gada uz nākamo. Ir veikti arī citi izmantojamības uzlabojumi gada beigu slēgšanas procesā.</td>
</tr>
<tr class="odd">
<td>Izmantojiet Virsgrāmatas ārvalstu valūtas pārvērtēšanas uzlabojumus.</td>
<td>Ārvalstu valūtas pārvērtēšanas Virsgrāmatas procesam ir veikti šādi uzlabojumi:
<ul>
<li>Maiņas kursa tips ir pievienots galvenajam kontam. Šis maiņas kursa tips tagad tiek izmantots, lai noteiktu maiņas kursu valūtas pārvērtēšanas laikā. Ja netiek definēts maiņas kursa tips, process turpinās izmantot maiņas kursa tipu, kas ir definēts virsgrāmatā.</li>
<li>Tagad ir vieglāk atlasīt galveno kontu un valūtu diapazonu, kuram palaist pārvērtēšanas procesu.</li>
<li>Pārvērtēšanu var palaist vairākām juridiskajām personām.</li>
<li>Sistēma tagad uztur katra pārvērtēšanas procesa vēsturi, kas tika veikts, kā arī Debitoru parādu (AR) un Kreditoru parādu (AP) pārvērtēšanas procesiem.</li>
<li>Izpildot procesu, tagad var priekšskatīt pārvērtēšanas rezultātus. Priekšskatījums parāda rezultātus visām juridiskajām personām, kurām process tika izpildīts. Pēc tam jūs varat grāmatot visas juridiskās personas vai to apakškopu no priekšskatījuma. Priekšskatījuma rezultātus var arī eksportēt uz Excel.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skatīt darbības papildu grāmatošanas līmeņiem.</td>
<td>Saraksta lapā <strong>Apgrozījuma bilance</strong> un pārskatā <strong>Dimensiju izraksts</strong>, jūs varat atlasīt papildu grāmatošanas līmeņus, kas tika pievienoti Virsgrāmatai. Atlasot papildu grāmatošanas līmeņus, korekcijas šiem grāmatošanas līmeņiem tiek iekļautas bilances saraksta lapā vai pārskatā.</td>
</tr>
<tr class="odd">
<td>Pievienot norādījumu dokumentācija finanšu perioda slēgšanas veidnei.</td>
<td>Iepriekš jūs varētu pievienot dokumentāciju pēc uzdevuma pabeigšanas. Piemēram, nebija iespējams pievienot pārskatu, kas tika ģenerēts. Tagad jūs varat arī pievienot norādījumu dokumenta veidni. Šis norādījumu dokuments pēc tam tiek kopēts uz katru uzdevumu finanšu perioda grafikā, lai uzdevuma īpašnieks varētu skatīt instrukcijas par to, kā pabeigt uzdevumu.</td>
</tr>
<tr class="even">
<td>Definēt starpuzņēmumu uzskaites iestatīšanu no koplietojamas lapas.</td>
<td><strong>Starpuzņēmumu uzskaites iestatījumu lapa</strong> tagad ir koplietojama, lai uzņēmums var definēt visus juridisko personu pārus, kas var slēgt darījumus viena ar otru. Turklāt, tagad jūs varat ievadīt darbību izcelsmes juridiskajā personā, nevis no mērķa juridiskās personas. Ja kāda no juridiskajām personām var uzsākt starpuzņēmumu darbību, nepieciešams definēt savstarpējo pāri. Tādēļ mērķa juridiskā persona arī ir iestatīta kā izcelsmes juridiska persona.</td>
</tr>
<tr class="odd">
<td>Iesniegt attaisnojuma dokumentus budžeta plāniem.</td>
<td>Jūs varat izveidot attaisnojuma veidni kā papildu dokumentāciju jebkurai pieprasītai budžeta summai. Lietotāji var aizpildīt veidnes datus un pievienot veidni budžeta plānam, lai to varētu izmantot apstiprināšanas procesa laikā.</td>
</tr>
<tr class="even">
<td>Iespējot papildu kārtulas budžeta reģistra ierakstiem.</td>
<td>Ja papildu noteikumi tiek konfigurēti Virsgrāmatā, šos noteikumus var izmantot jauniem ierakstiem un pārsūtījumiem budžeta reģistrā.</td>
</tr>
<tr class="odd">
<td>Gūt labumu no priekšapmaksas rēķina izrakstīšanas aktivitātes uzlabotas redzamības.</td>
<td>Jauna saraksta lapa <strong>Atvērtas priekšapmaksas</strong> sniedz pārskatu par priekšapmaksas rēķinu izrakstīšanas aktivitātes statusu. Lapa sniedz AP nodaļai informāciju par pirkuma pasūtījumiem, kuriem ir priekšapmaksas atlikuma vērtības, kas jāgrāmato, rēķinā iekļautas vērtības, kas jāapmaksā, un apmaksātas rēķinu vērtības, kas ir jāpielieto standarta rēķiniem. Turklāt uzlabojumi apmaksātu priekšapmaksas rēķinu automātiskā piemērošanā standarta rēķiniem, palīdz rēķinu izrakstīšanas darbiniekiem veikt datu ievadi efektīvāk.</td>
</tr>
<tr class="even">
<td>Izmantot <strong>Kreditora sadarbības rēķinu izveides</strong> darbvietu.</td>
<td>Jauna <strong>Rēķinu izveides</strong> darbvieta apgabalā <strong>Kreditora sadarbība</strong> ļauj ārējiem kreditoriem droši piekļūt savai rēķina informācijai. Piemēram, kreditori var redzēt, vai rēķins ir apmaksāts un iesniegt savu rēķinu. Šīs izmaiņas veicina efektīvāku un laicīgāku saziņu ar ārējiem kreditoriem. Tādējādi rēķinu izrakstīšanas darbiniekiem ir mazāk traucējumu.</td>
</tr>
<tr class="odd">
<td>Pārslēgt juridiskās personas rēķina izveides laikā.</td>
<td>Uzlabojumi ļauj rēķinu izrakstīšanas darbiniekiem, kam ir jāievada rēķinus vairākām juridiskajām personām, ātri mainīt juridisko personu no rēķinu izrakstīšanas lapām. Šis līdzeklis ietaupa laiku rēķinu izrakstīšanas darbiniekiem, jo tiem vairs nav nepieciešams izrakstīties no pašreizējās juridiskās personas un pierakstīties citā juridiskajā personā. Gan lapa <strong>Globāls rēķinu žurnāls</strong>, gan lapa <strong>Kreditora rēķini</strong> ļauj lietotājiem mainīt juridiskās personas datu ievades laikā.</td>
</tr>
<tr class="even">
<td>Elektronisko failu Iekšējā ieņēmumu dienesta (IRS) 1099 kombinētās federālās/pavalsts sistematizēšanas programmas atbalsts</td>
<td>Ja <strong>US</strong> konfigurācijas atslēga ir iespējota, 1099 elektroniskās iesniegšanas process nodrošina papildu funkcionalitāti, kas atbilst IRS noteikumiem par kombinēto federālās/pavalsts dokumentu sistematizācijas programmu. IRS izveidoja šo programmu, lai tā varētu elektroniski pārsūtīt informācijas atgriešanas uz iesaistītajām pavalstīm.</td>
</tr>
<tr class="odd">
<td>Segšanas uzlabojumi</td>
<td>Uzlabojumi palīdz maksājuma darbiniekiem veikt nosegšanu efektīvāk, jo darbinieki var atļaut vairāku negrāmatotu maksājumi nosegšanu pašā rēķinā.</td>
</tr>
<tr class="even">
<td>Starpuzņēmumu skats</td>
<td>Centralizēto maksājumu darbinieki tagad var skatīt kavējuma rēķinus dažādos uzņēmumos. Darbvietas <strong>Kreditoru maksājumi</strong> un <strong>Debitoru maksājumi</strong> tagad nodrošina labāku piekļuvi un kontroli pār nokavētiem rēķiniem, nodrošinot veidu, kā skatīt un filtrēt uzņēmumos, kas ir daļa no centralizēto maksājumu organizācijas hierarhijas.</td>
</tr>
<tr class="odd">
<td>Izmantojiet darbvietu <strong>Bankas pārvaldība</strong>.</td>
<td>Jaunā darbvieta <strong>Bankas pārvaldība</strong> palīdz izsekot jūsu juridisko personu bankas kontus un bilances. Pašreizējā un nenoslēgtā bilances ir uzreiz pieejamas visiem kontiem, un jūs varat lejupizpētīt no bilancēm detalizētos darbību dokumentos. Jūs varat arī skatīt vēsturiskus bilances datus katram bankas kontam vai kopsavilkumu par visiem bankas kontiem uzņēmumā īstermiņa un ilgtermiņa skatos. Jūs varat iegūt lielāku izpratni par bankas kontu saskaņošanu, jo pēdējās saskaņošanas datums tiek paziņots katram bankas kontam, kā arī ir indikators saskaņošanām, kas tiek apstrādātas.</td>
</tr>
<tr class="even">
<td>Importēt bankas izrakstus visām juridiskajām personām ar vienu darbību.</td>
<td>Tagad jūs varat importēt bankas izrakstus visām juridiskajām personām ar vienu darbību. Bankas izrakstu faili var saturēt izrakstus no daudziem bankas kontiem un juridiskajām personām, un zip faili var saturēt vairākus bankas izrakstu failus. Izmantojot vienu importēšanas procesu, jūs varat sākt visu ziņoto bankas kontu saskaņošanu visām juridiskajām personām. Šis līdzeklis palīdz ietaupīt laiku, jo jums nav jāpārslēdzas starp uzņēmumiem un vairāku izrakstu importēšanām. Jūs varat arī automātiski palaist atbilstības kārtulas visos importējamos pārskatos katrā uzņēmumā.</td>
</tr>
<tr class="odd">
<td>Novērtēšanas izsekošana</td>
<td>Vienam pamatlīdzeklim var būt vairāki novērtējumi atšķirīgiem uzskaites standartiem, un pēc izvēles var grāmatot saistītās darbības virsgrāmatā. Iepriekš, šie novērtējumi tika izsekoti, izmantojot vērtības modeļus vai nolietojuma grāmatas. Tagad jūs varat izsekot šiem novērtējumiem, kas ir pazīstami kā grāmatas, izmantojot vienotu žurnālu kopu, pieprasījumus un pārskatus. Unificētā pieredze vienkāršo ieviešanu un samazina interfeisu skaitu, ko pieprasa periodiskie procesi.</td>
</tr>
<tr class="even">
<td>Gūstiet labumu no starpuzņēmumu nolietojuma izpildes uzlabojumiem.</td>
<td>Tagad jūs varat sākt nolietojuma izpildi līdzekļiem visām juridiskajām personām no vienas lapas. Žurnālus var grāmatot arī automātiski, kad tie ir izveidoti. Jūs varat nosūtīt žurnālu izveidi un grāmatošanu pakešapstrādei, tādējādi nolietojums darbojas fonā. Šie uzlabojumi samazina neefektivitāti, jo jums nav jāsāk atsevišķas nolietojuma izpildes atsevišķi katram uzņēmumam. Uzlabojums iespējo labāku centralizētu pamatlīdzekļu pārvaldību.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Cilvēkkapitāla pārvaldība
| Ko iespējams izdarīt                                                                                | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Izveidot veiktspējas žurnālu.                                                                  | Pirms jūs pabeidzat savu pārskatu, jūs bieži vien apkopojat informāciju par aktivitātēm vai notikumiem, kuri papildina jūsu kā darbinieka panākumu sarakstu attiecīgajā pārskata periodā. Jūs varat pievienot ierakstu jūsu veiktspējas žurnālā, lai dokumentētu šīs aktivitātes un notikumus. Jūs varat pievienot šīs aktivitātes un notikumus mērķim vai veiktspējas pārskatu, lai sniegtu papildinformāciju recenzentam.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Izveidot vairāk detalizētu mērķu.                                                                    | Jums ir lielāka kontrole pār iestatīto mērķu saturu. Jūs varat izveidot mērījumus mērķiem, saistīt veiktspējas žurnāla ierakstus ar mērījumiem, pievienot un skatīt dokumentus. Jūs varat saglabāt mērķus kā veidnes, un atkārtoti izmantot tos ātrai iestatīšanai.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Izveidot vairāk detalizētu veiktspējas pārskatu.                                                      | Veiktspējas pārskati, kas oficiālāk tiek saukti par diskusijām, tagad ir pietiekami elastīgi, lai atbalstītu nepārtrauktas atsauksmes un oficiālākus pārskatus. Jūs varat ievilkt aktīvus mērķus, grāmatot komentārus par tiem, un pievienot sadaļas jūsu zināšanu pārskatīšanai. Tiek sniegtas papildu sadaļas, kurās jūs varat pievienot vai apskatīt mērījumus, veiktspējas žurnāla ierakstus, pielikumus un izrakstīšanās, kas ir saistītas ar pārskatu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Saistīt papildu pozīciju hierarhijas ar darbplūsmām.                                      | Jūs varat saistīt darbplūsmu ar pozīciju hierarhiju. Jūs varat arī modificēt darbplūsmas soļus, lai optimizētu apstiprināšanas procesu, lai tas atbilstu jūsu biznesa vajadzībām. Tādējādi jūs varat definēt spēkā esošu apstiprināšanas struktūru, kas atbilst dažādām pārskatu attiecībām, ko lieto jūsu organizācijā.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Darbplūsma atbalsta personas identifikācijas numuru (PIN) ievadīšanu Darbinieku pašapkalpošanās. | Darbplūsmas iespēja Personāla vadībai (HR) ir tikusi paplašināta, un tagad ir satur atbalstu PIN. Darbinieki var pievienot un rediģēt savu PIN, lai uzlabotu efektivitāti. Tomēr, personāla vadības darbinieki var pārskatīt šīs informācijas precizitāti un pabeigtību, pirms viņi to pievieno darbinieka ierakstam.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Izveidot mērķa veidnes, un izmantot tās, lai pievienotu jaunus mērķus.                                          | Jūs varat izveidot mērķa veidnes mērķiem, kas ir kopīgi daudziem darbiniekiem uzņēmumā. Darbinieki var pievienot savus mērķus no veidnes, vadītāji var pievienot mērķus viņu darba grupai no veidnes, personāla vadības darba grupas dalībnieki var pievienot mērķus darbiniekiem visā uzņēmumā.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Izveidot mērķa grupas, un izmantot tās, lai pievienotu jaunus mērķus.                                             | Jūs varat pievienot mērķa veidnes grupai un lietot grupas, lai izveidotu vienu vai vairākus mērķus darbiniekam, darba grupai, amatam, nodaļai vai uzņēmumam.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Lielāka kontrole pār pārskatīšanas procesu.                                                     | Jūs varat izmantot darbplūsmu, lai kontrolētu pārskatīšanas procesu. Jūs varat izveidot pārskata veidnes un izmantot tās, lai veidotu pārskatus. Pārskatam var pievienot arī vērtējumus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Izmantojiet pārskata periodus, lai noteiktu laika posmu pārskatīšanai.                                    | Jūs varat definēt laika periodu veiktspējas pārskatam, pārskata sākuma un beigu datumi tiek ievadīti automātiski. Tomēr šos noklusējuma datumus varat mainīt pēc nepieciešamības.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Piekļuve piecām jaunām personāla vadības Power BI satura pakotnēm                                     | Jaunās satura pakotnes sniedz personāla vadības organizācijām un personāla vadības nodaļu vadītājiem iespēju analizēt tālāk norādīto. Darbaspēka rādītāj • Demogrāfisko datu sadalījums pēc vecuma, dzimuma un ģimenes stāvokļa • Salīdziniet zaudējumu rādītājus pa gadiem un skatiet to iemeslu sarakstu, ko darbinieki ir norādījuši, aizejot no darba organizācijā • Skatiet atvērto pozīciju sarakstu, kā arī atvērto un aizpildīto pozīciju salīdzinājumu Kompensācijas un atvieglojumi • Salīdziniet stundu darba un algotos darbiniekus • Skatiet to darbinieku skaitu, kuri ir reģistrējušies pieejamajiem atvieglojumiem • Skatiet darbiniekus pēc nodarbinātības veida Personāla atlase • Analizējiet kandidātus, pamatojoties uz kandidātu skaitu, kandidātu izcelsmi un pozīcijām, uz kurām viņi ir pieteikušies Organizācijas apmācība • Reģistrācija kursiem pēc atrašanās vietas • Kursu apmeklējums pēc statusa • Kursiem reģistrēto darbinieku saraksts Darbinieku kompetences un izvietošana • Darbinieku prasmju saraksts • Prasmju veidu sadalījums pēc grupas dalībnieka |

## <a name="localizations"></a>Lokalizācijas
<table>




<thead>
<tr class="header">
<th>Ko iespējams izdarīt</th>
<th>Kāpēc tas ir svarīgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lokalizācijas ir pieejamas 18 papildu valstīm:
<ul>
<li>Austrija</li>
<li>Beļģija</li>
<li>Brazīlija</li>
<li>Ķīna</li>
<li>Čehijas Republika</li>
<li>Igaunija</li>
<li>Somija</li>
<li>Ungārija</li>
<li>Itālija</li>
<li>Latvija</li>
<li>Lietuva</li>
<li>Norvēģija</li>
<li>Polija</li>
<li>Saūda Arābija</li>
<li>Spānija</li>
<li>Zviedrija</li>
<li>Šveice</li>
<li>Taizeme</li>
</ul>
Šīm valstīm nepieciešama arī Mazumtirdzniecības lokalizācija. Šajās valstīs Mazumtirdzniecības lokalizācija netika pabeigta un ir paredzēts tikai H1 CY2017:
<ul>
<li>Brazīlija</li>
<li>Čehijas Republika</li>
<li>Igaunija</li>
<li>Ungārija</li>
<li>Latvija</li>
<li>Lietuva</li>
<li>Malaizija</li>
<li>Polija</li>
<li>Zviedrija</li>
</ul></td>
<td>Dynamics 365 for Operations ir pieejama papildu 18 valstīs. Kā daļu no mūsu darba, lai padarītu lokalizāciju vieglāku un vairāk konfigurējamu, regulēšanas elektroniskā pārskata funkcijas tika konvertētas uz Elektroniskā pārskata (ER) konfigurācijām, un daži regulēšanas Microsoft SQL Server pārskatu izveides pakalpojumu (SSRS) pārskati tika pārveidoti ER konfigurācijās, ko izmanto Excel veidnes. Šie konvertētie līdzekļi tiek īpaši minēti vēlāk šajā tabulā.</td>
</tr>
<tr class="even">
<td>Japāna – grupējiet pamatlīdzekļus, drukājot veidlapu 26 un tai pievienotās tabulas.</td>
<td>Veidlapa 26 jāiesniedz katrā pilsētā, kur darbojas korporācija. Lai samazinātu jūsu darbu, drukājot veidlapu 26, pamatlīdzekļus var automātiski grupēt un šķirot pēc atrašanās vietas.</td>
</tr>
<tr class="odd">
<td>Japāna – skatīt paātrinātā un papildu nolietojuma summas profilā.</td>
<td>Profils var sniegt precīzu summu novērtējumu paātrinātam un papildu nolietojumam.</td>
</tr>
<tr class="even">
<td>Japāna – pakāpeniski ieturamā nodokļa aprēķināšana.</td>
<td>Japānas valdība pieprasa ieturamā nodokļa aprēķināšanu pakāpeniski, pamatojoties uz maksājuma summu.</td>
</tr>
<tr class="odd">
<td>Japāna – importēt noteiktu lielu uzņēmumu ēku pasta indeksa failu.</td>
<td>Pasta indeksa failu, kuru iestāde nodrošina noteiktām lielām uzņēmumu ēkām, var importēt sistēmā. Adrese var būt atvasināta no pasta indeksiem.</td>
</tr>
<tr class="even">
<td>Japāna – konfigurēt dīkstāves periodu pamatlīdzekļiem.</td>
<td>Dīkstāves periodi ļauj lietotājam norādītajā periodā apturēt pamatlīdzekļu nolietojumu. Šī funkcionalitāte ir prasības nepieciešamība.</td>
</tr>
<tr class="odd">
<td>Eiropa – konfigurēt puses pievienotās vērtības nodokļa (PVN) reģistrācijas numuru puses adresei, izmantojot Reģistrācijas ID struktūru.</td>
<td>Jūs varat konfigurēt PVN reģistrācijas numuru puses adreses, izmantojot reģistrācijas ID struktūru, un jaunas <strong>PVN ID</strong> reģistrācijas kategorijas.</td>
</tr>
<tr class="even">
<td>Somija – konfigurēt debitora muitas numuru puses adresei, izmantojot Reģistrācijas ID struktūru.</td>
<td>Jūs varat konfigurēt debitora muitas numuru puses adreses, izmantojot reģistrācijas ID struktūru, un jaunu <strong>Debitora muitas ID</strong> reģistrācijas kategoriju.</td>
</tr>
<tr class="odd">
<td>Francija – drukāt debitora rēķinus formātā, kas ir raksturīgs Francijai.</td>
<td>Debitora rēķina izdruka tiek koriģēta Francijas specifiskām prasībām.</td>
</tr>
<tr class="even">
<td>Francija - ieviest hronoloģisku dokumentu numerāciju pēc finanšu perioda.</td>
<td>Lai atbilstu Francijas specifiskajām prasībām debitora rēķinu numerācijā, jūs varat iestatīt numuru sērijas debitoru rēķiniem katrā finanšu periodā.</td>
</tr>
<tr class="odd">
<td>Austrijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>ES pārdošanas saraksts XML formātā Austrijai</li>
<li>Intrastat formāts Austrijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Austrijai</li>
<li>ISO20022 Tiešais debeta maksājuma formāts Austrijai</li>
<li>Austrijas EDIFACT-PAYMUL formāts</li>
<li>PVN deklarācija Austrijai</li>
</ul></td>
</tr>
<tr class="even">
<td>Beļģijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>BLWI formāts Beļģijai</li>
<li>ES pārdošanas saraksts XML formātā Beļģijai</li>
<li>Pamatlīdzekļu pārskats Beļģijai</li>
<li>Intervat formāts Beļģijai</li>
<li>Intrastat formāts Beļģijai</li>
<li>Rēķinu apgrozījuma pārskats Beļģijai</li>
<li>Virsgrāmatas darbību eksportēšanas formāts Beļģijai</li>
<li>SWIFT kreditora maksājuma formāts Beļģijai</li>
<li>CODA bankas izraksta importēšanas formāts Beļģijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Beļģijai</li>
<li>ISO20022 Tiešais debeta maksājuma formāts Beļģijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Brazīlijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>GIA SP Brazīlijai</li>
<li>GIA-ST Brazīlijai</li>
</ul></td>
</tr>
<tr class="even">
<td>Čehijas lokalizācija – ER konfigurācijas</td>
<td><ul>
<li>ES pārdošanas saraksts XML formātā Čehijai</li>
<li>Intrastat formāts Čehijai</li>
<li>PVN deklarācija Čehijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ķīnas lokalizācija – ER konfigurācijas</td>
<td><ul>
<li>Debitoru vecumstruktūras atskaites formāts Ķīnai</li>
<li>Debitora maksājamās summas analīzes pārskata formāts Ķīnai</li>
<li>Kreditoru vecumstruktūras atskaites formāts Ķīnai</li>
<li>Kreditora maksājamās summas analīzes pārskata formāts Ķīnai</li>
<li>Saņemamā maksājuma formāta vecumstruktūras analīzes atskaite Ķīnai</li>
<li>Debitoru bilances atskaites formāts Ķīnai</li>
<li>Virsgrāmatas bilances atskaites formāts Ķīnai</li>
<li>Kreditoru bilances atskaites formāts Ķīnai</li>
<li>GBT fails Ķīnai</li>
<li>Zelta nodokļa eksportēšanas faila formāts</li>
<li>Ražošanas patēriņa novirzes pārskata formāts Ķīnai</li>
</ul></td>
</tr>
<tr class="even">
<td>Igaunijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>ES pārdošanas saraksts XML formātā Igaunijai</li>
<li>Intrastat formāts Igaunijai</li>
<li>Krājumu pārklasificēšanas akts Igaunijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Igaunijai</li>
<li>Debitoru kreditoru bilances paziņojuma pārskats Igaunijai</li>
<li>PVN deklarācija Igaunijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Somijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>ES pārdošanas saraksta TXT formāts Somijai</li>
<li>Intrastat formāts Somijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Somijai</li>
</ul></td>
</tr>
<tr class="even">
<td>Ungārijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>ES pārdošanas saraksts XML formātā Ungārijai</li>
<li>Intrastat formāts Ungārijai</li>
<li>Intrastat vienkāršots formāts Ungārijai</li>
<li>Eksportēt formātu Rēķinu sarakstam Ungārijai</li>
<li>PVN deklarācija Ungārijai</li>
<li>Uzskaitīta PVN deklarācija Ungārijai</li>
<li>Inventarizācijas akts Ungārijai</li>
<li>MultiCash maksājuma formāts Ungārijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Itālijas lokalizācija – ER konfigurācijas</td>
<td><ul>
<li>Intrastat formāts Itālijai</li>
<li>Projekta rēķina formāts Itālijai</li>
<li>Pārdošanas rēķina formāts Itālijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Itālijai</li>
<li>ISO20022 Tiešais debeta maksājuma formāts Itālijai</li>
<li>RIBA atgādinājuma pārskaitījuma formāts Itālijai</li>
<li>Vietējo nodokļu darbību pārskats Itālijai</li>
<li>Melnā saraksta pārskats Itālijai</li>
<li>Modello770 pārskats Itālijai</li>
<li>Ikgadējs nodokļu komunikācijas pārskats Itālijai</li>
</ul></td>
</tr>
<tr class="even">
<td>Latvijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>Kases ieņēmumu lietojuma pārskats (LV)</li>
<li>ES pārdošanas saraksts XML formāts Latvijai</li>
<li>ES pārdošanas saraksta labojumu XML formāts Latvijai</li>
<li>Intrastat (A) formāts Latvijai</li>
<li>Intrastat (B) formāts Latvijai</li>
<li>Krājumu uzskaites saraksts Latvijai</li>
<li>Krājumu uzskaites pārskats Latvijai</li>
<li>Krājumu kustība Latvijai</li>
<li>Iekšējās pārsūtīšanas piegādes pavadzīme Latvijai</li>
<li>Krājumu pārklasificēšanas dokuments Latvijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Latvijai</li>
<li>PVN deklarācija Latvijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lietuvas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>ES pārdošanas saraksts XML formātā Lietuvai</li>
<li>Intrastat formāts Lietuvai</li>
<li>Inventarizācijas akts Lietuvai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Lietuvai</li>
<li>Debitora kreditora savstarpējās saskaņošanas pārskats Lietuvai</li>
<li>PVN deklarācija Lietuvai</li>
</ul></td>
</tr>
<tr class="even">
<td>Norvēģijas lokalizācija – ER konfigurācijas</td>
<td><ul>
<li>Atgādinājuma vēstules formāts Norvēģijai</li>
<li>AutoGiro maksājuma formāts Norvēģijai</li>
<li>AvtaleGiro debitora maksājuma formāts Norvēģijai</li>
<li>eFaktura debitora maksājuma formāts Norvēģijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Norvēģijai</li>
<li>NETS maksājuma formāts Norvēģijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Polijas lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>Intrastat formāts Polijai</li>
<li>Noliktavas dokumenti Polijai</li>
<li>Krājumu pārklasificēšanas dokuments Polijai</li>
<li>MultiCash maksājuma formāts Polijai</li>
<li>MultiCash ārvalstu maksājuma formāts Polijai</li>
<li>Debitoru kreditoru bilances apstiprinājuma pārskats Polijai</li>
</ul></td>
</tr>
<tr class="even">
<td>Saūda Arābijas lokalizācija – ER konfigurācijas</td>
<td>Bank LC papildmaksu sadalījuma formāts Saūda Arābijai</td>
</tr>
<tr class="odd">
<td>Spānijas lokalizācija – ER konfigurācijas</td>
<td><ul>
<li>ES pārdošanas saraksts TXT formātā Spānijai</li>
<li>Intrastat formāts Spānijai</li>
<li>Projekta rēķina formāts Spānijai</li>
<li>Pārdošanas rēķina formāts Spānijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Spānijai</li>
<li>ISO20022 Tiešais debeta maksājuma formāts Spānijai</li>
<li>Spānijas PVN reģistra grāmatas formāts</li>
<li>Spānijas PVN reģistra grāmatu kopsavilkuma formāts</li>
<li>Deklarācijas 347 eksportēšana uz ASCII Spānijai</li>
<li>Deklarācijas 347 pārskats Spānijai</li>
</ul></td>
</tr>
<tr class="even">
<td>Zviedrijas lokalizācija – ER konfigurācijas</td>
<td><ul>
<li>Intrastat formāts Zviedrijai</li>
<li>Bankgirot Autogiro debitora maksājuma formāts Zviedrijai</li>
<li>Bankgirot kreditoru maksājumu formāts Zviedrijai</li>
<li>SWIFT kreditora maksājuma formāts Zviedrijai</li>
<li>SIE eksporta formāts Zviedrijai</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Zviedrijai</li>
</ul></td>
</tr>
<tr class="odd">
<td>Šveices lokalizācija- ER konfigurācijas</td>
<td><ul>
<li>DebitDirect maksājuma formāts Šveicei</li>
<li>LSV tiešais debeta maksājuma formāts Šveicei</li>
<li>ISO20022 Kredīta pārskaitījuma maksājuma formāts Šveicei</li>
<li>ISO20022 tiešais debeta maksājuma formāts Šveicei</li>
<li>ESR bankas izraksta importa formāts Šveicei</li>
</ul></td>
</tr>
<tr class="even">
<td>Vācija — Eksportēt kreditora maksājumus DTAZV formātā</td>
<td>Vācijā ir nepieciešams DTAZV ar ārzemju formāta specifikāciju, kas apzīmē kredīta pārskaitījuma (kreditora maksājuma) ziņojumu saskaņā ar specifikāciju par pārrobežu maksājumiem no Vācijas uz kontu ārvalstu bankā vai uz iekšzemes banku ārvalstu valūtā. 
</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektroniskie pārskati

| Ko iespējams izdarīt                                                                                                                                                                                                                                                                                     | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurēt ER pārskatus, lai ievietotu datus vairākos formātos, no Dokumentu pārvaldības krātuves elektroniskajos ziņojumos, kas tiek ģenerēti.                                                                                                                                                              | ER pārskati var ievietot datus elektroniskos ziņojumos, kas tiek ģenerēti no Dokumentu pārvaldības krātuves. Tāpēc biznesa dokumentu pielikumus var pievienot elektroniskajiem ziņojumiem, kas tiek izveidoti šim dokumentam, saskaņā ar likumdošanas prasībām. Pašlaik šos pielikumus var pievienot MIME formātā XML ziņojumam, kas tiek ģenerēts. Alternatīvi, pielikumus var pievienot Base64 formātā binārajam ziņojumam, kas tiek ģenerēts.                                                                      |
| Konfigurēt ER pārskatus, lai izveidotu elektroniskus dokumentus Excel, Microsoft Word vai PDF formātā.                                                                                                                                                                                                      | Viena konfigurācija ļauj ER pārskatiem ģenerēt elektroniskus dokumentus trīs dažādos formātos: OpenXML darblapa (Excel), Word un XML veidlapu datu formāts (XFDF) (PDF). Lietotāji var atlasīt formātu, pievienojot formāta veidni ER pārskatam kā Excel, Word vai PDF dokumentu.                                                                                                                                                                                                                                                                       |
| Konfigurēt ER pārskatus, lai ievietotu datus elektronisko dokumentu lappušu galvenēs un kājenēs, kas tiek ģenerēti OpenXML darblapas formātā, un lai kontrolētu lapu pārtraukumus.                                                                                                                               | ER pārskati var ievadīt biznesa datus lappušu galvenēs un kājenēs, kā arī kontrolēt, kur parādās lappuses pārtraukumi. Tādējādi, pārskati var atbalstīt ģenerēto elektronisko dokumentu lapu statiskas augšējās un apakšējās sadaļas. Tie atbalsta arī noteiktu šo dokumentu lapošanu, lai tie atbilstu likumdošanas prasībām.                                                                                                                                                                                                             |
| Konfigurējiet ER pārskatu adresātus, lai rezultāts tiek nosūtīts pa e-pastu, un biznesa dati un ER loģika (izteiksmes) var tikt izmantoti, lai izpildlaikā norādītu e-pasta adresi, kas jāizmanto.                                                                                                    | Iepriekš, konfigurējot ER adresātu, izvades adresāta e-pasta adresi varētu definēt noformēšanas laikā. Tagad jūs varat konfigurēt izteiksmi ER formātā. Šo izteiksmi tad var atlasīt adresātā kā e-pasta adreses avotu katrai formāta konfigurācijai, un katram rezultāta komponentam (mape vai fails) atsevišķi. Tādējādi, izpildot ER pārskatu, katru izveidoto failu var nosūtīt citam saņēmējam, un e-pasta adresi var definēt, pamatojoties uz ER loģiku un biznesa datiem. |
| Konfigurējiet ER pārskatu adresātu, lai rezultāts tiek nosūtīts uz Microsoft SharePoint mapi kā no jauna nosaukts fails, vai jauna esošā faila versija, un lai biznesa datus Microsoft Power BI struktūrā varētu izmantot kā datu kopu vai pārskatu.                 | Konfigurējot ER pārskatus, jūs varat viegli (bez kodēšana) sagatavot pieprasītos biznesa datus, lai tos varētu izmantot Power BI struktūrā. Izpildot šos ER pārskatus, jūs varat nodrošināt Power BI struktūru ar atbilstošiem biznesa datiem un/vai Excel pārskatiem, kas jau ir pieejami. Ja plānojat pārskata izpildes atkārtošanās režīmā, jūs varat izveidot ieplānotu biznesa datu sadali no Dynamics 365 for Operations uz Power BI, lai atbalstītu Power BI pārskatu atjaunināšanas grafiku.                             |
| Konfigurējiet ER pārskatus, lai izmantotu daļu no elektroniska dokumenta, kas jau ir izveidots kā datu avots, lai ģenerētu pārējo šī dokumenta daļu.                                                                                                                                             | Jūs varat konfigurēt ER pārskatus, kas veido rezultātu teksta formātā, lai veiktu dokumenta rindas uzskaiti. Šo informāciju var izmantot citās dokumenta daļās, lai izveidotu rindas, kas ietver kopsavilkuma informāciju. Kopsavilkuma informācija (kopsummas un numuri) var būt aprēķināta un drukāta uz elektroniskiem dokumentiem, kas tiek ģenerēti, neprasot papildu datu transformācijas. Tādējādi šis līdzeklis uzlabo pārskata izpildes veiktspēju, un palīdz nākotnē vieglāk uzturēt konfigurēto ER formātu.    |
| Konfigurējiet ER pārskatus, lai norādītu faila nosaukuma paplašinājumu elektroniskajam dokumentam, kas tiek ģenerēts teksta formātā.                                                                                                                                                                                 | Jūs varat konfigurēt ER pārskatus, lai izveidotu rezultātu teksta formātā, lai to var saglabāt kā failu ar noteiktu paplašinājumu. Papildus noklusējuma. txt paplašinājumam, jūs varat konfigurēt tādus paplašinājumus kā .csv un .prn, saskaņā ar formāta specifikāciju.                                                                                                                                                                                                                                                                             |
| Veidojiet jaunus ER pārskatus, kas ir balstīti uz konkrētu ER modeļa versiju.                                                                                                                                                                                                                          | Iepriekš, izveidojot jaunu ER formātu, tikai atlasītā ER modeļa jaunāko versiju varēja izmantot kā formāta datu avota atrašanās vietu. Tagad ir iespējams atlasīt jebkuru pieejamo atlasītā ER modeļa versiju. Šī funkcija ļauj uzturēt ER pārskatus pašreizējam gadam, un paralēli veidot jaunu ER modeļa versiju nākamajam gadam.                                                                                                                                                                                          |
| Meklēt datu avoti un formātus/modeļus pēc teksta, vai atlasītā artefakta ar vienu klikšķi. Aktīvi risiniet pārskatījuma konfliktus, un risiniet konfliktus starp konfigurācijām. Konfigurējiet ER pārskatus, lai izveidotu vairākus pārbaudes ziņojumus par kļūdām, kas tiek atklātas līdz pārskata izpilde tiek apturēta. | Vairāki lietotāja pieredzes (UX) uzlabojumi ER struktūrā palīdz lietotājiem strādāt ar ER efektīvi un viegli.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Rādīt **ER** darbvietu Power BI pārskatos.                                                                                                                                                                                                                                                      | Lietotāji var konfigurēt **ER darbvietas** lapu, lai tajā tiktu iekļauti jauni izvēlnes elementi un dinamiskie elementi, kas izpilda Power BI pārskatus.                                                                                                                                                                                                                                                                                                                                                                                                                       |

## <a name="payroll"></a>Alga
<table>




<thead>
<tr class="header">
<th>Ko iespējams izdarīt</th>
<th>Kāpēc tas ir svarīgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Konfigurējiet apmaksas ierakstus un apstrādājiet algas, izmantojot funkcionalitāti, kas ir ekvivalenta moduļa <strong>Alga</strong> funkcionalitātei sistēmā Microsoft Dynamics AX 2012 R3.</td>
<td>Tagad jūs varat konfigurēt un apstrādāt US alga, izmantojot līdzekļu kopu, kas ir ekvivalenta līdzekļu kopai sistēmā AX 2012 R3.
<ul>
<li>Jūs varat konfigurēt apmaksas ciklus un apmaksas periodus, darba ciklus un darba periodus, ieņēmumu kodus un ieņēmumu kodu grupas, grafikus, atvaļinājumu veidus un atvieglojumu uzkrājumu plānus.</li>
<li>Jūs varat arī iestatīt obligātus ieturējumus nodokļiem un atvieglojumiem, un reģistrēt algas informāciju amatiem un darbiniekiem, pārskatu un analīzes nolūkiem.</li>
<li>Jūs varat arī iestatīt un pārvaldīt ieturējumus ieturējumiem un nodokļu maksājumiem, kā arī jebkurām saistītajām administratīvajām maksām.</li>
</ul></td>
</tr>
<tr class="even">
<td>Pārraudzīt un apstrādāt jūsu apmaksas perioda procesu iespējams, izmantojot jauno darbvietu <strong>Algu pārvaldība</strong>.</td>
<td>Tagad jūs viegli varat pārraudzīt jūsu algu apstrādi. Acumirklī algu administratori var redzēt ienākumu un algu pārskatus, kuriem jāpievērš uzmanība, lai apmaksas būtu pilnīgas un precīzas. Darbvieta <strong>Algu pārvaldība</strong> ļauj lietotājiem pārraudzīt un palaist procesus no sākuma līdz beigām no vienas darbvietas.</td>
</tr>
<tr class="odd">
<td>Ģenerēt pozitīvā maksājuma failus algas čekiem.</td>
<td>Nav jaunu paplašinājumu Kases un bankas vadības pozitīvo maksājumu funkcionalitātei algu maksājumiem. Tika pievienoti atsevišķi izvēlnes elementi visā pamata procesā, lai iespējotu izolētu konfigurāciju, kas ir raksturīga algai. Funkcionalitāte ir identiska pamata pozitīvā maksājuma līdzeklim, kas tika izlaists Microsoft Dynamics AX programmas versijā 7.0.1 (2016. gada maijs). Šī paplašinājuma dēļ algu dati ir pilnīgi izolēti no pārējām pozitīvo maksājumu darbībām. Šīs izolēšana palīdz nodrošināt to, ka tikai algu lietotāji var piekļūt un redzēt datus, kas ir saistīts ar algu.</td>
</tr>
<tr class="even">
<td>Importējiet ienākumu izraksta rindas no ārēja avota, izmantojot jauno Ienākumu izraksta rindas datu elementu.</td>
<td>Svarīgs jauns datu elements ļauj integrēšanu ar ārējām laika un ienākumu aprēķina sistēmām. Datu elements importē ienākumu izraksta rindas un veic visu to pašu noklusējuma loģiku, ko lietotājs pa tiešo ievadīja ienākumu pārskatā. Pēc importēšanas, rindas tiek automātiski saistītas ar atbilstošu ienākumu izraksta dokumentu. Ja nepastāv atbilstošs ienākumu izraksta dokuments, dokuments tiek izveidots automātiski.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Plānošana un grafika veidošana
| Ko iespējams izdarīt                                                                                                                                                                                                      | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Iestatīt noklusējuma pasūtījuma iestatījumus pārdošanas un pirkšanas pasūtījumos, pamatojoties uz jebkuru aktīvu preces dimensiju preces šablonā. Tādējādi jūs varat definēt pasūtījuma noklusējuma iestatījumus noliktavas vienībai (NV) vai daļējai NV. | Jūs varat norādīt noklusējuma pasūtījuma iestatījumus, kas tiek piemēroti preces dimensijai vai aktīvu preces dimensiju kombinācijai. **Piemērs,** Jūs pārdodat preci ar nosaukumu Polo t-krekls. Šī prece ir pieejama divās krāsās: zaļā un zilā krāsā. Tā ir pieejama divos izmēros: mazs un vidējs. Krāsa un Izmērs ir aktīvas preces dimensijas Polo t-kreklam. Jūs varat bloķēt visus zaļo Polo t-kreklu pirkumus, neatkarīgi no to izmēra. |

## <a name="product-master-data"></a>Preces šablona dati
<table>




<thead>
<tr class="header">
<th>Ko iespējams izdarīt</th>
<th>Kāpēc tas ir svarīgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vienlaicīgi iestatiet pasūtījuma noklusējuma iestatījumus un vietai raksturīgo pasūtījumu iestatījumus, no vienas lapas.</td>
<td>Šis līdzeklis nodrošina labāku krājumu iestatījumu pārskatu.</td>
</tr>
<tr class="even">
<td>Izveidot preces variantu numuru nomenklatūru.</td>
<td>Preces variantu numuros varat iekļaut tādus elementus kā preču dimensijas, atribūti un rakstzīmes. Veidojot pārdošanas pasūtījumu vai pirkšanas pasūtījumu, jūs varat ātri atrast noteiktu produkta variantu.</td>
</tr>
<tr class="odd">
<td>Meklēt preces un preču variantus pārdošanas un pirkšanas scenārijos.</td>
<td>Veidojot pārdošanas vai pirkšanas rindas, jūs varat meklēt preces, izmantojot preču dimensijas un visus preču numurus, izņemot globālās tirdzniecības krājumu kodus (GTIN) un svītrkodus. Šī meklēšana ir pilnteksta meklēšana, kas aizstāj esošo "Sākas ar" meklēšanu, kas tiek izmantota pārdošanas un pirkšanas uzmeklēšanas sarakstā. Šī funkcija ļauj jums atrast preču grupas, ar līdzīgām īpašībām vai vienu preci, ar unikālām iezīmēm. Lai iespējotu šo līdzekli, atlasiet parametru <strong>Iespējot uzmeklēšanu preču meklēšanā</strong> lapā <strong>Meklēšanas parametri</strong>.</td>
</tr>
<tr class="even">
<td>Norādiet preces variantu tieši, veidojot pārdošanas vai pirkšanas darbību. Alternatīvi jūs varat atlasīt derīgu dimensiju kombināciju sarakstā.</td>
<td>Šis līdzeklis ir produktivitātes uzlabojums. <strong>Piemērs.</strong> Jūs pārdodat preci ar nosaukumu Polo t-krekls. Šī prece ir pieejama divās krāsās: zaļā un zilā krāsā. Tā ir pieejama divos izmēros: mazs un vidējs. Krāsa un Izmērs ir aktīvas preces dimensijas Polo t-kreklam. Ievadot pārdošanas rindu Polo t-kreklam, zaļā krāsā, izmērs - mazs, jums nav nepieciešams ievadīt datus laukos <strong>Krājuma kods</strong>, <strong>Krāsa</strong>, un <strong>Izmērs</strong>. Jūs varat izveidot rindu, rīkojoties pēc viena no šiem variantiem:
<ul>
<li>Laukā <strong>Krājuma kods</strong> ievadiet preces varianta numuru, krāsu vai izmēru. Uzmeklēšanā atrodiet noteikto variantu, kuru vēlaties pārdot, un izveidojiet pārdošanas rindu.</li>
<li>Laukā <strong>Krājuma kods</strong> ievadiet krājuma kodu. Dodieties uz jebkuru preces dimensijas lauku. Uzmeklēšanā <strong>Preces dimensija</strong> jūs redzēsiet visas izlaistās dimensiju kombinācijas, kas attiecas uz Polo t-kreklu. Ar vienu darbību jūs varat atlasīt preces variantu, kuru vēlaties pārdot.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Norādiet, vai preču numuri parādās darbību lapās.</td>
<td>Darbību lapas, piemēram, pārdošanas pasūtījumi un pirkšanas pasūtījumi, parāda tikai laukus <strong>Krājuma kods</strong> un <strong>Preces nosaukums</strong>. Lai redzētu lauku <strong>Preces numurs</strong>, atlasiet parametru <strong>Rādīt preces numurus formās</strong> sadaļā <strong>Preču informācijas pārvaldības parametri</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Projektu vadība un uzskaite
| Ko iespējams izdarīt                                                                                                           | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Grāmatojot rēķina priekšlikumus paketē, izmantojiet vēlo atlasi.                                                            | Projekta grāmatveži var iestatīt pakešuzdevumu, lai automātiski saņemtu rēķinu priekšlikumus grāmatošanai, ja šie priekšlikumi atbilst pakešuzdevumā norādītajiem kritērijiem. Šis līdzeklis uzlabo rēķina grāmatošanas automatizāciju, jo pakešuzdevums var darboties nepārtraukti, un automātiski izdod priekšlikumus grāmatošanai. |
| Izveidot analīzi Power BI darbvirsmā.                                                                                     | Biznesa informācijas (BI) saturu ar projektu saistītajiem un ar resursu saistītajiem datiem var viegli izveidot Power BI darbvirsmā.                                                                                                                                                                                                       |
| Izmantojiet pirkšanas pasūtījumu priekšapmaksas, un pareizi iekļaujiet tās projekta novērtējuma procesā.                               | Projekta pirkšanas pasūtījumiem priekšapmaksas ir jāapstrādā pirms daži maksājumu var tikt nodoti kreditoriem. Šie priekšapmaksas rēķini tagad parādās projekta novērtējuma/atzīšanas procesā projektiem, kas attiecas uz veidu **Fiksēta cena**.                                                                                           |
| Piekļūt un pārvaldīt izmaksas, ieņēmumu novērtējumus un krājumu vajadzības tieši no darba sadalījuma struktūras (WBS) uzdevuma. | Jūs varat pārvaldīt izmaksu aprēķinus, ieņēmumu novērtējumus un krājumu vajadzības noteiktiem WBS uzdevumiem, šī uzdevuma detalizētas informācijas dialoglodziņā, WBS plānošanas skatā.                                                                                                                                                                 |
| Atlasiet finansējuma avotu maksas žurnālos.                                                                                    | Ja līgums projektam satur vairākus finansējuma avotus, jūs varat atlasīt vienu noteiktu finansējuma avotu, kad tiek grāmatotas maksas. Ja jūs neatlasāt noteiktu finansējuma avotu, finansējuma nosacījumi, kas tiek norādīti līgumā, tiek izmantoti, lai piešķirtu maksu.                                                                   |
| Atvērt projekta izrakstus programmā Excel.                                                                                         | Jauni datu elementi virsgrāmatas un budžeta atjauninājumiem ļauj atvērt projekta izraksta datus programmā Excel, un izveidot analīzi, izmantojot Excel funkcionalitāti.                                                                                                                                                                           |
| Izmantojiet tikai vienu konfigurācijas atslēgu, lai aktivizētu funkcionalitāti Projektu vadībai un uzskaitei (PMA).                       | Ar projektu saistītās konfigurācijas atslēgas tika aizstātas ar vienu projekta konfigurācijas atslēgu, kas iespējo PMA funkcionalitāti.                                                                                                                                                                                                       |

## <a name="retail-and-commerce"></a>Mazumtirdzniecība un komercija
### <a name="advanced-warehouse-management-in-a-retail-store"></a>Papildu noliktavas pārvaldība mazumtirdzniecības veikalā

Mazumtirgotāji var izmantot Papildu noliktavas pārvaldības (WHS) risinājumu veikalos, un veikt nepieciešamos atjauninājumus pārdošanas punktu (POS) līdzekļos, lai to atbalstītu. Rokas risinājumu procesiem būtu jādarbojas veikalā tāpat, kā jebkurā citā noliktavā. Visi pašreizējie mazumtirdzniecības veikala krājumu procesi un jebkuru POS procesi, kas izveido vai atjaunina krājumu darbības, tiek atjaunināti īpašu WHS iespējotu noliktavu prasību izmantošanai.

| Ko iespējams izdarīt                                                                       | Kāpēc tas ir svarīgi                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lietojiet POS, lai uzmeklētu pieejamos krājumus WHS iespējotajos veikalos.                     | Meklējot krājumu, procesam ir jādarbojas tāpat kā iepriekš. Uzmeklēšanai vajadzētu rādīt pieejamo daudzumu noliktavas līmenī, un nevajadzētu ņemt vērā Atrašanās vietu, Krājumu statusu vai Noliktavas vienības izmērus. |
| Lietojiet POS, lai apstrādātu preču ieejas plūsmu pārsūtīšanas pasūtījumam WHS iespējota veikalā. | Varat saņemt pārsūtīšanas pasūtījumus POS WHS iespējotam veikalam un krājumiem. Lietotājam jābūt iespējai atlasīt saņemšanas atrašanās vietas, kā arī ievadīt noliktavas vienības ID, lai automātiski aizpildītu saņemšanas rindas.    |
| Lietojiet POS, lai apstrādātu preču ieejas plūsmu pirkšanas pasūtījumam WHS iespējota veikalā. | Varat saņemt pirkšanas pasūtījumus POS WHS iespējotam veikalam un krājumiem. Lietotājam jābūt iespējai atlasīt saņemšanas atrašanās vietas, kā arī ievadīt noliktavas vienības ID, lai automātiski aizpildītu saņemšanas rindas.    |
| Lietojiet POS, lai apstrādātu kravu no WHS iespējota veikala produktu.               | Jūs varat reģistrēt pārsūtīšanas no POS WHS iespējotam veikalam un krājumiem. Lietotājam jābūt iespējai atlasīt nosūtīšanas atrašanās vietas, krājumu statusam jābūt automātiski ģenerētam, un noliktavas vienības ir jāignorē.         |

### <a name="enable-seamless-omni-channel-commerce"></a>Iespējot viengabala visaptveroša kanāla komerciju

Viengabala visaptveroša kanāla komercija attiecas uz pārvaldību un pasūtījumu apstrādi fiziskajiem veikaliem, tiešsaistes veikaliem, zvanu centriem un mobilās komercijas pieredzei. Šim laidienam šajā jomā veikti šādi ieguldījumi:

-   Uzlabojumi e-komercijas veikalu publicēšanā
-   Jauna uz patērētāju virzīta mobilā lietojumprogramma, kas iespējo preču noteikšanu, konta pārvaldību un tiešsaistes iepirkšanos

| Ko iespējams izdarīt                                                                                                                                                                                                                                                                   | Kāpēc tas ir svarīgi                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Patērētājs: Pašreizējā laidiena uz patērētāju virzītā mobilā lietojumprogramma iespējo šādas funkcijas - produktu meklēšana, kategoriju pārlūkošana, pievienošana grozam un norēķināšanās kā viesim. Mazumtirgotāji arī var pielietot sava uzņēmuma zīmolu lietojumprogrammā, un pēc tam izvietot pakotni Android un iOS lietojuprogrammu veikaliem. | Mazumtirgotāji var viegli izveidot uz patērētāju virzītu mobilo lietojumprogrammu, kas ļauj klientiem pārlūkot, meklēt preces un nosūtīt preces kā viesim no mobilajām ierīcēm.                      |
| Klientu vēlmju saraksti e-komercijas tiešsaistes veikaliem                                                                                                                                                                                                                             | Neatkarīgi programmatūras piegādātāji (ISV) var izmantot vēlmju saraksta vadīklu, lai ļautu lietotājiem izveidot un pārvaldīt vairākus sarakstus tiešsaistes veikalos, un skatīt/lietot šos sarakstus POS. |
| Asinhronā debitora izveide, izmantojot e-komercijas tiešsaistes veikalus                                                                                                                                                                                                                  | ISV tagad var izveidot debitoru kontus pat tad, ja Commerce Data Exchange: Real-Time Service nav pieejams.                                                                        |
| Publicēt kanāla preces no Mazumtirdzniecības servera trešās puses veikalos.                                                                                                                                                                                                           | Mazumtirdzniecības serveris tagad atbalsta autentifikāciju pakalpojums pakalpojumam. ISV var izmantot kanāla preču publicēšanu no Mazumtirdzniecības servera trešās puses veikalos.               |

### <a name="extensibility"></a>Paplašināmība

-   Commerce runtime projekti tagad ir aizzīmogots no Retail SDK.
-   Vieglāka izvietošana un apkalpošana, izmantojot Microsoft komponentu un ISV pakotnes POS, Mazumtirdzniecības servera, datu bāzes, maksājumu un aparatūras stacijas.

| Ko iespējams izdarīt                                                                                                                 | Kāpēc tas ir svarīgi                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CRT/Mazumtirdzniecības serveris: Mazumtirgotāji vai ISV var paplašināt CRT, izmantojot paplašinājumu āķus. Iekļautās koda izmaiņas vairs netiek atbalstītas. | Lai iespējotu nepārtrauktu integrāciju un nepārtrauktu izvietošanu, ir pilnībā jāizvairās no iekļautā koda izmaiņām. Lai atbalstītu vieglu labojumfailu uzņemšanu bez jebkāda koda sapludināšanas un izvietošanas CRT komponentiem. |

### <a name="personalized-product-recommendations"></a>Personalizēti preču ieteikumi

| Ko iespējams izdarīt                                                                                                                                                                                                                                                                        | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skatiet personalizētus ieteikumus vairākās saskares vietās pārdošanas punktā (POS), lai noteiktu, kas debitoru varētu interesēt, pamatojoties uz viņa pirkumu vēsturi, krājumiem viņa vēlmju sarakstā, kā arī krājumiem, kurus citi debitori ir nopirkuši tiešsaistes un fiziskajos veikalos. | Ja mazumtirgotājam ir plašs preču katalogs, personalizētie ieteikumi palīdz debitoram atklāt preces un veikala darbiniekiem efektīvi apkalpot klientus. Preču ieteikumi nodrošina, ka debitoram tiek piedāvātas viņa interesēm un iepirkumu vēsturei atbilstošas preces, un tādējādi var palīdzēt mazumtirgotājiem veikt papildu pārdošanu un uzlabot klientu lojalitātes saglabāšanas rādītājus. Programmatūrā Microsoft Dynamics 365 for Retail preču ieteikumi tiek nodrošināti, izmantojot pakalpojumu Cognitive Services un Microsoft Azure algoritmisko mācīšanos. |

### <a name="pos-task-recorder"></a>POS uzdevumu reģistrētājs

| Ko iespējams izdarīt                                                                                                                                                                                                  | Kāpēc tas ir svarīgi                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mazumtirgotāji var izmantot POS uzdevumu ierakstītāju, lai veidotu apmācību materiālus, Biznesa procesu modelētājs (BPM) diagrammas, un izveidot Palīdzības saturu, lai uzlabotu produktivitāti un veiktu labāku pieteikumu analīzi un plānojumu. | Lai iespējotu nepārtrauktu integrāciju un nepārtrauktu izvietošanu, ir pilnībā jāizvairās no iekļautajām izmaiņām. Lai atbalstītu vieglu labojumfailu uzņemšanu bez jebkāda koda sapludināšanas un izvietošanas CRT komponentiem. |
| POS reāllaika palīdzība.                                                                                                                                                                                           | Kasieris/Vadītājs var saņemt reāllaika palīdzību no POS par biznesa procesu bez konteksta pārslēgšanas.                                                                                                           |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Veikala sistēma: viengabala lokāla veikala pieredzes sniegšana

Veikala sistēma ir izvietošanas izvēle mazumtirgotājiem, kas palīdz vadīt veikala darbību kopumu lokālā veikalā, Microsoft publiskajā mākonī vai klienta privātajā mākonī. Šim laidienam tvērums ir tikai veikala ietvaros. Lai labāk atbalstītu vides, kurām ir lēna un nedroša tīkla savienojamība, nepieciešams mazumtirgotājiem sniegt iespēju veikalā izvietot kanāla datu bāzi un Mazumtirdzniecības serveri. Pēc tam tie var turpināt darboties savos pamata uzņēmējdarbības scenārijos, pat ja nav savienojamības ar galveno pārvaldi (HQ). Pamatojoties uz dažādiem datu punktiem, kas satur tehniskās grupas diskusijas, klientu aptauju rezultātus un konkurentu analīzi, mēs esam noteikuši šādu risinājumu tvērumu kā ideāli piemērotu mūsu mērķa klientiem:

-   Pašapkalpošanās pakete ir pieejama Veikala sistēmai.
-   Noklusējuma instalācija ir viena lodziņa izvietošana, taču ir pieļaujama pielāgota izvietošana.
-   Viegla izvietošana/pašapkalpošanās.
-   Mazumtirdzniecības serveris un veikala datu bāze ir veikalā kopā ar Async klienta pakalpojumu.
-   Mazumtirdzniecības serveris veikalā sazinās tieši ar Programmas objektu serveri (AOS), HQ veikala sistēmai.
-   Atbalsta krustu termināļa scenārijus, kur nav HQ savienojamības.
-   Retail Modern POS un Mākoņa POS vienmēr sazinās ar Mazumtirdzniecības serveri veikalā.
-   Atbalsta Retail Modern POS un Mākoņa POS, ja nav HQ savienojamības.
-   Atbalsta Retail Modern POS – konkrētu bezsaistes datu bāzi (izolēta, lai sasniegtu katru Retail Modern POS gadījums), ja nav HQ savienojamības.
-   Autentifikācijas ir balstīta uz pakalpojums-pakalpojumam tikai Veikala sistēmai.
-   Reāllaika servisa zvani netiek atbalstīti, ja nav interneta savienojuma.
-   Retail Modern POS tiešā datu bāzes savienojamība ar kanāla datu bāzi netiek atbalstīta.
-   Iespējot telemetriju/pārraudzību.

| Ko iespējams izdarīt                                                                                                                                       | Kāpēc tas ir svarīgi                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Mazumtirgotājs lejupielādē Veikala sistēmas pašapkalpošanās instalētāju no Dynamics AX HQ datu bāzes kanāla lapas, un lejupielādē konfigurācijas failu.   | Mazumtirgotājs var efektīvi lejupielādēt pašapkalpošanās pakotni.                                          |
| Mazumtirgotājs instalē Veikala sistēmu, izmantojot pašapkalpošanās instalētāju.                                                                                 | Mazumtirgotājs var instalēt Veikala sistēmu, izmantojot pašapkalpošanās pakotni.                                |
| IT vadītājs konfigurē Veikala sistēmu Dynamics 365 for Operations (kanāla datu bāze, kanāla profils, veikals, izvietojama pakotne).             | IT vadītājs var konfigurēt Veikala sistēmu vieglāk un efektīvāk.                                       |
| Mazumtirgotājs izmanto Retail Modern POS lokālā veikalā, un var veikt reāllaika darbības, piemēram, izsniegt dāvanu kartes, ja ir savienojums. | Mazumtirgotājs var veikt reāllaika darbības no Veikala sistēmas, ja ir savienojums.                |
| Mazumtirgotājs var sinhronizēt datus no lokālā Veikala sistēmas uz HQ katru reizi, kad ir savienojums.                                                      | Mazumtirgotājs sinhronizēt uz un no Veikala sistēmas, ja ir savienojums.                              |
| Mazumtirgotājam var būt drošs savienojums starp lokālā Veikala sistēmu un HQ.                                                                 | Mazumtirgotājs var droši sazināties no Veikala sistēmas, ja ir savienojums.                     |
| IT vadītājs un Microsoft Operations var pārraudzīt un veidot pārskatu par lokālo Veikala sistēmu (diagnostika un pārskata veidošanas izmaiņas).                   | IT vadītājs un Microsoft Operations var pārraudzīt Veikala sistēmu droši un efektīvi novērst problēmas. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Universālās Windows platformas programma Retail Modern POS

Pašlaik Retail Modern POS ir pieejams tikai kā operētājsistēmas Windows 8.1 programma galddatoriem un planšetdatoriem, un kā mākoņa POS galddatoru vai planšetdatoru pārlūkprogrammām. Šajā laidienā Retail Modern POS tiek pārvērsts par Universālās Windows platformas programmu (UWP). Šī izmaiņas ļaus palaist Retail Modern POS jebkurā Windows 10 ierīcē (galddators, planšetdators vai viedtālrunis), un pat pārslēgties starp skatiem ierīcēm ar iespējotu nepārtrauktību.

| Ko iespējams izdarīt                                                   | Kāpēc tas ir svarīgi                                                                                     |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Iespējot svarīgu POS funkcionalitāti maza faktora ierīcēm. | Retail POS funkcionalitāte ir pieejama tālruņiem un citām maza faktora ierīcēm, kas darbojas ar Windows 10. |

## <a name="supply-chain-management"></a>Piegādes ķēdes pārvaldība
### <a name="consignment-inventory"></a>Sūtījuma krājumi

| Ko iespējams izdarīt                                                                                                                                                                | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kā kreditors, jūs varat uzglabāt izejmateriālus debitora noliktavā. Kā debitors, jūs varat atlikt faktisko pirkšanu līdz brīdim, kad izejmateriāli ir nepieciešami ražošanai. | Izejmateriālu krājuma saglabāšana var ietvert nopietnas izmaksas. Izmantojot sūtījuma krājumu, kreditors var glabāt izejmateriālus debitora noliktavā. Debitors var atlikt faktisko pirkšanu līdz brīdim, kad izejmateriāli ir nepieciešami ražošanai. Izejmateriāli tiek pasūtīti un saņemti, izmantojot sūtījuma papildināšanas pasūtījumu. Šis papildinājuma pasūtījums reģistrē fiziskās darbības, bet neietekmē virsgrāmatu. Lai atšķirtu klientam piederošus krājumus un kreditoram piederošus krājumus, jūs varat lietot krājumu dimensiju "Īpašnieks". Krājumu īpašnieka maiņu veic žurnāla process, kas apstrādā īpašumtiesību maiņu izejmateriāliem no kreditoram piederošiem krājumiem uz debitoram piederošiem krājumiem. Šis process aktivizē pirkšanas pasūtījuma un produkta ieejas plūsmas izveidi. **Piezīme:** šis līdzeklis ir ierobežots ienākošo sūtījumu izejmateriālu ražošanai. Tas nav integrēts ar Noliktavas pārvaldību (WHS) un Transportēšanas pārvaldību (TMS). |
| Kā kreditors, iegūstiet informāciju par nosūtīto krājumu, kas tiek pārsūtīts debitoram.                                                                      | Lai izrakstītu rēķinu debitoram, kreditoram ir nepieciešama informācija par izejmateriāliem, kas tika iegādāti no sūtījuma krājuma, un iegādes datums. Kreditors var arī pārraudzīt paredzamos rīcībā esošos krājumus debitora atrašanās vietā, izmantojot kreditoru sadarbības interfeisu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Pārvietot kreditora īpašumā esošos krājumus, izmantojot pārsūtīšanas žurnālu.                                                                                                                       | Lai izsekotu kreditora īpašumā esošo krājumu fizisko stāvokli, jums ir jābūt iespējai ierakstīt sistēmas pozīciju. Izmantojot pārsūtīšanas žurnālu, ir iespējams reģistrēt krājumu fizisko kustību, piemēram, pārvietošanos no vienas vietas noliktavā uz citu vietu šajā noliktavā.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Koriģēt kreditora īpašumā esošos krājumus, izmantojot uzskaites žurnālu.                                                                                                                     | Ir svarīgi saglabāt rīcībā esošo krājumu sistēmu sinhronizētu ar faktisko fizisko krājumu. Kreditora īpašumā esošos krājumus var koriģēt, izmantojot uzskaites procesus, piemēram, daudzuma korekcija un uzskaites žurnāla procesi.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Uzziniet vairāk par sūtījuma atbalstu sistēmā Dynamics 365 for Operations                                                                                                         | Papildinformāciju par sūtījuma apstrādes procesu atbalstu skatiet tēmās [Sūtījums](../../supply-chain/inventory/consignment.md), [Sūtījuma iestatīšana](../../supply-chain/inventory/set-up-consignment.md), [Sūtījuma papildināšanas pasūtījuma izveide (uzdevuma ceļvedis)](../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) un [Sūtījumu krājumu īpašumtiesību maiņa, pamatojoties uz ražošanas pieprasījumu (Uzdevuma ceļvedis)](../../supply-chain/inventory/tasks/change-ownership-consignment.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Kreditora sadarbība (iepriekš zināma kā Kreditoru portāls)

| Ko iespējams izdarīt                                                                      | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sniegt iespēju kreditoriem atbildēt uz katru pirkšanas pasūtījuma rindu un ierosināt izmaiņas.           | Dažos gadījumos kreditori vēlas pieņemt dažas pirkšanas pasūtījuma rindas, bet citas - noraidīt. Kreditori tagad var individuāli pārvaldīt pirkšanas pasūtījuma rindas. Katra rinda var būt noraidīta, pieņemta vai pieņemta ar izmaiņām. Piemēram, kreditori var mainīt piegādes datumu, sadalīt piegādi un daudzumu vai ieteikt alternatīvu krājumu.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sniegt kreditoriem iespēju pārvaldīt informāciju par kontaktpersonu.                                 | Kreditori var uzturēt sava uzņēmuma kontaktpersonas informāciju. Šī informācija ietver vārdus, e-pasta adreses un tālruņu numurus. Piekļuve šai funkcijai tiek nodrošināta ar īpašu drošības lomu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Koplietojiet dokumentus, kas ir saistīti ar kreditoru pirkšanas pasūtījumiem.                    | Kad nepieciešams koplietot dokumentu ar kreditoru, piemēram dokumentu par prasībām, ir ērti saistīt dokumentu ar atbilstošo pirkšanas pasūtījumu. Kreditors var koplietot piezīmes un pielikumus ar klientu, saistot dokumentu ar viņa vai viņas atbildi uz pirkšanas pasūtījumu. Dokumentu pārvaldība ir pakārtota atbalsta struktūra, un tikai piezīmes un pielikumi, kas tiek klasificēti kā "ārēji" var tikt koplietot ar kreditoriem.                                                                                                                                                                                                                                                                                                                              |
| Jaunu kreditora lietotāju nodrošināšana.                                                          | Ja jūsu kreditori izmanto kreditoru sadarbības interfeisu, viņiem ir ērts veids, kā pieprasīt jaunus lietotāju kontus, kad jaunām kontaktpersonām nepieciešama piekļuve kreditoru sadarbības interfeisam. Sagādes profesionāļi var iesniegt pieprasījumu lietotāja kontam kontaktpersonai kreditora organizācijā. Kreditora kontaktpersona, kura jau ir kreditoru sadarbības lietotājs, var arī iesniegt šo pieprasījuma veidu. Šis pieprasījums galu galā izveido jaunu lietotāju sistēmā Dynamics 365 for Operations, ar kreditoram noteiktām drošības lomām. Tas atvieglo arī pieprasījumu portālam Microsoft Azure B2B, sniegt lietotājam jaunu Azure Active Directory (Azure AD) lietotāja kontu. Kreditori var pieprasīt arī deaktivizēt noteiktus kreditoru interfeisa lietotāju kontus, vai mainīt to drošības lomas. |
| Uzziniet vairāk par kreditoru sadarbību sistēmā Dynamics 365 for Operations. | Plašāku informāciju par kreditoru sadarbību skatiet [Kreditoru sadarbība ar ārējiem kreditoriem](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Kreditoru sadarbība ar debitoriem](../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Pārvaldīt kreditoru sadarbības lietotājus](../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Iestatīt un uzturēt kreditoru sadarbību](../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md), un [Kreditora sadarbības rēķinu izveides darbvieta](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).                                                         |

### <a name="intercompany-order-processing"></a>Starpuzņēmuma pasūtījumu apstrāde

<table>




<thead>
<tr class="header">
<th>Ko iespējams izdarīt</th>
<th>Kāpēc tas ir svarīgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nosaka tieši pārdošanas pasūtījuma rindās, no kurienes jāiegūst pieprasījums, un kā tas tiek iegūts. <strong>Piemērs.</strong> Izveidojiet pārdošanas pasūtījuma rindu un kā piegādes veidu norādiet tiešo piegādi. Primārais kreditors tiek pievienots pārdošanas pasūtījuma rindai kā resursu avota punkts.</td>
<td>Plūsma pasūtījuma iegūšanai, ir būtiski uzlabota. Tagad jūs varat noteikt tieši pārdošanas pasūtījuma rindās, no kurienes jāiegūst pieprasījums, un kā tas tiek iegūts. Jums vairs nav jāgaida, kamēr visas rindas tiek pievienotas pārdošanas pasūtījumam. Jaunas opcijas pārdošanas pasūtījuma rindās ļauj jums norādīt piegādes veidu, norādot kreditoru. Saistot kreditoru ar pārdošanas pasūtījuma rindām, tiek izveidotas pasūtījuma ķēdes piegādei no kreditora.
<ul>
<li>Kreditors var būt starpuzņēmuma kreditors, kas izmanto iekšējo pirkšanas pasūtījumu un pārdošanas pasūtījumu, vai ārējais kreditoru, kas izmanto ārējo pirkšanas pasūtījumu.</li>
<li>Piegādes veids var būt <strong>Tiešā piegāde</strong> vai <strong>Krājums</strong>. Piegādes veids <strong>Krājums</strong> norāda, ka kreditoram jānodrošina vietējo krājumu pirms to nosūtīt debitoram.</li>
</ul></td>
</tr>
<tr class="even">
<td>Izveidot pasūtījuma solījumu tieši no pārdošanas pasūtījuma rindām. <strong>Piemērs.</strong> Izveidojiet pārdošanas pasūtījuma rindu, kas tiek iegūta no starpuzņēmumu kreditora. Atstājiet rindu. Piegādes datumi tiek aprēķināti saskaņā ar pieejamību resursu plānošanas uzņēmumā.</td>
<td>Veidojot pārdošanas pasūtījuma rindas, kas izmanto jauno resursu plānošanas informāciju, piegādes datumi tiek aprēķināti saskaņā ar vadīklu <strong>Piegādes datums</strong>. Piemēram, ja ir atlasīts starpuzņēmumu kreditors, tiek aprēķināta pieejamība resursu plānošanas uzņēmumā. Šādā veidā pasūtījuma ķēdes tiek automātiski izveidotas kopā ar pārdošanas pasūtījuma rindām. Šī funkcionalitāte palīdz garantēt, ka piegādes datumi kļūst redzami resursu plānošanas uzņēmumā, tādējādi pieejamie solīšanai (ATP) profili var apstrādāt paredzamās prasības uzreiz pēc pārdošanas pasūtījumu izveides.</td>
</tr>
<tr class="odd">
<td>Pārskatiet preču pieejamību visās izcelsmes vietās, un atlasiet labāko resursu izcelsmes opciju.</td>
<td>Lapa <strong>Piegādes alternatīvas</strong> ir pārveidota, un tagad sniedz noderīgu informāciju par visiem apstiprinātajiem iekšējiem un ārējiem kreditoriem. Šī informācija satur izcelsmes opcijas kreditora sagādei. Atlasot piegādes veidu, sistēma aprēķina iespējamos piegādes datumus. Jūs varat efektīvi atlasīt labāko opciju debitoram, un pielietot šo opciju katrai pārdošanas pasūtījuma rindai.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Noliktavas uzlabojumi lielapjoma sadales centriem

| Ko iespējams izdarīt                                                              | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Izveidot darbu, pēc tam, kad preces ir iepakotas iepakošanas stacijā.               | Šī funkcija ir noderīga, ja pēc manuāla iepakošanas darba (piemēram, paletizācija, kvalitātes pārbaude, sūtījumu konsolidēšana, vai izmaiņas iekraušanas dokos) ir papildu procesi. Jaunais darba veids **Iepakoto konteineru izdošana** ļauj jums modelēt šos uzdevumus, izmantojot atsevišķas darba rindas. Tagad jūs varat modelēt iepakošanas stacijas, lai ģenerētu darbu pēc iepakošanas. Šo darbu var izmantot, lai organizētu iepakoto krājumu kustību.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Grupēt konteinerus iepakošanas stacijā.                                     | Šī funkcija iespējo vairāku iepakojumu grupēšanu vienā konteinerā, vai noliktavas vienību iepakošanas stacijā. Piemēram, e-komercijas/vairumtirdzniecības operators var grupēt 100 atsevišķi iepakotus iepakojumus vienā konteinerā (piemēram paletes vai būris). Šo konteineru var pēc tam pārvietot, izvietot, vai iekraut, izmantojot vienu darba instrukciju, ko darbinieks paveic, skenējot vienu grupētā konteinera svītrkodu (numura zīmi). Šis līdzeklis samazina daudzu mazāku iepakoto konteineru pārvietošanas darbības. Papildinformāciju skatiet rakstā [Mobilās ierīces izvēlnes vienuma izveide noliktavas vienību konsolidācijai (uzdevuma ceļvedis)](../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md).                                                                                                                                                                                                                                                                                                                                                                                            |
| Izveidot iepakoto konteineru izlaišanas politiku.                               | Konteinera izlaišanas izraisīto darbu var izveidot automātiski vai manuāli. Kad tas notiek automātiski, darbs tiek ģenerēts pie konteinera slēgšanas, izmantojot atrašanās vietas direktīvu un darba veidnes struktūru. Kad izlaišana notiek manuāli, iepakotājs var izlemt, vai darbs ir jāģenerē vienam konteineram vai konteineru grupai. Šis līdzeklis samazina risku, kas slēgti konteineri tiks izdoti un pārvietoti pirms viņi ir gatavi pārvietošanai no iepakošanas stacijas. Tas ļauj arī ne sistematizētu grupētu izlaišanu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Saīsinātas izdošanas atkārtota piešķiršana                                                   | Ir pievienots atbalsts saīsinātas izdošanas procesiem, lai palīdzētu darbiniekam, kurš nevar izdot preces un vēlas izpildīt pasūtījumu, kad nepieciešamais krājums ir pieejams citā atrašanās vietā. Jūs varat izmantot automātisku atkārtota sadalījuma procesu, kurā tiek izmantotas atrašanās vietas direktīvas, lai izgūtu preces, ja tās ir pieejamas citā atrašanās vietā. Alternatīvi, izmantojot manuālu atkārtotu piešķiršanu, mobilā ierīce parāda atrašanās vietu sarakstu kopā ar pieejamo daudzumu. Noliktavas darbinieks pēc tam var atlasīt, kuras atrašanās vietas krājumu izmantot. Šīs divas metodes var iestatīt atsevišķi vai kombinēti vienā komandā, izvēlnē noliktavas darbinieks. Lietojot manuālu atkārtotu piešķiršanu, noliktavas darbinieks var izdot saīsinātu izdotā krājuma daudzumu no vairākām vietām. Papildinformāciju skatiet tēmā [Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana (uzdevuma ceļvedis)](../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md).                                                                                                                                                                                          |
| Pārvietot krājumu, kuram ir saistīts darbs.                             | Tagad jūs varat pārvietot krājumu, kuram ir saistīts darbs. Šis līdzeklis noder, piemēram, ja darbinieks vēlas atbrīvot iekraušanas doka vietu, un pārvietot reģistrētas paletes, kas gaida izvietošanu uz citu saņemšanas vietu. Doks tiek atbrīvots, un var saņemt papildu preču slodzi, un pārvietotais krājums tiek atjaunināts ar jauno izvietošanas informāciju. Šo līdzekli var izmantot arī, lai atbrīvotu vietu izdošanas vietās, pārvietojot krājumu, ar kuru ir saistīts darbs, atbrīvojot vietu papildināšanai. Jūs varat arī izmantot to, lai pārvietotu kravas no vienas sagatavošanas vietas uz citu, nezaudējot iekraušanas darbu, kas tika izveidots. Tādējādi, šis līdzeklis var palīdzēt optimizēt laiku, kas ir nepieciešams, lai iekrautu kravas automašīnas. Jūs varat pārvietot krājumu, kas ir rezervēts pārdošanas pasūtījumiem, pārsūtīt pasūtījumu izejas plūsmas, pārsūtīt pasūtījumu ieejas plūsmas un pirkšanas pasūtījumus. Pārvietošana tiks atspējota, ja tas izraisīs rindu sadalīšanos. Piemēram, ja jums ir darba rinda ar 100 krājumiem, jūs nevarat pārvietot tikai 30 no šiem krājumiem uz citu vietu. |
| Sapludināt noliktavas vienības, ar kurām ir saistīts darbs.                    | Jūs varat sapludināt noliktavas vienības, ar kurām ir saistīts izejošs darbs. Piemēram, ja izdošanu jāsadala vairākos darbos, varētu būt noderīgi atļaut sapludināt noliktavas vienības pēc tam, kad tās tiek piegādātas sagatavošanas vietā. Noliktavas vienības var konsolidēt tikai tad, ja tās ir vienā un tajā pašā vietā, ar vienādu slodzi, un to pašu piegādes informāciju.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Apturēt izdošanas darbu, kas ir saistīts ar papildināšanu rindas līmenī. | Tagad jūs varat apturēt darbu rindas līmenī, nevis galvenes līmenī, lai darbinieki varētu izpildīt izdošanas rindas, kas nav apturētas pieprasījuma papildināšanai. Tādējādi, vairumtirgotājam, kuram ir apjomīgi pārdošanas pasūtījumi, vai mazumtirgotājam, kuram ir apjomīgi pārdošanas pasūtījumi vai papildināšanas pārsūtīšanas pasūtījumi, var atļaut izdošanas darbu sākt visās rindās, kas nav pakļautas papildināšanas darbam. Izdošanas un papildināšanas darbu var pabeigt paralēli. Šo līdzekli var konfigurēt, lai jūs varētu atlasīt - apturēt galvenes līmenī vai rindas līmenī. Jūs varat arī izmantot abas metodes un izveidot darba veidni katrai metodei. Galvenes/rindas konfigurācija tiek iestatīta darba veidnēs, bet jūs to varat mainīt tieši izveidotajā darbā.                                                                                                                                                                                                                                                                                                                                                                      |
| Atcelt darbu, izmantojot mobilo ierīci.                                      | Tagad jūs varat atcelt darbu, izmantojot mobilo ierīci, ar vai bez pieprasījuma papildināšanai. Iepriekš bija jāizmanto bagātu klientu. Lai iespējotu šo funkcionalitāti, izveidojiet mobilās ierīces izvēlnes vienumu, ar režīmu, iestatītu uz **Netiešs** un aktivitātes kodu, iestatītu uz **Atcelt darbu**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

### <a name="warehouse-operation-enhancements"></a>Noliktavas operāciju uzlabojumi

| Ko iespējams izdarīt                    | Kāpēc tas ir svarīgi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modelēt dažādus konteineru veidus.   | Jūs varat izmantot dažādus konteineru veidus noliktavā, lai optimizētu uzglabāšanu un citu iemeslu dēļ. Jaunajam elementam Konteinera veids ir konteinera veidu fiziskie raksturlielumi. Tagad jūs varat saistīt noliktavas vienības ar noteiktu konteinera veidu, un izmantot novietojuma dimensijas ierobežojumus. Piemēram, šo funkciju varat izmantot, lai kontrolētu, cik paletes (vai citu konteineru veidu) tiek atļautas noteiktā vietā. Konteineru veidi tika pievienoti arī vienību secību grupām, lai pievienotu noklusējuma konteineru veidus saņemšanas procesam. Konteineru veidi var tikt lietoti kopā ar ienākošajām un izejošajām novietojuma direktīvām. Tās var izmantot arī rīcībā esošo krājumu skatā, lai noteiktu, cik daudz konteineru veidu pašlaik tiek uzglabāts. Papildinformācijai skatiet emuāra ziņu [Ar konteinera tipu saistītu noliktavas vienību lietošana, lai vadītu noliktavas vadības procesus](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Lai gan šī emuāra ziņa apraksta Microsoft Dynamics AX 2012 atjauninājumu, tas pats atbalsts tagad tika pievienots Dynamics 365 for Operations.                                                                                                                                                                                                                                                                                                                         |
| Atsaukt sūtījumus.                 | Noliktavā jums ir jābūt iespējai apstrādāt kavētas izmaiņas. Piemēram, dažas preces var būt bojātas, tāpēc jūs nevarat tās nosūtīt. Vai arī klients varētu veikt vēlu pieprasījums atcelt vai mainīt pasūtījumu. Dynamics 365 for Operations tagad ļauj jums atsaukt sūtījumu. Tādējādi jūs varat atcelt pavadzīmi, lai vēlāk to varētu atjaunināt ar pareiziem daudzumiem. Līdzīgi, saņemšanas plūsmā var atcelt produktu ieejas plūsmu, lai varētu izveidot atjauninātu versiju.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Izmantojiet paletes ar jauktiem krājumiem. | Tagad jūs var saņemt un reģistrēt "jauktas" paletes. Jaukta palete sastāv no dažādiem krājumiem, kas tiek apvienoti uz vienas paletes vienam vai vairākiem pirkšanas pasūtījumiem vai rindām. Visas reģistrācijas var apkopot vienā noliktavas vienībā. Šis process tiek iespējots, izmantojot noliktavas mobilo ierīci. Piemēram, ja jauktu krājumu palete tiek piegādāta noliktavā, saņemšanas darbinieks identificē krājumus un daudzums uz paletes pirms palete tiek pārvietota uz specializētu izvietošanas vietu. Izvietošanas vietas tiek identificētas saskaņā ar darba veidnēm un novietojuma direktīvām. Ja izvietošanas vietas ir sadalītas vairākiem krājumiem, ar fiksētām vietām, šī funkcija izveido tik daudz izvietošanas darba rindu, cik dažādu krājumu ir uz jauktās paletes. Šī funkcija padara saņemto jaukto krājumu paletes reģistrāciju un izvietošanu ātrāku un elastīgāku. Papildinformācijai skatiet emuāra ziņu [Saņemt un reģistrēt paleti ar jauktām pirmdokumenta rindām, izmantojot 1 noliktavas vienību — pirkšanas pasūtījuma atbilstības noteikšana](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) un informācija par jauktu palešu atbalstu [paziņojumā par mūsu neseno kumulatīvo atjauninājumu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Lai gan šī emuāra ziņa apraksta AX 2012 atjauninājumu, tas pats atbalsts tagad tika pievienots Dynamics 365 for Operations. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Papildu funkciju uzlabojumi Piegādes ķēdes pārvaldībā

<table>




<thead>
<tr class="header">
<th>Ko iespējams izdarīt</th>
<th>Kāpēc tas ir svarīgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izmantojiet jaunos datu elementus, lai importētu un eksportētu datus.</td>
<td>Jūs varat importēt un eksportēt datus, izmantojot šādus datu elementus:
<ul>
<li>Kravas rēķins</li>
<li>Apkopotie esošie krājumi pēc noliktavas un krājumu statusa</li>
<li>Krājumu maksas</li>
<li>Piedāvājums</li>
</ul></td>
</tr>
<tr class="even">
<td>Izmantojiet uzlaboto Gantt kontroli, lai izstrādātu interaktīvus plānošanas scenārijus.</td>
<td>Uzlabotā Gantt kontrole ļauj izstrādāt jaunus interaktīvus plānošanas scenārijus, un sniegt uzlabotu API, ko var izmantot, lai pielāgotu darbību izskatu. Daži no jaunajiem API:
<ul>
<li>Vertikāla darbību vilkšana un nomešana</li>
<li>Darbību pievienošana/noņemšana</li>
<li>Grāmatoto periodu priekšskatīšana kopsavilkuma joslā</li>
<li>Aktivitātes robežu krāsas un stila maiņa</li>
<li>Teksta krāsas, stila un fona maiņa režģī</li>
</ul></td>
</tr>
<tr class="odd">
<td>Labāka materiālu apstrāde un resursu plānošana.</td>
<td>Daži uzlabojumi ir veikti materiālu un resursu plānošanā:
<ul>
<li>Izejas plūsmas rezerve tagad tiek apstrādāta, kad krājums ir rīcībā esošs.</li>
<li>Piegādes datums tiek pārrakstīts, apstiprinot plānotos pasūtījumus.</li>
<li>Pasūtījumu izpildīšanas prioritāte pār drošības rezervi.</li>
<li>Plānoto pasūtījumu plānošanas pagātnē novēršana.</li>
</ul></td>
</tr>
<tr class="even">
<td>Ziņot par faktisko patēriņu ražošanai, un skatīt krājuma statusu.</td>
<td>Jūs varat skatīt faktisko ražošanas patēriņu. Turklāt, jauna izvēles rūtiņa <strong>Rādīt krājumu statusu</strong>, kas tika pievienota izvēlnes elementam <strong>Kustība</strong> sadaļā <strong>Darba izveide</strong> ļauj apskatīt krājuma statusu.</td>
</tr>
<tr class="odd">
<td>Aprēķināt tilpuma svaru, ja sūtījuma pārvadātāja likmes ir balstītas uz tilpuma svaru.</td>
<td>Tika pievienota jauna TMS likmes noteikšanas programma, kas ir balstīta uz tilpuma svaru, lai jūs varētu aprēķināt tilpuma svaru.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Skatiet arī
--------

[Jaunumi un izmaiņas](whats-new-changed.md)




