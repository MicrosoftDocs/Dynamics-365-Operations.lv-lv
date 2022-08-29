---
title: FORMATELEMENTNAME ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota FORMATELEMENTNAME Elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1c8c319075f8f39bec963df2c88d2d8d3beace43
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275442"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME ER funkcija

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME` funkcija atgriež vērtību *Virkne*, kas apzīmē pašreizējā elektroniskā pārskata (ER) formāta elementa nosaukumu.

## <a name="syntax"></a>Sintakse

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šo funkciju var izteikt ER izteiksmēs, kas bija konfigurētas rekvizītiem **Ievāktās datu atslēgas nosaukums** un **Ievāktās datu atslēgas vērtība** ER formāta komponentē no grupas **Teksts**, kas atrodas komponentē **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.

## <a name="example"></a>Paraugs

Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.

## <a name="additional-resources"></a>Papildu resursi

[Datu apkopošanas funkcijas](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
