---
title: DAYOFYEAR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DAYOFYEAR elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 755f5f1de28f95ed682648caf47155ad71c8f4b0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745493"
---
# <a name="dayofyear-er-function"></a>DAYOFYEAR ER funkcija

[!include [banner](../includes/banner.md)]

`DAYOFYEAR` funkcija atgriež *Vesela* skaitļa vērtību, kas reprezentē dienu skaitu no 1. janvāra līdz norādītajam datumam.

## <a name="syntax"></a>Sintakse

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumenti

`date`: *Datums*

Datuma vērtība, kas apzīmē datumu, kas jāizmanto, aprēķinot dienu skaitu.

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="example-1"></a>1. piemērs

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` atgriež **61**.

## <a name="example-2"></a>2. piemērs

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` atgriež **1**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)
