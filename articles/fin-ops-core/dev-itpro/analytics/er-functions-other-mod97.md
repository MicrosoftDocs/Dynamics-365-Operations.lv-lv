---
title: MOD_97 ER funkcija
description: Šajā rakstā ir sniegta informācija par MOD_97 funkciju Elektroniskie pārskati (ER).
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 55d2bce660186f10fc48e29f5cf03385a778a57a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285221"
---
# <a name="mod_97-er-function"></a>MOD_97 ER funkcija

[!include [banner](../includes/banner.md)]

`MOD_97` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD97 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem.

## <a name="syntax"></a>Sintakse

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Argumenti

`invoice number digits`: *Virkne*

Teksta vērtība, kas attēlo rēķina numura ciparus.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`MOD_97 ("VEND-200002")` atgriež **"20000285"**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
