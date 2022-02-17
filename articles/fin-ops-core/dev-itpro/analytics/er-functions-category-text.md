---
title: ER funkciju saraksts teksta kategorijā
description: Šajā tēmā ir sniegta informācija par teksta funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
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
ms.openlocfilehash: afe45bf1ff5c641346997aa4f32f3241dce2f0a2
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075504"
---
# <a name="list-of-er-functions-of-the-text-category"></a>ER funkciju saraksts teksta kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) teksta funkcijas var izmantot, lai izgūtu informāciju no un veiktu operācijas ar datu avotiem no datu veida *Virkne* Šajā tēmā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija | Apraksts |
|----------|-------------|
| [Char](er-functions-text-char.md) | Šī funkcija atgriež *Virknes* vērtību, kas parāda vienu rakstzīmi, uz kuru atsaucas norādītais unikoda numurs. |
| [Savienot](er-functions-text-concatenate.md) | Šī funkcija atgriež visas norādītās teksta virknes kā *Virknes* vērtību pēc tam, kad tās ir apvienotas vienā virknē. |
| [Formāts](er-functions-text-format.md) | Šī funkcija atgriež norādīto virkni kā *Virknes* vērtību, kas ir formatēta, aizstājot argumentu **%N** ar argumentu *N*. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Šī funkcija meklē konkrētu *Enum* vērtību norādītajā uzskaitījuma datu avotā, izmantojot uzskaitījuma nosaukumu, kas ir norādīts kā *Virknes* vērtība. Ja tiek tiek atrasta *Enum* vērtība, funkcija to atgriež. |
| [GetLabelText](er-functions-text-getlabeltext.md) | Šī funkcija meklē noteiktu etiķeti, lai atgrieztu a *[Stīga](er-formula-supported-data-types-primitive.md#string)* vērtība, kas apzīmē norādītās etiķetes tulkojumu norādītajā valodā. |
| [GuidValue](er-functions-text-guidvalue.md) | Šī funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Šī funkcija parsē datus formātā JavaScript Object Notation (JSON), kuriem piekļūst pa norādīto ceļu un izgūst skalāru vērtību, kas ir balstīta uz norādīto ID. Pēc tam tā atgriež izvērsto skalāro vērtību kā *Virknes* vērtību. |
| [Pa kreisi](er-functions-text-left.md) | Šī funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes sākuma. |
| [Len](er-functions-text-len.md) | Šī funkcija atgriež *Vesela skaitļa* vērtību, kas norāda norādītu zīmju skaitu norādītajā virknē. |
| [Lower](er-functions-text-lower.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību pēc tam, kad tā ir konvertēta mazajos burtos. |
| [Mid](er-functions-text-mid.md) | Šī funkcija atgriež *[Virknes](er-formula-supported-data-types-primitive.md#string)* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes, sākot no norādītas pozīcijas. |
| [NewGUID](er-functions-text-newguid.md) | Šī funkcija atgriež jaunizveidotu *[GUID](er-formula-supported-data-types-primitive.md#guid)* vērtību. |
| [NumberFormat](er-functions-text-numberformat.md) | Šī funkcija atgriež *Virknes* vērtību, kas norādīto skaitu uzrāda norādītajā formātā un pēc izvēles norādītajā kultūrā. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Šī funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tas ir uzrakstīts (tas ir, konvertēts teksta virknēs) norādītajā valodā. |
| [PadLeft](er-functions-text-padleft.md) | Šī funkcija atgriež norādīta garuma *Virknes* vērtību , kurā norādītās virknes sākumā ir ievadīta viena vai vairākas norādīto rakstzīmju instances. |
| [QrCode](er-functions-text-qrcode.md) | Šī funkcija atgriež *Konteinera* vērtību, kas parāda ātrās atbildes kodu (QR koda) attēlu norādītajai virknei binārā formātā. |
| [Aizvietot](er-functions-text-replace.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, ja visa vai daļa no tās ir aizstāta ar citu virkni. |
| [Pa labi](er-functions-text-right.md) | Šī funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes beigām. |
| [Teksts](er-functions-text-text.md) | Šī funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tā ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās programmas instances servera lokalizācijas iestatījumiem. |
| [Tulkot](er-functions-text-translate.md) | Šī funkcija atgriež *Virknes* vērtību, kas satur noteiktā teksta aizstāšanas rezultātu ar rakstzīmēm citai sniegtai rakstzīmju kopai. |
| [Trim](er-functions-text-trim.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, kam ir aprautas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem. |
| [Upper](er-functions-text-upper.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību pēc tam, kad tā ir konvertēta lielajos burtos. |

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
