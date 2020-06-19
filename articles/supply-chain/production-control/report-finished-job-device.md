---
title: Reģistrējiet pabeigšanu, izmantojot darba kartes ierīci
description: Šajā tēmā ir aprakstīts, kā konfigurēt sistēmu, lai darba kartes ierīces lietotāji varētu ziņot par pabeigtajām precēm no ražošanas pasūtījuma uz krājumiem.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403266"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Reģistrējiet pabeigšanu, izmantojot darba kartes ierīci

[!include [banner](../includes/banner.md)]

Darbinieki izmanto lapu **Pārskatu norises** darba kartes ierīcē, lai ziņotu par ražošanas darbam pabeigtajiem daudzumiem.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Kontrolēt, vai krājumiem ir pievienoti pabeigtie daudzumi

Lai kontrolētu, vai un kā pēdējā operācijā fiziski pabeigtie daudzumi jāpievieno krājumiem, veiciet tālāk minētās darbības.

1. Dodieties uz **Preces kontrole \> Iestatīšana \> Ražošanas izpilde \> Ražošanas pasūtījuma noklusējuma vērtības**.
1. Cilnē **Reģistrēt kā pabeigtu** iestatiet lauku **Atjaunināt pabeigto pārskatu tiešsaistē** uz vienu no tālāk minētajām vērtībām.

    - **Nē** — daudzums netiks pievienots krājumiem, kad daudzumi tiek reģistrēti pēdējā operācijā. Ražošanas pasūtījuma statuss nekad nemainīsies.
    - **Statuss + daudzums** — ražošanas pasūtījuma statuss tiks mainīts uz *Reģistrēts kā pabeigts*, un daudzums tiks reģistrēts kā pabeigts noliktavā.
    - **Daudzums** — daudzums tiks reģistrēts kā pabeigts noliktavā, bet ražošanas pasūtījuma statuss nekad nemainīsies.
    - **Statuss** — mainīsies tika ražošanas pasūtījuma statuss. Neviens daudzums netiks pievienots krājumiem, kad daudzumi tiek reģistrēti pēdējā operācijā.

> [!NOTE]
> Daudzumi netiek izsekoti krājumos, ja darbības, kuras ir reģistrētas kā pabeigtas, nav definētas kā pēdējā operācija. Tomēr šos daudzumus var izmantot, lai skatītu norisi. Tās var iekļaut arī kārtulās, kas kontrolē, vai darbinieki var sākt nākamo operāciju, pirms ir sasniegta noteiktā reģistrēto daudzumu robežvērtība iepriekšējā operācijā. Varat definēt šīs kārtulas cilnē **Daudzuma pārbaude**, kas atrodas lapā **Ražošanas pasūtījuma noklusētās vērtības**.

Papildinformāciju par to, kā strādāt ar lapu **Ražošanas pasūtījuma noklusētās vērtības**, skatiet [Ražošanas parametri ražošanas izpildē](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Reģistrēt partijas kontrolētos elementus kā pabeigtus

Darba kartes ierīce atbalsta trīs scenārijus ziņošanai par partijas elementiem. Šie scenāriji attiecas gan uz elementiem, kas ir iespējoti papildu noliktavas procesiem, gan uz elementiem, kas nav iespējoti papildu noliktavas procesiem.

- **Manuāli piešķirtie partijas numuri:** darbinieki ievada pielāgotu partijas numuru. Šis partijas numurs var būt no ārēja avota, kas sistēmai nav zināms.
- **Iepriekš definētie partijas numuri:** darbinieki atlasa partijas numuru partiju numuru sarakstā, ko sistēma automātiski izveido pirms ražošanas pasūtījuma nodošanas darba kartes ierīcei.
- **Fiksēti partijas numuri:** darbinieki neievada vai neatlasa partijas numuru. Tā vietā sistēma automātiski piešķir ražošanas pasūtījumam partijas numuru, pirms tas tiek izlaists ražošanai.

Lai iespējotu katru scenāriju, izpildiet tālāk aprakstītās darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet konfigurējamo preci.
1. Kopsavilkuma cilnes **Pārvaldīt krājumu** laukā **Partijas numuru grupa** atlasiet izsekošanas numuru grupu, kas iestatīta, lai atbalstītu jūsu scenāriju.

> [!NOTE]
> Pēc noklusējuma, ja partijas kontrolētajai precei nav piešķirta partijas numuru grupa, darba kartes ierīce nodrošina manuālu partijas numura ievadi reģistrācijas kā pabeigts laikā.

Šajās apakšsadaļās aprakstīts, kā iestatīt izsekošanas numuru grupas, lai atbalstītu katru no trim scenārijiem pārskatam par partijas elementiem.

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a>Partijas numura pārskata iespējošana darba kartes ierīcē

Lai iespējotu jūsu darbu karšu ierīces akceptēt partijas numuru, ziņojot par pabeigšanu, ir jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu tālāk norādītos līdzekļus (minētajā secībā).

1. Uzlabota lietotāja pieredze darba karšu ierīces norises pārskata dialogā
1. Iespējojiet, lai ievadītu partijas un sērijas numurus, vienlaikus ziņojot kā par pabeigtu no darba karšu ierīces (priekšskatījums)

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Iestatiet izsekošanas numuru grupu, kas ļauj darbiniekiem manuāli piešķirt partijas numuru

Lai ļautu manuāli piešķirt partijas numurus, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Manuāli** uz **Jā**.

    ![Izsekošanas numuru grupu lapa](media/tracking-number-group-manual.png "Izsekošanas numuru grupu lapa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir teksta lodziņš, kurā darbinieki var ievadīt jebkuru vērtību.

![Pārskata norises lapa ar lauku manuāliem partijas numuriem](media/job-card-device-batch-manual.png "Pārskata norises lapa ar lauku manuāliem partijas numuriem")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Iestatiet izsekošanas numuru grupu, kas nodrošina iepriekš definētu partijas numuru sarakstu

Lai nodrošinātu iepriekš definētu partijas numuru sarakstu, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana > Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Jā**.
1. Lietojiet lauku **Daudzumam**, lai sadalītu partijas numurus pēc daudzuma, pamatojoties uz ievadīto vērtību. Piemēram, jums ir ražošanas pasūtījums desmit vienībām un lauks **Daudzumam** ir iestatīts uz *2*. Šādā gadījumā, izveidojot ražošanas pasūtījumu, tam tiks piešķirti pieci partijas numuri.

    ![Izsekošanas numuru grupu lapa](media/tracking-number-group-predefined.png "Izsekošanas numuru grupu lapa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir nolaižams saraksts, kurā darbiniekiem jāievada iepriekš definētā vērtība.

![Pārskata norises lapa ar iepriekš definēto partijas numuru sarakstu](media/job-card-device-batch-predefined.png "Pārskata norises lapa ar iepriekš definēto partijas numuru sarakstu")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Iestatiet izsekošanas numuru grupu, kas automātiski piešķir partijas numurus

Ja partijas numuri jāpiešķir automātiski — bez darbinieka ievades — veiciet tālāk minētās darbības, lai iestatītu izsekošanas numuru grupu.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Nē**.
1. Iestatiet opciju **Manuāli** uz **Nē**.

    ![Izsekošanas numuru grupu lapa](media/tracking-number-group-fixed.png "Izsekošanas numuru grupu lapa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, rāda vērtību, bet darbinieki nevar to rediģēt.

![Pārskata norises lapa ar fiksētu partijas numuru](media/job-card-device-batch-fixed.png "Pārskata norises lapa ar fiksētu partijas numuru")

## <a name="report-as-finished-to-a-license-plate"></a>Ziņojums par pabeigšanu noliktavas unikālajai vienībai

Papildu noliktavas procesi var izmantot noliktavas unikālās vienības dimensiju, lai izsekotu krājumus noliktavas vietās, kas ir iestatītas šim nolūkam. Šādā gadījumā ir nepieciešams unikāls noliktavas vienības identifikators, kad darbinieks ziņo par pabeigtajiem daudzumiem.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Noliktavas unikālās vienības ziņošanas un uzlīmes drukāšanas iespējošana

Lai izmantotu šajā sadaļā aprakstītos līdzekļus, jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu tālāk norādītos līdzekļus (minētajā secībā).

1. Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu
1. Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss
1. Izdrukāt etiķeti no darba karšu ierīces

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Iestatīt ziņošanu par pabeigšanu noliktavas unikālajai vienībai

Lai kontrolētu, vai darbiniekiem ir atkārtoti jāizmanto esoša noliktavas vienība vai jāģenerē jauna noliktavas vienība, kad tiek reģistrēta krājumu pabeigšana, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Ražošanas kontrole \> Iestatīšana \> Ražošanas izpilde \> Konfigurēt darbu karti ierīcēm**.
2. Iestatiet tālāk norādītās opcijas katrai ierīcei.

    - **Ģenerēt noliktavas vienību** — iestatiet šo opciju uz **Jā**, lai katram pārskatam ģenerētu jaunas noliktavas vienības pabeigšanu. Iestatiet to uz **Nē**, ja katram pārskatam ir jāizmanto esoša noliktavas vienība kā pabeigta.
    - **Drukāt etiķeti** — iestatiet šo opciju uz **Jā**, ja darbiniekam ir jādrukā noliktavas vienības etiķete katram pārskatam kā pabeigta. Iestatiet to uz **Nē**, ja etiķete nav nepieciešama. 

![Konfigurēt darbu karti ierīču lapai](media/config-job-card-raf.png "Konfigurēt darbu karti ierīču lapai")

> [!NOTE]
> Lai konfigurētu etiķeti, dodieties uz **Noliktavas vadība \> Iestatīšana \> Dokumentu maršrutēšana \> Dokumentu maršrutēšana**. Papildinformāciju skatiet [Iespējot noliktavas vienības etiķetes drukāšanu](../warehousing/tasks/license-plate-label-printing.md).
