---
title: Weeknum ER (funkcija WEEKNUM ER)
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota funkcija WEEKNUM Electronic reporting (ER).
author: NickSelin
ms.date: 12/03/2021
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
ms.openlocfilehash: fe36d4142b6e4922e2cbca09bb0ca9f68f6680a0
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891368"
---
# <a name="weeknum-er-function"></a>Weeknum ER (funkcija WEEKNUM ER)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`WEEKNUM` Funkcija atgriež *[Integer](er-formula-supported-data-types-primitive.md#integer)* vērtību, kas attēlo tā gada nedēļu, kurā iekļauta norādītā *[datuma](er-formula-supported-data-types-primitive.md#date)* vērtība. Aprēķina pamatā ir no kultūras atkarīgi noteikumi, kas definē kalendāro nedēļu un nedēļas pirmo dienu.

## <a name="syntax"></a>Sintakse

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumenti</a>

`date`: *Datums*

Datuma vērtība, kas norāda datumu, kas jāizmanto gada nedēļas aprēķināšanai.

`culture`: *[virkne](er-formula-supported-data-types-primitive.md#string)*

Aprēķinam izmantojamā kultūra. Var izmantot kultūras kodus, kas tiek atbalstīti saskaņā ar .NET [standartiem](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Gada nedēļu aprēķina, pamatojoties uz [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) standartu, ja šo standartu ir pieņēmusi valsts vai reģions, kas ir paredzēts izpildlaikā. Pretējā gadījumā aprēķins ir balstīts uz valstij/reģionam specifiskiem valsts standartiem.

Ja izpildlaikā kā funkcijas arguments tiek norādīts neatbalstīts [kultūras](#arguments)`WEEKNUM` kods, tiek izmests izņēmums. Ja tukšā virkne ir norādīta kā kultūras kods, nedēļas numura aprēķināšanai tiek izmantots angļu valsts neitrālais kalendārs.

## <a name="examples"></a>Piemēri

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` atgriež **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` atgriež **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` atgriež **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` atgriež **21**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
