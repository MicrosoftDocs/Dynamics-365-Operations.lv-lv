---
title: EMPTYLIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYLIST elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559204"
---
# <a name="emptylist-er-function"></a>EMPTYLIST ER funkcija

[!include [banner](../includes/banner.md)]

`EMPTYLIST` funkcija atgriež tukšu *Ierakstu saraksta* vērtību, šī saraksta struktūrai kā avotu izmantojot norādīto sarakstu.

## <a name="syntax"></a>Sintakse

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="example"></a>Paraugs

`EMPTYLIST (SPLIT ("abc", 1))` atgriež jaunu tukšu sarakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]