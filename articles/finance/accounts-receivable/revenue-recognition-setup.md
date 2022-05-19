---
title: Ieņēmumu atzīšanas iestatīšana
description: Šajā tēmā ir aprakstītas ieņēmumu atzīšanas iestatīšanas opcijas un to izmantošana.
author: kweekley
ms.date: 04/28/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 86690af303eb87335c980bd7dae3ae34ce06a2a0
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725516"
---
# <a name="revenue-recognition-setup"></a>Ieņēmumu atzīšanas iestatīšana
[!include [banner](../includes/banner.md)]

Ir pievienots modulis **Ieņēmumu atzīšana**, kas ietver izvēlnes elementus visiem nepieciešamajiem iestatījumiem. Šajā tēmā ir aprakstītas iestatīšanas opcijas un to izmantošana.

> [!NOTE]
> Ieņēmumu atzīšanas līdzeklis tagad ir iespējots pēc noklusējuma, izmantojot līdzekļu pārvaldību. Ja jūsu organizācija neizmanto šo līdzekli, varat to izslēgt **līdzekļa pārvaldības** darbvietā.
>
> Ieņēmumu atzīšana, tostarp komplektu funkcionalitāte, netiek atbalstīta izmantošanai Commerce kanālos (e-komercija, POS, zvanu centrs). Krājumus, kas ir konfigurēti ieņēmumu atzīšanai, nedrīkst pievienot pasūtījumiem vai transakcijām, kas izveidotas Commerce kanālos.

Modulim **Ieņēmumu atzīšana** ir tālāk norādītās iestatīšanas opcijas.

- Ieņēmumu atzīšanas žurnāli
- Ieņēmumu atzīšanas parametri
- Ieņēmumu grafiki 
- Krājumu iestatīšana

    - Krājumu grupas un izlaistās preces
    - Ieņēmumu grafika definēšana
    - Ieņēmumu cenas definēšana
    - Krājumu iestatīšana

        - Ieņēmumu grafika definēšana
        - Ieņēmumu cenas definēšana

    - Grāmatošanas metodes
    - Komplekti

        - Komplekta komponenti
        - Komplekta krājums

- Projektu iestatījumi

## <a name="revenue-recognition-journals"></a>Ieņēmumu atzīšanas žurnāli

Ieņēmumu atzīšanai ir ieviests jauns žurnāla veids. Žurnāls ir obligāts un izmantojams divos scenārijos.

Pirmais scenārijs iestājas pēc visu līgumsaistību izpildes, kad atliktie ieņēmumi tiek atzīti, izveidojot ieņēmumu atzīšanas žurnālu, kas ir balstīts uz detalizēto informāciju par ieņēmumu grafiku. Žurnāls ietver uzskaites ierakstu, kas pārvieto bilanci no atlikto ieņēmumu virsgrāmatas konta uz ieņēmumu virsgrāmatas kontu.

Otrais scenārijs iestājas, kad pēc atkārtotas sadales tiek izveidots žurnāls. Atkārtota sadale notiek, kad pārdošanas pasūtījuma rinda tiek pievienota iepriekš rēķinā iekļautam pārdošanas pasūtījumam vai kad tiek izveidots jauns pārdošanas pasūtījums, kas ietver rindu, kura ir daļa no sākotnējā līguma. Ja rēķins tika grāmatots pirms jaunas pārdošanas pasūtījuma rindas pievienošanas, grāmatotajam debitora rēķinam ir jāizveido labošanas uzskaites ieraksts.

Žurnāls ir iestatīts lapā **Žurnālu nosaukumi** (**Ieņēmumu atzīšana \> Iestatīšana \> Žurnālu nosaukumi**). Žurnāla veidam ir jāiestata vērtība **Ieņēmumu atzīšana**. 

## <a name="parameters-for-revenue-recognition"></a>Ieņēmumu atzīšanas parametri

Ieņēmumu atzīšanas iestatījumi tiek konfigurēti lapas **Virsgrāmatas parametri** cilnē **Ieņēmumu atzīšana** (**Ieņēmumu atzīšana \> Iestatīšana \> Virsgrāmatas parametri**). Pieejami tālāk norādītie iestatījumi.

- **Ieņēmumu atzīšanas žurnāla nosaukums** — atlasiet žurnālu, kas tika izveidots ieņēmumu atzīšanai. Žurnāls ir nepieciešams, kad ieņēmumi tiek atzīti no ieņēmumu grafika vai kad pārdošanas pasūtījumam, kas jau ir iekļauts rēķinā, tiek veikta atkārtota sadale.
- **Iespējot atlaides sadalījuma metodi** — iestatiet šo opciju uz **Jā**, lai noteiktu ieņēmumu cenu, sadalot patieso tirgus vērtību, kas noteikta katras izlaistās preces ieņēmumu cenā. Šis sadalījums ietver jebkuru rindas atlaižu sadalījumu krājumos. Ja šī opcija ir iestatīta uz **Nē**, sistēma izmanto vidējo cenu, kas noteikta katras izlaistās preces ieņēmumu cenā. Ja šī opcija ir iestatīta uz **Nē**, bet izlaistajām precēm nav norādīta vidējā cena, ieņēmumu cenas sadale netiek veikta.
- **Iekļaut virsraksta atlaides** — iestatiet šo opciju uz **Jā**, lai noteiktu ieņēmumu cenu, sadalot virsraksta atlaides precēm. Ja šī opcija ir iestatīta uz **Nē**, virsraksta atlaide nav iekļauta ieņēmumu cenas sadalījumā.
- **Atspējot līguma termiņus** — iestatiet šo opciju uz **Jā**, ja preces, kuru ieņēmumu veids ir **Grāmatot līguma atbalstu**, var izlaist pat tad, ja tām nav definēti līguma sākuma un beigu datumi. Parasti līguma sākuma un beigu datumi ir nepieciešami krājumiem, kuru ieņēmumu veids ir **Grāmatot līguma atbalstu**. Kad līguma sākuma un beigu datumi netiek definēti, detalizēta informācija par ieņēmumu grafiku grāmatošanas vajadzībām tiek aprēķināta, izmantojot gadījumu skaitu un rēķina datumu.
- **Grāmatot rēķinu labojumus debitoru parādos, veicot atkārtotu sadali** — veicot atkārtoti sadali rēķiniem, kas jau ir iegrāmatoti, ir jālabo iegrāmatotā rēķina uzskaites ieraksts. Lietojiet šo opciju, lai norādītu, kā labojums ir veikts.

    - Iestatiet šo opciju uz **Nē**, lai ierobežotu labošanas transakcijas grāmatošanu virsgrāmatā. Kad šī opcija ir iestatīta uz **Nē**, debitoru parādos netiek izveidoti papildu dokumenti iekšējās uzskaites labojumam. Kad rēķins ir apmaksāts, segšanas procesā tiek izmantots iepriekšējais uzskaites ieraksts, lai grāmatotu visas termiņatlaides vai visu realizēto peļņu vai zaudējumus.
    - Iestatiet šo opciju uz **Jā**, lai automātiski izveidotu storno dokumentu un jaunu rēķinu labošanas transakcijai debitoru parādos. Tā kā šis labojums ir iekšējās uzskaites labojums, jaunie dokumenti netiek sūtīti vai nodoti debitoram. Storno dokuments tiek nosegts ar sākotnējo rēķinu, un jauno laboto rēķinu apmaksā debitors. Ņemiet vērā, ka visi trīs dokumenti tiek rādīti pārskatos, piemēram, debitora pārskatā.

[![Iestatījumu informācija.](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Ieņēmumu grafiki

Lai varētu atlikt ieņēmumus, katram gadījumam jāizveido ieņēmumu grafiks. Piemēram, ja jūsu organizācija piedāvā atbalstu sešu mēnešu, 12 mēnešu, 18 mēnešu un 24 mēnešu periodos, jums jāizveido ieņēmumu grafiks katram periodam. Ieņēmumu grafika iestatījumi nosaka, kā ieņēmumu cena tiek sadalīta atlasītajā periodu skaitā. Tie nosaka arī noklusējuma datumus, kas tiek ievadīti ieņēmumu grafikam, kurš tiek izveidots, grāmatojot rēķinu.

Ja ieņēmumi tiek atzīti pēc atskaites punkta, ieteicams izveidot ieņēmumu atzīšanas grafiku atbilstoši atskaites punktu skaitam neatkarīgi no atzīšanas datumiem. Pēc grafiku izveides varat tos rediģēt, lai tie atspoguļotu paredzamos atskaites punktu datumus. Šie ieraksti var tikt aizturēti līdz brīdim, kad tiek paziņots, ka atskaites punkts ir sasniegts un ieņēmumus var atzīt.

Ieņēmumu grafiki tiek izveidoti lapā **Ieņēmumu grafiki** (**Ieņēmumu atzīšana \> Iestatīšana \> Ieņēmumu grafiki**).

[![Ieņēmumu grafiki.](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Ievadiet aprakstošas vērtības laukos **Ieņēmumu grafiks** un **Apraksts**. Tālāk norādītie papildu iestatījumi tiek izmantoti, lai izveidotu ieņēmumu grafiku, kad rēķins ir iegrāmatots.

- **Gadījumi** — ievadiet mēnešu vai ieņēmumu atlikšanas gadījumu skaitu.
- **Automātiska aizturēšana** — atzīmējiet šo izvēles rūtiņu, ja, grāmatojot rēķinu, visas ieņēmumu grafika rindas nepieciešams aizturēt automātiski. Aizturēšana ir jānoņem no katras grafika rindas manuāli pirms rindas atlikto ieņēmumu atzīšanas.
- **Automātiskie līguma termiņi** — atzīmējiet šo izvēles rūtiņu, ja līguma sākuma un beigu datumi ir jāiestata automātiski. Šie datumi tiek iestatīti automātiski tikai izlaistajām precēm, kuru ieņēmumu veids ir **Grāmatot līguma atbalstu**. Līguma sākuma datums tiek automātiski iestatīts uz pārdošanas pasūtījuma rindas pieprasīto nosūtīšanas datumu, un līguma beigu datums tiek automātiski iestatīts uz sākuma datumu, kuram pieskaitīts mēnešu vai gadījumu skaits, kas definēts ieņēmumu grafika iestatījumos. Piemēram, precei pārdošanas pasūtījuma rindā ir viena gada garantija. Noklusējuma ieņēmumu grafiks ir **12M** (12 mēneši), un šim ieņēmumu ir atzīmēta izvēles rūtiņa **Automātiskie līguma termiņi**. Ja pārdošanas pasūtījuma rindas pieprasītais nosūtīšanas datums ir 2019. gada 16. decembris, līguma noklusējuma sākuma datums ir 2019. gada 16. decembris un līguma noklusējuma beigu datums ir 2020. gada 15. decembris.
- **Atzīšanas bāze** — atzīšanas bāze nosaka, kā ieņēmumu cena tiek sadalīta pa gadījumiem.

    - **Ik mēnesi pēc dienām** — summa tiek sadalīta, pamatojoties uz katra mēneša faktisko dienu skaitu.
    - **Ik mēnesi** — summa tiek sadalīta vienādi atbilstoši mēnešu skaitam, kas definēts gadījumos.
    - **Gadījumi** — summa tiek sadalīta vienādi atbilstoši gadījumu skaitam, bet tā var ietvert papildu periodu, atlasot parametru **Faktiskais sākuma datums** kā atzīšanas metodi.
    - **Finanšu periods pēc dienām** — summa tiek sadalīta, pamatojoties uz katra finanšu perioda faktisko dienu skaitu. 

         - **Mēneši pēc dienām** un **Finanšu periods pēc dienām** būs vienādi, ja finanšu periods seko kalendārajiem mēnešiem. Vienīgais izņēmums ir tad, kad atpazīšanas nosacījumi ir iestatīti uz **mēneša/perioda beigām** un **līguma sākuma** un **beigu datuma** lauki pārdošanas pasūtījuma rindā tiek atstāti tukši.

- **Atzīšanas metode** — atzīšanas metode nosaka datumus, kas tiek iestatīti rēķina ieņēmumu grafikā.

    - **Faktiskais sākuma datums** — grafiks tiek izveidots, izmantojot līguma sākuma datumu (krājumiem, kuru atbalsts tiek grāmatots \[PCS\]) vai rēķina datumu (svarīgiem un nesvarīgiem krājumiem).
    - **Mēneša/perioda 1. diena** — datums pirmajā grafika rindā ir līguma sākuma datums (vai rēķina datums). Tomēr visas turpmākās grafiku rindas tiek izveidotas mēneša vai finanšu perioda pirmajam datumam.
    - **Mēneša puses sadalījums** — pirmās grafika rindas datums ir atkarīgs no rēķina datuma. Ja rēķins ir iegrāmatots no mēneša pirmā līdz piecpadsmitajam datumam, ieņēmumu grafiks tiek izveidots, izmantojot mēneša pirmo dienu. Ja rēķins ir iegrāmatots sešpadsmitajā datumā vai vēlāk, ieņēmumu grafiks tiek izveidots, izmantojot nākamā mēneša pirmo dienu.

        - **Vidējā mēneša sadalījumu** nevar atlasīt, ja atpazīšanas bāze ir iestatīta uz **Finanšu periods pēc dienām**.

    - **Nākamā mēneša/perioda 1. diena** — datums, kurā sākas grafiks, ir nākamā mēneša vai finanšu perioda pirmā diena.
    - **Mēneša/perioda beigas** — datums pirmajā grafika rindā ir līguma sākuma datums (vai rēķina datums). Tomēr visas turpmākās grafiku rindas tiek izveidotas mēneša vai finanšu perioda pēdējai dienai. 

Atlasiet pogu **Detalizēta informācija par ieņēmumu grafiku**, lai skatītu vispārīgos periodus un procentuālās vērtības, kas tiek atzītas katrā periodā. Pēc noklusējuma vērtība **Atzīšanas procentuālā vērtība** tiek vienādi sadalīta atbilstoši periodu skaitam. Ja atzīšanas bāze ir iestatīta kā **Ik mēnesi**, atzīšanas procentuālo vērtību var mainīt. Mainot atzīšanas procentuālās vērtības, brīdinājuma ziņojums jūs informēs, ka kopsumma nav vienāda ar 100 procentiem. Ja saņemat šo ziņojumu, varat turpināt rediģēt rindas. Tomēr kopējā procentuālajai vērtībai jābūt vienādai ar 100, pirms aizverat lapu.

[![Detalizēta informācija par ieņēmumu grafiku.](./media/revenue-schedule-details-2nd-scrn.png)](./media/revenue-schedule-details-2nd-scrn.png)

## <a name="inventory-setup"></a>Krājumu iestatīšana

Varat atzīt pārdošanas pasūtījumos izlaisto preču ieņēmumus, bet ne ar pārdošanas kategorijām pārdošanas pasūtījumos vai brīva teksta rēķiniem, ja dokumentā nav ietverti nekādi krājumi. Atlases, ko veicat, iestatot izlaistās preces, nosaka, kā krājuma ieņēmumi tiek atzīti. Piemēram, atlases nosaka, vai ieņēmumu cena tiek sadalīta un vai ieņēmumi tiek atlikti, izmantojot ieņēmumu grafiku.

Iestatīšanu var sākt lapas **Krājumu grupa** kopsavilkuma cilnē **Ieņēmumu atzīšana** (**Ieņēmumu atzīšana \> Iestatīšana \> Krājumu un preču iestatīšana \> Krājumu grupa**). Šajā lapā ir vairāki iestatījumu lauki. Šie lauki tiek izmantoti, lai iestatītu noklusējuma vērtības tikai nesen izlaistajām precēm, kas izveidotas sistēmā. Izveidojot jaunas preces, šeit iestatītās vērtības tiek ievadītas pēc noklusējuma krājumu grupai. Varat ignorēt izlaisto preču noklusējuma vērtības lapā **Izlaistās preces** (**Ieņēmumu atzīšana \> Iestatīšana \> Krājumu un preču iestatīšana \> Izlaistās preces**). Noklusējuma vērtības, kas iestatītas izlaistajām precēm, pēc tam tiek pārnestas uz pārdošanas pasūtījumu.

## <a name="item-groups-and-released-products"></a>Krājumu grupas un izlaistās preces

### <a name="define-the-revenue-schedule"></a>Ieņēmumu grafika definēšana

Ieņēmumi pārdošanas pasūtījuma rindā tiek atlikti, ja izlaistajai precei ir definēts ieņēmumu grafiks, kas pēc noklusējuma tiek izmantots pārdošanas pasūtījuma rindā. Ja iestatījums jāizmanto precei pēc noklusējuma, varat definēt ieņēmumu grafiku lapas **Krājumu grupa** kopsavilkuma cilnē **Ieņēmumu atzīšana** (**Ieņēmumu atzīšana \> Iestatīšana \> Krājumu un preču iestatīšana \> Krājumu grupa**). Varat arī definēt izlaistās preces iestatījumu lapas **Izlaistās preces** kopsavilkuma cilnē **Ieņēmumu atzīšana** (**Ieņēmumu atzīšana \> Iestatīšana \> Krājumu iestatīšana \> Izlaistās preces**).

Laukā **Ieņēmumu grafiks** atlasiet ieņēmumu grafiku, kas norāda periodu, kurā ieņēmumi ir jāatliek. Ieņēmumu grafiks tiek ievadīts pārdošanas pasūtījuma rindā automātiski, un detalizēta informācija par grafiku tiek veidota, grāmatojot pārdošanas pasūtījuma rēķinu.

### <a name="define-the-revenue-price"></a>Ieņēmumu cenas definēšana

Krājumu grupas un izlaistās preces var iestatīt, izmantojot vidējās cenas metodi vai atlaides sadalījuma metodi. Abām metodēm ir nepieciešami dažādi iestatījumi lapā **Izlaistās preces**.

- **Vai ieņēmumu sadalījums ir aktīvs** — iestatiet šo opciju uz **Jā**, lai iekļautu izlaisto preci ieņēmumu sadalījuma aprēķinā. Ja šī opcija ir iestatīta uz **Nē**, izlaistā prece izmanto vidējās cenas metodi, ja vidējā cena ir definēta. Ja vidējā cena nav definēta, pārdošanas pasūtījuma rindā norādītā vienības cena tiek izmantota, lai grāmatotu ieņēmumus vai atliktos ieņēmumus.
- **Ieņēmumu veids** — atlasiet ieņēmumu veidu, kas nosaka izlaisto preci.

    - **Svarīgi** — krājums ir organizācijas ieņēmumu primārais avots. Šī vērtība ir noklusējuma iestatījums.
    - **Nav svarīgi** — krājums nav organizācijas ieņēmumu primārais avots. Izmantojot vidējās cenas iestatījumus, cena netiek iekļauta vidējā cenā un pēc tam tiek sadalīta. Piemēram, svarīgam krājumam ir fiksēta cena, kas jāatzīst kā ieņēmumi. Ja tiek piemērota atlaide, tā var netikt iekļauta svarīgu krājumu ieņēmumos, bet **tikai** līdz fiksētam cenas apmēram. Atlikusī atlaides daļa tiek atskaitīta no ieņēmumiem par nesvarīgiem krājumiem. Atlaide var arī tikt iekļauta ieņēmumos par svarīgiem krājumiem.
    - **Grāmatot līguma atbalstu** — krājums atbalsta citus elementus, kas ir iekļauti pārdošanai debitoram. Ieņēmumu cena tiek sadalīta starp svarīgām un nesvarīgām precēm, kas iekļautas pārdošanā. Atkarībā no iestatījumiem PCS krājumiem var nebūt nepieciešams definēt līguma sākuma un beigu datumus pārdošanas pasūtījuma rindā.

- **Neiekļaut izņēmumā** — iestatiet šo opciju uz **Jā**, lai norādītu, ka krājuma vidējo cenu nevar koriģēt zem definētās minimālās procentuālās vērtības vai virs maksimālās procentuālās vērtības. Visas ieņēmumu cenas tiks iegūtas no citas izlaistās preces ieņēmumu cenas, kas iekļauta pārdošanas pasūtījumā. Ja šī opcija ir iestatīta uz **Nē**, krājuma vidējo cenu var koriģēt vai neiekļaut. Ņemiet vērā, ka, pārdodot vairāk nekā vienu krājumu, kas ir iestatīts kā vidējā cena, ir jāiestata vismaz viena izlaistā prece, kur opcija **Neiekļaut izņēmumā** ir iestatīta uz **Nē**. Šādā veidā pastāv vismaz viens krājums, kam var piešķirt jebkādas atšķirības ieņēmumu cenā.
- **Vidējā cena** — iestatiet šo opciju uz **Jā**, lai norādītu, ka krājuma ieņēmumu cena ir jākoriģē tā, lai tā būtu vienāda ar vidējo cenu, ja tā ir mazāka par jūsu norādīto minimālo toleranci vai lielāka par maksimālo toleranci, un ka izņēmuma summa ir jāpiešķir rindām, kurās ir preces, kurām opcija **Neiekļaut izņēmumā** ir iestatīta uz **Nē**.

    - **Maksimālā tolerance** — ievadiet procentuālo vērtību, kas ir lielāka par atļauto vidējo cenu.
    - **Minimālā tolerance** — ievadiet procentuālo vērtību, kas ir mazāka par atļauto vidējo cenu.

Pēc tam, kad pabeigsit izlaistās preces iestatījumu konfigurēšanu, lapā **Ieņēmumu cenas** (dodieties uz **Ieņēmumu atzīšana \> Iestatīšana \> Krājumu iestatīšana \> Izlaistās preces** un pēc tam darbību rūtī cilnē **Pārdošana** grupā **Ieņēmumu atzīšana** atlasiet **Ieņēmumu cenas**) jums ir manuāli jādefinē ieņēmumu cena, ievadot patiesās vērtības cenu vai vidējo cenu (ja lietojat vidējās cenas metodi).

[![Ieņēmumu cenas.](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Ieņēmumu cena, kas tiek definēta manuāli šajā lapā, tiek izmantota, lai noteiktu ieņēmumu cenas sadalījumu katram pārdošanas pasūtījumam, pamatojoties uz definētajiem kritērijiem. Katrs kritērijs tiek saskaņots ar pārdošanas pasūtījuma rindu, lai noteiktu ieņēmumu cenu, kas jāizmanto sadalījuma procesā.

- **Krājuma kods** un **Krājumu saistība** — ieņēmumu cenu var definēt atsevišķai precei vai preču grupai. Laukā **Krājuma kods** atlasot **Tabula**, atlasiet izlaisto preci laukā **Krājumu saistība**. Laukā **Krājuma kods** atlasot **Grupa**, atlasiet krājumu grupu laukā **Krājumu saistība**.
- **Konta kods** un **Konta/grupas numurs** — ieņēmumu cenu var definēt visiem debitoriem, atsevišķam debitoram vai debitoru grupai. Laukā **Konta kods** atlasot **Visi**, cena tiek izmantota visiem debitoriem. Laukā **Konta kods** atlasot **Tabula**, atlasiet debitoru laukā **Konta/grupas numurs**. Laukā **Konta kods** atlasot **Grupa**, atlasiet debitoru grupu laukā **Konta/grupas numurs**.
- **Valūta** — katrai valūtai, kurā tiek ievadīts pārdošanas pasūtījums, ir jāievada atsevišķa ieņēmumu cena. Piemēram, ja pašlaik pārdodat ASV dolāros, Kanādas dolāros un eiro, jums jādefinē ieņēmumu cena visās trīs valūtās. Ieņēmumu cena netiek pārrēķināta no vienas valūtas, piemēram, uzskaites valūtas, uz jebkurām citām transakciju valūtām, ko lietojat.
- **Saraksta summa vai procentuālā vērtība** — norādiet, vai ieņēmumu cena ir iestatīta kā saraksta cenas summa vai procentuālā vērtība. Atlasot **Saraksta procentuālā vērtība**, lietotāji summas vietā var ievadīt vidējo cenu kā saraksta cenas procentuālo vērtību. Vērtība **Saraksta procentuālā vērtība** tiek izmantota tikai izlaistām precēm, kas iestatītas kā PCS krājumi.
- **Ieņēmumu sadalījuma cena** — atkarībā no vērtības, ko atlasījāt laukā **Saraksta summa vai procentuālā vērtība**, ievadiet summu vai procentuālo vērtību, lai attēlotu ieņēmumu cenu, kas tiek izmantota, lai sadalītu ieņēmumus pa pārdošanas pasūtījuma elementiem.
- **No datuma** un **Līdz datumam** — ievadiet datumu diapazonu, kuram ir aktīva ieņēmumu cena. Šie lauki nav obligāti.

Ja lapā **Virsgrāmatas parametri** opcija **Iespējot atlaides sadalījuma metodi** ir iestatīta uz **Jā** un ja lauks **Ieņēmumu veids** izlaistajai precei ir iestatīts uz **Grāmatot līguma atbalstu**, jums jānorāda arī krājumi, ko atbalsta izlaistā prece. Šo iestatījumu var iespējot lapā **Iestatīšanas bāze** (dodieties uz **Ieņēmumu atzīšana \> Iestatīšana \> Krājumu iestatīšana \> Izlaistās preces** un pēc tam darbību rūtī cilnē **Pārdošana** grupā **Ieņēmumu atzīšana** atlasiet **Iestatīšanas bāze**).

Lapā **Iestatīšanas bāze** pievienojiet ierakstu katrai krājumu grupai, ko atbalsta šis krājums. Veicot ieņēmumu sadali, ieņēmumu cena tiks sadalīta pa svarīgām un nesvarīgām PCS krājuma daļām.

### <a name="posting-profiles"></a>Grāmatošanas metodes

Trīs papildu grāmatošanas veidi atbalsta iespēju atlikt ieņēmumus. Šos grāmatošanas veidus var iestatīt lapas **Grāmatošana** cilnē **Pārdošanas pasūtījums** (**Ieņēmumu atzīšana \> Iestatīšana \> Krājumu un preču iestatīšana \> Grāmatošana**).

- **Atliktie ieņēmumi** — ievadiet ieņēmumu cenas galveno kontu, kas iegrāmato atliktajos ieņēmumos (nevis ieņēmumos). Ieņēmumu cena tiek atlikta, ja pārdošanas pasūtījuma rindai ir ieņēmumu grafiks.
- **Atliktā pārdoto preču pašizmaksa** — ievadiet pārdoto preču pašizmaksas summas galveno kontu, kas iegrāmato atliktajā pārdoto preču pašizmaksā, ja arī ieņēmumi tiek atlikti.
- **Daļējs rēķina ieņēmumu klīrings** — ievadiet klīringa konta galveno kontu, kas tiek izmantots, kad pārdošanas pasūtījums tiek daļēji iekļauts rēķinā vai kad notiek atkārtota sadale. Bilance šajā kontā tiek atgriezta uz 0 (nulli), kad pārdošanas pasūtījumi tiek pilnībā iekļauti rēķinā.

### <a name="bundles"></a>Komplekti

Komplekta krājumi ir unikālas izlaistās preces, kas iestatītas tā, lai tās iekļautu komponentus. Šis iestatījums tiek veikts, izmantojot materiālu komplekta (MK) funkcionalitāti. Kad pārdošanas pasūtījumā tiek ievadīts komplekta krājums, ieņēmumu cenu un ieņēmumu grafiku noteikšanai tiek izmantoti atsevišķi komponenti. Tomēr debitora izdrukātie dokumenti, piemēram, pārdošanas pasūtījums un rēķins, atspoguļo komplekta krājumu.

#### <a name="bundle-components"></a>Komplekta komponenti

Komponenti, kas iekļauti komplektā, ir jāiestata lapā **Izlaistās preces** (**Ieņēmumu atzīšana \> Iestatīšana \> Krājumu un preču iestatīšana \> Izlaistās preces**). Šie komponenti ir izlaistās preces, un tie ir jāiestata tādā pašā veidā kā preces, kas iekļautas MK. Piemēram, izlaistā prece var būt krājums ar veidu **Krājums** vai **Pakalpojums**, bet tā ir jāpiešķir krājumu modeļu grupai, kurā opcija **Uzkrātā prece** ir iestatīta uz **Jā**. Papildinformāciju skatiet MK krājumu iestatīšanas dokumentācijā.

Komponenti ir arī jāiestata ieņēmumu atzīšanai, it kā tie būtu preces, ko var pārdot atsevišķi pārdošanas pasūtījumā. Piemēram, pārliecinieties, ka katram komponentam ir definēta pareiza ieņēmumu cena un ka cenas bāze ir iestatīta PCS krājumiem.

#### <a name="bundle-items"></a>Komplekta krājumi

Iestatot komplekta krājumu, lapā **Izlaistās preces** ir jāiestata divi lauki (**Ieņēmumu atzīšana \> Iestatīšana \> Krājumu un preču iestatīšana \> Izlaistās preces**).

- Kopsavilkuma cilnē **Inženieris** laukā **Ražošanas veids** krājumam jābūt iestatītam kā MK krājumam.
- Kopsavilkuma cilnē **Vispārīgi** laukā **Komplekts** krājumam jābūt atzīmētam kā komplekta krājumam.

Pēc tam komponenti ir jāpiešķir komplektam/MK pamatkrājumam lapā **MK versijas** (dodieties uz **Ieņēmumu atzīšana \> Iestatīšana \> Krājumu un preču iestatīšana \> Izlaistās preces** un pēc tam darbību rūtī cilnē **Inženieris** grupā **MK** atlasiet **MK versijas**). Papildinformāciju skatiet MK iestatīšanas dokumentācijā.

[![Izlaistās preces, MK grafiki.](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Ja komplekta pamatkrājums un komplekta komponenti ir iestatīti sadalei, komplekta ieņēmumu cena tiks sadalīta pa komponentiem, pamatojoties uz to ieņēmumu seguma procentuālajām vērtībām.

## <a name="project-setup"></a>Projektu iestatījumi

Ieņēmumu atzīšanu var izmantot arī pārdošanas pasūtījumiem, kas tiek izveidoti, izmantojot laika un materiālu projektu. Pārdošanas pasūtījumiem, kas izveidoti no projektiem, ir jādefinē galvenie konti projekta grāmatošanas metodēs, kas tiek izmantotas projekta rēķinu grāmatošanai. Galvenie konti tiek definēti lapā **Virsgrāmatas grāmatošanas iestatījumi** (**Ieņēmumu atzīšana \> Iestatīšana \> Projekta iestatīšana \> Virsgrāmatas grāmatošanas iestatījumi**).

- **Atliktie rēķina ieņēmumi** (sadaļā **Ieņēmumu konti**) — ievadiet ieņēmumu cenas galveno kontu, kas iegrāmato atliktajos ieņēmumos (nevis ieņēmumos). Ieņēmumu cena tiek atlikta, ja pārdošanas pasūtījuma rindai ir ieņēmumu grafiks.
- **Atliktās izmaksas** (sadaļā **Izmaksu konti**) — ievadiet pārdoto preču pašizmaksas summas galveno kontu, kas iegrāmato atliktajā pārdoto preču pašizmaksā, ja arī ieņēmumi tiek atlikti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
