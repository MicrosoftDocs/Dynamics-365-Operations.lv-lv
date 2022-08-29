---
title: TEXT ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota funkcija TEXT Elektroniskie pārskati (ER).
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: a32da5588c5231b20bc8166d20888c1611ca273e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278862"
---
# <a name="text-er-function"></a>TEXT ER funkcija

[!include [banner](../includes/banner.md)]

`TEXT` funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tā ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās programmas instances servera lokalizācijas iestatījumiem.

## <a name="syntax"></a>Sintakse

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumenti

`number`: *Vesels skaitlis* vai *Reāls*

Skaitlis, kas ir jāpārvērš par teksta virkni.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Vērtībām ar tipu *Reāls* šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.

## <a name="example"></a>Paraugs

Microsoft Dynamics Ja 365 finanšu instances servera atrašanāsvieta ir definēta kā EN-US **,** atgriež pašreizējo finanšu sesijas datumu, 2015`TEXT (NOW ())`. gada 17. decembris, **kā teksta virkne "12/17/2015 07:59:23 AM"**. `TEXT (1/3)` atgriež **"0.33"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
