---
title: FUNKCIJA WEEKNUM ER
description: Šajā tēmā sniegta informācija par to, kā tiek izmantota funkcija WEEKNUM Electronic Reporting (ER).
author: NickSelin
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 37e62b32896e2030b3322a89ac4acdd6c18d5e3c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982181"
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

Aprēķinam izmantojamā kultūra. Var lietot kultūras kodus, kas tiek atbalstīti atbilstoši .NET [standartiem](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Gada nedēļa tiek aprēķināta, pamatojoties uz [ISO 8601 standartu, ja valsts vai reģions ir pieņēmis šo standartu, izpildlaikā tiek](https://www.iso.org/iso-8601-date-and-time-format.html) nodrošināta darbības vieta. Pretējā gadījumā aprēķins pamatojas uz valstij/reģionam specifiskiem valsts standartiem.

Ja izpildlaikā atbalstīts kultūras kods ir norādīts kā [funkcijas](#arguments)`WEEKNUM` arguments, tiek uzstāts kā izņēmums. Ja tukšā virkne ir sniegta kā kultūras kods, nedēļas numura aprēķinam tiek izmantots angļu valsts neitrālais kalendārs.

## <a name="examples"></a>Piemēri

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` atgriež **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` atgriež **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` atgriež **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` atgriež **21**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
