---
title: ER funkciju saraksts loģikas kategorijā
description: Šajā rakstā ir sniegta informācija par loģiskajām funkcijām, kas tiek atbalstītas Elektronisko pārskatu veidošanai (ER).
author: NickSelin
ms.date: 02/11/2021
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
ms.openlocfilehash: 2361fa0df3fe60813e75c772134299ad948f3582
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888196"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>ER funkciju saraksts loģikas kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) loģiskās funkcijas var izmantot, lai strādātu ar loģiskām vērtībām un veiktu vairāk nekā vienu salīdzinājumu vienā izteiksmē vai pārbaudītu vairākus nosacījumus. Šajā rakstā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija | Apraksts |
|----------|-------------|
| [And](er-functions-logical-and.md)                       | Šī funkcija atgriež *Būla* vērtību **TRUE**, ja visi norādītie nosacījumi ir patiesi. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [Pieteikums](er-functions-logical-case.md)                     | Šī funkcija novērtē norādītās izteiksmes vērtību pret norādītajām alternatīvajām opcijām un atgriež pirmās opcijas, kas ir vienāda ar norādītās izteiksmes vērtību, rezultātu. Pretējā gadījumā tas atgriež neobligātu noklusējuma rezultātu, ja noklusējuma rezultāts ir norādīts kā pēdējās funkcijas izsauktais arguments, pirms kura neatrodas opcija. Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība. |
| [Ietver](er-functions-logical-contains.md)             | Šī funkcija nosaka, vai norādītā ievade satur norādīto tekstu. Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade satur norādīto tekstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [EndsWith](er-functions-logical-endswith.md)             | Šī funkcija nosaka, vai norādītā ievade beidzas ar norādīto tekstu. Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade beidzas ar norādīto tekstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [Ja](er-functions-logical-if.md)                         | Šī funkcija atgriež pirmo norādīto vērtību, ja tiek izpildīts norādītais nosacījums. Pretējā gadījumā tiek atgriezta otrā norādītā vērtība. Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība. |
| [Ne](er-functions-logical-not.md)                       | Šī funkcija atgriež norādītā nosacījuma apgriezto loģisko vērtību kā *Būla* vērtību. |
| [Vai](er-functions-logical-or.md)                         | Šī funkcija atgriež *Būla* vērtību **FALSE**, ja visi norādītie nosacījumi ir nepatiesi. Šī funkcija atgriež *Būla* vērtību **TRUE**, ja jebkurš norādītais nosacījums ir patiess. |
| [StartsWith](er-functions-logical-startswith.md)         | Šī funkcija nosaka, vai norādītā ievade sākas ar norādīto tekstu. Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade sākas ar norādīto tekstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [ValueIn](er-functions-logical-valuein.md)               | Šī funkcija nosaka, vai norādītā ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai. Tas atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Šī funkcija nosaka, vai norādītā *Int64* vai *Integer* tipa ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai. Tas atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |


## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]