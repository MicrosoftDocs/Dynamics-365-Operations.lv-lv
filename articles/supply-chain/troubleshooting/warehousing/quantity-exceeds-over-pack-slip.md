---
title: Daudzums pārsniedz pasūtījuma pārsnieguma procentus pavadzīmju ģenerēšanas laikā
description: Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas pārsniedz pasūtījuma pārsniegšanas procentus.
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
ms.openlocfilehash: 00e3da7767b80e16f9351f59b109765bffc0128fe149cefafc1edda3a6cbcb96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781349"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Daudzums pārsniedz pasūtījuma pārsnieguma procentus pavadzīmju ģenerēšanas laikā

Kļūdas kods: SYS24920

## <a name="symptoms"></a>Simptomi

Kad ģenerējat pavadzīmi,, izejošā krava ietver daudzumu, kas pārsniedz pasūtījuma pārsniegšanas procentus.

Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:

> Pasūtījuma pārsniegšana rindā ir %1 %, bet atļauts ir tikai %2 %.

Tādēļ kravas pavadzīmi nevar ģenerēt.

## <a name="cause"></a>Iemesls

Kravas vai sūtījuma izdotais daudzums pārsniedz pasūtīto daudzumu, un tas nav pasūtījuma pārslogotās procentuālās vērtības diapazonā.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pielāgojiet krāvas rindu daudzumu.
- Pielāgojiet pārsnieguma procentuālo vērtību.
- Atsaukt un veikt korekcijas.

### <a name="adjust-the-load-line-quantity"></a>Pielāgojiet kravas rindu daudzumu

Izmantojiet šo procedūru, lai pielāgotu kravas rindas daudzumu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.
1. Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.
1. Cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentuālo vērtību.
1. Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.
1. Cilnē  **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.
1. Iestatiet lauku **Daudzums** uz izdoto daudzumu (t.i., uz lauka **Darba izveidotā daudzuma** vērtību), lai varētu turpināt pavadzīmes ģenerēšanu.

### <a name="adjust-the-over-delivery-percentage"></a>Pielāgojiet pārsnieguma procentuālo vērtību

Izmantojiet šo procedūru, lai pielāgotu pārsnieguma procentuālo vērtību.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.
1. Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.
1. Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentuālo vērtību.
1. Cilnē  **Rindu detāļas** atlasiet **Piegāde**, lai pievienotu rindu.
1. Iestatiet lauku **Pasūtījuma pārsniegšana** uz lielāku procentuālo vērtību, kas atbilst izdotajam daudzumam attiecībā pret kravas daudzumu, lai varētu turpināt pavadzīmes ģenerēšanu.

### <a name="reverse-and-make-adjustments"></a>Atsaukt un veikt korekcijas

Atsauciet visu, kas tika iegrāmatots kravai (piemēram, pavadzīmi, kravas apstiprinājumu un darbu), veiciet pārdošanas pasūtījuma korekcijas, vēlreiz izlaidiet pasūtījumu nosūtīšanai uz noliktavu un veiciet nosūtīšanas procedūru.

Izmantojiet šo procedūru, lai atceltu pavadzīmi.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atcelt pavadzīmes**.

Izmantojiet sekojošo procedūru, lai atsauktu sūtījuma apstiprinājumu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Atsaukt** atlasiet **Atsaukt kravas apstiprinājumu**.

Lai atsauktu darbu, izmantojiet šādu procedūru.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Darbību rūts cilnē **Kravas** grupā **Darbs** atlasiet **Atsaukt darbu**.
