---
title: EMPTYRECORD ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYRECORD elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743954"
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
