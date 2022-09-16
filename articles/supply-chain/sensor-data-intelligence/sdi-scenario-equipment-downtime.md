---
title: Datora statusa scenārijs
description: Šajā rakstā aprakstīts datora statusa scenārijs, kas ļauj jums izmantot sensora datus, lai pārraudzītu jūsu aprīkojuma pieejamību.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 1f2b424dccf1963a7917059d412b5df7937496ee
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428996"
---
# <a name="the-machine-status-scenario"></a>Datora statusa scenārijs

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Datora *statusa scenārijā* varat izmantot sensora datus, lai pārraudzītu jūsu aprīkojuma pieejamību. Ja iestatāt sensoru, kas sūta signālu, kad datora resursa ražošanas darbs rada ražojumu, bet noteiktā intervālā netiek saņemts sensora signālu, supervizora informācijas panelī tiek parādīts paziņojums.

## <a name="scenario-dependencies"></a>Scenārija atkarības

Datora *statusa* scenārijam ir šādas atkarības:

- Paziņojumu var nosūtīt tikai tad, ja ražošanas darbs tiek veikts kartētā datorā.
- UzIoT pārkraušanas *punktu jāsūta* signālu, kas norāda daļēji izeju.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Sagatavot demonstrācijas datus datora statusa scenārijam

Ja vēlaties *izmantot* demonstrācijas sistēmu, lai pārbaudītu datora statusa scenāriju, izmantojiet sistēmu, [kur ir instalēti demonstrācijas](../../fin-ops-core/fin-ops/get-started/demo-data.md) dati, *atlasiet USMF juridisko* personu (uzņēmumu) un sagatavojiet papildu demonstrācijas datus, kā aprakstīts šajā sadaļā. Ja izmantojat pats savu sensoru un datus, varat izlaist šo sadaļu.

### <a name="set-up-a-sensor-simulator"></a>Iestatiet sensora simulatoru

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

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Ražošanas izpildes interfeisa konfigurēšana

Ražošanas izpildes interfeiss tiks izmantots *, lai sāktu darbu, kas iepriekšējā sadaļā ieplānots un izdots krājumam ar numuru P0111*. Sekojiet šiem soļiem, lai konfigurētu ražošanas izpildes interfeisu.

1. Dodieties uz **Ražošanas kontrole \> Ražošanas izpilde \> Ražotnes izpilde**.
1. Ja iepriekš neesat iestatījis interfeisu, parādās pierakstīšanās lapa. Ievadiet savus akreditācijas datus.
1. Sveiciena lapā atlasiet **Konfigurēt**, lai atvērtu ierīces **konfigurēšanas** vedni.
1. Lapā Konfigurēt **ierīci — 1. solis — atlasiet** konfigurācijas lapu, atlasiet noklusējuma *konfigurāciju*.
1. Atlasiet **Nākamais**.
1. Lapā Konfigurēt **ierīci - 2. solis -** Definējiet ražošanas apgabala lapu, iestatiet **resursa lauku** *uz 3118*.
1. Atlasiet **Labi**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a> Iespējot meklēšanas opciju ražošanas izpildes interfeisā

Lai atvieglotu agrāk izlaista ražošanas pasūtījuma ražošanas darba a meklēšanu, izpildiet šos soļus, lai iespējotu meklēšanas opciju ražošanas izpildes interfeisā.

1. Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.
1. Atlasiet Noklusēto *konfigurāciju*.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju Iespējot **meklēšanu** kā *Jā*.
1. Aizvērt lapu.

### <a name="start-the-first-job-in-the-batch-order"></a>Sākt pirmo darbu pakešveida pasūtījumā

Izpildiet šos soļus, lai sāktu darbu, kas ieplānots resursam *3118*.

1. Dodieties uz **Ražošanas kontrole \> Ražošanas izpilde \> Ražotnes izpilde**.
1. Žetona **ID** laukā ievadiet *123*. Pēc tam atlasiet **pieteikšanās.**
1. Ja tiek piedāvāts kavējuma iemesls, atlasiet vienu no kartēm par kavējumu un pēc tam atlasiet **Labi**.
1. **Meklēšanas laukā** ievadiet partijas pasūtījuma numuru, par kuru iepriekš atzīmējāt. Pēc tam atlasiet atgriešanas **taustiņu**.
1. Atlasiet pasūtījumu un pēc tam atlasiet Sākt **darbu**.
1. **Dialoglodziņā Sākt darbu** atlasiet **Sākt**.

## <a name="set-up-the-machine-status-scenario"></a>Iestatīt datora statusa scenāriju

Ievērojiet šos soļus, lai iestatītu *datora statusa scenāriju* Piegādes ķēžu pārvaldībā.

1. Pārejiet uz **ražošanas kontroles iestatīšanas \>\> sensora datu inteliģences \> scenārijiem**.
1. Lodziņā Datora **statusa scenārijs** atlasiet **Konfigurēt**, lai atvērtu šī scenārija iestatīšanas vedni.
1. **Lapā Sensors** atlasiet **Jauns**, lai režģim pievienotu sensoru. Pēc tam iestatiet tai sekojošos laukus:

    - **Sensora ID** – ievadiet jūsu lietotā sensora ID. (Ja izmantojat Pārkaru PI Azure IoT tiešsaistes simulatoru un esat to iestatījis kā aprakstīts [Iestatiet simulētu sensoru testēšanai](sdi-set-up-simulated-sensor.md), ievadiet *MachineStatus*.)
    - **Sensora** apraksts – ievadiet sensora aprakstu.

1. Atkārtojiet iepriekšējo soli ar katru papildu sensoru, ko vēlaties pievienot tagad. Jebkurā laikā varat atgriezties un pievienot vairāk sensoru.
1. Atlasiet **Nākamais**.
1. Biznesa ierakstu **kartēšanas lapā** sadaļā **Sensors** atlasiet ierakstu vienam no tikko pievienotiem sensoriem.
1. Sadaļā Biznesa **ierakstu kartēšana** atlasiet **Jauns**, lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet biznesa ieraksta lauku **resursam**, kuru izmantojat, lai pārraudzītu atlasīto sensoru. (Ja izmantojat agrāk šajā rakstā izveidotos demonstrācijas datus, *iestatiet lauku uz 3118, Ar griešanas iekārtu*.)
1. Atlasiet **Nākamais**.
1. Lapā Datora **statusa slieksnis** definējiet, cik ilgi pēc *pēdējā* pārtraukuma signāļa sistēmai jānosūta datora statusa paziņojums. Slieksni var definēt divējādi:

    - **Noklusējuma slieksnis (minūtēs)** – iestatiet šo lauku, lai definētu noklusējuma slieksni. Tad šī vērtība tiks lietota visiem resursiem, **kur slieksnis, lai noteiktu, vai dators neatbild (minūtēs),** ir iestatīts uz divām minūtēm vai mazāku. Minimālā vērtība ir *2* (minūtes).
    - **Slieksnis, lai noteiktu iekārtu, kura neatbild (minūtēs)** — katram resursam režģī, kuram nevēlaties izmantot noklusējuma slieksni, ievadiet šajā laukā ignorēšanas vērtību. Resursi, kas iestatīti divu minūšu vai mazāk sliekšņa izmantošanai, izmantos noklusējuma **sliekšņa (minūšu)** iestatījumu.

    > [!NOTE]
    > Parasti jūs izmantosiet part-out *signālu* iekārtas statusa pārraudzībā. Tāpēc jums ir jāpārliecinās, vai katra iekārtas resursa slieksnis ir garāks nekā datoram nepieciešams ražot katru daļu.

1. Atlasiet **Nākamais**.
1. Režģī **aktivizējiet sensoru** lapu, atlasiet pievienoto sensoru un pēc tam atlasiet **Aktivizēt**. Katram aktivizētam sensoram režģī aktīvā kolonnā parādās **atzīme**.
1. Atl. **Pabeigt**.

## <a name="work-with-the-machine-status-scenario"></a>Darbs ar datora statusa scenāriju

Pēc jūsu sensoru instalēšanas un scenārija konfigurēšanas, varat aplūkot datora statusa notikumus Piegādes ķēžu pārvaldībā. Šajā sadaļā ir aprakstīts, kur un kā skatīt šo informāciju.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Skatīt datora statusa datus resursu statusa lapā

Resursu statusa **lapā supervizori** var pārraudzīt no sensoriem saņemtā daļas brīdinājuma laika skalu, *kas* ir kartēta uz katru iekārtas resursu. Sekojiet šiem soļiem, lai konfigurētu laika skalu.

1. Pārejiet uz **ražošanas kontroles \> ražošanas izpildes \> resursa statusu**.
1. **Dialoglodziņā Konfigurēt** iestatiet šādus laukus:

    - **Resurss** — atlasiet resursus, kurus vēlaties pārraudzīt. (Ja strādājat ar demonstrācijas datiem, atlasiet *3118*.)
    - **1. laika sērija** – atlasiet ierakstu (metrisko atslēgu), kura nosaukumam ir šāds formāts: *MachineReportingStatus:&lt; Sensor&gt;*
    - **Parādāmais vārds** – ievadiet *daļas no ārpusa*.

Šajā attēlā parādīts datora statusa datu piemērs resursa statusa **lapā standarta** operācijas laikā.

![Iekārtas statusa dati resursu statusa lapā standarta operācijas laikā.](media/sdi-resource-status-downtime-up.png "Iekārtas statusa dati resursu statusa lapā standarta operācijas laikā")

Šajā attēlā parādīts datora statusa datu piemērs, kad tiek atrastas dīkstāves laiks.

![Datora statusa dati resursu statusa lapā, kad ir noteiktas dīkstāves laiks.](media/sdi-resource-status-downtime-down.png "Datora statusa dati resursu statusa lapā, kad ir noteiktas dīkstāves laiks")

### <a name="view-machine-status-on-the-notifications-page"></a>Skatīt datora statusu paziņojumu lapā

Lapā Paziņojumi **supervizori var skatīt paziņojumus, kas tiek ģenerēti, kad ir pagājis pārāk daudz laika kopš brīža, kad sensors** *pēdējais* piegādāja detalizētu signālu. Katrs paziņojums sniedz apskatu par ražošanas darbu, kuru ietekmē aiziešanu, un sniedz iespēju atkārtoti piešķirt ietekmēto darbu citam resursam.

Lai atvērtu paziņojuma **lapu**, dodieties uz ražošanas **kontroles vaicājumiem \> un pārskatiem \> par sensora datu informācijas \> paziņojumiem**.

Šajā attēlā parādīts mašīnas statusa paziņojuma piemērs.

![Datora statusa paziņojuma piemērs.](media/sdi-resource-status-downtime-notification.png "Datora statusa paziņojuma piemērs")
