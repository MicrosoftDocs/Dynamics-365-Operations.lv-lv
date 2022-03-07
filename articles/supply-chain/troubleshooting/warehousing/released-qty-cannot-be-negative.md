---
title: Nevar atjaunināt noslodzes rindu, jo izpildei nodotais daudzums būtu negatīvs
description: Šī problēma rodas, atjauninot vai dzēšot noslodzes rindu, rodas negatīvs izlaistais daudzums.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728463"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Nevar atjaunināt noslodzes rindu, jo izpildei nodotais daudzums būtu negatīvs

Kļūdas kods: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Simptomi

Šī problēma rodas, atjauninot vai dzēšot noslodzes rindu, rodas negatīvs izlaistais daudzums. Šajā gadījumā, mēģinot atjaunināt vai dzēst noslodzes rindu, sistēma parāda šādu kļūdas ziņojumu:

> Izlaistais daudzums nevar būt negatīvs krājumam %1 laidienā %2.

Tādēļ noslodzes rindu nevar atjaunināt vai dzēst.

## <a name="cause"></a>Iemesls

Pēc noslodzes rindas atjaunināšanas vai dzēšanas sistēma atjaunina saistītās pārdošanas rindas izlaisto daudzumu (*whsSalesLine.ReleaseQty*). Sistēma novērtē izlaisto daudzumu un, ja atrod, ka rindas izlaistais daudzums pēc atjaunināšanas būs negatīvs, tā neļaus atjaunināt vai dzēst rindu. Šī validācija notiek ikreiz, kad mēģināsiet atjaunināt noslodzes rindas daudzumu vai mērvienību, izmantojot dažādas darbības, piemēram, kravas rindas dzēšanu, sūtījuma dzēšanu, kravas rindas daudzuma maiņu, izdotā daudzuma samazināšanu un īso izdošanu.

Visbiežākais šīs problēmas cēlonis ir izmaiņas vienības pārveidošana, kas tiek izmantota atvērtām kravas līnijām. Piemēram, vienību pārveidošana, kad pārdošanas pasūtījums tika izlaists, bija *50 Ea = 1 PL*. Tomēr pirms saistītās kravas nosūtīšanas paveikšanas vienību pārvēršana tika mainīta uz *100 Ea = 1 PL*.

## <a name="resolution"></a>Novēršana

Risinājums ir atgriezt vienības pārvēršanas izmaiņas, atjaunināt vai dzēst noslodzes rindu un pēc tam atkārtoti ieviest pārvēršanu. Jums ir jānovērš citas noslodzes, kas ietver krājumu, kas izraisīja problēmas apstrādi, līdz izdošana ir fiksēta. Pretējā gadījumā jaunās pārveidošanas var izmantot citām kravām, kas jau ir atvērtas.

Lai atrisinātu šo problēmu, izpildiet tālāk norādītos uzdevumus:

1. Pārskatiet mērvienību pārveidošanu, kas tika izmantota noslodzes rindai.
2. Pārskatiet pašreizējo krājuma vienības pārveidošanu un veiciet korekcijas, kas iespējos noslodzes rindas atjaunināšanu vai dzēšanai.
3. Atjauniniet vai dzēsiet noslodzes rindu un atgrieziet vienību pārveidošanas pielāgojumus.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Pārskatiet mērvienību pārveidošanu, kas tika izmantota noslodzes rindai

Izmantojiet tālāk norādītās darbības, lai pārskatītu noslodzes rindas un atzīmētu noslodzes rindai izmantoto vienību pārveidošanu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atlasiet kravu, kas ietver noslodzes rindu, ko nevar dzēst vai atjaunināt.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Augšējā režģī atlasiet atbilstošo darba ID.
1. Cilnes **Vispārīgi** lapas apakšdaļā aprēķiniet pārveidošanas kursu starp vērtību **Krājumu darba daudzums** un vērtību **Darba daudzums**. Pierakstiet likmi.
1. Atkārtojiet šo procedūru visiem atbilstošajiem darbu ID, lai nodrošinātu, ka tiek izmantota tā pati pārveidošana.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Pārskatīt pašreizējo krājuma vienības pārveidošanu un veikt korekcijas

Izmantojiet šo procedūru, lai pārskatītu preču vienību pārveidošanu un veiciet pielāgojumus, lai nodrošinātu, ka vienības pārveidošana ir saskaņota ar krāvas rindu.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet atbilstošu preci, lai dotos uz tās **Izlaistā produkta informācijas** lapu.
1. Darbību rūtī cilnē **Prece** grupā **Iestatīt**, atlasiet **Mērvienību pārveidošana**.
1. Atlasiet vienību pārveidošanu un veiciet pielāgojumus, izmantojot iepriekšējā sadaļā atrodamo pārveidošanu.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Atjauniniet vai dzēsiet noslodzes rindu un atgrieziet vienību pārveidošanas pielāgojumus

Izmantojiet šo procedūru, lai pēc vajadzības apstrādātu noslodzes rindu un atgrieztu vienību pārveidošanu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atvēriet kravu, kas ietver noslodzes rindu, ko nevar dzēst vai atjaunināt.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.
1. Ja nepieciešams, turpiniet ar nepieciešamajām darbībām. (Piemēram, dzēsiet kravas rindu vai mainiet tās daudzumu.)
1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet atbilstošu preci, lai dotos uz tās **Izlaistā produkta informācijas** lapu.
1. Darbību rūtī cilnē **Prece** grupā **Iestatīt**, atlasiet **Mērvienību pārveidošana**.
1. Atlasiet vienību pārveidošanu un atjaunojiet iepriekšējā sadaļā veiktās korekcijas.
