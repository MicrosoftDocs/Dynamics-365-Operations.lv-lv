---
title: INDEX ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota funkcija INDEX Electronic Reporting (ER).
author: kfend
ms.date: 05/20/2021
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
ms.openlocfilehash: 1ecac869644b09ee6564a4cd0eb53a82de9df25f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274032"
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

> [!NOTE]
> Tā kā šai funkcijai tiek izmantota vienreizējā numerācija, norādiet vērtību **1**, lai atgrieztu pirmo norādītā saraksta ierakstu.

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
