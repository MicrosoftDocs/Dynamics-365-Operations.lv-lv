---
title: "Rēķinu apmaksas scenāriju iestatīšana"
description: "Šajā tēmā ir aprakstīts, kā konfigurēt Dynamics 365 for Retail, lai atbalstītu dažādus scenārijus, kas attiecas uz rēķinu maksājumiem."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 53c4b9a9c9dac1add7021d909b2c8900d11e5c0c
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-pay-invoice-scenarios"></a>Rēķinu apmaksas scenāriju iestatīšana

[!include [banner](includes/banner.md)]

Funkcionalitāte Apmaksāt rēķinu programmā Dynamics 365 for Retail ir paplašināta, lai atbalstītu tālāk minētos elementus.
- Vairāku pārdošanas pasūtījumu rēķinu apmaksa vienā POS transakcijā.
- Dažādu debitora rēķinu veidu, tostarp brīva teksta rēķinu, projekta rēķinu un kredīta notu, apmaksa.

Lai iespējotu šos scenārijus, funkcionalitātes profils veikaliem jākonfigurē, kā norādīts tālāk.  

1. Dodieties uz **Mazumtirdzniecība > Kanāla iestatīšana > POS iestatījumi > POS profili > Funkcionalitātes profili** un izvēlieties profilu, kas ir piesaistīts veikaliem, kuriem vēlaties veikt izmaiņas.

1. Cilnē **Funkcijas** pēc nepieciešamības konfigurējiet šādus parametrus.

    - **Pārdošanas pasūtījuma rēķins** — atlasiet **Jā**, lai ļautu lietotājiem apmaksāt vienu vai vairākus pārdošanas pasūtījuma rēķinus vienā POS transakcijā.

    - **Brīva teksta rēķins** — atlasiet **Jā**, lai ļautu lietotājiem apmaksāt vienu vai vairākus brīva teksta rēķinus vienā POS transakcijā.

    - **Projekta rēķins** — atlasiet **Jā**, lai ļautu lietotājiem apmaksāt vienu vai vairākus projekta rēķinus vienā POS transakcijā.

    - **Pārdošanas pasūtījuma kredīta nota** — atlasiet **Jā**, lai ļautu lietotājiem nosegt vairākas pārdošanas pasūtījumu kredīta notas ar atvērtiem rēķiniem vai apstrādāt atmaksu debitoram par atvērtu kredīta notu.

> [!NOTE]
> Daļēju summu maksājums vai segšana vēl netiek atbalstīta.

