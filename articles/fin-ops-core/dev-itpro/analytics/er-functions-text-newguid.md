---
title: NEWGUID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NEWGUID Elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647946"
---
# <a name="newguid-er-function"></a>NEWGUID ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `NEWGUID` ģenerē jaunu globāli unikālu identifikatoru (GUID) un atgriež to kā *[GUID](er-formula-supported-data-types-primitive.md#guid)* vērtību.

## <a name="syntax"></a>Sintakse

```vb
NEWGUID ()
```

## <a name="return-values"></a>Atgrieztās vērtības

*GUID*

Iegūtā GUID vērtība.

## <a name="example"></a>Paraugs

`NEWGUID()` vienmēr atgriež jaunu *GUID* vērtību, piemēram, **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
