---
title: Detalizēta darba rindas informācija
description: Šajā tēmā ir sniegta informācija par lapu Detalizēta informācija par darba rindām, kurā ir attēlots visaptverošs, kārtojams un filtrējams saraksts ar atsevišķām darba rindām jūsu sistēmā.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4d7c6991c0171b0e09752b3305e0fa11a25b7833
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674115"
---
# <a name="work-line-details"></a>Detalizēta darba rindas informācija

[!include [banner](../includes/banner.md)]

Lapā **Detalizēta informācija par darba rindām** ir attēlots visaptverošs, kārtojams un filtrējams saraksts ar atsevišķām darba rindām jūsu sistēmā. Tas sniedz pilnīgu pārskatu par noliktavā plānoto un izpildīto darbu. Varat viegli pārslēgties starp visu darba rindu skatīšanu un tikai atvērto darba rindu skatīšanu. Detalizētajā informācijā, kas tiek sniegta katrai rindai, ir ietverts darba statuss, krājuma kods, novietojums, darba daudzums, kravas ID un sūtījuma ID.

## <a name="turn-on-the-work-line-details-feature"></a>Līdzekļa Detalizēta informācija par darba rindu ieslēgšana

No Piegādes ķēdes pārvaldības versijas 10.0.21 šī funkcija ir ieslēgta pēc noklusējuma. Administratori var izmantot Līdzekļu [pārvaldības lapu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai pārbaudītu līdzekļu statusu un aktivizētu vai atspējotu to, ja nepieciešams. Šeit līdzeklis tiek norādīts kā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Detalizēta informācija par darba rindu*

## <a name="open-and-use-the-work-line-details-page"></a>Lapas Detalizēta informācija par darba rindu atvēršana un lietošana

Lai skatītu detalizētu informāciju par darba rindu sarakstu, atveriet **Noliktavas pārvaldība \> Darbs \> Detalizēta informācija par darba rindu**. Šeit varat veikt tālāk norādītās darbības.

- Lietojiet lauku **Filtrs**, lai meklētu rindas ar konkrētu vērtību jebkuram pieejamajam parametram. (Pieejamajos parametros ietilpst daudzi parametri, kas režģī netiek rādīti kā kolonnas.)
- Izmantojiet izvēles rūtiņu **Rādīt slēgto**, lai rādītu vai paslēptu slēgtās rindas.
- Atlasiet **Rādīt dimensijas**, lai atvērtu dialoglodziņu **Dimensiju attēlojums**, kur varat izvēlēties režģī rādīt vai paslēpt dažādas dimensiju kolonnas.
- Atlasiet jebkuras kolonnas virsrakstu, lai atvērtu izvēlni, kurā varat izvēlēties šajā kolonnā kārtot vai filtrēt sarakstu pēc vērtībām.
- Atlasiet darba rindu un pēc tam atlasiet **Mainīt novietojumu**, lai atvērtu dialoglodziņu, kurā varēsit mainīt šīs darba rindas novietojumu. Jūsu norādītais novietojums pārlabos novietojuma direktīvas iestatījumu.
- Atlasiet darba rindu un pēc tam atlasiet **Atcelt darba rindu**, lai atvērtu dialoglodziņu, kur varat daļēji vai pilnībā samazināt šīs darba rindas daudzumu.
- Koriģējiet daudzumus.
- Skatiet jebkurā darba rindā ietvertās darbības.

## <a name="try-out-the-feature"></a>Līdzekļa izmēģināšana

Šajā sadaļā tiek piedāvāta demonstrācija no trīs daļām, kurā ir parādīts, kā strādāt ar detalizētu informāciju par darba rindu.

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo demonstrāciju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Varat izmantot šo demonstrāciju arī kā vadlīnijas, strādājot ar ražošanas sistēmu. Tomēr jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Pārbaude, vai scenārija iestatījumos ir ietverts pietiekami daudz pieejamo krājumu

Ja strādājat ar **USMF** demonstrācijas datiem, vispirms pārliecinieties, vai sistēma ir iestatīta tā, lai katrā atbilstošajā vietā būtu pieejami pietiekami daudz krājumu. Šajā demonstrācijā ir paredzēts, ka jums ir pieejami šādi krājumi:

- **Krājums M9200:** 45 ea. (vai vairāk)
- **Krājums M9202:** 10 ea. (vai vairāk)

Veiciet šīs darbības, lai pārbaudītu, vai ir pieejams pietiekami daudz krājumu, un lai veiktu visas nepieciešamās korekcijas.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Novietojuma direktīvas** un nosakiet, kuri izdošanas novietojumi ir izmantoti pārdošanas pasūtījuma izdošanai 51. noliktavā. (Papildinformāciju skatiet šeit: [Noliktavas darba kontrolēšana, izmantojot darbu veidnes un novietojuma direktīvas](control-warehouse-location-directives.md).)
1. Pārbaudiet krājumu līmeņus atbilstošajos novietojumos.
1. Pielāgojiet krājumus pēc nepieciešamības. Varat izveidot manuālo kustību, izmantot papildināšanu vai lietot jebkuru citu plūsmu, lai koriģētu krājumus.

### <a name="part-1-create-picking-work"></a>1. daļa: izdošanas darba izveide

Pirms sākt darba izveidi, pārliecinieties, vai noliktava ir iestatīta, lai paredzētajā veidā atbilstu darba prasībām.

Lai izveidotu izdošanas darbu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai atvērtu dialoglodziņu **Pārdošanas pasūtījuma izveide**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - Kopsavilkuma cilnē **Klients** iestatiet lauku **Klienta konts** uz _US-001_.
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noliktava** uz _51_.

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tajā ir ietverta jauna tukša rinda režģī **Pārdošanas pasūtījuma rindas**. Šajā pasūtījuma rindā iestatiet šādas vērtības:

    - **Krājuma numurs:** _M9200_
    - **Daudzums:** _20_
    - **Vienība:** _ea_

1. Atlasiet jaunu pasūtījuma rindu un pēc tam izvēlnē **Krājumi** atlasiet **Rezervācija**, lai atvēru lapu **Rezervācija**.
1. Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.
1. Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**. Sistēma izveido sūtījumu, pievieno to jaunajai kravai un izveido nepieciešamo darbu.
1. Tam pašam klienta kontam un noliktavai, ko izmantojāt pirmajā pasūtījumā, izveidojiet otru pārdošanas pasūtījumu. Pievienojiet šim pasūtījumam šādas divas pasūtījuma rindas:

    - **1. rinda:** iestatiet lauku **Kravas numurs** uz _M9200_, lauku **Daudzums** uz _25_ un lauku **Vienība** uz _Katrs_.
    - **2. rinda:** iestatiet lauku **Kravas numurs** uz _M9202_, lauku **Daudzums** uz _10_ un lauku **Vienība** uz _Katrs_.

1. Atkārtojiet 6.–8. darbību, lai rezervētu krājumus katrai pasūtījuma rindai (pa vienai), un pēc tam atkārtojiet 9. darbību, lai izdotu pasūtījumu noliktavai.

### <a name="part-2-change-the-location-for-a-work-line"></a>2. daļa: darba rindai paredzētā novietojuma maiņa

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Detalizēta informācija par darba rindu**.
1. Atrodiet darba rindas, kuras izveidojāt šai demonstrācijai, un atlasiet vienu no tām.
1. Atlasiet **Mainīt novietojumu**, lai atvērtu dialoglodziņu **Jauna novietojuma atlase**.
1. Dialoglodziņā **Jauna novietojuma atlase** laukā **Novietojums** darba rindai atlasiet jaunu novietojumu.
1. Atlasiet **Labi**, lai izmaiņas piemērotu un aizvērtu dialoglodziņu.

> [!IMPORTANT]
> Novietojuma izmaiņas varat iesniegt tikai tad, ja jaunajā novietojumā ir pieejami pietiekami daudz krājumu (izdošanai) vai tas atbilst novietojuma tipa pārbaudei (izvietošanai).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>3. daļa: darba rindas daudzuma mainīšana vai darba rindas atcelšana

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Detalizēta informācija par darba rindu**.
1. Atrodiet darba rindas, kuras izveidojāt šai demonstrācijai, un atlasiet vienu no tām. Ņemiet vērā, ka daudzumus varat atcelt vai mainīt tikai tām darba rindām, kur darba veids ir _izdošana_.
1. Atlasiet **Atcelt darba rindu**, lai atvērtu dialoglodziņu **Atceļamais daudzums**.
1. Dialoglodziņā **Atceļamais daudzums** mainiet vērtību laukā **Daudzums**, lai norādītu daudzumu, kas *jāatņem no* rindai pašlaik norādītā daudzuma. Pēc noklusējuma laukā **Daudzums** tiek rādīts viss daudzums.

    - Ja atcelsit visu daudzumu, vērtība **Darba statuss** tiks mainīta uz _Atcelts_, bet laukā **Darba daudzums** tiks rādīta sākotnējā vērtība.
    - Ja atcelsit tikai daļu daudzuma, lauks **Darba daudzums** tiks atjaunināts, lai rādītu jauno vērtību, bet vērtība **Darba statuss** netiks mainīta.

1. Atlasiet **Labi**, lai izmaiņas piemērotu un aizvērtu dialoglodziņu.

> [!IMPORTANT]
> Ja darba rindai atcelsit tikai daļu daudzuma, no kravas rindas ir jānoņem arī novecojušais daudzums. Pretējā gadījumā, ja netiek iestatīta pareiza nepietiekamas piegādes vērtība, kravas rindai nevar apstiprināt sūtīšanu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]