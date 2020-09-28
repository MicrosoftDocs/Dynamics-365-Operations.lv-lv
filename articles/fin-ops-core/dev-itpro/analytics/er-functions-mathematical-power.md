---
title: POWER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota POWER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744579"
---
# <a name="power-er-function"></a>POWER ER funkcija

[!include [banner](../includes/banner.md)]

`POWER` funkcija atgriež *Reālu* vērtību, kas atspoguļo rezultātu norādītā pozitīvā skaitļa palielināšanai līdz norādītajai jaudai.

## <a name="syntax"></a>Sintakse

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumenti

`number`: *Reāls* vai *Vesels skaitlis*

Skaitliska vērtība, kas ir jāpaaugstina līdz norādītajai jaudām.

`power`: *Reāls* vai *Vesels skaitlis*

Skaitliska vērtība, kas apzīmē konkrēto jaudu.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="example-1"></a>1. piemērs

`POWER (10, 2)` atgriež **100**.

## <a name="example-2"></a>2. piemērs

`POWER (4, 0.5)` atgriež **2**.

## <a name="additional-resources"></a>Papildu resursi

[Matemātiskās funkcijas](er-functions-category-mathematical.md)
