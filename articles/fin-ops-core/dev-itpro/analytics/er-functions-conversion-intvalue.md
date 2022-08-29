---
title: INTVALUE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota INTVALUE elektronisko pārskatu (ER) funkcija.
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282627"
---
# <a name="intvalue-er-function"></a>INTVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`INTVALUE` funkcija atgriež *Int* vērtību, kas apzīmē norādīto virkni.

## <a name="syntax-1"></a>Sintakse 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Teksta vērtība, kas ir jāpārvērš par *Int* skaitli.

`number`: *Reāls* vai *Vesels skaitlis*

Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int* skaitli.

## <a name="return-values"></a>Atgrieztās vērtības

*Int*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Tiek aprautas visas decimāldaļas.

## <a name="example-1"></a>1. piemērs

`INTVALUE ("100.77")` atgriež *Int* vērtību **100**.

## <a name="example-2"></a>2. piemērs

`INTVALUE (-100.77)` atgriež *Int* vērtību **-100**.

## <a name="additional-resources"></a>Papildu resursi

[Tipa pārveidošanas funkcijas](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
