---
title: Sistēmas grupēšana atvērtā darbu sarakstā
description: Šajā tēmā ir aprakstīts, kā filtrēt atvērto darbu sarakstu mobilajā ierīcē.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 826920980bdd2d30337c92553bd0367b119f676c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977342"
---
# <a name="system-grouping-on-an-open-work-list"></a>Sistēmas grupēšana atvērtā darbu sarakstā

[!include [banner](../includes/banner.md)]

Izmantojot sistēmas grupēšanas lauku, varat filtrēt atvērto darbu sarakstu, nerediģējot mobilās ierīces izvēlnes vienumu.
Tādā gadījumā sistēmas grupēšana darbojas darbu saraksta filtrēšanai vienā darba virsraksta laukā. Sistēmas grupēšanu nevar izmantot, lai filtrētu rindas līmeņa laukus.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Sistēmas grupēšanas atvērtā darbu sarakstā iestatīšana
Izmantojiet tālāk aprakstītās darbības, lai iestatītu sistēmas grupēšanu atvērtā darbu sarakstā.

-   No mobilās ierīces izvēlnes vienuma atlasiet **Režīms: netiešs** un **Aktivitātes kods: Parādīt atvērto darbu sarakstu**. Kļūst pieejamas tālāk minētās opcijas. Šīs opcijas ir nepieciešamas sistēmas grupēšanai atvērtajā darbu sarakstā. 

|        Opcija         |                                                                                                                                                                                                                                                                         Apraksts                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sistēmas grupēšanas atļaušana |                                                                                                                                                                                                                                                 Iespējo sistēmas grupēšanu atlasītajam darbu saraksta izvēlnes vienumam.                                                                                                                                                                                                                                                  |
| Sistēmas grupēšanas lauks | Pieejams tikai tad, ja vienumam <strong>Atļaut sistēmas darbu</strong> ir iestatīta opcija <strong>Jā</strong>. Atlasiet lauku, kas nosaka, kā izdošanas darbs tiks grupēts darbiniekiem. Piemēram, ja atlasīsiet lauku <strong>ShipmentId</strong>, darbinieks skenēs sūtījuma ID, lai grupētu izdošanas darbu. Pēc tam viss ar sūtījumu saistītais darbs tiks piešķirts darbiniekam. Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai. Izmantojiet lauku <strong>Sistēmas grupēšanas etiķete</strong>, lai informētu darbiniekus, kas jāskenē. |
| Sistēmas grupēšanas etiķete |                       Pieejams tikai tad, ja vienumam <strong>Atļaut sistēmas darbu</strong> ir iestatīta opcija <strong>Jā</strong>. Ievadiet informāciju darbiniekam par to, kas jāskenē, kad tiek grupēts izdošanas darbs. Piemēram, ja izmantojat lauku <strong>ShipmentId</strong>, lai grupētu izdošanas darbu pēc sūtījuma, varat šajā laukā ievadīt vērtību Sūtījuma ID. Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai. Turklāt laikā <strong>Sistēmas grupēšanas lauks</strong> ir jāatlasa lauks, pēc kura grupēt.                       |

