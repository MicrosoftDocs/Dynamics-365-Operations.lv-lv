---
title: INT64VALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INT64VALUE elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686055"
---
# <a name="int64value-er-function"></a>INT64VALUE ER funkcija

[!include [banner](../includes/banner.md)]

`INT64VALUE` funkcija atgriež *Int64* vērtību, kas apzīmē norādīto virkni.

## <a name="syntax-1"></a>Sintakse 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Teksta vērtība, kas ir jāpārvērš par *Int64* skaitli.

`number`: *Reāls* vai *Vesels skaitlis*

Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int64* skaitli.

## <a name="return-values"></a>Atgrieztās vērtības

*Int64*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Tiek aprautas visas decimāldaļas.

## <a name="example-1"></a>1. piemērs

`INT64VALUE ("22565422744")` atgriež *Int64* vērtību **22565422744**.

## <a name="example-2"></a>2. piemērs

`INT64VALUE ( VALUE("22565422744.77"))` atgriež *Int64* vērtību **22565422744**.

## <a name="additional-resources"></a>Papildu resursi

[Tipa pārveidošanas funkcijas](er-functions-category-type-conversion.md)
