---
title: IoT informācijas pārraudzība un pārvaldība
description: Šajā rakstā skaidrots, kā pārraudzīt un pārvaldīt Iot Intelligence.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f1804e8b9cfa407f6549dc146df17338c4d51572
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228865"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT informācijas pārraudzība un pārvaldība

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Šajā rakstā skaidrots, kā pārraudzīt un pārvaldīt Iot Intelligence.

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

Var simulēt rūpnīcas mašīnas signālus. Papildinformāciju skatiet šajos rakstos:

+ [IoT DevKit AZ3166 savienošana ar Azure IoT centrmezglu](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi tiešsaistes simulatora savienošana ar Azure IoT centrmezglu (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
