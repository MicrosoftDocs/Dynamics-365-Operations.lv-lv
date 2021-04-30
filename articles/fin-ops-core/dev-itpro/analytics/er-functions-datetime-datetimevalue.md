---
title: DATETIMEVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATETIMEVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/03/2019
ms.topic: article
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891285"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā [kultūrā](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) datuma/laika vērtībai. Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Sintakse 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Teksts, kas apzīmē formatējamo vērtību.

`format`: *Virkne*

Norādītā teksta formāts.

`culture`: *Virkne*

Kultūra, kas tiek izmantota dotā teksta formatēšanai.

## <a name="return-values"></a>Atgrieztās vērtības

*DateTime*

Iegūtā datuma/laika vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts. Piemēram, ja `DATETIMEVALUE` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru. Noklusējuma `culture` vērtība ir **EN-US**.

## <a name="example-1"></a>1. piemērs

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` atgriež **2:55:00 AM 2016. gada 21. decembrī**, pamatojoties uz norādīto pielāgoto formātu un noklusējuma lietojumprogrammas **EN-US** kultūru.

## <a name="example-2"></a>2. piemērs

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` atgriež **2:55:00 AM 2016. gada 21. decembrī**, pamatojoties uz norādīto pielāgoto formātu un kultūru.

Taču `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīga datuma/laika vērtība norādītajai kultūrai.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]