---
title: Papildināšana, pārsniedzot vietas ietilpību
description: Šajā tēmā ir sniegta informācija par funkciju Papildināšana, pārsniedzot vietas ietilpību. Šī funkcija ļauj veikt visus papildināšanas darbus, kas būs nepieciešami šīs dienas izveidošanai, un pārvalda šī papildināšanas darba pieejamību, lai nodrošinātu, ka saņemšanas vieta neizbeidzas krājumi un tā nepārsniedz noslodzi.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: d337c9ab01f86fa7f1b2cbd80674ccf6783f637b98cd26c838a6e44e287b2c7e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744610"
---
# <a name="replenishment-over-location-capacity"></a>Papildināšana, pārsniedzot vietas ietilpību

[!include [banner](../includes/banner.md)]

Dažām lielizmēra noliktavām vai noliktavām ar ierobežotu telpu ir jānosūta vairāk krājuma daudzumu dienā, nekā tas ietilptu izdošanas vietā. *Papildināšana, pārsniedzot vietas ietilpību* funkcija ļauj veikt visus papildināšanas darbus, kas būs nepieciešami šīs dienas izveidošanai, un pārvalda šī papildināšanas darba pieejamību, lai nodrošinātu, ka saņemšanas vieta neizbeidzas krājumi un tā nepārsniedz noslodzi.

Funkcija ļauj izveidot papildu papildināšanas darbu, nekā tas ietilptu atrašanās vietā, un tas bloķē papildināšanas darbus no pabeigšanas, ja vieta ir pilna. Tā kā krājumu līmenis izdošanas vietā nokrītas zem konfigurējama sliekšņa, tiek darīts lielāks papildināšanas darbs.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Ieslēgt Papildināšana, pārsniedzot vietas ietilpību funkciju

Lai padarītu šo līdzekli pieejamu, aktivizējiet tālāk norādītos līdzekļus [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (šādā secībā):

1. Organizācijas mēroga darba aizturēšana
1. Papildināšana, pārsniedzot vietas ietilpību

## <a name="set-up-the-feature-for-the-example-scenario"></a>Iestatīt līdzekli piemēra scenārijam

Šajā sadaļā ir sniegti norādījumi un piemērs, kas parāda, kā iestatīt šo funkciju un sagatavot parauga datus piemēru scenārijam, kas sniegts tālāk šajā tēmā.

### <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai, izmantojot šo [scenārija piemēru](#example-scenario), strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

### <a name="location-profile"></a>Novietojuma profils

Iespējot papildināt, pārsniedzot vietas ietilpību, funkcionalitāti novietojumu profilā.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojumu profili**.
1. Kreisajā rūtī atlasiet **PICK-06**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Papildināšana** iestatiet šādas vērtības:

    - **Pārsniegt novietojuma noslodzi:** *Jā*

        Iespējojot, tiks atļauts pārsniegt vietas maksimālo noslodzi, izmantojot papildināšana darbu. Tas arī iespējo citus laukus kopsavilkuma cilnē **Papildināšana**.

    - **Darba pieejamības sliekšņa tips:** *Daudzums*

        Šis lauks definē metodi, kas tiek izmantota, lai noteiktu, kad ir jānodod vairāk darba. Varat atbrīvot vai nu pēc daudzuma, vai procentiem:

        - *Procenti* – Atlasiet šo opciju, lai izmantotu procentuālo noslodzi, kas ir balstīta uz krājumu ierobežojumiem vai tilpumiem. Atlasot šo opciju, tiek aktivizēts **Pārpildes procentu** lauks un tiek atspējoti divi ar daudzumu saistīti lauki **Pārpildes daudzums** un **Pārpildes vienība**.

            Šo opciju var izmantot, ja izdošanas vietas izmanto tilpumus.

            Ja šī opcija ir atlasīta, iestatiet **Pārpildes procentu** lauku uz procentuālo daļu, pie kuras papildu papildināšanas darbs būs pieejams.

        - *Daudzums* - Atlasiet šo opciju, lai izmantotu specifisku daudzuma vērtību. Atlasot šo opciju, tiek deaktivizēts **Pārpildes procentu** lauks un tiek iespējoti lauki **Pārpildes daudzums** un **Pārpildes vienība**.

            Izmantojiet šo opciju, ja nelietojat apjoma datus par novietojumiem, kuri tiek papildināti, vai ja jums ir nemainīgi daudzumi, par kuriem vēlaties, lai uz vietas tiktu nogādāti vairāk krājumu.

           Ja šī opcija ir atlasīta, iestatiet **Pārpildes daudzumu** un **Pārpildes vienības** laukus uz daudzumu un mērvienību, kādā būs pieejams papildu papildināšanas darbs.

    - **Pārpildes daudzums:** *0.65*

        Šis lauks nosaka daudzumu, pie kura notiek novietojuma pārplūšana.

        Darbs būs pieejams ikreiz, kad rīcībā esošo daudzumu summa novietojumā un darba daudzums būs zemāks par šo vērtību. Jebkurš papildināšanas darbs virs šīs vērtības tiks bloķēts, un tas būs jāatbloķē manuāli.

        Novietojuma krājumu limiti tiek ņemti vērā, aprēķinot darba daudzumu.

    - **Pārpildes vienība:** *PL*

        Šis lauks nosaka vienību, kas ir saistīta ar pārpildes daudzumu.

        Šādā gadījumā papildu papildināšanas darbs būs pieejams, kad novietojumā līmenis samazinās uz 0,65 paletēm (PL).

    - **Pārpildes procentuālā vērtība**

        Šis lauks nosaka procentuālo daudzumu, pie kura notiek novietojuma pārplūšana.

        Darbs būs pieejams ikreiz, kad rīcībā esošo daudzumu summa novietojumā un darba daudzums būs zemāks par šo procentuālo daudzumu. Jebkura papildināšanas darba daudzuma procentuālā vērtība virs šīs vērtības tiks bloķēta, un tā būs jāatbloķē manuāli.

        Novietojuma krājumu limiti tiek ņemti vērā, aprēķinot darba procentuālo daudzumu. Ja nav definēts neviens rīcībā esošo krājumu ierobežojums, darba daudzuma procentuālā vērtība tiks aprēķināta pēc tilpuma, ja novietojuma profilā ir definēti tilpuma ierobežojumiem.

> [!IMPORTANT]
> Ja jūs izmantojat demonstrācijas datus **USMF** juridiskajai personai un iepriekš ieslēdzāt *Novietojuma numura zīmes pozicionēšanas* līdzekli, jums ir jāizslēdz opcija **Iespējot numura zīmes pozicionēšanas** iestatījumu **BULK-06** novietojuma profilā, lai pabeigtu mobilās darbības piemēru scenārijā.

### <a name="wave-step-code"></a>Kopuma darbības kods

> [!NOTE]
> Lai iestatītu kopuma soļa kodu atbilstoši šeit aprakstītajam, varat vispirms izmantot [funkciju pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu līdzekli vārdā *Organizācijas plašu kopuma soļa kods*.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma darbību kodi**.
1. Atlasiet **Jauns**, un iestatiet šādas vērtības:

    - **Kopuma darbības kods:** *Replen*
    - **Kopuma darbības apraksts:** *Papildināšana*
    - **Kopuma darbības veids:** *Papildināšana*

1. Atlasiet **Saglabāt**.

### <a name="replenishment-template"></a>Papildināšanas veidne

Papildināšanas veidnes ir kārtulu kopa, kas kontrolē novietojuma papildināšanas laiku un veidu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Sadaļā **Pārskats** atlasiet rindu, kur lauks **Papildināt veidni** ir iestatīts uz *Pieprasīt papildināšanu*.
1. Iestatiet šādas vērtības:

    - **Kopuma darbības kods:** *Replen*
    - **Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus** — *Jā*

1. Atlasiet **Saglabāt**.

### <a name="wave-template"></a>Kopuma veidne

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Kreisajā rūtī lauku **Kopuma veidnes tips** iestatiet vērtību *Sūtīšana*.
1. Atlasiet sarakstā veidni **61 Sūtīšana**
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Automātiskās papildināšanas darba laidiens** uz *Jā*.

    Iestatiet šo opciju uz *Jā*, lai izveidotu uz pieprasījuma balstītu papildināšanas darbu un automātiski to izlaistu. Jums ir jāpievieno papildināšanas kopuma metode kopuma veidnei un jāizveido papildināšanas veidne **Kopuma pieprasījuma** tipam. Iestatiet papildināšanas veidni lapā **Papildināšanas veidnes**. Lai iestatītu papildināšanas veidni, ir jāpievieno papildināšanas metode laidiena veidnei.

1. Kopsavilkuma cilnē **Metodes** kolonnā **Atlasītās metodes** atrodama šāda rinda:

    - **Metodes nosaukums:** *papildināt*
    - **Nosaukums:** *Papildināšana*

1. Iestatiet lauku **Kopuma soļa kods** šai rindai uz *Replen*.
1. Atlasiet **Saglabāt**.

## <a name="example-scenario"></a>Piemēra situācija

Pēc tam, kad esat veicis visus iepriekš aprakstītos, pieejamos parauga datus un to iestatījis, varat strādāt ar šo scenāriju, lai izmēģinātu *Papildināšana, pārsniedzot vietas ietilpību* funkciju. Šajā scenārijā parādītās vērtības pieņem, ka strādājat ar standarta demonstrācijas datiem, ar kuriem atlasījāt **USMF** juridisko personu un ka sagatavojāt parauga ierakstus, kas ir aprakstīti iepriekš šajā tēmā. Šis scenārijs kalpo arī kā piemērs, kas parāda, kā līdzekli var izmantot ražošanas iestatījumā.

### <a name="create-replenishment-work"></a>Izveidot papildināšanas darbu

#### <a name="create-sales-order-1"></a>1. pārdošanas pasūtījuma izveide

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**, lai atvērtu dialoglodziņu jauna pārdošanas pasūtījuma izveidošanai.
1. Dialoglodziņā iestatiet tālāk norādītās vērtības:

    - **Debitora konts:** *US-007*
    - **Noliktava:** *61*

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta jauna, tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *T0100*
    - **Daudzums:** *40*

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt vietu**.
1. Aizvērt lapu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Tiks saņemts informatīvi ziņojumi, kurā norādīts izveidotais kopuma ID un sūtījuma ID. Tiek izveidots arī papildināšanas kopums.

    Jūs saņemat arī brīdinājuma ziņojumu, kurā teikts: "Darba ID XXXX nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."

#### <a name="create-sales-order-2"></a>2. pārdošanas pasūtījuma izveide

1. Lapā **Visi pārdošanas pasūtījumi** atlasiet **Jauns**, lai atvērtu dialoglodziņu jauna pārdošanas pasūtījuma izveidošanai.
1. Dialoglodziņā iestatiet tālāk norādīto vērtību:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *61*

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta jauna, tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *T0100*
    - **Daudzums:** *60*

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt vietu**.
1. Aizvērt lapu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Tiks saņemts informatīvi ziņojumi, kurā norādīts izveidotais kopuma ID un sūtījuma ID. Tiek izveidots arī papildināšanas kopums.

    Jūs saņemat arī brīdinājuma ziņojumu, kurā teikts: "Darba ID XXXX nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."

#### <a name="create-sales-order-3"></a>3. pārdošanas pasūtījuma izveide

1. Lapā **Visi pārdošanas pasūtījumi** atlasiet **Jauns**, lai atvērtu dialoglodziņu jauna pārdošanas pasūtījuma izveidošanai.
1. Dialoglodziņā iestatiet tālāk norādītās vērtības:

    - **Debitora konts:** *US-004*
    - **Noliktava:** *61*

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta jauna, tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *T0100*
    - **Daudzums:** *30*

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt vietu**.
1. Aizvērt lapu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

    Tiks saņemts informatīvi ziņojumi, kurā norādīts izveidotais kopuma ID un sūtījuma ID. Tiek izveidots arī papildināšanas kopums.

    Jūs saņemat arī brīdinājuma ziņojumu, kurā teikts: "Darba ID XXXX nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."

#### <a name="view-work-details"></a>Skatīt detalizētu informāciju par darbu

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Sadaļā **Pārskats** filtrējiet **Noliktavas** kolonnu noliktavai *61*.
1. Ir jāredz, ka trīs pieprasījumu pārdošanas pasūtījumiem tika izveidoti septiņi darba ID.

    - Trijiem no septiņiem darba ID ir **Darba pasūtījuma tipa** vērtība no *Papildināšanas*, un četriem ir **Darba pasūtījuma tipa** vērtība no *Pārdošanas pasūtījumiem*.
    - Visiem trim darbu ID, kuru **Darba pasūtījuma tipa** vērtība no *Papildināšanas* ir vienāda ar *Saņemšanu* un *Izvietošanu* sadaļā **Rindas**:

        - **Saņemt:** *02A01R5S1B*
        - **Izvietot:** *06A01R2S1B*

    - Pārdošanas pasūtījumam 1 tika izveidoti divi darba ID.

1. Pierakstiet darba ID katram pārdošanas pasūtījumam.

Atkarībā no rīcībā esošajiem daudzumiem izveidotie darba daudzumi var nedaudz atšķirties. Tomēr kopumā izveidotajiem darba virsrakstiem ir jāatbilst šim scenārija paraugam.

#### <a name="on-hand-inventory-license-plate-id"></a>Rīcībā esošo krājumu numura zīmes ID

Vēlāk šajā scenārijā jūs izmantosiet Warehouse Management mobile programmu (vai emulatoru), kur ir jāidentificē numura zīme, lai pabeigtu izdošanas un papildināšanas scenārijus.

Lai atrastu numura zīmes ID, kas būs nepieciešams vēlāk, veiciet sekojošās darbības.

1. Dodieties uz **Krājumu vadība \> Uzziņas un atskaites \> Rīcībā esošie krājumu saraksts**.
1. Atlasiet pogu **Rādīt filtrus**, lai atvērtu filtra rūti.
1. Lai iegūtu scenārijam numura zīmes, ievadiet tālāk norādītos filtrēšanas kritērijus. Izmantojiet filtru *sākt ar*.

    - **Krājuma numurs:** *T0100*
    - **Noliktava:** *61*

1. Atlasiet **Lietot**.
1. Darbību rūtī atlasiet **Dimensijas**.
1. Dialoglodziņā **Dimensiju rādīšana** sadaļā **Noliktavas dimensijas** atlasiet visas vērtības.
1. Sadaļā **Darbības** atlasiet **Krājuma kods** un **Daudzums \<\> 0**.
1. Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. **Rīcībā esošais** režģis rāda unikāls noliktavas vienības identifikatorus krājumam *T0100* katrā novietojumā. Pierakstiet numura zīmi, kas atrodas katrā novietojumā, jo šī informācija būs nepieciešama vēlāk.
1. Aizvērt lapu.

### <a name="process-steps"></a>Procesa darbības

Pirmajos divos darba ID tiks veikta noliktavas novietojuma papildināšana. Darbs pie trešā papildināšanas darba tiks bloķēts, līdz krājumu līmenis izdošanas vietā nokrītas zem sliekšņa.

#### <a name="replenishment"></a>Papildināšana

1. Pierakstieties Warehouse Management mobile programmā kā lietotājs noliktavā *61*. (Ievadiet *61* kā lietotāja ID un *1* kā paroli.)
1. Doties uz **Krājumi \> Papildināšana**.

    Jūs tiekat aicināts pabeigt pirmo papildināšanas darbu. Tiek parādīts krājuma kods, daudzums, novietojumu, no kura izdot.

1. Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.
1. Atlasiet pogu **Labi** (atzīmes simbols).

    Sistēma ģenerē mērķa unikālo noliktavas vienības identifikatoru jaunajai numura zīmei izdotajam krājumam.

1. Lai apstiprinātu vērtību, atlasiet **Labi**.

    Izvietošanas darbs, kas uzdod lietotājam izvietot mērķa numura zīmi papildināšanas novietojumā. *Izvietošanas* novietojumam jābūt **06A01R2S1B**.

1. Apstipriniet detalizētu informāciju par izvietošanu un atlasiet **Labi**.

    Tiek parādīts ziņojums "Darbs pabeigts" un nākamās papildināšanas izdošanas uzdevuma detaļas: krājuma numurs, daudzums un novietojums, no kura izvieto. Izvietošanas novietojums būs vienāds ar pirmo papildināšanas novietojumu. Tāpēc numura zīmei būs tas pats numura zīmes ID, kas tika izmantots pirmajam papildināšanas darba uzdevumam.

1. Atkārtojiet iepriekšējās darbības, lai pabeigtu otrā darba uzdevuma papildināšanas darbu. Daudzums un mērķa numura zīme atšķirsies no daudzuma un mērķa numura zīmes pirmajam darba uzdevumam.

Kad otrais papildināšanas darbs ir pabeigts, jūs saņemat ziņojumu "Darbs pabeigts". Mobilā ierīce arī informē, ka nav pieejams darbs, kaut arī saglabājas daži papildināšanas darbi. Šī problēma rodas tādēļ, ka papildināšanas darbam ir *Aizturēts* pieejamības statuss, tāpēc tas ir atzīmēts kā **Bloķēts**.

*Aizturētais* statuss tika izraisīts, jo novietojuma profils saņemšanas novietojumam, kuram darbs tiek piešķirts, ir **Pārpildes daudzuma** vērtība *0,65 PL*. Divi iepriekšējie papildināšanas darba uzdevumi pildīja atrašanās vietu gandrīz līdz tā pārpildes ierobežojumam krājumam *T0100*. (Vienības pārveidošana krājumam ir *1 PL = 100 ea*.) Tāpēc atlikušā papildināšanas darba rezultātā novietojums pārsniegtu pārpildes robežu.

Kamēr no novietojuma netiks izdots pietiekami daudz krājumu, lai mobilās ierīces izvēlnes vienumā tas nepārsniegtu darba atbrīvošanas slieksni, šis papildināšanas darbs paliks bloķēts.

#### <a name="sales-order-pick"></a>Pārdošanas pasūtījums saņemšana

Pirms atlikušo papildināšanas darba uzdevumu var pabeigt, izdošanas novietojums ir jāsamazina līdz līmenim, kurā atlikušo papildināšanas darbu var atbloķēt. Citiem vārdiem sakot, rīcībā esošo krājumu daudzuma summa novietojumā un papildināšanas daudzums nedrīkst pārsniegt **Pārpildes daudzuma** vērtību. Ja šī summa ir mazāka nekā pārpildes daudzums, atlikušais papildināšanas darbs tiks atbloķēts.

1. Pierakstieties Warehouse Management mobile programmā kā lietotājs noliktavā *61*. (Ievadiet *61* kā lietotāja ID un *1* kā paroli.)
1. Doties uz **Izejošs \> Pārdošanas saņemšana**.
1. Ievadiet pirmo darba ID pārdošanas pasūtījumam 1.

    Skatiet to pārdošanas pasūtījumu darba ID, kurus esat veicis iepriekš **Darba informācijas** lapā. Šeit ievadītais darba ID ģenerēs izdošanas darbu daudzumam 10 EA no diviem atsevišķiem novietojumiem.

1. Atlasiet **Labi**.

    Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums, no kura izvēlēties pirmo atrašanās vietu.

1. Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.
1. Atlasiet pogu **Labi** (atzīmes simbols).

    Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums, no kura izvēlēties nākamo atrašanās vietu.

1. Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.
1. Atlasiet pogu **Labi** (atzīmes simbols).

    **Pārdošanas pasūtījumi: izdošana** lapa, kas dod jums iespēju izdot abus pabeigtos saņemšanas darbus uz izejošo sagatavošanas posmu norises vietu.

1. Atlasiet **Labi**.

    Tiek saņemts ziņojums "Darbība pabeigta".

1. Ievadiet otro darba ID pārdošanas pasūtījumam 1.

    Šim darba ID ir tikai viens saņemšanas uzdevums.

1. Atlasiet **Labi**.

    Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums.

1. Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.

    Norādītā numura zīme būs viena no sistēmas ģenerētajām numura zīmēm no papildināšanas darba uzdevumiem. Lai pārliecinātos, ka uztverat pareizo numura zīmes ID, pārbaudiet krājumus **Rīcībā esošā saraksta** lapā krājumam, novietojumam un daudzumam.

1. Atlasiet pogu **Labi** (atzīmes simbols).
1. Apstipriniet norādījumus par izdošanas uzdevumu uz izejošo sagatavošanas posmu novietojumu.
1. Atlasiet **Labi**.

    Tiek saņemts ziņojums "Darbība pabeigta".

Pārdošanas pasūtījums 2 ir bloķēts no saņemšanas, jo papildināšanas uzdevums, ar kuru tas ir saistīts, nav pabeigts. Pašlaik izdošanas vietā joprojām ir 30 ea daudzums, un pārdošanas pasūtījumam 2 papildināšanas daudzums ir 60 EA. Rīcībā esošo krājumu un papildināšanas krājumu summa (90 ea) pārsniedz pārpildes daudzumu 0,65 PL (vai 65 ea). Pirms papildināšanas darbu var pabeigt, ir jāsaņem pārdošanas pasūtījums 3.

1. Ievadiet darba ID pārdošanas pasūtījumam 3.

    Šim darba ID ir tikai viens saņemšanas uzdevums.

1. Atlasiet **Labi**.

    Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums.

1. Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.

    Norādītā numura zīme būs viena no sistēmas ģenerētajām numura zīmēm no papildināšanas darba uzdevumiem. Lai pārliecinātos, ka uztverat pareizo numura zīmes ID, pārbaudiet krājumus **Rīcībā esošā saraksta** lapā krājumam, novietojumam un daudzumam.

1. Atlasiet pogu **Labi** (atzīmes simbols).
1. Apstipriniet norādījumus par izdošanas uzdevumu uz izejošo sagatavošanas posmu novietojumu.
1. Atlasiet **Labi**.

    Tiek saņemts ziņojums "Darbība pabeigta".

Tiklīdz rīcībā esošo krājumu summa saņemšanas vietā un papildināšanas daudzums ir zem robežas, būs iespējams apstrādāt atlikušo papildināšanas darbu.

Atgriezieties **Darba informācijas** lapā un ievērojiet, ka papildināšanas darba pieejamība pēdējai papildināšanas vienībai (pārdošanas pasūtījumam 2) ir *Atvērta*, jo atrašanās vietā tagad ir pietiekami daudz vietas, lai akceptētu papildināšanu.

Tagad varat apstrādāt šo papildināšanas darbu ar mobilās ierīces starpniecību.

1. Doties uz **Krājumi \> Papildināšana**.

    Jūs tiekat aicināts pabeigt atlikušo papildināšanas darbu. Tiek parādīts krājuma kods, daudzums, novietojumu, no kura izdot.

1. Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.
1. Atlasiet pogu **Labi** (atzīmes simbols).

    Sistēma ģenerē mērķa unikālo noliktavas vienības identifikatoru jaunajai numura zīmei izdotajam krājumam.

1. Lai apstiprinātu vērtību, atlasiet **Labi**.

    Izvietošanas darbs, kas uzdod lietotājam izvietot mērķa numura zīmi papildināšanas novietojumā. *Izvietošanas* novietojumam jābūt **06A01R2S1B**.

1. Apstipriniet detalizētu informāciju par izvietošanu un atlasiet **Labi**.

    Tiek saņemti ziņojumi "Darbs pabeigts" un "Nav pieejams darbs".

Tagad varat saņemt 2. pārdošanas pasūtījums. Tas kļuva atbloķēts, kad tika pabeigts papildināšanas darbs, kas ir saistīts ar pārdošanas pasūtījumu.

1. Ievadiet darba ID 2. pārdošanas pasūtījumam.

    Šim darba ID ir tikai viens saņemšanas uzdevums.

1. Atlasiet **Labi**.

    Uzdevumu lapā **Pārdošanas pasūtījumi: saņemšana** ir norādīts krājuma numurs, daudzums un novietojums.

1. Laukā **LP** ievadiet krājuma unikālo noliktavas vienības identifikatoru, kas atrodas parādītajā novietojumā.

    Norādītā numura zīme būs sistēmas ģenerētā numura zīme no papildināšanas darba uzdevuma. Lai pārliecinātos, ka uztverat pareizo numura zīmes ID, pārbaudiet krājumus **Rīcībā esošā saraksta** lapā krājumam, novietojumam un daudzumam.

1. Atlasiet pogu **Labi** (atzīmes simbols).
1. Apstipriniet norādījumus par izdošanas uzdevumu uz izejošo sagatavošanas posmu novietojumu.
1. Atlasiet **Labi**.

    Tiek saņemts ziņojums "Darbība pabeigta".

## <a name="notes-and-tips"></a>Piezīmes un padomi

- Šī funkcionalitāte darbojas ar visiem papildināšanas tipiem: kopuma pieprasījums, min/max, noslodzes pieprasījums un slotēšana.
- Ja vēlaties, varat manuāli ignorēt papildināšanas darba pieejamību katram darba virsrakstam no **Darba informācijas** lapas.
- Kad sistēma iestata papildināšanas darba pieejamību, tā ņem vērā visus krājumus, kas jau ir novietojumā, pirms darbs ir pabeigts
- Katra pārdošanas pasūtījuma darba daļa ir saistīta ar specifisku papildināšanas darbu. Nav atbilstošas pārdošanas darba pieejamības funkcionalitātes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]