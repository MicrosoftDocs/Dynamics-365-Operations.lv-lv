---
title: Klastera pozīcija pilna
description: Šajā tēmā ir sniegta informācija par līdzekli Pilna klastera pozīcija. Šis līdzeklis piedāvā alternatīvu stingrākai darba pārtraukuma noteikumu izpildei, ja tiek izmantota klasteru izdošana, jo tas pieļauj lielāku kļūdu robežu konteineru vai tvertņu tilpuma ierobežojumos.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ad0f8e2fa6b3767c6b5d5549a36d52990f871531
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808850"
---
# <a name="cluster-position-full"></a>Klastera pozīcija pilna

[!include [banner](../includes/banner.md)]

Līdzeklis *Pilna klastera pozīcija* piedāvā alternatīvu stingrākai darba pārtraukuma noteikumu izpildei, ja tiek izmantota klasteru izdošana, jo tas pieļauj lielāku kļūdu robežu konteineru vai tvertņu tilpuma ierobežojumos. Kopējā scenārijā ne visi darba pasūtījuma vienumi iekļaujas atlasītajā konteinerā. Noliktavas darbiniekiem, kas veic klasteru izdošanu, šajā scenārijā ir dažas iespējas: viņiem ir vai nu jāsamainā konteineru uz lielāku, vai kopā ar vadītāju jāatrod citu risinājumu.

Šis līdzeklis ievieš iespēju darbināt pogu **Pilns** uz vienas no klastera darba vienībām. Vecākās versijās šī opcija bija pieejama tikai regulārai pasūtījumu izdošanai, nevis klastera izdošanai. Tomēr šis līdzeklis atšķiras no standarta pogas **Pilns** , jo tas atceļ atlikušo darbu. Tas neliecina, ka lietotājs tam pašam klasterim pievieno vēl vienu nodalījumu, un tas automātiski nerada jaunu darbu.

## <a name="turn-on-the-cluster-position-full-feature"></a>Ieslēgt līdzekli Pilna klastera pozīcija

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Pilna klastera pozīcija*

## <a name="setup"></a>Iestatīt

Šajā sadaļā ir sniegti norādījumi, un piemērs, kas parāda, kā iestatīt un izmantot līdzekli *Pilna klastera pozīcija* .

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo [scenārija piemēru](#example-scenario), strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Varat arī izmantot šo scenārija piemēru kā norādījumus darbam ar šo līdzekli ražošanas sistēmā. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības tiem iestatījumiem, kas šeit aprakstīti.

### <a name="cluster-profiles"></a>Klastera profili

Ir jānorāda, vai klastera ID tiek ģenerēti automātiski, cik daudz pozīciju tiek izmantotas, kad klasteri tiek sadalīti, un kā izdošanas darbs ir sakārtots un pārbaudīts.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Mobilā ierīce \> Klastera profili**.
1. Saraksta rūtī atlasiet ierakstu **Izveidot klasteri**.
1. Kopsavilkuma cilnē **Vispārīgi** pārbaudiet šādas vērtības:

    - **Ģenerēt klastera ID:** *Jā*
    - **Aktivizēt pozīcijas:** *Jā*
    - **Pozīciju skaits:** *2*
    - **Pozīcijas nosaukums:** *Skaitlisks*
    - **Pārtraukt klasteri pie:** *Ievietot*
    - **Kārtošanas pārbaudes veids:** *Pozīcijas skenēšana*

1. Kopsavilkuma cilnē **Klastera šķirošana** . Režģim ir jābūt tukšam (tas ir, tajā nedrīkst būt rindu).

### <a name="work-templates"></a>Darbu veidnes

Ir jādefinē, kā ir izveidots klastera izdošanas darbs.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Lapas augšmalā iestatiet lauku **Darba pasūtījuma veids** uz *Pārdošanas pasūtījumi*.
1. Pārliecinieties, vai ir uzskaitītas šādas darba veidnes no demonstrācijas datiem. Ja tās nav pieejamas, scenāriju vairs nevarēs pabeigt.

    - 61 SO stadija
    - 61 SO Klastera izdošana

### <a name="location-directives"></a>Vietas direktīvas

Jānorāda, no kurienes vienumi tiek izdoti un kur tie tiek ievietoti.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Saraksta galvenē iestatiet lauku **Darba pasūtījuma veids** uz *Pārdošanas pasūtījumi*.
1. Pārliecinieties, vai ir uzskaitītas šādas pārdošanas pasūtījumu direktīvas no demonstrācijas datiem. Ja tās nav pieejamas, scenāriju vairs nevarēs pabeigt.

    - 61 Klastera izdošana
    - 61 SO Izdošanas pasūtījums

### <a name="mobile-device-menu-items"></a>Mobilās ierīces izvēlnes vienumi

Jākonfigurē mobilās ierīces izvēlnes vienumu, lai izmantotu esošu darbu, ko novirzījusi klastera izdošana. Klastera izdošanai paredzētajā mobilās ierīces izvēlnes vienumā ir jābūt ieslēgtam parametram **Atļaut darba sadalīšanu**, un ir jāpievieno darba klase *SO Izdošana* .

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Saraksta rūtī atlasiet ierakstu **Izveidot izdošanas klasteri** .
1. Darbības rūtī atlasiet **Rediģēt** .
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Noteic:** *Klastera izdošana*
    - **Ģenerēt numura zīmi:** *Jā*
    - **Atļaut darba sadali** *Jā*
    - **Klastera profila ID:** *Klastera izveide*

    Pieņemiet noklusējuma vērtības visiem pārējiem laukiem.

1. Kopsavilkuma cilnē **Darba klases** pēc nepieciešamības pievienojiet šādas divas rindas:

    - 1. rinda (parasti ir demonstrācijas datos):

        - **Darba klases ID:** *Pārdošana* 
        - **Darba pasūtījuma veids:** *Pārdošanas pasūtījumi*

    - 2. rinda (varbūt nav demonstrācijas datos):

        - **Darba klases ID:** *SO Izdošana*
        - **Darba pasūtījuma veids:** *Pārdošanas pasūtījumi*

1. Dodieties uz **Darba apstiprināšanas iestatījumi** darbību rūtī.
1. Atlasiet **Rediģēt**.
1. Režģa rindā ievadiet šādas vērtības.
    - **Darba veids** - *Izdošana*
    - **Preces apstiprinājums** - *Atzīmējiet izvēles rūtiņu*

1. Darbības rūtī atlasiet **Saglabāt** un aizveriet lapu.

## <a name="create-picking-work"></a>Izveidot izdošanas darbu

Pirms klastera izdošanas sākšanas jāizveido daži izejošie darbi. Iepriekš izveidotais klastera profils norāda divas klastera pozīcijas. Tādēļ pārdošanas pasūtījuma izdošanai jāizveido vismaz divi darba ID. Šim scenārijam darbības tiks veiktas noliktavā *61*, un tās izmantos preces *L0101* un *T0100*. Demonstrācijas datos jābūt pietiekamam šo vienumu rīcībā esošo krājumu daudzumam. Pārliecinieties, vai jums ir pietiekami daudz krājumu, lai pabeigtu šīs darbības.

### <a name="create-sales-order-1"></a>1. pārdošanas pasūtījuma izveide

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu 1.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-010*
    - **Noliktava:** *61*

1. Atlasiet **Labi**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu, kurai ir šādi iestatījumi:

    - **Krājuma numurs:** *T0100*
    - **Daudzums:** *5*

1. Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet otru rindu, kurai ir šādi iestatījumi:

    - **Krājuma numurs:** *L0101*
    - **Daudzums:** *20*

1. Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.
1. Katrai rindai, ko tikko pievienojāt, veiciet šīs darbības, lai rezervētu krājumus:

    1. Atlasiet rezervējamo rindu.
    2. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.
    3. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
    4. Aizveriet lapu **Rezervācija**.

1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Kad izlaišana ir pabeigta, saņemsiet informatīvus ziņojumus, kas parāda izveidotos kopuma un noslodzes ID.

### <a name="create-sales-order-2"></a>2. pārdošanas pasūtījuma izveide

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu 2.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-011*
    - **Noliktava:** *61*

1. Atlasiet **Labi**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu, kurai ir šādi iestatījumi:

    - **Krājuma numurs:** *L0101*
    - **Daudzums:** *20*

1. Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet otru rindu, kurai ir šādi iestatījumi:

    - **Krājuma numurs:** *T0100*
    - **Daudzums:** *2*

1. Kopsavilkuma cilnē **Rindas detalizēta informācija** cilnē **Piegāde** iestatiet lauku **Apstiprināts nosūtīšanas datums** uz šodienas datumu.
1. Katrai rindai, ko tikko pievienojāt, veiciet šīs darbības, lai rezervētu krājumus:

    1. Atlasiet rezervējamo rindu.
    2. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.
    3. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
    4. Aizveriet lapu **Rezervācija**.

1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Kad izlaišana ir pabeigta, saņemsiet informatīvus ziņojumus, kas parāda izveidotos kopuma un noslodzes ID.

### <a name="get-work-ids-and-license-plate-numbers"></a>Iegūt darba ID un unikālus noliktavas vienības identifikatorus

Ir jāizveido divi darba ID, katram no kuriem ir divas izdošanas rindas. Sekojiet šiem soļiem, lai atrastu darba ID un unikālās noliktavas vienības piešķires.

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Režģī **Pārskats** meklējiet abu tikko izveidoto pārdošanas pasūtījumu kolonnu **Pasūtījuma numurs** . Katram pārdošanas pasūtījumam atzīmējiet atbilstošo darba ID.
1. Atlasiet rindu katram pārdošanas pasūtījumam, lai parādītu saistīto informāciju režģī **Rindas** . Atzīmējiet vietu, no kuras tiks izdota katra vienība.
1. Dodieties uz **Krājumu vadība \> Uzziņas un atskaites \> Rīcībā esošie krājumu saraksts**.
1. Darbību rūtī atlasiet **Dimensijas**, lai atvērtu dialoglodziņu **Dimensiju attēlojums** .
1. Pārliecinieties, vai ir atzīmētas izvēles rūtiņas **Numura zīme**, **Noliktava** un **Vienuma numurs** un pēc tam atlasiet **Labi**.
1. Rūtī **Filtrs** iestatiet šādus filtrus:

    - **Vienuma numurs** – **ir viens no** – *L0101* un *T100*
    - **Noliktava** – **sākas ar** – *61*

1. Atzīmējiet paradītās **Vienuma numurs** vērtības.

## <a name="example-scenario"></a><a name="example-scenario"></a>Piemēra situācija

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Mobilās ierīces plūsmas izpilde – Darba apstiprinājuma iestatījums precei

1. Pierakstieties Warehouse Management mobile programmā kā lietotājs noliktavā *61*.
1. Dodieties uz **Izejošie \> Izveidot klastera izdošanu**.

    Tiek parādīta lapa **UZDEVUMS: Piešķirt darbu klasterim** .

1. Ievadiet 1. pārdošanas pasūtījuma darba ID, lai to piešķirtu klastera pozīcijai 1.
1. Atlasiet **Labi** (atzīmes simbols).
1. Ievadiet 2. pārdošanas pasūtījuma darba ID, lai to piešķirtu klastera pozīcijai 2.
1. Atlasiet **Labi** (atzīmes simbols).

    Tiek parādīta lapa **UZDEVUMS: Klastera izdošanas izveide: Izdot** un tā parāda *Vienums L0101 2 PL*.

Tā kā klastera profils iestata pozīciju skaitu uz 2, sistēma automātiski novirza jūs uz pirmo konsolidēto izdošanu: divas paletes (PL) no vienuma *L0101*.

Šo darbību laikā jebkurā brīdī varat atlasīt cilni **Detalizēti** , lai apskatītu papildu informāciju par uzdevumu, piemēram, izdošanas vietu.

1. Iestatiet lauku **VIENĪBA** uz *L0101*. Tas apstiprina vienuma numuru, kas ir nepieciešams šim izvēlnes vienumam (jūs konfigurējāt to agrāk, atlasot **Darba apstiprināšanas iestatījumi**  no lapas **Mobilās ierīces izvēlnes vienums** , kad izveidojāt šo izvēlnes vienumu).
1. Ievadiet unikālu noliktavas vienības identifikatoru, kas ir saistīts ar vienību izdotajā novietojumā. Tiks izdotas divas paletes.
1. Iestatiet **LP** lauku uz *LP\_PICK\_01*.
1. Atlasiet **Labi** (atzīmes simbols).

    Tiek parādīta lapa **UZDEVUMS: Sakārtot: Klastera izdošanas izveide** . Šeit divas izdotās paletes tiks šķirotas izdošanas pozīcijā. Šī pozīcija varētu būt tvertne vai konteiners, ko izmanto, lai atdalītu izdotos krājumus pēc pārdošanas pasūtījuma.

1. Skatiet informāciju, kas tiek rādīta krājumam (*L0101*) un daudzumam (*20* ea), kas tiks sašķirots pozīcijā 1 (pārdošanas pasūtījumam 1).
1. Iestatiet **POZICIJA NA** lauku uz *1*.
1. Atlasiet **Labi** (atzīmes simbols).
1. Skatiet informāciju, kas tiek rādīta krājumam (*L0101*) un daudzumam (*20* ea), kas tiks sašķirots pozīcijā 2 (pārdošanas pasūtījumam 2).
1. Iestatiet **POZICIJA NA** lauku uz *2*.
1. Atlasiet **Labi** (atzīmes simbols).

    Tiek parādīta lapa **UZDEVUMS: Klastera izdošanas izveide: Izdot** un tā parāda *Vienums T0100 7 ea*.

Šādā gadījumā 1. pozīcija nevar akceptēt visu vienumu daudzumu, kas ir jāizdod, lai izpildītu 1. pārdošanas pasūtījumu. Pozīcijai ir jābūt atzīmētai kā pilnai. Šajā scenārijā jūs veiksiet daļēju otrā vienuma izdošanu. Otrais vienums tiks daļēji izdots 1. pozīcijai, un tiks izveidots jauns darbs, lai izdotu atlikušo daudzumu pasūtījuma izpildei.

1. Atlasiet pogu Izvēlne (dažreiz saukta par hamburgeru vai hamburgera pogu) un pēc tam atlasiet **Pilna pozīcija**.
1. Identificējiet pozīciju, kas ir pilna, un atlasiet *1*.
1. Atlasiet **Labi** (atzīmes simbols).
1. Ievadiet izdošanas daudzumu, ko joprojām var izdot 1. pozīcijā. Sistēma var noteikt, kurš vienuma numurs tiek izdots.
1. Ievadiet *2*.
1. Atlasiet **Labi** (atzīmes simbols).
1. Apstipriniet vienuma nmuru, lai pabeigtu atlikušo vienumu izdošanu 2. pozīcijā.
1. Iestatiet lauku **VIENĪBA** uz *T0100*.
1. Atlasiet **Labi** (atzīmes simbols).
1. Ievadiet numura zīmi, no kuras tiek izdots vienums, iestatot, lauku **LP** uz *LPREPL04*.
1. Atlasiet **Labi** (atzīmes simbols).
1. Skatiet informāciju, kas tiek rādīta krājumam (*T0100*) un daudzumam (*2* ea), kas tiks sašķirots pozīcijā 2 (pārdošanas pasūtījumam 2).
1. Iestatiet **POZICIJA NA** lauku uz *2*.
1. Atlasiet **Labi** (atzīmes simbols).
1. Skatiet informāciju, kas tiek rādīta krājumam (*T0100*) un daudzumam (*2* ea), kas tiks sašķirots pozīcijā 1 (pārdošanas pasūtījumam 1).
1. Iestatiet **POZICIJA NA** lauku uz *1*.
1. Atlasiet **Labi** (atzīmes simbols).

    Tiek parādīta lapa **UZDEVUMS: Klastera izdošanas izveide: Ievietot** .

Šajā scenārijā klastera izdošana ir pabeigta, un lietotājs ir novirzīts, lai izvietotu izdotos krājumus no 1. pozīcijas un 2. pozīcijas uz sagatavošanas vietu *STAGE01*.

1. Pārskatiet informāciju lapā. Tā parāda, ka kopējais daudzums *44* tiks izvietots uz sagatavošanas vietu.
1. Atlasiet **Labi** (atzīmes simbols).

    Tiek saņemts ziņojums "Klasteris pabeigts".

Tagad varat izmantot izvēlnes vienumu **Pārdošanas izdošana**, lai izdotu atlikušo daudzumu. Pēc tam varat izmantot izvēlnes vienumu **Pārdošanas iekraušana** , lai pārvietotu vienumus no sagatavošanas vietas uz iekraušanas doku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]