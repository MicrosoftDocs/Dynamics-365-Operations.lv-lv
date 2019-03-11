---
title: Rēķinu apmaksas scenāriju iestatīšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt programmu Dynamics 365 for Retail, lai atbalstītu dažādus scenārijus saistībā ar rēķinu maksājumiem.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "302587"
---
# <a name="set-up-pay-invoice-scenarios"></a>Rēķinu apmaksas scenāriju iestatīšana

[!include [banner](includes/banner.md)]

Rēķinu apmaksāšanas funkcionalitāte programmā Dynamics 365 for Retail ir paplašināta, lai atbalstītu tālāk minētos elementus.

- Vairāku pārdošanas pasūtījumu rēķinu apmaksa vienā POS transakcijā.
- Dažādu debitora rēķinu veidu, tostarp brīva teksta rēķinu, projekta rēķinu un kredīta notu, apmaksa.

Lai iespējotu šos scenārijus, funkcionalitātes profils veikaliem jākonfigurē, kā norādīts tālāk.

1. Dodieties uz **Mazumtirdzniecība \> Kanāla iestatīšana \> POS iestatījumi \> POS profili \> Funkcionalitātes profili** un izvēlieties profilu, kas ir piesaistīts veikaliem, kuriem vēlaties veikt izmaiņas.
2. Cilnē **Funkcijas** pēc nepieciešamības konfigurējiet tālāk norādītos parametrus.

    - **Pārdošanas pasūtījuma rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus pārdošanas pasūtījuma rēķinus vienā POS transakcijā.
    - **Brīva teksta rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus brīva teksta rēķinus vienā POS transakcijā.
    - **Projekta rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus projekta rēķinus vienā POS transakcijā.
    - **Pārdošanas pasūtījuma kredīta nota** — atlasiet **Jā**, lai atļautu lietotājiem nosegt vairākas pārdošanas pasūtījumu kredīta notas ar atvērtiem rēķiniem vai apstrādāt atmaksu debitoram par atvērtu kredīta notu.

> [!NOTE]
> Daļēju summu maksājums vai segšana vēl netiek atbalstīta.
