---
title: VALUE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija VALUE Electronic Reporting (ER).
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
ms.openlocfilehash: 0a47637c47ca6c947451efa1230191779401b4e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277668"
---
# <a name="value-er-function"></a>VALUE ER funkcija

[!include [banner](../includes/banner.md)]

`VALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās virknes vērtības.

## <a name="syntax"></a>Sintakse

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Virknes vērtība, kas ir jāpārvērš par skaitlisku vērtību.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme. Izņēmums tiek parādīts izpildes laikā, ja norādītā virkne satur citas rakstzīmes, kas nav skaitļi.

## <a name="example-1"></a>1. piemērs

`VALUE ("1 234,56")` palaiž izņēmumu.

## <a name="example-2"></a>2. piemērs

`VALUE ("1234,56")` atgriež **1234.56**.

## <a name="additional-resources"></a>Papildu resursi

[Tipa pārveidošanas funkcijas](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
