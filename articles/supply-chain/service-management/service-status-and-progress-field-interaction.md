---
title: Pakalpojuma statusa un progresa lauka mijiedarbība
description: Formā Pakalpojumu pasūtījumi lauks Progress galvenē atspoguļo visa pakalpojuma pasūtījuma statusu, un vērtība Statuss ziņo par atsevišķu pakalpojuma pasūtījuma rindu statusu.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0758c370fd1548770d596115b18f133071f3bbc0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566099"
---
# <a name="service-status-and-progress-field-interaction"></a>Pakalpojuma statusa un progresa lauka mijiedarbība

[!include [banner](../includes/banner.md)]

Formā **Pakalpojumu pasūtījumi** lauks **Progress** pakalpojuma pasūtījuma galvenē atspoguļo visa pakalpojuma pasūtījuma statusu, un vērtība **Statuss** ziņo par atsevišķu pakalpojuma pasūtījuma rindu statusu.

<table>
<colgroup>
<col />
<col />
<col />
<col />
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
