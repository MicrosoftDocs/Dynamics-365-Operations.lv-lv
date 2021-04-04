---
title: NULLDATETIME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NULLDATETIME elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 159abe09f158565fa9c38da530498329ff183fba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563442"
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