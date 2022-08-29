---
title: TRIM ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota TRIM elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273104"
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
