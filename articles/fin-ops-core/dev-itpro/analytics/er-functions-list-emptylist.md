---
title: EMPTYLIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYLIST elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb52d7d88f292720360ae913ead5be239165193
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687674"
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
