---
title: NULLDATETIME ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota NULLDATETIME elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 49b75a6cc1e2c1eee926ed8a235ae886d781ad3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287284"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER funkcija

[!include [banner](../includes/banner.md)]

`NULLDATETIME` funkcija atgriež *DateTime* vērtību, kas apzīmē **nulles** datuma/laika vērtību (1900. gada 1. janvāris) universālajā koordinētajā laikā (Griničas laikā \[GMT\]).

## <a name="syntax"></a>Sintakse

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Atgrieztās vērtības

*DateTime*

Iegūtā datuma/laika vērtība.

## <a name="example"></a>Paraugs

`DATETIMEFORMAT( NULLDATETIME(), "O")` atgriež virknes vērtību **1900-01-01T00:00:00.0000000+00:00**, kad tā tiek saukta procesa laikā, ko iniciēja lietojumprogrammas lietotājs, kuram ir laika joslas vērtība **(GMT) universālais koordinētais laiks** sadaļā **Valodas un valsts/reģiona preferences**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
