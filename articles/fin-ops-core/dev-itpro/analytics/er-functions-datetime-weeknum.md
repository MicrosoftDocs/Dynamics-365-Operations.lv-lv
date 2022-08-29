---
title: FUNKCIJA WEEKNUM ER
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija WEEKNUM Electronic Reporting (ER).
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268152"
---
# <a name="weeknum-er-function"></a>FUNKCIJA WEEKNUM ER

[!include [banner](../includes/banner.md)]

Funkcija `WEEKNUM` atgriež Vesela *[...](er-formula-supported-data-types-primitive.md#integer)* skaitļa vērtību, kas apzīmē gada nedēļu, kurā iekļauta norādītā *[Datuma](er-formula-supported-data-types-primitive.md#date)* vērtība. Aprēķina pamatā ir no kultūras atkarīgi noteikumi, kas definē kalendāro nedēļu un pirmo nedēļas dienu.

## <a name="syntax"></a>Sintakse

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumenti</a>

`date`: *Datums*

Datuma vērtība, kas norāda datumu, kuru izmantot gada nedēļas aprēķinam.

`culture`: *[virkne](er-formula-supported-data-types-primitive.md#string)*

Aprēķinam izmantojamā kultūra. Var lietot kultūras kodus, kas tiek atbalstīti saskaņā ar .NET [standartiem](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Gada nedēļa [tiek aprēķināta, pamatojoties uz ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) standartu, ja valsts vai reģions ir pieņēmis šo standartu, izpildlaikā tiek nodrošināta darbības vieta. Pretējā gadījumā aprēķins pamatojas uz valstij/reģionam specifiskiem valsts standartiem.

Ja izpildlaikā atbalstīts [kultūras](#arguments) kods ir norādīts `WEEKNUM` kā funkcijas arguments, tiek uzstāts kā izņēmums. Ja tukšā virkne ir sniegta kā kultūras kods, nedēļas numura aprēķinam tiek izmantots angļu valsts neitrālais kalendārs.

## <a name="examples"></a>Piemēri

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` atgriež **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` atgriež **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` atgriež **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` atgriež **21**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
