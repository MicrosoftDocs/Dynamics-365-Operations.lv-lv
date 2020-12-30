---
title: DATEFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEFORMAT elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684936"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER funkcija

[!include [banner](../includes/banner.md)]

`DATEFORMAT` funkcija atgriež *Virknes* vērtību, kas norādīto datuma vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Sintakse 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenti

`date`: *Datums*

Datuma/laika vērtība, kas apzīmē formatējamo datumu.

`format`: *Virkne*

Izvades virknes formāts.

`culture`: *Virkne*

Kultūra, ko izmantot formatēšanai.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā virknes vērtībā.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts. Piemēram, ja `DATEFORMAT` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru. Noklusējuma `culture` vērtība ir **EN-US**.

## <a name="example-1"></a>1. piemērs

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.

## <a name="example-2"></a>2. piemērs

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni  **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)
