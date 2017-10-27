---
title: "Pievienot finanšu dimensijas CFO darbvietai"
description: "Šajā tēmā izskaidrots, kā CFO darbvietai pievienot finanšu dimensijas, lai tās varētu izmantot virsgrāmatas un budžeta pārskatos."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e674948f642ab7525f96092a9a1f3adaae66974
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Pievienot finanšu dimensijas CFO darbvietai

[!include[banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā finanšu direktora (CFO) darbvietai pievienot finanšu dimensijas, lai tās varētu izmantot virsgrāmatas un budžeta pārskatos. CFO darbvietā ir cilne **Apskats** un cilne **Finanšu**. Abās šajās cilnēs pieejamos pārskatus nodrošina divi mēri: LedgerActivityMeasure un BudgetActivityMeasure. Programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs) pastāv relācija starp šiem diviem mēriem un elementu DimensionCombinationEntity. Tādējādi var atlasīt dimensijas.

1. Finance and Operations lapā **Elementu krātuve** atjauniniet **LedgerActivityMeasure** un **BudgetActivityMeasure** mērus.
2. Microsoft Visual Studio atveriet programmu Lietojumprogrammas pārlūks un meklējiet **LedgerCFO**.
3. Sadaļā **Resursi** atveriet **LedgerCFOWorkspacePBIX**.
4. Kad resurss tiek atvērts Microsoft Power BI darbvirsmā, atlasiet **Iegūt datus**, atlasiet **SQL Server datu bāze** un pēc tam atlasiet **Izveidot savienojumu**.
5. Ievadiet servera nosaukumu un ievadiet **AxDW** kā datu bāzi. Atlasiet **DirectQuery** un pēc tam **Labi**.
6. Meklējiet un atlasiet **LedgerActivityMeasure\_DimensionCombination** un pēc tam atlasiet **Ielādēt**.

    > [!TIP]
    > Laukā **Lauki** pārdēvējiet tabulu **Finanšu dimensijas** tā, lai to būtu viegli identificēt.

7. Atlasiet **Pārvaldīt relācijas** un pēc tam atlasiet **Jauns**.
8. Pirmajā laukā atlasiet **Virsgrāmatas aktivitātes** un pēc tam atlasiet **LedgerDimension**.
9. Otrajā laukā atlasiet **LedgerActivityMeasure\_DimensionCombination** (vai **Finanšu dimensijas**, ja pārdēvējāt tabulu). Atlasiet virsrakstu **DimensionCombinationRECID**.
10. Laukā **Kardinalitāte** atlasiet **Daudzi pret vienu**.
11. Mainiet vērtību **Krusteniskās filtrēšanas virziens** uz **Viens**.
12. Atlasiet gan **Aktivizēt šo relāciju**, gan **Pieņemt atsauces integritāti**, atlasiet **Labi** un pēc tam atlasiet **Aizvērt**.

    [![Relācijas izveide](./media/Create-relationship.png)](./media/Create-relationship.png)

13. Laukā **Lauki** tiek rādīta tabula un pieejamās finanšu dimensijas. Velciet nepieciešamās finanšu dimensijas uz pārskata līmeņa filtriem.
14. Saglabājiet izmaiņas.
15. Lietojumprogrammas objektu kokā (AOT) ar peles labo pogu noklikšķiniet uz projekta un pēc tam atlasiet **Sinhronizēt**.
16. Izveidojiet projektu un pēc tam atveriet lietojumprogrammu, lai skatītu rezultātus.

    [![Izpildīta darbvieta](./media/workspace.png)](./media/workspace.png)
