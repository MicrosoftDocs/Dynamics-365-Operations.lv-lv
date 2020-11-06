---
title: Zonas sliekšņa papildināšana
description: Uz zonu pamatota papildināšana izmanto minimālo/maksimālo (min./maks.) papildināšanas stratēģiju, bet novērtē visas noliktavas zonas, nevis tikai atsevišķus novietojumus. Tāpēc noliktavas vadītājs var ātrāk uzzināt par gadījumiem, kad izdošanas zonā ir nepieciešami papildu krājumi.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e13b5fd895fca7f8fe77809348d63ed8867dea9e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017326"
---
# <a name="zone-threshold-replenishment"></a>Zonas sliekšņa papildināšana

[!include [banner](../includes/banner.md)]

Uz zonu pamatota papildināšana izmanto minimālo/maksimālo (min./maks.) [papildināšanas](replenishment.md) stratēģiju, bet novērtē visas noliktavas zonas, nevis tikai atsevišķus novietojumus. Tāpēc noliktavas vadītājs var ātrāk uzzināt par gadījumiem, kad izdošanas zonā ir nepieciešami papildu krājumi.

Šī līdzekļa iestatīšana līdzinās uz novietojumu pamatotas papildināšanas iestatīšanai. Iestatot min./maks. papildināšanas veidni, varat arī norādīt, vai slieksnis ir jānovērtē katram novietojumam vai katrai zonai. Ja iestatāt uz zonām pamatotu novērtējumu, zonas atlases vaicājumam ir jāpievieno konkrētas zonas.

Tāpat kā uz novietojumu pamatota min./maks. papildināšana, uz zonu pamatota min./maks. papildināšana ir pamatota uz minimālo krājumu iestatīšanu, kas aktivizē papildināšanas darba izveidi atlasītiem krājumiem. Šis papildināšanas darbs palielinās krājumu līdz norādītajam maksimālajam zonas slieksnim.

> [!NOTE]
> Zonas papildināšanas procesi produkta variantiem netiek atbalstīti pašreizējā laidienā.


Atšķirībā no uz novietojumu pamatotas min./maks. papildināšanas, uz zonu pamatotai min./maks. papildināšanai nav nepieciešami izvietojumi, no novērtētu, vai novietojumos ir jāglabā kāds konkrēts krājums. Tāpēc uz zonu pamatotā papildināšana ļauj izmantot min./maks. papildināšanu pat tad, ja jums noliktavā nav fiksēta novietojuma katram krājumam vai krājuma variantam. Ja zonā esošais daudzums nokrītas zem norādītā minimālā sliekšņa, tiek izveidots papildināšanas darbs. Novietojuma direktīvas noteiks, kurā konkrētajā novietojumā ir jāievieto krājumi.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Līdzekļa Zonas sliekšņa papildināšana ieslēgšana

Lai varētu izmantot līdzekli *Zonas sliekšņa papildināšana* , tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Zonas sliekšņa papildināšana*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Uz zonu pamatotas papildināšanas iestatīšana

Lai iestatītu uz zonu pamatotu papildināšanu, ir jākonfigurē vairākas sistēmas daļas. Šajā sadaļā ir izklāstīti vairāki iestatījumi un nodrošināti demonstrācijas dati, ko varat ievadīt, ja šīs tēmas beigās vēlaties strādāt ar scenāriju.

### <a name="set-up-directive-codes"></a>Direktīvas kodu iestatīšana

[Direktīvas kodi](control-warehouse-location-directives.md) sniedz iespēju konkrētāk definēt novietojuma veidni, kas tiek izmantota darba veidnē. Katrs kods izveido kopīgu vērtību, uz ko varat atsaukties, konfigurējot katras veidnes veidu.

#### <a name="view-and-edit-directive-codes"></a>Direktīvas kodu skatīšana un rediģēšana

Lai skatītu vai rediģētu direktīvas kodus, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Direktīvas kodi**.

#### <a name="prepare-demo-data-directive-codes"></a>Demonstrācijas datu direktīvas kodu sagatavošana

Šajā piemērā ir parādīts, kā sagatavot direktīvas kodu. Ja plānojat strādāt ar scenāriju šīs tēmas beigās, izmantojiet šeit sniegtās demonstrācijas datu vērtības. Pretējā gadījumā izmantojiet savas vērtības.

1. Atlasiet **USMF** juridisko personu, lai strādātu ar demonstrācijas datiem.
1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Direktīvas kodi**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Direktīvas kods:** _Zonas papild._
    - **Direktīvas apraksts:** _Zonas papildināšana_

1. Atlasiet **Saglabāt** , lai saglabātu jauno kodu.

### <a name="set-up-replenishment-templates"></a>Iestatīt papildināšanas veidnes

[Min./maks. papildināšanas veidnes](tasks/set-up-min-max-replenishment-process.md) ir galvenais mehānisms optimālu līmeņu uzturēšanai izdošanas novietojumos. Šajās veidnēs ir jāiestata kārtulas, kas tiks izmantotas krājumu papildināšanai noliktavā. Papildināšana, ko veidnes var izmantot uz iekļaušanas zonu pamatotai papildināšanai.

#### <a name="view-and-edit-replenishment-templates"></a>Papildināšanas veidņu skatīšana un labošana

Papildināšanas veidne ir kārtulu kopa, kas kontrolē novietojuma papildināšanas laiku un veidu. Atlasiet veidni, lai kontrolētu, kad un kā tiek veikta papildināšana. Lai skatītu vai rediģētu papildināšanas veidnes, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes**.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Demonstrācijas datu papildināšanas veidnes sagatavošana

Šajā piemērā ir parādīts, kā sagatavot papildināšanas veidni. Ja plānojat strādāt ar scenāriju šīs tēmas beigās, izmantojiet šeit sniegtās demonstrācijas datu vērtības. Pretējā gadījumā izmantojiet savas vērtības.

1. Atlasiet **USMF** juridisko personu, lai strādātu ar demonstrācijas datiem.
1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes**.
1. Darbību rūtī atlasiet **Rediģēt** , lai lapu padarītu rediģējamu.
1. Lai režģim **Pārskats** pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Papildināšanas veidne:** _Zonas min/maks. papild._
    - **Apraksts:** _Zonas min./maks. papildināšana_
    - **Papildināšanas veids:** _Minimums vai maksimums_

1. Atlasiet **Saglabāt**.
1. Kamēr jaunā rinda vēl ir atlasīta režģī **Pārskats** , atlasiet vērtību **Jauns** virs režģa **Detalizēta informācija par papildināšanas veidni** , lai pievienotu rindu, kas ir saistīta ar tikko izveidoto papildināšanas veidni *Zonas min./maks. papild.*
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Kārtas numurs:** ievadiet _1_.
    - **Apraksts:** ievadiet _Izdošanas zonas papildināšana_.
    - **Papildināšanas vienība:** atlasiet _ea_.
    - **Pieprasījuma veids:** atstājiet šo lauku tukšu.
    - **Direktīvas kods:** šis lauks saista papildināšanas veidni ar novietojuma direktīvu. Atlasiet iepriekš izveidoto demonstrācijas datu direktīvas kodu ( _Zonas papild._ )
    - **Darba veidne:** Atstājiet šo lauku tukšu.
    - **Minimālais daudzums:** šajā laukā tiek iestatīts daudzums, saistībā ar kuru tiek aktivizēta papildināšana. Ievadiet _50_.
    - **Maksimālais daudzums:** šajā laukā tiek iestatīts maksimālais krājuma daudzums, kāds var būt zonā. Ģenerētais papildināšanas darbs palielinās krājumus līdz šim daudzumam. Ievadiet _150_.
    - **Vienība:** šajā laukā tiek iestatīta minimālo un maksimālo vērtību vienība. Atlasiet _ea_.
    - **Pieprasījuma pieaugums:** atlasiet _Noapaļot uz augšu_.
    - **Papildināt tukšus fiksētos novietojumus:** atlasiet šo izvēles rūtiņu.
    - **Papildināt tikai fiksētos novietojumus:** notīriet šo izvēles rūtiņu.
    - **Produkta vaicājuma režīms:** atlasiet _Produkta vaicājums_.
    - **Papildināšanas sliekšņa diapazons:** šajā laukā tiek definēts, vai veidnei ir jānovērtē pēc zonas vai pēc konkrēta novietojuma. Atlasiet _Zona_.
    - **Noliktava:** atlasiet _61_.

1. Atlasiet opciju **Atlasīt produktus** virs režģa **Detalizēta informācija par papildināšanas veidni**.
1. Dialoglodziņā **Produkta vaicājums** cilnē **Diapazon** atlasiet **Pievienot** , lai pievienotu rindu režģim.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** _Krājums_
    - **Atveidotā tabula:** _Krājums_
    - **Lauks:** _Krājuma numurs_
    - **Kritēriji:** _A0001_

1. Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.
1. Atlasiet opciju **Atlasīt papildināmās zonas** virs režģa **Detalizēta informācija par papildināšanas veidni**.
1. Dialoglodziņā **Zonas vaicājums** cilnē **Diapazons** pievienojiet rindu režģim.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** _Noliktavas zona_
    - **Atveidotā tabula:** _Noliktavas zona_
    - **Lauks:** _Zonas ID_
    - **Kritēriji:** _FLOOR_

1. Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.

### <a name="set-up-location-directives"></a>Iestatīt novietojuma direktīvas

Atšķirībā no min./maks. papildināšanas, kas pamatota uz novietojumu, uz zonu pamatotajai min./maks papildināšanai ir jāiestata gan izdošanas novietojuma direktīvas, gan izvietošanas novietojuma direktīvas, jo sistēma novērtē visu zonu, nevis tikai izejošā darba izdošanas novietojumu.

#### <a name="view-and-edit-location-directives"></a>Novietojuma direktīvu skatīšana un rediģēšana

Lai skatītu vai rediģētu novietojuma direktīvas, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Novietojuma direktīvas**.

Piemērus par to, kā izmantot iestatījumus, lai izveidotu nepieciešamās izdošanas novietojuma direktīvas un izvietošanas novietojuma direktīvas, skatiet nākamajā sadaļā.

#### <a name="prepare-demo-data-location-directives"></a>Demonstrācijas datu novietojuma direktīvas sagatavošana

Lai sagatavotu demonstrācijas datus tā, ka tos var izmantot scenārijā šīs tēmas beigās, ir jāizveido divas novietojuma direktīvas — viena izdošanai un viena izvietošanai.

##### <a name="create-a-replenishment-pick-directive"></a>Papildināšanas izdošanas direktīvas izveide

1. Atlasiet **USMF** juridisko personu, lai strādātu ar demonstrācijas datiem.
1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.
1. Kreisajā rūtī laukam **Darba pasūtījuma veids** iestatiet vērtību _Papildināšana_.
1. Lai izveidotu jaunu direktīvu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet šādas vērtības:

    - **Kārtas numurs:** akceptējiet noklusējuma vērtību.
    - **Nosaukums:** ievadiet _Zonas izdošana_.
    - **Darba veids:** atlasiet _Izdošana_.
    - **Vieta:** atlasiet _6_.
    - **Noliktava:** atlasiet _61_.
    - **Direktīvas kods:** atstājiet šo lauku tukšu.
    - **Vairāki SKU:** opcijai iestatiet vērtību _Nē_.

1. Atlasiet **Saglabāt** , lai izveidotu direktīvu, kurai ir jūsu līdz šim brīdim izveidotie iestatījumi.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns** , lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Kārtas numurs:** ievadiet _1_.
    - **No daudzuma:** ievadiet _0_.
    - **Līdz daudzumam:** ievadiet _10000000_.
    - **Vienība:** atstājiet šo lauku tukšu.
    - **Meklēt daudzumu:** atlasiet _Nav_.
    - **Ierobežot pēc vienības:** notīriet šo izvēles rūtiņu.
    - **Noapaļot līdz vienībai:** notīriet šo izvēles rūtiņu.
    - **Meklēt iepakojuma daudzumu:** notīriet šo izvēles rūtiņu.
    - **Atļaut sadali:** atlasiet šo izvēles rūtiņu.

1. Atlasiet **Saglabāt** , lai saglabātu jauno rindu.
1. Kamēr jūsu jaunā rinda vēl ir atlasīta režģī **Rindas** , kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns** , lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Kārtas numurs:** ievadiet _1_.
    - **Nosaukums:** ievadiet _Izdot no lielapjoma_.
    - **Fiksēta novietojuma lietojums:** atlasiet _Fiksēti un nefiksēti novietojumi_.
    - **Atļaut negatīvus krājumus:** notīriet šo izvēles rūtiņu.
    - **Partija iespējota:** notīriet šo izvēles rūtiņu.
    - **Stratēģija:** atlasiet _Nav_.

1. Atlasiet **Saglabāt** , lai saglabātu jauno darbību.
1. Kamēr jaunā darbība vēl ir atlasīta, atlasiet **Rediģēt vaicājumu** virs režģa **Novietojuma direktīvas darbības**.
1. Tiks parādīts dialoglodziņš, kurā varat atlasīt novietojumus, no kuriem papildināt. Cilnē **Diapazons** atlasiet **Pievienot** , lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** _Novietojumi_
    - **Atvasinātā tabula:** _Vietas_
    - **Lauks:** _Zonas ID_
    - **Kritēriji:** _LIELAPJOMA_

1. Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.
1. Atlasiet **Saglabāt** , lai saglabātu novietojuma direktīvu.

##### <a name="create-a-replenishment-put-directive"></a>Papildināšanas izvietošanas direktīvas izveide

1. Lapā **Novietojuma direktīvas** kreisajā rūtī pārbaudiet, vai laukam **Darba pasūtījuma veids** joprojām ir iestatīta vērtība _Papildināšana_.
1. Lai izveidotu vēl vienu jaunu direktīvu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet šādas vērtības:

    - **Kārtas numurs:** akceptējiet noklusējuma vērtību.
    - **Nosaukums:** ievadiet _Zonas izvietošana_.
    - **Darba pasūtījuma veids:** atlasiet _Izvietošana_.
    - **Vieta:** atlasiet _6_.
    - **Noliktava:** atlasiet _61_.
    - **Direktīvas kods**  — atlasiet _Zonas papild._ , lai saistītu novietojuma direktīvu ar papildināšanas veidni, ko izveidojāt iepriekš, izmantojot iepriekš izveidoto kodu.
    - **Vairāki SKU:** opcijai iestatiet vērtību _Nē_.

1. Atlasiet **Saglabāt** , lai izveidotu direktīvu, kurai ir jūsu līdz šim brīdim izveidotie iestatījumi.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns** , lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Kārtas numurs:** ievadiet _1_.
    - **No daudzuma:** ievadiet _0_.
    - **Līdz daudzumam:** ievadiet _10000000_.
    - **Vienība:** atstājiet šo lauku tukšu.
    - **Meklēt daudzumu:** atlasiet _Nav_.
    - **Ierobežot pēc vienības:** notīriet šo izvēles rūtiņu.
    - **Noapaļot līdz vienībai:** notīriet šo izvēles rūtiņu.
    - **Meklēt iepakojuma daudzumu:** notīriet šo izvēles rūtiņu.
    - **Atļaut sadali:** atlasiet šo izvēles rūtiņu.

1. Atlasiet **Saglabāt** , lai saglabātu jauno rindu.
1. Kamēr jūsu jaunā rinda vēl ir atlasīta režģī **Rindas** , kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns** , lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Kārtas numurs:** ievadiet _1_.
    - **Nosaukums:** ievadiet _Zonas izvietošana_.
    - **Fiksēta novietojuma lietojums:** atlasiet _Fiksēti un nefiksēti novietojumi_.
    - **Atļaut negatīvus krājumus:** notīriet šo izvēles rūtiņu.
    - **Partija iespējota:** notīriet šo izvēles rūtiņu.
    - **Stratēģija:** atlasiet _Konsolidēt_.

1. Atlasiet **Saglabāt** , lai saglabātu jauno darbību.
1. Kamēr jaunā darbība vēl ir atlasīta, atlasiet **Rediģēt vaicājumu** virs režģa **Novietojuma direktīvas darbības**.
1. Tiks parādīts dialoglodziņš, kurā varat atlasīt papildināmo zonu. Šai zonai ir jābūt tai pašai zonai, kas norādīta papildināšanas veidnē. Cilnē **Diapazons** atlasiet **Pievienot** , lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** _Novietojumi_
    - **Atvasinātā tabula:** _Vietas_
    - **Lauks:** _Zonas ID_
    - **Kritēriji:** _FLOOR_

1. Atlasiet **Labi** , lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.
1. Atlasiet **Saglabāt** , lai saglabātu novietojuma direktīvu.

## <a name="scenario"></a>Scenārijs

Šajā sadaļā ir pieejams parauga scenārijs, kur parādīts, kā strādāt ar līdzekli.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Parauga scenārijam nepieciešamo parauga datu sagatavošana

Pirms sākt darbu ar scenāriju, aktivizējiet parauga datus un iestatiet līdzekli, kā tas ir izklāstīts šajā sadaļā un iepriekšējās šīs tēmas sadaļās.

#### <a name="use-the-usmf-legal-entity"></a>USMF juridiskas personas izmantošana

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

#### <a name="prepare-additional-sample-data"></a>Papildu parauga datu sagatavošana

Kad atlasīsit **USMF** juridisko vienību, pievienojiet nepieciešamos papildu parauga datus, kas norādīti sadaļā [Uz zonu pamatotas papildināšanas iestatīšana](#setup) iepriekš šajā tēmā.

#### <a name="check-your-on-hand-inventory"></a>Rīcībā esošo krājumu pārbaude

Izpildiet šīs darbības, lai pārliecinātos, vai jūsu sistēmā ir iekļauti pietiekami daudz krājumu, kas nepieciešami parauga scenārija atbalstīšanai.

1. Pārbaudiet, vai rīcībā ir krājumi krājumam *A0001* divos dažādos novietojumos izdošanas zonā ( *FLOOR* ), kas ir norādīta papildināšanas veidnē. Tomēr kopējiem krājumiem ir jābūt mazākiem par nepieciešamo minimālo daudzumu ( *50* ), kas norādīts papildināšanas veidnē. Šādi varat simulēt, kā notiek aprēķini visai zonai, nevis tikai vienam atsevišķam novietojumam. **Izmantojiet jebkuru no noliktavas procesiem, lai pēc nepieciešamības koriģētu krājumus.**
1. Pārliecinieties, vai krājumam *A0001* ir pietiekami daudz krājumu lielapjoma novietojumā, kas norādīts zonas izdošanas novietojuma direktīvā, kur papildināšanas darbam ir jāpaņem krājumi no zonas ID *BULK*. Kopējiem krājumiem ir jābūt lielākiem par nepieciešamo maksimālo daudzumu ( *150* ), kas norādīts papildināšanas veidnē.
1. Ieteicama izvēles iespēja: izpildiet šīs darbības, lai izveidotu krājumu korekcijas žurnālu.

    1. Dodieties uz **Krājumu pārvaldība \> Žurnāla ieraksti \> Krājumi \> Krājumu korekcija**.
    1. Atlasiet **Jauns**.
    1. Dialoglodziņā **Krājumu žurnāla izveide** laukā **Noliktava** atlasiet *61*.
    1. Atlasiet **Labi**.
    1. Kopsavilkuma cilnē **Žurnāla rindas** izmantojiet pogu **Jauns** , lai režģim pievienotu trīs rindas un iestatītu tālāk norādītās vērtības. Pēc katras rindas iestatīšanas beigām atlasiet **Saglabāt**.

        - **1. rinda**

            - **Krājuma numurs:** *A0001*
            - **Vieta:** *6*
            - **Noliktava:** *61*
            - **Novietojums:** *02A01R1S1B*
            - **Unikāla noliktavas vienība**  — sarakstā atlasiet esošu unikālu noliktavas vienību sarakstā vai izveidojiet jaunu unikālu noliktavas vienību.
            - **Daudzums:** *1000*

        - **2. rinda**

            - **Krājuma numurs:** *A0001*
            - **Vieta:** *6*
            - **Noliktava:** *61*
            - **Novietojums:** *07A01R2S1B*
            - **Unikāla noliktavas vienība**  — sarakstā atlasiet esošu unikālu noliktavas vienību sarakstā vai izveidojiet jaunu unikālu noliktavas vienību.
            - **Daudzums:** *15*

        - **3. rinda**

            - **Krājuma numurs:** *A0001*
            - **Vieta:** *6*
            - **Noliktava:** *61*
            - **Novietojums:** *07A01R1S1B*
            - **Unikāla noliktavas vienība**  — sarakstā atlasiet esošu unikālu noliktavas vienību sarakstā vai izveidojiet jaunu unikālu noliktavas vienību.
            - **Daudzums:** *10*

    1. Darbību rūtī atlasiet **Pārbaudīt**. Pirms pāriešanas uz nākamo soli novērsiet visas atrastās kļūdas.
    1. Darbību rūtī atlasiet **Grāmatot** , lai noliktavā grāmatotu krājumus.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Parauga scenārijs: uz zonas pamatotas min./maks. papildināšanas izpilde

Kad ir ievietoti visi priekšnosacījuma parauga dati, varat aktivizēt papildināšanu, izpildot tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Papildināšana \> Papildināšanas**.
1. Dialoglodziņā **Papildināšana** kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**.
1. Dialoglodziņā **Vaicājums** cilnē **Diapazons** rediģējiet noklusējuma tabulas rindu, kā norādīts tālāk.

    - **Tabula:** atlasiet _Papildināšanas veidnes_.
    - **Atveidotā tabula:** atlasiet _Papildināšanas veidnes_.
    - **Lauks:** atlasiet _Papildināšanas veidne_.
    - **Kritēriji:** atlasiet _Zonas min./maks. papild._ Šī papildināšanas veidne ir tā papildināšanas veidne, kuru izveidojāt, kad šim scenārijam sagatavojāt demonstrācijas datus.

1. Atlasiet **Labi** , lai saglabātu vaicājumu, un dodieties atpakaļ uz dialoglodziņu **Papildināšana**.
1. Atlasiet **Labi** , lai palaistu papildināšanas veidni.

Papildināšanas darbs tagad ir izveidots, lai izdotu krājumus no zonas *BULK* un papildinātu zonu *FLOOR*.

## <a name="notes-and-tips"></a>Piezīmes un padomi

Tālāk ir sniegtas dažas piezīmes un padomi darbam ar līdzekli.

- Lai iestatītu papildināšanas darbu, kas tiks novirzīts uz vēlamo zonu, papildināšanas veidnes rindas un novietojuma direktīvas varat saistīt, izmantojot kādu no tālāk norādītajiem veidiem.

    - Rediģējiet novietojuma direktīvas galvenes vaicājumu un filtrējiet atlasītās papildināšanas veidnes rindas.
    - Izmantojiet direktīvas kodu papildināšanas veidnes rindā un saskaņojiet to ar izvietošanas novietojuma direktīvu.

- Ja izmantojat dinamiskos novietojumus, papildināšanas darbs tiks izveidots vai nu pirmajam pieejamajam novietojumam, vai novietojumam, kurā jau ir krājumi, ja novietojuma direktīvas darbība ir iestatīta izmantot stratēģiju **Konsolidēt**.
- Ja zonu vietā izmantojat fiksētus novietojumus, izmantojiet [standarta min./maks. papildināšanu](tasks/set-up-min-max-replenishment-process.md).
