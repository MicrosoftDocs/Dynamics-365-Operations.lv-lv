---
title: Sistēmas noteikta klastera izdošana
description: Šajā tēmā ir sniegts pārskats par sistēmas noteiktu klastera izdošanu Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3c474705e5260f4be62bc59d8d1d84a1ba597b6f96eafd8f673cc110285fc597
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772356"
---
# <a name="system-directed-cluster-picking"></a>Sistēmas noteikta klastera izdošana

[!include [banner](../includes/banner.md)]

Klastera izdošana ir daļa no izdošanas procesa, kas ļauj izdot preces vairākiem pasūtījumiem vienlaikus, sagrupējot tos izdošanas klasteros. Pēc tam izdošanas vieta ir jāapmeklē tikai vienu reizi. Parasti šī funkcionalitāte tiek izmantota mazu pasūtījumu izdošanai vai daudzumiem, kas ir mazāki par pieteikuma daudzumu.

Iestatot sistēmas noteiktu klastera izdošanu, varat klastera veidā izdot darba galvenes, pamatojoties uz sistēmas ģenerētu klasteri. Sistēma klastera veidā izdod līdz tam pozīciju skaitam, kas norādīts klastera profilā. Tādēļ vienlaikus varat izdot vairākus pasūtījumus bez nepieciešamības manuāli izveidot klasteri.

Sistēmas noteikta klastera izdošana piedāvā alternatīvu manuālai klastera veidošanai, kur klastera izveidošanai tiek izmantots klastera profils. Pirms izmantošanas klastera profilā jādefinē vairākas ar iestatīšanu saistītas rindas.

- **Pozīciju skaits** atbilst pasūtījumu skaitam, kas tiks ievietoti klasterī. Tāpēc tas atbilst kravu skaitam.
- **Klastera pārtraukšana** nosaka, kad klasteris jāpārtrauc.
- **Ģenerēt klastera ID** kontrolē, vai klastera ID jāģenerē sistēmai, vai to ievada lietotājs.
- **Kārtošanas pārbaudes veids** nosaka, vai ir nepieciešama pozīcijas pārbaude.

Sistēmas noteikta klastera izdošanai tiek izmantots jauns mobilās ierīces izvēlnes vienums. Atlasītajai opcijai **Noteicējs** jānorāda **Klastera profila ID**. Papildus tam sistēmas noteikta darbu secības vaicājumi var grupēt pasūtījumus, pamatojoties uz uzņēmumam specifiskiem kritērijiem. Tādējādi varat papildus optimizēt darba pasūtījumu piešķiri, norādot pielāgotus kārtošanas kritērijus, izmantojot sistēmas noteiktās darbu secības vaicājumus.

Kad ir iespējota sistēmas noteikta klastera izdošana, noliktavas darbiniekiem tiek norādīts klasteris, kur izdošanas pasūtījumi ir iepriekš piešķirti klastera pozīcijām. Tādējādi darbinieki var sākt izdot preci vairākiem darba pasūtījumiem, apmeklējot izdošanas vietu tikai vienu reizi. Izdošanas procesu sistēmas noteiktai klastera izdošanai ir tāds pats kā process lietotāja noteiktai klastera izdošanai.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Iespējot Sistēmas noteikto klastera izdošanas līdzekli

Lai varētu izmantot šo līdzekli, tam vispirms jābūt iespējotam sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības. Šeit līdzeklis tiek norādīts kā:

- **Modulis** — Noliktavas vadība
- **Līdzekļa nosaukums** — Sistēmas noteiktā klastera izdošana

Arī šim līdzeklim nepieciešams iespējot pakārtoto līdzekli. Pakārtotais līdzeklis ir:

- **Modulis** — Noliktavas vadība
- **Līdzekļa nosaukums** — Organizācijas līmeņa sistēmas noteikta darba secība

## <a name="set-up-system-directed-cluster-picking"></a>Sistēmas noteiktas klastera izdošanas iestatīšana

### <a name="create-cluster-profiles"></a>Klastera profilu izveidošana

Klastera profili kontrolē, kā sistēma izveido katru klasteri. Ja ir nepieciešami dažādi klasteri, katram mobilās ierīces izvēlnes vienumam jāizveido cits klastera profils.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilā ierīce \> Klastera profili**.
2. Atlasiet **Jauns**.
3. Laukā **Klastera profila ID** ievadiet **2. pozīcija**.
4. Laukā **Nosaukums** ievadiet **2. pozīcija**.
5. Kopsavilkuma cilnē **Vispārīgi** ievadiet tālāk norādīto informāciju.

    - **Ģenerēt klastera ID** — atlasiet **Jā**. Šī opcija nosaka, vai sistēma automātiski izveido klastera ID, vai arī lietotājs to izveidos izdošanas sākumā. 
    - **Aktivizēt pozīcijas** — atlasiet **Jā**. Šī opcija nosaka, vai pozīciju nosaukumi tiek ģenerēti automātiski, pamatojoties uz pozīcijas nosaukuma iestatījumu. Ja šī opcija iestatīta uz **Nē**, tiek izmantots pozīcijas unikālais noliktavas vienības identifikators.
    - **Pozīciju skaits** — atlasiet **2**. Šis lauks nosaka maksimālo pozīciju skaitu, kas var būt klasterim (t.i., maksimālais kārbu, kravu utt. skaits).
    - **Pozīcijas nosaukums** — atlasiet **Skaitlisks**, lai pozīcijas tiktu secīgi numurētas. Ja atlasīsiet **Alfabētiski**, pozīcijas tiks nosauktas alfabētiskā secībā.
    - **Pārtraukt klasteri pie** — atlasiet **Ievietot**. Šis lauks nosaka, kad klasteris tiek pārtraukts. 
    - **Kārtošanas pārbaudes veids** — atlasiet **Pozīcijas skenēšana**. Šis lauks nosaka, vai ir pārbaudīta ievietošanas pozīcijā darbība.
        
6. Kopsavilkuma cilnē **Klastera kārtošana** varat definēt kārtošanas kritērijus, izveidojot jaunu rindu un ievadot tālāk minēto informāciju.

    - **Secības numurs** — atlasiet **1**. Šis lauks nosaka secību, ar kādu sistēma veic kārtošanu. Vērtība tiek ievadīta automātiski, bet to iespējams mainīt, ja tas nepieciešams.
    - **Lauka nosaukums** — ievadiet **WMSLocationId**. Šis lauks nosaka lauku, ko rinda izmanto kā kārtošanas kritērijus.
    - **Kārtošana** — atlasiet **Augošā secībā**. Šis lauks nosaka, vai kārtošana tiek veikta augošā vai dilstošā secībā.

### <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide

Lai izveidotu jaunu mobilās ierīces izvēlnes vienumu sistēmas noteiktai klastera izdošanai un saistītu klastera profila ID ar mobilās ierīces izvēlnes vienumu, veiciet tālāk minētās darbības.

1. Dodieties uz **Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi**.
1. Atlasiet **Jauns**.
1. Sadaļā Galvene ievadiet šādu informāciju.
    - **Izvēlnes vienuma nosaukums** — SD klasteris
    - **Nosaukums** — SD klasteris
    - **Režīms** — darbs
    - **Izmantot esošo darbu** — Jā

1. Kopsavilkuma cilnē **Vispārīgi** ievadiet tālāk norādīto informāciju.
    - **Noteicējs** — Sistēmas noteikta klastera izdošana
    - **Ģenerēt noliktavas vienību** — Jā
    - **Klastera profila ID** — 2. pozīcija

1. Kopsavilkuma cilnē **Darba klases** iestatiet šīs mobilās ierīces izvēlnes vienumam derīgo darba klasi, iestatot tālāk minētos laukus.
    - **Darba klases ID** — Pārdošana
    - **Darba pasūtījuma veids** — pārdošanas pasūtījumi

1. Darbību rūtī **Mobilās ierīces izvēlnes elementi** atlasiet **Sistēmas noteiktas darba secības vaicājumi** un veiciet tālāk minētās darbības, lai norādītu jaunu sistēmas noteiktas darba secības vaicājumu.
    - Darbību rūtī atlasiet **Jauns**.
    - **Secības numurs** — 1
    - **Apraksts** — darba prioritāte — darba ID

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**
1. Atlasiet cilni **Šķirošana**
1. Atlasiet **Pievienot**, lai pievienotu jaunu rindu, un pēc tam ievadiet tālāk minēto.
    - **Tabula** — darbs
    - **Atveidotā tabula** — Darbs
    - **Lauks** — Darba prioritāte
    - **Meklēšanas virziens** — Augošā secībā
1. Atlasiet **Pievienot**, lai pievienotu otru rindu, un pēc tam ievadiet tālāk minēto.
    - **Tabula** — darbs
    - **Atveidotā tabula** — Darbs
    - **Lauks** — Darba ID
    - **Meklēšanas virziens** — Augošā secībā

1. Sistēma tagad kārtos darba ID klasterī vispirms pēc darba prioritātes un pēc tam — pēc darba ID.

### <a name="set-up-a-mobile-device-menu"></a>Mobilās ierīces izvēlnes iestatīšana

1. Dodieties uz **Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.
1. Pievienojiet izvēlnes elementu **SD klasteris**, kuru tikko izveidojāt, mobilās ierīces izvēlnei.
1. Atlasiet izvēlni **Izejošais**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Ritiniet, līdz atrodat **SD klasteris**.
1. Atlasiet opciju **SD klasteris**, tiks iespējota bultiņa, kas norāda uz sarakstu **Izvēlņu struktūra**.
1. Atlasiet **bultiņas** pogu, lai pārvietotu izvēlnes elementu **SD klasteris** uz izvēlnes struktūru **Izejošais**.
1. Sarakstā **Izvēlņu struktūra** atlasiet **SD klasteris**, pēc tam atlasiet bultiņas **Uz augšu** vai **Uz leju**, lai pārvietotu izvēlnes elementu vēlamajā pozīcijā mobilās ierīces izvēlnē.

## <a name="scenario"></a>Scenārijs

### <a name="create-picking-work"></a>Izveidot izdošanas darbu

Pirms varēsiet iestatīt sistēmas noteikta klastera izdošanu, ir jāizveido piemēroti izejošie darbi. Iepriekš izveidotais klastera profils norāda divas klastera pozīcijas. Tādējādi ir jāizveido vismaz divi darba ID. Šajā scenārijā jūs izveidosit divus pārdošanas pasūtījumus, rezervētos krājumus, izlaidīsit pārdošanas pasūtījumus uz noliktavu un pēc tam manuāli apstrādāsit kopumu.

1. Pārejiet uz sadaļu **Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.
1. Lai izveidotu pirmo pārdošanas pasūtījumu, Darbību rūtī atlasiet **Jauns**.
    - Tiks atvērta izvēlne **Izveidot pārdošanas pasūtījumu**, ievadiet tālāk minēto informāciju.
        - Kopsavilkuma cilnē **Debitors** ievadiet **Debitora konts** - **US-004**.
        - Kopsavilkuma cilnē **Vispārīgi** ievadiet **Noliktava** - **62**.
        - Atlasiet **Labi**, lai aizvērtu izvēlni izveidotu pārdošanas pasūtījumu.
    - Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindās** atlasiet **Pievienot rindu**, ja jauna rinda netiek pievienota automātiski, un ievadiet tālāk minēto.
        - **Krājuma numurs** — A0001
        - **Daudzums** — 1
        - Atlasiet **Pievienot rindu**, lai pievienotu otro rindu.
        - **Krājuma numurs** — A0002
        - **Daudzums** — 3
    - Rezervējiet krājumus abām tikko izveidotajām rindām.
        - Atlasiet **1. rinda**.
        - Darbību rūtī **Pārdošanas pasūtījuma rindas** atlasiet **Krājums** un pēc tam sarakstā atlasiet **Rezervācija**.
        - Veidlapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
        - Kad rezervēšana ir pabeigta, aizveriet veidlapu **Rezervācija**.
        - Atkārtojiet šīs darbības, lai rezervētu krājumus **2. rindai**.
1. Lai izveidotu otro pārdošanas pasūtījumu, darbību rūtī atlasiet **Jauns**
    - Tiks atvērta izvēlne **Izveidot pārdošanas pasūtījumu**, ievadiet tālāk minēto informāciju.
        - Kopsavilkuma cilnē **Debitors** ievadiet **Debitora konts** - **US-005**.
        - Kopsavilkuma cilnē **Vispārīgi** ievadiet **Noliktava** - **62**.
        - Atlasiet **Labi**, lai aizvērtu izvēlni un izveidotu pārdošanas pasūtījumu
    - Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindās** atlasiet **Pievienot rindu**, ja jauna rinda netiek pievienota automātiski, un ievadiet tālāk minēto informāciju.
        - **Krājuma numurs** — A0001
        - **Daudzums** — 4
        - Atlasiet **Pievienot rindu**, lai pievienotu otro rindu.
        - **Krājuma numurs** — A0002
        - **Daudzums** — 2
    - Rezervējiet krājumus abām tikko izveidotajām rindām.
        - Atlasiet **1. rinda**.
        - Darbību rūtī **Pārdošanas pasūtījuma rindas** atlasiet **Krājums** un pēc tam sarakstā atlasiet **Rezervācija**.
        - Veidlapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
        - Kad rezervēšana ir pabeigta, aizveriet veidlapu **Rezervācija**.
        - Atkārtojiet šīs darbības, lai rezervētu krājumus **2. rindai**.
    - Aizveriet pārdošanas pasūtījumu un atgriezieties saraksta lapā **Visi pārdošanas pasūtījumi**.
1. Atrodiet abus tikko izveidotos pārdošanas pasūtījumus (iespējams, ir jāatsvaidzina lapa). Tabulā atlasiet abus pārdošanas pasūtījumus, izmantojot sadaļas atzīmi.
    - Darbību rūtī **Visi pārdošanas pasūtījumi** atlasiet cilni **Noliktava**.
    - Grupā **Darbības** atlasiet **Nodot izpildei noliktavā**, lai abi pārdošanas pasūtījumi tiktu nodoti noliktavai.
1. Kad nodošanas noliktavas process ir pabeigta, tiks parādīts informatīvs ziņojums.
    - Katram pārdošanas pasūtījumam tiks izveidotas piegādes.
    - Tiks izveidots kopums, un abi sūtījumi tiks piešķirti šim kopumam. Pierakstiet **Kopuma ID**.
1. Dodieties uz **Noliktavas pārvaldība > Izejošie kopumi > Sūtījuma kopumi > Visi kopumi**.
    - Sarakstā **Visi kopumi** atrodiet un atlasiet to **Kopuma ID**, ko izveidojāt iepriekšējā darbībā.
    - Darbību rūtī atlasiet cilni **Kopums**.
    - Grupā **Kopums** atlasiet **Process**, lai apstrādātu kopumu un izveidotu **Darbu**.
    - Informācijas ziņojumi tiks ģenerēti, kad apstrāde ir pabeigta, norādot, ka darbs ir izveidots un kopums ir iegrāmatots.
1. **Neobligāti**: dodieties uz **Noliktavas pārvaldība > Darbs > Darba informācija**, lai skatītu izveidoto darbu. Tiek izveidoti divi dažādi darba ID. Katram darba ID ir divas izdošanas rindas.

### <a name="run-the-mobile-device-flow"></a>Mobilās ierīces plūsmas palaišana

1. Pierakstieties mobilajā ierīcē lietotājam noliktavā **62**.
1. **Galvenajā izvēlnē** atlasiet **Izejošais**.
1. Izvēlē **Izejošais** atlasiet **SD klasteris**, lai aktivizētu izdošanu.
    - Tiek izveidots klasteris, un tam tiek pievienoti divi darba ID, ko izveidojāt iepriekš. Ja esat izveidojis vairāk nekā divus darba ID, pievienoti klasterim tiek tikai pirmie divi. Ņemiet vērā, ka darba ID tiek pievienoti klasterim augošā secībā, kā norādījāt vaicājuma iestatījumā.

    > [!NOTE]
    > Jaunais klasteris tiek automātiski izveidots tikai tad, ja iepriekš ir izveidoti pietiekami daudz papildu darba ID. Pretējā gadījumā tiek parādīts šāds ziņojums: "Klasterim nav atrasts pietiekami darba."

    - Kad atlasāt izvēlni, tiek parādīts pirmais izdošanas ekrāns. Sistēma apkopo visas atbilstošās izdošanas rindas no diviem darba ID un novirza jūs vienreiz apmeklēt izdošanas vietu, lai varētu izpildīt abus pasūtījumus, izmantojot vienu izdošanu. Šis process tiek veikts tādā pašā veidā kā lietotāja noteikts klastera izdošanas process.

1. Apstipriniet pirmo izdošanas vietu un krājumu, atlasot **Labi**.
    - Izdošanas daudzums būs krājuma kopsumma, kas parādīta pārdošanas pasūtījumos klasterī.
1. Ievadiet pozīcijas nosaukumu (skaitlisku vai alfabētisku), lai apstiprinātu, ka pozīcijai izdotais krājuma daudzums tika ievietots pareizā pozīcijā.
1. Atkārtojiet šo procesu, līdz visai preču daudzumi ir izdoti un ievietoti pareizajā pozīcijā.
1. Pēdējais solis mobilajā ierīcē ir **Ievietot** ievietot klasteri galīgajā vietā. Atlasiet **Labi**
    - Kad ievietošanas operācija ir apstiprināta, klasteris tiek slēgts un pārtraukts, pamatojoties uz vērtību, ko klastera profilā iestatījāt laukam **Pārtraukt klasteri pie**. Darba ID arī tiek slēgti.
1. Mobilajā ierīcē tiek parādīts ziņojums "Klasteris pabeigts".


[!INCLUDE[footer-include](../../includes/footer-banner.md)]