---
title: SESSIONTODAY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SESSIONTODAY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2aa3d5e34e6dcd9b5d4a3fe3f21d7e3285adbcad
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745421"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER funkcija

[!include [banner](../includes/banner.md)]

`SESSIONTODAY` funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu.

## <a name="syntax"></a>Sintakse

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Atgrieztās vērtības

*Datums*

Iegūtā datuma vērtība.

## <a name="example"></a>Paraugs

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)
