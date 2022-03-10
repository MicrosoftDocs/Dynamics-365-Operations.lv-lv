---
title: Daudzums nesasniedz pasūtījuma procentus pavadzīmju ģenerēšanas laikā
description: Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas nesasniedz pasūtījuma procentus.
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
ms.openlocfilehash: 7cdc22eeabda6cf9f08484d698e5096f66af4a12
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920702"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Daudzums nesasniedz pasūtījuma procentus pavadzīmju ģenerēšanas laikā

Kļūdas kods: SYS24921

## <a name="symptoms"></a>Simptomi

Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas nesasniedz pasūtījuma procentus.

Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:

> Nepilns pasūtījums rindā ir %1 %, bet atļauts ir tikai %2 %.

Tādēļ kravas pavadzīmi nevar ģenerēt.

## <a name="cause"></a>Iemesls

Kravas vai sūtījuma izdotais daudzums nesasniedz pasūtīto daudzumu, un tas nav pasūtījuma procentuālās vērtības diapazonā.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pielāgojiet procentuālās vērtības nesasniegšanu.
- Atsaukt un veikt korekcijas.

### <a name="adjust-the-under-delivery-percentage"></a>Pielāgojiet procentuālās vērtības nesasniegšanu

Izmantojiet šo procedūru, lai pielāgotu procentuālās vērtības nesasniegšanu.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.
1. Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.
1. Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu krājumam, kas pārsniedz neļaus pasūtījuma apjoma procentuālo vērtību.
1. Cilnē **Detalizēta informācija par** rindu atlasiet **Piegāde**.
1. Iestatiet lauku **Pasūtījuma nesasniegšanu** uz lielāku procentuālo vērtību, kas atbilst izdotajam daudzumam attiecībā pret kravas daudzumu, lai varētu turpināt pavadzīmes ģenerēšanu.

### <a name="reverse-and-make-adjustments"></a>Atsaukt un veikt korekcijas

Atsauciet visu, kas tika iegrāmatots kravai (piemēram, pavadzīmi, kravas apstiprinājumu un darbu), veiciet pārdošanas pasūtījuma korekcijas, vēlreiz izlaidiet pasūtījumu nosūtīšanai uz noliktavu un veiciet nosūtīšanas procedūru.

Izmantojiet šo procedūru, lai atceltu pavadzīmi.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Darbību rūts cilnes Nosūtīt un saņemt grupā Atcelt pavadzīmes atlasiet **Atcelt** **·** **pavadzīmes**.

Izmantojiet sekojošo procedūru, lai atsauktu sūtījuma apstiprinājumu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Darbību rūts cilnē Nosūtīt **un saņemt** apgrieztajā grupā atlasiet Atsaukt **kravas** **apstiprinājumu**.

Lai atsauktu darbu, izmantojiet šādu procedūru.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Darbību rūts cilnes **Noslodzes** sadaļā Darba grupa atlasiet **Atsaukt** **darbu**.
