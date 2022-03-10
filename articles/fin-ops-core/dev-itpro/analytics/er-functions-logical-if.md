---
title: IF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota IF elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 8bd0a7181b441a0a00163b31d4f1116c8bad0705a7f3b52a2985f1b31ecdb28b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745214"
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