---
title: IoT informācijas pārraudzība un pārvaldība
description: Šajā tēmā ir paskaidrots, kā pārraudzīt un pārvaldīt IoT informāciju.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7aec17a6355caa133a671a242056e77b7f6bb461
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509561"
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

+ [IoT DevKit AZ3166 savienošana ar Azure IoT centrmezglu](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi tiešsaistes simulatora savienošana ar Azure IoT centrmezglu (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
