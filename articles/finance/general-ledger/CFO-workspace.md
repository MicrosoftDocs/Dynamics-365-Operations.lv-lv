---
title: Pievienot finanšu dimensijas CFO darbvietai
description: Šajā rakstā ir skaidrots, kā pievienot finanšu dimensijas CFO darbvietai, lai tās varētu izmantot Virsgrāmatas un budžeta pārskatiem.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ea453eed826dec2e97371ec559e91b94933bdce6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853385"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Pievienot finanšu dimensijas CFO darbvietai

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā finanšu dimensijas pievienot finanšu direktors (CFO) darbvietai, lai tās varētu izmantot Virsgrāmatas un budžeta pārskatiem. CFO darbvietā ir cilne **Apskats** un cilne **Finanšu**. Abās šajās cilnēs pieejamos pārskatus nodrošina divi mēri: LedgerActivityMeasure un BudgetActivityMeasure. Pastāv relācija starp šiem diviem mēriem un elementu DimensionCombinationEntity. Tādējādi var atlasīt dimensijas.

1. Finance lapā **Elementu krātuve** atjauniniet **LedgerActivityMeasure** un **BudgetActivityMeasure** mērus.
2. Programmā Microsoft Visual Studio atveriet lietojumprogrammu pārlūku un meklējiet **LedgerCFO**.
3. Sadaļā **Resursi** atveriet **LedgerCFOWorkspacePBIX**.
4. Kad Microsoft Power BI Desktop tiek atvērts resurss, atlasiet **Iegūt datus**, atlasiet **SQL servera datu bāze** un pēc tam atlasiet **Pieslēgties**.
5. Ievadiet servera nosaukumu un ievadiet **AxDW** kā datu bāzi. Atlasiet **DirectQuery** un pēc tam **Labi**.
6. Meklējiet un atlasiet **LedgerActivityMeasure\_DimensionCombination** un pēc tam atlasiet **Ielādēt**.

    > [!TIP]
    > Laukā **Lauki** pārdēvējiet tabulu **Finanšu dimensijas** tā, lai to būtu viegli identificēt.

7. Atlasiet **Pārvaldīt relācijas** un pēc tam atlasiet **Jauns**.
8. Pirmajā laukā atlasiet **Virsgrāmatas aktivitātes** un pēc tam atlasiet **LedgerDimension**.
9. Otrajā laukā atlasiet **LedgerActivityMeasure\_DimensionCombination** (vai **Finanšu dimensijas**, ja pārdēvējāt tabulu). Atlasiet virsrakstu  **DimensionCombinationRECID**.
10. Laukā **Kardinalitāte** atlasiet **Daudzi pret vienu**.
11. Mainiet vērtību **Krusteniskās filtrēšanas virziens** uz **Viens**.
12. Atlasiet gan **Aktivizēt šo relāciju**, gan **Pieņemt atsauces integritāti**, atlasiet **Labi** un pēc tam atlasiet **Aizvērt**.

    [![Relācijas izveide.](./media/Create-relationship.png)](./media/Create-relationship.png)

13. Laukā **Lauki** tiek rādīta tabula un pieejamās finanšu dimensijas. Velciet nepieciešamās finanšu dimensijas uz pārskata līmeņa filtriem.
14. Saglabājiet izmaiņas.
15. Lietojumprogrammas objektu kokā (AOT) ar peles labo pogu noklikšķiniet uz projekta un pēc tam atlasiet **Sinhronizēt**.
16. Izveidojiet projektu un pēc tam atveriet lietojumprogrammu, lai skatītu rezultātus.

    [![Izpildīta darbvieta.](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
