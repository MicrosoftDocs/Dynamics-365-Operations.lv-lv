---
title: REVERSE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota FUNKCIJA REVERSE Electronic Reporting (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: fce611b755865db15e8877e58d59bdf36bc730fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881524"
---
# <a name="reverse-er-function"></a>REVERSE ER funkcija

[!include [banner](../includes/banner.md)]

`REVERSE` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību apgrieztā kārtošanas secībā.

## <a name="syntax"></a>Sintakse

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="example-1"></a>1. piemērs

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` atgriež teksta vērtību **C**.

## <a name="example-2"></a>2. piemērs

Ja parametrs **Kreditors** ir konfigurēts kā elektronisko pārskatu (ER) datu avots, kurš atsaucas uz tabulu VendTable, tad izteiksme `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` atgriež sarakstu ar kreditoriem, kuri ir sakārtoti dilstošā secībā pēc nosaukuma.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]