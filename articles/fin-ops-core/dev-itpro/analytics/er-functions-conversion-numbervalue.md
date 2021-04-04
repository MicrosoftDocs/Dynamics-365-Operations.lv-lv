---
title: NUMBERVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMBERVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561426"
---
# <a name="numbervalue-er-function"></a>NUMBERVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`NUMBERVALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības. Konvertēšanas laikā tiek uzskatīti norādītie decimālo un ciparu grupēšanas atdalītāji.

## <a name="syntax"></a>Sintakse

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Teksta vērtība, kas ir jāpārvērš par *Reālu* skaitli.

`decimal separator`: Virkne

Decimāldaļu atdalītājs. Tas tiek izmantots, lai atdalītu veselā skaitļa un daļskaitļa daļas no decimālskaitļa.

`digit grouping separator`: *Virkne*

Ciparu grupēšanas atdalītājs. Tas tiek izmantots kā tūkstošu atdalītājs.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="example"></a>Paraugs

`NUMBERVALUE( "1 234,56", ",", " ")` atgriež **1234.56**.

## <a name="additional-resources"></a>Papildu resursi

[Tipa pārveidošanas funkcijas](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]