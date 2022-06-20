---
title: AND ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota AND Elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: bd31fc008b066d7e7d68588c41296537975c2b5c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894358"
---
# <a name="and-er-function"></a>AND ER funkcija

[!include [banner](../includes/banner.md)]

`AND` funkcija atgriež *Būla* vērtību **TRUE**, ja visi norādītie nosacījumi ir patiesi. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.

## <a name="syntax"></a>Sintakse

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenti

`condition 1`: *Būla*

Derīga nosacījuma izteiksme, kas ir jāpārbauda. Šis arguments ir obligāts.

`condition N`: *Būla*

Derīga nosacījuma izteiksme, kas ir jāpārbauda. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Loģisko funkciju argumentos var izmantot datu avota atsauces, skaitliskās un teksta vērtības, Būla vērtības, salīdzināšanas operatorus un citas elektronisko pārskatu (ER) funkcijas. Tomēr visi argumenti ir jānovērtē ar *Būla* vērtību **TRUE** vai **FALSE**.

## <a name="example"></a>Paraugs

`AND (1=1, "a"="a")` atgriež **TRUE**.

`AND (1=2, "a"="a")` atgriež **FALSE**.

## <a name="additional-resources"></a>Papildu resursi

[Loģiskas funkcijas](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]