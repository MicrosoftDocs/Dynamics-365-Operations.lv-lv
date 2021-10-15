---
title: Konteinera iepakošanas stratēģijas
description: Šajā tēmā aprakstītas atšķirības starp konteinera iepakošanas stratēģiju un sniegti piemēri.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4e5faf8e4544b2bcb58f3c578789b2bd379a27b0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572365"
---
# <a name="container-packing-strategies"></a>Konteinera iepakošanas stratēģijas

[!include [banner](../includes/banner.md)]

Šī *konteinera iepakošanas stratēģija* ir stratēģija, ko varat izmantot, lai definētu krājumu sadalījumus konteineros. Šajā tēmā skaidrotas atšķirības starp stratēģijām *Iepakot visos atvērtajos konteineros* un *Iepakot tikai pašreizējā konteinerā*.

- **Iepakot visos atvērtajos konteineros** — sistēmai ir jāpārbauda visi atvērtie konteineri, kas jau ir izveidoti konteinerizācijas cikla laikā, lai pārliecinātos, vai krājums ietilps vienā no tiem. Iepakošanas laikā sistēma pārbauda katru krājumu, lai noteiktu, vai tas iederas jebkurā no iepriekš izveidotajiem konteineriem. Ja krājums neietilpst esošajā konteinerā, sistēma izveido jaunu konteineru un turpina, līdz pabeigta visa pasūtījuma iepakošana.

    Piemēram, *n* pasūtītiem krājumiem nepieciešama konteinerizācija. Tādā gadījumā, katru reizi, kad sistēma apstrādā krājumu, kas neietilpst neviena esošā konteinerā, tiks veiktas visas (\[(*n* – 1) × (*n* + 1)\] ÷ 2) pārbaudes, lai novērtētu, vai krājums iederas esošos konteineros.

- **Iepakot tikai esošajā konteinerā** — Sistēmai jāpārbauda tikai nesen izveidotais konteiners, lai pārliecinātos, vai vienums tajā iederēsies. Iepakošanas laikā sistēma pārbauda katru krājumu, lai noteiktu, vai tas iederēsies nesen izveidotajā konteinerā. Ja krājums neietilpst šajā konteinerā, sistēma izveido jaunu konteineru un turpina, līdz pabeigta visa pasūtījuma iepakošana.

    Piemēram, *n* pasūtītiem krājumiem nepieciešama konteinerizācija. Sliktākajā gadījumā sistēma veiks visas (*n* – 1) pārbaudes, lai novērtētu, vai krājums iederas konteineros.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Konteinera iepakošanas stratēģiju plūsmas piemērs

Konteinerizācijai tiek iestatīti šādi vienumi.

| Objekts | Fiziskās dimensijas (platums × dziļums × augstums) | Lielums |
|---|---|---|
| HDMI kabelis 6´ | 1 × 1 × 1 | 1 |
| HDMI kabelis 12´ | 2 × 1 × 1 | 1 |
| HDMI kabelis 18´ | 3 × 1 × 1 | 2 |

Iepakošanai tiks izmantota tālāk norādītās rūtiņas iestatīšana.

| Konteiners | Fiziskās dimensijas (garums × platums × augstums) | Lielums | Tilpums |
|---|---|---|---|
| Vidēja kaste | 6 × 3 × 2 | 10. | 100 |

Visbeidzot jūs iestatāt pasūtījumu, kam ir šādas preces un daudzumi.

| Pārdošanas pasūtījumu rinda | Daudzums |
|---|---|
| HDMI kabelis 12´ | 9 |
| HDMI kabelis 18´ | 8 |
| HDMI kabelis 6´ | 13 |

Šajā tabulā ir apkopots, kā konteinerizācija darbojas, kad izmantojat stratēģiju *Iepakot visos atvērtajos konteineros* un, ja izmantojat stratēģiju *Iepakot tikai esošajā konteinerā*.

| Iepakot visos atvērtajos konteineros | Iepakot pašreizējā konteinerā |
|---|---|
| <p>HDMI kabelis 12´:</p><ol><li>Izveidot jaunu konteineru, CONT0001.</li><li>Ievietojiet 9 ea konteinerā CONT0001.</li></ol> | <p>HDMI kabelis 12´:</p><ol><li>Izveidot jaunu konteineru, CONT0001.</li><li>Ievietojiet 9 ea konteinerā CONT0001.</li></ol> |
| <p>HDMI kabelis 18´:</p><ol><li>Pārbaudiet, vai krājums var ietilpt konteinerā CONT0001.</li><li>Izveidot jaunu konteineru, CONT0002.</li><li>Ievietojiet 5 ea konteinerā CONT0002.</li><li>Izveidot jaunu konteineru, CONT0003.</li><li>Ievietojiet 3 ea konteinerā CONT0003.</li></ol> | <p>HDMI kabelis 18´:</p><ol><li>Pārbaudiet, vai krājums var ietilpt konteinerā CONT0001.</li><li>Izveidot jaunu konteineru, CONT0002.</li><li>Ievietojiet 5 ea konteinerā CONT0002.</li><li>Izveidot jaunu konteineru, CONT0003.</li><li>Ievietojiet 3 ea konteinerā CONT0003.</li></ol> |
| <p>HDMI kabelis 6´:</p><ol><li>Pārbaudiet, vai krājums var ietilpt konteinerā CONT0001.</li><li>Ievietojiet 1 ea konteinerā CONT0001.</li><li>Pārbaudiet, vai krājums var ietilpt konteinerā CONT0002.</li><li>Pārbaudiet, vai krājums var ietilpt konteinerā CONT0003.</li><li>Ievietojiet 4 ea konteinerā CONT0003.</li><li>Izveidot jaunu konteineru, CONT0004.</li><li>Ievietojiet 8 ea konteinerā CONT0004.</li></ol> | <p>HDMI kabelis 6´:</p><ol><li>Pārbaudiet, vai krājums var ietilpt konteinerā CONT0003.</li><li>Ievietojiet 4 ea konteinerā CONT0003.</li><li>Izveidot jaunu konteineru, CONT0004.</li><li>Ievietojiet 9 ea konteinerā CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Scenārija piemērs: iepakojiet vienu pasūtījumu katrā konteinerā

Šajā sadaļā ir scenārijs, kurā sistēma ir iestatīta vairāku pasūtījumu konsolidēšanai vienā sūtījumā. Tāpēc konteinerizācija tiks veikta no pārdošanas pasūtījuma, lai nodrošinātu, ka katrs pasūtījums, kurā ir vairākas preces, tiek iepakots savā konteinerā.

Šī funkcionalitāte ļauj rīkoties ar scenārijiem, kuros katrā konteinerā ir jāiepako tikai viens pārdošanas pasūtījums, tādējādi sadales centrs var veikt pilnu konteineru pārkraušanu sadales centrā starp mazumtirdzniecības veikaliem. Papildus mazumtirdzniecības scenārijiem (pasūtījums katram mazumtirdzniecības veikalam un nosūtīšana uz sadales centru pārkraušanai sadales centrā) šī tehnika parasti tiek izmantota arī racionālās piegādes ķēdēs (pārdošanas pasūtījums tikai laika ražošanas rindā).

Šajā scenārijā ir parādīts, kā var samazināt to konteineru skaitu, kas tiek novērtēti iepakošanas laikā, izmantojot konteinerizācijas stratēģiju *Iepakot tikai esošajā konteinerā*.

### <a name="prerequisites"></a>Priekšnosacījumi

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Ieslēgt iespēju Konsolidēt sūtījumus jūsu sistēmā

Šajā scenārijā tiek izmantots līdzeklis *Konsolidēt sūtījumus*. Ja šis līdzeklis sistēmā vēl nav pieejams, as ir jāslēdz, izmantojot [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

#### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Šis scenārijs ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.

### <a name="inspect-or-create-container-types"></a>Pārbaudīt vai izveidot konteineru tipus

Lai pārbaudītu konteinera tipus vai izveidotu jaunus konteineru tipus, ja tie ir nepieciešami, veiciet šīs darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Konteineri** \> **Konteineru tipi**.
1. Pārliecinieties, vai demonstrācijas datos ir pieejams katrs no šiem konteineru tipiem. Pēc vajadzības rediģējiet vai izveidojiet konteineru tipus.

    - Konteinera tips 1:

        - **Konteinera tipa kods:** *Kaste - liela*
        - **Apraksts:** *Liela kaste*
        - **Maksimālais neto svars:** *100*
        - **Tilpums:** *400*
        - **Garums:** *4*
        - **Platums:** *10*
        - **Augstums:** *10*

    - Konteinera tips 2:

        - **Konteinera tipa kods:** *Kaste - vidēja*
        - **Apraksts:** *Vidēja kaste*
        - **Maksimālais neto svars:** *50*
        - **Tilpums:** *200*
        - **Garums:** *2*
        - **Platums:** *10*
        - **Augstums:** *10*

    - Konteinera tips 3:

        - **Konteinera tipa kods:** *Kaste - maza*
        - **Apraksts:** *Maza kaste*
        - **Maksimālais neto svars:** *20*
        - **Tilpums:** *100*
        - **Garums:** *1*
        - **Platums:** *10*
        - **Augstums:** *10*

### <a name="inspect-or-create-container-groups"></a>Pārbaudīt vai izveidot konteineru grupas

Lai pārbaudītu konteinera grupas vai izveidotu jaunus konteineru grupas, ja tie ir nepieciešami, veiciet šīs darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru grupas**.
1. Pārliecinieties, vai demonstrācijas datos ir pieejamas šīs konteineru grupas. Ja tās nav pieejamas, atlasiet **Jauns**, lai tās izveidotu.

    - **Konteineru grupas ID:** *Kastes*
    - **Apraksts:** *Kastes izmēri*

1. Kopsavilkuma cilnē **Detalizēta informācija** pārliecinieties, vai pastāv tālāk norādītās rindas konteineru grupai *Kastes*. Ja tās nav, atlasiet **Jauns**, lai tās pievienotu.

    - 1. rinda:

        - **Secības numurs:** *1*
        - **Konteinera veids:** *Kaste - liela*
        - **Konteinera izmantošanas procentuālā vērtība:** *100*

    - 2. rinda:

        - **Secības numurs:** *2*
        - **Konteinera tips:** *Kaste - vidēja*
        - **Konteinera izmantošanas procentuālā vērtība:** *100*

    - 3. rinda:

        - **Secības numurs:** *3*
        - **Konteinera veids:** *Kaste-maza*
        - **Konteinera izmantošanas procentuālā vērtība:** *100*

### <a name="create-a-new-container-build-template"></a>Izveidojiet jaunu konteinera būvējuma veidni

Lai izveidotu jaunu konteinera būvējuma veidni, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Konteineri** \> **Konteinera būvējuma veidnes**.
1. Atlasiet **Jauns**, lai izveidotu konteinera būvējuma veidni, kurā ir šādi iestatījumi:

    - **Secības numurs:** *1*
    - **Konteinera veidnes ID:** *Kaste*
    - **Konteineru grupas ID:** *Kastes*
    - **Bāzes vaicājumu veidi:** *Pārdošanas sadalījuma rinda*
    - **Kopuma darbības kods:** *234*
    - **Atļaut izdošanas sadali:** *Jā*
    - **Konteinera iepakošanas stratēģija:** *Iepakot tikai pašreizējā konteinerā*
    - **Iepakot pēc direktīvas vienības:** *Nē*

1. Kamēr rinda jaunai veidnei joprojām ir atlasīta, darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Parādās standarta vaicājumu redaktora dialoglodziņš. Cilnē **Kārtošana** atlasiet **Pievienot**, lai pievienotu rindu, kurai ir šādi iestatījumi:

    - **Tabula:** *Pagaidu darba darbības*
    - **Atveidotā tabula:** *Pagaidu darba darbības*
    - **Lauks:** *Pasūtījuma numurs*
    - **Meklēšanas virziens:** *Augošā secībā*

    > [!IMPORTANT]
    > Lai izvairītos no meklēšanas visos citos atvērtajos konteineros un paātrinātu procesu, vienlaikus pārbaudot vienu konteineru, izmantojiet stratēģiju *Iepakot tikai pašreizējā konteinerā* papildus šķirošanai pēc pasūtījuma numura. Šī kombinācija darbosies kā darba veidnes darba pārtraukums.

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Kamēr rinda jaunai veidnei joprojām ir atlasīta, darbību rūtī atlasiet **Konteineru sajaukšanas ierobežojumi**.

    Tagad jūs pievienosiet ierobežojumu, kas ievieto krājumus no viena pasūtījuma vienā konteinerā. Krājumi no jebkura cita pasūtījuma tiks ievietoti atsevišķā konteinerā.

1. Atlasiet **Jauns**, lai izveidotu sajaukšanas ierobežojumu kurā ir šādi iestatījumi:

    - **Tabula:** *Pārdošanas pasūtījumi*
    - **Lauka atlase:** *SalesId* (Lauks režģī parādīsies kā *Pārdošanas pasūtījums*.)

1. Atlasiet **Labi**, lai pievienotu ierobežojumu.
1. Aizvērt lapu.

### <a name="set-up-a-wave-template-for-containerization"></a>Kopuma veidnes iestatīšana konteinerizācijai

Lai iestatītu kopuma veidni, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma veidnes**.
1. Saraksta rūtī lauku **Kopuma veidnes tips** iestatiet vērtību *Sūtīšana*.
1. Sarakstā atlasiet veidni **63 konteinerizācija**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Metodes** kolonnā **Atlasītās metodes** atrodama šāda rinda:

    - **Metodes nosaukums:** *konteinerizācija*
    - **Nosaukums:** *Konteinerizēšana*

1. Iestatiet lauku **Kopuma soļa kods** rindai uz *234*.

### <a name="set-up-a-work-template"></a>Darba veidnes iestatīšana

Lai iestatītu darba veidni, veiciet tālāk aprakstītās darbības.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Iestatiet lauku **Darba pasūtījuma veids** uz *Pirkšanas pasūtījumi*.
1. Režģī **Pārskats** atrodiet un atlasiet darba veidni, kas jāizmanto atsevišķu pasūtījumu iepakošanai vienā konteinerā. Šim scenārijam atlasiet **63 izdot konteineram** veidni.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Parādās standarta vaicājumu redaktora dialoglodziņš. Cilnē **Kārtošana** pievienojiet tālāk minētās rindas.

    - 1. rinda:

        - **Tabula:** *Pagaidu darba darbības*
        - **Atveidotā tabula:** *Pagaidu darba darbības*
        - **Lauks:** *Sūtījuma ID*
        - **Meklēšanas virziens:** *Augošā secībā*

    - 2. rinda:

        - **Tabula:** *Pagaidu darba darbības*
        - **Atveidotā tabula:** *Pagaidu darba darbības*
        - **Lauks:** *Pasūtījuma numurs*
        - **Meklēšanas virziens:** *Augošā secībā*

    - 3. rinda:

        - **Tabula:** *Pagaidu darba darbības*
        - **Atveidotā tabula:** *Pagaidu darba darbības*
        - **Lauks:** *Konteinera ID*
        - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.
1. Var tikt parādīts šāds ziņojums: “Grupēšana tiks atiestatīta, vai turpināt?” Lai turpinātu, atlasiet **Jā**.
1. Lai gan joprojām ir atlasīta veidne **63 Izdot konteineram**, darbību rūtī atlasiet **Darba virsraksta pārtraukumi**.

    Tagad tiks lietoti iestatījumi darba pārtraukumam, lai katrs pasūtījumā atvērts konteiners būtu saistīts ar vienu darba pasūtījumu.

1. Atzīmējiet izvēles rūtiņu **Grupēt pēc šī lauka** katrai rindai lapā **Darba virsraksta pārtraukumi** (**Sūtījuma ID**, **Pasūtījuma numurs** un **Konteinera ID**).
1. Aizvērt lapu.

### <a name="set-up-shipment-consolidation-policies"></a>Iestatiet sūtījumu konsolidācijas politikas

Lai iestatītu sūtījumu konsolidācijas politiku, rīkojieties šādi.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Saraksta rūtī iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.
1. Izvēlieties sarakstā politiku **Noklusējums**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Konsolidācijas lauki** sarakstā **Atlasītie lauki**, atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Pasūtījuma numurs*.
1. Atlasiet **Noņemt** pogu ![Bultiņa pa kreisi.](media/backward-button.png) lai pārvietotu lauku uz **Atlikušie lauki** sarakstu.
1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-physical-dimensions-for-the-product"></a>Iestatiet preces fiziskās dimensijas

Lai iestatītu fiziskas dimensijas precēm, kas tiks izmantotas šajā scenārijā, veiciet šīs darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet preci, kuras lauks **Krājuma numura** ir iestatīts uz *A0001*.
1. Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Fiziskās dimensijas**.
1. Lapā **Fiziskās dimensijas** jums vajadzētu redzēt šādu līniju režģī:

    - **Vienība:** *gab*
    - **Bruto svars:** *3,00*
    - **Platums:** *2,00*
    - **Dziļums:** *2,00*
    - **Augstums:** *4,00*
    - **Tilpums:** *16,00*

1. Aizvērt lapu.
1. Atlasiet preci, kuras lauks **Krājuma numura** ir iestatīts uz *A0002*.
1. Darbību rūtī cilnes **Pārvaldīt krājumus** grupā **Noliktava** atlasiet **Fiziskās dimensijas**.
1. Lapā **Fiziskās dimensijas** jums vajadzētu redzēt šādu līniju režģī:

    - **Vienība:** *gab*
    - **Bruto svars:** *4,00*
    - **Platums:** *3,00*
    - **Dziļums:** *1,00*
    - **Augstums:** *3,00*
    - **Tilpums:** *9,00*

### <a name="create-sales-order-1"></a>1. pārdošanas pasūtījuma izveide

Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Parādās dialoglodziņš jauna pārdošanas pasūtījuma izveidošanai. Iestatiet šādas vērtības:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *63*

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet šādas pārdošanas rindas:

    - 1. rinda:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *2*

    - 2. rinda:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *2*

1. Atlasiet pirmo rindu un pēc tam atlasiet **Krājumi \> Rezervēšana**.
1. Lapā **Rezervācija** atlasiet **Rezervēt vietu**. Tad aizveriet lapu.
1. Atkārtojiet iepriekšējās divas darbības otrajai rindai.
1. Aizvērt lapu.

### <a name="create-sales-order-2"></a>2. pārdošanas pasūtījuma izveide

Lai izveidotu otru pārdošanas pasūtījumu, rīkojieties šādi.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Parādās dialoglodziņš jauna pārdošanas pasūtījuma izveidošanai. Iestatiet šādas vērtības:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *63*

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet šādas pārdošanas rindas:

    - 1. rinda:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *4*

    - 2. rinda:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *4*

1. Atlasiet pirmo rindu un pēc tam atlasiet **Krājumi \> Rezervēšana**.
1. Lapā **Rezervācija** atlasiet **Rezervēt vietu**. Tad aizveriet lapu.
1. Atkārtojiet iepriekšējās divas darbības otrajai rindai.
1. Aizvērt lapu.

### <a name="create-the-load"></a>Kravas izveide

Lai izveidotu kravu katram pasūtījumam, kuru izveidojāt šim scenārijam, un pēc tam izlaistu to noliktavā, rīkojieties šādi.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.
1. Cilnē **Pārdošanas rindas** meklējiet un atlasiet visas pārdošanas pasūtījuma rindas šim scenārijam izveidotajiem pārdošanas pasūtījumiem.
1. Darbību rūtī cilnē **Piedāvājums un pieprasījums** grupā **Pievienot**, atlasiet **Jaunai kravai**. Atlasītās pasūtījuma rindas tiek pievienotas jaunai kravai.
1. Dialoglodziņā **Noslodzes veidnes piešķire** laukā **Noslodzes veidnes ID** atlasiet noslodzes veidni, piemēram, *40' konteiners*.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Sadaļā **Noslodzes** meklējiet un atlasiet tikko izveidoto noslodzi.
1. Atlasiet **Izlaist \> Pārvietot uz noliktavu**.
1. Dialoglodziņā **Pārvietot uz noliktavu** atlasiet **Labi**, lai pārvietotu atlasīto noslodzi uz noliktavu.

### <a name="verify-the-shipments-and-containers"></a>Pārbaudīt sūtījumus un konteinerus

Šī procedūra ļauj pārbaudīt izveidotās kravas. Izmantojiet to, lai pārskatītu pasūtījumu, ko izveidojāt šim scenārijam, lai pārliecinātos, ka esat ieguvis sagaidāmos rezultātus.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Atrodiet un atlasiet sūtījumu, kas tika izveidots tikko izlaistai kravai.
1. Darbības rūtī, cilnē **Transports** atlasiet **Skatīt konteinerus**.
1. Apstipriniet, ka krājumi no pārdošanas pasūtījumiem ir konteineros divos dažādos konteineros.

## <a name="additional-resources"></a>Papildu resursi

- [Konteinerizēšana](wave-containerization.md)
