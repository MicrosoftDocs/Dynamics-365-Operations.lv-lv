---
title: "Krājumu objekta vērtības"
description: "Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3149edfb54bad12fad043b78d9a6d3a7527f18e1
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-object-values"></a>Krājumu objekta vērtības

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības. 

Jaunā funkcija, kuras nosaukums ir **fiziskais daudzums** ļauj jums apskatīt noteikta krājuma objekta vērtības. 

Izmaksu objekts norāda elementa līmeni, kurā tiek veikta krājumu uzskaite. Plašāku informāciju par izmaksu objektiem skatiet sadaļā [Izmaksu objekti](cost-object.md). 

Lai skatītu noteikta krājumu objekta vērtības, lapā **Izmaksu objekts** noklikšķiniet uz vienuma **Fiziskais daudzums**. Krājumu objekta vērtība tiek aprēķināta tālāk norādītajā veidā. 

Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity 

Nākamajā piemērā ir parādīts, kā tiek aprēķinātas krājumu objekta un izmaksu objekta vērtības. Krājumam A ir reģistrēti divi preču saņemšanas notikumi:

-   1. preces saņemšana: daudzums = 100 gab., summa = $ 1000,00, vieta = 1, noliktava = 11, partijas Nr. = B1
-   2. preces saņemšana: daudzums = 50 gab., summa = $ 800,00, vieta = 1, noliktava = 11, partijas Nr. = B2

Šajā tabulā ir parādīts aprēķinu rezultāts izmaksu objektam. Rezultātu var skatīt lapā **Izmaksu objekts**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekta veids</th>
<th>Krājuma kods</th>
<th>Vieta</th>
<th>Daudzums</th>
<th>Krājumu uzskaites vienība</th>
<th>Vērtība</th>
<th>Vidējās vienības izmaksas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izmaksu objekts</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Gab.</td>
<td><p>$ 1800,00</p></td>
<td><p>$ 12,00</p></td>
</tr>
</tbody>
</table>

Šajā tabulā ir parādīts aprēķinu rezultāts krājumu objektam. Rezultātu var skatīt noklikšķinot uz **Fiziskais daudzums** lapā **Izmaksu objekts**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekta veids</th>
<th>Krājuma kods</th>
<th>Vieta</th>
<th>Noliktava</th>
<th>Paketes Nr.</th>
<th>Daudzums</th>
<th>Krājumu uzskaites vienība</th>
<th>Vērtība</th>
<th>Vidējās vienības izmaksas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Krājumu objekts</td>
<td>A</td>
<td>1</td>
<td>11.</td>
<td>B1</td>
<td>100</td>
<td>Gab.</td>
<td><p>$ 1200,00</p></td>
<td><p>$ 12,00</p></td>
</tr>
<tr class="even">
<td>Krājumu objekts</td>
<td>A</td>
<td>1.</td>
<td>11.</td>
<td>B2</td>
<td>50</td>
<td>Gab.</td>
<td><p>$ 600,00</p></td>
<td><p>$ 12,00</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Skatiet arī
--------

[Izmaksu objekti](cost-object.md)

[Izmaksu ieraksti](cost-entries.md)

[Jaunumi un izmaiņas programmatūrā Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)




