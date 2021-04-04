---
title: FORMATELEMENTNAME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FORMATELEMENTNAME elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561306"
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