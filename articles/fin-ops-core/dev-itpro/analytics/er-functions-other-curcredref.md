---
title: CURCREDREF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CURCREDREF elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 3923126060963122634d90c2ba8a380f534e9178
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686766"
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