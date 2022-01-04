---
title: Atjaunināšanai izmantotais daudzums pārsniedz saņemto/piegādāto daudzumu.
description: Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas pārsniedz izveidotā darba daudzumu, kas tika izdots un rezervēts pārdošanas pasūtījumam.
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
ms.openlocfilehash: ec5e0ac8dd097e5ebf016683fc5c17df7ecb2305
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920402"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Atjaunināšanai izmantotais daudzums pārsniedz saņemto/piegādāto daudzumu

Kļūdas kods: SYS7676

## <a name="symptoms"></a>Simptomi

Izveidojot pavadzīmi, izejošā kravā ir daudzums, kas pārsniedz izveidotā darba daudzumu, kas tika izdots un rezervēts pārdošanas pasūtījumam.

Mēģinot ģenerēt pavadzīmi, sistēma rāda šādu kļūdas ziņojumu:

> Atjaunināšanai atlasītais daudzums pārsniedz saņemto/piegādāto daudzumu.

Tādēļ kravas pavadzīmi nevar ģenerēt.

## <a name="cause"></a>Iemesls

Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu. Piemēram, šī problēma var rasties, ja noslodzes rindas daudzums, darba izveidotais daudzums vai izdotais daudzums nav pareizs.

## <a name="resolution"></a>Novēršana

Krava vai sūtījums pašlaik ir stāvoklī, kad pavadzīmes ģenerēšana neizdodas. Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.
- Pielāgojiet krāvas rindu daudzumu.
- Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Pārskatiet savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt

Izmantojiet šo procedūru, lai pārskatītu savas kravas rindas un pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar ģenerēt nosūtījumu.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.
1. Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.
1. Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.

### <a name="adjust-the-load-line-quantity"></a>Pielāgojiet kravas rindu daudzumu

Izmantojiet šo procedūru, lai pielāgotu kravas rindas daudzumu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kurai nevar ģenerēt pavadzīmi.
1. Darbību rūts cilnē Nosūtīt **un saņemt** apgrieztajā grupā atlasiet Atsaukt **kravas** **apstiprinājumu**.
1. Cilnē **Kravas rindas** atlasiet krājuma noslodzes rindu, kas izraisa problēmu.
1. Atlasiet **Samazināt izdoto daudzumu**, lai koriģētu izdoto daudzumu.
1. Iestatiet lauku **Samazināt kravas rindu**, lai atspoguļotu korekcijas kravas rindā.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Atsauciet visas izdošanas reģistrācijas un atceliet izdošanu

Ja kāds izmanto izdošanas reģistrāciju, lai slēgtu kravas rindu bez darba, var rasties neatbilstība starp kravas rindas daudzumu un izdoto daudzumu. Šajā gadījumā ir jāatgriež manuāla izdošanas reģistrācija un pēc tam, izmantojot mobilo programmu Warehouse Management, izdošanas process ir jāpabeidz.

Lai atsauktu izdošanas reģistrāciju, izmantojiet šādu procedūru.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pasūtījumi**.
1. Atlasiet pārdošanas pasūtījumu, kuram nevar grāmatot kravas pavadzīmi.
1. Cilnē **Pārdošanas pasūtījuma rindas** atlasiet pārdošanas pasūtījuma rindu, kam veikta izdošanas reģistrācija.
1. Atlasiet **Atjaunināt rindu \> Izdot**, lai anulētu krājumu izdošanu.
