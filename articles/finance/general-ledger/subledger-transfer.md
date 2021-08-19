---
title: Pārsūtīt apakšgrāmatu uz Virsgrāmatu
description: Šajā tēmā ir aprakstītas iespējas, kas saistītas ar apakšgrāmatas pārvirzīšanu Virsgrāmatā.
author: rcarlson
ms.date: 07/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 03c04a5eb8b544b582019ddd204382900b162d952842c901f69ed4a853bd8183
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716649"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Pārsūtīt apakšgrāmatu uz Virsgrāmatu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas iespējas, kas attiecas uz apakšgrāmatas žurnāla ierakstu partiju pārsūtīšanas kārtulām.

Versijā 8.1 tika veiktas izmaiņas, lai varētu pārsūtīt kārtulas, kas novecināja **sinhrono** opciju. Papildinformāciju skatiet šeit: [Noņemtie vai novecojušie līdzekļi programmai Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Apakšgrāmatas partiju pārsūtīšanai ir pieejamas šādas opcijas:

- **Asinhrons** — Apakšgrāmatas uzskaites ierakstu pārsūtīšana uz Virsgrāmatu tiek plānota nekavējoties. Virsgrāmatas dokuments tiks ierakstīts, tiklīdz būs pieejamie resursi, lai apstrādātu pieprasījumu serverī.
- **Plānotā partija** — pārsūtāmie apakšgrāmatas uzskaites ieraksti tiek pievienoti apstrādes rindai Virsgrāmatā. Rindas ieraksti tiks apstrādāti tādā secībā, kurā tie tiek saņemti. Katrs Virsgrāmatas dokuments atjaunos kontus plānotajā laikā, ja būs pieejamie resursi, lai apstrādātu pakešuzdevumu serverī.

Versijā 10.0.8 tika veikti uzlabojumi, lai uzlabotu opcijas **Asinhrons** veiktspēju. Šis līdzeklis ir iespējots zem līdzekļa nosaukuma **Apakšgrāmatas pārsūtīšana uz Virsgrāmatas veiktspējas optimizāciju**.

Apakšgrāmatas partiju asinhronās pārsūtīšanas funkcionalitāte palīdz uzlabot datu pārsūtīšanu no apakšgrāmatas uz Virsgrāmatu. Grupējot mazāku darbību kopas un pārsūtot darbības grupās, funkcionalitāte efektīvāk apstrādā darbības. Ja darbības tiek grupētas, pakešapstrādes servera resursi tiek izmantoti efektīvāk.

Apakšgrāmatas partiju asinhronai pārsūtīšanai nepieciešams, lai partijas serveris būtu iestatīts, pieejams tiešsaistē un darbotos. Pretējā gadījumā pārsūtīšanas opcija **Asinhrons** nedarbosies.

Efektivitātes maiņa pakešuzdevumu līmenī izmanto vienu periodisku pakešuzdevumu visām sistēmas juridiskajām personām. Izpildlaikā tiek izveidots jauns pakešuzdevums, lai apstrādātu nepieciešamos ierakstus, kas vēl nav pārsūtīti. Vairāk iestatījumu var kontrolēt no sistēmas administrēšanas lapas **Procesa automatizācija**. Šajā lapā varat modificēt fona procesu, mainīt biežumu un definēt vides periodu.

Papildinformāciju par procesa automatizācijas iestatīšanu skatiet sadaļā [Procesa automatizācija](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
