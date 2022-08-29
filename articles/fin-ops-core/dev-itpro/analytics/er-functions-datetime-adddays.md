---
title: ADDDAYS ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota ADDDAYS Elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274145"
---
# <a name="adddays-er-function"></a>ADDDAYS ER funkcija

[!include [banner](../includes/banner.md)]

`ADDDAYS` funkcija aprēķina *DateTime* vērtību, kas ir norādītais dienu skaits pirms vai pēc norādītā sākuma datuma.

## <a name="syntax"></a>Sintakse

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumenti

`datetime`: *DateTime*

Datuma/laika vērtība, kas apzīmē sākuma datumu.

`days`: *Vesels skaitlis*

Dienu skaits pirms vai pēc `datetime`.

## <a name="return-values"></a>Atgrieztās vērtības

*DateTime*

Iegūtā datuma/laika vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Pozitīva vērtība `days` norāda uz nākotnes datumu. Negatīva vērtība norāda uz pagātnes datumu.

## <a name="example-1"></a>1. piemērs

`ADDDAYS (NOW(), 7)` atgriež datumu un laiku septiņas dienas uz priekšu.

## <a name="example-2"></a>2. piemērs

`ADDDAYS (NOW(), -3)` atgriež datumu un laiku trīs dienas pagātnē.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
