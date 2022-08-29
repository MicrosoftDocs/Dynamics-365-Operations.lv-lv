---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šajā rakstā ir sniegta informācija par CN_GBT_ADDITIONALDIMENSIONID funkciju Elektroniskie pārskati (ER).
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281758"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER funkcija

[!include [banner](../includes/banner.md)]

`CN_GBT_ADDITIONALDIMENSIONID` funkcija atgriež *Virknes* vērtību, kas apzīmē vienu finanšu dimensijas ID, kas tiek ņemts no norādītās virknes. Norādītā virkne parāda visas dimensijas kā komatatdalītu ID sarakstu.

## <a name="syntax"></a>Sintakse

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* vērtība, kas parāda visas dimensijas kā komatatdalītu ID sarakstu.

`number`: Vesels skaitlis

*Vesela skaitļa* vērtība, kas definē pieprasītās dimensijas sērijas kodu norādītajā virknē.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` atgriež **"CC"**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
