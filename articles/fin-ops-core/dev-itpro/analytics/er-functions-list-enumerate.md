---
title: ENUMERATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ENUMERATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746655"
---
# <a name="enumerate-er-function"></a>ENUMERATE ER funkcija

[!include [banner](../includes/banner.md)]

`ENUMERATE` funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no uzskaitījumā norādītājiem saraksta ierakstiem.

## <a name="syntax"></a>Sintakse

```vb
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

- Lauku ieraksts (**Vērtība** komponents)
- Pašreizējā ieraksta indekss (**Number** komponents)

## <a name="example"></a>Paraugs

Tālāk esošajā attēlā datu avots **Enumerated** tiek izveidots kā uzskaitījuma kreditoru ierakstu saraksts no datu avota **Vendors**, kas atsaucas uz tabulu VendTable.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Šajā attēlā ir parādīta elektronisko pārskatu (ER) formāts. Šajā formātā tiek izveidoti saistījumi, lai ģenerētu izvadi XML formātā Šajā izvadē atsevišķi kreditori attēloti kā uzskaitījuma mezgli.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]