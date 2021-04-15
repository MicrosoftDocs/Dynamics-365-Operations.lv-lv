---
title: IoT informācijas pārraudzība un pārvaldība
description: Šajā tēmā ir paskaidrots, kā pārraudzīt un pārvaldīt IoT informāciju.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 94665b3646456b689a8e65e94b098e86e467d5e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813079"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT informācijas pārraudzība un pārvaldība

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā pārraudzīt un pārvaldīt IoT informāciju.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Pārraudzīt scenārijus programmā Microsoft Dynamics 365 Supply Chain Management

IoT informācijas apstrādi var pārraudzīt no vairākām vietām:

+ **Moduļi \> Ražošanas kontrole \> Pieprasījumi un pārskati \> IoT informācija \> Paziņojumi** – skatīt neatrisināto paziņojumu sarakstu.
+ **Moduļi \> Ražošanas kontrole \> Pieprasījumi un pārskati \> IoT informācija \> Slēgti paziņojumi** – skatīt to paziņojumu sarakstu, kas ir atrisināti vai noraidīti.
+ **Moduļi \> Ražošanas kontrole \> Pieprasījumi un pārskati \> IoT informācija \> Metrikas atslēgas** – skatīt **Resursa statusa** laika sēriju diagrammu metrikas atslēgas.
+ **Moduļi \> Ražošanas kontrole \> Ražošanas izpilde \> Resursa statuss** – izsekot konkrētu metriku, izmantojot dialoglodziņu **Konfigurēt**. Ja scenārijs nosaka izņēmumu, paziņojumā tiek parādīta informācija par izņēmumu.
+ **Darbvietas \> Ražošanas stāva pārvaldība \> Paziņojumi** – skatīt neatrisināto paziņojumu sarakstu.

## <a name="modify-a-running-iot-intelligence-scenario"></a>IoT informācijas scenārija darbības modificēšana

Kad scenārijs darbojas, var veikt šādas izmaiņas:

+ Pievienot jaunas sensora shēmas definīcijas.
+ Atlasīt jaunas signāla datu vērtības.
+ Atcelt esošo signāla datu vērtību atlasi.
+ Pievienot un kartēt jaunas signāla datu vērtības.
+ Atjaunināt sliekšņa vērtības.

Kad scenārijs darbojas, šādas izmaiņas ir aizliegtas:

+ Dzēst vai modificēt shēmas definīcijas, kuras pašlaik izmanto iespējots scenārijs.
+ Mainīt iespējota scenārija atlasītos shēmu ceļus.

## <a name="simulation-options"></a>Simulācijas opcijas

Var simulēt rūpnīcas mašīnas signālus. Papildinformāciju skatiet šādās tēmās:

+ [IoT DevKit AZ3166 savienošana ar Azure IoT centrmezglu](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi tiešsaistes simulatora savienošana ar Azure IoT centrmezglu (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Ierīces simulācijas risinājuma paātrinātāja pārskats](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]