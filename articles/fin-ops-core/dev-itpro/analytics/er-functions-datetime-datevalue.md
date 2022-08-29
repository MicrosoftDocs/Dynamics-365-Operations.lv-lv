---
title: DATEVALUE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija DATEVALUE Electronic Reporting (ER).
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268704"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`DATEVALUE` funkcija atgriež *[Datuma](er-formula-supported-data-types-primitive.md#date)* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā [kultūrā](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) datuma/laika vērtībai. Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Sintakse 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenti

`text`: *[Virkne](er-formula-supported-data-types-primitive.md#string)*

Teksts, kas apzīmē formatējamo vērtību.

`format`: *Virkne*

Norādītā teksta formāts. Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Virkne*

Kultūra, kas tiek izmantota dotā teksta formatēšanai. Informāciju par atbalstītajām kultūrām skatiet sadaļā [kultūra](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Atgrieztās vērtības

*Datums*

Iegūtā datuma vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts. Piemēram, ja `DATEVALUE` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru. Noklusējuma `culture` vērtība ir **EN-US**.

## <a name="example-1"></a>1. piemērs

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` atgriež datuma vērtību **2016. gada 21. decembris**, pamatojoties uz norādīto pielāgoto formātu un noklusējuma lietojumprogrammas **EN-US** kultūru.

## <a name="example-2"></a>2. piemērs

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` atgriež datuma vērtību **2016. gada 21. janvāri**, pamatojoties uz norādīto pielāgoto formātu un kultūru.

Taču `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīga datuma vērtība norādītajai kultūrai.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
