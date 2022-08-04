---
title: Plānotā pārkraušana sadales centrā
description: Šajā rakstā ir aprakstīta detalizēta plānotā pārkraušana sadales centrā, kur pasūtījumam nepieciešamais krājumu daudzums tiek virzīts tieši no saņemšanas vai izveides uz pareizo nosūtīšanas doku vai sagatavošanas vietu. Visi atlikušie krājumi no saņemšanas avota tiek novirzīti uz pareizo glabāšanas vietu, izmantojot regulāro izvietošanas procesu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 4f379b3cdb6830f989199afde7d751842047df79
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070295"
---
# <a name="planned-cross-docking"></a>Plānotā pārkraušana sadales centrā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīta detalizēta plānotā pārkraušana sadales centrā. Šajā tēmā ir aprakstīta uzlabota plānotā pārkraušana sadales centrā, kur pasūtījumam nepieciešamais krājumu daudzums ir novirzīts tieši no saņemšanas vai izveides uz pareizo nosūtīšanas doku vai sagatavošanas apgabalu. Visi atlikušie krājumi no saņemšanas avota tiek novirzīti uz pareizo glabāšanas vietu, izmantojot regulāro izvietošanas procesu.

Pārkraušana sadales centrā ļauj darbiniekiem izlaist ienākošo krājumu izvietošanu un izejošo krājumu izsniegšanu, kas jau ir atzīmēta izejošam pasūtījumam. Tāpēc, krājuma saskares reižu skaits tiek minimizēts iespēju robežās. Turklāt, ņemot vērā, ka ir mazāka mijiedarbība ar sistēmu, laika un vietas ietaupījums noliktavas ražotnē ir palielināts.

Pirms var veikt pārkraušanu sadales centrā, ir jākonfigurē jauna nosūtīšanas nosūtīšanai paredzētā veidne, kurā ir norādīts piegādes avots un citas prasību kopas pārkraušanai sadales centrā. Kad izejošais pasūtījums ir izveidots, rinda ir jāatzīmē ar ienākošo pasūtījumu, kas ietver to pašu elementu. Varat izvēlēties direktīvas koda lauku veidnē Pārkraušana sadales centrā, kas ir līdzīgs tam, kā iestatījāt papildināšanas un pirkšanas pasūtījumus.

Saņemšanas pasūtījuma saņemšanas laikā pārkraušanas sadales centrā iestatījums automātiski nosaka nepieciešamību veikt pārkraušanu sadales centrā un izveido vajadzīgā daudzuma kustības darbu, pamatojoties uz novietojuma direktīvas iestatījumiem.

> [!NOTE]
> Krājumu darbības *tiek* reģistrētas, atceļot pārkraušanas sadales centrā darbu, pat ja iestatījumi šai iespējai ir ieslēgti Noliktavas pārvaldības parametros.

## <a name="turn-on-the-planned-cross-docking-features"></a>Iespējot plānotās pārkraušanas opcijas

Ja sistēmā vēl nav ietverti šajā rakstā aprakstītie līdzekļi, [pārejiet](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) uz sadaļu Līdzekļu pārvaldība un slēdziet šādus līdzekļus šādā secībā:

1. *Plānotā pārkraušana sadales centrā*
1. *Pārkraušana sadales centrā — veidnes ar atrašanās vietas norādēm*
    > [!NOTE]
    > Šis līdzeklis ļauj lauku **Direktīvas kods** norādīt veidnē Pārkraušana sadales centrā līdzīgi tam, kā iestatījāt papildināšanas veidnes. Šī līdzekļa iespējošana neļauj galarezultātā pievienot direktīvas kodu darba veidnes Pārkraušana sadales centrā rindām pēdējai *Izvietojuma* rindai. Tas nodrošina, ka darba izveides laikā var noteikt pēdējo izvietošanas novietojumu, pirms tiek apsvērtas darba veidnes.

## <a name="setup"></a>Iestatīt

### <a name="regenerate-load-posting-methods"></a>Atkārtoti ģenerēt noslodzes grāmatošanas metodes

Plānotā pārkraušana sadales centrā tiek ieviesta kā noslodzes grāmatošanas metode. Pēc opcijas iespējošanas ir atkārtoti jāģenerē metodes.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noslodzes grāmatošanas metodes**.
1. Darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**.

    Kad reģenerācija ir pabeigta, ir jābūt redzamai metodei ar **Metodes nosaukuma** vērtību *planCrossDocking*.

1. Aizvērt lapu.

### <a name="create-a-cross-docking-template"></a>Izveidojiet pārkraušanas sadales centra veidni

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Pārkraušanas sadales centrā veidnes**.
1. Lai izveidotu veidni, darbību rūtī atlasiet **Jauns**.
1. Galvenē iestatiet šādas vērtības:

    - **Secība:** *1*

        Šis lauks nosaka secību, kādā tiek novērtētas veidnes.

    - **Pārkraušanas sadales centra veidnes ID:** *51*
    - **Apraksts:** *Noliktava 51*
    - **Pieprasījuma izlaides politika:** *Kvīts pirms piegādes*
    - **Noliktava:** *51*

1. Kopsavilkuma cilnes **Plānošana** iestatījums kontrolē veidnes darbību. Iestatiet šādas vērtības:

    - **Pieprasījuma prasības:** *Nav*

        Šis lauks nosaka pieprasījuma krājumu vajadzības. Ja pieprasījumam ir jābūt saistītam ar piegādi pirms nodošanas, atlasiet *Iezīmēšana*. Ja pieprasījumam ir jābūt rezervētam pasūtījumam pirms nodošanas, atlasiet *Pasūtījuma rezervācija*.

    - **Atrašanas tips:** *Piegādes vietas*

        Šis lauks nosaka, vai pārkraušanai sadales centrā ir jāizmanto nosūtījuma sagatavošanas/noslodzes vietas, vai arī ir jāizmanto novietojuma direktīvas, lai atrastu savas sagatavošanas/noslodzes vietas.

    - **Darba veidne:** Atstājiet šo lauku tukšu.

        Šis lauks definē darba veidni, kas jāizmanto, izveidojot pārkraušanas sadales centrā darbu.

    - **Atkārtoti apliecināt piegādes kvīti:** *Nē*

        Šī opcija nosaka, vai, saņemot kvīti, ir atkārtoti jāapliecina piegāde. Ja šī opcija ir iestatīta uz *Jā*, ir jāpārbauda gan maksimālais laika logs, gan beigu dienu diapazons.

    - **Direktīvas kods:** atstājiet šo lauku tukšu

        Šo opciju aktivizē līdzeklis *Veidnes Pārkraušana sadales centrā ar novietojuma direktīvam*. Sistēma izmanto novietojuma direktīvas, lai palīdzētu noteikt labāko novietojumu, uz kuru pārvietot krājumus pārkraušanai sadales centrā. To var iestatīt, katrai atbilstošai veidnei pārkraušanai sadales centrā piešķirot direktīvas kodu. Ja direktīvas kods ir iestatīts, sistēma meklē vietas direktīvas pēc direktīvas koda, ģenerējot darbu. Šādā veidā var ierobežot novietojuma direktīvas, kas tiek izmantotas noteiktai veidnei Pārkraušana sadales centrā.

    - **Validēt maksimālo laika logu:** *Jā*

        Šī opcija nosaka, vai maksimālais laika logs ir jānovērtē, kad ir atlasīts piegādes avots. Ja šī opcija ir iestatīta uz *Jā*, ir pieejami lauki, kas saistīti ar maksimālo un minimālo laiku logiem.

    - **Maksimālā laika logs:** *5*

        Šis lauks nosaka maksimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.

    - **Maksimālais laika loga bloks:** *Dienas*
    - **Minimālais laika logs:** *0*

        Šis lauks nosaka minimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.

    - **Minimālā laika loga vienība:** *Dienas*
    - **Termiņa beigu dienu diapazons:** *0*

        *Pirmā beigu datuma (FEFO) kritēriji:* Šis lauks nosaka maksimālo dienu skaitu starp pirmās beigu partijas, kas pašlaik atrodas noliktavā, beigu datumu un saņemto partiju.

1. Kopsavilkuma cilnē **Piegādes avoti** norādiet šai veidnei derīgus piegādes tipus. Atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:

    - **Secības numurs:** *1*
    - **Piegādes avots:** *Pirkuma pasūtījums*

> [!NOTE]
> Vaicājumu var iestatīt, lai kontrolētu, ja tiek izmantota īpaša pārkraušana sadales centra veidne. Veidnēm pārkraušanas sadales centra vaicājumam ir tikai tabula *InventTable* (krājumi) un iekšējā *WHSInventTable* (WMS krājumi) tabula. Ja vaicājumam vēlaties pievienot citas tabulas, varat tās pievienot, izmantojot tikai *esošos savienojumus* vai *neesošos savienojumus*. Filtrējot savienotās tabulas, katram atbilstošam ierakstam savienotajā tabulā tiek izgūts galvenās tabulas ieraksts. Ja savienojuma tips ir *esošie savienojumi*, meklēšana beidzas pēc pirmās atbilstības meklēšanas. Piemēram, ja pievienojat pārdošanas pasūtījuma rindu tabulu krājumu tabulai, sistēma validē un atgriež krājumus, kuriem vismaz vienai pārdošanas pasūtījuma rindai ir definēts nosacījums. Būtībā dati tiek iegūti no primāras (vienumu) tabulas, nevis no pakārtotās (pārdošanas pasūtījuma rindas) tabulas. Tāpēc filtrēšanu pēc pirmdokumentiem, piemēram, pārdošanas pasūtījuma rindām vai debitoriem, nevar veikt uzreiz.

### <a name="create-a-work-class"></a>Darba klases izveide

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.
1. Lai izveidotu darba klasi, darbību rūtī atlasiet **Jauns**.
1. Iestatiet šādas vērtības:

    - **Darba klases ID:** *Pārkraušana sadales centrā*
    - **Apraksts:** *Pārkraušana sadales centrā*
    - **Darba pasūtījuma tips:** *Pārkraušana sadales centrā*

### <a name="create-a-work-template"></a>Izveidojiet darba veidni

1. Doties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Darba veidnes**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.
1. Lai pievienotu rindu cilnē **Pārskats**, darbības rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Secības numurs:** *1*
    - **Pārkraušanas veidne:** *51 Pārkraušana sadales centrā*
    - **Pārkraušanas veidnes apraksts:** *51 Pārkraušana sadales centrā*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Darba veidnes informācija**.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Darba veids:** *Izdošana*
    - **Darba klases ID:** *Pārkraušana sadales centrā*

1. Atlasiet **Jauns**, lai pievienotu citu rindu, un iestatiet šādas vērtības:

    - **Darba veids:** *Izvietošana*
    - **Darba klases ID:** *Pārkraušana sadales centrā*

1. Atlasiet **Saglabāt** un apstipriniet, ka ir atlasīta rūtiņa **Derīgs** veidnei *51 Pārkraušana sadales centrā*.
1. Nav obligāti: atlasiet **Rediģēt vaicājumu**, ja vēlaties iestatīt kritērijus, lai kontrolētu, kad un kur tiek izmantota darba veidne.

    Vaicājumu var iestatīt, lai kontrolētu, kad tiek izmantota konkrētā darba veidne. Piemēram, varat norādīt, ka veidni var izmantot darbam tikai noteiktā vietā. Ja vēlaties, lai darba veidne pārkraušanai sadales centrā tiktu lietota noteiktā vietā, tās filtrēšana ir jāveic laukā **Sākuma novietojums**, nevis laukā **Novietojums**, jo saņemšanas procesu darba izveide (pirkšana, pārkraušana sadales centrā un papildināšana) sākas no izvietošanas rindas. Kad darbs ir izveidots, novietojuma direktīva iestata lauku **Novietojuma** uz izvietošanas novietojumu. Tomēr izdošanas vieta tiek glabāta laukā **Sākuma vieta**.

> [!NOTE]
> Darba klases ID *Izdošanas* un *Izvietošanas* darbu tipiem jābūt vienādiem.

### <a name="create-location-directives"></a>Novietojuma direktīvu izveide

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.
1. Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:

    - **Secības numurs:** *1*
    - **Nosaukums:** *51 Pārkraušana sadales centrā*
    - **Darba veids:** *Izvietošana*
    - **Vieta:** *5*
    - **Noliktava:** *51*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Rindas**.
1. Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **No daudzuma:** *1*
    - **Līdz daudzumam:** *1 000 000*

1. Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.
1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Nosaukums:** *Baydoor*
    - **Fiksēta novietojuma lietojums:** *Fiksētas un nefiksētas vietas*

1. Atlasiet **Saglabāt**, lai padarītu pogu **Rediģēt vaicājumu** rīkjoslā **Novietojuma direktīvu darbības** pieejamu.
1. Atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktoru.
1. Cilnē **Diapazons** pārliecinieties, ka šīs divas rindas ir konfigurētas:

    - 1. rinda:

        - **Tabula:** *Novietojumi*
        - **Atvasinātā tabula:** *Vietas*
        - **Lauks:** *Noliktava*
        - **Kritēriji:** *51*

    - 2. rinda:

        - **Tabula:** *Novietojumi*
        - **Atvasinātā tabula:** *Vietas*
        - **Lauks:** *Novietojums*
        - **Kritēriji:** *Baydoor*

1. Atlasiet **Labi**, lai aizvērtu vaicājuma lapu.

### <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Kreisās rūts izvēlnes elementu sarakstā atlasiet **Pirkumu izvietošana**.
1. Atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns**, lai pievienotu režģim rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Darba klases ID:** *Pārkraušana sadales centrā*
    - **Darba pasūtījuma tips:** *Pārkraušana sadales centrā*

1. Atlasiet **Saglabāt**.

## <a name="scenario"></a>Scenārijs

### <a name="create-a-purchase-order"></a>Pirkuma pasūtījuma izveide

Sekojiet šiem soļiem, lai izveidotu pirkuma pasūtījumu kā piegādes avotu.

1. Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:

    - **Tirgotāja konts:** *104*
    - **Noliktava:** *51*

1. Atlasiet **Labi** un pierakstiet pasūtījuma numuru.
1. Kopsavilkuma cilnei **Pirkuma pasūtījuma rindas** tiek pievienota jauna rinda. Iestatiet šādas vērtības šai rindai:

    - **Elementa numurs:** *A0001*
    - **Daudzums:** *5*

### <a name="create-a-sales-order"></a>Izveidot pārdošanas pasūtījumu

Sekojiet šiem soļiem, lai izveidotu pārdošanas pasūtījumu kā piegādes avotu.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Klienta konts:** *US-002*
    - **Noliktava:** *51*

1. Atlasiet **Labi**.
1. Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *3*

### <a name="create-planned-cross-docking"></a>Izveidot plānoto pārkraušanu sadales centrā

Sekojiet šiem soļiem, lai izveidotu plānoto pārkraušanu sadales centrā no pārdošanas pasūtījuma.

1. Lapā **Pārdošanas pasūtījuma detalizēta informācija** lapā tikko izveidotajam pārdošanas pasūtījumam atlasiet darbības rūtī cilnē **Noliktava** grupā **Darbības** atlasiet **Nodot izpildei noliktavā**.

    Darbība nodot noliktavā izveido sūtījumu un noslodzes rindu pārdošanas pasūtījuma rindai un mēģina piešķirt krājumus.
    
    Tiek parādīts informatīvs ziņojums. Tiek parādīts arī šāds brīdinājuma ziņojums: "Ar kopumu XXXX netika izveidots neviens darbs. Detalizētu informāciju meklējiet darba izveides vēstures žurnālā. " Šī darbība ir paredzama, jo noliktavā nav krājumu.

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** atlasiet **Detalizēta informācija par nosūtīšanu**.

    Tiek parādīta lapa **Detalizēta informācija par nosūtīšanu**, un tā parāda sūtījumu, kas tika izveidots pārdošanas pasūtījumam.

1. Kopsavilkuma cilnē **Noslodzes rindas** ievērojiet, ka **Plānotais pārkraušanas sadales centrā daudzums** ir iestatīts uz *3*. Tā kā noliktavā nav pieejami krājumi, bet derīgs piegādes avots ieradīsies laika loga ietvaros, kas ir definēts nosūtīšanas pārkraušanas veidnē, tika izveidots nosūtīšanas pārkraušanas daudzums.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet **Plānotā nosūtīšana-pārkraušana**, lai skatītu detalizētu informāciju par izveidoto nosūtīšanu-pārkraušanu.

## <a name="process-the-cross-docking"></a>Apstrādāt pārkraušanu sadales centrā

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Pirkuma pasūtījuma saņemšana, izmantojot noliktavas mobilo programmu

Sistēma saņems 5 elementu daudzumu no pirkuma pasūtījuma saņemšanas vietā un izveidos divus darba gabalus.

Pirmajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pārkraušana sadales centrā*, un tā ir saistīta ar pārdošanas pasūtījumu. Tā daudzums ir 3, un tas ir novirzīts uz galīgo nosūtīšanas vietu, lai to varētu nosūtīt nekavējoties.

Otrajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pirkuma pasūtījumi*, un tā ir saistīta ar pirkuma pasūtījumu. Tā atlikušais daudzums ir 2, kas netika nodots nosūtīšanai, un tas ir novirzīts izvietošanai noliktavā.

1. Pierakstieties mobilajā ierīcē kā lietotājs noliktavā *51*.
1. Doties uz **Ienākošie \> Pirkumu saņemšana**.
1. Laukā **PONum** ievadiet savu pirkuma pasūtījuma numuru.
1. Laukā **Daudzums** ievadiet *5*.
1. Atlasiet **Labi**.
1. Nākamajā lapā iestatiet lauku **Elements** uz *A0001*.
1. Atlasiet **Labi**.
1. Nākamajā lapā apstipriniet **PONum**, **Elements** un **Daudzums** vērtības, atlasot **Labi**.

    Tiek saņemts ziņojums "Darbība pabeigta".

1. Atlasiet **Atcelt**, lai izietu.

### <a name="put-away-to-cross-docking-and-bulk"></a>Nosūtīšanas-pārkraušanas un lielapjoma preču izvietošana

Patlaban abiem darba ID ir vienāda mērķa numura zīme. Lai veiktu nākamās darbības, ir jāiegūst darba ID un mērķa numura zīmes ID. Šo informāciju var iegūt no detalizētas informācijas par pirkuma pasūtījuma rindu un pārdošanas pasūtījuma rindu. Pārmaiņus varat doties uz **Noliktavas pārvaldība \> Darbs \> Darba detaļas** un filtrēt darbu, kur **Noliktavas** vērtība ir *51*.

1. Mobilajā ierīcē atveriet **Ienākošie \> Pirkumu izvietošana** un ievadiet mērķa numura zīmi no darba.
1. Laukā **ID** ievadiet mērķa numura zīmes ID no darba informācijas.

    Nosūtīšanas-pārkraušanas lapa ataino izdošanas vietu (*RECV*), mērķa numura zīmi (*numura zīmi*), krājumu (*A0001*) un daudzumu (*3*).

1. Atlasiet **Labi**.
1. Laukā **Mērķa LP** ievadiet mērķa numura zīmi numura zīmes ID, kas ir jānovieto (bez uzglabāšanas nosūtāms) uz nosūtīšanas vietu. Varat atlasīt jebkuru numura zīmes ID pēc savas izvēles.
1. Atlasiet **Labi**.
1. Laukā **ID** ievadiet mērķa numura zīmes ID.
1. Atlasiet **Labi**.
1. Apstipriniet darbu, izdodot atlikušo daudzumu 2, un pēc tam atlasiet **Labi**.
1. Nākamajā lapā atlasiet **Gatavs**, lai beigtu izdošanas procesu un sāktu izvietošanas procesu.

    Mobilajā programmā ir ietverta vieta un noliktavas numura zīme krājuma novietošanai.

1. Apstipriniet lielapjoma glabāšanas **Izvietošanu**, atlasot **Labi**.
1. Nākamajā lapā apstipriniet nosūtīšanai bez uzglabāšanas **Izvietošanu**, atlasot **Labi**.

    Tiek saņemts ziņojums "Darbība pabeigta".

1. Atlasiet **Atcelt**, lai izietu.

Sekojošajā attēlā ir parādīts, kā programmā Microsoft Dynamics 365 Supply Chain Management var tikt parādīts aizpildīts nosūtīšanas bez uzglabāšanas darbs.

![Nosūtīšanas bez uzglabāšanas darbs ir pabeigts.](media/PlannedCrossDockingWork.png "Nosūtīšanas bez uzglabāšanas darbs ir pabeigts")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
