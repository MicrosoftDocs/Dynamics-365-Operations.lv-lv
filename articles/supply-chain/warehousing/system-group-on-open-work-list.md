---
title: "Sistēmas grupēšana atvērtā darbu sarakstā"
description: "Šajā tēmā ir aprakstīts, kā filtrēt atvērto darbu sarakstu mobilajā ierīcē."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Sistēmas grupēšana atvērtā darbu sarakstā

[!include[banner](../includes/banner.md)]

Izmantojot sistēmas grupēšanas lauku, varat filtrēt atvērto darbu sarakstu, nerediģējot mobilās ierīces izvēlnes vienumu.
Tādā gadījumā sistēmas grupēšana darbojas darbu saraksta filtrēšanai vienā darba virsraksta laukā. Sistēmas grupēšanu nevar izmantot, lai filtrētu rindas līmeņa laukus.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Sistēmas grupēšanas atvērtā darbu sarakstā iestatīšana
Izmantojiet tālāk aprakstītās darbības, lai iestatītu sistēmas grupēšanu atvērtā darbu sarakstā.

-   No mobilās ierīces izvēlnes vienuma atlasiet **Režīms: netiešs** un **Aktivitātes kods: Parādīt atvērto darbu sarakstu**. Kļūst pieejamas tālāk minētās opcijas. Šīs opcijas ir nepieciešamas sistēmas grupēšanai atvērtajā darbu sarakstā. 

| Opcija        | Apraksts   | 
| ------------- | ------------- |
| Sistēmas grupēšanas atļaušana   | Iespējo sistēmas grupēšanu atlasītajam darbu saraksta izvēlnes vienumam.| 
| Sistēmas grupēšanas lauks   | Pieejams tikai tad, ja vienumam **Atļaut sistēmas darbu** ir iestatīta opcija **Jā**. Atlasiet lauku, kas nosaka, kā izdošanas darbs tiks grupēts darbiniekiem. Piemēram, ja atlasīsiet lauku **ShipmentId**, darbinieks skenēs sūtījuma ID, lai grupētu izdošanas darbu. Pēc tam viss ar sūtījumu saistītais darbs tiks piešķirts darbiniekam. Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai. Izmantojiet lauku **Sistēmas grupēšanas etiķete**, lai informētu darbiniekus, kas jāskenē. |
| Sistēmas grupēšanas etiķete   | Pieejams tikai tad, ja vienumam **Atļaut sistēmas darbu** ir iestatīta opcija **Jā**. Ievadiet informāciju darbiniekam par to, kas jāskenē, kad tiek grupēts izdošanas darbs. Piemēram, ja izmantojat lauku **ShipmentId**, lai grupētu izdošanas darbu pēc sūtījuma, varat šajā laukā ievadīt vērtību Sūtījuma ID. Lai izmantotu šo lauku, ir jāizveido izvēlnes vienums esoša sistēmas grupēta darba izmantošanai. Turklāt laikā **Sistēmas grupēšanas lauks** ir jāatlasa lauks, pēc kura grupēt.|

