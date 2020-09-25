---
title: ISOCREDREF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISOCREDREF elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744099"
---
# <a name="isocredref-er-function"></a>ISOCREDREF ER funkcija

[!include [banner](../includes/banner.md)]

`ISOCREDREF` funkcija atgriež *Virknes* vērtību, kas apzīmē Starptautiskās Standartizācijas organizācijas (ISO) kreditora atsauci atbilstoši norādītā rēķina numura cipariem un burtiem.

## <a name="syntax"></a>Sintakse

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumenti

`invoice number digits`: *Virkne*

Teksta vērtība, kas attēlo rēķina numura ciparus.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

> [!NOTE] 
> Lai izslēgtu alfabētu simbolus, kas nav saderīgi ar ISO, arguments `invoice number digits` pirms nodošanas šai funkcijai ir jātulko.

## <a name="example"></a>Paraugs

`ISOCredRef ("VEND-200002")` atgriež **"RF23VEND-200002"**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)
