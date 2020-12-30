---
title: ER funkciju saraksts loģikas kategorijā
description: Šajā tēmā ir sniegta informācija par loģikas funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a37b3341b05fde1283a21a0c52faec26cd1a7030
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686194"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>ER funkciju saraksts loģikas kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) loģiskās funkcijas var izmantot, lai strādātu ar loģiskām vērtībām un veiktu vairāk nekā vienu salīdzinājumu vienā izteiksmē vai pārbaudītu vairākus nosacījumus. Šajā tēmā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija | Apraksts |
|----------|-------------|
| [And](er-functions-logical-and.md)                       | Šī funkcija atgriež *Būla* vērtību **TRUE**, ja visi norādītie nosacījumi ir patiesi. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [Pieteikums](er-functions-logical-case.md)                     | Šī funkcija novērtē norādītās izteiksmes vērtību pret norādītajām alternatīvajām opcijām un atgriež pirmās opcijas, kas ir vienāda ar norādītās izteiksmes vērtību, rezultātu. Pretējā gadījumā tas atgriež neobligātu noklusējuma rezultātu, ja noklusējuma rezultāts ir norādīts kā pēdējās funkcijas izsauktais arguments, pirms kura neatrodas opcija. Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība. |
| [Ja](er-functions-logical-if.md)                         | Šī funkcija atgriež pirmo norādīto vērtību, ja tiek izpildīts norādītais nosacījums. Pretējā gadījumā tiek atgriezta otrā norādītā vērtība. Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība. |
| [Ne](er-functions-logical-not.md)                       | Šī funkcija atgriež norādītā nosacījuma apgriezto loģisko vērtību kā *Būla* vērtību. |
| [Vai](er-functions-logical-or.md)                         | Šī funkcija atgriež *Būla* vērtību **FALSE**, ja visi norādītie nosacījumi ir nepatiesi. Šī funkcija atgriež *Būla* vērtību **TRUE**, ja jebkurš norādītais nosacījums ir patiess. |
| [ValueIn](er-functions-logical-valuein.md)               | Šī funkcija nosaka, vai norādītā ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai. Tas atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Šī funkcija nosaka, vai norādītā *Int64* vai *Integer* tipa ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai. Tas atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |


## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)
