---
title: LISTJOIN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTJOIN elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9346afc88adb89c08098f39a5fd1c2cb82f664af2244b8cafbbe8a4d2f516c6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755806"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER funkcija

[!include [banner](../includes/banner.md)]

`LISTJOIN` funkcija atgriež *Ierakstu saraksta* vērtību, kas pārstāv jaunu savienotu ierakstu sarakstu, kas ir izveidots no norādītiem argumentiem.

## <a name="syntax"></a>Sintakse

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumenti

`list 1`: *Ierakstu saraksts*

Atsauce uz datu avotu *Ieraksta saraksta* datu tipam. Šis ir obligāts arguments.

`list N`: *Ierakstu saraksts*

Atsauce uz datu avotu *Ieraksta saraksta* datu tipam. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Izveidotā saraksta struktūrā ir tikai tie lauki, kas ir parādīti visu ierakstu saraksta struktūrā, kas ir minēti argumentos.

## <a name="example"></a>Paraugs

Ievadiet datu avotu **Ieraksts 1** veidam `Container`. Šis datu avots satur šādus ligzdotus `Calculated field` tipa laukus:

- **Kods**: šis lauks satur izteiksmi, kas atgriež `String` tipa vērtību.
- **Daudzums**: šis lauks satur izteiksmi, kas atgriež `Real` tipa vērtību.

Tad ievadiet datu avotu **Ieraksts 2** veidam `Container`. Šis datu avots satur šādus ligzdotus `Calculated field` tipa laukus:

- **Daudzums**: šis lauks satur izteiksmi, kas atgriež `Real` tipa vērtību.
- **IsValid**: šis lauks satur izteiksmi, kas atgriež `Boolean` tipa vērtību.

![ER modeļa kartēšanas noformētāja lapa.](./media/er-functions-list-listjoin-image1.gif)

Šajā gadījumā izteiksme `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` atgriež jaunu sarakstu, kurā ir divi ieraksti.

![ER modeļa kartēšanas veidotāja lapa ar diviem ierakstiem.](./media/er-functions-list-listjoin-image2.gif)

Šī saraksta struktūra sastāv no viena **Daudzuma** lauka tipā `Real`, jo šis lauks ir vienīgais lauks, kas tiek parādīts katrā izsauktās funkcijas argumentā.

![ER modeļa kartēšanas veidotāja lapas summas lauks.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)

[Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
