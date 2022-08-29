---
title: PADLEFT ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota PADLEFT Elektronisko pārskatu (ER) funkcija.
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
ms.openlocfilehash: dac1f9142a381238bf116c4bce65958da8afc4db
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278894"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
