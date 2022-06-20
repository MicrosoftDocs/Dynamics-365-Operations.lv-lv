---
title: Sistēmas grupēšana atvērtā darbu sarakstā
description: Šajā rakstā ir aprakstīts, kā filtrēt atvērto darbu sarakstu mobilajā ierīcē.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42e5862392cff57886c36bcbe138e13a8ce7ef23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849102"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]