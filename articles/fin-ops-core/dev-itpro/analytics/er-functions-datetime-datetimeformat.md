---
title: DATETIMEFORMAT ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija DATETIMEFORMAT Electronic reporting (ER).
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: e21b676046b6279826a728657fcc0d2a00a38b76
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287374"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER funkcija

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` funkcija atgriež *[Virknes](er-formula-supported-data-types-primitive.md#string)* vērtību, kas norādīto datuma/laika vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Sintakse 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumenti

`datetime`*[DateTime](er-formula-supported-data-types-primitive.md#datetime)*

Datuma/laika vērtība, kas apzīmē formatējamo datumu un laiku.

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

Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts. Piemēram, ja `DATETIMEFORMAT` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru. Noklusējuma `culture` vērtība ir **EN-US**.

Kad `DATETIMEFORMAT` funkcija konvertē konkrētu datuma/laika vērtību, tā ņem vērā tā programmas lietotāja laika joslas iestatījumu lietotājs, kurš darbina ER formātu, kura kontekstā tikusi izsaukta funkcija.

## <a name="example-1"></a>1. piemērs

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.

## <a name="example-2"></a>2. piemērs

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datuma/laika vērtību, 2015. gada 24. decembri, kā **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.

## <a name="example-3"></a>3. piemērs

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` atgriež virknes vērtību **2019-11-12T08:00:00.0000000-08:00**, kad tā tiek saukta procesa laikā, ko iniciēja lietojumprogrammas lietotājs, kuram ir laika joslas vērtība **(GMT-08:00) Klusā okeāna laiks (ASV & Kanāda)** sadaļā **Valodas un valsts/reģiona preferences**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
