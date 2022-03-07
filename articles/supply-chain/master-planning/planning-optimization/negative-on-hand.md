---
title: Plānošana ar negatīviem rīcībā esošajiem daudzumiem
description: Šajā tēmā izskaidrots, kā, lietojot plānošanas optimizāciju, tiek apstrādāts negatīvs rīcībā esošais daudzums.
author: ChristianRytt
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 97688e09aae9706dd85e7965aa08c7ea873a44d81391c39406e2e6367660e0d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758548"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Plānošana ar negatīviem rīcībā esošajiem daudzumiem

[!include [banner](../../includes/banner.md)]

Ja sistēma rāda negatīvu apkopotu rīcībā esošo daudzumu, plānošanas programma apstrādā daudzumu kā 0 (nulli), lai palīdzētu izvairīties no pasūtījuma apjoma pārsniegšanas. Lūk, kā šī funkcionalitāte darbojas:

1. Plānošanas optimizācijas funkcija apkopo rīcībā esošos daudzumus pie viszemākā vajadzību dimensiju līmeņa. (Piemēram, ja *novietojums* nav vajadzības dimensija, plānošanas optimizācijas apkopo rīcībā esošos daudzumus *noliktavas* līmenī.)
1. Ja kopējais rīcībā esošais daudzums vajadzību dimensiju zemākajā līmenī ir negatīvs, sistēma pieņem, ka rīcībā esošais daudzums patiesībā ir 0 (nulle).

> [!IMPORTANT]
> Plānošanas sistēma var būt tikai tik precīza, cik precīzi ir ievades dati. Ja ievades dati ir neprecīzi, tad negatīvie rīcībā esošie ieraksti norādīs, ka krājumu informācija programmā Microsoft Dynamics 365 Supply Chain Management nav sinhronizēta ar reālo pasauli. Tāpēc plānošanas rezultāts būs kļūdains. Lai iegūtu precīzu plānošanas rezultātu, ir jāsamazina to ierakstu skaits, kuros tiek rādīts negatīvais rīcībā esošais daudzums.

## <a name="example-1"></a>1. piemērs

13. noliktava ir konfigurēta šādā veidā:

- **Vajadzību kods:** Min./Max.
- **Minimālais:** 15 gab.
- **Maksimālais** : 25 gab.

Zemākais seguma dimensiju līmenis ir *noliktava*, un šādi rīcībā esošie daudzumi tiek ierakstīti *vietas* līmenī:

- **1. objekts, 13. noliktava, 1. vieta** 20 gab.
- **1. objekts, 13. noliktava, 2. vieta:** &minus;8 gab.

Tāpēc kopējais rīcībā esošais daudzums 13. noliktavai ir 12 gab. (= 20 gab. &minus; = 8 gab.).

Šādā gadījumā plānošanas programma izmanto kopējo rīcībā esošo daudzumu, kas ir 12 gab. 13. noliktavai.

Rezultāts tiek plānots 13 gab. pasūtījumam. (= 25 gab. &minus; 12 gab.), lai uzpildītu 13. noliktavu no 12 gab. uz 25 gab.

## <a name="example-2"></a>2. piemērs

13. noliktava ir konfigurēta šādā veidā:

- **Vajadzību kods:** Min./Max.
- **Minimālais:** 15 gab.
- **Maksimālais** : 25 gab.

Zemākais seguma dimensiju līmenis ir *noliktava*, un šādi rīcībā esošie daudzumi tiek ierakstīti *vietas* līmenī:

- **1. objekts, 13. noliktava, 1. vieta** 4 gab.
- **1. objekts, 13. noliktava, 2. vieta:** &minus;8 gab.

Tāpēc kopējais rīcībā esošais daudzums 13. noliktavai ir &minus;4 gab. (= 4 gab. &minus; = 8 gab.). Citiem vārdiem sakot, tas ir mazāks par 0 (nulli).

Šajā gadījumā plānošanas programma pieņem, ka rīcībā esošais daudzums 13. noliktavā ir 0 gab. nevis &minus;4 gab.

Rezultāts tiek plānots 25 gab. pasūtījumam. (= 25 gab. &minus; 0 gab.), lai uzpildītu 13. noliktavu no 0 gab. uz 25 gab.

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Plānošana, ja ir rezervēšana pret negatīviem rīcībā esošiem krājumiem

Ja krājumus koriģē, kamēr pastāv fiziskas rezervācijas, var radīt situāciju, kad pasūtījums ir fiziski rezervēts attiecībā pret negatīviem krājumiem. Šajā gadījumā, tā kā pastāv fiziska rezervācija, plānošanas optimizācija pieņem, ka to atbalsta rīcībā esošie krājumi, pat ja rīcībā esošo krājumu saņemšana sistēmā vēl nav reģistrēta. Tāpēc tiek pieņemts, ka papildināšana nav pieprasīta un neizveido plānoto pasūtījumu pasūtījuma daudzuma papildināšanai.

Tas ir atainots tālāk sniegtajā scenārija piemērā.

### <a name="example"></a>Paraugs

Sistēma tiek konfigurēta šādā veidā:

- Pastāv *FG* prece, un tai ir *10* gab. rīcībā esošo krājumu.
- Preces konfigurācija ļauj veikt fiziskus negatīvus krājumus.
- Pastāv pārdošanas pasūtījums daudzumam *10* gab. preču *FG*.
- Pārdošanas pasūtījuma daudzums ir fiziski rezervēts attiecībā pret esošajiem rīcībā esošajiem krājumiem.

Pēc tam koriģējiet preču *FG* daudzumu, lai rīcībā esošie krājumi būtu 0 (nulle). Tā kā rīcībā esošie preču krājumi ir nulle, pārdošanas pasūtījuma daudzums tagad tiek rezervēts pret negatīviem krājumiem. Tomēr, ja palaižat vispārējo plānošanu tagad, netiks izveidots plānotais pasūtījums pārdošanas pasūtījuma piegādei, jo optimizācijas plānošana pieņems, ka nepieciešamie rīcībā esošie krājumi ir, lai piegādātu fizisko rezervēšanu.

## <a name="related-resources"></a>Saistītie resursi

- [Plānošanas optimizācijas apskats](planning-optimization-overview.md)
- [Darba sākšana ar plānošanas optimizāciju](get-started.md)
- [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)
- [Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)
- [Plānošanas darba atcelšana](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
