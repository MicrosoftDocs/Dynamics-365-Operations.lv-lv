---
title: Dokumenti, kas gaida uzskaiti
description: Šajā rakstā ir aprakstīts, kā lietot funkcionalitāti lapā “Dokumenti, kas gaida uzskaiti”.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: e915c248abd1c842f8f01490a49db9b824644a29
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9424372"
---
# <a name="documents-pending-accounting"></a>Dokumenti, kas gaida uzskaiti

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā rakstā ir aprakstīts, kā lietot funkcionalitāti lapā **Dokumenti, kas gaida uzskaiti**.

Risinājumā Microsoft Dynamics 365 Finance 10.0.30 ir pieejams līdzeklis **Uzlabota pirmdokumentu uzskaites struktūras veiktspēja**. Šis līdzeklis uzlabo pirmdokumenta iespējotu dokumentu grāmatošanas procesu, sākot ar brīvā teksta rēķinu grāmatošanas procesu.

Ja šis līdzeklis ir iespējots, apakšgrāmatas dokumenta grāmatošana tiek veikta atsevišķi no uzskaites ģenerēšanas vai *reģistrācijas ieraksta žurnālā* procesa, kas izveido pilnu uzskaites detalizēto informāciju, kas tiek pārsūtīta uz virsgrāmatu. Piemēram, brīvā teksta rēķina grāmatošanas procesā debitora rēķins modulī **Debitoru parādi** tiek ierakstīts pirms pilnīgas uzskaites ģenerēšanas. Šis uzlabotās veiktspējas līdzeklis sniedz iespēju ātrāk ierakstīt debitoru rēķinus, kamēr uzskaites ģenerēšana kavējas.

Lapā **Dokumenti, kas gaida uzskaiti** ir pieejamas tālāk norādītās pogas.

- **Ģenerēt uzskaiti** — iesniegt dokumentu, kas pašlaik gaida konta ģenerēšanu reģistrācijas ierakstam žurnālā.
- **Skatīt sadales** — skatiet sarakstā atlasītā dokumenta uzskaites sadales.
- **Skatīt kļūdu žurnālu** — skatiet jebkuru kļūdas ziņojumu detaļas, kas pastāv dokumentam, kurā uzskaites stāvoklis norāda kļūdas. Tās pašas kļūdas ziņojuma detaļas varat skatīt, dokumenta rindā atlasot saiti **Kļūdu žurnāls**.

Uzskaites ģenerēšanu veic procesa automatizācijas fona process **Uzskaites struktūras procesors**. Papildinformāciju par visu procesu automatizāciju iestatīšanu un konfigurēšanu skatiet sadaļā [Procesu automatizācija](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
