---
title: POWER ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota POWER Electronic Reporting (ER) funkcija.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274002"
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
