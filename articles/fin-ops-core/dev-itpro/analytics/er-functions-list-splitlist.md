---
title: SPLITLIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLITLIST elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745573"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER funkcija

[!include [banner](../includes/banner.md)]

`SPLITLIST` funkcija sadala norādīto sarakstu apakšsarakstos (jeb partijās), kuri katrs satur norādītu ierakstu skaitu. Pēc tam tā atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību, kas sastāv no partijām.

## <a name="syntax-1"></a>Sintakse 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`number`: *Vesels skaitlis*

Maksimālais ierakstu skaits partijā.

`on-demand reading flag`: *Būla*

Vērtība *Būla*, kas norāda, vai pēc pieprasījuma jāģenerē apakšsarakstu elementi.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Atgriezts partiju saraksts satur šādus elementus:

 - **Vērtība:** *Saraksts*

    To ierakstu saraksts, kas pieder pašreizējai partijai.

- **BatchNumber:** *Vesels skaitlis*

    Pašreizējās partijas numurs atgrieztajā sarakstā.

Ja lasīšanas karodziņš pēc pieprasījuma ir iestatīts uz **Patiess**, pēc pieprasījuma tiek ģenerēti apakšsaraksti, kas ļauj samazināt atmiņas patēriņu, bet var izraisīt veiktspējas samazināšanos, ja elementi netiek izmantoti secīgi.

## <a name="example"></a>Paraugs

Tālāk esošajā attēlā redzamais datu avots **Rindas** tiek izveidots kā ierakstu saraksts, kuram ir trīs ieraksti. Šis saraksts tiek sadalīts divās partijās — katrā no partijām ir līdz diviem ierakstiem.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Tālāk esošajā attēlā parādīts izveidotā formāta izkārtojums. Šajā formāta izkārtojumā saistījumi ar datu avotu **Lines** tiek izveidoti, lai ģenerētu izvadi XML formātā Šajā izvadē ietverti atsevišķi mezgli katrai partijai un tajā esošajiem ierakstiem.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
