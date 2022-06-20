---
title: REPLACE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija REPLACE Electronic Reporting (ER).
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 6c2b1ba82d61a3c163f1d657035b66ace9f15c77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878376"
---
# <a name="replace-er-function"></a>REPLACE ER funkcija

[!include [banner](../includes/banner.md)]

`REPLACE` funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, ja visa vai daļa no tās ir aizstāta ar citu virkni.

## <a name="syntax"></a>Sintakse

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* tipa datu avota datu tipa derīgs ceļš.

`pattern`: *Virkne*

Ja `regular expression flag` arguments ir **FALSE**, šis arguments satur tekstu, kas ir jāaizstāj.

Ja `regular expression flag` arguments ir **TRUE**, šis arguments ietver parastu izteiksmi, kas definē gan meklēšanas rakstu, gan aizstājējtekstu.

`replacement`: *Virkne*

Ja `regular expression flag` arguments ir **FALSE**, šis arguments satur tekstu, kas ir jāizmanto kā aizstājējs.

Ja `regular expression flag` arguments ir **TRUE**, šis arguments netiek izmantots.

`regular expression flag`: *Būla*

*Būla* vērtība, kas norāda, vai aizstāšanas laikā tiek izmantota parasta izteiksme.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja `regular expression flag` arguments ir **patiess**, šī funkcija atgriež norādīto virkni pēc tam, kad tā ir mainīta, lietojot `pattern` argumenta norādīto regulāro izteiksmi. Regulārā izteiksme tiek izmantota, lai atrastu rakstzīmes, kas ir jāaizstāj.

Ja `regular expression flag` arguments ir **APLAMS**, šī funkcija atgriež norādīto virkni pēc tam, kad rakstzīmju kopa, kas definēta `pattern` argumentā, ir aizstāta ar `replacement` argumenta rakstzīmēm. 

## <a name="example-1"></a>1. piemērs

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` lieto parastu izteiksmi, kas noņem visus simbolus, kuri nav skaitļi, un atgriež **"19234564971"**. 

## <a name="example-2"></a>2. piemērs

`REPLACE ("abcdef", "cd", "GH", false)` aizstāj burtus **"cd"** ar virkni **"GH"** un atgriež **"abGHef"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]