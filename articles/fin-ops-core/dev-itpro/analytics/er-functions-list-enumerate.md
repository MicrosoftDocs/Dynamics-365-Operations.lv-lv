---
title: ENUMERATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ENUMERATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: f0a1c83ee869810e816b6d32ea890d172d2910e5
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916227"
---
# <a name="ENUMERATE">ENUMERATE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`ENUMERATE` funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no uzskaitījumā norādītājiem saraksta ierakstiem.

## <a name="syntax"></a>Sintakse

```
ENUMERATE (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Saraksts ar uzskaitītajiem atgrieztajiem ierakstiem parāda šādus papildu elementus:

- Lauku ieraksts (komponents **Vērtība**)
- Pašreizējā ieraksta indekss (komponents **Number**)

## <a name="example"></a>Paraugs

Tālāk esošajā attēlā datu avots **Enumerated** tiek izveidots kā uzskaitījuma kreditoru ierakstu saraksts no datu avota **Vendors**, kas atsaucas uz tabulu VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Šajā attēlā ir parādīta elektronisko pārskatu (ER) formāts. Šajā formātā tiek izveidoti saistījumi, lai ģenerētu izvadi XML formātā Šajā izvadē atsevišķi kreditori attēloti kā uzskaitījuma mezgli.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)
