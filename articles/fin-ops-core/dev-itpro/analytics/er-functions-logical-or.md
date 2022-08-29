---
title: OR ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota OR elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 99b5ee37af1ea1a69985fb79b762b31561334fd6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268092"
---
# <a name="or-er-function"></a>OR ER funkcija

[!include [banner](../includes/banner.md)]

`OR` funkcija atgriež *Būla* vērtību **FALSE**, ja visi norādītie nosacījumi ir nepatiesi. Šī funkcija atgriež *Būla* vērtību **TRUE**, ja jebkurš norādītais nosacījums ir patiess.

## <a name="syntax"></a>Sintakse

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenti

`condition 1`: *Būla*

Derīga nosacījuma izteiksme, kas ir jāpārbauda. Šis arguments ir obligāts.

`condition N`: *Būla*

Derīga nosacījuma izteiksme, kas ir jāpārbauda. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name="example"></a>Paraugs

`OR (1=2, "a"="a")` atgriež **TRUE**.

## <a name="additional-resources"></a>Papildu resursi

[Loģiskas funkcijas](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
