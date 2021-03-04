---
title: Noliktavas vietas statuss
description: Šajā tēmā ir sniegts pārskats par noliktavas novietojuma statusa funkciju.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 31216c24f54f22ec928eb143d4a913aabcd50cf8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433159"
---
# <a name="warehouse-location-status"></a>Noliktavas vietas statuss

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management ir iekļauti vairāki novietojuma lauki, kas ļauj elastīgi darboties ar novietojumiem un tos uzturēt. Novietojuma statusus varat iekļaut novietojuma direktīvas vaicājumā, lai labāk kontrolētu noliktavas plūsmu.

Tālāk norādītie četri lauki lapā **Novietojumi** izseko informāciju par novietojuma pašreizējo statusu. Šie lauki sniedz noliktavas vadītājiem iespēju iegūt pārskatu par noliktavas novietojumu statusu. Tāpat tie ļauj veikt detalizētu atskaišu veidošanu un filtrēšanu.

- **Krājuma numurs** – pašlaik novietojumā esošais krājums. Ja novietojumā ir vairāki krājumi, šis lauks ir tukšs.
- **Pēdējās aktivitātes datums un laiks** – pēdējā noliktavas darījuma laikspiedols, kas tika veikts saistībā ar novietojumu.
- **Vecumstruktūras datums** – datums, kad noliktavā tika ievietots krājums novietojumā. Šī vērtība tiek aprēķināta, ņemot vērā unikālas noliktavas vienības vecumstruktūras datumu. Tā ir precīza tiem novietojumiem, kurus var izsekot pēc unikāla noliktavas vienības identifikatora, bet var nebūt precīza novietojumiem, kas pēc unikāla noliktavas vienības identifikatora nav izsekojami.
- **Novietojuma statuss** – novietojuma statuss. Ir iespējamas četras vērtības:

    - **Nav noteikts** – novietojuma profils nevar izsekot statusu. Tāpēc pašreizējais statuss ir nezināms.
    - **Tukšs** – novietojumā pašlaik nav neviena krājuma.
    - **Izdošana** – izejošās darbības ir veiktas attiecībā pret novietojumu, jo pēdējoreiz tas bija tukšs.
    - **Glabāšana** – tikai ienākošās darbības ir veiktas attiecībā pret novietojumu, jo pēdējoreiz novietojums bija tukšs.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Līdzekļa Noliktavas novietojuma statuss ieslēgšana

Lai varētu izmantot līdzekli *Noliktavas novietojuma statuss*, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Noliktavas novietojuma statuss*

## <a name="set-up-warehouse-location-status"></a>Noliktavas novietojuma statusa iestatīšana

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Piemēru scenārijam nepieciešamo parauga datu sagatavošana

Pirms sākt darbu ar scenāriju, aktivizējiet parauga datus un iestatiet līdzekli, kā tas ir izklāstīts šajā sadaļā. Lai pabeigtu parauga scenāriju, ir jāizmanto noliktavas programma vai emulators, kura darbību nodrošina pārlūkprogramma. Noliktavas programma izmanto šeit izklāstītās darbības. Līdzīgas darbības ir emulatoram, kura darbību nodrošina pārlūkprogramma.

#### <a name="use-the-usmf-legal-entity"></a>USMF juridiskas personas izmantošana

Lai, izmantojot šo scenārija piemēru, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

#### <a name="set-up-location-profiles"></a>Iestatīt novietojuma profilus

Piemēra scenārijam sagatavojiet divus novietojuma profilus.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Novietojuma profili**.
1. Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.
1. Atlasiet profilu **LIELAPJOMA-06**.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Iespējot vienumu novietojumā** – iestatiet šai opcijai vienumu _Jā_.
    - **Iespējot novietojuma aktivitātes datumu un laiku** – iestatiet šai opcijai statusu _Jā_.
    - **Iespējot novietojuma statusu** – iestatiet šai opcijai vienumu _Jā_.

    Ar šīm opcijām tiek kontrolēts, vai atsauces lauki novietojumā ir aktīvi.

1. Profilam **IZDOŠANA-06** atkārtojiet 3.–4. darbību.

> [!NOTE]
> Kad parametri novietojuma profilā (**Iespējot krājumu novietojumā**, **Iespējot novietojuma aktivitāti**, **Iespējot novietojuma statusu**) tiek iestatīti uz *Jā*, sistēma nekavējoties atjaunina atbilstošos novietojumus, izpildot darbu *noliktavas novietojuma statusa konsekvences pārbaude*.

### <a name="scenario"></a>Scenārijs

1. Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.
1. Atlasiet **Jauns**.
1. Kopsavilkuma cilnes **Piegādātājs** **pirkšanas pasūtījuma izveides** dialoglodziņā laukā **Piegādātāja konts** atlasiet *104*.
1. Kopsavilkuma cilnes **Vispārīgi** laukā **Noliktava** atlasiet *61*.
1. Atlasiet **Labi**.
1. Jaunais pirkšanas pasūtījums ir atvērts. Tajā ir ietverta tukša rinda režģī **Pirkšanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** _A0002_
    - **Daudzums:** _5_

1. Darbību rūtī cilnē **Pirkšana** grupā **Darbības** atlasiet **Apstiprināt**, lai apstiprinātu pirkšanas pasūtījumu.
1. Mobilajā ierīcē atveriet **Ienākošais \> Pirkumu saņemšana**.
1. Atlasiet lauku **PONUM**, ievadiet pirkšanas pasūtījuma numuru un apstipriniet.
1. Atlasiet lauku **KRĀJUMS**, ievadiet *A0002* kā krājuma numuru un apstipriniet.
1. Lapā **DAUDZ** ievadiet ciparu *5* kā daudzumu un apstipriniet.

    Daudzumu var ievadīt kādā no tālāk norādītajiem veidiem.

    - Atlasiet pluszīmes (**+**) vai mīnusa zīmes (**–**) pogu, lai pievienotu vai atņemtu skaitlisku vērtību.
    - Atlasiet tukšo lauku starp pluszīmes (**+**) un mīnusa zīmes (**–**) pogām, lai atvērtu ciparu tastatūru.

1. Apstipriniet krājuma numura *A0002* un daudzuma *5* atlasi. Lapas apakšā tiks parādīts ziņojums “Darbs pabeigts”.
1. Augšējā labajā stūrī atlasiet izvēlnes pogu (dažkārt to dēvē par hamburgeru vai hamburgera pogu) un pēc tam atlasiet **Atcelt**, lai izietu no pozīcijas **Pirkumu saņemšana** un atgrieztos **ienākošajā** izvēlnē.
1. Pirkšanas pasūtījuma lapā atlasiet **Detalizēta informācija par darbu** virs režģa **Pirkšanas pasūtījuma rindas**.
1. Cilnē **Vispārīgi** atcerieties izveidotās vērtības **Darba ID** un **Mērķa unikāla noliktavas vienības identifikatora ID**.
1. Sadaļā **Rindas** atcerieties vērtības **Novietojums** darba veidiem *Izdošana* un *Izvietošana*.
1. Mobilajā ierīcē atveriet **Ienākošais \> Pirkumu izvietošana**.
1. Atlasiet lauku **ID**, ievadiet darba ID un apstipriniet.
1. Apstipriniet vēlreiz, lai pabeigtu ievadi *Izdošana*.
1. Augšējā labajā stūrī atlasiet izvēlnes pogu un pēc tam atlasiet **Gatavs**, lai pabeigtu *izdošanas* darbu.
1. Atzīmējiet izvietošanas novietojumu un apstipriniet. Lapas apakšā tiks parādīts ziņojums “Darbs pabeigts”.
1. Augšējā labajā stūrī atlasiet izvēlnes pogu un pēc tam atlasiet **Atcelt**, lai izietu no vienuma **Pirkumu izvietošana** un atgrieztos **ienākošajā** izvēlnē.
1. Atlasiet **Atpakaļ**, lai atgrieztos galvenajā izvēlnē.
1. Dynamics 365 Supply Chain Management atveriet **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojumi**.
1. Filtrējot sameklējiet vienumu **Novietojums** un ievadiet izvietošanas novietojumu no pirkšanas pasūtījuma darba. Vajadzētu tikt parādītiem šādiem rezultātiem:

    - Kolonnā **Novietojuma statuss** tiek rādīta *glabāšanas* vērtība, jo tika izvietots pēdējais darījums attiecībā pret šo novietojumu.
    - Kolonnā **Krājuma numurs** tiek rādīta vērtība *A0002*, jo šis krājums tika saņemts un izvietots novietojumā.
    - Kolonnā **Pēdējās aktivitātes datums un laiks** tiek rādīts laikspiedols tam datumam un laikam, kad darbs tika pabeigts novietojumā.

1. Mobilajā ierīcē atveriet **Kvalitāte \> Kustība**.
1. Atlasiet lauku **LOC/LP** un ievadiet novietojumu, kuru atzīmējāt iepriekšējās darbībās.
1. Apstipriniet parādīto informāciju. Atzīmējiet ģenerēto unikālo noliktavas vienības identifikatoru.
1. **Informācijas beigu** ekrānā atlasiet lauku **LOC/LP** un ievadiet *06A07R2S1B* kā novietojumu, uz kuru pārvietot krājumu.
1. **Informācijas beigu** ekrānā apstipriniet vērtību **LP** (mērķa unikālā noliktavas vienības identifikatora ID), kas tiek ģenerēta automātiski. Lapas apakšā tiks parādīts ziņojums “Darbs pabeigts”.
1. Augšējā labajā stūrī atlasiet izvēlnes pogu un pēc tam atlasiet **Atcelt**, lai izietu no vienuma **Kustība** un atgrieztos izvēlnē **Kvalitātes pārvaldība**.
1. Atlasiet **Atpakaļ**, lai atgrieztos galvenajā izvēlnē.
1. Dynamics 365 Supply Chain Management atveriet **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojumi**.
1. Atsvaidziniet lapu **Novietojumi** un vēlreiz apskatiet sākotnējo novietošanas novietojumu. Ņemiet vērā, ka lauka **Novietojuma statuss** vērtība tagad ir *Tukšs*, un kolonna **Krājuma numurs** ir tukša.
1. Apskatiet novietojuma *06A07R2S1B* ierakstu un ņemiet vērā, ka vērtība **Statuss** tagad ir mainīta uz *Glabāšana*, kā arī ir atjaunināti lauki **Krājuma numurs** un **Pēdējās aktivitātes datums un laiks**.
1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**.
1. Dialoglodziņā **Pārdošanas pasūtījuma izveide** **klienta konta** laukā atlasiet *US-002*.
1. Laukā **Noliktava** atlasiet *61*.
1. Atlasiet **Labi**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta tukša rinda režģī **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** _A0002_
    - **Daudzums:** _1_

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Krājumi** atlasiet **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu. Pēc tam augšējā labajā stūrī atlasiet pogu **Aizvērt** (**X**), lai aizvērtu lapu.
1. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.
1. Sadaļā **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** atlasiet **Detalizēta informācija par darbu**.
1. Nokopējiet izveidoto vērtību **Darba ID**.
1. Mobilajā ierīcē atveriet **Izejošs \> Pārdošanas izdošana**.
1. Atlasiet lauku **ID**, ievadiet iepriekš nokopēto darba ID un apstipriniet.
1. Lapā **Pārdošanas pasūtījumi: izdošana** laukā **LOC** ir ieteikts izdošanas novietojums kā iepriekš izveidotais novietošanas novietojums. Pierakstiet novietojumu.
1. Atlasiet lauku **LOC**, ievadiet novietojumu un apstipriniet.
1. Atlasiet lauku **LP**, ievadiet unikālo noliktavas vienības identifikatoru, ko pierakstījāt kustības darbības laikā, un apstipriniet.
1. Atlasiet lauku **Krājums**, ievadiet *A0002* kā krājuma numuru un apstipriniet.
1. Lapā **DAUDZ** ievadiet ciparu *1* kā daudzumu un apstipriniet.

    Daudzumu var ievadīt kādā no tālāk norādītajiem veidiem.

    - Atlasiet pluszīmes (**+**) vai mīnusa zīmes (**–**) pogu, lai pievienotu vai atņemtu skaitlisku vērtību.
    - Atlasiet tukšo lauku starp pluszīmes (**+**) un mīnusa zīmes (**–**) pogām, lai atvērtu ciparu tastatūru.

1. Atlasiet lauku **MĒRĶA LP**, ievadiet lietotāja definētu unikālu noliktavas vienības ID un apstipriniet.
1. Apstipriniet vēlreiz, lai pabeigtu izdošanas darbu. Lapas apakšā tiks parādīts ziņojums “Darbs pabeigts”.
1. Augšējā labajā stūrī atlasiet izvēlnes pogu un pēc tam atlasiet **Atcelt**, lai pabeigtu izdošanas aktivitāti un atgrieztos **izejošajā** izvēlnē.
1. Dynamics 365 Supply Chain Management atveriet **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Novietojumi**.
1. Filtrējot sameklējiet vienumu **Novietojums** un ievadiet izdošanas novietojumu no pārdošanas pasūtījuma darba.
1. Ņemiet vērā, ka lauks **Novietojuma statuss** tam novietojumam, no kura tika izdots pārdošanas pasūtījuma darbs, tagad ir iestatīts kā *Izdošana*, un ir atjaunināts lauks **Pēdējās aktivitātes datums un laiks**.

> [!NOTE]
> Novietojuma lauki tiek atjaunināti tikai ar noliktavas darbībām. Ja pārvietosit krājumus, izmantojot žurnālu vai citus procesus, kas nav noliktavas procesi, lauki netiks atjaunināti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]