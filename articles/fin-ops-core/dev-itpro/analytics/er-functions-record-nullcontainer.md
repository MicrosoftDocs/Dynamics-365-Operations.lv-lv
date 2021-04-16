---
title: NULLCONTAINER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NULLCONTAINER elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746511"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `NULLCONTAINER` atgriež norādītā saraksta pirmo ierakstu kā tukšu vērtību *Konteiners (ieraksts)*, kurai ir tāda pati struktūra kā ieraksta norādītajam ierakstu sarakstam.

## <a name="syntax"></a>Sintakse

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts* vai *Konteiners (ieraksts)*

*Ierakstu saraksta* vai *Konteinera (ieraksta)* tipa datu avota vienuma derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners (ieraksts)*

Iegūtā ieraksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

> [!NOTE] 
> Šī funkcija ir novecojusi. Tā vietā izmantojiet `EMPTYRECORD` funkciju. Plašāku informāciju skatiet šeit: [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Paraugs

`NULLCONTAINER (SPLIT ("abc", 1))` atgriež jaunu tukšu ierakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`. Plašāku informāciju skatiet šeit: [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Papildu resursi

[Ieraksta funkcijas](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]