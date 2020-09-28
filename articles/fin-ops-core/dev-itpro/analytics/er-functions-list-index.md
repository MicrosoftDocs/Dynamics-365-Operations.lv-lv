---
title: INDEX ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INDEX elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745182"
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
