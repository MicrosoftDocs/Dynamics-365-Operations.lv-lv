---
title: Atlikto maksājumu darbības abonementa norēķinos
description: Šajā tēmā aprakstītas dažādas darbības, ko var izmantot atlikto maksājumu darbībām kā daļa no ieņēmumiem un izdevumu atliktajiem rēķiniem abonementa norēķinos.
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
ms.openlocfilehash: f66c538afc732caf3faed3cfea6c695ff7f16273
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557977"
---
# <a name="deferral-default-transactions"></a>Atlikto maksājumu noklusējuma darbības

Šajā tēmā aprakstītas darbības, kas ļauj veikt ieņēmumu un izdevumu atliktos maksājumus. Atlikto maksājumu grafiki vienmēr tiek balstīti uz un ir atkarīgi no sākotnējā dokumenta vai rēķina grafika. Atlikto maksājumu grafiki tiek izveidoti pēc noklusējuma, un tos nevar ievadīt vai izveidot atsevišķi.

## <a name="sales-order-transaction-deferral"></a>Pārdošanas pasūtījuma transakciju atliktie ieņēmumi

Izmantojiet lapu **Atliktie rēķini** **vai Izveidot kredīta notu**, lai ievadītu vai labotu pārdošanas pasūtījuma rindas atlikto maksājumu parametrus.

> [!NOTE]
> Kad pārdošanas pasūtījums ir izveidots no norēķinu grafika, **visas vērtības lapā Atliktie norēķini vai Izveidot kredīta notu ir tikai lasāmas, un atlikto maksājumu parametrus** **nevar** rediģēt. Lai rediģētu vērtības, izmantojiet lapu **Modificēt** grafiku.

### <a name="edit-deferral-options"></a>Rediģēt atlikto maksājumu opcijas

Lai rediģētu atlikto maksājumu opcijas rindai, sekojiet šiem soļiem.

1. Izveidojiet pārdošanas pasūtījuma darbību.
2. Atlasiet rindu un pēc tam atlasiet Atliktie **maksājumus**.
3. Lapā Transakciju **atlikto maksājumu** opcijai **jābūt** iestatītai uz **Jā**. Pēc pieprasāmo lauku labošana.
4. Lai priekšskatītu atlikto maksājumu grafiku, atlasiet **Priekšskatīt**.
5. Ja jūs veicāt izmaiņas darbības atliktais maksājumam, izvēlieties **Labi**, un atgriezieties darbības lapā.
6. Iesniegt un grāmatot darbību.

Pēc darbības grāmatošanas atveriet lapu Visi atlikto **maksājumu grafiki,** lai skatītu atlikto maksājumu grafiku.

### <a name="create-a-credit-note"></a>Izveidot kredīta notu

Lai izveidotu kredīta notu, veiciet tālāk aprakstītās darbības.

1. Izveidojiet pārdošanas pasūtījuma darbību.
2. **Sadaļā Pārdošanas pasūtījuma rindas** atlasiet krājumu, kuram vēlaties izveidot kredīta notu.
3. Atlasiet **pārdošanas pasūtījuma rindu Jauns** \> **un** pēc tam atlasiet Kredīta **nota.**
4. Atlasiet **atliktos maksājumus**.
5. Lapā Pārdošanas **pasūtījuma transakciju atliktais rēķins** iestatiet krājumam **opciju** Pielāgot **esošo** grafiku uz Jā.
6. Laukā **Pielāgots** grafiks atlasiet atlikto maksājumu grafiku, kuram vēlaties piemērot kredīta notu.
7. Pēc izdošanas **atjauniniet laukus** **Pārrēķināt** datumu un beigu datumus.
8. Atlasiet **Labi**.
9. Pabeidziet pārdošanas pasūtījuma darbības grāmatošanu.

### <a name="purchase-orders-and-purchase-invoices"></a>Pirkšanas pasūtījumi un pirkšanas rēķini

Ja pirkšanas pasūtījumam vēlaties izmantot atlikto maksājumu funkcionalitāti, vispirms ģenerējiet rēķinu. Pēc tam izmantojiet lapu Neizlemti **kreditora rēķini**, lai rediģētu vai pievienotu atlikto maksājumu krājumus. Atliktos maksājumus nevar labot vai pievienot tieši pirkšanas pasūtījumam.

1. Izmantojiet lapu **Neizlemti kreditora rēķini**, lai ievadītu kreditora rēķinu.

    Kad ievadāt rindu, atliktais pasūtījums tiek automātiski iestatīts jūsu atlasa krājumam vai sagādes kategorijai. Šis atliktais maksājuma pamatā ir atlikto maksājumu iestatījumi atlikto **maksājumu noklusējumu** lapā. Atliktos maksājumus var labot vai pievienot sadales līmenī.

3. Pirkšanas rindā atlasiet Finanšu **sadales \> summas**.
4. Katrai sadales summai atlasiet Atliktos **maksājumus**. Kad rēķins ir iegrāmatots, atlikto maksājumu grafiks tiek izveidots katrai sadalei, kam ir iestatīts atliktais maksājuma mērķis.

### <a name="tax"></a>Nodokļi

Dažkārt nodokļa summa var būt pilnībā vai daļēji neatkopjama. Ja atliktā maksājuma rindas nodokļa summā ir atgūstamā summa, neatgūstamā nodokļa summa tiek iekļauta atliktā maksājuma grafika summā, kad rēķins tiek grāmatots.

### <a name="variance"></a>Novirze

Ja summa kreditora rēķina rindā atšķiras no summas pirkšanas pasūtījuma rindā, tiek izveidotas novirzes sadales. Ja rinda ir atlikta, virsgrāmatas konts šīm sadalēm tiek iestatīts uz atlikto maksājumu kontu, un summas tiek iekļautas atliktā maksājuma grafika summā, kad rēķins tiek grāmatots. Šīs sadales sauc "Cenas **novirze" un** " **Izmaksu novirze"**.

### <a name="general-journals-and-invoice-journals"></a>Virsgrāmatas žurnāli un rēķinu žurnāli

Izmantojiet atlikto **maksājumu lapu**, lai ievadītu atlikto maksājumu parametrus žurnāla dokumenta rindai. Var arī priekšskatīt atlikto maksājumu grafiku lineāro atlikto maksājumu. Kad ievadāt rindu, atliktais maksājuma konts tiek iestatīts automātiski, pamatojoties uz atlikto maksājumu kontu iestatījumiem atlikto **maksājumu noklusējuma lapā**. Katrai rindai atlikto maksājumu opcijas var mainīt manuāli. Kad žurnāla dokuments tiek iegrāmatots, tiek izveidots atlikto maksājumu grafiks.

#### <a name="post-and-transfer"></a>Grāmatot un pārsūtīt

Lai grāmatotu žurnāla dokumentu, izmantojiet komandu **Grāmatot un pārsūtīt**. Atlikto maksājumu opcijas sekos rindai, uz kuru attiecas dokuments. Dokumentiem, kuros nav kļūdu, tiek izveidots atlikto maksājumu grafiks, ja tas tiek atlikts. Dokumentam, kurā ir kļūda un tas tiek pārsūtīts, tam tiek pārsūtītas arī visas atlikto maksājumu opcijas.

#### <a name="tax"></a>Nodokļi

Dažkārt nodokļa summa var būt pilnībā vai daļēji neatkopjama. Ja atliktā maksājuma rindas nodokļa summā ir atgūstamā summa, neatgūstamā nodokļa summa tiek iekļauta atliktā maksājuma grafika summā, kad rēķins tiek grāmatots.

## <a name="free-text-invoice-transaction-deferral"></a>Brīva teksta rēķina darbības atliktais maksājuma

Izmantojiet atlikto **maksājumu lapu**, lai ievadītu atlikto maksājumu parametrus brīvā teksta rēķina rindas sadalei. Kad tiek ievadīta sadale, atliktais maksājuma automātiski tiek iestatīts, pamatojoties uz atliktā maksājuma iestatījumiem atlikto **maksājumu noklusējuma** lapā.

## <a name="fields"></a>Lauki

Lapā **Transakciju atlikto** maksājumu lapa satur šādus laukus.

| Lauks | Apraksts |
|-------|-------------|
| Atlikts | <p>Norādiet, vai rinda ir atliktais maksājumam:</p><ul><li>**Jā** – rinda ir atliktais maksājumam.</li><li>**Nē** — rinda nav atliktais maksājumam.</li></ul><p>Ja ir iestatīta opcija **Jā**, opcija **Pielāgot esošo** grafiku nav pieejama. Krājumiem un maksām, kas jau ir iestatīti kā atlikti, šī opcija tiek iestatīta uz **Jā**. Krājumiem un maksām, kas nav iestatīti kā atlikti pēc noklusējuma, iestatiet šo opciju uz **Jā**.</p> |
| Pielāgot esošo grafiku | <p>Norādiet, vai rinda ir esoša atlikto maksājumu grafika korekcija:</p><ul><li>**Jā** – jaunā pārdošanas rinda ir esoša atlikto maksājumu grafika korekcija. Šajā gadījumā var atlasīt atlikto maksājumu grafiku laukā Pielāgots **grafiks**.</li><li>**Nē** — jaunā pārdošanas rinda nav esoša atlikto maksājumu grafika korekcija.</li></ul><p>Ja šī opcija ir iestatīta uz **Jā**, **opcija** Atliktais maksājumu nav pieejama.</p> |
| Pielāgots grafiks | <p>Atlasiet atlikto maksājumu grafiku, kuru koriģē rinda. Pēc tam visas lapas vērtības tiek atjauninātas ar sākotnējās atlikto maksājumu grafika vērtībām. Šīs vērtības nevar rediģēt.</p><p>Šis lauks ir pieejams tikai tad, ja opcija **Pielāgot esošo** grafiku ir iestatīta uz **Jā**.</p> |
| Pārrēķina datums | <p>Norādiet perioda, no kura vēlaties pārrēķināt atlikušo summu, sākuma datumu. Noklusējuma datums ir nākamā neatpazīta perioda datums.</p><p>Šis lauks ir pieejams tikai tad, ja opcija **Pielāgot esošo** grafiku ir iestatīta uz **Jā**.</p> |
| Beigu datums | <p>Atkarībā no atliktā maksājuma tipa, beigu datumu var vai nevar atjaunināt:</p><ul><li>Lineārā atliktā maksājumam norādiet jauno grafika beigu datumu. Atlikto maksājumu grafika esošais beigu datums ir noklusējuma vērtība.</li><li>Atliktā maksājumam, kas ir atkarīgs no notikuma, norādiet kredīta notikuma rindas beigu datumu. Šis datums var būt tukšs.</li></ul><p>Šis lauks ir pieejams tikai tad, ja opcija **Pielāgot esošo** grafiku ir iestatīta uz **Jā**.</p> |
| Norēķinu grafika numurs | <p>Norēķinu grafika numurs.</p><p>Šis lauks ir pieejams tikai periodiskiem līguma norēķinu grafikiem.</p> |
| Atlikšanas korekcijas metode | <p>Atliktā maksājuma korekcijas metode. Šī vērtība sakrīt ar periodiskā **līguma norēķinu** grafika lapas masveida darba attiecību pārtraukšanas apstrādes vērtību.</p><p>Šis lauks ir pieejams tikai periodiskiem līguma norēķinu grafikiem.</p> |
| **Konti - Ieņēmumi** | |
| Atlikto maksājumu konts | <p>Atlikto maksājumu konts, kas ir pārdošanas pasūtījuma lapā redzamais **grāmatošanas** konts.</p><p>Ja rinda nav atlikta, šis lauks ir tukšs. Šajā gadījumā grāmatošanas konts ir ieņēmumu noklusējuma konts.</p> |
| Atzīšanas konts | <p>Norādiet kontu, kas tiek izmantots, kad atliktais konts tiek atpazīts. Šim kontam ir jāatšķiras no atlikto maksājumu konta.</p><p>Kad atliktā **maksājuma** opcija sākotnēji tiek iestatīta **uz Jā**, dimensiju vērtības, kas tiek izmantotas atlikto maksājumu kontā, tiek kopētas atpazīšanas kontā. Ja atlikto maksājumu kontā nav dimensijas atpazīšanas kontam, tā tiek ignorēta.</p> |
| Sākotnējās atzīšanas konts | <p>Atlasiet kontu sākotnējai ieņēmumu atzīšanai. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams tikai tad **, ja atlikto maksājumu** **·** **grāmatošanas metodes lauks lapā Ieņēmumu un izdevumu atlikto maksājumu parametri ir iestatīts uz Peļņa un** zaudējumi.</p> |
| Atzīšanas korespondējošais konts | <p>Atlasiet kontu korespondējošai ieņēmumu atzīšanai. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams tikai tad **, ja atlikto maksājumu** **·** **grāmatošanas metodes lauks lapā Ieņēmumu un izdevumu atlikto maksājumu parametri ir iestatīts uz Peļņa un** zaudējumi.</p> |
| **Konti - Atlaide** | Šī sadaļa tiek parādīta tikai atliktiem krājumiem. Atlikto maksājumu segšanai tas ir slēpts. |
| Atlikto maksājumu konts | <p>Norādiet atlaides atlikto maksājumu konta numuru. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams **tikai** **·** **tad, ja atlaides atliktā maksājuma opcijas lauks ir iestatīts uz Atsevišķs grafiks atlaidei lapā Ieņēmumu un izdevumu atlikto maksājumu parametri**, un atlaide tiek piemērota rindai.</p> |
| Atzīšanas konts | <p>Norādiet atlaides atzīšanas konta numuru. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams **tikai** **·** **tad, ja atlaides atliktā maksājuma opcijas lauks ir iestatīts uz Atsevišķs grafiks atlaidei lapā Ieņēmumu un izdevumu atlikto maksājumu parametri**, un atlaide tiek piemērota rindai.</p> |
| Sākotnējās atzīšanas konts | <p>Atlasiet kontu sākotnējās atlaides atpazīšanai. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams **tikai** **·** **tad, ja lauka Atlikto maksājumu grāmatošanas metode iestatījums** ir Peļņa un zaudējumi lapā Ieņēmumu un izdevumu atlikto maksājumu parametri, un rindai tiek piemērota atlaide.</p> |
| Atzīšanas korespondējošais konts | <p>Atlasiet kontu korespondējošai ieņēmumu atzīšanai. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams **tikai** **·** **tad, ja lauka Atlikto maksājumu grāmatošanas metode iestatījums** ir Peļņa un zaudējumi lapā Ieņēmumu un izdevumu atlikto maksājumu parametri, un rindai tiek piemērota atlaide.</p> |
| **Konti - Patēriņš** | Šī sadaļa tiek parādīta tikai atliktiem krājumiem. Atlikto maksājumu segšanai tas ir slēpts. |
| Atlikto maksājumu konts | <p>Norādiet patēriņa atlikto maksājumu konta numuru.</p><p>Standarta precēm tiek izveidoti divi atlikto maksājumu grafiki:</p><ul><li>**Standarta pārdošana** – ieņēmumu grafiks, kam ir kredīta bilance. Šajā gadījumā atlasiet patēriņa atlikto maksājumu kontu.</li><li>**Patēriņš** – patēriņa (pārdoto preču pašizmaksas \[PPPI\]) izdevumu grafiks, kam ir debeta bilance. Šajā gadījumā atlasiet patēriņa atzīšanas kontu.</li></ul><p>Kad rēķins ir iegrāmatots, patēriņa summa tiek grāmatota norādītajā patēriņa atliktā maksājuma kontā. Šie lauki nav pieejami pakalpojumu krājumiem.</p> |
| Atzīšanas konts | Norādiet patēriņa atzīšanas konta numuru. |
| Sākotnējās atzīšanas konts | <p>Norādiet kontu sākotnējai patēriņa atzīšanas summai. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams tikai tad **, ja atlikto maksājumu** **·** **grāmatošanas metodes lauks lapā Ieņēmumu un izdevumu atlikto maksājumu parametri ir iestatīts uz Peļņa un** zaudējumi.</p> |
| Atzīšanas korespondējošais konts | <p>Norādiet kontu patēriņa atzīšanas korespondējošai summai. Noklusētā vērtība ir no atlikto maksājumu **noklusējumu** lapas.</p><p>Šis lauks ir pieejams tikai tad **, ja atlikto maksājumu** **·** **grāmatošanas metodes lauks lapā Ieņēmumu un izdevumu atlikto maksājumu parametri ir iestatīts uz Peļņa un** zaudējumi.</p> |
| **Ieplānot** | |
| Grafika veids | <p>Atlasiet atliktā maksājuma grafika tipu: lineārā **·**(noklusējums) vai **atbilstoši notikumam**.</p><p>Lapā parādītās opcijas ir balstītas uz jūsu izvēlēto atlikto maksājumu grafika tipu.</p><p>Ja noklusējuma veidne ir iestatīta atlikto **maksājumu noklusējumu lapā darbības rindai, atlikto maksājumu grafika tips tiek pamatots uz atlasītās** veidnes tipu.</p> |
| **Grafiks - lineārā** | |
| Konsolidēt iepriekšējos periodus | <p>Norādiet, vai vēlaties konsolidēt atlikto maksājumu grafika rindas agrākiem periodiem:</p><ul><li>**Jā** – konsolidēt atlikto maksājumu grafika rindas par agrākiem periodiem.</li><li>**Nē** - nekonsolidējiet atlikto maksājumu grafika rindas agrākiem periodiem.</li></ul><p>Noklusētā vērtība ir no ieņēmumu **un izdevumu atlikto maksājumu parametru** lapas.</p> |
| Vienāds ar periodu | <p>Norādiet, vai dienu skaits katrā periodā ir vienāds vai atšķiras atkarībā no perioda:</p><ul><li>**Jā** – katram periodam ir vienāds dienu skaits.</li><li>**Nē** – periodiem nav vienāds dienu skaits.</li></ul><p>Kad šī opcija ir iestatīta **uz Nē**, dienu skaits periodā tiek apsvērts, kad tiek aprēķināta summa katrā periodā atlikto maksājumu grafikam.</p><p>Noklusētā vērtība ir no ieņēmumu **un izdevumu atlikto maksājumu parametru** lapas.</p> |
| Grafiks no veidnes | <p>Norādiet, vai atlikto maksājumu grafiks ir izveidots, pamatojoties uz veidni vai beigu datumu:</p><ul><li>**Jā** – atlikto maksājumu grafiks tiek izveidots, pamatojoties uz veidni.</li><li>**Nē** – atlikto maksājumu grafiks tiek izveidots, pamatojoties uz beigu datumu.</li></ul> |
| Veidne | Izvēlieties atliktā maksājuma veidni. |
| Pārlabot sākuma datumu | <p>Norādiet, vai vēlaties ignorēt sākuma datumu:</p><ul><li>**Jā** – ignorēt sākuma datumu ar datumu, kas ievadīts laukā **Sākuma** datums.</li><li>**Nē** – sākuma datums ir noklusējuma atliktā **maksājuma sākuma datuma** noteikums, kas tiek piemērots rēķina datumam, kas norādīts rēķina **grāmatošanas** lapā. Šo noteikumu var iestatīt ieņēmumu un **izdevumu atlikto maksājumu parametru** lapā.</li></ul> |
| Atlikšanas sākuma datums | Norādiet atliktā maksājuma sākuma datumu. Noklusētā vērtība ir darbības datums. |
| Atlikšanas beigu datums | <p>Atliktā maksājuma beigu datums</p><p>Šis datums tiek automātiski aprēķināts, balstoties uz atlikto maksājumu veidni. Ja neviena veidne netiek atlasīta, datums jāievada manuāli.</p> |
| **Grafiks - Pēc notikuma** | |
| Veidne | <p>Atlasiet uz notikumu balstītu veidni. Šis lauks nav obligāts.</p><p>Atlasot veidni, vērtības no veidnes pārraksta visus uz notikumiem balstīos datus un notikumu rindas.</p> |
| Sadalījuma tips | <p>Atlasiet notikuma rindu sadalījuma tipu:</p><ul><li>**Mainīgās** summas – katrai rindai tiek ievadīta noteikta sadalījuma summa.</li><li>**Vienādas** summas – summa katrai rindai tiek sadalīta vienādi.</li><li>**Procenti** – summa tiek sadalīta, pamatojoties uz katrai rindai ievadīto procentuālo vērtību.</li><li>**Pabeigtības procenti** – katrai rindai tiek ievadīta kopējā pabeigtības vērtība.</li><p>**Mainīgais** daudzums – katrai rindai tiek ievadīts noteikts sadalījuma daudzums.</li></ul><p>**Piezīme.** Ja vēlaties atlasīt pabeigtības **procentus**, datumiem jābūt augošā secībā.</p> |
| **Izveidot atsevišķus notikumus katrai vienībai** | |
| Apraksts | <p>Norādiet, vai vēlaties atsevišķus notikumus pa vienībām:</p><ul><li>**Jā** – atdaliet notikuma rindas tā, lai katram daudzumam būtu viena rinda.<p>Piemēram, ir trīs notikumu rindas, un rēķinam ir četri daudzumi. Šajā gadījumā iegūtajam atliktā maksājuma grafikam ir 12 rindas.</p></li><li>**Nē** – neatdaliet notikuma rindas.</li></ul> |
| Beigu konts | <p>Atlasiet kontu, kas tiek lietots atpazītām rindām, kurām beidzies derīguma termiņš. Kontu var atlasīt pēc atlikto maksājumu grafika izveidošanas.</p><p>Ja notikumam ir iestatīts beigu datums, atpazīšanas procesa laikā atpazīšanas summa tiek pāriet uz derīguma konta beigu kontu.</p> |
| **Grafiks — pa notikumiem balstītas rindas** | |
| Apraksts | Notikuma apraksts. |
| Atlikšanas beigu datums | <p>Atlasiet notikuma beigu datumu.</p><p>**Piezīme.** Ja atlasāt beigu datumu, lauks Beigu **datums** tiek notīrīts. Nevar izmantot gan beigu datumu, gan beigu datumu.</p> |
| Beigu datums | <p>Atlasiet notikuma beigu datumu.</p><p>**Piezīme.** Ja atlasāt beigu datumu, lauks Beigu **datums** tiek notīrīts. Nevar izmantot gan beigu datumu, gan beigu datumu.</p> |
| Daudzums | <p>Norādiet sadalījuma daudzumu. Noklusējuma vērtība visām rindām ir **0** (nulle). Atjauninot daudzumu, visu rindu daudzumam ir jābūt vienādam vai mazākam par pārdošanas pasūtījumā norādīto rindas krājuma daudzumu.</p><p>Šis lauks ir pieejams tikai tad, ja **lauka Sadalījuma tips** iestatījums ir **Mainīgais daudzums**.</p><p>Ja rindas krājuma daudzums pārdošanas pasūtījumā tiek mainīts tā, ka tas ir mazāks nekā sākotnējais daudzums un tiek izveidots rēķins, tiek izveidotas mazāk uz notikumu balstītas rindas. Kopējais sadalītais daudzums nepārsniedz daudzumu, kas ir norādīts sākotnējā pārdošanas pasūtījumā vai norēķinu grafikā.</p> |
| Sadalījuma procenti | <p>Norādiet sadalījuma procentus. Ja Sadalījuma **tipa lauks** ir iestatīts uz **procentuālo** **vērtību vai pabeigtības** procentu, varat manuāli ievadīt procentus. Pretējā gadījumā tas tiek aprēķināts automātiski.</p><p>Ja sadalījuma **tipa lauks** ir iestatīts **uz procentuālo** vērtību, procentu kopsummai ir jābūt vienādai ar 100.</p> |
| Summa | <p>Norādiet sadalījuma summu. Ja Sadalījuma **tipa lauks** ir iestatīts uz **Mainīgās** summas **vai pabeigtības** procentu, varat manuāli ievadīt summu.</p><p>Ja sadalījuma **tipa lauks** ir iestatīts uz **pabeigtības** procentu un šeit ievadāt summu, **pabeigšanas procentu lauka vērtība** tiek aprēķināta automātiski.</p><p>Noapaļošanas dēļ aprēķinātā summa var tieši neatbilst manuāli ievadītajām. Ja nepieciešama precīza summa, lauku Sadalījuma tips **iestatiet uz** Mainīgās **summas**.</p> |
| Pabeigtības procents | <p>Norādiet pabeigtības procentus. Vērtībai ir jābūt diapazonā no 0 (nulle) līdz 100.</p><p>Šis lauks ir pieejams tikai tad, ja **sadalījuma tipa** lauks ir iestatīts kā pabeigtības **procenti**.</p> |
| Pabeigšanas summa | <p>Aprēķinātā kopsumma visām atlikto maksājumu grafika rindām.</p><p>Ja Sadalījuma **tipa** lauks ir iestatīts uz **pabeigtības procentu**, varat summu ievadīt manuāli. Šajā gadījumā pabeigtās daļas procentos lauka **vērtība tiek** aprēķināta, pamatojoties uz jūsu ievadīto summu.</p><p>Noapaļošanas dēļ aprēķinātā summa var tieši neatbilst manuāli ievadītajām.</p><p>Šis lauks ir pieejams tikai tad, ja **sadalījuma tipa** lauks ir iestatīts kā pabeigtības **procenti**.</p> |
| Atpazīt grāmatojot | <p>Norādiet, vai rinda tiek automātiski atpazīta, tiklīdz darbība tiek grāmatota:</p><ul><li>**Atlasīts** – rinda tiek automātiski atpazīta, tiklīdz darbība tiek grāmatota.</li><li>**Nodzēsts** – rinda netiek atpazīta, tiklīdz tiek grāmatota darbība.</li></ul> |
| Atzīšanas konts | <p>Norādiet notikuma atzīšanas kontu, ja konts atšķiras no konta, ko izmanto visam atlikto maksājumu grafikam.</p><p>Šo lauku var lietot kopā ar opciju **Atpazīt pēc** grāmatošanas.</p> |
