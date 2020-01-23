---
title: Sistēmas noteikta klastera izdošana
description: Šajā tēmā ir sniegts pārskats par sistēmas noteiktu klastera izdošanu Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c3b23a5d3b77bae89e4845bdff4ab20f95c46497
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917860"
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

Sistēmas noteikta klastera izdošanai tiek izmantots jauns mobilās ierīces izvēlnes vienums. Opcijai **Noteicējs** jānorāda klastera profila ID. Papildus tam sistēmas noteikta vaicājumu secība var grupēt pasūtījumus, pamatojoties uz uzņēmumam specifiskiem kritērijiem. Tādējādi varat papildus optimizēt darba pasūtījumu piešķiri, norādot pielāgotus kārtošanas kritērijus sistēmas noteiktā vaicājumu secībā.

Kad ir paveikta sistēmas noteikta klastera izdošana, noliktavas darbiniekiem tiek norādīts klasteris, kur izdošanas pasūtījumi ir iepriekš piešķirti klastera pozīcijām. Tādējādi darbinieki var sākt izdot preci vairākiem darba pasūtījumiem, apmeklējot izdošanas vietu tikai vienu reizi. Izdošanas procesu sistēmas noteiktai klastera izdošanai ir tāds pats kā process lietotāja noteiktai klastera izdošanai.

## <a name="set-up-system-directed-cluster-picking"></a>Sistēmas noteiktas klastera izdošanas iestatīšana

### <a name="create-cluster-profiles"></a>Klastera profilu izveidošana

Klastera profili kontrolē, kā sistēma izveido katru klasteri. Ja ir nepieciešami dažādi klasteri, katram mobilās ierīces izvēlnes vienumam jāizveido cits klastera profils.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilā ierīce \> Klastera profili**.
2. Atlasiet **Jauns**.
3. Laukā **Klastera profila ID** ievadiet **2. pozīcija**.
4. Laukā **Nosaukums** ievadiet **2. pozīcija**.
5. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus.

    - **Ģenerēt klastera ID:** iestatiet šo opciju uz **Jā**. Šī opcija nosaka, vai sistēma automātiski izveido klastera ID, vai arī lietotājs to izveidos izdošanas sākumā.
    - **Aktivizēt pozīcijas:** iestatiet šo opciju uz **Jā**. Šī opcija nosaka, vai pozīciju nosaukumi tiek ģenerēti automātiski, pamatojoties uz pozīcijas nosaukuma iestatījumu. Ja šī opcija iestatīta uz **Nē**, tiek izmantots pozīcijas unikālais noliktavas vienības identifikators.
    - **Pozīciju skaits:** ievadiet **2**. Šis lauks nosaka maksimālo pozīciju skaitu, kas var būt klasterim (t.i., maksimālais kārbu, kravu utt. skaits).
    - **Pozīcijas nosaukums:** atlasiet **Skaitlisks**, lai pozīcijas tiktu secīgi numurētas. Ja atlasīsiet **Alfabētiski**, pozīcijas tiks nosauktas alfabētiskā secībā.
    - **Pārtraukt klasteri pie:** atlasiet **Ievietot**. Šis lauks nosaka, kad klasteris tiek pārtraukts.
    - **Kārtošanas pārbaudes veids:** atlasiet **Pozīcijas skenēšana**. Šis lauks nosaka, vai ir pārbaudīta ievietošanas pozīcijā darbība.

6. Kopsavilkuma cilnē **Klastera kārtošana** varat definēt kārtošanas kritērijus, izveidojot jaunu rindu un iestatot tālāk minētos laukus.

    - **Sērijas numurs:** šis lauks nosaka secību, ar kādu sistēma veic kārtošanu. Vērtība tiek ievadīta automātiski, bet to iespējams mainīt pēc nepieciešamības.
    - **Lauka nosaukums:** atlasiet **WMSLocationId**. Šis lauks nosaka lauku, ko rinda izmanto kā kārtošanas kritērijus.
    - **Kārtošana:** atlasiet **Augošā secībā**. Šis lauks nosaka, vai kārtošana tiek veikta augošā vai dilstošā secībā.

### <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide

Lai izveidotu jaunu mobilās ierīces izvēlnes vienumu sistēmas noteiktai klastera izdošanai un saistītu klastera profila ID ar mobilās ierīces izvēlnes vienumu, veiciet tālāk minētās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
2. Atlasiet **Jauns**.
3. Laukā **Izvēlnes vienuma nosaukums** ievadiet **SD klasteris**.
4. Laukā **Nosaukums** ievadiet **SD klasteris**.
5. Laukā **Režīms** atlasiet **Darba**.
6. Iestatiet opciju **Izmantot esošo darbu** uz **Jā**.
7. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus.

    - **Noteicējs:** atlasiet **Sistēmas noteikts**.
    - **Ģenerēt pozīcijas unikālo noliktavas vienības identifikatoru:** iestatiet šo opciju uz **Jā**.
    - **Klastera profila ID:** atlasiet **2. pozīcija**.

8. Kopsavilkuma cilnē **Darba klases** iestatiet šīs mobilās ierīces izvēlnes vienumam derīgo darba klasi, iestatot tālāk minētos laukus.

    - **Darba klases ID:** pārliecinieties, ka ir ievadīts **Pārdošana**.
    - **Darba pasūtījuma veids:** pārliecinieties, ka ir ievadīts **Pārdošanas pasūtījumi**.

9. Lai norādītu jaunu sistēmas noteiktu darba secības vaicājumu, veicot tālāk minētās darbības.

    1. Atlasiet **Jauns**.
    2. Laukā **Secības numurs** ievadiet **1**.
    3. Laukā **Apraksts** atlasiet **Darba prioritāte — darba ID**.

10. Izvēlnē atlasiet **Rediģēt vaicājumu**.
11. Cilnē **Kārtošana** iestatiet tālāk minētos laukus.

    - **Tabula:** iestatiet **Darbs**.
    - **Atveidotā tabula:** iestatiet **Darbs**.
    - **Lauks:** atlasiet **Darba prioritāte**.
    - **Meklēšanas virziens:** atlasiet **Augošā secībā**.
    - **Tabula:** iestatiet **Darbs**.
    - **Atveidotā tabula:** iestatiet **Darbs**.
    - **Lauks:** atlasiet **Darba ID**.
    - **Meklēšanas virziens:** atlasiet **Augošā secībā**.

Sistēma tagad kārtos darba ID klasterī vispirms pēc darba prioritātes un pēc tam — pēc darba ID.

### <a name="set-up-a-mobile-device-menu"></a>Mobilās ierīces izvēlnes iestatīšana

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
2. Pievienojiet tikko izveidoto izvēlnes vienumu vēlamajai izvēlnei.

## <a name="example"></a>Paraugs

### <a name="create-picking-work"></a>Izveidot izdošanas darbu

Pirms varēsiet iestatīt sistēmas noteikta klastera izdošanu, ir jāizveido daži piemēroti izejošie darbi. Iepriekš izveidotais klastera profils norāda divas klastera pozīcijas. Tādējādi ir jāizveido vismaz divi darba ID.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.
3. Laukā **Debitora konts** atlasiet jebkuru debitoru.
4. Kopsavilkuma cilnes **Vispārīgi** laukā **Noliktava** atlasiet noliktavu **62**.
5. Atlasiet **Labi**.
6. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Pievienot rindu**.
7. Laukā **Krājuma numurs** atlasiet **A0001**.
8. Laukā **Daudzums** ievadiet **1**.
9. Atlasiet **Pievienot rindu**, lai pievienotu otro rindu.
10. Laukā **Krājuma numurs** atlasiet **A0002**.
11. Laukā **Daudzums** ievadiet **3**.
12. Atkārtojiet no 2. līdz 6. darbībai.
13. Laukā **Krājuma numurs** atlasiet **A0001**.
14. Laukā **Daudzums** ievadiet **4**.
15. Atlasiet **Pievienot rindu**, lai pievienotu otro rindu.
16. Laukā **Krājuma numurs** atlasiet **A0002**.
17. Laukā **Daudzums** ievadiet **2**.

Rezervējiet krājumu un izdodiet to noliktavai. Tiek izveidoti divi dažādi darba ID. Katram darba ID ir divas izdošanas rindas.

### <a name="run-the-mobile-device-flow"></a>Mobilās ierīces plūsmas palaišana

1. Mobilajā ierīcē atlasiet izvēlni, kurā ir iekļauts jaunais mobilās ierīces izvēlnes vienums.
2. Atlasiet izvēlnes vienumu **SD klasteris** un iniciējiet izdošanu. Tiek izveidots klasteris, un tam tiek pievienoti divi darba ID, ko izveidojāt iepriekš. Ja esat izveidojis vairāk nekā divus darba ID, pievienoti klasterim tiek tikai pirmie divi. Ņemiet vērā, ka darba ID tiek pievienoti klasterim augošā secībā, kā norādījāt vaicājuma iestatījumā.

    > [!NOTE]
    > Jaunais klasteris tiek automātiski izveidots tikai tad, ja iepriekš ir izveidoti pietiekami daudz papildu darba ID. Pretējā gadījumā tiek parādīts šāds ziņojums: "Klasterim nav atrasts pietiekami darba."

    Kad atlasāt izvēlni, tiek parādīts pirmais izdošanas ekrāns. Sistēma apkopo visas atbilstošās izdošanas rindas no diviem darba ID un novirza jūs vienreiz apmeklēt izdošanas vietu, lai varētu izpildīt abus pasūtījumus, izmantojot vienu izdošanu. Šis process tiek veikts tādā pašā veidā kā lietotāja noteikts klastera izdošanas process.

3. Apstipriniet pirmo izdošanu. Pēc tam jāievada pozīcijas nosaukumu, lai apstiprinātu, ka preces ir ievietotas pareizajā pozīcijā.
4. Atkārtojiet šo procesu, līdz visas preces ir izdotas un ievietotas pareizajā pozīcijā.
5. Pēdējais solis mobilajā ierīcē ir ievietot klasteri galīgajā vietā. Kad šī ievietošanas operācija ir apstiprināta, klasteris tiek slēgts un pārtraukts, pamatojoties uz vērtību, ko klastera profilā iestatījāt laukam **Pārtraukt klasteri pie**. Darba ID arī tiek slēgti.
6. Mobilajā ierīcē tiek parādīts ziņojums "Klasteris pabeigts".
