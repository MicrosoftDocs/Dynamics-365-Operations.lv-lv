---
title: ATKĀRTOT ER funkciju
description: Šajā rakstā ir sniegta informācija, kā izmantot funkciju REPEAT Electronic Reporting (ER).
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220725"
---
# <a name="repeat-er-function"></a>ATKĀRTOT ER funkciju

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funkcija `REPEAT` veido ierakstu, kas satur lauku, kura vērtība atbilst norādītajai ievadei. Tad tā atgriež jaunu *ierakstu sarakstu*, kas tiek atkārtots noteiktu reižu skaitu.

## <a name="syntax"></a>Sintakse

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumenti

`item`: jebkurš atbalstītais [primitīvais](er-formula-supported-data-types-primitive.md) vai kompozītais [datu](er-formula-supported-data-types-composite.md) tips.

Atkārtoto vērtību.

`number`: *Vesels skaitlis*

Atkārtošanu skaits.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Atgriezto atkārtoto ierakstu saraksts atklāj sekojošos laukus:

- Norādītā vērtība (`Item` lauks)
- Pašreizējais ieraksta indekss (`Number` lauks)

> [!NOTE]
> Tā kā šai funkcijai tiek izmantota vienreizējā numerācija, `Number`**iegūtā saraksta pirmajam ierakstam lauka vērtība ir 1**.

Šo funkciju [var izmantot, lai reizinātu esošos datus, tādējādi jūs varat veikt elektronisko pārskatu (ER)](general-electronic-reporting.md)[risinājumu veiktspēju un apjoma pārbaudi, izmantojot Regression komplekta automatizācijas rīku (RSAT).](../perf-test/rsat/rsat-overview.md)

## <a name="example"></a>Paraugs

Jūs vēlaties ģenerēt dokumentu XML formātā `Party`, kam jāietver tik DAUDZ XML elementu, cik norādīts datu ievades laukā izpildlaika dialoglodziņā, pirms sākas ER formāta izpilde.

Šajā ilustrācijā parādīts ER [formāts](er-overview-components.md#format-component). Šajā formātā viens XML elements tiek `Party` pievienots, lai atklātu vienas puses rekvizītus.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Nākamajā ilustrācijā parādīti šādi konfigurētie datu avoti:

- Datu `Party` avots, kas pārstāv vienu pusi. Lauks `Party.Value` tiek izmantots, lai atklātu viena teksta vērtību.
- Datu `NumberOfRepeats`[avots,](er-user-input-parameter-data-sources.md) ko izmanto, lai piedāvātu datu ievades lauku dialoglodziņā izpildlaika laikā, lai varētu norādīt pušu skaitu, kas jāievada ģenerētajā dokumentā.
- Datu `Party2` avots, kas atkārto `Party` ierakstu, cik reižu norādīts datu `NumberOfRepeats` avotā.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Nākamajā ilustrācijā ir attēloti rediģējama ER formāta datu saistīumi, kas izveidoti izvadei XML formātā. Šis rezultāts kā uzskaitījuma zari uzdāvā atsevišķas puses.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Šajā attēlā parādīts rezultāts, kad tiek palaists noformētais formāts `NumberOfRepeats` un datu avota vērtība ir norādīta kā **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
