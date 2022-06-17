---
title: Rēķinu apmaksas scenāriju iestatīšana
description: Šajā rakstā ir aprakstīts, kā konfigurēt programmu Dynamics 365 Commerce, lai atbalstītu dažādus scenārijus saistībā ar rēķinu maksājumiem.
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
ms.openlocfilehash: 78af54fec771e5012aca095d07fd772988a56029
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885379"
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