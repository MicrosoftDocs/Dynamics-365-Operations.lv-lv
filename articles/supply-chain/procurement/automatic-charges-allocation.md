---
title: Automātisks maksu sadalījums
description: Maksu līdzeklis programmā Microsoft Dynamics 365 Supply Chain Management palīdz automātiski piešķirt maksas pirkšanas pasūtījumiem vai pārdošanas pasūtījumiem.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8067285237127bd43e8ff24166a15506cc0426f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983172"
---
# <a name="automatic-allocation-of-charges"></a>Automātisks maksu sadalījums

[!include [banner](../includes/banner.md)]

Balstoties uz debitoru, ar kuru strādājat, vai krājumu, kuru pārdodat, iespējams, vēlēsities piemērot noteiktas papildu maksas. Līdzeklis *maksas* programmā Microsoft Dynamics 365 Supply Chain Management palīdz automātiski piešķirt maksas pirkšanas pasūtījumiem vai pārdošanas pasūtījumiem.

Automātiskās maksas vai auto maksas tiek piemērotas automātiski, veidojot pārdošanas pasūtījumu vai pirkšanas pasūtījumu. Automātiskās maksas var definēt noteiktiem kreditoriem, debitoriem vai krājumiem. Varat arī definēt automātiskās maksas, kas attiecas uz visiem kreditoriem, debitoriem vai krājumiem.

## <a name="set-up-charges-codes"></a>Maksu kodu iestatīšana

Lai piešķirtu maksas, vispirms ir jādefinē maksu kodi.

1. Izpildiet kādu no šīm darbībām:

    - Pirkšanas pasūtījumiem: dodieties uz **Kreditori \> Maksu iestatīšana \> Maksas kodi**.
    - Pārdošanas pasūtījumiem: dodieties uz **Debitori \> Maksu iestatīšana \> Maksas kodi**.

1. Lai izveidotu maksu kodu, darbību rūtī atlasiet **Jauns**.
1. Jaunā ieraksta galvenē iestatiet tālāk norādītos laukus.

    - **Maksu kods** — ievadiet maksu kodu.
    - **Apraksts** — ievadiet maksu aprakstu.
    - **Krājumu PVN grupa** — atlasiet krājumu PVN grupu, ja tā ir piemērojama.
    - **Proporcionālā likme** — iestatiet šo opciju uz *Jā*, Ja vēlaties proporcionāli novērtēt savas maksas. Šī opcija ir pieejama tikai pārdošanas pasūtījumiem.
    - **Maksimālā summa** — ievadiet maksas kodam maksimāli atļauto summu. Šis lauks tiek izmantots, lai pārbaudītu kreditoru rēķinu maksas. Tas ir pieejams tikai pirkšanas pasūtījumiem.

        > [!NOTE]
        > Lai ieslēgtu funkcionalitāti pirkšanas pasūtījumu maksu validēšanai, dodieties uz **Kreditori \> Iestatījumi \> Kreditoru parametri**. Sadaļas **Rēķina validācija** kopsavilkuma cilnē **Rēķina validācija** iestatiet opciju **Iespējot rēķinu salīdzināšanas validāciju** uz *Jā*.

1. Kopsavilkuma cilnē **Grāmatošana** ietilpst sadaļas **Debets** un **Kredīts**. Atkarībā no Virsgrāmatas, kurā vēlaties grāmatot maksas, iestatiet šādus laukus:

    - **Veids** — atlasiet konta veidu, kurā grāmatojat (*Virsgrāmata*, *Debitors* vai *Krājums*).
    - **Grāmatošana** — atlasiet veidojamo grāmatojumu veidu (piemēram, *Starpnieka maksa* vai *Debitora norēķini*).
    - **Konts** — atlasiet kontu, kurā grāmatot maksu.

1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="create-charge-groups"></a>Maksu grupu izveide

Maksu grupas automātiski piešķir noteiktas maksas debitoru vai kreditoru grupai. Šajās apakšsadaļās ir aprakstīts, kā izveidot un piešķirt šīs maksu grupas.

### <a name="charge-groups-for-purchase-orders"></a>Pirkšanas pasūtījumu maksu grupas

Lai izveidotu maksu grupas pirkšanas pasūtījumiem, veiciet tālāk norādītās darbības.

1. Doties uz **Kreditori \> Maksu iestatīšana \> Kreditoru maksu grupa**.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un pēc tam atlasiet šos laukus:

    - **Maksu grupa** — ievadiet maksu grupas nosaukumu.
    - **Apraksts** — ievadiet maksu grupas aprakstu.

1. Darbību rūtī atlasiet **Saglabāt**.
1. Dodieties uz **Kreditori \> Kreditori \> Visi kreditori** un vai nu atveriet esošu kreditoru, vai izveidojiet jaunu kreditoru.
1. Kopsavilkuma cilnes sadaļā **Pirkšanas pasūtījums** **Pirkšanas pasūtījuma noklusējums** iestatiet lauku **Maksu grupa** uz tikko izveidoto maksu grupu.

### <a name="charge-groups-for-sales-orders"></a>Pārdošanas pasūtījumu maksu grupas

Lai izveidotu maksu grupas pārdošanas pasūtījumiem, veiciet tālāk norādītās darbības.

1. Dodieties uz **Debitori \> Maksu iestatīšana \> Debitora maksu grupas**.
1. Darbību rūtī atlasiet **Jauns**, lai pievienotu rindu režģim, un pēc tam atlasiet šos laukus:

    - **Maksu grupa** — ievadiet maksu grupas nosaukumu.
    - **Apraksts** — ievadiet maksu grupas aprakstu.

1. Darbību rūtī atlasiet **Saglabāt**.
1. Dodieties uz **Debitori \> Debitori \> Visi debitori** un vai nu atveriet esošu debitoru, vai izveidojiet jaunu debitoru.
1. Kopsavilkuma cilnes sadaļā **Pārdošanas pasūtījums** **Pirkšanas pasūtījuma noklusējums** iestatiet lauku **Maksu grupa** uz tikko izveidoto maksu grupu.

## <a name="define-auto-charges"></a>Automātisko maksu definēšana

Pēc maksu kodu iestatīšanas veiciet tālāk norādītās darbības, lai definētu automātiskās maksas.

1. Izpildiet kādu no šīm darbībām:

    - Pirkšanas pasūtījumiem: dodieties uz **Sagāde un avoti \> Iestatījumi \> Maksas \> Automātiskās maksas**.
    - Pārdošanas pasūtījumiem: dodieties uz **Debitori \> Setup \> Maksu iestatīšana \> Automātiskās maksas**.

1. Saraksta rūtī laukā **Līmenis** atlasiet līmeni, uz kuru attiecas jūsu automātiskā maksa.

    - *Galvenais* — piemēro maksas pasūtījuma galvenei.
    - *Rinda* — piemēro maksas pasūtījuma rindām.

1. Atlasiet esošu automātisko maksu, lai to rediģētu, vai atlasiet **Jauns**, lai definētu jaunu automātisko maksu.
1. Sarakstā **Konta kods** atlasiet vienu no tālāk norādītajām vērtībām, lai norādītu to kontu tvērumu, kas tiks ietekmēti.

    - *Tabula* — piešķirt maksas noteiktam debitoram vai kreditoram.
    - *Grupa* — piešķirt maksas papildmaksu grupai.
    - *Viss* – piešķirt maksas visiem debitoriem vai kreditoriem.

1. Laukā **Debitoru saistība** vai **Kreditoru saistība** atlasiet konkrētu debitoru vai kreditoru, ja iestatījāt lauku **Konta kods** uz *Tabula*. Ja lauku **Konta kods** iestatījāt uz *Grupa*, atlasiet debitora vai kreditora maksu grupu.
1. Laukā **Krājuma kods** atlasiet vienu no tālāk norādītajām vērtībām, lai norādītu to krājumu tvērumu, kas tiks ietekmēti. Krājuma kodu var atlasīt tikai tad, kad definējat automātiskās maksas rindas līmenī.

    - *Tabula* — piešķiriet maksas noteiktam krājumam.
    - *Grupa* — piešķirt maksas krājuma maksu grupai.
    - *Viss* — piešķiriet maksas visiem krājumiem.

1. Laukā **Krājumu saistība** atlasiet konkrētu krājumu, ja iestatāt lauku **Krājuma kods** uz *Tabula*. Ja iestatāt lauku **Krājuma kods** uz *Grupa*, atlasiet krājuma maksu grupu.
1. **Tikai pārdošanas pasūtījumiem:** laukā **Piegādes koda veids** atlasiet vienu no tālāk norādītajām vērtībām, lai noteiktu piegādes režīmu diapazonu, kas tiks ietekmēts.

    - *Tabula* — piešķirt maksas noteiktam piegādes veidam.
    - *Grupa* — piešķirt maksas piegādes grupas veidam.
    - *Viss* — piešķirt maksas visiem piegādes veidiem.

1. **Tikai pārdošanas pasūtījumiem:** laukā **Piegādes veida relācija** atlasiet konkrētu piegādes veidu, ja iestatāt lauku **Piegādes veida kods** uz *Tabula*. Ja iestatāt lauku **Piegādes veida kods** uz *Grupa*, atlasiet piegādes veida grupu.
1. Kopsavilkuma cilnē **Rindas** definējiet maksas un maksu likmes, kas tiks izmantotas, piemērojot pašreizējo automātisko maksu. Varat izmantot rīkjoslu šajā kopsavilkuma cilnē, lai pievienotu tik daudz rindu, cik nepieciešams. Katrai rindai iestatiet šādus laukus:

    - **Valūta** — atlasiet valūtu, kas jāizmanto maksas aprēķināšanai.
    - **Maksu kodu** — atlasiet maksas kodu.
    - **Kategorija** — atlasiet vienu no šīm vērtībām:

        - *Fiksēta* — maksa tiek ievadīta kā fiksēta summa rindā. Fiksētās maksas var izmantot maksām gan pasūtījuma galvenē, gan pasūtījuma rindās.
        - *Gabali* — maksa, pamatojoties uz vienību. Šīs maksas var izmantot tikai pasūtījuma rindās. Tās parādīsies, kad tiks aprēķināta pasūtījuma kopsumma.
        - *Procenti* — maksa tiek ievadīta kā procentuāls lielums rindā. Procentu maksas var izmantot maksām gan pasūtījuma galvenē, gan pasūtījuma rindās.
        - *Starpuzņēmumu procenti* — maksa tiek ievadīta kā procenti starpuzņēmumu pasūtījumu rindā. Starpuzņēmumu procentu maksas var izmantot tikai pasūtījuma rindās.
        - *Ārēja* — maksa tiek aprēķināta, izmantojot trešās puses pakalpojumu, kas ir saistīts ar vienu vai vairākiem nosūtījuma pārvadātājiem.

    - **Maksu vērtība** — ievadiet maksas vērtību, pamatojoties uz atlasīto kategoriju.
    - **Maksu valūtas kods** — norādiet maksas valūtu, ja vēlaties izmantot citu valūtu, nevis valūtu, ko norādījāt laukā **Valūta**. Citu valūtu ir iespējams izmantot tikai tad, ja lauks **Debeta veids** vai **Kredīta veids** atlasītajam maksu kodam ir iestatīts uz *Virsgrāmatas konts* vai *Krājums*.
    - **No summas** — norādiet sākuma summu, lai piemērotu automātisku maksu. Šajā kontekstā summa attiecas uz pasūtījuma kopsummu.
    - **Līdz summai** — norādiet beigu summu, lai piemērotu automātisku maksu. Šajā kontekstā summa attiecas uz pasūtījuma kopsummu.
    - **PVN grupa** — norādiet PVN grupu.
    - **Vieta** un **Noliktava** — norādiet vietu un noliktavu, ja maksas jāpiemēro tikai konkrētai vietai un noliktavai.
    - **Saglabāt** — atlasiet šo izvēles rūtiņu , lai saglabātu maksu transakcijas pēc rēķina izrakstīšanas, tā, ka maksa tiks lietota ik reizi, kad veidosiet jaunu rēķinu atlasītajam debitora kontam.

1. **Tikai pārdošanas pasūtījumiem:** ja vēlaties aprēķināt diferencētās izmaksas, papildinformāciju skatiet sadaļā [Pārdošanas pasūtījumu diferencētās maksas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders).

## <a name="allocate-charges-from-the-header-to-a-line"></a>Piešķirt maksas no galvenes uz rindu

Procedūrā zemāk ir parādīts, kā piešķirt galvenes līmeņa maksas rindai. Pirms sākat šo procedūru, jums jau ir jābūt *fiksētas summas* veida galvenes līmeņa maksai un pasūtījumam, kur šī maksa tiek piemērota. Turklāt pasūtījumā jau ir jābūt vismaz vienam rindas krājumam.

1. Atveriet pirkšanas pasūtījumu vai maksas pasūtījumu.
1. Darbību rūtī veiciet vienu no šīm darbībām:

    - Pirkšanas pasūtījumiem: cilnē **Pirkšana**, kas atrodas grupā **Maksas**, atlasiet **Piešķirt maksas**.
    - Pārdošanas pasūtījumiem: cilnē **Pārdošana**, kas atrodas grupā **Maksas**, atlasiet **Piešķirt maksas**.

1. Dialoglodziņā **Piešķirt maksas pasūtījuma rindām** iestatiet tālāk norādītos laukus.

    - **Maksu sadalījums** — atlasiet vienu no šīm vērtībām, lai norādītu, kā maksas jāpiešķir.

        - *Neto summa* — sadalīt izmaksas atbilstoši katrai rindas summai attiecībā pret kopējo neto summu.
        - *Daudzums* — sadalīt maksas atbilstoši katras rindas vienību skaitam attiecībā pret kopējo vienību skaitu.
        - *Rindai* — maksas tiek sadalītas vienādi starp rindu kopskaitu.

    - **Piešķirt maksas rindām** — atlasiet vērtību, lai norādītu, vai maksas jāpiešķir visām rindām, tikai pozitīvām rindām vai tikai negatīvām rindām.
    - **Piešķirt visu** — atlasiet šo izvēles rūtiņu, lai sadalītu maksas pirkšanas pasūtījuma rindām, pat ja papildmaksas koda debets nav *Krājums*.
    - **Saņemts** – atlasiet šo izvēles rūtiņu, lai sadalītu maksas tikai saņemtajām pasūtījuma rindām.
    - **Uzkrāts** – atlasiet šo izvēles rūtiņu, lai sadalītu maksas tikai inventarizētajām pasūtījuma rindām.
    - **Rādīt atlases un noņemt noteiktas rindas** — atlasiet šo izvēles rūtiņu, lai no šī sadalījuma izslēgtu noteiktas rindas. Atlasot šo izvēles rūtiņu, tiek atvērts režģis **Izvēlēties rindas, lai izslēgtu no sadalījuma**. Šajā režģī tiek iekļautas tikai tās rindas, kas atbilst kritērijiem, kas ir definēti iestatījumos **Piešķirt maksas rindām** un **Uzkrāts**. Piemēram, ja iestatāt lauku **Piešķirt maksas rindām** uz *Pozitīvās rindas* un atlasāt izvēles rūtiņu **Uzkrāts**, režģī tiek rādītas tikai tās rindas, kuras ir pozitīvas un inventarizētas. Turklāt režģis automātiski filtrē visas rindas, kurām jau ir saņemts pilns daudzums. Kamēr režģis ir atvērts, izņemiet atzīmi no izvēles rūtiņas **Iekļaut** katrai rindai, kas jāizslēdz no sadalījuma. 

        > [!IMPORTANT]
        > Strādājot ar režģi **Izvēlēties rindas, ko izslēgt no sadalījuma**, noteikti atstājiet režģi atvērtu, līdz atlasāt **Piešķirt**. Ja aizvērsit režģi, pirms atlasāt **Piešķirt**, iestatījumi režģī tiks zaudēti. Tāpēc maksas tiks piešķirtas, pamatojoties uz iepriekš definētajiem kritērijiem.

1. Atlasiet **Piešķirt**, lai iestatījumus piemērotu un aizvērtu dialoglodziņu.
