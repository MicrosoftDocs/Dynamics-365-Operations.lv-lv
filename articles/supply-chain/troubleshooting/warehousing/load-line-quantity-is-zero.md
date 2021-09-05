---
title: Nevar apstiprināt sūtījumu, jo kravas rindām ir nulles daudzums
description: Nevar apstiprināt sūtījumu, jo kravas rindām ir nulles daudzums.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 15aa7f5e72ff8f2c027b5b020a23328978aa02b0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344238"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Nevar apstiprināt sūtījumu, jo kravas rindām ir nulles daudzums

Kļūdas kods: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Visu noslodzē %1 esošo rindu daudzums ir nulle.  
> Kravas %1 piegādi nevarēja apstiprināt.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Sistēma novērtē, vai kravas rindu var apstiprināt, pamatojoties uz izveidotajiem darba ID, noslodzes rindas daudzumu un nepilnā pasūtījuma procentuālo vērtību. Ja sistēma konstatē, ka nav darba ID un ja nepilnā pasūtījuma procentuālā vērtība ir iestatīta uz 100 procentiem, sūtījumu nevar apstiprināt.

Piemēram, šī problēma var rasties, ja darbs ir atcelts un kravas rindas nepilnā pasūtījuma procentuālā vērtība ir 100 procenti.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad sūtījuma apstiprināšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pārskatiet savas kravas rindas, lai pārliecinātos, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.
- Pārskatiet kravas rindas, lai nodrošinātu, ka nepilnā pasūtījuma procentuālā vērtība un daudzumi ir saskaņoti ar izdoto darbu.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Pārskatiet savas kravas rindas, lai pārliecinātos, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt

Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas, lai pārliecinātos, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atvētiet kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.
1. Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.
1. Ja atradīsit neatbilstību, atceliet atbilstošo darbu, pārkonfigurējiet novietojuma direktīvu un atkārtoti izlaidiet krāvu. Norādījumus skatiet [Nevar apstiprināt sūtījumu, jo nav izdoti krājumi](picked-quantity-is-not-on-final.md).
1. Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Pārskatiet kravas rindas, lai nodrošinātu, ka nepilnā pasūtījuma procentuālā vērtība un daudzumi ir saskaņoti ar izdoto darbu

Izmantojiet šo procedūru, lai pārskatītu kravas rindas, lai nodrošinātu, ka nepilnā pasūtījuma procentuālā vērtība un daudzumi ir saskaņoti ar izdoto darbu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atvētiet kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz nepilnā pasūtījuma procentus.
1. Pēc vajadzības koriģējiet lauka **Nepilns pasūtījums** vērtību vai lauku **Daudzums**.

> [!TIP]
> Ja problēma vēl nav fiksēta, iespējams, būs jāpabeidz vairāk izdošanas darbu saistītajiem pārdošanas pasūtījumiem vai pārsūtīšanas pasūtījumiem, līdz pieejamais daudzums ir saskaņots ar kravu vai sūtījumu.
