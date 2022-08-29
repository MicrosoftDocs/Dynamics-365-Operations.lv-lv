---
title: LISTOFFIRSTITEM ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija LISTOFFIRSTITEM Electronic reporting (ER).
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
ms.openlocfilehash: dede32c58ef8dc67028ea17b8a26189f62f73593
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275591"
---
# <a name="listoffirstitem-er-function"></a>LISTOFFIRSTITEM ER funkcija

[!include [banner](../includes/banner.md)]

`LISTOFFIRSTITEM` funkcija atgriež *Ierakstu saraksta* vērtību, kas sastāv vienīgi no norādītā saraksta pirmā ieraksta.

## <a name="syntax"></a>Sintakse

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="example"></a>Paraugs

Izteiksme `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` atgriež teksta vērtību **"A".**

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
