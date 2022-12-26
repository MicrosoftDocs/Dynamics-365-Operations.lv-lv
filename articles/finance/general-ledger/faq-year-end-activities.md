---
title: Bieži uzdotie jautājumi par gada beigu aktivitātēm
description: Šajā rakstā uzskaitīti jautājumi, kas var rasties, slēdzot gadu, un atbildes, kas var palīdzēt ar gada beigu slēgšanas darbībām.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853046"
---
# <a name="year-end-activities-faq"></a>Bieži uzdotie jautājumi par gada beigu aktivitātēm 

[!include [banner](../includes/banner.md)]

Šajā rakstā uzskaitīti jautājumi, kas var rasties, slēdzot gadu, un atbildes, kas var palīdzēt ar gada beigu slēgšanas darbībām. Šajā rakstā galvenokārt ir apskatīti jautājumi par gada beigu slēgšanas aktivitātēm virsgrāmatā un saistībā ar kreditoriem.

## <a name="general-ledger-year-end-enhancements"></a>Virsgrāmatas gada beigu uzlabojumi

Microsoft Dynamics 365 Finance versijā 10.0.20 tika ieviests gada beigu slēgšanas uzlabojums. Šis uzlabojums pēc noklusējuma tiek iespējots, sākot ar versiju 10.0.25, un ir obligāts, sākot ar versiju 10.0.29. Ja jūsu organizācija izmanto versiju, kas vecāka par 10.0.25, pirms gada beigu slēgšanas procesa uzsākšanas ieteicams iespējot šo līdzekli. Lai varētu izmantot šo līdzekli, sistēmā tas vispirms ir jāieslēdz. Administratori var izmantot darbvietu **Līdzekļu pārvaldība**, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šis līdzeklis ir uzskaitīts šādā veidā:

- **Modulis:** Virsgrāmata
- **Līdzekļa nosaukums:** Virsgrāmatas gada beigu uzlabojumi

Gada beigu slēgšanas veidņu iestatīšana tika pārvietota uz jaunu iestatīšanas lapu **Gada beigu slēgšanas veidnes iestatīšana**. Esošā gada beigu slēgšanas lapa būs līdzīga lapai **Virsgrāmatas ārvalstu valūtas pārvērtēšana**, kur saraksts tiek rādīts katru reizi, kad tiek izpildīta vai atsaukta gada beigu slēgšana. Lapā netiks rādīta vēsturiskā informācija par gada beigu noslēgšanām, kas tika veiktas pirms līdzekļa iespējošanas. Uzskaites vadītājs var uzsākt gada beigu slēgšanu no jaunās lapas.

Lai atsauktu gada beigu slēgšanu, atlasiet atbilstošās juridiskās personas visjaunāko finanšu gadu un pēc tam atlasiet pogu **Atsaukt gada beigu slēgšanu**. Atsaukšana automātiski dzēsīs iepriekšējā gada beigu slēgšanas uzskaites ierakstus un atkārtoti neveiks automātisku gada beigu slēgšanu. Ja iespējojat līdzekli **Virsgrāmatas gada beigu uzlabojumi** pēc tam, kad ir beigta gada beigu slēgšana, un vēlaties atgriezt vēsturiskos gada beigu rezultātus, izpildiet vēsturisko gada beigu slēgšanu vēlreiz pēc tam, kad ir iespējots virsgrāmatas parametrs **Dzēst esošos gada beigu slēgšanas ierakstus, kad atkārtoti slēdzat gadu**.

Gada beigu slēgšanu varat atkārtoti izpildīt, restartējot atbilstošā finanšu gada un juridiskās personas procesu. Process turpinās izmantot virsgrāmatas parametru iestatījumu, lai noteiktu, vai gada beigu slēgšanas atkārtota palaišana tiks ņemta vērā tikai jaunajām vai mainītajām transakcijām vai pilnībā atsauks iepriekšējo slēgšanu.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Virsgrāmata: ir iespējots līdzeklis Virsgrāmatas gada beigu uzlabojumi. Kāpēc gada slēgšanas lapas vēstures sadaļā nevar skatīt iepriekš veiktās gada beigu slēgšanas?

Pirms līdzekļa **Virsgrāmatas gada beigu uzlabojumi** iespējošanas tiek izsekots datums un laiks, kurā tika izpildīts nesenākais gada beigu slēgšanas process. Tas neizseko vēsturi par katru reizi, kad tika veikta gada beigu slēgšana. Tādējādi nav pieejama informācija par katru gada beigu slēgšanas izpildi, un to nevar parādīt. Pēc līdzekļa iespējošanas tiek saglabāta informācija par nākamajiem gada beigu slēgšanas procesiem. Dokumentus par visiem gada beigu slēgšanas procesiem, pat tiem, kas izpildīti pirms līdzekļa iespējošanas, var skatīt lapā **Dokumentu transakcijas**. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Virsgrāmata: gada beigu noslēgšanas process neizdodas šādas kļūdas dēļ: “Gada beigu slēgšanu nevar izpildīt, jo viena vai vairākas virsgrāmatas transakcijas, kuras iegrāmatojāt finanšu gadā, ko slēdzat, tika iekļautas virsgrāmatas transakcijā citā finanšu gadā.” Ko nozīmē šī kļūda?

Tā kā ir iespējots līdzeklis **Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana**, no sākuma bilances tiek izslēgta tikai iegrāmatotā virsgrāmatas transakcija no finanšu gada, kas tiek slēgts. Šī darbība izraisa debeta un kredīta bilances atšķirību. Plašāku informāciju skatiet rakstā [Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Virsgrāmata: gada beigu slēgšanas procesa atsaukšana neizdodas šādas kļūdas dēļ: “Gada beigu slēgšanu datumam 1.1.2022. nevar atsaukt, jo sākuma bilances transakcija ir iegrāmatota virsgrāmatā finanšu gadā, kas sākas 1.1.2023.” Ko nozīmē šī kļūda?

Tā kā ir iespējots līdzeklis **Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana**, gada slēgšanas procesu atsaukšana nav atļauta, ja sākuma transakcijas ir iegrāmatotas jaunā finanšu gadā. Atsauciet ierakstus virsgrāmatā jaunajā 2023. finanšu gadā, pirms atsaucat gada beigu slēgšanu 2022. gada 1. janvārim. Varat arī slēgt gadu vēlreiz 2022. gada 1. janvārim, taču tikai jaunajiem koriģēšanas ierakstiem. Lai vēlreiz slēgtu gadu tikai korekcijām, atspējojiet virsgrāmatas parametru **Esošo gada beigu ierakstu dzēšana, kad atkārtoti slēdzat gadu**.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Virsgrāmata: kāpēc virsgrāmatas norēķinu automatizācija neapstrādā decembra virsgrāmatas norēķinu transakcijas?

Līdzeklis **Automatizēt virsgrāmatas norēķinus** izpilda to transakciju automatizāciju, kuru datums ir no pirmās finanšu gada dienas līdz pašreizējam datumam, kad tiek veikta izpilde. Finanšu gadiem, kas beidzas 31. decembrī, iespējams, būs jākoriģē izpildes datums, lai nodrošinātu, ka izpilde tiek veikta decembrī. Piemēram, automatizācijas izpilde ir iestatīta katra mēneša pirmajā dienā. Šī automatizācija tiks izpildīta 2022. gada 1. decembrī, un tās izpilde tiks ieplānota 2023. gada 1. janvārī. Ieteicams mainīt 2023. gada 1. janvāra izpildi, lai tā tiktu veikta 2022. gada 31. decembrī. Šī izmaiņa nodrošinās to, ka transakcijas, kuru datums ir 2.–31. decembris, tiks ņemtas vērā, veicot automātiskos norēķinus.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Virsgrāmata: kāda ir atšķirība starp darbību “Atsaukt gada beigu slēgšanu” un parametru “Esošo gada beigu ierakstu dzēšana, kad atkārtoti veicat slēgšanu” gada beigu slēgšanā?

Iespējams, ka pastāv neskaidrība par atšķirību starp darbību **Atsaukt gada beigu slēgšanu** un parametru **Esošo gada beigu ierakstu dzēšana, kad atkārtoti veicat slēgšanu** virsgrāmatā (**Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmatas parametri**).

Palaižot gada beigu slēgšanas procesu, atlasiet darbību **Atsaukt gada beigu slēgšanu**, lai dzēstu visus beigu bilances un sākuma bilances ierakstus tā, it kā gada beigu slēgšana nekad nebūtu veikta. Šajā gadījumā dokumenti tiks izdzēsti. Gada beigu slēgšana vairs netiks automātiski izpildīta. Lai izpildītu gada beigu slēgšanu, atlasiet darbību **Izpildīt gada beigu slēgšanu**.

Virsgrāmatas parametrs **Esošo gada beigu ierakstu dzēšana, kad atkārtoti slēdzat gadu** tiek lietots tikai tad, kad izpildāt (nevis atsaucat) gada beigu slēgšanu. Ja parametra iestatījums ir **Jā**, visi beigu bilances un sākuma bilances ieraksti tiks dzēsti, un gada beigu slēgšana tiks izpildīta vēlreiz. Šī opcija tiek izmantota, kad organizācija vēlas, lai visas transakcijas, tostarp korekcijas kopš pēdējās gada beigu slēgšanas, tiktu grāmatotas vienā uzskaites ierakstā beigu bilances un sākuma bilances ierakstiem. Ja parametra iestatījums ir **Nē**, visi beigu bilances un sākuma bilances ieraksti paliek nemainīgi. Tie netiek dzēsti. Tā vietā tiek izveidots jauns beigu bilances un sākuma bilances ieraksts tikai starpībai vai jaunām transakcijām, kas ir iegrāmatotas kopš pēdējās gada beigu slēgšanas atbilstošajam finanšu gadam.

> [!NOTE]
> Beigu bilances ieraksts tiek izveidots slēgšanas gadā. Tas notiek tikai tad, ja virsgrāmatas parametra **Veidot slēgšanas darbības pārsūtīšanas laikā** iestatījums ir **Jā**. Sākuma bilances ieraksts vienmēr tiek izveidots, jo šī ir nākamā gada sākuma bilance.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Virsgrāmata: kāda ir atšķirība starp opciju “Slēgt visu” un “Slēgt vienu” gada beigu slēgšanas procesa sadaļā “Nodot peļņas un zaudējumu dimensijas”?

Opcija **Slēgt visu** nodrošina grāmatoto transakciju sākotnējo finanšu dimensiju vērtību saglabāšanu un izmantošanu nesadalītās peļņas konta sākuma bilanču izveidei. Katrai unikālajai finanšu dimensiju vērtību kombinācijai tiek izveidota atsevišķa nesadalītās peļņas sākuma bilance. Ja ir atlasīta opcija **Slēgt vienu**, visas grāmatotās transakcijas, kurām ir šī finanšu dimensija, tiek summētas nesadalītās peļņas sākuma bilancē tai dimensijas vērtībai, kas ir ievadīta laukā, kas parādās pēc opcijas **Slēgt vienu**. 

Piemēram, visas finanšu gada transakcijas tika grāmatotas, izmantojot konta struktūru Galvenais konts — Nodaļa. Finanšu dimensijai Nodaļa veidnē ir atlasīta opcija **Slēgt vienu** un ir ievadīts 100 kā dimensijas vērtība. Ja visu nodaļā Nr. 200, 300 un 400 grāmatoto transakciju ieņēmumu kopsumma ir $100 000, tiek izveidota viena sākuma bilance opcijai Nesadalītā peļņa - 100. Ja atlasāt opciju **Slēgt vienu**, bet atstājat finanšu dimensijas vērtību tukšu, nesadalītajā peļņā tiek grāmatotas visas transakcijas, un dimensijas vērtība būs tukša.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Virsgrāmata: ja atlasu opciju “Slēgt vienu” gada beigu slēgšanas procesa sadaļā “Nodot peļņas un zaudējumu dimensijas”, vai tiks zaudēta detalizēta informācija par transakciju?

Opcijas **Slēgt visu** un **Slēgt vienu** tiek izmantotas, lai norādītu, kuras peļņas un zaudējumu kontos grāmatoto transakciju finanšu dimensijas ir jāpārsūta uz nesadalītās peļņas galveno kontu. Vēsturiskie, detalizētie grāmatojumi peļņas un zaudējumu aprēķinā netiek ietekmēti un saglabāsies ar informāciju. Opcija ietekmē tās informācijas detalizācijas līmeni, kas tiek nodota uz nesadalītās peļņas kontiem kā sākuma bilance nākamajā gadā. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Virsgrāmata: gada beigu slēgšanas process neizdodas, jo gada pārskata valūta nav bilancē. Ko šis nozīmē?

Šī kļūda var rasties pēc tam, kad tiek iespējots līdzeklis **Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana** (Apzināšanas līdzeklis). Kad līdzeklis ir iespējots, virsgrāmatas transakcijas, par kurām ir veikti norēķini, vairs netiks iekļautas nākamā finanšu gada sākuma bilancē, kad tiks izpildīta virsgrāmatas gada beigu slēgšana. Izslēdzot virsgrāmatas transakcijas, par kurām ir veikti norēķini, klientiem gada beigu slēgšanā var rasties izaicinājumi, ja virsgrāmata ir definēta ar pārskata valūtu.   
Virsgrāmatas norēķini tiek veikti tikai uzskaites valūtai.  Kad par virsgrāmatas transakcijām ir veikti norēķini, apstiprināšana nodrošina tikai to, ka debitoru summa uzskaites valūtā ir vienāda ar kredītu uzskaites valūtā. Pārskata valūtas summas šīm virsgrāmatas transakcijām netiek apstiprinātas, un to debitoru un kreditoru summas var nebūt vienādas.  Turklāt virsgrāmatas norēķini automātiski neaprēķina un neiegrāmato peļņu/zaudējumus pārskata valūtā.  Šo ierobežojumu dēļ darījumam ir jābūt peļņas/zaudējumu pārskata valūtā, kad tiek veikti virsgrāmatas norēķini.  Ja peļņa/zaudējumi netiek iekļauti virsgrāmatas norēķinos, veicot gada beigu slēgšanu, tiks saņemts ziņojums par bilances nesakritību.  Papildinformāciju skatiet rakstā [Virsgrāmatas norēķinu līdzekļa un pārskata valūtas bilances neatbilstība](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Virsgrāmata: kas jāmaina, lai palīdzētu uzlabot gada beigu apstrādes veiktspēju?

Lai uzlabotu gada beigu slēgšanas veiktspēju, var veikt vairākas izmaiņas. Ieteicams novērtēt šīs ieteiktās izmaiņas, lai noteiktu, vai tās atbilst jūsu organizācijai.

### <a name="optimize-year-end-close-service"></a>Pakalpojums Gada beigu slēgšanas optimizācija

Pakalpojums **Gada beigu slēgšanas optimizācija** sniedz iespēju Microsoft Dynamics 365 Finance klientiem paātrināt gada beigu noslēgšanu, nododot smago gada beigu datu apstrādi mikropakalpojumam. Laiks, kas tiek ietaupīts, ja gada beigu slēgšana notiek efektīvi, sniedz iespēju katrai Finance darba grupai finanšu pārskatu sagatavošanas procesā reaģēt laikus, ja ir nepieciešamas korekcijas. Veicot gada beigu slēgšanu mikropakalpojumā, tiek atbrīvoti vērtīgi resursi. Apstrādes veikšana citā līmenī samazina SQL Server slodzi un sniedz klientiem iespēju paātrināt gada beigu slēgšanas datu apstrādi.

Pakalpojums **Gada beigu slēgšanas optimizācija** ir pieejams versijā 10.0.31, lai vairāk klientu varētu lietot jauno pakalpojumu 2022. gada beigu sezonā. Turklāt pakalpojums ir atpakaļpārnests arī uz versiju 10.0.30 un 10.0.29. Papildinformāciju skatiet rakstā [Gada beigu slēgšanas optimizācija](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensiju kopas

Izpildot gada beigu slēgšanas procesu, tiek atjaunota katra dimensiju kopas bilance. Šāda darbība tieši ietekmē veiktspēju. Dažas organizācijas bez vajadzības izveido dimensiju kopas, jo tās tika kādreiz izmantotas vai arī kādreiz var tikt izmantotas. Tā kā šīs nevajadzīgās dimensiju kopas tiek atjaunotas gada beigu slēgšanā, process notiek ilgāk. Atvēliet laiku, lai novērtētu savas dimensiju kopas un dzēstu nevajadzīgās.

Nevajadzīgās dimensiju kopas ietekmē arī pakešuzdevumu **BudgetDimensionFocusInitializeBalance** (**Virsgrāmata \> Kontu plāns \> Dimensijas \> Finanšu dimensiju kopas**).

[![Finanšu dimensiju kopas.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Gada beigu slēgšanas veidnes konfigurācija

Gada beigu slēgšanas veidne ļauj organizācijām atlasīt finanšu dimensijas līmeni, ko uzturēt, pārsūtot peļņas un zaudējumu bilances uz nesadalīto peļņu. Iestatījumi ļauj organizācijai uzturēt detalizētas finanšu dimensijas (**Slēgt visu**), pārvietojot bilances uz nesadalīto peļņu vai izvēloties apkopot summas uz vienu dimensijas vērtību (**Slēgt vienu**). To var noteikt katrai finanšu dimensijai. Plašāku informāciju par šiem iestatījumiem skatiet rakstā [Gada beigu slēgšana](year-end-close.md).

Lai uzlabotu veiktspēju, ieteicams novērtēt organizācijas prasības un, ja iespējams, aizvērt tik daudz dimensiju, cik iespējams, izmantojot gada beigu opciju **Slēgt vienu**. Noslēdzot uz vienu dimensijas vērtību (kas var būt arī tukša vērtība), sistēma aprēķina mazāk detaļu, kad tiek aprēķinātas nesadalītās peļņas konta ierakstu bilances.

### <a name="degenerate-dimensions"></a>Deģenerētās dimensijas

Deģenerētā dimensija pati par sevi un kombinācijā ar citām dimensijām nesniedz praktiski nekādu atkārtotas izmantošanas labumu. Pastāv divu veidu deģenerētās dimensijas. Pirmais veids ir dimensija, kas ir individuāli deģenerēta. Parasti šis deģenerētās dimensijas veids būs tikai vienai transakcijai vai mazām transakciju kopām. Otrs veids ir dimensija, kas kļūst deģenerēta kombinācijā ar vienu vai vairākām papildu dimensijām, kuras nodrošina to pašu potenciālu, balstoties uz iespējamām permutācijām, ko var deģenerēt. Deģenerātā dimensija var būtiski ietekmēt gada beigu slēgšanas procesa veiktspēju. Lai minimizētu veiktspējas problēmas, gada beigu slēgšanas iestatījumā definējiet visas deģenerētās dimensijas kā **Slēgt vienu**, kā tas ir aprakstīts iepriekšējā sadaļā.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Kreditori: kādas izmaiņas ir veiktas, lai atbalstītu 1099 gada beigu pārskatu 2022. gadam?

#### <a name="update-to-all-1099-forms"></a>Atjaunināt visās 1099 veidlapās

Visās 1099 veidlapās 2022. taksācijas gadā ir veiktas šādas izmaiņas:

- 2021. gadā 1099 veidlapās tika fiksēts gads. Sākot no 2022. gada, gads tiek aizpildīts, veidojot pārskatu.

#### <a name="1099-misc"></a>1099-MISC

Visās 1099-MISC veidlapās 2022. taksācijas gadā ir veikti šādi atjauninājumi:

- 13. lauks: tagad norāda Ārzemju konta nodokļu atbilstības likuma (FATCA) aizpildīšanas prasību.
- 14. lauks: tagad tiek izmantots, lai ziņotu par “zelta izpletņa” pārsnieguma maksājumiem.
- 15. lauks: tagad tiek izmantots, lai ziņotu par maksājumu nekvalificētos atlikto atlīdzību (NQDC) plānos.
- 16. lauks: tagad tiek izmantots, lai ziņotu par ieturētajiem nodokļiem.
- 17. lauks: tagad tiek izmantots, lai ziņotu par maksātāja apgabala numuru.
- 18. lauks: tagad tiek izmantots, lai ziņotu par apgabala ienākumu nodokli.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Kreditori: 1099 — kā var mainīt 1099 lodziņu un vērtības kreditoram, kurš gada laikā nesekoja 1099 informācijai?

Izmantojiet funkcionalitāti **Atjaunināt 1099**, lai apskatītu iepriekš apmaksātos rēķinus un pareizi piešķirtu 1099 datus atbilstoši iestatījumiem lapas **Kreditors** cilnē **Nodoklis 1099**. Lai izmantotu funkciju **Atjaunināt 1099**, dodieties uz sadaļu **Kreditori \> Piegādātāji \> Visi piegādātāji**, atlasiet piegādātāju un pēc tam rūts Darbība cilnē **Piegādātājs** atlasiet **Atjaunināt 1099**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Vai var palaist funkciju Atjaunināt 1099 visiem kreditoriem vienlaicīgi?

Lai atjauninātu lodziņu 1099 kreditora ierakstā un atjauninātu transakcijas ar informāciju no lodziņa 1099, varat izmantot lapu **Atjaunināt 1099 informāciju vairākiem kreditoriem**. Lai atvērtu šo lapu, dodieties uz sadaļu **Kreditori \> Periodisks uzdevums \> Nodoklis 1099**. Lai piekļūtu lapai, jums ir jābūt piešķirtai drošības atļaujai saistībā ar opciju **Atjaunināt 1099 lauciņu un transakcijas vairākiem kreditoriem**.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Kreditori: 1099 — “Pārrēķināt esošās 1099 summas” salīdzinājumā ar “Atjaunināt visu” atjauninājuma 1099 utilītā

Izvēles rūtiņa **Pārrēķināt esošās 1099 summas** atiestata 1099 summu uz kopējām apmaksātajām vērtībām, ja tā tiek izmantota kopā ar izvēles rūtiņu **Atjaunināt visu**.

[![Nodokļa 1099 transakcijas: pirms atjaunināšanas rutīnas izpildes.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Izvēles rūtiņa **Pārrēķināt esošās 1099 summas** stājas spēkā tikai tad, ja rēķinā ir daļējas 1099 vērtības vai arī rēķins ir modificēts veidlapā Nodoklis 1099. Piemēram, jums ir rēķins, kura summa ir 1000,00 $, bet lietotājs rēķinā manuāli ieraksta 1099 summu 500,00 $.

[![Nodokļa 1099 transakcijas: izvēles rūtiņas “Atjaunināt visu” un “Pārrēķināt esošās 1099 summas” atzīmēšana.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Kad šis rēķins būs apmaksāts, 500,00 $ būs samaksātā 1099 summa. Veicot pārrēķināšanu, 1099 summa tiks mainīta uz 1000,00 $, kas ir kopējā samaksātā summa.

[![Nodokļa 1099 transakcijas: pēc 1099 rutīnas lietošanas.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Parādi kreditoriem: 1099 — manuāli izveidojiet 1099 transakcijas

Iespējams, organizācijai būs manuāli jāizveido 1099 transakcijas, kas nav saistītas ar rēķinu. Manuālas 1099 transakcijas var pievienot, dodoties uz **Parādi kreditoriem \> Periodiskie uzdevumi \> Nodoklis 1099 \> Kreditora nodokļa 1099 nosegšana**. Izvēlieties pogu **Manuālās 1099 transakcijas**.

Manuāli izveidotas 1099 transakcijas netiek atjauninātas, izmantojot procesu **Atjaunināt visu** vai **Pārrēķināt esošās 1099 summas** utilītā **Atjaunināt 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Kreditori: 1099 — vai Dynamics 365 Finance atbalsta veidlapu 1096?

Dynamics 365 Finance nedrukā 1096 gada kopsavilkumu un veidlapu ASV Informācijas atgriešanas pārsūtīšana.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Parādi kreditoriem: 1099 — vai ir kāds jauns līdzeklis, kas atbalsta 1099 pārskatu sniegšanu publiskajā sektorā?

Ir pievienots jauns publiskā sektora līdzeklis **Atjaunināt 1099 informāciju pēc galvenā konta**, ko var iespējot darbvietā **Līdzekļu pārvaldība**. Šis līdzeklis ļauj saistīt 1099 kreditora vērtības ar galveno kontu uzskaites sadalē, nevis ar kreditora ieraksta noklusējuma kontu.

Papildinformāciju skatiet rakstā [Kreditoru iestatīšana 1099 pārskatu veidošanai](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
