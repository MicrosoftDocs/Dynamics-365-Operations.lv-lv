---
title: DATEFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 4a6c113f5f8147cbeaab103e86a44d4c66272c13
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485496"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER funkcija

[!include [banner](../includes/banner.md)]

`DATEFORMAT` funkcija atgriež *[Virknes](er-formula-supported-data-types-primitive.md#string)* vērtību, kas norādīto datuma vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Sintakse 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenti

`date`*[Datums](er-formula-supported-data-types-primitive.md#date)*

Datuma/laika vērtība, kas apzīmē formatējamo datumu.

`format`: *Virkne*

Izvades virknes formāts. Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> Ja izmantojat standarta formātu vai pielāgotu formātu, formāta virkne ir reģistrjutīga. Piemēram, [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" formāta apzīmētājs atgriež datumu, izmantojot īsa datuma modeli, turpretī standarta "D" formāta apzīmētājs atgriež datumu, izmantojot garo datuma modeli. Turklāt [pielāgotais](/dotnet/standard/base-types/custom-date-and-time-format-strings) formāta apzīmētājs atgriež mēnesi no 1 līdz 12, bet pielāgotais "m" formāta apzīmētājs atgriež minūti no 0 līdz 59.

`culture`: *Virkne*

Kultūra, ko izmantot formatēšanai. Informāciju par atbalstītajām kultūrām skatiet sadaļā [kultūra](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā virknes vērtībā.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts. Piemēram, ja `DATEFORMAT` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru. Noklusējuma `culture` vērtība ir **EN-US**.

## <a name="example-1"></a>1. piemērs

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.

## <a name="example-2"></a>2. piemērs

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
