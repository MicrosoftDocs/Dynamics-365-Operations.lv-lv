---
title: ER funkciju saraksts veida konvertēšanas kategorijā
description: Šajā rakstā ir sniegta informācija par pārvēršanas funkcijām, kas tiek atbalstītas Elektronisko pārskatu veidošanai (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 37516ced402e0204ebd09d5b175ff56b040b9043
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889319"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>ER funkciju saraksts veida konvertēšanas kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko atskaišu veidošanas (ER) veida konvertēšanas funkcijas var izmantot, lai konvertētu vērtības starp veidiem. Šajā rakstā ir sniegts šo funkciju kopsavilkums.

## <a name="type-conversion-functions"></a>Veida pārveidošanas funkcijas

| Funkcija | Apraksts |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Šī funkcija atgriež *Int64* vērtību, kas apzīmē norādīto virkni. |
| [IntValue](er-functions-conversion-intvalue.md)       | Šī funkcija atgriež *Int* vērtību, kas apzīmē norādīto virkni. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Šī funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības. Konvertēšanas laikā tiek uzskatīti norādītie decimālo un ciparu grupēšanas atdalītāji. |
| [Vērtība](er-functions-conversion-value.md)             | Šī funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības. |

## <a name="type-conversion-functions-in-the-container-category"></a>Veida konvertēšanas funkcijas konteinera kategorijā

Šajā tabulā aprakstītas veida konvertēšanas funkcijas [konteinera](er-functions-category-container.md) kategorijā.

| Funkcija | Apraksts |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Šī funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *Konteiners*. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Veida konvertēšanas funkcijas datuma un laika kategorijā

Šajā tabulā aprakstītas veida konvertēšanas funkcijas [datuma un laika kategorijā](er-functions-category-datetime.md).

| Funkcija | Apraksts |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no dotās *Virknes* vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma/laika vērtībai. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā *Datuma* vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]). |
| [DateValue:](er-functions-datetime-datevalue.md)           | Šī funkcija atgriež *Datuma* vērtību, kas tiek konvertēta no dotās *Virknes* vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma vērtībai. |

## <a name="type-conversion-functions-in-the-list-category"></a>Veida konvertēšanas funkcijas saraksta kategorijā

Šajā tabulā aprakstītas veida konvertēšanas funkcijas [saraksta kategorijā](er-functions-category-list.md).

| Funkcija | Apraksts |
|----------|-------------|
| [Saraksts](er-functions-list-list.md)                 | Šī funkcija atgriež jaunu *Ierakstu saraksta* vērtību kā jaunu sarakstu, kas ir izveidots no norādītiem *Konteinera (ieraksta)* veida argumentiem. |
| [ListOfFields](er-functions-list-listoffields.md) | Šī funkcija atgriež *Ierakstu saraksta* vērtību, kas tiek izveidota, pamatojoties uz norādītā *Uzskaitījuma* vai *Konteinera (ieraksta)* veida argumenta struktūru. |
| [Sadalīt](er-functions-list-split.md)               | Šī funkcija sadala norādīto ievades *Virknes* vērtību apakšvirknēs un atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību. |
| [StringJoin](er-functions-list-stringjoin.md)     | Šī funkcija atgriež *Virknes* vērtību, kas sastāv no norādītā *Ierakstu saraksta* vērtībā norādītā lauka savirknētajām vērtībām. Vērtības var atdalīt ar norādīto norobežotāju. |

## <a name="type-conversion-functions-in-the-text-category"></a>Veida konvertēšanas funkcijas teksta kategorijā

Šajā tabulā aprakstītas veida konvertēšanas funkcijas [teksta kategorijā](er-functions-category-text.md).

| Funkcija | Apraksts |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē vienu rakstzīmi, uz kuru atsaucas norādītais unikoda numurs. |
| [GuidValue](er-functions-text-guidvalue.md)       | Šī funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē skaitu uzrāda norādītajā formātā un pēc izvēles norādītajā kultūrā. |
| [QrCode](er-functions-text-qrcode.md)             | Šī funkcija atgriež *Konteinera* vērtību, kas parāda ātrās atbildes kodu (QR koda) attēlu norādītajai virknei binārā formātā. |
| [Teksts](er-functions-text-text.md)                 | Šī funkcija atgriež *Virknes* vērtību, kas apzīmē norādīto skaitli pēc tam, kad tā ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās programmas instances servera lokalizācijas iestatījumiem. |

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]