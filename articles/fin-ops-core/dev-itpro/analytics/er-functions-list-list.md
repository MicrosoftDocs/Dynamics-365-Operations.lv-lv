---
title: LIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LIST elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 50cb8858301c030df07ad4af9fe2a9513f41fead
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750416"
---
# <a name="list-er-function"></a>LIST ER funkcija

[!include [banner](../includes/banner.md)]

`LIST` funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no jauna ierakstu saraksta, kas ir izveidots no norādītiem argumentiem.

## <a name="syntax"></a>Sintakse

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumenti

`record 1`: *Konteiners (ieraksts)*

Atsauce uz datu avotu *Ieraksta* datu tipam. Šis arguments ir obligāts.

`record N`: *Konteiners (ieraksts)*

Atsauce uz datu avotu *Ieraksta* datu tipam. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Izveidotā saraksta struktūrā ir tikai tie lauki, kas ir parādīti visu ierakstu struktūrā, kas ir minēti argumentos.

## <a name="example"></a>Paraugs

Ievadiet datu avotu **Ieraksts 1** veidam *Konteiners*. Šis datu avots satur šādus ligzdotus *Aprēķinātā lauka* tipa laukus:

- **Kods:** šis lauks satur izteiksmi, kas atgriež *Virknes* tipa vērtību.
- **Daudzums:** šis lauks satur izteiksmi, kas atgriež *Reālā skaitļa* tipa vērtību.

Tad ievadiet datu avotu **Ieraksts 2** veidam *Konteiners*. Šis datu avots satur šādus ligzdotus *Aprēķinātā lauka* tipa laukus:

- **Daudzums:** šis lauks satur izteiksmi, kas atgriež *Reālā skaitļa* tipa vērtību.
- **IsValid:** šis lauks satur izteiksmi, kas atgriež *Būla* tipa vērtību.

Šajā gadījumā izteiksme `LIST('Record 1', 'Record 2')` atgriež jaunu sarakstu, kurā ir divi ieraksti. Šī saraksta struktūra sastāv no viena **Daudzuma** lauka tipā *Reāls skaitlis*, jo šis lauks ir vienīgais lauks, kas tiek parādīts katrā izsauktās funkcijas argumentā.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]