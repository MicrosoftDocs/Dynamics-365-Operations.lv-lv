---
title: Pakalpojuma statusa un progresa lauka mijiedarbība
description: Formā Pakalpojumu pasūtījumi lauks Progress galvenē atspoguļo visa pakalpojuma pasūtījuma statusu, un vērtība Statuss ziņo par atsevišķu pakalpojuma pasūtījuma rindu statusu.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207328"
---
# <a name="service-status-and-progress-field-interaction"></a>Pakalpojuma statusa un progresa lauka mijiedarbība 

[!include [banner](../includes/banner.md)]


Formā **Pakalpojumu pasūtījumi** lauks **Progress** pakalpojuma pasūtījuma galvenē atspoguļo visa pakalpojuma pasūtījuma statusu, un vērtība **Statuss** ziņo par atsevišķu pakalpojuma pasūtījuma rindu statusu.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Progress</p></th>
<th><p>1. rindas statuss</p></th>
<th><p>2. rindas statuss</p></th>
<th><p>3. rindas statuss</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Notiek</strong></p></td>
<td><p><strong>Izveidots</strong></p></td>
<td><p><strong>Izveidots</strong></p></td>
<td><p><strong>Izveidots</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Notiek</strong></p></td>
<td><p><strong>Atcelts</strong></p></td>
<td><p><strong>Izveidots</strong></p></td>
<td><p><strong>Izveidots</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Notiek</strong></p></td>
<td><p><strong>Izveidots</strong></p></td>
<td><p><strong>Atcelts</strong></p></td>
<td><p><strong>Grāmatots</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Atcelts</strong></p></td>
<td><p><strong>Atcelts</strong></p></td>
<td><p><strong>Atcelts</strong></p></td>
<td><p><strong>Atcelts</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Grāmatots</strong></p></td>
<td><p><strong>Grāmatots</strong></p></td>
<td><p><strong>Grāmatots</strong></p></td>
<td><p><strong>Grāmatots</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Grāmatots</strong></p></td>
<td><p><strong>Grāmatots</strong></p></td>
<td><p><strong>Atcelts</strong></p></td>
<td><p><strong>Atcelts</strong></p></td>
</tr>
</tbody>
</table>


Pakalpojuma pasūtījuma progress vēl notiek, ja visām rindām ir statuss **Izveidots**; tas joprojām notiek, ja dažām no rindām ir statuss **Atcelts** vai **Grāmatots**.

Ja visas rindas pakalpojuma pasūtījumā ir atzīmētas kā **Grāmatots**, statusa pasūtījuma progress ir **Grāmatots**. Ja dažu rindu statuss ir **Grāmatots** un dažu rindu statuss ir **Atcelts**, progress joprojām ir **Grāmatots**.

  


