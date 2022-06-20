---
title: Atlaižu pārvaldības darījumu darbplūsmas
description: Šajā rakstā ir izskaidrots, kā iestatīt atlaižu pārvaldības darījuma darbplūsmu, lai apstiprinātu un aktivizētu darījumus.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2b1611ff7877efc4a2f98b8f84a1ef91971902ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869522"
---
# <a name="rebate-management-deal-workflows"></a>Atlaižu pārvaldības darījumu darbplūsmas

[!include [banner](../includes/banner.md)]

Lai apstiprinātu atlaižu darījumus, atlaižu pārvaldība izmanto to pašu darbplūsmas platformu, ko citas Finanšu un operāciju programmas. Divi darba procesi ir saistīti ar katru darbplūsmu:

- Viens darbplūsmas elements apstiprina darījumu.
- Viens darbplūsmas elements aktivizē darījumu, lai lietotājs vai darbplūsmas process varētu apstiprināt darbības.

Pirms atlaides darījuma izmantošanas tam jābūt aktīvam **Atlaižu pārvaldības** modulī. Lai aktivizētu darījumu, vispirms ir jāizveido un jākonfigurē *Atlaižu pārvaldības darījuma darbplūsma*.

Lietotāji nevar manuāli apstiprināt darījumus. Darbplūsma vienmēr ir jāizmanto.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Izveidot un pārvaldīt atlaižu pārvaldības darījumu darbplūsmas

Lai strādātu ar Atlaižu pārvaldības darījumu darbplūsmām, dodieties uz **Atlaižu pārvaldība \> Iestatījumi \> Atlaižu pārvaldības darbplūsmas**. Tur varat skatīt, izveidot un atjaunināt darbplūsmas pēc vajadzības. KVienlaicīgi var būt aktīvs tikai viens darbplūsmas veids. Papildinformāciju par darbplūsmām, kā **strādāt** ar atlaižu pārvaldības darbplūsmu lapu un kā izveidot darbplūsmas, skatiet darbplūsmas [sistēmas](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) pārskatā un saistītajos rakstos.

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
