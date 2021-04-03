---
title: ROuNDAMOUNT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUNDAMOUNT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: 2a80587236d17160a996d701ca4ae38be21c818c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563298"
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

Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, šī funkcija darbojas līdzīgi kā [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel funkcija un [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ funkcija.

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