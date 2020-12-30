---
title: REPLACE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota REPLACE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 3c9d3b6748ecb1680586a2d47a425b5ef98551f1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682923"
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
