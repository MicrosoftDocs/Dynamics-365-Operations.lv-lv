---
title: ER funkciju saraksts datuma un laika kategorijā
description: Šajā tēmā ir sniegta informācija par datuma un laika funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: 706331eaadf602aba46463fdcfc0d38f1fc94e08
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647267"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>ER funkciju saraksts datuma un laika kategorijā

[!include [banner](../includes/banner.md)]

Elektroniskā pārskata (ER) datuma un laika funkcijas var izmantot, lai iegūtu informāciju no datuma un laika vērtībām un veiktu operācijas ar tām. Šajā tēmā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija | Apraksts |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Šī funkcija atgriež *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* vērtību, kas ir norādītais dienu skaits pirms vai pēc norādītā sākuma datuma. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā datuma/laika vērtības vienā laika joslā uz datuma/laika vērtību citā laika joslā. |
| [DateFormat](er-functions-datetime-dateformat.md) | Šī funkcija atgriež *[Virknes](er-formula-supported-data-types-primitive.md#string)* vērtību, kas norādīto datuma vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā kultūrā. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Šī funkcija atgriež *Virknes* vērtību, kas norādīto datuma/laika vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā kultūrā. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma/laika vērtībai. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā datuma vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]). |
| [DateValue:](er-functions-datetime-datevalue.md) | Šī funkcija atgriež *Datuma* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma/laika vērtībai. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Šī funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no 1. janvāra līdz norādītajam datumam. |
| [Dienas](er-functions-datetime-days.md) | Šī funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no viena norādītā datuma līdz otram norādītajam datumam. |
| [Now](er-functions-datetime-now.md) | Šī funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu un laiku. |
| [NullDate](er-functions-datetime-nulldate.md) | Šī funkcija atgriež *Datuma* vērtību, kas apzīmē **nulles** datumu (1900. gada 1. janvāris). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Šī funkcija atgriež *DateTime* vērtību, kas apzīmē **nulles** datuma/laika vērtību (1900. gada 1. janvāris) universālajā koordinētajā laikā. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Šī funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu un laiku. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Šī funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu. |
| [Šodien](er-functions-datetime-today.md) | Šī funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu. |

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
