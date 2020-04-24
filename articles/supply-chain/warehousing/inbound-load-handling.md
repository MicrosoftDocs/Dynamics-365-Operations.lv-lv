---
title: Noliktavas apstrādes process ienākošajām slodzēm pirkšanas pasūtījumiem
description: Šī tēma apraksta noliktavas apstrādes procesu ienākošajām slodzēm pirkšanas pasūtījumiem.
author: omulvad
manager: AnnBe
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 709a75a259b1f8daa5b72e76b56942573c403f43
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261352"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Noliktavas apstrādes process ienākošajām slodzēm pirkšanas pasūtījumiem

Šī tēma apraksta noliktavas apstrādes procesu ienākošajām slodzēm pirkšanas pasūtījumiem.

Katrai saņemšanas noslodzei jūsu sistēmai jau ir jāiekļauj saistītais pārdošanas pasūtījums, un tas var ietvert arī saistīto noslodzes specifikāciju un/vai transportēšanas plānu. Lai iegūtu vairāk informācijas par to, kā izveidot un pārvaldīt ienākošo kravu, skatiet [Biznesa process: transportēšanas plānošana ienākošajām slodzēm](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Pārskats: kā ienākošās slodzes tiek veidotas, reģistrētas un saņemtas

Sekojošajā attēlā redzama parastā plūsma ienākošo slodžu apstrādei, kurām ir pirkšanas pasūtījuma daudzumi, kad tie ierodas noliktavā.

![Ienākošo noslodžu apstrādes process](media/inbound-process.png "Ienākošo noslodžu apstrādes process")

1. **Kreditors apstiprina pirkšanas pasūtījumu.**

    Process sākas, kad sistēmā tiek ievadīts pirkšanas pasūtījums un pēc tam piegādāts kreditoram, kas apstiprina pasūtījumu. Lai varētu izveidot ienākošās slodzes ierakstu, pirms tam ir jāpastāv pirkšanas pasūtījumam. Tomēr saņemšanas noslodzi var izveidot pat tad, ja pasūtījums nav apstiprināts. Papildinformāciju skatiet [Pirkšanas pasūtījumu apstiprināšana](../procurement/purchase-order-approval-confirmation.md).

1. **Ienākošās noslodzes ieraksts tiek izveidots, lai plānotu ierašanos un tā saturu.**

    Saņemšanas noslodzes ieraksts parāda kreditora sūtījumu vienam vai vairākiem pirkšanas pasūtījumiem. Paredzams, ka noslodze nokļūs noliktavā kā viena fiziska transportēšanas vienība (piemēram, kravas automašīnas). Saņemšanas noslodzes ieraksts tiek izmantots plānošanas nolūkiem un ļauj loģistikas koordinatoram izsekot kravas virzību no kreditora. Tas tiek izmantots arī, lai reģistrētu pasūtījumu rindu daudzumus un pārvaldītu norisi, izmantojot noliktavas operācijas, piemēram, saņemšanas un izvietošanas darbu. Noslodzes var izveidot automātiski vai manuāli, un tās var būt pamatotas vai nu uz pirkšanas pasūtījuma, vai arī no kreditora papildu sūtījuma paziņojuma (ASN). Papildinformāciju skatiet [Ienākošās noslodzes izveide vai modificēšana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Kreditors apstiprina noslodzes nosūtīšanu.**

    Kad kreditors nosūta noslodzi, loģistikas koordinators saņemšanas noliktavā apstiprina noslodzes nosūtīšanu. Ja saņemšanas uzņēmums izmanto **Transportēšanas pārvaldības** moduli, saņemšanas sūtījuma apstiprināšana izraisīs citus noslodzes pārvaldības procesus, kas ir saistīti ar ienākošajām noslodzēm. Papildinformācijai skatiet [Noslodzes apstiprināšana nosūtīšanai](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Noslodze pienāk noliktavā, un darbinieki reģistrē daudzumus.**

    Kad kravas automašīna ierodas noliktavas saņemšanas dokā, noliktavas darbinieki reģistrē noslodzes daudzumus. Kad tiek izmantots **Noliktavas pārvaldības** modulis, darbinieki veic reģistrāciju, izmantojot mobilās ierīces. Lai iegūtu papildinformāciju, skatiet sadaļu [Preču saņemšana no pirkšanas pasūtījumiem - reģistrācija](../procurement/product-receipt-against-purchase-orders.md#registration) un [Reģistrēt krājumu daudzumus, kas tiek saņemti uz ienākošo noslodzi](#register-item-quantities-arriving).

1. **Reģistrētie noslodzes daudzumi tiek grāmatoti attiecībā pret pirkšanas pasūtījumiem.**

    Kad noslodzes daudzumi ir reģistrēti, tie ir kolīdz saņemti, šiem daudzumiem jābūt iegrāmatotiem uzņēmuma krājumu virsgrāmatā, lai reģistrētu fizisko krājumu pieaugumu. Lai iegūtu papildinformāciju, skatiet [Preču saņemšana no pirkšanas pasūtījumiem - preču saņemšana](../procurement/product-receipt-against-purchase-orders.md#product-receipt) — [Grāmatot reģistrētos produktu daudzumus pirkšanas pasūtījumos](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Reģistrēt krājuma daudzumus, kas tiek saņemti ienākošajā noslodzē

Microsoft Dynamics 365 Supply Chain Management atbalsta vairākas darbības pieejas, lai reģistrētu pasūtāmo preču saņemšanu. Tāpēc sistēmu var konfigurēt, lai tā atbilstu jūsu konkrētajām biznesa prasībām. Šajā sadaļā ir aprakstīts, kā reģistrēt ienākošos krājumu daudzumus, izmantojot mobilo ierīci, kad sistēmā ir ieslēgta uzlabota noliktavas pārvaldība. Tomēr ir alternatīva plūsma, kas ir balstīta uz krājumu saņemšanas žurnāla, nevis mobilās ierīces izmantošanu. Papildinformāciju par šo plūsmu skatiet [Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu](tasks/register-items-advanced-warehousing.md).

Kad noliktavā vispirms ierodas ienākošā noslodze, noliktavas darbiniekiem ir jāreģistrē sūtījumā iekļautie krājumu daudzumi. Parasti tie izmanto roku skenerus. Šī darbplūsma ir pieejama tikai tad, ja sistēmā ir šādi krājumi:

- **Ienākošās noslodzes ieraksts, kas apraksta sūtījumā paredzētos krājumu daudzumus**

    Parasti kreditors apstiprina ienākošo noslodzes ierakstu, pirms sūtījums ierodas noliktavā. Tāpēc noslodzei ir statuss _Piegādāts_. Tomēr noliktavas darbinieki var arī reģistrēt krājumu daudzumus noslodzēm, kuru statuss ir _Atvērts_ vai _Saņemts_.

- **Mobilās ierīces izvēlne, kas ir konfigurēta, lai atbalstītu noslodzes saņemšanu**

    [Dynamics 365 for Finance and Operations— Warehousing app](install-configure-warehousing-app.md) mobilajām ierīcēm atbalsta šādus darba izveides procesus:

    - Kravas krājuma saņemšana
    - Kravas krājuma saņemšana un izvietošana
    - Jaukta numura zīmes saņemšana, kur **Pirmdokumenta rindas identifikācijas metodes**  lauks mobilo ierīču izvēlnes krājums ir iestatīts uz _Ielādēt krājuma saņemšanu_. Lai iegūtu papildinformāciju, skatiet [Jaukta numura zīmes saņemšana](mixed-license-plate-receiving.md).
    - Jaukta numura zīmes saņemšana un novietošana, kur **Pirmdokumenta rindas identifikācijas metodes**  lauks mobilo ierīču izvēlnes krājums ir iestatīts uz _Ielādēt krājuma saņemšanu_. Lai iegūtu papildinformāciju, skatiet [Jaukta numura zīmes saņemšana](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Neatkarīgi no procesa sistēma ģenerēs darbu, lai uzņemtu daudzumus, kas ir reģistrēti saņemšanas vietā un novietotu tos parastajā glabāšanas vietā. Kad tiek izmantots _Ielādēt vienumu saņemšanu un novietošanu_ vai _Jauktās numura zīmes saņemšanas un novietošanas_ process, ierīce norīkos arī darbinieku, kurš reģistrējis noslodzes daudzumu, veikt izvietošanas darbu kā daļu no reģistrācijas uzdevuma. Turpretī _Ielādēt krājuma saņemšanu_ un _Jauktās numura zīmes saņemšanas_ procesiem tiek pieņemts, ka izvietošanas darbs tiks veikts atsevišķi no reģistrācijas uzdevuma.

- **Darba veidne, kas definē ienākošo kravu savākšanu un izvietošanu**

    Šis krājums ir saistīts ar iepriekšējiem krājumiem. Ir jābūt vismaz vienai darba veidnei _Pirkšanas pasūtījums_ darba pasūtījuma veidam, un tai ir jāietver savākšanas/izvietošanas darba veida kopa.

Mobilā ierīce palīdz reģistrēt noliktavas saņemšanas ierēdni, izmantojot plūsmu noslodzes daudzuma reģistrācijai. Šajā plūsmā ir iekļautas vismaz šādas darbības katram noslodzes ID:

1. Ievadiet noslodzes ID.
2. Ievadiet krājuma kodu saņemtajam krājumam.
3. Ievadiet saņemtā krājuma koda daudzumu.
4. Ievadiet krājuma unikālo noliktavas vienības identifikatoru krājuma sākotnējai atrašanās vietai, ja sistēma nav iestatīta šī identifikatora automātiskai ģenerēšanai.
5. Nospiediet **Labi**.

Pēc tam, kad darbinieks pabeidz šos soļus, sistēma veic tālāk norādītos atjauninājumus atbilstošajās entītijās ar nosacījumu, ka pirkšanas pasūtījuma rindas daudzums, kas saņemts vienā noslodzē un visi noslodzes daudzumi ir reģistrēti:

| Elements | Grāmatojumi | Piezīme |
|---|---|---|
| Ielādēt | **Darba izveidotā daudzuma** lauks noslodzes rindā tiek atjaunināts, lai parādītu reģistrēto daudzumu. | **Noslodzes statusa** vērtība paliek _Piegādāts_ vai _Atvērta_, ja noslodzei nav palaists neviens sūtījuma apstiprinājums. Ja vismaz viena no izvietošanas darba rindām ir sākta, tā tiek mainīta uz _Darbībā_. |
| Pirkšanas pasūtījuma krājumu transakcija, kurai ir reģistrēti saistītie noslodzes daudzumi |<p>Tiek atjaunināti šādi lauki:</p><ul><li>Lauks <b>Saņemšana</b> ir iestatīts uz <i>Reģistrēti</i>.</li><li><b>Atrašanās vietas</b> lauks tiek atjaunināts ar saņemšanas doka atrašanās vietas kodu. (Šis kods ir norādīts katras noliktavas laukā<b>Noklusējuma saņemšanas vieta</b>.)</li><li><b>Numura zīmes</b> lauks ir atjaunināts ar unikālu noliktavas vienības identifikatoru, kas tika ievadīts vai ģenerēts reģistrācijas laikā.</li><li><b>Noslodzes ID</b> lauks tiek atjaunināts ar noslodzes numuru, pret kuru ir reģistrēts šis daudzums. (Skatiet piezīmi.)</li></ul> | Spēja saistīt pirkšanas pasūtījuma krājumu transakciju un daudzumus, kas ir reģistrēti pret noslodzi, tika ieviesti versijā 10.0.9 kā izvēles līdzeklis ar nosaukumu _Pirkšanas pasūtījuma krājumu transakcijas saistīšana ar noslodzi_. Šis līdzeklis ir īpaši izdevīgs operāciju plūsmām, kur viens iegādāto preču pasūtījums tiek piegādāts kā vairākas noslodzes, vai arī kad noslodze satur vairāku pirkšanas pasūtījumu daudzumus. |
| Noliktavas izvietošana | Darbs ir izveidots, pamatojoties uz darba veidni, lai uzdotu darbiniekam pārvietot reģistrētos daudzumus no saņemšanas vietas uz parasto glabāšanas vietu. | Glabāšanas vietas izvēli kontrolē izvietošanas novietojuma direktīva. Ja nav definēta neviena novietojuma direktīva, darbu izvietošanas vieta ir tukša. |

Ņemiet vērā, ka noliktavas darbinieki var reģistrēt pirkšanas pasūtījuma saņemšanu ar vienu vai vairākām saistītajām noslodzēm, neizmantojot _Noslodzes krājuma saņemšanas_ procesu. Pieejamas šādas metodes.

- **Mobilajā ierīcē:** izmantojiet _Pirkšanas pasūtījuma rindas saņemšanas_ un _Pirkšanas pasūtījuma rindas saņemšanas un izvietošanas_ procesus. (Ja pirkšanas pasūtījuma rindas daudzumam pastāv vairāk nekā viena noslodze, darbinieks nevar izmantot _Pirkšanas pasūtījuma rindas saņemšanas_ procesu. Tā vietā darbiniekam tiks sniegti norādījumi izmantot ierīces darbību, kas saistīta ar _Noslodzes krājuma saņemšanas_ procesu.)
- **Klientam:** lietojiet krājumu saņemšanas žurnālu.
- **Klientam:** izmantojiet **Reģistrācijas** darbību, kurai var piekļūt no pirkšanas pasūtījuma rindas.

> [!NOTE]
> Ja pirkšanas pasūtījuma saņemšana tiek reģistrēta, izmantojot jebkuru no iepriekšējām metodēm, starp pirkšanas pasūtījuma krājumu transakciju un noslodzi netiek izveidota saite, pat ja ir ieslēgts _Pirkšanas pasūtījuma krājumu darbības saistīšana ar noslodzi_ līdzeklis. Viens izņēmums šai kārtulai ir, kad izmantojat **Pirkšanas pasūtījuma rindas saņemšanas** opciju, un tikai vienai noslodzei ir statuss, kas nav _Saņemts_ pasūtījuma rindai.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Apstrādāt neatbilstības ienākošo noslodzes daudzumu reģistrācijas laikā

Noliktavas darbinieki var reģistrēt daļēju noslodzes daudzuma saņemšanas reģistrāciju. Katra daļējās noslodzes daudzuma saņemšana izveido atsevišķu krājuma transakciju, kuras saņemšanas statuss ir _Reģistrēts_ reģistrētajam daudzumam, un laidiena ID attiecas uz sākotnējo pirkšanas pasūtījuma rindu.

#### <a name="load-under-receiving"></a>Noslodzes nepilnīga saņemšana

Kad pienāk noslodze, ja krājumu daudzumi ir mazāki par noslodzes ierakstā norādītajiem daudzumiem, noliktavas saņemšanas personāls var tieši strādāt ar klientu, lai apliecinātu šo neatbilstību, samazinot noslodzes rindas daudzumu, lai tas atbilstu faktiskajam ievestajam un reģistrētajam daudzumam.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Noslodzes pārslodze

Pārslodze notiek, kad pienāk noslodzes, un krājumu daudzums pārsniedz paredzamo noslodzes rindas daudzumu. Jūs varat kontrolēt, vai un cik lielā mērā pārslodze ir atļauta noslodzes reģistrācijas laikā.

Lai kontrolētu to, kas notiek, kad noliktavas darbinieks mēģina reģistrēt pārsniegšanu, lietojiet **Noslodzes pārslodzes saņemšana** lauku atbilstošajiem mobilās ierīces izvēlnes krājumiem. Šis lauks ir pieejams mobilās ierīces izvēlnes krājumiem, kuri izmanto šādus darba izveides procesu veidus:

- Kravas krājuma saņemšana
- Kravas krājuma saņemšana un izvietošana
- Jaukta numura zīmes saņemšana, (kad **Pirmdokumenta rindas identifikācijas metodes**  lauks ir iestatīts uz _Ielādēt krājuma saņemšanu_)
- Jaukta numura zīmes saņemšana un izvietošana, (kad **Pirmdokumenta rindas identifikācijas metodes**  lauks ir iestatīts uz _Ielādēt krājuma saņemšanu_)

Šī tabula sniedz pāskaidro pieejamās opcijas **Noslodzes pārslodzes saņemšanas** laukam.

| Vērtība | apraksts |
|---|---|
| Atļaut | Darbinieki var reģistrēt tādu daudzumu saņemšanu, kas pārsniedz atlikušo nereģistrēto daudzumu atlasītajai noslodzei, bet tikai tad, ja kopējais reģistrētais daudzums nepārsniedz pirkšanas pasūtījuma rindas daudzumu, kas ir saistīts ar noslodzi (pēc pārsniegšanas procenta korekcijas). |
| Bloķēts | <p>Darbinieki nevar reģistrēt daudzuma saņemšanu, kas ir lielāks par atlikušo nereģistrēto daudzumu atlasītajai noslodzei (pēc koriģēšanas, lai varētu veikt pārsniegšanu procentos). Darbinieks, kurš mēģina reģistrēt saņemšanu saņems kļūdu, un nevarēs turpināt, kamēr viņš vai viņa nereģistrēs daudzumu, kas ir vienāds ar vai mazāks par atlikušo nereģistrēto noslodzes daudzumu.</p><p>Pēc noklusējuma pārsniegšanas procentuālā vērtība noslodzes rindā tiek kopēta no saistītās pirkšanas pasūtījuma rindas. Kad lauks <b>Noslodze pārslodze</b> ir iestatīts uz <i>Bloķēts</i>, sistēma izmanto pārsniegšanas procentuālo vērtību, lai aprēķinātu kopējo daudzumu, ko var reģistrēt noslodzes rindai. Tomēr šo vērtību var pārrakstīt atsevišķām noslodzēm pēc nepieciešamības. Šī uzvedība kļūst aktuāla saņemšanas plūsmu laikā, kad daļa vai viss pārpalikums, kas atspoguļo pasūtījuma līnijas pārsnieguma procentu, tiek sadalīts neproporcionāli vairākām noslodzēm. Lūk, ir piemērs:</p><ul><li>Vienai pirkšanas pasūtījuma rindai ir vairākas noslodzes.</li><li>Pirkšanas pasūtījuma rindai ir pārsniegšanas procentuālais daudzums, kas ir lielāks par 0 (nulle).</li><li>Daudzumi jau ir reģistrēti attiecībā pret vienu vai vairākām noslodzēm, neņemot vērā pārsniegto daudzumu procentos kontā.</li><li>Pārsniegšanas daudzums pienāk pēdējā noslodzē.</li></ul><p>Šajā scenārijā var izmantot mobilo ierīci, lai reģistrētu pēdējās noslodzes pārsniegšanas daudzumu tikai tad, ja noliktavas uzraudgs palielina pārsniegšanas procentuālo vērtību attiecīgajai noslodzes rindai no noklusētās vērtības uz vērtību kas ir pietiekami liela, lai pilnīgu pārsniegšanu varētu reģistrēt ar galīgo noslodzi.</p> |
| Bloķēt tikai slēgtajām noslodzēm | Darbinieki var saņemt noslodzes līniju daudzumus par atvērtām noslodzēm bet ne par noslodzēm, kuru statuss ir _Saņemts_. |

> [!NOTE]
> **Noslodzes pārslodzes saņemšanas** lauka noklusējuma vērtība ir _Atļauts_. Kad tiek izmantota šī vērtība, uzvedība atbilst standarta rīcībai, kas bija pieejama, pirms tika piedāvāta _Noslodžu daudzumu pārslodzes saņemšanas_ funkcija, kas norādīta versijā 10.0.11.

### <a name="put-away-the-registered-quantities"></a>Izvietot reģistrētos daudzumus

Kad reģistrācija ir pabeigta, mobilajā ierīcē, _Daudzuma saņemšanas reģistrācijas_ darbība atjaunina krājumu un noliktavas ierakstus, lai norādītu, ka daudzumi tagad ir saņemšanas doka vietā un ir pieejami rezervēšanai. Tomēr uzņēmuma noliktavas darbības parasti prasa, lai daudzums tiktu pārvietots no saņemšanas doka uz parasto noliktavas krātuvi, lai varētu notikt sekojošie savākšanas procesi. Instrukcijas par izvietošanu tiek apkopotas izvietošanas darbā, kas tiek automātiski ģenerēts, kad ienākošā noslodze tiek reģistrēta kā saņemta.

Kad noliktavas darbinieks ir pabeidzis izvietošanas darbu, sistēma reģistrē un seko rezultātam, atjauninot vairākus elementus, kā apkopots tabulā.

| Elements | Grāmatojumi | Piezīme |
|---|---|---|
| Ielādēt | <p>Tiek atjaunināti šādi lauki:</p><ul><li><b>Noslodzes statusa</b> vērtība tiek mainīta uz <i>Procesā</i>.</li><li><b>Darba statusa</b> vērtība ir nomainīta uz <i>100.00% no pabeigtā darba</i>.</li></ul> | **Noslodzes statusa** vērtība tiek mainīta uz _Procesā_, kad darbinieks sāk izvietošanas uzdevumu vismaz vienai izvietošanas darba rindai. |
| Darba krājumu transakcijas, ar kurām saistītie daudzumi ir izvietoti | **Saņemšanas** un **Atrašanās vietas** lauki un citi atbilstošie lauki tiek atjaunināti, lai atspoguļotu pārvietošanu no saņemšanas vietas uz glabāšanas vietu. | Pirkšanas pasūtījuma krājumu transakcijas **saņemšanas stāvoklis** paliek _Reģistrēts_. |
| Noliktavas izvietošana | **Darba statusa** vērtība ir mainīta uz _Slēgts_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Nosūtīt reģistrētos preču daudzumus pret pirkuma pasūtījumiem

Kad sistēmā tiek reģistrēti ienākošo preču daudzumi, tie kļūst pieejami rezervācijām saistībā ar pārdošanu un citām izejošām un iekšējām darbībām. Tomēr sistēma vēl nav atjauninājusi krājumu (pagaidu) kontus. Šis atjauninājums var notikt tikai tad, ja operāciju grupa iegrāmato reģistrētās preču saņemšanas.

Lai atvērtu lapu, kurā var grāmatot preču saņemšanu, operāciju grupas dalībnieki var veikt _jebkuru_no šīm darbībām:

- Atveriet atbilstošo noslodzes ierakstu un pēc tam atlasiet **Preču saņemšanas** darbību.
- Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Atjaunināt preču saņemšanas** un pēc tam laukā **Noslodzes ID** norādiet noslodzi grāmatošanai.
- Atveriet atbilstošo pirkšanas pasūtījumu un pēc tam atlasiet **Preču saņemšanas** darbību.
- Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Preču saņemšana \> Preču saņemšanas darba nosūtīšana**.

**Preču saņemšanas** darbība, kas ir pieejama lapā **Noslodze** (un līdzvērtīgajā lapā atjaunināšanas darbam, **Atjaunināt preču saņemšanas** lapa), var atjaunināt preču saņemšanas daudzumus tikai pirkšanas pasūtījuma daudzumos, kuru statuss ir _Reģistrēts_. Tomēr **Preču saņemšanas** darbība, kas ir pieejama **Pirkšanas pasūtījuma** lapā, var ietvert daudzumus abos apstrādes statusos (_Pasūtīts_ un _Reģistrēts_). Tas var arī kontrolēt preču saņemšanas grāmatošanas apjomu, izmantojot papildu parametrus, piemēram, _Saņemt daudzumu tagad_ un _Reģistrētie daudzumi un pakalpojumi_.

Preču saņemšana var tikt grāmatota tikai pasūtījumiem, kuru statuss ir _Apstiprināts_. Neapstiprinātiem pirkšanas pasūtījumiem, **Preču saņemšanas** darbība parādīsies kā nav pieejama.

### <a name="post-registered-quantities-from-the-load-page"></a>Grāmatot reģistrēto daudzumu no noslodzes lapas

Lai saņemtu preču un nosūtītu reģistrētos daudzumus no **Noslodzes** lapas, ir jābūt šādiem priekšnoteikumiem:

- Noslodzei ir jābūt vismaz vienai daudzuma vienībai ar statusu _Reģistrēts_.
- Noslodzes statusam ir jābūt _Nosūtīts_.
- Pirkšanas pasūtījumam, kas ir saistīts ar noslodzi, ir jābūt statusam _Apstiprināts_.

> [!NOTE]
> Ja noslodzes statuss nav iestatīts kā _Piegādāts_, sistēma automātiski apstiprinās noslodzi, pirms tā palaiž preču saņemšanas atjauninājumu. (Noslodzes statuss tiek iestatīts uz _Piegādāts_, kad lietotājs reģistrē noslodzes saņemšanas sūtījumu.)

Lai saņemtu preču un nosūtītu saņemšanas reģistrāciju, kas saistīta ar izvēlēto noslodzi, darbinieks atlasa **Preču saņemšanas** darbību lapā **Noslodze**. Atvērtajai lapai ir šādas galvenās detaļas:

- **Daudzuma** lauks sadaļā **Parametri** cilnē **Iestatījumi** rāda _reģistrēto daudzumu_. Šeit nav pieejamas citas opcijas.
- Režģis kopsavilkuma cilnē **Pārskats** uzskaita visus pirkšanas pasūtījumus, kas iekļauti atlasītajā noslodzē.
- Režģis kopsavilkuma cilnē **Rindas** uzskaita visas pasūtījuma rindas, kurām ir reģistrēts daudzums.

> [!NOTE]
> Daudzumi pasūtījuma rindām, kas tiek rādītas cilnē **Rinda**, tiek aprēķināti atšķirīgi atkarībā no tā, vai ir ir pieejams līdzeklis _Atļaut vairākas preču saņemšanas uz noslodzi_ un ir ieslēgts jūsu Supply Chain Management versijā.
>
> | Versija | Aprēķins |
> |---|---|
> | Versijas pirms 10.0.10 versijas un jaunākas, kur _Atļaut vairākas preču saņemšanas uz noslodzi_ līdzeklis nav ieslēgts | Rindas daudzums ir visu reģistrēto daudzumu kopsumma _šai pirkšanas pasūtījuma rindai_ neatkarīgi no tā, vai reģistrācija tika veikta pa vairākām noslodzēm, neatkarīgi no noslodzes, mobilās ierīces vai klienta. |
> | Versija 10.0.10 jaunākas, kur _Atļaut vairākas preču saņemšanas uz noslodzi_ līdzeklis ir ieslēgts | Rindas daudzums ir visu reģistrēto daudzumu kopsumma _noslodzes ierakstam_, no kura **Preču saņemšanas grāmatošanas** darbība tika uzsākta. |

Kad lietotājs atlasa **Labi**, lai apstiprinātu preču saņemšanas grāmatošanu, sistēmai ir šādi galvenie atjauninājumi uz atbilstošiem elementiem.

| Elements | Grāmatojumi |
|---|---|
| Pirkšanas pasūtījuma krājuma transakcija, kurai ir iekļauti rindas daudzumi grāmatošanas jomā | <p>Tiek atjaunināti šādi lauki (bet ņemiet vērā, ka ir arī vairāki citi atjauninājumi):</p><ul><li>Lauks <b>Saņemšana</b> ir iestatīts uz <i>Saņemts</i>.</li><li><b>Fiziskā datuma</b> lauks tiek atjaunināts ar grāmatošanas datumu.</li></ul> |
| Noslodze, no kuras lietotājs grāmatojis preču saņemšanu | Noslodzes atjauninājumi būs atkarīgi no izmantotās versijas, kā arī no **Atļaut vairākas preču saņemšanas uz noslodzi** lauka iestatījumiem. Kārtulas ir aprakstītas tabulā, kas parādītas tālāk šajā sadaļā. |

**Atļaut vairākas preču saņemšanas uz noslodzi** lauks ļauj uzņēmumiem izvēlēties ienākošo noslodžu saņemšanas politiku. Atkarībā no darbības plūsmām uzņēmumi var izvēlēties atļaut vai neatļaut vairākus preču saņemšanas grāmatojumus vienai un tai pašai noslodzei. Mēs iesakām, lai loģistikas vadītājs iestata **Atļaut vairākas preču saņemšanas uz noslodzi** lauku uz vienu no šīm vērtībām:

- **Nē** – atlasiet šo vērtību, ja noliktavas saņemšanas darbinieki vienmēr reģistrē visus pasūtījuma daudzumus, kas tiek saņemti ar katru noslodzi norādītajā laika periodā. Ja noslodzes daudzumi nav reģistrēti, sistēma pieņem, ka tie neatnāca, vai arī tie netika iekrauti, un tāpēc tos nedrīkst uzskatīt par noslodzes daļu. Preču saņemšanas grāmatošana, kas tiek palaista no noslodzes, izmanto to pašu pieņēmumu. Papildus preču saņemšanai, kurā tiek atjaunināti visi reģistrētie daudzumi (tā galvenā funkcija), tas pasludina noslodzi par pabeigtu un slēgtu papildu apstrādei. Šādā gadījumā visi noslodzes rindu daudzumi tiek automātiski atjaunināti uz reģistrētajiem daudzumiem, noslodzes rindas bez reģistrētajiem daudzumiem tiek dzēstas un noslodzes statuss tiek nomainīts uz _Saņemts_.
- **Jā** – atlasiet šo vērtību, ja noliktavas saņemšanas darbiniekiem nepieciešams vairāk laika, lai reģistrētu visus daudzumus noslodzei, kas pienākas, bet pa to laiku jums ir jāgrāmato jau reģistrētie daudzumi. Šādā gadījumā loģistikas vadītājs vēlas paturēt noslodzi atvērtu pat tad, kad ir palaists preču saņemšanas grāmatošanas darbs, lai atlikušos noslodzes daudzumus varētu reģistrēt un pastāvīgi atjaunināt preču saņemšanu virsgrāmatā.
- **Uzvedne** – atlasiet šo vērtību, ja jūsu noslodzes saņemšanas prakse ir sajaukta, un ir nepieciešams lēmums katru reizi, kad tiek palaista preču saņemšanas grāmatošana.

Šajā tabulā ir apkopota informācija par **Atļaut vairākas preču saņemšanas uz noslodzi** iestatījuma ietekmi.

| Atļaut vairākas preču saņemšanu uz noslodzi | Noslodzes daudzums | Kravas statuss | Piezīme |
|---|---|---|---|
| Kad šis lauks nav pieejams (versijas pirms 10.0.10) | <p>Noslodzes daudzums ir iestatīts tā, lai tas būtu vienāds ar reģistrēto daudzumu.</p><p>Ja noslodzes daudzums ir atjaunināts uz 0 (nulli), kas nozīmē, ka reģistrācija nav veikta, noslodzes rinda tiek dzēsta.</p><p>Ja noslodzei nav rindu, tā tiek dzēsta.</p> | _Saņemts_ | Ja pasūtījuma rindas reģistrētajam daudzumam pastāv vairākas noslodzes, tikai tās kravas statuss, no kuras tika nosūtīta saņemšana, tiek atjaunināts uz _Saņemts_. |
| Nr. | <p>Noslodzes daudzums ir iestatīts tā, lai tas būtu vienāds ar reģistrēto daudzumu, kas ir saistīts ar noslodzes ID.</p><p>Ja krājumu transakcijai nav ierakstīts noslodzes ID, uzvedība sakrīt ar uzvedību versijās pirms 10.0.10.</p> | _Saņemts_ | |
| Jā | Nav atjauninājumu | _Saņemts_, ja kopējais reģistrētais noslodzes daudzums ir vienāds ar vai lielāks par noslodzes daudzumu | |
| Jā | Nav atjauninājumu | _Piegādāts_ vai _Procesā_, ja kopējais reģistrētais noslodzes daudzums ir mazāks par noslodzes daudzumu | |

Pēc tam, kad **Noslodzes statusa** lauks ir iestatīts uz _Saņemts_, šai noslodzei vairs nevar veikt preču saņemšanas grāmatojumus. Tomēr darbinieks var reģistrēt atlikušo pasūtījuma daudzumu attiecībā pret saņemto noslodzi šādos apstākļos. (Plašāku informāciju skatiet [Noslodzes pārslodze](#load-over-receiving) iepriekš šajā tēmā.)

- Supply Chain Management versija ir vecāka par versiju 10.0.11.
- Līdzeklis _Noslodzes daudzuma pārslodze_ ir ieslēgta, un lauks **Noslodzes rindas daudzuma pārslodze**, kas atrodas mobilās ierīces izvēlnes vienumā noslodzes saņemšanas darbībai, ir iestatīts uz _Atļaut_.

Lai preces saņemšanas gadījumā tiktu reģistrēti papildu reģistrēti noslodzes daudzumi, salīdzinot ar noslodzi, kuras statuss ir  _Saņemts_, lietotājam ir jāizpilda grāmatošanas darbība no saistītā pirkšanas pasūtījuma.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Grāmatot reģistrēto daudzumu no Pirkšanas pasūtījuma lapas

Lai preces saņemšanas laikā reģistrētos daudzumus ierakstītu no **Pirkšanas pasūtījuma** lapas, lietotājs izpilda šādus uzdevumus, pirms viņš vai viņa atlasa **Preču saņemšanas** darbību:

- Iestatiet **Daudzuma** lauku sadaļā **Parametri** cilnē **Iestatījumi** uz _Reģistrēto daudzumu_.
- Laukā **Preču saņemšana** ievadiet grāmatošanas laikā iekļauto pirkšanas pasūtījumu numurus.

> [!NOTE]
> Rindas daudzums, kas ir iekļauts grāmatošanā, ir visu reģistrēto daudzumu kopsumma šai pirkšanas pasūtījuma rindai neatkarīgi no tā, vai daudzuma reģistrācija ir tikusi veikta pa vairākām noslodzēm, neatkarīgi no noslodzes, mobilās ierīces vai klienta. Tas pats noteikums attiecas uz gadījumiem, kad preču saņemšanas grāmatošana tiek veikta no noslodzes, ja lauks **Atļaut vairākas preču saņemšanas uz noslodzi** vai nu nav pieejams, vai arī tas nav iespējots.

Kad lietotājs atlasa **Labi**, lai apstiprinātu preču saņemšanas grāmatošanu, sistēmai ir šādi galvenie atjauninājumi uz atbilstošiem elementiem.

| Elements | Grāmatojumi |
|---|---|
| Pirkšanas pasūtījuma krājuma transakcija, kurai ir iekļauti rindas daudzumi grāmatošanas jomā | <p>Tiek atjaunināti šādi lauki (bet ņemiet vērā, ka ir arī vairāki citi atjauninājumi):</p><ul><li>Lauks <b>Saņemšana</b> ir iestatīts uz <i>Saņemts</i>.</li><li><b>Fiziskā datuma</b> lauks tiek atjaunināts ar preču saņemšanas grāmatošanas darbības datumu.</li></ul> |
| Ielādēt | Noslodzes atjauninājumi ir atkarīgi no tā, vai lauks **Atļaut vairākas preču saņemšanas uz noslodzi** ir pieejams un iespējots. Kārtulas ir aprakstītas nākamajā tabulā. |

Šajā tabulā ir apkopota informācija par **Atļaut vairākas preču saņemšanas uz noslodzi** iestatījuma ietekmi.

| Atļaut vairākas preču saņemšanas vienai kravai | Noslodzes daudzums | Kravas statuss | Piezīme |
|---|---|---|---|
| Ja šis lauks ir atspējots vai nav pieejams (versijās pirms 10.0.10) | Nav atjauninājumu | Atjauninājumi nav veikti. ( Statuss paliek _Atvērts_, _Piegādāts_ vai _Procesā_.) | Tā kā preču saņemšanas grāmatošana ir uzsākta no pirkšanas pasūtījuma, tad atjaunināšanas loģikai nav informācijas par saistību starp reģistrētajiem daudzumiem tās piemērošanas jomā un slodzēm, kad reģistrācija tika ierakstīta. Tāpēc tas nevar atlasīt noslodzi statusa atjaunināšanai. |
| Iespējota | Nav atjauninājumu | <p>Notiek viena no sekojošajām darbībām:</p><ul><li>Statuss tiek nomainīts uz <i>Saņemts</i>, ja pirkšanas pasūtījuma krājumu transakciju kopējais saņemšanas un iegādātais daudzums ir lielāks vai vienāds ar to saistītās noslodzes daudzumu.</li><li>Statuss paliek <i>Atvērts</i>, <i>Piegādāts</i> vai <i>Procesā</i>, ja iepriekšējais nosacījums nav izpildīts visām noslodzes rindām.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Atlasiet atbilstošu preču saņemšanas grāmatošanas opciju jūsu loģistikas operācijām

Kā iepriekš aprakstīts, sistēma piedāvā divas preču saņemšanas grāmatošanas opcijas. Opcijām var piekļūt šādās vietās:

- **Noslodzes** lapā vai no **Noliktavas pārvaldības \> Periodisko uzdevumu** izvēlnes kā atjaunināšanas darbu
- Lapā **Pirkšanas pasūtījums** vai no **Sagādes un resursi \> Pirkšanas pasūtījumi \> Saņemtās preces** izvēlnes kā atjaunināšanas darbu

Uzņēmumiem, kas izmanto noslodzes, lai plānotu un pārvaldītu savu ienākošo pasūtījumu transportēšanas un noliktavas apstrādes, ieteicams izmantot šādas funkcijas, kas ir paredzētas darbam ar noslodzēm:

- **Noslodžu krājumu saņemšanas** darbības savās noliktavas mobilajās ierīcēs, lai reģistrētu preču daudzumu ierašanos pret noslodzi
- **Preču saņemšanas grāmatošanas** darbības, kas ir iniciētas no noslodzes, lai atjauninātu krājuma virsgrāmatu

> [!NOTE]
> Citas daudzuma reģistrācijas un preču saņemšanas grāmatošanas funkcijas var izmantot, lai atbalstītu atbilstošos, ienākošos darbības procesus. Tomēr, ja izmantojat tās, kas ir savstarpēji aizstātas ar atvēlētām noslodzes funkcijām, varat ietekmēt noslodžu ierakstu datu precizitāti un tādējādi arī noslodzes vadības plūsmu neviendabīgumu.

## <a name="example-scenarios"></a>Piemēra situācijas

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Sagatavojiet savu sistēmu, lai palaistu parauga scenārijus

Lai strādātu ar šajā sadaļā aprakstītajiem paraugu scenārijiem, vispirms ir jāpārliecinās, vai sistēmā ir ieslēgti visi vajadzīgie līdzekļi. Nepieciešamajiem demonstrācijas datiem jābūt pieejamiem arī sistēmā.

#### <a name="turn-on-the-required-features"></a>Ieslēgt nepieciešamos līdzekļus

Šie scenāriji pieprasa _Vairāku preču saņemšanas grāmatošanu uz noslodzi_ līdzekli un tā priekšnosacījumu līdzekli. Administratori var ieslēgt šos līdzekļus, veicot šādas darbības.

1. Atveriet darbvietu **Funkcionalitātes pārvaldība**. (Pilnīgu informāciju par to, kā atrast un izmantot šo darbvietu, skatiet [Līdzekļu pārvaldības pārskats](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)

1. Ieslēdziet _Saistīt pirkšanas pasūtījuma krājumu transakcijas ar noslodzi_ līdzekli, kas norādītas sekojošā veidā:

    - **Modulis:** _Noliktavas vadība_
    - **Līdzekļa nosaukums:** _Saistīt pirkšanas pasūtījuma krājumu transakcijas ar kravu_

1. Ieslēdziet _Vairāku preču saņemšanas grāmatošanu uz noslodzi_ līdzekli, kas norādītas sekojošā veidā:

    - **Modulis:** _Noliktavas vadība_
    - **Līdzekļa nosaukums:** _Vairāku preču ieejas plūsmu iegrāmatošana uz noslodzi_

#### <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai, izmantojot šos scenārijus, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta demonstrācijas dati. Pirms sākat, jāatlasa arī **USMF** juridiskā persona.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Pievienojiet izvēlnes elementu noslodzes krājumu saņemšanai, kad tiek lietota mobilā ierīce

Pirms noliktavas saņemšanas darbinieki var izmantot mobilo ierīci, lai reģistrētu ienākošos krājumus, kas ir saistīti ar noslodzi, šim nolūkam ir jāizveido mobilās ierīces izvēlnes elements.

Šajā sadaļā jūs izveidosiet mobilās ierīces izvēlnes elementu un pievienosiet to esošai izvēlnei. Noliktavas darbinieks pēc tam var atlasīt izvēlnes elementu Noliktavas programmā.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilās ierīce \> Mobilās ierīces izvēlnes vienumi** un pārliecinieties, ka mobilās ierīces izvēlnē ir ietverts izvēlnes elements, kam ir šādi iestatījumi:

    - **Režīms:** _Darbs_
    - **Darba izveides process:** _Noslodzes krājuma saņemšana_
    - **Ģenerēt numura zīmi:** _Jā_

    Varat atstāt visus pārējos iestatījumus noklusējuma vērtībās.

    ![Mobilās ierīces izvēlnes krājuma iestatījumi](media/inbound-mobile-menu-items.png "Mobilās ierīces izvēlnes krājuma iestatījumi")

    Papildinformāciju par mobilās ierīces izvēlnes krājuma iestatīšanu skatiet [Mobilo ierīču iestatīšana noliktavas darbam](configure-mobile-devices-warehouse.md).

2. Pēc tam, kad esat pabeidzis izvēlnes krājuma iestatīšanu, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilās ierīce \> Mobilās ierīces izvēlnes krājumi** un pievienojiet to izvēlnes struktūrai jūsu mobilajām ierīcēm.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>1. piemēra scenārijs: reģistrēt noslodzi, kurā trūkst dažu krājumu

Šajā scenārijā ir parādīts, kā reģistrēt daudzumus ienākošai noslodzei, kur nav iekļauti visi paredzētie daudzumi. Pēc tam tiek parādīts, kā grāmatot preču saņemšanu pirkšanas pasūtījumam.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Izveidot noslodzi, lai plānotu pirkšanas pasūtījuma saņemšanu

Šajā procedūrā jūs manuāli izveidosiet pirkšanas pasūtījumu un saistīto noslodzi. Pēc tam jūs atjaunināsiet noslodzi, lai modelētu, ka tā tiek piegādāta no kreditora (kas atjaunina noslodzes statusu). Pēc tam noliktavas plānotāji var filtrēt noslodzes pēc **Noslodzes statusa**, lai atrastu paredzamās ienākošās noslodzes.

1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi  \> Visi pirkšanas pasūtījumi**.
1. Atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pirkšanas pasūtījumu** iestatiet **Kreditora konta** lauku uz _1001_.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu izveidotu pirkšanas pasūtījumu.
1. Jaunais pirkšanas pasūtījums jau ietver rindu zem **Pirkšanas pasūtījuma rindām**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** _A0001_
    - **Noliktava:** _24_
    - **Daudzums:** _10_

1. Darbību rūts cilnē **Pirkums** atlasiet **Darbības \> Apstiprināt**. Pasūtījuma statuss tagad ir _Apstiprināts_.
1. Darbību rūts cilnē **Noliktava** atlasiet **Darbības \> Kravu plānošanas rīks**.
1. Darbības rūts lapā **Kravu plānošanas rīks** cilnē **Piedāvājums un pieprasījums** atlasiet **Pievienot \> Jaunai noslodzei**.
1. Dialoglodziņā **Noslodzes veidnes piešķire** iestatiet **iNoslodzes veidnes ID** lauku uz _20' konteineru_.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu atgrieztos uz rīku.
1. Sadaļā **Noslodzes** atlasiet **Noslodzes ID**, lai atvērtu tikko izveidoto noslodzi.
1. Pārskatiet noslodzes galveni un rindas detaļas, un ievērojiet šādus punktus:

    - Kopsavilkuma cilnē **Noslodze** **Noslodzes statusa** lauks ir iestatīts uz _Atvērts_.
    - Sadaļā **Noslodzes rindas** ir viena rinda, kur **Daudzuma** lauks ir iestatīts uz _10_, un lauks **Darba izveidotais daudzums** ir iestatīts kā _0_ (nulle).

    ![Detalizēta informācija par kravu](media/inbound-load-details.png "Detalizēta informācija par kravu")

1. Darbību rūts cilnē **Nosūtīt un saņemt**, atlasiet **Apstiprināt \> Ienākošais sūtījums**. Ievērojiet, ka **Noslodzes statuss** ir mainīts uz _Piegādāts_.
1. Atzīmējiet **Noslodzes ID** vērtību, lai to varētu izmantot nākamajā procedūrā.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Reģistrēt noslodzi saņēmušo daudzumu saņemšanu

Kad noslodze pienāk noliktavas saņemšanas dokā, saņemšanas lietvedis reģistrē noslodzes daudzumus mobilajā ierīcē.

1. Izmantojiet savu mobilo ierīci, lai ieietu noliktavā 24. (Standarta demonstrācijas datos piesakieties, izmantojot _24_ kā lietotāja ID un _1_ kā paroli.)
1. Atlasiet _Noslodzes krājuma saņemšanas_ izvēlnes elementu, ko izveidojāt šim scenārijam.
1. Sekojiet datu ievades instrukcijām ekrānā, lai ievadītu šādas vērtības. (Pasūtījums var atšķirties atkarībā no izmantotās mobilās ierīces vai emulatora.)

    - **Noslodze** — ievadiet iepriekšējā procedūrā izveidoto noslodzes ID.
    - **Prece** — ievadiet _A0001_, kas ir šai noslodzei paredzētais krājums.
    - **Daudzums** – ievadiet _9_ kā faktisko daudzumu, kas atrodas noslodzē. Ievērojiet, ka šis daudzums ir mazāks par paredzamo daudzumu.

1. Turpiniet darbplūsmas izpildi, atstājot visus pārējos laukus tukšus vai iestatītus uz to noklusētajām vērtībām, līdz ierīce informē, ka darbs ir pabeigts.

Noslodzes saņemšanas uzdevums tagad ir pabeigts, un saņemšanas ierēdnis var pāriet pie nākamā uzdevuma. Tomēr noliktavas saņemšanas personāls vēlāk pārskatīs noslodzes ierakstu un varēs redzēt, ka saņemtais daudzums ir mazāks par paredzamo daudzumu. Viņi pabeigs šo procedūru, izmantojot Web klientu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Sarakstā atrodiet noslodzi, ko tikko saņēmāt. (Iespējams, ir jāatlasa izvēles rūtiņa **Rādīt slēgto**, lai iekļautu ienākošās noslodzes, kuru statuss ir _Piegādāts_.) Pēc tam atlasiet saiti **Noslodzes ID** kolonnā, lai atvērtu noslodzi.
1. Noslodzes ierakstā ievērojiet, ka **Noslodzes statusa** vērtība paliek _Piegādāts_, bet **Darba izveidotā daudzuma** vērtība noslodzes līnijā ir mainījusies uz _9_.
1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi  \> Visi pirkšanas pasūtījumi**.
1. Sarakstā sameklējiet tikko saņemto pirkumu un pēc tam kolonnā **Pirkšanas pasūtījums** atlasiet saiti, lai atvērtu pasūtījumu.
\
1. **Pirkšanas pasūtījuma rindās** kopsavilkuma cilnē atlasiet **Krājumi \> Skatīt \> Traksakcijas**.
1. Pārskatiet divu pirkšanas pasūtījumu traksakciju detaļas. (Iespējams, ir jāpersonalizē lapa **Krājumu transakcijas**, lai tiktu rādīts **Noslodzes ID** lauks režģī.) Ir jābūt redzamām divām transakcijām:

    - Transakcija ar saņemšanu statusā  _Reģistrēts_, ataino reģistrācijas daudzumu _9_, kas tika veikts ar noteiktu noslodzi, izmantojot mobilo ierīci. **Noslodzes ID** ir saistīts ar attiecīgo transakciju.
    - Transakcija, kurai ir saņemšana statusā _Pasūtīts_, norāda atlikušo nereģistrēto pasūtījuma rindas ar daudzumu _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Preču saņemšana norāda reģistrētos noslodzes daudzumus pret pirkuma pasūtījumiem

Šajā procedūrā preču saņemšana tiks nosūtīta pēc krājuma, kuru reģistrējāt noslodzei. Tādējādi saņemtie krājumi un saistītās izmaksas tiks pievienoti uzņēmuma virsgrāmatai.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Sarakstā atrodiet noslodzi, ko tikko saņēmāt. (Iespējams, ir jāatlasa izvēles rūtiņa **Rādīt slēgto**, lai iekļautu ienākošās noslodzes, kuru statuss ir _Piegādāts_.) Pēc tam atlasiet saiti **Noslodzes ID** kolonnā, lai atvērtu noslodzi.
1. Darbību rūts cilnē **Nosūtīt un saņemt**, atlasiet **Saņemt \> Preču saņemšana**. Atlasiet **Jā**, ja jums tiek piedāvāts apstiprināt transakciju.
1. Pārbaudiet režģi dialoglodziņā **Preču saņemšanas grāmatošana** kopsavilkuma cilnē **Rindas**. Jums vajadzētu redzēt pirkšanas pasūtījuma rindu, kurai daudzums ir reģistrēts pret atlasīto noslodzi.

    > [!NOTE]
    > Versijās, kur _Vairāku preču saņemšanas grāmatojumi uz noslodzi_ līdzeklis nav pieejams vai nav iespējots, noklusētais daudzums, kas tiek uzrādīts **Noslodzes rindu** režģī, būs kopējais daudzums, kas reģistrēts visās noslodzēs, kas saistītas ar pirkšanas pasūtījuma rindu.

1. Kopsavilkuma cilnē **Pārskats** pārbaudiet režģi laukā **Preču saņemšana**. Ņemiet vērā, ka tas ir jāiestata uz skaitli, kas ietver atlasītās noslodzes ID.
1. Atlasiet **Labi**, lai grāmatotu preču saņemšanu un aizvērtu dialoglodziņu **Preču saņemšanas grāmatošana**.
1. Tiek atgriezta informācija par noslodzi. Ņemiet vērā šādus punktus:

    - **Noslodzes statusa** lauks tagad ir iestatīts uz _Saņemts_.
    - Noslodzes rindā **Daudzuma** vērtība noslodzei ir mainījusies no _10_ uz _9_ gb, lai tas atbilstu reģistrētajam daudzumam, bet **Darba izveidotā daudzuma** vērtība joprojām ir _9_.

Ja pirkšanas grupa neplāno piegādāt kreditoru atlikušo pasūtījuma daudzumu 1, tas var slēgt pasūtījumu, atjauninot rindas piegādes atlikumu uz _0_. Tomēr, ja tiek ātri konstatēts, ka sākotnējā noslodzē ir saņemts trūkstošais gabals, noliktavas personāls var veikt vienu no šīm darbībām:

- Reģistrēt daudzumu attiecībā pret vienu un to pašu noslodzi. Šādā gadījumā **Noslodzes statusa** lauks tiks atiestatīts uz _Piegādāts_, un **Darba izveidotā daudzuma** vērtība tiks atjaunināta uz _10_. Šī izvēle ir pieejama tikai šādās situācijās:

    - Nav pieejams līdzeklis _Noslodzes daudzumu pārslodze_, vai arī tas nav iespējots.
    - Līdzeklis _Noslodzes daudzumu pārslodze_ ir pieejams un iespējots, un **Noslodzes rindas daudzuma pārslodzes** lauks ir iestatīts uz _Atļaut_.

- Pievienojiet daudzumu jaunai vai esošai noslodzei un apstrādājiet to ierastajā veidā.
- Reģistrēt un/vai saņemt daudzumu tādā veidā, kas neietver noslodzes apstrādi.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>2. piemēra scenārijs: reģistrēt daudzumus, kas tiek saņemti vairākās saņemšanas noslodzēs, kur trūkst dažu krājumu

Šādā gadījumā ienākošais sūtījums, kas ir saistīts ar vienu pirkšanas pasūtījuma rindu, tiks sadalīts divās noslodzēm. Piemēram, pirkšanas pasūtījuma rinda var tikt sadalīta vairākās noslodzēs, ņemot vērā svara un/vai tilpuma fizisko slodžu ierobežojumus.

Šis scenārijs arī parāda, kā apstrādāt vairāku preču saņemšanas grāmatojumus vienai un tai pašai noslodzei. Jūs reģistrēsit daudzumus, kas tiek saņemti vairākās saņemšanas noslodzēs, bet daudzumi neatbilst paredzētajiem daudzumiem. Izmaksu atjauninājumi, kas rodas, izmantojot preču saņemšanas grāmatošanu, tiks veikti vairākas reizes vienai un tai pašai noslodzei.

#### <a name="set-up-load-receiving-policies"></a>Iestatīt noslodzes saņemšanas ierobežojumus

Šajā procedūrā jūs iespējosiet vairāku preču saņemšanas grāmatojumus no vienas un tās pašas noslodzes.

1. Doties uz **Noliktavas vadība\> Iestatīšana \> Noliktavas vadības parametri**.
1. Cilnē **Noslodzes** iestatiet **Atļaut vairāku preču saņemšanu uz noslodzi** lauku uz _Jā_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Izveidot divas noslodzes, lai plānotu pirkšanas pasūtījuma saņemšanu

Šajā procedūrā jūs manuāli izveidosiet pirkšanas pasūtījumu un divas noslodzes. Pēc tam jūs manuāli atjaunināsiet katru noslodzi, lai modelētu, ka tā tiek piegādāta no kreditora (kas atjaunina noslodzes statusu). Pēc tam noliktavas plānotāji var filtrēt noslodzes pēc **Noslodzes statusa**, lai atrastu paredzamās ienākošās noslodzes.

Jūs arī uzzināsit, kā iestatīt pirkšanas pasūtījuma rindu, lai varētu saņemt daudzumu, kas ir par 20 procentiem vairāk nekā rindai norādītajam daudzumam.

1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi  \> Visi pirkšanas pasūtījumi**.
1. Atlasiet **Jauns**.
1. Kopsavilkuma cilnē **Kreditors** iestatiet **Kreditora konta** lauku uz _1001_ un pēc tam atlasiet **Labi**.
1. Jaunais pirkšanas pasūtījums tiek atvērts, un tajā ir iekļauta tukša rinda **Pirkšanas pasūtījuma rindu** režģī. Šajā pasūtījuma rindā iestatiet šādas vērtības:

    - **Krājuma numurs:** _A0001_
    - **Noliktava:** _24_
    - **Daudzums:** _10_

1. Kopsavilkuma cilnē **Rindas informācija** cilnē **Piegāde** iestatiet **Pārsniegtās piegādes** lauku uz _20_.
1. Darbību rūts cilnē **Pirkums** atlasiet **Darbības \> Apstiprināt**. Pasūtījuma statuss tagad ir _Apstiprināts_.
1. Darbību rūts cilnē **Noliktava** atlasiet **Darbības \> Kravu plānošanas rīks**.
1. Darbības rūts lapā **Kravu plānošanas rīks** cilnē **Piedāvājums un pieprasījums** atlasiet **Pievienot \> Jaunai noslodzei**.
1. Dialoglodziņā **Noslodzes veidnes piešķire** iestatiet **iNoslodzes veidnes ID** lauku uz _20' konteineru_. Cilnē **Detaļas** mainiet **Daudzuma** vērtību no _10_ uz _5_, lai daļēji pievienotu pirkšanas pasūtījuma rindas daudzumu.
1. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu dialoglodziņu.
1. Atkārtojiet no 8. līdz 10. solim, lai izveidotu otro noslodzi. Šoreiz **Daudzuma** lauks jau ir jāiestata uz _5_.
1. Lapā **Kravu plānošanas rīks**, kas atrodas režģī **Noslodzes**, atlasiet **Noslodzes ID** vērtību pirmajai izveidotajai noslodzei. Tiek parādīta lapa **Noslodzes detaļas**, un parādās atlasītā noslodze. Rīkojieties šādi:

    1. Darbību rūts cilnē **Nosūtīt un saņemt**, atlasiet **Apstiprināt \> Ienākošais sūtījums**.
    1. Ievērojiet, ka **Noslodzes statusa** vērtība ir mainīta uz _Piegādāts_.
    1. Atlasiet aizvēršanas pogu, lai atgrieztos lapā **Kravu plānošanas rīks**.

1. Atkārtojiet iepriekšējo soli otrajai izveidotajai noslodzei.
1. Pierakstiet divas **Noslodzes ID** vērtības, kas parādās režģī **Noslodzes**.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Reģistrēt daudzumu daļēju saņemšanu, kas saņemti pirmajā noslodzē, un grāmatot reģistrēto noslodzes daudzumu

Kad noslodzes pienāk noliktavas saņemšanas dokā, saņemšanas lietvedis reģistrē noslodzes daudzumus mobilajā ierīcē. Reģistrētie krājumi, kas ir saistīti ar noslodzi, pēc tam tiek atjaunināti uzņēmuma virsgrāmatā, grāmatojot pirkšanas pasūtījuma preču saņemšanu, kas pamatota uz noslodzi.

Šī procedūra parāda, kā saņemšanas ierēdnis reģistrē noslodzes daudzumus mobilajā ierīcē.

1. Izmantojiet savu mobilo ierīci, lai ieietu noliktavā 24. (Standarta demonstrācijas datos piesakieties, izmantojot _24_ kā lietotāja ID un _1_ kā paroli.)
1. Atlasiet _Noslodzes krājuma saņemšanas_ izvēlnes elementu, ko izveidojāt šim scenārijam.
1. Sekojiet datu ievades instrukcijām ekrānā, lai ievadītu šādas vērtības. (Pasūtījums var atšķirties atkarībā no izmantotās mobilās ierīces vai emulatora.)

    - **Noslodze** — ievadiet iepriekšējā procedūrā izveidoto pirmo noslodzes ID.
    - **Prece** — ievadiet _A0001_, kas ir šai noslodzei paredzētais krājums.
    - **Daudzums** – ievadiet _3_. Ievērojiet, ka šis daudzums ir mazāks par paredzamo daudzumu. Šajā scenārijā iedomājieties, ka jums kā saņemošajam ierēdnim nav laika reģistrēt visus šīs noslodzes daudzumus. Vēlāk, veicot šo procedūru, tiks reģistrēti atlikušie gabali, atkārtojot šo soli un iestatot lauku **Daudzums** uz _2_.

1. Turpiniet darbplūsmas izpildi, atstājot visus pārējos laukus tukšus vai iestatītus uz to noklusētajām vērtībām, līdz ierīce informē, ka darbs ir pabeigts.
1. Tīmekļa klientā dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Sarakstā sameklējiet tikko saņemto noslodzi un atlasiet **Noslodzes ID** vērtību, lai atvērtu noslodzi. Noslodzes ierakstā ievērojiet, ka **Noslodzes statusa** vērtība paliek _Piegādāts_, bet **Darba izveidotā daudzuma** vērtība noslodzes līnijā ir mainījusies uz _3_.
1. Darbību rūts cilnē **Nosūtīt un saņemt**, atlasiet **Saņemt \> Preču saņemšana**. Atlasiet **Jā**, ja jums tiek piedāvāts apstiprināt transakciju.
1. Dialoglodziņā **Preču saņemšanas grāmatošana** pārskatiet, bet nemainiet parādītās vērtības un pēc tam atlasiet **Labi**.
1. Jūs atgriežaties uz atlasītās noslodzes **Noslodzes informācijas** lapu. Ņemiet vērā šādus punktus:

    - **Noslodzes statusa** lauks paliek iestatīts uz _Piegādats_.
    - Noslodzes rindā **Daudzuma** vērtība noslodzei joprojām ir _5_ gb, kas ir sākotnējais noslodzes daudzums, un **Darba izveidotā daudzuma** vērtība joprojām ir _3_.

1. Pabeidziet šīs noslodzes atlikušo daudzumu reģistrāciju, atkārtojot šo procedūru. Tomēr 3. solī iestatiet **Daudzuma** lauku uz _2_.

Pirmās noslodzes saņemšanas uzdevums tagad ir pabeigts. Divi preču saņemšanas žurnāli ir izveidoti, viens katram no diviem jūsu izpildītajiem preču saņemšanas atjauninājumiem.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Reģistrēt daudzumu, kas saņemts otrajā noslodze, un konts pārsniegtajam daudzumam

Šim scenārijam saņemšanas lietvedis saņems reģistru daudzumam, kas pārsniedz noslodzē pastāvošo daudzumu. Pārsniegtā saņemšana ir atļauta, jo sistēma ir iestatīta, lai atļautu pārsniegšanu.

1. Izmantojiet savu mobilo ierīci, lai ieietu noliktavā 24. (Standarta demonstrācijas datos piesakieties, izmantojot _24_ kā lietotāja ID un _1_ kā paroli.)
1. Atlasiet _Noslodzes krājuma saņemšanas_ izvēlnes elementu, ko izveidojāt šim scenārijam.
1. Sekojiet datu ievades instrukcijām ekrānā, lai ievadītu šādas vērtības. (Pasūtījums var atšķirties atkarībā no izmantotās mobilās ierīces vai emulatora.)

    - **Noslodze** — ievadiet otrās noslodzes ID, ko izveidojāt iepriekš.
    - **Prece** — ievadiet _A0001_, kas ir šai noslodzei paredzētais krājums.
    - **Daudzums** – ievadiet _7_, kas ir atlikušais daudzums, ko kreditors ir pilnvarots piegādāt kā daļu no kopējā pirkšanas pasūtījuma daudzuma 12 (kur 10 ir sākotnējais pasūtījuma daudzums, un 2 ir atļautais 20 procentu pārsniegšanas daudzums). Atcerieties, ka 5 gb jau ir reģistrēti attiecībā pret pirmo noslodzi.

Otrā noslodze tagad ir atjaunināta ar daudzumu 7, un to var saņemt preču saņemšanā, kas tiek atjaunināta, pamatojoties uz šo daudzumu.
