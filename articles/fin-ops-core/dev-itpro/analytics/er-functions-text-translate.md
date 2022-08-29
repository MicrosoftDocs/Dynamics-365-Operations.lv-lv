---
title: TRANSLATE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota funkcija TULKOT elektronisko pārskatu (ER).
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278447"
---
# <a name="translate-er-function"></a>TRANSLATE ER funkcija

[!include [banner](../includes/banner.md)]

`TRANSLATE` funkcija atgriež *Virknes* vērtību, kas satur noteiktā teksta rakstzīmju aizstāšanas rezultātu citas nodrošinātās kopas rakstzīmēs.

## <a name="syntax"></a>Sintakse

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* tipa datu avota datu tipa derīgs ceļš.

`pattern`: *Virkne*

Teksts, kas ir jāaizstāj.

`replacement`: *Virkne*

Teksts, ko izmantot kā aizvietotāju.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

`TRANSLATE` funkcija aizstāj pa vienai rakstzīmei reizē. Funkcija aizvieto pirmo `text` argumenta rakstzīmi ar `pattern` argumenta pirmo rakstzīmi un pēc tam otro rakstzīmi un seko tai pašai plūsmai līdz beigām. Kad rakstzīme no `text` un `pattern` argumentiem atbilst, tā tiek aizstāta ar rakstzīmi no `replacement` argumenta, kas atrodas tādā pašā pozīcijā kā rakstzīme no `pattern` argumenta. Ja rakstzīme tiek parādīta vairākas reizes `pattern` argumentā, tiek izmantota `replacement` argumenta kartēšana, kas atbilst šīs rakstzīmes pirmajam parādīšanās gadījumam.

## <a name="example-1"></a>1. piemērs

`TRANSLATE ("abcdef", "cd", "GH")` aizvieto norādītā  **"abcdef"** teksta **"c"** rakstzīmi ar `replacement` teksta **"G"** rakstzīmi sakarā ar:
-   Rakstzīme **"c"** tiek parādīta `pattern` teksta pirmajā pozīcijā.
-   `replacement` teksta pirmajā pozīcijā ir ietverta rakstzīme **"G"**.

## <a name="example-2"></a>2. piemērs

`TRANSLATE ("abcdef", "ccd", "GH")` atgriež **"abGdef"**.

## <a name="example-3"></a>3. piemērs

`TRANSLATE ("abccba", "abc", "123")` atgriež **"123321"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
