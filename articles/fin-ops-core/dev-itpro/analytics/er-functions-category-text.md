---
title: ER funkciju saraksts teksta kategorijā
description: Šajā tēmā ir sniegta informācija par teksta funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f519d242fe74196b0d12bdc9df4f1b4b0e585752
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916618"
---
# <a name="list-of-er-functions-of-the-text-category"></a>ER funkciju saraksts teksta kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) teksta funkcijas var izmantot, lai izgūtu informāciju no un veiktu operācijas ar datu avotiem no datu veida *Virkne* Šajā tēmā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija | Apraksts |
|----------|-------------|
| [Char](er-functions-text-char.md) | Šī funkcija atgriež *Virknes* vērtību, kas parāda vienu rakstzīmi, uz kuru atsaucas norādītais unikoda numurs. |
| [Savienot](er-functions-text-concatenate.md) | Šī funkcija atgriež visas norādītās teksta virknes kā *Virknes* vērtību pēc tam, kad tās ir apvienotas vienā virknē. |
| [Formāts](er-functions-text-format.md) | Šī funkcija atgriež norādīto virkni kā *Virknes* vērtību, kas ir formatēta, aizstājot argumentu  **%N** ar argumentu *N*. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Šī funkcija meklē konkrētu *Enum* vērtību norādītajā uzskaitījuma datu avotā, izmantojot uzskaitījuma nosaukumu, kas ir norādīts kā *Virknes* vērtība. Ja tiek tiek atrasta *Enum* vērtība, funkcija to atgriež. |
| [GuidValue](er-functions-text-guidvalue.md) | Šī funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Šī funkcija parsē datus formātā JavaScript Object Notation (JSON), kuriem piekļūst pa norādīto ceļu un izgūst skalāru vērtību, kas ir balstīta uz norādīto ID. Pēc tam tā atgriež izvērsto skalāro vērtību kā *Virknes* vērtību. |
| [Pa kreisi](er-functions-text-left.md) | Šī funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes sākuma. |
| [Len](er-functions-text-len.md) | Šī funkcija atgriež *Vesela skaitļa* vērtību, kas norāda norādītu zīmju skaitu norādītajā virknē. |
| [Lower](er-functions-text-lower.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību pēc tam, kad tā ir konvertēta mazajos burtos. |
| [Mid](er-functions-text-mid.md) | Šī funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes, sākot no norādītas pozīcijas. |
| [NumberFormat](er-functions-text-numberformat.md) | Šī funkcija atgriež *Virknes* vērtību, kas norādīto skaitu uzrāda norādītajā formātā un pēc izvēles norādītajā kultūrā. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Šī funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tas ir uzrakstīts (tas ir, konvertēts teksta virknēs) norādītajā valodā. |
| [PadLeft](er-functions-text-padleft.md) | Šī funkcija atgriež norādīta garuma *Virknes* vērtību , kurā norādītās virknes sākumā ir ievadīta viena vai vairākas norādīto rakstzīmju instances. |
| [QrCode](er-functions-text-qrcode.md) | Šī funkcija atgriež *Konteinera* vērtību, kas parāda ātrās atbildes kodu (QR koda) attēlu norādītajai virknei binārā formātā. |
| [Aizvietot](er-functions-text-replace.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, ja visa vai daļa no tās ir aizstāta ar citu virkni. |
| [Pa labi](er-functions-text-right.md) | Šī funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes beigām. |
| [Teksts](er-functions-text-text.md) | Šī funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tā ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās programmas instances servera lokalizācijas iestatījumiem. |
| [Tulkot](er-functions-text-translate.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, ja visa vai daļa no tās ir aizstāta ar citu virkni. |
| [Trim](er-functions-text-trim.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, kam ir aprautas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem. |
| [Upper](er-functions-text-upper.md) | Šī funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību pēc tam, kad tā ir konvertēta lielajos burtos. |

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)
