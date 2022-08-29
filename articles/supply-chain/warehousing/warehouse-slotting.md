---
title: Noliktavu slotu veidošana
description: Šajā rakstā ir sniegta informācija par noliktavas slotu. Noliktavu slotu veidošana sniedz iespēju konsolidēt pieprasījumu pēc krājuma un mērvienības no pasūtījumiem ar statusu Pasūtīts, Rezervēts vai Izlaists. Tas palīdz noliktavu vadītājiem pārdomāti plānot izdošanas novietojumus, pirms viņi izlaiž pasūtījumus noliktavā un izveido izdošanas darbu.
author: Mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: bb86800f1491e8cb9ad629ed6cc1c76e9393e945
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336041"
---
# <a name="warehouse-slotting"></a>Noliktavu slotu veidošana

[!include [banner](../includes/banner.md)]

Ir pieejami vairāki noliktavas slotu veidošanas līdzekļi, lai palīdzētu noliktavu vadītājiem pārdomāti plānot izdošanas novietojumus, pirms viņi izlaiž pasūtījumus noliktavā un izveido izdošanas darbu.

*Noliktavu slotu veidošanas līdzeklis* sniedz iespēju konsolidēt pieprasījumu pēc krājuma un mērvienības no pasūtījumiem ar statusu *Pasūtīts*, *Rezervēts* vai *Izlaists*. Pēc tam ģenerēto pieprasījumu var lietot novietojumiem, kas tiks izmantoti izdošanai, pamatojoties uz daudzumu, vienību, fiziskām dimensijām, fiksētiem novietojumiem un citām vērtībām. Kad slotu veidošanas plāns ir gatavs, var izveidot papildināšanas darbu, lai katram novietojumam piegādātu atbilstošu krājumu daudzumu.

Līdzeklis *Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem* sniedz iespēju noliktavas vadītājiem papildināt izdošanas vietas, pamatojoties uz pārsūtīšanas pasūtījumiem, kas vēl nav izlaisti uz noliktavu. Tas nodrošina, ka izdošanas vietas ietver visus krājumus, kas ir nepieciešami pārsūtīšanas pasūtījumiem pēc to izlaišanas uz noliktavu. Šim līdzeklim ir nepieciešams, lai tiktu ieslēgts arī līdzeklis *Noliktavas slotu veidošana*.

Līdzeklis *Noliktavas slotu sadalījuma uzlabojumi* pievieno opciju veidnes rindām, ko izmanto līdzeklis *Noliktavas slotu veidošana*. Šī opcija sniedz sistēmai iespēju aplūkot esošos rīcībā esošos krājumus mērķa vietā. Tāpēc slotu veidošanai var ģenerēt mazāk papildinājumu. Līdzeklim *Noliktavas slotu sadalījuma uzlabojumi* ir nepieciešams, lai jūs ieslēgtu arī līdzekli *Noliktavas slotu veidošana*. To pēc izvēles var izmantot kopā ar līdzekli *Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem*.

## <a name="turn-on-the-warehouse-slotting-features"></a>Līdzekļu Noliktavu slotu veidošana ieslēgšana

Pirms šo funkciju lietošanas tās sistēmai ir jāieslēdz. Administratori var izmantot [līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļu statusu un tos ieslēgtu, ja tas nepieciešams. Ieslēgt tālāk minētos līdzekļus pēc vajadzības:

- Noliktavas slotu funkcija
- Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem

    > [!IMPORTANT]
    > Līdzeklim *Noliktavas slotu veidošana* jābūt ieslēgtam pirms šā līdzekļa ieslēgšanas.

- Noliktavas slotu veidošanas sadalījuma uzlabojumi

    > [!IMPORTANT]
    > Līdzeklim *Noliktavas slotu veidošana* jābūt ieslēgtam pirms šā līdzekļa ieslēgšanas.

## <a name="set-up-warehouse-slotting"></a>Noliktavu slotu veidošanas iestatīšana

Lai izmantotu noliktavu slotu veidošanu, sistēmā ir jāiestata tālāk norādītie elementi.

- Slotu veidošanas mērvienību pakāpes
- Direktīvu kodi
- Slotu veidošanas veidnes
- Vietas direktīvas

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Mērvienību pakāpju izveide slotu veidošanai

Mērvienību pakāpes ļauj slotu veidošanas nolūkā kopā grupēt vairākas mērvienības. Piemēram, ja no tā paša kastu izdošanas apgabala tiek izdotas vairāku lielumu kastes, visiem lielumiem var izveidot vienu līmeni. **Katrai mērvienībai, kas būs pakāpes daļa, ir jāizveido rinda.**

1. Atveriet **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Slotu veidošanas mērvienību pakāpes**.
1. Atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Mērvienības pakāpe:** *EaBoxPl*
    - **Apraksts:** *katra kastes palete*

1. Atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Mērvienība** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Vienība:** *kaste*
    - **Apraksts:** atstājiet šo lauku tukšu. Saglabājot izmaiņas, tas tiks automātiski aizpildīts.
    - **Vienības klase:** *daudzums*

1. Atlasiet **Jauns**, lai režģim pievienotu otru rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Vienība:** *ea*
    - **Apraksts:** atstājiet šo lauku tukšu. Saglabājot izmaiņas, tas tiks automātiski aizpildīts.
    - **Vienības klase:** *daudzums*

1. Atlasiet **Jauns**, lai režģim pievienotu trešo rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Vienība:** *PL*
    - **Apraksts:** atstājiet šo lauku tukšu. Saglabājot izmaiņas, tas tiks automātiski aizpildīts.
    - **Vienības klase:** *daudzums*

1. Atlasiet **Saglabāt**, lai saglabātu pakāpi.

### <a name="create-a-directive-code-for-slotting"></a>Slotu veidošanas direktīvas koda izveide

Atlasiet direktīvas kodu, ko saistīt ar veidni.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Direktīvas kodi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Direktīvas kods** ievadiet *Slotu veidošana*.
1. Laukā **Direktīvas apraksts** ievadiet *Slotu veidošana*.

### <a name="set-up-slotting-templates"></a>Noliktavu slotu veidņu iestatīšana

Ar katru slotu veidošanas veidni kontrolē, kā krājumi tiek piešķirti novietojumiem kādai konkrētai noliktavai. Katrā veidnē ir jābūt rindai, kas paredzēta katrai slotu veidošanas specifikācijai. Izmantojiet šajā sadaļā pieejamās procedūras, lai iestatītu slotu veidošanas veidnes.

1. Atveriet **Noliktavas pārvaldība \> Iestatījumi \> Papildināšana \> Slotu veidošanas veidnes**.
1. Atlasiet **Jauns**, lai izveidotu veidni.

Pēc tam ir jāiestata veidnes galvene, slotu veidošanas specifikācijas un novietojumu direktīvas, kā tas ir izskaidrots nākamajās apakšsadaļās. Slotu veidošanas pārsūtīšanas pasūtījumiem iestatījums līdzinās pārdošanas pasūtījumu slotu veidošanas iestatījumam, taču lauks **Pieprasījuma veids** tiek iestatīts uz *Pārsūtīšanas pasūtījumi*, nevis *Pārdošanas pasūtījums*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Pārdošanas pasūtījuma slotu veidošanas veidnes galvenes iestatīšana

1. Veidnes galvenē iestatiet tālāk norādītās vērtības.

    - **Slotu veidošanas veidne:** _61_
    - **Apraksts:** _61_
    - **Pieprasījuma veids:** *pārdošanas pasūtījums*

        > [!NOTE]
        > Pašlaik *Pārdošanas pasūtījumi* un *Pārsūtīšanas pasūtījumi* ir vienīgie pieprasījumu veidi, kas tiek atbalstīti. Varat atlasīt *Pārsūtīšanas pasūtījumus* tikai tad, ja līdzeklis *Noliktavas slotu veidošana pārsūtīšanas pasūtījumiem* ir ieslēgts.

    - **Pieprasījuma stratēģija:** _pasūtīts_

        Šajā laukā ir pieejamas tālāk norādītās vērtības.

        - **Pasūtīts** — pilnībā pasūtīts pārdošanas pasūtījuma daudzums ir uzskatāms par pieprasījumu.
        - **Rezervēts** — par pieprasījumu ir uzskatāmi tikai rezervētie (fiziskie un pasūtītie) pārdošanas pasūtījuma rindas daudzumi.
        - **Izlaists** – izlaistais daudzums ir jāuzskata par pieprasījumu.

    - **Noliktava:** _61_
    - **Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus** — _Jā_

Varat arī norādīt vaicājumu, lai sašaurinātu novērtējamā pieprasījuma apjomu.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Slotu veidošanas specifikāciju iestatīšana katrai veidnei

Katrai pārdošanas pasūtījuma veidnei, ko izveidojat, veiciet tālāk norādītās darbības, lai katrai slotu veidošanas specifikācijai pievienotu rindu.

1. Kopsavilkuma cilnē **Detalizēta informācija par slotu veidošanas veidni** atlasiet **Jauns**, lai izveidotu veidnes rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Secība:** _1_
    - **Apraksts:** _fiksēts novietojums_
    - **Minimālais daudzums:** _1_

        Šajā laukā ir definēts rindai nepieciešamais minimālais pieprasījuma daudzums.

    - **Maksimālais daudzums:** _1000000_

        Šajā laukā ir definēts rindai derīgais maksimālais pieprasījuma daudzums.

    - **Vienība:** atstājiet šo lauku tukšu.

        Šajā laukā ir definēta mērvienība, uz kuru attiecas minimālie un maksimālie daudzumi.

    - **Mērvienības pakāpe:** _EaBoxPl_

        Šajā laukā ir definēts rindai derīgās pieprasījuma mērvienības. (Plašāku informāciju skatiet [Iestatīt mērvienības pakāpes sadaļas slotēšanai](#unit-tiers) iepriekš šajā rakstā.)

    - **Piešķirt slota kritēriju:** _apsvērt daudz._

        Šajā laukā ir pieejamas tālāk norādītās vērtības.

        - **Pieņemt, ka tukšs** — šī sistēma pieņems, ka visi novietojumi izdošanas apgabalā ir tukši un šajos novietojumos nepārbaudīs krājumus.
        - **Apsvērt daudz.**  — sistēma pārbaudīs novietojumus izdošanas apgabalā, meklējot krājumus, un izlaidīs visus novietojumus, kas nebūs tukši.
        - **Apsvērt rīcībā esošo** — sistēmai jāpārbauda, vai mērķa novietojums ietver nerezervētu daudzumu krājumam pieprasījuma rindā. Ja daudzums ir pietiekami liels, lai apmierinātu vismaz vienu pieprasījuma rindas vienību, ģenerētais slotu veidošanas plāna ieraksts tiek samazināts par pieejamo apjomu. Piemēram, ja pieprasījums ir 10 gadījumi un viens gadījums ir rīcībā esošs, tad izvietotais pieprasījums būs deviņi gadījumi. Ja pieprasījums ir 10 gadījumi un katrs gadījums ir rīcībā esošs, tad izvietotais pieprasījums būs 10 gadījumi. Šī vērtība ir pieejama tikai tad, kad ir ieslēgts līdzeklis *Noliktavas slotu veidošanas uzlabojumi*.

    - **Direktīvas kods:** _slotu veidošana_

        Šis lauks nosaka novietojuma direktīvu, kas tiek izmantota, lai atrastu papildināšana darba izdošanas novietojumu.

    - **Pārpildes novietojums:** atstājiet šo lauku tukšu.

        Šis lauks definē novietojumu, kurā tiek novietoti krājumi, ja rindas apstrādes laikā daudzumam nevar atrast novietojumu.

    - **Atļaut palaišanu:** _Jā_

        Ja šai opcijai ir iestatīta vērtība *Jā*, ja katram pieprasījumam nevar izveidot slotu, tiks izveidots kustības darbs, lai izņemtu krājumus no novietojumiem, kuros ir krājumi, bet nekam nav izveidoti sloti. Pēc tam veidne atkal tiek palaista. Šoreiz tā ignorē krājumus novietojumos. Šī funkcija darbojas vislabāk, ja laukam **Piešķirt slota kritēriju** ir iestatīta vērtība _Apsvērt daudz_.

    - **Fiksēta novietojuma lietojums:** _tikai produktam paredzēti fiksēti novietojumi_

        Šajā laukā ir pieejamas tālāk norādītās vērtības.

        - **Fiksēti un nefiksēti novietojumi** — sistēmai nevajadzētu būt ierobežojumam izmantot tikai fiksētus novietojumus.
        - **Tikai produktam paredzēti fiksēti novietojumi** — sistēmai vajadzētu izveidot slotus tikai uz novietojumiem, kas ir produktam paredzēti fiksēti novietojumi.
        - **Tikai produkta variantam paredzēti fiksēti novietojumi** — sistēmai vajadzētu izveidot slotus tikai uz novietojumiem, kas ir produkta variantam paredzēti fiksēti novietojumi.

> [!NOTE]
> Ja slotu veidošanas veidne satur vismaz vienu rindu, kurā lauks **Piešķirt slota kritēriju** ir iestatīts kā *Apsvērt rīcībā esošo*, atļaut papildinājumus vairs nav atļauts nevienai veidnes rindai.

1. Atlasiet **Saglabāt**.
1. Atlasiet **Jauns**, lai izveidotu otro veidnes rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Secība:** _2_
    - **Apraksts:** _Cits_
    - **Minimālais daudz.:** _1_
    - **Maksimālais daudz.:** _1000000_
    - **Vienība:** atstājiet šo lauku tukšu.
    - **Mērvienības pakāpe:** _EaBoxPl_
    - **Piešķirt slota kritēriju:** _apsvērt daudz._
    - **Direktīvas kods:** _slotu veidošana_
    - **Pārpildes novietojums:** atstājiet šo lauku tukšu.
    - **Atļaut palaišanu:** _Jā_
    - **Izmantot fiksētus novietojumus:** _fiksēti un nefiksēti novietojumi_

    Otrajai rindai paredzētajā vaicājumā norādiet kritērijus, kas tiks izmantoti, lai noteiktu, kuriem novietojumiem šai rindai var izveidot pieprasījuma slotu.

1. Atlasiet rindu, kur laukam **Secība** ir iestatīta vērtība *2*.
1. Atlasiet **Rediģēt vaicājumu**.
1. Cilnē **Diapazons** atlasiet **Pievienot**, lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Atvasinātā tabula:** *Vietas*
    - **Lauks:** *Atrašanās vietas profila ID*
    - **Kritēriji:** *Pick-06* (atlasiet dubulto pluszīmi \[**++**\] laukā, lai izvērstu sarakstu, un pēc tam atlasiet *Pick-06* - *6. izdošanas vieta*).

1. Atlasiet **Labi**.

#### <a name="set-up-location-directives"></a>Iestatīt novietojuma direktīvas

Lai atbalstītu slotu veidošanas izdošanas, ir jāiestata vismaz viena novietojuma direktīva. Izmantojiet šajā sadaļā pieejamās procedūras, lai izveidotu jaunu *papildināšanas novietojuma direktīvu* slotu veidošanas izdošanas gadījumiem.

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.
1. Kreisajā rūtī, laukā **Darba pasūtījuma veids** atlasiet *Papildināšana*.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunās novietojuma direktīvas galvenes laukā **Nosaukums** ievadiet *61. slotu veidošanas izdošana*.
1. Laukā **Kārtas numurs** akceptējiet noklusējuma vērtību.

##### <a name="configure-the-location-directives-fasttab"></a>Novietojuma direktīvas kopsavilkuma cilnes konfigurēšana

1. Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Darba veids:** _Izdošana_
    - **Vieta:** _6_
    - **Noliktava:** _61_
    - **Direktīvas kods:** _slotu veidošana_

1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Rindas**.

##### <a name="configure-the-lines-fasttab"></a>Rindu kopsavilkuma cilnes konfigurēšana

1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, lai izveidotu jaunu rindu.
1. Jaunajā rindā iestatiet šādas vērtības.

    - **No daudzuma:** _0_
    - **Līdz daudzumam:** _1 000 000_

1. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.
1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Novietojuma direktīvas darbību kopsavilkuma cilnes konfigurēšana

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai izveidotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Kārtas numurs:** akceptējiet noklusējuma vērtību.
    - **Nosaukums:** _lielapjoma_
    - **Stratēģija:** _Nav_

1. Pieņemiet noklusējuma vērtības atlikušajiem laukiem.
1. Atlasiet **Saglabāt**, lai padarītu pieejamu pogu **Rediģēt vaicājumu**.

##### <a name="edit-the-query"></a>Rediģēt vaicājumu

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.
1. Cilnē **Diapazons** atlasiet **Pievienot**, lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Atvasinātā tabula:** *Vietas*
    - **Lauks:** *Zonas ID*
    - **Kritēriji:** *lielapjoma* (atlasiet dubulto pluszīmi \[**++**\] laukā, lai izvērstu sarakstu, un pēc tam atlasiet *Lielapjoma*.)

1. Atlasiet **Labi**.

## <a name="scenario"></a>Scenārijs

### <a name="set-up-the-scenario"></a>Scenārija iestatīšana

Šim scenārijam izmantojiet iebūvēto datu paraugu un izveidojiet ierakstus, kas ir raksturoti šajā sadaļā.

#### <a name="use-the-usmf-sample-data"></a>USMF datu parauga izmantošana

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/fin-ops/get-started/demo-data.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

#### <a name="create-demand"></a>Pieprasījuma izveide

Izpildiet šīs darbības, lai izveidotu pieprasījumu, kuram lietosit slotu veidošanu.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet _US-007_.
1. Laukā **Noliktava** atlasiet _61_.
1. Atlasiet **Labi**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājums:** _L0101_
    - **Daudzums:** _20_

1. Atlasiet **Pievienot rindu**, lai pievienotu jaunu rindu, un iestatiet šādas vērtības:

    - **Krājums:** _T0100_
    - **Daudzums:** _8_

1. Atlasiet **Saglabāt**.
1. Atlasiet **Jauns**, lai izveidotu otro pārdošanas pasūtījumu.
1. Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet _US-008_.
1. Laukā **Noliktava** atlasiet _61_.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājums:** _T0100_
    - **Daudzums:** _1_

1. Atlasiet **Saglabāt**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Tipiska slotu veidošanas scenārija apskate

Kad visi priekšnosacījuma elementi ir ieviesti, kā tas tika izklāstīts iepriekšējā sadaļā, jūs esat gatavs izmēģināt līdzekli, izpildot katru šajā sadaļā norādīto uzdevumu.

#### <a name="generate-demand"></a>Ģenerēt pieprasījumu

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Slotu veidošanas veidnes** un atlasiet slotu veidošanas veidni, ko izveidojāt iepriekš.
1. Darbību rūtī atlasiet **Ģenerēt pieprasījumu**. Šī komanda novērtē visu pieprasījumu, kas atrodas sistēmā un atbilst slotu veidošanas veidnes vaicājumam. Pēc tam kopējais pieprasījums no visiem pasūtījumiem tiek konsolidēts vienā rindā katram daudzumam/mērvienībai. Kad process ir pabeigts, tiek parādīts informācijas ziņojums.

#### <a name="slotting-demand"></a>Slotu veidošanas pieprasījums

*Slotu veidošanas pieprasījums* parāda pieprasījuma ģenerēšanas rezultātus, pamatojoties uz slotu veidošanas veidnes iestatījumu.

- Darbību rūtī atlasiet **Slotu veidošanas pieprasījums**, lai skatītu rezultātus no komandas **Ģenerēt pieprasījumu**. Slotu veidošanas pieprasījumā esošās rindas var rediģēt. Varat dzēst rindu, pievienot jaunu rindu vai rediģēt detalizētu informāciju par rindu.

> [!NOTE]
> Pieprasījumu varat rediģēt manuāli vai to importēt no ārējās sistēmas, izmantojot datu pārvaldību. Viss, kas būs iekļauts slotu veidošanas pieprasījumā, tiks izmantots nākamajā darbībā neatkarīgi no izcelsmes vietas.

#### <a name="locate-demand"></a>Atrast pieprasījumu

Pēc pieprasījuma ģenerēšanas izmantojiet komandu **Meklēt pieprasījumu**, lai ģenerētu *slotu veidošanas plānu*.

- Darbību rūtī atlasiet **Meklēt pieprasījumu**. Tiek izpildīts slotu veidošanas process. Kad process ir pabeigts, tiek parādīts informācijas ziņojums.

#### <a name="slotting-plan"></a>Slotu veidošanas plāns

Slotu veidošanas plāns rāda novietojumu, kuram tika piešķirts katrs krājums/daudzums, vai tika izmantota pārpilde, izveidots palaišanas darbs un vai tika izmantota veidnes rinda. *Visi pieprasījumi, kuriem nevar izveidot slotu, ir izcelti sarkanā krāsā.*

- Darbību rūtī atlasiet **Slotu veidošanas plāns**, lai skatītu rezultātus.

> [!NOTE]
> - Tagad procesi **Ģenerēt pieprasījumu**, **Izvietot pieprasījumu** un **Palaist papildināšanu** darbojas smilškastē. (Šie procesi ir pieejami no Darbību rūts lapā **Slotu veidošanas veidnes**.)
> - Procesi **Ģenerēt pieprasījumu**, **Izvietot pieprasījumu** un **Palaist papildināšanu** ir aprīkoti ar slēdzeni, lai nodrošinātu, ka tos nevar aktivizēt vienlaicīgi. Pretējā gadījumā izmantotie dati var tikt dzēsti.
> - Procesi **Ģenerēt pieprasījumu** un **Izvietot pieprasījumu** parāda brīdinājumu, ja izpilde neģenerēja ierakstus vai ja ierakstos trūkst informācijas.
> - Kad atlasāt **Slotu veidošanas plāns**, lapas darbību rūtī nav pogu **Jauns** **Rediģēt** vai **Dzēst**, jo datu avotu nevar rediģēt.
> - Kad atlasāt **Palaist papildināšanu**, sistēma validē atlasīto slota veidni un procesus.

#### <a name="create-replenishment"></a>Papildināšana izveide

Pēc slotu veidošanas plāna izveides ir jāizveido *papildināšanas darbs*, pamatojoties uz plānu.

- Darbību rūtī atlasiet **Palaist papildināšanu**. Kad process ir pabeigts, tiek parādīts informācijas ziņojums. Šis ziņojums norāda galveņu skaitu, kas tika izveidotas darba būvējuma ID.

Novietojuma direktīvas, kas tiks izmantotas, ir identificētas, pamatojoties uz katrā veidnes rindā norādīto direktīvas kodu.

## <a name="tips"></a>Padomi

### <a name="set-up-automatic-slotting"></a>Automātiskas slotu veidošanas iestatīšana

Kad visi nepieciešamie elementi ir ieviesti, varat izpildīt tālāk norādītās darbības, lai iestatītu slotu veidošanas automātisku izpildi.

1. Dodieties uz **Noliktavas pārvaldība \> Papildināšana \> Izpildīt slotu veidošanu**.
1. Norādiet izpildāmās slotu veidošanas darbības. Atlasiet vienu vai vairākas no tālāk norādītajām slotu veidošanas darbībām.

    - Ģenerēt pieprasījumu
    - Atrast pieprasījumu
    - Izveidot papildināšanas darbu

    > [!NOTE]
    > Slotu veidošanas darbības ir progresīvas. Ja vēlaties atlasīt *Meklēt pieprasījumu*, vispirms ir jāatlasa *Ģenerēt pieprasījumu*.

1. Norādiet, kura slotu veidošanas veidne ir jāizmanto.
1. Ja vēlaties, varat iestatīt automātisku periodiskuma izpildi.

Scenārijā iekļautajiem uzdevumiem **neiestatiet** automātisku slotu veidošanu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]