---
title: Uzturēšanas pieprasījumi
description: Šajā tēmā sniegts pārskats par uzturēšanas pieprasījumu pārvaldību Līdzekļu pārvaldībā
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e973dfe9a0ae290efbdf04a73854269ed371cea26af9d161ea5dc15027eda4ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773637"
---
# <a name="maintenance-requests"></a>Uzturēšanas pieprasījumi

[!include [banner](../../includes/banner.md)]

Uzturēšanas pieprasījumi ir piezīmes vai deklarācijas, kas izveidotas, lai paziņotu vadītājam vai plānotājam, ka līdzeklim var būt nepieciešams uzturēšanas vai labošanas darbs, taču neveidojot darba pasūtījumu. Ja uzturēšanas pieprasījuma saturs tiek uzskatīts par derīgu, pēc tam var izveidot darba pasūtījumu, pamatojoties uz uzturēšanas pieprasījumu.

Uzturēšanas pieprasījumus var izveidot jebkuram līdzeklim Līdzekļu pārvaldībā. Atkarībā no tā, kā jūsu uzņēmums izmanto uzturēšanas pieprasījumus, var izveidot dažādus uzturēšanas pieprasījumu veidus. Daži piemēri:

- Uzturēšanas pieprasījumi
- Piezīmes
- Labojumi vai uzlabojumi
- Investīcijas
- Labošana noliktavā (Šis veids tiek izmantots, ja saņemat līdzekļus no citas atrašanās vietas, lai varētu veikt uzturēšanas vai labošanas darbu, un pēc tam atgriežat līdzekli, kad darbs ir pabeigts.)

## <a name="view-maintenance-requests"></a>Skatīt uzturēšanas pieprasījumus

Lai skatītu uzturēšanas pieprasījumus, atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Visi uzturēšanas pieprasījumi**, **Aktīvie ctive uzturēšanas pieprasījumi** vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**. Katrā saraksta lapā ir redzama daļa no informācijas, kas saistīta ar uzturēšanas pieprasījumu.

![Skatīt uzturēšanas pieprasījumus.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Izmantojiet saraksta lapu **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**, lai skatītu uzturēšanas pieprasījumu sarakstu, kas ietver vai nu funkcionālos novietojumus, ar kuriem esat saistīts kā darbinieks vai līdzekļus, kas ir uzstādīti funkcionālajos novietojumos, ar kuriem esat saistīts kā darbinieks. (Informāciju par to, kā iestatīt funkcionālos novietojumus uzturēšanas darbiniekiem, skatiet sadaļā [Uzturēšanas darbinieki un darbinieku grupas](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Kaut arī debitora konta informācija ir pieejama Līdzekļu pakalpojumu pārvaldībā (ārējā uzturēšana), tā nav pieejama Līdzekļu pārvaldībā (iekšējā uzturēšana).

Lai atvērtu ieraksta detalizētu skatu saraksta lapā **Visi uzturēšanas pieprasījumu**, režģa skatā atlasiet saiti kolonnā **Uzturēšanas pieprasījums**.

![Skatīt detalizēto informāciju par uzturēšanas pieprasījumu.](media/02-manage-maintenance-requests.png)

Pogas darbības rūtī ir sakārtotas cilnēs. Nākamajā tabulā ir īsi aprakstītas pogas, kas saistītas ar Līdzekļu pārvaldību.

| Pogas nosaukums                      | Apraksts |
|----------------------------------|-------------|
| Labot                             | Rediģēt atlasīto uzturēšanas pieprasījumu. |
| Jauna                              | Izveidot jaunu uzturēšanas pieprasījumu. |
| Dzēst                           | Dzēst atlasīto uzturēšanas pieprasījumu. |
| Darba pasūtījumu kopa                  | Pievienojiet atlasīto uzturēšanas pieprasījumu darba pasūtījumu kopai. |
| Darba pasūtījums                       | Izveidojiet darba pasūtījumu, pamatojoties uz atlasīto uzturēšanas pieprasījumu. |
| Līdzekļa defekts                      | Noklikšķiniet uz **Līdzekļa defekti**, kur varat izveidot defektu reģistrāciju atlasītajā uzturēšanas pieprasījumā. |
| Darba pasūtījumi                      | Parādīt sarakstu ar visiem darba pasūtījumiem, kas ir saistīti ar atlasīto uzturēšanas pieprasījumu. |
| Uzturēšanas pieprasījuma stāvokļa atjaunināšana | Atjauniniet uzturēšanas pieprasījuma stāvokli. |
| Dzīves cikla stāvokļa žurnāls              | Skatiet žurnālu, kas rāda atlasītā uzturēšanas pieprasījuma dzīves cikla stāvokļus. |
| Detalizēta informācija par uzturēšanas pieprasījumu      | Izdrukājiet pārskatu, kas rāda detalizētu informāciju par atlasīto uzturēšanas pieprasījumu. |
| Patapinājuma līdzekļa nosūtīšana                  | Atlasiet patapinājuma līdzekli, kam vajadzētu būt pagaidu aizstājējam līdzeklim, kurš atlasīts atlasītajā uzturēšanas pieprasījumā. |
| Patapinājuma līdzekļa atgriešana                | Reģistrējiet patapinājuma līdzekli kā atgrieztu. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]