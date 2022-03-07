---
title: VALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota VALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 04d3320276bc1e23436bd9baa7a84da36314d6c3bf7f84694aa2e01e31230a0b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713946"
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