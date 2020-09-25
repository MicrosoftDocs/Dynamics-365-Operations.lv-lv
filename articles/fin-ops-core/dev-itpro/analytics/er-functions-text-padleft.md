---
title: PADLEFT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota PADLEFT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744363"
---
# <a name="padleft-er-function"></a>PADLEFT ER funkcija

[!include [banner](../includes/banner.md)]

`PADLEFT` funkcija norādītā garuma *Virknes* vērtību, kurā norādītās virknes sākumā ir ievadītas norādītās rakstzīmes.

## <a name="syntax"></a>Sintakse

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* vērtība, kas apzīmē oriģinālo tekstu.

`length`: *Vesels skaitlis*

*Vesela skaitļa* vērtība, kas apzīmē rakstzīmju galīgo skaitu ievadītajā virknē.

`padding chars`: *Virkne*

Rakstzīmes, kas jāizmanto ievadīšanai.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`PADLEFT ("1234", 10, "`&nbsp;`")` atgriež teksta virkni **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
