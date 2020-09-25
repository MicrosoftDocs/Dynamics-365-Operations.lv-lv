---
title: VALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota VALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745517"
---
# <a name="value-er-function"></a>VALUE ER funkcija

[!include [banner](../includes/banner.md)]

`VALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās virknes vērtības.

## <a name="syntax"></a>Sintakse

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Virknes vērtība, kas ir jāpārvērš par skaitlisku vērtību.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme. Izņēmums tiek parādīts izpildes laikā, ja norādītā virkne satur citas rakstzīmes, kas nav skaitļi.

## <a name="example-1"></a>1. piemērs

`VALUE ("1 234,56")` palaiž izņēmumu.

## <a name="example-2"></a>2. piemērs

`VALUE ("1234,56")` atgriež **1234.56**.

## <a name="additional-resources"></a>Papildu resursi

[Tipa pārveidošanas funkcijas](er-functions-category-type-conversion.md)
