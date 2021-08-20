---
title: Vienota darbu ID numuru secība
description: Šī funkcija nodrošina vienu unificētu numuru sēriju, kas ģenerē ražošanas kontroles, ražošanas izpildes, laika un apmeklētības moduļu darbu ID numurus.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8ff8fae0bb20b11b15c7520fbb14727ff0372ca0255adc82599c6680a64671af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748719"
---
# <a name="unified-number-sequence-for-job-ids"></a>Vienota darbu ID numuru secība

[!include [banner](../includes/banner.md)]

Šī funkcija nodrošina vienu unificētu numuru sēriju, kas ģenerē ražošanas kontroles, ražošanas izpildes, laika un apmeklētības moduļu darbu ID numurus. Iepriekš var izvēlēties atšķirīgu numuru sēriju katram no šiem moduļiem, kas var izraisīt konfliktējošus darba ID numurus, ja divas vai vairākas šīs sērijas izmantoja identisku formātu. Šāds konflikts var izraisīt datu bojāšanu.

## <a name="turn-on-this-feature-for-your-system"></a>Līdzekļa ieslēgšana sistēmā

Ja sistēmā vēl nav ietverti šajā tēmā aprakstītie līdzekļi, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet līdzekli *Krājumu darbību arhīvs*.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Vienota darbu ID numuru secības iestatīšana

Pēc šīs funkcijas iespējošanas esošie **Darba identifikācijas** numuru sērijas iestatījumi, kas atrodas ražošanas kontroles, ražošanas izpildes un laika un apmeklētības moduļu parametru lapās, tiks noņemti un tiks pievienots jauns **Unificētais darba ID** lauks. **Unificētā darba ID** vērtība tiek koplietota ar visiem trim moduļiem, tādējādi nodrošinot, ka visi moduļi atsaucas uz vienu un to pašu numuru sēriju. Tāpēc darba ID būs unikāls visos trīs moduļos, un konflikts nekad nebūs.

Vienota darbu ID numuru secības iestatīšana:

1. Iespējojiet funkciju tā, kā tas ir aprakstīts iepriekšējā sadaļā.
1. Vai nu identificējiet numuru secību, ko vēlaties izmantot saviem vienotajam darba ID, vai izveidojiet jaunu. Plašāku informāciju par numuru secību skatiet [Numuru sērijas pārskats](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Pārejiet uz lapu **Ražošanas kontroles parametri**, **Ražošanas izpildes parametri** vai **Laika un apmeklējuma parametri**. Nav svarīgi, kuru vēlaties, jo, veicot šo iestatījumu jebkurā no šīm lapām, visas pārējās lapas tiks atjauninātas automātiski.
1. Atveriet cilni **Numuru sērijas** atlasītajā parametru lapā.
1. Piešķiriet **Numuru sērijas kodu**, kuru iepriekš identificējāt **Unificētā darba ID** režģa rindai.
