---
title: MID ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota MID elektronisko pārskatu (ER) funkcija.
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
ms.openlocfilehash: c53963876db92bb07ed5ac49f009ed4f9bc5e8c4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285915"
---
# <a name="mid-er-function"></a>MID ER funkcija

[!include [banner](../includes/banner.md)]

`MID` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes, sākot no norādītas pozīcijas.

## <a name="syntax"></a>Sintakse

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* vērtība, kas norāda tekstu, no kura jāatgriež rakstzīmes.

`starting position`: *Vesels skaitlis*

*Vesela skaitļa* vērtība, kas norāda pirmās rakstzīmes novietojumu, kura ir jāatgriež no norādītā teksta.

`number of characters`: *Vesels skaitlis*

*Vesela skaitļa* vērtība, kas norāda skaitu rakstzīmēm, kuras ir jāatgriež, sākot no norādītās sākuma pozīcijas.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja `starting position` argumenta vērtība ir mazāka par 0 (nulli), atgrieztās rakstzīmes tiek skaitītas no norādītās virknes pirmās pozīcijas.

Ja `starting position` argumenta vērtība pārsniedz norādītās virknes garumu, tiek atgriezta tukša virkne.

## <a name="example"></a>Paraugs

`MID ("Sample", 2, 3)` atgriež **"amp"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
