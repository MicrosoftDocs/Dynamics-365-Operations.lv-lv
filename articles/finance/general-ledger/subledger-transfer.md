---
title: Pārsūtīt apakšgrāmatu uz Virsgrāmatu
description: Šajā tēmā ir aprakstītas iespējas, kas saistītas ar apakšgrāmatas pārvirzīšanu Virsgrāmatā.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 70a34fa1f4ee540d89ec05816e4065fb3e1df9ef
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727319"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Pārsūtīt apakšgrāmatu uz Virsgrāmatu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas iespējas, kas attiecas uz apakšgrāmatas žurnāla ierakstu partiju pārsūtīšanas kārtulām.

Versijā 8.1 tika veiktas izmaiņas, lai varētu pārsūtīt kārtulas, kas novecināja **sinhrono** opciju. Papildinformāciju skatiet finanšu [un operāciju noņemtos vai novecojušus līdzekļus](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Apakšgrāmatas partiju pārsūtīšanai ir pieejamas šādas opcijas:

- **Asinhrons** — Apakšgrāmatas uzskaites ierakstu pārsūtīšana uz Virsgrāmatu tiek plānota nekavējoties. Virsgrāmatas dokuments tiks ierakstīts, tiklīdz būs pieejamie resursi, lai apstrādātu pieprasījumu serverī.
- **Plānotā partija** — pārsūtāmie apakšgrāmatas uzskaites ieraksti tiek pievienoti apstrādes rindai Virsgrāmatā. Rindas ieraksti tiks apstrādāti tādā secībā, kurā tie tiek saņemti. Katrs Virsgrāmatas dokuments atjaunos kontus plānotajā laikā, ja būs pieejamie resursi, lai apstrādātu pakešuzdevumu serverī.

Versijā 10.0.8 tika veikti uzlabojumi, lai uzlabotu opcijas **Asinhrons** veiktspēju. Šis līdzeklis ir iespējots zem līdzekļa nosaukuma **Apakšgrāmatas pārsūtīšana uz Virsgrāmatas veiktspējas optimizāciju**.

Apakšgrāmatas partiju asinhronās pārsūtīšanas funkcionalitāte palīdz uzlabot datu pārsūtīšanu no apakšgrāmatas uz Virsgrāmatu. Grupējot mazāku darbību kopas un pārsūtot darbības grupās, funkcionalitāte efektīvāk apstrādā darbības. Ja darbības tiek grupētas, pakešapstrādes servera resursi tiek izmantoti efektīvāk.

Apakšgrāmatas partiju asinhronai pārsūtīšanai nepieciešams, lai pakešu serveri iestatītu tiešsaistē un darbojas, jo pakešuzdevumi ir izveidoti pakešu servera tūlītējai izpildei. Ja apakšgrāmatas **pārsūtīšana** uz Virsgrāmatas veiktspējas optimizācijas līdzekli ir iespējota, **·** **jāiespējo** arī procesa automatizācijas sistēmas pakešuzdevums ar nosaukumu "Apstrādāt automatizācijas aptauju sistēmas darbu". Plašāku informāciju skatiet tēmā [Procesa automatizācija](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Efektivitātes maiņa pakešuzdevumu līmenī izmanto vienu periodisku pakešuzdevumu visām sistēmas juridiskajām personām. Izpildlaikā tiek izveidots jauns pakešuzdevums, lai apstrādātu nepieciešamos ierakstus, kas vēl nav pārsūtīti. Vairāk iestatījumu var kontrolēt no sistēmas administrēšanas lapas **Procesa automatizācija**. Šajā lapā varat modificēt fona procesu, mainīt biežumu un definēt vides periodu.

Papildinformāciju par procesa automatizācijas iestatīšanu skatiet sadaļā [Procesa automatizācija](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
