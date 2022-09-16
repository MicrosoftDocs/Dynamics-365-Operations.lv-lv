---
title: Līdzekļa uzturēšanas scenārijs
description: Šajā rakstā aprakstīts līdzekļu uzturēšanas scenārijs, kas ļauj jums izmantot sensora datus, lai izveidotu skaitītāja ierakstus, kas seko mašīnas līdzekļu izmantošanai.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ff3944b987314a688a5829b05f8627479e3e79ed
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428993"
---
# <a name="the-asset-maintenance-scenario"></a>Līdzekļa uzturēšanas scenārijs

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Līdzekļu *uzturēšanas scenārijā* varat izmantot sensora datus, lai izveidotu skaitītāju ierakstus. Skaitītāja ieraksti izseko iekārtas pamatlīdzekļa izmantošanu un tiek izmantoti kā ievade, lai ģenerētu mašīnu līdzekļu uzturēšanas grafiku.

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Sagatavot demonstrācijas datus līdzekļa uzturēšanas scenārijam

Ja vēlaties *izmantot* demonstrācijas sistēmu, lai pārbaudītu līdzekļu uzturēšanas scenāriju, izmantojiet sistēmu, [kur ir instalēti demonstrācijas](../../fin-ops-core/fin-ops/get-started/demo-data.md) dati, *atlasiet USMF juridisko* personu (uzņēmumu) un sagatavojiet papildu demonstrācijas datus, kā aprakstīts šajā sadaļā. Ja izmantojat pats savu sensoru un datus, varat izlaist šo sadaļu.

Šajā sadaļā kā piemērs iestatīsiet *AK-101,* Gaisa transporta vērtību demonstrācijas datos. Tad redzēsiet, kā gaidāmos uzturēšanas darbus var prognozēt, balstoties uz sensora zīmi, kas mēra stundu skaitu, cik ilgi gaisa gaiss darbojas. Jūs iestatīsiet arī apkopes plānu, kur gaiss ir jāuztur ik pēc 10 000 stundām.

### <a name="set-up-a-sensor-simulator"></a>Iestatiet sensora simulatoru

Ja vēlaties mēģināt šo scenāriju, neizmantojot fizisku sensoru, varat iestatīt simulatoru, lai ģenerētu nepieciešamos signālus. Papildinformāciju skatiet sadaļā [Simulētā sensora iestatīšana testēšanai](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Izveidot līdzekļu skaitītāju, lai izsekotu ražošanas stundas

Sekojiet šiem soļiem, lai izveidotu līdzekļu skaitītāju ražošanas stundu izsekošanai.

1. Dodieties uz **Līdzekļu pārvaldība \> Iestatījumi \> Līdzekļu tipi \> Skaitītāji**.
1. Darbību rūtī atlasiet Jauns, lai **izveidotu** skaitītāju.
1. Galvenē iestatiet šādas vērtības:

    - **Skaitītājs:** *ProductionHr*
    - **Nosaukums:** *ražošanas stundas*

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Vienība:** *hr*
    - **Atjaunināt:** *manuāli*
    - **Kopējais apkopojums:** *summa*

1. Kopsavilkuma cilnē **Līdzekļu** veidi atlasiet Pievienot **rindu**.
1. Jaunajā rindā laukam Līdzekļa tips **iestatiet** vērtību *Gaiss*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Izveidot līdzekļa uzturēšanas plānu

Sekojiet šiem soļiem, lai izveidotu pamatlīdzekļa uzturēšanas plānu.

1. Dodieties uz Pamatlīdzekļu **pārvaldības iestatījuma \> Preventīvās \> uzturēšanas \> uzturēšanas plānu**.
1. Darbību rūtī atlasiet Jauns **, lai** izveidotu uzturēšanas plānu.
1. Galvenē iestatiet šādas vērtības:

    - **Uzturēšanas plāns:** *AirKnife*
    - **Nosaukums:** *Gaisa knupīju plāns*

1. Kopsavilkuma cilnē **Detalizēta informācija** iestatiet šādas vērtības:

    - **Plāna datums:** ievadiet šodienas datumu.
    - **Aktīvs:** *Jā*

1. Kopsavilkuma cilnē **Rindas** atlasiet Pievienot līdzekļu **skaitītāja rindu**, lai režģim pievienotu rindu. Pēc tam iestatiet tai šādas vērtības:

    - **Darba pasūtījuma apraksts:** *gaisa transporta uzturēšana*
    - **Uzturēšanas darba tips: preventīvs** *·*
    - **Intervāla tips:** *atkārtots no pēdējā darba pasūtījuma*
    - **Perioda biežums:** *10 000*
    - **Skaitītājs:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Iestatīt līdzekļa uzturēšanas scenāriju

Ievērojiet šos soļus, lai iestatītu *līdzekļu uzturēšanas scenāriju* Piegādes ķēžu pārvaldībā.

1. Dodieties uz **Pamatlīdzekļu pārvaldības iestatīšanas \>\> sensora datu informācijas \> scenārijiem**.
1. Lodziņā Līdzekļu **uzturēšanas scenārijs** atlasiet **Konfigurēt**, lai atvērtu šī scenārija iestatīšanas vedni.
1. **Lapā Sensors** atlasiet **Jauns**, lai režģim pievienotu sensoru. Pēc tam iestatiet tai sekojošos laukus:

    - **Sensora ID** – ievadiet jūsu lietotā sensora ID. (Ja izmantojat Pārkaru PI Azure IoT tiešsaistes simulatoru un esat to iestatījis kā aprakstīts [Iestatīt simulētu sensoru testēšanai](sdi-set-up-simulated-sensor.md), ievadiet *AssetMaintenance*.)
    - **Sensora** apraksts – ievadiet sensora aprakstu.

1. Atkārtojiet iepriekšējo soli ar katru papildu sensoru, ko vēlaties pievienot tagad. Jebkurā laikā varat atgriezties un pievienot vairāk sensoru.
1. Atlasiet **Nākamais**.
1. Biznesa ierakstu **kartēšanas lapā** sadaļā **Sensors** atlasiet ierakstu vienam no tikko pievienotiem sensoriem.
1. Sadaļā Biznesa **ierakstu kartēšana** atlasiet **Jauns**, lai režģim pievienotu rindu.
1. Jaunās rindas biznesa ieraksta tipa **laukam automātiski** jābūt iestatītam uz *Assets(EntAssetObjectTable)*. Iestatiet biznesa **ieraksta lauku** resursam, kuru izmantojat, lai pārraudzītu atlasīto sensoru. (Ja izmantojat agrāk šajā rakstā izveidotos demonstrācijas datus, iestatiet to uz *AK-101, AK-101 1. rindai ar gaisa kondicionēšanas informāciju*.)
1. Uzreiz pēc biznesa ieraksta tipa atlases rindai, kuru pievienojāt iepriekšējā solī, režģim automātiski tiek pievienota otrā rinda. Šajā rindā biznesa ieraksta tipa **laukam** jābūt iestatītam uz *Counters(EntAssetCounterType)*. Iestatiet biznesa **ieraksta lauku** uz līdzekļu skaitītāju, ko atjaunināt, ņemot vērā izvēlētā sensora signālus. (Ja izmantojat agrāk šajā rakstā izveidotos demonstrācijas datus, iestatiet to uz *ProductionHr, ražošanas stundas*.)
1. Atlasiet **Nākamais**.
1. Režģī **aktivizējiet sensoru** lapu, atlasiet pievienoto sensoru un pēc tam atlasiet **Aktivizēt**. Katram aktivizētam sensoram režģī aktīvā kolonnā parādās **atzīme**.
1. Atl. **Pabeigt**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Darbs ar līdzekļu uzturēšanas scenāriju

### <a name="view-counter-values"></a>Skatīt skaitītāju vērtības

Kad dati ir sagatavoti un *līdzekļa* uzturēšanas scenārijs ir konfigurēts un aktivizēts, varat redzēt, kā pamatlīdzekļu skaitītāja ieraksti tiek ievietoti, pamatojoties uz sensora datiem.

1. Dodieties uz **Visi \> pamatlīdzekļi, kas \> atrodas pamatlīdzekļu pārvaldībā**.
1. Atrodiet un atlasiet līdzekli, kuru vēlaties pārbaudīt. (Ja izmantojat demonstrācijas datus, ko iepriekš izveidojāt šajā rakstā, atlasiet *AK-101*.)
1. Darbību rūtī, uz **cilnes** Pamatlīdzeklis **grupā** **Preventīvs izvēlieties Skaitītāji,** lai atvērtu lapu skaitītāja ierakstiem pamatlīdzeklim *AK-101*.

### <a name="generate-maintenance-work-orders"></a>Ģenerēt uzturēšanas darba pasūtījumus

Pēc tam, kad iespējots *līdzekļa* uzturēšanas scenārijs un iestatīts uzturēšanas plāns, jūs variet palaist uzturēšanas grafiku, lai izveidotu uzturēšanas darba pasūtījumus. Papildinformāciju par to, kā strādāt ar preventīvu uzturēšanu, skatiet preventīvās [uzturēšanas apskatu](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
