---
title: Pārtraukt norēķinu grafikus
description: Šajā tēmā skaidrots, kā pārtraukt norēķinu grafikus un norēķinu grafika rindas abonementa norēķinos.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: df81cc888e893c6a4a127e1a43426a0a0b56f0d1
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470831"
---
# <a name="terminate-billing-schedules"></a>Pārtraukt norēķinu grafikus

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā pārtraukt norēķinu grafikus un norēķinu grafika rindas abonementa norēķinos. Kad pārtraucat norēķinu grafiku, tam jābūt ar statusu **Aktīvs**. Tā statuss nevar būt **Aizturēts**. Tāpat, kad beidzat norēķinu grafika rindu, tai jābūt **aktīvai**. Norēķinu grafika virsraksta sadaļa netiek ietekmēta, ja pārtraucat norēķinu grafika rindu.

Lai pārtrauktu norēķinu grafiku vai norēķinu grafika rindu, dodieties uz vienu no šīm vietām:

- Visu **/aktīvo norēķinu grafiku** saraksta lapa
- Noteikts norēķinu grafiks lapā **Visi norēķinu** grafiki
- Noteikta norēķinu grafika rinda visu **norēķinu grafiku** lapā

> [!NOTE]
> Ja vēlaties pārtraukt vairākas norēķinu grafika vienlaicīgi, izmantojiet lapu Masveida darba **attiecību pārtraukšana.**

## <a name="terminate-a-billing-schedule-or-line"></a>Pārtraukt norēķinu grafiku vai rindu

Lai pārtrauktu norēķinu grafiku vai norēķinu grafika rindu, sekojiet šiem soļiem.

1. Atlasiet norēķinu grafiku vai norēķinu grafika rindu un pēc tam atlasiet **Pārtraukt**. 
2. Iestatiet atbrīvošanas **datuma**, **atbrīvošanas tipa** un iemesla **koda laukus**.
3. Laukā Kredīta **opcija iestatiet** vērtību Izdot **kredītu**.
4. Izvēlieties **Pārtraukt darba attiecības**.

Norēķinu grafika statuss mainās, pamatojoties uz atlasīto darba attiecību pārtraukšanas tipu. Ja kā darba **attiecību pārtraukšanas** veidu atlasījāt Atlikuma rēķinu, visu norēķinu grafika rindu statuss ir Pēdējie **norēķini**. Norēķinu grafika statuss paliek aktīvs **,** līdz tiek apstrādāts pēdējais rēķins. Kad pēdējais rēķins ir apstrādāts, statuss tiek atjaunināts uz **Izbeigts**. Ja kā darba attiecību pārtraukšanas **tipu atlasījāt Pielāgot grafiku, norēķinu grafika statuss nekavējoties tiek atjaunināts uz Pārtraukts** **.**

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Pārtraukt norēķinu grafiku vai rindu un piemērot atmaksu

Lai pārtrauktu norēķinu grafiku vai norēķinu grafika rindu un lietotu atmaksu, sekojiet šiem soļiem.

1. Atlasiet norēķinu grafiku vai norēķinu grafika rindu un pēc tam atlasiet **Pārtraukt**.
2. Iestatiet laukus **Atbrīvošanas** datums, **Darba** attiecību pārtraukšanas **tips**, Iemesla kods **un Kredīta** opcija.
3. Atlasiet Pārtraukt **ar atmaksu**. Tiek **parādīta masveida darba attiecību** pārtraukšanas apstrādes lapa, kas tiek filtrēta, lai tajā būtu parādīts norēķinu grafiks.
4. Atlasiet **Skatīt priekšskatījumu**, lai skatītu norēķinu grafiku rindas, un pēc tam atlasiet **Apstrādāt**.

Pēc kredīta apstrādes atveriet lapu Skatīt **norēķinu detalizētu informāciju**, lai pārskatītu kredītu, kas tika piemērots norēķinu grafikam. Ja kredīta summa ir lielāka par 0 (nulli), visas turpmākās nenodzēstās rindas tiek dzēstas un aizstātas ar norēķinu informācijas rindām, kas parāda negatīvās kredīta summas, kas tika piemērotas norēķinu grafikam.

### <a name="view-example"></a>Skatīt piemēru

Norēķinu grafikā ir šāda informācija:

- Sākuma datums ir 2020. gada 1. janvāris.
- Beigu datums ir 2020. gada 31. decembris.
- Norēķinu perioda summa ir 100,00 mēnesī.
- Rēķini ir izveidoti norēķinu periodiem no janvāra līdz jūlijam.
- Līguma izbeigšanas datums ir 2020. gada 15. jūnijs.

Kad kredīta korekcija ir apstrādāta, visi turpmāko norēķinu periodi (no augusta līdz decembrim) tiek noņemti no lapas **Skatīt norēķinu detaļu**. Kredīta korekcijas rinda tiek pievienota pēc jūlija norēķinu perioda:

- 16. jūnijs – 31. jūlijs, ar kredīta summu 150,00

Ja tiek izmantota funkcija Nenobīdētie ieņēmumi, **tad nenobīdāmo ieņēmumu žurnāla ieraksta audita** lapa tiek atjaunināta ar darba attiecību pārtraukšanas ierakstu.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Pārtraukt norēķinu grafiku vai rindu, nelietojot kredītu

Lai pārtrauktu norēķinu grafiku vai norēķinu grafika rindu, nepiemērojot kredītu, sekojiet šiem soļiem.

1. Atlasiet norēķinu grafiku vai norēķinu grafika rindu un pēc tam atlasiet **Pārtraukt**.
2. Iestatiet lauku **Atbrīvošanas** datums.
3. Lauku Atbrīvošanas **tips** iestatiet uz Nav **korekcijas**. Lauks **Kredīta opcija** automātiski tiek iestatīts uz Nav **kredīta**.
3. Iestatiet lauku **Iemesla** kods.
4. Laukā **Darba attiecību pārtraukšanas** piezīmes ievadiet visas nepieciešamās piezīmes.
5. Izvēlieties **Pārtraukt darba attiecības**. 

Pēc darba attiecību pārtraukšanas apstrādes visas norēķinu informācijas rindas pēc atbrīvošanas datuma tiek noņemtas. (Šajās rindās ir iekļauta darba attiecību pārtraukšanas datums.) Nevar izveidot rēķinus rindām, ar ko pārtrauktas darba attiecības. Ja darba attiecību pārtraukšana tiek noņemta, visas pārtrauktās rindas tiek pievienotas **atpakaļ lapai Skatīt norēķinu informāciju** un kļūst pieejamas iekļaušanai rēķinā.

## <a name="fields"></a>Lauki

Lapā **Skatīt norēķinu detalizētu informāciju** ir ietverti tālāk šie lauki.

| Lauks | Apraksts |
|-------|-------------| 
| Atbrīvošanas datums | Atlasiet datumu, kad vēlaties pārtraukt norēķinu grafiku vai norēķinu grafika rindu. |
| Izbeigšanas veids | <p>Atlasiet atbrīvošanas tipu:</p><ul><li>**Pielāgot grafiku** . Nogrieziet norēķinu periodus rindai darba attiecību pārtraukšanas datumā un mainiet rindas statusu uz Pēdējie **norēķini**. Ja rindas krājumam pastāv atlikto maksājumu grafiks, tas tiek koriģēts, atceļot summu, kuru vairs nav jāatpazīst. Ja norēķinu sākuma datums ir pēc atbrīvošanas datuma, pārējie norēķinu periodi tiek noņemti.</li><li>**Atlikušais** vekseļu rēķins - pievienojiet atlikušo summu norēķinu periodam darba attiecību pārtraukšanas periodam un mainiet rindas statusu uz Pēdējie **norēķini**. Ja rindas krājumam pastāv atlikto maksājumu grafiks, atliktā maksājuma beigu datums tiek atjaunināts. Ja norēķinu sākuma datums ir pēc atbrīvošanas datuma, visu atlikušo norēķinu periodu kopējā summa tiek pievienota norēķinu periodam, un atlikušie norēķinu periodi tiek noņemti.</li><li>**Nav** korekciju - pārtrauciet norēķinu periodus rindai norādītajā darba attiecību pārtraukšanas datumā. Korekcijas nav veiktas. Ja ir atlasīts šis atbrīvošanas tips, **opcijas Kredīts lauks** **ir** iestatīts uz Nav kredīta un **lauks Ikdienas prorate** ir iestatīts uz **Nē.** Abi šie lauki pēc tam kļūst tikai lasāmi, un tos nevar mainīt.</li></ul> |
| Kredīta opcija | <p>Izvēlieties, kā kredīts tiek lietots, kad beidzat norēķinu grafika rindu:</p><ul><li>**Kredīta korekcija** - izveidojiet kredīta korekciju norēķinu grafikam, ja rinda ir izbeigta. Kredīta korekcija tiek parādīta norēķinu grafika nākamajā norēķinu periodā. Pārrēķins arī automātiski koriģē rēķina summu nākamajam norēķinu periodam, līdz kredīts ir pabeigts norēķinu grafikam.</li><li>**Izsniegt kredītu** - izveidojiet kredīta notu, kad tiek pārtraukts norēķinu grafiks vai norēķinu grafika rinda.</li><li>**Nav kredīta** - neveidojiet kredīta korekciju vai kredīta notu, ja tiek pārtraukts norēķinu grafiks vai norēķinu grafika rinda. Šī opcija ir pieejama tikai tad, ja izmantojat bez korekcijas veida **darba** attiecību pārtraukšanu, lai pārtrauktu norēķinu grafiku.</li></ul><p>Noklusējuma opcija ir no periodisko **līgumu norēķinu parametru** lapas.</p> |
| Iemeslu kodi | Atlasiet atbrīvošanas iemesla kodu. |
| Iemesla apraksts | Pamatojuma koda apraksts. |
| Izbeigšanas piezīmes | Ievadiet visas piezīmes par darba attiecību pārtraukšanu. |

<!--## Additional information-->
