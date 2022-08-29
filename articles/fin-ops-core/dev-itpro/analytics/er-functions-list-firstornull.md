---
title: FIRSTORNULL ER funkcija
description: Šajā rakstā skaidrots, kā tiek izmantota firstLLAULL elektronisko pārskatu (ER) funkcija
author: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 7ee1a5c1b6ac13581608f9adbda42fae0706d225
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273194"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER funkcija

[!include [banner](../includes/banner.md)]

`FIRSTORNULL` funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis ieraksts nav tukšs. Ja ieraksts ir tukšs, šī funkcija atgriež tukšu *Konteinera (ieraksta)* vērtību.

## <a name="syntax"></a>Sintakse

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners (ieraksts)*

Iegūtā ieraksta vērtība.

## <a name="example"></a>Paraugs

Izteiksme `FIRSTORNULL(SPLIT("",1)).Value` atgriež tukšu virkni (**""**).

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
