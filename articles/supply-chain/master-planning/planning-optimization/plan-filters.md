---
title: Izmantot filtrus plānam
description: Šajā tēmā izskaidrots, kā izmantot filtrus plānam, kad izmanto funkcionalitāti Plānošanas optimizācija.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
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
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774007"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a>Izmantot filtrus plānam

Kad tiek izmantota plānošanas optimizācijas funkcionalitāte, var izmantot filtru plānam. Plāna filtrs vienmēr tiks lietots vispārējās plānošanas izpildes laikā. Plāna filtrs ir noderīgs, ja vēlaties ierobežot plānu līdz noteiktai krājumu grupai, un pārliecināties, vai citi krājumi nav ietverti kā daļa no iegūtās vispārējās plānošanas.

Ja tiek lietots plāna filtrs un tiek lietots arī izpildlaika filtrs vispārējās plānošanas izpildes laikā, tikai abu filtru krustpunkts tiek iekļauts plānošanas darbībā.

## <a name="example-scenario"></a>Piemēra situācija

Ir iestatīts plāna filtrs, kas ietver krājumus A, B un C. Vispārējā plānošana tiek palaista vienam un tam pašam plānam, bet tiek piemēroti dažādi izpildlaika filtri:

- **Izpildlaika filtrs, kas ietver krājumu D:** Netiek plānoti krājumi, jo starp plāna filtru un izpildlaika filtru nav krustpunkta.
- **Izpildlaika filtrs, kas ietver krājumus A un D:** Plānošanas darbībā iekļauj tikai krājumu A, jo krājums D nav daļa no plāna filtra.
- **Izpildlaika filtrs, kas ietver krājumu B:** Plānošanas darbībā iekļauj tikai krājumu B, un tiek paturēta iepriekšējais plānošanas izvade krājumam A.
- **Izpildlaika filtrs, kas ietver visus elementus (tukšs filtrs):** Krājumi A, B un C tiek iekļauti plānošanas darbībā, un iepriekšējā plānošanas izvade A un B tiek pārrakstīta.

> [!NOTE]
> Jums vajadzētu izvairīties no plāna filtra iestatīšanas plānā, kas ir izvēlēts kā **Pašreizējais dinamiskais vispārējais plāns** **Vispārējās plānošanas parametru** lapā. Pretējā gadījumā dinamiskā vispārējā plāna funkcionalitāte tiks ierobežota līdz filtrētajiem krājumiem. Piemēram, ja neto vajadzības tiek atjauninātas krājumam, kas nav daļa no plāna filtra, rezultāts netiks ģenerēts.

## <a name="related-resources"></a>Saistītie resursi

[Plānošanas optimizācijas pārskats](planning-optimization-overview.md)

[Darba sākšana ar Plānošanas optimizāciju](get-started.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)
