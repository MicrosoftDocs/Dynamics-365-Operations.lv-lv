---
title: ISEMPTY ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota ISEMPTY Elektronisko pārskatu (ER) funkcija.
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
ms.openlocfilehash: e1f1ac1cc1729ef6d0f0301f12cc3f4b07fc6110
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273224"
---
# <a name="isempty-er-function"></a>ISEMPTY ER funkcija

[!include [banner](../includes/banner.md)]

`ISEMPTY` funkcija atgriež *Būla* vērtību **TRUE**, ja norādītajā sarakstā nav ierakstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.

## <a name="syntax"></a>Sintakse

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name="example-1"></a>1. piemērs

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `ISEMPTY(DS)` atgriež **FALSE**.

## <a name="example-2"></a>2. piemērs

Izteiksme `ISEMPTY (SPLIT ("",1))` atgriež **TRUE**.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
