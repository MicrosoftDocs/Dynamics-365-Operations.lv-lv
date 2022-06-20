---
title: Izmantot filtrus plānam
description: Šajā rakstā ir izskaidrots, kā izmantot plāna filtrus, kad tiek izmantota plānošanas optimizācijas funkcionalitāte.
author: t-benebo
ms.date: 01/08/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c2df379be0876225bc7b0301d21f4e6660b04eb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875309"
---
# <a name="apply-filters-to-a-plan"></a>Izmantot filtrus plānam

[!include [banner](../../includes/banner.md)]

Kad tiek izmantota plānošanas optimizācijas funkcionalitāte, var izmantot filtru plānam. **Plāna filtrs**  vienmēr tiks lietots vispārējās plānošanas izpildes laikā. **Plāna filtrs** ir noderīgs, ja vēlaties ierobežot plānu līdz noteiktai krājumu grupai, un pārliecināties, vai citi krājumi nav ietverti kā daļa no iegūtās vispārējās plānošanas.

Ja tiek lietots **Plāna filtrs** un tiek lietots arī izpildlaika filtrs vispārējās plānošanas izpildes laikā, tikai abu filtru krustpunkts tiek iekļauts plānošanas darbībā.

**Plāna filtram** var piekļūt no **Vispārējiem plāniem**, kad tiek izmantota plānošanas optimizācija.

## <a name="example-scenario"></a>Piemēra situācija

Ir iestatīts plāna filtrs, kas ietver krājumus A, B un C. Vispārējā plānošana tiek palaista vienam un tam pašam plānam, bet tiek piemēroti dažādi izpildlaika filtri:

- **Izpildlaika filtrs, kas ietver krājumu D:** Netiek plānoti krājumi, jo starp plāna filtru un izpildlaika filtru nav krustpunkta.
- **Izpildlaika filtrs, kas ietver krājumus A un D:** Plānošanas darbībā iekļauj tikai krājumu A, jo krājums D nav daļa no plāna filtra.
- **Izpildlaika filtrs, kas ietver krājumu B:** Plānošanas darbībā iekļauj tikai krājumu B, un tiek paturēta iepriekšējais plānošanas izvade krājumam A.
- **Izpildlaika filtrs, kas ietver visus elementus (tukšs filtrs):** Krājumi A, B un C tiek iekļauti plānošanas darbībā, un iepriekšējā plānošanas izvade A un B tiek pārrakstīta.

> [!NOTE]
> Ja vispārējās **plānošanas** **parametru** lapā iestatāt plāna filtru, kas lapā Vispārējās plānošanas parametri ir atlasīts kā pašreizējais dinamiskais vispārējais plāns, tad dinamiskā vispārējā plāna funkcionalitāte tiks ierobežota līdz filtrētiem krājumiem. Piemēram, ja neto vajadzības tiek atjauninātas krājumam, kas nav daļa no plāna filtra, rezultāts netiks ģenerēts.

## <a name="related-resources"></a>Saistītie resursi

[Plānošanas optimizācijas pārskats](planning-optimization-overview.md)

[Darba sākšana ar Plānošanas optimizāciju](get-started.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
