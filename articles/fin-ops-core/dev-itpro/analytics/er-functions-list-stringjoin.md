---
title: STRINGJOIN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota STRINGJOIN elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917193"
---
# <a name="STRINGJOIN">STRINGJOIN ER funkcija</a>

[!include [banner](../includes/banner.md)]

`STRINGJOIN` funkcija atgriež *Virknes* vērtību, kas sastāv no norādītā saraksta norādītā lauka savirknētajām vērtībām. Vērtības var atdalīt ar norādīto norobežotāju.

## <a name="syntax"></a>Sintakse

```
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`field`: *Lauks*

Derīgs ceļš laukam no veida *Virkne* norādītajā sarakstā.

`delimiter`: *Virkne*

Norobežotājs, ko izmanto, lai atdalītu apakšvirknes.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

Ja `SPLIT("abc" , 1)` ievadāt kā datu avotu **DS**, izteiksme `STRINGJOIN (DS, DS.Value, "-")` atgriež **"a-b-c"**.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)
