---
title: Ražošanas aizkaves scenārijs
description: Šajā rakstā ir aprakstīts ražošanas aizkavēšanās scenārijs, kas ģenerē paziņojumu, ja ražošanas caurlaide samazinās zem noteiktas sliekšņa vērtības.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690026"
---
# <a name="the-production-delays-scenario"></a>Ražošanas aizkaves scenārijs

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Ražošanas *aizkavēšanās scenārijs* ģenerē paziņojumu, ja ražošanas caurlaide ir zem noteiktas sliekšņa vērtības. Šajā scenārijā katram saražotam *krājumam* tiek nosūtīts Microsoft Azure atstādāls IoT hub. Šādā Dynamics 365 Supply Chain Management gadījumā pasūtījuma aizkave tiek aprēķināta, pamatojoties uz laiku, cik ilgi ražošanas pasūtījums ir plānots palaist, ražomo krājumu skaitu, *darba* izpildes laiku un saņemto daļēji pabeigto signālu skaitu. Ja nepilna darba brīdinājumu skaits zem sliekšņa *vērtības samazinās*, tiek ģenerēts paziņojums par aizkavēšanos.

## <a name="scenario-dependencies"></a>Scenārija atkarības

Ražošanas *aizkavēšanās scenārijam* ir šādas atkarības:

- Brīdinājums var tikt parādīts tikai tad, ja ražošanas pasūtījums darbojas kartētā iekārtā.
- Uz IoT hub jāsūta *kartēta* datora daļējie atslēglauku un jāiekļauj unikāls rekvizīta nosaukums.
- UNIX rekvizīts laikspiedols, kur vērtība ir izteikta milisekundēs (ms), ir jāatrodas Azure IoT Hub ziņojumā.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Sagatavot demonstrācijas datus preces aizkaves scenārijam

Ja vēlaties *izmantot* demonstrācijas sistēmu, lai pārbaudītu ražošanas aizkavēšanās scenāriju, izmantojiet sistēmu, [kur ir instalēti demonstrācijas](../../fin-ops-core/fin-ops/get-started/demo-data.md) dati, *atlasiet USMF juridisko* personu (uzņēmumu) un sagatavojiet papildu demonstrācijas datus, kā aprakstīts šajā sadaļā. Ja izmantojat pats savu sensoru un datus, varat izlaist šo sadaļu.

### <a name="set-up-sensor-simulator"></a>Iestatīt sensora simulatoru

Ja vēlaties mēģināt šo scenāriju, neizmantojot fizisku sensoru, varat iestatīt simulatoru, lai ģenerētu nepieciešamos signālus. Papildinformāciju skatiet sadaļā [Simulētā sensora iestatīšana testēšanai](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Pārbaudiet, vai resurss 3118 tiek izmantots precei P0111

Ražošanas pasūtījums tiks plānots un nodots izpildei. Tāpēc ražošanas darbs tiek izdots resursam *3118* (*Pasūtījumu griešanas iekārta*). Izpildiet šīs darbības, lai pārbaudītu, *vai resurss 3118* tiek izmantots precei *P0111* demonstrācijas datos.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atrodiet un atlasiet preci, kuras krājuma **numura lauks** ir iestatīts uz *P0111*.
1. Darbību rūts cilnes **Inženieris** grupā **Skats** atlasiet **Maršruts**.
1. **Maršruta lapas** cilnē Pārskats **lapas** apakšā atlasiet rindu, kur **oper. Nr.** Lauka <a0/& iestatījums *ir 30*.
1. Cilnē Resursu **prasības**, kas atrodas lapas apakšā, pārliecinieties, *ka ar operāciju ir saistīts resurss 3118* (*Ar* griešanas iekārtu).

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Izveidot un izlaist preces P0111 ražošanas pasūtījumu

Sekojiet šiem soļiem, lai izveidotu un izlaistu preces *P0111 ražošanas pasūtījumu*.

1. Doties uz **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.
1. Lapā Visi **ražošanas pasūtījumi** darbību rūtī atlasiet Jauns partijas **pasūtījums**.
1. Pakešuzdevuma **izveides** dialoglodziņā iestatiet šādas vērtības:

    - **Krājuma numurs:** *P0111*
    - **Daudzums:** *10*

1. Atlasiet **Izveidot**, lai izveidotu pasūtījumu un atgrieztos pie **visu ražošanas pasūtījumu** lapas.
1. Izmantojiet filtra **lauku**, lai meklētu ražošanas pasūtījumus, kur krājuma **numura lauks** ir iestatīts uz *P0111*. Pēc tam atrodiet un atlasiet tikko izveidoto ražošanas pasūtījumu.
1. Darbību rūts cilnē **Ražošanas pasūtījums**, grupā **Process** atlasiet **Aplēst**.
1. Novērtējuma dialoglodziņā **atlasiet** Labi, lai **palaistu** budžetu.
1. Darbību rūts cilnē Ražošanas **pasūtījums** grupā **Process** atlasiet Nodot **izpildei**.
1. Dialoglodziņā Izlaišana **(** izpildei) atzīmējiet tā pakešuzdevuma pasūtījuma numuru, kuru tikko izveidojāt.
1. Atlasiet **Labi,** lai izlaistu pasūtījumu.

### <a name="configure-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa konfigurēšana

Ja tas vēl nav izdarīts, konfigurējiet ražošanas izpildes interfeisu, *lai rādītu resursam 3118* piešķirtos darbus (*Informāciju par griešanas iekārtu*). Norādījumus skatiet šādās sadaļās:

- [Ražošanas izpildes interfeisa konfigurēšana](sdi-scenario-equipment-downtime.md#config-pfe)
- [Iespējot meklēšanas opciju ražošanas izpildes interfeisā](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Sākt pirmo darbu pakešveida pasūtījumā

Veiciet šīs darbības, lai sāktu pirmo darbu pakešuzdevumu pasūtījumā.

1. Dodieties uz **Ražošanas kontrole \> Ražošanas izpilde \> Ražotnes izpilde**.
1. Žetona **ID** laukā ievadiet *123*. Pēc tam atlasiet **pieteikšanās.**
1. Ja tiek piedāvāts kavējuma iemesls, atlasiet vienu no kartēm par kavējumu un pēc tam atlasiet **Labi**.
1. **Meklēšanas laukā** ievadiet partijas pasūtījuma numuru, par kuru iepriekš atzīmējāt. Pēc tam atlasiet atgriešanas **taustiņu**.
1. Atlasiet pasūtījumu un pēc tam atlasiet Sākt **darbu**.
1. **Dialoglodziņā Sākt darbu** atlasiet **Sākt**.

## <a name="set-up-the-production-delays-scenario"></a>Iestatīt ražošanas aizkaves scenāriju

Sekojiet šiem soļiem, lai iestatītu *ražošanas aizkavēšanās* scenāriju Piegādes ķēžu pārvaldībā.

1. Pārejiet uz **ražošanas kontroles iestatīšanas \>\> sensora datu inteliģences \> scenārijiem**.
1. Lodziņā Ražošanas **aizkaves** scenārijs atlasiet **Konfigurēt**, lai atvērtu iestatīšanas vedni šim scenārijam.
1. **Lapā Sensors** atlasiet **Jauns**, lai režģim pievienotu sensoru. Pēc tam iestatiet tai sekojošos laukus:

    - **Sensora ID** – ievadiet jūsu lietotā sensora ID. (Ja izmantojat Pārkaru PI Azure IoT tiešsaistes simulatoru un esat to iestatījis kā aprakstīts [Iestatīt simulētu sensoru testēšanai](sdi-set-up-simulated-sensor.md), ievadiet *ProductionDelay*.)
    - **Sensora** apraksts – ievadiet sensora aprakstu.

1. Atkārtojiet iepriekšējo soli ar katru papildu sensoru, ko vēlaties pievienot tagad. Jebkurā laikā varat atgriezties un pievienot vairāk sensoru.
1. Atlasiet **Nākamais**.
1. Biznesa ierakstu **kartēšanas lapā** sadaļā **Sensors** atlasiet ierakstu vienam no tikko pievienotiem sensoriem.
1. Sadaļā Biznesa **ierakstu kartēšana** atlasiet **Jauns**, lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet biznesa ierakstu **uz resursu**, kuru izvēlētā sensora jūs izmantojat, lai pārraudzītu. (Ja izmantojat agrāk šajā rakstā izveidotos demonstrācijas datus, iestatiet to *uz 3118, Summu griešanas iekārta*.)
1. Atlasiet **Nākamais**.
1. Ja izmantojat **agrāk šajā rakstā izveidotos** demonstrācijas datus, lapā Ražošanas aizkavēšanās novirzes slieksnis rīkojieties šādi:

    1. Atlasiet krājuma **saistības kolonnas** virsrakstu, lai atvērtu nolaižamo dialoglodziņu, kurā ir ietverti kolonnas meklēšanas filtri. Meklēšanas *lodziņā ievadiet P0111* un pēc tam atlasiet **Lietot**.
    2. Atlasiet rindu, kur operācijas **lauks** ir iestatīts uz Apgriezt */Izgriezt*. Iestatiet paziņojuma **slieksni aizkavēšanās (%)** laukam uz slieksni (kā procentus), par kādu jānosūta paziņojums.

1. Atlasiet **Nākamais**.
1. Režģī **aktivizējiet sensoru** lapu, atlasiet pievienoto sensoru un pēc tam atlasiet **Aktivizēt**. Katram aktivizētam sensoram režģī aktīvā kolonnā parādās **atzīme**.
1. Atl. **Pabeigt**.

## <a name="work-with-the-production-delays-scenario"></a>Darbs ar ražošanas aizkaves scenāriju

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Skatīt ražošanas aizkaves datus resursu statusa lapā

Resursu statusa **lapā supervizori** var pārraudzīt no katra datora resursa kartētajiem sensoriem saņemto signālu laicīgu grafiku. Sekojiet šiem soļiem, lai konfigurētu laika skalu.

1. Pārejiet uz **ražošanas kontroles \> ražošanas izpildes \> resursa statusu**.
1. **Dialoglodziņā Konfigurēt** iestatiet šādus laukus:

    - **Resurss** — atlasiet resursus, kurus vēlaties pārraudzīt. (Ja strādājat ar demonstrācijas datiem, atlasiet *3118*.)
    - **1** . laika sērija – atlasiet ierakstu (metrisko atslēgu), kura nosaukumam ir šāds formāts: *ProductionJobDelayed:ActualQuantity:&lt; JobId&gt;*
    - **Parādāmais vārds** – ievadiet *daļas no ārpusa.*
