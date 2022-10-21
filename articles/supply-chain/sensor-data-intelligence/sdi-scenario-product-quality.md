---
title: Produkta kvalitātes scenārijs
description: Šajā rakstā ir sniegta informācija par preces kvalitātes scenāriju. Šajā scenārijā tiek izmantots sensors, lai izmērītu preču paketes kvalitāti un ģenerētu brīdinājumu, ja mērījums neatrodas definētajā slieksni.
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
ms.openlocfilehash: c0f1c57251234921779f67faf61d47cdde119e64
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690053"
---
# <a name="the-product-quality-scenario"></a>Produkta kvalitātes scenārijs

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Produkta kvalitātes *scenārijā* ir iestatīts sensors, lai izmērītu produkta paketes kvalitāti ražotnes uz grīdas. Ja mērījums atrodas ārpus produkta definētā sliekšņa, paziņojums tiek rādīts supervizora vadības panelī. Piemēram, ar sensoru tiek mērīts produkts, kas tiek saražots no ražošanas līnijas. Ja mērījums ir ārpus preces minimālās vai maksimālās vērtības, tiek ģenerēts paziņojums.

## <a name="scenario-dependencies"></a>Scenārija atkarības

Produkta *kvalitātes* scenārijam ir šādas atkarības:

- Brīdinājumu var parādīt tikai tad, ja ražošanas pasūtījums darbojas uz kartētas mašīnas un ja šī iekārta ražo preci, kam ir kartēts partijas atribūts.
- Signāls, kas apzīmē partijas atribūtu, ir jānosūta uz IoT Hub, un ir jāiekļauj unikāls rekvizīta nosaukums.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Sagatavot demonstrācijas datus preces kvalitātes scenārijam

Ja vēlaties *izmantot* demonstrācijas sistēmu, lai pārbaudītu produkta kvalitātes scenāriju, izmantojiet sistēmu, [kur ir instalēti demonstrācijas](../../fin-ops-core/fin-ops/get-started/demo-data.md) dati, *atlasiet USMF juridisko* personu (uzņēmumu) un sagatavojiet papildu demonstrācijas datus, kā aprakstīts šajā sadaļā. Ja izmantojat pats savu sensoru un datus, varat izlaist šo sadaļu.

Šajā sadaļā jūs iestatīsiet demonstrācijas *datus, lai varētu izmantot izlaisto preci P0111* (Composite *Case*) ar *preces kvalitātes scenāriju*. Šajā scenārijā sistēma izseko, vai partijas atribūta vērtība, ko mēra ar sensoru, ir ārpus ar preci saistītā partijas atribūta definētās sliekšņa vērtības.

### <a name="set-up-a-sensor-simulator"></a>Iestatiet sensora simulatoru

Ja vēlaties mēģināt šo scenāriju, neizmantojot fizisku sensoru, varat iestatīt simulatoru, lai ģenerētu nepieciešamos signālus. Papildinformāciju skatiet sadaļā [Simulētā sensora iestatīšana testēšanai](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Saistīt partijas atribūtu un resursu ar preci P0111

Izpildiet šīs darbības *, lai saistītu partijas atribūtu ar preci P0111* (*Kompozītiepakojums*) *un pārbaudītu, ka resursam 3118 (* Datora *griešana) tiek izmantots resurss 3118*.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atrodiet un atlasiet preci, kuras krājuma **numura lauks** ir iestatīts uz *P0111*.
1. Darbību rūts cilnes Pārvaldīt krājumu **partijas** atribūtu **grupā** atlasiet Precei **raksturīga.**
1. Lapā Precei **raksturīgai** lapai atlasiet **Jauns**, lai izveidotu precei raksturīgu partijas atribūtu.
1. Virsrakstā iestatiet šādus laukus:

    - **Atribūta kods** – atlasiet pārraugāmo atribūtu diapazonu (*Tabula*, Grupa *vai* *Visi*). Šim scenārijam atlasiet *Tabulu*, jo jūs vienmēr pārraudzīsiet vienu atribūtu.
    - **Atribūta relācija** – atlasiet atribūtu, kuru izmantosiet *preces kvalitātes scenārijā*, lai uzraudzītu vērtību. Šajā piemērā izvēlieties *Ieturēts*, kas ir atribūts, kas ir iekļauts standarta demonstrācijas datos.

1. Kopsavilkuma cilnes **Vērtības** laukos **Minimālais** **un** Maksimālais definējiet pieņemamo vērtību diapazonu, par kādu atribūtam ir jāatbilst kvalitātes pārbaudei. Ja sensors sniedz pārskatu par vērtību ārpus šī diapazona, sistēma to identificēs kā kvalitātes pārkāpumu. Citi šīs FastTab lauki nav saistīti ar preces kvalitātes *scenāriju*. Pašlaik redzētās noklusētās vērtības ir no demonstrācijas datiem. Tāpēc atstājiet tos tāpat, kā tie ir, **·** **un** aizveriet lapu Precei, lai atgrieztos izpildei nodoto preču informācijas lapā par krājumu *P0111.*
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

## <a name="set-up-the-product-quality-scenario"></a>Iestatīt preces kvalitātes scenāriju

Sekojiet šiem soļiem, lai iestatītu *preces kvalitātes scenāriju* Piegādes ķēžu pārvaldībā.

1. Pārejiet uz **ražošanas kontroles iestatīšanas \>\> sensora datu inteliģences \> scenārijiem**.
1. Lodziņā Preces **kvalitātes scenārijs** atlasiet **Konfigurēt**, lai atvērtu iestatīšanas vedni šim scenārijam.
1. **Lapā Sensors** atlasiet **Jauns**, lai režģim pievienotu sensoru. Pēc tam iestatiet tai sekojošos laukus:

    - **Sensora ID** – ievadiet jūsu lietotā sensora ID. (Ja izmantojat Pārkaru PI Azure IoT tiešsaistes simulatoru un esat to iestatījis kā aprakstīts [Iestatīt simulētu sensoru testēšanai](sdi-set-up-simulated-sensor.md), ievadiet *Kvalitāti*.)
    - **Sensora** apraksts – ievadiet sensora aprakstu.

1. Atkārtojiet iepriekšējo soli ar katru papildu sensoru, ko vēlaties pievienot tagad. Jebkurā laikā varat atgriezties un pievienot vairāk sensoru.
1. Atlasiet **Nākamais**.
1. Biznesa ierakstu **kartēšanas lapā** sadaļā **Sensors** atlasiet ierakstu vienam no tikko pievienotiem sensoriem.
1. Sadaļā Biznesa **ierakstu kartēšana** atlasiet **Jauns**, lai režģim pievienotu rindu.
1. Jaunajā rindā biznesa ieraksta tipa **lauks automātiski** jāiestata uz *Resources(WrkCtrTable)*. Iestatiet biznesa **ieraksta lauku** resursam, kuru izmantojat, lai pārraudzītu atlasīto sensoru. (Ja izmantojat agrāk šajā rakstā izveidotos demonstrācijas datus, iestatiet to *uz 3118, Summu griešanas iekārta*.)
1. Uzreiz pēc biznesa ieraksta tipa atlases rindai, kuru pievienojāt iepriekšējā solī, režģim automātiski tiek pievienota otrā rinda. Šajā rindā biznesa ieraksta tipa **laukam** jābūt iestatītam uz *Partijas atribūti (PdsBatchAttrib)*. Iestatiet biznesa **ieraksta lauku** uz partijas atribūtu, kuru izmantojat izvēlētā sensora pārraudzībai. (Ja izmantojat agrāk šajā rakstā izveidotos demonstrācijas datus, iestatiet to uz *iepriekš atstāstības, procentuālais daudzums procentos*).
1. Atlasiet **Nākamais**.
1. Režģī **aktivizējiet sensoru** lapu, atlasiet pievienoto sensoru un pēc tam atlasiet **Aktivizēt**. Katram aktivizētam sensoram režģī aktīvā kolonnā parādās **atzīme**.
1. Atl. **Pabeigt**.

## <a name="work-with-the-product-quality-scenario"></a>Darbs ar preces kvalitātes scenāriju

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Skatīt preces kvalitātes datus resursu statusa lapā

Lapā Resursu **statuss supervizori** var pārraudzīt produktu kvalitātes signālu laika grafiku, kas tiek saņemts no sensoriem, kas ir kartēti katram iekārtas resursam. Sekojiet šiem soļiem, lai konfigurētu laika skalu.

1. Pārejiet uz **ražošanas kontroles \> ražošanas izpildes \> resursa statusu**.
1. **Dialoglodziņā Konfigurēt** iestatiet šādus laukus:

    - **Resurss** — atlasiet resursus, kurus vēlaties pārraudzīt. (Ja strādājat ar demonstrācijas datiem, atlasiet *3118*.)
    - **1. laika sērija** – atlasiet ierakstu (metrisko atslēgu), kura nosaukumam ir šāds formāts: *ProductQuality:&lt; JobId&gt;:&lt; AttributeName&gt;*
    - **Parādāmais nosaukums** - ievadiet *partijas atribūta vērtības*.

Šajā attēlā parādīts preču kvalitātes datu piemērs resursu **statusa** lapā, kad vērtība ir pieņemamo vērtību diapazonā.

![Preces kvalitātes dati resursu statusa lapā, kad vērtība ir diapazonā.](media/sdi-product-quality-in-range.png "Preces kvalitātes dati resursu statusa lapā, kad vērtība ir diapazonā")

Šajā attēlā parādīts preču kvalitātes datu piemērs, kad noteikta ārpus diapazona vērtība.

![Preces kvalitātes dati resursu statusa lapā, kad noteikta ārpus diapazona vērtība.](media/sdi-product-quality-out-of-range.png "Preces kvalitātes dati resursu statusa lapā, kad noteikta ārpus diapazona vērtība")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Skatīt preces kvalitātes datus paziņojumu lapā

Supervizori **lapā Paziņojumi var skatīt paziņojumu, kas tiek ģenerēts, kad sensors** mēra partijas atribūta vērtību, kas ir ārpus partijas atribūta definētā sliekšņa. Katrs paziņojums sniedz apskatu par ražošanas darbu, kuru ietekmē aiziešanu, un sniedz iespēju atkārtoti piešķirt ietekmēto darbu citam resursam.

Lai atvērtu paziņojuma **lapu**, dodieties uz ražošanas **kontroles vaicājumiem \> un pārskatiem \> par sensora datu informācijas \> paziņojumiem**.

Šajā ilustrācijā parādīts preces kvalitātes paziņojuma piemērs.

![Preces kvalitātes paziņojuma piemērs.](media/sdi-product-quality-notification.png "Preces kvalitātes paziņojuma piemērs")
