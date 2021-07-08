---
title: Vienības fiziskais atlikušais daudzums nedrīkst būt nulle
description: Izveidojot pavadzīmi, tai piegādāto datu krājumu daudzums nav nulle, bet pārdošanas daudzums ir nulle.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248792"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Vienības fiziskais atlikušais daudzums nedrīkst būt nulle

Kļūdas kods: SYS19591

## <a name="symptoms"></a>Simptomi

Izveidojot pavadzīmi, tai piegādāto datu krājumu daudzums nav nulle, bet pārdošanas daudzums ir nulle.

Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:

> Vienības %1 fiziskais atlikums nedrīkst būt nulle.

Tādēļ kravas pavadzīmi nevar ģenerēt.

## <a name="cause"></a>Iemesls

Sistēma aprēķina fizisko atlikušo daudzumu krājumu uzskaites vienībā un fizisko atlikušo daudzumu nosūtīšanas vienībā. Ja sistēma konstatē, ka fiziskais atlikušais daudzums nosūtīšanas vienībā ir 0 (nulle), bet fiziskais atlikušais daudzums krājumu uzskaites vienībā nav 0, pavadzīmi nevar ģenerēt. Piemēram, šī problēma var rasties, ja pārdošanas vienība un krājuma uzskaites vienība atšķiras un vienību pārveidošana nav precīza.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.
- Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez noapaļošanas problēmām.
- Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti.
- Pārliecinieties, vai krājumu mērvienība ir mazāka nekā pārdošanas mērvienība.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt

Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.
1. Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.
1. Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez noapaļošanas problēmām

Izmantojiet šo procedūru, lai pārskatītu kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez noapaļošanas problēmām.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.
1. Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.
1. Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsniegumu.
1. Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.
1. Cilnē  **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.
1. Iestatiet lauku **Daudzums** uz izdoto daudzumu (t.i., uz lauka **Darba izveidotā daudzuma** vērtību), lai varētu turpināt pavadzīmes ģenerēšanu.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti

Izmantojiet šo procedūru, lai pārskatītu kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.
1. Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu. Atzīmējiet lauku **Daudzums** un **Vienība** vērtību.
1. Pārejiet uz sadaļu **Organizācijas administrēšana \> Vienības \> Vienības**.
1. Atlasiet vienību, kurai nevar ģenerēt pavadzīmi.
1. Pēc vajadzības pielāgojiet lauka **Decimālā precizitāte** vērtību.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Pārliecinieties, vai krājumu mērvienība ir mazāka nekā pārdošanas mērvienība

Pārliecinieties, vai krājumu mērvienība ir mazāka nekā pārdošanas mērvienība. Ja nepieciešams, apsveriet iespēju atkārtoti konfigurēt krājuma mērvienību.
