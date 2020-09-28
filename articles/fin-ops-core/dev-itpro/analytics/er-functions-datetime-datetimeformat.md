---
title: DATETIMEFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATETIMEFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 65b988e6c58aed35577288e01157b8c1f76e6efd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744867"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER funkcija

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` funkcija atgriež *Virknes vērtību*, kas norādīto datuma/laika vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Sintakse 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumenti

`datetime`: *DateTime*

Datuma/laika vērtība, kas apzīmē formatējamo datumu un laiku.

`format`: *Virkne*

Izvades virknes formāts.

`culture`: *Virkne*

Kultūra, ko izmantot formatēšanai.

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

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` atgriež virknes vērtību **2019-11-12T 08:00:00.0000000-08:00**, kad tā tiek saukta procesa laikā, ko iniciēja lietojumprogrammas lietotājs, kuram ir laika joslas vērtība **(GMT-08:00) Klusā okeāna laiks (ASV & Kanāda)** sadaļā **Valodas un valsts/reģiona preferences.**

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)
