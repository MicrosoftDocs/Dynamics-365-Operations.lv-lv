---
title: Svītrkodu tipu uzturēšana
description: Šajā procedūrā parādīts, kā iestatīt jaunu svītrkoda definīciju, ko pēc tam var izmantot kā daļu no izdošanas saraksta pārskata.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571117"
---
# <a name="maintain-bar-code-types"></a>Svītrkodu tipu uzturēšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā iestatīt jaunu svītrkoda definīciju, ko pēc tam var izmantot kā daļu no izdošanas saraksta pārskata. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Ja izmantojat USMF varat izmantot piemēra vērtības, kas parādītas. Šos uzdevumus parasti veic noliktavas pārvaldnieks.

1. Dodieties uz sadaļu **Svītrkodi**.
1. Atlasiet **Jauns**.
1. Laukā **Svītrkodu iestatījumi** ierakstiet kādu vērtību.
1. Laukā **Apraksts** ierakstiet kādu vērtību.
1. Atlasiet opciju laukā **Svītrkoda tips**.
    * Ja izmantojat USMF, varat atlasīt "Kods 39".
1. Laukā **Maskas ID** norādiet svītrkoda maskas ID. Svītrkoda maskas tiek izmantotas, lai izveidotu svītrkodus un ātri identificētu svītrkodus, kuri tiek skenēti pārdošanas punkta (POS) sistēmā. Papildinformāciju skatiet sadaļā [Svītrkoda masku iestatīšana](../../../commerce/set-up-bar-code-masks.md).
1. Ievadiet skaitli laukā **Lielums**.
1. Ievadiet skaitli laukā **Maksimālais garums**.
1. Atlasiet **Saglabāt**.
1. Aizvērt lapu.
1. Dodieties uz sadaļu **Krājumu un noliktavas vadības parametri**.
1. Laukā **Svītrkodu iestatījumi** ievadiet vai atlasiet vērtību.
    * Atlasiet svītrkoda iestatījumu, ko izveidojāt iepriekš, taču ņemiet vērā, ka svītrkoda formātam jāatbilst unikālā identifikatora formātam procesā izmantojamajam ieraksta tipam. Piemēram, izdošanas maršrutiem svītrkoda formātam ir jāatbilst izdošanas maršruta atsauces formātam, kas parasti ir numuru sērija.  
1. Atlasiet **Saglabāt**.
1. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
