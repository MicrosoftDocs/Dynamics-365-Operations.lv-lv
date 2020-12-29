---
title: Reģistrējiet pabeigšanu, izmantojot darba kartes ierīci
description: Šajā tēmā ir aprakstīts, kā konfigurēt sistēmu, lai darba kartes ierīces lietotāji varētu ziņot par pabeigtajām precēm no ražošanas pasūtījuma uz krājumiem.
author: johanhoffmann
manager: tfehr
ms.date: 07/31/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6ba5d8bc0c22f97e6d2ce61c636090e04fae5abd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432710"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Reģistrējiet pabeigšanu, izmantojot darba kartes ierīci

[!include [banner](../includes/banner.md)]

Darbinieki izmanto lapu **Pārskatu norises** darba kartes ierīcē, lai ziņotu par ražošanas darbam pabeigtajiem daudzumiem. Šajā tēmā ir aprakstīts, kā iestatīt dažādas opcijas, kas nosaka, kā darbinieki var ziņot par pabeigšanu, izmantojot šo lapu, un kas notiek tālāk. Opcijas ietver:

- Kontrolēt, vai un kā krājumiem tiek pievienoti pabeigtie daudzumi.
- Kontrolē, vai un kā partijas numuri tiek ģenerēti un pielietoti, ziņojot par pabeigšanu.
- Kontrolē, vai un kā sērijas numuri tiek ģenerēti un pielietoti, ziņojot par pabeigšanu.
- Kontrolē, vai un kā ziņot par pabeigšanu reģistrācijas numura zīmē.

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

- **Manuāli piešķirtie partijas numuri** - darbinieki ievada pielāgotu partijas numuru. Šis partijas numurs var būt no ārēja avota, kas sistēmai nav zināms.
- **Iepriekš definētie partijas numuri** - darbinieki atlasa partijas numuru partiju numuru sarakstā, ko sistēma automātiski izveido pirms ražošanas pasūtījuma nodošanas darba kartes ierīcei.
- **Fiksēti partijas numuri** - darbinieki neievada vai neatlasa partijas numuru. Tā vietā sistēma automātiski piešķir ražošanas pasūtījumam partijas numuru, pirms tas tiek izlaists ražošanai.


### <a name="enable-the-feature-on-your-system"></a>Iespējot līdzekli sistēmā

Lai iespējotu jūsu darbu karšu ierīces akceptēt partijas numuru, ziņojot par pabeigšanu, ir jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu tālāk norādītos līdzekļus (minētajā secībā).

1. Uzlabota lietotāja pieredze darba karšu ierīces norises pārskata dialogā
1. Iespējojiet, lai ievadītu partijas un sērijas numurus, vienlaikus ziņojot kā par pabeigtu no darba karšu ierīces (priekšskatījums)

### <a name="configure-products-that-require-batch-number-reporting"></a>Konfigurēt preces, kurām nepieciešams partijas numura pārskats

Lai iespējotu preci, kas atbalsta jebkuru no pieejamajiem partijas kontrolētajiem scenārijiem, rīkojieties šādi:

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet konfigurējamo preci.
1. Kopsavilkuma cilnes **Pārvaldīt krājumu** laukā **Partijas numuru grupa** atlasiet izsekošanas numuru grupu, kas iestatīta, lai atbalstītu jūsu scenāriju.

> [!NOTE]
> Pēc noklusējuma, ja partijas kontrolētajai precei nav piešķirta partijas numuru grupa, darba kartes ierīce nodrošina manuālu partijas numura ievadi reģistrācijas kā pabeigts laikā.

Šajās sadaļās aprakstīts, kā iestatīt izsekošanas numuru grupas, lai atbalstītu katru no trim scenārijiem pārskatam par partijas elementiem.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Iestatiet izsekošanas numuru grupu, kas ļauj darbiniekiem manuāli piešķirt partijas numuru

Lai ļautu manuāli piešķirt partijas numurus, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Manuāli** uz **Jā**.

    ![Manuālu partijas numuru izsekošanas numuru grupa](media/tracking-number-group-manual.png "Manuālu partijas numuru izsekošanas numuru grupa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir teksta lodziņš, kurā darbinieki var ievadīt jebkuru vērtību.

![Pārskata norises lapa ar lauku manuāliem partijas numuriem](media/job-card-device-batch-manual.png "Pārskata norises lapa ar lauku manuāliem partijas numuriem")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Iestatiet izsekošanas numuru grupu, kas nodrošina iepriekš definētu partijas numuru sarakstu

Lai nodrošinātu iepriekš definētu partijas numuru sarakstu, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana > Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Jā**.
1. Lietojiet lauku **Pēc daudzuma**, lai sadalītu partijas numurus pēc daudzuma, pamatojoties uz ievadīto vērtību. Piemēram, jums ir ražošanas pasūtījums desmit vienībām un lauks **Pēc daudzuma** ir iestatīts uz *2*. Šādā gadījumā, izveidojot ražošanas pasūtījumu, tam tiks piešķirti pieci partijas numuri.

    ![Iepriekš definēta partijas numuru izsekošanas numuru grupa](media/tracking-number-group-predefined.png "Iepriekš definēta partijas numuru izsekošanas numuru grupa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir nolaižams saraksts, kurā darbiniekiem jāievada iepriekš definētā vērtība.

![Pārskata norises lapa ar iepriekš definēto partijas numuru sarakstu](media/job-card-device-batch-predefined.png "Pārskata norises lapa ar iepriekš definēto partijas numuru sarakstu")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Iestatiet izsekošanas numuru grupu, kas automātiski piešķir partijas numurus

Ja partijas numuri jāpiešķir automātiski — bez darbinieka ievades — veiciet tālāk minētās darbības, lai iestatītu izsekošanas numuru grupu.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Nē**.
1. Iestatiet opciju **Manuāli** uz **Nē**.

    ![Fiksētu partijas numuru izsekošanas numuru grupa](media/tracking-number-group-fixed.png "Fiksētu partijas numuru izsekošanas numuru grupa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, rāda vērtību, bet darbinieki nevar to rediģēt.

![Pārskata norises lapa ar fiksētu partijas numuru](media/job-card-device-batch-fixed.png "Pārskata norises lapa ar fiksētu partijas numuru")

## <a name="report-serial-controlled-items-as-finished"></a>Reģistrēt sērijveidā kontrolētos elementus kā pabeigtus

Darba kartes ierīce atbalsta trīs scenārijus ziņošanai par sērijveida kontrolētiem elementiem. Šie scenāriji attiecas gan uz elementiem, kas ir iespējoti papildu noliktavas procesiem, gan uz elementiem, kas nav iespējoti papildu noliktavas procesiem.

- **Manuāli piešķirtie sērijas numuri** - darbinieki ievada pielāgotu sērijas numuru. Šis sērijas numurs var būt no ārēja avota, kas sistēmai nav zināms.
- **Iepriekš definētie sērijas numuri** - darbinieki atlasa sērijas numuru sērijas numuru sarakstā, ko sistēma automātiski izveido pirms ražošanas pasūtījuma nodošanas darba kartes ierīcei.
- **Fiksēti sērijas numurs** - darbinieki neievada vai neatlasa sērijas numuru. Tā vietā sistēma automātiski piešķir ražošanas pasūtījumam sērijas numuru, pirms tas tiek izlaists ražošanai.

### <a name="enable-the-feature-on-your-system"></a>Iespējot līdzekli sistēmā

Lai iespējotu jūsu darbu karšu ierīces akceptēt sērijas numuru, ziņojot par pabeigšanu, ir jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu tālāk norādītos līdzekļus (minētajā secībā).

1. Uzlabota lietotāja pieredze darba karšu ierīces norises pārskata dialogā
1. Iespējojiet, lai ievadītu partijas un sērijas numurus, vienlaikus ziņojot kā par pabeigtu no darba karšu ierīces (priekšskatījums)

### <a name="configure-products-that-require-serial-number-reporting"></a>Konfigurēt preces, kurām nepieciešams sērijas numura pārskats

Lai iespējotu preci, kas atbalsta jebkuru no pieejamajiem sērijveida kontrolētajiem scenārijiem, rīkojieties šādi:

Lai iespējotu katru scenāriju, izpildiet tālāk aprakstītās darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet konfigurējamo preci.
1. Kopsavilkuma cilnes **Pārvaldīt krājumu** laukā **Sērijas numuru grupa** atlasiet izsekošanas numuru grupu, kas iestatīta, lai atbalstītu jūsu scenāriju.

> [!NOTE]
> Pēc noklusējuma, ja sērijveida kontrolētajai precei nav piešķirta sērijas numuru grupa, darba kartes ierīce nodrošina manuālu sērijas numura ievadi reģistrācijas kā pabeigts laikā.

Šajās sadaļās aprakstīts, kā iestatīt izsekošanas numuru grupas, lai atbalstītu katru no trim scenārijiem pārskatam par sērijveida kontrolētiem elementiem.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Iestatiet izsekošanas numuru grupu, kas ļauj darbiniekiem manuāli piešķirt sērijas numuru

Lai ļautu manuāli piešķirt sērijas numurus, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Manuāli** uz **Jā**.

    ![Izsekošanas numuru grupu lapa, sērijas numuri](media/tracking-number-group-manual-serial.png "Izsekošanas numuru grupu lapa, sērijas numuri")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā sērijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Sērijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir teksta lodziņš, kurā darbinieki var ievadīt jebkuru vērtību sērijas numuram. Ievadot vērtību, tā tiek pievienota sērijas numuru sarakstam. Sarakstā darbinieki to var izdarīt sekojoši:

- Lai atzīmētu sērijas numuru kā norakstītu, atlasiet pogu **Brāķis** attiecīgajai rindai. Darbinieks tiks lūgts sniegt **Kļūdas iemeslu**.
- Lai dzēstu sērijas numuru, atlasiet pogu **Dzēst** attiecīgajai rindai.

![Pārskata norises lapa ar lauku manuāliem sērijas numuriem](media/job-card-device-serial-manual.png "Pārskata norises lapa ar lauku manuāliem sērijas numuriem")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Iestatiet izsekošanas numuru grupu, kas nodrošina iepriekš definētu sērijas numuru sarakstu

Lai nodrošinātu iepriekš definētu sērijas numuru sarakstu, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Jā**.
1. Lietojiet lauku **Pēc daudzuma**, lai sadalītu sērijas numurus pa vienam daudzumam.

    ![Iepriekš definēta sērijas numuru izsekošanas numuru grupa](media/tracking-number-group-predefined-sn.png "Iepriekš definēta sērijas numuru izsekošanas numuru grupa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā sērijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Sērijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir nolaižams saraksts, kurā darbiniekiem jāievada iepriekš definētā vērtība.

![Pārskata norises lapa ar iepriekš definēto sērijas numuru sarakstu](media/job-card-device-serial-predefined.png "Pārskata norises lapa ar iepriekš definēto sērijas numuru sarakstu")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Iestatiet izsekošanas numuru grupu, kas automātiski piešķir sērijas numurus

Ja sērijas numurs jāpiešķir automātiski — bez darbinieka ievades — veiciet tālāk minētās darbības, lai iestatītu izsekošanas numuru grupu.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.
1. Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Nē**.
1. Iestatiet opciju **Manuāli** uz **Nē**.

    ![Fiksētu sērijas numuru izsekošanas numuru grupa](media/tracking-number-group-fixed-sn.png "Fiksētu sērijas numuru izsekošanas numuru grupa")

1. Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā sērijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.

Izmantojot šo scenāriju, lauks **Sērijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, rāda vērtību, bet darbinieki nevar to rediģēt. Šis scenārijs ir būtisks tikai tad, kad tiek izveidots ražošanas pasūtījums vienam sērijveida kontrolētam krājuma daudzumam.

![Pārskata norises lapa ar fiksētu sērijas numuru](media/job-card-device-serial-fixed.png "Pārskata norises lapa ar fiksētiem sērijas numuriem")

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
