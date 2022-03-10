---
title: LEFT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LEFT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 5d0056dbe46b20432aacb35a971895b987fdbf1b8ebc0d2679bb1e52eb3c4cc2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762480"
---
# <a name="left-er-function"></a>LEFT ER funkcija

[!include [banner](../includes/banner.md)]

`LEFT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes sākuma.

## <a name="syntax"></a>Sintakse

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* vērtība, kas apzīmē oriģinālo tekstu.

`number`: *Vesels skaitlis*

Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta sākuma.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`LEFT ("Sample", 3)` atgriež **"Sam"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]