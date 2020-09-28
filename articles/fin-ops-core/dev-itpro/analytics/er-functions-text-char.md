---
title: CHAR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CHAR elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744965"
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
