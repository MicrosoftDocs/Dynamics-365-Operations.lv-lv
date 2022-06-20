---
title: POWER ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota POWER Electronic Reporting (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da3ae988b57cb5588de1e2fd8ee962b77b5534ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864693"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]