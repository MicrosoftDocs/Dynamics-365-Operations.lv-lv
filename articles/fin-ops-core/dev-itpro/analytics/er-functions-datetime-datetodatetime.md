---
title: DATETODATETIME ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota funkcija DATETODATETIME Electronic Reporting (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287314"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME ER funkcija

[!include [banner](../includes/banner.md)]

`DATETODATETIME` funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā datuma vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]).

## <a name="syntax"></a>Sintakse

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumenti

`date`: *Datums*

Datuma/laika vērtība, kas apzīmē konvertējamo datumu.

## <a name="return-values"></a>Atgrieztās vērtības

*DateTime*

Iegūtā datuma/laika vērtība.

## <a name="example-1"></a>1. piemērs

`DATETODATETIME (CompInfo. 'getCurrentDate()')` Atgriež pašreizējās Microsoft Dynamics 365 finanšu sesijas datumu, 2015. gada 24. decembris, **kā 12/24/2015 12:00:00 AM**. Šajā piemērā **CompInfo** ir finanšu un operāciju/**tabulas tipa elektronisko pārskatu (ER)** datu avots, un tas attiecas uz tabulu CompanyInfo.

## <a name="example-2"></a>2. piemērs

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` atgriež datuma/laika vērtību **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
