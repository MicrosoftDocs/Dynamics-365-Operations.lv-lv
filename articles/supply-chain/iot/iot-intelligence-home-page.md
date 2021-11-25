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
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782685"
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

+ **Ražošanas aizkave** – šis scenārijs salīdzina faktisko cikla laiku ar plānoto cikla laiku. Supply Chain Management jūs informē, kad ražošana nav ieplānota, tādējādi varat uzlabot operāciju efektivitāti un izvairīties no pasūtījumu kavēšanās.
+ **Aprīkojuma dīkstāves laiks** - šis scenārijs salīdzina mērīto darbspēju ar lietotāja definētajiem parametriem. Supply Chain Management paziņo, kad tiek pārsniegts nepieejamības slieksnis, lai varētu veikt darbības, piemēram, ražošanas darba pasūtījuma pārplānošanu vai uzturēšanas darba pasūtījuma izveidi.
+ **Produkta kvalitāte** – šis scenārijs salīdzina sensora lasījumus, piemēram, augstākās un temperatūras ar lietotāja definētiem kvalitātes rādītājiem. Supply Chain Management paziņo, kad rodas novirze, tādējādi jūs varat saglabāt kvalitātes standartus un minimizēt atkritumus.

Šajā ilustrācijā parādīta Azure Iot Hub, Iot Informācija un Supply Chain Management mijiedarbība.

![Iot Hub, Iot Informācija un Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Iestatīšana

Varat iestatīt un konfigurēt Lietiskā interneta informāciju, nerakstot nekādus kodus. Šeit ir pamata soļi.

1. [Iestatīt Azure resursus](iot-azure-setup.md) - izveidojiet IoT pārkraušanas punktu, Redis kešatmiņu un atslēgas kešatmiņu, kam var piekļūt no Supply Chain Management.
2. [Ziņojumu shēmas formāti IoT hub](iot-schema-format.md) - konfigurējiet ierīces, lai sūtītu ziņojumus uz Iot Hub, un definējiet JavaScript Object Notation (JSON) ziņojuma formātu.
3. Līdzekļu pārvaldībā iespējojiet IoT Informācijas funkcionalitātes karodziņu. 
4. [Instalējiet Iot Informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) - instalējiet pievienojumprogrammu LCS un konfigurējiet Azure slepeno informāciju.
5. [Iestatīt rādījumus](iot-metrics-setup.md) – iestatiet rādījumus Supply Chain Management.
6. [Scenāriju iestatīšana](iot-scenario-setup.md) – iestatīt scenārijus Supply Chain Management.

## <a name="tracking-and-maintenance"></a>Izsekošana un uzturēšana

+ [Pārraudzīt scenārijus programmā Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Scenārija atspējošana](iot-scenario-setup.md#disable-a-scenario)
+ [Pievienojumprogrammas atinstalēšana](iot-lcs-setup.md#uninstall-addin)
+ [IoT Intelligence scenārija darbības modificēšana](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Simulācijas opcijas](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]