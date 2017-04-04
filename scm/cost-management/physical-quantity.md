---
title: "Krājumu objektu vērtības"
description: "Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Krājumu objektu vērtības

Šajā rakstā ir sniegta informācija par to, kā tiek aprēķinātas krājuma objekta vērtības. 

Jaunā funkcionalitāte, kas saucas * * fiziskais daudzums * * ļauj jums redzēt kādu noteiktu krājumu priekšmetu vērtības. Izmaksu objekts norāda elementa līmeni, kurā tiek veikta krājumu uzskaite. Plašāku informāciju par izmaksu objektiem skatiet sadaļā [Izmaksu objekti](cost-object.md). Lai apskatītu noteiktu krājumu objekta vērtības, noklikšķiniet uz **fiziskais daudzums** par **izmaksu objektam** lapu. Lūk, cik objektu krājumu vērtību aprēķina: krājumu objektu. Vērtība = izmaksu objektam. Vidējā pašizmaksa × krājumu objektu. Šajā piemērā daudzums parāda objektu krājumu un izmaksu objektam vērtības aprēķināšanu. Krājumam A ir reģistrēti divi preču saņemšanas notikumi:

-   Preču saņemšanas 1: daudzums = 100 gab., summa = $1,000.00 vieta = 1, noliktava = 11, sērijas Nr. = B1
-   Preču saņemšanas 2: daudzums = 50 gab., summa = $800.00 vieta = 1, noliktava = 11, sērijas Nr. = B2

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

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Kādi ir jaunie un mainītie sistēmā Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


