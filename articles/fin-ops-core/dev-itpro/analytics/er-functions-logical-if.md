---
title: IF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota IF elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b29302ffe534f2439519e57c6a6b8c94c1df8d62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917147"
---
# <a name="IF">IF ER funkcija</a>

[!include [banner](../includes/banner.md)]

`IF` funkcija atgriež pirmo norādīto vērtību, ja tiek izpildīts norādītais nosacījums. Pretējā gadījumā tiek atgriezta otrā norādītā vērtība. Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.

## <a name="syntax"></a>Sintakse

```
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
