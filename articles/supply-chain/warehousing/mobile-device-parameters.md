---
title: Globālie mobilās ierīces parametri
description: Šajā tēmā skaidrots, kā iestatīt mobilās ierīces lietotāja iestatījumus Noliktavas pārvaldības parametru lapā.
author: HuberIvan
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-huberivan
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 03c10232d55c99c73e625170797f89f6c77e812b
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505585"
---
# <a name="global-mobile-device-parameters"></a>Globālie mobilās ierīces parametri

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt globālos noliktavu pārvaldības parametrus, kuri ietekmē to, kā sistēma mijiedarbojas ar mobilajām ierīcēm.

Papildinformāciju par to, kā iestatīt noliktavu darbiniekus, skatiet sadaļā [Noliktavas darbinieka pārvaldība](manage-warehouse-workers.md). Lai iegūtu detalizētu informāciju, kas saistīta ar numura zīmes apstrādi mobilajās ierīcēs, skatiet [Numura zīmes saņemšana ar Warehouse Management mobile programmas starpniecību](warehousing-mobile-device-app-license-plate-receiving.md). Papildinformāciju par ciklu skaitīšanas procesiem skatiet rakstā [Ciklu skaitīšana](cycle-counting.md) un [Ciklu skaitīšanas scenāriju piemēri](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Atveriet Noliktavu pārvaldības parametru lapu

Lai atvērtu **Noliktavu pārvaldības parametru** lapu, dodieties uz **Noliktavu pārvaldība\> Iestatīšana\> Noliktavu pārvaldības parametri**. Pēc tam varat iestatīt laukus, kuri ir saistīti ar mobilo ierīču darbu, kā aprakstīts nākamajā šīs tēmas sadaļā.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Mobilās ierīces kopsavilkuma cilne cilnē Vispārīgi

Globālie mobilās ierīces iestatījumi ir atrodami Lapas **Noliktavu pārvaldības parametri** cilnes **Vispārīgi** kopsavilkuma cilnē **Mobilā ierīce**. Pieejami tālāk norādītie lauki.

| Lauks | Apraksts |
|---|---|
| Mobilās ierīces piezīmes tips | Atlasiet to informācijas tipu, kas tiek rādīts darbiniekiem pārdošanas pasūtījuma izdošanas laikā. |
| Skenēšanas daudzuma ierobežojums | Ievadiet maksimālo krājuma vienību daudzumu, kuru darbinieks var katras sesijas laikā skenēt ar mobilās ierīces izvēlnes elementu, kura **Darba izveides procesa** vērtība ir *Pielāgošana*. Šis lauks neietekmē skenējumus, kuri tiek veikti ar jebkuru citu izvēlnes elementu. |
| Izmantot mobilās ierīces sesijas reģistrāciju | Iestatiet šo opciju uz *Jā*, lai uzturētu darbinieku pieteikšanās vēstures reģistru. Lai skatītu reģistru, dodieties uz **Darba lietotāju sesijas\> Vaicājumi un atskaites \> Mobilo ierīču žurnāli \>Darba lietotāju sesijas**. |
| Glabāto kļūdu skaits | Ievadiet maksimālo kļūmju ierakstu skaitu, kuras sistēmai vajadzētu glabāt. Lai skatītu kļūdu reģistru, dodieties uz **Darba lietotāju sesijas\> Vaicājumi un atskaites \> Mobilo ierīču žurnāli \>Darba lietotāju sesijas**. |
| Noklusējuma noliktavas pārsūtīšanas žurnāls | Atlasiet žurnālu, kas tiek izmantots, kad darbinieki lieto mobilo ierīci, lai pārvietotu preces no vienas noliktavas uz citu. |
| Veicot ārēju pārskatīšanu, atļaut pirkšanas pasūtījuma rindas reģistrāciju | Iestatiet šo opciju uz *Jā*, ja darbiniekiem vajadzētu varēt lietot mobilo ierīci, lai reģistrētu pasūtījuma rindas pirkuma pasūtījumiem ar **Apstiprinājuma statusa** vērtību *Notiek iekšējā pārskatīšana*. Iestatiet šo opciju uz *Nē*, lai neļautu darbiniekiem reģistrēt to pirkuma pasūtījumu rindas, kuriem notiek ārējā pārskatīšana. |
| Iespējot RSAT atbalstu | Šis lauks iespējo Warehouse Management mobilās programmas uzdevumu pārbaudītāju, kas reģistrē un validē katru programmas veikto darbību. Tā kā šis process var ievērojami palēnināt sistēmas veiktspēju, jums vajadzētu pārbaudītāju iespējot tikai testēšanas laikā. Jums to nevajadzētu iespējot ražošanas vidē. |
