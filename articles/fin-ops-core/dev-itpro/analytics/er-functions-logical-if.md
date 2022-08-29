---
title: IF ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota FUNKCIJA IF Electronic Reporting (ER).
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b674a6f3e86af3763a251cbdc7c30fb8c5ed0f55
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275555"
---
# <a name="if-er-function"></a>IF ER funkcija

[!include [banner](../includes/banner.md)]

`IF` funkcija atgriež pirmo norādīto vērtību, ja tiek izpildīts norādītais nosacījums. Pretējā gadījumā tiek atgriezta otrā norādītā vērtība. Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.

## <a name="syntax"></a>Sintakse

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumenti

`condition`: *Būla*

Derīga nosacījuma izteiksme, kas ir jāpārbauda.

`first value`: *Jebkurš no atbalstītajiem datu tipiem*

Rezultāts, kas tiek atgriezts, ja nosacījums ir izpildīts.

`second value`: *Jebkurš no atbalstītajiem datu tipiem*

Rezultāts, kas tiek atgriezts, ja nosacījums nav izpildīts.

## <a name="return-values"></a>Atgrieztās vērtības

*Jebkurš no atbalstītajiem datu tipiem*

Jebkura atbalstītā datu tipa iegūtā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Argumenti `first value` un `second value` ir jānorāda, izmantojot vienu datu tipu. Noformēšanas laikā tiek parādīts izņēmums, ja konfigurētās vērtības nesakrīt.

Ja pirmā rezultāta vērtība un otrā rezultāta vērtība ir *Konteinera (ieraksta)* vai *Ierakstu saraksta* datu tipa vērtības, rezultātam ir tikai tie lauki, kas ir abās vērtībās.

## <a name="example"></a>Paraugs

`IF (1=2, "condition is met", "condition is not met")` atgriež virkni **"nosacījums nav izpildīts"**.

## <a name="additional-resources"></a>Papildu resursi

[Loģiskas funkcijas](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
