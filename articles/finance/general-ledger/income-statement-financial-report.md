---
title: Peļņas vai zaudējumu aprēķina finanšu pārskats
description: Šajā rakstā ir aprakstīts peļņas vai zaudējumu aprēķina noklusējuma pārskats. Tajā ir aprakstīti arī ar šo pārskatu saistītie veidošanas bloki.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118c7207f6efc252c0265d6c8f7b949c0e178203bf8523585aa2bfc53a69a6a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746396"
---
# <a name="income-statement-financial-report"></a>Peļņas vai zaudējumu aprēķina finanšu pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts peļņas vai zaudējumu aprēķina noklusējuma pārskats. Tajā ir aprakstīti arī ar šo pārskatu saistītie veidošanas bloki. 

## <a name="default-income-statement-report"></a>Noklusējuma peļņas vai zaudējumu aprēķina pārskats

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



## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskatu veidošanas apskats](financial-reporting-getting-started.md)

[Finanšu pārskatu skatīšana](view-financial-reports.md)

[Dynamics finanšu pārskatu veidošanas emuārs](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]