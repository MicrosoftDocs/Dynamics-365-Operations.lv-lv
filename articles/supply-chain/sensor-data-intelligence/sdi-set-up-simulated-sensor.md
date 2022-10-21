---
title: Iestatīt simulētu sensoru testēšanas veikšanai
description: Šajā rakstā ir aprakstīts, kā iestatīt simulatoru, ko varat izmantot, lai pārbaudītu Sensora datu informāciju, neinstalējot jebkādus fiziskos sensorus.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f12d6e1d417a260477b1eb4e027b850d1862f51f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689809"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Iestatīt simulētu sensoru testēšanas veikšanai

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Ja vēlaties pārbaudīt sensora datu informāciju, neinstalējot jebkādus fiziskus sensorus, varat izmantot Simulatora PI Azure IoT tiešsaistes simulatora *pakalpojumu,* lai uzcenotu sensora signālus un sūtītu tos uz interneta darbību internetam (IoT)Microsoft Azure. Papildinformāciju par simulatoru skatiet sadaļā [Abonementa Krājuma Pi tiešsaistes simulatora savienošana ar Azure IoT hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Video instrukcijas

Šajā video parādīts, kā iestatīt simulētu sensoru testēšanai. Pārējās šī raksta sadaļas sniedz tās pašas instrukcijas uz tekstu balstītā formātā.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Izveidot ierīci azure Iot hub

Vispirms jāiestata ierīce, lai autentificētu sensora signālus Azure Iot hub.

1. Azure atveriet resursu sarakstu resursu grupai, kuru izveidojāt lietošanai ar sensora datu informāciju. (Plašāku informāciju skatiet [Izvietojiet IoT risinājumu Azure](sdi-deploy-iot-solution-on-azure.md).)
1. Resursu sarakstā atrodiet ierakstu, kur lauks Tips **ir** iestatīts uz *IoT hub*. Kolonnā Nosaukums **atlasiet** nosaukumu, lai atvērtu detalizētas informācijas lapu resursam.
1. Kreisajā navigācijas rūtī atlasiet **Ierīces**.
1. **Ierīču lapā** atlasiet Pievienot **ierīci**.
1. **Lapā Izveidot ierīci iestatiet** šādus laukus:

    - **Ierīces ID** – ievadiet jaunās ierīces nosaukumu (piemēram, *Mans-IoT-Device*).
    - **Autentifikācijas tips** - izvēlieties simetriskas *atslēgas*.
    - **Automātiski ģenerēt atslēgas** - atzīmējiet šo izvēles rūtiņu.
    - **Savienojiet šo ierīci ar IoT pārkraušanas punkts** — atlasiet *Iespējot*.

1. Atlasiet **Saglabāt,** lai atgrieztos **ierīču** lapā.
1. Atrast jauno ierīci sarakstā. Kolonnā Ierīces **ID** atlasiet nosaukumu, lai atvērtu ierīces detalizētas informācijas lapu. Ja sarakstā nav redzama jaunā ierīce, atsvaidziniet lapu.
1. Kopējiet **primārā savienojuma virknes** vērtību (piemēram, atlasot pogu **Kopēt uz starpliktuvi**). Šī vērtība būs nepieciešama vēlāk, kad uzstādīsiet Norādāmo IoT simulatoru emulējošos slāņus. Tāpēc apsveriet iespēju to ielīmēt teksta failā tagad.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Pievienojiet Azure savienojuma virkni Paralēlā Pi IoT simulatoram

Izpildiet šīs darbības, lai Pievienotu savienojuma virkni no ierīces Azure IoT pārkraušanas centrā skriptam Pakalpojuma Neprakta pakalpojumā.

1. Atveriet Pēcteču [Pi IoT simulatoru](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Kodu redaktora rūtī atrodiet rindu, kas satur sekojošo komandu.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Nomainiet palīdzības tekstu, ieskaitot iekavas, ar **primārā savienojuma virknes** vērtību, ko pārkopējat iepriekšējā sadaļā. Rezultātiem vajadzētu izskatīties līdzīgi kā tālāk sniegtais piemērs.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Pievienojiet sensora ID un vērtības lietderīgā slodzeiĀdē, Kas Irkā PI IoT simulatorā

Tagad jums ir jāiestata Nosūtīšanaplio Pi IoT simulators ar simulētiem sensoriem un vērtībām, kuras tie nosūtīs kā lietderīgo slodzi.

- Kodu redaktorā Norādāmo Pi IoT simulatorā `getMessage` atrodiet funkciju un rediģējiet to, lai tā atbilstu šādam kodam. (Sensori ir iestatīti rindās `cb()` .)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Sensoru identi štatu identi štata ID, kas ir definēti Kodu redaktorā, kas paredzēts Dcplio Pi IoT simulatoram, jābūt identiskiem ar sensora IDENTi tā, kā vēlāk norādīsiet piegādes ķēdes pārvaldības scenārijiem. Iepriekšējā piemēra kodā tiek lietoti human-readable sensora D. Tomēr faktiskā scenārijā sensora ID būs globāli unikālas identifikatora (GUID) vērtības, ko nodrošina sensora ražotājs. Šajā piemērā izmantotie cilvēklasāmie sensora D tiek izmantoti arī produktu kvalitātes scenārija, līdzekļu uzturēšanas scenārija, [...](sdi-scenario-product-quality.md)[ražošanas aizkaves scenārija un mašīnas statusa scenārija piemēros.](sdi-scenario-asset-maintenance.md)[...](sdi-scenario-production-delays.md)[...](sdi-scenario-equipment-downtime.md) Tāpēc izmantojiet šo kodu, ja darbosies šajos scenārijos.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Rediģēt intervālu sensora signālu sūtīšanai

Tagad ir jāiestata intervāls, kurā Qtplio Pi IoT simulatoram jāsūta emulētie sensora signāļi.

1. Kodu redaktorā Norādāmā Pi IoT simulatorā atrodiet sekojošo funkciju piesaukšanu.

    `setInterval(sendMessage, 2000);`

2. Pēc noklusējuma Nemitēta Pi IoT simulators sūta sensora signālu ik pēc 2000 milisekundēm (divas sekundes). Vērtību var pielāgot nepieciešamai vērtībai.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Palaidiet Pēcteču Pi IoT simulatoru

- Atlasiet Izpildīt **,** lai sāktu simulatoru un sāktu sūtīt simulētus sensora datus.
