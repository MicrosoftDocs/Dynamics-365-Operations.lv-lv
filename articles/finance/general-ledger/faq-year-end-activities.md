---
title: Bieži uzdotie jautājumi par gada beigu aktivitātēm
description: Šajā rakstā uzskaitīti jautājumi, kas var rasties, slēdzot gadu, un atbildes, kas var palīdzēt ar gada beigu slēgšanas darbībām.
author: moaamer
ms.date: 11/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a75d1e3e68837a437b2369ba369b0063e015b12
ms.sourcegitcommit: 78cbb125f20a33df38bda0546203b8f837cbcd93
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/09/2022
ms.locfileid: "9751963"
---
# <a name="year-end-activities-faq"></a>Bieži uzdotie jautājumi par gada beigu aktivitātēm 

[!include [banner](../includes/banner.md)]

Šajā rakstā uzskaitīti jautājumi, kas var rasties, slēdzot gadu, un atbildes, kas var palīdzēt ar gada beigu slēgšanas darbībām. Šajā rakstā galvenokārt ir apskatīti jautājumi par gada beigu slēgšanas aktivitātēm virsgrāmatai un kreditoriem.

## <a name="general-ledger-year-end-enhancements"></a>Virsgrāmatas gada beigu uzlabojumi 
Versijā 10.0.20 tika ieviests gada beigu slēgšanas uzlabojums, kas ir aktivizēts pēc noklusējuma, sākot ar versiju 10.0.25. Ja jūsu organizācija izmanto versiju, kas vecāka par 10.0.25, pirms gada beigu slēgšanas procesa uzsākšanas ieteicams iespējot šo līdzekli. Lai varētu izmantot šo līdzekli, sistēmā tas vispirms ir jāiespējo. Administratori var izmantot Līdzekļu pārvaldības darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šis līdzeklis ir uzskaitīts šādā veidā:

 - Modulis: Virsgrāmata
 - Līdzekļa nosaukums: Virsgrāmatas gada beigu uzlabojumi

Gada beigu slēgšanas veidņu iestatīšana tika pārvietota uz jaunu iestatīšanas lapu **Gada beigu slēgšanas veidnes iestatīšana**. Esošā gada beigu slēgšanas lapa mainīsies tādā veidā, kas līdzīgs virsgrāmatas ārvalstu valūtas pārvērtēšanai, kur saraksts tiek rādīts katru reizi, kad tiek palaista vai atsaukta gada beigu slēgšana. Uzskaites vadītājs var uzsākt gada beigu slēgšanu no jaunās lapas. 

Lai atsauktu gada beigu slēgšanu, atlasiet atbilstošās juridiskās personas visjaunāko finanšu gadu un izvēlieties pogu **Atsaukt gada beigu slēgšanu**. Atsaukšana automātiski dzēsīs iepriekšējā gada beigu slēgšanas uzskaites ierakstus un atkārtoti neveiks automātisku gada beigu slēgšanu. 

Gada beigu slēgšanu varat atkārtoti palaist, restartējot atbilstošā finanšu gada un juridiskās personas procesu. Process turpinās izmantot virsgrāmatas parametru iestatījumus, lai noteiktu, vai gada beigu slēgšanas atkārtota palaišana tiks ņemta vērā tikai jaunajām vai mainītajām transakcijām vai pilnībā atsauks iepriekšējo slēgšanu, atkārtoti palaižot šo procesu visām transakcijām.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Virsgrāmata: kā lai es zinu, vai mēs palaižam gada beigu slēgšanas procesu, nevis gada beigu slēgšanas atsaukšanu?
Ir pieredzēts, ka organizācijas mēģina palaist gada beigu slēgšanas procesu, taču tās vietā izpilda gada beigu slēgšanas atsaukšanu. Ja gada beigu slēgšana tiek ļoti ātri pabeigta vai gada beigu slēgšana nerada sākuma bilances, pārbaudiet iestatījumu **Atsaukt iepriekšējo slēgšanu** sadaļā **Gada beigu slēgšana** (**Virsgrāmata > Perioda slēgšana > Gada beigu slēgšana > Palaist finanšu slēgšanu**). 

[![Gada beigu slēgšanas palaišana salīdzinājuma ar gada beigu slēgšanas atsaukšanu.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Ja atlase **Atsaukt iepriekšējo slēgšanu** ir iestatīta uz **Jā**, tiek stornēta iepriekšējā gada beigu slēgšana. Ja tiek izpildīta atsaukšanas darbība, visi beigu bilances un sākuma bilances ieraksti tiks dzēsti, it kā gada beigu slēgšana nekad nebūtu palaista. Dokumenti ir izdzēsti. Gada beigu slēgšana vairs netiks automātiski atkārtoti izpildīta. Šis process ir jāsāk vēlreiz, šoreiz nomainot iestatījumu **Atsaukt iepriekšējo slēgšanu** uz **Nē**. 

> [!NOTE]
> Beigu bilances ieraksts pēc izvēles tiek izveidots slēgšanas gadā. Tas notiek tikai tad, ja virsgrāmatas parametrs **Veidot slēgšanas darbības pārsūtīšanas laikā** ir iestatīts uz **Jā**. Sākuma bilances ieraksts vienmēr tiek izveidots, jo šī ir nākamā gada sākuma bilance.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Virsgrāmata: kāda ir atšķirība starp atsaukšanu un VG dzēšanas parametru gada beigu slēgšanai?
Var rasties pārpratumi par, to kāda ir atšķirība starp parametru **Atsaukt iepriekšējo slēgšanu**, kas atrodas dialoglodziņā **Gada beigu slēgšana**, un parametru **Gada slēgšanas darbību dzēšana pārsūtīšanas laikā**, kas atrodas virsgrāmatā (**Virsgrāmata > Perioda slēgšana > Gada slēgšana > Palaist finanšu slēgšanu**).  

[![Atšķirība starp atsaukšanu un VG dzēšanas parametru gada beigu slēgšanai.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Palaižot gada beigu slēgšanas procesu, nolaižamajā izvēlnē atlasiet **Atsaukt iepriekšējo slēgšanu**, lai dzēstu visus beigu bilances un sākuma bilances ierakstus tā, it kā gada beigu slēgšana nekad nebūtu palaista. Dokumenti tiks izdzēsti. Gada beigu slēgšana vairs netiks automātiski atkārtoti izpildīta. Lai palaistu gada beigu slēgšanas darbību, šis process ir jāsāk vēlreiz, šoreiz mainot iestatījumu **Atsaukt iepriekšējo slēgšanu** uz **Nē** (**Virsgrāmata > Virsgrāmatas iestatījumi > Virsgrāmatas parametri**). 

[![Virsgrāmatas parametru iestatījums.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Virsgrāmatas parametrs **Gada slēgšanas darbību dzēšana pārsūtīšanas laikā** tiek lietots tikai gada beigu slēgšanas (ne atsaukšanas) procesa laikā (iestatījums **Atsaukt iepriekšējo slēgšanu** ir iestatīts uz **Nē**). Ja šis parametrs ir iestatīts kā **Jā**, visi beigu bilances un sākuma bilances ieraksti tiks dzēsti un gada beigu slēgšana tiks palaista vēlreiz. Šo procesu izmanto, kad organizācija vēlas, lai visas darbības, tostarp korekcijas kopš pēdējā gada beigu slēgšanas, tiktu grāmatotas vienā uzskaites ierakstā beigu bilances un sākuma bilances ierakstiem. 

Ja šī opcija ir iestatīta uz **Nē**, visi beigu bilances un sākuma bilances ieraksti paliek nemainīgi. Tie netiek izdzēsti. Tā vietā tiek izveidots jauns beigu bilances un sākuma bilances ieraksts tikai delta vai jaunām transakcijām, kas grāmatotas kopš pēdējā gada beigu slēgšanas atbilstošajam finanšu gadam.  

> [!NOTE]
> Beigu bilances ieraksts tiek izveidots slēgšanas gadā. Tas notiek tikai tad, ja virsgrāmatas parametra **Veidot slēgšanas darbības pārsūtīšanas laikā** iestatījums ir **Jā**. Sākuma bilances ieraksts vienmēr tiek izveidots, jo šī ir nākamā gada sākuma bilance. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Virsgrāmata: kas jāmaina, lai uzlabotu gada beigu apstrādes veiktspēju? 
Lai uzlabotu gada beigu slēgšanas veiktspēju, ir iespējams veikt vairākas izmaiņas. Ieteicams novērtēt šīs ieteiktās izmaiņas, lai apsvērtu, vai tās atbilst jūsu organizācijai.  

### <a name="dimension-sets"></a>Dimensiju kopas
Palaižot gada beigu slēgšanas procesu, katra dimensiju kopas bilance tiek atjaunota un tieši ietekmē veiktspēju. Dažas organizācijas bez vajadzības izveido dimensiju kopas, jo tās tika kādreiz izmantotas vai arī kādreiz var tikt izmantotas.  Šīs nevajadzīgās dimensiju kopas joprojām tiek atjaunotas gada beigu slēgšanā, kas paildzina procesu. Atvēliet laiku, lai novērtētu savas dimensiju kopas un dzēstu visas nevajadzīgās dimensiju kopas.

Nevajadzīgās dimensiju kopas ietekmē arī pakešuzdevumu **BudgetDimensionFocusInitializeBalance** (**Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensiju kopas**).

[![Finanšu dimensiju kopas.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Gada beigu slēgšanas veidnes konfigurācija
Gada beigu slēgšanas veidne ļauj organizācijām atlasīt finanšu dimensijas līmeni, ko uzturēt, pārsūtot peļņas un zaudējumu bilances uz nesadalīto peļņu. Iestatījumi ļauj organizācijai uzturēt detalizētas finanšu dimensijas (**Slēgt visu**), pārvietojot bilances uz nesadalīto peļņu vai izvēloties apkopot summas uz vienu dimensijas vērtību (**Slēgt vienu**). To var noteikt katrai finanšu dimensijai. Plašāku informāciju par šiem iestatījumiem skatiet rakstā [Gada beigu slēgšana](year-end-close.md).

Lai uzlabotu veiktspēju, ieteicams novērtēt organizācijas prasības un, ja iespējams, aizvērt tik daudz dimensiju, cik iespējams, izmantojot gada beigu opciju **Slēgt vienu**. Noslēdzot uz vienu dimensijas vērtību (kas var būt arī tukša vērtība), sistēma aprēķina mazāk detaļu, kad tiek aprēķinātas nesadalītās peļņas konta ierakstu bilances.

## <a name="degenerate-dimensions"></a>Deģenerētās dimensijas

Deģenerētā dimensija pati par sevi un kombinācijā ar citām dimensijām nesniedz praktiski nekādu atkārtotas izmantošanas labumu. Pastāv divu veidu deģenerētās dimensijas. Pirmais veids ir dimensija, kas ir individuāli deģenerēta. Parasti šis deģenerētās dimensijas veids būs tikai vienai transakcijai vai mazām transakciju kopām. Otrs veids ir dimensija, kas kļūst deģenerēta kombinācijā ar vienu vai vairākām papildu dimensijām, kuras nodrošina to pašu potenciālu, balstoties uz iespējamām permutācijām, ko var deģenerēt. Deģenerātā dimensija var būtiski ietekmēt gada beigu slēgšanas procesa veiktspēju. Lai minimizētu veiktspējas problēmas, gada beigu slēgšanas iestatījumā definējiet visas deģenerētās dimensijas kā **Slēgt vienu**, kā tas ir aprakstīts iepriekšējā sadaļā.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Virsgrāmata: ko dara perioda un gada beigu slēgšana?
 
[![Perioda slēgšana, gada beigu slēgšana.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Veiktspējas uzlabojumi finanšu dimensiju kopu atjaunošanai
Versijā 10.0.16 pievienotais jaunais līdzeklis uzlabo gada beigu slēgšanas un konsolidācijas procesu veiktspēju. Līdzekļa nosaukums ir Veiktspējas uzlabojumi finanšu dimensiju kopu atjaunošanai. Šis līdzeklis maina veidu, kādā tiek atjaunotas dimensiju kopas, lai tās tiktu atjaunotas tikai attiecīgajā laika posmā. Iepriekšējās versijās dimensiju kopas tika atjaunotas visiem datumiem. Piemēram, ja jūs slēdzat 2020. gadu, sistēma atjaunos tikai 2020. finanšu gada transakciju bilances. Ja konsolidācija tiek palaista datumu diapazonā 2020. gada 1. novembris – 2020. gada 30. novembris, sistēma atjaunos bilances tikai šim datumu diapazonam.

Lai varētu izmantot šo līdzekli, sistēmā tas vispirms ir jāiespējo. Administratori var izmantot Līdzekļu pārvaldības darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šis līdzeklis ir uzskaitīts šādā veidā:
 
- Modulis: Virsgrāmata
- Līdzekļa nosaukums: Veiktspējas uzlabojumi finanšu dimensiju kopu atjaunošanai

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Parādi kreditoriem: kādas izmaiņas ir veiktas, lai atbalstītu 1099 gada beigu pārskatu 2021. gadam?

2021. gadā formas DIV, NEC un MISC ir mazliet mainījušās, un ir pievienoti daži papildu lodziņi.

#### <a name="div-new-box2e-2f"></a>DIV: jauns lodziņš 2e, 2f
 
- Lodziņš 2e. Rāda lodziņa 1a summas daļu, kas ir 897. sadaļas peļņa, kura ir attiecināma uz ASV nekustamā īpašuma procentu (U.S. real property interests — USRPI) izvietojumu.  
- Lodziņš 2f. Rāda lodziņa 2a summas daļu, kas ir 897. sadaļas peļņa, kura ir attiecināma uz USRPI izvietojumu. Ņemiet vērā, ka lodziņi 2e un 2f attiecas tikai uz ārvalstniekiem un entītijām, kuru ienākumi tiek nodoti vai izplatīti tiešajiem vai netiešiem ārvalstu īpašniekiem vai labuma guvējiem. Tas tiek vispārēji uzskatīts par efektīvu saistību ar tirdzniecību vai uzņēmējdarbību Amerikas Savienotajās Valstīs. Skatiet jūsu nodokļu atgriešanas instrukcijas. 
 
#### <a name="nec-new-box-2"></a>NEC: jauns lodziņš 2 
 
Ja lodziņš 2 ir atzīmēts, sniedziet pārskatu par patēriņa precēm vismaz USD 5000 apmērā, kas jums tika pārdotas tālākpārdošanai uz pirkšanas-pārdošanas, depozīta-komisijas vai citiem pamatiem. Parasti sniedziet pārskatu par visiem ieņēmumiem no šo preču pārdošanas grafikā C (forma 1040). 
 
Tikmēr NEC formas lielums ir mainīts. Drukājot lapā ir trīs formas. 
 
#### <a name="misc-new-box-11"></a>MISC: jauns lodziņš 11 
 
Lodziņā 11 tiek rādīta summa, kas samaksāta par zivju iegādi tālākpārdošanai no jebkuras personas, kas ir iesaistīta tirdzniecībā vai zivju ķeršanas uzņēmējdarbībā. Lai ziņotu par šiem ienākumiem, skatiet jūsu nodokļu atgriešanas instrukcijas. 
 
#### <a name="electronic-filing"></a>Iesniegšana elektroniski 
Informāciju par iesniegšanu elektroniski skatiet šeit: [Publikācija par iesniegšanas elektroniski prasībām](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

2021. gada e-pārskatam atjauninātas formāta specifikācijas un ierakstu izkārtojumi 
- 2. sadaļa Izdevēja “A” ieraksts. 
- Summu kodi — palielināta lauka pozīcija 28-45, garums līdz 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>2. sadaļa Izdevēja “A” ieraksts maksājumu pārskatam formā 1099-DIV: 
- Summas veids — pievienota 897. sadaļa Parastās dividendes un pievienots summas kods H. 
- Summas veids — pievienota 897. sadaļa Kapitāla pieaugums un pievienots summas kods J. 
 
#### <a name="sec-3-payee-b-record"></a>3. sadaļa Saņēmēja “B” ieraksts 
- Vispārīgās informācijas ieraksti — atjauninātā trešā aizzīme no 16.–18. maksājumu summas lauka. 
- Lauka virsraksta maksājums H — atjaunināta lauka pozīcija 247-258, lauka virsraksts, garums un vispārīgais lauka apraksts. 
- Lauka virsraksta maksājums J — atjaunināta lauka pozīcija 259-270, lauka virsraksts, garums un vispārīgais lauka apraksts. 
- Atjaunināts tukšais lauks lauka pozīcijā 271-286. 
- Atjaunināts ārvalsts indikators lauka pozīcijā 287. 
- Atjaunināts pirmā saņēmēja nosaukuma rindas lauks lauka pozīcijā 288-327. 
- Atjaunināts otrā saņēmēja nosaukuma rindas lauks lauka pozīcijā 328-367. 
- Ierakstu izkārtojuma pozīcijas, forma 1099-MISC — izdzēsta lauka pozīcija 548 un lauka virsraksts FATCA aizpildīšanas prasību indikators. 
- Ierakstu izkārtojuma pozīcijas, forma 1099-NEC — atjaunināts 545-546 uz tukšu, atjaunināts lauks 547 uz tiešās pārdošanas indikatoru, garums un apraksts, kā arī remarkas, atjaunināts lauks 548-722 uz tukšu. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>4. sadaļas Izdevēja beigas “C” ieraksts 
- Lauka virsraksta maksājums H — atjaunināta lauka pozīcija 304-321, lauka virsraksts, garums un vispārīgais lauka apraksts. 
- Lauka virsraksta maksājums J — atjaunināta lauka pozīcija 322-339, lauka virsraksts, garums un vispārīgais lauka apraksts. 
- Lauka virsraksts 340-499 — atjaunināts garums uz 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>5. sadaļas Stāvokļa kopsummas “K” ieraksts 
- Lauka virsraksta maksājums H — atjaunināta lauka pozīcija 304-321, lauka virsraksts, garums un vispārīgais lauka apraksts. 
- Lauka virsraksta maksājums J — atjaunināta lauka pozīcija 322-339, lauka virsraksts, garums un vispārīgais lauka apraksts. 
- Lauka virsraksts 340-499 — atjaunināts garums uz 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Parādi kreditoriem: 1099 — Kā var mainīt 1099 lodziņu un vērtības kreditoram, kurš gada laikā nesekoja 1099 informācijai?
Izmantojiet funkcionalitāti Atjaunināt 1099 (**Parādi kreditoriem > Kreditori >Visi kreditori > Atlasīt kreditoru > Lentes cilne Kreditors > Atjaunināt 1099**), lai apskatītu iepriekš apmaksātos rēķinus un pareizi piešķirtu 1099 datus atbilstoši iestatījumiem **kreditoru** lapas cilnē **Nodoklis 1099**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Vai var palaist atjauninājumu 1099 visiem kreditoriem vienlaicīgi?
Nē. Rutīnas atjauninājums 1099 vienlaikus tiek veikts tikai vienam kreditoram. Ja šī prasība ir nepieciešama jūsu organizācijai, lūdzu, balsojiet par ideju ar nosaukumu [Kreditora 1099 datu atjauninājuma paketes apstrāde](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Parādi kreditoriem: 1099 — “Pārrēķināt esošās 1099 summas” salīdzinājumā ar “Atjaunināt visu” atjauninājuma 1099 utilītā
Izvēles rūtiņa **Pārrēķināt esošās 1099 summas** atiestata 1099 summu uz kopējām apmaksātajām vērtībām, ja tās tiek izmantotas kopā ar izvēles rūtiņu **Atjaunināt visu**. 

[![Nodokļa 1099 transakcijas: pirms atjaunināšanas rutīnas izpildes.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Izvēles rūtiņa **Pārrēķināt esošās 1099 summas** stājas spēkā tikai tad, ja rēķinā ir daļējas 1099 vērtības vai arī tā ir modificēta veidlapā Nodoklis 1099. Piemēram, pieņemsim, ka rēķins ir novērtēts ar 1000,00 $, bet lietotājs rēķinā par 500,00 $ manuāli ieraksta 1099 summu.

[![Nodokļa 1099 transakcijas: izvēles rūtiņas “Atjaunināt visu” un “Pārrēķināt esošās 1099 summas” atzīmēšana.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Kad tas būs apmaksāts, 500,00 $ būs samaksātā 1099 summa. Veicot pārrēķināšanas rutīnu, sistēma mainīs 1099 summu uz 1000,00 $, kas ir kopējā samaksātā summa.

[![Nodokļa 1099 transakcijas: pēc 1099 rutīnas lietošanas.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Parādi kreditoriem: 1099 — manuāli izveidojiet 1099 transakcijas
Iespējams, organizācijai būs manuāli jāizveido 1099 transakcijas, kas nav saistītas ar rēķinu. Manuālas 1099 transakcijas var pievienot, dodoties uz **Parādi kreditoriem > Periodiskie uzdevumi > Nodoklis 1099 > Kreditora nodokļa 1099 nosegšana**. Izvēlieties pogu **Manuālās 1099 transakcijas**. 

Manuāli izveidotas 1099 transakcijas netiek atjauninātas, izmantojot procesu **Atjaunināt visu** vai **Pārrēķināt esošo 1099 summas** utilītā **Atjaunināt 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Parādi kreditoriem: 1099 — vai Dynamics 365 Finance atbalsta veidlapu 1096? 

Dynamics 365 Finance nedrukā 1096 gada kopsavilkumu un veidlapu ASV Informācijas atgriešanas pārsūtīšana.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Parādi kreditoriem: 1099 — vai ir kāds jauns līdzeklis, kas atbalsta 1099 pārskatu sniegšanu publiskajā sektorā? 
Ir pievienots jauns publiskā sektora līdzeklis **Atjaunināt 1099 informāciju pēc galvenā konta**, ko var iespējot darbvietā **Līdzekļu pārvaldība**. Šis līdzeklis ļauj saistīt 1099 kreditora vērtības ar galveno kontu uzskaites sadalē, nevis ar kreditora ieraksta noklusējuma kontu.

Papildinformāciju skatiet rakstā [Kreditoru iestatīšana 1099 pārskatu veidošanai](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
