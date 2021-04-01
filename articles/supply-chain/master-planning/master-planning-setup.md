---
title: Vispārējās plānošanas iestatīšana
description: Šajā tēmā ir aprakstītas dažādas svarīgas stratēģijas un parametri, kas tiek izmantoti vispārējās plānošanas iestatīšanai.
author: t-benebo
manager: tfehr
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 5fd24ad91b669b054b88cd187309038f1716e582
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256211"
---
# <a name="set-up-master-planning"></a>Vispārējās plānošanas iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas dažādas svarīgas stratēģijas un parametri, kas tiek izmantoti vispārējās plānošanas iestatīšanai. Tajā ir ietverts tādu plānu tipu apskats, kuri tiek izmantoti vispārējā plānošanā, un paskaidrots, kura plāna stratēģija ir jāizmanto atkarībā no jūsu uzņēmuma vajadzībām. Tajā aprakstīti arī galvenie parametri, kas ietekmē plānu, un paskaidrots, kā šie parametri ietekmē plānotos pasūtījumus, kas tiek ieteikti.

## <a name="types-of-master-plans"></a>Vispārējo plānu tipi

Vispārējai plānošanai ir divi plānu tipi: statiski un dinamiski. Katrs tips ir paredzēts citam lietojumam. Lai iegūtu vislabākos rezultātus, ieteicams izmantot jūsu scenārijam atbilstošu plānu.

### <a name="static-plan"></a>Statiskais plāns

Statiskais plāns paliek nemainīgs neatkarīgi no jebkādām izmaiņām piedāvājumā un pieprasījumā līdz nākamajai vispārējās plānošanas izpildes reizei.

Statiskais plāns tiek izmantots, lai pieņemtu un apstiprinātu pasūtījumus, kas tiek ieteikti. Tas ir darbības plāns, ko var izmantot dažādi uzņēmuma darbinieki (piemēram, sagādnieks vai ražošanas plānotājs), lai pieņemtu pamatotus lēmumus un veiktu ikdienas uzdevumus un aktivitātes.

Statiskais plāns arī atbalsta pārģenerēšanu. Katru reizi, kad tiek palaista vispārējā plānošana, tiek aprēķināts pilnīgi jauns optimizēts plāns, un esošie pasūtījumi, kas nav apstiprināti, tiek dzēsti.

### <a name="dynamic-plan"></a>Dinamiskais plāns

Dinamiskais plāns parasti sākas kā statiskā plāna kopija, bet to var atjaunināt katru reizi, kad tiek mainīti pamatdati. Piemēram, ja dati mainās, tiek izveidots jauns pārdošanas pasūtījums.

Dinamiskais plāns tiek izmantots ekspromta plānošanai. Tas ļauj uzņēmumam pārraudzīt mainīgo pasūtījumu tīklu un krājumu pieejamību, neizjaucot statisko plānu, ko citi lietotāji izmanto saviem darba procesiem. Tas īpaši tiek izmantots iegādes pieejamībai (CTP). Dinamiskais plāns ir noklusējuma plāns, kad neto vajadzības tiek atvērtas no pasūtījuma lapām (piemēram, pārdošanas pasūtījuma, pirkšanas pasūtījuma vai ražošanas pasūtījuma lapām).

Dinamiskais plāns izmanto neto izmaiņas. Tāpēc tas palīdz nodrošināt ātrāku izpildes laiku.

## <a name="strategies-for-using-master-plans"></a>Vispārējo plānu izmantošanas stratēģijas

Vispārējā plānošanā varat izmantot vai nu vienu plānu, vai divus plānus. Stratēģija, ko izmantojat, ir atkarīga no jūsu uzņēmuma vajadzībām.

### <a name="one-plan-strategy"></a>Viena plāna stratēģija

Viena plāna stratēģijas gadījumā tas pats vispārējais plāns tiek izmantots gan statiskajam plānam, gan dinamiskajam plānam. Šī stratēģija tiek izmantota plānveida scenārijiem, kuros parasti nav jāsimulē plāns, kas izpilda pasūtījumu.

Viena plāna stratēģiju parasti izmanto mazumtirdzniecības un izplatīšanas nozarēs vai arī, ja pārdošanas piegādes datumi ir apstiprināti, pamatojoties uz pakalpojumu līmeņa līgumiem (SLA) vai izpildes laikiem. Plānam piegādes datuma kontroli var izmantot bez CTP.

Ja ir jāveic simulācija, plānu var palaist atkārtoti krājumiem, kuriem nepieciešama simulācija. Plānotie pasūtījumi, ko izveido pasūtījumu simulācijas, parasti ir apstiprināti.

### <a name="two-plan-strategy"></a>Divu plānu stratēģija

Divu plānu stratēģijas gadījumā tiek izmantots statiskais plāns un cits dinamiskais plāns. Divu plānu stratēģija parasti tiek izmantota konfigurācijas atbilstoši pasūtījumam scenārijos, kuros ir jāveic pārdošanas pasūtījumu simulācijas un jāaprēķina precīzi pārdošanas pasūtījumu nosūtīšanas datumi, bet aprēķini nedrīkst ietekmēt ikdienas operācijas. Šīs simulācijas vienmēr tiek veiktas dinamiskajā plānā. Divu plānu stratēģija ir noderīga, piemēram, autobūves un oriģinālā aprīkojuma ražošanas (OEM) nozarēs.

Divu plānu stratēģijas gadījumā var izmantot piegādes datuma kontroles CTP. Lietojot CTP, tā automātiski aktivizē izpildi dinamiskajā plānā.

### <a name="setting-up-the-plans"></a>Plānu iestatīšana

Plānus var izveidot lapā **Vispārējie plāni** (**Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**).

Varat norādīt, kuri plāni tiks izmantoti statiskajam plānam un dinamiskajam plānam, iestatot laukus **Pašreizējais statiskais vispārējais plāns** un **Pašreizējais dinamiskais vispārējais plāns** lapā **Vispārējās plānošanas parametri** (**Vispārējā plānošana \> Iestatījumi \> Vispārējās plānošanas parametri**). Lai izmantotu viena plāna stratēģiju, izvēlieties to pašu plānu laukos **Pašreizējais statiskais vispārējais plāns** un **Pašreizējais dinamiskais vispārējais plāns**.

## <a name="types-of-planning-methods"></a>Plānošanas metožu tipi

Lai palaistu vispārējo plānošanu, var izmantot trīs aprēķina metodes: pārģenerēšana un neto izmaiņas. Palaižot katra metode izveido citu plānu.

Norādiet plānošanas metodi dialoglodziņā **Vispārējās plānošanas izpilde**. Lai atvērtu šo dialoglodziņu, pārejiet uz **Vispārējā plānošana \> Vispārējā plānošana \> Izpildīt \> Vispārējā plānošana** vai atlasiet vienumu **Izpildīt** darbvietā **Vispārējā plānošana**.

### <a name="regeneration"></a>Pārģenerēšana

Pārģenerēšanas plānošanas metode dzēš esošos plānotos pasūtījumus, izņemot gadījumus, kad tie ir apstiprināti. Tā ģenerē jaunus plānotos pasūtījumus, pamatojoties uz visām prasībām. Pārģenerēšana ir vienīgā plānošanas metode, kas ir pieejama statiskajiem plāniem.

- Tiek ņemtas vērā piegādes izmaiņas. Šīs izmaiņas ietver izmaiņas budžetā.
- Šī metode ievēro vajadzības aprēķināšanas metodi **Periods**.
- Šī metode atbalsta preču aizvietošanas funkcionalitāti (PI).

### <a name="net-change"></a>Neto apgrozījums

Neto izmaiņu plānošanas metode ģenerē plānotos pasūtījumus, lai segtu prasības, kas izveidotas vai mainītas kopš pēdējās vispārējās plānošanas izpildes. Piegādes izmaiņas netiek ņemtas vērā, kad tiek izpildīta šī metode. Sistēma neņem vērā jaunas piegādes, un iepriekš izveidotie plānotie pasūtījumi netiek dzēsti, ja tie vairs nav nepieciešami. Neto izmaiņu plānošanas metode tiek izpildīta ātrāk nekā pārģenerēšanas metode. Tā ir pieejama tikai dinamiskajiem plāniem.

- Darbību datumi un turpmākie datumi tiek atjaunināti visiem pieprasījumiem.
- Šī metode neievēro vajadzības aprēķināšanas metodi **Periods**.
- Šī metode neizpilda budžetu, pat ja tā ir atlasīta plānā.
- Šī metode neatbalsta preču aizvietošanas funkcionalitāti (PI).

### <a name="net-change-minimized"></a>Minimizēts neto apgrozījums

Minimizēto neto izmaiņu plānošanas metode ģenerē plānotos pasūtījumus, lai segtu tikai prasības, kas izveidotas vai mainītas kopš pēdējās vispārējās plānošanas izpildes. Šai metodei atšķirībā no neto izmaiņu metodes darbību datumi un turpmākie datumi tiek atjaunināti tikai jaunajām vai mainītajām prasībām. Šī plānošanas metode ir pieejama tikai dinamiskajiem plāniem.

## <a name="types-of-scheduling-methods"></a>Plānošanas metožu tipi

Katram plānam lapas **Vispārējie plāni** kopsavilkuma cilnē **Vispārīgi** (**Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**) ir jāatlasa plānošanas metode, kas tiek izmantota ražošanas pasūtījumiem. Varat plānot ražošanu operāciju līmenī un darbu līmenī.

### <a name="operations-scheduling"></a>Operāciju plānošana

Operāciju plānošanu var lietot, lai sniegtu vispārēju ražošanas procesa novērtējumu laika periodam. Operāciju plānošana neizvērš ražošanas maršruta operācijas darbos. Plašāku informāciju par operāciju plānošanu skatiet tēmā [Operāciju plānošana](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Darbu plānošana

Darbu plānošana ir detalizētāka plānošanas metode, kurā katra operācija tiek sadalīta atsevišķos uzdevumos vai darbos. Darbu plānošana ietver informāciju par noslodzi. Tā parasti tiek izmantota atsevišķu darbu plānošanai ražotnē nekavējoties vai īstermiņa periodā. Plašāku informāciju par darbu plānošanu skatiet tēmā [Darbu plānošana](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Periods dienās

Katram plānam var izvēlēties, cik tālu nākotnē ir jāaprēķina dažādas prasības un citi apsvērumi, izmantojot vispārējo plānošanu. Šo laikposmu sauc par *periodu*. Lai iegūtu vislabākos rezultātus vispārējā plānošanā, ieteicams koriģēt dažādus periodus atbilstoši jūsu uzņēmuma vajadzībām. Katram plānam periodus var atrast lapas **Vispārējie plāni** kopsavilkuma cilnē **Periodi dienās** (**Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**).

> [!NOTE]
> Periodi norāda, cik tālu nākotnē tiek aprēķinātas dažādas prasības un citi apsvērumi, izmantojot vispārējo plānošanu. Šajā lapā atlasītie periodi pārlabos vajadzību grupā definētos periodus. Tas nozīmē, ka, iestatot laika perioda opciju uz „Jā” un definējot dienas, tiks pārlabots laika periods, kas definēts vajadzības grupā. Iestatot vienumu Nē, periods tiks definēts vajadzību grupā. Visbeidzot, ja nevēlaties vai nav nepieciešams izmantot opciju (piemēram, nevēlaties izmantot darbību ziņojumus), iestatiet vienumu **Jā**, un pēc tam iestatiet periodam **0** (nulle) dienas.

### <a name="coverage"></a>Vajadzība

Vajadzību periods norāda plānošanas periodu vai to, kad ir jāiekļauj pieprasījums. Citiem vārdiem sakot, tas norāda jūsu plānošanas diapazonu.

Iestatot opcijai **Vajadzība** vienumu **Jā**, var pārlabot vajadzību periodu, kas definēts krājumam vispārējās plānošanas laikā. Šādā gadījumā ievadiet dienu skaitu, kuru laikā vispārējās plānošanas aprēķinam ir jāsedz prasības. Vajadzības periods ir aprēķināts, sākot no pašreizējā datuma. Vajadzības, kas parādās pirms pašreizējā datuma, vienmēr tiek apstrādātas.

> [!NOTE]
> Lai iegūtu vislabākos rezultātus vispārējā plānošanā, ieteicams koriģēt vajadzību periodu atbilstoši plānošanas diapazonam.

### <a name="freeze"></a>Iesaldēt

Periods bez izmaiņām norāda periodu, kad esošie plānotie pasūtījumi netiek mainīti, palaižot jaunu vispārējo plānu. Plānotie pasūtījumi tiek bloķēti, un netiks ieteikti jauni plānotie pasūtījumi.

Iestatot opcijai **Bloķēt** vienumu **Jā**, var pārlabot periodu bez izmaiņām, kas definēts krājumam vispārējās plānošanas laikā. Šādā gadījumā ievadiet dienu skaitu, kuru laikā aktivitātes plānošana ir jābloķē. Atcerieties, ka šajā periodā jauni plānošanas pasūtījumi netiek veidoti un pašreizējos plānotos pasūtījumus nevar mainīt.

### <a name="firming"></a>Apstiprināšana

Apstiprināšanas periods norāda laika diapazonu, kurā plānotie pasūtījumi tiek automātiski pārveidoti par ražošanas un pirkšanas pasūtījumiem. Šo procesu arī sauc par *automātiska plānoto pasūtījumu apstiprināšanu*.

Iestatot opcijai **Apstiprināšana** vienumu **Jā**, var pārlabot apstiprināšanas periodu, kas definēts krājumam vispārējās plānošanas laikā. Šādā gadījumā ievadiet dienu skaitu, kuru laikā plānotie pirkšanas pasūtījumi un plānotie ražošanas pasūtījumi automātiski jāapstiprina. Apstiprināšanas periods tiek aprēķināts uz priekšu, sākot no vispārējās plānošanas datuma. Plānotā pirkšanas pasūtījuma automātisko apstiprināšanu var veikt tikai tad, ja krājums ir saistīts ar kreditoru.

### <a name="forecast-plan"></a>Budžeta plāns

Budžeta plāna periods norāda, cik tālu nākotnē vispārējā plānošana izveidos plānotos pasūtījumus krājumiem, kuriem ir prognozēts pieprasījums.

Iestatot opcijai **Budžeta plāns** vienumu **Jā**, var pārlabot budžeta plāna periodu, kas definēts krājumam vispārējās plānošanas laikā. Šādā gadījumā ievadiet dienu skaitu, kuru laikā pārdošanas prognoze no budžeta plāna jāietver vispārējā plānošanā.

### <a name="capacity"></a>Noslodze

Noslodzes periods norāda, cik tālu nākotnē sistēma ņems vērā jūsu resursu maksimālo noslodzi, veicot pasūtījumu plānošanu. Citiem vārdiem sakot, plānā tiks paredzēti ražošanas pasūtījumi, izmantojot ražošanas maršrutu krājumiem, un tas ņems vērā ražošanas maršruta resursus un katra resursa maksimālo noslodzi.

Iestatot opcijai **Noslodze** vienumu **Jā**, var pārlabot noslodzes periodu, kas definēts krājumam vispārējās plānošanas laikā. Šādā gadījumā ievadiet dienu skaitu, kurās plānotajiem ražošanas pasūtījumiem ir jāplāno noslodze. Vispārējā plānošanā tiek izmantots krājuma aktīvais ražošanas maršruts un plānošana atpakaļ no vajadzības datuma. Ja vajadzības datums plānotajam ražošanas pasūtījumam ir ārpus noslodzes perioda, krājuma piegādes laiks nosaka izpildes laiku. Noslodzes periods tiek aprēķināts, sākot no pašreizējā datuma.

### <a name="action-message"></a>Optimizācijas priekšlikums

Darbību ziņojumi iesaka izmaiņas, ko var veikt esošajam piegādes pasūtījumam, lai palīdzētu optimizēt piegādes plānu. Piemēram, tie var ieteikt turpināt vai atlikt pasūtījumus vai arī palielināt vai samazināt pasūtījuma daudzumus.

Iestatot opcijai **Darbības ziņojums** vienumu **Jā**, var pārlabot darbības ziņojuma periodu, kas definēts krājumam vispārējās plānošanas laikā. Šādā gadījumā ievadiet dienu skaitu, kuru laikā vispārējai plānošanai jāveido vajadzību darbību ziņojumi. Darbību ziņojumu periods tiek aprēķināts, sākot no pašreizējā datuma.

Plašāku informāciju par darbību ziņojumiem skatiet tēmā [Darbību ziņojumi](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Darbības ziņojumu aprēķins izraisa ilgāku izpildes laiku vispārējai plānošanai. Ja darbības ziņojumi netiek regulāri analizēti un pielietoti (katru dienu, katru nedēļu utt.), apsveriet iespēju izslēgt aprēķinu vispārējās plānošanas izpildes laikā. Lai izslēgtu aprēķinu, lapā **Vispārējie plāni** iestatiet periodam **Darbības ziņojums** vērtību **0** (nulle) vispārējam plānam, kas tiek palaists. Arī pārliecinieties, ka iestatījums **Darbības ziņojuma** ir izslēgts visām vajadzību grupām.

### <a name="calculated-delays"></a>Aprēķinātie kavējumi

Varat norādīt, cik tālu nākotnē tiek noteikti un ziņoti iespējamie plānoto pasūtījumu kavējumi. Šādā veidā var ieplānot iespējamos (kavētos) piegādes datumus.

Ja plānoto pasūtījumu nevar izpildīt pieprasītajā datumā, tas tiek plānots agrākajā transakcijas izpildes datumā, pamatojoties uz izpildes laikiem un materiālu un noslodzes pieejamību.

### <a name="approved-requisitions-time-fence"></a>Apstiprināto pieprasījumu periods

Varat iestatīt vispārējo plānošanu, lai izveidotu plānotos pasūtījumus pieprasījumam. Iestatiet opcijai **Iekļaut pieprasījumus** vienumu **Jā** lapas **Vispārējie plāni** cilnē **Vispārīgi**. Pēc tam, ja apstiprināta pieprasījuma mērķis ir papildināšana, vispārējā plānošana automātiski izveido atbilstošu plānoto pasūtījumu, lai to izpildītu. Papildināšanas metodi nosaka piegādes politika, kas iestatīta krājumiem jūsu organizācijā. Pēc papildināšanas pieprasījuma izveides un apstiprināšanas lietotājam nav jāveic papildu darbības.

Iestatot opcijai **Apstiprināto pieprasījumu periods** vienumu **Jā** kopsavilkuma cilnē **Periods dienās**, varat pārlabot apstiprināto pieprasījumu periodu, kas noteikts attiecīgajam krājumam vispārējās plānošanas laikā. Šādā gadījumā ievadiet dienu skaitu pagātnē, kuru laikā pieprasījums no apstiprinātiem pieprasījumiem ar mērķi Papildināšana jāiekļauj vispārējā plānošanā. Piemēram, var norādīt, ka vērā jāņem un jāplāno tikai neizpildīts, nokavēts pieprasījums no apstiprinātiem pieprasījumiem, kas tika izveidoti pēdējo 10 dienu laikā.

### <a name="sequencing"></a>Secība

Secība ļauj sakārtot plānotos pasūtījumus, pamatojoties uz secības atribūtiem, kas saistīti ar pabeigto preci. To bieži izmanto, lai sagatavotu ražošanas pasūtījumus iepakojumam. Piemēram, to var izmantot, lai iepakotu kastes noteiktā secībā, pamatojoties uz krāsu un izmēru.

Iestatot opcijai **Secība** vienumu **Jā**, varat norādīt, cik tālu nākotnē operācijas vai darbi jāsakārto noteiktā secībā. Ņemiet vērā — jo ilgāks ir periods, jo ilgāks laiks ir nepieciešams vispārējās plānošanas izpildei.

### <a name="calculated-delays"></a>Aprēķinātie kavējumi

Aizkaves opcijas palīdz nodrošināt, ka pasūtījumiem ir izpildāmi plānotie datumi. Lapas **Vispārējie plāni** kopsavilkuma cilnē **Aprēķinātās aizkaves** ir pieejamas šādas opcijas:

- **Nodrošināt, lai plānotie pasūtījumi netiek izveidoti pirms vispārējās plānošanas izpildes datuma** — iestatiet šai opcijai vienumu **Jā**, lai palīdzētu nodrošināt, ka pasūtījumus nevar plānot datumos, kas jau ir pagājuši.
- **Pieskaitīt aprēķināto aizkavi vajadzības datumam** (sadaļā **Plānotie pirkšanas pasūtījumi**) — iestatiet šai opcijai vienumu **Jā**, lai pieskaitītu aprēķināto aizkavi vajadzībām.
- **Pieskaitīt aprēķināto aizkavi vajadzības datumam** (sadaļā **Plānotie ražošanas pasūtījumi**) — iestatiet šai opcijai vienumu **Jā**, lai pieskaitītu aprēķināto aizkavi vajadzībām.
- **Pieskaitīt aprēķināto aizkavi vajadzības datumam** (sadaļā **Plānotā pārsūtīšana**) — iestatiet šai opcijai vienumu **Jā**, lai pieskaitītu aprēķināto aizkavi vajadzībām.
- **Pieskaitīt aprēķināto aizkavi vajadzības datumam** (sadaļā **Plānotais Kanban**) — iestatiet šai opcijai vienumu **Jā**, lai pieskaitītu aprēķināto aizkavi vajadzībām.

Iestatot opcijām **Pieskaitīt aprēķināto aizkavi vajadzības datumam** vienumu **Jā**, lai pievienotu aizkaves vajadzībām, sistēma ņem vērā resursu noslodzi un izveido izpildāmus plānotos pasūtījumus. Plānoto pasūtījumu datumu pārrēķins palielina vispārējās plānošanas izpildes laiku. Tāpēc, ja nav nepieciešams izmantot aizkaves, iestatiet opcijai vienumu **Nē**.

## <a name="positive-and-negative-days"></a>Pozitīvās un negatīvās dienas

Pozitīvas un negatīvas dienas ietekmē to, kā vispārējā plānošana piedāvā plānotos pasūtījumus un darbības. Pozitīvās un negatīvās dienas tiek iestatītas krājuma vajadzību grupai. Varat definēt dažādas vajadzību grupas un iestatīt to parametrus lapā **Vajadzību grupas** (**Vispārējā plānošana \> Iestatījumi \> Vajadzības \> Vajadzību grupas**).

### <a name="positive-days"></a>Dienas(+)

Pozitīvās dienas norāda, cik tālu nākotnē vispārējā plānošana ņem vērā pašreizējos krājumus vai ieejas plūsmu, lai izpildītu turpmāko pieprasījumu. Piemēram, ja vienumam Dienas(+) ir iestatīta vērtība **100**, pašreizējos krājumus var izmantot, lai izpildītu pieprasījumu nākamajās 100 dienās. Ja ir izveidots pasūtījums 150 dienas pēc pašreizējā datuma, vispārējā plānošana izveidos plānoto pasūtījumu, lai apmierinātu šo pieprasījumu, pat ja attiecīgie rīcībā esošie krājumi var nodrošināt pasūtījuma izpildi. Ātras realizācijas krājumiem, kuriem ir īss izpildes laiks, iespējams, nevēlēsities izmantot rīcībā esošos krājumus pasūtījumam, kas paredzēts tālā nākotnē. Šādu ātras realizācijas krājumu gadījumā pašreizējie rīcībā esošie krājumi tiks ātri pārdoti, un turpmāk varēs veikt papildu pasūtījumus, lai savlaicīgi izpildītu turpmāko pieprasījumu, kas būtu iespējams, pateicoties krājuma īsajam izpildes laikam.

Pozitīvas dienas ietekmē arī darbību ziņojumus. Piemēram, sistēma var ieteikt palielināt plānoto pirkšanas pasūtījumu, lai tajā tiktu ietverts pieprasījums norādītajā pozitīvo dienu skaitā nākotnē. Ja vienumam Dienas(+) ir iestatīta vērtība **100** un ja ir krājuma pieprasījums 30 dienu laikā pēc pašreizējā datuma, sistēma izveidos plānoto pasūtījumu, lai izpildītu šo pieprasījumu. Ja ir pieprasījums pēc tā paša krājuma 90 dienu laikā pēc pašreizējā datuma, sistēma ieteiks palielināt pasūtījuma daudzumu 30 dienu laikā pēc pašreizējā datuma, lai pasūtījumā tiktu iekļauts arī pieprasījums 90 dienu laikā. Tomēr, ja pieprasījums pēc krājuma ir 150 dienu laikā pēc pašreizējā datuma, sistēma neieteiks palielināt pasūtījuma daudzumu, kas jau bija ieplānots. Tā vietā tiks izveidots jauns plānotais pasūtījums.

Parasti vienumam Dienas(+) kā vērtību iestata skaitli starp krājuma ilgāko izpildes laiku un vajadzības periodu. Ieteicams piešķirt krājumus, kas tiek regulāri iepirkti vai ražoti, vajadzību grupai, kurā pozitīvās dienas ir vienādas ar krājuma izpildes laiku.

### <a name="negative-days"></a>Dienas(-)

Negatīvās dienas norāda, cik ilgi būs atļautas krājumu ieejas plūsmas. Tās norāda dienu skaitu, ko esat gatavs gaidīt, pirms veicat jaunu papildināšanas pasūtījumu, ja ir negatīvs krājumu daudzums vai ja nav pietiekami krājumu. Vienums Dienas(-) sniedz atbildi uz jautājumu, vai ir jāizveido jauns krājuma pirkšanas pasūtījums vai arī ir jāizmanto esošais iepirkums, kaut arī ir zināms, ka krājuma piegāde tiks kavēta?

Piemēram, jums ir pārdošanas pasūtījums krājumam 15 dienas pēc pašreizējā datuma. Šim pašam krājumam ir arī pirkšanas pasūtījums. Šis pirkšanas pasūtījums tiks saņemts 20 dienu laikā no pašreizējā datuma. Vai vēlaties, lai sistēma izveidotu pirkšanas pasūtījumu šim pārdošanas pasūtījumam, vai arī vēlaties izmantot esošo pasūtījumu, pat ja pārdošanas pasūtījumu nevar izpildīt laikā? Ja vienumam Dienas(-) ir iestatīta vērtība, kas ir mazāka par **5**, lai norādītu, ka krājumu var aizkavēt ne vairāk kā par piecām dienām, sistēma izveido jaunu plānoto pirkšanas pasūtījumu, lai izpildītu pārdošanas pasūtījumu. Ja vienumam Dienas(-) ir iestatīta vērtība, kas ir lielāka par **5**, sistēma izmanto krājuma esošo pasūtījumu.

Negatīvās dienas ietekmē arī vispārējās plānošanas veiktspēju. Ja vienumam Dienas(-) ir iestatīta liela vērtība, tiks izveidoti daudzi darbību ziņojumi.

Ieteicams iestatīt vienumam Dienas(-) skaitli, kas ir mazāks par krājuma izpildes laiku.

### <a name="dynamic-negative-days"></a>Dinamiskās negatīvās dienas

Dinamiskās negatīvās dienas ņem vērā krājuma izpildes laiku un norādītās negatīvās dienas. Sistēma izveidos jaunu plānoto pirkšanas pasūtījumu, pamatojoties uz negatīvo dienu periodu, kas tiek aprēķināts, izmantojot šādu formulu:

Izpildes laiks + Negatīvās dienas + Pašreizējais datums – Vajadzības datums

Sistēma izmanto tikai plānotos piegādes pasūtījumus, kas atrodas šajā periodā, un izveido jaunu plānoto pasūtījumu ārpus tā. Dinamisko negatīvo dienu priekšrocība ir tā, ka tajās tiks iekļauts atsevišķas preces izpildes laiks, lai atkārtoti izmantotu esošos pasūtījumus un izvairītos no tādu jaunu plānoto pasūtījumu izveidošanas, kuriem būs vēlāks datums izpildes laika izraisītās aizkaves dēļ. 

Plašāku informāciju skatiet tēmā [Negatīvās dienas un dinamiskās negatīvās dienas](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]