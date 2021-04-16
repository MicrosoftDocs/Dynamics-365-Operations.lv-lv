---
title: ER funkciju saraksts datu vākšanas kategorijā
description: Šajā tēmā ir sniegta informācija par datu apkopošanas funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 31b5e7b08a3de77d461fff5e42164975e53dfe1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748067"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>ER funkciju saraksts datu vākšanas kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) datu apkopošanas funkcijas tiek izmantotas, lai veiktu skaitīšanu un summēšanu ER formātā, kas tiek palaists, pamatojoties uz datiem par izvadi, kas jau ir ģenerēti **teksta** vai **XML** formātā. Šī pieeja tiek izmantota, lai palīdzētu uzlabot izpildīto ER formāta veiktspēju, lai ģenerētos dokumentos ievadītu kopsummu vērtības, un citiem nolūkiem. Šajā tēmā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija | Apraksts |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Šī funkcija atgriež vērtību *Ierakstu saraksts*, kurā ir to vērtību saraksts, ko atgrieza formāta elementu rekvizīts **Ievāktā datu atslēgas vērtība** un kas tika savākts, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā, un kas atbilst norādītajiem nosacījumiem. Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības. |
| [CountIF](er-functions-datacollection-countif.md) | Šī funkcija atgriež vērtību *Vesels skaitlis*, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam. Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības. |
| [CountIFs](er-functions-datacollection-countifs.md) | Šī funkcija atgriež vērtību *Vesels skaitlis*, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem. Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Šī funkcija atgriež vērtību *Virkne*, kas apzīmē pašreizējā ER formāta elementa nosaukumu. |
| [SumIF](er-functions-datacollection-sumif.md) | Šī funkcija atgriež vērtību *Reāls skaitlis*, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam. Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Šī funkcija atgriež vērtību *Reāls skaitlis*, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem. Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības. |

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]