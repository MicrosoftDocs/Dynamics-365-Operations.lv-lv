---
title: Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana
description: Šajā tēmā ir sniegta informācija par uzlabojumiem, kas ietekmē Virsgrāmatas segšanas un Virsgrāmatas gada beigu slēgšanu.
author: kweekley
ms.date: 01/31/2022
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
ms.openlocfilehash: acfbcf1467363262769884063efbc1a6d6e21eb1
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075735"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Virsgrāmatas norēķinu un gada beigu slēgšanas savstarpējā apzināšana

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Finance versijā 10.0.25 **līdzekļu pārvaldības** darbvietā **ir pieejama izpratne starp Virsgrāmatas segšanas un gada beigu slēgšanas** līdzekli. Šis līdzeklis pievieno divus primāros uzlabojumus, kas ietekmē Virsgrāmatas segšanu un Virsgrāmatas gada beigu slēgšanu.

Virsgrāmatas gada beigu slēgšanas laikā Virsgrāmatas darbības, kas ir nosegtas, vairs netiks iekļautas nākamā finanšu gada sākuma bilancē. Šis uzlabojums nodrošina, ka sākuma bilancē tiek iekļautas tikai nenostabilētas Virsgrāmatas darbības. Tas ir svarīgi, ja tiek palaista Virsgrāmatas ārvalstu valūtas pārvērtēšana. Ārvalstu valūtas pārvērtēšana tiek palaista tikai Tām Virsgrāmatas darbībām, kuru statuss **nav nosegts**. Tomēr pirms **tika izlaista virsgrāmatas segšanas un gada beigu slēgšanas** funkcija Informētība, sākuma bilancē tika apkopota gan darbība, kuras statuss ir Nosegts **, gan darbības, kuru statuss** **ir Nav nosegts**, un apkopotās summas statuss tika iestatīts uz **Nenosegts**.

Otrais uzlabojums ļauj grāmatot detalizētas sākuma bilances darbības Virsgrāmatas gada beigu slēgšanas laikā. **Ja gada beigu slēgšanas** opcija Paturēt detaļas ir iestatīta uz **Jā**, katrai Virsgrāmatas darbībai, kas nav nosegta, tiks izveidota atsevišķa sākuma bilance. Šis iestatījums ir definēts katram galvenajam kontam Virsgrāmatas nosegšanas iestatījumos. Saglabājot detalizētas sākuma bilances darbības, ievērojami uzlabojat iespēju nosegt nenostabilotās Virsgrāmatas darbības nākamajā finanšu gadā.

Lai atbalstītu jaunos uzlabojumus, tika veiktas izmaiņas Virsgrāmatas segšanā un gada beigu noslēgnē.

### <a name="changes-to-ledger-settlement"></a>Izmaiņas Virsgrāmatas segšanā

- Virsgrāmatas nosegšana jāveic finanšu gada laikā.
- Virsgrāmatas nosegšana jāveic darbībām vienā galvenajā kontā. Galvenais konts tagad ir obligāts filtrs Virsgrāmatas nosegšanas **lapā**.
- Virsgrāmatas segšanu un Virsgrāmatas nosegšanas storno apvēršanu nevar veikt darbībām, kas grāmatotas slēgtā finanšu gadā (citiem vārdiem sakot, ir izpildīta gada beigu slēgšana).

### <a name="changes-to-year-end-close"></a>Izmaiņas gada beigu noslēguma beigās

- Gada beigu slēgšanu nevar atsaukt, ja nākamajā finanšu gadā ir nosegtas kādas sākuma bilances darbības. Šīs izmaiņas tiek izmantotas, ja gada beigu slēgšana tiek atsaukta vai tiek atkārtoti palaista gada beigu slēgšana un **, atkārtoti aizverot gadu, Virsgrāmatas parametros ir iestatīta** **opcija Dzēst esošos gada** beigu ierakstus.
- **Ja jebkuram Virsgrāmatas nosegšanas bilances kontam ir iestatīta opcija Paturēt detalizētu informāciju gada beigu slēgšanas** laikā, **šim** galvenajam kontam tiks izveidotas detalizētākas sākuma bilances darbības.

## <a name="before-you-enable-the-feature"></a>Pirms līdzekļa iespējošana

Tā kā funkcionalitāte un datu modelis ir mainīts, pirms funkcijas iespējošana ir svarīgi ņemt vērā šādus punktus:

- Visas darbības, kas ir atzīmētas nosegšanai, bet nav nosegtas, tiks automātiski noņemtas, kad līdzeklis ir iespējots. Lai novērstu darba zudumu, pirms šī līdzekļa iespējošana nostabilizējat visas atzīmētās darbības.
- Dažas organizācijas gada beigu slēgšanu palaiž vairākas reizes vienam finanšu gadam. Neiespējojiet līdzekli, ja gada beigu slēgšana jau ir palaista vienu reizi un tiks palaista vēlreiz tajā pašā finanšu gadā. Līdzeklis ir jāiespējo pirms pirmā gada beigu slēgšanas apstrādes vai pēc finanšu gada pēdējā gada beigu slēgšanas apstrādes.

  Ja vēlaties iespējot šo līdzekli, bet gada beigu slēgšana jau ir palaista vienu reizi, lai iespējotu līdzekli, gada beigu slēgšana ir jāmaina.

- Tā kā norēķinu slēgšana finanšu gados vairs nav atļauta, ieteicams iespējot šo līdzekli pirms gada beigu slēgšanas procesa sākšanas. Pēc tam, lai nodrošinātu, ka nākamā finanšu gada sākuma bilances neietekmē iepriekšējie starpfiskālie gada norēķini, sākuma bilances darbība ir jānosedz par slēdzamo finanšu gadu.
- Tā kā norēķini starp galvenajiem kontiem vairs nav atļauti, pielāgojiet kontu plānu vai procesus pēc vajadzības, lai nodrošinātu, ka Virsgrāmatas segšanu var veikt tajā pašā galvenajā kontā.
- Līdzekli nevar iespējot, ja tiek izmantots publiskā sektora gada beigu slēgšanas process.

## <a name="set-up-ledger-settlement"></a>Iestatīt Virsgrāmatas segšanu

Pēc šī līdzekļa iespējošanas un pirms nākamā gada beigu slēgšanas katrai organizācijai ir jānosaka, vai tā saglabās detalizētu informāciju par transakciju gada beigās. Izvēle neietekmē sākuma bilances grāmatojumus no iepriekšējā gada beigu slēgšanas procesiem.

Gada **beigu slēgšanas** opcija Paturēt detalizētu informāciju ir iestatīta katram galvenajam kontam **lapā Virsgrāmatas nosegšanas iestatījumi**.

1.  Dodieties uz **VirsgrāmatasLedger** > **iestatīšanaVispārnējie** > **Virsgrāmatas parametri**.
2.  Cilnē **Virsgrāmatas nosegšana atlasiet** Virsgrāmatas nosegšanas **konti**.

- vai -

1.  Dodieties uz **VirsgrāmatasPeriodic** > **uzdevumiLedger** > **nosegšana.**
2.  Atlasiet **Virsgrāmatas nosegšanas konti**.

Lapai Virsgrāmatas nosegšanas ir pievienotas **divas kolonnas**:
    
- **Galvenā konta tips** – šī kolonna ir paredzēta tikai informatīviem nolūkiem. Tas parāda tipam, kas piešķirts galvenajam kontam.
- **Paturēt detalizētu informāciju gada beigās slēgšanas** laikā – pēc noklusējuma opcija ir iestatīta uz **Nē**. To var iestatīt uz **Jā** tikai tad, ja vērtība **kolonnā Galvenā konta tips** ir **Bilance**, **Aktīvs** vai **Saistības**. Ja opcija ir iestatīta uz **Nē**, sākuma bilances tiek grāmatotas kopsavilkumā, kā tas ir tipisks gada beigu slēgšanas laikā. Ja tas ir iestatīts uz **Jā**, sākuma bilances tiks izveidotas detalizēti katrai Virsgrāmatas darbībai, kas nav nosegta galvenajam kontam.

## <a name="year-end-close"></a>Gada beigu slēgšana

Palaižot gada beigu slēgšanu, dodoties uz **Virsgrāmatasperioda** > **slēgšanuGada** > **beigu slēgšanas**, process izveido sākuma bilances galvenajiem kontiem, kas definēti Virsgrāmatas nosegšanai. Sākuma bilances tiek veidotas kopsavilkumā vai detalizācijas ziņā atkarībā no Virsgrāmatas nosegšanas iestatījumiem. Process neietver Virsgrāmatas darbības, kas ir nosegtas, neatkarīgi no tā, vai katra galvenā konta sākuma bilance tiek grāmatota kopsavilkumā vai detalizēti.

Piemēram, 2021. finanšu gadā galvenajā kontā tiek grāmatotas vairākas darbības 130100.

| Žurnāla numurs | Dokuments  | Datums       | Veids      | Virsgrāmatas konts | Konta nosaukums        | Apraksts       | Valūta | Summa darījuma valūtā | Summa  | Summa pārskata valūtā |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 12/3/2021  | Lietošanas | 130100-001-    | Debitoru parādi | Pakalpojuma maksa       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 12/5/2021  | Lietošanas | 130100-002-    | Debitoru parādi | Utilītas         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 12/16/2021 | Lietošanas | 130100-001-    | Debitoru parādi | Kompensācija            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |                   | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 12/21/2021 | Lietošanas | 130100-002-    | Debitoru parādi | Kredīts kontā | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 12/28/2021 | Lietošanas | 130100-001-    | Debitoru parādi | Utilītas         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 12/29/2021 | Lietošanas | 130100-002-    | Debitoru parādi | Pakalpojums           | USD      | 300                            | 300     | 300                          |

No šīm darbībām trīs tiek nosegtas Virsgrāmatas nosegšanas laikā.

Ir rēķins par 175 ASV dolāriem (USD 175). Šis rēķins tika apmaksāts, veicot maksājumu eiro (EUR), un tika ņemta termiņatlaide.

| Žurnāla numurs | Dokuments  | Datums       | Veids      | Virsgrāmatas konts | Konta nosaukums        | Apraksts | Valūta | Summa darījuma valūtā | Summa  | Summa pārskata valūtā |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 12/5/2021  | Lietošanas | 130100-002-    | Debitoru parādi | Utilītas   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |             | USD      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Lietošanas | 130100-002-    | Debitoru parādi |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Galvenā konta rezultāti 130100 atkarīgi no tā, vai līdzeklis ir iespējots pirms gada beigu slēgšanas. Ja līdzeklis ir iespējots, rezultāts ir atkarīgs arī no gada beigu slēgšanas opcijas Paturēt detaļas iestatījuma.

### <a name="the-feature-isnt-enabled"></a>Līdzeklis nav iespējots
Gada beigu slēgšana izveido trīs sākuma bilances darbības galvenajam kontam 130100 2022. gadā. Darbību summa uzskaites valūtā ir USD 525.

| Žurnāla numurs | Dokuments  | Datums     | Veids    | Virsgrāmatas konts | Konta nosaukums        | Apraksts | Valūta | Summa darījuma valūtā | Summa  | Summa pārskata valūtā |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Lai gan maksājuma darījums par EUR -127,11 tika nosegts Virsgrāmatā, darījums joprojām tiek pārnests kā sākuma atlikums.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Līdzeklis ir iespējots un saglabāt detalizētu informāciju gada beigu beigās = Nē

Gada beigu slēgšana izveido divas sākuma bilances darbības galvenajam kontam 130100 2022. gadā. Darbību summa uzskaites valūtā joprojām ir USD 525, bet Virsgrāmatas nosegtās darbības tiek izslēgtas no sākuma bilances. Konta 130100-002 - kopējā summa ir USD 125 USD 299.12 vietā, un darījums par EUR 127.11 / USD 174.12 ir pilnībā izslēgts.

| Žurnāla numurs | Dokuments  | Datums     | Veids    | Virsgrāmatas konts | Konta nosaukums        | Apraksts | Valūta | Summa darījuma valūtā | Summa | Summa pārskata valūtā |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Līdzeklis ir iespējots un saglabāt detalizētu informāciju gada beigās slēgšanas laikā = Jā

Gada beigu slēgšana izveido piecas sākuma bilances darbības galvenajam kontam 130100 2022. gadā. Katrai no piecām nepabeigtajām darbībām tiek izveidota atsevišķa sākuma bilances darbība. Darbību summa uzskaites valūtā joprojām ir USD 525.

| Žurnāla numurs | Dokuments  | Datums     | Veids    | Virsgrāmatas konts | Konta nosaukums        | Apraksts       | Valūta | Summa darījuma valūtā | Summa | Summa pārskata valūtā |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi | Pakalpojuma maksa       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi | Kompensācija            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi | Kredīts kontā | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-001-    | Debitoru parādi | Utilītas         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1.1.2022. | Sākuma | 130100-002-    | Debitoru parādi | Pakalpojums           | USD      | 300                            | 300    | 300                          |

Kad tiek glabāta detalizēta informācija par darbību, sākotnējās detalizētās darbības netiek ietekmētas. Tie paliek iegrāmatoti un nemieri finanšu gadā, kas tiek slēgts. Sākuma bilancei tiek izveidota šo darbību kopija. Sākotnējās darbības vērtības tiek kopētas sākuma bilances darbībās.

- Virsgrāmatas konts (galvenais konts un visas finanšu dimensijas)
- Summas darījumu, grāmatvedības un pārskata valūtās
- Apraksts
- Grāmatošanas līmenis
- Grāmatošanas tips

   > [!NOTE]
   > Citām sākuma bilances darbībām netiek piešķirts grāmatošanas tips. Tāpēc grāmatošanas tipu var izmantot, lai detalizēti atšķirtu uzsāktās sākuma darbības.

Dažiem sākotnējo darbību laukiem ir jāmainās detalizētajās sākuma bilances darbībās. Sākuma bilances darbību datums vienmēr ir nākamā finanšu gada pirmā diena. Žurnāla numuram ir jāmainās, un dokumenta numurs mainās uz vērtību, kas ievadīta dialoglodziņā Gada beigu slēgšana.

Informāciju no sākotnējām darbībām var atrast Virsgrāmatas nosegšanas **lapā**. Katra detalizēta sākuma bilances darbība parāda režģa **kolonnu Sākotnējās darbības datums**. Šī kolonna var palīdzēt saskaņot darbības jaunajā finanšu gadā. Varat atlasīt **Skatīt oriģinālo dokumentu**, lai atgrieztos pie pilna sākotnējā dokumenta.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Noslēgt darījumus
Lai segtu virsgrāmatas transakcijas, izpildiet tālāk aprakstītos norādījumus.

1. Dodieties uz **VirsgrāmatasPeriodic** > **uzdevumiLedger** > **nosegšana.**
2.  Iestatiet filtrus lapas augšdaļā.

    1. Atlasīt datumu diapazonu. Vai arī atlasiet datumu intervāla kodu, lai automātiski aizpildītu datumu diapazonu.

       - Datumu diapazons nevar šķērsot finanšu gadus. Ja datumu diapazons krusto finanšu gadus, atlasot **Rādīt darbības**, darbības netiks rādītas.
       - Ja datumu diapazons ir atvērtā finanšu gadā, darbības var nosegt un segšanu var atsaukt. Ja datumu diapazons ir slēgtā finanšu gadā vai ja gada beigu slēgšana ir pabeigta, darbības tiek rādītas, bet tās nevar nosegt vai nesakratīt. Darbības var noņemt atzīmi tikai slēgtā finanšu gadā. Ja datumu diapazons ir slēgtā finanšu gadā, **pogas Atzīmētās** darbības **nosegt** un **Atsaukt atzīmētās darbības** nav pieejamas.

    2. Atlasiet galveno kontu, par ko rādīt darbības. Šis lauks ir obligāts. Uzmeklēšana parāda tikai galvenos kontus, kas atlasīti **uzņēmuma kontu plāna Virsgrāmatas nosegšanas** lapā.
    3. Atlasiet grāmatošanas līmeni. Nevar nosegt darbības, kas atrodas dažādos grāmatošanas slāņos.
    4. Lai galveno kontu un dimensijas rādītu atsevišķās kolonnās, atlasiet finanšu dimensiju kopu.

3.  Atlasiet **Rādīt darbības**, lai parādītu visas darbības, kas atbilst uzstādītajiem filtriem. Ka maināt kādu no filtriem vai dimensiju kopām, vienums **Rādīt transakcijas** ir jāatlasa vēlreiz.
4.  Atlasiet nosegšanas rindas. Vērtība **laukā Atlasītā summa** lapas augšdaļā palielinās vai samazinās, lai atspoguļotu kopējo summu atlasītajās rindās.
5.  Kad darbību atlase ir pabeigta, atlasiet **Atzīmēt atlasīto**. Katrai atlasītajai darbībai kolonnā Atzīmēts **tiek** parādīta atzīme. Turklāt vērtība laukā Atzīmētā **summa** virs režģa palielinās vai samazinās, lai atspoguļotu kopējo summu iezīmētajās rindās.
6.  Ja vērtība laukā Atzīmētā **summa** ir **0** (nulle), atlasiet **Nosegt atzīmētās darbības**.

    - Daļēja segšana nav atļauta. Piemēram, nevar nosegt $100 debeta transakciju pret $90 kredīta transakciju. Arī atlikusī $10 kredīta darbība ir jāatzīmē iekļaušanai norēķinā.
    - Ievadiet nosegšanas datumu. Datumam jābūt to darbību pēdējā datumā vai vēlāk, kas atzīmētas nosegšanai.

Atzīmēto transakciju statuss tiek atjaunināts uz **Nosegts**.

> [!IMPORTANT]
> Visas darbības, kuras esat atzīmējis aktīvajai juridiskajai personai un atlasītajam galvenajam kontam nosegšanai, tiks nosegtas. Darbībām nav jāparādās lapā. Tie tiks nokārtoti pat tad, ja tie ir paslēpti filtra dēļ.

Daži procesi, piemēram, darbības anulēšana, automātiski nosegt Virsgrāmatas darbības. Piemēram, maksājums un rēķins tiek nosegti debitoru parādos, un segšana ģenerē realizētos guvumus/zaudējumus. Maksājuma un rēķina segšana nenokārto Virsgrāmatas darbības, piemēram, darbības debitoru virsgrāmatas kontam. Tomēr, ja maksājums un rēķins ir atsegti debitoru parādos, stornēšanas uzskaites ieraksts, kas tika grāmatots debitoru nosegšanas apvērses laikā, izraisīs sākotnējo un stornējamo grāmatvedības ierakstu apmaksu Virsgrāmatā. Ja ir iespējota **izpratne starp Virsgrāmatas segšanu un gada beigu slēgšanas** līdzekli, virsgrāmatas apvērses segšana nenotiek automātiski, ja stornēšanas datums ir citā finanšu gadā.

## <a name="use-excel-for-ledger-settlement"></a>Excel izmantošana Virsgrāmatas nosegšanai

Darbības, kas tiek rādītas Virsgrāmatas nosegšanas **lapā**, var eksportēt uz programmu Excel. Programmā Excel var tālāk filtrēt darbības, lai noteiktu, kuras darbības atzīmēt nosegšanai.
Abas Virsgrāmatas nosegšanas entītijas eksportē Virsgrāmatas darbības tikai galvenajam kontam, kas atlasīts Virsgrāmatas nosegšanas **lapā**. Lai gan darbības slēgtajiem finanšu gadiem joprojām var atzīmēt vai neatzīmēt, izmantojot programmu Excel, tās nevar nosegt. Turklāt nosegtās darbības nevar atsaukt šim finanšu gadam.

## <a name="make-transactions-easier-to-find"></a>Transakciju atrašanas atvieglošana

**Virsgrāmatas nosegšanas** lapā ir iekļautas iespējas, kas atvieglo nosegšanai nepieciešamo darbību skatīšanu.

• Izmantojiet **filtru Atzīmēts**, lai filtrētu darbības atkarībā no tā, **vai tām ir atzīmēta izvēles rūtiņa Atzīmēt**.
• Izmantojiet **filtru Statuss**, lai filtrētu darbības, pamatojoties uz to statusu.
• Atlasiet **Kārtot pēc absolūtās summas**, lai kārtotu summas pēc absolūtās vērtības. Tādā veidā var grupēt debetus un kredītus, kuriem ir vienāda summa.

## <a name="reverse-a-settlement"></a>Nosegšanas anulēšana

Var anulēt nosegšanu, kas tika veikta kļūdaini.

1.  Izpildiet 1.–3 [. darbību sadaļā Darbību](#settle-transactions) segšana, lai parādītu jūs interesējošās darbības.
2.  Filtrā **Statuss** atlasiet **Nosegts**.
3.  Atlasiet rindas anulēšanai.
4.  Atlasiet **Atsaukt atzīmētās darbības**. Visu to darbību statuss, kurām ir vienāds nosegšanas ID, tiek atjaunināts uz **Nav nosegts**.

> [!IMPORTANT]
> Visas darbības ar vienādu nosegšanas ID tiks atsauktas, pat ja tās nav atzīmētas. Piemēram, tika atzīmētas un nosegtas četras rindas. Visām četrām rindām ir vienāds nosegšanas ID. Atzīmējot vienu no šīm četrām rindām un pēc tam atlasot **Atsaukt atzīmētās darbības**, visas četras rindas tiks atsauktas.






