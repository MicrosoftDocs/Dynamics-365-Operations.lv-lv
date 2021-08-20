---
title: NUMBERFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMBERFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 0208796382bd6564539ebbe3d902cc41dedce235adafefe1126961774cdb2076
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749732"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER funkcija

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT` funkcija atgriež *Virknes* vērtību, kas norādīto skaitu uzrāda norādītajā formātā un pēc izvēles norādītajā [kultūrā](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-numeric-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>Sintakse 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumenti

`number`: *Vesels skaitlis* vai *Reāls*

Skaitliska vērtība, kas norāda skaitli, kas ir jāformatē.

`format`: *Virkne*

*Virknes* vērtība, kas apzīmē formātu.

`culture`: *Virkne*

*Virknes* vērtība, kas apzīmē kultūru, kuru izmantot formatēšanai.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja kultūra nav definēta kā izsauktās funkcijas arguments, šī funkcija tiek palaista kontekstā, kas nosaka, kāda kultūra tiek izmantota skaitļu formatēšanai.

## <a name="example-1"></a>1. piemērs

Kultūrai **EN-US** izteiksme `NUMBERFORMAT (0.45, "p")` atgriež **"45.00 %"** un `NUMBERFORMAT (10.45, "#")` atgriež **"10"**.

## <a name="example-2"></a>2. piemērs

`NUMBERFORMAT (10/3, "F2", "de")` atgriež **3,33**, bet `NUMBERFORMAT (10/3, "F2", "en-us")` atgriež **3,33**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]