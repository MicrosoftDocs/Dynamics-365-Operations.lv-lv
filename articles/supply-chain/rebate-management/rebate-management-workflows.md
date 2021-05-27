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
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020391"
---
# <a name="rebate-management-deal-workflows"></a>Atlaižu pārvaldības darījumu darbplūsmas

[!include [banner](../includes/banner.md)]

Lai apstiprinātu atlaižu darījumus, atlaižu pārvaldība izmanto to pašu darbplūsmas platformu, ko citas Finance and Operations lietojumprogrammas. Divi darba procesi ir saistīti ar katru darbplūsmu:

- Viens darbplūsmas elements aktivizē darījumu, lai lietotājs vai darbplūsmas process varētu apstiprināt darbības.
- Viens darbplūsmas elements apstiprina darījumu.

Pirms atlaides darījuma izmantošanas tam jābūt aktīvam **Atlaižu pārvaldības** modulī. Lai aktivizētu darījumu, vispirms ir jāizveido un jākonfigurē *Atlaižu pārvaldības darījuma darbplūsma*.

Kad atlaižu pārvaldībai ir aktivizēta darbplūsma, lietotāji darījumus nevar apstiprināt manuāli. Darbplūsma vienmēr ir jāizmanto.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Izveidot un pārvaldīt atlaižu pārvaldības darījumu darbplūsmas

Lai strādātu ar Atlaižu pārvaldības darījumu darbplūsmām, dodieties uz **Atlaižu pārvaldība \> Iestatījumi \> Atlaižu pārvaldības darbplūsmas**. Tur varat skatīt, izveidot un atjaunināt darbplūsmas pēc vajadzības. KVienlaicīgi var būt aktīvs tikai viens darbplūsmas veids. Papildinformāciju par darbplūsmām, kā strādāt ar **Atlaižu pārvaldības darbplūsmu** lapu un kā izveidot darbplūsmas, skatiet [Darbplūsmas sistēmas pārskats](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) un ar to saistītās tēmas.

## <a name="use-a-workflow-to-activate-a-deal"></a>Izmantojiet darbplūsmu, lai aktivizētu darījumu

Lai aktivizētu darījumu, izmantojot darbplūsmu, atveriet darījumu (piemēram, lapā **Visi atlaižu pārvaldības darījumi**). Darbību rūtī atlasiet **Darbplūsma \> Iesniegt**. Kad jaunais darījums darbplūsmā ir apstrādāts un apstiprināts, tas būs aktīvs un gatavs lietošanai.

Pēc darījuma aktivizēšanas tā iestatījumu nevar mainīt. Ja jums ir jāmaina aktīvs darījums, deaktivizējiet to un tad izveidojiet jaunu darījumu. Ja jaunais darījums būs līdzīgs vecajam darījumam, to var izveidot, kopējot veco darījumu.
