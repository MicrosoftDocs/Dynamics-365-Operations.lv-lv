---
title: EMPTYRECORD ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija EMPTYRECORD Electronic Reporting (ER).
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
ms.openlocfilehash: 6f339347187f145b90f14d56017097ff3d7712e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886825"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `EMPTYRECORD` atgriež norādītā saraksta pirmo ierakstu kā tukšu vērtību *Konteiners (ieraksts)*, kurai ir tāda pati struktūra kā ieraksta norādītajam ierakstu sarakstam.

## <a name="syntax"></a>Sintakse

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts* vai *Konteiners (ieraksts)*

*Ierakstu saraksta* vai *Konteinera (ieraksta)* tipa datu avota vienuma derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners (ieraksts)*

Iegūtā ieraksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

> [!NOTE] 
> Ieraksts null ir ieraksts, kurā visos laukos ir tukšas vērtības. Tukša vērtība skaitļiem ir **0** (nulle), virknēm tā ir tukša virkne utt.

## <a name="example"></a>Paraugs

`EMPTYRECORD (SPLIT ("abc", 1))` atgriež jaunu tukšu ierakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`. Plašāku informāciju skatiet šeit: [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Papildu resursi

[Ieraksta funkcijas](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]