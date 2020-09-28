---
title: MID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota MID elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744723"
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
