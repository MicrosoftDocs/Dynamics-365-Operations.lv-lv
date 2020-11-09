---
title: Transportēšanas pārvaldības pārskats
description: Šajā tēmā ir sniegts apskats par zvanu transportēšanas pārvaldības funkcionalitāti Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4affc5846ee329a4571d6fb3e0c42873387241ad
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016382"
---
# <a name="transportation-management-overview"></a>Transportēšanas pārvaldības pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts apskats par zvanu transportēšanas pārvaldības funkcionalitāti Supply Chain Management.

Transportēšanas pārvaldība jums ļauj lietot jūsu uzņēmuma transportēšanu, kā arī ļauj identificēt kreditoru un maršrutēšanas risinājumus ienākošiem un izejošiem pasūtījumiem. Piemēram, var norādīt ātrāko ceļu vai vislētāko sūtījuma likmi. Šajā tabulā ir aprakstīti galvenie scenāriji attiecībā uz moduļa Transportēšanas pārvaldība lietošanu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenārijs</th>
<th>Transportēšanas pārvaldības sniegtās iespējas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izmantojiet ārējos loģistikas pakalpojumu sniedzējus transportēšanas darbībām.</td>
<td>Izmantojiet transportēšanas pārvaldību ienākošajai un izejošajai transportēšanai.</td>
</tr>
<tr class="even">
<td>Paša uzņēmum&#39;a autoparks ir pieejams piegādei/saņemšanai, un piegādes maksas tiek nodotas debitoriem.</td>
<td>Izejošajiem procesiem transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas maksas un nodotu tās debitoriem. Tomēr na&#39;v nepieciešams pārvadātāja rēķina saskaņošanas process.</td>
</tr>
<tr class="odd">
<td>Paša uzņēmum&#39;a autoparks ir pieejams piegādei/saņemšanai, taču piegādes maksas netie&#39;k nodotas debitoriem, jo preču cenās ir iekļauta transportēšana.</td>
<td>Liela daļa transportēšanas pārvaldības funkcionalitātes na&#39;v nepieciešama. Tomēr transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas likmes un attiecīgi pielāgotu pārdošanas cenu.</td>
</tr>
<tr class="even">
<td>Loģistikas pakalpojumus sniedz cita juridiska persona tajā pašā uzņēmumā.</td>
<td><ul>
<li>Transportēšanas pārvaldību var izmantot, veicot darbības ar citu juridisku personu tāpat kā ar jebkuru citu sūtījumu pārvadātāju. Ekonomiskās darbības starp juridiskajām personām neva&#39;r automatizēt. Tādēļ jums jāapstrādā šīs darbības manuāli (piemēram, izveidojot pirkšanas pasūtījumu).</li>
<li>Juridiskajā personā, kas nodrošina loģistikas pakalpojumus, transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas likmes.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>Transportēšanas plānošana Supply Chain Management
Modulī Transportēšanas pārvaldība transportēšanas plānošanu var balstīt uz pasūtījumiem vai uz sūtījumiem, kuri izveidoti, pamatojoties uz šiem pasūtījumiem. Sūtījumi vienmēr pastāv kādā noteiktā brīdī, bet nav nepieciešami transportēšanas plānošanai. Pārsūtīšanas pasūtījumi ir daļa no izejošās plūsmas scenārija, un tos var plānot kopā ar pārdošanas pasūtījumiem. 

![Zīmējuma ielāde](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Ienākošā transportēšana
Ja pasūtat preces pie kreditora, un tās ir jāpiegādā uz jūsu noliktavu, ieteicams pašiem organizēt transportu preču pārvešanai. Pārvešanas plānošanai un ienākošās kravas saņemšanai varat izmantot programmatūru Supply Chain Management. Tālāk redzamajā attēlā ir attēlota biznesa procesa plūsma attiecībā uz ienākošas kravas transportēšanu. 

![Biznesa procesa plūsma ienākošo kravu transportēšanai](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Izejošā transportēšana
Var plānot un apstrādāt izejošo kravu, lai nosūtītu noteiktus krājumus no uzņēmuma noliktavas debitoram. Pārvešanas plānošanai un izejošās kravas sūtīšanai varat izmantot programmatūru Supply Chain Management. Tālāk ir paskaidrota nosūtīšanas izejošo noslodžu plānošanas un apstrādes biznesa procesa plūsma. 

![Izejošo kravu plānošana un apstrāde](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Noslodzes plānošana
Programmatūra Supply Chain Management nodrošina noslodzes plānošanas stratēģiju, kuras nosaukums ir Uz apjomu balstīta noslodzes plānošanas stratēģija. Šī stratēģija ļauj izmantot maksimālās vērtības, kuras ir norādītas garumam un svaram noslodzes veidnē, vai arī iestatījumus var ignorēt, ievadot jaunas vērtības. Lai izmantotu šo stratēģiju, atlasiet to laukā **Noslodzes plānošanas stratēģija** kopsavilkuma cilnē **Iestatījumi** lapā **Noslodzes plānošanas rīks**. Turklāt var pievienot savas noslodzes plānošanas stratēģijas, izveidojot jaunu klasi lietojumprogrammas objektu kokā (AOT).



