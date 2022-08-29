---
title: NUMBERVALUE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija NUMBERVALUE Electronic Reporting (ER).
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2e39cf59cabd44583e78ff2c35a7ae4d6edbd7ee
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282597"
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
