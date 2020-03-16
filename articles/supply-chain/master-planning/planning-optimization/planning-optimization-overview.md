---
title: Plānošanas optimizācijas pārskats
description: Šajā tēmā ir sniegts pārskats par Plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: 9ccf00b6fcd1e3a6002086360b1a4c5c464ba054
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076159"
---
# <a name="planning-optimization-overview"></a>Plānošanas optimizācijas pārskats

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Plānošanas optimizācijas pievienojumprogramma, kas paredzēta Microsoft Dynamics 365 Supply Chain Management, ļauj veikt vispārējās plānošanas aprēķinus Dynamics 365 Supply Chain Management, kas tiek notiek ārpusē, un saistīto SQL datu bāzi. Priekšrocības, kas saistītas ar plānošanas optimizācijas funkcionalitāti, vispārējās plānošanas izpildes laikā ietver uzlabotu veiktspēju un minimālu ietekmi uz SQL datu bāzi. Ātro plānošanu var veikt arī darba stundu laikā, lai plānotāji varētu nekavējoties reaģēt uz pieprasījumu vai parametru izmaiņām.

Lai izmantotu plānošanas optimizāciju, jums ir jāinstalē Plānošanas optimizācijas pievienojumprogramma no jūsu projekta Microsoft Dynamics Lifecycle Services (LCS) un jāieslēdz Plānošanas optimizācijas funkcionalitāte Supply Chain Management. Papildinformāciju skatiet [Sākt darbu ar Plānošanas optimizāciju ](get-started.md).

Sekojošajā attēlā redzama Plānošanas optimizācijas priekšrocība darba stundu laikā.

![Plānošanas optimizācijas priekšrocība darba stundu laikā](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Uzlabota veiktspēja

Plānošanas optimizāciju var izmantot scenārijos, kas ietver ilgstošus galvenos plānus. Tas ir īpaši izstrādāts ļoti ātriem aprēķiniem, kas ietver ļoti lielus datu apjomus. Tā kā tas ir izveidots kā hiperpielāgojams daudznomnieka pakalpojums, vairākas instances vienlaicīgi var strādāt kopā, lai aprēķinātu plānu. Turklāt plānošanas pakalpojums noņem vispārējās plānošanas noslodzi no sistēmas un strādā ar datu plūsmu, kas samazina servera noslodzi.

Plānošanas optimizācija var palīdzēt sasniegt šādus mērķus:

- Uzlabot plānošanas veiktspēju, izmantojot īsāku izpildlaiku.
- Samazināt ietekmi uz citiem procesiem vispārējās plānošanas izpildes laikā.
- Veikt biežāku plānošanu. (Jūs neesat ierobežots ar ikdienas plānošanu.)
- Esiet pārliecināts, ka turpmākā biznesa izaugsme nepārslogos plānošanas sistēmu.

## <a name="architecture-and-data-flow"></a>Arhitektūra un datu plūsma

Kad Plānošanas optimizācijas pievienojumprogramma ir instalēta no LCS, tiek izveidots drošs savienojums ar Plānošanas optimizācijas pakalpojumiem. Pakalpojums atrodas tajā pašā datu centra valstī vai reģionā, kā saistītā Supply Chain Management instance. Pēc Plānošanas optimizācijas iestatīšanas, kad tiek palaista vispārējā plānošana, galvenie dati un transakciju dati tiek sūtīti no Supply Chain Management uz Plānošanas optimizācijas pakalpojumu.

Ja Plānošanas optimizācijas pievienojumprogramma ir atinstalēta, visi saistītie dati Plānošanas optimizācijas pakalpojumā tiek noņemti.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Augsta līmeņa datu plūsma atjaunošanai tiek veikta

1. Supply Chain Management klients nosūta signālu, lai pieprasītu plānošanas palaišanu no plānošanas optimizācijas.
2. Plānošanas optimizācija pieprasa vajadzīgos datus, izmantojot iebūvēto savienotāju.
3. SQL datu bāze sūta pieprasīto informāciju par iestatīšanas, šablona un darbības datiem plānošanas optimizēšanai, izmantojot savienotāju. Savienotājs tulko informāciju starp Supply Chain Management un plānošanas optimizācijas pakalpojumu.
4. Plānošanas optimizācijas pakalpojuma rīcībā ir ar plānošanu saistīti dati atmiņā un tiek veikti vajadzīgie aprēķini.
5. Plānošanas rezultāts tiek nosūtīts uz Supply Chain Management  datu bāzi, izmantojot savienotāju. Rezultātos ietilpst informācija, piemēram, plānotie pasūtījumi un piesaistes informācija. Plānošanas optimizācija nosūta signālu uz Supply Chain Management, lai norādītu, ka plānošanas izpilde ir pabeigta. Tas arī nosūta jebkādus svarīgus ziņojumus un brīdinājumus.

Nākamajā attēlā ir redzamas datu plūsmas.

![Datu plūsma atjaunošanai tiek veikta](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Saistītie resursi

[Darba sākšana ar Plānošanas optimizāciju](get-started.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Filtru lietošana plānam](plan-filters.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)
