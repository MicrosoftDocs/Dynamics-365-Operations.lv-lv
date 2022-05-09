---
title: IoT Informācijas sākumlapa
description: Šī tēma sniedz saites uz informāciju par IoT Informāciju.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c587f4e6a1dd58a7b8c238fc5afb16774828b2a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644391"
---
# <a name="iot-intelligence-home-page"></a>IoT Informācijas sākumlapa

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Pašlaik šī funkcija ir pieejama tikai šādās valstīs/reģionos:
>
> - ASV (Amerikas Savienotās Valstis)
> - ES (Eiropas Savienība)
> - AU (Austrālija)
> - CA (Kanāda)
> - UK (Apvienotā Karaliste)

Iot Informācija ir Microsoft Dynamics 365 Supply Chain Management pievienojumprogramma. Tas integrē lietiskā interneta (IoT) signālus ar datiem Supply Chain Management, lai izveidotu darbību saprotamus priekšstatus.

IoT Informācija atbalsta šādus scenārijus:

- **Ražošanas aizkave** – šis scenārijs salīdzina faktisko cikla laiku ar plānoto cikla laiku. Supply Chain Management jūs informē, kad ražošana nav ieplānota, tādējādi varat uzlabot operāciju efektivitāti un izvairīties no pasūtījumu kavēšanās.
- **Aprīkojuma dīkstāves laiks** - šis scenārijs salīdzina mērīto darbspēju ar lietotāja definētajiem parametriem. Supply Chain Management paziņo, kad tiek pārsniegts nepieejamības slieksnis, lai varētu veikt darbības, piemēram, ražošanas darba pasūtījuma pārplānošanu vai uzturēšanas darba pasūtījuma izveidi.
- **Produkta kvalitāte** – šis scenārijs salīdzina sensora lasījumus, piemēram, augstākās un temperatūras ar lietotāja definētiem kvalitātes rādītājiem. Supply Chain Management paziņo, kad rodas novirze, tādējādi jūs varat saglabāt kvalitātes standartus un minimizēt atkritumus.

Šajā ilustrācijā parādīta Azure Iot Hub, Iot Informācija un Supply Chain Management mijiedarbība.

![Iot Hub, Iot Informācija un Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Izsekošana un uzturēšana

- [Pārraudzīt scenārijus programmā Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Scenārija atspējošana](iot-scenario-setup.md#disable-a-scenario)
- [IoT Intelligence scenārija darbības modificēšana](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Simulācijas opcijas](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]