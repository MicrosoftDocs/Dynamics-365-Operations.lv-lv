---
title: Bilances finanšu pārskati
description: Šajā rakstā ir aprakstīti noklusējuma pārskati bilancēm. Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64e3624b387820bea3bfea9c2a4b2f48b0aa9822
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189025"
---
# <a name="balance-sheet-financial-reports"></a>Bilances finanšu pārskati

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti noklusējuma pārskati bilancēm. Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki. 

## <a name="default-balance-sheet-reports"></a>Noklusējuma bilances pārskati

Ir divi noklusējuma bilances pārskati. Vienā pārskatā sadaļas ir izvietotas secīgi. Otrā pārskatā sadaļas atrodas blakus.

| Noklusējuma pārskats                       | Ko tā dara                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Bilance — noklusējums              | Sniedz pārskatu par organizācijas finanšu pozīciju attiecībā uz gadu.                                                                 |
| Līdzās atvērta bilance — noklusējums | Sniedz pārskatu par organizācijas finanšu pozīciju attiecībā uz gadu. Līdzās tiek rādīti aktīvi un saistības, kā arī akcionāru kapitāls. |

## <a name="building-blocks"></a>Veidošanas bloki
Bilances finanšu pārskati izmanto tālāk aprakstītos veidošanas blokus.

| Noklusējuma atskaite                       | Rindas definīcija                       | Kolonnas definīcija             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Bilance — noklusējums              | Bilance — noklusējums              | Šī gada un novirzes - noklusējuma    |
| Līdzās atvērta bilance — noklusējums | Līdzās atvērta bilance — noklusējums | Šī gada kolonna - noklusējuma |

### <a name="row-definition"></a>Rindas definīcija

Rindas definīcijas abiem bilances pārskatiem satur sadaļas, kas atbilst katrai tradicionālās bilances daļai. Blakus izvietojuma pārskatā iekļauti kolonnu pārtraukumi, tādējādi saistības un īpašnieka kapitāls tiek attēloti līdzās aktīviem. Abu rindu definīciju izveidē tiek izmantota galvenā konta kategorijas dimensija. Tāpēc ikviens var ģenerēt pārskatus bez nepieciešamības veikt modifikācijas.

### <a name="column-definition"></a>Kolonnas definīcija

Kolonnu definīcijas satur dažādu veidu kolonnas, lai sniegtu dažāda līmeņa detaļas un finanšu datus.

-   **Šī gada un novirzes – noklusējuma kolonnu tipi**
    -   **DESC** — apraksts no rindas definīcijas.
    -   **FD** — finanšu dati par šo gadu līdz šim brīdim.
    -   **FD** — finanšu dati par pagājušo gadu.
    -   **CALC** — novirze, atņemot pagājušajā gada summas no šī gada summām.

<!-- -->

-   **Šī gada kolonna — noklusējuma**
    -   **DESC** — apraksts no rindas definīcijas.
    -   **FD** — finanšu dati par šo gadu līdz šim brīdim.



## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskatu veidošanas apskats](financial-reporting-getting-started.md)

[Finanšu pārskatu skatīšana](view-financial-reports.md)

[Dynamics finanšu pārskatu veidošanas emuārs](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]