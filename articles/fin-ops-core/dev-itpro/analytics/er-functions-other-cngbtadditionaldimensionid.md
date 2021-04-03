---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CN_GBT_ADDITIONALDIMENSIONID elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: 5774bb6928ae321af923819d6b2cc609dbf35b99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564146"
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