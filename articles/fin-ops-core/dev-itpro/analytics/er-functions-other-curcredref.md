---
title: CURCREDREF ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota CURCREDREF elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 28651a4c238fd56625700ccb6a2a9d73aa23e8d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901598"
---
# <a name="curcredref-er-function"></a>CURCREDREF ER funkcija

[!include [banner](../includes/banner.md)]

`CURCREDREF` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem.

## <a name="syntax"></a>Sintakse

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumenti

`invoice number digits`: *Virkne*

Teksta vērtība, kas attēlo rēķina numura ciparus.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`CURCredRef ("VEND-200002")` atgriež **"2200002"**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]