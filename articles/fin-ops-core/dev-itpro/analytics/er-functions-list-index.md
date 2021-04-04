---
title: INDEX ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INDEX elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 88be8f8bdc82bf3eab5c99e72046c794d8fac361
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566929"
---
# <a name="index-er-function"></a>INDEX ER funkcija

[!include [banner](../includes/banner.md)]

`INDEX` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas ir atlasīta, izmantojot norādītajā sarakstā norādīto skaitlisko indeksu. Tiek parādīts izņēmums, ja indekss neietilpst sarakstā esošo ierakstu diapazonā.

## <a name="syntax"></a>Sintakse

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`index`: *Vesels skaitlis*

Skaitlisks indekss, kas norāda vajadzīgā ieraksta novietojumu norādītajā sarakstā.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners (ieraksts)*

Iegūtā ieraksta vērtība.

## <a name="example-1"></a>1. piemērs

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`,izteiksme `DS.Value` atgriež teksta vērtību **"B"** otrajam ierakstam šajā ierakstu sarakstā. Izteiksme `INDEX (SPLIT ("A|B|C", "|"), 2).Value` arī atgriež teksta vērtību **"B"**.

## <a name="example-2"></a>2. piemērs

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `INDEX (SPLIT ("A|B|C", "|"), 4).Value` izpildlaikā rāda izņēmumu.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]