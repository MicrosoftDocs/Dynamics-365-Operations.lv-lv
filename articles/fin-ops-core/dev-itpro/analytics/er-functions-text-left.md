---
title: LEFT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LEFT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743787"
---
# <a name="left-er-function"></a>LEFT ER funkcija

[!include [banner](../includes/banner.md)]

`LEFT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes sākuma.

## <a name="syntax"></a>Sintakse

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* vērtība, kas apzīmē oriģinālo tekstu.

`number`: *Vesels skaitlis*

Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta sākuma.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`LEFT ("Sample", 3)` atgriež **"Sam"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
