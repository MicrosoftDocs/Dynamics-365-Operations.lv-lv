---
title: ROUNDDOWN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUNDDOWN elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744531"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER funkcija

[!include [banner](../includes/banner.md)]

`ROUNDDOWN` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots uz leju līdz norādītajam ciparu skaitam aiz komata.

## <a name="syntax"></a>Sintakse

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenti

`number`: *Reāls*

Skaitliska vērtība, kas ir jānoapaļo uz leju.

`decimals`: *Vesels skaitlis*

Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šī funkcija darbojas līdzīgi funkcijai [ROUND](er-functions-mathematical-round.md), bet norādīto skaitli tā vienmēr noapaļo uz leju (nulles virzienā).

## <a name="example-1"></a>1. piemērs

`ROUNDDOWN (1200.767, 2)` noapaļo uz leju līdz diviem cipariem aiz komata un atgriež **1200.76**. 

## <a name="example-2"></a>2. piemērs

`ROUNDDOWN (1700.767, -3)` noapaļo uz leju līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.

## <a name="additional-resources"></a>Papildu resursi

[Matemātiskās funkcijas](er-functions-category-mathematical.md)
