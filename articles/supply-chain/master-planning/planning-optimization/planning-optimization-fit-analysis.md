---
title: Plānošanas optimizācijas saderības analīze
description: Šajā tēmā skaidrots, kā verificēt jūsu pašreizējos iestatījumus un datus, salīdzinot ar Plānošanas optimizācijas funkcionalitātes iespējām.
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774006"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a>Plānošanas optimizācijas saderības analīze

Lai apskatītu, cik saderīgi ir jūsu pašreizējie iestatījumi un dati ar Plānošanas optimizācijas funkcionalitāti, dodieties uz **Vispārējā plānošana**\>**Iestatīšana**\>**Plānošanas optimizācijas saderības analīze**, un pēc tam atlasiet **Palaist analīzi**. Ja analīze atklāj neatbilstības, tās ir uzskaitītas tajā pašā lapā. (Analīze var ilgt dažas minūtes.)

> [!NOTE]
> Ja atrastas neatbilstības, joprojām varat izmantot Plānošanas optimizāciju. Saderības analīzes rezultāti tikai rāda vietas, kur plānošanas pakalpojums neievēros jūsu pašreizējos iestatījumus. Citiem vārdiem, tas rāda vietas, kur daži procesi var tikt ignorēti vai, iespējams, netiek atbalstīti.

## <a name="analysis-results-example-1"></a>Analīzes rezultāti: 1. piemērs

- **Līdzeklis:** ražošana
- **Problēma:** krājumi ar MK līmeni lielāki par nulli: 56
- **Paskaidrojums:** saderības analīze atrada 56 krājumus, kuriem ir materiālu komplekta (MK) iestatījums ražošanai. Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta ražošanu, tā izveidos plānotos pirkšanas pasūtījumus, nevis plānotos ražošanas pasūtījumus. Tiks parādīts arī brīdinājums, kas uzskaita ietekmētos krājumus.

### <a name="analysis-results-example-2"></a>Analīzes rezultāti: 2. piemērs

- **Līdzeklis:** darbības
- **Problēma:** nodrošinājuma grupas ar iespējotu darbību aprēķinu: 6
- **Paskaidrojums:** saderības analīze atrada sešas nodrošinājuma grupas, kurās ir ieslēgts darbības aprēķins. Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta darbības, vispārējās plānošanas laikā netiks ģenerētas darbības.

## <a name="related-resources"></a>Saistītie resursi

[Plānošanas optimizācijas pārskats](planning-optimization-overview.md)

[Darba sākšana ar Plānošanas optimizāciju](get-started.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Filtru lietošana plānam](plan-filters.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)
