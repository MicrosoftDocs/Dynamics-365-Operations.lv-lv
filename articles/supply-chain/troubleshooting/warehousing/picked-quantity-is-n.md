---
title: Pavadzīmes ģenerēšanas laikā izdotais daudzums nav pietiekams
description: Izveidojot pavadzīmi, izejošā kravā ir iztotais daudzums, kas neatbilst izveidotajam darba daudzumam uz kravas rindas.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249138"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Pavadzīmes ģenerēšanas laikā izdotais daudzums nav pietiekams

Kļūdas kods: SYS54073

## <a name="symptoms"></a>Simptomi

Izveidojot pavadzīmi, izejošā kravā ir iztotais daudzums, kas neatbilst izveidotajam darba daudzumam uz kravas rindas.

Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:

> Tā kā %1 ir izdoti, %2 nevar grāmatot, ja atlikumam attiecīgi ir jābūt %3.

Tādēļ kravas pavadzīmi nevar ģenerēt.

## <a name="cause"></a>Iemesls

Pavadzīmi nevar ģenerēt tās pašreizējā stāvoklī, jo var pastāvēt viens no tālāk norādītajiem nosacījumiem:

- Saistītais darbs vēl nav izdots un pārvietots uz beigu nosūtīšanas vietu.
- Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu.
- Kravas rindas daudzums, darba izveidotais daudzums un izdotais daudzums nesakrīt.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.
- Pielāgojiet krāvas rindu daudzumu.
- Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt

Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.
1. Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.
1. Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.

### <a name="adjust-the-load-line-quantity"></a>Pielāgojiet kravas rindu daudzumu

Izmantojiet šo procedūru, lai pielāgotu kravas rindas daudzumu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.
1. Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.
1. Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas rada problēmu.
1. Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.
1. Iestatiet lauku **Samazināt kravas rindu**, lai atspoguļotu korekcijas kravas rindā.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu

Problēma var rasties, jo kāds izmanto izdošanas reģistrāciju, lai aizvērtu kravas rindu bez darba. Šajā gadījumā ir jāatgriež manuāla izdošanas reģistrācija un pēc tam, izmantojot mobilo programmu Warehouse Management, izdošanas process ir jāpabeidz.

Lai atsauktu izdošanas reģistrāciju, izmantojiet šādu procedūru.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.
1. Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.
1. Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu, kam veikta izdošanas reģistrācija.
1. Atlasiet **Atjaunināt rindu \> Izdot**, lai anulētu krājumu izdošanu.
