---
title: FORMATELEMENTNAME ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota FORMATELEMENTNAME Elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0a733c3c70cede6395b3d7454d82ce4d999e7e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851985"
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