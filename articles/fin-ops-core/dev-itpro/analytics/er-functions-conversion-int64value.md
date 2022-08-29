---
title: INT64VALUE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota INT64VALUE elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 4af6cd4ba8b08fe00f53e9dfb1a9156354ec17fc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292592"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
