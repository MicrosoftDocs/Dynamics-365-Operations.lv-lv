---
title: ROuNDAMOUNT ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota ROUNDAMOUNT elektronisko pārskatu (ER) funkcija.
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
ms.openlocfilehash: 0e4de43f865ca21822ab2c0c345026d2e9113ca2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286035"
---
# <a name="roundamount-er-function"></a>ROuNDAMOUNT ER funkcija

[!include [banner](../includes/banner.md)]

`ROUNDAMOUNT` funkcija atgriež *Reālu* vērtību, kas apzīmē rezultātu norādītās summas noapaļošanai uz tuvāko cita skaitļa reizinātāju saskaņā ar norādīto noapaļošanas kārtulu.

## <a name="syntax"></a>Sintakse

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumenti

`number`: *Int* vai *Real*

Skaitliska vērtība, kas ir jānoapaļo.

`decimals`: *Int* vai *Real*

Skaitlis, līdz kura daudzkārtnim ir jānoapaļo `number` parametra vērtība.

`round rule`: *Uzskaitījuma vērtība*

Uzskaitījuma vērtība **RoundOffType** uzskaitījumam, kas definē noapaļošanas kārtulu. Šis uzskaitījums piedāvā šādas vērtības:

- Parasts (parastais)
- Uz leju (RoundDown)
- Noapaļot uz augšu (RoundUp)

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība ir reizinātājs vērtībai, ko norāda parametrs `decimals` un kas ir vistuvāk `number` parametra norādītajai vērtībai.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja `number` parametrs ir nulle, šī funkcija vienmēr atgriež nulli.

Ja `decimals` parametrs ir nulle, šī funkcija noapaļo uz noklusējuma noapaļoto vērtību. Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, noklusējuma noapaļotā vērtība ir **0,01.** Pretējā gadījumā noklusējuma noapaļotā vērtība ir **1,0.**

Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, šī funkcija noapaļo līdz tuvākajai noapaļošanās summai.

Ja `round rule` parametrs ir iestatīts uz **RoundOffType.RoundDown**, šī funkcija noapaļo nulles virzienā līdz tuvākajai noapaļošanās summai.

Ja `round rule` parametrs ir iestatīts uz **RoundOffType.RoundUp**, šī funkcija noapaļo prom no nulles līdz tuvākajai noapaļošanās summai.

Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, šī funkcija darbojas līdzīgi kā [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel funkcija un [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ funkcija.

## <a name="remarks"></a>Piezīmes

Lai skaitlisko vērtību noapaļotu līdz noteiktam decimāldaļu skaitam, izmantojiet funkciju [ROUND](er-functions-mathematical-round.md)

## <a name="example"></a>Paraugs

Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 7,35. 

Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 7,35. 

Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 8,4.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)

[Matemātiskās funkcijas](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
