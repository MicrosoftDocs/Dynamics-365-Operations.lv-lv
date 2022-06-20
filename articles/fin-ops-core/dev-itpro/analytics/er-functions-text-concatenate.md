---
title: CONCATENATE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota CONCATENATE elektronisko pārskatu (ER) funkcija
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
ms.openlocfilehash: 926c3acf92fc8017c3c4a7814855a6871c1cacc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863269"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER funkcija

[!include [banner](../includes/banner.md)]

`CONCATENATE` funkcija atgriež visas norādītās teksta virknes kā *Virknes* vērtību pēc tam, kad tās ir apvienotas vienā virknē.

## <a name="syntax"></a>Sintakse

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumenti

`text 1`: *Virkne*

Atsauce uz datu avotu *Virknes* datu tipam. Šis arguments ir obligāts.

`text N`: *Virkne*

Atsauce uz datu avotu *Virknes* datu tipam. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`CONCATENATE ("abc", "def")` atgriež **"abcdef"**.

## <a name="usage-notes"></a>Lietošanas piezīmes

Arī izteiksme `"abc" & "def"` atgriež **"abcdef"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]