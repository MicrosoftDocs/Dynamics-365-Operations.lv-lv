---
title: TRIM ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TRIM elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 816f6d6623bb778c9186d294c9b67db7edddd671
ms.sourcegitcommit: 753714ac0dabc4b7ce91509757cd19f7be4a4793
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367796"
---
# <a name="trim-er-function"></a>TRIM ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `TRIM` atgriež norādīto teksta virkni kā *virknes* vērtību pēc cilnes, pārvadāšanas atgriešanas, līnijvades un veidlapu plūsmas rakstzīmes ir aizstātas ar vienu atstarpes rakstzīmi, pēc tam, kad ir apcirstas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem.

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

Dažos gadījumos, iespējams, vēlēsities apcirst sākuma un beigu atstarpes, bet vēlaties saglabāt norādītā teksta formatējumu. Piemēram, ja šis teksts attēlo adresi, kuru var ievadīt vairākrindiņu tekstlodziņā un kurā var būt līnijvads un pārvadāšanas atgriešanas formatējums. Šādā gadījumā izmantojiet šādu izteiksmi: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` kur `text` ir arguments, kas attiecas uz norādīto teksta virkni.

## <a name="example-1"></a>1. piemērs

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` atgriež **"Sample text"**.

## <a name="example-2"></a>2. piemērs

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` atgriež **"Teksta paraugs"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)

[REPLACE ER funkcija](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
