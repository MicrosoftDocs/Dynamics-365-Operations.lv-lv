---
title: OR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota OR elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686982"
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
