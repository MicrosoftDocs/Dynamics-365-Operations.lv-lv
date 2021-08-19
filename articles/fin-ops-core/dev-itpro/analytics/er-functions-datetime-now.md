---
title: NOW ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NOW elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cbbc3623249338c8af943974717a077f68945acfeea2b5e8c4d33c544c58734b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772012"
---
# <a name="now-er-function"></a>NOW ER funkcija

[!include [banner](../includes/banner.md)]

`NOW` funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu un laiku.

## <a name="syntax"></a>Sintakse

```vb
NOW ()
```

## <a name="return-values"></a>Atgrieztās vērtības

*DateTime*

Iegūtā datuma/laika vērtība.

## <a name="example"></a>Paraugs

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]