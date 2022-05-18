---
title: Viens dokuments
description: Viens dokuments ļauj finanšu žurnālos (virsgrāmatas žurnālā, pamatlīdzekļu žurnālā, kreditoru maksājumu žurnālā u. c. žurnālos) ievadīt vairākas apakšgrāmatas transakcijas saistībā ar vienu dokumentu.
author: kweekley
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 9a0a9a3f23a3aec0077fd1a64c55fea567b72800
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722497"
---
# <a name="one-voucher"></a>Viens dokuments

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


## <a name="what-is-one-voucher"></a>Kas ir Viens dokuments?

Esošā funkcionalitāte jums ļauj finanšu žurnālos (vispārējā žurnālā, pamatlīdzekļu žurnālā, kreditoru maksājumu žurnālā un citos žurnālos) ievadīt vairākas apakšgrāmatas transakcijas (debitora, kreditora, pamatlīdzekļu, projekta un banku) viena dokumenta kontekstā. Microsoft šo funkcionalitāti apzīmē kā *Viens dokuments*. Vienu dokumentu varat izveidot, izmantojot vienu no tālāk aprakstītajām metodēm.

- Iestatiet žurnāla nosaukumu (**Virsgrāmata** \> **Žurnāla iestatīšana** \> **Žurnālu nosaukumi**) tā, lai lauks **Jauns dokuments** būtu iestatīts uz **Tikai viena dokumenta numurs**. Tagad visas rindas, ko pievienojat šim žurnālam, tiek ietvertas tajā pašā dokumentā. Tādēļ šo dokumentu var ievadīt kā vairāku rindu dokumentu, kā tās pašas rindas kontu/korespondējošo kontu vai kā kombināciju.

    [![Atsevišķas rindas.](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Viena dokumenta definīcija **neattiecas** uz gadījumiem, kur žurnālu nosaukumi ir iestatīti kā **Tikai viena dokumenta numurs**, bet pēc tam lietotājs ievada dokumentu, kurā ir tikai Virsgrāmatas kontu tipi. Šajā tēmā Viens dokuments nozīmē, ka pastāv viens dokuments, kurā ir vairāki kreditori, debitori, bankas, pamatlīdzekļi vai projekti.

- Ievadiet vairāku rindu dokumentu, kurā nav norādīts korespondējošais konts.

    [![Vairāku rindu dokuments.](./media/Multi-line.png)](./media/Multi-line.png)

- Ievadiet dokumentu, kurā gan kontā, gan korespondējošajā kontā ir apakšgrāmatas konta tips, piemēram, **Kreditors**/**Kreditors**, **Debitors**/**Debitors**, **Kreditors**/**Debitors** vai **Banka**/**Banka**.

    [![Apakšgrāmatas dokuments.](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Funkcionalitātes Viens dokuments problēmas

Funkcionalitātē Viens dokuments var rasties problēmas, veicot nosegšanu, aprēķinot nodokļus, anulējot transakcijas, saskaņojot apakšgrāmatu ar Virsgrāmatu, veidojot finanšu pārskatus un veicot citas darbības. (Papildinformāciju par problēmām, kas var rasties, veicot nosegšanu, skatiet, piemēram, rakstā [Viens dokuments ar vairākiem debitoru vai kreditoru ierakstiem](../accounts-payable/single-voucher-multiple-customer-vendor-records.md).) Lai šie procesi darbotos un pārskati tiktu izveidoti pareizi, šiem procesiem un pārskatiem ir nepieciešami transakcijas dati. Lai gan dažos scenārijos viss var darboties pareizi, atkarībā no jūsu organizācijas iestatījumiem, problēmas bieži rodas, ja vienā dokumentā ir ievadītas vairākas transakcijas.

Piemēram, jūs iegrāmatojat tālāk norādīto vairāku rindu dokumentu.

[![Vairāku rindu dokumenta piemērs.](./media/example.png)](./media/example.png)

Pēc tam ģenerējat pārskatu **Izdevumi pēc kreditora** darbvietā **Finanšu ieskati**. Šajā pārskatā izdevumu konta bilances tiek grupētas pēc kreditoru grupas un pēc tam — pēc kreditora. Kad tiek ģenerēts pārskats, sistēma nevar noteikt, kuras kreditoru grupas/kreditori ir radījuši izdevumus 250,00 apmērā. Tā kā trūkst transakcijas datu, sistēma pieņem, ka visus izdevumus 250,00 apmērā izraisīja pirmais dokumentā atrodamais kreditors. Tādēļ izdevumu summa 250,00, kas ir ietverta galvenā konta 600120 bilancē, tiek rādīta pie attiecīgās kreditoru grupas/kreditora. Taču ir ļoti iespējams, ka pirmais dokumentā atrodamais kreditors nav īstais kreditors. Tādēļ pārskats, visticamāk, ir nepareizs.

[![Pārskats Izdevumi pēc kreditora.](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Funkcionalitātes Viens dokuments turpmākais izmantojums

Sakarā ar problēmām, kas var rasties, izmantojot Viens dokuments, šī funkcionalitāte galu galā būs novecojusi. Tomēr, tā kā pastāv funkcionāli trūkumi, kas ir atkarīgi no šīs funkcionalitātes, novecošana nenotiks uzreiz. Tā vietā tiks izmantots tālāk norādītais grafiks.

- **2018. gada pavasara laidiens** — šī funkcionalitāte tika izslēgta, izmantojot lapas **Virsgrāmatas parametri** cilnes **Vispārīgi** parametru **Atļaut vairākas transakcijas vienā dokumentā**. Tomēr varat to atkārtoti ieslēgt, ja jūsu organizācijā tiek izmantots kāds no tālāk šajā tēmā uzskaitītajiem scenārijiem funkcionālo trūkumu novēršanai.

    - Ja biznesa scenārijā nav vajadzīgs Viens dokuments, ieteicams atstāt funkcionalitāti izslēgtu. Microsoft nelabos kļūdas šajā tēmā tālāk norādītajās jomās, ja šī funkcionalitāte tiek izmantota, kaut gan pastāv cits risinājums.
    - Ieteicams pārtraukt Viens dokuments izmantošanu integrācijai, ja vien funkcionalitāte nepieciešama kāda funkcionālā trūkuma novēršanai.

- **Vēlāki laidieni** – vairākas no šīm biznesa darbībām ir izpildāmas, tikai izmantojot Viens dokuments. Microsoft jānodrošina, lai pēc funkcionalitātes novecošanas sistēmā joprojām tiktu izpildītas visas identificētās biznesa darbības. Tāpēc, iespējams, būs jāpievieno jauni līdzekļi, lai aizpildītu funkcionālos trūkumus. Microsoft nevar nodrošināt konkrētu risinājumu, jo katra līdzekļa trūkumi atšķiras un ir jāizvērtē, pamatojoties uz biznesa darbībām. Daži funkcionālie trūkumi, iespējams, tiks aizstāti ar līdzekļiem, kas palīdz izpildīt noteiktas biznesa darbības. Tomēr citus trūkumus var novērst, turpinot atļaut ierakstus žurnālā, it kā izmantojot Vienu dokumentu, bet uzlabojot sistēmu, lai pēc vajadzības izsekotu detalizētāku informāciju.

Kad būs novērsti visi funkcionālie trūkumi, Microsoft paziņos, ka līdzeklis kļūs novecojis. Tomēr novecošana nebūs spēkā vismaz vienu gadu pēc šī paziņojuma. Lai gan Microsoft nevar sniegt novērtējumu par to, kad Viena dokumenta funkcionalitāte būs novecojusi, iespējams, ka tas būs vismaz pēc diviem gadiem. Microsoft politika ir ieturēt vismaz 12 mēnešus starp paziņojumu par novecojušu funkcionalitāti un faktisko novecošanu, tādējādi debitoriem un neatkarīgiem programmatūras kreditoriem (ISV) ir laiks, lai reaģētu uz izmaiņām. Piemēram, organizācijai varētu būt nepieciešams atjaunināt savus biznesa procesus, elementus un integrācijas.

Viena dokumenta novecošana ir būtiska izmaiņa, par ko tiks plaši brīdināts. Kā daļa no šīs komunikācijas Microsoft atjauninās šo tēmu, iegrāmatojiet tiešsaistes Microsoft Dynamics ziņu 365 Finanses, atjauniniet tēmu "Noņemts vai novecojis", komunicē ar izmaiņām attiecīgajās Microsoft konferencēs un tā tālāk.

## <a name="why-use-one-voucher"></a>Kādos gadījumos izmantot funkcionalitāti Viens dokuments?

Pamatojoties uz sarunām ar klientiem, tālāk norādītajā sarakstā Microsoft apkopoja scenārijus, kādos klienti izmanto funkcionalitāti Viens dokuments, vai iemeslus, kāpēc viņi šo funkcionalitāti izmanto. Dažas no šīm biznesa darbībām ir izpildāmas, tikai izmantojot funkcionalitāti Viens dokuments. Tomēr daudzos scenārijos noteiktas biznesa darbības var izpildīt, izmantojot citus risinājumus.

### <a name="scenarios-that-require-one-voucher"></a>Scenāriji, kādos nepieciešams izmantot funkcionalitāti Viens dokuments

Tālāk norādītajos scenārijos noteiktas darbības ir izpildāmas, tikai izmantojot funkcionalitāti Viens dokuments. Ja jūsu organizācijā tiek izmantots jebkurš no šiem scenārijiem, jums ir jāiespējo vairāku transakciju ievadīšana vienā dokumentā, mainot parametra **Atļaut vairākas transakcijas vienā dokumentā** iestatījumu lapā **Virsgrāmatas parametri**. Šī trūkstošā funkcionalitāte tiks nodrošināta, izmantojot citus līdzekļus vēlākos laidienos.

> [!NOTE]
> [Katrai no sekojošajām situācijām lauks **Atļaut vairākas darbības vienā dokumentā** ir jāiestata uz Jā, kopsavilkuma cilnē **Vispārīgi** lapā **Virsgrāmatas parametri**.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Kreditora vai debitora maksājumu grāmatošana bankas kontā kopsavilkuma formā

**Scenārijs.** Organizācija savā bankā iesniedz sarakstu ar kreditoriem un summām, un banka izmanto šo sarakstu, lai veiktu maksājumus kreditoriem organizācijas vārdā. Banka iegrāmato maksājumu summu bankas kontā kā vienu atvilkumu.

Kopsavilkuma izveide par kreditoru maksājumiem tiek atbalstīta tikai funkcionalitātē Viens dokuments. Katrs kreditors tiek ievadīts kā atsevišķa rinda, lai uzturētu informāciju apakšgrāmatā Parādi kreditoriem. Taču visu maksājumu kopsumma tiek novirzīta uz vienu bankas konta rindu. Tādējādi atvilkums bankas apakšgrāmatā tiek parādīts kā viena kopsumma.

**Scenārijs.** Organizācija deponē debitoru maksājumus, vai banka deponē debitoru maksājumus organizācijas vārdā, un depozīts bankas kontā tiek rādīts kā vienreizēja izmaksa.

Debitoru maksājumu kopsavilkuma izveide parasti tiek atbalstīta, izmantojot depozīta funkcionalitāti. Tomēr, ja jūs maksājuma metodei izmantojat opciju “pagaidu”, šis scenārijs tiek atbalstīts, tikai izmantojot funkcionalitāti Viens dokuments. Debitoru maksājumi tiek ievadīti tādā pašā veidā, kā norādīts par kreditoru maksājumu kopsavilkuma izveidi.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Biznesa notikuma transakciju grupēšanas mehānisms

**Scenārijs.** Organizācijai ir viens biznesa notikums, kas izraisa vairākas transakcijas. Tomēr grāmatvedības nodaļa vēlas skatīt visus uzskaites ierakstus kopā, lai varētu efektīvāk veikt auditu.

Ja organizācijai ir nepieciešams skatīt visus biznesa notikuma uzskaites ierakstus kopā, ir jāizmanto funkcionalitāte Viens dokuments. 

### <a name="country-specific-features"></a>Noteiktās valstīs izmantojami līdzekļi

**Scenārijs.** Līdzekļa Vienkāršais administratīvais dokuments (SAD) darbības nodrošināšanai Polijā pašlaik ir nepieciešams izmantot vienu dokumentu. Jums ir jāturpina izmantot funkcionalitāte Viens dokuments, līdz šim līdzeklim būs pieejama grupēšanas opcija. Iespējami arī citi noteiktās valstīs izmantojami līdzekļi, kuriem ir nepieciešams izmantot funkcionalitāti Viens dokuments.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Debitoru priekšapmaksas maksājumu žurnāls, kurā nodokļi ir norādīti vairākās rindās

Šādā gadījumā vienā dokumentā norādītie debitori atbilst vienam un tam pašam debitoram, jo transakcija simulē debitora pasūtījuma rindas. Priekšapmaksas dati ir jāievada vienā dokumentā, jo nodokļu aprēķināšana ir jāveic debitora veiktā viena maksājuma rindās.

### <a name="customer-reimbursement"></a>Debitoru kompensācija

**Scenārijs.** Debitors veic priekšapmaksu par pasūtījumu, un pasūtījuma rindās ir norādīti dažādi nodokļi, kas ir jāreģistrē, veicot priekšapmaksu. Debitora priekšapmaksas maksājums ir viena transakcija, kas simulē pasūtījuma rindas, lai attiecīgo nodokli varētu ierakstīt katrā summas rindā.

Ja kompensācijas periodiskais uzdevums tiek palaists no moduļa Debitoru parādi, tas izveido transakciju bilances pārvietošanai no debitora uz kreditoru. Šī scenārija nolūkos ir jāizmanto funkcionalitāte Viens dokuments, lai debitoram izsniegtu kompensāciju.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Pamatlīdzekļu uzturēšana: nolietojums ar atpakaļejošu datumu, līdzekļa sadalīšana, nolietojuma aprēķināšana izslēgšanas gadā
Ar versiju 10.0.21 un vēlākām versijām pamatlīdzekļu darbības nolietojumam ar atvasināto nolietojumu, pamatlīdzekļa sadalījumu un pamatlīdzekļa izslēgšanas nolietojuma aprēķinu tiek izveidotas, izmantojot dažādus dokumentu numurus.

### <a name="bills-of-exchange-and-promissory-notes"></a>Vekseļi un parādzīmes
Vekseļiem un parādzīmēm ir nepieciešams, lai tiktu lietota funkcionalitāte Viens dokuments, jo ar transakcijām debitora vai kreditora bilance tiek pārvietota no viena Virsgrāmatas konta Debitoru parādi/Parādi kreditoriem uz citu, balstoties uz maksājuma stāvokli.

## <a name="scenarios-that-dont-require-one-voucher"></a>Scenāriji, kādos izmantot funkcionalitāti Viens dokuments nav nepieciešams

Tālāk norādītos scenārijus var izpildīt, izmantojot citus līdzekļus, tādēļ nevajadzētu lietot funkcionalitāti Viens dokuments.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Debitora maksājumu grāmatošana bankas kontā kopsavilkuma formā

Organizācija deponē debitoru maksājumus, vai banka deponē debitoru maksājumus organizācijas vārdā, un depozīts bankas kontā tiek rādīts kā vienreizēja izmaksa.

Ja maksāšanas metodei netiek izmantota opcija “pagaidu”, debitoru maksājumu kopsavilkuma izveide tiek atbalstīta, izmantojot depozīta funkcionalitāti.

### <a name="netting"></a>Tīkli

Tīklā kreditora un debitora bilances tiek salīdzinātas viena ar otru, jo kreditors un debitors ir viena un tā pati puse. Šī pieeja minimizē naudas apmaiņas plūsmu starp organizāciju un debitora/kreditora pusi.

Tīklu var izveidot, ievadot pieaugumu un samazinājumu atsevišķos dokumentos un pēc tam iegrāmatojot novirzīšanu uz norēķinu Virsgrāmatas kontu.

### <a name="post-in-summary-to-the-general-ledger"></a>Kopsavilkuma grāmatošana Virsgrāmatā

Organizācijas bieži vēlas Virsgrāmatā grāmatot kopsavilkuma formā, lai samazinātu datu apjomu. Taču šīm organizācijām parasti joprojām ir nepieciešams uzturēt šo transakciju datus. Ja grāmatošana tiek veikta kopsavilkuma formā, izmantojot vienu dokumentu, transakciju dati nav zināmi un tos nevar saglabāt.

- Tā kā transakciju datus pašlaik nevar uzturēt, grāmatošanai kopsavilkuma formā organizācijām ir ieteicams **neizmantot** funkcionalitāti Viens dokuments.
- Pēc funkcionalitātes Viens dokuments noņemšanas žurnālos var ieviest struktūras Pirmdokuments un Uzskaite. Šīs struktūras nodrošinās transakciju datu uzturēšanu un kopsavilkuma izveidi Virsgrāmatā.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Vairāku neiegrāmatotu maksājumu segšana, izmantojot vienu rēķinu

Šis scenārijs parasti attiecas uz organizācijām, kur debitori var izmantot vairākas maksājuma metodes, lai norēķinātos par pirkumiem. Šādā gadījumā organizācijai ir nepieciešams reģistrēt vairākus negrāmatotus maksājumus un segt tos atbilstoši debitora rēķinam.

Jauns līdzeklis, kas ir pievienots Microsoft Dynamics 365 for Operations versijā 1611 (2016. gada novembris), sniedz iespēju nosegt vairākus negrāmatotus maksājumus, izmantojot vienu rēķinu. Vairāki debitoru maksājumi vairs nav jāievada vienā dokumentā.

### <a name="import-bank-statement-transactions"></a>Bankas izraksta transakciju importēšana

Bankas bieži veic un saņem maksājumus organizācijas vārdā, un šīs transakcijas tiek reģistrētas programmā Finance, izmantojot no bankas saņemtu failu. Organizācijām bieži ir nepieciešams šādas transakcijas sagrupēt, izmantojot failā norādīto bankas izraksta numuru. Tā kā bankas izrakstā tiek parādīta detalizēta informācija par katru transakciju, bankas apakšgrāmatā nav nepieciešams grāmatot kopsavilkumu.

Transakcijas var tikt sagrupētas, izmantojot citus žurnāla laukus, piemēram, žurnāla pakešuzdevuma numuru vai dokumenta numuru.


### <a name="transfer-balances"></a>Pārsūtīt bilances

Organizācijai, iespējams, būs nepieciešams pārsūtīt viena kreditora bilanci citam kreditoram, vai nu tāpēc, ka radusies kļūda, vai tāpēc, ka atbildība ir piešķirta citam kreditoram. Šāda veida pārsūtīšana rodas arī kontu tipiem, piemēram, kontiem **Debitori** un **Banka**.

Bilances pārsūtīšanu no viena konta (kreditora, debitora, bankas un citiem kontiem) uz citu kontu var veikt, izmantojot atsevišķus dokumentus, un novirzīšanu var grāmatot uz norēķinu Virsgrāmatas kontu.

### <a name="enter-beginning-balances"></a>Sākuma bilanču ievadīšana

Organizācijas bieži ievada sākuma bilances apakšgrāmatas kontiem (kreditoriem, debitoriem, pamatlīdzekļiem u. c. kontiem) kā viena dokumenta transakciju. Sākuma bilances katram apakšgrāmatas kontam var ievadīt kā atsevišķus dokumentus, un nobīdi var iegrāmatot norēķinu Virsgrāmatas kontā.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Iegrāmatota debitora vai kreditora dokumenta uzskaites ieraksta labošana

Organizācijai var būt nepieciešams labot debitoru vai kreditoru Virsgrāmatas kontā iegrāmatota rēķina uzskaites ierakstu, bet šo rēķinu nevar atsaukt vai labot, izmantojot citu mehānismu.

Ja labojums ir jāveic Virsgrāmatas kontā Debitoru parādi vai Parādi kreditoriem, korekcija ir jāveic tieši Virsgrāmatas kontā. Korekciju nevar veikt, izmantojot iegrāmatošanu kreditora vai debitora kontā. Izmantojot šo pieeju, korekciju ir iespējams veikt tikai laikā, kamēr sistēma netiek lietota un Virsgrāmatas kontā īslaicīgi ir atļauts veikt manuālu ievadi.

### <a name="the-system-allows-it"></a>Funkcionalitāte ir pieejama sistēmā

Organizācijas, neizprotot sekas, bieži izmanto funkcionalitāti Viens dokuments tikai tāpēc, ka sistēma ļauj to izmantot.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
