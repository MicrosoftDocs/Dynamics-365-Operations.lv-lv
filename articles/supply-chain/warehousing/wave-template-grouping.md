---
title: Kopuma veidņu grupēšana
description: Kopuma veidņu grupēšana ļauj sistēmai izmantot kopuma veidnes iestatījumus, lai, pamatojoties uz jūsu noteiktajiem kritērijiem, definētu, kā ir jāsadala izlaistās rindas un tās jāpiešķir jauniem vai esošiem kopumiem. Šis līdzeklis var noderēt noliktavās, kur kopumi tiek izveidoti, pamatojoties uz konkrētiem kritērijiem, bet vadītāji dod priekšroku kopumu automātiskai izveidei (nevis manuālai).
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9cbc0b6655de740628bcf3709d250ac02238038b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015830"
---
# <a name="wave-template-grouping"></a>Kopuma veidņu grupēšana

[!include [banner](../includes/banner.md)]

Kopuma veidņu grupēšana ļauj sistēmai izmantot [kopuma veidnes](tasks/configure-wave-processing.md) iestatījumus, lai, pamatojoties uz jūsu noteiktajiem kritērijiem, definētu, kā ir jāsadala izlaistās rindas un tās jāpiešķir jauniem vai esošiem kopumiem. Šis līdzeklis var noderēt noliktavās, kur kopumi tiek izveidoti, pamatojoties uz konkrētiem kritērijiem, bet vadītāji dod priekšroku kopumu automātiskai izveidei (nevis manuālai). Tā ļauj sistēmai piešķirt katru no jauna izlaistu sūtījumu pirmajam kopumam, ko sistēma atrod ar atbilstošām grupēšanas lauka vērtībām. Ja neviena atbilstība netiek atrasta, sistēma jaunajam sūtījumam izveido jaunu kopumu.

> [!IMPORTANT]
> Kopuma veidņu grupēšana netiek atbalstīta darba veidiem *ražošanas izejmateriāla izdošana* vai *Kanban izdošana*. Iemesls — kopuma grupēšanas pamatā ir sūtījumi, bet šie darba veidi neizmanto sūtījumus.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Līdzekļa Kopuma veidņu grupēšana ieslēgšana

Lai varētu izmantot līdzekli *Kopuma veidņu grupēšana* , tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Kopuma veidņu grupēšana*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Iestatiet kopuma veidni, lai izmantotu kopuma veidņu grupēšanu

Lai padarītu pieejamu kopuma veidņu grupēšanu, veiciet tālāk norādītās darbības [kopuma veidnes](tasks/configure-wave-processing.md) iestatīšanai.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Kreisajā rūtī atlasiet kopuma veidni, kas jāiestata. Ja vēlaties ar šajā tēmā minēto scenāriju strādāt vēlāk, izmantojot demonstrācijas datus, atlasiet veidni **62 sūtījuma noklusējums**.
1. Darbību rūtī atlasiet **Rediģēt** , lai lapu padarītu rediģējamu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Automatizēt kopuma izveidi:** *Jā*
    - **Piešķirt atvērtajiem kopumiem:** *Jā*
    - **Apstrādāt kopumu, to pārvietojot uz noliktavu:** *Nē*

1. Darbību rūtī atlasiet **Rediģēt vaicājumu** , lai atvērtu vaicājuma dialoglodziņu.
1. Vaicājuma dialoglodziņā cilnē **Kārtošana** pārskatiet kārtošanas kritērijus un pārliecinieties, vai ir iekļauta kārtula, kas ietver lauku, ko vēlaties izmatot jūsu kopumu grupēšanai.

    Ja gatavojaties strādāt ar scenāriju, izmantojot demonstrācijas datus, pievienojiet rindu, kurai ir tālāk norādītās vērtības.

    - **Tabula:** *Sūtījumi*
    - **Atvasinātā tabula:** *Sūtījumi*
    - **Lauks:** *Pārvadātāja pakalpojums*

        > [!NOTE]
        > Pēc šīs vērtības atlasīšanas, iespējams, tiks rādīts šāds ziņojums: “Lauks Pārvadātāja pakalpojums nav indeksa lauks. Vai šim vēlaties pievienot kārtošanu?” Lai pievienotu kārtošanu, atlasiet **Jā**.

    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi** , lai saglabātu izmaiņas un aizvērtu vaicājuma dialoglodziņu.
1. Darbību rūtī atlasiet **Kopuma veidņu grupēšana**.
1. Lapā **Kopuma veidņu grupēšana** atzīmējiet izvēles rūtiņu **Grupēt pēc** katrai rindai, kuru vēlaties izmantot, lai pasūtījuma rindas pēc nepieciešamības grupētu kopumos. Ja gatavojaties strādāt ar šo scenāriju, izmantojot demonstrācijas datus, rindai *Pārvadātāja pakalpojums* atzīmējiet izvēles rūtiņu **Grupēt pēc**.
1. Atlasiet **Saglabāt**.
1. Aizveriet lapu **Kopuma veidņu grupēšana**.
1. Atlasiet **Saglabāt** , lai saglabātu veidni.

## <a name="scenario"></a>Scenārijs

Šajā sadaļā ir nodrošināts skripts, kuru varat izmantot, lai uzzinātu, ko šis līdzeklis nodrošina un kā ar to darboties.

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Varat arī izmantot šo scenāriju kā norādījumus, lai līdzekli lietotu darbā ar ražošanas sistēmu. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.

### <a name="scenario-wave-template-grouping"></a>Scenārijs: Kopuma veidņu grupēšana

Šajā scenārijā ir izskaidrots, kā izmantot kopuma veidņu grupēšanu, lai automātiski izveidotu vairākus kopumus, pamatojoties uz kopuma veidnē definētajiem grupēšanas kritērijiem. Šajā scenārijā kopuma veidne ir iestatīta sistēmā, lai katram pārvadātāja pakalpojumam izveidotu vienu kopumu.

Pirms darba sākšanas sagatavojiet kopuma veidni, kā tas ir iepriekš izklāstīts šīs tēmas sadaļā [Kopuma veidnes iestatīšana, lai izmantotu kopuma veidņu grupēšanu](#set-up-template). Ja strādāsit ar šim scenārijam paredzētajiem demonstrācijas datiem, noteikti izmantojiet šajā procedūrā ieteiktās demonstrācijas datu vērtības. Šajā iestatījumā kopumi tiks grupēti atbilstoši pārvadātāja pakalpojumam, kas ir iestatīts katram pārdošanas pasūtījumam.

#### <a name="create-sales-order-1"></a>1. pārdošanas pasūtījuma izveide

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns** , lai izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - Kopsavilkuma cilnē **Klients** iestatiet laukam **Klienta konts** vērtību *US-004*.
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.

1. Atlasiet **Labi** , lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.
1. Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**. Pierakstiet pārdošanas pasūtījuma numuru.
1. Pārejiet uz skatu **Galvene**.
1. Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.

    - **Sūtījuma pārvadātājs:** *Kravas lidmašīnas*
    - **Pārvadātāja pakalpojums:** *Gaisa*

1. Pārejiet atpakaļ uz skatu **Rindas**.
1. Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu** , lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *2*

1. Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu** , lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Darbību rūtī cilnē **Noliktava** , kas atrodas grupā **Darbības** , atlasiet **Nodot izpildei noliktavā**.
1. Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums. Pierakstiet kopuma ID numuru un sūtījuma ID numurus.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>No 1. pārdošanas pasūtījuma izveidotā kopuma skatīšana

1. Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.
1. Atlasiet kopuma ID, kas tika izveidots no pārdošanas pasūtījuma.
1. Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.
1. Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas**.

#### <a name="create-sales-order-2"></a>2. pārdošanas pasūtījuma izveide

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns** , lai izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - Kopsavilkuma cilnē **Klients** iestatiet lauka **Klienta konts** vērtību uz *US-005*.
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.

1. Atlasiet **Labi** , lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.
1. Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**. Pierakstiet pārdošanas pasūtījuma numuru.
1. Pārejiet uz skatu **Galvene**.
1. Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.

    - **Sūtījuma pārvadātājs:** *Ziedu pārvietošana*
    - **Pārvadātāja pakalpojums:** *Stand.*

1. Pārejiet atpakaļ uz skatu **Rindas**.
1. Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu** , lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *1*

1. Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu** , lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Darbību rūtī cilnē **Noliktava** , kas atrodas grupā **Darbības** , atlasiet **Nodot izpildei noliktavā**.
1. Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums. Pierakstiet kopuma ID numuru un sūtījuma ID numurus. Ņemiet vērā, ka kopuma ID atšķiras no pirmā pārdošanas pasūtījuma kopuma ID.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>No 2. pārdošanas pasūtījuma izveidotā kopuma skatīšana

1. Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.
1. Atlasiet kopuma ID, kas tika izveidots no otrā pārdošanas pasūtījuma.
1. Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.
1. Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas**.

Šim sūtījumam tika izveidots jauns kopums, jo tas izmanto no pirmā pārdošanas pasūtījuma atšķirīgu pārvadātāja pakalpojumu.

#### <a name="create-sales-order-3"></a>3. pārdošanas pasūtījuma izveide

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns** , lai izveidotu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - Kopsavilkuma cilnē **Klients** iestatiet lauka **Klienta konts** vērtību uz *US-006*.
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.

1. Atlasiet **Labi** , lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.
1. Jaunais pārdošanas pasūtījums tiek atvērts skatā **Rindas**. Pierakstiet pārdošanas pasūtījuma numuru.
1. Pārejiet uz skatu **Galvene**.
1. Kopsavilkuma cilnē **Piegāde** sadaļā **Transportēšana** iestatiet tālāk norādītās vērtības.

    - **Sūtījuma pārvadātājs:** *Kravas lidmašīnas*
    - **Pārvadātāja pakalpojums:** *Gaisa*

1. Pārejiet atpakaļ uz skatu **Rindas**.
1. Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu** , lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *1*

1. Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Darbību rūts lapā **Rezervācija** atlasiet **Rezervēt laidienu** , lai noliktavā rezervētu pilnu atlasītās rindas daudzumu.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Darbību rūtī cilnē **Noliktava** , kas atrodas grupā **Darbības** , atlasiet **Nodot izpildei noliktavā**.
1. Saņemsit informatīvu ziņojumu, kurā būs norādīts šī pasūtījuma sūtījums un kopums. Pierakstiet kopuma ID numuru un sūtījuma ID numurus. Sūtījums ir piešķirts esošajam kopumam no pirmā pārdošanas pasūtījuma.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>1. un 3. pārdošanas pasūtījuma kopumu skatīšana

1. Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.
1. Atlasiet kopuma ID, kas tika izveidots no trešā pārdošanas pasūtījuma.
1. Atlasiet kopuma ID saiti, lai atvērtu lapu ar detalizētu informāciju par kopumu.
1. Ņemiet vērā, ka sūtījums tika pievienots kopsavilkuma cilnei **Kopuma rindas** kopā ar pirmajam pārdošanas pasūtījumam paredzēto sūtījumu.
