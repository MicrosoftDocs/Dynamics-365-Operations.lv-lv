---
title: Rēķinu apmaksas scenāriju iestatīšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt programmu Dynamics 365 Commerce, lai atbalstītu dažādus scenārijus saistībā ar rēķinu maksājumiem.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08d3cf48c0bea6f0e13dda49e53b314a6037860d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804557"
---
# <a name="set-up-pay-invoice-scenarios"></a>Rēķinu apmaksas scenāriju iestatīšana

[!include [banner](includes/banner.md)]

Rēķinu apmaksāšanas funkcionalitāte programmā Dynamics 365 Commerce ir paplašināta, lai atbalstītu tālāk minētos elementus.

- Vairāku pārdošanas pasūtījumu rēķinu apmaksa vienā POS transakcijā.
- Dažādu debitora rēķinu veidu, tostarp brīva teksta rēķinu, projekta rēķinu un kredīta notu, apmaksa.

Lai iespējotu šos scenārijus, funkcionalitātes profils veikaliem jākonfigurē, kā norādīts tālāk.

1. Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> POS iestatījumi \> POS profili \> Funkcionalitātes profili** un izvēlieties profilu, kas ir piesaistīts veikaliem, kuriem vēlaties veikt izmaiņas.
2. Cilnē **Funkcijas** pēc nepieciešamības konfigurējiet tālāk norādītos parametrus.

    - **Pārdošanas pasūtījuma rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus pārdošanas pasūtījuma rēķinus vienā POS transakcijā.
    - **Brīva teksta rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus brīva teksta rēķinus vienā POS transakcijā.
    - **Projekta rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus projekta rēķinus vienā POS transakcijā.
    - **Pārdošanas pasūtījuma kredīta nota** — atlasiet **Jā**, lai atļautu lietotājiem nosegt vairākas pārdošanas pasūtījumu kredīta notas ar atvērtiem rēķiniem vai apstrādāt atmaksu debitoram par atvērtu kredīta notu.

> [!NOTE]
> Daļēju summu maksājums vai segšana vēl netiek atbalstīta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]