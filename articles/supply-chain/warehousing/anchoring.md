---
title: Noenkurošana
description: Šajā tēmā paskaidrots, kā iespējot un lietot enkurošanu.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505586"
---
# <a name="anchoring"></a>Noenkurošana

[!include [banner](../includes/banner.md)]

Šajā tēma sniegta informācija par enkurošanas procedūru. Tajā aprakstīta konfigurācija, kura ir vajadzīga, un loģika, kura tiek palaista, kad noliktavas darbinieks nomaina vai nu izstādīšanas vietu vai iekraušanas vietu.

Enkurošanas līdzeklis ļauj pārlabot izstādīšanas vai iekraušanas vietu. Visi atvērtie nolikumi pēc tam tiks pārvirzīti uz jauno izstādīšanas vai iekraušanas vietu, kuru būsi norādījuši.

Šis līdzeklis palīdz darbiniekiem būt efektīvākiem, sūtot preces. Daži piemēri:

- Ja darbiniekam ir jānovieto 1. pasūtījuma krājumi sagatavošanas posma novietojumā pie 1. doka, viņš nevar to izdarīt, jo no novietojuma vēl nav paņemta iepriekšējā krava. Tā vietā, lai gaidītu, kamēr kļūs pieejams 1. doka sagatavošanas posma novietojums, darbinieks var izlemt izmantot 2. doka sagatavošanas posma novietojumu. Šādā gadījumā darbinieks ignorē ieteikto sagatavošanas posma novietojumu. Visu darba pasūtījuma atlikušo krājumu izvietošanas novietojums tiek atjaunināts uz 2. doka sagatavošanas posma novietojumu.
- Darbinieks, kuram vienai piegādei jāveic vairākas saņemšanas, var pārliecināties, ka visi noliktie krājumi tiek salikti vienuviet. Tādējādi ir vajadzīgs mazāk laika, lai iekrautu preces kravas automašīnā.

Enkurojuma konfigurēšana mobilo ierīču izvēlnes elementiem veic, izmantojot opciju **Enkurot**. Ja iestatāt šo opciju uz *Jā*, jūs varat lietot lauku **Enkurot pēc**, lai norādītu, vai vēlaties enkurot pēc sūtījuma vai pēc kravas. Ja iestatāt lauku **Enkurot pēc** uz vērtību *Sūtījums*, turpmāki atvērtie nolikumi tiks mainīti uz jauno attiecīgā sūtījuma vietu. Ja iestatāt to uz vērtību *Krava*, turpmāki atvērtie nolikumi tiks mainīti uz šīs kravas jauno vietu.

> [!IMPORTANT]
> Turpmāku atvērto nolikumu vieta tiks mainīta tikai tajās darba rindās, kuras ir ģenerētas no vienas un tās pašas darba veidnes rindas. Citiem vārdiem sakot, sistēma enkuros nolikuma rindas, kuras ceļas no vienas un tās pašas darba veidnes rindas.

Šajā tēmā sniegts scenārijs, kurā parādīts, kā darbojas enkurošana. Scenārija laikā jūs izveidosiet pārdošanas pasūtījumu kopu un izlaidīsiet to noliktavā. Pēc tam tiks pārlabota piedāvātā izstādīšanas vieta un pārbaudīts, ka visi atlikušie izvietošanas darbi ir novirzīti uz jauno vietu.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Scenārija priekšnosacījums: padarīt pieejamus demonstrācijas datus

Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu *USMF*, pirms sākat darbu.

## <a name="scenario-setup"></a>Scenāriju iestatīšana

Pirms strādājat ar piemēra scenāriju, jums ir jāiespējo enkurošana attiecīgajai mobilās ierīces izvēlnes vienībai.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Mobilās ierīces izvēlnes vienuma iestatīšana, lai iespējotu enkurošanu.

Izpildiet tālāk norādītās darbības, lai iespējotu mobilās ierīces izvēlnes vienuma enkurošanu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Saraksta rūtī atlasiet ierakstu ar nosaukumu *Pārdošnas izdošana*. Ja nevienam esošam ierakstam nav šī nosaukuma, izveidojiet to. Apstipriniet vai iestatiet ierakstam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Pārdošanas izdošana*
    - **Nosaukums:** *Pārdošanas izdošana*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Jā*
    - **Noteikts:** *Lietotāja noteikts*
    - **Enkurošana:** *Jā*

        Šis iestatījums liek sistēmai enkurot kopā vairākas darba pasūtījuma rindas pārdošanas izdošanas laikā.

    - **Enkurot pēc:** *Krava*

        Šis iestatījums liek sistēmai enkurot pēc kravas.

    - **Ignorēt mērķa noliktavas vienību:** *Jā*
    - **Ignorēt numura zīmi izvietošanas laikā:** *Jā*
    - **Lietotājs, kurš bloķējis darbu:** *Jā*
    - **Atļaut pārmērīgu izdošanu:** *Jā*

### <a name="set-up-a-work-template-to-enable-staging"></a>Iestatiet darba veidni, lai iespējotu izstādīšanu

Izpildiet tālāk norādītās darbības, lai konfigurētu darba veidni, lai iespējotu izstādīšanu. Šī konfigurācija atbalstīs scenāriju, kurā darbiniek noliek vienumus pasūtījuma izstādīšanas vietā.

1. Doties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Darba veidnes**.
1. Laukā **Darba pasūtījuma veids** atlasiet *Pārdošanas pasūtījumi*.
1. Režģī atlasiet darba veidni **61 SO Stage**.
1. Sadaļā **Darba veidnes informācija** pārliecinieties, ka pastāv šādas rindas un ka tās ir konfigurētas, kā parādīts:

    - 1. rinda:

        - **Darba veids:** *Izdošana*
        - **Obligāts:** atlasīts (= *Jā*)
        - **Darba klases ID:** *SO Izdošana*

    - 2. rinda:

        - **Darba veids:** *Izvietošana*
        - **Obligāts:** atlasīts (= *Jā*)
        - **Direktīvas kods:** *Posms*
        - **Darba klases ID:** *SO Izdošana*

    - 3. rinda:

        - **Darba veids:** *Izdošana*
        - **Obligāts:** atlasīts (= *Jā*)
        - **Apturēt darbu:** *Jā*
        - **Darba klases ID:** *SO krava*

    - 4. rinda:

        - **Darba veids:** *Izvietošana*
        - **Obligāts:** atlasīts (= *Jā*)
        - **Direktīvas kods:** *Baydoor*
        - **Darba klases ID:** *SO krava*

1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma redaktoru.
1. Cilnē **Diapazons** pārliecinieties, ka ir klātesoša šī rinda:

    - **Tabula:** *Pagaidu darba darbības*
    - **Atveidotā tabula:** *Pagaidu darba darbības*
    - **Lauks:** *Noliktava*
    - **Kritēriji:** *61*

1. Cilnē **Kārtošana** pārliecinieties, ka ir klātesoša šī rinda:

    - **Tabula:** *Pagaidu darba darbības*
    - **Atveidotā tabula:** *Pagaidu darba darbības*
    - **Lauks:** *Sūtījuma ID*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**, lai piemērotu iestatījumus un aizvērtu vaicājumu redaktoru. Apstipriniet izmaiņas, ja to prasa vednis.
1. Darbību rūtī atlasiet **Darba galvenes pārtraukumi**.
1. Rindā, kur lauks **Lauka nosaukums** ir iestatīts uz *Sūtījuma ID*, pārliecinieties, ka ir atzīmēta izvēles rūtiņa **Grupēt pēc šī lauka**.

### <a name="set-up-license-plates-locations-and-inventory"></a>Iestatiet numura zīmes, atrašanās vietas un krājumus

Pirms pārdošanas pasūtījumu un sūtījumu izveides, ir jāpārliecinās, vai pastāv vajadzīgās vietas, numura zīmes un krājumi.

1. Dodoties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Numura zīmes un izveidojiet divas numura zīmes:**.

    - MyLP1
    - MyLP2

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Atrašanās vietas** un izveidojiet šādas vietas, ja tās jau nav klātesošas.

    | Noliktava | Novietojums   | Atrašanās vietas profila ID | Zonas ID   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | STĀVS     |
    | 61        | 06A01R3S1B | PICK-06             | STĀVS     |
    | 61        | STAGE01    | STAGE               | *(Tukšs)* |
    | 61        | STAGE02    | STAGE               | *(Tukšs)* |
    | 61        | STAGE03    | STAGE               | *(Tukšs)* |
    | 61        | STAGE04    | STAGE               | *(Tukšs)* |

1. Pārliecinieties, ka ir pieejams šāds krājums. Pielāgojot krājumus, varat izveidot manuālo kustību, izmantot papildināšanu vai jebkuru citu plūsmu.

    | Krājums | Daudzums | Noliktava | Novietojums   | Numura zīme |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Pieprasījuma izveide

Pirms varat izmēģināt enkurošanas funkcionalitāti, ir jāizveido pieprasījums. Šim scenārijam izveidosit trīs pārdošanas pasūtījumus vienam un tam pašam klientam.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu pirmo pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *61*

1. Atlasiet **Labi**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta tukša rinda kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *1*

1. Rīkjoslā atlasiet **Pievienot rindu**, lai pievienotu otro pārdošanas pasūtījuma rindu un tai iestatītu šādas vērtības:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *1*

1. Izpildiet šīs darbības katrai pasūtījuma pārdošanas rindai, lai rezervētu tai krājumus:

    1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet pārdošanas pasūtījuma rindu.
    1. Rīkjoslā atlasiet **Krājums \> Rezervācija**.
    1. Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.
    1. Darbību rūtī atlasiet **Saglabāt**.

1. Atkārtojiet no 2. līdz 6. solim, lai izveidotu otro pārdošanas pasūtījumu. Iestatiet rindai šādas vērtības:

    - Dialoglodziņā **Izveidot pārdošanas pasūtījumu**:

        - **Debitora konts:** *US-001*
        - **Noliktava:** *61*

    - Pārdošanas pasūtījuma 1. rindā:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *2*

    - Pārdošanas pasūtījuma 2. rindā:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *2*

1. Atkārtojiet 7. darbību, lai rezervētu katru rindu 2. pārdošanas pasūtījumam.
1. Atkārtojiet no 2. līdz 6. solim, lai izveidotu trešo pārdošanas pasūtījumu. Iestatiet rindai šādas vērtības:

    - Dialoglodziņā **Izveidot pārdošanas pasūtījumu**:

        - **Debitora konts:** *US-001*
        - **Noliktava:** *61*

    - Pārdošanas pasūtījuma 1. rindā:

        - **Krājuma numurs:** *A0001*
        - **Daudzums:** *3*

    - Pārdošanas pasūtījuma 2. rindā:

        - **Krājuma numurs:** *A0002*
        - **Daudzums:** *3*

1. Atkārtojiet 7. darbību, lai rezervētu katru rindu 3. pārdošanas pasūtījumam.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Izmantojiet noslodzes plānošanas darbvietu, lai izveidotu kravu un nodotu to noliktavā

Lai izveidotu kravu pasūtījumiem, kurus izveidojāt šim scenārijam, un pēc tam izlaistu to noliktavā, rīkojieties šādi.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.
1. Cilnē **Pārdošanas rindas** meklējiet un atlasiet visas pārdošanas pasūtījuma rindas 1. un 2. pārdošanas pasūtījumam.
1. Darbību rūtī cilnē **Piedāvājums un pieprasījums** grupā **Pievienot**, atlasiet **Jaunai kravai**.
1. Dialoglodziņā **Noslodzes veidnes piešķire** laukā **Noslodzes veidnes ID** atlasiet noslodzes veidni, piemēram, *Stnd noslodzes veidne*.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Sadaļā **Kravas** meklējiet un atlasiet izveidoto kravu.
1. Rīkjoslā atlasiet **Izlaist \> Pārvietot uz noliktavu**.
1. Dialoglodziņā **Izlaist slodzi uz noliktavu** atlasiet **Labi**, lai pārvietotu atlasīto noslodzi uz noliktavu.
1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Visi darbi**, lai skatītu izveidoto darbu. Vajadzētu tikt atrastiem diviem jauniem darba ID — vienam uz katru jauno sūtījumu. Katram darba ID ir izdošanas un nolikšanas rindas, kuras novieto krājumu no izdošanas vietām izvietošanas vietās un no izvietošanas vietas uz noliktavu. Atzīmējiet **Noslodzes ID** vērtību pirmajam sūtījumam, lai to varētu izmantot nākamajā procedūrā.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Pārdošanas pasūtījuma izdošana uz pirmā sūtījuma sagatavošanas vietu

1. Pierakstieties Warehouse Management mobile programmā kā darbinieks noliktavā *61*. (Standarta demonstrācijas datos var pieteikties, izmantojot lietotāja ID _61_ un paroli _1_.)
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Pārdošanas izdošana**.
1. Atlasiet lauku **ID** un pēc tam ievadiet darba ID no pirmā sūtījuma.
1. Apstipriniet ievadīto.
1. Laukā **LP** ievadiet unikālu noliktavas vienības identifikatoru no pirmā vienuma (*MyLP1*.)
1. Apstipriniet ievadīto.
1. Laukā **Mērķa LP** ievadiet jebkuru skaitli (mērķa numura zīmei nav jau jāpastāv).

    Visas izveidotās rindas no apstrādātā kopuma tiks izdotas tai pašai mērķa noliktavas vienībai.

1. Apstipriniet ievadīto.
1. wLaukā **LP** ievadiet unikālu noliktavas vienības identifikatoru no otrā vienuma (*MyLP2*.)
1. Apstipriniet ievadīto.

    Iedomājieties, ka darbinieks ir apkopojis pasūtījumu, taču, nonākot darbam norādītajā sagatavošanas vietā, secina, ka šī vieta ir jau aizņemta. Taču darbinieks var redzēt, ka ir pieejama vēl viena tuvumā esoša vieta (*STAGE03*). Tāpēc darbinieks lūgs mainīt sagatavošanas vietu. Tā kā ir iespējots enkurošanas līdzeklis, sistēma automātiski atjauninās sagatavošanas vietu šim un saistītajiem darbiem.

1. Atlasiet **Pārlabot Loc**, lai pārlabotu piedāvāto sagatavošanas vietu.
1. Laukā **Darba izņēmumi** norādiet *Sagatavošanas josla mainīta*.
1. Laukā **Atrašanās vieta** ievadiet jauno sagatavošanas vietu (*STAGE03*.)
1. Apstipriniet ievadīto. Tiek saņemts ziņojums “Darbs pabeigts”.
1. Dodieties uz **Noliktavas pārvaldība \> Darbs\> Viss darbs**.
1. Atveriet pirmā sūtījuma darba ID. Pārbaudiet, vai sagatavošanas vieta tika atjaunināta uz jauno vietu (*STAGE03*), kura tika definēta, izmantojot mobilo ierīci.
1. Atveriet otrā sūtījuma darba ID. Pārbaudiet, vai sagatavošanas vieta tika atjaunināta uz jauno sagatavošanas vietu (*STAGE03*) enkurošanas iestatījumu dēļ.

> [!NOTE]
> Visām atlikušajām atvērtajām nolikšanas darba rindām ar vienu sagatavošanas vietu un kuras tika ģenerētas no vienas darba veidnes rindas, atrašanās vieta tiks atjaunināta uz jauno vietu.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Izmantojiet noslodzes plānošanas darbvietu, lai esošajai kravai pievienotu jaunu pārdošanas pasūtījumu.

Izpildiet tālāk norādītās darbības, lai kravai pievienotu pasūtījumu un to pēc tam izlaistu uz noliktavu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.
1. Cilnē **Pārdošanas rindas** meklējiet un atlasiet visas pārdošanas 3. pārdošanas pasūtījumam.
1. Darbības rūts cilnē **Piegāde un pieprasījums**, grupā **Pievienot** atlasiet **Uz esošo kravu**, lai atlasītās pasūtījuma rindas pievienotu esošai kravai.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Sadaļā **Kravas** meklējiet un atlasiet kravu no iepriekšējām darbībām.
1. Atlasiet **Izlaist \> Pārvietot uz noliktavu**.
1. Dialoglodziņā **Izlaist slodzi uz noliktavu** atlasiet **Labi**, lai pārvietotu atlasīto noslodzi uz noliktavu.
1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Visi darbi**, lai skatītu izveidoto darbu. Atzīmējiet **Noslodzes ID** vērtību, lai to varētu izmantot nākamajā procedūrā.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Pārdošanas pasūtījuma izdošana uz trešā sūtījuma sagatavošanas vietu

1. Piesakieties mobilajā programmā kā darbinieks noliktavā *61*.
1. Galvenajā izvēlnē atlasiet **Izejošs**.
1. Izvēlnē **Izejošs** atlasiet **Pārdošanas izdošana**.
1. Atlasiet lauku **ID** un pēc tam ievadiet darba ID no trešā sūtījuma.
1. Apstipriniet ievadīto.
1. Laukā **LP** ievadiet unikālu noliktavas vienības identifikatoru no pirmā vienuma (*MyLP1*.)
1. Apstipriniet ievadīto.
1. Laukā **Mērķa LP** ievadiet jebkuru skaitli (mērķa numura zīmei nav jau jāpastāv).
1. Apstipriniet ievadīto.
1. wLaukā **LP** ievadiet unikālu noliktavas vienības identifikatoru no otrā vienuma (*MyLP2*.)
1. Apstipriniet ievadīto.

    Attiecībā uz pirmo kravu iedomājieties, ka darbinieks konstatē, ka norādītā sagatavošanas vieta nav pieejama. Tāpēc viņš vēlas lietot citu sagatavošanas vietu (*STAGE04*).

1. Atlasiet **Pārlabot Loc**, lai pārlabotu piedāvāto sagatavošanas vietu.
1. Laukā **Darba izņēmumi** norādiet *Sagatavošanas josla mainīta*.
1. Laukā **Atrašanās vieta** ievadiet jauno sagatavošanas vietu (*STAGE04*.)
1. Apstipriniet ievadīto. Tiek saņemts ziņojums “Darbs pabeigts”.
1. Dodieties uz **Noliktavas pārvaldība \> Darbs\> Viss darbs**.
1. Atveriet pirmā sūtījuma darba ID. Pārbaudiet, vai sagatavošanas vieta nav atjaunināta uz jauno sagatavošanas vietu (*STAGE04*), jo atlikusī atvērtā izvietošanas rinda neatbild pabeigtās izvietošanas rindas darba veidnes rindai.
1. Atveriet otrā sūtījuma darba ID. Pārbaudiet, vai sagatavošanas vieta nav atjaunināta uz jauno sagatavošanas vietu (*STAGE04*), jo sagatavošanas vieta neatbilst izpildītās izvietošanas rindas sagatavošanas vietai. Citiem vārdiem sakot, izpildītā izvietošanas darba rinda un atlikusī atvērtā darba rinda ir ar atšķirīgām sagatavošanas vietām un šajā gadījumā tiek atjauninātas tikai tās rindas, kurām ir vienādas sagatavošanas vietas.
1. Atveriet trešā sūtījuma darba ID. Pārbaudiet, vai sagatavošanas vieta tika atjaunināta uz jauno sagatavošanas vietu (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
