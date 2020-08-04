---
title: Izejošā kārtošana
description: Šajā tēmā ir sniegta informācija par izejošo kārtošanu. Šī funkcionalitāte ļauj vieglāk apstrādāt mazus konteinerus un palīdz noliktavas darbiniekiem labāk plānot un organizēt palešu skaitu kravas automašīnā.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e72249e26fb8f291f804cf5f2e4ce98bf88cd5bf
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596252"
---
# <a name="outbound-sorting"></a>Izejošā kārtošana

[!include [banner](../includes/banner.md)]

Šī funkcionalitāte ļauj vieglāk apstrādāt mazus konteinerus un palīdz noliktavas darbiniekiem labāk plānot un organizēt palešu skaitu kravas automašīnā. Izmantojot izejošo kārtošanu, varat kārtot iepakotos konteinerus pareizajā paletē pēc tam, kad tie bijuši iepakošanas stacijā. Varat veidot arī iepakošanas hierarhiju.

Šī funkcionalitāte ļauj veidot paletes no konteineriem, kas iepakoti, izmantojot iepakošanas funkcionalitāti. Konteiners netiek sūtīts uz galējo nosūtīšanas vietu, kā tas ir sākotnējā iepakošanas plūsmā. Tā vietā darbinieki var slēgt konteineru un pārvietot to uz kārtošanas veida vietu. Pēc tam konteinerus var kārtot pozīcijās, kur katrā no tām ir noliktavas vienība (LP). Kad konteineri ir sašķiroti, var izveidot darbu, lai nosūtītu visu LP uz galējo nosūtīšanas doku vai sagatavošanas vietām, balstoties uz novietojuma direktīvām vai jūsu vajadzībām. Turklāt kārtošanas pozīcijas slēgšanas darbība var nekavējoties pārvietot krājumus uz galīgo nosūtīšanas vietu un izdot to pasūtījumam.

## <a name="turn-on-the-outbound-sorting-feature"></a>Ieslēgt līdzekli Izejošā kārtošana

Lai varētu izmantot līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Izejošā kārtošana*

## <a name="setup"></a>Iestatīt

Šim scenārijam ir jāizmanto standarta **USMF** demonstrācijas dati un noliktava *62*. Kā arī ir jāpabeidz iestatīšana, kas aprakstīta nākamajās apakšsadaļās.

### <a name="set-up-a-wave-template"></a>Iestatiet kopuma veidni

Šis iestatījums automātiski apstrādā kopumu un izveido darbu, kad rinda tiek nodotas izpildei noliktavā.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Veidņu sarakstā atlasiet **62. noliktava**.
1. Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, ka opcija **Apstrādāt kopumu, to pārvietojot uz noliktavu** ir iestatīts uz *Jā*.

### <a name="set-up-a-worker"></a>Darbinieka iestatīšana

Iepakošanas stacija tiek uzskatīta par atrašanās vietu. Noliktavas darbinieki, kuri piesakās iepakošanas stacijā, redz un strādā tikai ar sūtījumiem un konteineriem, kas ir paredzēti noteiktai iepakošanas vietai. Lietotājs, kurš piesakās Microsoft Dynamics 365, ir jāiestata kā darbinieks Noliktavas pārvaldībā. Ja lietotāja vārds neparādās darba lietotāju sarakstā, izmantojiet nākamo procedūru, lai to pievienotu.

> [!NOTE]
> Šīs darbības pieņem, ka lietotājs jau ir sistēmā un ir saistīts ar darbinieku vai nodarbināto modulī **Human Resources**.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.
1. Atlasiet **Jauns**.
1. Laukā **Nodarbinātais** atlasiet mērķa lietotāju darbinieku sarakstā.
1. Atlasiet **Atlasīt**.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Lietotāji** atlasiet **Jauns**, lai izveidotu mobilās ierīces kontu, un iestatiet tālāk norādītās vērtības:

    - **Lietotāja ID:** ievadiet unikālu ID.
    - **Lietotājvārds:** ievadiet ID nosaukumu.
    - **Noklusējuma noliktava:** *62*
    - **Izvēlnes nosaukums:** *Galvenā*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Tiek parādīts dialoglodziņš **Iestatīt paroli**, kur varat izveidot vienkāršu paroli, ko lietotājs var izmantot, lai pieteiktos mobilajā programmā. Iestatiet šādas vērtības:

    - **Parole:** ievadiet vienkāršu paroli.
    - **Apstiprināt paroli:** vēlreiz ievadiet to pašu paroli.

1. Atlasiet **Iestatīt paroli**.

    Paziņojums darbību centrā informē, ka jūsu izveidotajam lietotājam ir iestatīta parole.

### <a name="create-a-location-type"></a>Novietojuma veida izveide

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma veidi**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojuma veidu, un iestatiet šādas vērtības:

    - **Novietojuma veids:** *SORT*
    - **Apraksts:** *Kārtot*

1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-warehouse-management-parameters"></a>Noliktavas pārvaldības parametru iestatīšana

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.
1. Cilnē **Vispārīgi**, kopsavilkuma cilnē **Novietojuma veidi** iestatiet lauku **Kārtošanas novietojuma veids** uz *SORT*.
1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-a-location-profile"></a>Novietojuma profila iestatīšana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Novietojuma profila ID:** *Sorting*
    - **Nosaukums:** *Kārtošana*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Novietojuma formāts:** *ASRB* (aile-statīvs-plaukts-nodalījums)
    - **Novietojuma veids:** *SORT*
    - **Izmantot noliktavas vienības izsekošanu:** *Jā*
    - **Atļaut jauktus krājumus:** *Jā* (iestatot šo opciju uz *Jā*, opcija **Atļaut jauktu krājumu partijas** tiek automātiski iestatīta uz *Jā*, un to nevar mainīt atsevišķi.)

1. Atlasiet **Saglabāt**.

### <a name="set-up-a-location"></a>Novietojuma iestatīšana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojums**.
1. Virsrakstā noņemiet atzīmi izvēles rūtiņai **Ģenerēt novietojuma kontrolciparus**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu novietojumu, un iestatiet šādas vērtības:

    - **Noliktava:** *62*
    - **Novietojums:** *SORT*
    - **Novietojuma profila ID:** *SORTING*

1. Atlasiet **Saglabāt**.

### <a name="set-up-an-outbound-sorting-template"></a>Izejošās kārtošanas veidnes iestatīšana

Izejošās kārtošanas veidne nosaka, vai darbs ir izveidots no kārtošanas vietas un vai kārtošana tiek veikta manuāli vai automātiski.

Šim scenārijam ir jāizveido izejošās kārtošanas veidne, lai pēc iepakošanas stacijas, veidotu paletes.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Izejošās kārtošanas veidne**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunās veidnes galvenē iestatiet tālāk norādītās vērtības:

    - **Izejošās kārtošanas veidnes ID:** *AutoWork*
    - **Apraksts:** *Automātiska darba izveide*
    - **Izejošās kārtošanas veidnes veids:** *Konteiners*
    - **Noliktava:** *62*
    - **Novietojums:** *SORT*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Kārtošanas pārbaude:** *Pozīcijas skenēšana*.
    - **Izveidot darbu slēgtai pozīcijai:** *Jā*

        Ja šī opcija ir iestatīta uz *Jā*, kad pozīcija tiek slēgta, tiks izveidots darbs, lai pārvietotu krājumus uz galējo nosūtīšanas vietu. Ja tā ir iestatīta uz *Nē*, krājumi tiks nekavējoties izdoti pasūtījumam, kad pozīcija tiks slēgta.

    - **Pozīcijas piešķiršana:** *Automātiski*

        Ja šajā laukā ir iestatīts *Manuāli*, lietotājam vienmēr jānorāda, kurā pozīcijā krājumi ir jākārto. Ja tajā ir iestatīts *Automātiski*, sistēma automātiski novirzīs krājumus uz pozīciju, kad vien iespējams, pamatojoties uz kārtošanas veidnes pārtraukumiem.

1. Atlasiet **Saglabāt**, lai darbību rūtī padarītu pieejamu pogu **Rediģēt vaicājumu**.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora cilnē **Kārtošana** pievienojiet rindu, kurai ir šādas vērtības:

    - **Tabula:** *Sūtījumi*
    - **Atvasinātā tabula:** *Sūtījumi*
    - **Lauks:** *Pārvadātāja pakalpojums*

        Kad vērtības ir atlasītas, iespējams, tiks parādīts šāds ziņojums: “Lauks Pārvadātāja pakalpojums nav indeksa lauks. Vai šim vēlaties pievienot kārtošanu?” Atlasiet **Jā**.

    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**.
1. Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?” Atlasiet **Jā**.

    Tagad darbību rūtī ir pieejama poga **Izejošās kārtošanas veidnes pārtraukumi**.

1. Darbību rūtī atlasiet **Izejošās kārtošanas veidnes pārtraukumi**.
1. Dialoglodziņā **Izejošās kārtošanas kritēriji** iestatiet šādas vērtības:

    - **Atsauces tabulas nosaukums:** *Sūtījumi*
    - **Atsauces lauka nosaukums:** *Pārvadātāja pakalpojums*
    - **Grupēt pēc lauka:** atzīmējiet šo izvēles rūtiņu, lai grupētu sūtījumus pēc pārvadātāja pakalpojuma.

1. Atlasiet **Labi**, lai iestatījumus saglabātu un aizvērtu dialoglodziņu.

### <a name="set-up-container-packing-policies"></a>Konteineru iepakošanas politiku iestatīšana

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru iepakošanas politikas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunās politikas galvenē iestatiet tālāk norādītās vērtības:

    - **Konteineru iepakošanas politika:** *Sort*
    - **Apraksts:** *Kārtot*

1. Kopsavilkuma cilnē **Pārskats** iestatiet šādas vērtības:

    - **Noliktava:** *62*
    - **Kārtošanas noklusējuma novietojums:** *SORT*
    - **Svara vienība:** *kg*
    - **Konteineru slēgšanas politika:** *Automātiska izlaide*
    - **Konteineru izlaides politika:** *Piešķirt konteineru izejošās kārtošanas pozīcijai*

1. Atlasiet **Saglabāt**.

### <a name="set-up-packing-profiles"></a>Iepakošanas profilu iestatīšana

Izveidojiet jaunu iepakošanas profilu, kas tiks izmantots kopā ar kārtošanas funkcionalitāti.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Iepakošana \> Iepakošanas profili**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu rindu, un iestatiet tai šādas vērtības:

    - **Iepakošanas profila ID:** *Sort*
    - **Apraksts:** *Kārtot*
    - **Konteineru iepakošanas politika:** *Sort*
    - **Konteinera ID režīms:** *Automātiski*
    - **Konteinera veids:** *Kaste - liela*
    - **Konteinera slēgšanas laikā automātiski izveidot konteineru:** notīrīts (= *Nē*)

1. Atlasiet **Saglabāt**.

### <a name="set-up-work-classes"></a>Darba klašu iestatīšana

Iestatiet darba klasi, kas tiks izmantota kopā ar kārtošanu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu kārtošanas darba klasi, un iestatiet tai šādas vērtības:

    - **Darba klases ID:** *Sort*
    - **Apraksts:** *Kārtot*
    - **Darba pasūtījuma veids:** *Kārtotu krājumu izdošana*

1. Atlasiet **Saglabāt**.

### <a name="set-up-mobile-device-menu-items"></a>Mobilās ierīces izvēlnes vienumu iestatīšana

#### <a name="set-up-a-new-pallet-menu-item"></a>Jaunas paletes izvēlnes vienuma iestatīšana

Izveidojiet mobilās ierīces izvēlnes vienumu, lai veidotu paletes kārtošanas laikā.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Paletes izveide*
    - **Nosaukums:** *Paletes izveide*
    - **Režīms:** *Netiešs*
    - **Izmantot esošo darbu:** *Nē*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Aktivitātes kods:** *Izejošā kārtošana*

        Kad šis lauks ir iestatīts uz *Izejošā kārtošana*, tiek parādīts lauks **Izejošās kārtošanas veidnes ID**.

    - **Procesu ceļveža izmantošana:** *Jā*

        Kad lauks **Aktivitātes kods** ir iestatīts uz *Izejošā kārtošana*, šī opcija tiek automātiski iestatīta uz *Jā*.

    - **Izejošās kārtošanas veidnes ID:** *AutoWork*

1. Atlasiet **Saglabāt**.

#### <a name="set-up-a-new-loading-menu-item"></a>Jaunas iekraušanas izvēlnes vienuma iestatīšana

Izveidojiet izvēlnes vienumu, kas ļauj lietotājiem pārvietot sakārtotās krājuma vienības uz nosūtīšanas vietu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Load from Sorting*
    - **Nosaukums:** *Ielādēt no kārtošanas*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Jā*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noteicējs:** uz *Lietotāja noteikts*.
1. Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:

    - **Darba klases ID:** *SORT*
    - **Darba pasūtījuma veids:** *Kārtotu krājumu izdošana*

1. Atlasiet **Saglabāt**.

### <a name="set-up-the-mobile-device-menu"></a>Mobilās ierīces izvēlnes iestatīšana

Tagad mobilās ierīces izvēlnei ir jāpievieno jauni izvēlnes vienumi.

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Atlasiet izvēlni **Izejošais**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kolonnā **Pieejamās izvēlnes un izvēļņu elementi** meklējiet un atlasiet **Paletes izveide**.
1. Atlasiet bultiņas pa labi pogu, lai pārvietotu **Paletes izveide** uz kolonnu **Izvēlnes struktūra**.
1. Izmantojiet bultiņas uz augšu un uz leju, lai izvēlnes vienumu **Paletes izveide** novietotu vēlamajā pozīcijā mobilās ierīces izvēlnē.
1. Atlasiet **Saglabāt**.
1. Atkārtojiet šo procedūru, lai pievienotu izvēlnes vienumu **Ielādēt no kārtošanas** izvēlnei **Izejošs**.

### <a name="set-up-location-directives"></a>Iestatīt novietojuma direktīvas

*Novietojuma direktīvas* ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai. Tagad ir jāizveido kārtula, lai pārvaldītu kārtošanas darbu.

#### <a name="set-up-a-single-sku-directive"></a>Iestatīt vienu SKU direktīvu

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Kreisajā rūtī mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kārtotu krājumu izdošana*.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Secība:** *1*
    - **Nosaukums:** *Baydoor*

1. Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības:

    - **Darba veids:** *Izvietošana*
    - **Vieta:** *6*
    - **Noliktava:** *62*
    - **Vairākas SKU:** *Nē*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Rindas**.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Secība:** *1*
    - **No:** *0*
    - **Līdz:** *1 000 000*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Novietojuma direktīvu darbības**.
1. Kopsavilkuma cilnē **Novietojuma direktīvu darbības** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Secība:** *1*
    - **Nosaukums:** *Baydoor*

1. Atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora cilnē **Diapazons** sameklējiet rindu, kurā lauks **Lauks** ir iestatīts uz *Novietojums*. Iestatiet lauku **Kritēriji** šai rindai uz *Angāra durvis*.
1. Atlasiet **Labi**, lai saglabātu iestatījumus un aizvērtu vaicājumu redaktoru.

#### <a name="set-up-a-multiple-sku-directive"></a>Iestatīt vairākas SKU direktīvas

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Kreisajā rūtī mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kārtotu krājumu izdošana*.
1. Darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Secība:** *2*
    - **Nosaukums:** *Baydoor Multi*

1. Kopsavilkuma cilnē **Novietojuma direktīvas** iestatiet tālāk norādītās vērtības:

    - **Darba veids:** *Izvietošana*
    - **Vieta:** *6*
    - **Noliktava:** *62*
    - **Vairākas SKU:** *Jā*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Rindas**.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Secība:** *1*
    - **No:** *0*
    - **Līdz:** *1 000 000*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu rīkjoslu kopsavilkuma cilnē **Novietojuma direktīvu darbības**.
1. Kopsavilkuma cilnē **Novietojuma direktīvu darbības** atlasiet **Jauns**, un pēc tam jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

    - **Secība:** *1*
    - **Nosaukums:** *Baydoor Multi*

1. Atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora cilnē **Diapazons** sameklējiet rindu, kurā lauks **Lauks** ir iestatīts uz *Novietojums*. Iestatiet lauku **Kritēriji** šai rindai uz *Angāra durvis*.
1. Atlasiet **Labi**, lai saglabātu iestatījumus un aizvērtu vaicājumu redaktoru.

### <a name="set-up-work-templates"></a>Iestatīt darba veidnes

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Mainiet lauka **Darba pasūtījuma veids** vērtību uz *Kārtotu krājumu izdošana*.
1. Lai izveidotu darba veidni, darbību rūtī atlasiet **Jauns**.
1. Cilnē **Pārskats** iestatiet šādas vērtības:

    - **Secība:** *1*
    - **Darba veidne:** *Sort*
    - **Darba veidnes apraksts:** *Kārtot*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Darba veidnes informācija**.
1. Kopsavilkuma cilnē **Darba veidnes informācija** atlasiet **Jauns**, lai pievienotu rindu, un pēc tam iestatiet tai šādas vērtības:

    - **Darba veids:** *Izdošana*
    - **Darba klases ID:** *SORT*

1. Vēlreiz atlasiet **Jauns**, lai pievienotu otro rindu, un tad iestatiet tai šādas vērtības:

    - **Darba veids:** *Izvietošana*
    - **Darba klases ID:** *SORT*

1. Atlasiet **Saglabāt**.

## <a name="scenario"></a>Scenārijs

Šis scenārijs simulē situāciju, kad iepakotie konteineri tiek automātiski kārtoti dažādām pozīcijām (paletēm) pēc iepakošanas stacijas, atkarībā no sūtījuma pārvadātāja pakalpojuma. Pēc tam, kad visi noslodzes krājumi ir iepakoti un sakārtoti pēc adreses, paletes tiks pārvietotas uz angāra durvīm.

### <a name="create-sales-orders-and-picking-work"></a>Pārdošanas pasūtījuma un izdošanas darba izveide

#### <a name="create-sales-order-1"></a>1. pārdošanas pasūtījuma izveide

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-005*
    - **Noliktava:** *62*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

    Jaunais pārdošanas pasūtījums ir atvērts.

1. Pārejiet uz skatu **Galvene**.
1. Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.

    - **Sūtījuma pārvadātājs:** *Kravas lidmašīnas*
    - **Pārvadātāja pakalpojums:** *Gaisa*

1. Pārejiet uz skatu **Rindas**.
1. Ja jauna, tukša rinda netiek automātiski pievienota režģim, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai to pievienotu.
1. Jaunajā pasūtījuma rindā iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *2*

1. Kamēr jaunā pasūtījuma rinda joprojām ir atlasīta, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**, izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.
1. Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums. Pierakstiet kopuma ID un sūtījuma ID numurus.

#### <a name="sales-order-2"></a>2. pārdošanas pasūtījums

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-006*
    - **Noliktava:** *62*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Šajā pasūtījuma rindā iestatiet šādas vērtības:

    - **Krājums:** *A0001*
    - **Daudzums:** *1*

1. Kopsavilkuma cilnē **Rindas informācija**, cilnē **Piegāde** iestatiet lauku **Piegādes režīms** uz *Flowe-STD*.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, un pēc tam otrajā pasūtījuma rindā iestatiet šādas vērtības:

    - **Krājums:** *A0002*
    - **Daudzums:** *1*

1. Kopsavilkuma cilnē **Rindas informācija**, cilnē **Piegāde** mainiet vērtību laukam **Piegādes režīms** uz *Air C-Air*.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet pirmo pasūtījuma rindu. Tad izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet otro pasūtījuma rindu. Tad izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.
1. Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums. Ievērojiet, ka ir izveidoti divi kopuma ID numuri un divi sūtījuma ID numuri, viens katram piegādes režīmam pārdošanas pasūtījumu rindām.

#### <a name="get-the-work-ids-from-the-work-details"></a>Darba ID iegūšana no darba informācijas

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Lapā tiek rādīti no pārdošanas pasūtījumiem izveidotie darba ID. Izmantojiet kopuma ID un sūtījuma ID no izveidotajiem pārdošanas pasūtījumiem, lai atrastu darba ID katram kopumam un sūtījumam. Pierakstiet šos darba ID, jo tie būs vajadzīgi nākamajās darbībās. Ievērojiet, ka otrajam pārdošanas pasūtījumam ir izveidoti divi darba ID. Ja dažādi krājumi tiek izdoti no dažādām vietām, tiek ģenerēti atsevišķi darba ID.

### <a name="pick-items-for-the-sales-orders"></a>Krājumu izdošana pārdošanas pasūtījumiem

Pabeidziet izveidoto darbu, izmantojot mobilo ierīci, lai pārvietotu krājumus uz iepakošanas staciju.

1. Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Pārdošanas izdošana**.
1. Laukā **ID** ievadiet darba ID, kas tika izveidots 1. pārdošanas pasūtījumam.
1. Atlasiet **Labi**.
1. Lapā **Pārdošanas pasūtījumi - izdošana**, ievadiet mērķa LP, kas tika izveidots 1. pārdošanas pasūtījumam. Ievērojiet, ka tiek rādīta izdošanas vieta (*bulk-001*), krājums (*A0001*) un daudzums (*2 gab.*).
1. Atlasiet **Labi**.
1. Pārskatiet informāciju lapā **Pārdošanas pasūtījumi - izvietošana**. Laukam **Vieta** ir jānorāda, ka izdotie krājumi ir jānosūta uz atrašanās vietu *Iepakot*.
1. Atlasiet **Labi**.

    Lapā **Skenēt darba ID / noliktavas vienības ID** tiek saņemts ziņojums “Darbs pabeigts”, norādot, ka darba ID no 1. pārdošanas pasūtījuma ir pabeigts.

    Tagad tiks izdots 2. pārdošanas pasūtījums.

1. Laukā **ID** ievadiet darba ID, kas tika izveidots 2. pārdošanas pasūtījumam, kur 1. rindai ir krājums *A0001*.
1. Atlasiet **Labi**.
1. Lapā **Pārdošanas pasūtījumi - izdošana** ievadiet mērķa LP. Ievērojiet, ka tiek rādīta izdošanas vieta (*bulk-001*), krājums (*A0001*) un daudzums (*1 gab.*).
1. Atlasiet **Labi**.
1. Pārskatiet informāciju lapā **Pārdošanas pasūtījumi - izvietošana**. Laukam **Vieta** ir jānorāda, ka izdotie krājumi ir jānosūta uz atrašanās vietu *Iepakot*.
1. Atlasiet **Labi**.

    Lapā **Skenēt darba ID / noliktavas vienības ID** tiek saņemts ziņojums “Darbs pabeigts”. Šis ziņojums norāda, ka 2. pārdošanas pasūtījuma 1. rindas darba ID ir pabeigts.

1. Laukā **ID** ievadiet darba ID, kas tika izveidots 2. pārdošanas pasūtījumam, kur 2. rindai ir krājums *A0002*.
1. Atlasiet **Labi**.
1. Lapā **Pārdošanas pasūtījumi - izdošana** ievadiet mērķa LP. Ievērojiet, ka tiek rādīta izdošanas vieta (*bulk-002*), krājums (*A0001*) un daudzums (*1 gab.*).
1. Atlasiet **Labi**.
1. Pārskatiet informāciju lapā **Pārdošanas pasūtījumi - izvietošana**. Laukam **Vieta** ir jānorāda, ka izdotie krājumi ir jānosūta uz atrašanās vietu *Iepakot*.
1. Atlasiet **Labi**.

    Lapā **Skenēt darba ID / noliktavas vienības ID** tiek saņemts ziņojums “Darbs pabeigts”. Šis ziņojums norāda, ka 2. pārdošanas pasūtījuma 2. rindas darba ID ir pabeigts.

### <a name="pack-sales-orders-into-containers"></a>Pārdošanas pasūtījumu iepakošana konteineros

#### <a name="pack-sales-order-1-into-containers"></a>1. pārdošanas pasūtījuma iepakošana konteineros

1. Dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Iepakot**.

    Tiek parādīts dialoglodziņš **Atlasīt iepakošanas staciju**. Pēc noklusējuma lauks **Darbinieks** ir jāiestata uz tā darbinieka vārda, ko iestatījāt iepriekš.

1. Iestatiet šādas vērtības, lai skatītu un strādātu ar sūtījumiem un konteineriem, kas ir paredzēti noteiktai iepakošanas vietai:

    - **Vieta:** *6*
    - **Noliktava:** *62*
    - **Atrašanās vieta:** *Pakotne*
    - **Iepakošanas profila ID:** *Sort*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Lapas **Pakotne** laukā **Noliktavas vienība vai sūtījums**, ievadiet mērķa LP 1. pārdošanas pasūtījumam. Pēc tam atlasiet klaviatūras taustiņu **Cilne** vai **Ievadīt**, lai izietu no lauka.
1. Darbību rūtī atlasiet **Jauns konteiners**.
1. Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**. Pierakstiet konteinera ID.
1. Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:

    - **Daudzums:** *1*
    - **Identifikators:** krājums *A0001*

1. Darbību rūtī atlasiet **Slēgt konteineru**.
1. Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.
1. Atlasiet **Labi**. Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.
1. Izveidojiet otru konteineru, lai pievienotu otro krājumu, no LP 1. pārdošanas pasūtījuma uz jauno konteineru.
1. Darbību rūtī atlasiet **Jauns konteiners**.
1. Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**. Pierakstiet konteinera ID.
1. Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:

    - **Daudzums:** *1*
    - **Identifikators:** krājums *A0001*

1. Darbību rūtī atlasiet **Slēgt konteineru**.
1. Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.
1. Atlasiet **Labi**. Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.

#### <a name="pack-sales-order-2-into-containers"></a>2. pārdošanas pasūtījuma iepakošana konteineros

1. Lapas **Pakotne** laukā **Noliktavas vienība vai sūtījums**, ievadiet mērķa LP 2. pārdošanas pasūtījuma 1. rindai. Pēc tam atlasiet klaviatūras taustiņu **Cilne** vai **Ievadīt**, lai izietu no lauka.
1. Darbību rūtī atlasiet **Jauns konteiners**.
1. Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**. Pierakstiet konteinera ID.
1. Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:

    - **Daudzums:** *1*
    - **Identifikators:** krājums *A0001*

1. Darbību rūtī atlasiet **Slēgt konteineru**.
1. Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.
1. Atlasiet **Labi**. Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.
1. Laukā **Noliktavas vienība vai sūtījums**, ievadiet mērķa LP 2. pārdošanas pasūtījuma 2. rindai. Pēc tam atlasiet klaviatūras taustiņu **Cilne** vai **Ievadīt**, lai izietu no lauka.
1. Darbību rūtī atlasiet **Jauns konteiners**.
1. Pieņemiet visus noklusējuma iestatījumus un atlasiet **Labi**. Pierakstiet konteinera ID.
1. Kopsavilkuma cilnē **Krājuma iepakošana** iestatiet šādas vērtības:

    - **Daudzums:** *1*
    - **Identifikatora lauks:** krājums *A0002*

1. Darbību rūtī atlasiet **Slēgt konteineru**.
1. Dialoglodziņā **Slēgt konteineru** atlasiet **Iegūt sistēmas svaru**, lai sistēma atjauninātu lauku **Bruto svars**.
1. Atlasiet **Labi**. Konteiners ir pārvietots uz novietni *SORT* un ir gatavs kārtošanai.

Lai skatītu konteineru informāciju, dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Konteineri** un meklējiet konteineru ID, kas tika izveidoti iepakošanas laikā.

### <a name="sort-the-containers"></a>Konteineru kārtošana

> [!IMPORTANT]
> Kad piekļūstat izvēlnes vienumam **Paletes izveide** mobilajā programmā, lai veiktu izejošo kārtošanu, tiks parādīta poga, kas ir apzīmēta kā **Pilns**. *Nelietojiet pogu **Pilns**, lai kārtotu vai slēgtu pozīciju.*
>
> Poga **Pilns** tiek nodrošināta pēc noklusējuma, un to nevar atspējot vai noņemt no lapas. To nelieto funkcijai *Izejošā kārtošana*.

#### <a name="sort-the-first-container"></a>Pirmā konteinera kārtošana

1. Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Paletes izveide**.
1. Laukā **LP/Con** ievadiet pirmā konteinera ID, kas ir saistīts ar 1. pārdošanas pasūtījumu.
1. Atlasiet **Labi**.
1. Tā kā pašlaik nav kārtošanas pozīciju, tā ir jānorāda. Laukā **Kārtošanas pozīcijas ID** ievadiet *SP01*.
1. Tā kā neviena LP pašlaik nav saistīta ar kārtošanas pozīciju *SP01*, tā ir jānorāda. Laukā **LP** ievadiet *PLP01*.
1. Atlasiet **Labi**.
1. Tā kā ir ieslēgta kārtošanas pozīcijas pārbaude, jums vēlreiz ir jāievada kārtošanas pozīcijas ID. Laukā **Kārtošanas pozīcijas ID** ievadiet *SP01*.
1. Atlasiet **Labi**.

    Tiek saņemts ziņojums “Darbs pabeigts”.

> [!TIP]
> Lai skatītu kārtošanas pozīciju un tajā iekļauto LP, dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Izejošās kārtošanas pozīciju piešķires**.
>
> Lapā **Izejošās kārtošanas pozīciju piešķires** tiek parādītas visas šobrīd aktīvās kārtošanas pozīcijas. Lauks **Kārtošanas pozīcijas transakcijas** parāda ar katru kārtošanas pozīciju saistīto LP un konteinerus, kas ir kārtošanas pozīcijā. Ievērojiet, ka pašlaik pastāv viena kārtošanas pozīcija un ka kopsavilkuma cilne **Kārtošanas pozīcijas kritēriji** parāda kritērijus **Sūtījums – Pārvadātāja pakalpojums – Gaisa**.

#### <a name="sort-the-remaining-containers"></a>Atlikušo konteineru kārtošana

1. Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Paletes izveide**.
1. Laukā **LP/Con** ievadiet otrā konteinera ID, kas ir saistīts ar 1. pārdošanas pasūtījumu.
1. Atlasiet **Labi**. Tā kā kārtošanas veidne ir iestatīta automātiskai kārtošanai un kārtošanas pozīcija ar atbilstošajiem kritērijiem jau pastāv, jūs automātiski tiekat novirzīts uz pareizo kārtošanas pozīciju.
1. Atlasiet **Labi**.
1. Apstipriniet kārtošanas pozīcijas ID, norādot, ka krājumi ir pareizajā vietā. Laukā **Kārtošanas pozīcijas ID** ievadiet *SP01*.
1. Atlasiet **Labi**.

    1. pārdošanas pasūtījuma otrā konteinera darbs ir pabeigts. Tagad tiks šķiroti atlikušie konteineri no 2. pārdošanas pasūtījuma.

1. Laukā **LP/Con** ievadiet konteinera ID no 2. pārdošanas pasūtījuma konteinera, kas satur krājumu *A0001*. Tā kā pārvadātāja pakalpojums ir atšķirīgs, tiek parādīta uzvedne ievadīt jaunu kārtošanas pozīciju un piešķirt šai pozīcijai LP. Izmantojiet kārtošanas pozīciju *SP02* un LP *PLP02*.
1. Atlasiet **Labi**.
1. Apstipriniet kārtošanas pozīciju, laukā **Kārtošanas pozīcijas ID** ievadot *SP02*.
1. Atlasiet **Labi**.

    Konteinera darbs ir pabeigts.

1. Laukā **LP/Con** ievadiet konteinera ID 2. pārdošanas pasūtījuma atlikušajam konteineram, kas satur krājumu *A0002*. Tā kā pārvadātāja pakalpojums ir tāds pats kā pārvadātāja pakalpojums 1. pārdošanas pasūtījumam, sistēma parāda esošo kārtošanas pozīciju ar atbilstošajiem kritērijiem.
1. Atlasiet **Labi**.
1. Apstipriniet kārtošanas pozīciju, laukā **Kārtošanas pozīcijas ID** ievadot *SP01*.
1. Atlasiet **Labi**.

    Konteinera darbs ir pabeigts.

### <a name="close-the-outbound-sorting-positions"></a>Slēgt izejošās kārtošanas pozīcijas

Kad visi krājumi ir sakārtoti, pozīcija ir jāslēdz, lai varētu izveidot darbu. Tiks izveidots kārtots krājumu izdošanas darbs, lai veiktu inventarizāciju angāra durvīm.

#### <a name="close-a-position-from-the-mobile-device"></a>Pozīcijas slēgšana no mobilās ierīces

1. Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Paletes izveide**.
1. Laukā **LP/Con** ievadiet kārtotā konteinera ID kārtošanas pozīciju *SP01*.
1. Atlasiet **Labi**.
1. Tiek parādīts šāds ziņojums: “Konteiners jau ir sakārtots pēc pozīcijas SP01. Vai slēgt pozīciju?” Atlasiet **Aizvērt**.

    Darbs ir pabeigts.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Pozīcijas slēgšana no izejošās kārtošanas pozīcijas piešķirēm

1. Dodieties uz **Noliktavas pārvaldība \> Iepakošana un konteinerizēšana \> Izejošās kārtošanas pozīciju piešķires**.
1. Kreisajā kolonnā atlasiet **SP02**. Šī izejošās kārtošanas pozīcijas rinda ir tā, kuru slēgsit.
1. Darbību rūtī atlasiet **Slēgt pozīciju**. Kārtošanas pozīcijas ieraksts ir slēgts un vairs netiek rādīts.

    > [!TIP]
    > Lai tiktu rādīti visi slēgtie pozīciju ieraksti, atzīmējiet izvēles rūtiņu **Rādīt slēgto**.

### <a name="sorted-inventory-picking"></a>Kārtoto krājumu izdošana

Pabeidziet kārtoto krājumu izdošanas darbu. Kad tas ir pabeigts, krājumi tiks izdoti pārdošanas pasūtījumam. Šajā brīdī tiek lietoti visi pārējie noliktavas procesi.

1. Mobilajā ierīcē piesakieties noliktavā *62*, izmantojot lietotāja ID, ko izveidojāt šim scenārijam (vai esoša demonstrācijas datu lietotāja ID).
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Ielādēt no kārtošanas**.
1. Ievadiet mērķa LP ID no pirmās kārtošanas pozīcijas, *SP01*. Iestatiet lauku **ID** uz *PLP01*.
1. Atlasiet **Labi**.
1. Lapā **Kārtoto krājumu izdošana: Izdot** tiek rādīts veicamais izdošanas darbs. Izdot no novietojuma *SORT* un mērķa LP *PLP01*, kam ir vairāki krājumi un daudzums ir *3*.
1. Atlasiet **Labi**.
1. Lapā **Kārtoto krājumu izdošana: Izvietot** tiek rādīts veicamais izvietošanas darbs. Izvietot novietojumā *Baydoor* un mērķa LP *PLP01*, kam ir vairāki krājumi un daudzums ir *3*.
1. Atlasiet **Labi**.

    Darbs ir pabeigts.

1. Ievadiet mērķa noliktavas vienības ID no otrās kārtošanas pozīcijas, *SP02*. Iestatiet lauku **ID** uz *PLP02*.
1. Atlasiet **Labi**.
1. Lapā **Kārtoto krājumu izdošana: Izdot** tiek rādīts veicamais izdošanas darbs. Izdot no novietojuma *SORT* un mērķa LP *PLP02*, kam ir vairāki krājumi un daudzums ir *1*.
1. Atlasiet **Labi**.
1. Lapā **Kārtoto krājumu izdošana: Izvietot** tiek rādīts veicamais izvietošanas darbs. Izvietot novietojumā *Baydoor* un mērķa LP *PLP02*, kam ir vairāki krājumi un daudzums ir *1*.
1. Atlasiet **Labi**.

    Darbs ir pabeigts.

No šī brīža tiek lietoti visi pārējie noliktavas procesi.
