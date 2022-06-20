---
title: TRIM ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota TRIM elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864661"
---
# <a name="trim-er-function"></a>TRIM ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `TRIM` atgriež norādīto teksta virkni kā Virknes vērtību pēc cilnes, atgriešanas klienti, rindu padeve un formas padeves rakstzīmes ir aizvietotas ar vienu atstarpi pēc atstarpju sākuma un pēdējās apciršanas, un pēc vairāku atstarpju izņemšanas *starp* vārdiem.

## <a name="syntax"></a>Sintakse

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Dažos gadījumos, iespējams, vēlēsieties saīsināt sākuma un beigu atstarpes, bet vēlaties saglabāt formatēšanu norādītajam tekstam. Piemēram, ja šis teksts norāda adresi, ko varētu ievadīt daudzrindu teksta lodziņā un var ietvert rindu padeves un piegādes atgriešanas formatēšanu. Šajā gadījumā izmantojiet šādu izteiksmi: kur `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` ir arguments `text`, kas attiecas uz norādīto teksta virkni.

## <a name="example-1"></a>1. piemērs

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` atgriež **"Sample text"**.

## <a name="example-2"></a>2. piemērs

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` Atgriež " **Parauga teksts"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)

[REPLACE ER funkcija](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
