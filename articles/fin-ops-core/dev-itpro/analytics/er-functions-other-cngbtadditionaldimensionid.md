---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CN_GBT_ADDITIONALDIMENSIONID elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686814"
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
