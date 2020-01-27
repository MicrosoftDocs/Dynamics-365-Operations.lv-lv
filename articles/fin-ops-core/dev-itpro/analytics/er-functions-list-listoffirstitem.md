---
title: LISTOFFIRSTITEM ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTOFFIRSTITEM elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917262"
---
# <a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER funkcija</a>

[!include [banner](../includes/banner.md)]

`LISTOFFIRSTITEM` funkcija atgriež *Ierakstu saraksta* vērtību, kas sastāv vienīgi no norādītā saraksta pirmā ieraksta.

## <a name="syntax"></a>Sintakse

```
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="example"></a>Paraugs

Izteiksme `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` atgriež teksta vērtību **"A".**

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)
