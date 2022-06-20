---
title: Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana
description: Šajā rakstā ir sniegta informācija par uzlabojumiem, kas ietekmē Virsgrāmatas nosegšanas un Virsgrāmatas gada beigu slēgšanas.
author: kweekley
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 30d3cc0bbd97cd006f12d06cda64ee63cb42252e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902521"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana

[!include [banner](../includes/banner.md)]


Microsoft Dynamics 365 Finanšu versijā 10.0.25 līdzekli **Virsgrāmatas nosegšanas un gada beigu** **slēgšanas līdzekli var izmantot līdzekļu pārvaldības darbvietā**. Šis līdzeklis pievieno divus primāros uzlabojumus, kas ietekmē Virsgrāmatas segšanu un Virsgrāmatas gada beigu aizvēršanu.

Virsgrāmatas gada beigu slēgšanas laikā nosegtās Virsgrāmatas darbības vairs netiks ietvertas nākamā finanšu gada sākuma bilancē. Šis uzlabojumi nodrošina, ka sākuma bilancē tiek iekļautas tikai nenosegtās Virsgrāmatas darbības. Ir svarīgi, kad tiek palaista Virsgrāmatas ārvalstu valūtas pārvērtēšana. Ārvalstu valūtas pārvērtēšana tiek palaista tikai Virsgrāmatas darbībām ar statusu Nav **nosegts**. Tomēr pirms **bija atbrīvota virsgrāmatas nosegšanas un gada beigu slēgšanas funkcijas apzināšana,** **·** **sākuma bilance summēja abas darbības, kurām ir statuss Nosegts un tām, kurām ir statuss Nav nosegts un** apkopotās summas statuss tika iestatīts uz Nav nosegts.**·**

Otrais uzlabojumi ļauj jums grāmatot detalizētas sākuma bilances darbības Virsgrāmatas gada beigu slēgšanas laikā. Ja opcija **Saglabāt informāciju gada beigu slēgšanas laikā** **ir** iestatīta uz Jā, katrai virsgrāmatas darbībai, kas nav nosegta, tiks izveidota atsevišķa sākuma bilance. Šis iestatījums tiek definēts katram galvenajam kontam Virsgrāmatas nosegšanas iestatījumā. Uzturot detalizētas darbības sākuma bilancei, jūs ļoti uzlabosiet spēju nosegtās Virsgrāmatas darbības nākamajā finanšu gadā.

Lai atbalstītu jaunos uzlabojumus, tika veiktas izmaiņas Virsgrāmatas nosegšanai un gada beigu aizvēršanai.

### <a name="changes-to-ledger-settlement"></a>Virsgrāmatas nosegšanas izmaiņas

- Virsgrāmatas nosegšana jāveic finanšu gada laikā.
- Virsgrāmatas nosegšana jāveic darbībām vienā galvenajā kontā. Galvenais konts tagad ir nepieciešams filtrs Virsgrāmatas nosegšanas **lapā**.
- Virsgrāmatas nosegšanu un Virsgrāmatas nosegšanas atcelšanu nevar veikt darbībām, kas ir grāmatotas slēgtā finanšu gadā (citiem vārdiem, ir veikta gada beigu slēgšana).

### <a name="changes-to-year-end-close"></a>Izmaiņas gada beigu slēgšanas

- Gada beigu slēgšanu nevar atcelt, ja nākamajā finanšu gadā ir nosegtas atvērtas bilances darbības. Šī izmaiņa tiek piemērota, **·** **atsaucot** gada beigu slēgšanu vai atkārtoti palaižot gada beigu slēgšanu un virsgrāmatas parametros atkārtoti slēdzot gadu, dzēst esošos gada beigu ierakstus.
- Ja gada **beigu slēgšanas laikā** **detalizēta** informācija par visu Virsgrāmatas nosegšanas bilances kontu ir iestatīta uz Jā, šim galvenajam kontam tiks izveidotas detalizētāka sākuma bilances darbības.

## <a name="before-you-enable-the-feature"></a>Pirms funkcijas iespējošanas

Sakarā ar izmaiņām funkcionalitātē un datu modelī, ir svarīgi pirms funkcijas aktivizēšanas ņemt vērā šādus punktus:

- Tā kā sākuma bilancē tiek ņemtas vērā tikai apmaksātās darbības, jānosedz pašreizējā finanšu gada darbības, kas ir nosegtas ar iepriekšējā finanšu gada darbībām. Darbības ir jāatiestata attiecībā pret pašreizējā finanšu gada darbībām. To var izdarīt, koriģējot ierakstu pašreizējā finanšu gadā. Korekcija anualizē apkopotās sākuma bilances un korespondējošos datus ar detalizēto darbību, kas nepieciešama, lai nosegtu virsgrāmatas ierakstus šajā gadā. 

  > [!IMPORTANT]
  > Ja tas nav izdarīts, palaižot **gada** beigu slēgšanu pašreizējam finanšu gadam, saņemsit bilances beigu kļūdas ziņojumu. Ja nav iespējams nenosegt un atiestatīt Virsgrāmatas darbības ar vienu un to pašu finanšu gadu, neiespējojiet šo līdzekli līdz pēc gada beigu slēgšanas. Iespējojiet iespēju tūlīt pēc gada beigu slēgšanas pabeigšanas un pirms visas jaunas Virsgrāmatas darbības tiek nosegtas nākamajā finanšu gadā. 
  
- Ja šī funkcija ir aktivizēta, visām darbībām, kas ir atzīmētas nosegšanai, bet nav segtas, tiks automātiski noņemtas atzīmes. Lai novērstu jebkādus darba zaudējumus, nosedziet visas atzīmētās darbības pirms iespējojat funkciju.
- Dažas organizācijas gada beigu slēgšanu vairākiem laikiem palaistu vienu un to pašu finanšu gadu. Neiespējot šo līdzekli, ja gada beigu slēgšana jau ir palaista vienu reizi un tiks vēlreiz izpildīta tam pašam finanšu gadam. Šī funkcija jāiespējo pirms pirmā gada beigu slēgšanas apstrādes vai pēc pēdējā finanšu gada beigu slēgšanas apstrādes.

  Ja vēlaties iespējot funkciju, bet gada beigu aizvēršana jau ir palaista vienu reizi, pirms funkcijas iespējošanas ir jāatgriež gada beigas.

- Tā kā nosegšana starp galvenajiem kontiem vairs nav atļauta, pielāgojiet savu kontu plānu vai procesus, kas nepieciešami, lai nodrošinātu, ka Virsgrāmatas nosegšanu var veikt vienā un tajā pašā galvenajā kontā.
- Šo līdzekli nevar iespējot, ja tiek izmantots publiskā sektora gada beigu slēgšanas process.

## <a name="set-up-ledger-settlement"></a>Iestatīt Virsgrāmatas nosegšanu

Pēc funkcijas iespējošanas un pirms nākamā gada beigu slēgšanas katrai organizācijai ir jānosaka, vai gada beigu slēgšanas laikā jūsu darbības informācija tiks uzturēta. Izvēle neietekmē sākuma bilances grāmatojumus no iepriekšējā gada beigu slēgšanas procesiem.

Opcija **Saglabāt detalizēto informāciju gada beigu slēgšanas** laikā ir iestatīta katram galvenajam kontam Virsgrāmatas nosegšanas **iestatījumu** lapā.

1.  Dodieties uz **Virsgrāmatas** > **iestatījumu Virsgrāmatas** > **parametriem**.
2.  Cilnē Virsgrāmatas **nosegšana atlasiet Virsgrāmatas** nosegšanas **kontus**.

- vai -

1.  Dodieties uz Virsgrāmatas **periodiskajiem** > **uzdevumiem, nosegšanas** > **virsgrāmatā**.
2.  Atlasiet Virsgrāmatas **nosegšanas kontus**.

Ir pievienotas divas kolonnas Virsgrāmatas nosegšanas **lapai**:
    
- **Galvenā konta tips** – šī kolonna ir tikai informatīvā nolūkā. Tas parāda tipu, kas piešķirts galvenajam kontam.
- **Uzglabāt detalizēto informāciju gada beigu** slēgšanas laikā — pēc noklusējuma opcija ir iestatīta uz **Nē**. To var iestatīt uz Jā **tikai** tad, ja vērtība **kolonnā Galvenā** konta tips ir **Bilance**, **Pamatlīdzeklis** vai **Saistības**. Kad opcija ir iestatīta uz **Nē**, sākuma bilances tiks grāmatotas kopsavilkumā, kā parasti gada beigu slēgšanas laikā. Ja tās iestatījums ir **Jā**, sākuma bilances tiks detalizēti izveidotas katrai Virsgrāmatas darbībai, kas nav nosegta galvenajam kontam.

## <a name="year-end-close"></a>Gada beigu slēgšana

Palaižot gada beigu slēgšanu, **·** > **·** > **ejot** uz Virsgrāmatas perioda slēgšanu Gada beigas, process izveido sākuma bilances galvenajiem kontiem, kas definēti Virsgrāmatas nosegšanai. Sākuma bilances tiek veidotas kopsavilkuma vai detalizētā veidā atkarībā no virsgrāmatas nosegšanas iestatījumiem. Šajā procesā tiek iekļauti virsgrāmatas darījumi, kas ir segti, neatkarīgi no tā, vai katram galvenajam kontam tiek grāmatota sākuma bilance kopsavilkuma vai detalizēta informācija.

Piemēram, 2021. finanšu 130100 galvenajā kontā tiek grāmatotas vairākas darbības.

| Žurnāla numurs | Dokuments  | Datums       | Veids      | Virsgrāmatas konts | Konta nosaukums        | Apraksts       | Valūta | Summa darījuma valūtā | Summa  | Summa pārskata valūtā |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 12/3/2021  | Lietošanas | 130100-001-    | Debitoru parādi | Pakalpojuma maksa       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 12/5/2021  | Lietošanas | 130100-002-    | Debitoru parādi | Utilītas         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 12/16/2021 | Lietošanas | 130100-001-    | Debitoru parādi | Kompensācija            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |                   | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 12/21/2021 | Lietošanas | 130100-002-    | Debitoru parādi | Starpkonta kredīts | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 12/28/2021 | Lietošanas | 130100-001-    | Debitoru parādi | Utilītas         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 12/29/2021 | Lietošanas | 130100-002-    | Debitoru parādi | Pakalpojums           | USD      | 300                            | 300     | 300                          |

No šīm darbībām trīs tiek nosegtas Virsgrāmatas nosegšanas laikā.

Rēķins ir par 175 ASV dolāriem (175 USD). Šis rēķins tika apmaksāts, izmantojot maksājumu eiro (EUR), un tika ņemta termiņatlaide.

| Žurnāla numurs | Dokuments  | Datums       | Veids      | Virsgrāmatas konts | Konta nosaukums        | Apraksts | Valūta | Summa darījuma valūtā | Summa  | Summa pārskata valūtā |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 12/5/2021  | Lietošanas | 130100-002-    | Debitoru parādi | Utilītas   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |             | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Galvenā konta konta rezultāti 130100 atkarīgi no tā, vai funkcija ir iespējota pirms gada beigu slēgšanas. Ja ir aktivizēta šī funkcija, arī rezultāts ir atkarīgs no opcijas Saglabāt informāciju iestatījuma gada beigu slēgšanas laikā.

### <a name="the-feature-isnt-enabled"></a>Līdzeklis nav iespējots.
Gada beigu slēgšanas rezultātā tiek izveidoti trīs sākuma bilances darījumi galvenajam kontam 130100 2022. gadā. Darbību summa uzskaites valūtā ir USD 525.

| Žurnāla numurs | Dokuments  | Datums     | Veids    | Virsgrāmatas konts | Konta nosaukums        | Apraksts | Valūta | Summa darījuma valūtā | Summa  | Summa pārskata valūtā |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Kaut arī maksājuma darbība PAR EUR -127,11 tika apmaksāta Virsgrāmatā, darbība joprojām ir uz priekšu kā sākuma bilance.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Līdzeklis ir iespējots un Uzglabāt detalizēto informāciju gada beigu slēgšanas laikā = Nē

Gada beigu slēgšanas rezultātā tiek izveidoti divi sākuma bilances darījumi galvenajam kontam 130100 2022. gadā. Darbību summa uzskaites valūtā joprojām ir slēgtaUSD 525 bet Virsgrāmatas apmaksātās darbības tiek izslēgtas no sākuma bilances. Konta 130100-002- kopsumma ir USD 125, nevis USD 299.12, un darbība par EUR 127,11/USD 174,12 tiek pilnībā izslēgta.

| Žurnāla numurs | Dokuments  | Datums     | Veids    | Virsgrāmatas konts | Konta nosaukums        | Apraksts | Valūta | Summa darījuma valūtā | Summa | Summa pārskata valūtā |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Līdzeklis ir iespējots un Uzglabāt detalizēto informāciju gada beigu slēgšanas laikā = Jā

Gada beigu slēgšanas rezultātā tiek izveidoti pieci sākuma bilances darījumi galvenajam kontam 130100 2022. gadā. Katrai no piecām darbībām, kas netika segtas, tiek izveidota atsevišķa sākuma bilances darbība. Darbību summa uzskaites valūtā joprojām ir USD 525.

| Žurnāla numurs | Dokuments  | Datums     | Veids    | Virsgrāmatas konts | Konta nosaukums        | Apraksts       | Valūta | Summa darījuma valūtā | Summa | Summa pārskata valūtā |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi | Pakalpojuma maksa       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi | Kompensācija            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi | Starpkonta kredīts | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi | Utilītas         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi | Pakalpojums           | USD      | 300                            | 300    | 300                          |

Paturot informāciju par transakciju, oriģinālās detalizētās darbības netiek ietekmētas. Tās tiek iegrāmatotas un nenosegtas slēgtā finanšu gadā. Šo darbību kopija tiek izveidota sākuma bilancei. Šīs vērtības no sākotnējām darbībām tiek kopētas uz sākuma bilances darbībām.

- Virsgrāmatas konts (galvenais konts un visas finanšu dimensijas)
- Summas darījuma, uzskaites un pārskata valūtās
- Apraksts
- Grāmatošanas līmenis
- Grāmatošanas tips

   > [!NOTE]
   > Grāmatošanas tipam nav piešķirtas citas sākuma bilances darbības. Tāpēc grāmatošanas tipu var izmantot, lai atšķirtu sākuma darbības, kas tika detalizēti iesniegtas uz priekšu.

Dažiem sākotnējās darbības laukiem ir jāmainās detalizētajā darbību sākuma bilancē. Sākuma bilances darbību datums vienmēr ir nākamā finanšu gada pirmā diena. Žurnāla numuram ir jāmainās, un dokumenta numurs mainās uz vērtību, kas ievadīta gada beigu slēgšanas dialoglodziņā.

Informāciju no oriģinālajām darbībām var atrast Virsgrāmatas nosegšanas **lapā**. Katra detalizēta sākuma bilances darbība rāda **sākotnējo darbības datuma** kolonnu režģī. Šī kolonna var palīdzēt saskaņot darbības jaunajā finanšu gadā. Varat atlasīt Skatīt **oriģinālo dokumentu,** lai atgrieztos pie pilna oriģinālā dokumenta.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Noslēgt darījumus
Lai segtu virsgrāmatas transakcijas, izpildiet tālāk aprakstītos norādījumus.

1. Dodieties uz Virsgrāmatas **periodiskajiem** > **uzdevumiem, nosegšanas** > **virsgrāmatā**.
2.  Iestatiet filtrus lapas augšpusē.

    1. Atlasīt datumu diapazonu. Alternatīvi atlasiet datumu intervāla kodu, lai automātiski aizpildītu datumu diapazonu.

       - Datumu diapazons nevar šķērsot finanšu gadus. Ja datumu diapazons šķērso finanšu gadus, atlasot Rādīt darbības, darbības netiks **rādītas**.
       - Ja datumu diapazons ir atvērtā finanšu gadā, darbības var nosegt un segšanu var atcelt. Ja datumu diapazons ir slēgtā finanšu gadā vai gada beigu slēgšana ir pabeigta, tiek rādītas darbības, bet tās nevar nosegt vai nenosegt. Darbību atzīmi var noņemt tikai slēgtā finanšu gadā. Ja datumu diapazons ir slēgtā finanšu gadā, **nav** pieejamas pogas Iezīmēt, **·** **Nosegt atzīmētās darbības un Atcelt** atzīmētās darbības.

    2. Atlasiet galveno kontu, par kuru jārāda darbības. Šis lauks ir obligāts. Uzmeklēšana parāda tikai galvenos kontus, kas atlasīti **uzņēmuma** kontu plāna Virsgrāmatas nosegšanas lapā.
    3. Atlasiet grāmatošanas līmeni. Nevar nosegt darbības, kas ir atšķirīgos grāmatošanas līmeņos.
    4. Lai rādītu galveno kontu un dimensijas atsevišķās kolonnās, atlasiet finanšu dimensiju kopu.

3.  Atlasiet **Rādīt darbības,** lai tiktu rādītas visas darbības, kas atbilst iestatītajiem filtriem. Ka maināt kādu no filtriem vai dimensiju kopām, vienums **Rādīt transakcijas** ir jāatlasa vēlreiz.
4.  Atlasīt rindas nosegšanai. Vērtība laukā **Atlasītā summa** lapas augšdaļā palielinās vai samazinās, lai atspoguļotu atlasīto rindu kopsummu.
5.  Kad darbību atlase pabeigta, atlasiet **Iezīmēt**. Katrai atlasītajai darbībai kolonnā Atzīmēts tiek parādīta **atzīme**. Turklāt vērtība atzīmētās summas **laukā** virs režģa palielinās vai samazinās, lai atspoguļotu atzīmēto rindu kopējo summu.
6.  Ja vērtība laukā Atzīmētā **summa** ir **0 (nulle**), atlasiet Nosegt **iezīmētās darbības**.

    - Daļēja segšana nav atļauta. Piemēram, jūs nevarat segt debeta $100 pret kredīta $90 darbību. Atlikušās $10 darbības arī jāatzīmē iekļaušanai segšanā.
    - Ievadiet segšanas datumu. Datumam jābūt vēlākam par vai vēlākam par segšanai atzīmēto darbību datumu.

Atzīmēto transakciju statuss tiek atjaunināts uz **Nosegts**.

> [!IMPORTANT]
> Tiks nosegtas visas darbības, kas atzīmētas aktīvās juridiskās personas nosegšanai, un atlasītais galvenais konts. Darbībām nav jābūt parādītām lapā. Tās tiks segtas pat tad, ja tās ir slēptas filtra dēļ.

Daži procesi, piemēram, darbības atsaukšana, automātiski nosedz Virsgrāmatas darbības. Piemēram, maksājums un rēķins tiek apmaksāts ar debitoru parādiem, un nosegšana ģenerē realizēto peļņu/zaudējumu. Maksājuma un rēķina nosegšana nenosedz nekādas Virsgrāmatas darbības, piemēram, darbības debitoru parādu Virsgrāmatas kontam. Tomēr, ja maksājums un rēķins debitoru parādos nav nosegts, atceļošs uzskaites ieraksts, kas tika grāmatots debitoru parādu nosegšanas atcelšanas laikā, rezultātā sākotnējie un atceļamie uzskaites ieraksti tiks nosegti Virsgrāmatā. Ja ir **iespējota funkcija** Apzināšana starp virsgrāmatas nosegšanu un gada beigu slēgšanu, virsgrāmatas apgriešanas nosegšana automātiski netiek veikta, ja atcelšanas datums ir citā finanšu gadā.

## <a name="use-excel-for-ledger-settlement"></a>Izmantot Excel virsgrāmatas nosegšanai

Darbības, kas parādītas Virsgrāmatas **nosegšanas** lapā, var eksportēt uz Excel. Programmā Excel var veikt turpmākās filtrēšanas darbības, lai noteiktu, kuras darbības atzīmēt nosegšanai.
Abi Virsgrāmatas nosegšanas elementi eksportē virsgrāmatas darbības tikai galvenajam kontam, kas ir atlasīts Virsgrāmatas **nosegšanas** lapā. Kaut arī slēgto finanšu gadu darbības joprojām var atzīmēt vai noņemt atzīmi, izmantojot Excel, tās nevar nosegt. Papildus tam, apmaksātās darbības nevar atsaukt šim finanšu gadam.

## <a name="make-transactions-easier-to-find"></a>Transakciju atrašanas atvieglošana

Virsgrāmatas **nosegšanas** darbību lapa ietver iespējas, kas atvieglo nosegšanai nepieciešamas darbības skatīšanu.

• Izmantojiet atzīmēto **filtru**, lai filtrētu darbības, pamatojoties uz **to,** vai ir atzīmēta izvēles rūtiņa Atzīmētās.
• Izmantojiet statusa filtru **,** lai filtrētu darbības, balstoties uz to statusu.
• Atlasiet Kārtot **pēc absolūtās summas,** lai kārtotu summas pēc absolūtās vērtības. Šādā veidā var grupēt debetus un kredītus, kuriem ir vienāda summa.

## <a name="reverse-a-settlement"></a>Nosegšanas anulēšana

Var anulēt nosegšanu, kas tika veikta kļūdaini.

1.  Izpildiet sadaļas Nosegt darbības 1. līdz [3](#settle-transactions). soli, lai parādītu interesētās darbības.
2.  Filtrā **Statuss** atlasiet **Nosegts**.
3.  Atlasīt rindas atgriešanai.
4.  Atlasiet Atcelt **atzīmētās darbības**. Visu darbību ar vienādu nosegšanas ID statuss tiek atjaunināts uz Nav **nosegts**.

> [!IMPORTANT]
> Visas darbības, kurām ir vienāds nosegšanas ID, tiks atceltas pat tad, ja tās nav atzīmētas. Piemēram, četras rindas tika atzīmētas un nosegtas. Visām četrām rindām ir viens segšanas ID. Ja atzīmēsiet vienu no šīm četrām rindām un pēc tam **atlasīsiet** Atcelt atzīmētās darbības, visas četras rindas tiks atceltas.






