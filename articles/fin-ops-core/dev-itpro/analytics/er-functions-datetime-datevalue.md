---
title: DATEVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682417"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`DATEVALUE` funkcija atgriež *Datuma* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) datuma/laika vērtībai. Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Sintakse 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Teksts, kas apzīmē formatējamo vērtību.

`format`: *Virkne*

Norādītā teksta formāts.

`culture`: *Virkne*

Kultūra, kas tiek izmantota dotā teksta formatēšanai.

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
