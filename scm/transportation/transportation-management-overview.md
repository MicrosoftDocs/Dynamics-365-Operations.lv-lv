---
title: "Transportēšanas pārvaldības pārskats"
description: "Šajā tēmā ir sniegts apskats par transportēšanas pārvaldības funkcionalitāti programmā Microsoft Dynamics 365 for Operations."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3136fd95c4c56495a391668d6c854a6ae1e36479
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-overview"></a>Transportēšanas pārvaldības pārskats

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegts apskats par transportēšanas pārvaldības funkcionalitāti programmā Microsoft Dynamics 365 for Operations.

Transportēšanas pārvaldība ļauj pārvaldīt jūsu uzņēmuma transportēšanu un arī ļauj noteikt piegādātāja un maršrutēšanas risinājumus ienākošiem un izejošiem pasūtījumiem. Piemēram, var norādīt ātrāko ceļu vai vislētāko sūtījuma likmi. Nākamajā tabulā ir aprakstīti galvenie scenāriji attiecībā uz moduļa Transportēšanas pārvaldība lietošanu programmā Microsoft Dynamics 365 for Operations.

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
<td>Paša uzņēmuma autoparks ir pieejams piegādei/saņemšanai, un piegādes maksas tiek nodotas debitoriem.</td>
<td>Izejošajiem procesiem transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas maksas un nodotu tās debitoriem. Tomēr nav nepieciešams pārvadātāja rēķina saskaņošanas process.</td>
</tr>
<tr class="odd">
<td>Paša uzņēmuma autoparks ir pieejams piegādei/saņemšanai, taču piegādes maksas netiek nodotas debitoriem, jo preču cenās ir iekļauta transportēšana.</td>
<td>Liela daļa transportēšanas pārvaldības funkcionalitātes nav nepieciešama. Tomēr transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas likmes un attiecīgi pielāgotu pārdošanas cenu.</td>
</tr>
<tr class="even">
<td>Loģistikas pakalpojumus sniedz cita juridiska persona tajā pašā uzņēmumā.</td>
<td><ul>
<li>Transportēšanas pārvaldību var izmantot, veicot darbības ar citu juridisku personu tāpat kā ar jebkuru citu sūtījumu pārvadātāju. Ekonomiskās darbības starp juridiskajām personām nevar automatizēt. Tādēļ jums jāapstrādā šīs darbības manuāli (piemēram, izveidojot pirkšanas pasūtījumu).</li>
<li>Juridiskajā personā, kas nodrošina loģistikas pakalpojumus, transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas likmes.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-dynamics-365-for-operations"></a>Transporta plānošana programmā Dynamics 365 for Operations
Modulī Transportēšanas pārvaldība transportēšanas plānošanu var balstīt uz pasūtījumiem vai uz sūtījumiem, kuri izveidoti, pamatojoties uz šiem pasūtījumiem. Sūtījumi vienmēr pastāv kādā noteiktā brīdī, bet nav nepieciešami transportēšanas plānošanai. Pārsūtīšanas pasūtījumi ir daļa no izejošās plūsmas scenārija, un tos var plānot kopā ar pārdošanas pasūtījumiem. 

![Zīmējuma ielāde](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Ienākošā transportēšana
Ja pasūtat preces pie kreditora, un tās ir jāpiegādā uz jūsu noliktavu, ieteicams pašiem organizēt transportu preču pārvešanai. Pārvešanas plānošanai un ienākošās kravas saņemšanai varat izmantot programmu Dynamics 365 for Operations. Tālāk redzamajā attēlā ir attēlota biznesa procesa plūsma attiecībā uz ienākošas kravas transportēšanu. 

![Biznesa procesa plūsma ienākošo kravu transportēšanai](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Izejošā transportēšana
Var plānot un apstrādāt izejošo kravu, lai nosūtītu noteiktus krājumus no uzņēmuma noliktavas debitoram. Programmu Dynamics 365 for Operations varat izmantot, lai plānotu izejošo kravu transportēšanu un nosūtīšanu. Tālāk ir paskaidrota nosūtīšanas izejošo noslodžu plānošanas un apstrādes biznesa procesa plūsma. 

![Izejošo kravu plānošana un apstrāde](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Noslodzes plānošana
Programma Dynamics 365 for Operations nodrošina noslodzes plānošanas stratēģiju, kuras nosaukums ir Uz apjomu balstīta noslodzes plānošanas stratēģija. Šī stratēģija ļauj izmantot maksimālās vērtības, kuras ir norādītas garumam un svaram noslodzes veidnē, vai arī iestatījumus var ignorēt, ievadot jaunas vērtības. Lai izmantotu šo stratēģiju, atlasiet to laukā **Noslodzes plānošanas stratēģija** kopsavilkuma cilnē **Iestatījumi** lapā **Noslodzes plānošanas rīks**. Turklāt var pievienot savas noslodzes plānošanas stratēģijas, izveidojot jaunu klasi lietojumprogrammas objektu kokā (AOT).




