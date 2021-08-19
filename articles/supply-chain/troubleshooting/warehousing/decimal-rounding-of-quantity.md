---
title: Fiziskā daudzuma decimāldaļas noapaļošana nav pareiza
description: Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas neatbilst decimāldaļas precizitātei, kas ir definēta vienībā.
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
ms.openlocfilehash: ddfac7106eb0e8b934516ca10e3950891d10910a2ccdef1868faf25812243159
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726565"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Fiziskā daudzuma decimāldaļas noapaļošana nav pareiza

Kļūdas kods: SYS19589

## <a name="symptoms"></a>Simptomi

Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas neatbilst decimāldaļas precizitātei, kas ir definēta vienībā.

Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:

> Nepareizi noapaļotas vienības %1 fiziskā daudzuma decimāldaļas.

Tādēļ kravas pavadzīmi nevar ģenerēt.

## <a name="cause"></a>Iemesls

Sistēma novērtē, vai nosūtīšanas daudzuma decimālā noapaļošana atbilst nosūtīšanas vienībai definētajai decimāldaļas precizitātei. Kad sistēma noapaļo nosūtāmo daudzumu līdz norādītajam decimāldaļu skaitam, ja tiek atrasts, ka noapaļotais nosūtīšanas daudzums neatbilst faktiskajam nosūtīšanas daudzumam, jūs nevarat ģenerēt pavadzīmi. Piemēram, šī problēma var rasties, ja pārdošanas daudzums ir 1,75 kilogrami (kg), bet decimālā precizitāte ir iestatīta uz *1*.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez decimālskaitļiem un jebkurām citām noapaļošanas problēmām.
- Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka vienība un daudzums ir saskaņoti ar vienības decimālo precizitāti.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Pārskatiet kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez decimālskaitļiem un jebkurām citām noapaļošanas problēmām

Izmantojiet šo procedūru, lai pārskatītu kravas rindas un veiciet pielāgojumus, lai nodrošinātu, ka daudzumu var notīrīt bez decimālskaitļiem un jebkurām citām noapaļošanas problēmām.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.
1. Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.
1. Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu.
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
