---
title: Atlaižu pārvaldības darījumu darbplūsmas
description: Šajā tēmā skaidrots, kā iestatīt atlaižu pārvaldības darījuma darbplūsmu, lai apstiprinātu un aktivizētu darījumus.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f18c3bd95901303379c460d026bc944cee809b7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576668"
---
# <a name="rebate-management-deal-workflows"></a>Atlaižu pārvaldības darījumu darbplūsmas

[!include [banner](../includes/banner.md)]

Lai apstiprinātu atlaižu darījumus, atlaižu pārvaldība izmanto to pašu darbplūsmas platformu, ko citas Finance and Operations lietojumprogrammas. Divi darba procesi ir saistīti ar katru darbplūsmu:

- Viens darbplūsmas elements apstiprina darījumu.
- Viens darbplūsmas elements aktivizē darījumu, lai lietotājs vai darbplūsmas process varētu apstiprināt darbības.

Pirms atlaides darījuma izmantošanas tam jābūt aktīvam **Atlaižu pārvaldības** modulī. Lai aktivizētu darījumu, vispirms ir jāizveido un jākonfigurē *Atlaižu pārvaldības darījuma darbplūsma*.

Lietotāji nevar manuāli apstiprināt darījumus. Darbplūsma vienmēr ir jāizmanto.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Izveidot un pārvaldīt atlaižu pārvaldības darījumu darbplūsmas

Lai strādātu ar Atlaižu pārvaldības darījumu darbplūsmām, dodieties uz **Atlaižu pārvaldība \> Iestatījumi \> Atlaižu pārvaldības darbplūsmas**. Tur varat skatīt, izveidot un atjaunināt darbplūsmas pēc vajadzības. KVienlaicīgi var būt aktīvs tikai viens darbplūsmas veids. Papildinformāciju par darbplūsmām, kā strādāt ar **Atlaižu pārvaldības darbplūsmu** lapu un kā izveidot darbplūsmas, skatiet [Darbplūsmas sistēmas pārskats](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) un ar to saistītās tēmas.

## <a name="use-a-workflow-to-activate-a-deal"></a>Izmantojiet darbplūsmu, lai aktivizētu darījumu

Lai aktivizētu darījumu, izmantojot darbplūsmu, atveriet darījumu (piemēram, lapā **Visi atlaižu pārvaldības darījumi** ). Darbību rūtī atlasiet **Darbplūsma \> Iesniegt**. Kad jaunais darījums darbplūsmā ir apstrādāts un apstiprināts, tas būs aktīvs un gatavs lietošanai.

Pēc darījuma aktivizēšanas lielāko tās iestatījumu daļu nevar mainīt. Ja jums ir jāmaina aktīvs darījums, vispirms deaktivizējiet to un tad izveidojiet jaunu darījumu. Ja jaunais darījums būs līdzīgs vecajam darījumam, to var izveidot, kopējot veco darījumu.

Jūs varat mainīt sekojošos iestatījumus darījumam pēc tā aktivizēšanas:

- Saskaņot pēc
- Kumulatīvā garantija
- Grāmatošanas metode
- Garantijas grāmatošanas profils
- Dokumentu piezīmes
- Valūta
- No datuma
- Līdz datumam

Turklāt atlaides rindas var noņemt.
