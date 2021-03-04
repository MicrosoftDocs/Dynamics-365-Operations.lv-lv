---
title: Uzlabota kravu plānošana kopuma laikā
description: Šajā tēmā ir sniegta informācija par uzlabota kopuma kravu plānošanu, kas kopuma izpildes laikā automātiski piešķir sūtījumus esošajiem kopumiem. Tādējādi varat izveidot jēgpilnas kravas, kas atbilst kravas automašīnām, neizmantojot kravu plānošanas rīku.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 7f51b3d65c8dd1e11296956c37ef9dfe568e5ec2
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654202"
---
# <a name="advanced-load-building-during-wave"></a>Uzlabota kravu plānošana kopuma laikā

[!include [banner](../includes/banner.md)]

Uzlabota kopuma kravu plānošana, kas kopuma izpildes laikā automātiski piešķir sūtījumus esošajiem kopumiem. Tādējādi varat izveidot jēgpilnas kravas, kas atbilst kravas automašīnām, neizmantojot kravu plānošanas rīku. Šī iespēja ir noderīga uzņēmumiem, kuri vēlas izmantot kravas jēdzienu, lai izsekotu un plānotu preču nosūtīšanu kravas automašīnā/piekabē, bet nevēlas veidot šīs kravas manuāli katru dienu.

Kopuma apstrādes laikā sistēma parasti izveido jaunu kravu katram sūtījumam, kam nav piešķirta krava. Tomēr, ja ir ieslēgta uzlabota kopuma kravu plānošana, sistēma katru nepiešķirto sūtījumu piešķir esošai kravai (ja pastāv atbilstoša krava) un jaunas kravas tiek izveidotas tikai tad, kad ir nepieciešamas. Uzlabota kopuma kravu plānošana automātiski izveido jaunas kravas, pamatojoties uz jūsu definētajiem kritērijiem.

Lai izmantotu šo līdzekli, sistēma ir jāiestata sekojoši:

- Izveidojiet *kopuma veidnes*, kas ietver jauno **buildLoads** metodi. Šī metode padara uzlabota kopuma kravu plānošanu pieejamu kopumiem, kas izmanto šīs veidnes.
- Iestatiet *kravu plānošanas veidnes*, lai katra no tām būtu saistīta ar noteiktu kopuma veidni un metodi. Kravas plānošanas veidnes kontrolē, kuras kravas (esošas vai jaunas) kravas rindas ir nokomplektētas pievienošanai. Varat kombinēt vai atdalīt sūtījumus, pamatojoties uz tādiem kritērijiem kā kravas veidne, aprīkojums un uz citu lauku vērtībām kravas rindā.
- Definējiet *kravas komplekta grupas*, lai kontrolētu, kuri krājumi ir vai nav kombinējami vienā kravā. Norādiet arī, vai ierobežojumam jāveido brīdinājums vai kļūda un vai ir jānovērtē kravas veidnes tilpuma ierobežojums.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Iespējot uzlabota kopuma kravu plānošanu sistēmā

Lai varētu izmantot uzlabota kopuma kravu plānošanu, sistēmā ir jābūt iespējotiem diviem līdzekļiem. Administratori var izmantot [līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu šo līdzekļu statusu un tos ieslēgtu, ja tas nepieciešams. Darbvietā **Līdzekļu pārvaldība** līdzekļi ir uzskaitīti šādi:

- Kopuma kravu plānošanas līdzeklis:

    - **Modulis:** *Noliktavas vadība*
    - **Līdzekļa nosaukums:** *Kopuma kravu plānošanas līdzeklis*

- Organizācijas līmeņa kopuma darbības kods:

    - **Modulis:** *Noliktavas vadība*
    - **Līdzekļa nosaukums:** *Organizācijas līmeņa kopuma darbības kods*

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo demonstrāciju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Varat izmantot šo demonstrāciju arī kā vadlīnijas šī līdzekļa izmantošanai, strādājot ar ražošanas sistēmu. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Pārliecināšanās, vai scenārija iestatījumi ietver pietiekami daudz pieejamo krājumu

Ja strādājat ar **USMF** demonstrācijas datiem, vispirms pārliecinieties, vai sistēma ir iestatīta tā, lai katrā atbilstošajā vietā būtu pietiekami daudz krājumu. Šajā demonstrācijā ir paredzēts, ka *62.* noliktavā ir pieejami šādi krājumi:

- **Krājums A0001:** 10 gab.
- **Krājums A0002:** 10 gab.
- **Krājums M9200:** 10 katrs

Krājums **M9200** ir jāpievieno noliktavai. Izpildiet apakšsadaļās aprakstītās procedūras, lai to pievienotu krājumiem.

#### <a name="create-a-new-license-plate-id"></a>Izveidojiet jaunu noliktavas vienības ID

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Noliktava** \> **Noliktavas vienības**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunās rindas laukā **Noliktavas vienība** ievadiet *LP6203*.
1. Atlasiet **Saglabāt**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Izveidojiet standarta izmaksas krājumam M9200 6. vietā

1. DOdieties uz **Preču informācijas pārvaldība** \> **Preces** \> **Nodotās preces**.
1. Meklējiet **M9200**.
1. Atlasiet krājuma rindu un pēc tam darbību rūtī cilnē **Pārvaldīt izmaksas** grupā **Iestatīt** atlasiet **Krājuma cena**.
1. Lapā **Krājuma cena** atlasiet cilni **Neapstiprinātās cenas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Izmaksu aprēķināšanas veids:** *Plānotās izmaksas*
    - **Cenas veids:** *Izmaksas*
    - **Versija:** *10*
    - **Vieta:** *6*
    - **Cena:** *1,60*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Aktivizēt neapstiprinātās cenas**.
1. Atlasiet cilni **Aktīvās cenas**, lai pārbaudītu, vai *6.* vietai ir pievienota jauna izmaksu cena.

#### <a name="create-inventory-in-warehouse-62"></a>Krājumu izveidošana 62. noliktavā

1. Dodieties uz **Krājumu pārvaldība** \> **Žurnāla ieraksti** \> **Krājumi** \> **Krājumu korekcija**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot krājumu žurnālu**, kopsavilkuma cilnē **Pārskats** laukā **Noliktava** ievadiet *62*. Pieņemiet noklusējuma vērtības visos pārējos laukos.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.
1. Tiek atvērta lapa **Krājumu korekcija**. Kopsavilkuma cilnē **Žurnāla rindas** atlasiet **Jauns**, lai pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības. Pieņemiet noklusējuma vērtības visos pārējos laukos.

    - **Krājuma numurs:** *M9200*
    - **Vieta:** *bulk-003*
    - **Daudzums:** mainiet vērtību uz *10*.

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Validēt**, lai pārbaudītu kļūdas.
1. Dialoglodziņā **Žurnāla pārbaude** atlasiet **Labi**, lai sāktu pārbaudi. Kad pārbaude ir pabeigta, tiek saņemts ziņojums.
1. Darbību rūtī atlasiet **Grāmatot**, lai sāktu krājumu korekcijas.
1. Dialoglodziņā **Žurnāla grāmatošana** atlasiet **Labi**, lai sāktu grāmatošanu. Kad grāmatošana ir pabeigta, tiek saņemts ziņojums.

## <a name="set-up-advanced-wave-load-building"></a>Uzlabota kopuma kravu plānošanas iestatīšana

### <a name="regenerate-wave-process-methods"></a>Kopuma procesa metožu atkārtota ģenerēšana

Lai padarītu pieejamu kravu plānošanas metodi (**buildLoads**), var būt nepieciešams atkārtoti ģenerēt kopuma procesa metodes.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Kopumi** \> **Kopuma procesa metodes**.
2. Pārbaudiet, vai sarakstā ir **buildLoads**. Ja tā nav, darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**, lai to pievienotu.

### <a name="set-up-wave-templates"></a>Kopuma veidņu iestatīšana

Lai izmantotu uzlabota kopuma kravu plānošanu, katrā atbilstošajā [kopuma veidnē](tasks/configure-wave-processing.md) ir jāiekļauj **buildLoads** metode.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Kopumi** \> **Kopuma veidnes**.
1. Atlasiet kopuma veidni.

    Ja strādājat ar **USMF** demonstrācijas datiem, atlasiet veidni **62 Sūtījums pēc noklusējuma**.

1. Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.
1. Kopsavilkuma cilnē **Metodes** režģī **Atlikušās metodes**, atlasiet **buildLoads** metodi.
1. Atlasiet bultiņas pa labi pogu, lai pārvietotu **buildLoads** metodi uz režģi **Atlasītās metodes**.
1. Lai **buildLoads** metodei piešķirtu vērtību **Kopuma darbības kods**, lapā **Kopuma darbības kodi** vispirms ir jāizveido kods. Varat izmantot jebkuru vērtību, bet noteikti pierakstiet to, jo tā būs nepieciešama vēlāk. Lai izveidotu kodu **WSC2112**, veiciet šādas darbības:

    1. Metodes **buildLoads** rindā ar peles labo pogu noklikšķiniet uz nolaižamās bultiņas laukā **Kopuma darbības kods** un pēc tam atlasiet **Skatīt detalizēti**.
    1. Lapā **Kopuma darbību kodi** darbību rūtī atlasiet **Jauns**.
    1. Laukā **Kopuma darbības kods** ievadiet *WSC2112*.
    1. Laukā **Kopuma darbības apraksts** ievadiet *WSC2112*.
    1. Laukā **Kopuma darbības veids** atlasiet *Kravu plānošana*.

1. Atlasiet **Saglabāt** un aizveriet lapu.
1. Metodes **buildLoads** rindā laukā **Kopuma darbības kods**, atlasiet tikko izveidoto kodu (**WSC2112**).
1. Darbību rūtī atlasiet **Saglabāt**.

> [!NOTE]
> Kopuma darbību kodi ir kodi, ko lietotāji var iestatīt un izmantot, lai saistītu konkrētas kopuma metodes instances ar atbilstošajām veidnēm. Veidnēs ir ietvertas papildināšanas, konteinerizēšanas, etiķešu drukāšanas, noslodzes veidošanas un kārtošanas veidnes.
>
> Kad netiek lietoti kopuma darbību kodi, lietotājiem jāievada brīvs teksts, lai atsauktos uz noteiktu veidni no kopuma metodes instances. Brīvajam tekstam ir nosliece uz kļūdām, tāpēc lietotājiem ir jāpārliecinās, vai kopuma darbību teksts, kas tika pievienots konkrētajai kopuma darbību metodei kopuma veidnē, tieši atbilst kopuma darbību tekstam mērķa veidnē.
>
> Kopuma darbību kodi noteiktam kopuma darbību tipam ir iestatīti atsevišķā lapā. Katrai kopuma darbību metodes instancei kopuma veidnē, kas pieprasa kopuma darbības kodu, nolaižamajā sarakstā jābūt atlasītam kopuma darbības kodam. Atlase nolaižamajā sarakstā aizstāj brīvā teksta ievadi un palīdz samazināt cilvēka kļūdas risku un ietekmi. Iestatīšanas kodus lieto, lai veidotu saiti uz kopuma darbību metodi kopuma veidnē uz metodi mērķa veidnē.

### <a name="set-up-load-mix-groups"></a>Kravas komplekta grupu iestatīšana

Kravas komplekta grupas veido kārtulas krājumu tipiem, ko var kombinēt vienā kravā. Varat iestatīt tik daudz kravas komplekta grupu, cik ir nepieciešams. Tomēr ir jābūt vismaz vienai, lai izmantotu uzlabota kopuma kravu plānošanu. Lai izveidotu kravas komplekta grupu, veiciet šādas darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Krava** \> **Kravas komplekta grupas**.
1. Lai izveidotu kravas grupu, darbību rūtī atlasiet **Jauns**.
1. Laukā **Kravas komplekta grupas ID** ievadiet jaunās grupas nosaukumu.

    Ja strādājat ar **USMF** demonstrācijas datiem, iestatiet šādas vērtības:

    - **Kravas komplekta grupas ID:** *TV*
    - **Apraksts:** *TV*

1. Darbību rūtī atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Kravas komplekta grupas kritēriji**.
1. Kopsavilkuma cilnē **Kravas komplekta grupas kritēriji** atlasiet **Jauns**, lai režģim pievienotu rindu.
1. Jaunās rindas katrā laukā iestatiet vēlamās vērtības. Šīs vērtības nosaka krājuma grupas, kas tiek uzskatītas par kravas komplektu.

    Ja strādājat ar **USMF** demonstrācijas datiem, laukā **Krājumu grupa** atlasiet *TV&Video*.

1. Darbību rūtī atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Kravas komplekta grupas ierobežojumi**.
1. Kopsavilkuma cilnē **Kravas komplekta grupas ierobežojumi** atlasiet **Jauns**, lai režģim pievienotu rindu.
1. Jaunās rindas katrā laukā iestatiet vēlamās vērtības.

    Ja strādājat ar **USMF** demonstrācijas datiem, iestatiet šādas vērtības:

    - **Krājuma grupa:** *CarAudio*
    - **Kravas plānošanas darbība:** *Ierobežot* (šī vērtība neļaus krājumiem, kas pieder **CarAudio** krājuma grupai, atrasties tajā pašā kravā kā krājumiem, kas pieder **TV&Video** krājuma grupai.)

1. Turpiniet strādāt ar kārtulām, kamēr ir pievienoti visi kritēriji un ierobežojumi, kas ir nepieciešami kravas komplekta grupai.

Ja strādājat ar **USMF** demonstrācijas datiem, tagad šis iestatījums ir pabeigts.

### <a name="set-up-load-build-templates"></a>Kravas plānošanas veidņu iestatīšana

Varat iestatīt tik daudz kravas plānošanas veidnes, cik ir nepieciešams. Tomēr ir jābūt vismaz vienai, lai izmantotu uzlabota kopuma kravu plānošanu. Lai izveidotu kravas plānošanas veidni, veiciet šādas darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatīšana** \> **Krava** \> **Kopuma kravu plānošanas veidnes**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības.

    | Lauks | apraksts | USMF demonstrācijas datu vērtība |
    |---|---|---|
    | Sērijas numurs | Secība, kādā tiks novērtētas veidnes. | *1* |
    | Noslodzes plānošanas veidnes nosaukums | Ievadiet unikālu kravas plānošanas veidnes identifikatoru. Jums ir jāievada tās veidnes nosaukums, kuru iepriekš izveidojāt vai atjauninājāt šajā iestatījumā. | *62 Sūtījums pēc noklusējuma* |
    | Kopuma darbības kods | Ievadiet kopuma darbības kodu, ko izmantot, lai saistītu veidni ar kopuma metodi. Jums ir jāievada kods, ko atlasījāt metodei **buildLoads**, kad šajā iestatījumā iepriekš iestatījāt kopuma veidni. | *WSC2112* |
    | Kravas veidnes ID | Atlasiet kravas veidni, kas tiks izmantota, plānojot jaunas kravas, un saskaņota, piešķirot esošajām kravām. Kravas veidne nosaka maksimālo svaru un tilpumu, kas ir atļauts visai kravai. | *Standarta noslodzes veidne* |
    | Aprīkojums | Aprīkojums, kas tiks saskaņots, piešķirot esošās kravas un ievadīts jaunajām kravām. | Atstājiet šo lauku tukšu. |
    | Noslodzes komplekta grupas ID | Atlasiet kravas komplekta grupu, ko izmantot, ja krājums ir atļauts kravai. Komplekta grupa nosaka kārtulas krājumu tipiem, ko var kombinēt vienā kravā. Ir jāatlasa viena no komplekta grupām, kuru iepriekš izveidojāt šajā iestatījumā. | *TV* |
    | Izmantot atvērtās noslodzes | Atlasiet, vai ir jāpievieno esošās atvērtās kravas. Pieejamas šādas opcijas<ul><li>**Nav** – nepievienot atvērtās kravas nevienai esošajai kravai.</li><li>**Jebkura** – pievienot atvērtās kravas visām esošajām kravām, kas ir derīgas rindai.</li><li>**Piešķirts** – Atvērtās kravas pievienot kravai, kas piešķirta kopumam.</li></ul> | *Jebkurš* |
    | Izveidot noslodzes | Norādiet, vai jāveido jaunas kravas, ja neviena no esošajām kravām neatbilst kritērijiem. | Atlasīts (= *Jā*) |
    | Atļaut sūtījuma rindas sadalījumu | Norādiet, vai viena kravas rinda var tikt sadalīta starp vairākām kravām, ja pilna rinda pārsniedz maksimālo kravas veidnes noslodzi. | Notīrīts (= *Nē*) |
    | Apstiprināt tilpuma rādītājus | Norādiet, vai kravu plānošanai būtu jāpārbauda svars un tilpums, ja visas kravas rindas tiek pievienotas, nodrošinot kravas veidnes tilpuma ierobežojumu ievērošanu. | Notīrīts (= *Nē*) |

1. Darbību rūtī atlasiet **Saglabāt**, lai padarītu pieejamu opciju **Rediģēt vaicājumu**.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājuma rediģēšanas dialoglodziņu.
1. Dialoglodziņa cilnē **Kārtošana** atlasiet **Pievienot**, lai režģim pievienotu rindu.
1. Jaunajā rindā definējiet kārtošanas nosacījumus, ko vēlaties izmantot. Piemēram, iestatiet šādas vērtības, lai kārtotu meklēšanas rezultātus augošā secībā pēc pasūtījuma numura:

    - **Tabula:** *Kravas informācija*
    - **Atveidotā tabula:** *Kravas informācija*
    - **Lauks:** *Pasūtījuma numurs*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**, lai saglabātu izmaiņas un aizvērtu dialoglodziņu.
1. Kopsavilkuma cilnē **Sadalīt pēc** iestatiet kārtulas, lai kontrolētu, kā tiek sadalītas kravas. Parasti ir iespējams sadalīt pielāgotos laukus, kas ir izvērsti kravas rindai, piemēram, **Maršrutēt**, **Apskatīt** vai **Izpildīt**. Piemēram, lai izveidotu vienu kravu katram pasūtījuma numuram, atlasiet izvēles rūtiņu **Sadalīt pēc** rindai, kurai ir šādas vērtības:

    - **Atsauces tabulas nosaukums:** *Kravas informācija*
    - **Atsauces lauka nosaukums:** *Pasūtījuma numurs*

## <a name="scenario"></a>Scenārijs

Scenārijā parādīts, kā šajā tēmā iepriekš aprakstītie iestatījumi ietekmē noliktavas operācijas, apstrādājot pārdošanas pasūtījumu. Scenārijā tiek izmantoti **USMF** demonstrācijas dati kopā ar citām demonstrācijas vērtībām, kas sniegtas šo iestatījumu instrukcijās.

### <a name="create-sales-orders"></a>Pārdošanas pasūtījumu izveide

1. Dodieties uz **Pārdošana un mārketings** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**, lai atvērtu dialoglodziņu **Izveidot pārdošanas pasūtījumu**.
1. Dialoglodziņā iestatiet tālāk norādītās vērtības:

    - Kopsavilkuma cilnē **Klients** iestatiet lauku **Klienta konts** uz *US-007*.
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet laukam **Noliktava** vērtību *62*.

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Jaunajai rindai iestatiet lauku **Krājuma numurs** uz *A0001* un lauku **Daudzums** uz *1*.
1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapā **Rezervācija** darbību rūtī atlasiet **Rezervēt vietu**.
1. Atlasiet pogu **Aizvērt** (**X**) lapas augšējā labajā stūrī, lai atgrieztos pārdošanas pasūtījumā.
1. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**. Sistēma izveido sūtījumu un pievieno to jaunajai kravai, jo neviena esošā krava neietver kravas rindas ar šādu pasūtījuma numuru.

    Tiek saņemti informatīvi ziņojumi, norādot šim pasūtījumam izveidoto darbu, kopumu un sūtījumu.

1. Lai pārdošanas rindā apstiprinātu kravas, sūtījuma un darba detaļas, atlasiet rindu un pēc tam izvēlnē **Noliktava** virs režģa atlasiet **Kravas detaļas**, **Sūtījuma detaļas** vai **Darba detaļas**.
1. Tikko izveidotajā pārdošanas pasūtījumā kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai pievienotu vēl vienu rindu.
1. Jaunajā rindā iestatiet lauku **Krājuma numurs** uz *A0002* un lauku **Daudzums** uz *1*.
1. Atkārtojiet darbības no 6 līdz 9, lai rezervētu rindu un izlaistu to noliktavā. Sistēma izveido **jaunu** sūtījumu rindai, kuru pievienojāt. Tomēr, izmantojot uzlabota kopuma kravu plānošanu, sistēma pievieno šo sūtījumu un kravas rindu esošam laidienam. Neizmantojot uzlabota kopuma kravu plānošanu, sistēma sūtījumam izveidos jaunu kravu.
1. Tikko izveidotajā pārdošanas pasūtījumā kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai pievienotu vēl vienu rindu.
1. Jaunajā rindā iestatiet lauku **Krājuma numurs** uz *M9200* un lauku **Daudzums** uz *1*.
1. Atkārtojiet darbības no 6 līdz 9, lai rezervētu rindu un izlaistu to noliktavā. Tā pat kā iepriekš, sistēma izveidos **jaunu** sūtījumu rindai, kuru pievienojāt. Tomēr, tā kā krājums ir no **CarAudio** krājuma grupas, tas **nespēj nodot ierobežojumus, ko iestatāt kravas komplekta grupai**. Tāpēc tas tiek **pievienots jaunai kravai**. Ja kravas plānošanas veidnē netika norādīta kravas komplekta grupa, tad sūtījums tika pievienots pirmajai kravai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]