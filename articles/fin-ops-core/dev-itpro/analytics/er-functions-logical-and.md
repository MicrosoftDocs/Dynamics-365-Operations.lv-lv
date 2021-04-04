---
title: AND ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota AND elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: 068b9a3b2cf2e5bffe895bc4e8a7cbb2d8025ad7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560089"
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