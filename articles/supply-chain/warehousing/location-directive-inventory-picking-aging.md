---
title: Novietojuma direktīvas krājumu izdošanas vecumstruktūras
description: Šajā rakstā skaidrots, kā izdošanas laikā lietot "pirmais ārā" (FIRST in, first out – FIFO) un "pirmais ārā" (LIFO) novietojuma direktīvas.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4ed1308ea36b731b156b518182846b60a59528d5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335621"
---
# <a name="location-directive-inventory-picking-aging"></a>Novietojuma direktīvas krājumu izdošanas vecumstruktūras

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā izdošanas laikā lietot "pirmais ārā" (FIRST in, first out – FIFO) un "pirmais ārā" (LIFO) novietojuma direktīvas. Šīs stratēģijas darbojas savienojumā ar vecumstruktūras datumiem, kas tiek ierakstīti novietojumā, lai izsekotu, kad krājumi pirmo reizi ievadīti noliktavā. Līdzeklis *Novietojuma direktīvas krājumu izdošanas vecumstruktūras* izmanto novietojuma datumu, lai noteiktu vecumstruktūras. Līdzeklis *Noliktavas novietojuma statuss* atjaunina novietojuma datumu, pamatojoties uz noliktavas vienības datumu.

Varat izmantot FIFO un LIFO stratēģiju, lai nosūtītu gan partijas izsekotos krājumus, gan partijas neizsekotos krājumus, pamatojoties uz datumu, kad krājumi ievadīti noliktavā. Šī iespēja var būt īpaši noderīga partijas neizsekotajiem krājumiem, kuru beigu datums nav pieejams kārtošanai.

Kad krājumi pirmo reizi tiek saņemti vai izveidoti noliktavā, sistēma atjaunina atbilstošo noliktavas vienību, lai pašreizējais datums tiktu parādīts kā vecumstruktūras datums. Pēc tam šo datumu izmanto novietojuma direktīvas stratēģijas, lai identificētu vecākos vai jaunākos krājumus noliktavā. Ja krājumi tiek pārvietoti uz novietojumu, kas netiek izsekots ar noliktavas vienību, tad novietojums tiek atjaunināts ar vecumstruktūras informāciju, un šī informācija pēc tam tiek izmantota stratēģijās.

## <a name="turn-on-the-feature"></a>Līdzekļa iespējošana

Lai padarītu šo līdzekli pieejamu, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) šādā secībā:

1. *Noliktavas atrašanās* vietas statuss (versijā 10.0.29) šis līdzeklis ir obligāts un to nevar izslēgt. Papildinformāciju skatiet noliktavas [atrašanās vietas statusā](warehouse-location-status.md).
1. *Novietojuma direktīvas krājumu izdošanas vecumstruktūras*

## <a name="feature-requirements"></a>Līdzekļa prasības

Lai izmantotu šo līdzekli, opcija **Iespējot novietojuma statusu** ir jāiestata uz *Jā* katram [novietojuma profilam](tasks/create-location-profile.md), kas tiek izmantots veikala krājumiem. Lai novietojuma profilam iestatītu šo opciju, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojuma profili** un atlasiet novietojuma profilu. Opciju varat atrast kopsavilkuma cilnē **Vispārīgi**.

## <a name="feature-scenarios"></a>Līdzekļa scenāriji

Šajā sadaļā ir sniegti piemēri, kā iestatīt un izmantot FIFO un LIFO stratēģiju.

> [!TIP]
> Šajā sadaļā ir sniegti divi scenāriji, viens FIFO un viens LIFO. Sniegtajās procedūrās tiek pieņemts, ka abus scenārijus veiksit pēc kārtas. Ieteicams veikt abus scenārijus, lai varētu izprast atšķirību starp abām stratēģijām.

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šos scenārijus, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/fin-ops/get-started/demo-data.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Varat izmantot šos scenārijus arī kā norādījumus šī līdzekļa izmantošanai ražošanas sistēmā. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības katram iestatījumam, kas šeit aprakstīts.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Scenāriju iestatīšana

Demonstrācijas datiem ir nepieciešama iestatīšana un krājumu korekcija, lai atbalstītu scenārijus. Veiciet šādas darbības, lai izveidotu krājumu datus, kas nepieciešami, strādājot ar FIFO un LIFO scenārijiem.

1. Piesakieties sistēmā, kurā ir instalēti demonstrācijas dati, un atlasiet **USMF** juridisko personu.
1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Novietojuma profilu sarakstā atlasiet **FLOOR-05**.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Iespējot novietojuma statusu** uz *Jā*.
1. Atlasiet **Saglabāt**.
1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Novietojuma direktīvu sarakstā atlasiet **63 izdot konteinerizēšanai**.
1. Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atradīsiet rindu, kur lauks **Secības numurs** ir iestatīts uz *1*, un izpildīsiet vienu no šīm darbībām:

    - Ja iestatāt FIFO scenāriju, mainiet lauka **Stratēģija** vērtību uz *FIFO novietojuma vecumstruktūras*.
    - Ja iestatāt LIFO scenāriju, mainiet lauka **Stratēģija** vērtību uz *LIFO novietojuma vecumstruktūras*.

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Rediģēt vaicājumu**.
1. Vaicājuma dialoglodziņa cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, un pēc tam iestatiet šādas vērtības:

    - **Tabula:** *Novietojumi*
    - **Atvasinātā tabula:** *Vietas*
    - **Lauks:** *Zonas ID*
    - **Kritēriji:** *Stāvs*

1. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu vaicājuma dialoglodziņu.
1. Atlasiet **Saglabāt**, lai saglabātu novietojuma direktīvas izmaiņas.
1. Lai atbalstītu scenārijus, mobilajā ierīcē vai programmā *Dynamics 365 Supply Chain Management - Uzglabāšana noliktavā* savā datorā, veiciet šādas darbības, lai noņemtu esošos krājumus no noliktavas vietas:

    1. Piesakieties *63* noliktavā, izmantojot atbilstošu lietotāja ID un paroli.
    1. Galvenajā izvēlnē atlasiet **Kvalitāte**.
    1. Izvēlnē **Kvalitātes pārvaldība** atlasiet **Brāķis**.
    1. Lapā **Brāķis** atlasiet lauku **LOC/LP** un pēc tam ievadiet *63\_1*.
    1. Atlasiet **Ievadīt** vai **Labi**.
    1. Apstipriniet **Brāķis** informāciju, lai veiktu **Izejošā korekcija**, atlasot **Ievadīt** vai **Labi**.

    Kad noliktavas vienības krājumi ir koriģēti, tiek parādīts ziņojums “Darbs pabeigts”.

    Šīs darbības atstāj krājumus divos demonstrācijas datu novietojumos. Katram novietojumam ir cits vecumstruktūras datums. Novietojuma *FL-001* vecumstruktūras datums ir 2017. gada 15. aprīlis un novietojuma *FL-002* vecumstruktūras datums ir 2017. gada 29. janvāris. Abos novietojumos ir ietverts krājums *A0001*.

    Lai skatītu šos datus, dodieties uz **Krājumu pārvaldība \> Pieprasījumi un pārskati \> Rīcībā esošs** un pēc tam filtrējiet noliktavu *63* un krājumu *A0001*. Rindās, kur lauks **Novietojums** ir iestatīts uz *FL-001* vai *FL-002*, atlasiet rindu ar pozitīvu **Fiziskie krājumi** vērtību un pēc tam darbību rūtī atlasiet **Transakcijas**. Laukā **Fiziskais datums** tiks parādīts datums, kas atbilst vienam no iepriekš minētajiem vecumstruktūras datumiem.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>1. scenārijs: iestatīt un izmantot FIFO novietojuma vecumstruktūras

FIFO stratēģija atrod novietojumu, kas ietver vecāko vecumstruktūras datumu, un piešķir izdošanu, pamatojoties uz šo vecumstruktūras datumu.

1. Ja vēl neesat to izdarījis, [sagatavojiet datu paraugus](#demo-set-up), kas ir nepieciešami šim scenārijam.
1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - Kopsavilkuma cilnē **Klients** iestatiet lauku **Klienta konts** uz *US-001*.
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noliktava** uz *63*.

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tas ietver jaunu, tukšu rindu režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Šai pasūtījuma rindai iestatiet lauku **Krājuma kods** uz *A0001* un lauku **Daudzums** uz *1*.
1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu šī krājuma pasūtīto daudzumu no atlasītās noliktavas krājumiem.
1. Aizveriet lapu **Rezervācija**.
1. Lapā **Pārdošanas pasūtījums**, darbību rūtī cilnē **Noliktava** grupā **Darbības**, atlasiet **Pārvietot uz noliktavu**. Tiek parādīti informatīvi ziņojumi. Sistēma izveido sūtījumu, pievieno to jaunajai kravai un izveido nepieciešamo darbu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** izvēlnē **Noliktava**, atlasiet **Darba informācija**, lai atvērtu darbu, kas tika izveidots šim pārdošanas pasūtījumam. Ievērojiet, ka rinda **Darba veids**, kurā ir vērtība *Izdot*, rāda **Novietojums** vērtību *FL-002*. Šis novietojums ietver noliktavas vienību ar vecāko vecumstruktūras datumu (FIFO).
1. Atlasiet **Noliktava \> Sūtījuma informācija**.
1. Kopsavilkuma cilnē **Vispārīgi** pierakstiet kopuma ID, lai varētu to izmantot 2. scenārijā.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>2. scenārijs: iestatīt un izmantot LIFO novietojuma vecumstruktūras

LIFO stratēģija atrod novietojumu, kas ietver jaunāko vecumstruktūras datumu, un piešķir izdošanu, pamatojoties uz šo vecumstruktūras datumu. 2. scenārijā ir jārediģē 1. scenārija iestatījums (FIFO) un atkārtoti jāizmanto pārdošanas pasūtījums un kopums, kas tika izveidoti scenārija laikā.

1. Pirms sākat šo scenāriju, iestatiet un pabeidziet pilnu FIFO scenāriju, kā aprakstīts [iepriekšējā sadaļā](#fifo-demo). Šajā scenārijā ir atkārtoti jāizmanto kopums un lielākā daļa iestatījumu, kas tika izveidoti iepriekšējam scenārijam.
1. Rediģējiet **63 izdot konteinerizēšanai** novietojuma direktīvu, lai tā izmantotu *LIFO novietojuma vecumstruktūras* stratēģiju, kā aprakstīts [Scenāriju iestatīšanas](#demo-set-up) procedūras pirmajā daļā.

    Pēc tam modificējiet kopumu, kas tika izveidots pārdošanas pasūtījumam 1. scenārijā, lai tiktu izmantota stratēģija *LIFO novietojuma vecumstruktūras*.

1. Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.
1. Atlasiet un atveriet kopumu, kas ietver pasūtījumu, ko izveidojāt FIFO scenārijam.
1. Darbību rūtī cilnē **Darbs** atlasiet **Atcelt**, lai atceltu darbu, ko izveidojāt FIFO scenārijam.
1. Darbību rūts cilnē **Kopums**, grupā **Kopums** atlasiet **Apstrādāt**.
1. Kad apstrāde ir pabeigta, darbību rūtī cilnes **Kopums** grupā **Saistītā informācija**, atlasiet **Darbs**, lai atvērtu darbu, kas tika izveidots šim kopumam.
1. Lapā **Darbs** cilnē **Pārskats** ir jābūt divām rindām. Atlasiet rindu, kur lauks **Darba statuss** ir iestatīts uz *Atvērt*.
1. Ievērojiet, ka rinda **Darba veids**, kurā ir vērtība *Izdot*, rāda **Novietojums** vērtību *FL-001*. Šis novietojums ietver noliktavas vienību ar jaunāko vecumstruktūras datumu (LIFO).

Šajos scenārijos ir redzams, kā novietojuma vecumstruktūras stratēģija novirza darbu uz krājumu novietojumu, kurā ir vai nu vecākie krājumi, vai jaunākie krājumi, atkarībā no atlasītās stratēģijas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
