---
title: Projektam paredzēti pirkšanas pasūtījumi
description: Šajā rakstā ir aprakstītas dažādas metodes, ko var izmantot, lai izveidotu projektam paredzētus pirkšanas pasūtījumus. Izmantojamā metode ir atkarīga no pirkšanas pasūtījuma mērķa, kad iepirktie krājumi tiek patērēti un to izmaksas tiek attiecinātas uz projektu.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174562"
---
# <a name="purchase-orders-for-a-project"></a>Projektam paredzēti pirkšanas pasūtījumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas dažādas metodes, ko var izmantot, lai izveidotu projektam paredzētus pirkšanas pasūtījumus. Izmantojamā metode ir atkarīga no pirkšanas pasūtījuma mērķa, kad iepirktie krājumi tiek patērēti un to izmaksas tiek attiecinātas uz projektu.

### <a name="methods-for-creating-a-purchase-order"></a>Pirkšanas pasūtījuma izveides metodes

Lai izveidotu pirkšanas pasūtījumu projektu vadības un uzskaites modulī, var izmantot vienu no tālāk aprakstītajām metodēm. Pirkšanas pasūtījuma mērķis nosaka, kad pirkšanas pasūtījums tiek izmantots, un, līdz ar to, kad krājumu izmaksas tiek attiecinātas uz projektu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Mērķis</th>
<th>Krājumu patēriņš</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izveidojiet pirkšanas pasūtījumu tieši no projekta.</td>
<td>Izmantojiet šo metodi, lai iegādātos krājumus ārējam kreditoram izmantošanai projektā. Pirkšanas pasūtījumu var izveidot divējādi.
<ul>
<li>No paša projekta. Šajā gadījumā projekts ir jau definēts pirkšanas pasūtījumam.</li>
<li>Pārejot uz projekta pirkšanas pasūtījumu. Jums ir jāizvēlas gan kreditors, gan projekts, kuram veidot pirkšanas pasūtījumu.</li>
</ul></td>
<td>Krājumus izmanto, kad kreditora rēķins tiek atjaunināts.</td>
</tr>
<tr class="even">
<td>Izveidot pirkšanas pasūtījumu no pārdošanas pasūtījuma.</td>
<td>Izmantojiet šo metodi, ja vēlaties pirkt krājumus, veidojot pārdošanas pasūtījumu no projekta.</td>
<td>Krājumus izmanto, kad tiek izveidots pārdošanas pasūtījuma rēķins debitoram.</td>
</tr>
<tr class="odd">
<td>Izveidot pirkšanas pasūtījumu no krājumu vajadzības.</td>
<td>Izmantojiet šo metodi, ja vēlaties pirkt krājumus, izveidojot krājumu vajadzību no projekta.</td>
<td>Krājumus izmanto, atjauninot krājumu vajadzības pavadzīmi.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Kad jaunināt kreditora rēķinu vai pavadzīmi, tiek parādīta uzvedne ar aicinājumu atjaunināt krājumu vajadzības pavadzīmi.

Plašāku informāciju skatiet šeit: [Saņemt pirkšanas pasūtījuma krājumus no krājumu vajadzības](tasks/receive-items-purchase-order-item-requirement.md).
