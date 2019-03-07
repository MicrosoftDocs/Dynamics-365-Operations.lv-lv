---
title: Divkāršā valūta
description: Šajā tēmā ir sniegta informācija par divkāršo valūtu — gadījumu, kad pārskata valūta tiek izmantota kā otrā uzskaites valūta programmā Microsoft Dynamics 365 for Finance and Operations.
author: kweekley
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 8de178ec80f7408d657e746b633703f386c8e02d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "330314"
---
# <a name="dual-currency"></a>Divkāršā valūta

[!include [banner](../includes/banner.md)]

Funkcionalitāte, kas tika ieviesta Microsoft Dynamics 365 for Finance and Operations versijā 8.1 (2018. gada oktobris), sniedz iespēju mainīt pārskata valūtas pielietojumu un izmantot to kā otro uzskaites valūtu. Šī funkcionalitāte tiek saukta par *divkāršo valūtu*. Divkāršās valūtas izmaiņas nevar izslēgt, izmantojot konfigurācijas atslēgu vai parametru. Tā kā pārskata valūta tiek izmantota kā otrā norēķinu valūta, ir mainīts veids, kādā tiek aprēķināta pārskata valūta grāmatošanas loģikā.

Turklāt dažādi moduļi ir uzlaboti, lai izsekotu, iekļautu pārskatos un izmantotu pārskata valūtu dažādos procesos. Izmaiņas attiecas uz moduļiem **Virsgrāmata**, **Finanšu pārskati**, **Kreditori**, **Debitori**, **Kases un bankas vadība**, un **Pamatlīdzekļi**. Pēc jaunināšanas ir jāveic noteikti soļi attiecībā uz moduļiem Kases un bankas vadība un Pamatlīdzekļi. Tādēļ uzmanīgi izlasiet šīs tēmas attiecīgās sadaļas.

## <a name="posting-process"></a>Grāmatošanas process

Grāmatošanas loģika ir mainīta visām transakcijām, kas ģenerē uzskaites ierakstu virsgrāmatā. Tālāk ir aprakstīts, kā pārskata valūta tika aprēķināta iepriekš.

Darījuma valūtas summa \> Uzskaites valūtas summa \> Pārskata valūtas summa

Piemēram, transakcija ir ievadīta Kanādas dolāros (CAD). CAD summa tiek pārrēķināta uz uzskaites valūtu, kas ir ASV dolārs (USD). Pēc tam USD summa tiek pārrēķināta uz pārskata valūtu, kas ir eiro (EUR). Tādēļ ir jābūt valūtas maiņas kursiem pārrēķināšanai no CAD uz USD un no USD uz EUR.

Tālāk ir norādīts jaunais aprēķins.

Darījuma valūtas summa \> Uzskaites valūtas summa

Darījuma valūtas summa \> Pārskata valūtas summa

Šo izmaiņu dēļ tagad jābūt valūtas maiņas kursiem pārrēķināšanai no CAD uz USD un no CAD uz EUR.

## <a name="reports-and-inquiries"></a>Pārskati un pieprasījumi

Dažādos pārskatos un pieprasījumos tagad tiek rādītas gan pārskata valūtas summas, gan uzskaites valūtas summas. Ne visi pārskati un pieprasījumi ir atjaunināti. Piemēram, nav mainījušies pārskati, kuros summas ir parādītas tikai darījuma valūtā.

Izmaiņas ir veiktas atbilstoši vienam no diviem modeļiem.

- Ja pārskatā vai pieprasījumā bija pietiekami daudz vietas, lai parādītu summas gan uzskaites valūtā, gan pārskata valūtā, tika pievienotas pārskata valūtas summas.
- Ja pārskatā vai pieprasījumā nebija pietiekami daudz vietas, lai rādītu summas abās valūtās, tika pievienota opcija, lai lietotāji varētu izvēlēties, kura valūta tiek parādīta.

Dažādiem pārskatiem un pieprasījumiem arī tika pievienota loģika, lai nerādītu pārskata valūtas summas, ja pārskata valūta ir tāda pati kā uzskaites valūta vai ja pārskata valūta nebija definēta virsgrāmatā attiecīgajai juridiskajai personai.

## <a name="financial-journals"></a>Finanšu žurnāli

Finanšu žurnāli, piemēram, virsgrāmatas žurnāls un kreditoru rēķinu žurnāls, ir atjaunināti tā, ka tie ietver papildu informāciju par pārskata valūtu. Dokumentu un žurnālu kopsummas tagad tiek rādītas pārskata valūtā. Turklāt informācija par pārskata valūtas maiņas kursu tagad parādās žurnāla rindu cilnē **Vispārēji**. Tādējādi varat pārlabot pārskata valūtas maiņas kursu, ievadot transakcijas.

## <a name="module-changes"></a>Moduļu izmaiņas

Tālāk minētajos moduļos pārskata valūta tiek izmantota kā otrā uzskaites valūta.

- [Virsgrāmata](#general-ledger)
- [Finanšu pārskati](#financial-reporting)
- [Kreditori](#accounts-payable-and-accounts-receivable)
- [Debitori](#accounts-payable-and-accounts-receivable)
- [Skaidras naudas un bankas pārvaldība](#cash-and-bank-management)
- [Pamatlīdzekļi](#fixed-assets)

### <a name="general-ledger"></a>Virsgrāmata

Ja virsgrāmatā tika definēta pārskata valūta, virsgrāmata jau izsekoja visas pārskata valūtas summas par katru uzskaites ierakstu. Tomēr šīs summas tagad tiek pārrēķinātas no darījumu valūtas summām.

Modulī **Virsgrāmata** tika veiktas šādas papildu izmaiņas.

- Virsgrāmatā var definēt atsevišķu maiņas kursa tipu pārskata valūtai. Ja organizācija nevēlas izmantot citu maiņas kursa tipu, attiecīgās pārskata valūtas maiņas kursa tipa lauku var atstāt tukšu. Vai arī var atlasīt to pašu maiņas kursa tipu, kas tiek izmantots uzskaites valūtai. Ja šo lauku atstājat tukšu, sistēma izmanto uzskaites valūtas maiņas kursa tipu.
- Jauns žurnāls — pārskata valūtas korekcijas žurnāls— ļauj grāmatot virsgrāmatas kontos korekcijas tikai pārskata valūtā. Šis žurnāls ļauj veikt grāmatošanu tikai virsgrāmatas kontos. Tas neatbalsta starpuzņēmumu, un valūtai jābūt tādas juridiskās personas pārskata valūtai, kurai ir iegrāmatots žurnāls. Kad žurnāls ir iegrāmatots, darījuma valūtas un uzskaites valūtas summas ir 0 (nulle), un pārskata valūtas summa tiek iegrāmatota, izmantojot summu, kas ir ievadīta attiecīgajai transakcijai. Tā kā ir mainījies pārskata valūtas izmantošanas veids moduļos **Kreditori**, **Debitori** un **Pamatlīdzekļi**, šo žurnālu var izmantot korekcijām pēc jaunināšanas. Piemērus, kuros aprakstīts, kā lietot šo žurnālu, skatiet sadaļās par attiecīgajiem moduļiem.
- Perioda sadalījuma process ir atjaunināts tā, ka tas sadala summas darījuma, uzskaites un pārskata valūtās. Iepriekš summas tika sadalītas darījuma un uzskaites valūtās, un pēc tam uzskaites valūtas summa tika pārrēķināta uz pārskata valūtu. Šādas darbības rezultātā virsgrāmatas konta bilance varēja tikt parādīta pārskata valūtā. Tagad, kad summas tiek aprēķinātas un izmantotas uzskaites ierakstā, pārrēķināšana netiek veikta.
- Ārvalstu valūtas pārvērtēšanas procesā jau tika veikta summu pārvērtēšana pārskata valūtā. Tomēr pārskata valūtas summu tagad aprēķina, izmantojot darījuma valūtas summu, kā aprakstīts sadaļā [Grāmatošanas process](#posting-process) iepriekš šajā tēmā.
- Daudziem pārskatiem un pieprasījumiem virsgrāmatā jau tika izmantota pārskata valūta, taču dažiem tas netika darīts. Viens šāds piemērs ir saraksta lapa **Apgrozījuma bilance**. Šī saraksta lapa tagad ietver kolonnas gan uzskaites valūtai, gan pārskata valūtai. Ņemiet vērā, ka pārskata valūtas kolonnas tiek slēptas, ja uzskaites valūta ir vienāda ar pārskata valūtu vai ja virsgrāmatā nav definēta pārskata valūta.

### <a name="financial-reporting"></a>Finanšu pārskatu veidošana

Moduļa **Finanšu pārskati** uzlabojums ļauj iekļaut pārskata valūtas summas finanšu pārskatā divos veidos. Kolonnas definīcijā var tieši izveidot pārskatu par pārskata valūtas summām, kas iegrāmatotas virsgrāmatā (jauna funkcionalitāte). Vai arī varat turpināt pārrēķināt summas no uzskaites valūtas uz pārskata valūtu (esošā funkcionalitāte).

Šīs izmaiņas ir pieejamas, izmantojot iestatījumu **Valūtas attēlojums** kolonnas definīcijā. Atlasot **Pārskata valūta no virsgrāmatas**, kolonnas summas netiek pārrēķinātas. Tā vietā tās tiek iekļautas pārskatā tieši no virsgrāmatas. Ja vēlaties, lai kolonnā tiktu rādītas pārrēķinātās summas, atlasiet opciju **Pārrēķināt uz XXXX**, kur *XXXX* ir pārskata valūta, kas ir attiecīgajā kolonnā. Šajā gadījumā uzskaites valūtas summas tiks pārrēķinātas uz atlasīto valūtu, izmantojot esošo pārrēķināšanas funkcionalitāti.

### <a name="accounts-payable-and-accounts-receivable"></a>Kreditori un debitori

Moduļos **Kreditori** un **Debitori** jau tika izsekotas pārskata valūtas summas. Tomēr summas netika rādītas vai izmantotas dažādos procesos. Tika veiktas tālāk norādītās izmaiņas.

- Pārskata valūtas summas tagad tiek rādītas gan debitoru, gan kreditoru transakcijās. Pārskata valūtas summas tiek rādītas arī katras transakcijas sākuma bilancei.
- Vecumstruktūras process ir atjaunināts, lai organizācija varētu apskatīt vecumstruktūras intervālus uzskaites valūtā vai pārskata valūtā.
- Dažādi pieprasījumi un pārskati tika atjaunināti tā, ka tie parāda pārskata valūtas summas. Kā piemērus var minēt pārskatus **Debitoru un virsgrāmatas saskaņošana** un **Kreditoru un virsgrāmatas saskaņošana**.
- Ārvalstu valūtas pārvērtēšanas procesā jau tika veikta summu pārvērtēšana pārskata valūtā. Tomēr pārskata valūtas summu tagad aprēķina, izmantojot darījuma valūtas summu, kā aprakstīts sadaļā [Grāmatošanas process](#posting-process).
- **Jaunināšanas apsvērums:** pirms jaunināšanas dokumentu (rēķinu, maksājumu utt.) pārskata valūtas summas aprēķina, izmantojot uzskaites valūtu. Piemēram, rēķins ir grāmatots pirms organizācijas jaunināšanas, un attiecīgais rēķins nav apmaksāts. Jaunināšanas laikā nav mainīts rēķina uzskaites ieraksts. Tomēr pēc jaunināšanas ir spēkā izmaiņas attiecībā uz divkāršo valūtu. Tādēļ, kad tiek veikts maksājums par rēķinu, maksājuma pārskata valūtas summa tagad tiek aprēķināta, izmantojot darījuma valūtas summu. Kad tiek veikts maksājums un apmaksāts rēķins, var tikt aprēķināta neliela starpība starp realizētās peļņas/zaudējumu summu, jo pārskata valūtas summas tagad tiek aprēķinātas citādāk. Ja aprēķinātā starpība tiek uzskatīta par nozīmīgu, jauno pārskata valūtas korekcijas žurnālu var izmantot, lai koriģētu realizētās peļņas/zaudējumu un kreditoru/debitoru virsgrāmatas kontu bilanci tikai pārskata valūtā.

### <a name="cash-and-bank-management"></a>Kases un banku pārvaldība

Iepriekš modulis **Kases un bankas vadība** neizsekoja pārskata valūtas summas transakcijām, kuras tika grāmatotas atbilstoši katram bankas kontam. Pēc jaunināšanas pārskata valūtas summas automātiski tiek izsekotas visām jaunajām transakcijām, kas tiek grāmatotas. Tomēr pārskata valūtas summas ir jāpievieno iepriekš grāmatotajām transakcijām apakšgrāmatā.

- **Jaunināšanas apsvērums:** tā kā bankas konta transakcijas iepriekš neizsekoja pārskata valūtas summas apakšgrāmatā, ir pievienots vednis, lai jūs varētu pievienot pārskata valūtas summas bankas konta transakcijām. Šis vednis **neveic** atkārtotu grāmatošanu virsgrāmatā. Tā vietā tas atjaunina virsgrāmatā esošās pārskata valūtas summas apakšgrāmatas tabulās.

    - Lai palaistu vedni, atlasiet **Kases un bankas vadība** \> **Iestatīšana** \> **Pārskata valūtas summu pievienošana bankas konta transakcijām**.
    - Vednis parāda transakcijas visos pašreizējā uzņēmuma bankas kontos, kuru pārskata valūtas summa ir 0 (nulle). Ir iekļautas tikai transakcijas, kas iegrāmatotas pirms jaunināšanas.
    - Katrai bankas konta transakcijai vednis atrod atbilstošos uzskaites ierakstus virsgrāmatā un ievada noklusējuma pārskata valūtas summu. Lai gan summas var rediģēt, to **nav** ieteicams darīt. Pretējā gadījumā, iespējams, nevarēsit saskaņot bankas kontu bilances ar virsgrāmatu. Vienīgais gadījums, kad būtu jārediģē summa, ir tad, ja pārskata valūtas summu nevar atrast virsgrāmatā. Šādā gadījumā vednis parāda pārskata valūtas summu 0 (nulle).
    - Ja vednī atlasāt **Atcelt**, bankas konta transakcijas un jebkādas pārskata valūtas summu izmaiņas tiek saglabātas līdz nākamajai vedņa palaišanas reizei. Tomēr pārskata valūtas summas netiek atjauninātas bankas konta transakcijās. Šī atjaunināšana notiek tikai tad, ja vednī atlasāt **Pabeigt**. Vedni var palaist vairākas reizes. Tādēļ var novērst jebkuras nepareizas pārskata valūtas summas, ja ir pieļauta kļūda.

- Modulī Kases un bankas vadība netika mainīti procesi, taču tika atjaunināti dažādi pārskati un pieprasījumi tā, lai tie rādītu pārskata valūtas summas. Naudas plūsmas prognožu pārskati ir izņēmums. Tie netika atjaunināti, lai iekļautu pārskata valūtas summas.

### <a name="fixed-assets"></a>Pamatlīdzekļi

Iepriekš modulis **Pamatlīdzekļi** neizsekoja pārskata valūtas summas transakcijām, kuras tika grāmatotas atbilstoši katrai pamatlīdzekļu grāmatai. Pēc jaunināšanas pārskata valūtas summas automātiski tiek izsekotas visām jaunajām transakcijām, kas tiek grāmatotas. Tomēr pārskata valūtas summas ir jāpievieno iepriekš grāmatotajām transakcijām apakšgrāmatā.

Turklāt nolietojuma procesā ir veiktas būtiskas izmaiņas. Šīm izmaiņām ir nepieciešamas lietotāja darbības pēc jaunināšanas. Ir svarīgi izlasīt un izprast tālāk minētās izmaiņas pat tad, ja vēl neizmantojat moduli Pamatlīdzekļi.

- Ir mainījies veids, kā nolietojuma processnosaka pārskata valūtas summu. Šajā scenārijā ir salīdzināts, kā nolietojums iepriekš noteica pārskata valūtas summu un kā tas tagad nosaka pārskata valūtas summu.

    **Nolietojuma scenārijs**

    Pamatlīdzeklis tiek iegādāts un grāmatots, norādot šādas summas. Ņemiet vērā, ka pārskata valūtas summa tiek iegrāmatota virsgrāmatā, bet tā netiek saglabāta pamatlīdzekļu apakšgrāmatas tabulās.

    | Darbības veids | Darbības summa | Valūtas kurss | Uzskaites valūtas summa | Valūtas kurss | Pārskata valūtas summa |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Iegāde      | 1 000 000 DKK      | 2,0           | 500 000 USD                | 2,5           | 200 000 EUR               |

    **Iepriekšējais nolietojums pārskata valūtā**

    Gada beigās tiek izpildīts nolietojuma priekšlikums un tiek aprēķinātas šādas summas.

    | Darbības veids | Darbības summa | Valūtas kurss | Uzskaites valūtas summa | Valūtas kurss | Pārskata valūtas summa |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Nolietojums     | 50 000 USD         | 1,0           | 50 000 USD                 | 2,6           | 19 230,77 EUR             |

    Kad tiek izpildīts nolietojuma priekšlikums, tas aprēķina uzskaites valūtas summu, izmantojot nolietojuma metodi. Pēc tam tas pārrēķina attiecīgo summu pārskata valūtā, izmantojot pašreizējo maiņas kursu starp USD un EUR. Šis pārrēķins rada problēmas, jo līdzekli nevar pilnībā nolietot pārskata valūtā, izmantojot tūlītējo likmi.

    **Jauns nolietojums pārskata valūtā**

    Nolietojuma process ir izmainīts tā, lai pārskata valūtas summu arī aprēķinātu, izmantojot nolietojuma metodi. Tālāk ir sniegti līdzekļa nolietojuma izpildes rezultāti.

    | Darbības veids | Darbības summa | Valūtas kurss | Uzskaites valūtas summa | Valūtas kurss                                                       | Pārskata valūtas summa |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Nolietojums     | 50 000 USD         | 1,0           | 50 000 USD                 | 2,5<blockquote>[!NOTE] Kaut gan šis valūtas kurss ir redzams, tas netiek izmantots pārrēķināšanai uz pārskata valūtu.</blockquote> | 20 000 EUR                |

    Izpildot nolietojuma priekšlikumu, tas aprēķina gan uzskaites valūtas summu, gan pārskata valūtas summu, izmantojot nolietojuma metodi. Pēc tam summas tiek izmantotas uzskaites ierakstā virsgrāmatā. Netiek veikta pārrēķināšana, lai noteiktu pārskata valūtas summu.

- **Jaunināšanas apsvērums:** tā kā pamatlīdzekļu grāmatas transakcijas iepriekš neizsekoja pārskata valūtu, ir pievienots vednis, lai jūs varētu pievienot pārskata valūtas summas pamatlīdzekļu grāmatas transakcijām. Šis vednis **neveic** atkārtotu grāmatošanu virsgrāmatā. Tā kā ir mainīts veids, kādā nolietojuma priekšlikums aprēķina pārskata valūtas summas, vednis ir **jāpalaiž** un jāpabeidz katram uzņēmumam, pirms organizācija var ievadīt nolietojuma transakcijas.

    - Lai palaistu ceļvedi, izvēlieties **Pamatlīdzekļi** \> **Iestatīšana** \> **Pievienot pārskata valūtas summas pamatlīdzekļu grāmatām**.
    - Vednis parāda transakcijas visās pašreizējā uzņēmuma pamatlīdzekļu grāmatās, kuru pārskata valūtas summa ir 0 (nulle). Ir iekļautas tikai transakcijas, kas iegrāmatotas pirms jaunināšanas.
    - Vednis **neiegūst** pārskata valūtas summas no virsgrāmatas. Kā aprakstīts iepriekšējā scenārijā, pārskata valūtas summām, kas sākotnēji bija grāmatotas virsgrāmatā, tika nepareizi izmantota tūlītējā likme. Šīm summām nevajadzētu parādīties pamatlīdzekļu apakšgrāmatā, jo nākamajā nolietojuma aprēķinā tiks izmantotas nepareizas summas. Tā vietā vednis atrod maiņas kursu pirmās iegādes datumā. Pēc tam tas izmanto attiecīgo maiņas kursu, lai ieteiktu pārskata valūtas summu, kas jāgrāmato apakšgrāmatā. Piemēram, tālāk redzami iespējamie vedņa attēlotie dati saistībā ar iepriekšējo scenāriju.

        | Pamatlīdzeklis | Rezervēšana      | Darbības veids | Darījuma datums | Valūta | Summa darījuma valūtā | Daudzums  | Maiņas kurss | Pārskata valūtas summa |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Iegāde      | 6/3/2016         | DKK      | 1 000 000                      | 500 000 | 2,5       | 250 000                   |
        | BUIL-00001  | 200\_SLLT | Nolietojums     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250 000                   |
        | BUIL-00001  | 200\_SLLT | Nolietojums     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250 000                   |
        | BUIL-00001  | 200\_SLLT | Nolietojums     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250 000                   |

    - Daudzi debitori izsekoja savu līdzekļu transakciju informāciju darbgrāmatās. Šī informācija ietver maiņas kursus un summas. Ja šie dati ir darbgrāmatā, var izveidot pielāgotu maiņas kursa tipu un atjaunināt, izmantojot maiņas kursus no darbgrāmatas. Šis maiņas kursa tips pēc tam tiks izmantots, lai ievadītu noklusējuma maiņas kursu iegādes datumā un aprēķinātu pārskata valūtas summu. Ja nav atlasīts maiņas kursa tips, vednis izmanto maiņas kursa tipu, kas tika definēts virsgrāmatā.
    - Maiņas kursu un pārskata valūtas summas var mainīt. Ja maiņas kurss tiek mainīts, pārskata valūtas summa tiek pārrēķināta, izmantojot jauno likmi.
    - Ja vednī atlasāt **Atcelt**, pamatlīdzekļu grāmatas transakcijas un jebkādas maiņas kursa vai pārskata valūtas summu izmaiņas tiek saglabātas līdz nākamajai vedņa palaišanas reizei. Tomēr pārskata valūtas summas netiek atjauninātas pamatlīdzekļu grāmatas transakcijās. Šī atjaunināšana notiek tikai tad, ja vednī atlasāt **Pabeigt**. Vedni var palaist vairākas reizes. Tādēļ var novērst jebkuras nepareizas pārskata valūtas summas, ja ir pieļauta kļūda.
    - Kad pārskata valūtas summas tiek pilnībā atjauninātas apakšgrāmatā, opcijai **Vai pamatlīdzekļu grāmatu transakcijās esat atjauninājis visas pārskata valūtas summas?** ir **jāiestata** vienums **Jā** un pēc tam jāatlasa **Pabeigt**. Nolietojuma aprēķinus nevar pabeigt, līdz opcijai **Vai pamatlīdzekļu grāmatu transakcijās esat atjauninājis visas pārskata valūtas summas?** ir iestatīts vienums **Jā**. Pēc tam, kad attiecīgajai opcijai ir iestatīts vienums **Jā**, vednis vairs nav pieejams.
    - Pēc tam, kad pamatlīdzekļu transakcijas apakšgrāmatā ir atjauninātas ar pārskata valūtas summām, šīs summas neatbildīs summām, kuras bija sākotnēji grāmatotas virsgrāmatā. Tomēr pārskata valūtas korekcijas žurnālu var izmantot, lai atjauninātu nolietojuma virsgrāmatas kontu bilances, lai tās atbilstu sākotnēji grāmatotajām summām.
    - Jaunais elements **Līdzekļu transakciju pārskata valūtas summas**, kas ir pievienots darbvietā **Datu pārvaldība**, ļauj eksportēt datus no vedņa. Pēc tam datus var izmantot, lai noteiktu pamatlīdzekļu apakšgrāmatas bilanci nolietojuma transakcijām. Šo bilanci pēc tam var izmantot, lai noteiktu pārskata valūtas korekciju virsgrāmatā.

- **Jaunināšanas apsvērums:** pamatlīdzekļiem ir pievienoti jauni iestatījuma lauki, un tie tiek izmantoti nolietojuma aprēķinā. Iespējams, vajadzēs atjaunināt šos laukus pirms nākamā nolietojuma aprēķina.

    - Pamatlīdzekļu nolietojuma grāmatas (**Pamatlīdzekļi** \> **Grāmatas**) kopsavilkuma cilnē **Vispārēji** ir jauns lauks **Iegādes cena pārskata valūtā**.
    - Pamatlīdzekļu nolietojuma grāmatas (**Pamatlīdzekļi** \> **Grāmatas**) kopsavilkuma cilnē **Nolietojums** ir jauns lauks **Plānotā lūžņu vērtība pārskata valūtā**.
    - Pamatlīdzekļu parametru (**Pamatlīdzekļi** \> **Iestatīšana** \> **Pamatlīdzekļu parametri**) kopsavilkuma cilnē **Vispārēji** ir jauns lauks **Minimālā nolietojuma summa pārskata valūtā**.
    - Grāmatu (**Pamatlīdzekļi** \> **Iestatīšana** \> **Grāmatas**) kopsavilkuma cilnē **Vispārēji** ir divi jauni lauki: **Noapaļot nolietojumu pārskata valūtā** un **Atstāt atlikušo vērtību pārskata valūtā**.

- Ņemot vērā, ka tagad nolietojuma priekšlikums aprēķina summas gan uzskaites valūtā, gan pārskata valūtā, pamatlīdzekļu žurnāls ir atjaunināts, lai tas parādītu nolietojuma summas pārskata valūtā. Nolietojuma transakcijām darījuma valūta vienmēr ir uzskaites valūta. Tāpēc šīs summas arī turpmāk tiks norādītas kolonnās **Debets** un **Kredīts**. Režģim ir pievienotas divas jaunas kolonnas **Debets pārskata valūtā** un **Kredīts pārskata valūtā**.

    - Jaunie lauki ir pieejami tikai tad, ja transakcijas tips ir kāds no četriem nolietojuma tipiem: **Nolietojums**, **Nolietojuma korekcija**, **Ārkārtas nolietojums** vai **Speciālā nolietojuma atļautais daudzums**.
    - Ja nolietojuma transakcijas tips ir ievadīts pamatlīdzekļu žurnālā, pārskata valūtas summas tiks parādītas jaunajās kolonnās. Šīs summas var mainīt.
    - Ja uzskaites valūta un pārskata valūtas virsgrāmatā ir vienādas, summas tiks sinhronizētas. Ja maināt summu **Kredīts**, summa **Kredīts pārskata valūtā** tiks automātiski mainīta, lai nodrošinātu savstarpēju atbilstību.
    - Ievadot pamatlīdzekļu žurnālā jebkuru citu transakcijas tipu, summas **Debets pārskata valūtā** un **Kredīts pārskata valūtā** nekad netiek rādītas nedz pirms, nedz pēc grāmatošanas. Uzskaites valūtas un pārskata valūtas summas joprojām ir pieejamas dokumentā, kas tiek grāmatots virsgrāmatā.
