---
title: CHAR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CHAR elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563202"
---
# <a name="char-er-function"></a>CHAR ER funkcija

[!include [banner](../includes/banner.md)]

`CHAR` funkcija atgriež *Virknes* vērtību, kas parāda vienu rakstzīmi, uz kuru atsaucas norādītais unikoda numurs.

## <a name="syntax"></a>Sintakse

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumenti

`number`: *Vesels skaitlis*

Skaitlis, kas atbilst paredzētai vienai rakstzīmei.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šīs funkcijas atgrieztā virkne ir atkarīga kodējuma, kas ir atlasīts vecākelementa formāta elementā **FILE**. Atbalstīto kodējumu sarakstu skatiet tēmā [Kodējuma klase](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Paraugs

`CHAR (255)` atgriež **"ÿ"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]