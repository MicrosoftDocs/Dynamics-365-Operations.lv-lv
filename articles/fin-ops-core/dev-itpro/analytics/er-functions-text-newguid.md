---
title: NEWGUID ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota NEW UZD ELEKTRONISKO pārskatu (ER) funkcija.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274778"
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
