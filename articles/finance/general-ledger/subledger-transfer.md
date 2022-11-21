---
title: Pārsūtīt apakšgrāmatu uz Virsgrāmatu
description: Šajā rakstā ir aprakstītas iespējas, kas ir saistītas ar Virsgrāmatas apakšgrāmatas pārsūtīšanas procesu Virsgrāmatā.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7ef93b81ce37128f7ff400eb4034ffea01756038
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779858"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Pārsūtīt apakšgrāmatu uz Virsgrāmatu

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas iespējas, kas ir saistītas ar apakšgrāmatas žurnāla ierakstu partiju pārsūtīšanas kārtulām.

Versijā 8.1 tika veiktas izmaiņas, lai varētu pārsūtīt kārtulas, kas novecināja **sinhrono** opciju. Papildinformāciju skatiet sadaļā [Noņemtie vai novecojušie līdzekļi programmai Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Apakšgrāmatas partiju pārsūtīšanai ir pieejamas šādas opcijas:

- **Asinhrons** — Apakšgrāmatas uzskaites ierakstu pārsūtīšana uz Virsgrāmatu tiek plānota nekavējoties. Virsgrāmatas dokuments tiks ierakstīts, tiklīdz būs pieejamie resursi, lai apstrādātu pieprasījumu serverī.
- **Plānotā partija** — pārsūtāmie apakšgrāmatas uzskaites ieraksti tiek pievienoti apstrādes rindai Virsgrāmatā. Rindas ieraksti tiks apstrādāti tādā secībā, kurā tie tiek saņemti. Katrs Virsgrāmatas dokuments atjaunos kontus plānotajā laikā, ja būs pieejamie resursi, lai apstrādātu pakešuzdevumu serverī.

Tika veikti uzlabojumi, **lai uzlabotu asinhronās** opcijas veiktspēju. Šis līdzeklis ir iespējots zem līdzekļa nosaukuma **Apakšgrāmatas pārsūtīšana uz Virsgrāmatas veiktspējas optimizāciju**.

Apakšgrāmatas partiju asinhronās pārsūtīšanas funkcionalitāte palīdz uzlabot datu pārsūtīšanu no apakšgrāmatas uz Virsgrāmatu. Grupējot mazāku darbību kopas un pārsūtot darbības grupās, funkcionalitāte efektīvāk apstrādā darbības. Ja darbības tiek grupētas, pakešapstrādes servera resursi tiek izmantoti efektīvāk.

Asinhronai apakšgrāmatas pakešu pārsūtīšanai ir nepieciešams, lai pakešu serveris tiktu iestatīts tiešsaistē un darbotos, jo pakešuzdevumi tiek izveidoti tūlītējai izpildei pakešu serverī. **Ja ir iespējota apakšgrāmatas pārsūtīšana uz virsgrāmatas veiktspējas optimizācijas** līdzekli, ir jāiespējo arī procesu automatizācijas **sistēmas** pakešuzdevums ar nosaukumu **Procesu automatizācijas aptaujas sistēmas darbs**. Plašāku informāciju skatiet tēmā [Procesa automatizācija](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Efektivitātes maiņa pakešuzdevumu līmenī izmanto vienu periodisku pakešuzdevumu visām sistēmas juridiskajām personām. Izpildlaikā tiek izveidots jauns pakešuzdevums, lai apstrādātu nepieciešamos ierakstus, kas vēl nav pārsūtīti. Vairāk iestatījumu var kontrolēt no sistēmas administrēšanas lapas **Procesa automatizācija**. Šajā lapā varat modificēt fona procesu, mainīt biežumu un definēt vides periodu.

Papildinformāciju par procesa automatizācijas iestatīšanu skatiet sadaļā [Procesa automatizācija](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

