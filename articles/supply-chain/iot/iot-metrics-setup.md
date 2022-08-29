---
title: Metrikas iestatīšana IoT Informācijai
description: Šajā rakstā skaidrots, kā iestatīt IoT Intelligence rādītājus.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fddfee837761a4f23b42257424582a3c76c3d493
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228333"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>Metrikas iestatīšana IoT Informācijai

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

## <a name="configure-metrics"></a>Konfigurēt metriku

Ja vēlaties skatīt ziņojumu laika sērijas diagrammas programmā Microsoft Dynamics 365 Supply Chain Management, ir jāiestata metrika, izpildot šādas darbības.

1. Kopēt Redis kešatmiņas savienojuma virkni:

    1. Dodieties uz Redis kešatmiņu Azure portālā.
    2. Dodieties uz **Iestatījumi** \> **Piekļuves atslēgas**.
    3. Kopējiet vērtību **Primārā savienojuma virkne** laukā.

2. Risinājumā Supply Chain Management dodieties uz **Ražošanas kontrole \> Iestatījumi \> IoT Informācija \> Scenārija parametri**.
3. Lapas **Scenārija parametri** cilnē **Laiku sērija**, laukā **Redis metriska veikala savienojuma virkne**, ielīmējiet savienojuma virkni, kas tika nokopēta agrāk. Izmantojot šo darbību, Supply Chain Management varat vizualizēt metriku no Azure IoT Hub. Ielīmējot vērtību laukā, tā tiek parādīta kā **\*\*\*\*\*\***.

    > [!NOTE]
    > Atjauninot Redis kešatmiņas savienojuma virkni, ir jāatjaunina arī šis lauks.

4. Dodieties uz **Ražošanas kontrole \> Vaicājumi un pārskati \> IoT Informācija \> Metrikas atslēgas**.
5. Lapā **Metrikas atslēgas** atlasiet **Atjaunināt**.
6. Dialoglodziņā **Atjaunināt metrikas atslēgas** ievērojiet, ka laukā ir atlasīta opcija **Palaist fonā**. Atlasiet **Labi**.

Visas metrikas atslēgas Redis kešatmiņā tiek izgūtas un pievienotas **Metrikas atslēgu** sarakstam. Metrikas vērtības neparādīsies, kamēr nebūs [iespējoti scenāriji](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Konfigurēt Resursu statusa laika sēriju

Lai konfigurētu **Resursu statusa** laika sēriju, sekojiet šiem soļiem.

1. Supply Chain Management dodieties uz **Ražošanas kontrole \> Ražošanas izpilde \> Resursa statuss**.
2. Lapā **Resursu statuss** atlasiet **Konfigurēt**.
2. Dialoglodziņa **Konfigurēt** sarakstā **Resursi** atlasiet krājumu pārraudzīšanai.
3. Izvēlieties pogu **Rediģēt** **1. laika sērijai**.
4. Dialoglodziņā **Atlasīt laika sērijas** atlasiet metriku režģī. (Varat izmantot arī **Atjaunināt metrikas atslēgu** saiti, lai atjauninātu metrikas atslēgas no šī dialoglodziņa.)
5. Atlasiet **Labi**, lai atgrieztos dialoglodziņā **Konfigurēt**.
6. Ievadiet parādāmo nosaukumu.
7. Laukā **Rādīt datus no** atlasiet laika posmu.
8. Atlasiet **Labi**.

Tiek parādīta diagramma.

## <a name="delete-a-metric-key"></a>Metrikas atslēgas dzēšana

1. Supply Chain Management dodieties uz **Ražošanas kontrole \> Vaicājumi un pārskati \> IoT Informācija \> Metrikas atslēgas**.
2. Lapā **Metrikas atslēgas** atlasiet metrikas atslēgu, ko dzēst.
3. Atlasiet **Dzēst**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]