---
title: Plānošana ar negatīviem rīcībā esošajiem daudzumiem
description: Šajā tēmā izskaidrots, kā, lietojot plānošanas optimizāciju, tiek apstrādāts negatīvs rīcībā esošais daudzums.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983470"
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

Rezultāts tiek plānots 13 gab. pasūtījumam. (= 25 gab. &minus;12 gab.), lai uzpildītu 13. noliktavu no 12 gab. uz 25 gab.

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

Rezultāts tiek plānots 25 gab. pasūtījumam. (= 25 gab. &minus;0 gab.), lai uzpildītu 13. noliktavu no 0 gab. uz 25 gab.

## <a name="related-resources"></a>Saistītie resursi

[Plānošanas optimizācijas apskats](planning-optimization-overview.md)

[Darba sākšana ar plānošanas optimizāciju](get-started.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]