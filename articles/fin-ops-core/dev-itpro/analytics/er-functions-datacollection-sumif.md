---
title: SUMIF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SUMIF elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 6f5069d197abf2e38d09012defeb982a9e5e1234
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565968"
---
# <a name="sumif-er-function"></a>SUMIF ER funkcija

[!include [banner](../includes/banner.md)]

`SUMIF` funkcija atgriež vērtību *Reāls* skaitlis, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam. Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.

## <a name="syntax"></a>Sintakse

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Argumenti

`key name for summing`: *Virkne*

Vērtība, kas tiek atgriezta, izmantojot izteiksmi, kas konfigurēta komponenta elektroniskā pārskata (ER) formāta rekvizītā **Ievāktās atslēgas nosaukums**, kurai summēšanas nolūkā ir jāizmanto saistījuma vērtība.

Rekvizītu **Ievāktās datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.

`condition range` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.

`condition value` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.

## <a name="example"></a>Paraugs

Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.

Lai iegūtu papildu informāciju un piemērus par šīs funkcijas izmantošanu, skatiet [Secības elementu izpildes atlikšana ER formātos](er-defer-sequence-element.md#Example) un [XML elementu izpildes atlikšana ER formātos](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>Papildu resursi

[Datu apkopošanas funkcijas](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]