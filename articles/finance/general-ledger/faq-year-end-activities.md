---
title: Bieži uzdotie jautājumi par gada beigu aktivitātēm
description: Šī tēma ir kompilēta, lai palīdzētu nokārtot gada beigu slēgšanas aktivitātes.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a9feafcab5969e9ec8fcbb8a6903d7b59505f6ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249415"
---
# <a name="year-end-activities-faq"></a>Bieži uzdotie jautājumi par gada beigu aktivitātēm 

Šī tēma ir kompilēta, lai palīdzētu nokārtot gada beigu slēgšanas aktivitātes. Šajā tēmā galvenokārt ir apskatīti jautājumi par gada beigu slēgšanas aktivitātēm virsgrāmatai un parādiem kreditoriem.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Virsgrāmata: kā lai es zinu, vai mēs palaižam gada beigu slēgšanas procesu, nevis gada beigu slēgšanas atsaukšanu?
Ir pieredzēts, ka organizācijas mēģina palaist gada beigu slēgšanas procesu, taču tās vietā izpilda gada beigu slēgšanas atsaukšanu. Ja gada beigu slēgšana tiek ļoti ātri pabeigta vai gada beigu slēgšana nerada sākuma bilances, pārbaudiet iestatījumu **Atsaukt iepriekšējo slēgšanu** sadaļā **Gada beigu slēgšana** (**Virsgrāmata > Perioda slēgšana > Gada beigu slēgšana > Palaist finanšu slēgšanu**). 

[![Gada beigu slēgšanas palaišana salīdzinājuma ar gada beigu slēgšanas atsaukšanu](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Ja atlase **Atsaukt iepriekšējo slēgšanu** ir iestatīta uz **Jā**, tiek stornēta iepriekšējā gada beigu slēgšana. Ja tiek izpildīta atsaukšanas darbība, visi beigu bilances un sākuma bilances ieraksti tiks dzēsti, it kā gada beigu slēgšana nekad nebūtu palaista. Dokumenti ir izdzēsti. Gada beigu slēgšana vairs netiks automātiski atkārtoti izpildīta. Šis process ir jāsāk vēlreiz, šoreiz nomainot iestatījumu **Atsaukt iepriekšējo slēgšanu** uz **Nē**. 

> [!NOTE]
> Beigu bilances ieraksts pēc izvēles tiek izveidots slēgšanas gadā. Tas notiek tikai tad, ja virsgrāmatas parametrs **Veidot slēgšanas darbības pārsūtīšanas laikā** ir iestatīts uz **Jā**. Sākuma bilances ieraksts vienmēr tiek izveidots, jo šī ir nākamā gada sākuma bilance.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Virsgrāmata: kāda ir atšķirība starp atsaukšanu un VG dzēšanas parametru gada beigu slēgšanai?
Var rasties pārpratumi par, to kāda ir atšķirība starp parametru **Atsaukt iepriekšējo slēgšanu**, kas atrodas dialoglodziņā **Gada beigu slēgšana**, un parametru **Gada slēgšanas darbību dzēšana pārsūtīšanas laikā**, kas atrodas virsgrāmatā (**Virsgrāmata > Perioda slēgšana > Gada slēgšana > Palaist finanšu slēgšanu**).  

[![Atšķirība starp atsaukšanu un VG dzēšanas parametru gada beigu slēgšanai](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Palaižot gada beigu slēgšanas procesu, nolaižamajā izvēlnē atlasiet **Atsaukt iepriekšējo slēgšanu**, lai dzēstu visus beigu bilances un sākuma bilances ierakstus tā, it kā gada beigu slēgšana nekad nebūtu palaista. Dokumenti tiks izdzēsti. Gada beigu slēgšana vairs netiks automātiski atkārtoti izpildīta. Lai palaistu gada beigu slēgšanas darbību, šis process ir jāsāk vēlreiz, šoreiz mainot iestatījumu **Atsaukt iepriekšējo slēgšanu** uz **Nē** (**Virsgrāmata > Virsgrāmatas iestatījumi > Virsgrāmatas parametri**). 

[![Virsgrāmatas parametru iestatījums](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Virsgrāmatas parametrs **Gada slēgšanas darbību dzēšana pārsūtīšanas laikā** tiek lietots tikai gada beigu slēgšanas (ne atsaukšanas) procesa laikā (iestatījums **Atsaukt iepriekšējo slēgšanu** ir iestatīts uz **Nē**). Ja šis parametrs ir iestatīts kā **Jā**, visi beigu bilances un sākuma bilances ieraksti tiks dzēsti un gada beigu slēgšana tiks palaista vēlreiz. Šo procesu izmanto, kad organizācija vēlas, lai visas darbības, tostarp korekcijas kopš pēdējā gada beigu slēgšanas, tiktu grāmatotas vienā uzskaites ierakstā beigu bilances un sākuma bilances ierakstiem. 

Ja šī opcija ir iestatīta uz **Nē**, visi beigu bilances un sākuma bilances ieraksti paliek nemainīgi. Tie netiek izdzēsti. Tā vietā tiek izveidots jauns beigu bilances un sākuma bilances ieraksts tikai delta vai jaunām transakcijām, kas grāmatotas kopš pēdējā gada beigu slēgšanas atbilstošajam finanšu gadam.  

> [!NOTE]
> Beigu bilances ieraksts tiek izveidots slēgšanas gadā. Tas notiek tikai tad, ja virsgrāmatas parametrs **Veidot slēgšanas darbības pārsūtīšanas laikā** ir iestatīts uz **Jā**. Sākuma bilances ieraksts vienmēr tiek izveidots, jo šī ir nākamā gada sākuma bilance. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Virsgrāmata: kas jāmaina, lai uzlabotu gada beigu apstrādes veiktspēju? 
Lai uzlabotu gada beigu slēgšanas veiktspēju, ir iespējams veikt vairākas izmaiņas. Ieteicams novērtēt šīs ieteiktās izmaiņas, lai apsvērtu, vai tās atbilst jūsu organizācijai.  

### <a name="dimension-sets"></a>Dimensiju kopas
Palaižot gada beigu slēgšanas procesu, katra dimensiju kopas bilance tiek atjaunota un tieši ietekmē veiktspēju. Dažas organizācijas bez vajadzības izveido dimensiju kopas, jo tās tika kādreiz izmantotas vai arī kādreiz var tikt izmantotas.  Šīs nevajadzīgās dimensiju kopas joprojām tiek atjaunotas gada beigu slēgšanā, kas paildzina procesu. Atvēliet laiku, lai novērtētu savas dimensiju kopas un dzēstu visas nevajadzīgās dimensiju kopas.

Nevajadzīgās dimensiju kopas ietekmē arī pakešuzdevumu **BudgetDimensionFocusInitializeBalance** (**Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensiju kopas**).

[![Finanšu dimensiju kopas](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Gada beigu slēgšanas veidnes konfigurācija
Gada beigu slēgšanas veidne ļauj organizācijām atlasīt finanšu dimensijas līmeni, ko uzturēt, pārsūtot peļņas un zaudējumu bilances uz nesadalīto peļņu. Iestatījumi ļauj organizācijai uzturēt detalizētas finanšu dimensijas (**Slēgt visu**), pārvietojot bilances uz nesadalīto peļņu vai izvēloties apkopot summas uz vienu dimensijas vērtību (**Slēgt vienu**). To var noteikt katrai finanšu dimensijai. Plašāku informāciju par šiem iestatījumiem skatiet tēmā [Gada beigu slēgšana](year-end-close.md).

Lai uzlabotu veiktspēju, ieteicams novērtēt organizācijas prasības un, ja iespējams, aizvērt tik daudz dimensiju, cik iespējams, izmantojot gada beigu opciju **Slēgt vienu**. Noslēdzot uz vienu dimensijas vērtību (kas var būt arī tukša vērtība), sistēma aprēķina mazāk detaļu, kad tiek aprēķinātas nesadalītās peļņas konta ierakstu bilances.

### <a name="10013-update-or-later"></a>10.0.13 atjauninājums vai jaunāka versija
Ja kopš pēdējās reizes, kad jūsu organizācija gada beigās veica gada slēgšanu, esat atjauninājis uz versiju 10.0.13 vai jaunāku versiju, gada beigu slēgšanas process var aizņemt vairāk laika [HashV2 līdzekļa implementēšanas](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2) dēļ. (Termins *jaukšana* attiecas uz lauku, kas ir aprēķināts no citiem virknes laukiem. Tika atjaunināts API jaukšanas GUID vērtības aprēķināšanai, lai uzlabotu drošību.) Lai paātrinātu gada beigu slēgšanas procesu, pirms gada beigu slēgšanas palaišanas ieteicams atjaunot dimensiju kopu bilances. Ja dimensiju kopas bilanču atjaunošana jau ir veikta pēc 10.0.13 atjauninājuma ieviešanas, nav nepieciešams vēlreiz palaist atjaunošanas procesu.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Virsgrāmata – ko dara perioda slēgšana – gada beigu slēgšana?
 
[![Perioda slēgšana, gada beigu slēgšana](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Veiktspējas uzlabojumi finanšu dimensiju kopu atjaunošanai (jauns līdzeklis)
Versijā 10.0.16 pievienots jauns līdzeklis, kas uzlabo gada beigu slēgšanas un konsolidācijas procesu veiktspēju. Līdzekļa nosaukums ir Veiktspējas uzlabojumi finanšu dimensiju kopu atjaunošanai. Šis līdzeklis maina veidu, kādā tiek atjaunotas dimensiju kopas, lai tās tiktu atjaunotas tikai attiecīgajā laika posmā. Iepriekšējās versijās dimensiju kopas tika atjaunotas visiem datumiem. Piemēram, ja jūs slēdzat 2020. gadu, sistēma atjaunos tikai 2020. finanšu gada transakciju bilances. Ja konsolidācija tiek palaista datumu diapazonā 2020. gada 1. novembris – 2020. gada 30. novembris, sistēma atjaunos bilances tikai šim datumu diapazonam.

Tā kā šis līdzeklis tiek uzskatīts par traucējumus radošām izmaiņām, jums tas ir jāiespējo, izmantojot **līdzekļu pārvaldības** darbvietu.
 
[![Gada beigu slēgšana](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Parādi kreditoriem: kādas izmaiņas ir veiktas, lai atbalstītu 1099 gada beigu pārskatu 2020. gadam?

1099 gada beigu izmaiņām 2020. gadā ir pievienoti divi jauni regulēšanas līdzekļi. Pirmais līdzeklis **Lietot izmaiņas 1099-NEC un 1099-MISC veidlapām 2020. gadā** tika izlaists kā obligāts līdzeklis gada vidū. Tā mērķis ir nodrošināt, lai 1099 transakciju datus 2020. gadam varētu izsekot jaunajai veidlapai 1099-NEC. Šis līdzeklis pievienoja 1099 laukus, kas ir nepieciešami, lai atbalstītu jaunos 1099-NEC un atjauninātos 1099-MISC laukus. Šis atjauninājums arī jaunināja kreditora ieraksta datus 1099 lodziņa informācijai. 

Otrais regulēšanas līdzeklis **1099 pārskati, kas atjaunināti 2020. gada nodokļu likumam**, satur šādas izmaiņas.

- 1099-OID — IRS ir pārveidojis veidlapu nepārtrauktai lietošanai.
   - Drukājot jāaizpilda pārskata gada 3. un 4. cipars. Lietojiet **pārskata gada** lauka 3. un 4. ciparu no **nodokļa 1099 drukāšanas opcijām**. 

- 1099-NEC — jauna veidlapa 2020. gadam. Šis reģistrē kompensāciju, kas nav darbinieku kompensācija. 

-   1099-MISC – Lai izveidotu veidlapu 1099-NEC, IRS ir pārskatījis veidlapu 1099-MISC un pārkārtojis lodziņu numurus noteiktu ienākumu pārskatu izveidei.
Izmaiņas ienākumu uzskaitē un veidlapas lodziņu numuros ir norādītas zemāk.
   - Maksātāja veiktā tiešā 5000 $ pārdošana (izvēles rūtiņa) 7. lodziņā.
   - Ražas apdrošināšanas ieņēmumi tiek uzrādīti 9. lodziņā.
   - Bruto ieņēmumi, kas attiecas uz advokātu, tiek uzrādīti 10. lodziņā.
   - 409. sadaļas atliktie maksājuma dokumenti ir uzrādīti 12. lodziņā.
   - Nekvalificēto atlikto atlīdzību ieņēmumi ir uzrādīti 14. lodziņā.
   - 15., 16. un 17. lodziņā tiek norādīts ieturētais valsts nodoklis, valsts identifikācijas numurs un attiecīgā štatā nopelnīto ienākumu summa.

- 2020. gadā nav nekādu izmaiņu attiecībā uz 1099-DIV vai 1099-INT.

- Iesniegšana elektroniski — formāts ir mainījies, lai pielāgotos jaunajai NEC veidlapai un iepriekš aprakstītajām MISC lodziņu izmaiņām. Lai iegūtu sīkāku informāciju par elektroniskās iesniegšanas prasībām, skatiet [IRS publikāciju 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Parādi kreditoriem: 1099 — Kā var mainīt 1099 lodziņu un vērtības kreditoram, kurš gada laikā nesekoja 1099 informācijai?
Izmantojiet funkcionalitāti Atjaunināt 1099 (**Parādi kreditoriem > Kreditori >Visi kreditori > Atlasīt kreditoru > Lentes cilne Kreditors > Atjaunināt 1099**), lai izietu cauri iepriekš apmaksātām rēķinu darbībām, lai pareizi piešķirtu 1099 datus atbilstoši iestatījumiem **kreditoru** lapas cilnē **Nodoklis 1099**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Vai var palaist atjauninājumu 1099 visiem kreditoriem vienlaicīgi?
Nē. Rutīnas atjauninājums 1099 vienlaikus tiek veikts tikai vienam kreditoram. Ja šī prasība ir nepieciešama jūsu organizācijai, lūdzu, balsojiet par ideju ar nosaukumu [Kreditora 1099 datu atjauninājuma pakešuzdevums](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Parādi kreditoriem: 1099 – “Pārrēķināt esošās 1099 summas” salīdzinājumā ar “Atjaunināt visu” atjauninājuma 1099 utilītā.
Izvēles rūtiņa **Pārrēķināt esošās 1099 summas** atiestata 1099 summu uz kopējām apmaksātajām vērtībām, ja tās tiek izmantotas kopā ar izvēles rūtiņu **Atjaunināt visu**. 

[![Nodokļa 1099 transakcijas: pirms atjaunināšanas rutīnas izpildes](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Izvēles rūtiņa **Pārrēķināt esošās 1099 summas** stājas spēkā tikai tad, ja rēķinā ir daļējas 1099 vērtības vai arī tā ir modificēta veidlapā Nodoklis 1099. Piemēram, pieņemsim, ka rēķins ir novērtēts ar 1000,00 $, bet lietotājs rēķinā par 500,00 $ manuāli ieraksta 1099 summu.

[![Nodokļa 1099 transakcijas: izvēles rūtiņas “Atjaunināt visu” un “Pārrēķināt esošās 1099 summas” atzīmēšana](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Kad tas būs apmaksāts, 500,00 $ būs samaksātā 1099 summa. Veicot pārrēķināšanas rutīnu, sistēma mainīs 1099 summu uz 1000,00 $, kas ir kopējā samaksātā summa.

[![Nodokļa 1099 transakcijas: pēc 1099 rutīnas lietošanas](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Parādi kreditoriem: 1099 — manuāli izveidojiet 1099 transakcijas
Iespējams, organizācijai ir manuāli jāizveido 1099 transakcijas, kas nav saistītas ar rēķinu. Manuālas 1099 transakcijas var pievienot, dodoties uz **Parādi kreditoriem > Periodiskie uzdevumi > Nodoklis 1099 > Kreditora nodokļa 1099 nosegšana**. Izvēlieties pogu **Manuālās 1099 transakcijas**. 

Manuāli izveidotas 1099 transakcijas netiek atjauninātas, izmantojot procesu **Atjaunināt visu** vai **Pārrēķināt esošo 1099 summas** utilītā **Atjaunināt 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Parādi kreditoriem: 1099 — vai Dynamics 365 Finance atbalsta veidlapu 1096? 

Dynamics 365 Finance nedrukā 1096 gada kopsavilkumu un veidlapu ASV Informācijas atgriešanas pārsūtīšana.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Parādi kreditoriem: 1099 — vai ir kāds jauns līdzeklis, kas atbalsta 1099 pārskatu sniegšanu publiskajā sektorā? 
Ir pievienots jauns publiskā sektora līdzeklis **Atjaunināt 1099 informāciju pēc galvenā konta**, ko var iespējot darbvietā **Līdzekļu pārvaldība**. Šis līdzeklis ļauj saistīt 1099 kreditora vērtības ar galveno kontu uzskaites sadalē, nevis ar kreditora ieraksta noklusējuma kontu.

Papildinformāciju skatiet rakstā [Kreditoru iestatīšana 1099 pārskatu veidošanai](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]