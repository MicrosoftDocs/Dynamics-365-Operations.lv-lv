---
title: "Peļņas vai zaudējumu aprēķina finanšu pārskats"
description: "Šajā rakstā ir aprakstīts peļņas vai zaudējumu aprēķina noklusējuma pārskats. Tajā ir aprakstīti arī ar šo pārskatu saistītie veidošanas bloki."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8dd289c1943afb55373ba682afcc3cd107cb67a7
ms.lasthandoff: 03/31/2017


---

# <a name="income-statement-financial-report"></a>Peļņas vai zaudējumu aprēķina finanšu pārskats

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts peļņas vai zaudējumu aprēķina noklusējuma pārskats. Tajā ir aprakstīti arī ar šo pārskatu saistītie veidošanas bloki. 

<a name="default-income-statement-report"></a>Noklusējuma peļņas vai zaudējumu aprēķina pārskats
-------------------------------

| Noklusējuma pārskats             | Ko tā dara                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Peļņas vai zaudējumu aprēķins — noklusējums | Sniedz organizācijas ienesīguma pārskatu pašreizējam periodam un arī šim gadam. |

## <a name="building-blocks"></a>Veidošanas bloki
Peļņas vai zaudējumu aprēķina finanšu pārskats izmanto tālāk aprakstītos veidošanas blokus.

| Noklusējuma atskaite             | Rindas definīcija                     | Kolonnas definīcija          |
|----------------------------|------------------------------------|----------------------------|
| Peļņas vai zaudējumu aprēķins — noklusējums | Kopsavilkuma peļņas vai zaudējumu aprēķins — noklusējums | Periodisks un šī gada - noklusējuma |

### <a name="row-definition"></a>Rindas definīcija

Rindas definīcijā "kopsavilkuma peļņas vai zaudējumu aprēķins — noklusējuma" iekļauta sadaļa katrai tradicionālā aprēķina daļai. Šīs rindas definīcijas izveidē tiek izmantota galvenā konta kategorijas dimensija. Tāpēc ikviens var ģenerēt pārskatu bez nepieciešamības veikt modifikācijas.

### <a name="column-definition"></a>Kolonnas definīcija

Kolonnu definīcijas satur dažādu veidu kolonnas, lai sniegtu dažāda līmeņa detaļas un finanšu datus.

-   **Periodisks un šī gada – noklusējuma kolonnu tipi**
    -   **DESC** — apraksts no rindas definīcijas.
    -   **FD** — finanšu dati par pašreizējo periodu.
    -   **FD** — finanšu dati par šo gadu.

 

<a name="see-also"></a>Skatiet arī
--------

[Finanšu pārskati](financial-reporting-getting-started.md)

[Finanšu pārskatu skatīšana](view-financial-reports.md)

[Dynamics finanšu pārskatu emuārs](http://blogs.msdn.com/b/dynamics_financial_reporting/)




