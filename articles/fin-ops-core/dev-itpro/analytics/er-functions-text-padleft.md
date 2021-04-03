---
title: PADLEFT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota PADLEFT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562689"
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