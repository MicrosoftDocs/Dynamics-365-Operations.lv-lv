---
title: ROUNDUP ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota ROUNDUP elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec4fdce6f072c5c3d87b139c8f64bd63a8a3eccd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855650"
---
# <a name="roundup-er-function"></a>ROUNDUP ER funkcija

[!include [banner](../includes/banner.md)]

`ROUNDUP` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.

## <a name="syntax"></a>Sintakse

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenti

`number`: *Reāls*

Skaitliska vērtība, kas ir jānoapaļo uz augšu.

`decimals`: *Vesels skaitlis*

Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šī funkcija darbojas līdzīgi funkcijai [ROUND](er-functions-mathematical-round.md), bet norādīto skaitli tā vienmēr noapaļo uz augšu (prom no nulles).

## <a name="example-1"></a>1. piemērs

`ROUNDUP (1200.763, 2)` noapaļo uz augšu līdz diviem cipariem aiz komata un atgriež **1200.77**.

## <a name="example-2"></a>2. piemērs

`ROUNDUP (1200.767, -3)` noapaļo uz augšu līdz tuvākajam 1 000 reizinājumam un atgriež **2000**.

## <a name="additional-resources"></a>Papildu resursi

[Matemātiskās funkcijas](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]