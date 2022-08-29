---
title: DAYOFYEAR ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija DAYOFYEAR Elektronisko pārskatu (ER).
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
ms.openlocfilehash: e49a80b2ef3c7defcfc23e868374cec5832dc913
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292562"
---
# <a name="dayofyear-er-function"></a>DAYOFYEAR ER funkcija

[!include [banner](../includes/banner.md)]

`DAYOFYEAR` funkcija atgriež *Vesela* skaitļa vērtību, kas reprezentē dienu skaitu no 1. janvāra līdz norādītajam datumam.

## <a name="syntax"></a>Sintakse

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumenti

`date`: *Datums*

Datuma vērtība, kas apzīmē datumu, kas jāizmanto, aprēķinot dienu skaitu.

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="example-1"></a>1. piemērs

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` atgriež **61**.

## <a name="example-2"></a>2. piemērs

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` atgriež **1**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
