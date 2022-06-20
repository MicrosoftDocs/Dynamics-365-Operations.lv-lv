---
title: Kādēļ es nevaru atgriezt šo darījumu?
description: Šajā rakstā ir aprakstīti dažādi pamatojumi, kāpēc darbības nevar atcelt. Tajā ir uzskaitīti arī šīs problēmas risinājumi.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9a8b26584b1a9b82440583db693cd14daa580e22
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876187"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Kādēļ es nevaru atgriezt šo darījumu?

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti dažādi pamatojumi, kāpēc darbības nevar atcelt. Tajā ir uzskaitīti arī šīs problēmas risinājumi.

## <a name="symptom"></a>Simptoms

Organizācijas var saskarties ar situācijām, kad tām ir jāatgriež iegrāmatotā darbība. Dažreiz sistēma neļaus tām atsaukt šīs darbības. Šī uzvedība var uzdot divus jautājumus:

- Kādēļ es nevaru atgriezt šo darījumu?
- Kā masveida apgriešanas funkcija ietekmē šo uzvedību?

## <a name="resolution"></a>Novēršana

Pirms darbību stornšanas darbībām ir jāatbilst noteiktiem kritērijiem. Pārējās šī raksta sadaļas sniedz apstiprinājumu katram modulim. Lai gan šis raksts fokusējas Microsoft Dynamics uz darbībām 365 Finansēs, dažas koncepcijas un apstiprināšanu var pielietot citām programmām, piemēram, Dynamics 365 Supply Chain Management.

Turklāt darbības apvērses vieta var ietekmēt to, vai to var atcelt. Piemēram, kreditora maksājumu, kas ir iegrāmatots kā čeks, var atcelt tikai no bankas kontu darbību lapas sadaļas **Čeki**. To nevar anulēt no **Virsgrāmatas dokumentu** darbību lapas.

Ja **Līdzekļu pārvaldības** darbvietā ir ieslēgta **Vairāku dokumentu funkcijas masveida apgriešana** (ko sauc arī par masveida apgriešanas funkciju), tā ietekmē, cik darbību var atcelt un kur tās var atcelt. Šī funkcija nodrošina divas priekšrocības, ja tā ir ieslēgta:

- Dažiem darbību tipiem vienlaicīgi var atlasīt un anulēt vairāk nekā vienu darbību no žurnāla, no kura tā grāmatota, vai no **Dokumentu darbību** lapas. Tomēr individuālām darbībām jābūt neatgriezeniskām, pirms funkcija ir ieslēgta. Pirms šīs funkcijas ieviestas, darbības bija jāpārtrauc pa vienam.
- *Dažas* apakšgrāmatas transakcijas var anulēt žurnālā (Virsgrāmatas žurnālā) vai **Dokumentu transakciju** lapā. Tie nav apgriezti no apakšgrāmatas lapas. Piemēram, kreditoru rēķinu žurnālu var atgriezt tikai no **Kreditoru darbību** lapas. Tomēr to tagad var anulēt arī no Virsgrāmatas puses no žurnāla vai **Dokumentu darbību** lapas. Katrā šī raksta sadaļā ir izskaidroti darījumu veidi, uz kuriem šis atvieglojums neattiecas.

Masveida apgriešanas funkcija **neiespējo** vairāk darbību tipu apgriešanu. Ja darbības tipu iepriekš nav iespējams apgriezt, to vairs nav iespējams apgriezt pēc tam, kad funkcija ir ieslēgta. Piemēram, pirkšanas pasūtījuma kreditoru rēķinus nevar atsaukt, neskatoties uz to, vai masveida atgriešanas funkcija ir ieslēgta.

Plašāku informāciju par masveida apgriešanas līdzekli skatiet sadaļā [Žurnāla grāmatošanas anulēšana](reverse-journal-posting.md).

## <a name="general-ledger"></a>Virsgrāmata

Virsgrāmatas korekcijas tiek ievadītas, tikai izmantojot Virsgrāmatas kontus. Tāpēc tie atjaunina tikai Virsgrāmatu.

Ja masveida anulēšanas funkcija ir izslēgta, lielāko daļu Virsgrāmatas korekciju var atcelt atsevišķi no Virsgrāmatas lapas **Darbības \<main account\>** (**LedgerTransAccount**). (Precīzu lapas nosaukumu atšķiras atkarībā no atlasītā galvenā konta.) Lapa parāda katru darbību, kas ir grāmatota galvenajā kontā. Parasti tas tiek atvērts no **Apgrozījuma bilances saraksta** lapas vai atlasot **Darbības dokumentu** **Darbību** lapā.

Ja masveida anulēšanas funkcija ir ieslēgta, vienu vai vairākus Virsgrāmatas dokumentus tagad var atcelt **Dokumentu darbību** lapā un no žurnāla, no kura darbība tika grāmatota. Izņēmumi ir Virsgrāmatas ārvalstu valūtas pārvērtēšanas, konsolidācijas un gada beigu slēgšanas darbības. Šīs darbības tiek apgrieztas no lapām, no kurām tika palaista gada beigu aizvēršana.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Pamatojums, kāpēc darījumus nevar anulēt

Darbības nevar atcelt šādu iemeslu dēļ:

- Virsgrāmatas žurnāls:

    - Finanšu periods ir aizturēts vai neatgriezeniski slēgts:

        - Ja atceļošais datums ir finanšu periodā, kas nav atvērts, darbību nevar atgriezt.
        - Ja darbība atbalsta atceļoša datuma ievadi, darbību var atcelt, mainot atcelšanas datumu uz atvērtu periodu.

    - Gada beigu slēgšanas procesa izpilde:

        - Darbības uzskaites datums ir finanšu gadā, kas ir bijis līdz gada beigu slēdzam. Lai gan periods finanšu gadā vēl ir atvērts, darījumu nevar atcelt, ja finanšu gadam ir palaists gada beigu slēgšanas process. Finanšu gada statuss ir citāds nekā finanšu gada periodiem.
        - Gada beigu slēgšanas var atcelt, un tad darbību var atcelt. Šī pieeja, iespējams, nav opcija. Var būt vienkāršāk manuāli ievadīt atceļošo darbību slēgtā finanšu gada vai nākamā finanšu gada atvērtā periodā atkarībā no finanšu slēgšanas procesa statusa. Ja jauna darbība tiek grāmatota finanšu gada atvērtā periodā, kas ticis slēgts gada beigu slēgšanas procesā, gada beigu slēgšana ir jāpalaiž vēlreiz.

    - Darbības anulēšana jau tiek apstrādāta:

        - Ja darbība tiek apgriezta, procesam jābūt pabeigtam. Atsevišķu anulēšanas procesu nevar veikt. 
        - Pēc atcelšanas pabeigšanas anulēto darbību var atsaukt atkārtoti (t.i., atgriešanu var atcelt).

    - Virsgrāmatas nosegšana:

        - Ja viena vai vairākas darbības rindas ir nosegtas Virsgrāmatā, izmantojot **Virsgrāmatas nosegšanas** periodisko uzdevumu (**Virsgrāmata \> Periodiskie uzdevumi \> Virsgrāmatas nosegšana)**, lai ieraksts būtu tabulā LedgerTransSettlement, darbību nevar atcelt.
        - Gada beigu slēgšanas var atcelt, un tad darbību var atcelt.

    - Starpuzņēmums:

        - Ja darbība ir starpuzņēmuma darbība, to nevar atcelt.
        - Darbība **nav** starpuzņēmumu darbība, bet tiek grāmatota galvenajā kontā "līdz" vai "no", kas ir definēts **Starpuzņēmumu iestatījumu** lapā.

    - Uzkrājumi:

        - Ja uzkrātais Virsgrāmatas dokuments tiek atgriezts, uzkrātais ieraksts un visas atbilstošās uzkrājuma apakš darbības tiks atceltas.
        - Atsevišķas uzkrājumu apakštransakcijas nevar atcelt.

- Ieņēmumu atzīšanas žurnāli:

    - Ieņēmumu atpazīšanas darījumus nevar atsaukt.
    - Ja ieņēmumi tiek atpazīti caur ieņēmumu atzīšanas žurnālu, dokuments tiek grāmatots tikai Virsgrāmatas kontos. Tādējādi, tādās lapās kā **Dokumentu darbības**, darbības parādās tā, it kā tās būtu tikai Virsgrāmatas ieraksti.

- Ārvalstu valūtas pārvērtēšana:

    - Ārvalstu valūtas pārvērtēšanas darbības var atsaukt, bet tikai no Virsgrāmatas **Ārvalstu valūtas pārvērtēšanas** lapas, no kuras tika palaista pārvērtēšana.
    - Atgriešanu var pabeigt tikai tad, ja tā ir grāmatota atvērtajā finanšu periodā.

- Konsolidācija:

    - Konsolidācijas darbības var atcelt, bet tikai no **Konsolidācijas darbību** lapas.
    - Atgriešanu var pabeigt tikai tad, ja tā ir grāmatota atvērtajā finanšu periodā.

- Gada noslēgums:

    - Gada noslēguma darbības (gan slēgšanas, gan sākuma darbības) var atcelt šādos veidos:

        - Ja Virsgrāmatas gada beigu slēgšanas uzlabojumu līdzeklis ir izslēgts, atlasiet dialoglodziņā **Gada beigās** opciju **Atsaukt iepriekšēju slēgšanu**.
        - Ja Virsgrāmatas gada beigu uzlabojumu līdzeklis ir ieslēgts, atlasiet uzņēmuma un finanšu gada ierakstus, kas tika izveidoti gada beigu slēgšanas lapai **Gada noslēgums**, un pēc tam atlasiet **Atcelt gada noslēgumu**.

    - Ņemiet vērā, ka gada beigu slēgšanas anulēšana faktiski dzēš slēgšanas un atvēršanas darbības. Atceļošs dokuments nekad netiek grāmatots.

## <a name="accounts-payable"></a>Kreditoru parādi

Vairāki darījumu tipi atjaunina kreditoru apakšgrāmatas. Piemēri ietver kreditoru rēķinus, kreditoru rēķinu žurnālus un izdevumu pārskatus.

Ja funkcija Masveida atgriešana ir izslēgta, darbības var atcelt atsevišķi vai nu no rēķinu **Kreditoru darbību** lapas, vai **Bankas konta** lapā čeku maksājumiem.

Ja masveida anulēšanas funkcija ir ieslēgta, vienu vai vairākus Virsgrāmatas dokumentus tagad var atcelt **Dokumentu darbību** lapā un no žurnāla, no kura darbība tika grāmatota. Tomēr kreditora maksājumus joprojām var atcelt tikai no bankas konta. Turklāt kreditora darbības nevar atsaukt no **Virsgrāmatas \<main account\>** lapas Darbības. Tos var atcelt tikai no **Dokumentu darbību** lapas.

Ņemiet vērā, ka dažas darbības vispār nevar atsaukt. Piemēri ietver pirkšanas pasūtījuma kreditora rēķinus un elektroniskos kreditoru maksājumus.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Pamatojumi, kāpēc darījumus nevar anulēt

Darbības nevar atcelt šādu iemeslu dēļ:

- Finanšu periods ir aizturēts vai neatgriezeniski slēgts:

    - Ja atceļošais datums ir finanšu periodā, kas nav atvērts, darbību nevar atgriezt.
    - Ja darbība atbalsta atceļoša datuma ievadi, darbību var atcelt, mainot atcelšanas datumu uz atvērtu periodu.

- Virsgrāmatas gada beigu slēgšanas procesa izpilde:

    - Darbības uzskaites datums ir finanšu gadā, kas noslēgts Virsgrāmatā. Lai gan periods finanšu gadā vēl ir atvērts, darījumu nevar atcelt, ja finanšu gadam ir palaists gada beigu slēgšanas process. Finanšu gada statuss ir citāds nekā finanšu gada periodiem.
    - Gada beigu slēgšanas var atcelt, un tad darbību var atcelt. Šī pieeja, iespējams, nav opcija. Var būt vienkāršāk manuāli ievadīt atceļošo darbību slēgtā finanšu gada vai nākamā finanšu gada atvērtā periodā atkarībā no finanšu slēgšanas procesa statusa. Ja jauna darbība tiek grāmatota finanšu gada atvērtā periodā, kas ticis slēgts gada beigu slēgšanas procesā, gada beigu slēgšana ir jāpalaiž vēlreiz.

- Apakšgrāmatas žurnāla ieraksts nav pārsūtīts uz Virsgrāmatu:

    - Šis iemesls attiecas tikai uz kreditora rēķiniem, kas nav pirkšanas pasūtījumi.
    - Lai ierakstu pārsūtītu uz Virsgrāmatu, lietojiet **Apakšgrāmatas žurnāla ierakstus**, kas vēl nav pārsūtīti. Pēc tam kreditora rēķinu, kas nav pirkšanas pasūtījums, var atcelt no **Kreditoru darbību** lapas.

- Nosegšana:

    - Darbība (piemēram, rēķins vai maksājums) tiek segta vai atzīmēta segšanai.

        - Jūs varat pārbaudīt, vai darbība ir nosegta vai atzīmēta segšanai, atlasot lapā **Skatīt nosegšanas** vai **Nosegšana \> Nosegšanas vēsture** lapā **Debitoru darbības**.
        - Nosegšanu var atsaukt arī no lapas **Kreditoru darbības** (**Nosegšana \> Atsaukt nosegšanu**), ja kāda no darbībām ir jāatgriež.

- Dokuments ietver vairāk nekā vienu apakšgrāmatas darījumu, kas ievadīts, izmantojot vienu dokumenta numuru (viena dokumenta izsniegšana).
- Rēķins nav apstiprināts:

    - Ja **Apstiprinājuma** izvēles rūtiņa rēķinā nav atzīmēta, rēķinu nevar atgriezt.

        - Šajā gadījumā apstiprinājums neattiecas uz apstiprinājumiem darbplūsmas procesā, bet uz rēķina **Apstiprināšanas** opciju. Šo opciju lieto, lai neļautu rēķina apmaksu. Parasti tas tiek izmantots kreditoru rēķinu reģistra rēķiniem.

- Darbība ir rēķina pūlā:

    - Rēķinu pūlā nevar atsaukt tieši no **Kreditoru darbību** lapas. Tā vietā tā ir jāatgriež caur atcelšanas procesu **Rēķinu apstiprināšanas žurnāla** lapā.

- Darbībai ir pamata rēķins, kas ir labots (Indijas lokalizācija).
- Darbībai ir parādzīmes statuss **Rēķins pārskaitīts**.
- Darbība tiek izmantota daļējai nodokļu apmaksai.
- Darbība ietver kreditora kontu, bet tiek atcelta no nepareizas lapas, piemēram, lapas **Darbības \<main account\>**:

    - Kā šis iemesls iesaka, pat ja ir ieslēgta masveida apgriešanas funkcija, dažas apakšgrāmatas darbības var atcelt tikai no noteiktām lapām.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Darbību tipi, ko nevar anulēt

Nevar atsaukt šādus darījumu veidus:

- Ārvalstu valūtas pārvērtēšana:

    - Atšķirībā no Virsgrāmatas ārvalstu valūtas pārvērtēšanas, debitoru un kreditoru ārvalstu valūtas pārvērtēšanu nevar atsaukt. Tā vietā pārvērtēšana ir jāpalaiž vēlreiz, izmantojot rēķina datumu. Šajā gadījumā pārvērtēšana izmanto maiņas kursu no rēķina datuma, un pamatā nerealizētā peļņa vai zaudējumi tiek uz 0 (nulle). Tāpēc rezultāts ir līdzīgs iepriekšējās pārvērtēšanas atcelšanas rezultātam. Tomēr ievērojiet, ka tā pati summa netiks atgriezta, ja rēķinā tika mainīts noklusējuma valūtas maiņas kurss.

- Pirkšanas pasūtījuma rēķina atgriešana:

    - Lai atsauktu kreditora rēķinu, jāizveido kredīta rēķins. Plašāku informāciju par to, kā izveidot atceļoša darbība, skatiet Sadaļā [Pirkšanas atgriešanas pasūtījuma izveide](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Parādzīme
- Bankas akreditīva eksportēšana

## <a name="accounts-receivable"></a>Debitoru parādi

Vairāki darījumu tipi atjaunina kreditoru apakšgrāmatas. Piemēri iekļauj debitoru rēķinus no pārdošanas pasūtījumiem, debitoru rēķiniem, kas ievadīti caur Virsgrāmatas žurnālu, brīvā teksta rēķinus, debitoru maksājumus un norakstīšanas.

Ja funkcija Masveida atgriešana ir izslēgta, darbības var atcelt atsevišķi vai nu no rēķinu **Debitoru darbību** lapas, vai **Bankas konta** lapā depozītiem. Papildinformāciju par to, kā atgriezt maksājumu, skatiet [tālāk šī raksta sadaļā Skaidra](cant-reverse-transctns.md#cash-and-bank-management) nauda un bankas pārvaldība.

Ja masveida anulēšanas funkcija ir ieslēgta, vienu vai vairākus debitoru dokumentus tagad var atcelt **Dokumentu darbību** lapā un no žurnāla, no kura darbība tika grāmatota. Tomēr depozītus joprojām var anulēt tikai no bankas konta, un brīvā teksta rēķinus var anulēt tikai no sākotnējās lapas (ja ir ieslēgta funkcija, kas ļauj veikt korekcijas). Turklāt kreditora darbības nevar atsaukt no Virsgrāmatas lapas **Darbības \<main account\>**. Tomēr tos var atcelt tikai no **Dokumentu darbību** lapas.

Ņemiet vērā, ka dažas darbības vispār nevar atsaukt. Piemēri ietver pārdošanas pasūtījumu debitoru rēķinus un norakstīšanas.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Pamatojums, kāpēc darījumus nevar anulēt

Darbības nevar atcelt šādu iemeslu dēļ:

- Finanšu periods ir aizturēts vai neatgriezeniski slēgts:

    - Ja atceļošais datums ir finanšu periodā, kas nav atvērts, darbību nevar atgriezt.
    - Ja darbība atbalsta atceļoša datuma ievadi, darbību var atcelt, mainot atcelšanas datumu uz atvērtu periodu.

- Virsgrāmatas gada beigu slēgšanas procesa izpilde:

    - Darbības uzskaites datums ir finanšu gadā, kas ir bijis līdz Virsgrāmatas gada noslēgumam. Lai gan periods finanšu gadā vēl ir atvērts, darījumu nevar atcelt, ja finanšu gadam ir palaists gada beigu slēgšanas process. Finanšu gada statuss ir citāds nekā finanšu gada periodiem.
    - Gada beigu slēgšanas var atcelt, un tad darbību var atcelt. Šī pieeja, iespējams, nav opcija. Var būt vienkāršāk manuāli ievadīt atceļošo darbību slēgtā finanšu gada vai nākamā finanšu gada atvērtā periodā atkarībā no finanšu slēgšanas procesa statusa. Ja jauna darbība tiek grāmatota finanšu gada atvērtā periodā, kas ticis slēgts gada beigu slēgšanas procesā, gada beigu slēgšana ir jāpalaiž vēlreiz.

- Apakšgrāmatas žurnāla ieraksts nav pārsūtīts uz Virsgrāmatu:

    - Šis iemesls attiecas tikai uz brīva teksta rēķiniem.
    - Lai ierakstu pārsūtītu uz Virsgrāmatu, lietojiet **Apakšgrāmatas žurnāla ierakstus**, kas vēl nav pārsūtīti. Brīvā teksta rēķinu pēc tam var atsaukt vai labot, ja labojumu funkcionalitāte ir aktivizēta.

- Nosegšana:

    - Darbība (piemēram, rēķins vai maksājums) tiek segta vai atzīmēta segšanai.

        - Jūs varat pārbaudīt, vai darbība ir nosegta vai atzīmēta segšanai, atlasot lapā **Skatīt nosegšanas** vai **Nosegšana \> Nosegšanas vēsture** lapā **Debitoru darbības**.
        - Nosegšanu var atsaukt arī no lapas **Debitoru darbības** (**Nosegšana \> Atsaukt nosegšanu**), ja kāda no darbībām ir jāatgriež.

- Dokuments ietver vairāk nekā vienu apakšgrāmatas darījumu, kas ievadīts, izmantojot vienu dokumenta numuru (viena dokumenta izsniegšana).
- Rēķins nav apstiprināts:

    - Ja **Apstiprinājuma** izvēles rūtiņa rēķinā nav atzīmēta, rēķinu nevar atgriezt.

        - Šajā gadījumā apstiprinājums neattiecas uz apstiprinājumiem darbplūsmas procesā, bet uz rēķina **Apstiprināšanas** opciju. Šo opciju lieto, lai neļautu rēķina apmaksu. Kaut arī šī opcija parasti tiek izmantota Parādi kreditoriem, tā ir pieejama arī debitoru parādu rēķiniem, kas tiek ievadīti caur žurnāliem.

- Darbībai ir pamata rēķins, kas ir labots (Indijas lokalizācija).
- Darbība ietver debitora kontu, bet tiek atcelta no nepareizas lapas, piemēram, lapas **Darbības \<main account\>**:

    - Kā šis iemesls iesaka, pat ja ir ieslēgta masveida apgriešanas funkcija, dažas apakšgrāmatas darbības var atcelt tikai no noteiktām lapām.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Darbību tipi, ko nevar anulēt

Nevar atsaukt šādus darījumu veidus:

- Ārvalstu valūtas pārvērtēšana:

    - Atšķirībā no Virsgrāmatas ārvalstu valūtas pārvērtēšanas, debitoru un kreditoru ārvalstu valūtas pārvērtēšanu nevar atsaukt. Tā vietā pārvērtēšana ir jāpalaiž vēlreiz, izmantojot rēķina datumu. Šajā gadījumā pārvērtēšana izmanto maiņas kursu no rēķina datuma, un pamatā nerealizētā peļņa vai zaudējumi tiek uz 0 (nulle). Tāpēc rezultāts ir līdzīgs iepriekšējās pārvērtēšanas atcelšanas rezultātam. Tomēr ievērojiet, ka tā pati summa netiks atgriezta, ja rēķinā tika mainīts noklusējuma valūtas maiņas kurss.

- Darbība, kas koriģējusi ieturēto nodokli
- Pārdošanas pasūtījuma debitora rēķins:

    - Lai atsauktu darījumu, jāizveido kredīta rēķins vai atgriešana. Informāciju par to, kā izveidot atcelšanas darbību, skatiet [Pārdošanas atgriešanas](../../supply-chain/warehousing/sales-returns.md).

- Vekselis
- Kases aparāta darbība
- Papildu korekcija
- Procentu paziņojums
- Atgādinājuma vēstules
- Bankas akreditīvs
- Eksporta krava
- Ieņēmumu atzīšanas žurnāli:

    - Ja ieņēmumi tiek atpazīti caur ieņēmumu atzīšanas žurnālu, dokuments tiek grāmatots tikai Virsgrāmatas kontos. Tāpēc tās parādās it kā tās būtu tikai Virsgrāmatas ieraksti. Šos ierakstus nevar atcelt, jo ieņēmumu grafiks netiks atkārtoti atvērts, lai ieņēmumus atpazītu atkal.

## <a name="cash-and-bank-management"></a>Kases un bankas vadība

Vairāki transakciju tipi atjaunina bankas apakšgrāmatas, izmantojot Virsgrāmatas žurnālu. Piemēri ietver kreditoru maksājumus, debitoru maksājumus un bankas pārskaitījumus.

Ja funkcija Masveida atgriešana ir izslēgta, darbības var atcelt atsevišķi vai nu no rēķinu **Debitoru darbību** lapas, vai **Bankas konta** lapā depozītiem.

Ja masveida anulēšanas funkcija ir ieslēgta, vienu vai vairākus Virsgrāmatas dokumentus tagad var atcelt **Dokumentu darbību** lapā un no žurnāla, no kura darbība tika grāmatota. Tomēr depozītus joprojām var atcelt tikai no bankas konta. Turklāt bankas transakcijas nevar atsaukt no Virsgrāmatas lapas **Darbības \<main account\>**. Tomēr tos var atcelt tikai no **Dokumentu darbību** lapas.

Ņemiet vērā, ka dažas darbības vispār nevar atsaukt. Piemēri ietver elektroniskos kreditoru maksājumus.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Pamatojums, kāpēc darījumus nevar anulēt

Darbības nevar atcelt šādu iemeslu dēļ:

- Finanšu periods ir aizturēts vai neatgriezeniski slēgts:

    - Ja atceļošais datums ir finanšu periodā, kas nav atvērts, darbību nevar atgriezt.
    - Ja darbība atbalsta atceļoša datuma ievadi, darbību var atcelt, mainot atcelšanas datumu uz atvērtu periodu.

- Virsgrāmatas gada beigu slēgšanas procesa izpilde:

    - Darbības uzskaites datums ir finanšu gadā, kas ir bijis līdz Virsgrāmatas gada noslēgumam. Lai gan periods finanšu gadā vēl ir atvērts, darījumu nevar atcelt, ja finanšu gadam ir palaists gada beigu slēgšanas process. Finanšu gada statuss ir citāds nekā finanšu gada periodiem.
    - Gada beigu slēgšanas var atcelt, un tad darbību var atcelt. Šī pieeja, iespējams, nav opcija. Var būt vienkāršāk manuāli ievadīt atceļošo darbību slēgtā finanšu gada vai nākamā finanšu gada atvērtā periodā atkarībā no finanšu slēgšanas procesa statusa. Ja jauna darbība tiek grāmatota finanšu gada atvērtā periodā, kas ticis slēgts gada beigu slēgšanas procesā, gada beigu slēgšana ir jāpalaiž vēlreiz.

- Nosegšana:

    - Darbība (piemēram, rēķins vai maksājums) tiek segta vai atzīmēta segšanai.

        - Jūs varat pārbaudīt, vai darbība ir nosegta vai atzīmēta segšanai, atlasot lapā **Skatīt nosegšanas** vai **Nosegšana \> Nosegšanas vēsture** lapā **Kreditoru darbības** vai **Debitoru darbības**.
        - Nosegšanu var atsaukt arī no lapas **Kreditoru darbības** vai **Debitoru darbības** (**Nosegšana \> Atsaukt nosegšanu**), ja kāda no darbībām ir jāatgriež.

- Dokuments ietver vairāk nekā vienu apakšgrāmatas darījumu, kas ievadīts, izmantojot vienu dokumenta numuru (viena dokumenta izsniegšana).
- Pagaidu darbības:

    - Ja darbība ir saistīta ar pagaidu maksājumu, to nevar atgriezt.
    - Ja pagaidu maksājums ir jāatgriež, vispirms maksājums ir jānotīra no pagaidu konta uz banku. Pēc tam maksājumu var atcelt, ja tas atbilst citiem apstiprināšanas kritērijiem.

- Darījums ietver bankas kontu, bet tiek anulēts no lapas **Darbības \<main account\>** vai no nepareizas apakšvirsgrāmatas, piemēram, Debitoru parādi vai Kreditoru parādi:

    - Kā šis iemesls iesaka, pat ja ir ieslēgta masveida apgriešanas funkcija, dažas apakšgrāmatas darbības var atcelt tikai no noteiktām lapām.

- Bankas ārvalstu valūtas pārvērtēšana:

    - Bankas ārvalstu valūtas pārvērtēšanu var atsaukt. Tomēr atcelšana var būt novērsta, ja pabeigsiet atcelšanas soļus hronoloģiskā secībā. Piemēram, ja pārvērtēšana tika veikta martā un aprīlī, marta pārvērtēšanu nevar atcelt, kamēr netiks atsaukta aprīļa pārvērtēšana.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Darbību tipi, ko nevar anulēt

Nevar atsaukt šādus darījumu veidus:

- Kreditoru maksājumi, kas tika veikti kā elektronisko līdzekļu pārskaitījumi (EFT)
- Parādzīmes
- Vekseļi

## <a name="fixed-assets"></a>Pamatlīdzekļi

Vairāki transakciju tipi atjaunina pamatlīdzekļu apakšvirsgrāmatas. Piemēri ietver iegādi un nolietojumu.

Ja masveida apgriešanas funkcija ir izslēgta, darbības var apgriezt atsevišķi no **Kreditoru darbību** lapas, no **Pamatlīdzekļu darbību** lapas vai no Pamatlīdzekļu izlaišanas atkarībā no darbības tipa.

Ja masveida anulēšanas funkcija ir ieslēgta, vienu vai vairākus Virsgrāmatas dokumentus tagad var atcelt **Dokumentu darbību** lapā un no žurnāla, no kura darbība tika grāmatota.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Pamatojums, kāpēc darījumus nevar anulēt

Darbības nevar atcelt šādu iemeslu dēļ:

- Finanšu periods ir aizturēts vai neatgriezeniski slēgts:

    - Ja atceļošais datums ir finanšu periodā, kas nav atvērts, darbību nevar atgriezt.
    - Ja darbība atbalsta atceļoša datuma ievadi, darbību var atcelt, mainot atcelšanas datumu uz atvērtu periodu.

- Virsgrāmatas gada beigu slēgšanas procesa izpilde:

    - Darbības uzskaites datums ir finanšu gadā, kas noslēgts Virsgrāmatā. Lai gan periods finanšu gadā vēl ir atvērts, darījumu nevar atcelt, ja finanšu gadam ir palaists gada beigu slēgšanas process. Finanšu gada statuss ir citāds nekā finanšu gada periodiem.
    - Gada beigu slēgšanas var atcelt, un tad darbību var atcelt. Šī pieeja, iespējams, nav opcija. Var būt vienkāršāk manuāli ievadīt atceļošo darbību slēgtā finanšu gada vai nākamā finanšu gada atvērtā periodā atkarībā no finanšu slēgšanas procesa statusa. Ja jauna darbība tiek grāmatota finanšu gada atvērtā periodā, kas ticis slēgts gada beigu slēgšanas procesā, gada beigu slēgšana ir jāpalaiž vēlreiz.

- Iegādes:

    - Ja pirkšanas pasūtījuma kreditora rēķinā ir notikusi iegāde, atgriešana jāveic, ievadot kreditora kreditora rēķinu. Plašāku informāciju par to, kā izveidot atcelšanas darbību, skatiet Sadaļā [Pirkšanas atgriešanas pasūtījuma izveide](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Iegāde radās projekta darbībai.
    - Iegādi nevar atsaukt pēc tam, kad pamatlīdzeklim ir grāmatots nolietojums. Nolietojums ir jāatgriež pirms iegādes atsaukšanas.
    - Ja pamatlīdzekļa vērtības modeļa vai nolietojuma grāmatas statuss nav atvērts, darbību nevar atsaukt.

- Utilizācija:

    - Utilizācija tiek veikta, izmantojot brīva teksta rēķinu:

        - Brīvā teksta rēķina labošana tiek bloķēta, ja tas ietver pamatlīdzekli. Tomēr, ja pamatlīdzeklis tiek izslēgts caur žurnālu, brīvā teksta rēķinu var atcelt no pamatlīdzekļa ieraksta.

    - Ja pamatlīdzekļa vērtības modeļa vai nolietojuma grāmatas statuss nav atvērts, darbību nevar atsaukt.

- Nolietojums:

    - Nolietojumu **var** atcelt, ja tiek iegrāmatots arī sekojošais nolietojums. Tomēr jūs saņemsit brīdinājumu, jo šī pieeja nav labākā prakse.
    - Ja pamatlīdzekļa vērtības modeļa vai nolietojuma grāmatas statuss nav atvērts, darbību nevar atsaukt.

- Darbības (vai apgrieztās darbības) noteiktam pamatlīdzeklim un pamatlīdzekļu grāmatai pastāv dokumenta darbības datumā vai vēlāk.
- Darījums ietver bankas kontu, bet tiek anulēts no lapas **Darbības \<main account\>** vai no nepareizas apakšvirsgrāmatas, piemēram, Debitoru parādi vai Kreditoru parādi:

    - Kā šis iemesls iesaka, pat ja ir ieslēgta masveida apgriešanas funkcija, dažas apakšgrāmatas darbības var atcelt tikai no noteiktām lapām.
    - Ja iegāde notiek nepirkta pasūtījuma kreditora rēķinā vai kreditora rēķinu žurnālā, to var atcelt tikai kreditoru darbību lapā, kas atrodas sadaļā **Kreditoru parādi**.
    - Ja līdzeklis tiek iegādāts no pamatlīdzekļu izlaides, to var anulēt no **Saistību darbību** lapas, izlaižot pamatlīdzekli.
