---
title: TRIM ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TRIM elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f7999ccbcd167280cca1abc48377c36d2bc15f
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744219"
---
# <a name="trim-er-function"></a>TRIM ER funkcija

[!include [banner](../includes/banner.md)]

`TRIM` funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, kam ir aprautas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem.

## <a name="syntax"></a>Sintakse

```vb
TRIM (text )
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` atgriež **"Sample text"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
