---
title: CONCATENATE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota CONCATENATE elektronisko pārskatu (ER) funkcija
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 230bbbac5df7824c3ef7d0550cc45dbf6c374858
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267290"
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
