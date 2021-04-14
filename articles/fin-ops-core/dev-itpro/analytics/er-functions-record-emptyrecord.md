---
title: EMPTYRECORD ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYRECORD elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746535"
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