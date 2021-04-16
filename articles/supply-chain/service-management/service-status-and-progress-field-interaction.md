---
title: Pakalpojuma statusa un progresa lauka mijiedarbība
description: Formā Pakalpojumu pasūtījumi lauks Progress galvenē atspoguļo visa pakalpojuma pasūtījuma statusu, un vērtība Statuss ziņo par atsevišķu pakalpojuma pasūtījuma rindu statusu.
author: ShylaThompson
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
ms.openlocfilehash: a767f4fddb79e720e5466791e984025de16a932a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824466"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]